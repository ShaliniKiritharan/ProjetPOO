# Projet Programmation orienté objet 2022-2023

## L2-Informatique Groupe A

### Auteurs: Ahcene ALOUANE/ Shalini Kiritharan

#### Objectifs du projet
  * Exploration complètes d'un repertoire pour retenir seulement les fichiers ODT
  * Extraction des métadonnées d'un fichier ODT
  * Modification de métadonnées( le titre du fichier)

##### Les procédés pour répondre aux différentes foctionalités demandées:
  * Explication de la partie exploration d'un repertoire: Le programme prend en entrée le chemin d'un repertoire. L'analyse du type mime des fichiers contenues dans ce répertoire et dans les sous répertoires perment de retenir seulement les Fichiers Odt. Pour analiser les sous répertoires, nous avanons utilisé la récursivité.
  * Explication pour l'extarcation et la modification des métadonnées d'un fichier Odt: Au départ le programme prend en paramètre un fichier Odt. Pour analiser les métadonnées de ce fichier, il est utile de le renommer en .zip afin d'obtenir un dossier compressé dans lequel figurent des fichiers xml et des sous répertoires contenant les images,le contenue du fichier odt, ... Après avoir renommé, l'étape suivante est de décompresser ce repetoire zip qui permet d'accéder à ses contenes. 
Le fichier Meta.xml contient les métadonnées telles que le titre, le sujet, le nombre de paragraphe, le nombre de caractère, ...    L'outil qui permet d'analiser le fichier Xml est le "JAVA DOM PARSER" , un pacage qui existe en java. En effet, dans ce pacquage il existe des méthodes qui permettent d'analiser, de lire et de modififiers le contenue d'un fichier xml. Pour visualiser les modifications faites dans le fichier meta.xml, nous avons recompressé et renommé en .odt le repertoire décompressé afin d'obtenir le fichier ODT de départ mais aves les changements.

#### Les différentes classes utilisées pour la partie console de notre logiciel:
  * Exploration : Cette classe permet d'explorer un répertoire donné pour retenir seulement les fichiers Odt
  * Decompression : Cette classe permet décompresser un dossier décompressé
  * Meta : Cette classe permet d'extraire les métadonnées du fichier XMl
  * ModifyXmlDomParser : Cette classe permet de modifier les métadonnées
  * Compression : Cette classe permet de compresser un répertoire
  * Test : Cette classe permet de tester notre application en mode console

#### Les différentes classes utilisés pour la partie graphique de notre logiciel:
  * ExplorationInterface : Cette classe permet d'avoir un fenêtre qui explore un repertoire donné pour afficher les fichies odt contenus dedans
  * ExtractionInterface : Cette classe permet d'avoir un fenêtre qui affiche les métadonnées d'un fichier Odt et de modifier son titre. 
  * MainInterface : Cette classe permet d'avoir une fenêtre principale qui revoie au deux autres fnêtres citées au-dessus selon le choix de l'utilisateur.

#### Le scénarios d'exécution (Les commandes à utiliser)
  * java -jar cli.jar ( Cette commande indique qu'il manque des parametres et propose de taper "--hep" pour avoir l'aide.
  * java -jar cli.jar --help (Cette commande indique les options possibles de notre logiel avec ses rôles.
  * java -jar cli.jar -d . (Cette commande permet l'exploration complète du répertoire courant pour affciher Seulement les fichiers Odt)
  * java -jar cli.jar -f nomFichierOdt (Cette commande prend en etrée un fichier odt et affciche ses métadonnées)
  * java -jar cli.jar -f nomFichier --tilte "titre à remplacer" (Cette commande modifie le titre du fichier odt donné
  * java -jar gui.jar (Cette commande permet de lancer l'interface graphique de notre logicel)
