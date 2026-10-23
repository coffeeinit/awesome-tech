name: Submit a Database
description: Suggest a new database to be added to the list
title: "[Add]: <Database Name>"
labels: ["enhancement", "database-submission"]
body:
  - type: input
    id: db_name
    attributes:
      label: Database Name
      placeholder: "e.g., DuckDB"
    validations:
      required: true
  - type: input
    id: db_url
    attributes:
      label: Website or Repository URL
      placeholder: "https://..."
    validations:
      required: true
  - type: dropdown
    id: db_category
    attributes:
      label: Category
      options:
        - Embedded Databases
        - Vector Databases
        - Backend-as-a-Service (BaaS)
        - Relational Databases (RDBMS)
        - Document Databases
        - Key-Value Stores
        - In-Memory Databases
        - Columnar Analytics (OLAP)
        - Graph Databases
        - Time-Series Databases
        - Wide-Column Stores
        - Search Engine Databases
        - Spatial & Geospatial
        - Immutable & Ledger
        - Version-Controlled
        - Event-Sourcing
        - CRDT & Local-First Sync
    validations:
      required: true
  - type: textarea
    id: db_desc
    attributes:
      label: Short Description
      placeholder: "1-sentence summary of what it does."
    validations:
      required: true
