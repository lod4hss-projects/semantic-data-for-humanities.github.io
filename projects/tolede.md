---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Data For Humanities
subtitle: Projets aboutis
menubar: menu_projects
toc: true
layout: page
---

# Chantier : La maison médiévale à Tolède (XIVe-XVIe)

--------------------------------------------------------

## Présentation

> Il s'agit de rendre FAIR de jeux de données associés au projet "Toledo medieval: Espacio y Tiempo" ([site officiel](http://toledo.medievalgis.fr/)), par le biais d'une modélisation fondée sur CIDOC CRM.
> 
> Auteurs : Jean Passini (CNRS/EHESS), Jean Pierre Molènat (CNRS/IRHT).
> 
> Contact chantier : Carmen Brando (EHESS).

Lors des dernières années, les chercheurs du projet ont pu constituer plusieurs jeux de données à partir du travail sur le terrain et de la consultation d'archives à Tolède. 

  * Maisons, répertorie les pièces des maisons médiévales à Tolède avec leurs fonction et mesures (créateur: Jean Passini). [maisons_v09072020.xls](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:maisons_v09072020.xls)
  * Impots, l'évolution des tribus ou "impôt" que chaque habitant devait payer au XVIème siècle à l'église (créateur: Jean Pierre Molènat). [impots.7z](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:impots.7z).
  * Contrats/transactions, liste des contrats d'achat de maisons par des habitants de Tolède (créateur: Jean Passini). [contrats.xls](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:contrats.xls)

J'ai eu la permission des auteurs pour mettre les données en ligne.
Après avoir complété et retravaillé ces données, elles seront publiées dans un entrepôt de données de la recherche SHS comme Nakala (CNRS) ou Didomena (Ehess), et exploitées dans un SI géohistorique.

---------------------------------------------------

## Sources

Archivo Catedral Toledo (ACT), fondo Obras Fábricas, cotas OF 356 y OF 356 bis. 
Ces archives sont localisées dessus d'une chapelle de la Catedral de Toledo.

----------------------------------------------------

## Publications associées

> Toledo a finales de la edad media / Jean Passini, Jean-Pierre Molénat / Toledo : Colegio Oficial de Arquitectos de castilla-la-Mancha , 1995

------------------------------------------------------

## Description détaillée des données

### Maisons

Chaque entrée correspond à une pièce d'une maison et chacune des pièces ont un code, année attestée, fonction, code de la maison, mesures et surface en varas, ... Ce fichier a été créé à partir d'une compilation de textes transcrits décrivant les maisons sur deux années, en 1439 et 1492. La sémantique des colonnes du fichier est décrite ci-dessous.

* Colonne A (CODE_PIECE_COMPLET) : code unique créé par le chercheur pour identifier la pièce concernée, il comprend aussi le code du quartier ainsi que de la maison ;
* Colonne B (CODE_MAISON_COMPLET) : code complet créé par le chercheur pour identifier la maison de la pièce correspondante, il comprend aussi le code du quartier ainsi que de la maison ;
* Colonne C (ANNEE) : année à laquelle l'existence de la maison est attestée par la source ; 
* Colonne D (FONCTION_PIECE) : function de la pièce parfois avec information de contexte, l'orthographe est celle de la source, dans une transcription réalisé par un paléographe, donc le vocabulaire est celui du texte.
* Colonne E (CODE_QUARTIER) : code du quartier où se trouve la maison de la pièce concernée ;
* Colonne F (CODE_MAISON) : code de la maison où se trouve la pièce concernée ; 
* Colonne G (CODE_PIECE) : code de la pièce concernée ; 
* Colonne H (SITUATION_PIECE_NIVEAU) : situation de la pièce suivant le niveau ;
* Colonne I (N_PIECE_NIVEAU) : nombre de pièces par niveau ;
* Colonne J (LONGUEUR_VARAS) : longueur de la pièce en varas ; 
* Colonne K (LARGEUR_VARAS) : largeur de la pièce en varas ;
* Colonne L (SURFACE_VARAS) : surface en varas ;
* Colonne M (LONGUEUR_METRES) : longueur de la pièce en mètres ;
* Colonne N (LARGEUR_METRES) : largeur de la pièce en mètres ;
* Colonne O (SURFACE_METRES): surface en mètres ;
* Colonne P (RAPPORT_LONG_LARG) : rapport long/larg estimé, c'est important car il détermine une période (Islamique, XII-XII-XIV-XV siècle) ;
* Colonne Q (TEXT_SITUATION) : expression (approx.) dans la source qui situe la maison (ex. cerca, ensomo, en la entrada), le vocabulaire est intéressant ;
* Colonne R (COORD_X) :  coordonnée X en système ED_1950_UTM_Zone_30N ;
* Colonne S (COORD_Y) : coordonnée Y en système ED_1950_UTM_Zone_30N ;
* Colonne T (PAROISSE) : le nom de la paroisse (collación, parroquia) où se trouve la maison ;
* Colonne U (IMPOT) :  tribut (impot) en maravedis (monnaie), important pour évaluer l'importance de la maison, le quartier, etc.
 
### Correspondances de classes et de propriétés pour les lignes (individus) et colonnes (propriétés, caractéristiques...)

L'extension CIDOC CRM BA (A CRM extension for buildings archaeology information modelling) est très adaptée pour modéliser une bonne partie de ce domaine.
* les pièces : B2 Morphological Building Section, B4 Empty Morphological Building Section
* les maisons : B1 Built Work
* l'appartenance d'une pièce à une maison : BP1 is section of (Domain: B2 Morphological Building Section, Range: B1 Built Work) 
* coordonnées geographiques : E47 spatial coordinates
* fonction de pièces : 
* datation de maison selon les sources : E52 Time span ?
* les quartiers : Place appelation ?
* les mesures de pièces : pas de propriété d'objet direct (Dimension), plutôt passer par une temporal entity
* commentaire décrivant (parfois) la situation relative de pièces : BP11.2 is connected through..
* l'appartenance d'une maison à un quartier
* situation de pièces dans la maison en niveaux
* impots : ?

### Documentation

[lien](http://www.cidoc-crm.org/crmba/sites/default/files/2016-12-3%23CRMba_v1.4.1_UR.pdf)

--------------------------------------------

## À faire

### Contrats/transactions

Chaque entrée represente une vente qui est décrite en termes des propriétés telles que : prénom + patronyme, surnom, metier, sexe, religion, filiation, état civil, domicile, date (dans laquelle l'information est attestée), domicile, code de la maison (en cours de saisie), qualification, action, condition, Type de contrat, montant, monnaie, bailleur / acheteur, cote, n° entrée.
* A discuter : des identifiants pour chaque personne ? un vocabulaire controlé pour les métiers ? un thésaurus pour les adresses ?

### Impôts

Pour une année donnée (dans un onglet), une entrée correspond à un impot reglé par une personne à Tolède avec l'adresse (nom de la rue et un code d'immeuble) de l'immeuble pour lequel l'impot est payé, le type d'immeuble, superficie en m2 du RDC (sans l'espace extérieur), nombre de niveaux, metier, montant, ..
