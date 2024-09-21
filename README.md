
```markdown
# A* Search Algorithm for Shortest Path Between Cities

## Table of Contents
- [Overview](#overview)
- [How A* Works](#how-a-works)
- [File Structure](#file-structure)
- [Input Data](#input-data)
  - [cities.csv](#citiescsv)
  - [roads.csv](#roadscsv)
- [How to Run the Code](#how-to-run-the-code)
- [Output](#output)
- [Example Files](#example-files)
- [Requirements](#requirements)

## Overview
This repository contains an implementation of the A* Search Algorithm designed to find the shortest path between two cities using geographical data. The algorithm leverages the haversine distance as a heuristic function, allowing for efficient pathfinding.

## How A* Works
The A* algorithm operates by combining:
- **Actual Cost** to reach a node \( g(n) \)
- **Heuristic Estimate** of the cost to the goal \( h(n) \), calculated using the haversine distance.

This combination enables A* to efficiently explore paths and find the shortest route between cities.

## File Structure
```
/your-repo
│
├── astar.py           # Python implementation of the A* algorithm
├── cities.csv        # City names with latitude and longitude
└── roads.csv         # Direct connections between cities
```

## Input Data
### cities.csv
Each row represents a city, formatted as follows:
```
CityName, Latitude, Longitude
```

### roads.csv
Each row represents a direct connection between two cities, formatted as:
```
City1, City2
```

## How to Run the Code
1. Clone the repository or download the files.
2. Ensure `cities.csv` and `roads.csv` are in the same directory as `astar.py`.
3. Execute the program via the command line using the syntax:
   ```bash
   python astar.py <start_city> <goal_city>
   ```
   **Example:**
   ```bash
   python astar.py Dalhart San_Antonio
   ```

## Output
The program will display the shortest path and the total distance in kilometers:
```
Dalhart - Amarillo - Lubbock - San Angelo - San Antonio
Total Distance: [Some Number] km
```
If no path is found, the output will be:
```
Path not found!
```

## Example Files
### cities.csv
```csv
Dalhart, 36.0609, -102.5202
Amarillo, 35.2218, -101.8313
San_Antonio, 29.4241, -98.4936
```

### roads.csv
```csv
Dalhart, Amarillo
Amarillo, Lubbock
Lubbock, San_Angelo
San_Angelo, San_Antonio
```

## Requirements
- **Python Version:** 3.x
- **Libraries:** 
  - `math`
  - `heapq`
  - `csv`
  - `sys`

```