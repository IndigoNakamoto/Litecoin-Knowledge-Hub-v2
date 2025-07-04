# **Project Roadmap: Litecoin Knowledge Hub**

## **Project Scope & Objectives**

A RAG (Retrieval-Augmented Generation) Chatbot for Litecoin users that delivers real-time, high-accuracy answers by retrieving from a human-vetted, Payload CMS–managed knowledge base. Instrumentation, test-eval harnesses, and user feedback loops are baked in from day one to drive us past 95% answer accuracy.

---

## **Strategic Value Proposition**

1. **Ensuring Data Accuracy**

   * Canonical, curated content in Payload CMS
   * Nightly regression tests against a canonical Q&A suite

2. **Providing Real-Time Information**

   * Live blockchain & market API lookups
   * Accuracy alerts on metric drift

3. **Delivering Verifiable Trust**

   * In-line citations to Payload articles & APIs
   * User ratings (1–5★ + 👍/👎) feeding back into editorial workflows

---

## **Phase 1: MVP Core Foundation & Launch**

*Goal: Ship a stable, content-driven RAG pipeline with basic metrics and lay the groundwork for feedback loops.*

| Deliverable                                                  | Description                                                                                                                                      |
| :----------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------- |
| **1.1 Payload CMS Editorial Workflow**                       | Role-based drafts → Foundation approval → publish                                                                                                |
| **1.2 Content Structuring & Sync**                           | Define Payload collections; `afterChange` hooks → Content Sync Service                                                                           |
| **1.3 Core RAG Pipeline**                                    | **Haystack-powered pipeline:** Haystack Preprocessor for chunking/embeddings, FAISS/Elasticsearch DocumentStore, and a Retriever-Ranker-Reader pipeline integrated with Gemini Pro. |
| **1.4 Omnichannel Integration & Intent Handling**            | Integrate Chatwoot for omnichannel support and configure Dialogflow for initial intent routing.                                                  |
| **1.5 Production Deployment**                                | Next.js on Vercel, FastAPI & CMS hosted; public, stable MVP                                                                                      |
| **1.6 Basic Instrumentation**                                | Log queries/responses/docs; expose `/metrics`; initial Grafana dashboards                                                                        |
| **1.7 MVP Content Population & Validation**                  | Populate Payload with “Litecoin Basics & FAQ”; run end-to-end test queries (“What is Litecoin?”, etc.) to confirm accurate ingestion & retrieval |
| **1.8 MVP Testing, Refinement & Deployment**                 | Comprehensive UI/UX, performance & security tests; refine based on feedback; full production rollout; verify monitoring/logging                  |

> **Current Sprint:**
> (To be determined)

---

## **Phase 2: UX, Accuracy & Feedback Loops**

*Goal: Drive continuous improvement and transparency so we never dip below 95% accuracy.*

| Milestone                             | Focus                                                                                       |
| :------------------------------------ | :------------------------------------------------------------------------------------------ |
| **2.1 Source Citations**              | In-line footnotes linking to Payload entries & API docs                                     |
| **2.2 Contextual Discovery**          | Generate 2–3 follow-ups after each answer                                                   |
| **2.3 Hybrid Retrieval & Re-ranking** | Vector + keyword search; domain-driven re-ranking (implemented via Haystack Pipelines)      |
| **2.4 User Feedback Widgets**         | 👍/👎, 1–5★, “suggest edit” → Feedback sent to the Metrics Service for aggregation and analysis. |
| **2.5 Automated Test-Eval Harness**   | Leverage **Haystack's Eval module** to run nightly tests on a 200–500 Q&A suite; set pass/fail thresholds and alerts. |
| **2.6 Metrics & Dashboards**          | Answer Accuracy %, Precision@k, Satisfaction Score; Grafana + daily summaries              |
| **2.7 Error Clustering & Triage**     | Weekly export of failures & 👎 votes; cluster & tag; editorial sprints to tackle top issues |
| **2.8 Human Support Escalation**      | Define and implement the escalation path from the chatbot to human support agents within Chatwoot. |

---

## **Phase 3: Live Data & Developer Integrations**

*Goal: Surface real-time blockchain and market info, plus developer resources—all backed by our trust & feedback engine.*

| Feature                               | Description                                                 |
| :------------------------------------ | :---------------------------------------------------------- |
| **3.1 Transaction & Block Explorer**  | Live lookups + contextual explanations                      |
| **3.2 Market Data & Insights**        | Real-time price, cap, volume; historical charts             |
| **3.3 Developer Docs & SDK Snippets** | Ingest official Litecoin docs; “show me example” code flows |

---

## **Architectural Overview**

For a detailed visual representation of the system architecture, please see the [architecture.mmd](architecture.mmd) file.

---

## **Major Milestones & Timeline**

| Phase & Milestone | Due Date | Status |
| :--- | :--- | :--- |
| **Phase 1: MVP Core Foundation & Launch** | | |
| **1.1 Payload CMS Editorial Workflow** | TBD | ⬜ Planned |
| **1.2 Content Structuring & Sync** | TBD | ⬜ Planned |
| **1.3 Core RAG Pipeline** | TBD | ⬜ Planned |
| **1.4 Omnichannel Integration & Intent Handling** | TBD | ⬜ Planned |
| **1.5 Production Deployment** | TBD | ⬜ Planned |
| **1.6 Basic Instrumentation** | TBD | ⬜ Planned |
| **1.7 MVP Content Population & Validation** | TBD | ⬜ Planned |
| **1.8 MVP Testing, Refinement & Deployment** | TBD | ⬜ Planned |
| **Phase 2: UX, Accuracy & Feedback Loops** | | |
| **2.1 Source Citations** | TBD | ⬜ Planned |
| **2.2 Contextual Discovery** | TBD | ⬜ Planned |
| **2.3 Hybrid Retrieval & Re-ranking** | TBD | ⬜ Planned |
| **2.4 User Feedback Widgets** | TBD | ⬜ Planned |
| **2.5 Automated Test-Eval Harness** | TBD | ⬜ Planned |
| **2.6 Metrics & Dashboards** | TBD | ⬜ Planned |
| **2.7 Error Clustering & Triage** | TBD | ⬜ Planned |
| **2.8 Human Support Escalation** | TBD | ⬜ Planned |
| **Phase 3: Live Data & Developer Integrations** | | |
| **3.1 Transaction & Block Explorer** | TBD | ⬜ Planned |
| **3.2 Market Data & Insights** | TBD | ⬜ Planned |
| **3.3 Developer Docs & SDK Snippets** | TBD | ⬜ Planned |

---

## **Completion Criteria**

* **≥ 95% Automated Accuracy** on nightly regression suite
* **≥ 4.5 ★ Avg. User Rating** with < 5% 👎 votes
* **Weekly Triage** of failure clusters & backlog reduction
* **Full Editorial & Feedback Loop** operational (Payload CMS & Metrics Service)
