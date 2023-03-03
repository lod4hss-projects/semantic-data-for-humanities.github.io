---
## Feel free to add content and custom Front Matter to this file.
## To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Data For Humanities
subtitle: Points d'accès à des données
menubar: menu_sparql
toc: true
layout: page
---

# PRELIB — Projet de recherche en littérature bretonne

--------------------------------------------------------

## Jeu de données converti en RDF
  

* [Site original du projet](https://mshb.huma-num.fr/prelib/)
* [Site de publication](https://crbc-dataset.huma-num.fr/) de données SQL interrogeable
* [Documentation de la transformation](https://github.com/Semantic-Data-for-Humanities/prelib-to-rdf/wiki)

--------------------------------------------------------

## Exemples de requêtes

### Liste des classes avec effectifs

Voir les [résultats de la requête](https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=SELECT+%3Fclass+%28COUNT%28*%29+AS+%3Feff%29+WHERE+%7BGRAPH+%3Chttps%3A%2F%2Fdataforhumanities.org%2Fsparql-endpoint%2Fprelib-v1%3E+%7B%3Fs+a+%3Fclass%7D%7D+GROUP+BY+%3Fclass+ORDER+BY+DESC%28%3Feff%29&should-sponge=&format=text%2Fhtml&timeout=0&debug=on).
```sparql
SELECT ?class (COUNT(*) AS ?eff)<br/>
WHERE {GRAPH <https://dataforhumanities.org/sparql-endpoint/prelib-v1> {?s a ?class}}

GROUP BY ?class
ORDER BY DESC(?eff)
```

### Liste des propriétés avec effectifs

Voir les [résultats de la requête](https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=SELECT+%3Fproperty+%28COUNT%28*%29+AS+%3Feff%29+WHERE+%7BGRAPH+%3Chttps%3A%2F%2Fdataforhumanities.org%2Fsparql-endpoint%2Fprelib-v1%3E+%7B%3Fs+%3Fproperty+%3Fo%7D%7D+GROUP+BY+%3Fproperty+ORDER+BY+DESC%28%3Feff%29+&should-sponge=&format=text%2Fhtml&timeout=0&debug=on).
```sparql
SELECT ?property (COUNT(*) AS ?eff) 
WHERE {GRAPH <https://dataforhumanities.org/sparql-endpoint/prelib-v1> 
{?s ?property ?o}}
GROUP BY ?property
ORDER BY DESC(?eff)
```

### Entités Personnes du corpus

Voir les [résultats de la requête](https://dataforhumanities.abes.fr/sparql?default-gr[aph-uri=&query=prefix+cidoc%3A+%3Chttp%3A%2F%2Fwww.cidoc-crm.org%2Fcidoc-crm%2F%3E%0D%0Aselect+%3Fs+where+%7B+%3Fs+rdf%3Atype+cidoc%3AE21_Person+.+%7D%0D%0Alimit+50&should-sponge=&format=text%2Fhtml&timeout=0&debug=on).
```sparql
PREFIX cidoc: <http://www.cidoc-crm.org/cidoc-crm/>
SELECT ?s WHERE { ?s rdf:type cidoc:E21_Person . }
LIMIT 50
```

### Inspection des classes

Voir les [résultats de la requête](https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=SELECT+%28COUNT%28*%29+as+%3Feff%29+%3Fg+%3Fp+%3Fclass%0D%0A++++WHERE+%0D%0A++++%7Bgraph+%3Fg+%0D%0A++++%7B+%3Fs+a+%3Chttp%3A%2F%2Fwww.cidoc-crm.org%2Fcidoc-crm%2FE21_Person%3E%3B+%3Fp+%3Fo.%0D%0A++++%3Fo+a+%3Fclass.%0D%0A++++FILTER++%28%3Fp+not+in+%28rdf%3Atype%2C+rdfs%3Alabel%29%29%0D%0A++++%7D+%0D%0A++++%7D+GROUP+BY+%3Fg+%3Fp+%3Fclass&should-sponge=&format=text%2Fhtml&timeout=0&debug=on).
```sparql
SELECT (COUNT(*) as ?eff) ?g ?p ?class
WHERE {
	graph ?g {
		?s a http://www.cidoc-crm.org/cidoc-crm/E21_Person;
			?p ?o.
    	?o a ?class.
    	FILTER  (?p not in (rdf:type, rdfs:label))
    	} 
    }
GROUP BY ?g ?p ?class
```