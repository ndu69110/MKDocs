---
date:
  created: 2025-07-30
categories:
  - Markdown
tags:
  - Markdown
  - Visual Studio Code
draft: true
links:
  - index.md
#readtime: 15
authors:
  - team
---

# Mise en route : à la découverte de Markdown

## Qu'est-ce que Markdown ?

Markdown est un langage de balisage léger que vous pouvez utiliser pour ajouter des éléments de formatage aux documents texte en clair. Créé par [John Gruber](https://daringfireball.net/projects/markdown/) en 2004, Markdown est désormais l'un des langages de balisage les plus populaires au monde.

L'utilisation de Markdown est différente de l'utilisation d'un [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) éditeur. 

<!-- more -->

Dans une application comme Microsoft Word, vous cliquez sur des boutons pour formater des mots et des phrases, et les modifications sont visibles immédiatement. Markdown n'est pas comme ça. Lorsque vous créez un fichier au format Markdown, vous ajoutez la syntaxe Markdown au texte pour indiquer quels mots et expressions doivent avoir une apparence différente.

Par exemple, pour désigner un titre, vous ajoutez un signe numérique avant lui (par exemple, `# Heading One`). Ou pour mettre une phrase en gras, vous ajoutez deux astérisques avant et après (par exemple, `**this text is bold**`). Il faudra peut-être un certain temps pour s'habituer à voir la syntaxe Markdown dans votre texte, surtout si vous êtes habitué aux applications WYSIWYG. La capture d'écran ci-dessous montre un fichier Markdown affiché dans le [Éditeur de texte Visual Studio Code](https://www.markdownguide.org/tools/vscode/).

![](https://www.ndu69.com/Screenshots/screenshot_2025-07-30_21-05-09.jpg)

Vous pouvez ajouter des éléments de formatage Markdown à un fichier texte en clair à l'aide d'une application d'édition de texte. Vous pouvez également utiliser l’une des nombreuses applications Markdown pour les systèmes d’exploitation macOS, Windows, Linux, iOS et Android. Il existe également plusieurs applications Web spécialement conçues pour écrire dans Markdown.

Selon l'application que vous utilisez, vous ne pourrez peut-être pas prévisualiser le document formaté en temps réel. Mais ce n'est pas grave. [Selon Gruber](https://daringfireball.net/projects/markdown/), La syntaxe Markdown est conçue pour être lisible et discrète, afin que le texte des fichiers Markdown puisse être lu même s'il n'est pas rendu.

> L’objectif de conception primordial de la syntaxe de formatage de Markdown est de la rendre aussi lisible que possible. L'idée est qu'un document au format Markdown doit être publiable tel quel, sous forme de texte brut, sans donner l'impression qu'il a été balisé avec des balises ou des instructions de formatage.

**En résumé, Markdown est un outil de conversion de texte en HTML destiné aux rédacteurs web. Markdown vous permet d'écrire dans un format texte brut facile à lire et à écrire, puis de le convertir en HTML structurellement valide.**

---

## Pourquoi utiliser Markdown ?

Vous vous demandez peut-être pourquoi les gens utilisent Markdown au lieu d’un éditeur WYSIWYG. Pourquoi écrire avec Markdown quand vous pouvez appuyer sur des boutons dans une interface pour formater votre texte ? Il s’avère qu’il existe plusieurs raisons pour lesquelles les gens utilisent Markdown au lieu des éditeurs WYSIWYG.

- Markdown peut être utilisé pour tout. Les gens l'utilisent pour créer [sites web](https://www.markdownguide.org/getting-started/#websites), [documents](https://www.markdownguide.org/getting-started/#documents), [notes](https://www.markdownguide.org/getting-started/#notes), [livres](https://www.markdownguide.org/getting-started/#books), [présentations](https://www.markdownguide.org/getting-started/#presentations), [messages électroniques](https://www.markdownguide.org/getting-started/#email), et [documentation technique](https://www.markdownguide.org/getting-started/#documentation).
- Markdown est portable. Les fichiers contenant du texte au format Markdown peuvent être ouverts à l'aide de pratiquement n'importe quelle application. Si vous décidez que vous n'aimez pas l'application Markdown que vous utilisez actuellement, vous pouvez importer vos fichiers Markdown dans une autre application Markdown. Cela contraste fortement avec les applications de traitement de texte comme Microsoft Word qui verrouillent votre contenu dans un format de fichier propriétaire.
- Markdown est indépendant de la plateforme. Vous pouvez créer du texte au format Markdown sur n’importe quel appareil exécutant n’importe quel système d’exploitation.
- Markdown est une preuve d'avenir. Même si l'application que vous utilisez cesse de fonctionner à un moment donné dans le futur, vous pourrez toujours lire votre texte au format Markdown à l'aide d'une application d'édition de texte. Il s’agit d’une considération importante lorsqu’il s’agit de livres, de thèses universitaires et d’autres documents marquants qui doivent être conservés indéfiniment.
- Markdown est partout. Sites Web comme [Reddit](https://www.markdownguide.org/tools/reddit/) et GitHub prend en charge Markdown, et de nombreuses applications de bureau et Web le prennent en charge.

---

## Licence

Markdown est un logiciel libre, disponible sous une licence open source de type BSD. Consultez la page [Licence](https://daringfireball.net/projects/markdown/license) pour plus d'informations.

---

## Donner un coup de pied dans les pneus

La meilleure façon de commencer avec Markdown est de l’utiliser. C'est plus facile que jamais grâce à une variété d'outils gratuits.

Vous n'avez même pas besoin de télécharger quoi que ce soit. Il existe plusieurs éditeurs Markdown en ligne que vous pouvez utiliser pour essayer d'écrire dans Markdown. [Dillinger](https://dillinger.io/) est l'un des meilleurs éditeurs Markdown en ligne. Ouvrez simplement le site et commencez à taper dans le volet de gauche. Un aperçu du document rendu apparaît dans le volet de droite.

![](https://www.ndu69.com/Screenshots/screenshot_2025-07-30_21-08-12.jpg)

Vous souhaiterez probablement garder le site Web de Dillinger ouvert pendant que vous lisez ce guide. De cette façon, vous pouvez essayer la syntaxe au fur et à mesure que vous en apprenez davantage. Une fois que vous vous êtes familiarisé avec Markdown, vous souhaiterez peut-être utiliser une application Markdown qui peut être installée sur votre ordinateur de bureau ou votre appareil mobile.

---

## Comment ça marche ?

Dillinger facilite l'écriture dans Markdown car il cache ce qui se passe dans les coulisses, mais il vaut la peine d'explorer le fonctionnement du processus en général.

Lorsque vous écrivez dans Markdown, le texte est stocké dans un fichier texte brut doté d'un `.md` ou `.markdown` extension. Mais alors quoi ? Comment votre fichier au format Markdown est-il converti en HTML ou en document prêt à imprimer ?

La réponse courte est que vous avez besoin d’un *Application Markdown* capable de traiter le fichier Markdown. Il existe de nombreuses applications disponibles — allant des scripts simples aux applications de bureau qui ressemblent à Microsoft Word. Malgré leurs différences visuelles, toutes les applications font la même chose. Comme Dillinger, ils convertissent tous le texte au format Markdown en HTML afin qu'il puisse être affiché dans les navigateurs Web.

Les applications Markdown utilisent ce qu'on appelle un *Processeur Markdown* (également communément appelé “analyseur” ou “implémentation”) pour prendre le texte au format Markdown et le sortir au format HTML. À ce stade, votre document peut être consulté dans un navigateur Web ou combiné avec une feuille de style et imprimé. Vous pouvez voir une représentation visuelle de ce processus ci-dessous.

>  **Remarque :** L'application Markdown et le processeur sont deux composants distincts. Par souci de concision, je les ai combinés en un seul élément (« application Markdown ») dans la figure ci-dessous.

![](https://www.ndu69.com/Screenshots/screenshot_2025-07-30_21-09-17.jpg)

Pour résumer, il s’agit d’un processus en quatre parties :

1. Créez un fichier Markdown à l'aide d'un éditeur de texte ou d'une application Markdown dédiée. Le fichier doit avoir un `.md` ou `.markdown` extension.
2. Ouvrez le fichier Markdown dans une application Markdown.
3. Utilisez l'application Markdown pour convertir le fichier Markdown en document HTML.
4. Affichez le fichier HTML dans un navigateur Web ou utilisez l'application Markdown pour le convertir dans un autre format de fichier, comme PDF.

De votre point de vue, le processus variera quelque peu en fonction de l’application que vous utilisez. Par exemple, Dillinger combine essentiellement les étapes 1 à 3 en une seule interface transparente — tout ce que vous avez à faire est de taper dans le volet de gauche et la sortie rendue apparaît comme par magie dans le volet de droite. Mais si vous utilisez d’autres outils, comme un éditeur de texte avec un générateur de site Web statique, vous constaterez que le processus est beaucoup plus visible.

---

## À quoi sert Markdown ?

Markdown est un moyen rapide et simple de prendre des notes, de créer du contenu pour un site Web et de produire des documents prêts à imprimer.

Il ne faut pas longtemps pour apprendre la syntaxe Markdown, et une fois que vous savez comment l'utiliser, vous pouvez écrire en utilisant Markdown à peu près partout. La plupart des gens utilisent Markdown pour créer du contenu pour le Web, mais Markdown est idéal pour formater tout, des messages électroniques aux listes de courses.

Voici quelques exemples de ce que vous pouvez faire avec Markdown.

### Sites Web

Markdown a été conçu pour le Web, il n’est donc pas surprenant qu’il existe de nombreuses applications spécifiquement conçues pour créer du contenu de site Web.

Si vous recherchez le moyen le plus simple possible de créer un site Web avec des fichiers Markdown, consultez [tache.im](https://blot.im/). Après votre inscription à Blot, il crée un dossier Dropbox sur votre ordinateur. Faites simplement glisser et déposez vos fichiers Markdown dans le dossier et — pouf ! — ils sont sur votre site Web. Ça ne pourrait pas être plus facile.

Si vous connaissez HTML, CSS et le contrôle de version, consultez [Jekyll](https://www.markdownguide.org/tools/jekyll/), un générateur de site statique populaire qui prend des fichiers Markdown et crée un site Web HTML. L’un des avantages de cette approche est que [Pages GitHub](https://www.markdownguide.org/tools/github-pages/) fournit un hébergement gratuit pour les sites Web générés par Jekyll. Si Jekyll n'est pas votre tasse de thé, choisissez-en un [de nombreux autres générateurs de sites statiques disponibles](https://jamstack.org/generators/).

 **Remarque :** Prise sans vergogne ! Si vous souhaitez apprendre à créer des sites Web statiques à partir de zéro, consultez [*Le guide du site statique*](https://www.staticguide.org/), un autre livre que j'ai écrit.

Si vous souhaitez utiliser un système de gestion de contenu (CMS) pour alimenter votre site Web, jetez un œil à [Fantôme](https://www.markdownguide.org/tools/ghost/). C'est une plateforme de blogs gratuite et open source avec un bel éditeur Markdown. Si vous êtes un utilisateur de WordPress, vous serez heureux de savoir qu'il existe [Prise en charge de Markdown](https://wordpress.com/support/wordpress-editor/blocks/markdown-block/) pour les sites Web hébergés sur WordPress.com. Les sites WordPress auto-hébergés peuvent utiliser le [Plugin Jetpack](https://jetpack.com/support/jetpack-blocks/markdown/).

### Documents

Markdown n'a pas toutes les cloches et sifflets des traitements de texte comme Microsoft Word, mais il est assez bon pour créer des documents de base comme des devoirs et des lettres. Vous pouvez utiliser une application de création de documents Markdown pour créer et exporter des documents au format Markdown au format de fichier PDF ou HTML. La partie PDF est essentielle, car une fois que vous avez un document PDF, vous pouvez tout en faire — l'imprimer, l'envoyer par e-mail ou le télécharger sur un site Web.

Voici quelques applications de création de documents Markdown que je recommande :

- **Mac :** [MacDown](https://www.markdownguide.org/tools/macdown/), [IA Écrivain](https://www.markdownguide.org/tools/ia-writer/), ou [Marqué 2](https://www.markdownguide.org/tools/marked-2/)
- **iOS / Android :** [IA Écrivain](https://www.markdownguide.org/tools/ia-writer/)
- **Fenêtres :** [nègre](https://kde.github.io/ghostwriter/) ou [Monstre de Markdown](https://markdownmonster.west-wind.com/)
- **Linux :** [ReText](https://github.com/retext-project/retext) ou [nègre](https://kde.github.io/ghostwriter/)
- **Web :** [Dillinger](https://www.markdownguide.org/tools/dillinger/) ou [StackModifier](https://www.markdownguide.org/tools/stackedit/)

### Notes

À presque tous les égards, Markdown est la syntaxe idéale pour prendre des notes. Malheureusement, [Evernote](https://evernote.com/) et [Une note](https://www.onenote.com/), deux des applications de notes les plus populaires, ne prennent actuellement pas en charge Markdown. La bonne nouvelle est que plusieurs autres applications de notes *do* soutenir Markdown :

- [Obsidienne](https://www.markdownguide.org/tools/obsidian/) est une application de prise de notes Markdown populaire chargée de fonctionnalités.
- [Simplenote](https://www.markdownguide.org/tools/simplenote/) est une application de prise de notes gratuite et simple disponible pour toutes les plateformes.
- [Notable](https://www.markdownguide.org/tools/notable/) est une application de prise de notes qui fonctionne sur une variété de plates-formes.
- [Ours](https://www.markdownguide.org/tools/bear/) est une application de type Evernote disponible pour les appareils Mac et iOS. Il n'utilise pas exclusivement Markdown par défaut, mais vous pouvez activer le mode de compatibilité Markdown.
- [Joplin](https://www.markdownguide.org/tools/joplin/) est une application de prise de notes qui respecte votre vie privée. Il est disponible pour toutes les plateformes.
- [Note d'amplification](https://www.markdownguide.org/tools/boostnote/) se présente comme une “application open source de prise de notes conçue pour les programmeurs.”

Si vous ne pouvez pas vous séparer d'Evernote, consultez [Marxique](https://marxi.co/), un éditeur Markdown par abonnement pour Evernote, ou utilisez [Markdown ici](https://www.markdownguide.org/tools/markdown-here/) avec le site Evernote.

### Livres

Vous cherchez à auto-éditer un roman ? Essayer [Leanpub](https://leanpub.com/), un service qui prend vos fichiers au format Markdown et les transforme en livre électronique. Leanpub génère votre livre au format de fichier PDF, EPUB et MOBI. Si vous souhaitez créer des copies de poche de votre livre, vous pouvez télécharger le fichier PDF sur un autre service tel que [Édition directe Kindle](https://kdp.amazon.com/). Pour en savoir plus sur l'écriture et l'auto-édition d'un livre à l'aide de Markdown, lisez [cet article de blog](https://medium.com/techspiration-ideas-making-it-happen/how-i-wrote-and-published-my-novel-using-only-open-source-tools-5cdfbd7c00ca).

### Présentations

Croyez-le ou non, vous pouvez générer des présentations à partir de fichiers au format Markdown. Créer des présentations dans Markdown demande un peu de temps pour s'y habituer, mais une fois que vous avez compris, c'est beaucoup plus rapide et plus facile que d'utiliser une application comme PowerPoint ou Keynote. [Remarque](https://remarkjs.com/) ([Projet GitHub](https://github.com/gnab/remark)) est un outil de diaporama Markdown populaire basé sur un navigateur, tel quel [Cleaver](https://jdan.github.io/cleaver/) ([Projet GitHub](https://github.com/jdan/cleaver)) et [Marp](https://marp.app/) ([Projet GitHub](https://github.com/marp-team/marp)). Si vous utilisez un Mac et préférez utiliser une application, consultez [Pont](https://www.decksetapp.com/) ou [Hyperdeck](https://hyperdeck.io/).

### Email

Si vous envoyez beaucoup d'e-mails et que vous en avez assez des contrôles de formatage disponibles sur la plupart des sites Web des fournisseurs de messagerie, vous serez heureux d'apprendre qu'il existe un moyen simple d'écrire des messages électroniques à l'aide de Markdown. [Markdown ici](https://www.markdownguide.org/tools/markdown-here/) est une extension de navigateur gratuite et open source qui convertit le texte au format Markdown en HTML prêt à être envoyé.

### Collaboration

Les applications de collaboration et de messagerie d’équipe sont un moyen populaire de communiquer avec des collègues et des amis au travail et à la maison. Ces applications n'utilisent pas toutes les fonctionnalités de Markdown, mais les fonctionnalités qu'elles fournissent sont assez utiles. Par exemple, la possibilité de mettre du texte en gras et en italique sans utiliser l’interface WYSIWYG est assez pratique. [Slack](https://www.markdownguide.org/tools/slack/), [Discorde](https://www.markdownguide.org/tools/discord/), [Wiki.js](https://www.markdownguide.org/tools/wiki-js/), et [Mattermost](https://www.markdownguide.org/tools/mattermost/) sont toutes de bonnes applications de collaboration.

### Documentation

Markdown convient naturellement à la documentation technique. Des entreprises comme GitHub se tournent de plus en plus vers Markdown pour leur documentation — consultez leur [article de blog](https://github.com/blog/1939-how-github-uses-github-to-document-github) sur la façon dont ils ont migré leur documentation au format Markdown vers [Jekyll](https://www.markdownguide.org/tools/jekyll/). Si vous rédigez de la documentation pour un produit ou un service, jetez un œil à ces outils pratiques :

- [Lisez les documents](https://readthedocs.org/) peut générer un site Web de documentation à partir de vos fichiers Markdown open source. Connectez simplement votre référentiel GitHub à leur service et poussez — Read the Docs fait le reste. Ils ont aussi un [service pour les entités commerciales](https://readthedocs.com/).
- [MkDocs](https://www.markdownguide.org/tools/mkdocs/) est un générateur de site statique rapide et simple destiné à la création de documentation de projet. Les fichiers sources de documentation sont écrits en Markdown et configurés avec un seul fichier de configuration YAML. MkDocs en a plusieurs [thèmes intégrés](https://www.mkdocs.org/user-guide/styling-your-docs/), y compris un port du [Lisez les documents](https://readthedocs.org/) thème de documentation à utiliser avec MkDocs. L’un des thèmes les plus récents est [Matériel MkDocs](https://squidfunk.github.io/mkdocs-material/).
- [Docusaurus](https://www.markdownguide.org/tools/docusaurus/) est un générateur de sites statiques conçu exclusivement pour la création de sites Web de documentation. Il prend en charge les traductions, la recherche et la gestion des versions.
- [VuePress](https://vuepress.vuejs.org/) est un générateur de site statique alimenté par [Vue](https://vuejs.org/) et optimisé pour la rédaction de documentation technique.
- [Jekyll](https://www.markdownguide.org/tools/jekyll/) a été mentionné plus tôt dans la section sur les sites Web, mais c'est également une bonne option pour générer un site Web de documentation à partir de fichiers Markdown. Si vous empruntez cet itinéraire, assurez-vous de consulter le [Thème de documentation Jekyll](https://idratherbewriting.com/documentation-theme-jekyll/).

---

## Saveurs de Markdown

L’un des aspects les plus déroutants de l’utilisation de Markdown est que pratiquement toutes les applications Markdown implémentent une version légèrement différente de Markdown. Ces variantes de Markdown sont communément appelées *saveurs*. C'est votre travail de maîtriser n'importe quelle version de Markdown que votre application a implémentée.

Pour comprendre le concept des saveurs Markdown, il peut être utile de les considérer comme des dialectes linguistiques. Les habitants de New York parlent anglais tout comme ceux de Londres, mais il existe des différences substantielles entre les dialectes utilisés dans les deux villes. Il en va de même pour les personnes utilisant différentes applications Markdown. Utilisation [Dillinger](https://www.markdownguide.org/tools/dillinger/) écrire avec Markdown est une expérience très différente de celle utilisée [Ulysse](https://www.markdownguide.org/tools/ulysses/).

Practically speaking, this means you never know exactly what a company means when they say they support “Markdown.” Are they talking about only the [basic syntax elements](https://www.markdownguide.org/basic-syntax/), or all of the basic and [extended syntax elements](https://www.markdownguide.org/extended-syntax/) combined, or some arbitrary combination of syntax elements? You won’t know until you read the documentation or start using the application.

Si vous débutez, le meilleur conseil que je puisse vous donner est de choisir une application Markdown avec un bon support Markdown. Cela contribuera grandement à maintenir la portabilité de vos fichiers Markdown. Vous souhaiterez peut-être stocker et utiliser vos fichiers Markdown dans d’autres applications, et pour ce faire, vous devez commencer par une application qui offre un bon support. Vous pouvez utiliser le [répertoire des outils](https://www.markdownguide.org/tools/) pour trouver une application qui correspond à vos attentes.

---

## Ressources supplémentaires

Il existe de nombreuses ressources que vous pouvez utiliser pour apprendre Markdown. Voici quelques autres ressources d’introduction :

- [Documentation Markdown de John Gruber](https://daringfireball.net/projects/markdown/). Le guide original écrit par le créateur de Markdown.
- [Tutoriel Markdown](https://www.markdowntutorial.com/). Un site Web open source qui vous permet d'essayer Markdown dans votre navigateur Web.
- [Superbe Markdown](https://github.com/mundimark/awesome-markdown). Une liste d'outils Markdown et de ressources d'apprentissage.
- [Composition Markdown](https://dave.autonoma.ca/blog/2019/05/22/typesetting-markdown-part-1). Une série en plusieurs parties qui décrit un écosystème de composition de documents Markdown à l'aide de [pandoc](https://pandoc.org/) et [ConTeXt](https://www.contextgarden.net/).