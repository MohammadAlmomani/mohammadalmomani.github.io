---
layout: page
title: "Trajectory-Based Nonlinear Indices for Real-Time Monitoring and Quantification of Short-Term Voltage Stability"
description: "Trajectory-based nonlinear indices for real-time short-term voltage stability monitoring using EMD, Lyapunov exponents, KL divergence, delayed voltage recovery analysis, oscillation stability assessment, and Nordic test system validation."
permalink: /papers/trajectory-based-nonlinear-indices-stvs/
---

# Trajectory-Based Nonlinear Indices for Real-Time Monitoring and Quantification of Short-Term Voltage Stability

**Authors:** Mohammad Almomani, Muhammad Sarwar, and Venkataramana Ajjarapu  
**Research Area:** Short-Term Voltage Stability, Voltage Trajectory Analytics, Real-Time Stability Assessment  
**Status:** arXiv preprint / submitted version  
**arXiv:** [https://arxiv.org/abs/2604.07051](https://arxiv.org/abs/2604.07051)

---

## Search-Friendly Title

Real-Time Short-Term Voltage Stability Monitoring Using EMD, Lyapunov Exponents, KL Divergence, and Voltage Trajectory Indices

---

## Short Summary

This paper presents trajectory-based nonlinear indices for real-time monitoring and quantification of short-term voltage stability (STVS). The method addresses the coexistence of delayed voltage recovery and voltage oscillations, which are often treated separately in existing STVS studies.

The proposed framework decomposes post-fault voltage trajectories into slow recovery and oscillatory components using Empirical Mode Decomposition (EMD). It then applies Lyapunov exponent analysis to each component and uses Kullback-Leibler (KL) divergence to quantify the degree of stability relative to a critical reference signal.

The framework provides two complementary indices:

- **Recovery Stability Index** for delayed voltage recovery and relay-tripping risk.
- **Oscillation Stability Index** for damped or undamped voltage oscillations.

Unlike binary stable/unstable classifiers, the proposed method provides a quantitative stability margin that indicates how close the system is to instability.

---

## Abstract

Existing short-term voltage stability (STVS) methods typically address either voltage oscillations or delayed voltage recovery; however, the coexistence of both phenomena has not been adequately covered in the literature. Moreover, existing real-time STVS assessment methods often provide only binary stability classifications.

This paper proposes novel indices that enable early detection and quantify the degree of stability. The proposed method decomposes post-fault voltage trajectories using Empirical Mode Decomposition (EMD) into residual and oscillatory components. It then employs Lyapunov Exponents (LEs) to characterize the dynamic behavior of each component and evaluates the stability degree using Kullback-Leibler (KL) divergence by comparing the LEs of each component with those of a predefined critical signal.

The proposed indices assess oscillatory stability significantly faster than the traditional LE method applied directly to the original signal. Specifically, they detect stability within 0.6 seconds after a fault, compared to approximately 10 seconds for the conventional LE approach. In addition, the delayed-recovery index can identify generator trips caused by over-excitation limits within 3 seconds, well before the actual trip occurs at approximately 20 seconds, thereby providing operators and controllers sufficient time to take preventive actions.

Thresholds are derived to distinguish between stable and unstable cases while offering a graded measure of the stability margin. Simulation studies on the Nordic test system under varying load conditions demonstrate the effectiveness of the proposed indices.

---

## Research Gap

Existing real-time STVS assessment methods often focus either on delayed voltage recovery or on voltage oscillations, but not both together. In practical power systems, single-phase induction motors can create delayed voltage recovery while three-phase induction motors can create voltage oscillations, causing multi-time-scale voltage dynamics.

Many existing methods also provide only binary stable/unstable classifications. This paper addresses these gaps by separating recovery-driven and oscillatory voltage dynamics and by developing quantitative nonlinear stability indices that measure proximity to instability.

---

## Main Contributions

1. **Separation of slow and fast voltage dynamics**  
   The proposed method separates slow delayed-recovery dynamics from fast oscillatory voltage dynamics using EMD.

2. **Recovery Stability Index**  
   A recovery index is introduced to quantify delayed voltage recovery and predict relay-tripping risk associated with over-excitation limiters and low-voltage protection.

3. **Oscillation Stability Index**  
   An oscillation index is introduced to quantify the proximity of post-fault voltage oscillations to instability.

4. **Lyapunov-exponent-based nonlinear assessment**  
   The method uses finite-size and finite-time Lyapunov exponents to characterize convergence or divergence of voltage trajectory components.

5. **KL-divergence-based stability quantification**  
   KL divergence is used to compare observed divergence-factor distributions with a critical reference distribution.

6. **Fast real-time detection**  
   The proposed oscillation stability index detects stability within approximately 0.6 seconds after a disturbance.

7. **Early delayed-recovery trip prediction**  
   The recovery index identifies generator-tripping risk within approximately 3 seconds, before the actual trip occurs.

8. **Nordic test-system validation**  
   The method is validated using the Nordic test system with dynamic composite load models and varying motor-load penetration levels.

---

## Method Overview

The proposed framework follows these main steps:

### 1. Post-Fault Voltage Trajectory Extraction

Voltage trajectories are collected after a fault or large disturbance.

### 2. Empirical Mode Decomposition

The voltage signal is decomposed into:

- residual component representing slow voltage recovery,
- intrinsic mode functions representing oscillatory behavior.

### 3. Lyapunov Exponent Calculation

- FSLE is applied to residual components to evaluate delayed recovery.
- FTLE is applied to oscillatory components to evaluate damping or divergence.

### 4. Divergence-Factor Construction

The exponential of the Lyapunov exponent is used to form a divergence-factor distribution.

### 5. KL-Divergence Stability Index

KL divergence compares the observed divergence-factor distribution with a critical reference distribution.

### 6. Stability Margin Calculation

The resulting index provides a quantitative measure of proximity to instability.

---

## Proposed Stability Indices

### Recovery Stability Index

The Recovery Stability Index evaluates delayed voltage recovery by analyzing the residual component of the voltage trajectory. It is designed to identify slow recovery conditions that may lead to over-excitation limiter activation, low-voltage protection operation, or generator tripping.

### Oscillation Stability Index

The Oscillation Stability Index evaluates the oscillatory component of the voltage trajectory. It is designed to detect whether post-fault voltage oscillations are damped, sustained, or growing.

---

## Test System

The paper validates the proposed indices using:

- Nordic test system
- Composite dynamic load model
- Three-phase induction motor load components
- Single-phase induction motor load components
- 100 ms three-phase fault scenarios
- Different dynamic motor-load penetration levels
- Generator over-excitation limiter modeling

---

## Key Results

- The proposed oscillation stability index detects stable behavior within approximately **0.6 seconds** after fault clearing.
- The conventional Lyapunov exponent method may require approximately **10 seconds** for classification.
- The recovery index can identify generator-tripping risk within approximately **3 seconds**.
- The delayed-recovery instability may physically occur around **20 seconds**, giving the proposed method early-warning capability.
- The proposed index separates slow recovery behavior from oscillatory behavior, avoiding misleading classification caused by mixed time-scale dynamics.
- Simulation results on the Nordic test system show that the index captures both stability classification and proximity to instability.
- The index reflects the effect of system strength, fault location, and dynamic load composition.

---

## Search-Friendly Questions

### What is short-term voltage stability?

Short-term voltage stability refers to the ability of a power system to maintain acceptable voltages during the first seconds after a large disturbance, especially when fast-acting loads, induction motors, protection devices, and inverter-based resources influence post-fault voltage dynamics.

### What problem does this paper solve?

This paper solves the problem of real-time STVS assessment when delayed voltage recovery and voltage oscillations occur together. Existing methods often treat these two phenomena separately or provide only a binary stable/unstable result.

### How does this method detect short-term voltage instability?

The method decomposes post-fault voltage trajectories using EMD, applies Lyapunov exponent analysis to residual and oscillatory components, and uses KL divergence to quantify the distance from a critical reference signal.

### What is the Recovery Stability Index?

The Recovery Stability Index quantifies the slow recovery component of the voltage trajectory and predicts delayed-recovery-related tripping risk.

### What is the Oscillation Stability Index?

The Oscillation Stability Index quantifies the damping or divergence of voltage oscillations after a disturbance.

### Why is EMD used in this paper?

EMD is used to separate the post-fault voltage trajectory into residual and oscillatory components, allowing delayed recovery and oscillatory instability to be evaluated separately.

### Why are Lyapunov exponents used?

Lyapunov exponents measure whether nearby trajectories converge or diverge. This makes them useful for nonlinear voltage stability assessment from measured voltage trajectories.

### Why is KL divergence used?

KL divergence is used to quantify the statistical distance between the observed divergence-factor distribution and a critical reference distribution, producing a graded stability index.

### How fast is the proposed index?

The oscillation stability index can detect stability within approximately 0.6 seconds after fault clearing. The recovery index can identify delayed-recovery trip risk within approximately 3 seconds.

### What test system is used?

The method is validated using the Nordic test system with dynamic composite load models and varying motor-load penetration levels.

### How is this different from traditional Lyapunov-exponent methods?

Traditional Lyapunov-exponent methods may give delayed or misleading results when slow recovery and oscillatory dynamics coexist. This paper separates the two components first, then evaluates each with a dedicated index.

---

## Keywords

short-term voltage stability; STVS; voltage trajectory; voltage trajectory stability index; delayed voltage recovery; fault-induced delayed voltage recovery; FIDVR; transient voltage response; voltage oscillation; oscillation stability index; recovery stability index; Lyapunov exponent; finite-time Lyapunov exponent; FTLE; finite-size Lyapunov exponent; FSLE; empirical mode decomposition; EMD; multivariate empirical mode decomposition; MEMD; Kullback-Leibler divergence; KL divergence; nonlinear stability index; real-time dynamic stability assessment; PMU-based stability monitoring; voltage stability margin; Nordic test system; dynamic load model; induction motor load; over-excitation limiter; OEL; low-voltage ride-through; LVRT; voltage recovery; power system stability; measurement-based stability assessment.

---

## Citation

```bibtex
@misc{almomani2026trajectory,
  title         = {Trajectory-Based Nonlinear Indices for Real-Time Monitoring and Quantification of Short-Term Voltage Stability},
  author        = {Almomani, Mohammad and Sarwar, Muhammad and Ajjarapu, Venkataramana},
  year          = {2026},
  eprint        = {2604.07051},
  archivePrefix = {arXiv},
  primaryClass  = {eess.SY},
  url           = {https://arxiv.org/abs/2604.07051}
}
```

---

## Links

- **arXiv page:** [https://arxiv.org/abs/2604.07051](https://arxiv.org/abs/2604.07051)
- **PDF:** [https://arxiv.org/pdf/2604.07051](https://arxiv.org/pdf/2604.07051)
- **Code repository:** Coming soon.
- **Dataset / test cases:** Coming soon.
- **Related work:** Short-term voltage stability, delayed voltage recovery, Lyapunov-exponent-based stability assessment, and voltage trajectory analytics.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Trajectory-Based Nonlinear Indices for Real-Time Monitoring and Quantification of Short-Term Voltage Stability",
  "name": "Trajectory-Based Nonlinear Indices for Real-Time Monitoring and Quantification of Short-Term Voltage Stability",
  "description": "A trajectory-based nonlinear framework for real-time short-term voltage stability monitoring using EMD, Lyapunov exponents, KL divergence, delayed voltage recovery analysis, oscillation stability assessment, and Nordic test system validation.",
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
    "STVS",
    "voltage trajectory",
    "delayed voltage recovery",
    "FIDVR",
    "Lyapunov exponent",
    "finite-time Lyapunov exponent",
    "finite-size Lyapunov exponent",
    "empirical mode decomposition",
    "EMD",
    "Kullback-Leibler divergence",
    "KL divergence",
    "recovery stability index",
    "oscillation stability index",
    "real-time dynamic stability assessment",
    "PMU-based stability monitoring",
    "Nordic test system"
  ],
  "url": "https://mohammadalmomani.github.io/papers/trajectory-based-nonlinear-indices-stvs/",
  "sameAs": [
    "https://arxiv.org/abs/2604.07051"
  ],
  "identifier": "arXiv:2604.07051",
  "isAccessibleForFree": true
}
</script>
