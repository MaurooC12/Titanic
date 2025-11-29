# Workshop 1: Systems Engineering Analysis 

## Overview
This workshop establishes the conceptual foundation of the project. Instead of immediately applying predictive algorithms, we analyzed the Kaggle Titanic dataset from a **Systems Engineering perspective**.

The dataset was defined as a **closed system** where passenger attributes serve as inputs that interact through internal rules (social norms, physical constraints) to produce a binary output (Survival). This stage focused on identifying the system's boundaries, constraints, and inherent complexity.

---

## System Definition
We mapped the dataset features to standard system components:

### 1. Inputs (System Elements)
The raw attributes defining each unit (passenger) within the system:
* **Demographic:** `Sex`, `Age`.
* **Socioeconomic:** `Pclass`, `Fare`.
* **Social Grouping:** `SibSp`, `Parch` (Family structure).
* **Logistic:** `Embarked`, `Cabin`, `Ticket`.

### 2. Processes (Internal Logic)
Observable transformations and interactions strictly within the data:
* **Stratification:** The interaction between *Pclass* and *Fare* defining status.
* **Grouping:** The combination of *SibSp* and *Parch* forming family units.

### 3. Output (System State)
* **Target Variable:** `Survived` (0 or 1).
* **Nature:** An emergent result of the interaction between the inputs.

---

## Complexity, Chaos & Sensitivity
A critical part of this workshop was identifying why the system is difficult to model:

### System Constraints
* **Missing Data:** Significant gaps in `Age` and `Cabin` introduce uncertainty and instability.
* **Rigidity:** The system is limited to a fixed set of variables, requiring interpretation of categorical data.

### Sensitivity Analysis
We observed that the system is **highly sensitive to initial conditions**:
* Small modifications to *Age* or *Sex* inputs can drastically shift the survival outcome.
* Minor changes in *Pclass* affect multiple related behaviors (Fare distribution, Embarkation point).

### Chaotic Behavior
* **Outliers:** High-fare passengers in lower classes (and vice-versa) represent system anomalies.
* **Non-linearity:** Variables interact in non-additive ways (e.g., the survival rate of a "Male" changes entirely depending on "Age" and "Class").

---

## Contents

| File | Description |
| :--- | :--- |
| `Workshop-1.pdf` | **Full Analysis Report.** Detailed breakdown of system elements, relations, and complexity analysis. |
| `architecture_diagram_corrected.png` | Visual representation of the Input-Process-Output logical flow. |
