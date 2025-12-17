---
title: Projects
icon: fas fa-code-branch
order: 2
---

Below are the experiments I am currently building or planning. Each one is intentionally scoped so I can deliver a demo-worthy slice in a few weekends.

### GenAI News Copilot · 2025
Streamlit front-end that answers questions about curated news using retrieval-augmented generation, guardrailed APIs, and an AWS-backed document store.

**Architecture sketch:**
1. Python crawler (feedparser + BeautifulSoup) collects articles, normalizes text, and stores documents in S3 plus metadata in DynamoDB/OpenSearch.
2. Indexer lambda chunks articles, generates embeddings (AWS Bedrock or local model), and registers them in a vector store.
3. Guardrails layer wraps LLM calls, filters responses, and ensures every answer cites sources.
4. Streamlit app handles auth, issues semantic search queries, calls the guardrailed API, and displays answers with citations.


### Data & AI Platform Starter · 2024
Ship an infrastructure-as-code template that spins up ingestion (Kafka + Debezium), transformation (dbt + Dagster), and serving (DuckDB/Delta tables) so analytics teams can bootstrap trustworthy metrics quickly.

**Architecture sketch:**
- Wire Kafka, Debezium, Postgres OLTP, and DuckDB via docker-compose.
- Add Dagster jobs to move CDC topics into an object store and trigger dbt models.
- Publish a sample dashboard (Metabase or lightweight Streamlit) powered by the curated metrics.


### React CRM Playground · 2022-2023
A polished React SPA (likely Next.js + Chakra UI) that demonstrates contact management, a deal kanban, and activity timelines using mocked API services.

**Architecture sketch:**
- Define personas and sample datasets for contacts, opportunities, and tasks.
- Build reusable UI primitives (avatar stacks, kanban columns, activity feed) with responsive design.
- Add MSW scenarios for optimistic updates, errors, and latency to simulate real-world API behavior.

Have something interesting I should explore or collaborate on? [Reach out](mailto:frank.tao@outlook.com) and let’s chat.
