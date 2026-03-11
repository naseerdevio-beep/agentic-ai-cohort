# Project ReguFlow-Agent 🚀
### Autonomous SLM Orchestration for Dynamic Regulatory Compliance

---

## 🎯 Purpose of The Project
In an enterprise environment, regulatory documents (ISO, NIST, GDPR, etc.) are living entities. Traditional RAG systems fail because they are static and prone to "version-drift" hallucinations. 

**ReguFlow-Agent** is an advanced AI/ML project designed to build a self-healing, autonomous compliance system. The goal is to move beyond simple "Chat with PDF" applications and develop an **Agentic SLM Workflow** that can monitor, ingest, and reason over high-stakes documents with the precision of a Frontier Model (like Gemini 3 Flash) but at the cost and privacy of a local Small Language Model (SLM).

---

## 🧠 Foundational Concepts & Enterprise Relevance

This project imparts skills that are foundational to developing **Production-Grade AI**:

* **Agentic RAG (The First Principle):** Moving from a linear "Retrieve -> Generate" pipeline to a "Plan -> Retrieve -> Verify -> Refine" loop. This ensures the model self-corrects before delivering a response.
* **Atomic Versioning & Data Freshness:** Understanding the data engineering required to keep a Vector Database in sync with real-world document changes (Automatic CRUD operations on vectors).
* **SLM Parity & FinOps:** Learning how to optimize a 3B-7B parameter model (via Fine-Tuning or specialized Prompting) to match the reasoning capabilities of a 1T+ parameter model, drastically reducing enterprise inference costs.
* **Data Sovereignty:** Running local inference (on-prem/desktop) to ensure sensitive regulatory queries never leave the organization's infrastructure.

---

## 🛠 Technical Requirements

### 1. Autonomous Ingestion & Sync (Data Engineering)
* **Event-Driven Crawler:** Build a Python-based crawler (Scrapy/Playwright) to monitor a target regulatory site.
* **Semantic Versioning:** Implement a hashing mechanism. If `Document_v1.pdf` is updated to `v2.pdf`:
    * The system must automatically purge all vectors associated with `v1`.
    * The system must vectorize and upsert `v2` immediately.
* **Hybrid Indexing:** Utilize a Vector Database (ChromaDB or Qdrant) alongside a simple Metadata Store to track document relationships and "effective dates."

### 2. The Agentic SLM Core
* **Local SLM Deployment:** Interns must run an open-source SLM (e.g., **Phi-4, Llama 3.2 3B, or Mistral 7B**) locally using **Ollama** or **vLLM**.
* **Agentic Reasoning Loop:** Implement the **ReAct (Reason + Act)** pattern. The agent must:
    1.  **Analyze** the user query to determine which regulatory domain it hits.
    2.  **Search** the vector DB using specialized tools.
    3.  **Validate** the retrieved context against version metadata.
    4.  **Synthesize** the final answer.
* **Tool-Use:** The SLM must be configured to call internal Python functions (tools) for document comparison and date-logic.

### 3. Achieving Response Parity
* **The Gold Standard:** Use a Frontier LLM (Gemini 3 Flash) as the benchmark for "Perfect" answers.
* **Alignment via RAFT:** Use **Retrieval-Augmented Fine-Tuning (RAFT)** logic to train the SLM to ignore "distractor" documents and focus only on the relevant, newest versions.
* **Quantization Mastery:** Interns must evaluate the performance trade-offs between GGUF 4-bit, 8-bit, and FP16 weights.

---

## 📜 Rules of Engagement (To Prevent Copy-Pasting)

To ensure true comprehension of underlying concepts:

1.  **The "Zero-Wrapper" Policy:** You are **prohibited** from using high-level "Agent" wrappers (e.g., LangChain's `AgentExecutor`). You must write the loop logic, tool-calling parsers, and prompt-orchestration in raw Python.
2.  **IDE Constraint:** The entire project must be developed using **Cursor** or **Antigravity**. You must leverage AI-pair programming to refactor code, but you must be able to explain every line of the "Reasoning Loop."
3.  **No Internet Inference for SLM:** During the final demo, the SLM must function entirely **offline** on your local machine or a private cloud instance to prove data sovereignty.
4.  **Traceability:** Every response must include a "Thought Trace" (Chain of Thought) and a "Version Stamp" (e.g., *Source: NIST-800-53 Rev 5, Updated 2026-01-10*).

---

## 📊 Evaluation Criteria

| Metric | Goal | Description |
| :--- | :--- | :--- |
| **Semantic Accuracy** | > 85% Parity | How close is the SLM's answer to the Frontier Model's answer (using LLM-as-a-Judge)? |
| **Sync Latency** | < 2 Minutes | Time taken for a new web update to be reflected in the Agent's answers. |
| **Hallucination Rate** | < 3% | Percentage of responses where the agent cites a document version that has been deleted. |
| **Reasoning Depth** | Qualitative | Ability of the agent to recognize when two regulatory documents contradict each other. |
| **Inference Speed** | > 15 t/s | The local SLM must maintain a usable tokens-per-second rate on standard hardware. |