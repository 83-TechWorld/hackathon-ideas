# 🚀 CFT 2025 Hackathon Project Ideas

This repository contains six innovative GenAI + Automation ideas that solve real-world challenges in enterprise environments.  
Each section includes **name, explanation, steps to achieve, use case, current gap, better solution, tech stack, and prerequisites**.

---

## 1. PulseOne (Centralised Performance Tool)

**Explanation:**  
PulseOne provides a single dashboard to monitor API/application performance by running synthetic tests with dynamic variables. It eliminates reliance on costly and fragmented monitoring tools.

**Steps to Achieve:**  
1. Collect API endpoints (Swagger/Postman, DNS).  
2. Build synthetic tests (k6/Locust).  
3. Store metrics in a time-series DB.  
4. Visualize in Grafana/Metabase.  
5. Integrate LLM to explain anomalies.  

**Use Case:**  
Unified API performance insights across teams for faster troubleshooting and capacity planning.  

**What Doesn’t Exist:**  
Most companies use siloed monitoring (New Relic, Datadog), not a **central, customizable in-house tool**.  

**Better Solution:**  
Customizable, cheaper, and variable-driven performance tool with unified dashboards.  

**Tech Stack:**  
- Backend: Node.js / Spring Boot  
- Testing: k6 / Locust / JMeter  
- Database: TimescaleDB / InfluxDB  
- Visualization: Grafana / Metabase  
- LLM: GPT/Claude for anomaly explanation  

**Prerequisites:**  
- List of APIs with authentication details  
- Monitoring infra (Prometheus/log collection)  

---

## 2. SprintShip (Auto Deployments with Jira + n8n + LLM)

**Explanation:**  
SprintShip automates deployments by connecting Jira sprint closures to GitHub Actions, generating release notes and CI/CD pipelines automatically.  

**Steps to Achieve:**  
1. Connect Jira API to detect sprint closure.  
2. Fetch tickets & generate release notes with LLM.  
3. Auto-generate GitHub Actions YAML workflow.  
4. Trigger CI/CD deployment pipeline.  
5. Notify teams via Slack/Teams.  

**Use Case:**  
Reduces manual effort in release management and minimizes errors in CI/CD.  

**What Doesn’t Exist:**  
No native link between **Jira releases → auto CI/CD pipelines**.  

**Better Solution:**  
Automated “Jira-to-deploy” workflow with AI-generated changelogs and deployments.  

**Tech Stack:**  
- Workflow: n8n / Temporal.io  
- CI/CD: GitHub Actions / ArgoCD  
- LLM: GPT-4/5 for summarization  
- Integrations: Jira API, GitHub API, Slack/Teams API  

**Prerequisites:**  
- Jira API access  
- GitHub Actions setup with deployment permissions  

---

## 3. HireWise (Requirement Matching Bot)

**Explanation:**  
HireWise matches resumes with job descriptions using embeddings and explains fit/gap with AI, going beyond keyword-based ATS systems.  

**Steps to Achieve:**  
1. Parse job requirements and candidate resumes.  
2. Generate embeddings for semantic comparison.  
3. Rank candidates by similarity score.  
4. Use LLM to explain match quality.  
5. Provide recruiter-friendly UI.  

**Use Case:**  
Recruiters quickly identify the best candidates and reduce bias in shortlisting.  

**What Doesn’t Exist:**  
ATS systems rely mostly on **keywords**, not contextual skill matching.  

**Better Solution:**  
Semantic understanding of skills + LLM explainability for better recruitment.  

**Tech Stack:**  
- Backend: Python (FastAPI)  
- LLM Embeddings: OpenAI / HuggingFace InstructorXL  
- DB: Pinecone / Weaviate / pgvector  
- Frontend: React / Next.js  

**Prerequisites:**  
- Resume dataset + job descriptions  
- Vector database setup  

---

## 4. TechHive (Centralised Technical Bot)

**Explanation:**  
TechHive is a knowledge bot trained on internal docs, wikis, and Confluence that provides instant technical guidance, migration steps, and troubleshooting help.  

**Steps to Achieve:**  
1. Crawl/export internal docs and wikis.  
2. Index into vector DB.  
3. Implement RAG pipeline with LLM.  
4. Deploy as Slack/Teams bot.  
5. Fine-tune for company guidelines.  

**Use Case:**  
Helps employees resolve technical issues faster without searching multiple systems.  

**What Doesn’t Exist:**  
No **unified assistant** combining all company documentation.  

**Better Solution:**  
One centralised LLM-powered bot for all technical queries.  

**Tech Stack:**  
- RAG: LangChain / LlamaIndex  
- DB: Pinecone / Weaviate / pgvector  
- LLM: GPT-4/5 or Llama 3  
- Integration: Slack/Teams SDK  

**Prerequisites:**  
- Access to all documentation sources  
- Internal knowledge export permissions  

---

## 5. DeckCraft (AI-Powered PPT Maker)

**Explanation:**  
DeckCraft generates branded PowerPoint decks from simple prompts, following company templates and guidelines.  

**Steps to Achieve:**  
1. Take input prompt (topic, audience).  
2. Generate slide structure and content using LLM.  
3. Build branded PPT with python-pptx.  
4. Apply company logo, colors, and fonts.  
5. Export editable PPT file.  

**Use Case:**  
Saves management time spent creating repetitive presentations.  

**What Doesn’t Exist:**  
Copilot/Canva don’t enforce **strict company branding rules**.  

**Better Solution:**  
Instant branded decks aligned with corporate guidelines.  

**Tech Stack:**  
- Language Model: GPT-4/5  
- PPT: python-pptx, reportlab  
- UI: Streamlit / React  

**Prerequisites:**  
- Company PPT templates and brand guidelines  

---

## 6. GreenOps (Carbon-Aware Kubernetes Monitoring)

**Explanation:**  
GreenOps measures Kubernetes resource usage, converts it into CO₂ emissions, and uses AI to suggest optimizations for greener and cost-efficient cloud operations.  

**Steps to Achieve:**  
1. Install CloudAware SDK in Kubernetes cluster.  
2. Collect usage metrics (CPU, GPU, storage).  
3. Map usage → carbon footprint (CO₂eq).  
4. Build Grafana dashboards.  
5. Use LLM for optimization recommendations.  

**Use Case:**  
Helps organizations with **ESG reporting** and carbon reduction strategies.  

**What Doesn’t Exist:**  
No standard tool links **Kubernetes usage → carbon impact → AI recommendations**.  

**Better Solution:**  
Actionable sustainability insights with AI-driven cloud optimization.  

**Tech Stack:**  
- Monitoring: Prometheus + Grafana  
- SDK: CloudAware SDK / Cloud Carbon Footprint  
- Backend: FastAPI / Python  
- LLM: GPT/Llama for recommendations  

**Prerequisites:**  
- Kubernetes cluster access  
- SDK installation + carbon conversion data


# RiskTalk 🛡️💬
**Talk to your risks, get instant insights.**

RiskTalk is a **natural language assistant for operational risks and incidents**.  
Instead of logging into multiple dashboards or manually checking KRIs (Key Risk Indicators),  
users can simply **chat** with RiskTalk to:

- Ask about **previous vs current risk values**  
- Check if a **risk is above or below threshold**  
- Retrieve **incident action numbers**  
- Get a quick **summary of operational risks** across projects  

---

## 🚀 Use Case

### Current Problem
Management and users must manually log into risk systems, navigate dashboards, and interpret values. This slows down decision-making and introduces friction.

### What Doesn’t Exist Today
Most companies lack a **central conversational interface** that connects to risk data systems (KRI, incidents, operational risk logs).

### Better Solution (RiskTalk)
A **chat-based assistant** that integrates with risk systems, allowing users to interact naturally:

- “What was the last KRI value for cheque loss?”  
- “Is the current fraud risk above threshold?”  
- “Show me the action number for incident RISK-123.”  

---

## 🛠️ Steps to Achieve

1. **Data Access & APIs**  
   - Integrate with your risk/KRI systems (databases, REST APIs, or internal tools).  
   - Define endpoints for risk values, thresholds, incidents, and actions.  

2. **Natural Language Layer**  
   - Use an **LLM (OpenAI GPT, LLaMA, Mistral, or company LLM)** to parse user questions.  
   - Map natural queries to backend APIs (e.g., "previous KRI" → `/api/kri/history`).  

3. **Conversational Bot Interface**  
   - Build a web chat UI (React + TypeScript + WebSockets/REST).  
   - Optionally integrate into **Slack / MS Teams / company intranet**.  

4. **Threshold Analysis & Alerts**  
   - Compare values with thresholds.  
   - Return results like:  
     > “The current fraud KRI is 12, which is above the threshold of 10 🚨.”  

5. **Continuous Improvement**  
   - Add feedback loop (“Did this answer help?”).  
   - Train on historical queries to improve accuracy.  

---

## 📊 Example Queries

- “What is the current KRI value for cheque loss?”  
- “Show me the last 3 incident values for fraud.”  
- “Is vendor risk above threshold?”  
- “Give me the risk action number for RISK-0021.”  

---

## 🧰 Tech Stack

- **Frontend:** React + TypeScript + Tailwind (chat UI)  
- **Backend:** FastAPI (Python) or Spring Boot (Java) for API orchestration  
- **Database:** PostgreSQL / MySQL (for KRI & incident values)  
- **LLM Layer:**  
  - OpenAI GPT / Azure OpenAI  
  - OR open-source (LLaMA2, Mistral, RAG with LangChain)  
- **Integration:** Slack / MS Teams / Web Portal  
- **Dashboard (optional):** Grafana / Superset for visualization  

---

## 📋 Prerequisites

- Access to **risk/KRI/incident data sources** (APIs, DB, or ETL pipelines)  
- LLM API key or deployed open-source LLM  
- Basic infrastructure:  
  - Containerization (Docker + Kubernetes for scaling)  
  - Authentication (SSO / OAuth2)  
- Optional: Cloud setup for logging & monitoring (AWS/GCP/Azure)  

---

## 🌟 Why RiskTalk?

✅ One-stop conversational interface for **all operational risks**  
✅ Removes the need for manual dashboard navigation  
✅ Helps **management make faster risk decisions**  
✅ Reusable across **KRI, operational risk, incidents, thresholds**  

---

## 📐 Architecture (High-Level)

```mermaid
flowchart TD
    U(User) -->|Ask Question| UI(Chat_UI)
    UI --> API(Backend_API)
    API --> LLM(LLM_Parser)
    LLM --> DB(Risk_KRI_Database)
    DB --> API
    API --> UI
    UI -->|Response| U
