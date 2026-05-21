# Hi there 👋

I'm **Shogo Tsuneto**, a software engineer interested in **modern microservices architecture**, **schema-first development**, and building clean, minimal, and extensible tools across the stack.

## 🦀 Rust & WebAssembly

Exploring modern frontend development with Rust:

### [pomodoro-leptos-csr](https://github.com/shogotsuneto/pomodoro-leptos-csr)
A Pomodoro timer that runs entirely in the browser, built with the [Leptos](https://leptos.dev/) framework (client-side rendering) and compiled to WebAssembly. Features work/break cycles with auto-start, configurable durations, task attribution, session history, and in-flight session persistence via IndexedDB. Built and deployed to GitHub Pages with Trunk. **[Live app →](https://shogotsuneto.github.io/pomodoro-leptos-csr/)**

## 🔐 Authentication & API Tooling

Tools for modern API development, testing, and identity:

### [jwks-mock-api](https://github.com/shogotsuneto/jwks-mock-api)
A lightweight mock JSON Web Key Set (JWKS) service for backend API development and testing. Single binary (~10MB) with dynamic JWT claims, multiple keys support, and OAuth 2.0 token introspection — useful for exercising JWKS and OAuth 2.0 flows without a full identity provider.

### [simple-query-server](https://github.com/shogotsuneto/simple-query-server)
A lightweight server with YAML-based configuration for database connections and query definitions. Create read-only database APIs without writing custom code for each query.

## 🎯 Event Sourcing & CQRS

Building blocks for event-driven architecture with clean Go interfaces:

### [go-simple-eventstore](https://github.com/shogotsuneto/go-simple-eventstore)
A lightweight Go library providing a unified interface for event stores across various databases. Features append-only storage, cursor-based consumption, and multiple backend adapters (PostgreSQL, In-Memory, DynamoDB in progress).

### [go-eventsourced](https://github.com/shogotsuneto/go-eventsourced)
Minimal in-memory event-sourced state management for Go with clean State interface constraint design. Type-safe event handling with generic constraints and thread-safe operations.

### [go-simple-es-projector](https://github.com/shogotsuneto/go-simple-es-projector)
A minimal event worker that repeatedly pulls events from an event source and invokes user-provided projection logic. Users control checkpoint storage and transactional atomicity.

## 🎭 Dapr Actor Model

Schema-first tooling for distributed actor systems:

- **[dapr-actor-gen](https://github.com/shogotsuneto/dapr-actor-gen)** — Code generator producing Go interfaces and types from OpenAPI 3.0 specs for Dapr actors.
- **[dapr-actor-experiment](https://github.com/shogotsuneto/dapr-actor-experiment)** — Demo of Dapr actors covering state management, method invocation, and CQRS.
