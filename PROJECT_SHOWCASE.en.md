# Fuyao Zhiyuan | Complete Platform Introduction

[中文](PROJECT_SHOWCASE.md) · [English overview](README.en.md)

## Positioning

Fuyao Zhiyuan is an integrated platform for college-application assistance and career planning. We combine admissions information, personalized recommendation algorithms, an AI advisor, multiple clients and institutional workspaces. Users can move from research and filtering to application-plan composition, diagnosis, consultation and planning deliverables.

The product connects five needs: accessible information, relevant eligibility conditions, editable plans, interactive consultation and persistent outputs.

## Who it serves

**Students and parents** compare scores, ranks, regions, subject requirements, institutions, majors and personal preferences.

**Educational consulting organizations** manage student profiles, review and edit plans, continue consultations and planning cases, and handle report documents.

**Platform operators** manage users, roles, entitlements, orders, promotions and service records.

## 1. Data and information services

Data models cover institution profiles, major classifications and career directions, historical admission scores and ranks, enrollment plans, regional batches, score-distribution tables and admission policies.

Discovery uses region, year, batch, subjects and the student profile as a shared context. Search results connect to institution and major details, historical information, enrollment conditions and subsequent selection workflows.

Major information includes courses and employment directions. Subject-choice and interest modules provide additional context for discussing education and development goals.

## 2. Recommendations and application plans

The recommendation engine derives candidates from the student's regional, batch and subject context, processes score/rank information, applies preferences, and organizes filtered results into relative-risk groups.

It supports both grouped-major and individual-major structures. Group summaries, child selections and application ordering have distinct meanings, allowing results to become an editable plan.

Reach/match/safer groupings communicate relative reference levels. They are rule- and data-based aids, not externally calibrated admission guarantees. Public materials do not disclose production parameters or claim an unverified accuracy rate.

## 3. AI advisor

The advisor links natural-language interaction with structured business tools. It can consult profiles, institution/major and admission information, candidate filters, and application-plan viewing and editing tools, then explain returned results through streamed responses.

User preferences can become structured filters or plan operations. Tool results supply the business state used in subsequent explanations. The server contains input validation, business authorization, tool-status handling and conversation records.

We describe the integration of model services with product workflows, rather than claim that a general-purpose foundation model was trained by the platform.

## 4. Plan management and diagnosis

Users can select major groups or individual majors, edit order, inspect composition statistics and export plans. User-edited order is preserved rather than replaced by recommendation sorting during display.

Existing plans can enter through file-parsing and diagnosis-related workflows. Structured records are combined with student context to organize analysis and exportable documents.

Selection, editing, statistics and diagnosis support a progression from candidate discovery to plan composition and review.

## 5. Subjects, interests and development directions

Subject-choice assistance, career-interest/personality assessments and major/career information supplement academic conditions with discussion of interests and goals.

They are supporting inputs for students and advisers, not a single assessment that determines the appropriate major or career.

## 6. Career planning and report delivery

A planning case starts with basic information and goals. Multi-turn consultation and choice responses clarify background, constraints and directions. Records connect that process to report services and document retrieval.

The project organizes resources and templates for further study, employment, study abroad and other pathways. Planning records, consultation state, report state and documents make cases revisitable.

Report processing and file readiness are separate. Document lists, downloads and sharing complete the delivery path. The actual workflow is not described as fully automatic production requiring no service participation.

## 7. Institutional workspace and operations

Institutional modules support student/user lists, academic and planning records, plan viewing/editing, service allowances and report documents.

Operations modules cover users and roles, statistics, orders and entitlements, promotions and service configuration. Identity and authorization connect roles to specific business records and resources.

These modules support an operational service, rather than only a collection of search and chat screens.

## 8. Multi-client product system

| Client | Primary direction |
|---|---|
| WeChat Mini Program | Mobile profiles, discovery, recommendations, plans, diagnosis, assessments and personal records |
| Individual Web | Desktop research, input, plan management, AI and planning workflows |
| Institutional Web | Student records, plans, consultation/planning cases and document services |
| iOS | Native discovery, plan management, AI interviews, planning and download/share interactions |
| Android | Mobile client engineering and integration with shared services |
| Public information pages | Product information, service descriptions, privacy information and user terms |

Shared services and models support different device-specific interactions. Feature parity and publication status are not automatically identical across client versions.

## Technology

Python/FastAPI organizes backend business services. SQLAlchemy and MySQL support structured data, while Redis is used in caching and state-related paths. Web uses Vue, the Mini Program uses uni-app, iOS uses Swift/SwiftUI, and Android has corresponding client engineering.

Recommendation services handle queries, constraints, risk references and group aggregation. AI services use tools and streaming to connect language interaction to business data. Identity, profiles, records, permissions and documents provide shared foundations.

Engineering mechanisms address pagination, cache invalidation, repeated requests, selection identities, conversation records and asynchronous document delivery.

![Platform architecture / 平台架构](assets/platform-architecture.png)

## Value

**For individual users:** organize information and choices into a coherent workflow, using filters, plan management and AI consultation to support comparison.

**For institutions:** connect student records, plans, consultations and documents in a continuing service workspace.

**For the product organization:** build a coordinated foundation of data, recommendation, intelligent interaction, clients and operations across application assistance and career planning.

This presentation describes implemented modules and product design, without adding unverified user-volume, commercial-return or effectiveness figures. Admissions conditions and policies should be checked against the applicable formal information.

See the [technical deep dive](docs/TECHNICAL_DETAILS.en.md) for implementation mechanisms.
