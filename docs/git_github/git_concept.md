---
date: 2025-07-28
categories:
    - Documentation
tags:
    - Git
    - Github
---

![](https://www.ndu69.com/Screenshots/screenshot_2025-07-29_12-52-39.jpg)

# Git et Github

## Qu'est ce que Git ?

**Git** est un **système de gestion de contrôle de code source (SCM)**, gratuit et open source. Sa fonction principale est de vous permettre de **gérer les modifications apportées aux fichiers au fil du temps** et de **revenir en arrière** pour voir ou restaurer ces modifications. C'est une capacité essentielle qui signifie que si vous "faites des erreurs", vous pouvez simplement revenir à une version précédente de votre projet.

### Concepts clés de Git

*   **Gestion des modifications** : Git enregistre l'historique des changements apportés à vos fichiers, vous permettant de comparer les différences entre les versions et de voir qui a modifié quoi. Si vous modifiez un fichier, Git reconnaîtra que ce fichier a été modifié.
*   **Dépôt (Repository)** : Un dépôt Git est un dossier qui contient tous les fichiers nécessaires pour suivre les changements. Vous l'initialisez localement sur votre ordinateur à l'aide de la commande `git init` dans le répertoire de votre projet. Une fois initialisé, un dossier caché appelé `.git` est créé, contenant tous les fichiers nécessaires au dépôt.
*   **Branches** :
    *   Une branche est fondamentalement une **copie de votre branche principale** (souvent appelée 'main' ou 'master') qui inclut toutes les entrées de l'historique des modifications.
    *   Son but est de vous permettre de travailler sur de **nouvelles fonctionnalités ou des corrections de bugs sans affecter la branche principale**.
    *   La branche par défaut est souvent configurée comme 'main'.
    *   Vous pouvez créer une nouvelle branche avec `git branch [nom_de_branche]` ou la créer et y passer directement avec `git switch -c [nom_de_branche]`.
    *   Pour voir les branches existantes et la branche active (indiquée par un astérisque), utilisez `git branch`.
    *   Pour passer d'une branche à l'autre, utilisez `git switch [nom_de_branche]`.
    *   Une fois les modifications d'une branche fusionnées, la branche peut être supprimée à l'aide de `git branch -d [nom_de_branche]`.
*   **Commit (Engagement)** :
    *   Un commit est comme une **instantané de votre dépôt à un moment donné**, enregistrant l'état actuel de tous vos fichiers.
    *   C'est l'équivalent d'écrire une entrée dans un "livre d'histoire".
    *   Chaque commit a un **identifiant unique**, inclut l'auteur (avec le nom et l'adresse e-mail configurés préalablement via `git config`) et la date associée.
    *   Les commits sont accompagnés d'un message descriptif pour expliquer les changements.
    *   La commande pour créer un commit est `git commit -m "votre message"`.
    *   Vous pouvez **amender** le dernier commit (`git commit --amend`) pour corriger le message ou les fichiers inclus sans créer un nouveau commit dans l'historique.
*   **Zones d'environnement de Git** : Git opère dans trois environnements clés :
    *   **Fichiers de travail (Working files)** : L'endroit où vous apportez des modifications aux fichiers.
    *   **Zone de staging (Staging area)** : Une "zone d'attente" pour vos fichiers modifiés avant qu'ils ne soient committés. Les fichiers ici sont prêts à être inclus dans le prochain commit.
    *   **Dépôt (Committed)** : L'endroit où les modifications sont enregistrées de manière permanente dans l'historique via un commit.
*   **Suivi des fichiers (`git add`)** :
    *   Pour que Git reconnaisse les modifications apportées à un fichier, il doit être "suivi". Initialement, les fichiers sont "non suivis".
    *   Vous pouvez ajouter des fichiers à la zone de staging (pour être suivis) avec `git add [nom_de_fichier]` ou ajouter tous les fichiers non suivis ou modifiés avec `git add --all`, `git add -A`, ou simplement `git add .`.
    *   Les fichiers peuvent être "dé-stagés" (retirés temporairement de la zone de staging pour le prochain commit) avec `git restore --staged [nom_de_fichier]` ou `git rm --cached [nom_de_fichier]`.
*   **Ignorer des fichiers (`.gitignore`)** :
    *   Vous pouvez indiquer à Git d'ignorer complètement certains fichiers, dossiers ou extensions en créant un fichier nommé `.gitignore`.
    *   C'est utile pour les fichiers générés automatiquement, les fichiers journaux ou les données sensibles, comme les salaires des employés, que vous ne voulez pas inclure dans votre projet.
*   **Opérations sur les fichiers** :
    *   **Supprimer des fichiers** : Les fichiers suivis peuvent être supprimés via Git avec `git rm [nom_de_fichier]` ou directement via l'explorateur de fichiers. Git reconnaîtra la suppression.
    *   **Restaurer des fichiers** : Si un fichier supprimé était précédemment committé, vous pouvez le restaurer avec `git restore [nom_de_fichier]`.
    *   **Renommer des fichiers** : Cela peut être fait directement dans l'explorateur de fichiers ou via le terminal avec `git mv [ancien_nom] [nouveau_nom]`.
*   **Historique des commits (`git log`)** :
    *   La commande `git log` vous permet de consulter l'historique de tous les commits effectués, du plus récent au plus ancien.
    *   `git log --oneline` offre une vue abrégée de l'historique.
    *   `git log -p` affiche les différences détaillées (ce qui a été modifié) pour chaque commit.
    *   Git offre des options avancées pour rechercher des commits, filtrer par date, et plus encore. Vous pouvez obtenir de l'aide détaillée en utilisant `git help log`.
*   **Fusion (Merge)** :
    *   Le processus de fusion des modifications d'une branche dans une autre, généralement d'une branche de fonctionnalité vers la branche 'main'.
    *   Utilisez `git merge [nom_de_branche]` pour intégrer les changements.
    *   Si des modifications concurrentes ont été apportées au même fichier dans les deux branches, cela peut entraîner des **conflits de fusion**. Vous devez alors résoudre ces conflits manuellement en éditant le fichier pour choisir les modifications à conserver, puis committer la résolution.
*   **Réinitialisation (`git reset`) et Rebasage (`git rebase`)** :
    *   Git permet de **revenir à des commits précédents** à l'aide de `git reset`.
    *   Le **rebasage** permet de modifier ce qui apparaît dans l'historique des commits et l'ordre dans lequel ils apparaissent, même de fusionner des commits ensemble.
*   **Interactions avec les dépôts distants** : Bien que GitHub soit une plateforme d'hébergement, Git lui-même fournit les commandes pour interagir avec des dépôts distants :
    *   **`git remote`** : Permet de configurer une connexion à un dépôt distant (par exemple, sur GitHub), souvent nommé `origin`.
    *   **`git push`** : Permet d'envoyer les modifications de votre dépôt local vers le dépôt distant. Vous pouvez pousser toutes les branches avec `git push --all`.
    *   **`git pull`** : Télécharge les modifications d'un dépôt distant et les fusionne automatiquement avec votre dépôt local. C'est une combinaison de `git fetch` (télécharger l'historique) et `git merge` (fusionner).

En résumé, Git est un outil puissant pour le **contrôle de version en local**, permettant la gestion détaillée de l'historique des fichiers, la création de branches pour un développement isolé, et la fusion des changements. Il est le fondement sur lequel des plateformes comme GitHub construisent leurs capacités de collaboration.

## Qu'est ce que Github ?

**GitHub** est une **plateforme d'hébergement de dépôts Git dans le cloud** qui facilite la collaboration. C'est une plateforme populaire qui permet de **gérer les projets** et de travailler à plusieurs sur des dépôts Git.

Voici les concepts clés et les fonctionnalités associées de GitHub, selon les sources :

*   **Hébergement de dépôts Git** : GitHub vous permet d'héberger vos dépôts Git dans le cloud. Cela est utile pour la collaboration en équipe, mais aussi pour un travail individuel, car cela fournit une **sauvegarde de vos fichiers de dépôt** si quelque chose arrive à votre ordinateur local.
*   **Plateforme de collaboration et de gestion de projet** :
    *   GitHub est décrit comme un "site de codage social".
    *   Il offre des outils pour gérer des projets, tels que les **tableaux Kanban**, le suivi des **problèmes (Issues)**, et la possibilité d'assigner des fonctionnalités ou des bugs à différentes personnes.
    *   Vous pouvez décider de rendre un dépôt public (n'importe qui peut y accéder) ou privé (vous pouvez assigner l'accès à des individus spécifiques).
*   **Interaction avec Git (dépôts locaux)** :
    *   Vous pouvez établir une **connexion distante** entre votre dépôt Git local et un dépôt GitHub en utilisant la commande `git remote add origin [URL]`. "Origin" est un nom courant pour cette connexion distante.
    *   Les modifications de votre dépôt local peuvent être **envoyées (pushed)** vers GitHub avec la commande `git push`. Vous pouvez envoyer toutes vos branches vers GitHub en utilisant `git push --all`.
    *   Les modifications effectuées sur GitHub (dans le cloud) peuvent être **téléchargées (pulled)** et fusionnées automatiquement dans votre dépôt local avec la commande `git pull`. `git pull` combine `git fetch` (télécharger l'historique des branches de suivi à distance) et `git merge` (fusionner cet historique dans votre machine locale) en une seule commande.
*   **Fonctionnalités Clés sur GitHub** :
    *   **Création de dépôts** : Vous pouvez créer un nouveau dépôt directement sur GitHub. Lors de la création, vous pouvez choisir d'ajouter un fichier README, un fichier `.gitignore` (que vous aviez peut-être créé manuellement localement) ou une licence.
    *   **Visualisation des fichiers et de l'historique** : Vous pouvez voir tous les fichiers de votre dépôt, prévisualiser certains fichiers (comme les images .png), et consulter le dernier changement ou commit pour un fichier spécifique, y compris les détails des modifications.
    *   **Modification de fichiers directement sur GitHub** : Il est possible d'éditer des fichiers directement sur la plateforme et de les *committer*.
    *   **Issues (Problèmes)** : C'est une section où vous pouvez consigner les demandes de fonctionnalités ou les bugs. Les problèmes peuvent être titrés, détaillés, assignés à des collaborateurs, étiquetés (par exemple, "bug"), et liés à des projets ou des jalons. C'est un espace pour la discussion et la priorisation des tâches.
    *   **Pull Requests (Demandes de tirage)** : Une fonctionnalité qui permet de proposer des modifications à une branche (souvent la branche 'main') qui nécessitent une approbation avant d'être fusionnées. Elles facilitent la révision de code par d'autres collaborateurs et la discussion avant l'intégration. Une Pull Request peut être liée à un problème existant, et sa fusion peut automatiquement clôturer le problème correspondant.
    *   **Branches** : GitHub affiche les différentes branches de votre dépôt, comme la branche `main` et d'autres branches comme `UpdateText`.
    *   **Autres Onglets de Projet** :
        *   **Actions** : Pour exécuter différents tests et gérer votre dépôt via des programmes.
        *   **Projects** : Une vue de gestion de projet pour organiser les problèmes et les pull requests.
        *   **Wiki** : Pour documenter votre code, fonctionnant comme une Wikipedia pour votre projet.
        *   **Security (Sécurité)** : Pour gérer les politiques de sécurité, définir des actions en cas de vulnérabilité, et configurer des analyses.
        *   **Insights (Aperçus)** : Pour visualiser les contributions, le trafic, le nombre de problèmes fermés, de commits et de contributeurs.
        *   **Settings (Paramètres)** : Pour configurer divers paramètres du projet, y compris l'ajout de collaborateurs.
    *   **Releases (Versions)** : Vous pouvez créer des versions de votre projet, attribuer des balises et des titres, et permettre aux utilisateurs de télécharger le code source d'une version spécifique.

## Intégration de Git et GitHub

Globalement, Git et GitHub sont deux outils essentiels pour la gestion de versions et la collaboration en développement logiciel. 

Git permet également de gérer des fonctionnalités avancées comme la gestion des branches pour le développement parallèle, la résolution des conflits de fusion, tandis que GitHub est une plateforme de collaboration en ligne, couvrant la création de dépôts cloud, la synchronisation des dépôts locaux, la gestion des problèmes, les "pull requests" et les "releases".

L'intégration de Git et GitHub repose sur leurs rôles complémentaires : Git est l'outil de **contrôle de version local**, tandis que GitHub est une **plateforme d'hébergement et de collaboration en ligne** pour les dépôts Git.

Voici comment Git et GitHub s'intègrent et les avantages qu'ils offrent ensemble :

### Git : Le système de contrôle de version local
Git est un **système de gestion de contrôle de code source (SCM)** gratuit et open source. Sa fonction principale est de vous permettre de **gérer les modifications apportées aux fichiers au fil du temps** et de **revenir en arrière** pour voir ou restaurer ces modifications. Vous pouvez comparer les différences entre les versions et voir qui a modifié quoi.
Toutes les opérations de Git mentionnées précédemment (initialisation de dépôts, création de commits, gestion des branches, réinitialisation, rebasage, etc.) se déroulent initialement sur votre machine locale.

### GitHub : La plateforme d'hébergement et de collaboration
GitHub est une **plateforme d'hébergement** qui vous permet de **collaborer avec d'autres personnes sur vos dépôts Git**. C'est un "dépôt dans le cloud", ou un "site de codage social".

**Pourquoi intégrer Git avec GitHub ?**
L'intégration de votre dépôt Git local avec GitHub offre plusieurs avantages :
*   **Collaboration** : Permet à plusieurs personnes de travailler ensemble sur le même projet.
*   **Sauvegarde** : Stocker votre dépôt dans le cloud assure une sauvegarde de vos fichiers en cas de problème avec votre ordinateur local.
*   **Gestion de projet** : GitHub offre des outils supplémentaires pour la gestion de projet, comme les tableaux Kanban, le suivi des problèmes (issues) et l'affectation de tâches.

### Processus d'intégration et de synchronisation

1.  **Création d'un compte et d'un dépôt GitHub** :
    *   Vous commencez par créer un compte sur le site web de GitHub.
    *   Ensuite, vous créez un **nouveau dépôt (repository) sur GitHub**. Lors de cette création, vous pouvez nommer le dépôt, ajouter une description, choisir s'il est public ou privé, et même y inclure directement un fichier README ou `.gitignore`.

2.  **Connexion du dépôt Git local à GitHub (`git remote add origin`)** :
    *   Une fois votre dépôt GitHub créé, la plateforme vous fournit des commandes pour le connecter à votre dépôt Git local existant.
    *   La première étape consiste souvent à établir une **connexion distante** entre votre dépôt local et celui de GitHub. Ceci est fait en utilisant la commande `git remote add origin [URL_de_votre_repo_GitHub]`. `origin` est un nom courant donné à cette connexion distante.

3.  **Envoi des modifications locales vers GitHub (`git push`)** :
    *   Après avoir committé vos modifications dans votre dépôt Git local, vous pouvez les **pousser (push)** vers le dépôt distant sur GitHub.
    *   La commande `git push` envoie le contenu de votre dépôt local vers le cloud.
    *   Vous pouvez pousser toutes vos branches locales vers GitHub en utilisant `git push --all`.

4.  **Récupération des modifications de GitHub vers le local (`git pull`)** :
    *   Si d'autres collaborateurs ont apporté des modifications et les ont poussées vers GitHub, ou si vous avez effectué des modifications directement sur GitHub, vous pouvez **télécharger ces changements** et les intégrer à votre dépôt local.
    *   Cela peut être fait en deux étapes :
        *   `git fetch` : Télécharge l'historique des modifications depuis les branches distantes.
        *   `git merge` : Fusionne ces modifications téléchargées avec votre dépôt local.
    *   Alternativement, vous pouvez utiliser la commande **`git pull`**, qui combine `git fetch` et `git merge` en une seule opération, téléchargeant et fusionnant automatiquement les fichiers.

### Fonctionnalités de collaboration avancées de GitHub
Au-delà du simple hébergement, GitHub ajoute des couches de fonctionnalités pour la gestion de projet et la collaboration :

*   **Gestion des Fichiers en Ligne** : Vous pouvez prévisualiser les fichiers, voir l'historique des changements (`git log` en ligne), et même **éditer et committer des changements directement sur GitHub** via l'interface web.
*   **Issues (Problèmes)** : Un système pour suivre les requêtes de fonctionnalités, les bugs ou les tâches. Vous pouvez créer de nouvelles issues, leur attribuer un titre et une description, les assigner à des membres de l'équipe, ajouter des étiquettes (labels) comme "bug", et les lier à des projets ou des jalons. Les discussions sur ces problèmes peuvent avoir lieu directement sur la page de l'issue.
*   **Pull Requests (Demandes de Tirage)** : Une fonctionnalité clé de la collaboration. Lorsqu'un développeur travaille sur une nouvelle fonctionnalité ou une correction de bug dans une branche séparée, il peut soumettre une "pull request" pour proposer que ses changements soient fusionnés dans la branche principale (généralement `main`). Cela permet à d'autres membres de l'équipe de **revoir le code**, de discuter des changements et de les approuver avant la fusion. Une pull request peut être liée à une issue, et sa fusion peut automatiquement fermer l'issue correspondante.
*   **Actions** : Permet d'automatiser des flux de travail, comme l'exécution de tests (intégration continue).
*   **Projets** : Une vue de gestion de projet qui regroupe les issues et les pull requests.
*   **Wiki** : Pour documenter le code et le projet, agissant comme une base de connaissances spécifique au projet.
*   **Sécurité** : Gère les politiques de sécurité et peut configurer des analyses de vulnérabilité.
*   **Insights (Aperçus)** : Fournit des statistiques sur les contributions au projet, le trafic, les issues fermées, le nombre de commits, etc..
*   **Paramètres** : Permet de configurer divers aspects du projet, y compris l'ajout de collaborateurs.
*   **Releases (Versions)** : Permet de marquer des points spécifiques dans l'historique du projet comme des versions officielles, rendant le code source téléchargeable pour chaque version.

En résumé, tandis que **Git gère l'historique et les versions des fichiers localement**, **GitHub étend cette capacité au-delà de votre machine**, en fournissant un environnement centralisé pour le stockage, la collaboration, et la gestion de projet, rendant le développement de logiciels en équipe beaucoup plus efficace.

