# GraphQL Engineering Handbook
## From first principles to production APIs, monoliths, microservices, Redis, Kafka, security, clients, and building your own GraphQL platform

> **Purpose:** A practical, architecture-first guide for learning GraphQL and using it as a serious API layer in your own projects.
>
> **Core idea:** GraphQL is not a database, not an ORM, not a microservice framework, and not a replacement for HTTP. It is a typed API query language and execution model that can sit above almost any backend.

---

# Table of Contents

1. [What GraphQL actually is](#1-what-graphql-actually-is)
2. [What Meta originally built GraphQL to solve](#2-what-meta-originally-built-graphql-to-solve)
3. [GraphQL mental model](#3-graphql-mental-model)
4. [GraphQL versus REST](#4-graphql-versus-rest)
5. [The complete GraphQL request lifecycle](#5-the-complete-graphql-request-lifecycle)
6. [Schema-first design](#6-schema-first-design)
7. [Queries](#7-queries)
8. [Variables, aliases, fragments, directives](#8-variables-aliases-fragments-directives)
9. [Mutations](#9-mutations)
10. [Subscriptions and real-time systems](#10-subscriptions-and-real-time-systems)
11. [Resolvers](#11-resolvers)
12. [DataLoader and the N+1 problem](#12-dataloader-and-the-n1-problem)
13. [GraphQL as an API layer over databases](#13-graphql-as-an-api-layer-over-databases)
14. [GraphQL over REST and existing services](#14-graphql-over-rest-and-existing-services)
15. [GraphQL + Redis](#15-graphql--redis)
16. [GraphQL + Kafka](#16-graphql--kafka)
17. [GraphQL + Redis + Kafka together](#17-graphql--redis--kafka-together)
18. [Monolithic GraphQL architecture](#18-monolithic-graphql-architecture)
19. [Modular monolith](#19-modular-monolith)
20. [Microservices and federated GraphQL](#20-microservices-and-federated-graphql)
21. [When NOT to use federation](#21-when-not-to-use-federation)
22. [Building your own GraphQL gateway](#22-building-your-own-graphql-gateway)
23. [Meta / Relay design lessons](#23-meta--relay-design-lessons)
24. [GraphQL security](#24-graphql-security)
25. [Authentication](#25-authentication)
26. [Authorization](#26-authorization)
27. [Query complexity, depth, batching and DoS](#27-query-complexity-depth-batching-and-dos)
28. [Introspection and production exposure](#28-introspection-and-production-exposure)
29. [Persisted queries and trusted documents](#29-persisted-queries-and-trusted-documents)
30. [Rate limiting](#30-rate-limiting)
31. [Caching](#31-caching)
32. [HTTP, CDN and transport](#32-http-cdn-and-transport)
33. [Error handling](#33-error-handling)
34. [Transactions and mutations](#34-transactions-and-mutations)
35. [Idempotency](#35-idempotency)
36. [Observability](#36-observability)
37. [Tracing](#37-tracing)
38. [Schema evolution](#38-schema-evolution)
39. [API versioning](#39-api-versioning)
40. [GraphQL clients](#40-graphql-clients)
41. [Relay-style client architecture](#41-relay-style-client-architecture)
42. [Web applications](#42-web-applications)
43. [Mobile applications](#43-mobile-applications)
44. [Multiple frontends and one graph](#44-multiple-frontends-and-one-graph)
45. [Files, uploads and downloads](#45-files-uploads-and-downloads)
46. [Background jobs](#46-background-jobs)
47. [Search engines](#47-search-engines)
48. [Object storage](#48-object-storage)
49. [GraphQL with PostgreSQL](#49-graphql-with-postgresql)
50. [GraphQL with MongoDB](#50-graphql-with-mongodb)
51. [GraphQL with gRPC](#51-graphql-with-grpc)
52. [GraphQL and event-driven architecture](#52-graphql-and-event-driven-architecture)
53. [GraphQL gateway patterns](#53-graphql-gateway-patterns)
54. [Schema organization](#54-schema-organization)
55. [Naming conventions](#55-naming-conventions)
56. [Pagination](#56-pagination)
57. [Filtering, sorting and searching](#57-filtering-sorting-and-searching)
58. [Relay Cursor Connections](#58-relay-cursor-connections)
59. [Bulk operations](#59-bulk-operations)
60. [Multi-tenancy](#60-multi-tenancy)
61. [RBAC and ABAC](#61-rbac-and-abac)
62. [Service-to-service security](#62-service-to-service-security)
63. [Secrets](#63-secrets)
64. [Production architecture](#64-production-architecture)
65. [High availability](#65-high-availability)
66. [Scaling](#66-scaling)
67. [Failure modes](#67-failure-modes)
68. [Testing](#68-testing)
69. [Load testing](#69-load-testing)
70. [Schema testing](#70-schema-testing)
71. [Security testing](#71-security-testing)
72. [Building a GraphQL server from scratch](#72-building-a-graphql-server-from-scratch)
73. [Building your own GraphQL platform](#73-building-your-own-graphql-platform)
74. [A practical Go architecture](#74-a-practical-go-architecture)
75. [A practical TypeScript architecture](#75-a-practical-typescript-architecture)
76. [Suggested project layout](#76-suggested-project-layout)
77. [Example production schema](#77-example-production-schema)
78. [Example request flow](#78-example-request-flow)
79. [Example Redis architecture](#79-example-redis-architecture)
80. [Example Kafka architecture](#80-example-kafka-architecture)
81. [Example microservice architecture](#81-example-microservice-architecture)
82. [A custom GraphQL router design](#82-a-custom-graphql-router-design)
83. [GraphQL gateway versus REST gateway](#83-graphql-gateway-versus-rest-gateway)
84. [Common mistakes](#84-common-mistakes)
85. [What to learn first](#85-what-to-learn-first)
86. [Production checklist](#86-production-checklist)
87. [Reference sources](#87-reference-sources)

---

# 1. What GraphQL actually is

GraphQL is a **typed query language and execution system for APIs**.

A client describes the shape of the data it wants:

```graphql
query GetUser {
  user(id: "123") {
    id
    name
    email
  }
}
```

The server validates that request against a schema and executes the fields through resolver functions.

The response follows the requested shape:

```json
{
  "data": {
    "user": {
      "id": "123",
      "name": "Jana",
      "email": "user@example.com"
    }
  }
}
```

The important point is:

**GraphQL does not own your data.**

It can sit above:

- PostgreSQL
- MySQL
- MongoDB
- Redis
- Kafka
- REST APIs
- gRPC services
- legacy systems
- search engines
- object storage
- external SaaS APIs
- filesystem services
- business logic
- other GraphQL services

Meta explicitly described GraphQL as a protocol/API layer rather than a storage system. Their original implementation was designed to use existing databases and business logic rather than replace them.

That distinction is fundamental.

---

# 2. What Meta originally built GraphQL to solve

GraphQL originated inside Facebook/Meta around the needs of its mobile applications.

The original problem was not:

> "We need a cooler version of REST."

The problem was closer to:

> "Our clients need complex, nested product data, and the server API should let the client describe that data without forcing the client into a fixed set of resource endpoints."

Meta's original engineering article describes several important characteristics:

1. **Hierarchical**
2. **Strongly typed**
3. **Client-shaped responses**
4. **Storage agnostic**
5. **Introspective**
6. **Version-friendly**

Source:

https://engineering.fb.com/2015/09/14/core-infra/graphql-a-data-query-language/

The original Meta explanation is especially important because it prevents a common misunderstanding.

GraphQL is not:

```text
GraphQL -> Database
```

It is more like:

```text
                 ┌───────────────┐
Web ------------>│               │
Mobile ---------->│   GraphQL     │
Desktop --------->│   API Layer   │
CLI -------------->│               │
Other services --->│               │
                 └───────┬───────┘
                         │
            ┌────────────┼────────────┐
            │            │            │
        PostgreSQL     Redis        REST
            │            │            │
         services      cache       services
```

GraphQL decides how a client can ask for data.

It does not dictate where the data comes from.

---

# 3. GraphQL mental model

Think of GraphQL as a typed graph-shaped contract.

Suppose your application has:

```text
User
 ├── Orders
 │    └── Products
 └── Profile
      └── Organization
```

A GraphQL query can follow those relationships:

```graphql
query {
  user(id: "123") {
    name

    profile {
      avatarUrl
    }

    orders {
      id

      products {
        name
        price
      }
    }
  }
}
```

The graph is logical.

Your database does not have to literally be a graph database.

For example:

```text
PostgreSQL

users
orders
order_items
products
profiles
organizations
```

can still be exposed as:

```text
User
 ├── profile
 ├── orders
 │    └── products
 └── organization
```

The resolver layer creates that logical graph.

---

# 4. GraphQL versus REST

GraphQL and REST are not mutually exclusive.

A serious architecture can use both.

## REST

A REST-oriented API might expose:

```http
GET /users/123
GET /users/123/orders
GET /orders/456
GET /orders/456/items
GET /products/789
```

The client may need multiple requests.

## GraphQL

The same product can expose:

```graphql
query {
  user(id: "123") {
    name
    orders {
      id
      items {
        product {
          name
        }
      }
    }
  }
}
```

The client describes the desired shape.

## GraphQL can sit above REST

For example:

```text
                    GraphQL
                       │
             ┌─────────┼─────────┐
             │         │         │
          REST API   PostgreSQL  Redis
             │
          Legacy ERP
```

The GraphQL resolver for:

```graphql
customer(id: ID!)
```

could call:

```http
GET /legacy/customers/{id}
```

There is no rule saying GraphQL resolvers must directly query SQL.

Apollo Federation also explicitly supports combining GraphQL APIs with REST APIs and other sources.

---

# 5. The complete GraphQL request lifecycle

A production request can conceptually pass through these stages:

```text
Client
  │
  │ HTTPS
  ▼
CDN / WAF / Load Balancer
  │
  ▼
Authentication
  │
  ▼
GraphQL HTTP Handler
  │
  ▼
Parse
  │
  ▼
Validate
  │
  ▼
Operation selection
  │
  ▼
Authorization
  │
  ▼
Complexity / depth checks
  │
  ▼
Persisted-operation lookup
  │
  ▼
Execution
  │
  ├── Resolver A -> Redis
  │
  ├── Resolver B -> PostgreSQL
  │
  ├── Resolver C -> REST
  │
  └── Resolver D -> service
  │
  ▼
DataLoader batching
  │
  ▼
Business logic
  │
  ▼
Response
  │
  ▼
Observability
```

For a federated system:

```text
Client
  │
  ▼
GraphQL Router
  │
  ├── Users subgraph
  ├── Orders subgraph
  ├── Products subgraph
  └── Payments subgraph
```

The router creates a plan describing which services must be queried and in what order/parallelism.

---

# 6. Schema-first design

The schema is the public contract.

Example:

```graphql
type User {
  id: ID!
  name: String!
  email: String!
}

type Query {
  user(id: ID!): User
}
```

The `!` means non-null.

```graphql
id: ID!
```

means:

```text
id must exist
```

while:

```graphql
email: String
```

means:

```text
email may be null
```

## Root types

GraphQL has root operation types:

```graphql
type Query {
  ...
}

type Mutation {
  ...
}

type Subscription {
  ...
}
```

Queries read.

Mutations change state.

Subscriptions represent long-lived event streams.

---

# 7. Queries

Basic query:

```graphql
query GetUser($id: ID!) {
  user(id: $id) {
    id
    name
  }
}
```

Variables:

```json
{
  "id": "123"
}
```

GraphQL queries are strongly typed against the schema.

If the schema says:

```graphql
user(id: ID!)
```

then this is invalid:

```graphql
user()
```

The GraphQL execution pipeline should reject invalid operations before normal resolver execution.

Official GraphQL query documentation:

https://graphql.org/learn/queries/

---

# 8. Variables, aliases, fragments, directives

## Variables

Do not construct query strings with user input.

Prefer:

```graphql
query User($id: ID!) {
  user(id: $id) {
    id
    name
  }
}
```

with:

```json
{
  "id": "123"
}
```

This provides better validation and avoids treating user data as executable query text.

## Aliases

```graphql
query {
  primary: user(id: "1") {
    name
  }

  secondary: user(id: "2") {
    name
  }
}
```

## Fragments

```graphql
fragment UserCard on User {
  id
  name
  avatarUrl
}
```

Then:

```graphql
query {
  user(id: "123") {
    ...UserCard
  }
}
```

Fragments are especially useful for component-oriented applications.

## Directives

GraphQL supports directives such as:

```graphql
@include
@skip
@deprecated
```

Servers can also define custom directives depending on the implementation.

---

# 9. Mutations

A mutation represents a state-changing operation.

Example:

```graphql
mutation CreateProject($input: CreateProjectInput!) {
  createProject(input: $input) {
    project {
      id
      name
    }
  }
}
```

Input:

```graphql
input CreateProjectInput {
  name: String!
  description: String
}
```

A useful mutation structure is:

```graphql
type Mutation {
  createProject(input: CreateProjectInput!): CreateProjectPayload!
}
```

with:

```graphql
type CreateProjectPayload {
  project: Project
  errors: [UserError!]!
}
```

This makes application errors explicit.

---

# 10. Subscriptions and real-time systems

A subscription represents a long-lived operation.

Example:

```graphql
subscription ProjectEvents($projectId: ID!) {
  projectEvents(projectId: $projectId) {
    id
    type
    timestamp
  }
}
```

Possible transport:

- WebSocket
- Server-Sent Events
- multipart HTTP
- callback-based architectures

The exact transport is not the GraphQL language itself.

GraphQL.org notes that HTTP is common for normal operations, while WebSockets or Server-Sent Events can be used for long-lived subscription operations.

Apollo currently documents multiple subscription approaches, including WebSocket-based subgraph communication and HTTP-oriented subscription delivery.

Sources:

https://graphql.org/learn/security/

https://www.apollographql.com/docs/graphos/routing/v3/operations/subscriptions/overview

Important architecture:

```text
                     Kafka
                       │
                       ▼
                Event processing
                       │
                       ▼
                 Redis / broker
                       │
                       ▼
                GraphQL servers
                       │
                       ▼
                    Clients
```

Do not rely on in-memory PubSub when multiple GraphQL instances exist.

Apollo explicitly warns that in-memory PubSub does not distribute events between multiple server instances and recommends an external event system such as Redis or Kafka.

Source:

https://www.apollographql.com/docs/apollo-server/data/subscriptions

---

# 11. Resolvers

A resolver connects a schema field to actual application behavior.

Conceptually:

```graphql
type Query {
  user(id: ID!): User
}
```

maps to:

```text
Query.user
      │
      ▼
UserService.getUser(id)
      │
      ▼
Repository
      │
      ▼
PostgreSQL
```

A resolver should normally NOT become a giant database/business-logic function.

Bad:

```text
resolver
 ├── SQL
 ├── authorization
 ├── payment logic
 ├── Kafka
 ├── cache
 ├── formatting
 └── 500 lines
```

Better:

```text
resolver
   │
   ├── authorization
   │
   ▼
service
   │
   ├── repository
   ├── cache
   ├── event publisher
   └── external clients
```

GraphQL should be the API boundary, not the place where the entire application is dumped.

---

# 12. DataLoader and the N+1 problem

Consider:

```graphql
query {
  users {
    id
    name

    organization {
      id
      name
    }
  }
}
```

Suppose there are 100 users.

A naive implementation may perform:

```text
1 query -> users

100 queries -> organizations
```

Total:

```text
101 database queries
```

This is the N+1 problem.

A DataLoader-style design batches:

```text
1 query -> users

1 query -> organizations WHERE id IN (...)
```

Total:

```text
2 queries
```

GraphQL does not magically eliminate N+1.

You must design resolver data access correctly.

Good resolver stack:

```text
GraphQL field
     │
     ▼
DataLoader
     │
     ▼
Service / repository
     │
     ▼
database
```

For Go, the `graph-gophers/graphql-go` project documents field inspection, prefetching, and mechanisms aimed at avoiding N+1 problems.

Source:

https://github.com/graph-gophers/graphql-go

---

# 13. GraphQL as an API layer over databases

A common architecture:

```text
                     GraphQL API
                          │
        ┌─────────────────┼─────────────────┐
        │                 │                 │
       User              Order            Product
      Service            Service           Service
        │                 │                 │
        ▼                 ▼                 ▼
    PostgreSQL        PostgreSQL        PostgreSQL
```

For a monolith:

```text
GraphQL
   │
Application services
   │
Repositories
   │
PostgreSQL
```

GraphQL should not dictate whether you use:

- SQL
- ORM
- query builder
- raw SQL
- document DB
- graph DB

The storage model remains an implementation choice.

---

# 14. GraphQL over REST and existing services

A migration strategy can be:

```text
Existing REST APIs
       │
       ▼
GraphQL adapter
       │
       ▼
New clients
```

Example:

```graphql
type Query {
  customer(id: ID!): Customer
}
```

Resolver:

```text
customer(id)
    │
    ▼
GET /customers/{id}
    │
    ▼
REST service
```

This is extremely useful for legacy modernization.

You can introduce GraphQL without rewriting every backend.

Later:

```text
GraphQL
   │
   ├── REST legacy
   ├── new service
   ├── PostgreSQL
   └── external SaaS
```

Then gradually replace old sources.

---

# 15. GraphQL + Redis

Redis can have several completely different roles.

Do not think:

> GraphQL uses Redis.

Instead ask:

> Which GraphQL subsystem needs Redis?

Possible roles:

### 15.1 Cache

```text
GraphQL
   │
   ▼
Service
   │
   ├── Redis
   │
   └── PostgreSQL
```

### 15.2 Session / short-lived state

```text
GraphQL
   │
   ▼
Redis session
```

### 15.3 Rate limiting

```text
request
   │
   ▼
Redis counter
   │
   ├── allowed
   └── rejected
```

### 15.4 Pub/Sub

```text
GraphQL server A
      │
      ▼
    Redis
      │
      ▼
GraphQL server B
```

### 15.5 Distributed locks

Use carefully.

A lock is not automatically a transaction.

### 15.6 Persisted query registry

```text
operation hash
      │
      ▼
Redis
      │
      ▼
stored GraphQL operation
```

Redis is infrastructure around GraphQL, not a requirement of GraphQL.

---

# 16. GraphQL + Kafka

Kafka is fundamentally different from Redis Pub/Sub.

Kafka is designed around durable event streams, partitions, consumer groups and replayable event processing.

GraphQL is a request/response API layer.

A strong architecture often looks like:

```text
Client
  │
  ▼
GraphQL
  │
  ├── Query -> database
  │
  └── Mutation
        │
        ▼
     application
        │
        ├── database transaction
        │
        └── Kafka event
```

Example:

```graphql
mutation CreateOrder($input: CreateOrderInput!) {
  createOrder(input: $input) {
    order {
      id
      status
    }
  }
}
```

The application can:

1. validate authorization
2. validate input
3. create order
4. commit transaction
5. publish an event
6. return the mutation result

The exact event consistency strategy matters.

---

# 17. GraphQL + Redis + Kafka together

A more complete system:

```text
                         ┌──────────────┐
Web -------------------->│              │
Mobile ----------------->│   GraphQL    │
Desktop ---------------->│     API      │
CLI -------------------->│              │
                         └──────┬───────┘
                                │
                 ┌──────────────┼──────────────┐
                 │              │              │
                 ▼              ▼              ▼
              Redis        Application       PostgreSQL
             cache        services             │
                 │              │              │
                 │              ▼              │
                 │            Kafka <──────────┘
                 │              │
                 │       ┌──────┼──────┐
                 │       ▼      ▼      ▼
                 │    Search  Email  Analytics
                 │
                 ▼
             subscriptions
                 │
                 ▼
              clients
```

A useful division is:

```text
GraphQL = client-facing API

PostgreSQL = authoritative transactional state

Redis = fast ephemeral/distributed state

Kafka = durable asynchronous event stream

Workers = asynchronous processing
```

This separation keeps the architecture understandable.

---

# 18. Monolithic GraphQL architecture

Start simple.

A production monolith can be:

```text
                    Internet
                       │
                       ▼
                  Load Balancer
                       │
                       ▼
                GraphQL application
                       │
       ┌───────────────┼────────────────┐
       │               │                │
    Users module    Orders module    Billing module
       │               │                │
       └───────────────┼────────────────┘
                       │
                  PostgreSQL
```

One process.

One GraphQL schema.

One deployment.

Internally modular.

This is often the best place to start.

Do not create 15 microservices just because GraphQL can federate them.

---

# 19. Modular monolith

A stronger intermediate design:

```text
GraphQL
   │
   ├── users/
   ├── projects/
   ├── billing/
   ├── notifications/
   └── analytics/
```

Each module owns:

- schema types
- resolver registration
- service layer
- repository layer
- events
- tests

But everything can still run in one process.

Example:

```text
modules/
  users/
    schema.graphql
    resolver.go
    service.go
    repository.go

  orders/
    schema.graphql
    resolver.go
    service.go
    repository.go
```

Later a module can become a service.

This is an excellent migration path.

---

# 20. Microservices and federated GraphQL

When the system becomes large:

```text
                    Client
                      │
                      ▼
                GraphQL Router
                      │
       ┌──────────────┼───────────────┐
       │              │               │
       ▼              ▼               ▼
   Users service  Orders service  Payments service
       │              │               │
       ▼              ▼               ▼
   PostgreSQL     PostgreSQL       PostgreSQL
```

The client still sees:

```graphql
query {
  user(id: "1") {
    name
    orders {
      total
    }
  }
}
```

The client does not need to know:

```text
users service = service A
orders service = service B
```

Apollo describes this as federation: multiple APIs are composed into a unified graph, with a router as the single entry point.

Source:

https://www.apollographql.com/docs/graphos/schema-design/federated-schemas/federation

---

# 21. When NOT to use federation

Do not introduce federation because:

- it sounds enterprise
- you have three tables
- you want a microservice badge
- you saw a supergraph diagram
- you want to avoid designing your application

Federation introduces:

- composition
- routing
- distributed failure
- schema ownership
- service-to-service authentication
- network latency
- query planning
- cross-service authorization complexity
- distributed tracing
- deployment coordination

For a small application:

```text
GraphQL monolith
```

is usually better.

For a growing application:

```text
modular monolith
```

is often better.

For genuinely independent domains:

```text
federated graph
```

can become useful.

---

# 22. Building your own GraphQL gateway

You can build your own gateway.

Conceptually:

```text
Client
  │
  ▼
Your GraphQL Gateway
  │
  ├── validate
  ├── authenticate
  ├── authorize
  ├── rate limit
  ├── complexity check
  ├── query planning
  ├── execute
  └── observe
       │
       ├── service A
       ├── service B
       ├── REST
       ├── gRPC
       └── database
```

But distinguish two projects:

### GraphQL server

Understands:

```text
schema
parse
validate
execute
resolve
```

### GraphQL gateway/router

Adds:

```text
service discovery
schema composition
routing
query planning
distributed execution
cross-service policy
```

Do not implement federation before you understand a normal GraphQL executor.

---

# 23. Meta / Relay design lessons

Meta's Relay work is especially valuable for learning how GraphQL is used at scale.

Relay emphasizes:

- colocated data requirements
- GraphQL fragments
- declarative data fetching
- static queries
- ahead-of-time optimization
- normalized client state
- generated artifacts

Meta's Relay Modern article explains that the team wanted UI components to own their data requirements rather than forcing unrelated parts of the codebase to manage network requests.

Source:

https://engineering.fb.com/2017/04/18/web/relay-modern-simpler-faster-more-extensible/

## Colocation

A component can define:

```graphql
fragment UserProfile_user on User {
  id
  name
  avatarUrl
}
```

The component says:

> This is the data I require.

Another component can define another fragment.

A higher-level query composes them.

This is a powerful architecture for large frontends.

---

# 24. GraphQL security

GraphQL requires normal API security plus GraphQL-specific controls.

GraphQL.org identifies malicious operations and resource exhaustion as important security concerns.

Source:

https://graphql.org/learn/security/

Apollo similarly recommends defense in depth and limiting unnecessary API discoverability.

Source:

https://www.apollographql.com/docs/graphos/platform/security/overview

A production security stack can be:

```text
Internet
   │
   ▼
TLS
   │
   ▼
WAF
   │
   ▼
DDoS protection
   │
   ▼
Load balancer
   │
   ▼
Authentication
   │
   ▼
Authorization
   │
   ▼
Persisted operation check
   │
   ▼
Depth / complexity
   │
   ▼
Rate limit
   │
   ▼
GraphQL execution
```

---

# 25. Authentication

Authentication answers:

> Who is this caller?

Common approaches:

- OAuth 2.0
- OpenID Connect
- JWT
- session cookies
- API keys
- mTLS for internal services

A GraphQL request should produce a request context:

```text
context
 ├── user ID
 ├── tenant ID
 ├── roles
 ├── scopes
 ├── authentication method
 └── request ID
```

Resolvers can then use that context.

Do not trust:

```graphql
user(id: "some-other-user")
```

just because the caller is authenticated.

Authentication != authorization.

---

# 26. Authorization

Authorization answers:

> Is this caller allowed to perform this operation on this resource?

Example:

```graphql
query {
  project(id: "123") {
    secrets
  }
}
```

Being logged in is not enough.

You may need:

```text
authenticated?
    │
    ▼
belongs to tenant?
    │
    ▼
member of project?
    │
    ▼
has project.read?
    │
    ▼
can read secrets?
```

Prefer authorization based on domain rules.

Bad:

```text
if role == "admin"
```

everywhere.

Better:

```text
authorization service/policy
    │
    ├── tenant
    ├── resource
    ├── action
    └── principal
```

---

# 27. Query complexity, depth, batching and DoS

GraphQL allows nested queries.

That flexibility can become dangerous.

Example:

```graphql
query {
  users {
    friends {
      friends {
        friends {
          friends {
            friends {
              id
            }
          }
        }
      }
    }
  }
}
```

The problem is not merely query length.

A small query can cause enormous backend work.

You can use:

## Maximum depth

Example:

```text
maxDepth = 8
```

## Complexity scoring

Example conceptual cost:

```text
User = 1
Orders = 5
Order.items = 5
Product.recommendations = 20
```

Reject operations whose estimated cost exceeds a limit.

## Pagination limits

Do not allow:

```graphql
users(first: 1000000)
```

Prefer:

```text
max page size = 100
```

## Resolver timeouts

Every external operation should have a timeout.

## Concurrency limits

Do not allow a single query to fan out into thousands of downstream calls.

## Rate limiting

Apply limits per:

- IP
- user
- tenant
- token
- operation
- service

---

# 28. Introspection and production exposure

GraphQL introspection is extremely useful in development.

Tools can discover:

```text
types
fields
arguments
directives
descriptions
```

This enables:

- GraphiQL
- code generation
- IDE tooling
- schema documentation

But internal production graphs may not want unlimited public introspection.

Apollo specifically recommends restricting discoverability for non-public production graphs and ensuring subgraph internals such as `_service` are not publicly exposed.

Source:

https://www.apollographql.com/docs/graphos/platform/security/overview

Do not blindly disable introspection for every API.

Public developer APIs may intentionally need it.

Use an environment/security policy.

---

# 29. Persisted queries and trusted documents

One of the most important production techniques is:

```text
client
   │
   │ operation ID/hash
   ▼
GraphQL server
   │
   ▼
known operation registry
   │
   ▼
validate/execute
```

Instead of allowing arbitrary query text from an untrusted client, you can maintain a list of approved operations.

Meta's Relay Modern work described static queries where queries can be known ahead of time and replaced on the wire by small identifiers.

GraphQL.org's performance documentation also discusses persisted queries and trusted documents.

Sources:

https://engineering.fb.com/2017/04/18/web/relay-modern-simpler-faster-more-extensible/

https://graphql.org/learn/performance/

Benefits:

- smaller requests
- less parsing
- better caching
- operation safelisting
- reduced attack surface
- predictable workload
- easier observability

---

# 30. Rate limiting

GraphQL complicates naive rate limiting because:

```text
1 HTTP request
```

can represent very different amounts of work.

Therefore use multiple dimensions.

Example:

```text
per-IP:
  100 requests/min

per-user:
  300 requests/min

per-operation:
  search = 60/min
  expensiveReport = 10/min

complexity:
  max 1000 points/request
```

Redis is a common implementation substrate for distributed rate limits.

Example conceptual key:

```text
ratelimit:user:123:minute
```

Use atomic Redis operations and expirations.

---

# 31. Caching

GraphQL caching has multiple layers.

## Layer 1: CDN / HTTP

Good for appropriate GET requests and public/cacheable operations.

## Layer 2: persisted operation cache

```text
operation hash -> compiled/parsed operation
```

## Layer 3: query plan cache

Relevant to federated routers.

Apollo documents query plan caching as a way to avoid repeatedly generating plans for identical operations.

Source:

https://www.apollographql.com/docs/graphos/routing/v3/query-planning/caching

## Layer 4: application cache

```text
user:123 -> User
```

## Layer 5: database cache

Database buffer pools, indexes, etc.

Do not assume:

> GraphQL = uncachable.

GraphQL.org explicitly documents caching approaches and GET/persisted query strategies.

Source:

https://graphql.org/learn/performance/

---

# 32. HTTP, CDN and transport

GraphQL is commonly transported over HTTP.

A typical endpoint:

```http
POST /graphql
```

Request:

```json
{
  "query": "query User($id: ID!) { user(id: $id) { id name } }",
  "variables": {
    "id": "123"
  },
  "operationName": "User"
}
```

The protocol and transport are distinct concepts.

You can use:

- HTTP
- WebSocket
- SSE
- other transports depending on implementation/specification

Normal queries and mutations generally work well over HTTP.

Subscriptions may use a streaming transport.

---

# 33. Error handling

GraphQL responses can contain:

```json
{
  "data": {...},
  "errors": [...]
}
```

Do not expose internal stack traces.

Bad:

```json
{
  "message": "pq: password authentication failed for user postgres"
}
```

Good:

```json
{
  "message": "Internal server error",
  "extensions": {
    "code": "INTERNAL_ERROR"
  }
}
```

Internal logs can contain:

```text
request_id
trace_id
operation_name
service
exception
database error
```

The client gets a safe error.

---

# 34. Transactions and mutations

A mutation may touch multiple tables.

Example:

```text
createOrder
   │
   ├── orders
   ├── order_items
   ├── inventory
   └── payment intent
```

Do not assume GraphQL makes this atomic.

The application service must define transaction boundaries.

Example:

```text
GraphQL mutation
      │
      ▼
OrderService.Create
      │
      ▼
DB transaction
 ├── insert order
 ├── insert items
 └── update inventory
      │
      ▼
commit
```

External services require a different consistency strategy.

---

# 35. Idempotency

Mutations may be retried.

Especially with:

- mobile networks
- payment APIs
- job retries
- proxies
- client retries

A mutation like:

```graphql
mutation {
  createPayment(...)
}
```

must not accidentally charge twice.

Use idempotency keys:

```text
Idempotency-Key: abc123
```

Store the operation result against that key.

Conceptually:

```text
tenant + user + operation + idempotency_key
```

becomes a unique operation identity.

---

# 36. Observability

Every GraphQL request should be observable.

Capture:

```text
request ID
trace ID
operation name
user/tenant
latency
status
errors
complexity
depth
resolver timings
downstream calls
cache hits
cache misses
```

Avoid logging sensitive query variables blindly.

A useful metric set:

```text
graphql_requests_total
graphql_request_duration
graphql_errors_total
graphql_complexity
graphql_depth
resolver_duration
dataloader_batch_size
redis_latency
database_latency
kafka_publish_latency
```

---

# 37. Tracing

A distributed GraphQL system benefits heavily from tracing.

Example:

```text
Trace
│
├── GraphQL request
│    │
│    ├── authorization
│    │
│    ├── user resolver
│    │    └── PostgreSQL
│    │
│    └── orders resolver
│         ├── Redis
│         └── Orders service
│              └── PostgreSQL
```

Use OpenTelemetry where possible.

The Go `graph-gophers/graphql-go` project documents OpenTelemetry support.

Source:

https://github.com/graph-gophers/graphql-go

---

# 38. Schema evolution

GraphQL encourages additive schema evolution.

Instead of:

```text
/api/v1
/api/v2
/api/v3
```

you can often:

```graphql
type User {
  name: String!
  displayName: String
}
```

Add a field:

```text
displayName
```

and deprecate:

```graphql
name: String! @deprecated(reason: "Use displayName")
```

Clients can migrate independently.

This does NOT mean GraphQL has zero breaking changes.

Removing a field that clients still use is breaking.

Therefore you need:

- usage tracking
- schema checks
- deprecation policy
- client migration
- contract testing

---

# 39. API versioning

GraphQL often avoids URL versioning.

Instead:

```text
one evolving schema
```

with:

```text
add fields
deprecate fields
remove only after clients migrate
```

But versioning can still exist at other levels:

```text
schema contract version
client version
mobile application version
operation version
service API version
event version
```

GraphQL does not magically solve compatibility.

---

# 40. GraphQL clients

Common client approaches include:

- Apollo Client
- Relay
- urql
- language-specific GraphQL clients
- generated typed clients
- custom clients

The client is responsible for:

- sending operations
- variables
- caching
- retries
- error handling
- authentication
- sometimes optimistic updates

Relay is especially interesting if you want to study Meta's approach.

Meta's Relay architecture treats data dependencies as first-class, composable fragments.

---

# 41. Relay-style client architecture

The conceptual flow:

```text
Component
   │
   ├── UI definition
   │
   └── GraphQL fragment
          │
          ▼
      compiler
          │
          ▼
    generated artifact
          │
          ▼
       runtime
          │
          ▼
      GraphQL API
```

This reduces runtime query construction.

Meta's Relay Modern work explicitly describes static queries and ahead-of-time optimization.

Source:

https://engineering.fb.com/2017/04/18/web/relay-modern-simpler-faster-more-extensible/

---

# 42. Web applications

A modern web architecture:

```text
Browser
  │
  ▼
Next.js / React / Vue / other frontend
  │
  ▼
GraphQL
  │
  ├── application services
  ├── REST
  ├── PostgreSQL
  └── Redis
```

The browser does not need to know every backend service.

This is one of the strongest GraphQL use cases.

---

# 43. Mobile applications

GraphQL is especially useful for mobile because network calls can be expensive.

A mobile screen might need:

```text
user
feed
notifications
recommendations
unread count
```

REST may require several calls.

GraphQL can allow a single operation to describe the needed shape.

Meta originally built GraphQL around this class of mobile data-fetching problem.

Their later Mobile GraphQL platform continues to support Facebook and Instagram applications.

Source:

https://engineering.fb.com/2025/03/31/data-infrastructure/mobile-graphql-meta-2025/

---

# 44. Multiple frontends and one graph

One backend graph can serve:

```text
Web
Mobile iOS
Mobile Android
Desktop
Admin
CLI
Internal tools
AI agents
Partner applications
```

Example:

```text
                  GraphQL
                     │
       ┌─────────────┼──────────────┐
       │             │              │
      Web          Mobile          CLI
       │             │              │
       └─────────────┼──────────────┘
                     │
                 services
```

Each client can request the fields it needs.

This is often more maintainable than building a separate backend API for every frontend.

---

# 45. Files, uploads and downloads

Do not force large binary files through ordinary GraphQL response payloads.

A better pattern:

```graphql
mutation CreateUpload {
  createUpload(...) {
    uploadUrl
    objectKey
  }
}
```

Then:

```text
client
  │
  ├── GraphQL -> receives upload authorization
  │
  └── object storage -> uploads file
```

GraphQL manages metadata and authorization.

Object storage handles large binary transfer.

Possible storage:

- S3
- MinIO
- GCS
- Azure Blob
- equivalent object storage

---

# 46. Background jobs

GraphQL should not necessarily execute every expensive operation synchronously.

Example:

```graphql
mutation GenerateReport($input: ReportInput!) {
  generateReport(input: $input) {
    job {
      id
      status
    }
  }
}
```

Flow:

```text
GraphQL
  │
  ▼
create job
  │
  ▼
Kafka / queue
  │
  ▼
worker
  │
  ▼
generate report
  │
  ▼
store result
```

Client can then query:

```graphql
query {
  job(id: "123") {
    status
    resultUrl
  }
}
```

or subscribe to job events.

---

# 47. Search engines

GraphQL can expose search:

```graphql
query Search($query: String!) {
  search(query: $query) {
    total
    results {
      id
      title
      score
    }
  }
}
```

Resolver:

```text
GraphQL
   │
   ▼
SearchService
   │
   ▼
OpenSearch / Elasticsearch
```

GraphQL should expose a stable domain-level search contract rather than leaking every search-engine-specific option.

---

# 48. Object storage

A common architecture:

```text
GraphQL
  │
  ├── metadata -> PostgreSQL
  │
  └── presigned URL -> object storage
```

For a document:

```text
Document
 ├── id
 ├── name
 ├── owner
 ├── contentType
 ├── objectKey
 └── size
```

GraphQL exposes metadata.

Object storage owns bytes.

---

# 49. GraphQL with PostgreSQL

PostgreSQL is an excellent transactional backing store.

Example:

```text
GraphQL
   │
   ▼
Service
   │
   ▼
Repository
   │
   ▼
PostgreSQL
```

Avoid putting SQL directly into every resolver.

Use repositories or data-access modules.

Example:

```text
UserResolver
    ↓
UserService
    ↓
UserRepository
    ↓
PostgreSQL
```

This also makes testing easier.

---

# 50. GraphQL with MongoDB

The same API can sit above MongoDB:

```text
GraphQL
   │
   ▼
UserService
   │
   ▼
MongoDB
```

GraphQL schema remains a domain contract.

Do not expose your database schema one-to-one just because it is convenient.

Database models and API models are allowed to differ.

---

# 51. GraphQL with gRPC

Internal services may use gRPC while clients use GraphQL.

Architecture:

```text
Browser
   │
   ▼
GraphQL
   │
   ├── gRPC -> Users
   ├── gRPC -> Orders
   └── gRPC -> Payments
```

This can be useful when:

- internal services need strongly typed RPC
- external clients benefit from GraphQL
- different teams own backend services

GraphQL becomes the client-facing aggregation layer.

---

# 52. GraphQL and event-driven architecture

GraphQL and event-driven architecture solve different problems.

GraphQL:

```text
request -> response
```

Events:

```text
event -> consumers
```

Together:

```text
Mutation
   │
   ▼
Domain change
   │
   ├── response -> GraphQL client
   │
   └── event -> Kafka
                 │
        ┌────────┼────────┐
        ▼        ▼        ▼
     Search   Email   Analytics
```

This is a powerful pattern.

---

# 53. GraphQL gateway patterns

There are several gateway architectures.

## Pattern A: Single monolith

```text
Client
  ↓
GraphQL
  ↓
Application
```

## Pattern B: BFF

```text
Mobile
  ↓
Mobile GraphQL BFF
  ↓
Services
```

```text
Web
  ↓
Web GraphQL BFF
  ↓
Services
```

## Pattern C: Unified gateway

```text
Clients
   ↓
GraphQL gateway
   ↓
Services
```

## Pattern D: Federation

```text
Clients
   ↓
Federated router
   ├── Users subgraph
   ├── Orders subgraph
   └── Billing subgraph
```

Choose the simplest architecture that satisfies the requirement.

---

# 54. Schema organization

Avoid a giant:

```text
schema.graphql
```

with thousands of lines.

Use domain modules:

```text
schema/
  user.graphql
  project.graphql
  order.graphql
  billing.graphql
  notification.graphql
```

Compose them into the application schema.

This maps naturally to a modular monolith.

---

# 55. Naming conventions

Prefer clear domain names.

Good:

```graphql
user
users
createProject
updateProject
deleteProject
```

Avoid strange RPC-style names:

```graphql
doGetUserThing
executeProjectUpdateNow
```

Inputs:

```graphql
input CreateProjectInput {
  name: String!
}
```

Payloads:

```graphql
type CreateProjectPayload {
  project: Project
  errors: [UserError!]!
}
```

---

# 56. Pagination

Never expose unlimited lists.

Bad:

```graphql
users: [User!]!
```

without pagination for a potentially huge dataset.

Better:

```graphql
users(first: 20, after: "..."): UserConnection!
```

---

# 57. Filtering, sorting and searching

Example:

```graphql
projects(
  first: Int
  after: String
  filter: ProjectFilter
  sort: ProjectSort
): ProjectConnection!
```

Keep filters domain-oriented.

Do not expose arbitrary SQL:

```graphql
where: String
```

That creates a security and abstraction disaster.

---

# 58. Relay Cursor Connections

A common pagination pattern:

```graphql
type ProjectConnection {
  edges: [ProjectEdge!]!
  pageInfo: PageInfo!
}

type ProjectEdge {
  cursor: String!
  node: Project!
}

type PageInfo {
  hasNextPage: Boolean!
  endCursor: String
}
```

Query:

```graphql
query {
  projects(first: 20) {
    edges {
      cursor
      node {
        id
        name
      }
    }

    pageInfo {
      hasNextPage
      endCursor
    }
  }
}
```

This is particularly useful for large datasets and Relay-style clients.

---

# 59. Bulk operations

Do not create mutations that accept unlimited objects.

Bad:

```graphql
createUsers(users: [UserInput!]!)
```

with millions of records.

Better:

```graphql
startImport(input: ImportInput!): ImportJob!
```

Then:

```text
GraphQL
   ↓
job
   ↓
worker
   ↓
batch processing
```

---

# 60. Multi-tenancy

If your application is SaaS:

```text
request context
 ├── user_id
 └── tenant_id
```

Every data-access operation should enforce tenant boundaries.

Do not trust:

```graphql
project(id: "project-from-another-tenant")
```

to be safe.

Repository/service logic must enforce:

```text
WHERE tenant_id = currentTenant
```

or an equivalent policy.

---

# 61. RBAC and ABAC

RBAC:

```text
admin
editor
viewer
```

ABAC:

```text
principal
resource
action
context
```

Example:

```text
Can user 123 update project 456?
```

Policy can consider:

```text
tenant
role
project ownership
resource state
time
IP/network
service identity
```

For larger systems, authorization should become a reusable policy layer rather than hundreds of resolver-specific `if` statements.

---

# 62. Service-to-service security

In a microservice architecture:

```text
GraphQL Router
   │
   ├── Users
   ├── Orders
   └── Billing
```

Do not make services trust arbitrary internet requests.

Prefer:

```text
private network
+
mTLS/service identity
+
service authorization
+
short-lived credentials
```

The GraphQL gateway authenticating a user does not mean every internal service should blindly trust every field request.

---

# 63. Secrets

Never put:

```text
database password
API secret
private key
Kafka credential
```

into:

```graphql
context
```

in a way that could leak through logs or responses.

Use a secrets manager or secure environment configuration.

Never return secrets through GraphQL merely because a database model contains them.

---

# 64. Production architecture

A strong general-purpose architecture:

```text
                         Internet
                            │
                            ▼
                         WAF/CDN
                            │
                            ▼
                      Load Balancer
                            │
                  ┌─────────┴─────────┐
                  │                   │
             GraphQL #1          GraphQL #2
                  │                   │
                  └─────────┬─────────┘
                            │
             ┌──────────────┼──────────────┐
             │              │              │
             ▼              ▼              ▼
           Redis        PostgreSQL       Kafka
             │                             │
             │                    ┌────────┼────────┐
             │                    ▼        ▼        ▼
             │                  Worker   Search   Analytics
             │
             ▼
        subscriptions
```

---

# 65. High availability

Avoid:

```text
one GraphQL process
one Redis
one database
```

for serious production systems.

But do not blindly duplicate everything.

A reasonable progression:

### Stage 1

```text
1 GraphQL
1 PostgreSQL
1 Redis
```

### Stage 2

```text
2+ GraphQL
managed PostgreSQL
Redis HA
```

### Stage 3

```text
GraphQL fleet
distributed cache
database HA/read replicas
Kafka cluster
workers
```

Scale the bottleneck.

---

# 66. Scaling

GraphQL servers should ideally be stateless.

Then:

```text
                Load Balancer
                 /    |    \
                /     |     \
              GQL    GQL    GQL
               \      |      /
                \     |     /
                  Redis
                    │
                PostgreSQL
```

Do not store subscription state only in process memory if clients can land on different instances.

Use distributed infrastructure where required.

---

# 67. Failure modes

Plan for:

```text
GraphQL -> Redis unavailable
GraphQL -> PostgreSQL unavailable
GraphQL -> Kafka unavailable
GraphQL -> REST service timeout
GraphQL -> gRPC timeout
GraphQL -> search unavailable
```

Each dependency needs:

- timeout
- retry policy
- circuit breaker where appropriate
- fallback where appropriate
- metrics
- tracing
- safe error

Do not retry everything.

Retries can amplify outages.

---

# 68. Testing

GraphQL testing should operate at several levels.

## Schema tests

Does the schema compile?

## Validation tests

Does invalid input fail?

## Resolver tests

Does resolver behavior work?

## Service tests

Does domain logic work?

## Integration tests

Does GraphQL work with the real database?

## Contract tests

Does the schema remain compatible?

## Security tests

Can a user access another tenant?

---

# 69. Load testing

GraphQL load testing must test **operation shapes**, not just requests per second.

Example:

```text
GetUser
GetFeed
Search
CreateOrder
Dashboard
AdminReport
```

A:

```text
1000 requests/sec
```

benchmark means little if every operation has different cost.

Track:

```text
operation
complexity
depth
latency
database queries
downstream calls
cache hit ratio
```

---

# 70. Schema testing

Before deployment:

```text
new schema
    │
    ▼
composition
    │
    ▼
breaking-change check
    │
    ▼
client operation check
    │
    ▼
deploy
```

For federation:

```text
subgraph schema A
subgraph schema B
        │
        ▼
composition
        │
        ▼
supergraph
```

Do not deploy a breaking schema change blindly.

---

# 71. Security testing

Test:

```text
unauthenticated access
cross-tenant access
IDOR
deep queries
large lists
aliases
fragments
recursive relationships
batching
introspection
persisted query bypass
rate-limit bypass
mutation replay
error leakage
```

Especially test authorization on object access.

---

# 72. Building a GraphQL server from scratch

To understand GraphQL deeply, implement a small version.

The basic engine needs:

```text
1. lexer/parser
2. AST
3. schema
4. validation
5. execution
6. resolver dispatch
7. serialization
```

Conceptual pipeline:

```text
query string
     │
     ▼
lexer
     │
     ▼
parser
     │
     ▼
AST
     │
     ▼
validator
     │
     ▼
executor
     │
     ▼
resolvers
     │
     ▼
result
```

The official JavaScript reference implementation is `graphql-js`.

Source:

https://github.com/graphql/graphql-js

For Go, examples include:

https://github.com/graphql-go/graphql

and:

https://github.com/graph-gophers/graphql-go

---

# 73. Building your own GraphQL platform

If your goal is not merely to use GraphQL but to build your own GraphQL platform, divide it into layers.

## Layer 1: GraphQL core

```text
lexer
parser
AST
schema
validation
execution
```

## Layer 2: HTTP

```text
POST /graphql
GET /graphql
```

## Layer 3: runtime

```text
resolver execution
context
timeouts
concurrency
```

## Layer 4: application

```text
services
repositories
authorization
events
```

## Layer 5: infrastructure

```text
Redis
Kafka
PostgreSQL
OpenTelemetry
```

## Layer 6: gateway

```text
routing
composition
query planning
```

## Layer 7: developer platform

```text
GraphiQL
schema registry
code generation
operation registry
schema checks
documentation
```

---

# 74. A practical Go architecture

If building this in Go:

```text
cmd/
  api/
    main.go

internal/
  graphql/
    schema/
    resolver/
    middleware/
    directives/

  auth/
  users/
  projects/
  billing/
  notifications/

  database/
  redis/
  kafka/

  observability/
```

Dependency direction:

```text
GraphQL
   ↓
Application services
   ↓
Repositories / adapters
   ↓
Infrastructure
```

Avoid:

```text
GraphQL resolver
   ↓
everything
```

---

# 75. A practical TypeScript architecture

Example:

```text
src/
  graphql/
    schema/
    resolvers/
    directives/

  modules/
    users/
      service.ts
      repository.ts
    projects/
      service.ts
      repository.ts

  infrastructure/
    postgres/
    redis/
    kafka/

  auth/
  observability/
```

Again:

```text
resolver
   ↓
service
   ↓
repository
```

---

# 76. Suggested project layout

A scalable project:

```text
project/
├── cmd/
├── internal/
│   ├── graphql/
│   │   ├── schema/
│   │   ├── resolver/
│   │   ├── middleware/
│   │   └── directives/
│   │
│   ├── users/
│   ├── projects/
│   ├── billing/
│   ├── orders/
│   │
│   ├── postgres/
│   ├── redis/
│   ├── kafka/
│   ├── auth/
│   └── observability/
│
├── migrations/
├── schema/
├── tests/
└── docs/
```

---

# 77. Example production schema

```graphql
scalar DateTime
scalar JSON

type User {
  id: ID!
  name: String!
  email: String!
  projects(first: Int = 20, after: String): ProjectConnection!
}

type Project {
  id: ID!
  name: String!
  owner: User!
  status: ProjectStatus!
  createdAt: DateTime!
}

enum ProjectStatus {
  ACTIVE
  PAUSED
  ARCHIVED
}

type ProjectConnection {
  edges: [ProjectEdge!]!
  pageInfo: PageInfo!
}

type ProjectEdge {
  cursor: String!
  node: Project!
}

type PageInfo {
  hasNextPage: Boolean!
  endCursor: String
}

input CreateProjectInput {
  name: String!
}

type UserError {
  code: String!
  message: String!
  field: String
}

type CreateProjectPayload {
  project: Project
  errors: [UserError!]!
}

type Query {
  viewer: User
  user(id: ID!): User
  project(id: ID!): Project
}

type Mutation {
  createProject(
    input: CreateProjectInput!
  ): CreateProjectPayload!
}
```

This schema is already enough to support:

- web
- mobile
- CLI
- admin UI

without creating separate endpoints for every screen.

---

# 78. Example request flow

Client:

```graphql
query Dashboard {
  viewer {
    id
    name

    projects(first: 20) {
      edges {
        node {
          id
          name
          status
        }
      }
    }
  }
}
```

Server:

```text
HTTP
 ↓
auth middleware
 ↓
GraphQL parser
 ↓
validation
 ↓
operation lookup
 ↓
authorization
 ↓
viewer resolver
 ↓
Project DataLoader
 ↓
PostgreSQL
 ↓
response
```

Potential optimization:

```text
viewer
 ↓
Redis
 ↓
cache hit
```

---

# 79. Example Redis architecture

```text
                  GraphQL
                     │
             ┌───────┼────────┐
             │       │        │
          cache   rate limit  pubsub
             │       │        │
             └───────┼────────┘
                     │
                   Redis
```

Possible keys:

```text
user:123
project:456
ratelimit:user:123:minute
operation:sha256:abc
```

Use TTLs deliberately.

Do not turn Redis into an accidental second database unless you intentionally design it that way.

---

# 80. Example Kafka architecture

Mutation:

```text
GraphQL
   │
   ▼
OrderService
   │
   ├── PostgreSQL transaction
   │
   └── outbox
          │
          ▼
        Kafka
          │
    ┌─────┼─────┐
    ▼     ▼     ▼
 Search Email Analytics
```

The outbox pattern is often safer than:

```text
DB commit
   +
Kafka publish
```

because a crash can occur between those two actions.

With an outbox:

```text
DB transaction
 ├── business data
 └── event outbox
```

then a publisher sends outbox events to Kafka.

---

# 81. Example microservice architecture

```text
                         Clients
                            │
                            ▼
                    GraphQL Router
                            │
        ┌───────────────────┼──────────────────┐
        │                   │                  │
        ▼                   ▼                  ▼
   Users Subgraph      Orders Subgraph   Billing Subgraph
        │                   │                  │
        ▼                   ▼                  ▼
    PostgreSQL          PostgreSQL         PostgreSQL
        │                   │                  │
        └───────────────────┼──────────────────┘
                            │
                           Kafka
                            │
              ┌─────────────┼─────────────┐
              ▼             ▼             ▼
           Search         Email        Analytics
```

The client sees one graph.

The backend remains distributed.

---

# 82. A custom GraphQL router design

If you eventually want to build your own router, think of it as several independent systems.

## Schema registry

```text
subgraph schema
       │
       ▼
composition
       │
       ▼
supergraph/API schema
```

## Query planner

Input:

```graphql
query {
  user {
    name
    orders {
      total
    }
  }
}
```

Output conceptually:

```text
1. Fetch User from Users
2. Get user identity
3. Fetch Orders for that user
4. Merge results
```

## Executor

```text
plan
 ↓
parallelizable tasks
 ↓
service requests
 ↓
join
 ↓
response
```

## Policy engine

```text
authentication
authorization
rate limit
complexity
timeouts
```

## Observability

```text
trace
metrics
logs
```

Do not start by implementing all of this.

Build:

```text
single GraphQL server
→ modular server
→ service adapters
→ simple gateway
→ composition
→ federation/query planning
```

incrementally.

---

# 83. GraphQL gateway versus REST gateway

REST gateway:

```text
GET /users/123
GET /orders/456
```

GraphQL gateway:

```graphql
query {
  user(id: "123") {
    name
    orders {
      total
    }
  }
}
```

REST gateways are often simpler for:

- fixed resources
- HTTP caching
- public APIs
- simple integrations

GraphQL gateways are often strong for:

- multiple clients
- nested data
- rapidly changing UI requirements
- aggregating many backends
- typed client contracts

A system can use both.

---

# 84. Common mistakes

## Mistake 1: Treating GraphQL as a database

Wrong:

```text
GraphQL = database
```

Correct:

```text
GraphQL = API layer
```

## Mistake 2: Resolver contains everything

Wrong:

```text
resolver = 800 lines
```

Use application services.

## Mistake 3: No pagination

Never expose unlimited collections.

## Mistake 4: No complexity controls

GraphQL can produce expensive execution trees.

## Mistake 5: Blind introspection exposure

Decide intentionally.

## Mistake 6: No authorization at object level

Authentication is not enough.

## Mistake 7: In-memory subscriptions in a multi-instance system

Use distributed infrastructure.

## Mistake 8: Making everything a microservice

Start modular.

## Mistake 9: Using Kafka for everything

Kafka is not a cache.

## Mistake 10: Using Redis for everything

Redis is not automatically your primary database.

## Mistake 11: Putting secrets in GraphQL

Never.

## Mistake 12: Assuming GraphQL eliminates versioning problems

Schema compatibility still matters.

## Mistake 13: Assuming one request means one backend operation

One GraphQL request can fan out to many dependencies.

## Mistake 14: Logging entire queries with sensitive variables

Redact sensitive information.

---

# 85. What to learn first

A good learning sequence:

## Phase 1 — Core GraphQL

Learn:

```text
schema
types
fields
queries
variables
mutations
fragments
directives
errors
```

## Phase 2 — Server implementation

Learn:

```text
parser
validation
execution
resolvers
context
middleware
```

## Phase 3 — Database

Build:

```text
GraphQL
+
PostgreSQL
```

## Phase 4 — Performance

Add:

```text
DataLoader
Redis
pagination
complexity limits
caching
```

## Phase 5 — Security

Add:

```text
authentication
authorization
rate limiting
trusted operations
introspection policy
timeouts
```

## Phase 6 — Events

Add:

```text
Kafka
workers
outbox
subscriptions
```

## Phase 7 — Distributed systems

Learn:

```text
microservices
service discovery
tracing
federation
query planning
```

## Phase 8 — Platform

Build:

```text
schema registry
operation registry
GraphiQL
documentation
code generation
CI checks
observability
```

---

# 86. Production checklist

## API

- [ ] schema reviewed
- [ ] pagination implemented
- [ ] mutation inputs validated
- [ ] consistent error model
- [ ] operation names required
- [ ] schema descriptions written

## Security

- [ ] TLS
- [ ] authentication
- [ ] authorization
- [ ] tenant isolation
- [ ] rate limits
- [ ] query depth limit
- [ ] query complexity limit
- [ ] maximum page size
- [ ] resolver timeouts
- [ ] introspection policy
- [ ] persisted/trusted operations where appropriate
- [ ] secrets excluded from logs

## Performance

- [ ] DataLoader/batching
- [ ] database indexes
- [ ] Redis where useful
- [ ] cache invalidation strategy
- [ ] operation caching
- [ ] query-plan caching for federated systems
- [ ] CDN strategy where applicable

## Distributed systems

- [ ] service timeouts
- [ ] retry policy
- [ ] circuit breakers where appropriate
- [ ] Kafka durability strategy
- [ ] outbox where required
- [ ] subscription distribution
- [ ] tracing

## Operations

- [ ] metrics
- [ ] logs
- [ ] traces
- [ ] dashboards
- [ ] alerts
- [ ] load tests
- [ ] schema compatibility checks
- [ ] rollback strategy

---

# 87. Reference sources

The following sources were used to construct this handbook. Prefer the official/specification sources when learning the fundamentals.

## Meta / Facebook

### Original GraphQL announcement

Meta Engineering:

https://engineering.fb.com/2015/09/14/core-infra/graphql-a-data-query-language/

Important concepts from this article:

- GraphQL was created for product/client data requirements.
- GraphQL queries mirror their responses.
- GraphQL is hierarchical.
- GraphQL is strongly typed.
- GraphQL is storage agnostic.
- GraphQL is introspective.
- GraphQL supports gradual schema evolution.
- GraphQL can sit above existing backend systems.

### Facebook GraphQL technical talk

https://engineering.fb.com/2016/03/15/core-infra/facebook-boston-tech-talk-graphql/

### Relay Modern

https://engineering.fb.com/2017/04/18/web/relay-modern-simpler-faster-more-extensible/

Important concepts:

- colocated data dependencies
- fragments
- declarative fetching
- static queries
- ahead-of-time optimization
- generated artifacts

### Mobile GraphQL at Meta in 2025

https://engineering.fb.com/2025/03/31/data-infrastructure/mobile-graphql-meta-2025/

Useful for understanding that Meta continues to use GraphQL as a major mobile data-fetching platform.

---

## GraphQL Foundation / Official GraphQL documentation

### Main GraphQL site

https://graphql.org/

### Queries

https://graphql.org/learn/queries/

### Security

https://graphql.org/learn/security/

### Performance

https://graphql.org/learn/performance/

### GraphQL specification

https://spec.graphql.org/

### GraphQL over HTTP

https://graphql.github.io/graphql-over-http/

---

## Reference implementations

### GraphQL.js

https://github.com/graphql/graphql-js

The reference JavaScript implementation.

### graphql-go

https://github.com/graphql-go/graphql

Go implementation.

### graph-gophers/graphql-go

https://github.com/graph-gophers/graphql-go

Go GraphQL server with schema/resolver checking, context, OpenTelemetry support, subscriptions, and performance-oriented execution features.

---

## Apollo

### Federation overview

https://www.apollographql.com/docs/graphos/schema-design/federated-schemas/federation

### Federation subgraph specification

https://www.apollographql.com/docs/graphos/schema-design/federated-schemas/reference/subgraph-spec

### GraphQL security

https://www.apollographql.com/docs/graphos/platform/security/overview

### Subscriptions

https://www.apollographql.com/docs/apollo-server/data/subscriptions

### Federation subscriptions

https://www.apollographql.com/docs/graphos/routing/v3/operations/subscriptions/overview

### Query plan caching

https://www.apollographql.com/docs/graphos/routing/v3/query-planning/caching

### Enterprise reference architecture

https://www.apollographql.com/docs/graphos/resources/architecture

---

## GraphQL Yoga

https://the-guild.dev/graphql/yoga-server/docs/features/subscriptions

Useful for understanding SSE subscriptions and Redis-backed distributed event delivery.

---

# Final architecture principles

If you remember only a few things, remember these:

## 1. GraphQL is an API layer

```text
GraphQL
   ↓
your application
   ↓
your infrastructure
```

## 2. GraphQL does not require a particular database

```text
GraphQL
 ├── PostgreSQL
 ├── Redis
 ├── Kafka
 ├── REST
 ├── gRPC
 ├── MongoDB
 └── anything else
```

## 3. Start with a monolith

```text
GraphQL
   ↓
modular application
   ↓
database
```

Then grow.

## 4. Use Redis for specific infrastructure problems

```text
cache
rate limiting
short-lived state
distributed pub/sub
```

not automatically as the source of truth.

## 5. Use Kafka for asynchronous events

```text
mutation
  ↓
transaction
  ↓
event
  ↓
Kafka
  ↓
workers
```

## 6. Use subscriptions for real-time client updates

They are not a replacement for Kafka.

Kafka is an event backbone.

GraphQL subscriptions are a client-facing delivery mechanism.

## 7. Use federation only when distribution is actually needed

```text
monolith
  ↓
modular monolith
  ↓
services
  ↓
federated graph
```

is a healthy progression.

## 8. Security is layered

```text
TLS
WAF
authentication
authorization
rate limits
trusted operations
complexity limits
depth limits
timeouts
tenant isolation
observability
```

## 9. Meta's biggest architectural lesson is not syntax

The important idea is:

> Let product clients describe the data they need while keeping the backend implementation behind a typed, evolvable contract.

That is why GraphQL can sit above very different backend architectures.

## 10. Build your own platform incrementally

If your goal is to understand GraphQL deeply enough to build your own system:

```text
GraphQL parser
       ↓
schema
       ↓
validation
       ↓
execution
       ↓
resolvers
       ↓
service layer
       ↓
PostgreSQL
       ↓
Redis
       ↓
Kafka
       ↓
subscriptions
       ↓
security
       ↓
observability
       ↓
gateway
       ↓
composition
       ↓
query planning
```

Do not jump directly to the final box.

Build every layer until you understand why it exists.

---

# Recommended learning project

Build one project that evolves through these stages.

## Project: "Platform API"

### Stage 1

```text
Go
GraphQL
PostgreSQL
```

Implement:

```text
User
Project
Task
```

### Stage 2

Add:

```text
DataLoader
pagination
authorization
```

### Stage 3

Add:

```text
Redis
```

for:

```text
cache
rate limiting
```

### Stage 4

Add:

```text
Kafka
```

for:

```text
ProjectCreated
TaskCreated
TaskUpdated
```

### Stage 5

Add:

```text
subscriptions
```

so clients receive:

```text
TaskUpdated
```

in real time.

### Stage 6

Add:

```text
trusted operations
complexity limits
depth limits
introspection policy
```

### Stage 7

Split:

```text
users
projects
tasks
```

into services.

### Stage 8

Introduce a router.

### Stage 9

Implement schema composition.

### Stage 10

Implement a minimal query planner.

At that point you will understand GraphQL not just as:

```graphql
query {
  user {
    name
  }
}
```

but as a complete API execution platform.

---

# One final mental model

The cleanest way to think about the whole ecosystem is:

```text
                         CLIENTS
       ┌────────────┬────────────┬─────────────┐
       │            │            │             │
      Web         iOS         Android         CLI
       │            │            │             │
       └────────────┴──────┬─────┴─────────────┘
                           │
                           ▼
                    ┌─────────────┐
                    │   GraphQL   │
                    │ API / BFF   │
                    └──────┬──────┘
                           │
              ┌────────────┼────────────┐
              │            │            │
              ▼            ▼            ▼
          Auth/Policy    Resolver     Operation
              │            │          Registry
              │            │
              │            ▼
              │       Service Layer
              │            │
       ┌──────┼────────────┼───────────────┐
       │      │            │               │
       ▼      ▼            ▼               ▼
    Redis PostgreSQL     REST            gRPC
       │      │            │               │
       │      │            └──────┬────────┘
       │      │                   │
       │      ▼                   ▼
       │   Transaction       Other systems
       │      │
       │      ▼
       │    Outbox
       │      │
       └──────┼──────────────────────┐
              ▼                      ▼
            Kafka                Workers
              │                      │
       ┌──────┼─────────┐            │
       ▼      ▼         ▼            ▼
    Search  Email   Analytics     Object Store
       │
       ▼
   Subscriptions / client updates
```

GraphQL is the **typed client-facing contract and execution layer**.

Redis, PostgreSQL, Kafka, REST, gRPC, search, object storage, workers and microservices remain independent building blocks underneath it.

That separation is what makes the architecture scalable and understandable.


---

# 88. Additional research: Meta's real GraphQL ecosystem

This section was added after reviewing the Meta engineering material, current GraphQL specifications, Relay documentation, Apollo Router/Federation documentation, OWASP guidance, and the `win3zz/Meta-Owned-IT-Assets` repository.

The goal is not to copy Meta's internal architecture. The goal is to extract reusable engineering principles.

---

## 88.1 The `Meta-Owned-IT-Assets` repository: what it actually teaches

Repository:

https://github.com/win3zz/Meta-Owned-IT-Assets

The repository is a curated security-research list of technology and internet-facing assets associated with Meta. The author explains that the list was assembled using public asset-discovery and internet-measurement sources and explicitly warns researchers to follow Meta's authorization and bug-bounty rules before testing anything.

This distinction matters:

```text
Meta-Owned-IT-Assets
        │
        ├── asset discovery
        ├── technology identification
        ├── security research
        └── attack-surface awareness
```

It is **not**:

```text
Meta GraphQL source architecture
```

and it should not be treated as proof that a particular product is currently part of Meta's production GraphQL stack.

The most useful lesson for a GraphQL engineer is therefore architectural:

> A large API is only one part of an organization's attack surface.

The repository discusses categories such as:

- authorization problems
- IDOR/BOLA-style issues
- CSRF
- XSS
- rate limiting
- business-logic flaws
- OAuth/SSO configuration
- information disclosure
- third-party applications
- externally exposed administrative systems

These categories map directly to the security model of a GraphQL API.

Source:

https://github.com/win3zz/Meta-Owned-IT-Assets

Use this repository for **security learning and attack-surface modeling**, not as an operational target list.

---

# 89. What Meta's GraphQL articles reveal when read together

Reading Meta's articles individually can make GraphQL look like a query-language feature.

Reading them together reveals something much larger.

The evolution is roughly:

```text
GraphQL
   ↓
Relay
   ↓
static operations
   ↓
compiler
   ↓
generated artifacts
   ↓
mobile optimization
   ↓
large-scale client architecture
```

Meta's original GraphQL article describes GraphQL as a strongly typed, hierarchical and introspective API system where clients describe the data they need.

The Relay Modern article then shows how Meta moved complexity out of application runtime and into compilation.

The 2025 Mobile GraphQL article shows that GraphQL remains part of Meta's mobile data-fetching platform.

Sources:

https://engineering.fb.com/2015/09/14/core-infra/graphql-a-data-query-language/

https://engineering.fb.com/2017/04/18/web/relay-modern-simpler-faster-more-extensible/

https://engineering.fb.com/2025/03/31/data-infrastructure/mobile-graphql-meta-2025/

---

# 90. The most important Meta lesson: move work earlier

A major theme in Relay is:

```text
runtime work
        ↓
compile-time work
```

Instead of making the device repeatedly construct and process everything dynamically:

```text
mobile app
   ↓
build query string
   ↓
send query
   ↓
server parses
   ↓
server validates
```

Meta's Relay approach can move significant work to development/build time:

```text
GraphQL fragments
      ↓
Relay compiler
      ↓
optimized query
      ↓
generated artifact
      ↓
small runtime request
```

This produces an important general architecture principle:

> If something can be safely verified or optimized before production runtime, consider moving that work earlier.

Examples:

```text
schema validation
operation validation
TypeScript generation
query extraction
persisted operations
query normalization
query optimization
client artifact generation
```

This principle is useful even if you never use Relay.

---

# 91. GraphQL is a contract compiler ecosystem, not merely an HTTP endpoint

A simplistic GraphQL architecture is:

```text
HTTP
 ↓
GraphQL
 ↓
database
```

A mature architecture is closer to:

```text
                Schema
                  │
       ┌──────────┼───────────┐
       ▼          ▼           ▼
    Compiler   Validation   Documentation
       │          │           │
       ▼          ▼           ▼
  Generated    Trusted      Developer
   Client      Operations      Tools
       │          │
       └────┬─────┘
            ▼
          Runtime
```

The schema becomes the source of truth for:

- client types
- IDE tooling
- validation
- documentation
- persisted operations
- compatibility checks
- query analysis
- authorization metadata
- federation composition

This is one reason GraphQL can become a platform rather than merely an endpoint.

---

# 92. Meta's static-query idea and modern persisted operations

Meta's Relay Modern article explains a key optimization:

If the operation is known ahead of time, the application can send a small identifier rather than repeatedly transmitting the complete GraphQL operation.

Conceptually:

```text
Traditional:

client
  ↓
large query text
  ↓
server


Persisted operation:

client
  ↓
operation ID/hash
  ↓
server
  ↓
trusted operation registry
  ↓
query
```

Apollo's current APQ documentation describes a related mechanism in which clients can send a hash of the query instead of the full query string.

Source:

https://www.apollographql.com/docs/graphos/routing/v3/operations/apq

This is useful for:

- mobile bandwidth
- latency
- operation safelisting
- security
- observability
- predictable server workloads

---

# 93. Trusted documents versus automatic persisted queries

These concepts should not be confused.

## APQ

The client can initially send a hash.

If the server does not have the operation, the client may send the full query so the server can learn/cache it.

Concept:

```text
hash
 ↓
known?
 ├── yes → execute
 └── no  → obtain full operation
```

## Trusted/persisted operations

The server can maintain an approved registry.

Concept:

```text
operation ID
 ↓
allowlist
 ├── found → execute
 └── missing → reject
```

The second model can provide a stronger production security boundary for applications where the server controls the clients.

---

# 94. Security lesson from the Meta asset repository

The repository's security observations are valuable because they reinforce an important principle:

> Strong infrastructure does not eliminate application-layer authorization bugs.

The author specifically discusses categories such as IDOR, authorization flaws, rate limiting and business-logic vulnerabilities.

For GraphQL, that means you should not assume:

```text
JWT valid
```

means:

```text
request authorized
```

Instead:

```text
authentication
      ↓
identity
      ↓
tenant
      ↓
resource
      ↓
action
      ↓
field/data authorization
```

A valid token can still be unauthorized to read or mutate a specific object.

---

# 95. GraphQL-specific IDOR/BOLA model

Suppose:

```graphql
query {
  project(id: "123") {
    name
    billing
  }
}
```

Authentication may succeed.

But authorization must still answer:

```text
Does caller X have permission to read project 123?
```

A dangerous resolver:

```text
project(id)
    ↓
SELECT * FROM projects WHERE id = ?
```

A safer design:

```text
project(id)
    ↓
current tenant
    ↓
authorization policy
    ↓
resource lookup
    ↓
allowed fields
```

For multi-tenant systems:

```sql
SELECT *
FROM projects
WHERE id = ?
  AND tenant_id = ?
```

can provide an important enforcement layer.

But authorization should not depend solely on SQL filtering; business authorization must remain explicit.

---

# 96. Edge authorization and node authorization

OWASP's GraphQL Cheat Sheet highlights a subtle but important problem: authorization must be checked on both relationships/edges and the objects/nodes reached through them.

Example:

```graphql
viewer {
  projects {
    billingAccount {
      secretData
    }
  }
}
```

Checking:

```text
viewer -> projects
```

does not necessarily prove:

```text
viewer -> billingAccount -> secretData
```

is allowed.

Security should therefore follow the actual object graph.

Source:

https://cheatsheetseries.owasp.org/cheatsheets/GraphQL_Cheat_Sheet.html

---

# 97. GraphQL depth is only one part of query cost

GraphQL.org recommends depth limiting as one defense against deeply nested operations.

But depth alone is insufficient.

Example:

```graphql
users(first: 100) {
  orders(first: 100) {
    items(first: 100) {
      product {
        recommendations(first: 100) {
          ...
        }
      }
    }
  }
}
```

Even if depth is moderate, the multiplicative fan-out can be enormous.

Think of query cost as:

```text
cost ≈
  field cost
  × list cardinality
  × nesting/fanout
  × downstream cost
```

Apollo's current demand-control system goes further by estimating operation cost and can apply global and subgraph-specific limits.

Source:

https://www.apollographql.com/docs/graphos/routing/v3/security/demand-control

---

# 98. Security controls should be layered

A mature GraphQL endpoint can have:

```text
                 Internet
                    │
                    ▼
                  WAF
                    │
                    ▼
               TLS / HTTPS
                    │
                    ▼
            Authentication
                    │
                    ▼
             Authorization
                    │
                    ▼
          Operation allowlist
                    │
                    ▼
             Parse limits
                    │
                    ▼
          Query depth limit
                    │
                    ▼
        Query cost / demand control
                    │
                    ▼
              Rate limit
                    │
                    ▼
              Execution
                    │
                    ▼
          Downstream services
```

Apollo's router security documentation follows a similar defense-in-depth philosophy and includes authentication, authorization, persisted operations, request limits, demand control and CSRF/CORS protections.

Source:

https://www.apollographql.com/docs/graphos/routing/v3/security

---

# 99. Introspection is a product decision, not a universal security switch

GraphQL introspection is one of the reasons the ecosystem has such strong developer tooling.

The GraphQL specification explicitly defines introspection.

It enables:

```text
GraphiQL
schema documentation
code generation
IDE autocomplete
client validation
developer tooling
```

Source:

https://spec.graphql.org/September2025/

But an internal administrative graph may not want unrestricted public schema discovery.

OWASP recommends carefully considering introspection and GraphiQL exposure in production.

Apollo also recommends protecting internal federation-specific fields such as `_service` and `_entities` from public access.

Sources:

https://cheatsheetseries.owasp.org/cheatsheets/GraphQL_Cheat_Sheet.html

https://www.apollographql.com/docs/graphos/platform/security/overview

The right policy is therefore:

```text
development:
  introspection = enabled

internal authenticated API:
  introspection = controlled

public developer API:
  introspection = intentional/public

private production graph:
  introspection = restricted
```

---

# 100. Federation adds a new security boundary

In a federated system:

```text
Client
  ↓
Router
  ↓
Subgraph A
Subgraph B
Subgraph C
```

The router is the public entry point.

Apollo recommends that subgraphs should not be directly accessible to arbitrary external clients.

Why?

Because federation adds special machinery.

For example:

```graphql
Query._service
Query._entities
```

exist for federation composition and entity resolution.

Apollo specifically warns that exposing these publicly can disclose schema information or allow clients to bypass intended router-level controls.

Source:

https://www.apollographql.com/docs/graphos/platform/security/overview

Therefore:

```text
Internet
   │
   ▼
Router
   │
   ├── authenticated
   ├── authorized
   ├── rate-limited
   ├── complexity checked
   └── observed
          │
          ▼
      private subgraphs
```

---

# 101. Router security is not enough

Even if:

```text
Router authorization = correct
```

a subgraph should not automatically become completely trusted.

Use defense in depth:

```text
Router
  │
  ├── authentication
  ├── authorization
  ├── demand control
  └── rate limit
       │
       ▼
Subgraph
  │
  ├── service authentication
  ├── resource authorization
  ├── validation
  └── database authorization
```

This is especially important in zero-trust environments.

---

# 102. Federation is an orchestration system

Apollo's federation documentation makes a useful architectural point:

The client sends one GraphQL operation to the router.

The router coordinates multiple APIs and returns a unified response.

Those sources can include:

- GraphQL subgraphs
- REST APIs
- other data sources

Source:

https://www.apollographql.com/docs/graphos/schema-design/federated-schemas/federation

So:

```text
GraphQL
```

does not have to mean:

```text
every service must speak GraphQL
```

A gateway can normalize heterogeneous backend systems.

---

# 103. A practical heterogeneous backend

A realistic architecture can be:

```text
                         Client
                           │
                           ▼
                    GraphQL Router
                           │
        ┌──────────────────┼───────────────────┐
        │                  │                   │
        ▼                  ▼                   ▼
   GraphQL service      REST API           gRPC service
        │                  │                   │
        ▼                  ▼                   ▼
   PostgreSQL          Legacy ERP          Payment system
```

Then:

```text
Redis
Kafka
OpenSearch
Object storage
```

can sit behind those services.

GraphQL becomes a consistent client contract over an inconsistent backend world.

That is one of the strongest reasons to use it.

---

# 104. Redis in modern GraphQL routers

Current Apollo Router documentation provides concrete examples of Redis being used for more than ordinary application caching.

Redis can support:

```text
APQ distributed cache
query-plan cache
response cache
```

Apollo documents distributed APQ caching where multiple router instances share a Redis-backed cache.

Source:

https://www.apollographql.com/docs/graphos/routing/v3/operations/apq

Apollo also documents Redis-backed response caching for subgraph and connector responses.

Source:

https://www.apollographql.com/docs/graphos/routing/v3/performance/caching/response-caching/overview

This gives a useful architecture:

```text
                Load Balancer
                /     |     \
               /      |      \
          Router 1  Router 2  Router 3
               \      |      /
                \     |     /
                  Redis
                    │
        ┌───────────┼────────────┐
        ▼           ▼            ▼
       APQ       Query plans   Response cache
```

---

# 105. GraphQL caching is not the same as HTTP caching

GraphQL responses are often composed from different sources.

For example:

```graphql
product {
  name
  price
  inventory
  reviews
  viewerCartStatus
}
```

These fields can have completely different:

```text
TTL
privacy
authorization
source
freshness
```

A five-minute cache may be fine for:

```text
product.name
```

but dangerous for:

```text
inventory
viewerCartStatus
```

Apollo's response-cache documentation explicitly discusses mixed TTLs, personalized data, entity-level caching and authorization-aware caching.

Source:

https://www.apollographql.com/docs/graphos/routing/v3/performance/caching/response-caching/overview

---

# 106. Multi-tenant cache safety

A major danger:

```text
tenant A
  ↓
cache key
  ↓
tenant B receives A's data
```

Never allow a shared cache key to ignore authorization context when the underlying data is private.

Possible key dimensions:

```text
operation
variables
tenant
user
authorization context
locale
feature flags
```

Apollo's current response-cache documentation explicitly supports private data caching and custom cache keys for contexts such as tenant IDs and locale.

Source:

https://www.apollographql.com/docs/graphos/routing/v3/performance/caching/response-caching/customization

---

# 107. Kafka should not be confused with GraphQL subscriptions

This is a very important architectural distinction.

Kafka:

```text
durable event stream
```

GraphQL subscription:

```text
client-facing live data delivery
```

A good architecture:

```text
                    Kafka
                      │
                      ▼
                 Event consumer
                      │
              ┌───────┴───────┐
              ▼               ▼
           Redis           GraphQL
              │               │
              └───────┬───────┘
                      ▼
                    Client
```

Kafka may be the source of events.

GraphQL subscription is how a particular client consumes a useful projection of those events.

---

# 108. Subscription architecture at scale

Do not build:

```text
GraphQL server 1
  ↓
in-memory events
```

when you have:

```text
GraphQL server 1
GraphQL server 2
GraphQL server 3
```

Instead:

```text
Event source
    │
    ▼
Redis/Kafka/event broker
    │
 ┌──┼────────┐
 ▼  ▼        ▼
GQL GQL      GQL
 │   │        │
 └───┴────────┘
      │
      ▼
    Clients
```

Apollo documents external PubSub infrastructure for distributed subscription systems and current router subscription mechanisms.

Sources:

https://www.apollographql.com/docs/apollo-server/data/subscriptions

https://www.apollographql.com/docs/graphos/routing/v3/operations/subscriptions/overview

---

# 109. HTTP subscriptions are evolving

A useful current development is that GraphQL subscriptions do not necessarily mean:

```text
WebSocket client
```

Apollo Router's current documentation describes multipart HTTP for client-facing subscriptions and WebSocket or callback mechanisms between router and subgraph depending on configuration.

Source:

https://www.apollographql.com/docs/graphos/routing/v3/operations/subscriptions/overview

Apollo also documents an HTTP callback protocol designed for router/subgraph subscription delivery.

Source:

https://www.apollographql.com/docs/graphos/routing/v3/operations/subscriptions/callback-protocol

This means your own GraphQL platform should keep:

```text
GraphQL subscription semantics
```

separate from:

```text
transport implementation
```

---

# 110. Query planning becomes necessary when the graph is distributed

For a monolith:

```text
query
 ↓
resolver
```

For federation:

```text
query
 ↓
parse
 ↓
validate
 ↓
compose/query plan
 ↓
fetch service A
 ↓
use returned entity keys
 ↓
fetch service B
 ↓
merge
 ↓
response
```

Example:

```graphql
query {
  user(id: "1") {
    name
    orders {
      total
    }
  }
}
```

Possible plan:

```text
Step 1:
Users
  GET user 1
  return:
    id
    name

Step 2:
Orders
  using user.id
  GET orders for user 1

Step 3:
merge
```

The router is therefore not merely a reverse proxy.

It is an execution planner.

---

# 111. Query-plan caching

If the same operation occurs repeatedly:

```text
query text
    ↓
parse
    ↓
validate
    ↓
plan
```

can be expensive.

A router can cache:

```text
operation signature
      ↓
query plan
```

Apollo documents both in-memory and Redis-backed distributed query-plan caching.

Source:

https://www.apollographql.com/docs/graphos/routing/query-planning/caching

This is another example of moving expensive work away from the hot path.

---

# 112. Query batching needs careful security controls

GraphQL can support sending multiple operations in a single HTTP request.

That can be useful:

```text
network request
   ↓
operation A
operation B
operation C
```

But batching can also amplify brute-force or denial-of-service behavior.

OWASP specifically calls out batching attacks.

Source:

https://cheatsheetseries.owasp.org/cheatsheets/GraphQL_Cheat_Sheet.html

Therefore define:

```text
max operations per request
max total complexity
max total cost
rate limit
authorization
```

---

# 113. Meta's Relay design and cache normalization

Relay's current documentation emphasizes normalized client state.

The basic idea:

```text
User:123
```

is a canonical entity.

If one query updates:

```text
User:123.name
```

other components referencing the same entity can observe the update.

Relay also uses global object identification and connections as core patterns.

Source:

https://relay.dev/

This is not merely a client convenience.

It changes how you design your GraphQL schema.

---

# 114. Global object identification

Relay recommends globally unique object IDs.

Example:

```graphql
interface Node {
  id: ID!
}
```

Then:

```graphql
type User implements Node {
  id: ID!
  name: String!
}
```

A client can reason about:

```text
User:123
Project:456
Order:789
```

without requiring every query to invent a separate identity scheme.

Relay's documentation describes global object identification as important for reliable caching and refetching.

Source:

https://relay.dev/

---

# 115. Connections are more than pagination

Relay's connection model gives you:

```text
edges
nodes
cursor
pageInfo
```

This provides room for relationship metadata.

Example:

```graphql
type ProjectMemberEdge {
  cursor: String!
  node: User!
  role: ProjectRole!
  joinedAt: DateTime!
}
```

Now the relationship itself has data.

This is much better than:

```graphql
members: [User!]!
```

when the relationship contains business meaning.

---

# 116. Meta's architecture points toward compiler-assisted APIs

If you are designing your own GraphQL platform, consider building:

```text
Schema
  ↓
Operation compiler
  ↓
Static analysis
  ↓
Generated client artifacts
  ↓
Runtime
```

Possible compiler checks:

```text
unknown field
wrong argument
wrong variable type
deprecated field
missing required field
fragment mismatch
authorization metadata
query complexity
operation naming
```

Then CI can reject bad operations before deployment.

---

# 117. Your own GraphQL platform: recommended architecture

If you want to build your own system instead of adopting Apollo wholesale, use this staged architecture.

## Version 0

```text
GraphQL parser
GraphQL schema
GraphQL validator
GraphQL executor
HTTP
```

## Version 1

```text
PostgreSQL
DataLoader
auth
pagination
```

## Version 2

```text
Redis
rate limits
operation cache
persisted operations
```

## Version 3

```text
Kafka
events
workers
subscriptions
```

## Version 4

```text
operation compiler
generated clients
schema registry
compatibility checks
```

## Version 5

```text
service registry
schema composition
router
query planner
```

## Version 6

```text
distributed tracing
demand control
advanced caching
traffic shaping
multi-tenant policy
```

This gives you a serious GraphQL platform without attempting to clone Apollo on day one.

---

# 118. Recommended architecture for your own project

For a normal project:

```text
                    Web / Mobile / CLI
                           │
                           ▼
                     GraphQL Server
                           │
                    ┌──────┴──────┐
                    │             │
              Auth/Policy       GraphQL
                    │             │
                    └──────┬──────┘
                           │
                      Service layer
                           │
              ┌────────────┼────────────┐
              │            │            │
          PostgreSQL      Redis        Kafka
              │                         │
              │                    background
              │                      workers
              │                         │
              └────────────┬────────────┘
                           ▼
                     domain state
```

Do this before federation.

---

# 119. Recommended architecture for a large platform

When services genuinely become independent:

```text
                         Clients
                            │
                            ▼
                     GraphQL Router
                            │
         ┌──────────────────┼───────────────────┐
         │                  │                   │
         ▼                  ▼                   ▼
       Users              Projects            Billing
      Subgraph            Subgraph            Subgraph
         │                  │                   │
         ▼                  ▼                   ▼
     PostgreSQL          PostgreSQL          PostgreSQL
         │                  │                   │
         └──────────────────┼───────────────────┘
                            ▼
                           Kafka
                            │
                  ┌─────────┼─────────┐
                  ▼         ▼         ▼
                Search    Email     Analytics
```

Use:

```text
Redis
```

for carefully chosen distributed/cache workloads.

Use:

```text
Kafka
```

for event streaming.

Use:

```text
GraphQL Router
```

for client-facing orchestration.

---

# 120. Security architecture for your own GraphQL platform

Recommended:

```text
                    Internet
                       │
                       ▼
                    WAF/CDN
                       │
                       ▼
                  API Gateway
                       │
                       ▼
                 Authentication
                       │
                       ▼
                  GraphQL Router
                       │
       ┌───────────────┼────────────────┐
       │               │                │
       ▼               ▼                ▼
  Safelist         Demand Control   Rate Limit
       │               │                │
       └───────────────┼────────────────┘
                       ▼
                 Authorization
                       │
                       ▼
                 Query execution
                       │
              ┌────────┼────────┐
              ▼        ▼        ▼
           Redis      DB      services
                       │
                       ▼
                    Kafka
```

Every layer has a purpose.

---

# 121. What the Meta asset research adds to your security model

The asset repository should change how you think about GraphQL security in one major way:

Do not model security as:

```text
GraphQL endpoint
```

Model it as:

```text
organization
 │
 ├── public applications
 ├── API gateways
 ├── GraphQL
 ├── REST
 ├── third-party SaaS
 ├── identity systems
 ├── support systems
 ├── internal applications
 ├── CI/CD
 ├── DNS
 ├── cloud infrastructure
 └── developer tooling
```

A vulnerability in a third-party system can become relevant to the overall security posture even if GraphQL itself is perfectly implemented.

This is why enterprise security is broader than API syntax.

---

# 122. GraphQL attack-surface model

For your own system, maintain an inventory like:

```text
API
 ├── GraphQL endpoint
 ├── REST endpoints
 ├── WebSocket/SSE
 └── webhooks

Identity
 ├── OAuth
 ├── OIDC
 ├── JWT
 └── service credentials

Data
 ├── PostgreSQL
 ├── Redis
 ├── object storage
 └── search

Messaging
 ├── Kafka
 └── workers

Infrastructure
 ├── router
 ├── load balancer
 ├── WAF
 ├── DNS
 └── observability

Third party
 ├── payments
 ├── email
 ├── analytics
 └── SaaS
```

Then ask for each:

```text
Who can access it?
What can they do?
What data crosses the boundary?
What happens when it fails?
What is logged?
What is cached?
What is exposed publicly?
```

---

# 123. Do not turn reconnaissance into production architecture

The `Meta-Owned-IT-Assets` repository is useful for understanding the breadth of a real organization's exposed technology surface.

But your own architecture should be built from:

```text
requirements
threat model
data flows
trust boundaries
performance requirements
availability requirements
compliance requirements
```

not from:

```text
"What technologies does Meta expose?"
```

Meta's infrastructure has vastly different scale and constraints from a small product.

The reusable lesson is the design principle, not the exact stack.

---

# 124. Official reading map

For serious GraphQL learning, use these sources in this order.

## Level 1 — Specification

Read:

https://spec.graphql.org/September2025/

Learn:

```text
language
types
validation
execution
introspection
```

## Level 2 — GraphQL.org

Read:

https://graphql.org/

Then:

https://graphql.org/learn/security/

https://graphql.org/learn/performance/

Learn:

```text
API design
security
performance
pagination
```

## Level 3 — Meta

Read:

https://engineering.fb.com/2015/09/14/core-infra/graphql-a-data-query-language/

Then:

https://engineering.fb.com/2017/04/18/web/relay-modern-simpler-faster-more-extensible/

Then:

https://engineering.fb.com/2025/03/31/data-infrastructure/mobile-graphql-meta-2025/

Learn:

```text
why GraphQL exists
how Relay shaped its use
static operations
compiler architecture
mobile optimization
large-scale client data fetching
```

## Level 4 — Relay

Read:

https://relay.dev/

Learn:

```text
fragments
connections
global IDs
normalized cache
compiler
optimistic mutations
incremental data
```

## Level 5 — OWASP

Read:

https://cheatsheetseries.owasp.org/cheatsheets/GraphQL_Cheat_Sheet.html

Learn:

```text
IDOR/BOLA
authorization
DoS
batching
introspection
error leakage
input validation
```

## Level 6 — Apollo Federation

Read:

https://www.apollographql.com/docs/graphos/schema-design/federated-schemas/federation

Then:

https://www.apollographql.com/docs/graphos/routing/v3/security

Learn:

```text
router
subgraphs
composition
query planning
security
demand control
persisted operations
```

## Level 7 — Apollo performance

Read:

https://www.apollographql.com/docs/graphos/routing/v3/performance

Learn:

```text
Redis
response caching
query plan caching
APQ
traffic shaping
batching
timeouts
```

## Level 8 — Meta security research context

Read:

https://github.com/win3zz/Meta-Owned-IT-Assets

Use it to think about:

```text
asset inventory
third-party software
attack surface
authorization flaws
business logic
information disclosure
security boundaries
```

Do not use the repository's listed assets as targets unless you have explicit authorization.

---

# 125. Updated master mental model

After combining the Meta, GraphQL Foundation, Relay, OWASP and Apollo material, the cleanest model is:

```text
                         PRODUCT CLIENTS
          ┌───────────────┬───────────────┐
          │               │               │
         Web            Mobile           CLI
          │               │               │
          └───────────────┼───────────────┘
                          ▼
                  ┌────────────────┐
                  │ GraphQL Client │
                  │ / Relay / SDK  │
                  └───────┬────────┘
                          │
                    HTTPS / HTTP
                          │
                          ▼
               ┌──────────────────────┐
               │ WAF / Load Balancer  │
               └──────────┬───────────┘
                          ▼
               ┌──────────────────────┐
               │ GraphQL Router/API   │
               ├──────────────────────┤
               │ Auth                 │
               │ Authorization        │
               │ Safelist/APQ         │
               │ Rate limits          │
               │ Depth/cost           │
               │ Validation           │
               │ Observability        │
               └──────────┬───────────┘
                          │
                ┌─────────┴─────────┐
                │                   │
                ▼                   ▼
          Monolithic app       Federation router
                │                   │
                │          ┌────────┼─────────┐
                │          ▼        ▼         ▼
                │       Users    Orders    Billing
                │       service  service   service
                │          │        │         │
                └──────────┼────────┼─────────┘
                           │
                 ┌─────────┼─────────┐
                 ▼         ▼         ▼
              PostgreSQL Redis     REST/gRPC
                 │         │         │
                 │         │         │
                 └────┬────┴─────────┘
                      ▼
                    Kafka
                      │
             ┌────────┼─────────┐
             ▼        ▼         ▼
          Workers   Search   Analytics
             │
             ▼
        Object storage

```

The major lesson is:

```text
GraphQL
    =
typed client-facing contract
+
query validation
+
execution
+
composition/orchestration when needed
```

It does **not** mean:

```text
GraphQL = database
GraphQL = Redis
GraphQL = Kafka
GraphQL = microservices
GraphQL = Apollo
GraphQL = REST replacement
```

Those are separate architectural decisions.

---

# 126. Final recommendation for your learning project

For your own implementation, I would deliberately build this:

```text
                    Your GraphQL Platform
                           │
        ┌──────────────────┼──────────────────┐
        ▼                  ▼                  ▼
      Schema            Compiler           Docs
        │                  │                  │
        ▼                  ▼                  ▼
    Validation       Generated SDK       GraphiQL
        │
        ▼
     Executor
        │
        ▼
    Resolvers
        │
        ▼
   Service layer
        │
 ┌──────┼───────────┐
 ▼      ▼           ▼
SQL   Redis        Kafka
 │      │           │
 ▼      ▼           ▼
DB    cache       workers
                   │
                   ▼
               subscriptions
```

Then, only after this works:

```text
single server
     ↓
modular monolith
     ↓
multiple services
     ↓
schema composition
     ↓
router
     ↓
query planner
     ↓
federated graph
```

That sequence teaches the underlying GraphQL mechanics rather than teaching you only how to configure somebody else's router.

---

# 127. Research conclusion

The combined evidence from Meta's engineering publications, the GraphQL specification, Relay's current documentation, OWASP's security guidance, Apollo's current router/federation documentation, and the Meta asset/security-research repository points to a consistent architecture:

**GraphQL works best as a typed boundary between product clients and a heterogeneous backend system.**

At small scale:

```text
GraphQL → application → PostgreSQL
```

At medium scale:

```text
GraphQL → modular application → PostgreSQL + Redis + Kafka
```

At large scale:

```text
Clients
  ↓
GraphQL Router
  ↓
federated services
  ↓
databases / caches / events / external APIs
```

And at every scale:

```text
authentication
authorization
validation
resource limits
observability
schema governance
```

remain first-class.

Meta's work adds another important lesson:

**push predictable work toward compile time, make data requirements explicit, and keep runtime behavior efficient and observable.**

The security research adds another:

**protect the entire system boundary, not only the GraphQL endpoint.**

That combination is a much stronger foundation for designing your own GraphQL platform than simply copying an Apollo configuration.



---

# 128. GraphQL Resource Library — Official Sites, References, Guides, Tools, and Further Learning

This section is the **reference shelf for the entire handbook**. Use it as a living map rather than trying to read every resource in order.

The links are grouped by authority and purpose:

1. GraphQL specification and official ecosystem
2. Official learning and tutorials
3. Meta / Relay engineering
4. Apollo and federation
5. Security
6. Server implementations
7. Client implementations
8. IDEs and developer tooling
9. Schema governance and compatibility
10. Data sources, gateways, and integration tools
11. Real-time / subscriptions
12. Observability and production operations
13. Books, courses, talks, and community resources
14. Source code and standards for serious implementers
15. Recommended reading order

> **Rule:** Prefer the official specification and project documentation when determining what GraphQL *is*. Use framework/vendor documentation to learn how a particular implementation behaves. Do not treat one vendor's implementation as the GraphQL standard.

---

## 129. The GraphQL Specification — Start Here for the Actual Standard

### 129.1 GraphQL.org

**Official GraphQL website**

- https://graphql.org/
- https://graphql.org/learn/
- https://graphql.org/resources/
- https://graphql.org/code/
- https://graphql.org/community/

The official site is the best starting point for learning the ecosystem, discovering implementations, reading best practices, and finding community resources.

The official Learn section now includes fundamentals as well as schema governance and schema-change-management material. citeturn0search1turn0search5

### 129.2 GraphQL Specification

**Official specification**

- https://spec.graphql.org/
- https://spec.graphql.org/draft/

Read this when you want to understand the actual language and execution model rather than a framework abstraction.

Important areas:

- Lexical grammar
- Language
- Types
- Type system
- Validation
- Execution
- Introspection
- Response format
- Directives
- Variables
- Fragments
- Interfaces
- Unions
- Input objects
- Mutations
- Subscription semantics

The official GraphQL FAQ states that the latest working draft is available at `spec.graphql.org/draft`, while released editions have stable permalink URLs. citeturn0search9

### 129.3 GraphQL Specification Repository

- https://github.com/graphql/graphql-spec

Use this to understand:

- specification development
- proposals
- working-group discussions
- changes between editions
- GraphQL Auxiliary Proposals
- implementation implications

This is particularly useful once you are interested in building your own GraphQL implementation.

### 129.4 GraphQL.js — Reference Implementation

- https://github.com/graphql/graphql-js
- https://graphql.org/graphql-js/

GraphQL.js is the reference JavaScript implementation.

It demonstrates the two fundamental server-side responsibilities:

```text
Schema definition
       +
Query execution
```

The project itself recommends studying its tests alongside the specification. citeturn0search0turn0search20

For someone building a GraphQL engine, reading GraphQL.js alongside the specification is one of the most useful implementation exercises.

---

# 130. Official GraphQL Learning Path

## 130.1 GraphQL Learn

**Primary beginner → intermediate resource**

- https://graphql.org/learn/

Recommended sequence:

```text
Introduction
   ↓
Schemas & Types
   ↓
Queries
   ↓
Mutations
   ↓
Validation
   ↓
Execution
   ↓
Introspection
   ↓
Best Practices
   ↓
Schema Governance
```

The official learning site explicitly covers fundamentals, best practices, schema governance, review, and schema change management. citeturn0search1

## 130.2 GraphQL Tutorials

- https://graphql.org/learn/
- https://graphql.org/resources/

The official resources hub links to:

- GraphQL.js tutorials
- Apollo Odyssey
- Yoga tutorials
- Hasura tutorials
- videos
- books
- community material
- GraphQL conferences and talks

citeturn0search5

## 130.3 GraphQL FAQ

- https://graphql.org/faq/

Useful for questions such as:

- Is GraphQL tied to a database?
- Is GraphQL only for React?
- How does GraphQL interact with databases?
- How should resolvers be structured?
- How does GraphQL differ from REST?
- How does the specification evolve?

The official FAQ explicitly describes resolvers as normally delegating to a business/data-access layer that can communicate with APIs, databases, caches, and other sources. citeturn0search14

---

# 131. Meta Engineering and Relay

Meta is particularly important for understanding **why GraphQL became a platform rather than merely a query syntax**.

## 131.1 Meta Engineering

- https://engineering.fb.com/

Search/read:

- GraphQL
- Relay
- mobile GraphQL
- Facebook.com rebuild
- data fetching
- compiler architecture

Important articles already discussed in this handbook include:

### GraphQL: A data query language

https://engineering.fb.com/2015/09/14/core-infra/graphql-a-data-query-language/

Study this for:

- why GraphQL was created
- typed API contracts
- hierarchical data requirements
- introspection
- mobile data fetching
- GraphiQL
- GraphQL.js

### Relay Modern

https://engineering.fb.com/2017/04/07/web/relay-modern-simpler-faster-more-extensible/

Study this for:

- fragments
- colocated data requirements
- compiler architecture
- static/persisted operations
- normalized client state
- ahead-of-time optimization
- runtime/compiler separation

### Mobile GraphQL at Meta

https://engineering.fb.com/

Search for:

**Mobile GraphQL at Meta in 2025**

Use this to understand how GraphQL evolved into a large-scale mobile data platform.

---

# 132. Relay — Deep Client Architecture

## Official Relay

- https://relay.dev/
- https://relay.dev/docs/
- https://github.com/facebook/relay

Relay is especially valuable if you want to understand:

```text
GraphQL schema
      ↓
Fragments
      ↓
Compiler
      ↓
Generated operations
      ↓
Normalized client store
      ↓
UI
```

Study:

- fragments
- connections
- pagination
- refetchable fragments
- mutations
- optimistic updates
- garbage collection
- compiler
- generated artifacts
- persisted operations
- streaming/defer

Relay is useful even if you never use React, because its architecture demonstrates how a GraphQL client can move work from runtime to build time.

---

# 133. Apollo GraphQL

Apollo is one of the most important practical references for production GraphQL architecture.

## 133.1 Apollo Documentation

- https://www.apollographql.com/docs

The current documentation covers:

- GraphQL servers
- clients
- federation
- routers
- schema design
- security
- caching
- observability
- performance
- subscriptions
- connectors
- persisted operations
- query planning

citeturn0search19

## 133.2 Apollo Federation

- https://www.apollographql.com/docs/graphos/schema-design/federated-schemas/federation

Study this carefully if you want:

```text
multiple services
       ↓
multiple GraphQL subgraphs
       ↓
federated schema
       ↓
router
       ↓
one client-facing GraphQL API
```

Apollo describes federation as an orchestration layer that combines multiple APIs into a unified GraphQL API. The underlying APIs can include GraphQL and other data sources. citeturn0search4

## 133.3 Apollo Router

- https://www.apollographql.com/docs/graphos/routing/

Study:

- routing
- query planning
- subgraph communication
- authentication
- authorization
- persisted operations
- demand control
- traffic shaping
- caching
- telemetry
- deployment

**Important version note:** Apollo's Router 3 documentation is currently marked as preview. Production users should distinguish it from the current production Router documentation. citeturn0search11

## 133.4 Apollo Security

- https://www.apollographql.com/docs/graphos/platform/security/
- https://www.apollographql.com/docs/graphos/routing/security/

Important subjects:

- authentication
- authorization
- CORS
- CSRF
- request limits
- demand control
- persisted queries
- safelisting
- subgraph authentication
- schema discoverability
- router/subgraph isolation

Apollo's security guidance emphasizes defense in depth rather than assuming that one gateway check is sufficient. citeturn0search7turn0search10

## 133.5 Apollo Performance

- https://www.apollographql.com/docs/graphos/routing/performance/

Study:

- response caching
- Redis-backed caching
- query planning
- APQ
- batching
- traffic shaping
- concurrency
- latency
- distributed router deployments

Apollo's current router documentation describes Redis-backed distributed response caching and authorization-aware cache separation. citeturn0search8

---

# 134. OWASP — GraphQL Security

## GraphQL Cheat Sheet

**Official OWASP resource**

- https://cheatsheetseries.owasp.org/cheatsheets/GraphQL_Cheat_Sheet.html

This should be treated as required reading before exposing a serious GraphQL API publicly.

Topics include:

- input validation
- access control
- authorization
- expensive queries
- DoS
- introspection
- GraphiQL
- error handling
- insecure defaults
- batching attacks
- rate limiting
- security monitoring

OWASP specifically recommends controlling expensive operations and enforcing proper access control. citeturn0search13

## OWASP API Security

Also study the broader OWASP API Security material:

- https://owasp.org/API-Security/

GraphQL does not eliminate normal API security problems.

You still need to defend:

```text
Authentication
Authorization
BOLA / IDOR
BFLA
Injection
CSRF
SSRF
Rate abuse
Data leakage
Business-logic abuse
Resource exhaustion
```

GraphQL adds another layer:

```text
Query complexity
Query depth
Field amplification
Alias abuse
Batching abuse
Introspection exposure
Resolver fan-out
Federation abuse
```

---

# 135. GraphQL Server Implementations

GraphQL is a specification. Pick an implementation appropriate for your language and architecture.

## JavaScript / TypeScript

### GraphQL.js

- https://github.com/graphql/graphql-js

Best for understanding the reference implementation.

### Apollo Server

- https://www.apollographql.com/docs/apollo-server/

Good for:

- Node.js
- TypeScript
- production GraphQL APIs
- Apollo ecosystem

### GraphQL Yoga

- https://the-guild.dev/graphql/yoga-server

Useful for:

- modern GraphQL servers
- Node
- serverless
- edge runtimes
- flexible integrations

### GraphQL Helix

- https://github.com/contrawork/graphql-helix

Useful as a lower-level HTTP-oriented GraphQL server toolkit.

---

# 136. Go GraphQL

Since this handbook is also intended to support building serious infrastructure in Go, study:

## gqlgen

- https://gqlgen.com/
- https://github.com/99designs/gqlgen

gqlgen is one of the major Go GraphQL implementations.

Particularly useful topics:

```text
Schema-first development
Resolvers
Generated code
Context propagation
Middleware
DataLoader
Subscriptions
Directives
Testing
Complexity limits
```

A practical Go stack for this handbook can therefore be:

```text
Go
 ↓
gqlgen
 ↓
PostgreSQL
 ↓
DataLoader
 ↓
Redis
 ↓
Kafka
 ↓
OpenTelemetry
```

---

# 137. Java GraphQL

## GraphQL Java

- https://www.graphql-java.com/
- https://github.com/graphql-java/graphql-java

Useful for understanding:

- execution
- instrumentation
- data fetching
- Java server integration
- query complexity
- asynchronous execution

GraphQL Java is particularly useful for understanding how a GraphQL execution engine integrates with an enterprise JVM application.

---

# 138. Python GraphQL

Important implementations include:

### Graphene

- https://graphene-python.org/
- https://github.com/graphql-python/graphene

### Strawberry

- https://strawberry.rocks/
- https://github.com/strawberry-graphql/strawberry

When choosing Python tooling, compare:

```text
Schema-first
vs
Code-first
vs
Type-hint-driven
```

Do not assume that the framework's preferred schema-definition style is a property of GraphQL itself.

---

# 139. .NET / C#

## Hot Chocolate

- https://chillicream.com/docs/hotchocolate/
- https://github.com/ChilliCream/graphql-platform

Important areas:

- schema stitching
- federation
- projections
- filtering
- sorting
- authorization
- subscriptions
- DataLoader

---

# 140. Rust GraphQL

## async-graphql

- https://async-graphql.github.io/async-graphql/en/introduction.html
- https://github.com/async-graphql/async-graphql

Useful if you are interested in:

- Rust
- async execution
- strongly typed implementations
- performance-oriented servers

---

# 141. GraphQL Clients

GraphQL is not just a server technology.

## Apollo Client

- https://www.apollographql.com/docs/react/
- https://www.apollographql.com/docs/ios/
- https://www.apollographql.com/docs/kotlin/

Study:

- normalized caching
- cache policies
- optimistic updates
- pagination
- mutations
- subscriptions
- generated types

## Relay

- https://relay.dev/

Study this when you want a compiler-oriented GraphQL client.

## urql

- https://commerce.nearform.com/open-source/urql/
- https://github.com/urql-graphql/urql

Useful for lightweight React/web GraphQL applications.

## GraphQL Request / lightweight clients

Search the GraphQL ecosystem directory for language-specific clients rather than assuming one client fits every application.

Official ecosystem directory:

- https://graphql.org/code/

---

# 142. GraphiQL — The GraphQL IDE

## Official GraphiQL

- https://github.com/graphql/graphiql

GraphiQL is an official GraphQL Foundation project and reference IDE ecosystem.

It is useful for:

```text
Schema exploration
Query development
Introspection
Documentation
Testing
IDE integration
Language services
```

The repository describes GraphiQL as the reference GraphQL IDE and language-service ecosystem. citeturn0search16

**Security note:** never assume that exposing an interactive GraphiQL interface in production is automatically safe. Treat it as part of your API's discoverability surface.

---

# 143. GraphQL Code Generator

## GraphQL Code Generator

- https://the-guild.dev/graphql/codegen
- https://github.com/dotansimha/graphql-code-generator

Useful for:

```text
GraphQL schema
      ↓
operations
      ↓
generated types
      ↓
generated client/server code
```

Use it to learn the broader principle:

> A GraphQL schema can become an input to a build-time toolchain rather than remaining only a runtime document.

This is directly related to the compiler-oriented architecture discussed in the Meta/Relay sections.

---

# 144. GraphQL ESLint

## GraphQL ESLint

- https://the-guild.dev/graphql/eslint
- https://github.com/B2o5T/graphql-eslint

Useful for:

- validating operations
- enforcing schema conventions
- detecting deprecated fields
- enforcing naming standards
- preventing bad query patterns
- CI enforcement

---

# 145. GraphQL Inspector

## GraphQL Inspector

- https://graphql-inspector.com/
- https://github.com/graphql-hive/graphql-inspector

Useful for:

```text
Schema diff
Breaking-change detection
Schema validation
CI/CD
Documents validation
Compatibility checks
```

For a serious GraphQL platform, schema compatibility testing should be treated similarly to an API contract test.

---

# 146. GraphQL Voyager

## GraphQL Voyager

- https://github.com/graphql-kit/graphql-voyager

Useful for visually exploring a GraphQL schema as a graph.

Good for:

- learning
- architecture inspection
- discovering relationships
- understanding large schemas

Do not confuse visualization with governance. A graph visualization helps you see complexity; it does not control complexity.

---

# 147. GraphQL Mesh

## GraphQL Mesh

- https://the-guild.dev/graphql/mesh
- https://github.com/ardatan/graphql-mesh

Useful for learning how GraphQL can sit above heterogeneous systems.

Conceptually:

```text
REST
OpenAPI
gRPC
GraphQL
SQL
SOAP
other sources
       ↓
GraphQL layer
```

This is especially useful for understanding the difference between:

```text
GraphQL as an API contract
```

and:

```text
GraphQL as an orchestration/integration layer
```

---

# 148. Hasura

## Hasura

- https://hasura.io/docs/
- https://github.com/hasura/graphql-engine

Hasura is useful as a reference for:

```text
Database
   ↓
GraphQL
   ↓
Authorization
   ↓
API
```

It is particularly useful when learning how a GraphQL API can be generated around an existing data model.

However, do not use Hasura's architecture as a definition of GraphQL itself.

---

# 149. GraphQL Hive / Schema Registry Concepts

## GraphQL Hive

- https://the-guild.dev/graphql/hive
- https://github.com/graphql-hive

Useful for studying:

- schema registry
- schema checks
- usage reporting
- contracts
- breaking-change detection
- distributed graph governance

This becomes relevant when moving from:

```text
one GraphQL server
```

to:

```text
many teams
many services
many schemas
many deployments
```

---

# 150. Real-Time GraphQL

GraphQL subscriptions are important, but remember:

> A GraphQL subscription is a client-facing API mechanism, not a replacement for Kafka.

Study:

- GraphQL subscriptions
- WebSockets
- Server-Sent Events
- event brokers
- durable event logs
- fan-out
- backpressure
- reconnect semantics

Official starting point:

- https://graphql.org/learn/subscriptions/

Apollo subscription documentation:

- https://www.apollographql.com/docs/apollo-server/data/subscriptions/

The architecture should normally look more like:

```text
                   Kafka
                     │
          ┌──────────┴──────────┐
          ▼                     ▼
       Worker A              Worker B
          │                     │
          └──────────┬──────────┘
                     ▼
              Subscription
                  Layer
                     │
                     ▼
                  Client
```

rather than:

```text
Client
  ↓
GraphQL
  ↓
Kafka
```

GraphQL is the client-facing API contract. Kafka is the durable event infrastructure.

---

# 151. Redis + GraphQL References

Redis is not part of GraphQL itself.

Study Redis as an infrastructure component supporting:

```text
Caching
Rate limiting
APQ
Distributed coordination
Session/state support
Pub/sub where appropriate
Query-plan caching
Response caching
```

Official Redis documentation:

- https://redis.io/docs/

Apollo Redis-related production concepts:

- Apollo Router distributed caching
- APQ
- response caching
- query-plan caching

Apollo's current performance documentation describes Redis-backed distributed response caching and authorization-aware cache separation. citeturn0search8

### Critical cache rule

Never make this mistake:

```text
cache["query"] = response
```

when the response depends on:

```text
user
tenant
role
locale
permissions
feature flags
authorization context
```

The cache key must represent the relevant security and personalization dimensions.

---

# 152. Kafka + GraphQL References

## Apache Kafka

- https://kafka.apache.org/documentation/

Study:

- topics
- partitions
- producers
- consumers
- consumer groups
- offsets
- ordering
- retention
- replay
- delivery semantics
- compaction
- transactions

Then study how GraphQL sits above Kafka.

A useful mental model:

```text
Kafka
 = event infrastructure

GraphQL
 = API contract

Subscription
 = client-facing real-time delivery mechanism
```

This distinction prevents a large number of architecture mistakes.

---

# 153. Federation Alternatives

Apollo Federation is not the only possible architecture.

Research:

### GraphQL schema stitching

- https://the-guild.dev/graphql/stitching

### GraphQL Mesh

- https://the-guild.dev/graphql/mesh

### Apollo Federation

- https://www.apollographql.com/docs/graphos/schema-design/federated-schemas/federation

Compare:

```text
Schema Stitching
Federation
Gateway aggregation
BFF
Modular monolith
Single GraphQL server
```

Do not introduce federation simply because your system has multiple services.

A modular monolith can be dramatically simpler.

---

# 154. GraphQL Architecture Patterns to Research

Search/read about these patterns individually:

## Single GraphQL Server

```text
Client
  ↓
GraphQL
  ↓
Application
  ↓
DB
```

Best for learning.

## Modular Monolith

```text
GraphQL
   ↓
Application
 ┌─┴─────────────┐
 │ Users         │
 │ Billing       │
 │ Products      │
 │ Orders        │
 └───────────────┘
   ↓
Database
```

Often the best starting point for a serious product.

## GraphQL BFF

```text
Frontend
   ↓
GraphQL BFF
 ├── REST
 ├── gRPC
 ├── DB
 └── external APIs
```

Useful when GraphQL primarily exists to shape data for clients.

## Federated Graph

```text
Client
  ↓
Router
 ├── Users
 ├── Orders
 ├── Billing
 └── Inventory
```

Useful when independent teams/services need a unified graph.

---

# 155. GraphQL Observability

Research these topics:

```text
OpenTelemetry
Distributed tracing
Resolver timing
Query operation names
Query signatures
Error rates
Field-level latency
Database fan-out
N+1 detection
Cache hit/miss
Query complexity
Router latency
Subgraph latency
```

## OpenTelemetry

- https://opentelemetry.io/docs/

A serious GraphQL system should allow you to answer:

```text
Which operation was slow?
        ↓
Which field was slow?
        ↓
Which resolver was slow?
        ↓
Which service was slow?
        ↓
Which database query was slow?
        ↓
Was Redis involved?
        ↓
Was Kafka involved?
```

Without this, GraphQL can become a beautiful abstraction hiding a terrible execution path.

---

# 156. GraphQL Testing

Research and implement at least:

## Schema tests

```text
Does the schema build?
```

## Validation tests

```text
Does invalid GraphQL fail?
```

## Resolver tests

```text
Does each field return the correct result?
```

## Authorization tests

```text
Can user A access user B's data?
```

## Integration tests

```text
GraphQL
 → DB
 → Redis
 → Kafka
```

## Contract tests

```text
Schema
 → client operations
```

## Compatibility tests

```text
old client
      ↓
new schema
```

## Load tests

```text
simple query
deep query
wide query
expensive query
batch
subscription
```

## Security tests

```text
IDOR/BOLA
BFLA
query depth
query complexity
alias abuse
batch abuse
introspection
CSRF
rate limits
authorization bypass
```

---

# 157. Schema Governance

Official GraphQL learning resources now include schema ownership, governance models, schema review, and schema change management. citeturn0search1

Research:

```text
Schema ownership
Schema review
Deprecation
Breaking changes
Compatibility
Field usage
Operation registry
Persisted operations
Schema registry
CI checks
Federation composition
Contract testing
```

A mature GraphQL organization should be able to answer:

> Who owns this field?

> Who uses this field?

> Can we remove it?

> Is it deprecated?

> Which clients will break?

> Which service resolves it?

> What is its authorization policy?

> What is its performance cost?

---

# 158. Persisted Queries / APQ / Safelisting

These concepts are related but not identical.

## Persisted operations

The server knows an operation ahead of time.

```text
Client
  ↓
operation ID
  ↓
server
  ↓
known query
```

## APQ

The client sends a hash.

```text
hash(query)
    ↓
server
    ↓
known?
```

If known, the server can avoid receiving the full operation text.

## Safelisting

Only explicitly approved operations may execute.

```text
approved operation
       ↓
allowed

unknown operation
       ↓
rejected
```

Use these concepts deliberately rather than calling everything "persisted queries."

---

# 159. GraphQL Security Research References

Beyond OWASP, research:

- GraphQL security testing
- API authorization
- BOLA/IDOR
- BFLA
- GraphQL DoS
- query complexity
- batching attacks
- alias attacks
- introspection exposure
- schema leakage
- federation security
- resolver authorization
- business-logic abuse

Useful high-level sources:

- https://owasp.org/API-Security/
- https://cheatsheetseries.owasp.org/
- https://graphql.org/learn/
- https://www.apollographql.com/docs/graphos/platform/security/

The previously discussed `win3zz/Meta-Owned-IT-Assets` repository should be treated as a **security-research/asset-inventory reference**, not as an official Meta GraphQL architecture guide.

For safe learning, extract the general lessons:

```text
large organization
      ↓
many public/internal assets
      ↓
many API surfaces
      ↓
many authorization boundaries
      ↓
configuration differences
      ↓
security bugs
```

Do not treat a public asset inventory as permission to test systems.

---

# 160. GraphQL Community and Ecosystem Discovery

## GraphQL Foundation

- https://graphql.org/foundation/

## GraphQL Blog

- https://graphql.org/blog/

The official resource hub includes announcements, specification work, grants, ecosystem news, videos, reading resources, and community material. citeturn0search5

## GraphQL Working Group

- https://github.com/graphql/graphql-wg

Useful once you want to understand how GraphQL itself evolves.

## GraphQL GitHub Organization

- https://github.com/graphql

Important repositories include:

```text
graphql-spec
graphql-js
graphiql
graphql-wg
```

---

# 161. Books and Long-Form Learning

Use the official GraphQL resource hub to discover currently maintained books and learning material:

- https://graphql.org/resources/

For books, prefer resources that teach the specification and architectural principles rather than only a particular vendor framework.

Good long-form subjects include:

```text
GraphQL fundamentals
API design
schema design
distributed systems
event-driven architecture
database design
security
frontend data fetching
microservices
federation
observability
```

A GraphQL book should complement — not replace — the specification.

---

# 162. Conferences and Talks

Use the official GraphQL resources/video library:

- https://graphql.org/resources/

Search conference talks for:

```text
GraphQL at scale
Relay
Meta GraphQL
Apollo Federation
schema governance
GraphQL security
query planning
GraphQL performance
GraphQL compiler
mobile GraphQL
subscriptions
large GraphQL schemas
```

Conference talks are especially useful for seeing problems that documentation often simplifies.

---

# 163. GitHub Search Strategy

When researching GraphQL implementations, search GitHub for:

```text
graphql server
graphql execution engine
graphql parser
graphql validator
graphql query planner
graphql federation
graphql router
graphql dataloader
graphql complexity
graphql persisted queries
graphql schema registry
graphql subscriptions
graphql opentelemetry
```

Then inspect:

```text
README
spec references
tests
benchmarks
issues
design documents
release notes
```

**Tests are particularly important.**

A GraphQL implementation's tests often reveal more about its real semantics than a marketing page.

---

# 164. What to Read for Each Layer

## Layer 1 — Standard

Read:

1. GraphQL.org
2. GraphQL specification
3. GraphQL.js

Goal:

```text
Understand what GraphQL actually is.
```

## Layer 2 — API Design

Read:

1. GraphQL Learn
2. GraphQL best practices
3. Relay documentation
4. Apollo schema-design documentation

Goal:

```text
Design good schemas.
```

## Layer 3 — Application

Read:

1. gqlgen / Apollo Server / Yoga / your chosen implementation
2. DataLoader
3. database integration
4. authorization

Goal:

```text
Build a real GraphQL service.
```

## Layer 4 — Infrastructure

Read:

1. Redis documentation
2. Kafka documentation
3. OpenTelemetry
4. caching documentation
5. router/gateway documentation

Goal:

```text
Build a production architecture.
```

## Layer 5 — Distributed Graph

Read:

1. Apollo Federation
2. Federation specification
3. Router/query-planning documentation
4. schema governance
5. schema registry tooling

Goal:

```text
Operate many services behind one graph.
```

## Layer 6 — Security

Read:

1. OWASP GraphQL Cheat Sheet
2. OWASP API Security
3. Apollo security docs
4. implementation-specific security documentation

Goal:

```text
Make the graph difficult to abuse.
```

## Layer 7 — Compiler / Platform

Read:

1. Relay compiler
2. GraphQL Code Generator
3. persisted operations
4. APQ
5. schema registries
6. query planning
7. static analysis

Goal:

```text
Move expensive or dangerous work from runtime to build/deployment time.
```

---

# 165. The "Official First" Rule

When investigating a GraphQL feature, use this order:

```text
1. GraphQL specification
          ↓
2. GraphQL.org documentation
          ↓
3. Official implementation documentation
          ↓
4. Official GitHub repository/tests
          ↓
5. OWASP/security guidance
          ↓
6. Engineering blogs
          ↓
7. Community articles
          ↓
8. Stack Overflow / Reddit / random blogs
```

Do not reverse this order.

A random blog may explain something clearly while still describing an obsolete version or a vendor-specific behavior as though it were GraphQL itself.

---

# 166. Recommended Master Bookmark Set

If you want only the most important bookmarks, keep these:

### Standards

- https://graphql.org/
- https://spec.graphql.org/draft/
- https://github.com/graphql/graphql-spec

### Learning

- https://graphql.org/learn/
- https://graphql.org/resources/

### Reference implementation

- https://github.com/graphql/graphql-js

### Meta / Relay

- https://engineering.fb.com/
- https://relay.dev/
- https://github.com/facebook/relay

### Apollo

- https://www.apollographql.com/docs
- https://www.apollographql.com/docs/graphos/schema-design/federated-schemas/federation
- https://www.apollographql.com/docs/graphos/routing/
- https://www.apollographql.com/docs/graphos/platform/security/

### Security

- https://cheatsheetseries.owasp.org/cheatsheets/GraphQL_Cheat_Sheet.html
- https://owasp.org/API-Security/

### Go

- https://gqlgen.com/

### TypeScript / JavaScript

- https://the-guild.dev/graphql/yoga-server
- https://the-guild.dev/graphql/codegen

### Tooling

- https://github.com/graphql/graphiql
- https://graphql-inspector.com/
- https://github.com/graphql-kit/graphql-voyager

### Observability

- https://opentelemetry.io/docs/

### Infrastructure

- https://redis.io/docs/
- https://kafka.apache.org/documentation/

---

# 167. The Complete Learning Path

If the purpose of this handbook is **to actually become capable of designing and building GraphQL infrastructure**, use this sequence.

## Phase 1 — Learn the protocol

Read:

```text
GraphQL.org
   ↓
Specification
   ↓
GraphQL.js
```

Build:

```text
schema
query
mutation
fragment
variable
directive
resolver
validation
```

---

## Phase 2 — Build one serious API

Build:

```text
GraphQL
   ↓
Go / gqlgen
   ↓
PostgreSQL
```

Implement:

```text
Authentication
Authorization
DataLoader
Pagination
Errors
Testing
```

---

## Phase 3 — Add Redis

Implement:

```text
Redis
 ├── response cache
 ├── rate limit
 └── persisted-operation/APQ storage
```

Then deliberately test:

```text
same query
different user
different tenant
different permissions
```

and verify that cache isolation is correct.

---

## Phase 4 — Add Kafka

Build:

```text
GraphQL mutation
       ↓
business operation
       ↓
Kafka event
       ↓
consumer
       ↓
materialized state
```

Then add:

```text
Kafka
  ↓
subscription layer
  ↓
GraphQL client
```

---

## Phase 5 — Production security

Add:

```text
Authentication
Authorization
Input validation
Depth limit
Complexity limit
Rate limit
Request size limit
Persisted operations
Safelist
CSRF protection
CORS policy
Audit logging
Security monitoring
```

Run security tests before moving on.

---

## Phase 6 — Observability

Add:

```text
OpenTelemetry
      ↓
GraphQL operation
      ↓
resolver
      ↓
DB
      ↓
Redis
      ↓
Kafka
```

Measure:

```text
latency
errors
cache hit rate
DB queries
resolver fan-out
query complexity
subscription count
Kafka lag
```

---

## Phase 7 — Modularize

Start with:

```text
one GraphQL server
```

Then organize internally:

```text
Users
Orders
Billing
Inventory
```

Do **not** immediately create microservices.

---

## Phase 8 — Microservices

Only after the modular architecture has a reason to split:

```text
Users service
Orders service
Billing service
Inventory service
```

Then decide whether the client should see:

```text
multiple APIs
```

or:

```text
one GraphQL graph
```

---

## Phase 9 — Federation

Introduce:

```text
Router
   ↓
Subgraphs
```

Study:

```text
composition
entities
keys
query planning
subgraph authentication
router authentication
schema governance
```

---

## Phase 10 — Compiler / Platform

Finally build:

```text
Schema
  ↓
Validation
  ↓
Static analysis
  ↓
Operation registry
  ↓
Generated code
  ↓
Persisted operations
  ↓
Query planning
  ↓
Runtime
```

At this point you are no longer merely **using GraphQL**.

You are understanding how to build a **GraphQL platform**.

---

# 168. Final Reference Architecture

The concepts in this handbook can ultimately be combined into:

```text
                           CLIENTS
                              │
             ┌────────────────┼────────────────┐
             │                │                │
           Web             Mobile           Internal
             │                │                │
             └────────────────┼────────────────┘
                              │
                              ▼
                    ┌──────────────────┐
                    │  API Edge / WAF  │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ GraphQL Router   │
                    │                  │
                    │ Auth             │
                    │ CORS / CSRF      │
                    │ Safelist         │
                    │ Rate limits      │
                    │ Demand control   │
                    │ Query planning   │
                    │ Telemetry        │
                    └────────┬─────────┘
                             │
             ┌───────────────┼────────────────┐
             │               │                │
             ▼               ▼                ▼
        Users Graph      Orders Graph    Billing Graph
             │               │                │
             └───────────────┼────────────────┘
                             │
          ┌──────────────────┼───────────────────┐
          │                  │                   │
          ▼                  ▼                   ▼
     PostgreSQL           Redis                APIs
          │                  │
          │                  │
          └──────────┬───────┘
                     │
                     ▼
                   Kafka
                     │
          ┌──────────┼──────────┐
          ▼          ▼          ▼
       Worker A   Worker B   Worker C
          │          │          │
          └──────────┼──────────┘
                     │
                     ▼
              Subscription Layer
                     │
                     ▼
                  CLIENTS
```

The important lesson is that **GraphQL is one layer in this system**.

It does not replace:

```text
PostgreSQL
Redis
Kafka
HTTP
gRPC
REST
microservices
authentication
authorization
observability
WAF
CI/CD
```

Instead, GraphQL provides a typed client-facing contract and an execution/orchestration model that can sit above those systems.

---

# 169. Final "Do Not Confuse These" Table

| Technology | What it actually is |
|---|---|
| GraphQL | API query language + execution/type system |
| GraphQL schema | Typed API contract |
| Resolver | Field execution/data-fetching function |
| GraphQL server | Runtime exposing a GraphQL schema |
| GraphQL client | Software constructing/executing GraphQL operations |
| Relay | GraphQL client + compiler/runtime architecture |
| Apollo Client | GraphQL client ecosystem |
| Apollo Server | GraphQL server implementation |
| Apollo Router | Graph/API routing and orchestration runtime |
| Federation | Architecture for composing multiple APIs/subgraphs |
| REST | Resource-oriented HTTP API style |
| gRPC | RPC framework/protocol ecosystem |
| Redis | In-memory data structure store / infrastructure component |
| Kafka | Distributed event streaming platform |
| DataLoader | Batching/caching utility commonly used with GraphQL |
| GraphQL subscription | Long-lived client-facing GraphQL operation |
| WebSocket | Transport commonly used for long-lived communication |
| SSE | HTTP-based server-to-client streaming mechanism |
| Persisted query | Server-known GraphQL operation |
| APQ | Hash-based automatic persisted-query mechanism |
| Safelist | Explicit allowlist of permitted operations |
| Query complexity | Estimate/control of operation cost |
| Query depth | Structural depth limit |
| Schema registry | System for storing/validating/distributing schemas |
| GraphQL compiler | Build-time transformation/analysis of GraphQL |
| OpenTelemetry | Vendor-neutral observability framework |

---

# 170. Final Rule for Learning GraphQL

Do not learn GraphQL as:

```text
"How do I write this query?"
```

Learn it as:

```text
What contract does the schema expose?
            ↓
How is the operation validated?
            ↓
How is it executed?
            ↓
Which resolvers run?
            ↓
How many backend calls happen?
            ↓
What authorization applies?
            ↓
What is cached?
            ↓
What is persisted?
            ↓
What is the query cost?
            ↓
What happens across services?
            ↓
What happens when the system scales?
            ↓
How is it observed?
            ↓
How is it secured?
            ↓
How does the schema evolve?
```

That is the difference between **knowing GraphQL syntax** and **understanding GraphQL engineering**.

---

# 171. Official Source Verification Notes

The resource list above was checked against current official documentation while preparing this handbook.

Particularly important verified sources include:

- GraphQL.org Learn and Resources for official learning material and ecosystem discovery. citeturn0search1turn0search5
- GraphQL specification guidance identifying the current working draft at `spec.graphql.org/draft`. citeturn0search9
- GraphQL.js as the reference JavaScript implementation. citeturn0search0
- Apollo Federation documentation for unified federated APIs and router/subgraph architecture. citeturn0search4
- Apollo security documentation for authentication, authorization, safelisting, CORS, CSRF, request limits, and demand control. citeturn0search10
- Apollo performance documentation for response caching and distributed Redis-backed caching. citeturn0search8
- OWASP's GraphQL Cheat Sheet for GraphQL-specific security considerations. citeturn0search13
- GraphiQL's official repository for the GraphQL IDE/language-service ecosystem. citeturn0search16

**When a framework/vendor page conflicts with the GraphQL specification, investigate the difference instead of assuming the framework defines GraphQL.**
