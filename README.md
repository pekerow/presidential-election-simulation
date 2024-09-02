# U.S. Presidential Election Simulation

This repository contains a Python-based Monte Carlo simulation designed to model the outcomes of U.S. presidential elections. The simulation leverages state-level electoral data and the Partisan Voting Index (PVI) to probabilistically determine the results of each state's electoral votes over 10,000 simulated elections.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [How It Works](#how-it-works)
- [Requirements](#requirements)
- [Usage](#usage)
- [Output](#output)
- [Visualizations](#visualizations)
- [License](#license)

## Introduction

The goal of this project is to simulate the U.S. presidential election using probabilistic methods. This simulation runs 10,000 iterations of the election to estimate the likelihood of each candidate winning based on state-level Partisan Voting Index (PVI) values. Each state is treated as an independent event, and its probability of going for either candidate is calculated based on historical voting trends and the PVI.

The simulation uses state-level electoral vote distributions based on the 2020 U.S. census and adjusts the likelihood of each candidate winning each state using the state’s PVI score. The simulation provides insights into how competitive states influence the final election outcome.

## Features

- **Monte Carlo Simulation**: Simulates 10,000 possible U.S. presidential election outcomes.
- **Dynamic Probabilities**: Each state's outcome is determined by its PVI value, adjusting probabilities based on the state's leaning.
- **Electoral Vote Distribution**: Allocates electoral votes based on the results of each state.
- **Customizable Simulation Parameters**: Adjust the number of simulations or the PVI scores to analyze different election scenarios.
- **Results Visualization**: Generates multiple plots including bar plots, density plots, cumulative distribution functions (CDF), and histograms to visualize the distribution of electoral votes and margins.

## How It Works

1. **State-Level Data**: Each state is assigned a number of electoral votes based on the 2020 census and a Partisan Voting Index (PVI) score. The PVI indicates how much a state leans toward one party, with positive values favoring Republicans (Trump) and negative values favoring Democrats (Harris).

2. **Adjusted Probabilities**: The probability of each candidate winning a state is adjusted based on the state’s PVI. Solidly red or blue states have very high probabilities for their respective parties, while swing states have probabilities closer to 50/50.

3. **Monte Carlo Simulation**: The election is simulated 10,000 times. In each simulation, the outcome of each state is randomly determined based on the calculated probabilities, and the electoral votes are tallied for each candidate.

4. **Results Analysis**: The simulation tracks how many times each candidate wins the overall election (i.e., receives 270 or more electoral votes) and saves the results to a CSV file for further analysis.

5. **Visualization**: Various plots are generated to visualize the outcomes, including:
    - **Bar Plot**: Displays the total number of victories for Trump and Harris across all simulations.
    - **Density Plot**: Visualizes the distribution of electoral votes for each candidate.
    - **Cumulative Distribution Function (CDF)**: Shows the cumulative probability of electoral votes for each candidate.
    - **Electoral Vote Margin Histogram**: Illustrates the distribution of electoral vote margins across all simulations.

A Canva document with plots reporting on the results of one particular simulation can be viewed [here](https://www.canva.com/design/DAGPK3WzI70/VorPrV2s0f3tfbWqSRX-yQ/edit?utm_content=DAGPK3WzI70&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton).

## Requirements

- Python 3.x
- Required packages:
  - `numpy`
  - `pandas`
  - `seaborn`
  - `matplotlib`

You can install the required packages using pip:

```bash
pip install numpy pandas seaborn matplotlib
```

## Usage

1. Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/election-simulation.git
cd election-simulation
```

2. Open the Jupyter or Colab notebook:

   - If using Jupyter Notebook:
     ```bash
     jupyter notebook election_sim.ipynb
     ```
   - If using Google Colab, upload the notebook (`election_sim.ipynb`) directly to Colab.

3. Run the cells sequentially to execute the election simulation and generate the plots.

## Output

- **CSV File**: Contains the results of all 10,000 simulations, including the total number of electoral votes won by each candidate and the outcome of each state's electoral votes in each simulation.
- **Visualizations**: 
  - **Bar Plot**: Displays the total number of victories for Trump and Harris across all simulations.
  - **Density Plot**: Shows the probability density of electoral votes for Trump and Harris.
  - **Cumulative Distribution Function (CDF)**: Illustrates the cumulative probability of electoral votes for each candidate.
  - **Electoral Vote Margin Histogram**: Depicts the distribution of electoral vote margins across all simulations.

Here is an example of the output CSV structure:

| Trump | Harris | States                                                                 |
|-------|--------|------------------------------------------------------------------------|
| 305   | 233    | {'Alabama': 'Trump', 'Alaska': 'Trump', 'Arizona': 'Harris', ...}      |
| 270   | 268    | {'Alabama': 'Trump', 'Alaska': 'Harris', 'Arizona': 'Trump', ...}      |
| ...   | ...    | ...                                                                    |

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---
