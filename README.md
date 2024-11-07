# Gishushu Traffic Light System

Overview
=========

The Gishushu Traffic Light System is designed to manage traffic flow and pedestrian crossings at a busy intersection with multiple directions: North, South, East, and West. Using a state-dependent dynamic interaction model, the system prioritizes pedestrian safety while minimizing traffic flow disruption.

Specifications
--------------
1. Directions and Movements
===========================

The intersection has the following vehicle directions:

North-Bound: N-N, N-E, N-W
South-Bound: S-S, S-E, S-W
East-Bound: E-S, E-E, E-N, E-W
West-Bound: W-S, W-W, W-N, W-E
Each direction allows vehicles to proceed based on the Green, Yellow, or Red state assigned to their corresponding phase.

2. System Phases
=================

The system operates in four main vehicle phases (A, B, C, D) and two pedestrian crossing phases (North-South and East-West). These phases proceed in a cyclical manner:

Vehicle Phase A: Green light for North-bound traffic (N-N, N-E, N-W).
---------------

Green: Vehicles in Phase A move freely.
Yellow: Warning phase before Red.
Red: Vehicles stop to allow pedestrians or other vehicles to proceed.
Vehicle Phase B: Green light for South-bound traffic (S-S, S-E, S-W).
---------------

Same cycle as Phase A.
Vehicle Phase C: Green light for East-bound traffic (E-S, E-E, E-N, E-W).

Same cycle as Phase A.
Vehicle Phase D: Green light for West-bound traffic (W-S, W-W, W-N, W-E).

Same cycle as Phase A.
3. Pedestrian Crossing Phases
==============================
Pedestrians can cross in parallel to vehicle phases, minimizing traffic disruption:

Pedestrian Crossing - North-South:

Pedestrians cross in the North-South direction.
Vehicle Status: Vehicles in Phase A and Phase B stop (Red light), while Phases C and D remain in their current state.
Pedestrian Crossing - East-West:

Pedestrians cross in the East-West direction.
Vehicle Status: Vehicles in Phase C and Phase D stop (Red light), while Phases A and B remain in their current state.
4. Cycle Sequence
=================
The system follows a repeating cycle for each phase:

Phase A (North-bound) - Green → Yellow → Red
Pedestrian Crossing - North-South: Stops vehicles in Phases A and B.
Phase B (South-bound) - Green → Yellow → Red
Pedestrian Crossing - East-West: Stops vehicles in Phases C and D.
Phase C (East-bound) - Green → Yellow → Red
Pedestrian Crossing - North-South: Stops vehicles in Phases A and B.
Phase D (West-bound) - Green → Yellow → Red
Pedestrian Crossing - East-West: Stops vehicles in Phases C and D.
This cycle ensures efficient vehicle movement while providing safe pedestrian crossings with minimal traffic interruptions.

5. Safety Measures
==================
Yellow Light for Vehicles: Each vehicle phase includes a Yellow light as a transition before Red to help drivers anticipate stops.
Parallel Pedestrian Crossings: Pedestrians cross parallel to vehicle flows, allowing safe pedestrian movement while keeping some vehicle directions active.
6. Key Features
===============
State-Dependent Phasing: Transitions between phases are controlled by timers and states, ensuring no conflicts between vehicle and pedestrian crossings.
Parallel Pedestrian Integration: Allows pedestrian crossings alongside vehicle flow to optimize intersection efficiency.

Example Traffic Light State Flow
---------------------------------
Here is a sample cycle for the system:

Phase A - North-bound vehicles (N-N, N-E, N-W) Green → Yellow → Red
Pedestrian Crossing North-South: Stops vehicles in Phases A and B.
Phase B - South-bound vehicles (S-S, S-E, S-W) Green → Yellow → Red
Pedestrian Crossing East-West: Stops vehicles in Phases C and D.
Repeat Cycle.
This sequence maximizes efficiency by managing traffic and pedestrian movement dynamically.