# Carte de Résonance — Format & règles de construction

La carte de résonance est l'**apport propre** du Miroir Trans-échelle. Elle ne crée aucun contenu nouveau ; elle **structure le dialogue** entre les sorties de P1 (symbolique) et P2 (analytique).

Ce fichier détaille :
- les règles de construction
- les quatre types de croisement
- les règles de lecture
- la synthèse trans-échelle
- des exemples annotés

---

## Règle fondamentale

> **La carte de résonance est traçable.**
>
> Chaque ligne du tableau doit renvoyer à un élément *précis* de P1 et/ou de P2. Si un élément n'est ni dans P1 ni dans P2, il n'a pas sa place dans la carte.

Cette règle est le garde-fou contre le glissement le plus probable du skill : que la passe de synthèse devienne une nouvelle source d'affirmations non-vérifiables.

---

## Structure du tableau croisé

| Colonne | Contenu | Source |
|---------|---------|--------|
| **Élément P1** | Archétype, motif, fragment de Phrase FdD | Sortie de la Passe 1 |
| **Élément P2** | Signal faible, hypothèse, indicateur | Sortie de la Passe 2 |
| **Type** | Catégorie du croisement (voir ci-dessous) | Déterminé par règles |
| **Lecture croisée** | Ce que le croisement révèle | Synthèse de l'agent |

Le tableau peut compter **6 à 12 lignes** typiquement. Au-delà, scinder en sous-tableaux thématiques.

---

## Les quatre types de croisement

### 1. Convergence forte

**Définition** : un élément de P1 et un élément de P2 pointent **explicitement** dans la même direction, sur la même dynamique.

**Exemple** :
- P1 : *Archétype actif : Le Bouffon (subversion par retournement)*
- P2 : *Signal faible : glissement lexical, le ministre parle désormais d'« opportunité » là où il parlait d'« obligation »*
- Type : **Convergence forte**
- Lecture croisée : *"Un retournement narratif est en cours. Symbole et signal pointent vers une inversion de posture délibérée. Robustesse double — à confirmer dans les 4 prochaines semaines."*

**Implication** : la convergence forte n'est **pas une preuve** ; elle est une **augmentation de robustesse**. Deux registres peuvent partager un biais commun.

---

### 2. Convergence faible

**Définition** : un alignement partiel, sur une dimension secondaire ou implicite.

**Exemple** :
- P1 : *Motif : seuil (passage entre deux états)*
- P2 : *Hypothèse H2 : transition prudente plutôt que rupture*
- Type : **Convergence faible**
- Lecture croisée : *"Les deux registres reconnaissent une dynamique de passage, mais P1 ne tranche pas sur sa nature et P2 hésite encore entre rupture et transition. À surveiller — cohérence partielle."*

**Implication** : à inscrire dans la veille active, pas dans les conclusions.

---

### 3. Dissonance

**Définition** : un élément de P1 et un élément de P2 se **contredisent** structurellement.

**Exemple** :
- P1 : *Archétype actif : Le Souverain (affirmation d'autorité, ordre stable)*
- P2 : *Hypothèse H1 (la plus probable) : effondrement institutionnel imminent*
- Type : **Dissonance**
- Lecture croisée : *"Le symbolique voit de la stabilité affichée, l'analytique voit l'érosion réelle. Cet écart est typique d'un régime en fin de cycle : la façade symbolique persiste alors que les fondations cèdent. Point critique à creuser."*

**Implication** : **la dissonance est l'élément le plus précieux** de la carte. Elle révèle une asymétrie entre ce qui est performé (symbole) et ce qui se prépare (signal), ou inversement.

**Règle** : ne jamais "résoudre" une dissonance en choisissant un côté. Toujours l'**expliciter comme telle** et la conserver comme question ouverte.

---

### 4. Angle mort (asymétrie)

**Définition** : un élément n'apparaît **que dans un seul des deux registres**, sans corrélat dans l'autre.

**Deux sous-types** :

#### 4a. Angle mort analytique
Quelque chose vu par le symbolique seul. Indique un *défaut de capteur* dans la veille OSINT.

**Exemple** :
- P1 : *Archétype actif : Le Passeur (transformation par perte, deuil)*
- P2 : *—*
- Type : **Angle mort analytique**
- Lecture croisée : *"Le symbolique repère une dimension de deuil collectif que les indicateurs OSINT ne captent pas. À investiguer : enquêtes sociales, signaux culturels, art contemporain, recherche académique sur le moral collectif."*

#### 4b. Angle mort symbolique
Quelque chose vu par l'analytique seul. Indique un *défaut d'imagination* dans la lecture archétypale.

**Exemple** :
- P1 : *—*
- P2 : *Signal faible : trois startups défensives non liées ont levé 200M$ en 6 semaines dans le secteur Y*
- Type : **Angle mort symbolique**
- Lecture croisée : *"Un mouvement capital significatif n'a pas de correspondance symbolique évidente dans le tirage. À interpréter : quel archétype émergent cela rejoue-t-il ? Possible Semeur (préparation) ou Combattant (anticipation de confrontation)."*

**Implication** : un angle mort n'est pas une faiblesse de l'analyse — c'est une **opportunité de mise à jour** des grilles de lecture.

---

## Synthèse trans-échelle

Après le tableau, l'agent produit une synthèse en **quatre points**.

### 1. VERROUILLÉ (convergences fortes)

> *"Ce que les deux registres confirment ensemble — et donc ce sur quoi on peut s'appuyer avec un niveau de confiance accru, sans pour autant en faire une certitude."*

Format recommandé : 2 à 4 puces brèves.

### 2. DISSONANT (à creuser)

> *"Ce qui se contredit, et pourquoi. La dissonance est traitée comme un *fait analytique en soi* — pas comme une erreur à corriger."*

Format recommandé : 1 à 3 dissonances explicitées, avec une question ouverte pour chacune.

### 3. ANGLES MORTS

> *"Ce qu'un seul registre a vu. Ces points méritent une investigation complémentaire dans l'autre registre."*

Format recommandé : 2 colonnes (vu par symbolique seul / vu par analytique seul).

### 4. RECOMMANDATIONS

Trois types d'actions :

- **Hypothèses prioritaires** : parmi les H1/H2/H3 de P2, lesquelles sont renforcées ou affaiblies par la lecture croisée ?
- **Indicateurs à monitorer** : que faut-il surveiller dans les semaines/mois à venir pour valider ou réfuter les convergences ?
- **Questions ouvertes** : qu'est-ce que la carte laisse en suspens et qui mérite une investigation à part ?

---

## Exemple complet annoté

**Situation soumise** : *"Une grande entreprise tech annonce sa restructuration. La communication officielle parle d'« agilité retrouvée ». 1500 départs annoncés sur 18 mois. Le PDG multiplie les apparitions médiatiques."*

### Passe 1 (compacte)
- Archétypes : **Le Souverain** (affirmation), **Le Bouffon** (retournement narratif), **L'Ombre** (refoulé)
- Motifs : **rupture** + **spirale médiatique**
- Phrase FdD : *« Le Souverain parle fort parce que l'Ombre derrière lui ne se tait plus. La spirale médiatique est un masque qui se serre. »*
- Angles d'ouverture : (a) De quoi le PDG cherche-t-il à se distraire ? (b) Quel narratif interne est-il en train de céder ?

### Passe 2 (compacte)
- Question : *"Quelle est la probabilité que cette restructuration soit le prélude à une crise plus profonde (cession, hostile takeover, scandale) dans les 12 mois ?"*
- Signaux faibles : (a) le PDG a vendu pour $40M de stock options le mois précédent (b) trois directeurs financiers ont démissionné en cascade depuis 90 jours (c) glissement lexical : passage de "croissance" à "agilité" dans les communications
- Hypothèses : H1 = restructuration ordinaire ; H2 = préparation à cession/fusion ; H3 = scandale financier en gestation
- Scénarios : optimiste (vraie agilité), probable (consolidation par cession), critique (révélation scandale dans 6-9 mois)
- Biais : confirmation (on cherche à valider H3 parce qu'elle est plus narrativement satisfaisante)

### Passe 3 — Tableau croisé

| Élément P1 (sym) | Élément P2 (ana) | Type | Lecture croisée |
|------------------|------------------|------|-----------------|
| Le Souverain (affirmation) | Multiplication apparitions PDG | Convergence forte | Le surcroît de visibilité corrèle avec une affirmation d'autorité — typique d'un pouvoir contesté en interne. |
| Le Bouffon (retournement narratif) | Glissement lexical "croissance" → "agilité" | Convergence forte | Inversion délibérée du récit. Le mot change avant les faits — soit anticipation, soit dissimulation. |
| L'Ombre (refoulé) | Vente $40M stock + démissions CFO | Convergence forte | Le symbolique nomme un non-dit ; l'analytique le documente. **Triple convergence.** Robustesse maximale sur ce point. |
| Motif : rupture | Hypothèse H2 (cession) + H3 (scandale) | Convergence faible | Les deux hypothèses partagent une logique de rupture, mais l'analyse n'arbitre pas. |
| Spirale médiatique | — | Angle mort analytique | Le motif de spirale (intensification) n'a pas d'indicateur direct dans P2. À ajouter à la veille : fréquence et tonalité des prises de parole. |
| — | 1500 départs sur 18 mois (calendrier lent) | Angle mort symbolique | Le rythme étalé n'a pas de lecture archétypale immédiate — pourrait indiquer un Tisseur (orchestration) plutôt qu'une Ombre. À réinterpréter. |

### Synthèse trans-échelle

**VERROUILLÉ** :
- Une affirmation d'autorité publique alors qu'une dynamique de retrait/extraction se prépare en coulisses (Souverain × surcommunication).
- Le récit officiel est en train d'être réécrit — l'inversion lexicale est documentée et symboliquement nommée.

**DISSONANT** :
- Le calendrier étalé (18 mois) résiste à la lecture symbolique de rupture brutale. Cette dissonance suggère que **H2 (cession orchestrée)** est plus probable que **H3 (scandale subit)** — la lenteur est compatible avec une préparation, pas avec une crise.

**ANGLES MORTS** :
- *Symbolique seul* : la spirale médiatique comme indicateur autonome à intégrer dans la veille OSINT.
- *Analytique seul* : le calendrier 18 mois mérite une relecture archétypale (Tisseur ? Semeur ?).

**RECOMMANDATIONS** :
- *Hypothèse prioritaire* : H2 (cession/fusion préparée) — robustesse double, dissonance résolue en sa faveur.
- *Indicateurs à monitorer* : approches de fonds activistes, rumeurs M&A sectorielles, comportement du board, mouvements de stock des autres dirigeants.
- *Questions ouvertes* : qui sont les acheteurs potentiels ? Quel est le scénario de communication post-annonce ? Le scandale (H3) reste-t-il une possibilité résiduelle ?

---

## Règles d'écriture

1. **Ton sobre dans la P3.** Même si P1 emploie un registre poétique, la synthèse trans-échelle est sobre, factuelle, traçable.
2. **Toujours indiquer la traçabilité.** Chaque affirmation de synthèse doit pouvoir être rattachée à une ligne du tableau.
3. **Ne jamais combler les dissonances.** Si P1 et P2 se contredisent, l'agent ne tranche pas — il *explicite* la contradiction et la transforme en question.
4. **Préserver la modestie épistémique.** La carte de résonance ne dit pas la vérité ; elle dit ce qui *résiste à plusieurs lectures*.
