---
layout: page
title: "Application of Artificial Intelligence Techniques for Modeling and Simulation of Photovoltaic Arrays"
description: "AI-based photovoltaic array modeling using genetic algorithm, cuckoo optimization algorithm, single-diode model, two-diode model, I-V characteristic fitting, MATLAB simulation, and Mutah University PV power plant validation."
permalink: /papers/ai-techniques-modeling-simulation-photovoltaic-arrays/
---

# Application of Artificial Intelligence Techniques for Modeling and Simulation of Photovoltaic Arrays

**Authors:** Mohammad Almomani, Ali S. Al-Dmour, and Seba Algharaibeh  
**Research Area:** Photovoltaic Modeling, AI-Based Optimization, Renewable Energy Simulation  
**Journal:** Jordan Journal of Electrical Engineering  
**Volume / Issue:** Volume 6, Number 4, 2020  
**Pages:** 296–314  
**DOI:** [10.5455/jjee.204-1595628009](https://doi.org/10.5455/jjee.204-1595628009)

---

## Search-Friendly Title

AI-Based Modeling and Simulation of Photovoltaic Arrays Using Genetic Algorithm, Cuckoo Optimization Algorithm, Single-Diode Model, and Two-Diode Model

---

## Short Summary

This paper presents an artificial-intelligence-based method for modeling photovoltaic arrays using the **Genetic Algorithm (GA)** and **Cuckoo Optimization Algorithm (COA)**.

The proposed approach estimates the unknown parameters of PV array models directly from datasheet information. It is applied to both:

- **single-diode PV model**,
- **two-diode PV model**.

The optimization method fits the mathematical current-voltage characteristic to the three main PV datasheet points:

- short-circuit current,
- open-circuit voltage,
- maximum power point.

The models are implemented in MATLAB 2020a and validated using experimental data from the Mutah University PV power plant.

---

## Abstract

This paper presents an artificial-intelligence-based method for modeling photovoltaic arrays. Genetic Algorithm and Cuckoo Optimization Algorithm are used to obtain the parameters of the PV array model using PV cell datasheet information.

The adopted models are implemented in MATLAB 2020a for both single-diode and two-diode PV models. The proposed optimization method fits the mathematical current-voltage characteristic to the main datasheet points without requiring manual guessing or pre-estimation of unknown parameters.

The obtained models are tested and validated using experimental data from the Mutah University PV power plant. Results show that the two-diode model is more accurate than the single-diode model. The results also show that Cuckoo Optimization Algorithm handles the optimization problem better than Genetic Algorithm, requiring fewer iterations and achieving better fitness values under different temperature and solar irradiance conditions.

---

## Research Gap

Many PV modeling approaches require assumptions, simplifications, or estimated parameters that can reduce model accuracy.

Common limitations include:

- assuming equal saturation currents in the two-diode model,
- assuming fixed ideality-factor relationships,
- introducing artificial parameters that do not directly match physical PV circuit parameters,
- relying on manual parameter tuning,
- using simplified models that reduce maximum power point accuracy.

This paper addresses these gaps by using GA and COA to identify physically meaningful PV model parameters directly from datasheet values and validate them against real PV plant measurements.

---

## Main Contributions

1. **AI-based PV parameter extraction**  
   GA and COA are used to estimate unknown PV model parameters from datasheet information.

2. **Single-diode and two-diode model comparison**  
   The paper compares both PV models under the same optimization framework.

3. **Three-point I-V fitting**  
   The model is fitted using open-circuit voltage, short-circuit current, and maximum power point.

4. **No manual parameter guessing**  
   The approach avoids arbitrary assumptions and manual estimation of unknown PV parameters.

5. **Temperature-dependent saturation current modeling**  
   The paper introduces a heat-effect factor for diode saturation current considering the energy-gap temperature effect.

6. **MATLAB implementation**  
   The models are implemented and simulated in MATLAB 2020a.

7. **Experimental validation**  
   The model is validated using data from the Mutah University PV power plant.

8. **COA versus GA comparison**  
   COA provides better convergence behavior and fitness values than GA in the reported cases.

---

## Method Overview

The proposed modeling process follows these steps:

### 1. Select PV Model

Two model structures are considered:

- single-diode model,
- two-diode model.

### 2. Extract Datasheet Points

The method uses PV datasheet values:

- open-circuit voltage,
- short-circuit current,
- voltage at maximum power,
- current at maximum power,
- temperature coefficients,
- number of series cells,
- number of parallel cells.

### 3. Define Model Constraints

The optimization problem includes:

- open-circuit constraint,
- maximum power point constraint,
- maximum power slope constraint.

### 4. Define Fitness Function

The cost function minimizes the error between measured and calculated open-circuit voltage across temperature variation.

### 5. Optimize PV Parameters

GA and COA are used to estimate:

- diode saturation current,
- diode ideality factor,
- series resistance,
- parallel resistance,
- two-diode model parameters.

### 6. Validate With Experimental Data

The optimized models are compared with measured PV data from the Mutah University PV power plant.

---

## PV Models

### Single-Diode Model

The single-diode model uses one diode, a current source, series resistance, and shunt resistance. It is simpler and computationally easier but less accurate near the maximum power point.

### Two-Diode Model

The two-diode model includes two diode branches and better represents recombination and diffusion effects. It is more complex but provides higher accuracy for PV array simulation.

---

## Optimization Algorithms

### Genetic Algorithm

GA is a population-based optimization method inspired by biological evolution. It uses selection, crossover, and mutation to search for optimal PV model parameters.

### Cuckoo Optimization Algorithm

COA is a population-based soft computing method inspired by cuckoo egg-laying behavior. In this paper, COA converges with fewer iterations and better fitness values compared with GA.

---

## Test PV Module

The paper uses the JAM6(K)-72-340/PR PV module from the Mutah University PV power plant.

Important datasheet values include:

- maximum power: 340 W,
- voltage at maximum power: 38.18 V,
- current at maximum power: 8.91 A,
- open-circuit voltage: 46.86 V,
- short-circuit current: 9.46 A,
- number of series cells: 72,
- number of parallel strings: 1.

---

## Key Results

- The two-diode model is more accurate than the single-diode model.
- COA provides better performance than GA for the PV parameter extraction problem.
- COA achieves better fitness values with fewer iterations.
- The proposed model fits the I-V curve using the main datasheet points without manual parameter guessing.
- Experimental validation with Mutah University PV power plant data confirms the usefulness of the optimized model.
- The method supports PV array simulation under different temperature and solar irradiance values.
- The proposed approach is useful for PV converter simulation, renewable-energy system studies, and PV plant modeling.

---

## Search-Friendly Questions

### What is the main goal of this paper?

The main goal is to model photovoltaic arrays accurately using artificial intelligence techniques, especially GA and COA.

### What PV models are studied?

The paper studies the single-diode and two-diode PV models.

### Which optimization algorithms are used?

The paper uses Genetic Algorithm and Cuckoo Optimization Algorithm.

### Why is the two-diode model important?

The two-diode model improves accuracy, especially around the maximum power point and under varying temperature and irradiance conditions.

### Why is COA useful for PV modeling?

COA gives better convergence and better fitness values compared with GA in the reported simulations.

### What data is used for validation?

Experimental data from the Mutah University PV power plant is used for validation.

### What software is used?

MATLAB 2020a is used for modeling and simulation.

### What is the practical application?

The model can be used for PV array simulation, PV power converter design, and renewable-energy system studies.

---

## Keywords

photovoltaic array modeling; PV array simulation; photovoltaic cell model; PV module model; artificial intelligence; genetic algorithm; GA; cuckoo optimization algorithm; COA; two-diode model; single-diode model; I-V characteristic; current-voltage curve; maximum power point; open-circuit voltage; short-circuit current; PV parameter extraction; MATLAB 2020a; Mutah University PV power plant; renewable energy modeling; solar irradiance; temperature effect; diode saturation current; PV system optimization.

---

## Citation

```bibtex
@article{almomani2020pvai,
  title   = {Application of Artificial Intelligence Techniques for Modeling and Simulation of Photovoltaic Arrays},
  author  = {Almomani, Mohammad and Al-Dmour, Ali S. and Algharaibeh, Seba},
  journal = {Jordan Journal of Electrical Engineering},
  volume  = {6},
  number  = {4},
  pages   = {296--314},
  year    = {2020},
  doi     = {10.5455/jjee.204-1595628009},
  url     = {https://doi.org/10.5455/jjee.204-1595628009}
}
```

---

## Links

- **DOI:** [https://doi.org/10.5455/jjee.204-1595628009](https://doi.org/10.5455/jjee.204-1595628009)
- **Code repository:** Coming soon.
- **MATLAB implementation:** Coming soon.
- **Experimental data:** Coming soon.
- **Related work:** Islanding Detection Method Based Artificial Neural Network; Prediction of Transient Stability Using Wide Area Measurements Based on ANN.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Application of Artificial Intelligence Techniques for Modeling and Simulation of Photovoltaic Arrays",
  "name": "Application of Artificial Intelligence Techniques for Modeling and Simulation of Photovoltaic Arrays",
  "description": "AI-based photovoltaic array modeling using genetic algorithm, cuckoo optimization algorithm, single-diode model, two-diode model, I-V characteristic fitting, MATLAB simulation, and Mutah University PV power plant validation.",
  "author": [
    {"@type": "Person", "name": "Mohammad Almomani"},
    {"@type": "Person", "name": "Ali S. Al-Dmour"},
    {"@type": "Person", "name": "Seba Algharaibeh"}
  ],
  "keywords": [
    "photovoltaic array modeling",
    "PV simulation",
    "genetic algorithm",
    "cuckoo optimization algorithm",
    "two-diode model",
    "single-diode model",
    "I-V characteristic",
    "PV parameter extraction",
    "MATLAB",
    "renewable energy"
  ],
  "url": "https://mohammadalmomani.github.io/papers/ai-techniques-modeling-simulation-photovoltaic-arrays/",
  "sameAs": [
    "https://doi.org/10.5455/jjee.204-1595628009"
  ],
  "identifier": "https://doi.org/10.5455/jjee.204-1595628009",
  "isAccessibleForFree": true,
  "publisher": {
    "@type": "Organization",
    "name": "Jordan Journal of Electrical Engineering"
  }
}
</script>
