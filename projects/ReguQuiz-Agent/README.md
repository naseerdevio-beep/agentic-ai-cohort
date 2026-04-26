# Project ReguQuiz-Agent 🎓
### Autonomous Pedagogical Orchestration for Compliance Mastery

---

## 🎯 Purpose
**ReguQuiz-Agent** is an intelligent "Examiner" system. It autonomously generates and administers adaptive exams based on specific regulatory standards (e.g., ISO 42001, NIST RMF). It aims to verify that an end-user has truly mastered a compliance framework by moving through sequential levels of difficulty and providing a verifiable comprehension rating.

---

## 🧠 Foundational Concepts
* **Bloom's Taxonomy:** Designing agents that test different cognitive levels (Knowledge, Application, Analysis).
* **Adaptive Evaluation:** A dynamic feedback loop that increases or decreases difficulty based on user performance.
* **Knowledge Retrieval:** Using targeted vector searches to ground the exam in a specific policy.

---

## 🛠 Technical Requirements
1. **Dynamic Syllabus Generation:** The agent must "read" the standard and create a list of key concepts to test.
2. **Sequential Exam Loop:** Implement a 10-step adaptive questionnaire.
3. **Reasoning-Based Grading:** The local SLM must grade free-text answers and provide citations for why the user was correct or incorrect.
4. **Final Comprehension Profiling:** Output a mastery score and identify specific knowledge gaps.

---

## 📜 Rules
* **No Hardcoded Questions:** All questions must be generated on-the-fly from the document context.
* **State Persistence:** Must maintain the state of the exam across sessions.
* **Local SLM only:** The exam must run locally to demonstrate private, cost-effective evaluation.
