 v

Graph Databases allow vertices and edges both to have properties

Edges <-> Foreign Keys (You cannot have metadata between foreign keys)
Graph databases are relevant when you have frequent many to many relationships

*Common Graph Problems*
Dependencies
 - Failure Chains
 - Order of Operation

Clustering
 - Finding things closely related to each other (Friend of friends, Fraud)

Similarity
 - Similar paths or patterns

Matching / Categorization
 - Google Maps

Database Types
- Key Value : Dynamo DB, Redist
- Column Family : Cassandra, Apache HBase
- Document : MongoDB, CouchBase
- Relational (SQL) : Oracle, Microsoft SQL Server
- Graph : Neo4J, Datastax

RDF versus Property Model
- Work with Subject - Predicate Object
- Entities are triplets
- Efficiently in finding relationships in your data

Property Model
- Work with Nodes-Edges-Properties
- Seperate Entities for Edges and Nodes
- Both Nodes and Edges can have properties
- Efficiently traverse relationships in your data