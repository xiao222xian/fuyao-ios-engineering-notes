# Platform Architecture | Clients and Shared Business Services

[中文](PLATFORM_ARCHITECTURE.md) · [Technical deep dive](TECHNICAL_DETAILS.en.md)

![Platform architecture / 平台架构](../assets/platform-architecture.png)

## Technology layers

| Layer | Technologies or mechanisms | Responsibilities |
|---|---|---|
| Backend | Python, FastAPI, SQLAlchemy | APIs, business rules, discovery, recommendation, identity and services |
| Data/cache | MySQL, Redis | Structured information, records, statistics and applicable caches |
| Web | Vue 3, TypeScript, componentized pages | Desktop discovery, plans and institutional workflows |
| Mini Program | uni-app / Vue ecosystem | WeChat mobile workflows |
| iOS | Swift, SwiftUI, asynchronous state management | Native discovery, consultation, planning and sharing |
| Android | Kotlin/Gradle and mobile integration | Android client engineering and shared-service access |
| AI integration | Tool calls, structured models and streaming | Connect language interaction to business data and actions |
| Documents | Parsing, templates and export-related services | Plans, diagnosis and report retrieval |

## Shared business models

Profiles, institutions/majors, plan entries, conversations, planning cases and documents are common entities. Clients consume services and organize interfaces for their own contexts.

Shared models do not imply identical functionality in every client version. Consistency comes from explicit provenance, field meanings and permissions, not identical screen layouts.

## Contracts and state

Queries retain region, year, batch, subjects and profile context. Optional fields and compatible shapes are handled at integration boundaries. Group summaries, child-major selections, manual ordering and recommendation sorting have separate semantics.

## AI tools and authorization

Business tools remain responsible for parameter validation, authorization and record ownership. Tool state, results and presentation are organized separately and delivered through events.

This lets intelligent interaction reuse existing business constraints instead of bypassing them.

## Asynchronous resources

Search needs first-load and refresh phases; conversations need event handling and cancellation; reports need processing state and file readiness. Pagination, request coordination, cache synchronization, history and document access address these different lifecycles.

The mechanisms are not advertised as unmeasured high-concurrency performance or unconditional reliability guarantees.

## Public disclosure

The diagram is an original responsibility map, not a production deployment map. Real addresses, interfaces, accounts, parameters and internal topology are excluded. Archived modules and historical checks are not evidence of current publication or acceptance across every client.
