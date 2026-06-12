---
layout: page
title: "Ringdown Analysis for Low-Frequency Oscillation Identification"
description: "Ringdown analysis for low-frequency oscillation identification using LPC, Prony analysis, Steiglitz-McBride method, adaptive buffer size, PMU measurements, latency-delay compensation, data-dropout compensation, and reduced-order wide-area damping controller modeling."
permalink: /papers/ringdown-analysis-low-frequency-oscillation-identification/
---

# Ringdown Analysis for Low-Frequency Oscillation Identification

**Authors:** Mohammad M. Al-Momani, Khaled Awasa, Abdullah Odienate, Ibrahim Reda, and Seba F. Algharaibeh  
**Research Area:** Low-Frequency Oscillation Identification, Ringdown Analysis, PMU-Based Wide-Area Damping Control  
**Conference:** 2022 Advances in Science and Engineering Technology International Conferences (ASET)  
**DOI:** [10.1109/ASET53988.2022.9735122](https://doi.org/10.1109/ASET53988.2022.9735122)  
**IEEE Xplore:** [https://ieeexplore.ieee.org/document/9735122](https://ieeexplore.ieee.org/document/9735122)

---

## Search-Friendly Title

PMU-Based Ringdown Analysis for Low-Frequency Oscillation Identification Using LPC, Prony Analysis, Steiglitz-McBride, Adaptive Buffer Size, and Wide-Area Damping Control

---

## Short Summary

This paper studies ringdown-analysis methods for identifying low-frequency oscillation modes in power systems and preparing online wide-area damping controllers.

The paper focuses on three key techniques:

- **Linear Prediction Criteria (LPC)** for latency-delay and data-dropout compensation,
- **Prony analysis** for estimating oscillation-mode transfer functions and eigenvalues,
- **Steiglitz-McBride method** for improved oscillation-mode estimation.

The proposed framework uses PMU measurements from a three-area test system after a three-phase fault. The goal is to estimate low-frequency oscillation modes online and extract a reduced-order transfer function that can be used in a wide-area damping controller.

---

## Abstract

Low-frequency oscillations can reduce power system damping and threaten dynamic stability. Wide-area damping controllers require online identification of oscillation modes from measured signals. However, practical communication systems introduce latency delay and data dropout, which can reduce controller performance.

This paper investigates ringdown-analysis techniques for low-frequency oscillation identification. A modified Linear Prediction Criteria method is proposed to compensate for communication latency and missing PMU samples. Prony analysis and the Steiglitz-McBride method are then used to estimate oscillation-mode eigenvalues and transfer functions.

An adaptive buffer-size approach is proposed to reduce dependence on offline damping controllers. A simple order-reduction method based on zero-pole cancellation is applied to obtain a low-order transfer function suitable for wide-area controller implementation.

Simulation results on a three-area test system show that LPC can compensate for data dropout and latency delay, while the Steiglitz-McBride method provides more accurate oscillation-mode estimation than Prony analysis for the tested cases.

---

## Research Gap

Many ringdown-analysis methods assume ideal communication conditions. In real wide-area damping control, PMU data can be affected by:

- communication latency,
- missing samples,
- packet dropout,
- limited buffer size,
- delay before enough post-disturbance data is collected.

Existing offline wide-area damping controllers may also become ineffective when loading, topology, renewable penetration, observability, controllability, or interarea oscillation phase changes.

This paper addresses these gaps by combining LPC-based preprocessing, adaptive buffer-size estimation, Prony analysis, Steiglitz-McBride estimation, and reduced-order transfer-function modeling.

---

## Main Contributions

1. **Ringdown analysis for WADC preprocessing**  
   The paper applies ringdown-analysis methods to prepare online wide-area damping controller models.

2. **LPC-based latency-delay compensation**  
   Linear Prediction Criteria is modified to predict future samples and compensate for communication delay.

3. **LPC-based data-dropout compensation**  
   Missing PMU samples are estimated using previous samples and predicted values.

4. **Adaptive buffer-size strategy**  
   Adaptive buffer size is proposed for LPC, Prony, and Steiglitz-McBride methods to reduce dependence on offline damping controllers.

5. **Prony-based oscillation-mode estimation**  
   Prony analysis is used to estimate low-frequency oscillation eigenvalues and transfer functions from ringdown data.

6. **Steiglitz-McBride-based oscillation-mode estimation**  
   The Steiglitz-McBride method is compared with Prony analysis and shown to provide improved estimation accuracy in the studied case.

7. **Reduced-order WADC model**  
   A high-order estimated model is reduced using zero-pole cancellation to obtain a low-order transfer function suitable for controller design.

8. **Three-area test-system validation**  
   The framework is tested using generator rotor-speed signals from a three-area test system under a three-phase fault.

---

## Method Overview

The proposed workflow follows these steps:

### 1. Collect PMU Ringdown Data

Generator speed signals are collected from PMUs after a three-phase fault in a three-area test system.

### 2. Select the Dominant Signal

The first generator speed signal is selected because it has the highest oscillation amplitude in the studied case.

### 3. Apply LPC Preprocessing

LPC is used to handle:

- future sample prediction,
- time-delay compensation,
- missing-sample recovery,
- packet-dropout compensation.

### 4. Estimate Oscillation Modes

Two ringdown methods are used:

- Prony analysis,
- Steiglitz-McBride estimation.

### 5. Extract Transfer Function

The estimated signal model is converted into a transfer function representation that can be used for wide-area damping control.

### 6. Reduce Model Order

Zero-pole cancellation is applied to reduce a high-order model to a lower-order model suitable for controller implementation.

---

## Linear Prediction Criteria for WADC

The LPC method is used as a preprocessing tool for wide-area damping control.

### Data-Dropout Compensation

When PMU samples are missing, LPC estimates the missing values using previous measured samples. If more than one sample is missing, the algorithm recursively uses estimated values to fill the missing data sequence.

### Latency-Delay Compensation

For communication delay, LPC predicts future samples based on previous measurements. This allows the WADC to operate with compensated signals instead of delayed signals.

### Adaptive Buffer Size

Instead of using a fixed buffer length, the adaptive buffer starts with the first available samples and increases as new data arrives. This reduces the time required before online estimation becomes usable.

---

## Prony Analysis

Prony analysis models the ringdown signal as a sum of damped exponentials or damped sinusoids. It estimates the discrete-time roots and converts them into continuous-time eigenvalues.

The method is useful for identifying:

- oscillation frequency,
- damping,
- modal eigenvalues,
- transfer-function approximations.

The paper shows that a larger model order can improve the Prony-based estimate, but it may also produce a high-order transfer function that needs reduction before controller design.

---

## Steiglitz-McBride Method

The Steiglitz-McBride method estimates a rational transfer function by minimizing the difference between the measured signal and the model response.

In the studied case, the Steiglitz-McBride method provides more accurate signal estimation than Prony analysis. A 7th-order Steiglitz-McBride model gives a close response to the original signal, and higher-order Steiglitz-McBride models reduce error further.

---

## Reduced-Order Modeling for WADC

For controller implementation, a very high-order model is not practical.

The paper estimates a high-order model and then applies zero-pole cancellation. In the reported case:

- the original estimated model has 100th order,
- 91 states are cancelled using a tolerance of 1e-5,
- the reduced model has 9th order,
- the 9th-order reduced model captures the main frequency-domain behavior of the original model.

This makes the reduced model more practical for wide-area damping controller design.

---

## Test System

The paper uses:

- a three-area test system,
- string configuration,
- case A operating condition,
- three-phase fault at bus 9 / L9,
- fault period from 2.0 s to 2.1 s,
- generator rotor-speed PMU signals,
- 50 samples per second PMU reporting rate for a 50 Hz system.

---

## Key Results

- LPC can compensate for missing data samples and communication delay in PMU signals.
- The paper demonstrates data-dropout compensation for a dropout length of 4 samples, equivalent to approximately 80 ms at 50 samples/s.
- The paper demonstrates latency-delay compensation for a 100 ms delay.
- Adaptive buffer size improves online applicability because the estimator can begin working before a large fixed buffer is filled.
- Prony analysis can estimate oscillation-mode transfer functions but may require high model order for good accuracy.
- A 100th-order Prony-based model can be reduced to a 9th-order model through zero-pole cancellation.
- The reduced 9th-order model preserves the main frequency-domain behavior of the original high-order model.
- The reduced 9th-order model is more accurate than a direct 10th-order Prony model in the studied case.
- The Steiglitz-McBride method is more accurate than Prony analysis for the tested signal.
- A 7th-order Steiglitz-McBride model gives a close response to the original signal.
- The paper recommends considering the Steiglitz-McBride method for wide-area controller enhancement.

---

## Why This Paper Matters

This paper is important because it bridges the gap between low-frequency oscillation identification and practical wide-area damping control implementation.

It does not only estimate oscillation modes. It also addresses practical WADC problems:

- communication latency,
- packet dropout,
- online buffer-size limitations,
- model-order reduction,
- transfer-function extraction for controller design.

This makes the paper relevant to PMU-based control, online dynamic stability monitoring, low-inertia systems, and renewable-rich grids.

---

## Search-Friendly Questions

### What is ringdown analysis in power systems?

Ringdown analysis estimates modal properties such as frequency and damping from post-disturbance oscillatory signals. It is commonly used to identify low-frequency electromechanical modes.

### What problem does this paper solve?

This paper solves the problem of identifying low-frequency oscillation modes for online wide-area damping control under practical communication issues such as latency delay and data dropout.

### Why is LPC used?

LPC is used to predict missing or delayed PMU samples, making the measured signal more suitable for real-time wide-area damping control.

### How does LPC handle data dropout?

LPC fills missing samples using predicted values based on previous measured samples.

### How does LPC handle time delay?

LPC predicts future samples according to the delay length, allowing the controller to use compensated rather than delayed measurements.

### What is the role of Prony analysis?

Prony analysis estimates oscillation-mode eigenvalues and transfer functions from ringdown signals.

### What is the role of the Steiglitz-McBride method?

The Steiglitz-McBride method estimates a rational transfer function and provides more accurate signal estimation than Prony analysis in the studied case.

### Why is adaptive buffer size important?

Adaptive buffer size allows online estimation to begin earlier, reducing dependence on an offline damping controller while waiting for a fixed buffer to fill.

### Why is model-order reduction needed?

High-order estimated models are not convenient for controller design. Zero-pole cancellation reduces model order while preserving the main dynamic behavior.

### What test system is used?

The paper uses a three-area test system with PMU-based generator speed measurements after a three-phase fault.

### How is this paper connected to wide-area damping control?

The estimated and reduced transfer function can be used to design or update a wide-area damping controller online.

---

## Keywords

ringdown analysis; low-frequency oscillation identification; low-frequency oscillation; LFO; electromechanical oscillation; interarea mode identification; PMU measurements; phasor measurement unit; wide-area damping controller; WADC; wide-area monitoring system; WAMS; Linear Prediction Criteria; LPC; latency-delay compensation; time-delay compensation; data dropout; packet dropout; Prony analysis; Prony method; Steiglitz-McBride method; McBride method; adaptive buffer size; oscillation-mode transfer function; eigenvalue estimation; zero-pole cancellation; reduced-order model; model-order reduction; three-area test system; generator speed signal; small-signal stability; online damping control; power system stability.

---

## Citation

```bibtex
@inproceedings{almomani2022ringdown,
  title     = {Ringdown Analysis for Low-Frequency Oscillation Identification},
  author    = {Al-Momani, Mohammad M. and Awasa, Khaled and Odienate, Abdullah and Reda, Ibrahim and Algharaibeh, Seba F.},
  booktitle = {2022 Advances in Science and Engineering Technology International Conferences (ASET)},
  year      = {2022},
  doi       = {10.1109/ASET53988.2022.9735122},
  url       = {https://ieeexplore.ieee.org/document/9735122}
}
```

---

## Links

- **IEEE Xplore:** [https://ieeexplore.ieee.org/document/9735122](https://ieeexplore.ieee.org/document/9735122)
- **DOI:** [https://doi.org/10.1109/ASET53988.2022.9735122](https://doi.org/10.1109/ASET53988.2022.9735122)
- **Code repository:** Coming soon.
- **MATLAB implementation:** Coming soon.
- **Related work:** Low Frequency Oscillation Analysis for Dynamic Performance of Power Systems; The Impact of Wind Generation on Low Frequency Oscillation in Power Systems; ANN-Based Low-Frequency Oscillation Damping.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Ringdown Analysis for Low-Frequency Oscillation Identification",
  "name": "Ringdown Analysis for Low-Frequency Oscillation Identification",
  "description": "A PMU-based ringdown analysis framework for low-frequency oscillation identification using LPC, Prony analysis, Steiglitz-McBride estimation, adaptive buffer size, data-dropout compensation, latency-delay compensation, and reduced-order WADC modeling.",
  "author": [
    {
      "@type": "Person",
      "name": "Mohammad M. Al-Momani"
    },
    {
      "@type": "Person",
      "name": "Khaled Awasa"
    },
    {
      "@type": "Person",
      "name": "Abdullah Odienate"
    },
    {
      "@type": "Person",
      "name": "Ibrahim Reda"
    },
    {
      "@type": "Person",
      "name": "Seba F. Algharaibeh"
    }
  ],
  "keywords": [
    "ringdown analysis",
    "low-frequency oscillation",
    "LFO",
    "wide-area damping controller",
    "WADC",
    "PMU",
    "phasor measurement unit",
    "Linear Prediction Criteria",
    "LPC",
    "latency-delay compensation",
    "data dropout",
    "Prony analysis",
    "Steiglitz-McBride",
    "adaptive buffer size",
    "zero-pole cancellation",
    "reduced-order model",
    "three-area test system",
    "power system stability"
  ],
  "url": "https://mohammadalmomani.github.io/papers/ringdown-analysis-low-frequency-oscillation-identification/",
  "sameAs": [
    "https://ieeexplore.ieee.org/document/9735122",
    "https://doi.org/10.1109/ASET53988.2022.9735122"
  ],
  "identifier": "https://doi.org/10.1109/ASET53988.2022.9735122",
  "isAccessibleForFree": false,
  "publisher": {
    "@type": "Organization",
    "name": "IEEE"
  }
}
</script>
