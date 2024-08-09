# Digital Botanical Garden Initiative queries based on the EMI ontology

All .rq files were automatically generated with the [generate-rq-files](generate-rq-files) bash script. To do so, this script retrieves the queries stored in the RDF graph `<https://sib-swiss.github.io/sparql-examples/examples/dbgi/>` in the emi-dbgi repostitory 
accessible via the SPARQL endpoint: https://biosoda.unil.ch/graphdb/repositories/emi-dbgi or with GraphDB workbench at https://biosoda.unil.ch/graphdb/sparql.

The queries in the RDF graph `<https://sib-swiss.github.io/sparql-examples/examples/dbgi/>` were loaded from the Turtle files available at https://github.com/sib-swiss/sparql-examples/tree/master/examples/dbgi

For further information about the EMI ontology, see [here](https://github.com/digital-botanical-gardens-initiative/earth_metabolome_ontology/tree/main)

# Running the rq file generator
Install jq, a json command line tool: https://jqlang.github.io/jq/
- Ubuntu
`sudo apt-get install jq`
- MacOs with brew
`brew install jq`

Run the script
```bash 
./generate-rq-files -o ./ -t "#+\t- DBGI\n" -p "emi-dbgi" -e "https://biosoda.unil.ch/graphdb/repositories/emi-dbgi"
```

The files will be saved in the current directory where the script was executed as defined with option `-o`. For more information about options, run 

`./generate-rq-files -h` 
