---
layout: page
title: "Novel Data-Driven Indices for Early Detection and Quantification of Short-Term Voltage Instability from Voltage Trajectories"
description: "Data-driven short-term voltage stability indices for early detection and quantification of voltage instability using voltage trajectories, EMD, Lyapunov exponents, KL divergence, delayed voltage recovery, oscillation stability, OEL, LVRT, and Nordic power system validation."
permalink: /papers/novel-data-driven-indices-stvsi/
---

# Novel Data-Driven Indices for Early Detection and Quantification of Short-Term Voltage Instability from Voltage Trajectories

**Authors:** Mohammad Almomani, Muhammad Sarwar, and Venkataramana Ajjarapu  
**Research Area:** Short-Term Voltage Stability, Voltage Trajectory Analytics, Data-Driven Stability Indices  
**Venue:** 2025 IEEE Power & Energy Society General Meeting (PESGM)  
**DOI:** [10.1109/PESGM52009.2025.11225182](https://doi.org/10.1109/PESGM52009.2025.11225182)  
**IEEE Xplore:** [https://ieeexplore.ieee.org/abstract/document/11225182](https://ieeexplore.ieee.org/abstract/document/11225182)

---

## Search-Friendly Title

Data-Driven Short-Term Voltage Stability Index Using Voltage Trajectories, EMD, Lyapunov Exponents, and KL Divergence

---

## Short Summary

This paper proposes a data-driven Short-Term Voltage Stability Index (STVSI) for early detection and quantification of voltage instability from post-fault voltage trajectories.

The method combines:

- Empirical Mode Decomposition (EMD),
- Lyapunov Exponent-based trajectory analysis,
- Kullback-Leibler (KL) divergence,
- entropy-based stability quantification.

The voltage trajectory is decomposed into two components:

- a **residual component** representing delayed voltage recovery,
- an **oscillatory component** representing voltage oscillations.

This allows the method to separately evaluate instability caused by slow voltage recovery, such as OEL or LVRT-related tripping, and instability caused by undamped voltage oscillations.

---

## Abstract

This paper presents a data-driven Short-Term Voltage Stability Index (STVSI) for early detection and quantification of short-term voltage instability from voltage trajectories.

The proposed method is measurement-based and decomposes post-fault voltage trajectories using Empirical Mode Decomposition (EMD). The residual component captures delayed voltage recovery, while the oscillatory component captures voltage oscillations. Lyapunov Exponent-based detection is then used to evaluate the dynamic behavior of each component.

To move beyond binary stable/unstable classification, the method uses an entropy-based metric and KL divergence to quantify the proximity of the system to instability. Separate indices are developed for recovery-related instability and oscillation-related instability.

Simulation studies on the Nordic power system demonstrate that the proposed STVSI can identify and categorize voltage stability issues and provide a qualitative measure of the degree of stability.

---

## Research Gap

Existing Lyapunov Exponent-based methods can detect instability, but they often provide only binary classification and may misinterpret voltage trajectories that include both delayed recovery and oscillations.

In short-term voltage stability events, slow voltage recovery and voltage oscillations may occur together. This creates mixed dynamic behavior that makes conventional maximum Lyapunov Exponent methods difficult to interpret.

This paper addresses this gap by decomposing voltage trajectories into residual and oscillatory components and evaluating each component separately using data-driven stability indices.

---

## Main Contributions

1. **Voltage-trajectory-based STVSI**  
   A Short-Term Voltage Stability Index is developed using measured post-fault voltage trajectories.

2. **Separation of recovery and oscillatory dynamics**  
   EMD is used to decompose voltage signals into residual and oscillatory components.

3. **Recovery Stability Index**  
   The residual component is used to detect delayed voltage recovery and potential instability caused by OEL or LVRT-related tripping.

4. **Oscillation Stability Index**  
   The oscillatory component is used to detect instability caused by undamped voltage oscillations.

5. **Lyapunov Exponent-based detection**  
   Lyapunov Exponents are calculated over a short time window to characterize the convergence or divergence of voltage trajectory components.

6. **KL-divergence and entropy-based quantification**  
   KL divergence is used to quantify the statistical distance between the observed stability behavior and a reference distribution.

7. **Degree of stability, not only binary classification**  
   The method provides a qualitative measure of stability strength and proximity to instability.

8. **Nordic system validation**  
   The method is validated using the Nordic power system under different dynamic load percentages and motor-load compositions.

---

## Method Overview

The proposed STVSI framework follows these steps:

### 1. Voltage Trajectory Collection

Post-fault voltage trajectories are collected after a disturbance.

### 2. Empirical Mode Decomposition

The voltage signal is decomposed into:

- residual component,
- intrinsic mode functions.

The residual captures delayed recovery, while the intrinsic mode functions capture oscillatory behavior.

### 3. Lyapunov Exponent Calculation

Lyapunov Exponents are calculated for each decomposed component over a short time window.

### 4. Probability Distribution Construction

The distribution of the Lyapunov Exponent-based divergence factor is constructed for each component.

### 5. KL-Divergence Calculation

KL divergence compares the observed distribution with a shifted-reversed Gompertz reference distribution.

### 6. Stability Index Calculation

Two indices are calculated:

- Recovery-caused stability index,
- Oscillation-caused stability index.

### 7. Stability Classification and Quantification

The computed index values are compared with critical thresholds to identify stable, critical, or unstable cases.

---

## Proposed Stability Indices

### Recovery Stability Index

The Recovery Stability Index evaluates delayed voltage recovery using the residual component extracted from EMD. It is designed to detect instability associated with:

- Fault-Induced Delayed Voltage Recovery (FIDVR),
- Over Excitation Limiter (OEL) activation,
- Low Voltage Ride-Through (LVRT) relay activation,
- quasi-steady-state instability after delayed recovery.

A lower recovery index indicates stronger stability, while a higher value indicates proximity to recovery-induced instability.

### Oscillation Stability Index

The Oscillation Stability Index evaluates the oscillatory component of the voltage trajectory using the intrinsic mode functions extracted from EMD.

A high oscillation index indicates ineffective damping and possible oscillation-driven instability. A lower value indicates stable or well-damped oscillatory behavior.

---

## Test System

The paper validates the proposed method using:

- Nordic power system,
- operating point A,
- OEL modeling,
- dynamic composite load behavior,
- Motor A, Motor B, Motor C, and Motor D components,
- different dynamic load percentages,
- 3-second post-fault stability-index calculation,
- 50-second extended simulation for quasi-steady-state validation.

---

## Key Results

- The proposed index can identify unstable behavior within approximately **3 seconds** after the fault.
- The full instability in the reported recovery case occurs around **25 seconds**, showing the early-warning capability of the method.
- For Motor D recovery cases, the method distinguishes between **80% dynamic load instability** and **75% dynamic load close-to-stable behavior**.
- For Motor A oscillatory cases, the method identifies stable oscillatory behavior.
- The oscillatory stability threshold is set at **1**, and the reported stable oscillation index value is approximately **0.218**.
- The recovery index increases as the dynamic load percentage increases, showing that the method quantifies the degree of stability.
- The index reaches the critical threshold at approximately **80% dynamic load**, indicating instability.
- The method provides separate measures for recovery-related instability and oscillation-related instability.

---

## Search-Friendly Questions

### What is the main goal of this paper?

The main goal is to develop a data-driven Short-Term Voltage Stability Index that can detect and quantify short-term voltage instability from post-fault voltage trajectories.

### What is STVSI?

STVSI stands for Short-Term Voltage Stability Index. It is a measurement-based index that evaluates voltage trajectory behavior after a disturbance to determine whether the system is stable, critical, or unstable.

### How does this paper detect short-term voltage instability?

The method decomposes the voltage trajectory using EMD, calculates Lyapunov Exponents for the residual and oscillatory components, and applies KL divergence to quantify the distance from a reference stability distribution.

### Why is EMD used?

EMD separates the voltage trajectory into residual and oscillatory components. This makes it possible to evaluate delayed voltage recovery and voltage oscillations separately.

### What does the residual component represent?

The residual component represents the slow voltage recovery trend after a disturbance. It is used to evaluate delayed voltage recovery and possible OEL or LVRT-related instability.

### What do the intrinsic mode functions represent?

The intrinsic mode functions represent oscillatory components of the voltage trajectory. They are used to evaluate whether voltage oscillations are damped or undamped.

### Why are Lyapunov Exponents used?

Lyapunov Exponents measure whether voltage trajectories converge or diverge. They provide a nonlinear dynamic indicator of stability from measured voltage signals.

### Why is KL divergence used?

KL divergence quantifies the statistical distance between the observed Lyapunov Exponent distribution and a reference distribution, allowing the method to measure the degree of stability.

### How is this different from binary stability classification?

Instead of only saying stable or unstable, the proposed index provides a measure of how close the system is to instability.

### What types of instability can the proposed index detect?

The proposed index can detect recovery-induced instability caused by delayed voltage recovery and oscillation-induced instability caused by undamped voltage oscillations.

### What test system is used?

The method is validated using the Nordic power system with different dynamic load levels and motor-load compositions.

### How fast does the method detect instability?

The method can identify unstable behavior within approximately 3 seconds after a fault in the reported simulation case.

---

## Keywords

short-term voltage stability; STVSI; short-term voltage stability index; voltage trajectory; voltage trajectory stability index; data-driven voltage stability assessment; early detection of voltage instability; voltage instability quantification; delayed voltage recovery; fault-induced delayed voltage recovery; FIDVR; Lyapunov Exponent; maximum Lyapunov Exponent; MLE; Empirical Mode Decomposition; EMD; intrinsic mode functions; IMFs; residual component; KL divergence; Kullback-Leibler divergence; entropy-based stability metric; Over Excitation Limiter; OEL; Low Voltage Ride-Through; LVRT; Nordic power system; PMU-based monitoring; measurement-based stability assessment; oscillation stability index; recovery stability index; dynamic load; Motor A; Motor D; real-time voltage stability monitoring; power system stability.

---

## Citation

```bibtex
@inproceedings{almomani2025novel,
  title     = {Novel Data-Driven Indices for Early Detection and Quantification of Short-Term Voltage Instability from Voltage Trajectories},
  author    = {Almomani, Mohammad and Sarwar, Muhammad and Ajjarapu, Venkataramana},
  booktitle = {2025 IEEE Power & Energy Society General Meeting (PESGM)},
  year      = {2025},
  doi       = {10.1109/PESGM52009.2025.11225182},
  url       = {https://ieeexplore.ieee.org/abstract/document/11225182}
}
```

---

## Links

- **IEEE Xplore:** [https://ieeexplore.ieee.org/abstract/document/11225182](https://ieeexplore.ieee.org/abstract/document/11225182)
- **DOI:** [https://doi.org/10.1109/PESGM52009.2025.11225182](https://doi.org/10.1109/PESGM52009.2025.11225182)
- **Code repository:** Coming soon.
- **Dataset / test cases:** Coming soon.
- **Related work:** Trajectory-Based Nonlinear Indices for Real-Time Monitoring and Quantification of Short-Term Voltage Stability

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Novel Data-Driven Indices for Early Detection and Quantification of Short-Term Voltage Instability from Voltage Trajectories",
  "name": "Novel Data-Driven Indices for Early Detection and Quantification of Short-Term Voltage Instability from Voltage Trajectories",
  "description": "A data-driven short-term voltage stability index for early detection and quantification of voltage instability from voltage trajectories using EMD, Lyapunov Exponents, KL divergence, delayed voltage recovery analysis, and oscillation stability assessment.",
  "author": [
    {
      "@type": "Person",
      "name": "Mohammad Almomani"
    },
    {
      "@type": "Person",
      "name": "Muhammad Sarwar"
    },
    {
      "@type": "Person",
      "name": "Venkataramana Ajjarapu"
    }
  ],
  "keywords": [
    "short-term voltage stability",
    "STVSI",
    "voltage trajectory",
    "data-driven voltage stability assessment",
    "delayed voltage recovery",
    "FIDVR",
    "Lyapunov Exponent",
    "Empirical Mode Decomposition",
    "EMD",
    "intrinsic mode functions",
    "KL divergence",
    "entropy-based stability metric",
    "OEL",
    "LVRT",
    "Nordic power system",
    "PMU-based monitoring",
    "oscillation stability index",
    "recovery stability index"
  ],
  "url": "https://mohammadalmomani.github.io/papers/novel-data-driven-indices-stvsi/",
  "sameAs": [
    "https://ieeexplore.ieee.org/abstract/document/11225182",
    "https://doi.org/10.1109/PESGM52009.2025.11225182"
  ],
  "identifier": "https://doi.org/10.1109/PESGM52009.2025.11225182",
  "isAccessibleForFree": false,
  "publisher": {
    "@type": "Organization",
    "name": "IEEE"
  }
}
</script>
