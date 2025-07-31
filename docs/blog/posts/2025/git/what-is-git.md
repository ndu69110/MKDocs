---
date:
  created: 2022-07-31
categories:
  - Git
  - Repository
  - Branch
  - Commit
tags:
  - Git
  - Repository
  - Branch
  - Commit
draft: false
links:
  - index.md
#readtime: 15
authors:
  - team
---

# Introduction à Git et Github

## Qu'est-ce que Git ?

Un terme que j'ai eu tellement de mal à comprendre et qui est répandu désormais partout dans la tech est : qu'est-ce que **Git** exactement ? Tout d'abord, il est important de savoir que **Git est un système de contrôle de version distribué qui résout de gros problèmes pour les développeurs de logiciels**. 

<!-- more -->

Lorsque plusieurs développeurs travaillent sur un projet, des problèmes tels que des fichiers écrasés, des versions conflictuelles et des difficultés à suivre les modifications peuvent survenir. Git offre une solution en maintenant **essentiellement un historique des versions**, ce qui permet de voir sur quoi d'autres développeurs ont travaillé. Mais passons par un exemple concret d'un flux de travail Git pour que vous le compreniez vraiment. Tout d'abord, un développeur va **cloner un dépôt**, puis il **créera une branche pour une nouvelle fonctionnalité**, ce qui signifie essentiellement qu'il va construire une nouvelle partie du code et qu'il veut travailler dans sa propre zone, son propre espace. Ensuite, il va **effectuer et valider des modifications**, **pousser ces modifications vers un dépôt partagé** où toute l'équipe y a accès, puis **soumettre ces modifications pour révision** où des développeurs plus expérimentés les examineront, les critiqueront et donneront des retours agréables et parfois moins agréables. Et ensuite, une fois les modifications approuvées, elles sont **fusionnées dans le projet principal**, qui vous parvient finalement, à vous et à moi, pour que nous puissions commencer à l'utiliser.

---

## Qu'est-ce que Git ?

• **Système de Contrôle de Version Distribué (DVCS)** : Git est défini comme un système qui aide les développeurs à gérer les versions de leur code1.

• **Résolution de Problèmes Communs** : Il adresse des défis majeurs rencontrés lorsque plusieurs développeurs collaborent sur un même projet, tels que :

- Les fichiers écrasés
- Les versions conflictuelles
- Les difficultés à suivre les modifications


---

## Historique des Versions

Git résout ces problèmes en maintenant un historique détaillé des versions, permettant de visualiser les contributions de chaque développeur1.

**2\. Flux de Travail Git Typique (Exemple Concret) :** Le processus de travail avec Git, tel que décrit dans la vidéo, suit les étapes suivantes :

• **1\. Cloner un Dépôt (****repository****)** : Un développeur commence par créer une copie locale d'un projet Git existant1.

• **2\. Créer une Branche (****branch****)** : Pour développer une nouvelle fonctionnalité ou travailler sur une partie spécifique du code sans affecter le projet principal immédiatement, le développeur crée une "branche" personnelle1. C'est un espace de travail isolé1.

• **3\. Effectuer et Valider des Modifications (****make and commit changes****)** : Le développeur apporte les modifications nécessaires et les "valide" (sauvegarde les changements avec un message descriptif) dans sa branche locale1.

• **4\. Pousser les Modifications (****push changes****)** : Les modifications validées sont ensuite "poussées" vers un dépôt partagé, rendant le travail accessible à toute l'équipe1.

• **5\. Soumettre pour Révision (****submit for review****)** : Les changements sont soumis pour être examinés par des développeurs plus expérimentés. Ils revoient, critiquent et donnent des retours1.

• **6\. Fusionner dans le Projet Principal (****merge into the main project****)** : Une fois les modifications approuvées, elles sont intégrées (fusionnées) dans la branche principale du projet. Ces changements deviennent alors disponibles pour les utilisateurs finaux1.

