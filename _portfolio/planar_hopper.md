---
title: "Robotic Testbed for Research on Dynamic Legged Locomotion on Yielding Terrain"
excerpt: "I designed and built this robot leg (with help from several teammates in Robot Design Studio 2018) to serve as an experimental testbed for the latter half of my doctoral research.<br/><img src='/images/planar_hopping.gif' width='500'>"
collection: portfolio
---

<img src='/images/robot_collage.png'>

My doctoral research on dynamic legged locomotion on yielding terrain called for a custom robot that could hop in the sagittal plane across a bed of granular media.
This robot is a monopod, consisting of a body and a foot, coupled by a planar three-degree-of-freedom linkage actuated by three brushless DC (BLDC) motors.

While the research accomplished with this robot is the subject of an [upcoming paper](../_publications/lynch20xxplanar.md) (in preparation), this portfolio entry goes into detail on the engineering that went into the robot.

## Robot Design Principles

<img src='/images/robot_photo_front_view.png' width=500>

This robot leg design embodies three desirable properties:
1. The leg has three planar degrees of freedom (DOF), so the space of feasible contact wrenches is full-dimensional.
2. The leg is driven by quasidirect-drive actuators, which are highly backdrivable and have low hysterisis, improving the leg's ability to apply desired contact wrenches.
3. The leg's actuators act in parallel rather than series, reducing the torque required from each actuator as well as the mass/inertia of the linkage connecting the actuators to the foot.

This design cuts down on the inertia of the leg linkage enough that its dynamics can be neglected.
Instead of a complicated many-body system, the robot can be modeled as two planar rigid bodies (the body and the foot) connected by an ideal wrench source.
The computations required to control the simplified model are, in turn, simpler. which means they can be performed online at a high frequency (1 kHz, in this case).

Each actuator is built around a Maxon EC-90 Flat 90 W BLDC motor.
A 3:2 gear ratio is used for the left and right actuators and a 1:1 gear ratio for the middle actuator.
This "division of labor" works for typical leg configurations and contact wrenches because the torque required at the middle actuator is lower than the torques required at the left and right actuators.
These low gear ratios are achieved with timing belts rather than gearboxes, to reduce both mass and backlash.
The biggest downside of such low gear ratios is that the motors draw a lot of current (21.1 A at stall!), requiring an appropriately robust system-level electrical design, discussed below.

## Boom

<img src='/images/robot_and_boom_assembly.png' width=800>

The robot is mounted to the end of a carbon fiber boom so it sweeps out a circle (1.4 m radius) as it hops.
This allows me to focus on hopping and balancing in the sagittal plane without also having to contend with balancing in the out-of-plane direction---the latter increases the difficulty of locomotion without providing much scientific insight beyond what's already happening in the sagittal plane.
The opposite end of the boom has a metal peg on which I can load weight plates to reduce the effective gravity the robot experiences, from 1 G to about 1/4 G.
This reduces Joule heating at the motor windings (a negative side-effect of the extremely low gear ratio and high torques required to hop), which allows for more hops per experiment and less downtime between experiments.
The boom is long enough and the robot hops slowly enough that centripedal forces are small compared to contact forces and the robot's weight.

