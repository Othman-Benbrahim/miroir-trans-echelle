# Mode P3 itératif — Carte de résonance multi-cycles

Ce fichier décrit le **mode approfondi** du Miroir Trans-échelle, dans lequel la Passe 3 n'est pas produite en une seule itération, mais construite **par cycles successifs** avec retour utilisateur entre chaque.

C'est le mode adapté aux dossiers complexes — multi-acteurs, multi-échelles, riches en dissonances — pour lesquels une seule carte de résonance laisse trop d'éléments en suspens.

---

## Quand activer le mode itératif

Le mode itératif s'active automatiquement (ou sur demande utilisateur) quand au moins **deux** des critères suivants sont réunis :

| Critère | Indicateur |
|---------|-----------|
| **Multi-acteurs** | Le dossier implique plus de 4 acteurs avec rôles distincts |
| **Multi-échelles** | Présence simultanée de dynamiques micro (individus), méso (organisations), macro (structures) |
| **Multi-temporalités** | Échelles temporelles hétérogènes (court terme + cycle long) qui interagissent |
| **Densité de dissonances** | Plus de 3 dissonances identifiées en P3 standard |
| **Densité d'angles morts** | Plus de 3 angles morts (symétriques ou asymétriques) en P3 standard |
| **Demande utilisateur** | Mention explicite : *"approfondir"*, *"creuser"*, *"itératif"*, *"par cycles"* |

L'activation est annoncée explicitement à l'utilisateur :

> *"La complexité du dossier suggère un traitement itératif en plusieurs cycles. Souhaites-tu procéder ainsi (durée estimée : 60-90 min avec retours), ou conserver une carte unique ?"*

---

## Architecture des cycles

Le mode itératif comprend **3 à 4 cycles maximum**. Au-delà, le rendement marginal devient négatif et la "saturation analytique" guette.

```
┌────────────────────────────────────────────────────────────────┐
│  CYCLE 1 : CARTE INITIALE                                        │
│  ──────────────────────────                                       │
│  Exécution standard du pipeline P1 + P2 + P3                      │
│  → Identification des points clés : convergences fortes,          │
│    dissonances saillantes, angles morts                           │
│  → Retour utilisateur : que veux-tu creuser ?                     │
└──────────────────────┬─────────────────────────────────────────┘
                       │
                       ▼
┌────────────────────────────────────────────────────────────────┐
│  CYCLE 2 : APPROFONDISSEMENT DES DISSONANCES                     │
│  ─────────────────────────────────────────────                    │
│  Pour chaque dissonance retenue par l'utilisateur :               │
│  → P1 ciblée (relecture symbolique focalisée)                     │
│  → P2 ciblée (collecte de signaux additionnels)                   │
│  → Mini-carte de dissonance                                       │
│  → Retour utilisateur : quoi confirmer, quoi écarter ?            │
└──────────────────────┬─────────────────────────────────────────┘
                       │
                       ▼
┌────────────────────────────────────────────────────────────────┐
│  CYCLE 3 : INTÉGRATION DES ANGLES MORTS                          │
│  ───────────────────────────────────────                          │
│  Pour chaque angle mort retenu :                                  │
│  → Élargissement de la grille manquante                           │
│    (archétypes étendus, signaux complémentaires, autre source)    │
│  → Mini-carte d'intégration                                       │
│  → Retour utilisateur : quels éléments nouveaux ?                 │
└──────────────────────┬─────────────────────────────────────────┘
                       │
                       ▼
┌────────────────────────────────────────────────────────────────┐
│  CYCLE 4 : SYNTHÈSE TRANS-CYCLES (optionnel)                     │
│  ─────────────────────────────────────────                        │
│  Compilation des cartes secondaires en une carte unique           │
│  enrichie. Identification des éléments stables vs émergents.      │
│  Rapport final structuré.                                         │
└────────────────────────────────────────────────────────────────┘
```

---

## Détail de chaque cycle

### CYCLE 1 — Carte initiale (établir la grille)

**But** : produire la première carte de résonance et identifier les *points d'entrée* pour les cycles suivants.

**Procédure** : exécution standard du pipeline (P1 + P2 + P3 telles que décrites dans SKILL.md).

**Output spécifique au mode itératif** : en plus de la carte standard, l'agent produit en fin de cycle 1 une **section "Points d'entrée"** :

```
═══════════════════════════════════════════════
POINTS D'ENTRÉE POUR LES CYCLES SUIVANTS
═══════════════════════════════════════════════

DISSONANCES À CREUSER (par ordre de priorité) :
  D1 — [description courte] [pourquoi prioritaire]
  D2 — [description] [pourquoi]
  D3 — [description] [pourquoi]

ANGLES MORTS À INTÉGRER (par ordre de priorité) :
  A1 — [vu par P1 seul, manquant en P2] [comment combler]
  A2 — [vu par P2 seul, manquant en P1] [comment combler]
  A3 — [...]

QUESTION POUR L'UTILISATEUR :
  Sur quel(s) point(s) souhaites-tu approfondir ?
  (Tu peux en choisir 1 à 3 par cycle.)
```

### CYCLE 2 — Approfondissement des dissonances

**But** : transformer chaque dissonance retenue en analyse autonome, pour comprendre *pourquoi* les deux registres divergent.

**Procédure** pour chaque dissonance Dn retenue :

1. **Reformuler la dissonance** comme question d'investigation :
   - *"Pourquoi [archétype X] (P1) et [hypothèse Y] (P2) divergent-ils ?"*
   - *"Que cache cette divergence ?"*

2. **P1 ciblée** : relire la dimension symbolique avec un focus sur la dissonance.
   - Inviter d'autres archétypes (notamment du répertoire étendu) qui pourraient *concilier* ou *radicaliser* la lecture initiale.
   - Reformuler la Phrase FdD spécifiquement sur la dissonance.

3. **P2 ciblée** : collecter des signaux faibles supplémentaires qui éclairent la dissonance.
   - Élargir la grille de capteurs : sources additionnelles, indicateurs subtils, ce qui n'avait pas été collecté.
   - Tester si la dissonance résulte d'un manque de données ou d'une vraie tension structurelle.

4. **Mini-carte de dissonance** : un tableau croisé focalisé sur cette seule dissonance, qui peut produire trois résultats :
   - **Résolution** : la dissonance se dissout (l'un des registres était sous-informé).
   - **Confirmation** : la dissonance est réelle et structurelle (porteuse d'information).
   - **Reformulation** : la dissonance change de nature (ce n'était pas ce qu'on croyait).

**Output** : pour chaque dissonance creusée, une mini-carte + un statut clair (résolu / confirmé / reformulé).

### CYCLE 3 — Intégration des angles morts

**But** : enrichir la grille manquante de l'un des registres.

**Procédure** pour chaque angle mort An retenu :

#### Si An est un angle mort *analytique* (vu par P1 seul, manquant en P2)

L'agent élargit P2 :
- Source de données complémentaires (presse spécialisée, rapports académiques, données ouvertes sectorielles).
- Indicateurs alternatifs qui pourraient capter la dimension symbolique vue.
- Hypothèses nouvelles construites à partir de l'archétype identifié.

#### Si An est un angle mort *symbolique* (vu par P2 seul, manquant en P1)

L'agent élargit P1 :
- Mobilisation du **répertoire archétypal étendu** (`rdm-archetypes-etendus.md`) pour trouver une lecture qui capte le signal observé.
- Construction d'une nouvelle Phrase FdD focalisée sur ce signal.
- Ouverture éventuelle vers une tradition culturelle pertinente au dossier.

**Mini-carte d'intégration** : un tableau qui montre comment l'élément précédemment isolé trouve maintenant un correspondant dans l'autre registre, **ou** qui confirme qu'il reste isolé (information précieuse en soi).

### CYCLE 4 — Synthèse trans-cycles (optionnel)

**But** : compiler tout le travail des cycles précédents en une carte unique enrichie et un rapport final.

**Procédure** :

1. **Compilation** des cartes secondaires en une carte de résonance enrichie.
2. **Tri** des éléments en trois catégories :
   - **Stables** : éléments confirmés à travers les cycles (haute robustesse).
   - **Émergents** : éléments apparus dans les cycles 2-3 qui n'étaient pas dans la carte initiale.
   - **Disparus** : éléments de la carte initiale qui ont été réfutés ou reformulés.
3. **Identification des patterns trans-cycles** : ce qui revient sous plusieurs formes, ce qui se transforme à mesure qu'on creuse.
4. **Synthèse finale** au format standard (verrouillé / dissonant / angles morts / recommandations), mais cette fois robustifiée par le travail itératif.

---

## Format des retours utilisateur entre cycles

À la fin de chaque cycle (1, 2, 3), l'agent invite l'utilisateur à répondre à un **bloc de questions standardisé** :

```
══════════════════════════════════════════════
QUESTIONS DE TRANSITION — Fin du cycle N
══════════════════════════════════════════════

1. Quels éléments produits par ce cycle te semblent
   les plus justes / fertiles / pertinents ?
   (Cela renforce leur poids dans les cycles suivants.)

2. Quels éléments te semblent forcés, plaqués, ou
   manqués ?
   (Cela les écarte ou les reformule.)

3. Quelle information nouvelle as-tu acquise depuis
   le cycle précédent que je devrais intégrer ?

4. Sur quel(s) point(s) souhaites-tu que le prochain
   cycle se concentre ?
```

L'utilisateur peut répondre brièvement ou en détail. L'agent intègre ses retours dans le cycle suivant comme **contraintes prioritaires**.

---

## Conditions d'arrêt

Le mode itératif s'arrête quand au moins une des conditions suivantes est remplie :

1. **Saturation analytique** : au cycle N, aucune nouvelle dissonance ni aucun nouvel angle mort significatif n'émerge.
2. **Convergence forte** : la majorité des éléments du dossier sont passés en *convergence forte* à travers les cycles.
3. **Limite de cycles** : 4 cycles atteints (limite haute recommandée).
4. **Décision utilisateur** : l'utilisateur estime avoir ce dont il a besoin.

L'arrêt est annoncé explicitement :

> *"Saturation atteinte au cycle N. Les éléments restants sont soit stabilisés, soit en attente d'information externe. Je propose de produire la synthèse trans-cycles."*

---

## Avertissements propres au mode itératif

### Risque 1 : Surajustement

Plus on creuse, plus on peut "expliquer" — au risque de produire une analyse trop ajustée aux signaux disponibles et fragile au moindre changement. C'est l'équivalent analytique du *overfitting* en machine learning.

**Contre-mesure** : à chaque cycle, l'agent demande explicitement *"qu'est-ce qui pourrait, dans les 6 prochains mois, invalider radicalement cette analyse ?"*. Cette question maintient la falsifiabilité.

### Risque 2 : Effet d'engagement (sunk cost)

Après 3 cycles de travail, on devient psychologiquement attaché aux conclusions provisoires. C'est un biais documenté.

**Contre-mesure** : avant la synthèse finale, l'agent fait un *cycle de réfutation* — il liste systématiquement les éléments les plus solides et demande : *"si je devais argumenter contre cette conclusion, par où commencer ?"*

### Risque 3 : Glissement de niveau de confiance

À mesure que les cycles s'enchaînent, on peut se mettre à parler des hypothèses comme si elles étaient des faits — le travail accumulé donnant une fausse autorité.

**Contre-mesure** : les marquages épistémologiques (`[REGISTRE SYMBOLIQUE]` / `[REGISTRE ANALYTIQUE]` / `[REGISTRE SYNTHÉTIQUE]`) doivent être **maintenus à chaque cycle**, même quand cela alourdit la lecture.

### Risque 4 : Saturation utilisateur

3 cycles + retours, c'est long. L'utilisateur peut se fatiguer et accepter trop vite ce que l'agent propose.

**Contre-mesure** : l'agent peut proposer une **pause** entre les cycles 2 et 3, en sauvegardant l'état (voir section suivante).

---

## Mémoire externe et reprise

Le Miroir Trans-échelle, comme les autres skills de l'écosystème, **n'a pas de mémoire interne persistante**. Pour qu'un travail itératif soit reprenable d'une session à l'autre, l'utilisateur doit maintenir un **journal de session** externe.

### Format recommandé : `miroir-log.md`

```markdown
# Miroir Trans-échelle — Journal de session

## Session du [date] sur dossier [nom]

### Cycle 1 — Carte initiale
[paste de la sortie complète]

### Retours utilisateur post-cycle 1
- Pertinents : [...]
- Plaqués : [...]
- Info nouvelle : [...]
- Focus pour cycle 2 : [...]

### Cycle 2 — Approfondissement
[paste]

### [etc.]

### Synthèse trans-cycles
[paste de la synthèse finale]

### Évaluation rétrospective (à compléter 1-3 mois plus tard)
- Quelles hypothèses se sont avérées ?
- Quels indicateurs de bascule ont été atteints ?
- Quels angles morts initiaux étaient pertinents ?
```

Ce journal devient une **archive de pratique** précieuse pour calibrer le skill au fil du temps. Il alimente aussi l'évaluation rétrospective du Miroir : ses convergences se valident-elles ? ses dissonances étaient-elles éclairantes ?

---

## Exemple sommaire : 3 cycles sur un dossier géopolitique

**Dossier** : *Évolution du rôle d'un État de taille moyenne (X) dans une zone de rivalité entre deux grandes puissances (A et B), sur un horizon de 24 mois.*

### Cycle 1 — Carte initiale

P1 identifie : archétypes *Le Voyageur* (X cherche sa place) + *Le Tisseur* (médiateur).
P2 identifie : signaux de double allégeance + glissements diplomatiques.
P3 : convergence forte sur "ambiguïté stratégique délibérée".

**Points d'entrée** : 3 dissonances (intérieur/extérieur, économie/sécurité, narratif officiel/pratique), 2 angles morts (dimension domestique vue par P1 seul, indicateur économique vu par P2 seul).

### Cycle 2 — Approfondissement de la dissonance "narratif officiel vs pratique"

P1 ciblée : invocation de l'archétype étendu *Eshu / Legba* (carrefour, ambiguïté constitutive) — l'ambiguïté n'est pas tactique, elle est *constitutive*.
P2 ciblée : collecte d'indicateurs comportementaux (déplacements, contrats, signatures).
Mini-carte : la dissonance se *confirme* — l'écart entre discours et pratique est structurel, pas conjoncturel.

### Cycle 3 — Intégration de l'angle mort "dimension domestique"

P2 élargie : recherche d'indicateurs politiques internes (opinion publique, presse domestique, mouvements sociaux).
Résultat : la dimension domestique exerce une pression que la lecture macro avait sous-estimée.

### Synthèse trans-cycles

Verrouillé : ambiguïté stratégique structurelle (3 cycles le confirment).
Dissonant résolu : discours/pratique = écart constitutif, pas tactique.
Émergent : la pression domestique comme facteur sous-estimé initialement.
Recommandation : monitorer prioritairement la cohésion domestique de X, plus que ses signaux diplomatiques.

---

## Limites finales

Le mode itératif **n'élimine pas l'incertitude** ; il la *cartographie mieux*. Une carte trans-cycles très robuste reste une carte — pas le territoire. La meilleure analyse ne dispense ni du jugement humain situé, ni de la décision sous incertitude. Le Miroir éclaire ; il ne tranche pas.
