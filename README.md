# System Analysis & Design Project — Kaggle Titanic Case Study

---

## Overview

This repository documents the academic development of the *Systems Analysis & Design* course at **Universidad Distrital Francisco José de Caldas**.

The project uses the Kaggle competition **“Titanic: Machine Learning from Disaster”** as a case study to apply systems thinking. Moving beyond simple predictive modeling, this project treats the dataset as a **closed system**, analyzing its internal constraints, sensitivity, and emergent behaviors through strictly engineered architecture and simulation.

---

## Project Structure

### Workshop 1 — Systems Engineering Analysis
**Focus:** Systemic Understanding & Chaos Theory  
This initial stage analyzes the Titanic dataset as a logic system. It identifies key **inputs, processes, and outputs**, while characterizing the system's **constraints** (e.g., missing data) and **sensitivity** (how small changes in *Age* or *Sex* drastically alter the outcome).
* **Key Concepts:** Nonlinear relationships, System boundaries, Sensitivity analysis.
* **Outcome:** Identification of "Chaos" sources (missing values, outliers).

> Detailed report available in: [`Workshop_1`](./Workshop_1)

---

### Workshop 2 — System Design and Requirements
**Focus:** Architecture & ISO 25010 Standards  
Based on the analysis, this phase translates insights into a formal **System Architecture**. We defined Functional and Non-Functional Requirements (R1-R6) and designed a modular architecture composed of three key layers:
1.  **Reliability Layer:** For data ingestion and imputation[cite: 77].
2.  **Maintainability Layer:** For modular feature engineering[cite: 83].
3.  **Usability Layer:** For interpretability of results[cite: 92].

> Requirements and Architecture specs in: [`Workshop_2`](./Workshop_2)

---

### Workshop 3 — Refinement & Project Management
**Focus:** Quality Assurance, Risk Analysis & Planning  
This workshop refined the architecture by implementing specific engineering modules to handle the identified chaos. It also introduced a **Project Management Plan** using Agile/Kanban methodologies and a **Risk Analysis** based on ISO 9000 to ensure process quality.
* **Key Concepts:** Fault Tolerance, Reliability Layer Implementation, Risk Mitigation.
* **Outcome:** A robust, deployable architecture design ready for simulation.

> Detailed refinement report in: [`Workshop_3`](./Workshop_3)

---

### Workshop 4 — Kaggle System Simulation 🚀
**Focus:** Computational Simulation & Validation  
The final stage validates the designed architecture through two distinct simulation scenarios, proving the system's ability to handle chaos and sensitivity.

#### Scenarios Implemented:
1.  **Scenario 1: Data-driven Simulation (Random Forest):**
    * Simulates the learning dynamics of the system.
    * **Result:** Validated that *Fare* and *Sex* are the highest sensitivity points in the system (Sensors).
2.  **Scenario 2: Event-based Simulation (Cellular Automata):**
    * Models the spatial dynamics of the evacuation on a 20x20 grid.
    * **Result:** Demonstrated **emergent behavior** where high-priority agents (Class 1) naturally block lower-priority agents, creating segregation patterns without explicit programming.

> **Source Code & Report:** [`Workshop_4_Simulation`](./Workshop_4_Simulation)

---

## Documentation

The `Documentation` folder contains complementary materials that support the system design and analysis process.  

It includes detailed technical reports, diagrams, datasets references, and visual documentation related to both workshops and the general system architecture.  

This section serves as a centralized space for project artifacts and supporting evidence used in the academic development of the Kaggle Titanic case study.



> 📄 Detailed report and specification of documentation files available within the folder [`Documentation`](./Documentation).

---

## Contributors

* **Julián Carvajal Garnica**
* **Andrés Mauricio Cepeda Villanueva**
* **Jhonatan David Moreno Barragán**
* **Andrés Camilo Ramos Rojas**

---

## 📜 License

This project is distributed under the **Apache License**.  
See the file [`LICENSE`](./LICENSE) for more details.
