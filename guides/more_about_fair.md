---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Data For Humanities
subtitle: Les principes FAIR
layout: page
toc: true
menubar: menu_guides
toc_title: Contenu
---

# Les principes FAIR

------------------------------------------

## Projet "FAIR data" en sciences historiques

Les [principes FAIR](https:www.go-fair.org/fair-principles/) ont pour finalité de mettre à la disposition des autres chercheurs et du public les données produites par la recherche, en appliquant une méthodologie qui les rend réutilisables. 

Le projet de FAIRisation des données, initié par le Pôle histoire numérique du LARHRA en mars 2020, ouvert à tou-te-s les intéressé-e-s, est dédié à la mise à disposition de données FAIR en histoire et à la mise en place d'un processus méthodologique en adéquation avec cette finalité. 

Les principes FAIR signifient que les données sur lesquelles les chercheurs travaillent sont:

> * **F**indable&nbsp;: D’abord, les données et les métadonnées doivent être facilement trouvables, autant par des humains que par des machines.
> * **A**ccessible&nbsp;: Ensuite, les données et les métadonnées doivent être facilement accessibles, donc il faut indiquer comment accéder à ces dernières.
> * **I**nteroperable&nbsp;: Puis, les données et les métadonnées peuvent être reprises pour les ajouter à d’autres données. Pour cela, la sémantique et la syntaxe doit avoir des standards communs à la communauté scientifique internationale.
> * **R**eusable&nbsp;: Enfin, les données et les métadonnées doivent pouvoir être réutiliser. Cela demande qu’elles soient bien décrites.

------------------------------------------

## FAIRisation ou FAIRification, quel différence&nbsp;?
   
  * La __FAIRisation__ (ou FAIRization) signifie l’ensemble du processus qui amènent à produire des données FAIR.

  * Quant à la __FAIRification__, elle correspond à la réalisation technique de la FAIRisation.

  * En amont de cette phase de FAIRification, il y a une phase de __pré-FAIRisation__  qui permet d’énoncer les objectifs de la FAIRification et d’identifier les données et les métadonnées à rendre FAIR. 

Cette distinction a été formulée par le groupe RDA-SHARC-IG ([Research Data Alliance](https:www.rd-alliance.org/) - SHAring Rewards and Credit -Interest Group). Elle permet de mieux appréhender les différentes étapes d’un projet de FAIRisation, bien qu’elle ne soit pour l’instant pas adoptée par la communauté scientifique. Les termes de FAIRisation et FAIRification sont souvent utilisés de façon interchangeables et dépendent de l’interlocuteur. On peut néanmoins remarquer que [GO FAIR](https:www.go-fair.org/), l’une des structures de référence, n’emploie que le terme FAIRification. 

Vous pouvez retrouvez le poster sur lequel la distinction est formulée: David Romain, Mabile Laurence, Yahia Mohamed, Thomsen Mogens, Cambon-Thomsen, Anne. [Evaluation tool of FAIR criteria literacy and compliance to foster research data sharing. 2. Open Science
FAIR Conference: “ Synergies for Sustainable, Open and Responsible Research ”](https:hal.archives-ouvertes.fr/hal-02164148), Sep 2019, Porto. (hal-02164148)

------------------------------------------

## Documentation

Vous retrouvez ici une documentation utile pour comprendre et réaliser de la __FAIRisation__.

### Les principes de la FAIRisation

* La page __[wikipedia](https:fr.wikipedia.org/wiki/Fair_data)__ française dédiée aux données FAIR.
* Vous retrouvez ici l'__article fondateur__ des principes FAIR: Wilkinson Mark D, et al., « [The FAIR Guiding Principles for scientific data management and stewardship](https:www.ncbi.nlm.nih.gov/pmc/articles/PMC4792175/) », Scientific Data, vol. 3, 15 mars 2016 (DOI : 10.1038/sdata.2016.18).
* Cette __affiche__ montre la totalité des principes FAIR et ce qu'ils impliquent: Jones Sarah, Grootveld Marjan, « [How FAIR are your data?](https:zenodo.org/record/1065991#.XRnw8IrgqMq)», Zenodo, 24 novembre 2017 (DOI: 10.5281/zenodo.1065991).
* Cette __page__ permet de connaître succinctement les principes FAIR: FORCE11, « [Guiding Principles for Findable, Accessible, Interoperable and Re-usable Data Publishing version b1.0](https:www.force11.org/fairprinciples) », sur FORCE11.
* Cette __page__ donne de façon plus détaillée et précise les principes FAIR: GO FAIR, « [FAIR Principles](https:www.go-fair.org/fair-principles/) », sur GO FAIR.
* Cette __présentation interactive__ permet de présenter l'ensemble des principes FAIR: « [Principes FAIR :Cellule Data stewardship Université Grenoble Alpes](https:gricad.gricad-pages.univ-grenoble-alpes.fr/cellule-data-stewardship/web/research_data/fair/) », sur Gricad.
* Une façon différente de comprendre les __différentes étapes de la FAIRisation__ sous la forme d'un __conte__. On retrouve, en miroir, les éléments du conte et les bonnes pratiques à avoir pour réaliser de la FAIRisation: Kryger Hansen Karsten, Buss Mareike, Sztuk Haahr Lea, [A FAIRy tale](https:zenodo.org/record/2248200#.XkVegPZFxaS), Zenodo, 2018 (DOI: 10.5281/zenodo.2248200).
* Ce rapport est un __petit guide__ pour la FAIRisation et permet notamment de bien formaliser ses métadonnées pour les mettre dans [Nakala](https:www.nakala.fr/) (l'entrepot de données d'Huma-Hum): Idmhand Fatiha, Galleron Ioana,[Guide pour la FAIRisation des données des corpus d’auteurs préparé par Idmhand Fatiha, Galleron Ioana V2 [Groupe de travail Data_Cahier](https:halshs.archives-ouvertes.fr/halshs-03037748)]. [Rapport de recherche], Huma-Num, 2020.
* Dans ce rapport de la Commission Européenne, vous retrouvez un __bilan__ très complet et détaillé sur la __mise en place du FAIRisation__ et les enjeux que cette dernière représente. Il est accompagné de pas mal de __schémas__ explicatifs: European Commission Expert Group on FAIR Data,[Turning FAIR into reality](https:ec.europa.eu/info/sites/info/files/turning_fair_into_reality_1.pdf), Luxembourg, Publications Office of the European Union, 2018 (DOI: 10.2777/1524).
* Posters sur les __données FAIR Géo-Historiques__ avec leur implémentation et leur interopérabilité dans la plate-forme __OntoME__:
* Beretta Francesco , Alamercery Vincent,Derks Sebastiaan, Petram Lodewijk, Schneider Jonas, [ Geohistorical FAIR data. Data integration and interoperability using the OntoME platform](https:halshs.archives-ouvertes.fr/halshs-02314003), Time Machine Conference 2019, Dresden, Octobre 2019.
* Alamercery Vincent, Beretta Francesco, [Produire des données géohistoriques « FAIR ». L'application OntoME et le consortium Data for History](https:halshs.archives-ouvertes.fr/halshs-02307315), La semaine des humanités numériques, Lyon, Octobre 2019.

### Recommandations

* Ce sont des __recommandations__ de la Commission Européenne en matière de FAIRisation: EOSC Executive Board, [Six Recommendations for Implementation of FAIR Practice](https:ec.europa.eu/info/sites/info/files/research_and_innovation/ki0120580enn.pdf), Luxembourg, Publications Office of the European Union, 2020 (DOI: 10.2777/986252).

### Initiatives

* Ils expliquent comment ils ont mis au point un __outil__ permettant de __mesurer__ le niveau de FAIRisation d'un jeu de données: Wilkinson Mark D., Susanna-Assunta Sansone, Erik Schultes, Peter Doorn, Luiz Olavo Bonino da Silva Santos, Dumontier Michel, «[A design framework and exemplar metrics for FAIRness»](https:www.biorxiv.org/content/10.1101/225490v3), bioRxiv, Cold Spring Harbor Laboratory, rubrique « New Results », 1ᵉʳ décembre 2017 (DOI: 10.1101/225490)

### Liens utiles

* [Go-fair](http:go-fair.org) sont des promoteurs à l'international de l'application des principes FAIR et du développement de la __science ouverte__. Ils ont notamment pour but de créer et d'améliorer des __infrastructures__ et les __pratiques__ pour le développement des principes FAIR.
* [FORCE11](https:www.force11.org/) est le site à l'origine des principes FAIR et à pour but de développer la __science ouverte__ et l'__interdisciplinarité.__ Ils se donnent pour mission de relier les communautés de chercheurs, en créant un espace collaboratif et mettant en avant de nouveaux outils pour ces derniers.