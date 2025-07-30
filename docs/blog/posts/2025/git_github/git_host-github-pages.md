---
date: 2025-07-28
categories:
    - Documentation
tags:
    - Git
    - Github
---

# Comment ajouter un domaine personnalisé aux pages GitHub (édition Hostinger)

[#webdev](https://dev.to/t/webdev) [#tutoriel](https://dev.to/t/tutorial) [#nuage](https://dev.to/t/cloud) [#débutants](https://dev.to/t/beginners)

J'ai récemment terminé mon site Web de portfolio et c'était un rêve devenu réalité d'avoir mon propre petit espace sur Internet. Pour y parvenir, j’ai acheté un nom de domaine chez Hostinger. J'utilisais déjà GitHub Pages pour héberger mon site, j'avais donc besoin d'y ajouter mon nouveau nom de domaine.

Il n'y avait pas de vidéos expliquant comment procéder, j'ai donc parcouru la documentation. Le processus est un peu différent pour Hostinger, mais si vous êtes comme moi et que vous souhaitez configurer les choses rapidement, vous pouvez suivre cet article de blog.

> Se référer à [cette](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

**Étape 1 : Accédez aux paramètres DNS de votre domaine Hostinger**

La première étape consiste à accéder aux paramètres DNS de votre domaine Hostinger. Vous pouvez le faire en visitant [https://hpanel.hostinger.com/domain/yourdomain.com/dns](https://hpanel.hostinger.com/domain/yourdomain.com/dns). Par exemple, [https://hpanel.hostinger.com/domain/sidharthmohanty.com/dns](https://hpanel.hostinger.com/domain/sidharthmohanty.com/dns).

**Étape 2 : Supprimer l'enregistrement CNAME existant et l'enregistrement de type A**

Par défaut, il devrait y avoir un enregistrement CNAME pour votre domaine. Cet enregistrement pointe votre domaine vers le site Web par défaut de Hostinger. Nous devons supprimer cet enregistrement afin de pouvoir créer un nouvel enregistrement CNAME qui pointe vers notre site GitHub Pages. Supprimez également toute valeur par défaut `A` tapez les enregistrements afin qu'il n'y ait pas de collision ou de conflit.

**Étape 3 : Créer deux nouveaux enregistrements CNAME**

Nous devons créer deux nouveaux enregistrements CNAME. Le premier record pointera `www.yourdomain.com` à `<your-github-username>.github.io`. Le deuxième record pointera `yourdomain.com` à `<your-github-username>.github.io`.

-   Entrez le type - CNAME, le nom - www, les points vers - .github.io, TTL que vous pouvez laisser par défaut. C'est pour quand quelqu'un tape `www.yourdomain.com`.
-   Ensuite, nous avons besoin de la même chose pour les domaines APEX ou lorsque quelqu'un tape simplement `yourdomain.com`, pour cela, entrez un autre CNAME avec le nom - @ et pointe vers .github.io. Cela définira automatiquement un type ALIAS et l'ajoutera aux enregistrements DNS.

Cela devrait ressembler à ceci une fois ajouté,

[![Enregistrements CNAME](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fvuii527quhbgc6dhya4l.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fvuii527quhbgc6dhya4l.png)

**Étape 4 : Ajouter les adresses IP des pages GitHub**

Enfin, nous devons ajouter les adresses IP des pages GitHub à nos enregistrements DNS. Ajouter un type, Nom - @, TTL peut être laissé comme enregistrements par défaut pour chacune des adresses IP suivantes (doit être copié et collé dans “Points to”)  

    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153
    

Enter fullscreen mode Exit fullscreen mode

Une fois que vous avez ajouté les adresses IP, vos enregistrements DNS devraient ressembler à ceci :

[![IP GitHub ajoutées](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fkg06mya6tuifq4v173di.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fkg06mya6tuifq4v173di.png)

**Étape 5 : Ajoutez le domaine personnalisé aux pages GitHub**

La dernière étape consiste à ajouter le domaine personnalisé aux pages GitHub. Vous pouvez le faire en accédant à votre référentiel GitHub et en cliquant sur le **Paramètres** tab. Ensuite, cliquez sur le **Pages** onglet et entrez votre domaine personnalisé dans le **Domaine personnalisé** champ.

[![Domaine personnalisé GitHub](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fkyzldwyetx7pdtykkmln.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fkyzldwyetx7pdtykkmln.png)  
[![Vérification DNS réussie](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F2aa6o4z2om9gyqjxllc2.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F2aa6o4z2om9gyqjxllc2.png)

Cela devrait fonctionner dès le départ si vous utilisez une branche “” pour déployer votre site, car GitHub ajoute un fichier CNAME à la branche, mais si vous utilisez un générateur de site statique, vous devez l'ajouter manuellement à votre `public` dossier.

`public/CNAME`(devrait être un capital sans extension)  

    yourdomain.com
    

Enter fullscreen mode Exit fullscreen mode

> Se référer à [cette](https://github.com/sidmohanty11/sidmohanty11.github.io/blob/main/public/CNAME).

Une fois que vous avez suivi toutes ces étapes, vous devriez pouvoir accéder à votre site Web en visitant `https://yourdomain.com`.

**Félicitations !** Vous avez maintenant ajouté avec succès un domaine personnalisé aux pages GitHub.

Merci d'avoir lu ce post ✨. Faites-moi savoir si vous le trouvez utile. Si vous souhaitez voir mon portfolio ou ce que je fais, vous pouvez visiter mon site Web à l'adresse [https://sidharthmohanty.com/](https://sidharthmohanty.com/).