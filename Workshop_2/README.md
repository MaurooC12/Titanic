# Workshop 2: System Design & Requirements Engineering 

## Overview
This workshop marks the transition from systemic analysis to **Engineering Design**. Building upon the findings of Workshop 1, we translated the Titanic dataset's characteristics into a formal **System Architecture** and a set of strict **Engineering Requirements**.

The goal was to design a system capable of handling the identified "Constraints" (missing data) and "Sensitivity" (nonlinear variable impact) while adhering to **ISO 25010** software quality standards.

---

## System Requirements
We derived functional and non-functional requirements directly from the dataset's internal structure:

### Functional Requirements (System Behavior)
* **R1 - Handling Missing Data (Reliability):** Robust imputation mechanisms for `Age` and `Cabin` to prevent system instability.
* **R2 - Consistent Categorical Processing:** Deterministic encoding for variables like `Sex` and `Embarked` to ensure reproducibility.
* **R3 - Sensitivity Management:** Stable transformations for high-impact variables (e.g., Sex, Pclass) to avoid amplifying small perturbations.
* **R4 - Feature Interaction Support:** Capability to engineer complex features (e.g., `FamilySize`) that reflect internal group structures.

### User-Centric Requirements
* **U1 - Interpretability:** The system must provide confidence metadata, not just binary predictions, to help users understand the result.
* **U3 - Reproducibility:** All preprocessing steps must be versioned to allow consistent replication of results.

---

## High-Level Architecture
The system is structured into three distinct layers to ensure modularity and fault tolerance:

### 1. Reliability Layer (Data Integrity)
* Acts as the system's "shield" against chaos.
* **Modules:** Data Validation, Imputation Module, and Outlier Management.

### 2. Maintainability & Scalability Layer (Core)
* Decouples transformation logic to allow independent updates.
* **Modules:** Text Processing (Titles), Numeric Binning, and Group Processing.

### 3. Usability Layer (Output)
* Ensures results are meaningful to the user.
* **Modules:** Classification Logic and Confidence Metadata generation.

---

## Handling Chaos & Sensitivity
Strategies designed to mitigate the systemic risks identified in Workshop 1:
* **Feedback Monitoring:** Continuous evaluation of model performance to detect drift.
* **Robust Preprocessing:** Normalization pipelines to limit the "Butterfly Effect" of small input changes.
* **Model Ensembles:** Using multiple models to reduce the variance caused by chaotic data patterns.

---

## Technical Stack
The selected tools support the modular and reproducible design:
* **Language:** Python 3.8+
* **Data Processing:** Pandas & NumPy (Data Layer)
* **Modeling:** Scikit-learn (Preprocessing & Modeling Layer)
* **Visualization:** Matplotlib/Seaborn (Evaluation Layer)
* **Version Control:** Git/GitHub (Traceability)

---

## Contents

| File | Description |
| :--- | :--- |
| `Workshop-2.pdf` | **Full Design Report.** Detailed documentation of requirements, architectural diagrams, and sensitivity mitigation strategies. |
| `architecture_diagram_corrected.png` | Visual representation of the Reliability, Maintainability, and Usability layers. |
