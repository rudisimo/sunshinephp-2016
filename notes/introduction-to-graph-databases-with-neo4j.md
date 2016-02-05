# Introduction to Graph Databases with Neo4j
> by: [Michael Moussa][1]  
> [https://legacy.joind.in/16780][2]

## Preface

### Seven bridges of Königsberg

* Proved by Euler in 1736 that the answer is "No"
* His solution is the first theorem of graph theory

### Applications

* Driving directions
* Product recommendations
* Financial fraud detection

### Differences

* RDBMS
  * Highly structured
  * Entities related via JOIN tables and FK
* Graph DB
  * Schemaless, flexible
  * Relationships are as important as the data itself

## neo4j

### Labeled Property Graph

* Entities are nodes containing various properties
* Relationships connect those nodes to others
* Nodes are grouped with like nodes using labels

### Cypher

* Neo4j's query language
* Declarative
* SQL-inspired
* Open Source: [http://opencypher.org](http://opencypher.org)

### Syntax

* Tokens are case-sensitive
* Relationships are arbitrary

### Resources

* Server: [http://neo4j.org/download](http://neo4j.org/download)
* Neo4j-PHP-Client: `composer require neoxygen/neoclient`


[1]: https://twitter.com/michaelmoussa
[2]: https://legacy.joind.in/16780
