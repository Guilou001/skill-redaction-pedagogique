# redaction-pedagogique

Un skill [Claude Code](https://claude.com/claude-code) pour écrire des README, rapports et documentations
pédagogiques en français : expliquer comme si le lecteur avait cinq ans sans rien perdre de la technicité,
définir chaque terme à sa première apparition, guider la lecture des tableaux et des figures, et tenir un ton
académique accessible (celui de mes travaux UQAM). Il encode aussi les interdits de forme (tirets longs,
lexique artificiel, annonces creuses) et le statut des chiffres (mesuré, rapporté, modélisé, non trouvé).

*A Claude Code skill for writing pedagogical French READMEs and reports: plain words with full technical
rigor, terms defined at first use, guided readings of tables and figures, measured numbers only.*

## Installation

Pour tous les projets (skill personnel) :

```bash
git clone https://github.com/Guilou001/skill-redaction-pedagogique ~/.claude/skills/redaction-pedagogique
```

Pour un seul projet : cloner dans `.claude/skills/redaction-pedagogique` à la racine du projet.

## Utilisation

Claude Code applique le skill quand la tâche est une rédaction destinée à un lecteur, ou sur demande :

```
/redaction-pedagogique réécris le README de ce dépôt
```

Le fichier `SKILL.md` contient les règles : la voix (section 1), la vulgarisation sans appauvrissement
(section 2), la mise en forme (section 3), les interdits (section 4), le statut des chiffres (section 5),
un gabarit de document (section 6) et la liste de contrôles (section 8).

## Exemple d'application

Le README de [memoire-uqam-2024](https://github.com/Guilou001/memoire-uqam-2024) a été écrit avec ces règles.

## Licence

MIT.
