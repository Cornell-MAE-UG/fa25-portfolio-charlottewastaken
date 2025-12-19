---
layout: project
title: Thermodyanamics Class Heat Exchanger Analysis
description: Design Challenge
technologies: [None]
---

<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/heat-exchanger.jpg' | relative_url }}" 
    alt="Heat Exchanger Setup"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 1. Heat exchanger experimental setup.
  </p>
</div>

As part of my Thermodynamics class at Cornell University, we were granted the opportunity to participate in a heat exchanger lab, in which we collected initial and final temperature data on two streams of water flowing through the device. Additionally, we explored the impact of adjusting whether the device was running in counter flow or parallel flow.  

Our experimental setup is shown in the above image. The setup consisted of a heat exchanger placed between two reservoirs of water - one containing hot water; the other cold water. Tubes affixed to pumps were placed into each container, and the pumps routed the water through the tubes, through the heat exchanger, and into two empty "discard" buckets at the other side. 

First, the temperature was measured in the initial hot and cold water reservoirs. Then, the heat exchanger was run for approximately two minutes, or until the water ran out. Lastly, the temperatures in the "discard" buckets were measured. This process was repeated for running the heat exchanger in "counter-flow" and "parallel flow" - ie, changing the direction of one of the two flows. The data collected from this process is shown in Figure 2.

<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/heat-exchanger-table.png' | relative_url }}" 
    alt="Data Table"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Figure 2. Experimental temperature data for counter-flow and parallel-flow cases.
  </p>
</div>

After collecting the data, I analyzed the heat exchanger device using course concepts of control volume energy balance and heat transfer. 

Note: This analysis is limited by the fact that the mass flow rate, mrate, was not recorded. However, using information about energy balance and heat transfer, we can still draw conclusions about the functionality of the device. 

The heat exchanger can be assessed using the control-volume energy balance equation:
<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/equation1.png' | relative_url }}" 
    alt="Equation 1"
    style="width: 25%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Equation 1.
  </p>
</div>

And for liquids like water,
<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/equation2.png' | relative_url }}" 
    alt="Equation 2"
    style="width: 25%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Equation 2.
  </p>
</div>

Which gives,
<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/equation3.png' | relative_url }}" 
    alt="Equation 3"
    style="width: 25%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Equation 3.
  </p>
</div>

Since specific heat is known,
<div style="max-width: 600px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/equation4.png' | relative_url }}" 
    alt="Equation 4"
    style="width: 25%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Equation 4.
  </p>
</div>

Based on the control volume energy balance, if the mass flow rates are equal for the hot and cold streams, and the device is adiabatic, the temperature change should be equal for the hot and cold streams. We compare the ratios for both counter flow and parallel flow:
<div style="max-width: 260px; margin: 1.5rem auto; text-align: center;">
  <img 
    src="{{ '/assets/images/calculations.png' | relative_url }}" 
    alt="Temperature Change Calculations"
    style="width: 100%; height: auto; border-radius: 8px;"
  >
  <p class="caption" style="font-size: 0.9rem; color: #666; margin-top: 0.5rem;">
    Temperature Change Calculations.
  </p>
</div>

Both counter flow and parallel flow show a disproportionately high heat drop in comparison to the cold rise. This suggests that either 1- the system is not adiabatic, or 2- the mass flow rates are not constant. Since the device can be trusted to maintain relatively constant flow rates, the former is the more likely explanation. 

The conclusion is that the device is not adiabatic, and furthermore, that operating in counter flow rather than parallel flow leads to a larger heat leak in the system. 

