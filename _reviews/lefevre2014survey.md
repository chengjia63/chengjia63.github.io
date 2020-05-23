---
layout: default
title: A survey on motion prediction and risk assessment for intelligent vehicles
---
# [A survey on motion prediction and risk assessment for intelligent vehicles](https://robomechjournal.springeropen.com/articles/10.1186/s40648-014-0001-z)

#### Stephanie Lefevre, Dizan Vasquez and Christian Laugier

---

## What is the Problem?
To improve safety and reduce risk of autonomous vehicles, we need mathematical
models to predict how the situation will evolve in the future

## Summary
The authors categorized motion modeling and prediction approaches into 3 levels:
physics-based models, maneuver-based models and interaction-aware models.
The authors also presented different ways to access risk in the context of 
intelligent vehicles.

### Physics-based models: 
Consider physical laws only. Use dynamic models (Lagrange's equations) or kinematic models (preferred) to predict trajectory. The trajectory may be predicted using:
- A single trajectory (without uncertainty)
- Gaussian noise simulation (KF)
- Monto Carlo simulation

### Maneuver-based models
Consider future motion of a vehicle and driver intent. Assume each vehicle is 
independent, and trajectory will match the intent
- Prototype trajectories: cluster trajectories into a finite set of typical     
    motion pattern, which can be represented using learned prototype 
    trajectories (either a unique prototype, multiple prototypes, a graph 
    structure (HMM), or Gaussian Processes). Trajectory can then be predicted
    by matching a partial trajectory to a prototype trajectory and use it
    as a model
- Maneuver intention estimation: first estimate intention (using heuristics, 
    discriminative ML, or HMM), then predict successive physical states
    (deriving input control, GP, Rapidly-exploring Random Tree).

### Interaction-aware models:
Consider inter-dependencies between vehicles' maneuvers
- Trajectory prototypes: inter-vehicle influences cannot be taken into
    account while learning. In matching phase, assume driver wish to avoid
    collisions, penalize pairs of trajectories that lead to unavoidable
    collision
- Dynamic Bayesian Networks: model pairwise dependencies using coupled HMMs.
    To reduce complexity, assume surround traffic affect the vehicle, but
    not vice versa. Traffic rules may also be incorporated. Other methods
    include using general probabilistic frameworks such as factored states,
    or use situational context to computer a driver's expected maneuver

### Risk assessment
- Based on collision: predict future trajectory and then detect collisions.
    The risk assessment can either be binary or probabilistic to account for
    uncertainty. Some systems focus on detecting unavoidable collision by 
    computing whether there is a collision free maneuver the driver can perform.
    We can also derive other risk indicators such as velocity, amount of overlap,
    probability of simultaneous occupancy, and time to collision / react
- Based on unusual or unexpected behavior: define or learn normal behavior, then
    identify unusual activities

## Key Insights
- Physics-based models are limited to short-term prediction (< 1s) prediction.
    They are unable to anticipate change of motion from maneuvers or external
    factors
- Prototype trajectories have a strictly deterministic time representation. It
    takes a large number of prototypes to model large variations in motion
    pattern and different road layouts
- Interaction-aware models are comprehensive but computationally expensive and
    not compatible with real time risk assessment
- Choice of risk assessment method is tightly coupled with the choice of a
    model

## Strengths
- The paper provides good high level overviews of the different classes of
    motion prediction algorithms

## Limitations/Weaknesses
- There are no quantitative comparisons between the different methods mentioned
    using a common benchmark
