---
permalink: /sparql-endpoint/prelib-v1
---



<div>
  <h2>PRELIB — Projet de recherche en littérature bretonne</h2>

  <div>
  <h3>Jeu de données converti en RDF</h3>
  
  <ul>
    <li><a target="_blank" href="https://mshb.huma-num.fr/prelib/">Site original du projet</a></li>
    <li><a target="_blank" href="https://crbc-dataset.huma-num.fr/">Site de publication</a> de données SQL interrogeable</li>
    <li><a href="https://github.com/Semantic-Data-for-Humanities/prelib-to-rdf/wiki">Documentation de la transformation</a></li>
  </ul>

  
</div>

<div>
  <h3>Exemples de requêtes</h3>
<h4>List des classes avec effectifs</h4>

<p>
  <a href="https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=SELECT+%3Fclass+%28COUNT%28*%29+AS+%3Feff%29+WHERE+%7BGRAPH+%3Chttps%3A%2F%2Fdataforhumanities.org%2Fsparql-endpoint%2Fprelib-v1%3E+%7B%3Fs+a+%3Fclass%7D%7D+GROUP+BY+%3Fclass+ORDER+BY+DESC%28%3Feff%29&should-sponge=&format=text%2Fhtml&timeout=0&debug=on">
    <code>
        SELECT ?class (COUNT(*) AS ?eff)<br/>
        WHERE {GRAPH <https://dataforhumanities.org/sparql-endpoint/prelib-v1> {?s a ?class}}
        <br/>
        GROUP BY ?class
<br/>
        ORDER BY DESC(?eff)
      </code>
    </a>  
  
</p>

  <h4>Liste des propriétés avec effectifs</h4>
  <p>
  <a href="https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=SELECT+%3Fproperty+%28COUNT%28*%29+AS+%3Feff%29+WHERE+%7BGRAPH+%3Chttps%3A%2F%2Fdataforhumanities.org%2Fsparql-endpoint%2Fprelib-v1%3E+%7B%3Fs+%3Fproperty+%3Fo%7D%7D+GROUP+BY+%3Fproperty+ORDER+BY+DESC%28%3Feff%29+&should-sponge=&format=text%2Fhtml&timeout=0&debug=on">
  <code>
    SELECT ?property (COUNT(*) AS ?eff) 
    WHERE {GRAPH <https://dataforhumanities.org/sparql-endpoint/prelib-v1> 
    {?s ?property ?o}}
    GROUP BY ?property
    ORDER BY DESC(?eff)
  </code> </a>
  </p>
    
  <h4>Entités Personnes du corpus</h4>
  <p>
  <a href="https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=SELECT+%3Fproperty+%28COUNT%28*%29+AS+%3Feff%29+WHERE+%7BGRAPH+%3Chttps%3A%2F%2Fdataforhumanities.org%2Fsparql-endpoint%2Fprelib-v1%3E+%7B%3Fs+%3Fproperty+%3Fo%7D%7D+GROUP+BY+%3Fproperty+ORDER+BY+DESC%28%3Feff%29+&should-sponge=&format=text%2Fhtml&timeout=0&debug=on](https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=select+%28count%28*%29+as+%3Feff%29+%3Fg+%3Fp+%3Fclass%0D%0Awhere+%0D%0A%0D%0A%7Bgraph+%3Fg+%0D%0A%0D%0A%7B+%3Fs+a+%3Chttp%3A%2F%2Fwww.cidoc-crm.org%2Fcidoc-crm%2FE21_Person%3E%3B%0D%0A+++++++++++++%3Fp+%3Fo.%0D%0A%3Fo+a+%3Fclass.%0D%0A%0D%0AFILTER++%28%3Fp+not+in+%28rdf%3Atype%2C+rdfs%3Alabel%29%29%0D%0A%0D%0A%7D+%0D%0A%0D%0A%7D+group+by+%3Fg+%3Fp+%3Fclass&should-sponge=&format=text%2Fhtml&timeout=0&debug=on](https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=prefix+cidoc%3A+%3Chttp%3A%2F%2Fwww.cidoc-crm.org%2Fcidoc-crm%2F%3E%0D%0Aselect+%3Fs+where+%7B+%3Fs+rdf%3Atype+cidoc%3AE21_Person+.+%7D%0D%0Alimit+50&should-sponge=&format=text%2Fhtml&timeout=0&debug=on">
  <code>
    
    prefix cidoc: <http://www.cidoc-crm.org/cidoc-crm/>
    select ?s where { ?s rdf:type cidoc:E21_Person . }
    limit 50
  </code> </a>
  </p>

    
  <h4>Inspection des classes</h4>
  <p>
  <a href="https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=SELECT+%3Fproperty+%28COUNT%28*%29+AS+%3Feff%29+WHERE+%7BGRAPH+%3Chttps%3A%2F%2Fdataforhumanities.org%2Fsparql-endpoint%2Fprelib-v1%3E+%7B%3Fs+%3Fproperty+%3Fo%7D%7D+GROUP+BY+%3Fproperty+ORDER+BY+DESC%28%3Feff%29+&should-sponge=&format=text%2Fhtml&timeout=0&debug=on](https://dataforhumanities.abes.fr/sparql?default-graph-uri=&query=select+%28count%28*%29+as+%3Feff%29+%3Fg+%3Fp+%3Fclass%0D%0Awhere+%0D%0A%0D%0A%7Bgraph+%3Fg+%0D%0A%0D%0A%7B+%3Fs+a+%3Chttp%3A%2F%2Fwww.cidoc-crm.org%2Fcidoc-crm%2FE21_Person%3E%3B%0D%0A+++++++++++++%3Fp+%3Fo.%0D%0A%3Fo+a+%3Fclass.%0D%0A%0D%0AFILTER++%28%3Fp+not+in+%28rdf%3Atype%2C+rdfs%3Alabel%29%29%0D%0A%0D%0A%7D+%0D%0A%0D%0A%7D+group+by+%3Fg+%3Fp+%3Fclass&should-sponge=&format=text%2Fhtml&timeout=0&debug=on">
  <code>
    
    select (count(*) as ?eff) ?g ?p ?class
    where 
    {graph ?g 
    { ?s a http://www.cidoc-crm.org/cidoc-crm/E21_Person; ?p ?o.
    ?o a ?class.
    FILTER  (?p not in (rdf:type, rdfs:label))
    } 
    } group by ?g ?p ?class
  </code> </a>
  </p>

</div>
</div>

