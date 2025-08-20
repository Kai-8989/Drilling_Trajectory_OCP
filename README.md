<div style="float: left">
  <img src='https://www.tu-clausthal.de/fileadmin/TU_Clausthal/images/CorporateDesign/Logo/Logo_TUC_de_Web.gif'>
</div>
<div style="float: right; font-size: 0.8em">
  <div style="margin-bottom: 0.8em">
    <span style="font-weight: bold; font-size: 1.2em;">Institut für Mathematik</span><br />
  </div>
    <div>
        Prof. Dr. Andreas Potschka<br />
        Kaisar Dawara
    </div>
  </div>
</div>

# TUC Drillbotics Trajectory optimization Tool

## Abstract

The TUC Drillbotics team participates in the international Drillbotics competition, where the drilling trajectory must be planned through a set of goal points that are not aligned in a straight line. The planned trajectory will be executed by an autonomous miniature drilling rig. Constraints on the trajectory are imposed by the physical properties of the Bottom Hole Assembly (BHA).

## Introduction

In the context of the Drillbotics competition, a key challenge lies in the automated generation of drillable trajectories through a predefined set of 3D coordinates, all under mechanical and physical constraints. To facilitate the development and comparison of various trajectory planning algorithms, a systematic evaluation framework is required.

The goal of this project is to design and implement a **trajectory optimization and evaluation tool** that quantitatively assesses the output of different planning approaches.

## Task Description

The task is to program a tool that evaluates generated trajectories. The tool should accept either a **discrete** (sequence of waypoints) or **continuous** (parametric curve) representation of a trajectory and compute a **composite cost function** based on multiple, weighted evaluation criteria.

### Evaluation Criteria

The evaluation tool will compute a cost based on the following (customizable) metrics:

- **Total Path Length**  
  Affects drilling time and material wear.

- **Cumulative Angular Deviation / Curvature**  
  Penalizes sharp bends and infeasible transitions. Encourages smoother trajectories and discourages zigzag paths, even if each individual bend is mechanically feasible.

- **Mechanical Feasibility Constraints**  
  Includes constraints such as maximum allowable deviation per segment and minimum radius of curvature.

- **Estimated Energy Consumption and Time**  
  Based on the geometry of the path and expected drilling dynamics.

### Features

- Composite cost function for multi-objective evaluation.
- Support for sensitivity analysis (adjustable weights).
- Comparison and ranking of different trajectory planning algorithms.
- Modular design to allow future extensions.

### Purpose

The scalar cost produced by the tool provides a **quantitative and objective basis** for:

- Comparing and ranking trajectory planning algorithms.
- Supporting iterative algorithm optimization.
- Encouraging multi-objective optimization in planning strategies.
****
