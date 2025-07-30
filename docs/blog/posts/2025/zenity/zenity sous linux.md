---
date:
  created: 2025-07-30
categories:
  - Markdown
tags:
  - Markdown
draft: true
links:
  - index.md
#readtime: 15
authors:
  - team
---

# Zenity et les boîtes de dialogues sous Linux



**Zenity** est un outil qui permet d'afficher des boîtes de dialogue GTK+ depuis la ligne de commandes ou au travers de scripts shell. Il est similaire à _gdialog_, mais son but est d'être plus simple. Il appartient à la même famille que _dialog_ (affichage de pseudo-boîtes de dialogue en console), _xdialog_ et _cdialog_.

<!-- more -->

## Installation[](https://doc.ubuntu-fr.org/zenity#installation)

Zenity est installé sur Ubuntu par défaut. Sinon, il suffit d'[installer le paquet](https://doc.ubuntu-fr.org/tutoriel/comment_installer_un_paquet "tutoriel:comment_installer_un_paquet") **[zenity](apt://zenity "apt://zenity")**.

Modifier

## Utilisation



| Type de fenêtre       | Argument           | Description                                                  |
| --------------------- | ------------------ | ------------------------------------------------------------ |
| Calendrier            | `--calendar`       | Affiche un calendrier                                        |
| Entrée                | `--entry`          | Permet la saisie de caractères                               |
| Erreur                | `--error`          | Affiche une erreur à l'écran                                 |
| Navigateur de fichier | `--file-selection` | Permet la sélection d'un fichier                             |
| Info                  | `--info`           | Affiche une information                                      |
| Liste                 | `--list`           | Affiche une liste                                            |
| Notification          | `--notification`   | Afficher une notification dans la zone prévue à cet effet    |
| Progress              | `--progress`       | Permet de visualiser le degré d'accomplissement d'une (suite de) tache(s)   à l'aide d'une barre de progression |
| Question              | `--question`       | Affiche une question ( OUI / NON )                           |
| Info texte            | `--text-info`      | Affiche un texte dans une fenêtre                            |
| Avertissement         | `--warning`        | Afficher un avertissement                                    |
| Scale                 | `--scale`          | Choisir une valeur numérique à l'aide d'un curseur           |
| Formulaire            | `--forms`          | Affiche un formulaire (à partir de la version 3.2.0)         |
| Mot de passe          | `--password`       | Demande un mot de passe (peut être utilisé avec 'sudo -S')   |
| Temporisation         | `--timeout`        | Définit le délai d'expiration de la boîte de dialogue en secondes |





### Exemples[](https://doc.ubuntu-fr.org/zenity#exemples)

Voici quelques infos bonus que certaines personnes ont trouvées. Car comme vous pouvez le constater, les infos sur Zenity ne sont pas légion…

Ces fonctions ne semblent pas fonctionner pour les fenêtres “entry”.

Zenity est basé sur GTK+, lui-même basé sur [Pango](http://library.gnome.org/devel/pango/stable/PangoMarkupFormat.html "http://library.gnome.org/devel/pango/stable/PangoMarkupFormat.html"), il est donc possible d'utiliser certaines fonctions de ce logiciel.



#### Coloration du texte[](https://doc.ubuntu-fr.org/zenity#coloration_du_texte)



Fenêtre de test :



``

```
zenity --info --text "
<span color=\"red\">red</span>
<span color=\"green\">green</span>
<span color=\"blue\">blue</span>
<span color=\"yellow\">yellow</span>
<span color=\"magenta\">magenta</span>
<span color=\"white\">white</span>
<span color=\"black\">black</span>
<span color=\"gray\">gray</span>
<span color=\"lightblue\">lightblue</span>
<span color=\"lightgray\">lightgray</span>"
```

#### Choix de la police pour le texte[](https://doc.ubuntu-fr.org/zenity#choix_de_la_police_pour_le_texte)

Marre de voir toujours la même police ? Il vous suffit donc d'utiliser la balise “span font-family”.



`<span font-family=\"Arial\">essai de polices</span>`



Fenêtre de test :



``

```
zenity --info --text "
<span font-family=\"Arial\">essai de polices</span>
<span font-family=\"sans-serif\">essai de polices</span>
<span font-family=\"Helvetica\">essai de polices</span>
<span font-family=\"impact\">essai de polices</span>
<span font-family=\"sans\">essai de polices</span>
<span font-family=\"webdings\">essai de polices</span>"
```



#### Changer la forme de la police[](https://doc.ubuntu-fr.org/zenity#changer_la_forme_de_la_police)

Un mot a besoin de ressortir du reste ? Il suffit de mettre en gras, en italique…



``

```
zenity --info --text "
<b>gras</b>
<big>grand</big>
<i>italique</i>
<s>barré</s>
<sub>indice</sub>
<sup>exposant</sup>
<small>petit</small>
<tt>espace entre les lettres</tt>
<u>souligné</u>"
```



#### Fenêtre avec liste de choix[](https://doc.ubuntu-fr.org/zenity#fenetre_avec_liste_de_choix)

[](https://doc.ubuntu-fr.org/_detail/zenity-entry.png?id=zenity "zenity-entry.png")



Il est possible de créer une fenêtre comme suit :

Pour cela, il faut créer une boite de type “entry” et ajouter les différents choix de la liste à la fin de la commande.

N'oubliez pas les guillemets si vous mettez des espaces dans les réponses. Ex :



``

```
zenity --entry --title="Jour"
--text="Veuillez indiquer le jour de la semaine"
Lundi Mardi Mercredi "Autre jour..."
```



![](https://www.ndu69.com/Screenshots/screenshot_2025-07-30_21-40-55.jpg)



Pour ajouter une réponse de base, utilisez l'option “entry-text” :



``

```
zenity --entry --title="Jour" \
--text="Veuillez indiquer le jour de la semaine" --entry-text="Lundi" Mardi Mercredi
```



#### Boîte de message et récupérer la valeur[](https://doc.ubuntu-fr.org/zenity#boite_de_message_et_recuperer_la_valeur)



``

```
   if ret=`zenity --entry --title='Titre de la vidéo' \ 
   --text='Saisissez le titre de la vidéo : '`
    then
       titre=$ret
          if [ "$titre" = "" ]
          then
        echo "Il faut un titre, tient pan t'es mort!"
        exit
          fi
    else
          echo "Tsss, un titre on dit, pas le bouton annuler!"
    exit
   fi
echo $titre
```



#### Méthode 2 pour récupérer la valeur[](https://doc.ubuntu-fr.org/zenity#methode_2_pour_recuperer_la_valeur)

Voici une méthode alternative à celle décrite ci-dessus :



``

```
dossierSortie=$(zenity --file-selection \
--title="Veuillez selectionner un dossier" \
--text="Choissisez un dossier quelconque" \
--directory);
 
echo ${dossierSortie}
sleep 10
```



#### Méthode 3 pour récupérer la valeur[](https://doc.ubuntu-fr.org/zenity#methode_3_pour_recuperer_la_valeur)

Très simple :



``

```
variable=$(zenity --entry --title="Choix" --text="Indiquez un mot")
 
echo "le mot choisi est "$variable
sleep 5
```



#### Méthode pour récupérer la valeur avec --question[](https://doc.ubuntu-fr.org/zenity#methode_pour_recuperer_la_valeur_avec_--question)



``

```
zenity --question \
--title "coffee" \
--text "Faire du café ?"
 
if [ $? = 0 ]
then
    echo "OUI ! Avec 2 sucres ..."
    sleep 3
else
    echo "NON ! Plutôt du thé ..."
    sleep 3
fi
```



#### Barres de progression[](https://doc.ubuntu-fr.org/zenity#barres_de_progression)

_Depuis [https://help.gnome.org/users/zenity/stable/progress.html.fr](https://help.gnome.org/users/zenity/stable/progress.html.fr "https://help.gnome.org/users/zenity/stable/progress.html.fr")_



| Commande                  | Rôle                                                         |
| ------------------------- | ------------------------------------------------------------ |
| `--text=text`             | Spécifier le texte affiché dans la boîte de dialogue de barre de progression. |
| `--percentage=percentage` | Spécifier le pourcentage initial réglé dans la boîte de dialogue de barre de progression. |
| `--auto-close`            | Fermer la boîte de dialogue quand la barre de progression atteint 100%. |
| `--pulsate`               | Utiliser une barre de progression discontinue jusqu'à ce qu'un caractère EOF soit lu sur l'entrée standard. |



-   Si une ligne commence par '#', le texte est mis à jour avec le texte de cette ligne.
    
-   Si une ligne contient seulement un nombre, le pourcentage est mis à jour avec ce nombre.
    
-   \--progress s'utilise avec un [pipe](https://doc.ubuntu-fr.org/pipe "pipe"). Vous devez donc mettre tout le code affecté par la barre de progression entre parenthèses.



Exemple:



``

```
#!/bin/sh
(
echo "10" ; sleep 1
echo "# Mise à jour des journaux de mail" ; sleep 1
echo "20" ; sleep 1
echo "# Remise à zéro des paramètres" ; sleep 1
echo "50" ; sleep 1
echo "Cette ligne est ignorée" ; sleep 1
echo "75" ; sleep 1
echo "# Redémarrage du système" ; sleep 1
echo "100" ; sleep 1
) |
zenity --progress \
  --title="Mise à jour des journaux système" \
  --text="Analyse des journaux de mail..." \
  --percentage=0
 
if [ "$?" = -1 ] ; then
  zenity --error \
    --text="Mise à jour annulée."
fi
```



_Voir aussi une utilisation concrète dans un script nautilus sur la documentation de [shred](https://doc.ubuntu-fr.org/shred#integrer_shred_a_nautilus_script "shred")_

#### Formulaire



> Cette fonction est disponible depuis la version 3.2.0 de Zenity : cela ne fonctionnera pas avec les versions antérieures.



| Commande                                 | Rôle                                                         |
| ---------------------------------------- | ------------------------------------------------------------ |
| `--text=Texte`                           | Spécifier le texte affiché dans la boîte de dialogue de barre de progression. |
| `--separator=SÉPARATEUR`                 | Définit le caractère séparateur de sortie.                   |
| `--add-entry=Nom du champ`               | Ajoute une nouvelle zone de saisie dans la boîte de dialogue de formulaire. |
| `--add-password=Nom du champ`            | Ajoute une nouvelle zone de saisie de mot de passe dans la boîte de dialogue   de formulaire. |
| `--add-calendar=Nom du champ calendrier` | Ajoute un nouveau calendrier dans la boîte de dialogue de formulaire. |
| `--forms-date-format=MODÈLE`             | Définit le format de la date retournée.                      |



Exemple:



``

```
#!/bin/bash
 
#On crée le formulaire en stockant les valeurs de sortie dans $cfgpass :/
cfgpass=`zenity --forms \
    --title="Exemple qui tue la mort" \
    --text="Définir un nouveau mot de passe" \
    --add-entry="Nom de l'utilisateur" \
    --add-password="Ancien mot de passe" \
    --add-password="Nouveau mot de passe" \
    --add-password="Confirmer le nouveau mot de passe" \
    --separator="|"`
 
#Si on clique sur le bouton Annuler
if [ "$?" -eq 1 ]; then
    #On quitte le script
    exit
fi
#Sinon on continue
#On peut récupérer les valeurs des différents champs de cette façon :
echo "$cfgpass" | cut -d "|" -f1 #Nom de l'utilisateur
echo "$cfgpass" | cut -d "|" -f2 | md5sum #Ancien Mot de passe
echo "$cfgpass" | cut -d "|" -f3 | md5sum #Nouveau Mot de passe
echo "$cfgpass" | cut -d "|" -f4 | md5sum #Confirmation du nouveau mot de passe
 
echo "Franchement la classe cette nouvelle fonction Zenity :P"
```



![](https://www.ndu69.com/Screenshots/screenshot_2025-07-30_21-49-52.jpg)



## Documentation de Zenity[](https://doc.ubuntu-fr.org/zenity#documentation_de_zenity)

Modifier

### Manuels[](https://doc.ubuntu-fr.org/zenity#manuels)

-   [Page officielle de Zenity](https://help.gnome.org/users/zenity/ "https://help.gnome.org/users/zenity/")
    
-   [Choisir sa version >> Manuel de Zenity](https://help.gnome.org/users/zenity/ "https://help.gnome.org/users/zenity/")
    
-   **(fr)** [« Programmation GNU Linux Zenity »](https://wiki.visionduweb.fr/index.php?title=Programmation_GNU_Linux_Zenity "https://wiki.visionduweb.fr/index.php?title=Programmation_GNU_Linux_Zenity") — Manuel en français illustré par des exemples de code
    

Modifier

### Exemples de code : Zenity par l'exemple[](https://doc.ubuntu-fr.org/zenity#exemples_de_codezenity_par_l_exemple)

-   **(fr)** [« Afficher des boîtes de dialogue avec Zenity »](https://www.chicoree.fr/w/Afficher_des_bo%C3%AEtes_de_dialogue_avec_Zenity "https://www.chicoree.fr/w/Afficher_des_bo%C3%AEtes_de_dialogue_avec_Zenity") — source : Chicoree.fr
    
-   **(fr)** [« Zenity a du style ! »](https://forum.ubuntu-fr.org/viewtopic.php?id=232644%20 "https://forum.ubuntu-fr.org/viewtopic.php?id=232644%20") — source : Forum Ubuntu ; sujet : balises HTML fontes et types de fontes dans Zenity
    
-   [Script de génération de fenêtre Zenity](https://doc.ubuntu-fr.org/zenitor_3 "zenitor_3") script compilé jusqu'à Zesty. Ne fonctionne pas pour les versions suivantes d'Ubuntu. Problèmes de dépendances
    
-   [Yad: un fork de Zenity](https://sourceforge.net/projects/yad-dialog/ "https://sourceforge.net/projects/yad-dialog/"): un script multitâches de Zenity