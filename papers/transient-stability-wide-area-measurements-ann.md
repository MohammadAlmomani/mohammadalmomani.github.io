---
layout: page
title: "Prediction of Transient Stability Using Wide Area Measurements Based on ANN"
description: "ANN-based transient stability prediction using WAMS, PMU measurements, IEEE 39-bus New England test system, generator speeds, pre-fault, during-fault and post-fault data, NEPLAN, MATLAB, and 100 ms post-fault prediction."
permalink: /papers/transient-stability-wide-area-measurements-ann/
---

# Prediction of Transient Stability Using Wide Area Measurements Based on ANN

**Authors:** Mohammad M. Al-Momani and Seba F. Al-Gharaibeh  
**Research Area:** Transient Stability Prediction, Wide-Area Monitoring, ANN-Based Stability Assessment  
**Journal:** International Journal of Emerging Trends in Engineering Research  
**Volume / Issue:** Volume 9, Number 11, 2021  
**Pages:** 1373–1378  
**DOI:** [10.30534/ijeter/2021/029112021](https://doi.org/10.30534/ijeter/2021/029112021)

---

## Search-Friendly Title

ANN-Based Transient Stability Prediction Using Wide-Area Measurements, PMU Data, Generator Speeds, IEEE 39-Bus System, NEPLAN, and MATLAB

---

## Short Summary

This paper proposes an artificial neural network method for early prediction of power system transient stability using wide-area measurements.

The method uses real-time dynamic data collected by WAMS / PMU infrastructure. The ANN input includes generator-speed information before, during, and after a fault. The output is the overall system stability status:

- stable,
- unstable.

The method is tested on the IEEE 39-bus New England test system. Dynamic simulations are performed in NEPLAN, and the ANN is designed in MATLAB 2019a.

The proposed model can predict an unstable state within approximately **100 ms after fault clearing**.

---

## Abstract

Transient stability prediction is the first step in a dynamic control system designed to prevent emergency or unstable operating conditions. This paper proposes an ANN-based method for early prediction of power system transient stability after fault clearing using real-time dynamic data collected from wide-area measurement systems.

A dataset is generated from contingency analysis on the IEEE 39-bus test system. Pre-fault, during-fault, and post-fault generator speeds are used as ANN inputs. The system status, stable or unstable, is used as the ANN output.

The IEEE 39-bus system is simulated in NEPLAN, and MATLAB 2019a is used to design the ANN. The proposed model can predict instability within 100 ms after the fault.

---

## Research Gap

Transient stability assessment is traditionally handled using:

- time-domain simulation,
- transient energy function methods,
- offline contingency analysis,
- model-based stability tools.

These approaches can be computationally expensive or too slow for real-time emergency control.

Machine learning can provide fast online prediction, but the model must use features that are available quickly after fault clearing. This paper addresses that need by using generator-speed measurements from WAMS before, during, and immediately after the fault.

---

## Main Contributions

1. **ANN-based transient stability prediction**  
   The paper develops a multilayer perceptron model for binary transient stability classification.

2. **Wide-area measurement input**  
   The model uses generator-speed data that can be obtained through PMU / WAMS infrastructure.

3. **Pre-fault, during-fault, and post-fault features**  
   The ANN input captures dynamic behavior over the fault event window.

4. **Fast post-fault decision**  
   The model predicts instability within 100 ms after fault clearing.

5. **IEEE 39-bus validation**  
   The method is tested on the IEEE 39-bus New England test system.

6. **NEPLAN and MATLAB implementation**  
   NEPLAN is used for dynamic simulation, and MATLAB 2019a is used for ANN design.

7. **Contingency-based dataset generation**  
   The dataset includes multiple contingencies, operating conditions, and fault clearing times.

---

## Method Overview

The proposed framework follows these steps:

### 1. Simulate Contingencies

Three-phase faults are applied at:

- generator buses,
- load buses,
- transmission line midpoints,
- transformer-related locations.

### 2. Vary Operating Conditions

The system is simulated under several loading conditions, including base case and ±10% loading.

### 3. Generate Stability Labels

Each case is labeled as stable or unstable based on the final rotor-angle behavior.

### 4. Extract ANN Features

The input features include generator speeds:

- before the fault,
- during the fault,
- after fault clearing.

### 5. Train Multilayer Perceptron

A feedforward ANN / multilayer perceptron is trained in MATLAB.

### 6. Predict Stability Online

After a fault is cleared, the trained ANN predicts whether the system will remain stable or become unstable.

---

## Test System

The method is tested on the IEEE 39-bus New England system.

The system includes:

- 10 generators,
- 46 transmission lines,
- 12 transformers,
- detailed generator models,
- exciters,
- turbines,
- stabilizers,
- governors.

---

## Dataset

The paper reports:

- 300 total operating cases,
- 152 stable cases,
- 148 unstable cases,
- three loading levels,
- three-phase faults,
- randomly selected clearing times from 5 to 12 cycles.

The ANN uses 20 inputs and one output.

---

## Key Results

- The ANN predicts transient stability using generator-speed measurements.
- The method can identify unstable conditions within approximately 100 ms after fault clearing.
- The model supports early emergency control actions.
- Generator speeds before, during, and after the fault provide useful dynamic information for classification.
- The method is suitable for WAMS-based wide-area protection and control.
- The IEEE 39-bus test system is used to validate the approach.
- NEPLAN is used for simulation, and MATLAB is used for ANN training.

---

## Search-Friendly Questions

### What is the main goal of this paper?

The main goal is to predict transient stability quickly after fault clearing using ANN and wide-area measurements.

### What input data does the ANN use?

The ANN uses pre-fault, during-fault, and post-fault generator speeds.

### What is the output of the ANN?

The output is the system stability status: stable or unstable.

### What test system is used?

The IEEE 39-bus New England test system is used.

### How fast can the method predict instability?

The proposed model can predict instability within about 100 ms after fault clearing.

### What software is used?

NEPLAN is used for dynamic simulations, and MATLAB 2019a is used for ANN design.

### How many cases are used?

The paper reports 300 cases, including 152 stable and 148 unstable cases.

### Why is this important for WAMS?

Fast prediction enables wide-area protection and control systems to initiate emergency actions before instability develops.

---

## Keywords

transient stability prediction; transient stability assessment; ANN; artificial neural network; multilayer perceptron; MLP; WAMS; wide-area monitoring system; PMU; phasor measurement unit; wide-area protection and control; WAPAC; IEEE 39-bus system; New England test system; generator speed; pre-fault data; during-fault data; post-fault data; NEPLAN; MATLAB 2019a; emergency control; power system stability; machine learning stability assessment; real-time stability prediction.

---

## Citation

```bibtex
@article{almomani2021transient,
  title   = {Prediction of Transient Stability Using Wide Area Measurements Based on ANN},
  author  = {Al-Momani, Mohammad M. and Al-Gharaibeh, Seba F.},
  journal = {International Journal of Emerging Trends in Engineering Research},
  volume  = {9},
  number  = {11},
  pages   = {1373--1378},
  year    = {2021},
  doi     = {10.30534/ijeter/2021/029112021},
  url     = {https://doi.org/10.30534/ijeter/2021/029112021}
}
```

---

## Links

- **DOI:** [https://doi.org/10.30534/ijeter/2021/029112021](https://doi.org/10.30534/ijeter/2021/029112021)
- **Code repository:** Coming soon.
- **NEPLAN / MATLAB files:** Coming soon.
- **Dataset:** Coming soon.
- **Related work:** ANN-Based Low-Frequency Oscillation Damping; Ringdown Analysis for Low-Frequency Oscillation Identification; Islanding Detection Method Based Artificial Neural Network.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Prediction of Transient Stability Using Wide Area Measurements Based on ANN",
  "name": "Prediction of Transient Stability Using Wide Area Measurements Based on ANN",
  "description": "ANN-based transient stability prediction using WAMS, PMU measurements, IEEE 39-bus New England test system, generator speeds, pre-fault, during-fault and post-fault data, NEPLAN, MATLAB, and 100 ms post-fault prediction.",
  "author": [
    {"@type": "Person", "name": "Mohammad M. Al-Momani"},
    {"@type": "Person", "name": "Seba F. Al-Gharaibeh"}
  ],
  "keywords": [
    "transient stability prediction",
    "ANN",
    "wide-area measurements",
    "WAMS",
    "PMU",
    "IEEE 39-bus",
    "generator speed",
    "NEPLAN",
    "MATLAB",
    "wide-area protection and control",
    "machine learning stability assessment"
  ],
  "url": "https://mohammadalmomani.github.io/papers/transient-stability-wide-area-measurements-ann/",
  "sameAs": [
    "https://doi.org/10.30534/ijeter/2021/029112021"
  ],
  "identifier": "https://doi.org/10.30534/ijeter/2021/029112021",
  "isAccessibleForFree": true,
  "publisher": {
    "@type": "Organization",
    "name": "International Journal of Emerging Trends in Engineering Research"
  }
}
</script>
