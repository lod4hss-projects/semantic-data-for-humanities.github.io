---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https:__jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Data For Humanities
subtitle: The FAIR principles
toc: false
menubar: menu_guides
layout: page
---

# Production de données FAIR en histoire : bonnes pratiques


### Prendre connaissance des données

La première étape consiste à prendre connaissance du contenu des données que l'on veut restructurer pour les transformer en données FAIR.

Voici un petit script Python qui facilite les choses lorsqu'on doit traiter des données stockées sous forme de tableau dans un tableur. Il permet de prendre connaissance contenu des données contenu dans un ou des tableurs excel (si on dispose d'un fichier .ods ou .csv il suffit de le convertir avec LibreOffice). Le fichier à télécharger  ([ici](https://wiki-arhn.larhra.fr/lib/exe/fetch.php?media=fairdata:exploration_donnees.zip)) est zippé, il doit donc être décompressé.

Le script permet d'obtenir : 
  * à partir d'un tableur avec une seule feuille un autre tableur dont chaque feuille contient la distribution des modalités contenu dans cette colonne. Ainsi, si le tableur de départ contenait un tableau avec 6 colonnes, le fichier de sortie contiendra 6 feuilles et dans chacune d'elle la liste des modalités apparaissant dans la colonne et le nombre d'occurrence de chacune de ces modalités.
  * à partir d'un tableur avec plusieurs feuilles, autant de fichiers qu'il y a de feuilles dans le fichier en entrée. Chaque fichier contient lui-même autant de feuille que de colonne dans le tableau qu'il résume.

N.B. : les tableaux doivent être bien structurés. Notamment éviter :

  * les cellules fusionnées, 
  * les tableaux dont les titres de colonnes comportent des accents et des espaces, 
  * les tableaux avec des lignes vides avant le tableau

Il est aussi préférable d'avoir un encodage en UTF-8.

Le dossier __exploration_donnees__ contient trois sous-dossiers : 

  * le dossier __data__ dans lequel il faut placer le ou les fichiers des tableurs excel que l'on veut explorer ;
  * le dossier __out__ dans lequel on récupère le ou les fichiers produits contenant les distribution des des modalités des colonnes des tableaux traités.
  * le dossier __scripts__ contenant le script python.

Les opérations à effectuer sont les suivantes : 

  * placer le ou les fichiers à explorer dans le dossier __data__
  * ouvrir Spyder (ou un autre IDE)
  * lancer le script (flèche verte dans Spyder). Selon le nombre de fichiers, le nombre de feuilles dans chacun d'eux et le volume des données, il peut être plus ou moins long.
  * récupérer les fichiers avec les distributions dans le dossier __out__


