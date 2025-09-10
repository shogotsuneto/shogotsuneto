# Hi there 👋

I'm **Shogo Tsuneto**, a software engineer passionate about **Event Sourcing**, **CQRS**, and **modern microservices architecture**. My repositories focus on building clean, minimal, and extensible tools for event-driven systems and schema-first development.

## 🎯 Event Sourcing & CQRS

Building blocks for event-driven architecture with clean Go interfaces:

### [go-simple-eventstore](https://github.com/shogotsuneto/go-simple-eventstore)
A lightweight Go library providing a unified interface for event stores across various databases. Features append-only storage, cursor-based consumption, and multiple backend adapters (PostgreSQL, In-Memory, DynamoDB in progress).

### [go-eventsourced](https://github.com/shogotsuneto/go-eventsourced)
Minimal in-memory event-sourced state management for Go with clean State interface constraint design. Type-safe event handling with generic constraints and thread-safe operations.

### [go-simple-es-projector](https://github.com/shogotsuneto/go-simple-es-projector)
A minimal event worker that repeatedly pulls events from an event source and invokes user-provided projection logic. Users control checkpoint storage and transactional atomicity.

### [simple-query-server](https://github.com/shogotsuneto/simple-query-server)
A lightweight Go server with YAML-based configuration for database connections and query definitions. Create read-only database APIs without writing custom code for each query.

## 🎭 Dapr Actor Model

Schema-first development tools and patterns for building distributed actor systems:

### [dapr-actor-gen](https://github.com/shogotsuneto/dapr-actor-gen)
A standalone code generator for creating Go interfaces, types, and factory functions from OpenAPI 3.0 specifications for Dapr actors. Enables schema-first development with type-safe code generation.

### [dapr-actor-experiment](https://github.com/shogotsuneto/dapr-actor-experiment)
A comprehensive demo of Dapr actors demonstrating state management, method invocation patterns, and CQRS architecture. Features authentication middleware, multiple actor types, and complete Docker setup.

## 🛠️ Developer Tools

Utilities for modern API development and testing:

### [jwks-mock-api](https://github.com/shogotsuneto/jwks-mock-api)
A lightweight mock JSON Web Key Set (JWKS) service for backend API development and testing. Single binary (~10MB) with dynamic JWT claims, multiple keys support, and OAuth 2.0 token introspection.

---

💡 **These repositories work together** to provide a complete toolkit for building event-sourced microservices with Dapr, from foundational event stores to complete applications with authentication.