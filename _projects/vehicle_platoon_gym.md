---
layout: page
title: vehicle-platoon-gym
description: A gym-compatible reinforcement learning environment for longitudinal vehicle platoon control and fuel efficiency optimization.
img: assets/img/platoon_proj.png
importance: 1
category: past
github: https://github.com/rafaelcunha2013/vehicle-platoon-gym
related_publications: true
---

A Python reinforcement learning environment built on the OpenAI Gym API that simulates longitudinal vehicle platoon dynamics. The agent learns to optimize fuel efficiency by switching between Adaptive Cruise Control (ACC) parameters in the presence of a stochastic jammer vehicle.

**Key features:**
- OpenAI Gym-compatible API
- Models a 1D platoon with stochastic disturbances (jammer vehicle)
- Designed to reproduce and extend the results from {% cite cunha2022reducing %} and {% cite goncalves2023fuel %}
