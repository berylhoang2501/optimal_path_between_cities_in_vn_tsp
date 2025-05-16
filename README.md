# Optimal Path Between Cities in Vietnam (TSP)

This project solves the **Traveling Salesman Problem (TSP)** for a set of cities in Vietnam, aiming to find the shortest route that visits each city exactly once and returns to the starting point. The solution uses a **simulated annealing** algorithm from the `python-tsp` library and visualizes the optimal path on an interactive map using Plotly.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [License](#license)

## Project Overview
The **Traveling Salesman Problem (TSP)** is a classic optimization challenge with applications in logistics and transportation. This project applies TSP to a dataset of 32 major cities in Vietnam, using their geographic coordinates to compute the shortest possible route.

**Objectives**:
- Find an optimal route connecting major cities in Vietnam.
- Visualize the route on an interactive map.
- Provide a scalable solution for logistics and route planning.

**Methodology**:
- Load and preprocess city data (names, latitudes, longitudes).
- Create a distance matrix using the great circle distance formula.
- Apply simulated annealing to find an approximate optimal path.
- Visualize the path using Plotly's interactive maps.

## Dataset
The dataset contains information about 32 major cities in Vietnam:
- `vn_data.py`: A Python file listing city names, latitudes, and longitudes.

**Note**: Due to data sensitivity, the dataset is not included in the repository. Contact me for access or provide your own dataset with a similar structure (city name, latitude, longitude).

## Installation
1. Clone the repository:

```
git clone https://github.com/berylhoang2501/Optimal-Path-Vietnam-TSP.git
cd Optimal-Path-Vietnam-TSP
```

2. Create a virtual environment and install dependencies

```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

## Usage

Run the Python script to compute and visualize the optimal path:

```
python scripts/optimal_path_between_cities_in_vn_tsp.py
```

## Results

- **Optimal Path:**

The simulated annealing algorithm computes an approximate shortest path connecting 32 cities in Vietnam.

The total distance of the path is output in kilometers (varies based on the dataset).

The path is visualized on an interactive map, showing the order of cities visited.

<img width="375" alt="Ảnh màn hình 2025-05-16 lúc 15 42 26" src="https://github.com/user-attachments/assets/89dfc7d0-31c3-4f04-8e3a-ef9f7b8170f2" />

<img width="410" alt="Ảnh màn hình 2025-05-16 lúc 15 43 02" src="https://github.com/user-attachments/assets/ce7e04e5-7c71-4349-ab76-814c71a9d2bc" />

- **Key Findings:**


Simulated annealing provides a high-quality solution but does not guarantee the absolute shortest path due to its heuristic nature.

The great circle distance matrix ensures accurate geographic distances between cities.

The solution is computationally efficient for small to medium datasets (e.g., 32 cities).

- **Limitations:**

For larger datasets, exact algorithms (computing all permutations) are infeasible due to factorial complexity.

The dataset is limited to 32 cities; expanding to more cities may require additional memory optimization.

- **Applications:**

Logistics: Optimize delivery routes for transportation companies.

Tourism: Plan efficient travel itineraries across Vietnam.



