# Algorithms and AI | Connecting Data, Recommendations and Consultation

[中文](ALGORITHM_AND_AI.md) · [Technical deep dive](TECHNICAL_DETAILS.en.md)

## Data foundation

The engine uses region, batch, subjects, score/rank and institution/major enrollment and historical information. Structured models connect institutions, majors, admission results, rank tables and policies so discovery, recommendations, plans and AI tools can refer to consistent entities.

![Recommendation pipeline / 推荐流程](../assets/recommendation-pipeline.png)

## Recommendation stages

**Eligibility:** region, batch and subject constraints define the starting pool. Positive and negative preferences further filter institutions, majors and locations.

**Score/rank matching:** student rank is compared with candidate historical or estimated ranks. Score ranges and conversion availability affect filtering; the applicable path can fall back to direct score filtering.

**Relative-risk presentation:** reference calculations support candidate ordering and reach/match/safer groups. These are data- and rule-driven aids rather than independently calibrated admission probabilities. Production coefficients and prediction data are protected; effectiveness metrics use defined, reproducible evaluation protocols.

**Group aggregation and plans:** eligible child majors are organized into groups. Group summaries and child selections remain distinct. Results feed application-plan editing, target risk composition, statistics and exports, while manual order is preserved.

## Query engineering

Lightweight filtering, ordering and pagination precede complete detail loading. Group aggregation and statistics have their own handling, with cache mechanisms in applicable paths.

Profile and preference changes require synchronization or invalidation. Performance conclusions are based on controlled benchmarks and production observation.

## AI business tools

| Direction | Function |
|---|---|
| Student profile | Score, rank, region, batch, subjects and relevant background |
| Institutions and majors | Admissions, subject directions, institution information and policies |
| Candidate filters | Inspect the pool and add or remove conditions |
| Plan management | View, edit, summarize and organize plans |
| Conversation and records | Preserve context and connect later interactions |

The model converts intent into tool calls. Business services validate parameters and authorization, execute the calls and return structured results for explanations and UI events. Business state comes from tools rather than only free-form model text.

![Agent workflow / Agent 协作](../assets/agent-workflow.png)

## Streaming and continuity

Events carry text, choices, operation status and results. Conversation history, profiles and preferences provide context. Task records, cancellation and recovery paths apply state-specific strategies to transport interruption, user cancellation and business failure.

## Planning resources and reports

Consultation clarifies goals and constraints. Resources and templates cover multiple educational and career pathways, with planning records linking the case to document delivery.

Report state and file availability are separate. Review and specialist participation remain available so AI assistance operates within a managed service-delivery workflow.

## Division of responsibilities

**Algorithms organize candidates and relative risk; AI interprets questions, calls tools and explains results; applications make the workflow actionable.**

The integration is the engineering contribution, centered on business data, recommendation algorithms, agent-tool orchestration and multi-client product coordination.
