---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Data For Humanities
subtitle: The FAIR principles
menubar: menu_guides
toc: false
layout: page
---
# Comment transformer les données hétérogènes semi-structurées (notamment issues de tableurs et CSV) en données FAIR ?

--------------------------------------------------------

## Descriptif sommaire du projet

Nous savons que la plupart des historien⋅nes produisent des données de recherche sous forme de texte ou de tableurs. Retenons pour cet atelier le cas des tableurs. D'ailleurs les bases de données réalisées de manière empirique et sans formation sont au final des tableurs avec interface graphique de saisie.

La question posée en termes de défi à l'atelier est : ces données sont-elles irrémédiablement perdues après la recherche ou pourrait-on rendre ces données FAIR - i.e. réutilisables pour d'autres recherches et écrites dans des formats accessibles par les machines (et donc pas seulement lues sur un site web) ? Comment remettre les données dans le circuit, tant pour les chercheur-es eux-elles mêmes que pour les autres chercheur-es et le public ?

Le défi relevé dans cet atelier vise à réfléchir, collectivement, aux réquis des principes 
FAIR appliqué à histoire. Quelles sont les conditions pour rendre les données de la recherche (dans ce cas des données semistructurées) accessibles dans le sens d'un processus de repliquabilité de la production des connaissances et de réutilisation pour de nouvelles recherches ?

Les réponses à ces questions n'existent pas toutes faites, l'objectif de l'atelier est de construire ensemble des bonnes pratiques à ce sujet, tout en partant de l'expérience du projet [symogih.org](http://symogih.org/) et autour des applications [OntoME](https://ontome.net/) de modélisation des connaissances et [Opentheso](https://www.mom.fr/ressources-numeriques/opentheso) de gestion de vocabulaires contrôlés.

--------------------------------------------------------

## Feuille de route

* je répère un fichier Excel ou CSV contenant des données que je veux publier et rendre réutilisables
* je définis quelles sont les conditions de publication (licence)
* je créer une page de documentation de mon projet sur le [wiki dédié à ce défi](accueil) – licence de la documentation du projet CC 4.0 BY SA donc mention explicite de l'auteur (?)
* je documente mon choix et les données de base sur la page dédiée à mon projet du wiki
* je l'inspecte et analyse le contenu du fichier. En particulier je définis ce que sont les lignes (individus, mentions d'individus, etc.), à quels individus du monde réel (physique ou imaginaire) ils correspondent, et ce que sont les colonnes en tant que propriétés de ces individus.
* je modélise le fichier comme tel en définissant à quelle classe appartiennent les individus (c'est-à-dire les lignes du ficher : personnes, mentions de personnes, d'activités, etc.)
* ensuite je modélise ses colonnes (c'est-à-dire les propriétés des individus) et je vérifie la présence des classes et propriétés correspondantes dans un [espace de noms OntoME](https://ontome.net/namespace/3)
* je complète éventuellement le modèle dans un espace de noms de OntoME
* je créer un profil correspondant à mon fichier ou mon projet, ou j'utilise un profil existant
* je vérifier la présence des classes de mes termes et instances dans [Opentheso](https://ontomeopentheso.mom.fr/ontomeopentheso/index.xhtml)
* j'importe le fichier dans Pandas (Python) ou sqlite je nettoye et crée un vocabulaire avec un seul terme par entrée 
* je l'importe dans Opentheso 
* je reçois des identifiants ark pour chaque terme et discute des définitions avec la communauté 
* j'aligne les termes avec les IdRef ou d'autres référentiels
* j'inspecte mes données après le mapping avec l'ontologie dans OntoME et l'alignement avec Opentheso
* je récupère dans mon fichier les identifiants correspondants (en utilisant Python)
* je nettoye automatiquement ou à la main les données
* avec un librairie Python RDF j'écris dans le SPARQL ENDPOINT  de l'ABES dans un graphe dédié à mon projet
* je documente tout le processus sur le wiki ou dans mes carnets jupyter publiés sur GitHub
* j'explore les données avec des librairies Python et document dans un carnet public ma démarche
* je me concerte avec d'autres collèques et je fais une proposition de site web PyProjects afin de publier mes données et des analyses, éventuellement interactives sous forme lisible par l'humain.



