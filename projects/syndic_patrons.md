---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Data For Humanities
subtitle: Projets aboutis
menubar: menu_projects
toc: true
layout: page
---

# Base des syndicats patronaux en Rhône-Alpes (XIXe-XXe siècles)

------------------------------------------

## Présentation

> Base initialement créée sous Filemaker Pro dans le cadre d'un projet financé. Il n'y a pas de données personnelles. Licence&nbsp;: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
> 
> Elles ont fait l'objet d'une première exploitation dans ce cadre de ce projet, mais peuvent servir de base pour d'autres projets ou bien de base documentaire.
> 
> Les données originelles sont [disponibles au format CSV](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:syndicats_patronaux_rhonealpes.csv.zip). Le séparateur est le symbole pipe, "`|`".
> 
> L'idée est pouvoir mettre ces données à disposition pour qu'elles puissent continuer de vivre et être liées à d'autres données (par exemple celles du [Système d'information patrons et patronat français](http://www.patronsdefrance.fr/)).

------------------------------------------

## Description du jeu de données


### Sources mobilisées

  * Série 10 M des archives départementales, dossiers des syndicats professionnels).
  * Archives des préfectures (registres d'inscription des syndicats professionnels).
  * Annuaires des syndicats professionnels

### Population étudiée

Chaque ligne correspond à un syndicat patronal, tel que défini par la loi de 1884 sur les syndicats professionnel (CIDOC CRM E40_Legal Body).


### Contenu des colonnes

Exploration du contenu des données, avant toute exploitation visuelle et analyse des données, afin de savoir en quoi consiste précisément les données, quel est le contenu de chaque colonne : 

  * quelles sont les différentes modalités présentes et combien de fois elles apparaissent
  * y a-t-il une ou plusieurs informations contenues dans un même champ, 
  * les champs avec plusieurs informations pourront-ils être facilement éclatés ou non, 
  * quel est le type de données (entier, texte, horodatage, boolean) de la colonne ? Est-il systématique ? 

Cette première exploration doit permettre de comprendre ce que contient la colonne au-delà de son label, quelle est la sémantique de son contenu.

Le fichier décrivant le contenu des colonnes&nbsp;:  [ici](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:syndicats_patronaux_rhonealpes_description_contenu.ods).

Dossier contenant un fichier csv par colonne avec la distribution des modalités contenues par chaque colonne&nbsp;: [ici](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:syndicats_patronaux_rhonealpes_description_contenu.ods)


A l'issue de cette exploration il ressort que :

  * certaines colonnes sont vides (nom en rouge) 
  * d'autres sont le résultat d'un calcul (nom en vert). 

Les données de ces dernières ne seront pas importées.

### Préparation du mapping

Chaque ligne du tableau concerne un syndicat patronal.

Syndicat patronal : correspond à la classe **E40 Legal Body** du CIDOC-CRM [Legal Body](http://ontome.dataforhistory.org/class/39) du CIDOC-CRM. En effet, il bénéficie d'une reconnaissance officielle et d'un statut légal (loi de mars 1884). La constitution de la base repose avant tout sur les archives produites par le processus d'enregistrement des syndicats professionnels définit par la loi de 1884, les lois ultérieures la modifiant ou la complétant ainsi que par les arrêtés et circulaires en précisant la mise en oeuvre.


Nouvelle version du fichier ne contenant que les colonnes qui seront traitées (les colonnes correspondant à des champs calculées ou vides ont été exclues) : [ici format .ods](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:syndicats_patronaux_rhonealpes_mapping.ods) et [ici format .xslx](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:syndicats_patronaux_rhonealpes_mapping.xlsx).



