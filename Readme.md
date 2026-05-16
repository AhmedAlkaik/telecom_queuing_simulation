# Telecommunications Queuing Analysis (M/M/c)

This repository contains the computational implementation of a discrete-event telecommunications system modeled as a continuous-time Markovian queuing process ($M/M/c$). 

This project was developed to evaluate a strict Service Level Agreement (SLA) boundary condition: $P(W \le 1 \text{ minute}) \ge 0.90$ using historical operational data.

## 📊 Project Overview
The analysis extracts empirical systemic parameters ($\lambda$ and $\mu$) during peak-hour intervals to evaluate a baseline configuration of 4 parallel servers. Numerical integration via the composite Simpson's 1/3 rule is applied to the continuous exponential probability density function (PDF) to calculate exact SLA compliance probabilities.

* **Baseline Result ($c=4$):** 42.22% Compliance (System Failure)
* **Optimized Result ($c=6$):** 96.50% Compliance (System Success)

## 🗂️ Repository Structure
* `/data/`: Contains the raw simulation dataset (`simulated_call_centre.csv`).
* `/notebooks/`: Contains the Jupyter Notebook (`queue_simulation.ipynb`) with the Erlang C algorithms and SciPy numerical integration logic.

## 🚀 Reproducing the Study
To run the simulation locally, ensure you have Python 3.9+ installed.

1. Clone the repository:
   ```bash
   git clone [https://github.com/YourUsername/telecom-queuing-simulation.git](https://github.com/YourUsername/telecom-queuing-simulation.git)

Install the required mathematical dependencies:

Bash
pip install -r requirements.txt

Launch Jupyter and open the notebook:

Bash
jupyter notebook notebooks/queuing_theory.ipynb

⚖️ License
This project is licensed under the MIT License - see the LICENSE file for details.
