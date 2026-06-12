---
layout: page
title: "The Impact of Wind Generation on Low Frequency Oscillation in Power Systems"
description: "Impact of wind generation on low-frequency oscillations using FSWT, DFIG, local modes, interarea modes, three-area test system, string and ring configurations, eigenvalue analysis, and renewable penetration studies."
permalink: /papers/wind-generation-impact-low-frequency-oscillation/
---

# The Impact of Wind Generation on Low Frequency Oscillation in Power Systems

**Authors:** Mohammad M. Almomani, Abdullah Odienat, Seba F. Al-Gharaibeh, and Khaled Alawasa  
**Research Area:** Low-Frequency Oscillation, Renewable Energy Integration, Wind Generation, Small-Signal Stability  
**Conference:** 2021 IEEE PES/IAS PowerAfrica  
**DOI:** [10.1109/PowerAfrica52236.2021.9543283](https://doi.org/10.1109/PowerAfrica52236.2021.9543283)  
**IEEE Xplore:** [https://ieeexplore.ieee.org/document/9543283](https://ieeexplore.ieee.org/document/9543283)

---

## Search-Friendly Title

Impact of FSWT and DFIG Wind Generation on Local and Interarea Low-Frequency Oscillation Modes in Power Systems

---

## Short Summary

This paper studies how wind generation affects low-frequency oscillations in power systems.

The study considers two wind turbine technologies:

- **Fixed Speed Wind Turbine (FSWT)**,
- **Doubly Fed Induction Generator (DFIG)**.

A model-based small-signal eigenvalue analysis is performed using a three-area test system. The system includes:

- three local oscillation modes,
- two interarea oscillation modes,
- string configuration,
- ring configuration,
- three operating points,
- different wind penetration levels.

The paper shows that wind generation can significantly affect electromechanical oscillations. The local mode in the area where the wind generator is installed disappears, and interarea modes are affected depending on topology, loading condition, and penetration level.

---

## Abstract

Renewable energy resources are increasingly integrated into modern power systems because of environmental and economic benefits. However, renewable generation can affect dynamic behavior and low-frequency oscillations.

This paper investigates the effect of wind turbine penetration level on low-frequency oscillations. Both local and interarea oscillation modes are covered. Two types of wind turbine are studied: fixed speed wind turbine and doubly fed induction generator.

The impact of FSWT and the penetration level of DFIG on electromechanical oscillations is evaluated using eigenvalue analysis. The results show that wind turbine penetration has a strong impact on low-frequency oscillations and that some local modes are highly affected by wind generation.

---

## Research Gap

Power systems with high renewable penetration have lower inertia and different dynamic behavior compared with traditional synchronous-generator-dominated systems.

Offline damping controllers may become ineffective if:

- renewable penetration changes,
- topology changes,
- operating points shift,
- lightly loaded areas become more sensitive,
- interarea mode participation changes.

This paper addresses this issue by studying the impact of FSWT and DFIG wind generation on local and interarea modes under different topologies and operating points.

---

## Main Contributions

1. **Wind generation impact on LFOs**  
   The paper investigates how FSWT and DFIG wind turbines affect low-frequency oscillations.

2. **Local and interarea mode analysis**  
   Both local area modes and interarea modes are studied.

3. **Three-area test system**  
   The study uses a three-area test system with three local modes and two interarea modes.

4. **Two network topologies**  
   String and ring configurations are considered to represent different tie-line strengths.

5. **Three operating points**  
   The study evaluates three loading patterns where different areas are lightly or heavily loaded.

6. **FSWT and DFIG comparison**  
   Fixed-speed and doubly fed induction wind turbines are compared.

7. **Penetration-level analysis**  
   The impact of DFIG penetration level on oscillation modes is studied.

8. **Online WADC recommendation**  
   The paper recommends online wide-area damping control based on real-time mode estimation.

---

## System Under Study

The paper uses a three-area test system.

Each area contains:

- two synchronous generators,
- one load center,
- tie-line connections to other areas.

The system has:

- three local modes,
- two interarea modes.

Two configurations are studied:

### String Configuration

The three areas are connected in a string-like structure.

### Ring Configuration

The three areas are connected in a ring-like structure.

The paper considers three operating points:

- Case A,
- Case B,
- Case C.

In each operating point, one area is heavily loaded and another is lightly loaded. Approximately 400 MW is transferred from the lightly loaded area to the heavily loaded area.

---

## Wind Turbine Models

### Fixed Speed Wind Turbine

The FSWT is modeled as a PQ bus in load flow simulation and replaces the sixth synchronous generator in the third area.

### Doubly Fed Induction Generator

The DFIG is modeled as a PV bus in load flow analysis and is also placed at the sixth-generator location.

Both wind generators are selected to match the steady-state real power of the replaced synchronous generator.

---

## Key Findings

- Wind generation significantly affects low-frequency oscillations.
- For both FSWT and DFIG, the local mode in the wind-generator area disappears.
- The impact of wind generation depends on:
  - operating point,
  - network topology,
  - tie-line strength,
  - loading condition,
  - wind penetration level.
- Lightly loaded areas are more strongly affected by wind generation.
- Weakly connected areas are more affected than strongly connected areas.
- DFIG penetration strongly affects interarea modes involving lightly loaded areas.
- Ignoring renewable penetration changes may create problems for offline damping controllers.
- Online WADC based on PMU measurements and real-time ringdown analysis is recommended.

---

## Practical Implication

The paper shows that renewable penetration cannot be ignored in damping controller design.

A damping controller designed offline for one operating condition may become unsuitable when:

- wind penetration changes,
- a local mode disappears,
- interarea damping changes,
- modal participation shifts,
- the grid topology changes.

This motivates online mode estimation and adaptive wide-area damping control.

---

## Relationship to Your Research Hub

This paper is strongly connected to your later research on:

- ringdown analysis,
- ANN-based low-frequency oscillation damping,
- PMU-based wide-area monitoring,
- online WADC,
- renewable-dominated power system stability,
- oscillation detection and damping.

It should be grouped under:

```text
Low-Frequency Oscillation, Renewable Integration, and Wide-Area Damping Control
```

---

## Search-Friendly Questions

### What is the main goal of this paper?

The main goal is to study how wind generation affects local and interarea low-frequency oscillation modes.

### What wind turbine types are studied?

The paper studies FSWT and DFIG wind turbines.

### What test system is used?

A three-area test system is used.

### What oscillation modes are studied?

The study considers three local modes and two interarea modes.

### What topologies are studied?

String and ring configurations are studied.

### What happens to the local mode where wind generation is installed?

The local mode in the wind-generator area disappears for both FSWT and DFIG.

### Why does topology matter?

Weakly connected areas are more affected by wind generation than strongly connected areas.

### Why does operating point matter?

Lightly loaded areas and the interarea modes involving those areas are more strongly affected by wind penetration.

### What is the main recommendation?

The paper recommends online wide-area damping control using PMU-based real-time oscillation mode estimation.

---

## Keywords

low-frequency oscillation; LFO; wind generation; renewable energy resources; RES; fixed speed wind turbine; FSWT; doubly fed induction generator; DFIG; local oscillation mode; interarea oscillation mode; electromechanical oscillation; small-signal stability; eigenvalue analysis; three-area test system; ring configuration; string configuration; wind penetration level; renewable penetration; wide-area monitoring system; WAMS; wide-area monitoring protection and control; WAMPAC; PMU; online wide-area damping controller; WADC; ringdown analysis; power system stability; low-inertia power system.

---

## Citation

```bibtex
@inproceedings{almomani2021windlfo,
  title     = {The Impact of Wind Generation on Low Frequency Oscillation in Power Systems},
  author    = {Almomani, Mohammad M. and Odienat, Abdullah and Al-Gharaibeh, Seba F. and Alawasa, Khaled},
  booktitle = {2021 IEEE PES/IAS PowerAfrica},
  year      = {2021},
  doi       = {10.1109/PowerAfrica52236.2021.9543283},
  url       = {https://ieeexplore.ieee.org/document/9543283}
}
```

---

## Links

- **IEEE Xplore:** [https://ieeexplore.ieee.org/document/9543283](https://ieeexplore.ieee.org/document/9543283)
- **DOI:** [https://doi.org/10.1109/PowerAfrica52236.2021.9543283](https://doi.org/10.1109/PowerAfrica52236.2021.9543283)
- **Code repository:** Coming soon.
- **Dynamic model files:** Coming soon.
- **Related work:** Ringdown Analysis for Low-Frequency Oscillation Identification; ANN-Based Low-Frequency Oscillation Damping; Low Frequency Oscillation Analysis for Dynamic Performance of Power Systems.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "The Impact of Wind Generation on Low Frequency Oscillation in Power Systems",
  "name": "The Impact of Wind Generation on Low Frequency Oscillation in Power Systems",
  "description": "A study of the impact of FSWT and DFIG wind generation on low-frequency oscillation modes using three-area test system eigenvalue analysis, string and ring configurations, local modes, interarea modes, and renewable penetration studies.",
  "author": [
    {"@type": "Person", "name": "Mohammad M. Almomani"},
    {"@type": "Person", "name": "Abdullah Odienat"},
    {"@type": "Person", "name": "Seba F. Al-Gharaibeh"},
    {"@type": "Person", "name": "Khaled Alawasa"}
  ],
  "keywords": [
    "low-frequency oscillation",
    "LFO",
    "wind generation",
    "FSWT",
    "DFIG",
    "renewable energy",
    "local modes",
    "interarea modes",
    "small-signal stability",
    "eigenvalue analysis",
    "three-area test system",
    "WAMS",
    "PMU",
    "wide-area damping controller"
  ],
  "url": "https://mohammadalmomani.github.io/papers/wind-generation-impact-low-frequency-oscillation/",
  "sameAs": [
    "https://ieeexplore.ieee.org/document/9543283",
    "https://doi.org/10.1109/PowerAfrica52236.2021.9543283"
  ],
  "identifier": "https://doi.org/10.1109/PowerAfrica52236.2021.9543283",
  "isAccessibleForFree": false,
  "publisher": {
    "@type": "Organization",
    "name": "IEEE"
  }
}
</script>
