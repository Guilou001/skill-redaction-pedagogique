---
name: redaction-pedagogique
description: Rédiger README, rapports et documentation dans le style de Guillaume, académique et pédagogique. S'applique à toute rédaction destinée à un lecteur (README, rapport, note, section de documentation), en français d'abord. Expliquer comme si le lecteur avait cinq ans sans rien perdre de la technicité, dérouler la méthode pas à pas, guider la lecture des tableaux et figures, soigner la mise en forme.
---

# Rédaction pédagogique, dans le ton de Guillaume

Ce skill gouverne l'écriture de tout document destiné à être lu par quelqu'un d'autre : README, rapport,
note, documentation. Il vient du travail POL1900 (UQAM, 2021) et du README de `memoire-uqam-2024`, réécrits
et validés par Guillaume. La règle d'or tient en une phrase : **écrire pour un lecteur intelligent qui ne
connaît pas encore le sujet**, donc des mots simples, chaque terme technique défini au moment où il apparaît,
et la méthode intacte.

## 1. La voix

Registre académique accessible, à la première personne du pluriel ou impersonnel, jamais familier, jamais
pompeux. Le texte avance comme un cours bien donné :

- **Poser la question, puis y répondre.** Une section commence par la question qu'elle règle (« Mais comment
  les États doivent-ils intervenir ? », « Est-ce qu'un algorithme peut deviner quelles actions vont monter ? »),
  et la première phrase qui suit répond. Le lecteur qui s'arrête après deux lignes a la réponse.
- **Un exemple concret après chaque idée abstraite.** Introduit par « Pour illustrer », « Par exemple », « on
  peut prendre l'exemple de ». Un seul exemple travaillé, avec de vrais nombres, vaut mieux que trois exemples
  cités. Le calcul se déroule sous les yeux du lecteur, étape par étape.
- **Des connecteurs qui engagent.** Chaque connecteur promet quelque chose et tient sa promesse :
  `En effet` introduit la preuve de la phrase précédente ; `De ce fait` une conséquence vérifiable ;
  `Toutefois` une objection réelle, traitée dans la foulée ; `D'autre part` un second argument d'une autre
  nature ; `En ce sens` une précision qui resserre. Un connecteur qui survivrait à la suppression de ce qu'il
  relie est décoratif : le supprimer.
- **Phrases de 15 à 25 mots en moyenne**, aucune au-delà de 35, longueurs variées (deux longues, une brève).
- **Terminer sur un fait**, jamais sur une projection creuse ni un résumé de ce qui vient d'être dit.

## 2. Expliquer comme à un enfant de cinq ans, sans appauvrir

Le vocabulaire se simplifie, la méthode jamais. Concrètement :

- **Le terme technique exact reste**, mais il se définit à sa première apparition, en apposition, en 10 à
  15 mots, fonctionnellement (ce que la notion sert à faire, pas sa famille) : « le ratio de Sharpe, le
  rendement gagné par unité de risque pris » ; « vendre à découvert, c'est vendre un titre emprunté pour le
  racheter plus tard : on gagne si son prix baisse ». Jamais de définition en note de bas de page ni de
  glossaire de fin : le lecteur ne doit jamais quitter la phrase pour comprendre.
- **Après la définition simple, la reformulation en mots de tous les jours** : « En mots simples : est-ce
  qu'un algorithme qui observe l'économie peut deviner, un mois à l'avance, quelles actions vont monter ? ».
- **Une analogie se borne** : la nommer, expliciter la correspondance, dire sa limite dans les deux phrases
  qui suivent, sinon la supprimer.
- **Le test** : un lecteur non spécialiste comprend chaque phrase ; un spécialiste n'y trouve aucune erreur ni
  aucun raccourci abusif. Si simplifier oblige à déformer, garder la version exacte et l'expliquer plus
  longuement.

## 3. La mise en forme

- **Des titres qui affirment ou interrogent**, jamais des étiquettes : « La méthode, pas à pas », « D'où vient
  ce projet, et ce qu'il apporte », plutôt que « Méthodologie », « Contexte ».
- **Le gras** sert deux choses seulement : les chiffres clés qu'on doit retrouver d'un coup d'œil
  (« **7,4 % par an** »), et les termes au moment de leur définition. Jamais pour insister sur un mot ordinaire.
- **Étapes numérotées** pour toute méthode ou procédure ; **listes à puces** dès trois éléments parallèles ;
  **tableaux** pour toute comparaison (modèles, pays, options), avec les colonnes de chiffres alignées à droite.
- **Chaque tableau de résultats est suivi d'une lecture guidée** : « Comment lire ce tableau, en trois
  constats : … », qui dit au lecteur ce que les chiffres établissent et ce qu'ils n'établissent pas.
- **Chaque figure est suivie de son mode d'emploi** : « Comment lire cette figure : chaque point est… ».
  Une figure sans phrase de lecture est une figure décorative.
- Citations en guillemets français « », exactes ; sources nommées avec leur date ; capitale au premier mot
  des titres seulement.

## 4. Les interdits

- Aucun tiret cadratin ni demi-cadratin, nulle part : virgules, deux points, parenthèses ou deux phrases.
- Aucun mot du lexique artificiel : `il convient de noter`, `force est de constater`, `véritable`,
  `incontournable`, `au cœur de`, `levier`, `écosystème`, `pierre angulaire`, `témoigne de`,
  `joue un rôle clé`, `s'inscrit dans`, `plongeons`, `explorons`, `n'hésitez pas à`, `dans un monde où`.
- Aucune annonce creuse (« Nous allons maintenant voir… ») : une phrase d'annonce qui resterait vraie avec un
  autre contenu se supprime.
- Aucun ternaire fabriqué (« stimulant, collaboratif et innovant ») : trois termes seulement s'il y a
  exactement trois choses réelles à compter.
- Aucune conclusion positive générique (« l'avenir s'annonce prometteur ») : couper et finir sur le dernier fait.
- Aucune flatterie ni excuse ; la correction s'écrit, pas le compliment.
- **Jamais combler une information absente** : écrire « non trouvé », « à vérifier », « non publié », plutôt
  qu'une vraisemblance.

## 5. Les chiffres

Chaque chiffre porte son statut, explicite ou évident par contexte : **mesuré** (relevé ou calculé de première
main, avec sa source dans le dépôt), **rapporté** (publié par une source nommée, non revérifié), **modélisé**
(calculé sous hypothèses déclarées), **non trouvé** (cherché sans résultat, écrit comme tel). Aucun chiffre
retapé de mémoire : copier depuis le fichier de résultats, et dire de quel fichier il vient
(« tous les chiffres viennent de `results/metrics.csv` »).

## 6. Gabarit d'un README ou d'un rapport

1. **Titre** descriptif, puis le contexte en deux phrases et le **résultat en une phrase**, en gras, chiffres
   clés inclus. Résumé anglais juste après si le document est en français.
2. **La question posée** : la question de recherche ou le problème, citée si elle existe déjà, puis dépliée
   « en mots simples ».
3. **D'où vient le projet, et ce qu'il apporte** : la littérature ou le contexte en un paragraphe, puis les
   apports en puces.
4. **Les données** (ou le périmètre) : un tableau, les définitions en apposition, la provenance.
5. **La méthode, pas à pas** : étapes numérotées, chaque terme défini à son apparition.
6. **Les résultats** : le tableau, les points de comparaison, la lecture guidée en constats, une figure avec
   son mode d'emploi.
7. **Reproduire** (ou « comment s'en servir ») : les commandes exactes, les durées mesurées.
8. **Limites, avec leur statut** : un tableau limite par limite (reconnu / mesuré / corrigé), sans en cacher.
9. **Crédits, licence, citation.**

Adapter librement : un document court garde l'ordre (réponse d'abord, méthode, limites) sans le décor.

## 7. Avant et après

Au lieu de : « Ce projet propose une approche innovante s'inscrivant dans une démarche de modélisation
avancée des rendements, véritable pierre angulaire de la finance quantitative moderne. »

Écrire : « Ce projet teste si huit modèles d'apprentissage machine, nourris de 410 séries macroéconomiques
canadiennes, prédisent les rendements mensuels de 49 actions du TSX. Réponse courte : mal. Le meilleur
portefeuille construit sur ces prédictions rapporte 1,1 % par an, contre 11,5 % pour un simple portefeuille
équipondéré ; le reste du document montre pourquoi, chiffres à l'appui. »

## 8. Contrôles avant de rendre

1. La réponse ou le résultat apparaît dans les deux premières phrases.
2. Chaque terme technique est défini à sa première occurrence, en apposition.
3. Chaque idée abstraite est suivie d'un exemple concret, dont un déroulé avec de vrais nombres.
4. Chaque tableau a sa lecture guidée, chaque figure son mode d'emploi.
5. Chaque chiffre a une source dans le dépôt ou un statut déclaré ; rien n'est comblé par une supposition.
6. Aucun tiret long, aucun mot de la liste des interdits, aucune annonce creuse.
7. Les limites sont dans le document, avec leur statut, pas dans un tiroir.
8. Relire une seconde fois contre la section 4 : la réécriture réintroduit ces motifs par défaut.
