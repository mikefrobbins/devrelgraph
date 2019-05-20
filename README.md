# devrelgraph
Hackathon project for graph  database for docs.

## Cypher to load files

```USING PERIODIC COMMIT
LOAD CSV WITH HEADERS FROM "http://www.mattbriggs.us/mycdn/nodefile.csv" AS row
CREATE (:Doc {filename: row.filename, filetype: row.type, path: row.path});```

Note: You can also use "file:///" to point to a local file.

to clear the database. This will delete all nodes in the database.

`MATCH (n) Delete (n)`