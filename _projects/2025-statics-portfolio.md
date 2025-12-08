---
layout: project
title: Statics Class Design Project
description: Design Challenge
technologies: [None]
image: /assets/images/statics-design-challenge-finaldesign.jpg
---
## Problem Definition

For my Statics and Mechanics of Solids class at Cornell University, we were given a design challenge to design a frame or mechanism capable of lifting the maximum possible weight to the highest possible height using an actuator, a bar, and three pin supports. We were asked to analyze the loads and deformation of the mechanism under two cases: first, considering the bar to be rigid, and second, considering the bar to be non-rigid (a beam). 

## Constraints and Objectives 

We were provided a 2D design space of 150cm long and 50cm tall, a rigid bar of a fixed length, and 3 pin supports, of which two need to be mounted on the ground, and a linear actuator to be chosen from an online catalog. The objective was to design a frame/mechanism to lift the maximum possible weight to the highest possible height, first under the assumption of a rigid bar, and second under the assumption of a non-rigid bar. 

## Design Degrees of Freedom

We had the freedom to select the following: the mechanism's orientation/geometry, the type of actuator, the length to which the actuator was extended, and the length of the bar.

## My Design - Preliminary 

<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-preliminarydesign.jpg' | relative_url }}" 
    alt="Design Challenge Preliminary Diagram"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 1. Design challenge preliminary diagram with unknowns.
  </p>
</div>


I oriented my design as shown in the sketch, with the bar and actuator both fixed to pin supports on the ground, and attached to each other at a third pin support, C. The weight was hung from the bar, attached at the bar's highest point in order to optimize the weight's final height. I selected the IMA 22 actuator because it had the highest force to length ratio among the actuators that were short enough to fit in the design space. The IMA 22 can support up to 36kN, and has a maximum length of 50cm. 

I chose to extend the actuator to its full length of 50cm to optimize the final height of the weight, and I chose for the bar to also have a length of 50cm in order to simplify the preliminary design geometry for analysis. With this decided, the next step was to determine the optimal distance between the two ground pin supports, A and B. 

## Analysis and Calculations

My goal in my analysis was to derive an expression for the weight on the bar, Fw, in terms of the angle between the bar and the ground, theta. From this expression, I would select the value of theta (and corresponding design geometry) to optimize Fw, determining 1. the maximum weight supported by my final design, and 2. the maximum height the weight could be lifted to. 

First, I created free body diagrams for the bar and the actuator: 

<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-FBDs.jpg' | relative_url }}" 
    alt="Bar and Actuator FBDs"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 2. Bar and Actuator FBDs.
  </p>
</div>


Using the bar FBD, the following two equilibrium equations are written:

<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-equilibrium.jpg' | relative_url }}" 
    alt="Equilibrium equations"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 3. Equilibrium equations.
  </p>
</div>

From (1), we see that the reaction force at A (Ra) is equivalent to the force supplied by the actuator (Fa). We use this equivalence to simplify (2) and solve for Fw:

<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-solving.jpg' | relative_url }}" 
    alt="Solving for Fw"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 4. Solving for Fw.
  </p>
</div>

Given that the maximum Fa is 36kN, we have:

<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-expression.jpg' | relative_url }}" 
    alt="Expression for Fw"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 5. Expression for Fw.
  </p>
</div>

Therefore, the theoretical maximum weight occurs when theta = 90 degrees. 

## My Design - Final

However, this geometry would require pins A and B to be coincident, an impractical and unstable design choice. Instead, 80 degrees was chosen, a degree measurement that achieves ~98% of the theoretical maximum weight, while also being stable and practically achievable. Evaluating the above equation for Fw, we see that the maximum weight supported by this design is 70.91kN. Through additional geometry calculation, we find that the maximum height the weight can be lifted to is 49.24. 

The final design geometry is shown below (not to scale):

<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-finaldesign.jpg' | relative_url }}" 
    alt="Final design sketch"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 6. Final design.
  </p>
</div>