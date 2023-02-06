# Projet HisArc-RDF

Partage et réutilisation de données archéologiques et historiques : une description en RDF appuyée sur les référentiels et les normes du web sémantique.

Ce projet est financé par l'[Agence nationale de la recherche](https://anr.fr/fr/lanr/engagements/la-science-ouverte/les-projets-laureats-de-lappel-flash-science-ouverte/projet-hisarc-rdf/) (2020-2022).

Le site dataforhumanities.org a été créé dans le cadre de ce projet pour mettre en avant la preuve de concept proposée (cf. plus bas). Il s'appuie sur différents dépôts github et sur un point d'accès SPARQL mis à disposition par l'ABES.

## Sommaire
- [Partenaires](#partenaires)
- [Présentation](#presentation)
- [Documentation](#documentation)
  - [Jeux de données Archeodunum, Bibracte et Marges arides](#doc1)
  - [Jeu de données PRELIB](#doc2)
- [Outils et applications](#outils)

## Partenaires <a name="partenaires"></a>

- [Archéorient](https://www.archeorient.mom.fr/)
- [LARHRA](https://larhra.ish-lyon.cnrs.fr/)
- [MOM](https://www.mom.fr/)
- [ABES](https://www.abes.fr/)
- [Bibracte](https://www.bibracte.fr)
- [Archéodunum](https://www.archeodunum.com)

## Présentation <a name="presentation"></a>

Porté par le laboratoire Archéorient et le LARHRA, le projet HisArc-RDF réunit un consortium pluridisciplinaire : archéologie, histoire, géographie, terminologie, bibliographie et informatique.

HisArc-RDF souhaite prototyper une chaîne opératoire de données « FAIR » Findable, accessible, interoperable, reusable sur des jeux de données archéologico-historiques structurellement et sémantiquement hétérogènes, en s'appuyant sur le partage et l’articulation de méthodes et d’outils logiciels et sémantiques développés dans chaque discipline. 

À partir de jeux-tests, composés de bases de données « maison » ou de fichiers textes numérisés, un travail de modélisation et d’alignement sera proposé pour établir la preuve de concept que les technologies du web sémantique (dont le RDF est le langage de base) permettent l’interopérabilité, c’est à dire l’intercommunication, de bases diverses et surtout la réutilisation des données produites.

L’interopérabilité de bases hétérogènes repose habituellement sur des concepts de haut niveau qui ont tendance à écraser les spécificités d’un domaine (le concept de haut niveau « objet physique » englobant aussi bien, par exemple, des pièces de monnaie que des arquebuses). Dans HisArc-RDF, nous souhaitons minimiser cet effet de dilution sémantique en faisant reposer l’interopérabilité non seulement sur le modèle conceptuel (ou ontologie) mais aussi sur les deux autres piliers que sont les thésaurus terminologiques et les référentiels d’autorité.

L’application [OntoME](https://ontome.net), développée par l'Axe de recherche en histoire numérique du LARHRA est au cœur du processus : elle permet la création d’ontologies proches du domaine étudié conçues comme des extensions du CIDOC CRM. Dans le cadre de cette ANR, pour permettre de créer un lien fort entre le modèle conceptuel et le thésaurus, une brique logicielle sera développée pour interconnecter OntoME à l’application de gestion de thésaurus [Opentheso](https://opentheso.hypotheses.org/) développée à la MOM. Parallèlement, Opentheso sera également interconnecté à la plateforme [IdRef](https://idref.fr) qui gère les autorités, c’est à dire les identifiants uniques des auteurs, institutions, concepts... utilisés par le catalogue SUDOC de l’Agence bibliographique de l’enseignement supérieur avec laquelle le LARHRA a signé une convention de coopération en 2019.

En fin de chaîne, les données hétérogènes ainsi traitées seront déposées dans un entrepôt permettant leur publication, leur interrogation et par conséquent leur réutilisation pour de nouvelles recherches grâce à un point d'accès SPARQL. 

Passé la preuve de concept, cette même chaîne opératoire pourrait être proposée à d’autres bases géo-historiques issues de différents projets de recherche qui pourront ainsi facilement s’interconnecter avec les données d’autres projets et répondre, de cette façon, à la demande institutionnelle forte d’ouverture des données de la recherche.

## Documentation <a name="documentation"></a>

### Jeux de données Archeodunum, Bibracte et Marges arides <a name="doc1"></a>
- [Wiki de la page github du projet](https://github.com/Semantic-Data-for-Humanities/HisArc-RDF/wiki)

### Jeu de données PRELIB <a name="doc2"></a>
- [Wiki du projet d'alignement](https://github.com/Semantic-Data-for-Humanities/prelib-to-rdf/wiki)

### Connecteur OntoME-Opentheso <a name="doc3"></a>
- [Présentation](https://github.com/Semantic-Data-for-Humanities/HisArc-RDF/blob/main/OntoME_Opentheso_Connection_202301.pdf)

## Outils et applications <a name="outils"></a>

- Environnement de gestion d'ontologies OntoME (développé par le LARHRA dans le cadre du consortium Geovistory) : https://ontome.net/
- Gestionnaire de thesaurus Openthesau (développé par la MOM) : https://opentheso.hypotheses.org/
  - Thesaurus Hypethesau : https://thesaurus.mom.fr/opentheso/?idt=25
  - Thesaurus OntoME : https://ontomeopentheso.mom.fr/ontomeopentheso/?idt=th8
- Environnement virtuel de recherche Geovistory (développé par KleioLab et le LARHRA dans le cadre du consortium Geovistory) : https://www.geovistory.org/
- Point d'accès SPARQL (mis à disposition par l'ABES) : https://dataforhumanities.org/sparql-endpoint/endpoint-description
  - Graphe PRELIB : https://dataforhumanities.org/sparql-endpoint/prelib-v1
  - Graphe Archeodunum : https://dataforhumanities.org/sparql-endpoint/vienne-2018 




