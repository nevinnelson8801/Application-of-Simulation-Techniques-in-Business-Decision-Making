# 🚚 Yellowstone Inc. — Simulation Portfolio

## 📋 Overview

This project presents a comprehensive simulation and process modelling portfolio developed for **Yellowstone Inc.**, a logistics company specialising in reliable and fast package delivery services. The assignment demonstrates how simulation techniques, modelling tools, and analytical methods can support operational decision-making in modern logistics environments.

The project was completed entirely using **Google Colab** with Python-based simulation and visualisation tools.

The report explores:

* 📦 Delivery time prediction under uncertain traffic conditions
* 🎲 Monte Carlo simulation and random number generation
* 📊 Data visualisation for logistics analytics
* ♟️ Game theory and payoff table analysis
* 🔄 Petri nets for process modelling
* 🧩 UML use case modelling for logistics systems

The overall objective of the project is to demonstrate how simulation can improve efficiency, reduce operational uncertainty, and support strategic planning within a logistics organisation.

---

# 🗂️ Repository Structure

```text
yellowstone-simulation-portfolio/
│
├── notebooks/
│   └── Untitled0.ipynb              # Google Colab notebook containing simulations and analysis
│
├── report/
│   └── yellowstone_report.docx      # Full academic assignment report
│
├── visualizations/
│   ├── monte_carlo_histogram.png    # Delivery time distribution charts
│   ├── payoff_table.png             # Game theory payoff matrix
│   ├── petri_net_diagram.png        # Petri net process model
│   └── uml_use_case.png             # UML use case diagram
│
├── data/
│   └── simulated_delivery_data.csv  # Simulated logistics data generated in Colab
│
└── README.md
```

---

# 🧱 Project Components

## 1️⃣ Simulation Fundamentals

The project begins with a theoretical explanation of simulation and its role in logistics and operations management.

### Simulation Types Discussed

| Simulation Type                 | Purpose                                   | Logistics Application         |
| ------------------------------- | ----------------------------------------- | ----------------------------- |
| Discrete-Event Simulation (DES) | Models events occurring at specific times | Warehouse operations          |
| Continuous Simulation           | Models continuously changing systems      | Fuel consumption tracking     |
| Agent-Based Simulation (ABS)    | Models independent interacting agents     | Driver and customer behaviour |
| Monte Carlo Simulation          | Uses random sampling for prediction       | Delivery time estimation      |
| System Dynamics                 | Models feedback-based systems             | Supply chain performance      |

---

## 2️⃣ Monte Carlo Simulation

A Monte Carlo simulation model was developed in Google Colab to predict package delivery times under uncertain traffic conditions.

### Simulation Assumptions

* Delivery Time Distribution:

genui{"math_block_widget_always_prefetch_v2":{"content":"T \sim N(\mu = 30,\sigma = 5)"}}

* Number of simulation runs: 10,000
* Random sampling generated using NumPy
* Visualisation performed using Matplotlib

### Key Results

| Metric                               | Value         |
| ------------------------------------ | ------------- |
| Mean Delivery Time                   | 29.99 minutes |
| Standard Deviation                   | 5.02 minutes  |
| Minimum Delivery Time                | 10.39 minutes |
| Maximum Delivery Time                | 49.63 minutes |
| 95th Percentile                      | 38.21 minutes |
| Probability of Delivery > 40 Minutes | 2.37%         |

### Business Insights

* Most deliveries are completed within the expected SLA target.
* Approximately 2.37% of deliveries exceed 40 minutes.
* The simulation helps Yellowstone Inc. estimate operational risk before real-world implementation.

---

# 🎲 Random Number Generation

Random numbers were used to simulate uncertain logistics behaviour including:

* Variable traffic conditions
* Random customer demand
* Vehicle delays
* Delivery duration variability

The project discusses the Linear Congruential Generator (LCG) method:

genui{"math_block_widget_always_prefetch_v2":{"content":"X_{n+1}=(aX_n+c)\bmod m"}}

The simulation itself used NumPy's random number generation functions available in Python through Google Colab.

---

# ♟️ Game Theory Analysis

A payoff table was developed to analyse strategic route selection between Yellowstone Inc. and a competing logistics company.

## Strategies

* Standard Route (S)
* Express Route (E)

| Yellowstone / Competitor | Standard (S) | Express (E) |
| ------------------------ | ------------ | ----------- |
| Standard (S)             | (5,5)        | (3,8)       |
| Express (E)              | (8,3)        | (6,6) ★     |

### Nash Equilibrium

The dominant strategy equilibrium occurs at:

**(Express, Express) = (6,6)**

This result demonstrates that both companies achieve the most stable and profitable outcome by selecting the Express strategy.

---

# 🔄 Petri Net Process Modelling

Petri nets were used to model Yellowstone Inc.’s package delivery workflow.

## Process Stages

1. Order Received
2. Sort Package
3. Load Vehicle
4. Dispatch Vehicle
5. Complete Delivery

### Petri Net Components

| Component   | Description                    |
| ----------- | ------------------------------ |
| Places      | Represent delivery states      |
| Transitions | Represent logistics activities |
| Tokens      | Represent package movement     |
| Arcs        | Represent workflow direction   |

### Key Findings

* Bottlenecks can be identified during sorting operations.
* Parallel activities can be modelled effectively.
* Petri nets provide a formal way to analyse logistics workflows.

---

# 🧩 UML System Design

A UML Use Case Diagram was created to model interactions within the package tracking system.

## Main Actors

| Actor                | Role                                       |
| -------------------- | ------------------------------------------ |
| Customer             | Tracks packages and receives notifications |
| Delivery Driver      | Updates delivery status                    |
| Warehouse Staff      | Scans and assigns packages                 |
| System Administrator | Manages reports and accounts               |
| Notification Service | Sends SMS/Email alerts                     |

## UML Concepts Used

* «include» relationships for mandatory notifications
* «extend» relationships for conditional delay alerts
* Use case modelling for requirement analysis

---

# 💻 Technologies Used

| Tool / Technology | Purpose                    |
| ----------------- | -------------------------- |
| Google Colab      | Development environment    |
| Python            | Simulation programming     |
| NumPy             | Random number generation   |
| Matplotlib        | Data visualisation         |
| Pandas            | Data handling and analysis |
| UML Modelling     | System design              |
| Petri Nets        | Process modelling          |

---

# 🚀 Getting Started

## Prerequisites

* Google account
* Google Colab access
* Basic Python knowledge

## Running the Project

### 1. Open Google Colab

Upload the notebook file:

```text
Untitled0.ipynb
```

### 2. Install Required Libraries

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

### 3. Run the Simulation Cells

Execute all notebook cells sequentially to:

* Generate random delivery times
* Run Monte Carlo simulations
* Produce visualisations
* Analyse logistics performance

---

# 📈 Key Outcomes

| Performance Area            | Result                                |
| --------------------------- | ------------------------------------- |
| Delivery Risk Estimation    | Achieved using Monte Carlo simulation |
| Operational Analysis        | Improved using Petri nets             |
| Strategic Decision Support  | Demonstrated with game theory         |
| System Design Understanding | Enhanced using UML                    |
| Data Visualisation          | Implemented with Python libraries     |

---

# 🔍 Key Concepts Demonstrated

* Monte Carlo Simulation
* Probability Distributions
* Random Number Generation
* Data Visualisation
* Nash Equilibrium
* Petri Net Modelling
* UML Use Case Design
* Logistics Process Analysis
* Simulation-Based Decision Making

---

# 📚 References

* Banks, J., Carson, J.S., Nelson, B.L. and Nicol, D.M. (2010) *Discrete-Event System Simulation*. 5th edn. Prentice Hall.
* Law, A.M. (2015) *Simulation Modeling and Analysis*. 5th edn. McGraw-Hill.
* Nash, J. (1950) 'Equilibrium points in n-person games', *Proceedings of the National Academy of Sciences*, 36(1), pp. 48-49.
* Peterson, J.L. (1977) 'Petri nets', *ACM Computing Surveys*, 9(3), pp. 223-252.
* Rossetti, M.D. (2015) *Simulation Modeling and Arena*. 2nd edn. Wiley.
* Fowler, M. (2004) *UML Distilled: A Brief Guide to the Standard Object Modelling Language*. 3rd edn. Addison-Wesley.

