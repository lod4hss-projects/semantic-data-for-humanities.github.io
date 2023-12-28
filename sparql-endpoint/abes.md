---
## Feel free to add content and custom Front Matter to this file.
## To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Data For Humanities
subtitle: Points d'accès à des données
menubar: menu_sparql
layout: page
---

# SPARQL-endpoint (hosted by ABES)

[Go to SPARQL-endpoint](https://dataforhumanities.abes.fr/sparql)

This SPARQL-endpoint is hosted by the Agence bibliographique de l'enseignement supérieur

It is structured in graphs that publish datasets stemming from SHS research.

The information contained in the data has been semantified using the ecosystem of CIDOC CRM extensions developed by the Semantic Data for Humanities and Social Sciences (SDHSS) project.

The entities they describe are aligned or directly identified with the IdRef authority files.

Access to the [list of existing graphs with real time number of triples per graph](https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=SELECT+%3Fg+%28count%28*%29+as+%3Feffectif%29%0D%0AWHERE%0D%0A%7B+GRAPH+%3Fg%0D%0A%7B%3Fs+%3Fp+%3Fo%7D%0D%0A%7D%0D%0Agroup+by+%3Fg%0D%0Aorder+by+desc%28%3Feffectif%29%0D%0A&should-sponge=&format=text%2Fhtml&timeout=0&debug=on).