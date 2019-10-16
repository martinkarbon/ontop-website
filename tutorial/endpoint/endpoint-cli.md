# Setting up an Ontop SPARQL endpoint with Ontop CLI

1. Download [Ontop CLI](https://github.com/ontop/ontop/releases) and unzip it to a directory, which is denoted as `$ONTOP_CLI_DIR` below.
2. Copy the H2 jdbc driver to `$ONTOP_CLI_DIR/jdbc` (if not done yet)
    * Mac/Linux: `cp jdbc/h2-1.4.196.jar $ONTOP_CLI_IDR/jdbc`
3. Start the h2 database.
4. Download [this OWL ontology file](input/university-complete.ttl).
5. Download [this mapping file](input/university-complete.obda).
6. Download [this properties file](input/university-complete.properties).
7. Start the Ontop endpoint:

```console
$ONTOP_CLI_DIR/ontop endpoint \
    --ontology=input/university-complete.ttl \
    --mapping=input/university-complete.obda \
    --properties=input/university-complete.properties \
    --cors-allowed-origins=http://yasgui.org # if needed
```

For Windows:

```console
ontop endpoint ^
    --ontology=input/university-complete.ttl ^
    --mapping=input/university-complete.obda ^
    --properties=input/university-complete.properties ^
    --cors-allowed-origins=http://yasgui.org 
```
