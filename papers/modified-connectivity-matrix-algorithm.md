---
layout: page
title: "Modified Connectivity Matrix Algorithm"
description: "Modified Connectivity Matrix Algorithm for optimal PMU placement with N-1 redundancy, zero-injection buses, measurement redundancy, line outage redundancy, connectivity matrix observability, and IEEE 14-bus, 30-bus, 57-bus, and 118-bus validation."
permalink: /papers/modified-connectivity-matrix-algorithm/
---

# Modified Connectivity Matrix Algorithm

**Authors:** Mohammad M. Al-Momani, Khaled Awasa, Abdullah Odienate, Omar Radaideh, and Seba F. Algharaibeh  
**Research Area:** Optimal PMU Placement, WAMS, Power System Observability, Measurement Redundancy  
**Conference:** 2022 Advances in Science and Engineering Technology International Conferences (ASET)  
**DOI:** [10.1109/ASET53988.2022.9735116](https://doi.org/10.1109/ASET53988.2022.9735116)  
**IEEE Xplore:** [https://ieeexplore.ieee.org/document/9735116](https://ieeexplore.ieee.org/document/9735116)

---

## Search-Friendly Title

Modified Connectivity Matrix Algorithm for Optimal PMU Placement With N-1 Redundancy, Zero-Injection Buses, and WAMS Observability

---

## Short Summary

This paper proposes the **Modified Connectivity Matrix Algorithm (MCMA)** for optimal phasor measurement unit placement in power systems.

The original Connectivity Matrix Algorithm (CMA) is a fast PMU placement method for achieving full system observability. This paper modifies CMA to support:

- **N-1 PMU loss criteria**,
- **double measurement redundancy**,
- **user-defined redundancy levels**,
- **zero-injection bus modeling**,
- **line-outage redundancy**,
- **partial redundancy at selected buses or lines**.

The algorithm is validated on IEEE 14-bus, IEEE 30-bus, IEEE 57-bus, and IEEE 118-bus systems. The reported computational time of MCMA is less than 10% of the fastest comparable algorithm in the literature.

---

## Abstract

The Connectivity Matrix Algorithm is a straightforward method for obtaining the optimal location of phasor measurement units in a power system. This paper proposes a modification to the Connectivity Matrix Algorithm to consider N-1 criteria.

The modified algorithm is valid for obtaining optimal PMU placement while considering any level of measurement redundancy at any selected location. The algorithm is validated with and without zero-injection buses for the double-redundancy condition.

The proposed MCMA is applied to IEEE 14-bus, IEEE 30-bus, IEEE 57-bus, and IEEE 118-bus systems. The computational time of the modified algorithm is reported to be less than 10% of the fastest algorithm in the literature.

---

## Research Gap

The original Connectivity Matrix Algorithm can identify PMU placements for full observability, but practical WAMS applications often require more than basic observability.

For real-time control, protection, and wide-area monitoring, the system may need:

- observability after a PMU loss,
- observability after a line outage,
- measurement redundancy at critical buses,
- redundancy for selected transmission lines,
- zero-injection bus modeling,
- application-specific redundancy levels.

This paper addresses this gap by modifying the CMA update rule and adding a checker condition that allows the user to control the required observability redundancy level.

---

## Main Contributions

1. **Modified Connectivity Matrix Algorithm**  
   The paper extends the original CMA to handle N-1 redundancy and measurement redundancy requirements.

2. **N-1 PMU loss criterion**  
   MCMA can place PMUs so the system remains observable even if one PMU is lost.

3. **Line-outage redundancy capability**  
   The algorithm can apply redundancy to selected connectivity matrix elements representing transmission lines.

4. **Flexible redundancy levels**  
   The user can select no redundancy, double redundancy, triple redundancy, or partial redundancy at selected locations.

5. **Zero-injection bus inclusion**  
   The method includes ZIB handling, improving PMU placement efficiency and reducing required PMU count.

6. **Checker-condition mechanism**  
   A checker is introduced to remove the effect of buses that have already achieved the required redundancy.

7. **Validation on standard IEEE systems**  
   The algorithm is tested on IEEE 14-bus, IEEE 30-bus, IEEE 57-bus, and IEEE 118-bus test systems.

8. **Fast computational performance**  
   The computational time is reported to be less than 10% of the fastest algorithm in the literature.

---

## Background: Connectivity Matrix Algorithm

The Connectivity Matrix Algorithm is based on the network connectivity matrix.

For a system with `n` buses, the connectivity matrix is an `n × n` matrix:

- diagonal elements are equal to 1,
- off-diagonal elements are 1 if two buses are directly connected,
- off-diagonal elements are 0 if two buses are not directly connected.

The original CMA selects PMU locations iteratively. At each iteration, the best PMU location is selected based on the connectivity matrix and an observability weight.

Once a PMU is installed at a bus, the bus itself and its directly connected neighboring buses become observable.

---

## Zero-Injection Bus Modeling

A zero-injection bus is a bus with no load and no generation. Zero-injection buses provide additional pseudo-measurement relationships that can reduce the number of required PMUs.

The paper discusses several ZIB implementation rules, including:

- removing a bus connected to a ZIB when observability can be inferred,
- removing a ZIB with two connections,
- reconnecting selected neighboring buses when a ZIB has three connections,
- merging connected ZIBs,
- simplifying cases where a ZIB has more than three connections.

Including ZIBs is important because it improves observability without requiring additional PMUs.

---

## Proposed MCMA Modification

The original CMA updates the modified matrix by replacing observable buses with zeros.

The proposed MCMA changes this update mechanism.

Instead of immediately removing observable buses, MCMA:

1. multiplies the rows of buses observed by one PMU by 2,
2. replaces the column of the bus where the PMU is installed with zeros,
3. applies a checker condition to identify buses that already meet the required redundancy.

For double redundancy:

```text
checker value = 4
```

For triple redundancy:

```text
checker value = 8
```

If an element reaches the checker value, it means that the bus has achieved the required observability redundancy and no longer needs weight in the next iteration.

---

## Optimal Bus Selection Rule

In MCMA, the modified matrix is used directly to select the next PMU location.

The optimal bus is selected using a weighted connectivity measure that prioritizes buses still needing observability or redundancy.

Conceptually, the algorithm selects the bus that maximizes observability gain while reducing the influence of already-observed buses.

This prevents repeated PMU placement at the same bus and allows the redundancy requirement to guide the placement sequence.

---

## Why MCMA Is Important

The MCMA is important because PMU placement for WAMS should not only answer:

```text
Where is the minimum number of PMUs for full observability?
```

It should also answer:

```text
Where should PMUs be placed so the system remains observable after PMU loss or line outage?
```

and:

```text
Which critical buses or lines should have higher redundancy?
```

This is essential for protection, control, state estimation, oscillation monitoring, voltage stability monitoring, remedial action schemes, and wide-area damping systems.

---

## IEEE 14-Bus Example

The paper uses the IEEE 14-bus system to explain the MCMA process.

For the double-redundancy condition with zero-injection bus consideration, the algorithm selects seven PMUs.

The optimal placement for IEEE 14-bus with ZIB and single PMU loss condition is:

```text
1, 2, 4, 6, 9, 10, 13
```

This means that the IEEE 14-bus system can remain observable under the selected redundancy condition using 7 PMUs.

---

## Validation Test Systems

The proposed MCMA is validated using:

- IEEE 14-bus system,
- IEEE 30-bus system,
- IEEE 57-bus system,
- IEEE 118-bus system.

The paper reports results both:

- without considering zero-injection buses,
- with zero-injection buses.

---

## Key Results Without Considering ZIBs

For a single PMU loss condition without considering zero-injection buses, the reported PMU counts are:

| Test System | Number of PMUs |
|---|---:|
| IEEE 14-bus | 9 |
| IEEE 30-bus | 20 |
| IEEE 57-bus | 32 |
| IEEE 118-bus | 66 |

---

## Key Results Considering ZIBs

For a single PMU loss condition considering zero-injection buses, the reported PMU counts are:

| Test System | Number of PMUs |
|---|---:|
| IEEE 14-bus | 7 |
| IEEE 30-bus | 15 |
| IEEE 57-bus | 24 |
| IEEE 118-bus | 62 |

These results show that including zero-injection buses can significantly reduce the number of PMUs required for N-1 observability.

---

## Comparison With Existing Algorithms

The paper compares MCMA with three existing algorithms for N-1 criteria considering zero-injection buses.

| Test System | Proposed MCMA | Algorithm 1 | Algorithm 2 | Algorithm 3 |
|---|---:|---:|---:|---:|
| IEEE 14-bus | 7 | 7 | 7 | 7 |
| IEEE 30-bus | 15 | 15 | 17 | 16 |
| IEEE 57-bus | 24 | 26 | 26 | 27 |
| IEEE 118-bus | 62 | 64 | 65 | 62 |

The proposed algorithm matches or improves the PMU count compared with the referenced algorithms for the reported systems.

---

## Three-Area Test System Result

The paper also notes that the three-area test system requires three PMUs to be fully observable at the selected operating point.

The PMU locations are:

```text
8, 11, 14
```

These locations make the system fully observable in both ring and string configurations.

---

## Practical Applications

The MCMA can support PMU placement for:

- wide-area monitoring systems,
- wide-area protection,
- wide-area control,
- state estimation,
- oscillation monitoring,
- small-signal stability monitoring,
- voltage stability monitoring,
- remedial action schemes,
- transmission-line outage monitoring,
- N-1 PMU loss robustness,
- smart grid control and protection.

---

## Relationship to Your Research Hub

This paper is a key foundation for your measurement-based stability research.

It connects directly to:

- PMU placement,
- WAMS design,
- low-frequency oscillation monitoring,
- ANN-based eigenvalue prediction,
- transient stability prediction using wide-area measurements,
- real-time voltage stability assessment,
- measurement redundancy for resilient stability monitoring.

For your research hub, this paper should be grouped under:

```text
PMU Placement, WAMS, and Measurement Infrastructure for Stability Monitoring
```

---

## Search-Friendly Questions

### What is the Modified Connectivity Matrix Algorithm?

The Modified Connectivity Matrix Algorithm is an optimal PMU placement method that extends the original Connectivity Matrix Algorithm to support N-1 criteria, measurement redundancy, zero-injection buses, and selected bus or line redundancy.

### What problem does this paper solve?

The paper solves the optimal PMU placement problem when full observability alone is not enough and the system requires redundancy for PMU loss, line outage, or selected critical buses.

### Why is N-1 PMU redundancy important?

N-1 redundancy ensures that the power system can remain observable even if one PMU fails or becomes unavailable.

### How does MCMA differ from the original CMA?

The original CMA removes observable buses from future iterations. MCMA instead reduces their weight by multiplying observable rows, uses a checker condition, and allows buses to remain active until the desired redundancy level is achieved.

### What is the checker condition?

The checker condition detects when a bus has reached the required redundancy level. For double redundancy, the checker value is 4. For triple redundancy, the checker value is 8.

### Can MCMA handle zero-injection buses?

Yes. The algorithm includes zero-injection bus implementation rules to improve observability and reduce the number of required PMUs.

### Can MCMA handle line outage redundancy?

Yes. For line outage redundancy, the checker condition can be applied to selected connectivity-matrix elements representing lines.

### Which IEEE systems are used for validation?

The paper validates MCMA on IEEE 14-bus, IEEE 30-bus, IEEE 57-bus, and IEEE 118-bus systems.

### How many PMUs are needed for IEEE 14-bus with ZIB and N-1 PMU loss?

The paper reports 7 PMUs.

### How many PMUs are needed for IEEE 118-bus with ZIB and N-1 PMU loss?

The paper reports 62 PMUs.

### How fast is MCMA?

The paper reports that the computational time of the modified algorithm is less than 10% of the fastest algorithm in the literature.

### Why is this paper important for WAMS?

It provides a fast and flexible PMU placement method that supports redundancy, observability, and application-specific monitoring requirements.

---

## Keywords

Modified Connectivity Matrix Algorithm; MCMA; Connectivity Matrix Algorithm; CMA; optimal PMU placement; OPP; phasor measurement unit; PMU; PMU redundancy; N-1 criterion; PMU loss; line outage redundancy; measurement redundancy; double redundancy; triple redundancy; zero-injection bus; ZIB; wide-area monitoring system; WAMS; wide-area monitoring protection and control; WAMPAC; power system observability; connectivity matrix; topology matrix; state estimation; IEEE 14-bus; IEEE 30-bus; IEEE 57-bus; IEEE 118-bus; smart grid monitoring; PMU placement algorithm; power system protection; synchrophasor measurement; resilient monitoring.

---

## Citation

```bibtex
@inproceedings{almomani2022modified,
  title     = {Modified Connectivity Matrix Algorithm},
  author    = {Al-Momani, Mohammad M. and Awasa, Khaled and Odienate, Abdullah and Radaideh, Omar and Algharaibeh, Seba F.},
  booktitle = {2022 Advances in Science and Engineering Technology International Conferences (ASET)},
  year      = {2022},
  doi       = {10.1109/ASET53988.2022.9735116},
  url       = {https://ieeexplore.ieee.org/document/9735116}
}
```

---

## Links

- **IEEE Xplore:** [https://ieeexplore.ieee.org/document/9735116](https://ieeexplore.ieee.org/document/9735116)
- **DOI:** [https://doi.org/10.1109/ASET53988.2022.9735116](https://doi.org/10.1109/ASET53988.2022.9735116)
- **Code repository:** Coming soon.
- **MATLAB implementation:** Coming soon.
- **Related work:** Connectivity Matrix Algorithm: A New Optimal Phasor Measurement Unit Placement Algorithm; Global-Binary Algorithm: New Optimal Phasor Measurement Unit Placement Algorithm; ANN-Based Low-Frequency Oscillation Damping.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Modified Connectivity Matrix Algorithm",
  "name": "Modified Connectivity Matrix Algorithm",
  "description": "A modified connectivity matrix algorithm for optimal PMU placement with N-1 redundancy, zero-injection buses, measurement redundancy, line-outage redundancy, and IEEE 14-bus, 30-bus, 57-bus, and 118-bus validation.",
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
      "name": "Omar Radaideh"
    },
    {
      "@type": "Person",
      "name": "Seba F. Algharaibeh"
    }
  ],
  "keywords": [
    "Modified Connectivity Matrix Algorithm",
    "MCMA",
    "Connectivity Matrix Algorithm",
    "CMA",
    "optimal PMU placement",
    "phasor measurement unit",
    "PMU",
    "N-1 criterion",
    "PMU redundancy",
    "zero-injection bus",
    "ZIB",
    "wide-area monitoring system",
    "WAMS",
    "WAMPAC",
    "power system observability",
    "IEEE 14-bus",
    "IEEE 30-bus",
    "IEEE 57-bus",
    "IEEE 118-bus",
    "state estimation"
  ],
  "url": "https://mohammadalmomani.github.io/papers/modified-connectivity-matrix-algorithm/",
  "sameAs": [
    "https://ieeexplore.ieee.org/document/9735116",
    "https://doi.org/10.1109/ASET53988.2022.9735116"
  ],
  "identifier": "https://doi.org/10.1109/ASET53988.2022.9735116",
  "isAccessibleForFree": false,
  "publisher": {
    "@type": "Organization",
    "name": "IEEE"
  }
}
</script>
