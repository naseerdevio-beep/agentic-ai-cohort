
## **Project: The Autonomous Gourmet Event Planner (AGEP)**

### **The "Why"**
Most AI apps just "chat." This project teaches you to build an **Agentic System**—a program that doesn't just talk, but **thinks, acts, and corrects itself** until a complex goal is met safely.

### **The Core Logic: Plan-Act-Reflect**
Instead of a single prompt, your app will run in a loop:
1.  **PLAN:** Break the dinner goal into sub-tasks (Menu, Shopping, Timing).
2.  **ACT:** Use tools to get real-world data (Prices, Ingredients, Allergy info).
3.  **REFLECT:** Audit the results. Does it fit the budget? Is it safe? 
    * *If NO:* Re-plan and try again.
    * *If YES:* Finalize and deliver.



---

### **Agent Roles (The Team)**
| Role | Responsibility | Tech Spec |
| :--- | :--- | :--- |
| **The Architect** | Designs the menu and strategy. | Temp 0.7 (Creative) |
| **The Executor** | Fetches prices and product availability. | Temp 0.1 (Precise) |
| **The Critic** | Checks the math (Budget vs. Reality). | Temp 0.0 (Strict) |
| **The Verifier** | Cross-checks ingredients for "hidden" allergies. | Temp 0.0 (Zero-Trust) |

---

### **Project Requirements**
* **Dynamic Inputs:** Must handle Guest Count, Budget, and Dietary Restrictions (e.g., Vegan + Nut-Allergy).
* **The Correction Loop:** If the Salmon is too expensive, the AI must automatically switch to a cheaper protein without asking the user.
* **The Safety Gate:** If the Architect suggests a "safe" dish that actually contains hidden allergens, the Verifier must catch it and reject the plan.
* **Termination Logic:** The system must stop after **5 failed attempts** and ask the human for help (Human-in-the-loop).



---

### **What You Will Learn**
1.  **Orchestration:** How to make specialized AI agents work as a cohesive team.
2.  **State Management:** How to track a "living" plan as it evolves.
3.  **Hallucination Prevention:** How to build "Zero-Trust" layers that verify AI claims against real databases.
4.  **Cost vs. Quality:** Balancing a model's creativity with real-world financial constraints.

**Next Step:** Use the provided Google ADK prompt in your IDE to generate the boilerplate code and begin your first "Plan-Act-Reflect" cycle!

---

Here are four enhancement ideas to evolve the Gourmet Architect project:

---

## 1. The "Experience Memory" Loop (Dynamic Few-Shot)
Standard agents treat every request as the first time they’ve ever cooked. This enhancement introduces a **Vector Database** (like Pinecone or Weaviate) to give the agents "Long-Term Memory."

* **The Loop:** Before the **Architect** plans, it queries the memory for past successful "Reflections."
* **The Sophistication:** If a previous loop rejected "Fresh Atlantic Salmon" because it was consistently over budget in April, the Architect learns to suggest "Steelhead Trout" immediately.
* **Concept Taught:** **RAG (Retrieval-Augmented Generation)** for agentic state and "Learning from Failure."

---

## 2. The "Adversarial Red-Teaming" Loop
Introduce a **"Saboteur Agent"** whose only job is to find edge-case failures in the Verifier’s safety checks.

* **The Loop:** After the **Verifier** clears a menu, the **Red-Teamer** attempts to find a loophole (e.g., "You cleared the Soy Sauce, but did you check if it contains wheat for the Gluten-Free guest?").
* **The Sophistication:** This creates a "Consensus Loop" where two agents must agree before the plan is finalized.
* **Concept Taught:** **Multi-Agent Debate** and **Robustness Testing**.



---

## 3. The "Dynamic Tool Synthesis" Loop (Self-Correction)
Instead of hard-coding APIs, give the **Executor** the ability to "write its own tools" when a standard search fails.

* **The Loop:** If the Grocery API is down or doesn't have a specific item, the Executor triggers a **Coder Agent** to write a quick web-scraper or a unit-conversion script (e.g., converting grams to ounces to verify budget).
* **The Sophistication:** The system isn't just using tools; it’s *building* them on the fly to solve roadblocks.
* **Concept Taught:** **LLMs as Tool Builders (LATB)** and **Recursive Loops**.

---

## 4. The "Multi-Modal Visual Audit" Loop
Add an image-generation and "Visual Reflection" step to the final output.

* **The Loop:** Once the plan is ready, a **Visual Agent** generates an image of the plated meal. A **Vision-Reflector** then analyzes that image to ensure it looks appetizing and matches the ingredients (e.g., "The plan says Salmon, but the image shows Whitefish—there is a discrepancy in the model's internal representation").
* **The Sophistication:** This adds a layer of "Cross-Modal Validation."
* **Concept Taught:** **Multimodal Reasoning** and **Vision-Language Model (VLM) Loops**.



---

### **Updated WhatsApp Blurb for Students:**
*🚀 LEVEL UP: AGENTIC ENHANCEMENTS 🚀*

We aren't just building a planner; we’re building a **Self-Evolving System**. New features we'll be adding:

🧠 **Experience Memory:** The AI "remembers" past budget failures so it doesn't repeat them.
👺 **Red-Teaming:** A "Saboteur" agent will try to trick the safety checker to ensure 100% allergy security.
🛠️ **Tool Synthesis:** If the AI doesn't have a tool, it will *write the code* to build one on the fly.
👁️ **Visual Audit:** Using Vision models to "look" at the meal and verify it matches the recipe.
