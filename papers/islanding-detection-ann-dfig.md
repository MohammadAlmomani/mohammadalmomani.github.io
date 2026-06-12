---
layout: page
title: "Islanding Detection Method Based Artificial Neural Network"
description: "Artificial-neural-network islanding detection method for DFIG-based distributed energy resources using phase voltage, phase current, neutral voltage, neutral current, three-phase power, backpropagation, genetic algorithm, cuckoo optimization, and sampling-rate analysis."
permalink: /papers/islanding-detection-ann-dfig/
---

# Islanding Detection Method Based Artificial Neural Network

**Authors:** Mohammad M. Al-Momani, Seba F. Al-Gharaibeh, Ali S. Al-Dmour, and Ahmed J. Allaham  
**Research Area:** Islanding Detection, Distributed Energy Resources, DFIG Wind Turbine Protection, ANN-Based Classification  
**Journal:** Jordan Journal of Energy  
**Volume / Issue:** Volume 1, Number 1, 2023  
**Article Link:** [https://dsr.mutah.edu.jo/index.php/jje/article/view/3](https://dsr.mutah.edu.jo/index.php/jje/article/view/3)

---

## Search-Friendly Title

ANN-Based Islanding Detection for DFIG Wind Turbines Using Phase Voltage, Phase Current, Three-Phase Power, Backpropagation, Genetic Algorithm, Cuckoo Optimization, and Sampling-Rate Analysis

---

## Short Summary

This paper proposes an artificial neural network-based islanding detection method for a doubly fed induction generator wind turbine.

The method treats islanding detection as a classification problem. Five ANN systems are developed using different input signals:

- phase voltage,
- phase current,
- neutral voltage,
- neutral current,
- three-phase power.

The ANN models are trained and compared using three learning methods:

- backpropagation,
- genetic algorithm,
- cuckoo optimization algorithm.

The paper also studies the effect of sampling rate on detection accuracy and computational burden. The results show that phase voltage, phase current, and three-phase power are more effective inputs than neutral voltage and neutral current. The paper reports that 16 samples per cycle can be sufficient to detect islanding within four cycles when using power-based input data.

---

## Abstract

Islanding detection is a critical protection function for distributed energy resources. Islanding occurs when part of a distribution system becomes electrically isolated from the main grid while the distributed generator continues to energize the local island. If islanding is not detected quickly, it can create safety risks, equipment damage, power-quality problems, and protection coordination issues.

This paper presents an islanding detection technique based on artificial neural networks for a doubly fed induction generator wind turbine. The ANN is used as a pattern classifier to distinguish islanding events from non-islanding events.

Five different ANN systems are developed using phase power, phase voltage, phase current, neutral voltage, and neutral current inputs. Feedforward ANN structures are trained using backpropagation, genetic algorithm, and cuckoo optimization algorithm. Different sampling rates are tested to evaluate accuracy and computational burden.

The study is implemented in MATLAB 2020a and validated using a simulated DFIG-based system under load increase, load decrease, and main-supply trip scenarios.

---

## Research Gap

Traditional islanding detection methods can be divided into remote, passive, active, and hybrid methods. Remote methods may require communication infrastructure, while active methods can disturb the system. Passive methods are simple but may suffer from non-detection zones.

ANN-based islanding detection offers a data-driven alternative, but practical design requires answering several questions:

- Which input signal is most effective?
- What sampling rate is needed?
- How much computation is required?
- Which learning algorithm gives acceptable performance?
- Can islanding be distinguished from load increase and load decrease events?

This paper addresses these questions by comparing multiple ANN input signals, multiple sampling rates, and multiple learning algorithms for DFIG islanding detection.

---

## Main Contributions

1. **ANN-based islanding detection for DFIG wind turbine**  
   The paper develops ANN classifiers to detect islanding in a DFIG-based DER system.

2. **Comparison of five input signal types**  
   The study compares phase voltage, phase current, neutral voltage, neutral current, and three-phase power as ANN inputs.

3. **Comparison of three training algorithms**  
   Backpropagation, genetic algorithm, and cuckoo optimization are used to train the ANN systems.

4. **Sampling-rate impact analysis**  
   The paper evaluates sampling rates including 400 Hz, 800 Hz, 1600 Hz, and 3200 Hz, corresponding to 8, 16, 32, and 64 samples per cycle.

5. **Computational burden evaluation**  
   The study considers computational time as part of the performance comparison.

6. **Load-change versus islanding classification**  
   The ANN is trained to distinguish main-supply trip from load increase and load decrease events.

7. **Practical recommendation**  
   The paper concludes that phase voltage, phase current, and power-based input data are more suitable than neutral voltage and neutral current for this islanding detection application.

---

## System Under Study

The simulated system includes:

- DFIG wind turbine,
- point of common coupling,
- local load,
- main utility grid,
- transformer and transmission/distribution connection,
- islanding event produced by tripping the main supply.

The study considers three event scenarios:

1. load increase to double value,
2. load decrease to half value,
3. main supply trip / islanding.

For each scenario, ten cycles are used:

- five cycles before the event,
- five cycles after the event.

---

## ANN Structure

The paper uses feedforward ANN classifiers.

For each sampling rate, the number of inputs depends on the number of samples per cycle. A full cycle is used as the input data window.

Examples:

- 400 Hz corresponds to 8 samples per cycle,
- 800 Hz corresponds to 16 samples per cycle,
- 1600 Hz corresponds to 32 samples per cycle,
- 3200 Hz corresponds to 64 samples per cycle.

The paper proposes formulas for selecting:

- the number of hidden layers,
- the number of neurons in each hidden layer,
- the number of weights in the ANN structure.

A sigmoid activation function is used for the ANN neurons.

---

## Learning Algorithms

### Backpropagation

Backpropagation is used as a standard gradient-based ANN training method. It is fast and widely used, but it can be affected by local minima.

### Genetic Algorithm

The genetic algorithm trains ANN weights using population-based optimization inspired by genetic evolution. Mutation is used to reduce the risk of local solutions.

### Cuckoo Optimization Algorithm

The cuckoo algorithm is used as another population-based optimization method inspired by cuckoo egg-laying behavior and habitat migration.

---

## Input Signal Types

### Phase Voltage

Phase voltage is one of the strongest input signals for ANN-based islanding detection in this study.

### Phase Current

Phase current also provides strong islanding classification performance.

### Three-Phase Power

Three-phase power is effective and provides a practical balance between accuracy and detection time.

### Neutral Voltage

Neutral voltage is less effective for this islanding detection application.

### Neutral Current

Neutral current is also less effective compared with phase voltage, phase current, and power.

---

## Training and Validation Data

The training and validation data are generated using different load levels.

Training load levels:

```text
0.2 p.u. to 2.0 p.u. with 0.1 p.u. step
```

Validation load levels:

```text
0.25 p.u. to 1.95 p.u. with 0.1 p.u. step
```

For the 800 Hz system, the test data size is reported as:

```text
600 × 16
```

The ANN classifies whether each data window corresponds to islanding or non-islanding behavior.

---

## Key Results

- The ANN can classify islanding events using local electrical measurements.
- Phase voltage, phase current, and three-phase power provide better islanding detection performance than neutral voltage and neutral current.
- Neutral voltage and neutral current are not recommended for this application.
- Higher sampling rates generally improve detection performance but increase computational burden.
- For phase-voltage-based backpropagation, very low mean absolute error is reported at several sampling rates.
- For phase-current-based backpropagation, strong results are reported, especially at 16 and 64 samples per cycle.
- For power-based input, 16 samples per cycle are sufficient to detect islanding within four cycles in the reported study.
- The study compares backpropagation, genetic algorithm, and cuckoo optimization as ANN training methods.
- Computational burden must be considered because higher sampling rates and optimization-based training methods can significantly increase training time.

---

## Practical Detection Insight

The most important practical conclusion is that islanding detection should not rely only on increasing sampling rate.

A good islanding detection design must balance:

- input signal quality,
- detection speed,
- computational burden,
- training algorithm,
- number of ANN inputs,
- robustness against non-islanding load changes.

For this paper, phase voltage, phase current, and three-phase power are the most useful measurement choices.

---

## Relationship to Your Research Hub

This paper connects to your broader research directions in:

- AI-based power system protection,
- DER and wind turbine integration,
- microgrid protection,
- WAMS-based monitoring,
- ANN-based stability and protection classification,
- data-driven power system event detection.

It should be grouped under:

```text
AI-Based Protection, DER Monitoring, and Microgrid Islanding Detection
```

It is also related to your later work on ANN-based oscillation damping and transient stability prediction using wide-area measurements.

---

## Search-Friendly Questions

### What is islanding detection?

Islanding detection identifies when a distributed energy resource continues to energize a local part of the network after separation from the main grid.

### Why is islanding detection important?

Islanding can create safety hazards, damage equipment, cause power-quality problems, and interfere with protection systems.

### What does this paper propose?

This paper proposes an ANN-based islanding detection method for a DFIG wind turbine system.

### What type of DER is studied?

The paper studies a doubly fed induction generator wind turbine.

### What ANN inputs are tested?

The tested inputs are phase voltage, phase current, neutral voltage, neutral current, and three-phase power.

### Which inputs perform best?

Phase voltage, phase current, and three-phase power perform better than neutral voltage and neutral current.

### Which ANN training algorithms are compared?

The paper compares backpropagation, genetic algorithm, and cuckoo optimization algorithm.

### What sampling rates are tested?

The paper studies 400 Hz, 800 Hz, 1600 Hz, and 3200 Hz, corresponding to 8, 16, 32, and 64 samples per cycle.

### What events are classified?

The ANN distinguishes islanding from non-islanding events such as load increase and load decrease.

### How fast can islanding be detected?

The paper reports that 16 samples per cycle are enough to detect islanding within four cycles when using power-based input data.

### Why are neutral voltage and neutral current less useful?

The paper concludes that neutral quantities are not suitable for this application compared with phase voltage, phase current, and power-based measurements.

---

## Keywords

islanding detection; islanding detection method; IDM; artificial neural network; ANN; feedforward neural network; backpropagation; genetic algorithm; GA; cuckoo optimization algorithm; cuckoo algorithm; DFIG; doubly fed induction generator; wind turbine islanding detection; distributed energy resources; DER; microgrid protection; anti-islanding protection; passive islanding detection; local islanding detection; phase voltage; phase current; neutral voltage; neutral current; three-phase power; power-based islanding detection; sampling rate; samples per cycle; 16 samples per cycle; four-cycle detection; MATLAB Simulink; power system protection; renewable energy integration; smart grid protection.

---

## Citation

```bibtex
@article{almomani2023islanding,
  title   = {Islanding Detection Method Based Artificial Neural Network},
  author  = {Al-Momani, Mohammad M. and Al-Gharaibeh, Seba F. and Al-Dmour, Ali S. and Allaham, Ahmed J.},
  journal = {Jordan Journal of Energy},
  volume  = {1},
  number  = {1},
  pages   = {19--35},
  year    = {2023},
  url     = {https://dsr.mutah.edu.jo/index.php/jje/article/view/3}
}
```

---

## Links

- **Journal page:** [https://dsr.mutah.edu.jo/index.php/jje/article/view/3](https://dsr.mutah.edu.jo/index.php/jje/article/view/3)
- **Code repository:** Coming soon.
- **MATLAB / Simulink model:** Coming soon.
- **Related work:** Prediction of Transient Stability Using Wide Area Measurements Based on ANN; ANN-Based Low-Frequency Oscillation Damping; Application of Artificial Intelligence Techniques for Modeling and Simulation of Photovoltaic Arrays.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Islanding Detection Method Based Artificial Neural Network",
  "name": "Islanding Detection Method Based Artificial Neural Network",
  "description": "An ANN-based islanding detection method for DFIG-based distributed energy resources using phase voltage, phase current, neutral voltage, neutral current, three-phase power, backpropagation, genetic algorithm, cuckoo optimization, and sampling-rate analysis.",
  "author": [
    {
      "@type": "Person",
      "name": "Mohammad M. Al-Momani"
    },
    {
      "@type": "Person",
      "name": "Seba F. Al-Gharaibeh"
    },
    {
      "@type": "Person",
      "name": "Ali S. Al-Dmour"
    },
    {
      "@type": "Person",
      "name": "Ahmed J. Allaham"
    }
  ],
  "keywords": [
    "islanding detection",
    "ANN",
    "artificial neural network",
    "DFIG",
    "doubly fed induction generator",
    "distributed energy resources",
    "DER",
    "microgrid protection",
    "backpropagation",
    "genetic algorithm",
    "cuckoo optimization",
    "phase voltage",
    "phase current",
    "neutral voltage",
    "neutral current",
    "three-phase power",
    "sampling rate",
    "anti-islanding protection",
    "MATLAB Simulink"
  ],
  "url": "https://mohammadalmomani.github.io/papers/islanding-detection-ann-dfig/",
  "sameAs": [
    "https://dsr.mutah.edu.jo/index.php/jje/article/view/3"
  ],
  "identifier": "https://dsr.mutah.edu.jo/index.php/jje/article/view/3",
  "isAccessibleForFree": true,
  "publisher": {
    "@type": "Organization",
    "name": "Jordan Journal of Energy"
  }
}
</script>
