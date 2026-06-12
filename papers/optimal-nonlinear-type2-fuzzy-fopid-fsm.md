---
layout: page
title: "An Optimal Nonlinear Type-2 Fuzzy FOPID Control Design Based on Integral Performance Criteria Using FSM"
description: "Optimal nonlinear Type-2 Fuzzy fractional-order PID control design using Fourier Series Method, integral performance criteria, modified TLBO, membership-function nonlinearity optimization, footprint of uncertainty optimization, and fractional-order control."
permalink: /papers/optimal-nonlinear-type2-fuzzy-fopid-fsm/
---

# An Optimal Nonlinear Type-2 Fuzzy FOPID Control Design Based on Integral Performance Criteria Using FSM

**Authors:** Mohammad M. Al-Momani, Amneh Al-Mbaideen, Abdullah I. Al-Odienat, Khaled Mohammad Alawasa, and Saba F. Al-Gharaibeh  
**Research Area:** Advanced Control Systems, Type-2 Fuzzy Control, Fractional-Order PID, Optimization-Based Controller Design  
**Journal:** IEEE Access  
**Year:** 2023  
**DOI:** [10.1109/ACCESS.2023.3279862](https://doi.org/10.1109/ACCESS.2023.3279862)  
**IEEE Xplore:** [https://ieeexplore.ieee.org/document/10135090](https://ieeexplore.ieee.org/document/10135090)

---

## Search-Friendly Title

Optimal Nonlinear Type-2 Fuzzy Fractional-Order PID Controller Design Using Fourier Series Method, Integral Performance Criteria, and Modified TLBO

---

## Short Summary

This paper proposes a four-step optimization algorithm for designing **nonlinear Type-2 Fuzzy fractional-order PID (FOPID)** controllers using the **Fourier Series Method (FSM)**.

The main idea is to combine:

- fractional-order PID control,
- Sugeno Type-2 fuzzy logic,
- nonlinear membership-function optimization,
- footprint of uncertainty optimization,
- integral performance criteria,
- Modified Teaching-Learning-Based Optimization (MTLBO),
- Fourier Series Method for fractional-order system response calculation.

Unlike many previous FOPID design methods that approximate fractional-order operators using integer-order equivalents, this work uses FSM to handle fractional-order dynamics more directly.

---

## Abstract

A fractional-order fuzzy PID controller combines the advantages of fractional calculus and fuzzy logic with the conventional PID controller. This paper proposes a four-stage optimization algorithm for the design of a Type-2 Fuzzy fractional-order PID controller based on the Fourier Series Method.

Three distinct control structures are introduced:

- Type-2 fuzzy fractional PD plus fractional PI controller,
- Type-2 fuzzy fractional PID controller,
- Type-2 fuzzy fractional PD plus Type-2 fuzzy fractional PI controller.

In addition to a modified multi-performance criterion cost function, four integral performance criteria are used as cost functions for each design stage. The proposed algorithm avoids the use of approximation equivalents for fractional-order systems and instead employs the Fourier Series Method.

The method also optimizes the nonlinearity of the upper membership function and the uncertainty range represented by the lower membership function, rather than selecting these membership functions arbitrarily. Simulation results show improved step-response performance compared with previous research and demonstrate the feasibility of the proposed design method for both integer-order and fractional-order plants.

---

## Research Gap

Previous hybrid fuzzy FOPID controller studies have several limitations.

First, many studies optimize only the PID or FOPID gains while keeping fuzzy membership functions fixed, linear, or uniformly distributed. This ignores the strong effect of membership-function shape and distribution on the final controller response.

Second, many Type-2 fuzzy controller designs choose the lower membership function arbitrarily. Since the lower membership function defines the footprint of uncertainty, arbitrary selection can limit robustness and reduce the physical meaning of the Type-2 fuzzy controller.

Third, many fractional-order PID designs approximate fractional-order operators using integer-order transfer-function equivalents. This approximation can reduce accuracy and may not fully preserve the dynamic behavior of the fractional-order controller.

This paper addresses these gaps by optimizing the controller gains, fractional orders, membership-function nonlinearity, and Type-2 fuzzy uncertainty footprint in a structured four-step design process.

---

## Main Contributions

1. **Four-step Type-2 Fuzzy FOPID design algorithm**  
   The paper proposes a systematic four-stage controller design process that optimizes the PID/FOPID parameters, fractional-order parameters, membership-function nonlinearity, and uncertainty footprint.

2. **Fourier Series Method for fractional-order response**  
   The method uses FSM to evaluate fractional-order system response without relying on approximation equivalents for the fractional-order operator.

3. **Optimization of nonlinear membership functions**  
   The algorithm optimizes the nonlinearity factor of the upper membership function instead of assuming uniformly distributed triangular membership functions.

4. **Optimization of Type-2 fuzzy footprint of uncertainty**  
   The lower membership function is optimized to tune the footprint of uncertainty instead of choosing it arbitrarily.

5. **Three Type-2 Fuzzy FOPID controller structures**  
   The paper compares three hybrid fuzzy-fractional controller structures under a consistent design framework.

6. **Multiple integral performance criteria**  
   The controller is optimized using ISE, ITSE, IT2SE, IAE, and a modified multi-performance criterion.

7. **Modified Teaching-Learning-Based Optimization**  
   A modified TLBO algorithm is introduced to optimize nonlinear fuzzy parameters and Type-2 fuzzy uncertainty parameters.

8. **Validation on integer-order and fractional-order plants**  
   The proposed design method is applied to benchmark integer-order and fractional-order systems.

9. **Comparison with previous algorithms**  
   The method is compared with recently published controller design approaches for high-order, time-delay, integrating, and fractional-order processes.

10. **Relevance to smart grids and renewable-energy control**  
   The paper highlights the potential application of the algorithm to low-frequency oscillation damping, smart-grid control, and renewable-energy integration problems.

---

## Controller Structures

The paper introduces and compares three Type-2 Fuzzy FOPID control structures.

### Structure 1: FFPD-FPI Controller

This structure combines a fractional fuzzy PD controller with a fractional PI controller.

**Search terms:** fractional fuzzy PD, fractional PI, FFPD-FPI, Type-2 fuzzy FOPID, hybrid fuzzy fractional controller.

### Structure 2: FFPID Controller

This structure implements a Type-2 fuzzy fractional PID controller in a single fuzzy-fractional control block.

**Search terms:** fuzzy fractional PID, Type-2 FFPID, fractional-order fuzzy PID, Sugeno Type-2 fuzzy PID.

### Structure 3: FFPD-FFPI Controller

This structure uses two parallel Type-2 fuzzy controllers: one for fractional fuzzy PD action and one for fractional fuzzy PI action.

**Search terms:** parallel fuzzy FOPID, FFPD-FFPI, fuzzy PD fuzzy PI controller, nonlinear Type-2 fuzzy fractional controller.

---

## Four-Step Design Process

The proposed design algorithm has four main steps.

### Step 1: Linear Type-1 Fuzzy PID

The design begins with a linear Type-1 fuzzy PID controller. The membership functions are uniformly distributed, the fuzzy rules preserve linearity, and the fractional orders are set to integer values.

This step provides the initial controller parameters corresponding to PID-like gains.

Optimized parameters:

- A,
- B,
- C,
- D.

### Step 2: Linear Type-1 Fuzzy FPID

Fractional-order parameters are added to the design. The fractional integration and differentiation orders are optimized along with the controller gains.

Optimized parameters:

- A,
- B,
- C,
- D,
- λ,
- μ.

This step captures the effect of fractional-order control and improves the step response relative to the integer-order design.

### Step 3: Nonlinear Type-1 Fuzzy FPID

The third step optimizes the nonlinearity of the membership functions. Instead of using uniformly distributed triangular membership functions, the method adjusts the distribution of the membership-function centers using nonlinear factors.

Optimized parameters:

- membership-function nonlinearity factors,
- nonlinear distribution parameters,
- fuzzy input/output membership shape parameters.

This step improves the controller response by tuning how the fuzzy controller responds near and away from the operating point.

### Step 4: Nonlinear Type-2 Fuzzy FPID

The final step optimizes the Type-2 fuzzy footprint of uncertainty by tuning the lower membership function.

Optimized parameters:

- lower membership function parameters,
- uncertainty footprint parameters,
- Type-2 fuzzy uncertainty scaling factors.

This step allows the controller to incorporate uncertainty more systematically.

---

## Why the Fourier Series Method Is Important

Many fractional-order PID design methods approximate the fractional operators using integer-order transfer functions. This paper avoids that limitation by using the Fourier Series Method to represent the step response of fractional-order transfer functions.

This is important because fractional-order systems and fractional-order controllers may lose important dynamic behavior when they are forced into integer-order approximations.

FSM allows the controller design to preserve the fractional-order behavior more directly during optimization.

---

## Optimization Criteria

The paper uses several integral performance criteria as objective functions.

### Integral Squared Error

ISE penalizes large tracking errors and is often useful for reducing overall energy of the error signal.

### Integral Time Squared Error

ITSE adds time weighting to squared error, penalizing errors that persist longer.

### Integral Squared Time Squared Error

IT2SE applies stronger time weighting, encouraging faster settling and reducing long-duration error.

### Integral Absolute Error

IAE minimizes the total absolute tracking error and often provides balanced time-domain performance.

### Multi-Performance Criterion

The paper introduces a modified multi-performance criterion:

```text
MPC = 0.4 × ISE + 0.2 × ITSE + 0.4 × IAE
```

This criterion combines multiple time-domain objectives to balance accuracy, settling behavior, and tracking performance.

---

## Modified Teaching-Learning-Based Optimization

The paper modifies the Teaching-Learning-Based Optimization algorithm to improve convergence.

The standard TLBO algorithm has two phases:

- teaching phase,
- learning phase.

The proposed modified version adds an assistant-level learning mechanism. In this stage, the population is sorted by cost value and divided into subgroups. The best solution in each subgroup acts as a teaching assistant, helping accelerate convergence and reduce the risk of local solutions.

This modification is especially useful for optimizing nonlinear fuzzy membership functions and Type-2 fuzzy uncertainty parameters.

---

## Benchmark Systems

The paper validates the method on multiple process types.

### Integer-Order Benchmark Plant

The first main benchmark is a three-pole underdamped integer-order plant:

```text
G(s) = 9 / ((s + 1)(s² + 2s + 9))
```

This system is used to test the four-step design procedure and compare the three controller structures.

### Fractional-Order Benchmark Plant

The second main benchmark is a fractional-order plant with non-integer powers of `s`. This benchmark demonstrates that the algorithm can handle fractional-order dynamics directly.

### Additional Validation Processes

The algorithm is also tested against multiple processes used in previous studies, including:

- first-order plus dead-time lag-dominant process,
- higher-order process,
- integrating time-delay process,
- first-order pulse dead-time delay-dominant process,
- fractional-order process.

---

## Key Technical Findings

- Adding fractional-order parameters improves the performance of all three controller structures compared with the initial linear Type-1 fuzzy PID design.
- The fractional-order step generally reduces settling time and improves response speed.
- Optimizing nonlinear fuzzy membership functions further improves the controller response.
- Optimizing the Type-2 fuzzy footprint of uncertainty improves linear fuzzy controllers more strongly than already-optimized nonlinear fuzzy controllers.
- Good performance can be achieved using either:
  - nonlinear Type-1 fuzzy control, or
  - linear Type-2 fuzzy control.
- The improvement provided by optimized Type-1 fuzzy nonlinearity can be comparable to the improvement obtained from Type-2 fuzzy uncertainty modeling.
- For some optimized nonlinear fuzzy controllers, optimizing the Type-2 uncertainty footprint gives limited additional improvement.
- For fractional-order plants, each design step improves the response, especially when using IAE-based optimization.
- The proposed MTLBO reaches results comparable to traditional TLBO with fewer iterations.

---

## Important Design Insight

One of the most important conclusions is that controller performance is not determined only by FOPID gains.

The membership-function geometry matters.

This means that the fuzzy controller design should not simply tune:

- Kp,
- Ki,
- Kd,
- λ,
- μ.

It should also tune:

- membership-function nonlinearity,
- membership-function distribution,
- upper membership function behavior,
- lower membership function behavior,
- footprint of uncertainty.

This is the key reason the proposed algorithm is more comprehensive than many previous fuzzy FOPID design methods.

---

## Validation Against Previous Research

The paper compares the proposed method with recently published algorithms for several process types.

The validation shows that:

- ITSE, IT2SE, and MPC criteria provide strong performance for the first process.
- IT2SE performs strongly for the second process in terms of overshoot and settling time.
- For the integrating time-delay process, all tested criteria improve performance compared with the selected previous algorithms.
- For the first-order pulse dead-time delay-dominant process, IT2SE gives the most effective controller among the tested cases.
- For fractional-order processes, the proposed algorithm improves rise-time performance compared with selected prior work.
- A modified objective including step-response maximum value can reduce overshoot while preserving strong rise-time performance.

---

## Computational Considerations

The simulations are implemented in MATLAB and Simulink. The paper reports that the first two optimization steps terminate when the optimal fitness value is achieved, while the third and fourth steps stop at the maximum number of MTLBO iterations.

The computational burden is higher in the third and fourth steps because nonlinear fuzzy logic and Type-2 fuzzy logic are simulated using MATLAB Simulink.

The paper notes that future work can reduce computational cost by representing nonlinear fuzzy and Type-2 fuzzy controllers using transfer-function models in the time or frequency domain.

The modified TLBO algorithm reaches results after 25 iterations that are comparable to roughly 50 iterations of traditional TLBO, while requiring approximately 75% of the time needed by the traditional approach.

---

## Future Applications

The paper identifies promising future applications in:

- smart-grid control,
- renewable-energy integration,
- low-frequency oscillation damping,
- power system stabilizer design,
- real-time digital simulation,
- Jordan power system implementation using RTDS at Mu’tah University.

For your research hub, this paper should be connected to your later work on low-frequency oscillation damping and ANN-based damping controllers because it provides an advanced control-design foundation.

---

## Search-Friendly Questions

### What is the main goal of this paper?

The main goal is to design an optimal nonlinear Type-2 Fuzzy fractional-order PID controller using a structured four-step optimization algorithm and the Fourier Series Method.

### What is a Type-2 Fuzzy FOPID controller?

A Type-2 Fuzzy FOPID controller combines Type-2 fuzzy logic with fractional-order PID control. It uses fuzzy rules to handle nonlinearity and uncertainty, while fractional-order integration and differentiation provide additional tuning flexibility.

### Why is Type-2 fuzzy logic used?

Type-2 fuzzy logic is used because it can represent uncertainty in the membership functions through the footprint of uncertainty. This can improve robustness compared with Type-1 fuzzy logic.

### What is the footprint of uncertainty?

The footprint of uncertainty is the region between the upper and lower membership functions in a Type-2 fuzzy set. It represents uncertainty in the fuzzy membership degree.

### Why is the lower membership function important?

The lower membership function defines the uncertainty range in the Type-2 fuzzy controller. Optimizing it gives a systematic way to tune the controller’s uncertainty handling instead of choosing the uncertainty range arbitrarily.

### What is the role of the upper membership function?

The upper membership function defines the outer boundary of the fuzzy set. In this paper, its nonlinearity is optimized to improve controller performance.

### What is the Fourier Series Method used for?

The Fourier Series Method is used to calculate the step response of fractional-order transfer functions without approximating fractional-order operators by integer-order transfer functions.

### Why is avoiding fractional-order approximation important?

Avoiding approximation helps preserve the true fractional-order dynamics of the controller and plant, which can improve accuracy in controller design.

### What is MTLBO?

MTLBO stands for Modified Teaching-Learning-Based Optimization. It is used to optimize nonlinear fuzzy membership parameters and Type-2 fuzzy uncertainty parameters.

### What performance criteria are used?

The paper uses ISE, ITSE, IT2SE, IAE, and MPC as objective functions for optimizing controller performance.

### What controller structures are compared?

The paper compares FFPD-FPI, FFPID, and FFPD-FFPI controller structures.

### What is the most important practical insight?

The most important insight is that optimal fuzzy FOPID design should tune not only the PID and fractional-order gains, but also the nonlinear membership-function distribution and the Type-2 fuzzy uncertainty footprint.

### Can this method be applied to power systems?

Yes. The paper highlights future applications in smart grids, renewable-energy integration, low-frequency oscillation damping, and RTDS-based power system implementation.

---

## Keywords

Type-2 fuzzy FOPID controller; nonlinear Type-2 fuzzy controller; fractional-order PID controller; FOPID; fractional-order fuzzy PID; Fourier Series Method; FSM; Sugeno Type-2 fuzzy controller; footprint of uncertainty; FOU; upper membership function; UMF; lower membership function; LMF; nonlinear membership function; membership-function optimization; fractional calculus; fractional-order control; PI lambda D mu controller; Modified Teaching-Learning-Based Optimization; MTLBO; Teaching-Learning-Based Optimization; TLBO; integral performance criteria; ISE; ITSE; IT2SE; IAE; multi-performance criterion; MPC; step response optimization; robust control; fuzzy fractional controller; optimal control design; smart grid control; renewable energy control; low-frequency oscillation damping; power system stabilizer; MATLAB Simulink.

---

## Citation

```bibtex
@article{almomani2023optimal,
  title   = {An Optimal Nonlinear Type-2 Fuzzy FOPID Control Design Based on Integral Performance Criteria Using FSM},
  author  = {Al-Momani, Mohammad M. and Al-Mbaideen, Amneh and Al-Odienat, Abdullah I. and Alawasa, Khaled Mohammad and Al-Gharaibeh, Saba F.},
  journal = {IEEE Access},
  volume  = {11},
  pages   = {53439--53467},
  year    = {2023},
  doi     = {10.1109/ACCESS.2023.3279862},
  url     = {https://ieeexplore.ieee.org/document/10135090}
}
```

---

## Links

- **IEEE Xplore:** [https://ieeexplore.ieee.org/document/10135090](https://ieeexplore.ieee.org/document/10135090)
- **DOI:** [https://doi.org/10.1109/ACCESS.2023.3279862](https://doi.org/10.1109/ACCESS.2023.3279862)
- **Code repository:** Coming soon.
- **MATLAB / Simulink files:** Coming soon.
- **Related work:** Low-frequency oscillation damping, Type-2 fuzzy control, fractional-order PID control, and renewable-energy power system control.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "An Optimal Nonlinear Type-2 Fuzzy FOPID Control Design Based on Integral Performance Criteria Using FSM",
  "name": "An Optimal Nonlinear Type-2 Fuzzy FOPID Control Design Based on Integral Performance Criteria Using FSM",
  "description": "A four-step optimal design method for nonlinear Type-2 Fuzzy fractional-order PID controllers using the Fourier Series Method, integral performance criteria, modified TLBO, membership-function nonlinearity optimization, and footprint of uncertainty optimization.",
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
      "name": "Abdullah I. Al-Odienat"
    },
    {
      "@type": "Person",
      "name": "Khaled Mohammad Alawasa"
    },
    {
      "@type": "Person",
      "name": "Saba F. Al-Gharaibeh"
    }
  ],
  "keywords": [
    "Type-2 fuzzy FOPID controller",
    "fractional-order PID",
    "FOPID",
    "Fourier Series Method",
    "FSM",
    "Sugeno Type-2 fuzzy controller",
    "footprint of uncertainty",
    "upper membership function",
    "lower membership function",
    "nonlinear membership function",
    "Modified Teaching-Learning-Based Optimization",
    "MTLBO",
    "integral performance criteria",
    "ISE",
    "ITSE",
    "IT2SE",
    "IAE",
    "MPC",
    "smart grid control",
    "low-frequency oscillation damping"
  ],
  "url": "https://mohammadalmomani.github.io/papers/optimal-nonlinear-type2-fuzzy-fopid-fsm/",
  "sameAs": [
    "https://ieeexplore.ieee.org/document/10135090",
    "https://doi.org/10.1109/ACCESS.2023.3279862"
  ],
  "identifier": "https://doi.org/10.1109/ACCESS.2023.3279862",
  "isAccessibleForFree": true,
  "publisher": {
    "@type": "Organization",
    "name": "IEEE"
  }
}
</script>
