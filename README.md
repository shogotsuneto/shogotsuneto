# Hi there 👋

I'm **Shogo Tsuneto**, a generalist full-stack engineer interested in **modern microservices architecture** and building clean, minimal, and extensible tools across the stack — from frontend to infrastructure.

I hold the **AWS Certified DevOps Engineer – Professional** certification, and I've passed Japan's IPA **Network Specialist** and **Database Specialist** exams — backing a breadth that spans application development, networking, databases, and operations.

## 🐙 Heptapedal — an app, and the platform that runs it

A personal knowledge base of prepared answers to frequently-asked questions, built for **job-interview preparation** and **spoken language-test practice** (IELTS, TOEFL). MCP-first: an LLM client searches your prompts and stories by topic or semantic similarity, then uses them to coach, drill, or grade you — the browser UI is a viewer over the same data. Running at **[heptapedal.com](https://heptapedal.com)**.

### [heptapedal-infra](https://github.com/shogotsuneto/heptapedal-infra)
The infrastructure and delivery behind it. Managed Kubernetes on DigitalOcean, described in OpenTofu (plain Terraform HCL) and delivered by Argo CD app-of-apps GitOps: Gateway API ingress, cert-manager DNS-01 wildcard TLS, Sealed Secrets, managed Postgres with pgvector, and Grafana Cloud telemetry with an external probe. Sized to run for well under $100/month, with every trade-off written down as an ADR rather than implied.

### heptapedal *(private)*
The application itself, in Rust. One `axum` process serves three surfaces — an MCP server, an HTTP API, and a Leptos full-stack web UI — layered over a shared core and split across workspace crates so a surface can be pulled out later along a seam that already exists. Postgres + pgvector holds per-entity embeddings for similarity search; Supabase backs web login, and personal access tokens authenticate MCP clients.

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
