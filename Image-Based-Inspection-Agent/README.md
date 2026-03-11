# Project Visual-Standard-Agent 🔍
### Precision Spatial Auditing & Adherence Intelligence

---

## 🎯 Purpose of The Project
In industries such as retail, logistics, and facilities management, "Order" is a direct proxy for operational efficiency and safety. **Visual-Standard-Agent** is an autonomous inspection system designed to enforce organizational standards by comparing a "Gold Standard Reference" image against live "Audit Images." 

The goal is to build an agent that doesn't just "see" pixels, but understands **spatial semantics**—identifying misplaced items, incorrect orientations, or layout violations, and providing a numerical adherence score with actionable corrective feedback.

---

## 🧠 Foundational Concepts & Enterprise Relevance
This project focuses on the core pillars of **Computer Vision (CV) and Spatial AI**:

* **Semantic Visual Diffing:** Moving beyond pixel-level subtraction to understand structural discrepancies (e.g., identifying that a car is "too far left" rather than just "different").
* **Zero-Shot Object Grounding:** Utilizing models like **OWL-ViT**, **Grounding DINO**, or **Florence-2** to detect and relate objects without requiring a custom-trained dataset for every new environment.
* **Perspective Correction & Homography:** Learning the geometry required to align images taken from different camera angles to a single "standard" coordinate system.
* **Automated Quality Assurance:** Replicating the high-value role of a human inspector with a scalable, 24/7 AI agent that reduces human error and operational costs.



---

## 🛠 Technical Requirements

### Phase 1: Reference Ingestion & Constraint Discovery
* **The "Standard" Encoder:** The agent must ingest a reference image and autonomously generate a **Spatial Policy Map** (JSON). This includes object classes, $(x, y)$ coordinates, and proximity relationships (e.g., "Item A must be 50px from Item B").
* **Constraint Derivation:** The agent must use a Vision-Language Model (VLM) to describe the "Rules" of the standard (e.g., "All labels must face forward," "No more than 3 units per row").

### Phase 2: The Inspection & Audit Loop
* **Spatial Alignment Engine:** Implement a pipeline to normalize the "Audit Image" (handling rotation, tilt, and zoom) so it matches the reference frame.
* **Discrepancy Detection:** Identify three types of violations:
    1. **Missing Items:** Elements in the standard not found in the audit.
    2. **Misplaced Items:** Correct items in the wrong spatial coordinates.
    3. **Orientation Errors:** Items rotated or flipped incorrectly.
* **Annotated Feedback:** The agent must output an image with **Bounding Box Overlays** and text bubbles suggesting specific movements (e.g., "Rotate 15° clockwise").

### Phase 3: Adherence Scoring & Reporting
* **The Scoring Algorithm:** Develop a weighted 1–10 scoring system. Points are deducted based on the severity of the violation (e.g., a safety violation in a parking lot deducts more than a minor alignment issue in a fridge).
* **Multi-Domain Deployment:** Test the agent on three distinct scenarios:
    1. **Parking Lot:** Alignment within lines and unauthorized vehicle detection.
    2. **Retail/Grocery Shelf:** "Planogram" compliance and facing accuracy.
    3. **Refrigerator/Storage:** Organizational order and proximity rules.

---

## 📜 Rules of Engagement (First-Principles Learning)

1. **Zero-Manual Labeling:** Interns are **forbidden** from manually defining the "rules" for the standard. The Agent must "look" at the reference image and generate the ruleset autonomously.
2. **Local LVM Mastery:** All analysis must be performed using local vision models (e.g., **InternVL-Chat** or **LLaVA**) to demonstrate data sovereignty and low-latency auditing.
3. **Reasoning-First Feedback:** The agent cannot just say "Error." It must explain **why** it's an error based on the reference standard (e.g., "The Audit shows Item C is missing, which breaks the symmetrical pattern of the Standard").
4. **IDE Constraint:** The project must be developed entirely using **Cursor** or **Antigravity**, specifically using the AI's ability to debug complex spatial coordinate math.

---

## 📊 Evaluation & Grading Criteria

| Metric | Goal | Description |
| :--- | :--- | :--- |
| **Object Recall** | > 95% | Frequency of correctly identifying all items from the reference in the audit image. |
| **Spatial Precision** | < 10% Margin | The accuracy of the suggested corrective movement (e.g., "Move 1 inch left"). |
| **Scoring Variance** | < 0.5 points | Consistency of the 1–10 rating across different audit images of the same quality level. |
| **Alignment Stability**| Robust | Ability to correctly align audit images taken from up to 30 degrees off-axis. |
| **Processing Speed** | < 5.0 seconds | The time from "Audit Upload" to the generation of the annotated feedback. |

---
