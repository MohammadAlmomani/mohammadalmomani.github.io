---
layout: page
title: "Enhanced Entropy-Based Metric for Characterization of Delayed Voltage Recovery"
description: "Enhanced voltage recovery violation index for FIDVR characterization using EMD, KL divergence, entropy-based metrics, over-voltage detection, under-voltage detection, Nordic system simulations, and voltage recovery envelopes."
permalink: /papers/enhanced-entropy-based-metric-delayed-voltage-recovery/
---

# Enhanced Entropy-Based Metric for Characterization of Delayed Voltage Recovery

**Authors:** Mohammad Almomani, Muhammad Sarwar, and Venkataramana Ajjarapu  
**Research Area:** Delayed Voltage Recovery, FIDVR, Voltage Recovery Violation Detection, Entropy-Based Metrics  
**Venue:** 2025 IEEE Power & Energy Society General Meeting (PESGM)  
**DOI:** [10.1109/PESGM52009.2025.11225642](https://doi.org/10.1109/PESGM52009.2025.11225642)  
**IEEE Xplore:** [https://ieeexplore.ieee.org/abstract/document/11225642](https://ieeexplore.ieee.org/abstract/document/11225642)

---

## Search-Friendly Title

Enhanced Voltage Recovery Violation Index for FIDVR Using EMD, KL Divergence, Over-Voltage Detection, and Under-Voltage Detection

---

## Short Summary

This paper proposes an **Enhanced Voltage Recovery Violation Index (EVRVI)** for quantifying fault-induced delayed voltage recovery (FIDVR) and voltage recovery violations.

The method improves traditional entropy-based KL-divergence metrics by using **Empirical Mode Decomposition (EMD)** to extract upper and lower voltage envelopes from post-fault voltage signals. These envelopes allow the method to separately detect:

- under-voltage recovery violations,
- over-voltage recovery violations,
- oscillatory recovery behavior,
- delayed voltage recovery events.

The proposed EVRVI is validated using the Nordic power system with more than **245,000 simulated scenarios**.

---

## Abstract

Ensuring accurate voltage violation detection in power systems is critical for operational reliability. This paper introduces an Enhanced Voltage Recovery Violation Index (EVRVI), a comprehensive index designed to quantify fault-induced delayed voltage recovery.

EVRVI enhances traditional entropy-based methods by leveraging Empirical Mode Decomposition (EMD) to extract key features from the voltage signal. These features are then used to quantify over-voltage and under-voltage events.

Simulations on the Nordic system involving more than 245,000 scenarios demonstrate EVRVI’s superior ability to identify and categorize voltage recovery issues compared with the traditional entropy-based measure. EVRVI significantly reduces false negatives in voltage violation detection and provides a reliable framework for over-voltage detection, making it a useful tool for modern power system studies.

---

## Research Gap

Traditional entropy-based KL-divergence methods are useful for quantifying delayed voltage recovery, but they have limitations when voltage trajectories include oscillations, over-voltage behavior, or complex recovery shapes.

These methods may produce:

- false positives when over-voltage is misclassified as a voltage recovery violation,
- false negatives when actual under-voltage violations are missed,
- inaccurate results when oscillations occur during delayed voltage recovery,
- inconsistent detection depending on histogram partitions and distribution parameters.

This paper addresses these gaps by using EMD-based upper and lower envelopes to separately quantify over-voltage and under-voltage recovery behavior.

---

## Main Contributions

1. **Enhanced Voltage Recovery Violation Index**  
   The paper introduces EVRVI as a comprehensive index for quantifying delayed voltage recovery and voltage recovery violations.

2. **Over-voltage and under-voltage detection**  
   EVRVI separately detects over-voltage and under-voltage violations instead of treating all voltage deviations as one class.

3. **EMD-based voltage envelope extraction**  
   Empirical Mode Decomposition is used to extract monotonic upper and lower envelopes from voltage signals.

4. **Improved FIDVR characterization**  
   The method improves characterization of fault-induced delayed voltage recovery, especially when oscillations are present.

5. **Reduced false negatives**  
   Compared with traditional KL divergence, EVRVI significantly reduces missed voltage violations.

6. **Large-scale Nordic system validation**  
   The method is validated using **245,729 scenarios** on the Nordic system.

7. **Robustness to parameter sensitivity**  
   EVRVI is less sensitive to the number of voltage partitions and variance settings than the traditional KL-divergence method.

---

## Method Overview

The proposed EVRVI framework follows these steps:

### 1. Post-Fault Voltage Signal Collection

Voltage trajectories are collected after a fault or disturbance.

### 2. Empirical Mode Decomposition

EMD decomposes the voltage signal into:

- intrinsic mode functions,
- residual trend.

### 3. Upper and Lower Envelope Extraction

The decomposed components are used to construct:

- an upper envelope for over-voltage recovery assessment,
- a lower envelope for under-voltage recovery assessment.

### 4. Probability Distribution Construction

The upper and lower envelope values are converted into probability distributions.

### 5. KL-Divergence Calculation

KL divergence compares the envelope distributions with an ideal normal distribution centered at 1 p.u.

### 6. EVRVI Calculation

Two EVRVI components are calculated:

- **EVRVI+** for over-voltage violations,
- **EVRVI−** for under-voltage violations.

### 7. Violation Classification

The computed EVRVI values are compared with reference violation thresholds to determine whether a voltage recovery violation occurred.

---

## Proposed Index

### EVRVI−: Under-Voltage Violation Index

EVRVI− measures under-voltage recovery violations using the lower envelope of the voltage signal. It is designed to identify delayed voltage recovery and FIDVR-type events.

### EVRVI+: Over-Voltage Violation Index

EVRVI+ measures over-voltage violations using the upper envelope of the voltage signal. It is designed to detect voltage overshoot and over-voltage recovery problems that traditional FIDVR metrics may not properly classify.

---

## Why EMD Is Used

EMD is used because delayed voltage recovery signals can be nonlinear, non-stationary, and oscillatory. By decomposing the signal and extracting upper/lower envelopes, EVRVI can compare monotonic voltage recovery profiles instead of comparing raw oscillatory signals directly.

This improves the reliability of KL-divergence-based voltage recovery assessment.

---

## Test System

The proposed method is validated using:

- Nordic power system,
- operating point A,
- composite load model,
- induction motor load components,
- dynamic voltage recovery scenarios,
- over-voltage scenarios,
- under-voltage scenarios,
- oscillatory voltage recovery scenarios,
- 10-second voltage recovery simulation window,
- more than 245,000 simulated cases.

---

## Key Results

- The study analyzes **245,729 scenarios**.
- The dataset includes:
  - **216,477 non-violation cases**,
  - **29,252 violation cases**.
- Traditional KL divergence detects many non-violation cases correctly but has a high false negative rate for violation cases.
- Traditional KL divergence misclassifies **12,030 violation cases** as false negatives.
- The traditional KL-divergence false negative rate is **41.1%** for violation cases.
- The traditional KL-divergence accuracy is:
  - **58.9%** for violation cases,
  - **99.7%** for non-violation cases.
- EVRVI accurately classifies the reported cases without errors in the tested dataset.
- The proposed EVRVI successfully detects both:
  - under-voltage violation with **EVRVI− ≈ 2.76**,
  - over-voltage violation with **EVRVI+ ≈ 1.8**.
- EVRVI requires approximately **1.2×** the computation time of traditional KL divergence due to envelope extraction.

---

## Search-Friendly Questions

### What is EVRVI?

EVRVI stands for Enhanced Voltage Recovery Violation Index. It is an index for detecting and quantifying delayed voltage recovery, under-voltage violations, and over-voltage violations from post-fault voltage trajectories.

### What problem does this paper solve?

This paper solves the problem of inaccurate voltage recovery violation detection when traditional entropy-based KL-divergence metrics face oscillations, over-voltage behavior, or complex delayed recovery profiles.

### What is fault-induced delayed voltage recovery?

Fault-induced delayed voltage recovery, or FIDVR, occurs when voltage does not recover to an acceptable level within the required time after a fault. It is often associated with induction motor stalling and dynamic load behavior.

### Why is traditional KL divergence not enough?

Traditional KL divergence can miss actual under-voltage violations, incorrectly classify over-voltage behavior, and struggle with oscillatory voltage recovery signals.

### How does EVRVI improve voltage recovery detection?

EVRVI uses EMD to extract upper and lower voltage envelopes, then applies KL divergence to those envelopes. This allows separate detection of over-voltage and under-voltage violations.

### What does EVRVI− measure?

EVRVI− measures under-voltage recovery violations using the lower envelope of the voltage trajectory.

### What does EVRVI+ measure?

EVRVI+ measures over-voltage violations using the upper envelope of the voltage trajectory.

### Why is EMD used in EVRVI?

EMD is used to decompose nonlinear and non-stationary voltage signals and extract envelope-based features that better represent voltage recovery behavior.

### What test system is used?

The method is tested on the Nordic power system using large-scale simulation scenarios.

### How many scenarios are tested?

The paper reports more than 245,000 simulated scenarios.

### How does EVRVI compare with traditional KL divergence?

Traditional KL divergence has a high false negative rate for voltage violation cases, while EVRVI improves detection accuracy by separating over-voltage and under-voltage recovery behavior.

### Can EVRVI detect over-voltage?

Yes. EVRVI includes EVRVI+, which is specifically designed to detect over-voltage violations.

---

## Keywords

enhanced voltage recovery violation index; EVRVI; voltage recovery violation index; delayed voltage recovery; fault-induced delayed voltage recovery; FIDVR; entropy-based metric; KL divergence; Kullback-Leibler divergence; empirical mode decomposition; EMD; voltage recovery envelope; upper envelope; lower envelope; over-voltage detection; under-voltage detection; voltage violation detection; voltage recovery assessment; voltage performance; Nordic power system; composite load model; induction motor load; short-term voltage stability; transient voltage recovery; oscillatory voltage recovery; voltage stability index; power system reliability; power system resilience.

---

## Citation

```bibtex
@inproceedings{almomani2025enhanced,
  title     = {Enhanced Entropy-Based Metric for Characterization of Delayed Voltage Recovery},
  author    = {Almomani, Mohammad and Sarwar, Muhammad and Ajjarapu, Venkataramana},
  booktitle = {2025 IEEE Power \& Energy Society General Meeting (PESGM)},
  year      = {2025},
  doi       = {10.1109/PESGM52009.2025.11225642},
  url       = {https://ieeexplore.ieee.org/abstract/document/11225642}
}
```

---

## Links

- **IEEE Xplore:** [https://ieeexplore.ieee.org/abstract/document/11225642](https://ieeexplore.ieee.org/abstract/document/11225642)
- **DOI:** [https://doi.org/10.1109/PESGM52009.2025.11225642](https://doi.org/10.1109/PESGM52009.2025.11225642)
- **Code repository:** Coming soon.
- **Dataset / test cases:** Coming soon.
- **Related work:** Novel Data-Driven Indices for Early Detection and Quantification of Short-Term Voltage Instability from Voltage Trajectories

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Enhanced Entropy-Based Metric for Characterization of Delayed Voltage Recovery",
  "name": "Enhanced Entropy-Based Metric for Characterization of Delayed Voltage Recovery",
  "description": "An enhanced voltage recovery violation index for FIDVR characterization using EMD, KL divergence, over-voltage detection, under-voltage detection, and Nordic power system simulations.",
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
    "EVRVI",
    "enhanced voltage recovery violation index",
    "delayed voltage recovery",
    "FIDVR",
    "KL divergence",
    "Kullback-Leibler divergence",
    "Empirical Mode Decomposition",
    "EMD",
    "over-voltage detection",
    "under-voltage detection",
    "voltage recovery violation",
    "Nordic power system",
    "short-term voltage stability",
    "voltage performance",
    "entropy-based metric"
  ],
  "url": "https://mohammadalmomani.github.io/papers/enhanced-entropy-based-metric-delayed-voltage-recovery/",
  "sameAs": [
    "https://ieeexplore.ieee.org/abstract/document/11225642",
    "https://doi.org/10.1109/PESGM52009.2025.11225642"
  ],
  "identifier": "https://doi.org/10.1109/PESGM52009.2025.11225642",
  "isAccessibleForFree": false,
  "publisher": {
    "@type": "Organization",
    "name": "IEEE"
  }
}
</script>
