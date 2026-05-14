# Interopérabilité avec les skills frères

Ce fichier décrit comment le Miroir Trans-échelle invoque les skills `fractales-du-destin` et `signaux-du-futur`, gère les cas où ils sont absents, et préserve la cohérence des sorties.

---

## Architecture d'orchestration

Le Miroir Trans-échelle est un **agent orchestrateur**. Il ne réimplémente pas la logique des skills frères ; il les **invoque** quand ils sont présents, et bascule en **mode compact** quand ils ne le sont pas.

```
                    ┌──────────────────────────────┐
                    │  MIROIR TRANS-ÉCHELLE        │
                    │  (orchestrateur + synthèse)  │
                    └──────────┬───────────────────┘
                               │
                ┌──────────────┼──────────────┐
                │              │              │
                ▼              ▼              ▼
        ┌─────────────┐ ┌─────────────┐ ┌─────────────┐
        │  FRACTALES  │ │   SIGNAUX   │ │ CARTE DE    │
        │  DU DESTIN  │ │   DU FUTUR  │ │ RÉSONANCE   │
        │   (P1)      │ │   (P2)      │ │   (P3)      │
        └─────────────┘ └─────────────┘ └─────────────┘
```

---

## Détection des skills frères

À l'activation du Miroir Trans-échelle, l'agent vérifie la présence des skills frères dans l'environnement :

1. **Détection automatique** : si Claude annonce dans `<available_skills>` la présence de `fractales-du-destin` ou `signaux-du-futur`, l'orchestration utilise le mode étendu.
2. **Détection par essai** : si les `available_skills` ne sont pas explicites, l'agent peut tenter une invocation et basculer en mode compact si elle échoue.
3. **Déclaration utilisateur** : l'utilisateur peut indiquer en début de session quels skills sont installés (`"j'ai installé fractales-du-destin et signaux-du-futur"`).

---

## Invocation du skill `fractales-du-destin` (Passe 1)

### Formulation d'appel

L'agent invoque Fractales du Destin avec une formulation standardisée :

> **Active Fractales du Destin sur la situation suivante :**
>
> [Résumé en 2-3 phrases de la situation soumise par l'utilisateur — neutralisé pour ne pas biaiser le tirage]
>
> **Format demandé** :
> - Tirage complet (5 cartes : Nœud · Bifurcation · Résonance · Ancrage · Miroir)
> - Double voix activée (Oracle + Gardien)
> - Phrase symbolique FdD finale
> - Pas de prédiction, pas de psychologisation
> - Ton suggestif, ouvert

### Récupération et intégration

L'agent reprend tel quel le tirage produit par Fractales et le **place dans la sortie sous l'en-tête P1**, sans altération. Il ne reformule pas, ne résume pas, ne psychologise pas.

### Extraction des éléments pour la P3

Pour alimenter le tableau croisé, l'agent extrait :
- Les **archétypes principaux** activés (par carte ou par famille)
- Les **motifs récurrents** identifiés par le Gardien
- La **Phrase symbolique FdD** in extenso (sa formulation est porteuse)
- Les **angles d'ouverture** soulevés (questions, perspectives)

Ces éléments deviennent les "Éléments P1" du tableau de résonance.

---

## Invocation du skill `signaux-du-futur` (Passe 2)

### Formulation d'appel

L'agent invoque Signaux du Futur avec une formulation standardisée :

> **Active OSINT-Prospective sur le dossier suivant :**
>
> [Résumé + corpus disponible : presse, dépêches, données ouvertes, contexte]
>
> **Format demandé** :
> - Méthodologie 11 étapes (au minimum : question d'incertitude, signaux faibles, 3 hypothèses concurrentes, 3 scénarios, indicateurs de bascule)
> - Contrôle des biais explicité
> - Aucune cible nommée pour action — surveillance analytique uniquement
> - Posture analyste : sobre, traçable, falsifiable

### Récupération et intégration

L'agent reprend la sortie OSINT et la **place sous l'en-tête P2**, sans altération.

### Extraction des éléments pour la P3

Pour alimenter le tableau croisé, l'agent extrait :
- La **question d'incertitude** principale
- Les **signaux faibles** repérés (chacun avec sa source et son degré de fiabilité)
- Les **hypothèses concurrentes** H1/H2/H3
- Les **indicateurs de bascule**
- Les **biais surveillés**

Ces éléments deviennent les "Éléments P2" du tableau de résonance.

---

## Mode compact (fallback)

### Quand l'activer

- Skill frère absent de l'environnement.
- Skill frère présent mais retourne une sortie incomplète ou vide.
- Demande utilisateur explicite d'une "version rapide".

### Versions compactes intégrées

Les versions compactes des deux pipelines sont décrites dans `pipeline-3-passes.md`. Elles sont volontairement **réduites mais fidèles** :
- Compact P1 : 4 étapes (archétypes, motifs, Phrase FdD, angles d'ouverture)
- Compact P2 : 5 étapes (question, signaux, 3 hypothèses, 3 scénarios, biais)

### Signalement à l'utilisateur

Quand le mode compact est activé, l'agent l'indique explicitement dans la sortie :

```
[Mode compact activé pour la passe X — skill frère 'nom-du-skill' indisponible]
```

Et propose en fin de sortie :

> *Pour une lecture étendue, considérer l'installation du skill `nom-du-skill` depuis le dépôt correspondant.*

---

## Gestion des conflits de version

Si les skills frères évoluent (nouvelles familles d'arcanes, nouvelle méthodologie OSINT), le Miroir Trans-échelle peut hériter de leurs sorties **sans modification** — il extrait ce dont il a besoin pour la P3, sans présupposer la structure exacte des sous-passes.

**Règle de robustesse** : l'extraction pour la P3 fonctionne tant que les sorties des skills frères contiennent :
- (P1) au moins un archétype identifié + une phrase symbolique
- (P2) au moins une hypothèse explicite + un signal faible identifié

En dessous de ce minimum, basculer en mode compact et notifier.

---

## Préservation de l'autonomie des skills frères

**Principe directeur** : le Miroir Trans-échelle ne **modifie jamais** les sorties des skills frères. Il les **agrège**.

Cela signifie :
- L'agent ne reformule pas la Phrase FdD pour la rendre "plus analytique".
- L'agent ne reformule pas une hypothèse OSINT pour la rendre "plus poétique".
- Chaque registre garde sa langue, sa tonalité, sa rigueur propre.

C'est cette **non-contamination** qui rend la P3 légitime : elle compare des productions intactes, pas des productions déjà alignées.

---

## Cas particulier : invocation séquentielle vs parallèle

### Séquence recommandée

Par défaut, l'agent exécute **P1 avant P2**. Pourquoi ?

1. **Asymétrie temporelle** : P1 est plus rapide, P2 est plus coûteux. Mieux vaut ouvrir avant de structurer.
2. **Évite la contamination analytique** : si P2 vient en premier, la lecture archétypale peut être biaisée par les hypothèses formulées.
3. **Cohérence avec le contexte de découverte → justification** (Reichenbach) : on génère avant de valider.

### Exception : situation à matière analytique forte

Si l'utilisateur soumet un **gros corpus factuel** (presse, données, rapports), il peut être préférable d'inverser :
- P2 d'abord pour structurer le matériau
- P1 ensuite, sur le matériau déjà cartographié

Dans ce cas, l'agent **annonce l'inversion** : *"Inversion P2→P1 activée en raison du volume factuel — la lecture symbolique opérera sur la structure analytique produite."*

---

## Variantes de profondeur

L'utilisateur peut demander des **versions plus ou moins profondes** du Miroir :

- **Express** (5-10 min) : P1 compact + P2 compact + P3 résumée (3 lignes de tableau, synthèse en 3 puces).
- **Standard** (15-30 min) : pipeline complet tel que décrit dans SKILL.md.
- **Approfondi** (par itérations) : P1 + P2 complets, P3 sur plusieurs itérations avec retour utilisateur entre chaque, exploration séparée des dissonances.

L'agent demande en début de session si nécessaire :

> *"Souhaites-tu une lecture express, standard ou approfondie ?"*

---

## Compatibilité avec les autres skills de l'écosystème

| Skill | Compatibilité | Note |
|-------|---------------|------|
| `hacking-narratif` | ★★★★★ | Pipeline tripartite proche — peut être invoqué pour Mode B (stratégique) en complément de P2 |
| `metalangage-resonances` | ★★★★☆ | Fournit le cadre théorique de la "résonance" — référence légitime |
| `langage-ecriture-realite` | ★★★★☆ | Instruction `RESONE` peut être invoquée pour formaliser la P3 |
| `tcai` | ★★★☆☆ | Compatible mais à manier avec précaution — mode acausal, à isoler de P2 |
| `miroir-des-paradigmes` | ★★☆☆☆ | Domaine personnel — peu pertinent pour des situations stratégiques |

---

## Notes d'implémentation

- L'agent **n'a pas besoin** de persister l'état entre les passes. Chaque passe produit une sortie auto-suffisante qui est ensuite reprise pour la P3.
- En cas d'environnement où Claude ne peut pas "appeler" un autre skill comme une fonction (pas de tool call dédié), l'invocation se fait par **réécriture du contexte** : l'agent incorpore mentalement les instructions du skill frère et produit la sortie au format attendu.
- L'utilisateur peut toujours **inspecter** chaque sous-sortie indépendamment : la traçabilité est totale.
