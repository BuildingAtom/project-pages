---
# Front matter. This is where you specify a lot of page variables.
title:  "Autonomous Robust Manipulation via Optimization with Uncertainty-aware Reachability"
date:   2023-01-30 17:02:40 -0500
description: >- # Supports markdown
  Can’t Touch This: Real-Time, Safe Motion Planning and Control for Manipulators Under Uncertainty
show-description: true

# Preview image for social media cards
image:
  path: https://roahmlab.github.io/armour-dev/figures/armour_summary_figure.png
  height: 108
  width: 227
  alt: Armour Summary Figure

# Only the first author is supported by twitter metadata
authors:
  - name: Jonathan Michaux
  - name: Patrick Holmes
  - name: Bohao Zhang
  - name: Che Chen
  - name: Baiyue Wang
  - name: Shrey Sahgal
  - name: Tiancheng Zhang
  - name: Sidhartha Dey
  - name: Shreyas Kousik
  - name: Ram Vasudevan

links:
  - icon: bi-file-earmark-text
    icon-library: bootstrap-icons
    text: Paper
    url: https://github.com/roahmlab/armour-dev
  - icon: github
    icon-library: simpleicons
    text: Code
    url: https://arxiv.org/abs/2301.13308

# End Front Matter
---

{%- include sections/authors -%}
{%- include sections/links -%}

<div class="fullwidth">
<iframe style="aspect-ratio: 16/9; height: 100%; width: 100%;" src="https://www.youtube.com/embed/-WtxxQyoxGo" title="Can’t Touch This: Real-Time, Safe Motion Planning and Control for Manipulators Under Uncertainty" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>


<div markdown="1" class="content-block grey justify">
# Introduction

A key challenge to the widespread deployment of robotic manipulators is the need to ensure safety in arbitrary environments while generating new motion plans in real-time.
In particular, one must ensure that the manipulator does not collide with obstacles, collide with itself, or exceed its own joint torque limits.
This challenge is compounded by the need to account for uncertainty in the mass and inertia of manipulated objects, and potentially the robot itself.
The present work addresses this challenge by proposing Autonomous Robust Manipulation via Optimization with Uncertainty-aware Reachability (`ARMOUR`), a provably-safe, receding-horizon trajectory planner and tracking controller framework for serial link manipulators.
In particular, this paper makes three contributions.
First, a robust, passivity-based controller enables a manipulator to track desired trajectories with bounded error despite uncertain dynamics.
Second, a novel variation on the Recursive Newton-Euler Algorithm (RNEA) allows \methodname to compute the set of all possible inputs required to track any trajectory within a continuum of desired trajectories.
Third, this paper provides a method to compute the swept volume of the manipulator given a reachable set of states; this enables one to guarantee safety by checking that the swept volume does not intersect with obstacles.
The proposed method is compared to state of the art methods and demonstrated on a variety of challenging manipulation examples in simulation, such as maneuvering a heavy dumbbell with uncertain mass around obstacles.
The link to the project website is

![Summary Figure](https://roahmlab.github.io/armour-dev/figures/armour_summary_figure.png "Summary Figure")
</div>

# Method

![Armour Method](https://roahmlab.github.io/armour-dev/figures/armour_method.png "Armour Method")

# Results

![Results Figure](https://roahmlab.github.io/armour-dev/figures/hard_scenarios_test.png "Results Figure")

<div markdown="1" class="content-block grey justify">

# Citation

* This work is supported by the Ford Motor Company via the Ford-UM Alliance under award N022977, National Science Foundation Career Award #1751093 and by the Office of Naval Research under Award Number N00014-18-1-2575
* ARMOUR was developed in [Robotics and Optimization for Analysis of Human Motion (ROAHM) Lab](http://www.roahmlab.com/) at University of Michigan - Ann Arbor.

```bibtex
@article{article,
    author = {Michaux, Jonathan and Holmes, Patrick and Zhang, Bohao and Chen, Che and Wang, Baiyue and Sahgal, Shrey and Zhang, Tiancheng and Dey, Sidhartha and Kousik, Shreyas and Vasudevan, Ram},
    year = {2023},
    month = {01},
    pages = {},
    title = {Can't Touch This: Real-Time, Safe Motion Planning and Control for Manipulators Under Uncertainty},
    doi = {10.48550/arXiv.2301.13308}
```
</div>