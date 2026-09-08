# Des consignes pour écrire des textes techniques plus clairs

Un texte peut utiliser des mots simples et rester difficile à comprendre. Il manque parfois la question de départ, le sens d'un chiffre ou l'explication de ce qu'un graphique montre.

Ce dépôt contient deux *skills*, des fichiers de consignes qu'un assistant de rédaction peut lire pour écrire et relire. Ils visent deux besoins distincts.

## Choisir le guide adapté

| Besoin | Fichier à utiliser |
|---|---|
| Expliquer clairement une méthode, un résultat ou un projet | [Rédaction pédagogique](SKILL.md) |
| Retrouver les habitudes d'écriture de Guillaume Vaudescal | [Écriture de Guillaume](ecriture-guillaume/SKILL.md) |

Le premier fixe une méthode de clarté et de vérification. Le second décrit une voix à partir de travaux de l'auteur. Ils peuvent donner des consignes différentes, qu'il faut départager selon le texte demandé.

## Voir la différence sur un exemple

| Formulation à revoir | Formulation expliquée |
|---|---|
| Le prix baisse de moitié, l'usage triple, la facture double. | Si le prix baisse de moitié et que l'usage triple, la facture augmente de 50 %. |

La réécriture corrige ici le raisonnement. Avec un prix initial de 2 euros et 10 unités, la facture vaut 20 euros. Avec un prix de 1 euro et 30 unités, elle vaut 30 euros.

Le même principe s'applique aux résultats financiers. Un chiffre doit préciser ce qu'il mesure, sur quelle période et avec quelles limites.

## Ce que la relecture demande

Présenter la question avant la méthode. Définir un terme au moment où il devient nécessaire. Accompagner chaque tableau ou figure d'une phrase qui aide à le lire.

Distinguer un résultat calculé d'une hypothèse ou d'une valeur citée. Vérifier les comparaisons et les petits calculs, même lorsqu'ils paraissent évidents.

Les consignes complètes et d'autres exemples sont dans les deux fichiers. Les extraits qui servent à décrire la voix de l'auteur restent dans leur document d'origine.

## Utiliser le premier guide dans Claude Code

La [documentation officielle des skills](https://code.claude.com/docs/en/skills) explique les emplacements personnels et ceux propres à un projet.

Pour une installation personnelle, cloner ce dépôt dans le dossier suivant.

```bash
git clone https://github.com/Guilou001/skill-redaction-pedagogique \
  ~/.claude/skills/redaction-pedagogique
```

On peut ensuite demander explicitement une relecture.

```text
/redaction-pedagogique Relis le README et explique les termes difficiles.
```

Le second guide possède son propre fichier et sa procédure dans la [présentation détaillée](docs/ETUDE_DETAILLEE.md).

## Ce que ces consignes ne garantissent pas

Elles ne vérifient pas automatiquement les faits et n'exécutent pas les calculs du document. Il faut consulter les sources et contrôler les résultats.

Une réponse peut aussi ne pas respecter toutes les consignes. La relecture du texte final reste nécessaire.

## Pour aller plus loin

[Méthodes, résultats complets et références](docs/ETUDE_DETAILLEE.md) · [Licence](LICENSE).

## English summary

Two writing guides separate clear technical explanation from an author's personal voice. They ask for defined terms, traceable numbers and guided chart reading. They are editorial instructions, not automated fact-checking or numerical validation.
