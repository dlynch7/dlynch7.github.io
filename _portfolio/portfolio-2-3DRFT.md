---
title: "Fast(er) 3D Resistive Force Theory"
excerpt: "This is a vectorized implementation of 3D resistive force theory (Agarwal et al., PNAS 2023) with support for custom intruder geometries.<br/><img src='/images/3D-RFT_illustrative_example.png' width='500'>"
collection: portfolio
---

This is a vectorized implementation of 3D resistive force theory ([Agarwal et al., PNAS 2023](https://doi.org/10.1073/pnas.2214017120)) with support for custom intruder geometries.
You can get the source code from [my GitHub repo](https://github.com/dlynch7/3DRFT).

<img src='/images/3D-RFT_illustrative_example.png' width='500'>

## What is Resistive Force Theory?
Resistive force theory (RFT) is a computational method that models the force distribution over an object moving through a resistive medium.
It was originally applied to low-Reynolds-number fluids ([Gray and Hancock, JEB, 1955](https://doi.org/10.1242/jeb.32.4.802)) but, more recently, it has turned out to work well for granular media too, first for planar motion ([Li et al., Science, 2013](https://doi.org/10.1126/science.1229163)) and, more recently, for three-dimensional motion ([Agarwal et al., PNAS 2023](https://doi.org/10.1073/pnas.2214017120)).

## What's Special about My Implementation?
It's fast...er.

<img src='/images/3DRFT_bunny_const_twist_anim.gif'>

<img src='/images/sphere_screws_simplified.png' width='500'>
