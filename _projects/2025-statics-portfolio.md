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

## Degrees of Freedom

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


I oriented my design as shown in the sketch, with the bar and actuator both fixed to pin supports on the ground, and attached to each other at a third pin support, C. The weight was hung from the bar, attached at the bar's highest point in order to optimize the weight's final height. I selected the IMA ("Integrated Servo Actuator") because it had the highest force to length ratio among the actuators that were short enough to fit in the design space. The IMA can support up to 36kN, and has a maximum length of 50cm. 

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

<div style="max-width: 300px; margin: 1.5rem auto; text-align: center;">
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

<div style="max-width: 300px; margin: 1.5rem auto; text-align: center;">
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

<div style="max-width: 180px; margin: 1.5rem auto; text-align: center;">
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
    Figure 6. Design challenge final design with all unknowns determined.
  </p>
</div>


## Part 2 - Non-Rigid Bar

The second part of the activity was to modify the scenario to the condition in which the bar is no longer rigid. Using my final design from part 1, my goals for part 2 were to 1) find the maximum deflection in the bar (now modeled as a beam), 2) choose a beam design such that vertical deflection is below 2% of the beam's length and is the most mass-efficient possible, and 3) present my final beam design in a diagram. 

1) Maximum deflection

To begin to find the maximum deflection, I revisited the FBD for the bar shown previously (Figure 2). For this problem, I assumed that only the transverse loads acting on the beam were impacting its deflection, and additionally, that Fw and Fa were acting in the same direction (note: this is not accurate to the FBD, it is purely being done as an exercise). 

Using the FBD, it is seen that the following transverse forces act on the bar:

<div style="max-width: 180px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-transverseforces.jpg' | relative_url }}" 
    alt="Transverse forces expressions"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 7. Expressions for transverse forces.
  </p>
</div>

Summing these, and taking into account the assumption noted above, the net transverse force on the beam is calculated to be approximately 24.63kN: 

<div style="max-width: 180px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-nettransverse.jpg' | relative_url }}" 
    alt="Net transverse forces expression"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 8. Expression for total transverse forces.
  </p>
</div>

The next step is to use the transverse force value to derive an expression for the total deflection of the beam. For a cantilever beam, the expression for deflection, y(x), in terms of transverse force applied, is:

<div style="max-width: 180px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-deflection.jpg' | relative_url }}" 
    alt="Cantilever beam deflection expression"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 9. Expression for deflection in a cantilever beam.
  </p>
</div>

Plugging in values for transverse force and length, we derive that deflection is:

<div style="max-width: 180px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-deflectionevaluation.jpg' | relative_url }}" 
    alt="Cantilever beam deflection evaluation"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 10. Evaluated expression for deflection.
  </p>
</div>


b) Choosing a beam design 

As clear from Figure 10, the total deflection of the beam cannot fully be analyzed without values for E and I, which cannot be determined until the beam's shape and material have been selected. 

The constraints for this design choice are that the vertical deflection of the beam must be less than 2% of its total length and the design must be the most mass-efficient possible. This allows us to determine a minimum value of EI: 

<div style="max-width: 180px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-EI.jpg' | relative_url }}" 
    alt="Calculating EI"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 11. Calculating EI.
  </p>
</div>

To prioritize material efficiency, I decided to choose the cross-section first (looking for something narrow and not material dense), then use its moment of inertia to find a material with an appropriate modulues of elasticity. To maximize material efficiency, I selected the W-Flange from my class's textbook, in particular, the W 100x19.3 (which was the narrowest available W-Flange to ensure it fit in the design space) --- shown below.

<div style="max-width: 180px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-flange.jpg' | relative_url }}" 
    alt="Flange drawing"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 12. W100x19.3 Flange.
  </p>
</div>

Using the moment of inertia of the flange, I calculated that the modulus of elasticity (E)of the beam's material must be greater than or equal to 32.7 GPa in order to satisfy the 2% condition:

<div style="max-width: 180px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-E.jpg' | relative_url }}" 
    alt="Modulus of elasticity calculation"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 13. Modulus of elasticity calculation.
  </p>
</div>

Utilizing my class's textbook, I looked for materials with E values close to 32.7 without being below. I noticed that magnesium alloy AZ31 was the closest, with E = 45 GPa. Additionally, it was less dense than other close competitors, including concrete, sandsonte, and magnesium alloy AZ80, making it the most mass-efficient.  

Recalculating the total deflection, it is shown that the total deflection of the beam is 0.485cm, ~0.9% of the beam's total length, satisfying the <2% condition.

c) Final beam diagram

<div style="max-width: 180px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/statics-design-challenge-finaldiagram.jpg' | relative_url }}" 
    alt="Final beam design diagram"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 14. Final beam design - length and cross-section.
  </p>
</div>