# Workshop 4: Kaggle System Simulation 

**System Analysis & Design Project** *Universidad Distrital Francisco José de Caldas*

## Overview
This folder contains the computational implementation of **Workshop 4**, focused on validating the System Architecture designed in previous workshops.

The objective is to explore the concepts of **Chaos** and **Sensitivity** within the Titanic system through two distinct simulation paradigms:
1.  **Data-Driven Simulation:** A Machine Learning model to measure variable sensitivity.
2.  **Event-Based Simulation:** A Cellular Automata model to visualize emergent spatial behavior.

---

## Contents

| File | Description |
| :--- | :--- |
| `Workshop4_Sim.ipynb` | **Main Jupyter Notebook**. Contains the complete Python code for data cleaning, modeling, and simulation logic. |
| `Workshop4_Report.pdf` | **Final Simulation Report**. A comprehensive PDF document analyzing the results, methodology, and architectural validation. |
| `requirements.txt` | List of Python dependencies required to run the simulation. |
| `*.png` | Generated artifacts (Sensitivity plots, Automata grids) used in the report. |

---

## Simulation Scenarios

### 1. The Reliability Layer (Data Preparation)
Before simulation, the raw data passes through the **Reliability Layer** designed in Workshop 3.
* **Action:** Imputation of missing *Age* values (using median) and *Embarked* (mode).
* **Result:** A stabilized dataset with 0 missing values, preventing system crashes during execution.

### 2. Scenario 1: Data-Driven Simulation (Random Forest)
* **Type:** Machine Learning (Supervised).
* **Model:** Random Forest Classifier (`n_estimators=100`).
* **Objective:** To quantify the "Sensitivity" of the system.
* **Key Finding:** The system is highly sensitive to **Fare** and **Sex**. Small changes in these variables trigger the largest shifts in survival probability.
* **Accuracy:** ~83% on validation data.

### 3. Scenario 2: Event-Based Simulation (Cellular Automata)
* **Type:** Agent-Based Modeling / Cellular Automata.
* **Grid:** 20x20 spatial representation of the ship.
* **Logic:** Agents attempt to move "Up" towards safety. Movement priority is assigned based on Ticket Class ($P_{Class1} > P_{Class3}$).
* **Emergent Behavior:** Without explicit programming, Class 1 agents naturally formed a blockade, trapping Class 3 agents at the bottom of the grid. This visualizes the physical manifestation of the system's bias.

---

## How to Run

To reproduce the simulations locally, follow these steps:

1.  **Clone the repository** (if you haven't already):
    ```bash
    git clone [https://github.com/YourUsername/Titanic.git](https://github.com/YourUsername/Titanic.git)
    cd Titanic/Workshop_4_Simulation
    ```

2.  **Install Dependencies:**
    It is recommended to use a virtual environment.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook Workshop4_Sim.ipynb
    ```

4.  **Execute All Cells:**
    Run the cells sequentially to perform data ingestion, cleaning, model training, and automata visualization.

---

## Dependencies
* Python 3.8+
* `pandas` - Data manipulation
* `numpy` - Matrix operations
* `matplotlib` & `seaborn` - Visualization
* `scikit-learn` - Machine Learning models
