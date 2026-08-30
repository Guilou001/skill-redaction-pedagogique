# redaction-pedagogique

> Un skill [Claude Code](https://claude.com/claude-code) qui fait écrire en français clair, sourcé et neutre, sans rien perdre de la technicité.

[![Licence MIT](https://img.shields.io/badge/licence-MIT-1a2744)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-skill-104af7)](https://claude.com/claude-code)
[![Langue](https://img.shields.io/badge/langue-fran%C3%A7ais-6b7280)](SKILL.md)

**Ce skill remplace les tics d'écriture des modèles de langage par une méthode de rédaction vérifiable.** Il impose trois choses au texte produit. Chaque terme technique se définit à l'endroit où il apparaît. Chaque phrase doit tenir debout logiquement, y compris ses calculs. Chaque chiffre porte son statut, mesuré, rapporté, calculé ou non trouvé.

*An opinionated Claude Code skill for writing French technical prose: plain words with full rigor, terms defined at first use, every invented calculation re-checked by hand, and numbers that carry their provenance.*

---

## Le problème qu'il règle

Un modèle de langage écrit spontanément une prose qui a l'air sérieuse et qui ne l'est pas. Trois défauts reviennent, et ils sont indépendants les uns des autres.

**Le remplissage.** Des formules qui occupent la place d'un argument. « Véritable pierre angulaire », « il convient de noter », « s'inscrit dans une démarche ». Elles resteraient vraies quel que soit le sujet, donc elles n'informent sur aucun.

**Les phrases qui ne tiennent pas debout.** Une prémisse que personne ne reconnaît, un calcul faux, une chronologie inversée, une phrase d'effet qui annonce une démonstration sans la faire. Le lecteur les repère sans rien connaître au sujet, et une seule suffit à lui faire douter du reste.

**Le glissement vers la plaidoirie.** Un adjectif qui juge à la place d'un chiffre qui mesure, une objection de paille, une source citée sans sa date ni son échantillon.

Ce skill traite les trois séparément, parce que corriger le premier ne corrige pas les deux autres.

---

## Les dix règles, en un coup d'œil

| # | Règle | Ce qu'elle impose |
|---|---|---|
| 1 | La voix | Poser la question, y répondre en premier. Connecteurs qui tiennent leur promesse. Phrases de 15 à 25 mots. |
| 2 | Expliquer sans appauvrir | Terme défini en apposition à sa première occurrence, jamais en glossaire de fin. |
| 3 | **La logique avant le style** | Dix défauts catalogués, et trois questions à poser à chaque phrase. |
| 4 | **Rester neutre** | Le chiffre plutôt que l'adjectif. L'objection la plus forte, pas la plus commode. |
| 5 | La mise en forme | Titres qui affirment. Lecture guidée sous chaque tableau et chaque figure. |
| 6 | Les interdits | Zéro tiret cadratin, lexique artificiel proscrit, aucune annonce creuse. |
| 7 | Les chiffres | Statut déclaré. Un complément à 100 est un calcul, pas une mesure. |
| 8 | Gabarit | Neuf blocs, de la réponse en une phrase jusqu'aux limites avec leur statut. |
| 9 | Avant et après | Trois réécritures commentées. |
| 10 | Contrôles | Onze vérifications, dont refaire chaque calcul inventé à la main. |

Comment lire ce tableau. Les règles 3 et 4 sont les ajouts les plus récents et les plus rentables. Les règles 1, 2 et 5 gouvernent la lisibilité, les règles 6 et 7 l'honnêteté, les règles 8 à 10 la relecture. Le détail de chacune vit dans [`SKILL.md`](SKILL.md).

---

## Avant et après

Trois cas réels, écrits puis rejetés en relecture.

### Le remplissage

> Ce projet propose une approche innovante s'inscrivant dans une démarche de modélisation avancée des rendements, véritable pierre angulaire de la finance quantitative moderne.

devient

> Ce projet teste si huit modèles d'apprentissage machine, nourris de 410 séries macroéconomiques canadiennes, prédisent les rendements mensuels de 49 actions du TSX. Réponse courte, mal. Le meilleur portefeuille construit sur ces prédictions rapporte 1,1 % par an, contre 11,5 % pour un simple portefeuille équipondéré.

### La phrase d'effet

> Quand un fournisseur annonce une baisse, le réflexe est d'attendre la suivante ou de passer au moins cher. Les deux réflexes sont faux.

devient

> Une baisse de tarif se lit d'abord comme une bonne nouvelle pour le budget. Elle en est rarement une, parce que votre facture ne dépend pas du prix affiché mais de la quantité que vous consommez. Or cette quantité augmente justement quand le prix descend.

Deux défauts corrigés d'un coup. Personne n'attend une seconde baisse le jour d'une première, et « les deux réflexes sont faux » annonçait une réfutation sans rien réfuter.

### Le calcul faux

> Le prix baisse de moitié, l'usage triple, la facture double.

devient

> Si le prix par jeton baisse de moitié et que votre consommation triple, votre facture n'est pas divisée par deux, elle augmente de 50 %.

Le calcul d'origine était faux, 0,5 multiplié par 3 donne 1,5. C'est le défaut le plus dangereux du lot, parce qu'aucun contrôle de style ne le voit.

---

## Installation

Pour tous vos projets, en skill personnel.

```bash
git clone https://github.com/Guilou001/skill-redaction-pedagogique \
  ~/.claude/skills/redaction-pedagogique
```

Pour un seul projet, à la racine de celui-ci.

```bash
git clone https://github.com/Guilou001/skill-redaction-pedagogique \
  .claude/skills/redaction-pedagogique
```

Vérifier que Claude Code le voit.

```bash
claude
> /redaction-pedagogique
```

---

## Utilisation

Claude Code applique le skill automatiquement dès que la tâche est une rédaction destinée à un lecteur. Vous pouvez aussi l'appeler explicitement.

```
/redaction-pedagogique réécris le README de ce dépôt
/redaction-pedagogique relis cet article contre les règles 3 et 4
/redaction-pedagogique passe les onze contrôles sur rapport.md
```

Le troisième usage est le plus utile en pratique. Le skill sert autant à relire qu'à écrire, et la relecture réintroduit les motifs interdits par simple retour au plus probable, ce que la règle 11 des contrôles rappelle explicitement.

---

## Ce que ce skill ne fait pas

- **Il ne vérifie pas les faits à votre place.** Il impose de déclarer le statut de chaque chiffre, il ne va pas chercher la source.
- **Il n'exécute aucun contrôle automatique.** Les onze contrôles se passent à la lecture. Un dépôt qui veut les automatiser écrit ses propres scripts.
- **Il ne couvre pas les autres langues.** Les règles de structure valent partout, les listes de mots proscrits sont propres au français.
- **Il ne remplace pas une ligne éditoriale.** Il dit comment écrire, pas quoi dire ni à qui.

---

## Structure du dépôt

```
SKILL.md    les dix règles, chargées par Claude Code
README.md   ce fichier
LICENSE     MIT
```

---

## Contribuer

Les propositions se font par issue ou pull request. Une règle nouvelle est acceptée si elle vient d'un défaut réellement observé dans un texte produit, et si elle est accompagnée de l'exemple avant et après. Une règle qui ne peut pas s'illustrer sur un cas concret ne se vérifie pas en relecture, donc ne sert à rien.

## Licence

MIT. Voir [LICENSE](LICENSE).

---

## Un second skill, à part : `ecriture-guillaume`

Ce dépôt porte désormais **deux skills distincts**, qui ne servent pas à la même chose et qui ne sont
pas fusionnés.

| | `redaction-pedagogique` (racine) | `ecriture-guillaume` (dossier) |
|---|---|---|
| Ce qu'il fait | impose une méthode de rédaction vérifiable | reproduit une voix précise, celle de Guillaume Vaudescal |
| D'où il vient | des règles tirées de la relecture d'une production en continu | de la mesure de sept travaux de maîtrise, 733 phrases comptées une à une |
| Ce qu'il interdit | les tics des modèles de langage | les mots qui n'existent pas en français, à commencer par les calques de l'anglais |
| Ce qu'il autorise | rien qui affaiblisse la rigueur | trois à cinq imperfections humaines par document |
| Quand l'employer | tout document destiné à un lecteur | quand le texte doit passer pour écrit par son auteur |

**Le point qui compte.** Le chapitre 1 d'`ecriture-guillaume` n'est pas le style, c'est le **sens**.
Il part d'un constat : un texte dans la bonne voix mais dont les mots ne veulent rien dire est un
échec plus grave qu'un texte hors voix. Il donne donc trois questions à passer sur chaque phrase, et
un tableau de 24 calques de l'anglais avec le mot juste à mettre à leur place.

Trois exemples du tableau :

| À ne pas écrire | Pourquoi c'est faux | Écrire à la place |
|---|---|---|
| une famille mince | « mince » ne se dit pas d'une catégorie | un métier qui n'a qu'un seul projet |
| une forme fermée | calque de *closed form* | une formule qui se calcule à la main |
| un seau de qualité | calque de *bucket* ; un seau est un récipient | une tranche de notation, une classe de risque |

Les deux skills peuvent coexister, l'un fixant la méthode et l'autre la voix. Ils peuvent aussi être
fusionnés plus tard, à une condition : les deux se contredisent sur trois points, l'annonce de plan,
le statut des chiffres et la longueur des phrases, et la fusion devra trancher au lieu de faire une
moyenne.

**Installation.** Copier `ecriture-guillaume/` dans `~/.claude/skills/`, à côté de
`redaction-pedagogique/`.

```bash
mkdir -p ~/.claude/skills/ecriture-guillaume
cp ecriture-guillaume/SKILL.md ~/.claude/skills/ecriture-guillaume/
```
