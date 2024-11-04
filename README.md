# Optimal Stop Calculation for Autonomous Unmanned Ground and Air Vehicles in Harvest Optimization

This repository contains the code and research paper for the project "Smart Agriculture with Autonomous Unmanned Ground and Air Vehicles: Approaches to Calculating Optimal Number of Stops in Harvest Optimization." This study explores optimization techniques using autonomous UAVs and UGVs to reduce harvest time by determining the optimal number of stops in an agricultural field.

## Table of Contents

- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Results](#results)
- [Citation](#citation)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Introduction

This project leverages robotics and optimization techniques to address efficiency in agriculture. Specifically, it utilizes autonomous Unmanned Ground Vehicles (UGVs) and Unmanned Aerial Vehicles (UAVs) to minimize the time required for harvesting operations. Using Particle Swarm Optimization (PSO), K-Means clustering, and heuristic algorithms, the study determines optimal stop locations for UGVs and UAVs to collect crops efficiently.

This work was published in a chapter titled "Smart Agriculture with Autonomous Unmanned Ground and Air Vehicles: Approaches to Calculating Optimal Number of Stops in Harvest Optimization" and provides insights into autonomous agricultural systems.

## Project Structure

The repository contains the following files:

Smart_Agriculture_Optimal_Stops/
├── docs/
│   └── Smart-Agriculture-With-Autonomous-Unmanned-Ground-and-Air-Vehicles.pdf  # Research paper
├── src/
│   └── Optimal Number of Stops UAV.jl                                          # Julia code for the optimization model
├── README.md                                                                   # Project documentation
└── LICENSE                                                                     # License information



- **docs/**: Contains the research paper for reference.
- **src/**: Contains the Julia script for running the optimization model.
- **README.md**: Detailed instructions and documentation for the project.

## Installation

To run the code, you will need [Julia](https://julialang.org/) and several specific packages. Follow these steps to set up the environment:

1. **Install Julia**:
   - Download and install Julia from [https://julialang.org/downloads/](https://julialang.org/downloads/).

2. **Install Required Julia Packages**:
   - Open the Julia REPL (Read-Eval-Print Loop) and install the required packages by running the following commands:
     ```julia
     using Pkg
     Pkg.add("JuMP")
     Pkg.add("Clustering")
     Pkg.add("Distances")
     Pkg.add("Gurobi") # Note: Gurobi requires a license (see instructions below).
     ```
   - **Gurobi License**:
     - Download Gurobi from [https://www.gurobi.com/](https://www.gurobi.com/).
     - Obtain a license (free academic or commercial).
     - Follow the instructions to set up and activate the Gurobi license.

## Usage

1. **Clone the Repository**:
   - In a terminal, clone this repository and navigate to the `src` directory:
     ```bash
     git clone https://github.com/yourusername/Smart_Agriculture_Optimal_Stops.git
     cd Smart_Agriculture_Optimal_Stops/src
     ```

2. **Run the Julia Code**:
   - Open Julia in the `src` directory and run the script:
     ```julia
     include("Optimal Number of Stops UAV.jl")
     ```
   - The script will compute the optimal stop locations and output the total harvest time for the UAVs and UGVs.

## Methodology

This study involves a multi-stage optimization model that uses:
1. **K-Means Clustering**: To determine optimal stop locations for UGVs.
2. **Heuristic TSP Algorithms**: Including Nearest Neighbor and 2-Opt, for route optimization of UGVs.
3. **Binary Mixed Integer Programming**: For assigning tasks to UAVs.
4. **Particle Swarm Optimization (PSO)**: To find the minimum harvest time based on the computed stops.

The model calculates the time UAVs and UGVs spend on each stop, aiming to minimize the total time spent during harvest.

## Results

The model was tested with a sample of 500 apples, resulting in the following optimal values:
- **Number of Optimal Stops**: 42
- **Total Harvest Time**: Approximately 228.25 minutes

These findings demonstrate that optimized stop locations significantly reduce harvest time, validating the effectiveness of the proposed model.

## Citation

If you use this work in your research, please cite it as follows:

Güzey, A., Akinci, M.M., & Guzey, H.M. (2020). Smart Agriculture with Autonomous Unmanned Ground and Air Vehicles: Approaches to Calculating Optimal Number of Stops in Harvest Optimization. In Artificial Intelligence and IoT-Based Technologies for Sustainable Farming and Smart Agriculture. DOI: 10.4018/978-1-7998-1722-2.ch010


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

This research was supported by the European Union and TUBITAK under Project Number 217E138. Special thanks to all contributors who made this study possible.

