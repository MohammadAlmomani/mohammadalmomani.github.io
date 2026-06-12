---
layout: page
title: "Damping Undammed Low Frequency Oscillations in Power Systems: An ANN-Based Approach Using Pre-Disturbance Data"
description: "ANN-based online wide-area damping controller for low-frequency oscillations using pre-disturbance PMU data, eigenvalue prediction, small-signal stability, partial observability, PMU placement, and three-area power system validation."
permalink: /papers/ann-damping-low-frequency-oscillations/
---

# Damping Undammed Low Frequency Oscillations in Power Systems: An ANN-Based Approach Using Pre-Disturbance Data

**Authors:** Mohammad M. Al-Momani, Amneh Al-Mbaideen, and Seba F. Al-Gharaibeh  
**Research Area:** Low-Frequency Oscillation Damping, ANN-Based Stability Monitoring, PMU-Based Wide-Area Control  
**Journal:** Jordan Journal of Energy  
**Volume / Issue:** Volume 1, Number 2, 2023  
**Article Link:** [https://dsr.mutah.edu.jo/index.php/jje/article/view/716](https://dsr.mutah.edu.jo/index.php/jje/article/view/716)

---

## Search-Friendly Title

ANN-Based Online Damping of Low-Frequency Oscillations Using Pre-Disturbance PMU Data and Eigenvalue Prediction

---

## Short Summary

This paper proposes an artificial neural network (ANN)-based online wide-area damping approach for low-frequency oscillations (LFOs) in power systems.

The method uses **pre-disturbance PMU data** to predict electromechanical eigenvalues before a disturbance occurs. Instead of relying only on post-disturbance ringdown analysis or offline damping controllers, the proposed method estimates local and interarea oscillation modes online using measurements such as:

- generator rotor angles,
- generator reactive powers,
- bus voltage angles,
- generator and load bus angles.

The approach is validated on a three-area test system using 406 training scenarios and 160 validation cases. The best-performing ANN input set is based on generator and load bus angles.

---

## Abstract

Low-frequency oscillations can reduce power system damping and may lead to system collapse if not properly detected and controlled. This paper studies undamped low-frequency oscillations and proposes an online damping controller based on artificial neural networks.

Traditional model-based methods for small-signal stability analysis can be difficult to apply online in large-scale systems because they require accurate models, system linearization, and updated operating conditions. Measurement-based methods using PMU data provide a practical alternative.

The proposed approach uses pre-disturbance measurements from phasor measurement units to train a feedforward ANN with backpropagation. The ANN predicts the real and imaginary parts of local and interarea eigenvalues. The study also investigates the impact of partial observability by comparing SCADA-only data with PMU-enhanced data.

The results show that ANN-based eigenvalue prediction can support online oscillation mode identification, damping assessment, and PMU deployment strategy.

---

## Research Gap

Most low-frequency oscillation monitoring methods rely on either:

- model-based small-signal stability analysis,
- post-disturbance ringdown data,
- offline controller design,
- complete system observability.

However, practical power systems may not be fully observable by PMUs, and waiting for post-disturbance data can delay damping action.

This paper addresses this gap by using **pre-disturbance PMU measurements** to predict electromechanical eigenvalues online. The method also studies how partial PMU observability affects eigenvalue prediction accuracy.

---

## Main Contributions

1. **ANN-based online eigenvalue prediction**  
   The paper develops a feedforward ANN model to predict local and interarea electromechanical modes from pre-disturbance measurements.

2. **Use of pre-disturbance PMU data**  
   Unlike post-disturbance ringdown methods, the proposed approach uses measurements available before the disturbance.

3. **Low-frequency oscillation damping support**  
   The ANN prediction can support online damping-control decisions and wide-area monitoring.

4. **Partial-observability analysis**  
   The paper studies how prediction accuracy changes when only part of the system is measured by PMUs and the remaining data comes from SCADA.

5. **Comparison of different input feature sets**  
   Four ANN input sets are evaluated:
   - generator bus angles,
   - generator reactive powers,
   - bus voltage angles,
   - generator and load bus angles.

6. **Training over many operating scenarios**  
   The ANN is trained using 406 scenarios covering different loading conditions and transmission-line topologies.

7. **Validation using additional cases**  
   The model is evaluated using 160 validation cases with varied load and capacitor values.

8. **PMU placement insight for oscillation monitoring**  
   The study shows how PMU location affects eigenvalue prediction accuracy and can guide PMU installation priority.

---

## Method Overview

The proposed method follows these steps:

### 1. Generate Operating Scenarios

A three-area test system is simulated under multiple loading conditions and transmission-line topologies.

### 2. Compute Electromechanical Modes

Small-signal analysis is used to compute eigenvalues for:

- three local modes,
- two interarea modes.

Each eigenvalue has a real and imaginary component, giving ten ANN outputs.

### 3. Build ANN Input Features

Four input-feature configurations are tested:

- generator bus angles,
- generator reactive powers,
- all bus voltage angles,
- generator and load bus angles.

### 4. Train Feedforward ANN

A feedforward ANN with backpropagation is trained in MATLAB. The dataset is divided into:

- 80% training,
- 10% validation,
- 10% testing.

### 5. Select the Best ANN Architecture

For each input set, different network architectures are tested. The best structure is selected based on minimum mean square error.

### 6. Validate Eigenvalue Prediction

The trained ANN predicts local and interarea eigenvalues for validation cases.

### 7. Analyze Partial Observability

The model is tested under SCADA-only data and PMU-enhanced partial observability to evaluate the benefit of PMU placement.

---

## ANN Input Features and Architectures

The study evaluates four measurement configurations.

| Input Feature Set | Number of Layers | Neurons Per Layer |
|---|---:|---|
| Generator bus angles | 4 | [10, 6, 7, 10] |
| Generator reactive power | 4 | [10, 10, 11, 11] |
| Bus voltage angles | 4 | [7, 11, 9, 11] |
| Generator and load bus angles | 4 | [11, 8, 10, 11] |

The best input configuration is the **generator and load bus angle-based system**, which achieves the lowest validation performance.

---

## Training and Validation Data

The ANN model is trained using:

- 406 total training scenarios,
- multiple load variations,
- multiple operating points,
- multiple line-outage topologies,
- 160 additional validation cases.

The output vector includes ten values:

- real parts of five eigenvalues,
- imaginary parts of five eigenvalues.

The five oscillation modes include:

- three local modes,
- two interarea modes.

---

## Key Results

- The generator and load bus angle-based ANN gives the best validation performance.
- Best validation performance values are:
  - 0.012152 at epoch 291 for generator bus angle input,
  - 0.015585 at epoch 62 for generator reactive power input,
  - 0.011733 at epoch 138 for bus voltage angle input,
  - 0.0096272 at epoch 123 for generator and load bus angle input.
- The confusion matrix reports approximately **98.3% correct predictions** and **1.7% incorrect predictions**.
- The maximum histogram error for training samples is approximately **0.002952**.
- The local-area mode prediction is more accurate than the interarea mode prediction.
- For partial observability with one PMU, bus 4 gives the best improvement.
- With one PMU at bus 4, the average absolute error decreases from 0.068022 for SCADA-only data to 0.066511.
- With two PMUs, the best locations are buses 4 and 11.
- With three PMUs at buses 4, 11, and 14, the partially observable system becomes very close to the true-data prediction case.

---

## Partial Observability and PMU Placement

The paper evaluates how PMU placement affects online eigenvalue prediction.

### One PMU Case

Candidate PMU locations:

- bus 4,
- bus 11,
- bus 14.

The best first PMU location is **bus 4**.

### Two PMU Case

Candidate pairs:

- buses 4 and 11,
- buses 4 and 14.

The best two-PMU configuration is **bus 4 and bus 11**.

### Three PMU Case

With PMUs at:

- bus 4,
- bus 11,
- bus 14,

the system becomes fully observable by PMUs, and the eigenvalue prediction becomes close to the true-data case.

---

## Why This Paper Matters

This paper connects three important research directions:

1. **Low-frequency oscillation monitoring**  
   It predicts local and interarea modes using measurement data.

2. **ANN-based power system stability assessment**  
   It uses data-driven models to estimate eigenvalues without requiring full online linearization.

3. **PMU placement for dynamic monitoring**  
   It shows that PMU placement can be optimized not only for static observability but also for oscillation-mode prediction accuracy.

This makes the work important for modern wide-area monitoring systems, low-inertia systems, and renewable-rich power grids.

---

## Search-Friendly Questions

### What is the main goal of this paper?

The main goal is to use an artificial neural network to predict low-frequency oscillation modes from pre-disturbance PMU data and support online damping control.

### What are low-frequency oscillations in power systems?

Low-frequency oscillations are electromechanical oscillations that occur between generators or groups of generators. If poorly damped, they can threaten small-signal stability and may lead to system collapse.

### Why does this paper use ANN?

ANN is used to learn the relationship between pre-disturbance measurements and electromechanical eigenvalues, enabling fast online prediction.

### What is different about this ANN approach?

The method uses pre-disturbance measurements rather than waiting for post-disturbance ringdown data.

### What measurements are used?

The paper tests generator angles, generator reactive powers, bus voltage angles, and generator/load bus angles.

### Which input gives the best ANN performance?

The generator and load bus angle-based input gives the best validation performance.

### How many scenarios are used?

The ANN is trained using 406 scenarios and validated using 160 additional cases.

### What modes are predicted?

The model predicts three local modes and two interarea modes, including real and imaginary eigenvalue components.

### How does partial observability affect the model?

Partial observability increases prediction error compared with true data, but adding PMUs reduces the error.

### What is the best first PMU location in the partial-observability study?

The best first PMU location is bus 4.

### What is the best two-PMU configuration?

The best two-PMU configuration is buses 4 and 11.

### How is this paper related to wide-area damping control?

The predicted eigenvalues can inform online damping-controller actions and support wide-area oscillation monitoring.

---

## Keywords

low-frequency oscillation; LFO; undamped low-frequency oscillation; undammed low-frequency oscillation; power system oscillation damping; ANN-based damping controller; artificial neural network; eigenvalue prediction; electromechanical modes; local modes; interarea modes; small-signal stability; pre-disturbance data; PMU data; phasor measurement unit; wide-area monitoring system; WAMS; wide-area damping controller; online damping control; ringdown analysis; measurement-based mode identification; partial observability; PMU placement; SCADA data; three-area test system; generator angles; bus voltage angles; generator reactive power; MATLAB neural network; power system stability.

---

## Citation

```bibtex
@article{almomani2023damping,
  title   = {Damping Undammed Low Frequency Oscillations in Power Systems: An ANN-Based Approach Using Pre-Disturbance Data},
  author  = {Al-Momani, Mohammad M. and Al-Mbaideen, Amneh and Al-Gharaibeh, Seba F.},
  journal = {Jordan Journal of Energy},
  volume  = {1},
  number  = {2},
  pages   = {6--20},
  year    = {2023},
  url     = {https://dsr.mutah.edu.jo/index.php/jje/article/view/716}
}
```

---

## Links

- **Journal page:** [https://dsr.mutah.edu.jo/index.php/jje/article/view/716](https://dsr.mutah.edu.jo/index.php/jje/article/view/716)
- **Code repository:** Coming soon.
- **Dataset / test cases:** Coming soon.
- **Related work:** Ringdown Analysis for Low-Frequency Oscillation Identification; Low Frequency Oscillation Analysis for Dynamic Performance of Power Systems; The Impact of Wind Generation on Low Frequency Oscillation in Power Systems.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Damping Undammed Low Frequency Oscillations in Power Systems: An ANN-Based Approach Using Pre-Disturbance Data",
  "name": "Damping Undammed Low Frequency Oscillations in Power Systems: An ANN-Based Approach Using Pre-Disturbance Data",
  "description": "An ANN-based online wide-area damping approach for low-frequency oscillations using pre-disturbance PMU data, eigenvalue prediction, partial observability analysis, and three-area power system validation.",
  "author": [
    {
      "@type": "Person",
      "name": "Mohammad M. Al-Momani"
    },
    {
      "@type": "Person",
      "name": "Amneh Al-Mbaideen"
    },
    {
      "@type": "Person",
      "name": "Seba F. Al-Gharaibeh"
    }
  ],
  "keywords": [
    "low-frequency oscillation",
    "LFO",
    "ANN-based damping controller",
    "artificial neural network",
    "pre-disturbance PMU data",
    "eigenvalue prediction",
    "local modes",
    "interarea modes",
    "small-signal stability",
    "phasor measurement unit",
    "PMU",
    "wide-area monitoring system",
    "partial observability",
    "PMU placement",
    "SCADA",
    "three-area test system"
  ],
  "url": "https://mohammadalmomani.github.io/papers/ann-damping-low-frequency-oscillations/",
  "sameAs": [
    "https://dsr.mutah.edu.jo/index.php/jje/article/view/716"
  ],
  "identifier": "https://dsr.mutah.edu.jo/index.php/jje/article/view/716",
  "isAccessibleForFree": true,
  "publisher": {
    "@type": "Organization",
    "name": "Jordan Journal of Energy"
  }
}
</script>
