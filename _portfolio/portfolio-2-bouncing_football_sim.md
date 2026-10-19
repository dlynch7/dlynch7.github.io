---
title: "Rigid-Body Mechanics on SE(3) with Impacts"
excerpt: "This project uses a geometric integrator and event detection to simulate an American football tumbling and bouncing on a hard surface.<br/><img src='/images/bouncing_football.gif' width='500'>"
collection: portfolio
---

This simple project combines a geometric integrator and event detection to simulate an American football (or a rugby ball!) tumbling through the air and bouncing on a hard surface.
<img src='/images/bouncing_football_trace_CoM.svg'>

This toy problem is a good application for so-called _geometric integrators_ that evolve the system configuration direction on the configuration manifold---SE(3), in this case---without relying on one or more charts of local coordinates.
Anyone who has tried to chase and catch a bouncing football knows that it can tumble and bounce wildly enough that no one coordinate chart is likely to be sufficient for representing its configuration for all time.

There are many kinds of geometric integrators in the literature.
For this project, I used a 4th-order Crouch-Grossman integrator (CG4), which essentially generalizes the standard 4th-order Runge-Kutta integrator (RK4) to manifolds.
Crouch-Grossman integrators were among the first geometric integrators to be developed, and more recent geometric integrators, including variational integrators, may have lower computational complexity and superior long-term energy/momentum conservation, but CG4 is a good starting point because it so closely resembles RK4.
