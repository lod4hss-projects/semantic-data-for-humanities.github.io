---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Data For Humanities
subtitle: Projets aboutis
menubar: menu_projects
toc: true
layout: page
---

# Défi données MaDICS-ADOC 2018

------------------------------------------

## Responsables

> **Francesco Beretta** (1), **François Mistral** (2)
>
> (1) UMR5190 LARHRA CNRS/Université de Lyon, Responsable du Pôle histoire numérique [francesco.beretta[at]ish-lyon.cnrs.fr]    (2) [ABES (Montpellier)](http://www.abes.fr/), Responsable d'IdRef - référentiels pour l'Enseignement Supérieur
>
> __Enrichir et exploiter un corpus de données historiques publiées sous forme de LOD : le [projet SIPROJURIS](http://siprojuris.symogih.org). Système d’information des professeurs de droit (1804-1950)__

------------------------------------------

## Présentation du défi

Le défi a été lancé lors de la journée Variété des données SHS, Nantes, 28 mai 2018, atelier associé à la conférence INFORSID 2018

* [Présentation du défi](http://eric.univ-lyon2.fr/adoc#).

Adresse courte pour ces pages: [https://tinyurl.com/data-challenge-2018](https://tinyurl.com/data-challenge-2018)

### Données

Le [projet SIPROJURIS](http://siprojuris.symogih.org/), dirigé par Catherine Fillon, maître de conférences en histoire du droit (Université Jean Monnet-Saint Etienne), et Emmanuelle Picard, maître de conférences en histoire (École Normale Supérieure de Lyon), a pour but de constituer un système d'information dédié à l'enseignement du droit en France au 19e et 20e siécles.

Une base de données a été constituée à partir de matériaux recoltés par une équipe de chercheurs (voir la [liste des participants](http://siprojuris.symogih.org/siprojuris/contributeurs)) principalement à partir des dossiers de carrière des enseignants en droit (Archives Nationales, site de Pierrefitte-sur-Seine; Centre des Archives Contemporaines de Fontainebleau), enrichis dans la mesure du possible par d'autres sources, notamment issues des archives déparementales ([liste des sources](http://siprojuris.symogih.org/siprojuris/sources-depouillees)).

La base de données, qui est hébergée sur la plateforme collaborative du projet [symogih.org](http://symogih.org), continuera à s’enrichir à la fois par l’introduction de nouveaux individus et par celle de données supplémentaires relatives à l’ensemble de la population du corpus. 

L'essentiel des données du projet [projet SIPROJURIS](http://siprojuris.symogih.org/) accessible sur le site web du projet a été également publié sur le [point d'accès SPARQL de la plateforme dans un graphe dédié](http://symogih.org/graph/siprojuris-sym), appelé //syprojuris-sym//.

Ce graphe contient 8310 informations concernant 567 professeurs. L'ontologie utilisée pour la publication RDF est celle adoptée dans la première phase du projet //symogih.org// (actuellement en cours d'alignement avec le CIDOC CRM dans le contexte du projet [Data for History](http://dataforhistory.org/)). Une page d'explication concernant la publication du graphe est accessible [à cette adresse](http://symogih.org/graph/siprojuris-sym). Une présentation générale du projet //symogih.org// avec une discussion de l'origine du modèle et des exemples de données RDF est disponible à [cette adresse](https://halshs.archives-ouvertes.fr/halshs-01253226) (sous forme de diapositives) et [dans ce texte](https://halshs.archives-ouvertes.fr/halshs-01559816).

Concernant les acteurs de la population, un alignement avec le [référentiel IdREF](https://www.idref.fr/) est en cours de réalisation en collaboration avec l'Agence bibliographique de l'enseignement supérieur (ABES). Il permet d'entrer pleinement dans la logique des //linked open data//: en effet, à partir de cet alignement, qui rend accessibles les passerelles représentées par ISNI et VIAF, d'autres ressources publiant des LOD, telles les données de la BNF, Wikidata, etc. deviennent accessibles. Dans le site du projet SIPROJURIS lui-même, les fiches des acteurs liés au référentiel IdREF sont enrichies avec les données issues directement du catalogue du SUDOC (également une ressource LOD): dans l'onglet //Bibliographie externe// de la fiche biographique d'un acteur (cf. par ex. [Jean Appleton](http://siprojuris.symogih.org/siprojuris/enseignant/44317)), on trouvera la liste des ouvrages et publications issues du SUDOC.

### Partie I du défi: Enrichir les données

Dans cette partie du défi, il s'agit d'enrichir les données avec d'autres ressources du web, sous forme de LOD ou en les extrayant de textes avec les méthodes de TALN.

Sur **[cette page](siprojuris:enrichir_les_donnes_avec_LOD)** on trouvera quelques pistes illustrant la manière de connecter les données SIPROJURIS avec d'autres données LOD afin d'élargir la population de professeurs étudiée et d'enrichir les informations disponibles.

### Partie II du défi: Analyser et visualiser les données

Dans cette partie, il s'agit d'analyser et de visualiser les données afin de répondre aux questions des historiens.

Les historien(ne)s qui participent à ce projet, et plus largement ceux et celles qui s'intéressent à la prosopographie des universitaires, sont très intéressés à découvrir des techniques d'analyse et de visualisation des données leur permettant de répondre à leurs questionnements. Répondre à leurs questions et partager les méthodes et le code ayant permis d'obtenir ces réponses leur permettra de mettre mieux en valeur les données recoltées.

Sur **[cette page](siprojuris:defi_donnees_2018_questions_historiens)** on trouvera la documentation concernant les questionnements auxquels les historie(ne)s aimeraient répondre en utilisant les données du projet SIPROJURIS, ainsi que d'autres données disponibles sur le web.

----------------------------------------------------------

## La documentation du défi

Un **pad** d'accompagnement du défi permettant de partager des questions, proposer des approches, etc. a été mis en place. Contacter les organisateurs pour y avoir accès.

Si on souhaite publier une documentation plus articulée des questions ou du travail effectué, ce wiki est à disposition. Une page dédiée à chaque projet d'analyse/enrichissement de données peut être ouverte.

Si des données issues de sources ouvertes, en complément aux données existantes, sont produites au format RDF, vous pouvez nous envoyer une sérialisation XML ou ttl et nous pourrons les importer dans un graphe dédié du SPARQL endpoint.

----------------------------------------------------------

## Un exemple: les données concernant un acteur


### Le parcours biographique de Gaston Louis Henry May (1849 - 1940)

Cf. la [page](http://siprojuris.symogih.org/siprojuris/enseignant/56241) qui lui est dédiée dans le projet SIPROJURIS.

### Requête qui reconstitute son parcours biographique

Requête à coller dans le [point d'accès SPARQL](http://bhp-publi.ish-lyon.cnrs.fr:8888/sparql) du projet [symogih.org](http://symogih.org).

```sparql
SELECT ?TyRoLabel ?infoStandardDate ?infoStandardLabel ?TyInLabel
WHERE {
GRAPH <http://symogih.org/graph/symogih-kute> {
    ?tyro rdfs:label ?TyRoLabel.
    ?tyin rdfs:label ?TyInLabel.
        {
        GRAPH <http://symogih.org/graph/siprojuris-sym> {
            ?s ?p syr:Actr56241;
                sym:isComponentOf ?info;
                sym:hasRoleType ?tyro.
            ?info sym:knowledgeUnitStandardLabel ?infoStandardLabel;
                sym:knowledgeUnitStandardDate ?infoStandardDate;
                sym:hasKnowledgeUnitType ?tyin.
            }
        }
    }
}
ORDER BY ?infoStandardDate
```