# Workshop 3: System Architecture Refinement & Project Management 


## Overview
This workshop focuses on transforming the logical model defined in Workshop 2 into a **robust, deployable engineering architecture**.

The primary objective was to address the system's "Constraints" and "Sensitivity" through specific architectural layers, aligned with **ISO 25010** quality standards. Additionally, a structured Project Management Plan was established using Agile methodologies to guide the development process.

---

## Architectural Evolution
The system design was refined from a simple Input-Process-Output model to a layered architecture focusing on robustness:

### 1. Reliability Layer (ISO 25010)
* **Goal:** Shield the system from "dirty" data and missing values.
* **Implementation:** Added specific modules for **Data Validation**, **Imputation** (handling missing Age/Cabin), and **Outlier Management**.
* **Impact:** Ensures that the core processing logic only receives stable, clean data.

### 2. Maintainability & Scalability Layer
* **Goal:** Ensure the system can evolve without breaking.
* **Implementation:** Decoupled the processing block into independent micro-services:
    * *Textual Processing* (Names/Titles).
    * *Numeric Processing* (Binning).
    * *Group Processing* (Family creation).
* **Standard:** Aligned with **CMMI** principles for modularity.

### 3. Usability Layer
* **Goal:** Make the output interpretable for the end-user.
* **Implementation:** The system outputs not just a binary prediction, but also **Confidence Metadata** to provide context on the certainty of the result.

---

## Project Management Plan
To ensure the successful delivery of the system, the team adopted an **Agile-inspired workflow** supported by a Kanban board.

### Team Roles
* **Project Manager:** Andrés Camilo Ramos
* **System Analyst:** Julián Carvajal
* **Data Engineer:** Jhonatan Moreno
* **ML Developer:** Andrés Cepeda
* **QA Tester:** All Members

### Risk Analysis
A comprehensive risk assessment was conducted (aligned with **ISO 9000**), identifying potential failure points such as:
* Data Quality Issues (Missing values).
* Model Sensitivity (Overfitting).
* Pipeline Failure (Service interruptions).

---

## Contents

| File | Description |
| :--- | :--- |
| `Workshop3.pdf` | **Full Report.** detailed documentation of the architecture, risk analysis, and project timeline. |
| `architecture_diagram.png` | Visual representation of the refined Reliability, Maintainability, and Usability layers. |
| `Workflow and Timeline Diagram.png` | Project timeline and Kanban structure diagram. |
