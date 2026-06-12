---

layout: page
title: "Trajectory-Based Nonlinear Indices for Real-Time Monitoring and Quantification of Short-Term Voltage Stability"
permalink: /papers/trajectory-based-nonlinear-indices-stvs/
-----------------------------------------------------------

# Trajectory-Based Nonlinear Indices for Real-Time Monitoring and Quantification of Short-Term Voltage Stability

**Authors:** Mohammad Almomani, Muhammad Sarwar, and Venkataramana Ajjarapu
**Research Area:** Short-Term Voltage Stability and Voltage Trajectory Analytics
**Status:** arXiv preprint / submitted version
**arXiv:** https://arxiv.org/abs/2604.07051

---

## Short Summary

This paper proposes trajectory-based nonlinear indices for real-time monitoring and quantification of short-term voltage stability (STVS). The method separates post-fault voltage trajectories into slow recovery and oscillatory components using Empirical Mode Decomposition (EMD). Lyapunov exponents are then used to characterize each component, and Kullback–Leibler (KL) divergence is used to quantify the stability degree relative to a critical reference signal.

The framework provides two complementary indices:

1. **Recovery Stability Index** for delayed voltage recovery and relay-tripping risk.
2. **Oscillation Stability Index** for damped or undamped voltage oscillations.

Unlike binary stable/unstable classifiers, the proposed method quantifies how close the system is to instability.

---

## Abstract

Existing short-term voltage stability methods typically address either voltage oscillations or delayed voltage recovery; however, the coexistence of both phenomena has not been adequately covered in the literature. Moreover, existing real-time STVS assessment methods often provide only binary stability classifications.

This paper proposes novel indices that enable early detection and quantify the degree of stability. The proposed method decomposes post-fault voltage trajectories using Empirical Mode Decomposition (EMD) into residual and oscillatory components. It then employs Lyapunov Exponents (LEs) to characterize the dynamic behavior of each component and evaluates the stability degree using Kullback–Leibler (KL) divergence by comparing the LEs of each component with those of a predefined critical signal.

The proposed indices assess oscillatory stability significantly faster than the traditional LE method applied directly to the original signal. Specifically, they detect stability within 0.6 seconds after a fault, compared to approximately 10 seconds for the conventional LE approach. In addition, the delayed-recovery index can identify generator trips caused by over-excitation limits within 3 seconds, well before the actual trip occurs at approximately 20 seconds, thereby providing operators and controllers sufficient time to take preventive actions.

Simulation studies on the Nordic test system under varying load conditions demonstrate the effectiveness of the proposed indices.

---

## Main Contributions

* Separates short-term voltage dynamics into **slow recovery dynamics** and **fast oscillatory dynamics**.
* Introduces a **Recovery Stability Index** to quantify delayed voltage recovery and predict relay-tripping risk.
* Introduces an **Oscillation Stability Index** to quantify damping and proximity to oscillatory instability.
* Uses **EMD**, **Lyapunov exponents**, and **KL divergence** to create interpretable nonlinear stability metrics.
* Detects oscillatory stability within approximately **0.6 seconds** after a disturbance.
* Predicts delayed-recovery-related generator tripping within approximately **3 seconds**.
* Provides a graded stability margin instead of only a binary stable/unstable classification.
* Validates the method using the **Nordic test system** with dynamic composite load models.

---

## Method Overview

The proposed method follows these steps:

1. **Post-fault voltage trajectory extraction**
   Voltage trajectories are collected after a disturbance.

2. **Empirical Mode Decomposition**
   The voltage signal is decomposed into:

   * residual component representing slow voltage recovery,
   * intrinsic mode functions representing oscillatory behavior.

3. **Lyapunov exponent calculation**

   * FSLE is applied to residual components to evaluate delayed recovery.
   * FTLE is applied to oscillatory components to evaluate damping or divergence.

4. **Divergence-factor construction**
   The exponential of the Lyapunov exponent is used to form a divergence factor distribution.

5. **KL-divergence-based stability index**
   KL divergence compares the observed divergence-factor distribution with a critical reference distribution.

6. **Stability margin calculation**
   The resulting index provides a quantitative measure of proximity to instability.

---

## Keywords

short-term voltage stability; STVS; voltage trajectory; delayed voltage recovery; FIDVR; Lyapunov exponent; finite-time Lyapunov exponent; finite-size Lyapunov exponent; empirical mode decomposition; EMD; multivariate EMD; Kullback–Leibler divergence; KL divergence; nonlinear stability index; real-time dynamic stability assessment; Nordic test system; voltage stability margin; oscillation stability; recovery stability index; PMU-based stability monitoring.

---

## Search-Friendly Questions

### What problem does this paper solve?

This paper addresses real-time short-term voltage stability assessment when delayed voltage recovery and voltage oscillations occur together. Existing methods often treat these phenomena separately or provide only binary stable/unstable results.

### What is the main idea of the proposed method?

The method separates a post-fault voltage trajectory into slow recovery and oscillatory components, applies Lyapunov-exponent analysis to each component, and uses KL divergence to quantify the stability degree.

### Why is this method useful for operators?

The method provides early warning and a quantitative stability margin, helping operators identify whether a system is stable, near critical, or moving toward instability.

### How fast is the proposed index?

The oscillation stability index can detect stability within about 0.6 seconds after a disturbance. The delayed-recovery index can identify generator-tripping risk within about 3 seconds.

### What test system is used?

The method is validated using the Nordic test system with composite dynamic load models and different motor-load penetration levels.

---

## Related Research Directions

* Short-term voltage stability assessment
* Real-time dynamic stability monitoring
* PMU-based voltage trajectory analysis
* Fault-induced delayed voltage recovery
* Lyapunov-exponent-based stability assessment
* Data-driven power system stability indices
* Stability monitoring for renewable- and DER-dominated grids

---

## Citation

```bibtex
@misc{almomani2026trajectory,
  title        = {Trajectory-Based Nonlinear Indices for Real-Time Monitoring and Quantification of Short-Term Voltage Stability},
  author       = {Almomani, Mohammad and Sarwar, Muhammad and Ajjarapu, Venkataramana},
  year         = {2026},
  eprint       = {2604.07051},
  archivePrefix= {arXiv},
  primaryClass = {eess.SY},
  url          = {https://arxiv.org/abs/2604.07051}
}
```

---

## Links

* **arXiv page:** https://arxiv.org/abs/2604.07051
* **PDF:** https://arxiv.org/pdf/2604.07051
* **Code:** will be added when available.
* **Dataset:** will be added when available.

---

## Recommended Citation Note

If you use the proposed STVS indices, voltage-trajectory decomposition method, Lyapunov-exponent implementation, or KL-divergence-based stability margin, please cite this paper.
