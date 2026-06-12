---
layout: page
title: "Extended Sensitivity-Aware Reactive Power Dispatch Algorithm for Smart Inverters with Multiple Control Modes"
description: "Extended sensitivity-aware reactive power dispatch algorithm for smart inverters with PQ, PV, and Volt-VAR control modes using Linear AC-OPF, LineDistFlow, VPP Volt-VAR dispatch, OpenDSS validation, IEEE 13-bus, and IEEE 123-bus test systems."
permalink: /papers/extended-sensitivity-aware-reactive-power-dispatch/
---

# Extended Sensitivity-Aware Reactive Power Dispatch Algorithm for Smart Inverters with Multiple Control Modes

**Authors:** Mohammad Almomani, Ahmed Alkhonain, and Venkataramana Ajjarapu  
**Research Area:** Smart Inverters, Reactive Power Dispatch, DER Coordination, Linear AC-OPF  
**Venue:** 2025 IEEE Power & Energy Society General Meeting (PESGM)  
**DOI:** [10.1109/PESGM52009.2025.11225466](https://doi.org/10.1109/PESGM52009.2025.11225466)  
**IEEE Xplore:** [https://ieeexplore.ieee.org/abstract/document/11225466](https://ieeexplore.ieee.org/abstract/document/11225466)

---

## Search-Friendly Title

Sensitivity-Aware Reactive Power Dispatch for Smart Inverters Using PQ, PV, Volt-VAR Control, Linear AC-OPF, and OpenDSS Validation

---

## Short Summary

This paper extends a sensitivity-aware reactive power dispatch algorithm for smart inverters operating under multiple control modes, including **PQ**, **PV**, and **Volt-VAR (VV)**.

The proposed method integrates smart inverter control modes into a scalable linear optimal power flow framework for unbalanced distribution systems. It enables distribution networks to operate as virtual power plants (VPPs) that provide coordinated voltage support and reactive power support to the transmission network.

The method is validated on the IEEE 13-bus and IEEE 123-bus distribution test systems, with OpenDSS simulations used to verify accuracy.

---

## Abstract

The increasing integration of Distributed Energy Resources (DERs) in distribution networks presents new challenges for voltage regulation and reactive power support. This paper extends a sensitivity-aware reactive power dispatch algorithm tailored to manage smart inverters operating under different control modes, including PQ, PV, and Volt-VAR (VV).

The proposed approach dynamically optimizes reactive power dispatch and voltage setpoints, enabling effective coordination among distribution systems as a virtual power plant (VPP) to support the transmission network.

The algorithm is applied to the IEEE 13-bus and IEEE 123-bus test systems, and its performance is validated by comparing results with OpenDSS simulations across various operating scenarios. Results show that the maximum error in the voltages is less than 0.015 p.u.

---

## Research Gap

Existing reactive power dispatch methods often focus on DERs operating in PQ mode or rely on nonlinear power flow formulations when modeling smart inverter control modes. This limits scalability and makes real-time dispatch more difficult in large unbalanced distribution networks.

This paper addresses this gap by integrating smart inverter control modes directly into a linear AC-OPF / LineDistFlow-based dispatch formulation. The method enables scalable optimization of PQ, PV, and Volt-VAR smart inverter operation while supporting distribution-level VPP coordination.

---

## Main Contributions

1. **Integration of smart inverter control modes into Linear OPF**  
   The paper incorporates PQ, PV, and Volt-VAR smart inverter modes into a linearized distribution optimal power flow framework.

2. **Sensitivity-aware dispatch for multiple inverter modes**  
   The proposed algorithm prioritizes inverter control actions based on sensitivity to substation reactive power and voltage support.

3. **Volt-VAR curve dispatch as a VPP service**  
   The method dispatches Volt-VAR curves directly to individual DERs, enabling distribution networks to behave as virtual power plants.

4. **Scalable linear optimization formulation**  
   The problem is reformulated as a standard linear optimization problem, improving computational efficiency for real-time dispatch.

5. **Validation with OpenDSS**  
   The proposed linear model is compared against OpenDSS simulations to validate voltage and reactive power accuracy.

6. **Testing on IEEE 13-bus and IEEE 123-bus systems**  
   The method is tested on standard distribution systems with multiple operating scenarios.

---

## Method Overview

The proposed dispatch framework follows these main steps:

### 1. Model the Unbalanced Distribution Network

The method uses a linearized distribution power flow model based on LinDistFlow / LinDist3Flow to represent unbalanced three-phase distribution networks.

### 2. Classify Smart Inverter Operating Modes

DERs are categorized based on their control mode:

- PQ mode,
- PV mode,
- Volt-VAR mode,
- non-generator buses.

### 3. Build Identification and Incidence Matrices

The algorithm constructs identification matrices for each inverter type and rearranges the network model to represent the contribution of each source category.

### 4. Formulate Linear Power Flow Equations

The power flow relationship is written in compact linear form, allowing voltage magnitudes, reactive power outputs, and voltage setpoints to be included in the optimization.

### 5. Formulate Sensitivity-Aware Dispatch Objective

The objective function prioritizes DERs that are most effective in supporting the substation and transmission network.

### 6. Apply Operational Constraints

The formulation includes constraints for:

- reactive power balance at the substation,
- upper and lower voltage limits,
- maximum power flow in distribution lines,
- maximum reactive power capability,
- VPP-level Volt-VAR curve requirements.

### 7. Validate Against OpenDSS

The proposed model is compared with OpenDSS simulations under multiple inverter operating modes.

---

## Smart Inverter Control Modes

### PQ Mode

In PQ mode, the inverter outputs fixed active power and fixed reactive power.

### PV Mode

In PV mode, the inverter maintains fixed active power while regulating voltage.

### Volt-VAR Mode

In Volt-VAR mode, the inverter adjusts reactive power based on local voltage according to a droop-based Volt-VAR curve.

### Mixed Mode

In mixed mode, different DERs operate under different control modes. This allows a distribution system to combine PQ, PV, and Volt-VAR operation in the same dispatch framework.

---

## Virtual Power Plant Voltage Support

The paper treats aggregated active distribution networks as virtual power plants that can provide reactive power support to the transmission system.

At the VPP level, a droop-based Volt-VAR relationship is used so that the distribution network can support the transmission system through coordinated reactive power response.

At the DER level, the dispatch algorithm disaggregates the VPP-level control requirement into individual smart inverter setpoints.

---

## Test Systems

The proposed method is validated using:

- IEEE 13-bus distribution test system,
- IEEE 123-bus distribution test system,
- PQ inverter operating scenario,
- PV inverter operating scenario,
- Volt-VAR inverter operating scenario,
- mixed inverter operating scenario,
- OpenDSS nonlinear simulation comparison.

---

## Key Results

- The proposed method achieves a maximum voltage error below **0.015 p.u.** compared with OpenDSS.
- In the IEEE 13-bus system, the maximum voltage deviation is approximately:
  - **0.015 p.u.** in PQ mode,
  - **0.010 p.u.** in PV mode,
  - **0.012 p.u.** in Volt-VAR mode,
  - **0.014 p.u.** in mixed control mode.
- The IEEE 123-bus case is solved in under **0.5 seconds**.
- The method provides acceptable accuracy compared with nonlinear OpenDSS simulations.
- The L1 norm voltage error is less than **0.5%**.
- The L1 norm reactive power error is around **8%** in the reported cases.
- The linear programming structure supports scalability to larger distribution systems.

---

## Search-Friendly Questions

### What is the main goal of this paper?

The main goal is to extend sensitivity-aware reactive power dispatch so that it can manage smart inverters operating under multiple control modes, including PQ, PV, and Volt-VAR.

### What problem does this paper solve?

The paper solves the problem of dispatching reactive power and voltage setpoints in DER-rich distribution systems with different smart inverter operating modes while maintaining scalability through a linear optimization formulation.

### What is sensitivity-aware reactive power dispatch?

Sensitivity-aware reactive power dispatch prioritizes DERs based on how strongly their reactive power affects voltage support or reactive power exchange at the substation.

### Which smart inverter modes are included?

The method includes PQ mode, PV mode, Volt-VAR mode, and mixed operation where different DERs operate under different modes.

### Why is Linear AC-OPF used?

Linear AC-OPF enables faster and more scalable optimization compared with nonlinear formulations, which is important for real-time or large-scale dispatch.

### How does this paper use Volt-VAR control?

The paper dispatches Volt-VAR control curves at the DER level and also uses VPP-level Volt-VAR behavior to coordinate distribution systems with the transmission network.

### What is the role of the virtual power plant?

The distribution system is treated as a virtual power plant that can provide coordinated reactive power and voltage support to the transmission network.

### How is the method validated?

The method is validated by comparing the proposed linear model with OpenDSS simulations on IEEE 13-bus and IEEE 123-bus test systems.

### What is the maximum voltage error?

The maximum voltage error reported is less than 0.015 p.u.

### How fast is the method on the IEEE 123-bus system?

The algorithm solves the IEEE 123-bus test case in under 0.5 seconds.

---

## Keywords

smart inverter; reactive power dispatch; sensitivity-aware dispatch; Volt-VAR control; Volt/VAR control; PQ mode; PV mode; smart inverter control modes; distributed energy resources; DERs; virtual power plant; VPP; TSO-DSO coordination; distribution system voltage support; transmission voltage support; Linear AC-OPF; linear optimal power flow; LineDistFlow; LinDistFlow; LinDist3Flow; unbalanced distribution network; reactive power support; voltage regulation; OpenDSS validation; IEEE 13-bus test system; IEEE 123-bus test system; DER voltage support; distribution optimal power flow; smart inverter setpoint optimization; Volt-VAR curve dispatch; power system optimization.

---

## Citation

```bibtex
@inproceedings{almomani2025extended,
  title     = {Extended Sensitivity-Aware Reactive Power Dispatch Algorithm for Smart Inverters with Multiple Control Modes},
  author    = {Almomani, Mohammad and Alkhonain, Ahmed and Ajjarapu, Venkataramana},
  booktitle = {2025 IEEE Power & Energy Society General Meeting (PESGM)},
  year      = {2025},
  doi       = {10.1109/PESGM52009.2025.11225466},
  url       = {https://ieeexplore.ieee.org/abstract/document/11225466}
}
```

---

## Links

- **IEEE Xplore:** [https://ieeexplore.ieee.org/abstract/document/11225466](https://ieeexplore.ieee.org/abstract/document/11225466)
- **DOI:** [https://doi.org/10.1109/PESGM52009.2025.11225466](https://doi.org/10.1109/PESGM52009.2025.11225466)
- **Code repository:** Coming soon.
- **Dataset / test cases:** Coming soon.
- **Related work:** TSO-DSO Coordinated Reactive Power Dispatch for Smart Inverters with Multiple Control Modes — Real-Time Implementation

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Extended Sensitivity-Aware Reactive Power Dispatch Algorithm for Smart Inverters with Multiple Control Modes",
  "name": "Extended Sensitivity-Aware Reactive Power Dispatch Algorithm for Smart Inverters with Multiple Control Modes",
  "description": "An extended sensitivity-aware reactive power dispatch algorithm for smart inverters with PQ, PV, and Volt-VAR control modes using Linear AC-OPF, VPP Volt-VAR dispatch, OpenDSS validation, and IEEE 13-bus and IEEE 123-bus test systems.",
  "author": [
    {
      "@type": "Person",
      "name": "Mohammad Almomani"
    },
    {
      "@type": "Person",
      "name": "Ahmed Alkhonain"
    },
    {
      "@type": "Person",
      "name": "Venkataramana Ajjarapu"
    }
  ],
  "keywords": [
    "smart inverter",
    "reactive power dispatch",
    "sensitivity-aware dispatch",
    "Volt-VAR control",
    "PQ mode",
    "PV mode",
    "DER",
    "virtual power plant",
    "VPP",
    "Linear AC-OPF",
    "LineDistFlow",
    "LinDist3Flow",
    "OpenDSS",
    "IEEE 13-bus",
    "IEEE 123-bus",
    "voltage regulation",
    "distribution optimal power flow"
  ],
  "url": "https://mohammadalmomani.github.io/papers/extended-sensitivity-aware-reactive-power-dispatch/",
  "sameAs": [
    "https://ieeexplore.ieee.org/abstract/document/11225466",
    "https://doi.org/10.1109/PESGM52009.2025.11225466"
  ],
  "identifier": "https://doi.org/10.1109/PESGM52009.2025.11225466",
  "isAccessibleForFree": false,
  "publisher": {
    "@type": "Organization",
    "name": "IEEE"
  }
}
</script>
