---
layout: page
title: "Global-Binary Algorithm: New Optimal Phasor Measurement Unit Placement Algorithm"
description: "Global-Binary Algorithm for optimal PMU placement using finite binary solution space, subsystem splitting, connectivity matrix, zero-injection buses, WAMS observability, Jordanian power system case study, and MATLAB implementation."
permalink: /papers/global-binary-optimal-pmu-placement/
---

# Global-Binary Algorithm: New Optimal Phasor Measurement Unit Placement Algorithm

**Authors:** Mohammad M. Al-Momani, Amneh Almbaideen, Seba F. Al-Gharaibah, Khaled Al-Awasa, and Ahmed J. Allahham  
**Research Area:** Optimal PMU Placement, WAMS, Power System Observability, Connectivity Matrix Algorithms  
**Journal:** Jordan Journal of Energy  
**Volume / Issue:** Volume 1, Number 1, 2023  
**Article Link:** [https://dsr.mutah.edu.jo/index.php/jje/article/view/4](https://dsr.mutah.edu.jo/index.php/jje/article/view/4)

---

## Search-Friendly Title

Global-Binary Algorithm for Optimal PMU Placement in Wide-Area Monitoring Systems Using Connectivity Matrix and Jordanian Power System Validation

---

## Short Summary

This paper proposes the **Global-Binary Algorithm**, a deterministic optimal phasor measurement unit placement method based on the finite solution space of binary placement problems.

The method searches possible PMU placement combinations to identify the minimum number of PMUs required for full system observability. To reduce computational burden in large systems, the network is divided into smaller subsystems using a splitting algorithm. The optimal placements of each subsystem are then combined to obtain global placement options for the full power system.

The method is validated using the Jordanian transmission power system and compared with four existing algorithms using IEEE test systems.

---

## Abstract

This paper proposes a new algorithm for optimal placement of phasor measurement units. The proposed algorithm is based on the concept that the solution space of any binary placement problem is finite.

The algorithm considers all possible placement cases within each subsystem, increasing the likelihood of obtaining a global solution. A large power system is divided into several subsystems, and the buses or transmission lines connecting the subsystems are called interconnected buses or interconnected lines.

The proposed algorithm is implemented in two main steps. The first step identifies the optimal placement for each subsystem by checking all possible solutions. The second step gathers the subsystem results to obtain the global optimal placement for the entire system.

Finally, all possible PMU placements with the optimal number of PMUs are identified so that the final placement can be selected based on user applications such as oscillation monitoring, voltage stability assessment, redundancy, disturbance analysis, or remedial action schemes.

The Jordanian power system is used as a case study, and MATLAB 2020a is used for implementation.

---

## Research Gap

Many existing optimal PMU placement algorithms provide only one placement solution or may produce different numbers of PMUs depending on the system and algorithm. Some algorithms work well for certain test systems but may not consistently find all optimal placements.

In practical WAMS design, the operator may need more than one optimal solution because the final placement depends on the intended application, such as:

- state estimation,
- low-frequency oscillation monitoring,
- voltage stability monitoring,
- disturbance analysis,
- remedial action schemes,
- black-start monitoring,
- model validation.

This paper addresses that gap by generating all possible optimal PMU placements with the minimum PMU number, allowing the user to choose the most suitable placement based on application-specific priorities.

---

## Main Contributions

1. **Global-Binary Algorithm for OPP**  
   The paper proposes a deterministic PMU placement algorithm based on finite binary solution-space search.

2. **Subsystem splitting for large networks**  
   The power system is divided into smaller subsystems to reduce the computational burden of exhaustive binary search.

3. **Connectivity-matrix-based observability**  
   The method uses a connectivity matrix to represent network topology and evaluate system observability.

4. **Zero-injection bus handling**  
   The algorithm considers zero-injection buses and the additional freedom of solution created by different pseudo-measurement rules.

5. **All optimal PMU placements**  
   Instead of returning only one solution, the algorithm identifies all possible PMU placements with the minimum number of PMUs.

6. **Application-dependent placement selection**  
   The final placement can be selected based on user-defined priorities such as redundancy, oscillation monitoring, voltage stability, and disturbance analysis.

7. **Jordanian power system case study**  
   The method is validated on the Jordanian transmission network after considering zero-injection buses.

8. **Comparison with existing OPP algorithms**  
   The method is compared with four algorithms from the literature using different IEEE test systems.

---

## Problem Formulation

The optimal PMU placement problem aims to minimize the number of installed PMUs while ensuring full system observability.

A binary variable represents whether a PMU is installed at a bus:

- `x_k = 1` if a PMU is installed at bus `k`,
- `x_k = 0` otherwise.

The observability vector is computed using the connectivity matrix:

```text
F = A × X
```

where:

- `A` is the connectivity matrix,
- `X` is the binary PMU placement vector,
- `F` is the observability vector.

For full observability, the condition is:

```text
F ≥ I
```

For redundancy or N-1 observability requirements, the condition can be generalized as:

```text
F ≥ B
```

where `B` is the required measurement redundancy vector.

---

## Observability Rules

The paper uses standard PMU observability rules:

1. If a PMU is installed at a bus, that bus is directly observable.
2. If a PMU is installed at a bus, adjacent buses become observable through line current and Ohm’s law.
3. If two adjacent bus voltages are known, the line current can be calculated.
4. If a zero-injection bus and all connected buses except one are observable, the remaining bus can be estimated.
5. If all buses adjacent to a zero-injection bus are observable, the zero-injection bus voltage can be estimated.

These rules allow the algorithm to include both direct PMU measurements and pseudo-measurements.

---

## Global-Binary Algorithm Overview

The proposed algorithm has three main stages.

### Stage 1: Split the System

The full network is divided into smaller subsystems. The splitting algorithm rearranges the connectivity matrix so that dense groups of connected buses are concentrated around the main diagonal.

This reduces the size of the search space for each subsystem.

### Stage 2: Find OPP for Each Subsystem

For each subsystem, the algorithm checks possible PMU placement combinations and identifies all minimum-PMU solutions that satisfy observability.

The output of this stage is a set of subspace solutions.

### Stage 3: Gather Global Solutions

The subspace solutions are combined to form full-system placement candidates. The algorithm then checks whether PMUs at interconnected buses can be removed while maintaining full observability.

The final output is a complete set of global optimal PMU placements with the minimum PMU count.

---

## Why the Splitting Algorithm Is Important

A direct binary search over a large power system can be computationally expensive because the solution space grows exponentially.

For a 30-bus system, the binary solution space size is:

```text
2^30 - 1
```

The splitting algorithm reduces this burden by dividing the system into smaller groups and then combining the optimal subsystem solutions.

This makes the global-binary concept more practical for large transmission systems.

---

## Jordanian Power System Case Study

The paper applies the proposed method to the Jordanian transmission power system.

Key details:

- The Jordanian system has 68 substations after considering zero-injection buses.
- The system is divided into three subsystems.
- The subsystem sizes are:
  - 22 buses,
  - 22 buses,
  - 24 buses.
- The interconnected buses include:
  - 34, 36, 40, 7, 2, 30, 35, 40, 15, 18, 28, 29, 49, 43, and 44.

---

## Key Results

- The optimal PMU numbers for the three subsystems are:
  - 7 PMUs,
  - 7 PMUs,
  - 8 PMUs.
- The initial combined subsystem result gives:
  - `7 + 7 + 8 = 21 PMUs`.
- The subspace solution sizes are:
  - 30,
  - 5,
  - 55.
- The total combined space solution size is:
  - `30 × 5 × 55 = 8250`.
- After checking interconnected buses, the algorithm confirms that:
  - **21 PMUs are sufficient** for full observability of the Jordanian system.
- The algorithm identifies:
  - **2760 optimal placement options** with 21 PMUs.
- The second-stage result shows that a PMU at bus 43 or bus 44 is unnecessary, but not both.
- These multiple optimal placements allow the operator to select the best PMU plan for specific WAMS applications.

---

## Application-Based Placement Selection

After identifying all optimal PMU placements, the final placement can be selected based on weighted application priorities.

Examples include:

- maximum measurement redundancy,
- low-frequency oscillation monitoring,
- generator and tie-line monitoring,
- voltage stability monitoring,
- critical bus coverage,
- disturbance analysis,
- remedial action schemes,
- load rejection schemes,
- reactive power compensation control,
- HVDC control monitoring,
- black-start monitoring,
- model validation,
- frequency response analysis.

This is one of the key strengths of the paper: it separates the mathematical minimum-PMU problem from the practical engineering decision of selecting the most useful placement.

---

## Relationship to Your Research Hub

This paper is strongly connected to your later research on:

- PMU-based oscillation monitoring,
- ANN-based eigenvalue prediction,
- low-frequency oscillation damping,
- WAMS-based transient stability prediction,
- voltage stability monitoring,
- data-driven power system stability assessment.

It can be positioned as one of the foundational papers in your research direction on **measurement infrastructure for real-time power system stability monitoring**.

---

## Search-Friendly Questions

### What is the Global-Binary Algorithm?

The Global-Binary Algorithm is an optimal PMU placement algorithm that searches finite binary placement combinations to find minimum-PMU solutions for full power system observability.

### What problem does this paper solve?

The paper solves the optimal phasor measurement unit placement problem for wide-area monitoring systems while identifying all possible optimal placements, not only one solution.

### Why is optimal PMU placement important?

PMUs are expensive and generate large amounts of data. Optimal placement ensures full system observability with the minimum number of PMUs.

### What is the role of the connectivity matrix?

The connectivity matrix represents the power network topology and is used to compute which buses are observable for a given PMU placement.

### What is a zero-injection bus?

A zero-injection bus is a bus without load or generation. It can provide additional observability relationships through network equations and pseudo-measurements.

### Why does the algorithm split the power system into subsystems?

Splitting reduces the computational burden of searching the full binary solution space for large systems.

### Does the algorithm return one placement or many placements?

The algorithm returns all possible optimal placements with the minimum number of PMUs.

### What system is used as the case study?

The Jordanian transmission power system is used as the main case study.

### How many PMUs are needed for the Jordanian system?

The paper reports that 21 PMUs are sufficient for full observability of the Jordanian system.

### How many optimal placement options are found?

The paper reports 2760 placement options using 21 PMUs.

### How can the final placement be selected?

The final placement can be selected based on application-specific criteria such as redundancy, oscillation monitoring, voltage stability, and disturbance analysis.

---

## Keywords

Global-Binary Algorithm; optimal PMU placement; OPP; phasor measurement unit; PMU placement; wide-area monitoring system; WAMS; power system observability; connectivity matrix; zero-injection bus; ZIB; binary search algorithm; finite solution space; PMU redundancy; N-1 observability; Jordanian power system; Jordan transmission system; state estimation; PMU placement MATLAB; WAMS design; low-frequency oscillation monitoring; voltage stability monitoring; disturbance analysis; remedial action scheme; RAS; black start monitoring; model validation; power system monitoring; transmission network observability.

---

## Citation

```bibtex
@article{almomani2023globalbinary,
  title   = {Global-Binary Algorithm; New Optimal Phasor Measurement Unit Placement Algorithm},
  author  = {Al-Momani, Mohammad M. and Almbaideen, Amneh and Al-Gharaibah, Seba F. and Al-Awasa, Khaled and Allahham, Ahmed J.},
  journal = {Jordan Journal of Energy},
  volume  = {1},
  number  = {1},
  pages   = {72--86},
  year    = {2023},
  url     = {https://dsr.mutah.edu.jo/index.php/jje/article/view/4}
}
```

---

## Links

- **Journal page:** [https://dsr.mutah.edu.jo/index.php/jje/article/view/4](https://dsr.mutah.edu.jo/index.php/jje/article/view/4)
- **Code repository:** Coming soon.
- **MATLAB implementation:** Coming soon.
- **Related work:** Connectivity Matrix Algorithm; Modified Connectivity Matrix Algorithm; ANN-Based Low-Frequency Oscillation Damping; WAMS-Based Transient Stability Prediction.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Global-Binary Algorithm: New Optimal Phasor Measurement Unit Placement Algorithm",
  "name": "Global-Binary Algorithm: New Optimal Phasor Measurement Unit Placement Algorithm",
  "description": "A global-binary optimal PMU placement algorithm for wide-area monitoring systems using finite binary solution-space search, subsystem splitting, connectivity matrix observability, zero-injection buses, and Jordanian power system validation.",
  "author": [
    {
      "@type": "Person",
      "name": "Mohammad M. Al-Momani"
    },
    {
      "@type": "Person",
      "name": "Amneh Almbaideen"
    },
    {
      "@type": "Person",
      "name": "Seba F. Al-Gharaibah"
    },
    {
      "@type": "Person",
      "name": "Khaled Al-Awasa"
    },
    {
      "@type": "Person",
      "name": "Ahmed J. Allahham"
    }
  ],
  "keywords": [
    "Global-Binary Algorithm",
    "optimal PMU placement",
    "phasor measurement unit",
    "PMU placement",
    "wide-area monitoring system",
    "WAMS",
    "connectivity matrix",
    "power system observability",
    "zero-injection bus",
    "Jordanian power system",
    "state estimation",
    "binary search",
    "measurement redundancy",
    "low-frequency oscillation monitoring",
    "voltage stability monitoring"
  ],
  "url": "https://mohammadalmomani.github.io/papers/global-binary-optimal-pmu-placement/",
  "sameAs": [
    "https://dsr.mutah.edu.jo/index.php/jje/article/view/4"
  ],
  "identifier": "https://dsr.mutah.edu.jo/index.php/jje/article/view/4",
  "isAccessibleForFree": true,
  "publisher": {
    "@type": "Organization",
    "name": "Jordan Journal of Energy"
  }
}
</script>
