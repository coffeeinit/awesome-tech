# Awesome Databases [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of modern database systems categorized strictly by core architecture.

## Table of Contents

1. [Embedded Databases](#1-embedded-databases)
2. [Vector Databases](#2-vector-databases)
3. [Backend-as-a-Service (BaaS)](#3-backend-as-a-service-baas)
4. [Relational Databases (RDBMS)](#4-relational-databases-rdbms)
5. [Document Databases](#5-document-databases)
6. [Key-Value Stores](#6-key-value-stores)
7. [In-Memory Databases](#7-in-memory-databases)
8. [Columnar Analytics (OLAP) Databases](#8-columnar-analytics-olap-databases)
9. [Graph Databases](#9-graph-databases)
10. [Time-Series Databases](#10-time-series-databases)
11. [Wide-Column Stores](#11-wide-column-stores)
12. [Search Engine Databases](#12-search-engine-databases)
13. [Spatial & Geospatial Databases](#13-spatial--geospatial-databases)
14. [Immutable & Ledger Databases](#14-immutable--ledger-databases)
15. [Version-Controlled Databases](#15-version-controlled-databases)
16. [Event-Sourcing Databases](#16-event-sourcing-databases)
17. [CRDT & Local-First Sync Engines](#17-crdt--local-first-sync-engines)
18. [Object Databases](#18-object-databases)
19. [RDF / Triple Stores & Knowledge Graphs](#19-rdf--triple-stores--knowledge-graphs)
20. [Multi-Model Databases](#20-multi-model-databases)
21. [Streaming & Real-Time Databases](#21-streaming--real-time-databases)
22. [Data Lakehouse & Table Formats](#22-data-lakehouse--table-formats)
23. [Query Engines & Federation](#23-query-engines--federation)
24. [Cache & Data Grid](#24-cache--data-grid)
25. [Mobile & Local-First Databases](#25-mobile--local-first-databases)

---

### 1. Embedded Databases

*Databases meant to run directly inside application binaries or on device disk/memory.*

* [**SQLite**](https://sqlite.org) – Serverless file-based transactional database engine
* [**DuckDB**](https://duckdb.org) – Embedded in-process analytical SQL engine
* [**PocketBase**](https://pocketbase.io) – Embedded Go-based database with admin dashboard
* [**LibSQL**](https://github.com/tursodatabase/libsql) – Open-source SQLite fork created for serverless edge deployments
* [**PGLite**](https://pglite.dev) – Lightweight PostgreSQL engine compiled to WebAssembly
* [**Realm**](https://github.com/realm/realm-core) – Mobile-first object database for client applications
* [**RocksDB**](https://rocksdb.org) – Embeddable persistent key-value store optimized for fast storage
* [**LevelDB**](https://github.com/google/leveldb) – Fast key-value storage library written at Google
* [**LMDB**](https://www.symas.com/lmdb) – Ultra-fast memory-mapped embedded key-value database
* [**UnQLite**](https://unqlite.org) – Embedded NoSQL transactional database engine
* [**ObjectBox**](https://objectbox.io) – High-speed embedded database for mobile and IoT applications
* [**WatermelonDB**](https://watermelondb.dev) – High-performance reactive database framework for React Native
* [**RxDB**](https://rxdb.info) – Local-first reactive database engine for Web Applications
* [**BerkeleyDB**](https://www.oracle.com/database/technologies/related/berkeleydb.html) – Legacy embedded key-value database library
* [**TinyDB**](https://github.com/msiemens/tinydb) – Lightweight document-oriented embedded database for Python
* [**H2**](https://h2database.com) – Lightweight embedded SQL engine written in Java
* [**HSQLDB**](https://hsqldb.org) – HyperSQL relational database engine written in Java
* [**Apache Derby**](https://db.apache.org/derby/) – Open-source relational database implemented entirely in Java
* [**BadgerDB**](https://github.com/dgraph-io/badger) – Fast embedded key-value database written in Go
* [**Sled**](https://github.com/spacejam/sled) – Modern embedded key-value store written in Rust
* [**Couchbase Lite**](https://www.couchbase.com/products/lite) – Embedded, syncable JSON document database for mobile and edge devices
* [**PouchDB**](https://pouchdb.com) – JavaScript database that syncs with CouchDB, runs in the browser
* [**NeDB**](https://github.com/louischatriot/nedb) – Embedded persistent database for Node.js, Electron, and the browser
* [**LokiJS**](https://github.com/techfort/LokiJS) – Fast, in-memory document-oriented datastore for Node.js and browser
* [**LowDB**](https://github.com/typicode/lowdb) – Small local JSON database powered by Lodash
* [**ZODB**](https://zodb.org) – Native object database for Python applications
* [**db4o**](https://en.wikipedia.org/wiki/Db4o) – Object database for Java and .NET (legacy)
* [**ObjectDB**](https://www.objectdb.com) – Object-oriented database management system for Java

---

### 2. Vector Databases

*Databases engineered specifically for storing, indexing, and querying high-dimensional embeddings.*

* [**Pinecone**](https://www.pinecone.io) – Cloud-native managed vector search service
* [**Milvus**](https://milvus.io) – Open-source distributed vector database
* [**Qdrant**](https://qdrant.tech) – Vector similarity search engine written in Rust
* [**Chroma**](https://www.trychroma.com) – Open-source embedding database for AI application development
* [**Weaviate**](https://weaviate.io) – Open-source vector engine with native machine-learning integrations
* [**LanceDB**](https://lancedb.com) – Developer-friendly embedded vector engine powered by Apache Arrow
* [**Marqo**](https://www.marqo.ai) – Tensor search engine with integrated multi-modal embeddings
* [**Vespa**](https://vespa.ai) – Scalable engine for big-data vector indexing and search
* [**Vald**](https://vald.vdaas.org) – Highly scalable distributed vector search engine built on Kubernetes
* [**Faiss**](https://github.com/facebookresearch/faiss) – Library for dense vector similarity search and clustering
* [**Deep Lake**](https://github.com/activeloop-ai/deeplake) – Vector database tailored specifically for deep learning datasets
* [**Turbopuffer**](https://turbopuffer.com) – Serverless vector database built on cloud object storage
* [**MyScale**](https://github.com/myscale/myscaledb) – Vector database tailored for SQL-based AI workloads
* [**Zilliz**](https://zilliz.com) – Cloud-managed enterprise platform powered by Milvus
* [**zvec**](https://github.com/alibaba/zvec) – Embedded vector database designed for on-device RAG
* [**pgvector**](https://github.com/pgvector/pgvector) – Open-source vector similarity search extension for PostgreSQL
* [**sqlite-vec**](https://github.com/asg017/sqlite-vec) – Vector search extension for SQLite, runs anywhere SQLite runs
* [**DuckDB VSS**](https://duckdb.org/docs/extensions/vss) – Vector similarity search extension for DuckDB
* [**Apache Lucene**](https://lucene.apache.org) – Java library providing full-text search with vector similarity support

---

### 3. Backend-as-a-Service (BaaS)

*Fully integrated application platforms combining real-time database, auth, and APIs.*

* [**Supabase**](https://supabase.com) – Open-source Firebase alternative built on top of PostgreSQL
* [**Firebase Realtime Database**](https://firebase.google.com/products/realtime-database) – Cloud-hosted NoSQL JSON store with live synchronization
* [**Firestore**](https://firebase.google.com/products/firestore) – Flexible, scalable NoSQL document backend platform
* [**Appwrite**](https://appwrite.io) – Self-hosted backend suite providing databases, storage, and authentication
* [**Nhost**](https://nhost.io) – Backend platform providing GraphQL APIs over PostgreSQL
* [**SurrealDB**](https://surrealdb.com) – Multi-model cloud platform database
* [**Convex**](https://www.convex.dev) – Reactive, real-time backend platform database
* [**InstantDB**](https://www.instantdb.com) – Client-side reactive graph backend engine
* [**Parse Platform**](https://parseplatform.org) – Open-source application backend framework
* [**Amplify DataStore**](https://docs.amplify.aws/gen1/javascript/build-a-backend/more-features/datastore/) – Offline-first cloud platform database by AWS
* [**8base**](https://www.8base.com) – Low-code cloud database engine powered by GraphQL
* [**Xano**](https://www.xano.com) – Scalable visual backend engine with hosted database
* [**Backendless**](https://backendless.com) – Visual development platform with built-in database services
* [**Hasura**](https://hasura.io) – Instant GraphQL and REST API engine over databases

---

### 4. Relational Databases (RDBMS)

*Classic row-oriented transactional SQL databases supporting strict ACID properties.*

* [**PostgreSQL**](https://www.postgresql.org) – Open-source object-relational database management system
* [**MySQL**](https://www.mysql.com) – Popular open-source relational database management system
* [**MariaDB**](https://mariadb.org) – Enterprise-grade community fork of MySQL
* [**Microsoft SQL Server**](https://www.microsoft.com/sql-server) – Enterprise relational database system developed by Microsoft
* [**Oracle Database**](https://www.oracle.com/database/) – Enterprise multi-model relational database system
* [**IBM Db2**](https://www.ibm.com/products/db2) – High-performance enterprise relational database
* [**Amazon Aurora**](https://aws.amazon.com/rds/aurora/) – Cloud-optimized relational engine compatible with Postgres and MySQL
* [**Google Cloud Spanner**](https://cloud.google.com/spanner) – Fully managed globally distributed relational SQL database
* [**CockroachDB**](https://www.cockroachlabs.com) – Distributed SQL database designed for cloud resilience
* [**YugabyteDB**](https://www.yugabyte.com) – Cloud-native distributed SQL database engine
* [**TiDB**](https://github.com/pingcap/tidb) – Open-source distributed SQL database compatible with MySQL
* [**AlloyDB**](https://cloud.google.com/alloydb) – Fully managed PostgreSQL-compatible engine built for enterprise workloads
* [**Firebird**](https://firebirdsql.org) – Relational database offering ANSI SQL features in a small footprint
* [**SingleStore**](https://www.singlestore.com) – Cloud-native distributed SQL engine for real-time transactions
* [**OceanBase**](https://www.oceanbase.com) – Enterprise distributed financial-grade relational database
* [**Informix**](https://www.ibm.com/products/informix) – High-efficiency relational database engine by IBM
* [**Percona Server for MySQL**](https://www.percona.com/mysql/software/percona-server-for-mysql) – Enterprise-enhanced drop-in replacement for MySQL
* [**Virtuoso**](https://virtuoso.openlinksw.com) – Hybrid relational engine with SPARQL capabilities
* [**SQLite Cloud**](https://sqlitecloud.io) – Cloud-distributed implementation of SQLite engines
* [**SAP HANA**](https://www.sap.com/products/technology-platform/hana.html) – In-memory, column-based relational database available as appliance or cloud service
* [**NuoDB**](https://www.nuodb.com) – Webscale distributed SQL database supporting ACID transactions
* [**VoltDB**](https://www.voltactivedata.com) – Distributed in-memory NewSQL RDBMS for high-frequency OLTP applications
* [**MySQL Cluster**](https://www.mysql.com/products/cluster/) – Shared-nothing distributed MySQL with NDB storage engine
* [**Azure SQL Database**](https://azure.microsoft.com/products/azure-sql/database/) – Fully managed intelligent cloud SQL database
* [**Azure Synapse Analytics**](https://azure.microsoft.com/products/synapse-analytics) – Cloud data warehouse formerly known as Azure SQL Data Warehouse

---

### 5. Document Databases

*Schema-flexible databases storing semi-structured documents (JSON, BSON, XML).*

* [**MongoDB**](https://www.mongodb.com) – Document-oriented NoSQL database system
* [**CouchDB**](https://couchdb.apache.org) – Open-source document database using HTTP and REST APIs
* [**Couchbase**](https://www.couchbase.com) – Distributed JSON document database with built-in caching
* [**Amazon DocumentDB**](https://aws.amazon.com/documentdb/) – Fully managed JSON document database service
* [**Azure Cosmos DB**](https://azure.microsoft.com/products/cosmos-db) – Multi-model globally distributed document database
* [**RethinkDB**](https://rethinkdb.com) – Real-time JSON database designed for push updates
* [**RavenDB**](https://ravendb.net) – Fully transactional NoSQL document database engine
* [**MarkLogic**](https://www.progress.com/marklogic) – Multi-model enterprise database for XML and JSON
* [**FerretDB**](https://www.ferretdb.com) – Open-source MongoDB alternative built on PostgreSQL
* [**ArangoDB**](https://arangodb.com) – Multi-model document and graph database
* [**OrientDB**](https://orientdb.org) – Multi-model document-graph hybrid database
* [**BaseX**](https://basex.org) – XML database engine and XPath/XQuery processor
* [**eXist-db**](https://exist-db.org) – Open-source native XML database
* [**Tigris**](https://github.com/tigrisdata/tigris) – Serverless document database built for cloud developers
* [**Percona Server for MongoDB**](https://www.percona.com/mongodb/software/percona-server-for-mongodb) – Enterprise replacement for MongoDB Community Edition
* [**PouchDB**](https://pouchdb.com) – JavaScript document database that syncs with CouchDB
* [**NeDB**](https://github.com/louischatriot/nedb) – Embedded persistent document database for Node.js
* [**LokiJS**](https://github.com/techfort/LokiJS) – In-memory document-oriented datastore for Node.js and browser
* [**LowDB**](https://github.com/typicode/lowdb) – Small local JSON database powered by Lodash

---

### 6. Key-Value Stores

*Persistent or persistent-optional data stores operating on single unique keys.*

* [**Etcd**](https://etcd.io) – Strongly consistent distributed key-value store used for system state
* [**Consul KV**](https://developer.hashicorp.com/consul/docs/dynamic-app-config/kv) – Distributed key-value store for configuration management
* [**Aerospike**](https://aerospike.com) – Flash-optimized real-time key-value database
* [**TiKV**](https://tikv.org) – Distributed transactional key-value database engine
* [**FoundationDB**](https://www.foundationdb.org) – Distributed key-value database built for ACID transactions
* [**BoltDB**](https://github.com/etcd-io/bbolt) – Pure Go persistent key-value store
* [**BerkeleyDB KV**](https://www.oracle.com/database/technologies/related/berkeleydb.html) – Low-level key-value data storage framework
* [**UnQLite KV**](https://unqlite.org) – Transactional key-value engine
* [**Sled KV**](https://github.com/spacejam/sled) – Embedded lock-free key-value database
* [**Redict**](https://redict.io) – Copy-left open-source key-value database
* [**HyperDex**](https://github.com/rescrv/HyperDex) – Searchable key-value store offering consistency and speed (legacy)
* [**Oracle Coherence**](https://coherence.community) – Enterprise-grade distributed key-value data grid
* [**Riak KV**](https://riak.com/products/riak-kv/) – Distributed NoSQL key-value store written in Erlang

---

### 7. In-Memory Databases

*Databases holding all active records in system RAM for minimal query latency.*

* [**Redis**](https://redis.io) – In-memory key-value data structure store
* [**Valkey**](https://valkey.io) – Open-source, high-performance in-memory data store
* [**Memcached**](https://memcached.org) – Distributed memory object caching system
* [**Dragonfly**](https://www.dragonflydb.io) – High-throughput in-memory data store compatible with Redis
* [**KeyDB**](https://github.com/Snapchat/KeyDB) – Multithreaded high-performance fork of Redis
* [**Garnet**](https://microsoft.github.io/garnet/) – High-performance in-memory cache store developed by Microsoft
* [**Hazelcast**](https://hazelcast.com) – Distributed in-memory data grid system
* [**Apache Geode**](https://geode.apache.org) – Real-time in-memory data management system
* [**GridGain**](https://www.gridgain.com) – Enterprise in-memory computing platform built on Apache Ignite
* [**Tarantool**](https://www.tarantool.io) – In-memory database and application server engine
* [**Mnesia**](https://www.erlang.org/doc/apps/mnesia/) – Distributed in-memory DBMS built into Erlang/OTP
* [**SAP HANA**](https://www.sap.com/products/technology-platform/hana.html) – In-memory column-based relational data store
* [**VoltDB**](https://www.voltactivedata.com) – In-memory NewSQL RDBMS for high-throughput OLTP
* [**Oracle TimesTen**](https://www.oracle.com/database/technologies/timesten.html) – In-memory SQL relational database delivering microsecond response for OLTP applications
* [**Apache Ignite**](https://ignite.apache.org) – Distributed in-memory computing platform and data grid

---

### 8. Columnar Analytics (OLAP) Databases

*Column-oriented databases built specifically for heavy aggregation and analytical data warehousing.*

* [**ClickHouse**](https://clickhouse.com) – Fast open-source columnar database management system
* [**Apache Druid**](https://druid.apache.org) – Real-time analytical data store designed for low-latency queries
* [**Apache Pinot**](https://pinot.apache.org) – Distributed analytical store built for real-time aggregation
* [**Snowflake**](https://www.snowflake.com) – Enterprise cloud data warehouse platform
* [**Amazon Redshift**](https://aws.amazon.com/redshift/) – Cloud data warehouse built for large-scale data analytics
* [**Google BigQuery**](https://cloud.google.com/bigquery) – Serverless enterprise data warehouse
* [**Databricks Lakehouse**](https://www.databricks.com) – Unified data analytics platform using Delta Lake
* [**Apache Doris**](https://doris.apache.org) – Real-time analytical database based on columnar engine
* [**StarRocks**](https://www.starrocks.io) – High-performance sub-second analytical database
* [**Greenplum**](https://greenplum.org) – Open-source massively parallel processing (MPP) analytical database
* [**Teradata Vantage**](https://www.teradata.com/platform/vantage) – Enterprise multi-cloud data analytics database
* [**Exasol**](https://www.exasol.com) – In-memory columnar analytics database
* [**Vertica**](https://www.vertica.com) – Massively parallel processing columnar database engine
* [**Hydra**](https://github.com/hydradatabase/hydra) – Open-source columnar PostgreSQL extension for analytics
* [**chDB**](https://github.com/chdb-io/chdb) – Embedded ClickHouse engine running in-process
* [**Apache Kylin**](https://kylin.apache.org) – Distributed analytical data warehouse providing SQL and multidimensional analysis on Hadoop and Spark
* [**Apache Phoenix**](https://phoenix.apache.org) – Relational database engine that runs SQL queries on HBase
* [**Apache Kudu**](https://kudu.apache.org) – Columnar storage engine for fast analytics on rapidly changing data
* [**Apache Hive**](https://hive.apache.org) – Data warehouse software for reading, writing, and managing large datasets in distributed storage

---

### 9. Graph Databases

*Databases using node and edge structures to represent and query interconnected data networks.*

* [**Neo4j**](https://neo4j.com) – Enterprise graph database management system
* [**Amazon Neptune**](https://aws.amazon.com/neptune/) – Managed graph database service
* [**Memgraph**](https://memgraph.com) – In-memory graph database running on native C++
* [**Dgraph**](https://dgraph.io) – Distributed graph database with native GraphQL support
* [**JanusGraph**](https://janusgraph.org) – Scalable distributed graph database
* [**TigerGraph**](https://www.tigergraph.com) – Enterprise graph analytics engine for real-time deep queries
* [**NebulaGraph**](https://www.nebula-graph.io) – Open-source distributed graph database engine
* [**Cayley**](https://github.com/cayleygraph/cayley) – Open-source graph database created at Google
* [**ArcadeDB**](https://arcadedb.com) – Multi-model graph database supporting Cypher and SQL
* [**FalkorDB**](https://www.falkordb.com) – Low-latency graph database built on top of Redis
* [**TypeDB**](https://typedb.com) – Strongly-typed knowledge-graph engine
* [**Stardog**](https://www.stardog.com) – Enterprise knowledge graph database platform
* [**GraphDB**](https://graphdb.ontotext.com) – Semantic RDF graph database engine
* [**Apache HugeGraph**](https://hugegraph.apache.org) – Distributed graph database designed for massive data graphs
* [**AgensGraph**](https://bitnine.net/agensgraph/) – Multi-model graph database based on PostgreSQL
* [**RedisGraph**](https://redis.io/docs/stack/graph/) – Graph database module for Redis (deprecated)

---

### 10. Time-Series Databases

*Databases engineered for indexing timestamped data, telemetry, metrics, and streams.*

* [**TimescaleDB**](https://github.com/timescale/timescaledb) – PostgreSQL-based time-series database engine
* [**InfluxDB**](https://www.influxdata.com) – High-throughput open-source time-series platform
* [**Prometheus**](https://prometheus.io) – Cloud-native monitoring system with a time-series store
* [**VictoriaMetrics**](https://victoriametrics.com) – Scalable long-term storage time-series system
* [**QuestDB**](https://questdb.com) – Fast SQL time-series database engine
* [**TDengine**](https://tdengine.com) – Big data time-series database designed for IoT metrics
* [**Apache IoTDB**](https://iotdb.apache.org) – High-performance time-series database for IoT infrastructure
* [**Graphite**](https://graphiteapp.org) – Scalable real-time graphing time-series database
* [**OpenTSDB**](http://opentsdb.net) – Distributed time-series database built on top of Apache HBase
* [**ReductStore**](https://www.reduct.store) – High-performance blob and time-series storage engine
* [**kdb+**](https://kx.com) – High-performance columnar time-series database used in finance
* [**Thanos**](https://thanos.io) – Highly available Prometheus setup with long-term storage capabilities
* [**Cortex**](https://cortexmetrics.io) – Horizontally scalable, multi-tenant Prometheus-compatible time-series store
* [**Grafana Mimir**](https://grafana.com/oss/mimir/) – Horizontally scalable, long-term storage for Prometheus metrics

---

### 11. Wide-Column Stores

*Horizontally scalable NoSQL databases based on Google's Bigtable architecture.*

* [**Apache Cassandra**](https://cassandra.apache.org) – Distributed wide-column NoSQL database system
* [**ScyllaDB**](https://www.scylladb.com) – High-performance C++ implementation of Apache Cassandra
* [**Apache HBase**](https://hbase.apache.org) – Distributed wide-column store built on Apache Hadoop
* [**Amazon DynamoDB**](https://aws.amazon.com/dynamodb/) – Managed serverless wide-column NoSQL service
* [**Google Cloud Bigtable**](https://cloud.google.com/bigtable) – Enterprise NoSQL wide-column database service
* [**Apache Accumulo**](https://accumulo.apache.org) – Sorted distributed key-value store with cell-level access controls
* [**Azure Managed Cassandra**](https://azure.microsoft.com/products/managed-instance-apache-cassandra) – Cloud-managed Apache Cassandra database

---

### 12. Search Engine Databases

*Databases designed for fast text indexing, fuzzy matching, and real-time search queries.*

* [**Elasticsearch**](https://www.elastic.co/elasticsearch) – Distributed full-text search and analytics engine
* [**OpenSearch**](https://opensearch.org) – Open-source search and analytics suite derived from Elasticsearch
* [**Meilisearch**](https://www.meilisearch.com) – Fast, open-source localized full-text search engine
* [**Typesense**](https://typesense.org) – Fast, typo-tolerant open-source search engine
* [**Apache Solr**](https://solr.apache.org) – Enterprise search platform built on Apache Lucene
* [**Manticore Search**](https://manticoresearch.com) – Open-source search database for full-text and vector search
* [**Sphinx**](http://sphinxsearch.com) – Legacy open-source full-text search engine
* [**Quickwit**](https://quickwit.io) – Distributed log search engine designed for cloud storage
* [**Tantivy**](https://github.com/quickwit-oss/tantivy) – Rust-based full-text search engine library
* [**Bleve**](https://blevesearch.com) – Modern text indexing engine written in Go
* [**Sonic**](https://github.com/valeriansaliou/sonic) – Lightweight, fast search backend written in Rust
* [**Algolia**](https://www.algolia.com) – Fully managed search-as-a-service solution with SDKs for most languages
* [**Swiftype**](https://swiftype.com) – Search-as-a-service platform for websites and mobile applications

---

### 13. Spatial & Geospatial Databases

*Databases specialized for indexing, calculating, and querying spatial coordinates.*

* [**PostGIS**](https://postgis.net) – Spatial database extender for PostgreSQL
* [**Tile38**](https://tile38.com) – In-memory spatial index and real-time geofence server
* [**SpatiaLite**](https://www.gaia-gis.it/fossil/libspatialite/) – Spatial extension for SQLite database engine
* [**H3 Engine**](https://h3geo.org) – Hexagonal hierarchical spatial indexing database engine
* [**GeoServer**](https://geoserver.org) – Open-source server for sharing geospatial data
* [**MongoDB Geospatial**](https://www.mongodb.com/docs/manual/geospatial-queries/) – Native geospatial indexing and querying via GeoJSON
* [**Elasticsearch Geo**](https://www.elastic.co/guide/en/elasticsearch/reference/current/geo-queries.html) – Geospatial search capabilities within Elasticsearch
* [**Redis Geo**](https://redis.io/docs/interact/search-and-query/query/geo/) – Geospatial indexing commands for location-based queries
* [**GeoMesa**](https://www.geomesa.org) – Distributed spatio-temporal database built on Apache Accumulo, HBase, and Cassandra

---

### 14. Immutable & Ledger Databases

*Databases providing cryptographically verifiable, append-only, and tamper-proof logs.*

* [**immudb**](https://immudb.io) – Lightweight open-source immutable database built for audit logs
* [**Amazon QLDB**](https://aws.amazon.com/qldb/) – Fully managed quantum ledger database service (legacy/discontinued)
* [**Fluree**](https://flur.ee) – Immutable graph ledger database platform
* [**BigchainDB**](https://www.bigchaindb.com) – Decentralized database with blockchain characteristics

---

### 15. Version-Controlled Databases

*Databases featuring Git-like branching, merging, and version history operations.*

* [**Dolt**](https://github.com/dolthub/dolt) – Git-style version-controlled SQL database
* [**TerminusDB**](https://terminusdb.com) – Knowledge graph database with version-control revision workflows
* [**Datomic**](https://www.datomic.com) – Transactional database offering time-travel historical queries
* [**Noms**](https://github.com/attic-labs/noms) – Versionable, Git-like decentralized database engine (legacy)

---

### 16. Event-Sourcing Databases

*Databases designed to record changes in application state as an append-only stream of events.*

* [**EventStoreDB**](https://github.com/EventStore/EventStore) – Operational database built specifically for Event Sourcing
* [**Axon Server**](https://www.axoniq.io) – Dedicated event store built for CQRS and Event Sourcing architectures

---

### 17. CRDT & Local-First Sync Engines

*Sync layers designed to synchronize state between distributed devices without conflict.*

* [**ElectricSQL**](https://electric-sql.com) – Sync engine linking PostgreSQL with edge SQLite databases
* [**PowerSync**](https://www.powersync.com) – Local-first synchronization layer for mobile and edge applications
* [**Triplit**](https://www.triplit.dev) – Full-stack relational database with real-time automatic synchronization
* [**Automerge**](https://automerge.org) – JSON-like CRDT library for building collaborative applications
* [**Yjs**](https://yjs.dev) – High-performance CRDT framework for building collaborative software
* [**Replicache**](https://replicache.dev) – Client-side sync framework for building local-first web apps
* [**Evolu**](https://www.evolu.dev) – Local-first platform with CRDT-based sync and SQLite storage
* [**Jazz**](https://jazz.tools) – Framework for building local-first apps with sync and collaboration
* [**TinyBase**](https://tinybase.org) – Reactive data store with synchronization and persistence for local-first apps
* [**Dexie.js**](https://dexie.org) – IndexedDB wrapper with sync capabilities for local-first web applications

---

### 18. Object Databases

*Databases that store data as native objects, closely integrating with object-oriented programming languages.*

* [**ZODB**](https://zodb.org) – Native object database for Python applications
* [**db4o**](https://en.wikipedia.org/wiki/Db4o) – Object database for Java and .NET, known for its simplicity
* [**ObjectDB**](https://www.objectdb.com) – Object-oriented database management system for Java
* [**GemStone/S**](https://gemtalksystems.com/products/gs64/) – Mature object database and application server for Smalltalk
* [**ObjectStore**](https://en.wikipedia.org/wiki/ObjectStore) – Object-oriented database from Object Design Inc.
* [**Versant Object Database**](https://en.wikipedia.org/wiki/Versant_Corporation) – Object database for C++, Java, and .NET
* [**Perst**](https://www.mcobject.com/perst/) – Embedded object-oriented database for Java and .NET
* [**Magma**](http://wiki.squeak.org/squeak/2665) – Smalltalk object database inspired by GemStone

---

### 19. RDF / Triple Stores & Knowledge Graphs

*Databases optimized for storing and querying RDF triples and semantic knowledge graphs.*

* [**AllegroGraph**](https://allegrograph.com) – Distributed graph and document database supporting OWL reasoning
* [**Blazegraph**](https://blazegraph.com) – High-performance RDF triple store with GPU acceleration
* [**Apache Jena TDB**](https://jena.apache.org/documentation/tdb/) – Native RDF triple store component of the Apache Jena framework
* [**Eclipse RDF4J**](https://rdf4j.org) – Java framework for processing RDF data, formerly known as Sesame
* [**GraphDB**](https://graphdb.ontotext.com) – Semantic RDF graph database engine from Ontotext
* [**Stardog**](https://www.stardog.com) – Enterprise knowledge graph platform with reasoning capabilities
* [**Virtuoso Universal Server**](https://virtuoso.openlinksw.com) – Hybrid RDF and relational database server
* [**MarkLogic**](https://www.progress.com/marklogic) – Multi-model database with native RDF and triple store support
* [**AnzoGraph DB**](https://www.cambridgesemantics.com/anzograph/) – Massively parallel RDF graph database for analytics

---

### 20. Multi-Model Databases

*Databases that natively support multiple data models (document, graph, key-value, relational) within a single engine.*

* [**ArangoDB**](https://arangodb.com) – Native multi-model database supporting document, graph, and key-value models
* [**OrientDB**](https://orientdb.org) – Multi-model database supporting document, graph, key-value, and object models
* [**SurrealDB**](https://surrealdb.com) – Multi-model database with document, graph, and relational capabilities
* [**MarkLogic**](https://www.progress.com/marklogic) – Multi-model enterprise database for documents, RDF, and semantics
* [**Azure Cosmos DB**](https://azure.microsoft.com/products/cosmos-db) – Globally distributed multi-model database with multiple API choices
* [**Couchbase**](https://www.couchbase.com) – Distributed multi-model database with document and key-value models
* [**InterSystems IRIS**](https://www.intersystems.com/products/intersystems-iris/) – Multi-model database with relational, object, and document support
* [**FaunaDB**](https://fauna.com) – Distributed multi-model database with document and relational capabilities

---

### 21. Streaming & Real-Time Databases

*Databases that continuously ingest, process, and serve data in real time through incrementally updated materialized views.*

* [**Materialize**](https://materialize.com) – Streaming database for consistency-critical workloads using SQL
* [**RisingWave**](https://risingwave.com) – Streaming database for cloud-scale real-time data processing
* [**ksqlDB**](https://ksqldb.io) – Kafka-native streaming SQL engine for real-time data processing
* [**Timeplus**](https://www.timeplus.com) – Unified stream and batch SQL engine for real-time analytics
* [**DeltaStream**](https://deltastream.io) – Multi-cloud streaming database for real-time data pipelines
* [**Rockset**](https://rockset.com) – Real-time analytics database for cloud data
* [**Apache Flink**](https://flink.apache.org) – Distributed stream processing engine with SQL support
* [**Arroyo**](https://www.arroyo.dev) – Distributed stream processing engine with SQL-based pipelines

---

### 22. Data Lakehouse & Table Formats

*Open table formats that bring ACID transactions and schema evolution to data lakes.*

* [**Delta Lake**](https://delta.io) – Open-source storage framework providing ACID transactions on data lakes
* [**Apache Iceberg**](https://iceberg.apache.org) – Open table format for huge analytic datasets with schema evolution
* [**Apache Hudi**](https://hudi.apache.org) – Transactional data lake platform with upserts and incremental processing
* [**Apache Paimon**](https://paimon.apache.org) – Streaming lakehouse table format with real-time updates
* [**Apache CarbonData**](https://carbondata.apache.org) – Indexed columnar storage format for big data analytics
* [**Lance**](https://lancedb.github.io/lance/) – Columnar data format optimized for ML workloads and vector search

---

### 23. Query Engines & Federation

*SQL query engines that federate across multiple data sources without moving data.*

* [**Trino**](https://trino.io) – Distributed SQL query engine for querying heterogeneous data sources
* [**Presto**](https://prestodb.io) – Distributed SQL query engine for big data analytics
* [**Apache Drill**](https://drill.apache.org) – Schema-free SQL query engine for NoSQL, RDBMS, Hadoop, and cloud storage
* [**Apache Impala**](https://impala.apache.org) – Massively parallel SQL query engine for Hadoop data
* [**Dremio**](https://www.dremio.com) – Self-service data analytics platform with data virtualization and acceleration

---

### 24. Cache & Data Grid

*In-memory distributed caching layers and data grids for high-performance applications.*

* [**Redis**](https://redis.io) – In-memory data structure store with caching, pub/sub, and more
* [**Valkey**](https://valkey.io) – Open-source, high-performance in-memory data store
* [**Memcached**](https://memcached.org) – Distributed memory object caching system
* [**Hazelcast**](https://hazelcast.com) – Distributed in-memory data grid
* [**Apache Ignite**](https://ignite.apache.org) – Distributed in-memory computing platform and data grid
* [**Oracle Coherence**](https://coherence.community) – Enterprise-grade distributed key-value data grid
* [**Dragonfly**](https://www.dragonflydb.io) – High-throughput in-memory data store compatible with Redis

---

### 25. Mobile & Local-First Databases

*Databases designed for mobile, edge, and local-first applications with offline sync capabilities.*

* [**Couchbase Lite**](https://www.couchbase.com/products/lite) – Embedded, syncable JSON document database for mobile and edge
* [**PouchDB**](https://pouchdb.com) – JavaScript database that syncs with CouchDB, runs in the browser
* [**RxDB**](https://rxdb.info) – Local-first reactive database engine for Web Applications
* [**WatermelonDB**](https://watermelondb.dev) – High-performance reactive database framework for React Native
* [**ObjectBox**](https://objectbox.io) – High-speed embedded database for mobile and IoT applications
* [**Dexie.js**](https://dexie.org) – IndexedDB wrapper for local-first web applications
* [**Realm**](https://github.com/realm/realm-core) – Mobile-first object database for client applications
* [**UnQLite**](https://unqlite.org) – Embedded NoSQL transactional database engine
* [**TinyBase**](https://tinybase.org) – Reactive data store with synchronization for local-first apps

---

## 🤝 Contributing

Contributions are welcome! To add a database, please use the issue template.

## 📜 License

[![CC0](https://img.shields.io/badge/License-CC0%201.0-lightgrey?style=for-the-badge)](LICENSE)

To the extent possible under law, all contributors have waived all copyright and related or neighboring rights to this work.
