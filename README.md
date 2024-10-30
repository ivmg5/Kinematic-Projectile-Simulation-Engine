# **Kinematic Projectile Simulation Engine**
> *Simulating the trajectories of projectiles launched from a volcanic eruption using the Verlet method for accurate motion representation.*

## **Introduction**
This project focuses on simulating the trajectories of projectiles launched from a volcanic eruption to predict their paths and impact points. By using the Verlet method, this model aims to provide tools for simulating similar situations and mitigating potential disasters in future eruptions.

## **Project Description**
- **Main functionality:** Calculates and graphically represents the trajectories of projectiles launched from a hypothetical volcano using the Verlet method.
- **Technologies used:** MATLAB, physics of moving bodies, and the Verlet mathematical model for trajectory simulations.
- **Challenges faced:** Implementing the summation of forces with drag conditions and adjusting precise trajectories within the code.
- **Future improvements:** Adding more user-input parameters to enhance model accuracy and simulation flexibility.

## **Table of Contents**
1. [Introduction](#introduction)
2. [Project Description](#project-description)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Testing](#testing)
6. [License](#license)

## **Installation**
1. **Prerequisites**:
   - **MATLAB** - [Download MATLAB](https://www.mathworks.com/downloads/)

2. **Clone the repository:**
   ```bash
   git clone https://github.com/ivmg5/Kinematic-Projectile-Simulation-Engine.git
   cd Kinematic-Projectile-Simulation-Engine
   ```

3. **Open the project in MATLAB:**
   - Open `main.mlx` in MATLAB to explore and run the simulation script.

### **Configuration Options**
- You can adjust variables such as `DEBUG=true` mode, environment variables like `rho_air`, `cd`, and initial conditions in `main.mlx`.

## **Usage**
To simulate volcanic projectile trajectories, follow these steps:
1. Open `main.mlx` in MATLAB.
2. Enter the number of trajectories you want to model when prompted.
3. For each trajectory, input:
   - Air resistance coefficient (`cd`).
   - Initial velocity of the projectile (`vi`).
   - Launch angle (`angle`) in degrees.
4. Observe the trajectory, maximum height, and horizontal range on the generated plot.

**Example output:**
```plaintext
The maximum height is 1500 m
The horizontal range is 3500 m
```

**Plot:**

The simulation will display a graph of the projectile’s trajectory along with key metrics.

## **Testing**
Run the MATLAB script by executing `main.mlx` in the MATLAB environment to validate functionality. Ensure the trajectory and results are as expected based on initial input values.

## **License**
This project is licensed under the MIT License.

[![Build Status](https://img.shields.io/badge/status-active-brightgreen)](#)
[![MATLAB Version](https://img.shields.io/badge/MATLAB-R2023a-blue)](#)
