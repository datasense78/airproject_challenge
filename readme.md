# 🚀 AlturaTech PolicyPilot Challenge

Welcome to the **PolicyPilot: AI Agentic Application Challenge**, where your task is to build an intelligent agent-based system that can answer complex internal company policy questions using real company documents and data.

This challenge tests your ability to:
- Build **multi-agent LLM orchestration**
- Implement **RAG (Retrieval-Augmented Generation)**
- Do **tool routing and document grounding**
- Handle **traceability, follow-up reasoning, and structured outputs**

---

## 🧠 Problem Statement

AlturaTech receives dozens of internal queries daily—from engineers, HR staff, and managers. These questions are buried across:
- PDF documents (HR Handbook, Security Protocol, Sales Playbook)
- A live HTML page (Engineering SOPs)

You must build an **AI Agentic System** that can:
1. Accept a user question
2. Route it to the correct document(s) via **routing logic or classifier**
3. Perform **multi-hop retrieval** if needed
4. Generate a final **structured answer** with:
   - Final answer
   - Source(s) used
   - Trace of document chunks or sections
   - Confidence score (optional)

---

## 📁 Documents Provided

| Type      | Title                                             | Source |
|-----------|---------------------------------------------------|--------|
| PDF       | Employee Lifecycle & Benefits Handbook            | `docs/hr_handbook.pdf`       |
| PDF       | Confidential Security Standards                   | `docs/security_protocol.pdf` |
| PDF       | Enterprise Sales Playbook                         | `docs/sales_playbook.pdf`    |
| Web Page  | Engineering SOPs (scrapable HTML)                | [https://your-username.github.io/your-repo-name](https://your-username.github.io/your-repo-name) |

---

## ⚙️ Project Requirements

You must use an **Agentic framework**. Options:
- LangGraph
- CrewAI
- Custom multi-agent controller in Python

Agents you must build:
- 🧱 **Router Agent** – identifies relevant doc(s) from user query
- 📚 **Retriever Agent** – performs vector or keyword-based chunk retrieval
- 🧠 **Reasoning Agent** – handles follow-ups, conflicting answers, or combines multiple document sections
- ✅ **Compliance Agent** – redacts risky content or adds policy-safe footnotes

---

## 🧪 Sample Questions & Expected Behaviors (Answers must be traceable to documents)

### 1. "Can I carry forward my leaves if I switch roles in Q4?"
- **Answer From:** `Employee Lifecycle & Benefits Handbook (PDF)`
- **Expected Output:**
  > "Yes, earned leave can be carried forward up to 18 days if your tenure exceeds 3 years. Switching roles does not reset your leave cycle. Per policy, internal transfers do not affect leave accrual or carry-forward unless a reset is initiated via AlturaBridge."  
  > *(Source: Page 2, Section 2 - Leave Policy)*

### 2. "What happens if someone injects an unauthorized container?"
- **Answer From:** `Confidential Security Standards (PDF)`
- **Expected Output:**
  > "Injection of rogue containers is automatically flagged by `SentinelGate`. It triggers Level 3 incident handling and logs are forwarded to the Digital Forensics Unit. Snapshots are preserved and user LDAP access is revoked."  
  > *(Source: Page 3, Section 8 - Forensics Trigger Points)*

### 3. "How often do Engineering on-call rotations happen?"
- **Answer From:** `Engineering SOPs (HTML Page)`
- **Expected Output:**
  > "On-call assignments rotate weekly. Alerts are routed through PagerDuty and posted to Slack via `altura-alerts@`."  
  > *(Source: HTML Section 4 - Monitoring & On-Call Rotation)*

### 4. "Can I give a 20% discount to a healthcare startup in Tier-2?"
- **Answer From:** `Enterprise Sales Playbook (PDF)`
- **Expected Output:**
  > "No. Discounts over 15% must be approved by Pricing Officers. Healthcare domain does not qualify for bundled SKUs unless escalated. Use the deal desk process and tag the CRM entry as `T2_STD`."  
  > *(Source: Page 2, Section 3 - Unauthorized Discounting)*

---

## ✅ Deliverables

- 📂 A clean repo with folders:
  - `/docs` → all provided PDFs
  - `/agents` → your agent definitions (Router, Retriever, etc)
  - `app.py` or `main.py` → your pipeline entry point
  - `README.md` → this file

- ✅ Final output must show:
  - Final answer
  - Source document name(s)
  - Retrieved text snippets or chunk IDs
  - Logs of agent decisions (optional but encouraged)

---

## 💡 Bonus Features

- 🕵️‍♂️ Show agent trace/flow in UI or logs
- 📊 Let user edit/refine question
- 🌐 Use PGVector, FAISS, or Chroma for chunk embedding
- 📄 Let user upload more docs in runtime (if you choose to support)

---

## 🏑 How to Submit

- Upload your repo to GitHub (public or private)
- Include a 2-minute demo video (screen recording is enough)
- Include a `demo_output.txt` or screenshots
- Optional: Deploy to Streamlit, Gradio, or HuggingFace Spaces

---

## 🧾 Evaluation Criteria (Total: 100 points)

| Criteria                            | Points |
|-------------------------------------|--------|
| Functional multi-agent architecture | 25     |
| Accurate routing and retrieval      | 20     |
| Correct use of source content       | 20     |
| Clear, structured final output      | 10     |
| Traceability / Logging of steps     | 10     |
| Bonus features (trace UI, edits)    | 10     |
| Code quality + modularity           | 5      |

Projects scoring 85+ will be considered for special feature/demo slot with the AlturaTech AI team.

---

## 🙌 Best of Luck!
Make it smart. Make it traceable. Make it useful.

For doubts, email us at: **challenge@alturatech.io**
