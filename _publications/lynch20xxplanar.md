---
title: "A Template-and-Anchor Approach to Dynamic Legged Locomotion on Yielding Terrain"
collection: publications
category: inprep
permalink: /publication/lynch20xxplanar
excerpt: ''
date: 20xx-xx-xx
venue: 'N/A'
# paperurl: 'https://academicpages.github.io/files/paper3.pdf'
# citation: 'Your Name, You. (2024). &quot;Paper Title Number 3.&quot; <i>GitHub Journal of Bugs</i>. 1(3).'
---
Abstract
===
Complex terrain, where legged robots have the potential to outperform wheeled or tracked robots, is difficult to model, and model-based approaches to planning and control for legged locomotion have been largely confined to substrates that are easily modeled.
Moreover, because complex terrain is difficult to model, it is also difficult to simulate, so transferring locomotion policies learned in simulation to the real world remains challenging, and innovations in data-driven control have only recently enabled legged robots to take their first steps out of the modeled world and onto complex terrain.
Instead, a combination of model-based and data-driven control, possibly integrated in an active-learning framework, has a greater chance of enabling legged robots to operate robustly and efficiently on yielding substrates.
This paper contributes to the model-based foundations of such an approach.
Specifically, this paper presents a reduced-order model of foot-ground interaction that captures the fundamental physical features of foot-ground interaction on yielding terrain, namely a finite yield threshold that depends on foot size, foot depth, and ground stiffness.
We use multi-phase trajectory optimization to plan stance-phase contact wrench profiles for a monopod hopping in the sagittal plane, obtaining trajectories that are consistent with this reduced-order model of foot-ground interaction and achieve requested centroidal momentum at each touchdown.
We stabilize the optimal trajectory with time-varying linear feedback control, and we validate our results on a custom-built robot with three planar degrees of freedom that hops across a prepared granular media trackway.