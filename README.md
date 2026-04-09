# ROB Final Project

This repository contains a MuJoCo-based robotics project built around the Universal Robots UR10e arm. It combines core robotics coursework topics such as forward kinematics, inverse kinematics, and velocity kinematics with visual simulation outputs, and extends them into a 3D Fruit Ninja-style robot interaction demo.

## Overview

The project is organized around two main Jupyter notebooks:

1. `FORFinalProject.ipynb`
   Covers the core robotics assignments for the UR10e manipulator:
   - Forward Kinematics (Position)
   - Inverse Kinematics (Position)
   - Forward Kinematics (Velocity)
   - Inverse Kinematics (Velocity)

2. `3Dfruitninjasimulation.ipynb`
   Extends the project into a dynamic robot simulation where the UR10e interacts with moving fruit objects in a MuJoCo environment.

Together, these notebooks make the project more than a set of equations or isolated functions: they connect robotics theory to visual, simulation-based results.

## What This Project Covers

### Kinematics for the UR10e

The main notebook implements and visualizes:

- Forward kinematics using UR10e DH parameters
- Inverse kinematics for reaching target positions
- End-effector velocity estimation using the Jacobian
- Joint velocity solving for desired end-effector motion

The results are rendered in MuJoCo and exported as GIFs, making it easy to inspect whether the implementation behaves as expected.

### 3D Fruit Ninja-Style Robot Simulation

The second notebook builds a custom MuJoCo scene in which the UR10e tracks and strikes fruit-like objects. It includes:

- Fruit spawning and state management
- Position-based IK for target interception
- Quintic trajectory generation for smooth motion segments
- Inverse dynamics feedforward torque generation
- Predictive rollout and PD-based hold control

This turns the project into a practical robotics simulation demo rather than a notebook-only math exercise.

## Repository Structure

```text
.
|-- FORFinalProject.ipynb
|-- 3Dfruitninjasimulation.ipynb
|-- robot_free_fall.xml
|-- mujoco_menagerie/
|   `-- universal_robots_ur10e/
|-- ur10e_FK_position.gif
|-- ur10e_IK_position.gif
|-- ur10e_FK_velocity.gif
|-- ur10e_IK_velocity.gif
|-- robot_dynamics_simulation.gif
|-- output.gif
`-- FORFinalProject.zip
```

## Key Files

- `FORFinalProject.ipynb`
  Main course project notebook for UR10e kinematics and visualization.

- `3Dfruitninjasimulation.ipynb`
  Extended notebook for torque-driven dynamic interaction with moving fruit objects.

- `robot_free_fall.xml`
  Custom MuJoCo MJCF file describing the robot and fruit simulation scene.

- `mujoco_menagerie/universal_robots_ur10e/`
  UR10e robot model assets, scene configuration, and supporting mesh files.

- `*.gif`
  Exported simulation results from the notebooks.

## Technologies Used

- Python
- Jupyter Notebook
- MuJoCo
- NumPy
- SciPy
- Matplotlib
- Pillow
- XML / MJCF scene modeling

## How to Run

### 1. Set up a Python environment

A Python 3.10+ environment is recommended.

```bash
pip install mujoco numpy scipy matplotlib pillow ipython ipykernel notebook
```

### 2. Launch Jupyter

```bash
jupyter notebook
```

Then open and run the notebooks in order:

1. `FORFinalProject.ipynb`
2. `3Dfruitninjasimulation.ipynb`

Each notebook is written to be executed from top to bottom.

## Output Files

This repository already includes example simulation outputs such as:

- `ur10e_FK_position.gif`
- `ur10e_IK_position.gif`
- `ur10e_FK_velocity.gif`
- `ur10e_IK_velocity.gif`
- `robot_dynamics_simulation.gif`
- `output.gif`

These files provide quick visual confirmation of the kinematics and dynamics results.

## Project Type

This repository is best understood as a course or research-style simulation project rather than a packaged software library. It is well suited for:

- Robotics coursework or final project submission
- MuJoCo-based robot simulation practice
- UR10e kinematics and control demonstrations
- Notebook-centered experimentation and visualization

## Notes

- The UR10e model assets are included through the `mujoco_menagerie` directory.
- Some files appear to be generated outputs or submission artifacts.
- The current repository structure is notebook-oriented and experimental, not organized as a reusable Python package.

## Acknowledgment

The UR10e MuJoCo model in `mujoco_menagerie/universal_robots_ur10e` is based on the MuJoCo Menagerie robot description and assets for the Universal Robots UR10e.
