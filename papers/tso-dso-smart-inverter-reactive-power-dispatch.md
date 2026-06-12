---
layout: page
title: "TSO-DSO Coordinated Reactive Power Dispatch for Smart Inverters with Multiple Control Modes"
description: "Real-time TSO-DSO coordinated reactive power dispatch for IEEE 1547 smart inverters using MILP, SOS1, RLS, Volt-VAR, Volt-Watt, Watt-VAR, OpenDSS, and IEEE 13-bus and IEEE 123-bus test systems."
permalink: /papers/tso-dso-smart-inverter-reactive-power-dispatch/
---

# TSO-DSO Coordinated Reactive Power Dispatch for Smart Inverters with Multiple Control Modes — Real-Time Implementation

**Authors:** Mohammad Almomani, Ahmed Alkhonain, and Venkataramana Ajjarapu  
**Research Area:** DER Coordination, Smart Inverter Control, TSO-DSO Reactive Power Dispatch  
**Status:** arXiv preprint / submitted version  
**arXiv:** [https://arxiv.org/abs/2604.07064](https://arxiv.org/abs/2604.07064)

---

## Search-Friendly Title

Real-Time TSO-DSO Reactive Power Dispatch for IEEE 1547 Smart Inverters Using Volt-VAR, Volt-Watt, Watt-VAR, MILP, SOS1, and RLS

---

## Short Summary

This paper presents a real-time Transmission System Operator–Distribution System Operator (TSO-DSO) coordinated reactive power dispatch framework for DER-rich distribution systems with smart inverters.

The proposed method models IEEE 1547-compliant smart inverter control modes, including **Volt-VAR**, **Volt-Watt**, and **Watt-VAR**. The framework uses a sensitivity-aware mixed-integer linear programming (MILP) formulation, Special Ordered Sets of type 1 (SOS1), Recursive Least Squares (RLS) estimation, and an observable/unobservable network reformulation to support real-time implementation under limited measurement conditions.

The method is validated using IEEE 13-bus and IEEE 123-bus distribution systems connected to an IEEE 9-bus transmission system.

---

## Abstract

This paper presents TSO-DSO coordinated reactive power dispatch with a focus on real-time implementation. A sensitivity-aware mixed-integer linear programming (MILP) formulation is developed to model IEEE 1547-compliant droop-based control modes of smart inverters, including Volt-VAR, Volt-Watt, and Watt-VAR.

The algorithm employs a hierarchical optimization strategy using Special Ordered Sets of type 1 (SOS1) to enhance computational efficiency. It also supports limited-measurement scenarios using Recursive Least Squares (RLS) estimation.

The proposed method is tested on IEEE 13-bus and IEEE 123-bus distribution networks connected to a 9-bus transmission system. Results demonstrate the feasibility and effectiveness of the real-time dispatch framework in improving voltage regulation and minimizing power curtailment.

---

## Research Gap

Existing reactive power dispatch and distribution optimal power flow methods often do not fully capture the local IEEE 1547 droop-based behavior of smart inverters. Many approaches assume simplified inverter models, fixed control modes, full network observability, or ideal P-Q flexibility.

This paper addresses this gap by jointly optimizing smart inverter operation modes and droop parameters in a real-time TSO-DSO coordination framework while considering limited observability and practical local controller behavior.

---

## Main Contributions

1. **Unified MILP formulation for IEEE 1547 smart inverter control modes**  
   Volt-VAR, Volt-Watt, and Watt-VAR droop control modes are modeled using piecewise-linear constraints and Big-M modeling.

2. **Real-time hierarchical optimization using SOS1**  
   The method uses SOS1-based mode and segment selection to improve computational scalability.

3. **Limited-observability implementation using RLS**  
   The distribution network is divided into observable and unobservable sets, and Recursive Least Squares is used to estimate unknown parameters online.

4. **TSO-DSO coordination algorithm**  
   The framework includes DSO aggregation, TSO reactive power dispatch, DSO disaggregation, and iterative re-aggregation.

5. **Validation on standard test systems**  
   The method is tested on IEEE 13-bus and IEEE 123-bus distribution networks connected to an IEEE 9-bus transmission system.

6. **Improved voltage regulation with low curtailment**  
   The optimized smart-inverter dispatch improves voltage support while reducing unnecessary real-power curtailment.

---

## Method Overview

The proposed framework has three main stages:

### 1. DSO Aggregation

The DSO estimates the available distribution-level reactive power capability at the TSO-DSO interface.

### 2. TSO Dispatch

The TSO solves a transmission-level reactive power dispatch problem and sends a requested reactive power value to the DSO.

### 3. DSO Disaggregation

The DSO allocates the requested reactive power among DER smart inverters while respecting local inverter control modes, droop curves, voltage constraints, and active-power limits.

---

## Smart Inverter Control Modes

### Volt-VAR Control

Reactive power is adjusted based on local voltage magnitude.

### Volt-Watt Control

Active power is curtailed when voltage exceeds specified limits.

### Watt-VAR Control

Reactive power is adjusted based on active power output.

---

## Optimization and Implementation Tools

- Mixed-Integer Linear Programming (MILP)
- Special Ordered Sets of type 1 (SOS1)
- Big-M piecewise-linear modeling
- LineDistOPF / LinDist3Flow-based distribution modeling
- Recursive Least Squares (RLS) estimation
- OpenDSS and Python for distribution simulation
- Gurobi for optimization
- PandaPower / PowerModels / Julia for transmission-level simulation

---

## Test Systems

- IEEE 13-bus distribution test system
- IEEE 123-bus distribution test system
- IEEE 9-bus transmission test system
- Multiple DER penetration scenarios
- Multiple smart-inverter control scenarios
- Limited-measurement and real-time implementation settings

---

## Key Results

- SOS1 improves computational efficiency compared with a full binary MILP formulation.
- The optimized droop-based operation reaches the maximum available active power while preserving useful reactive flexibility.
- The optimized mode achieves a reactive flexibility range of approximately **1.4 MVAR injection to -0.9 MVAR absorption** in the reported case.
- The iterative TSO-DSO coordination process tracks the requested reactive power with small error after a limited number of DSO iterations.
- Coordinated multi-mode smart-inverter dispatch improves transmission-voltage profiles under contingency conditions.
- The SOS1 formulation scales better than the binary formulation for large numbers of DERs.

---

## Search-Friendly Questions

### What is TSO-DSO coordinated reactive power dispatch?

TSO-DSO coordinated reactive power dispatch is a framework where the distribution system estimates its available reactive power flexibility from DERs and communicates this capability to the transmission operator. The transmission operator then requests reactive power support, and the distribution operator disaggregates the request among local DERs.

### How are smart inverters used for reactive power dispatch?

Smart inverters provide reactive power support through IEEE 1547 control modes such as Volt-VAR, Volt-Watt, and Watt-VAR. This paper optimizes the selection of these modes and their droop parameters so that dispatch commands remain feasible for local inverter controllers.

### Why is IEEE 1547 important for smart inverter dispatch?

IEEE 1547 defines interconnection and interoperability requirements for DERs and includes operational modes for voltage and reactive power support. Modeling these modes is important because smart inverters cannot always follow arbitrary P-Q setpoints if those setpoints violate their embedded local control curves.

### Why does this paper use SOS1?

SOS1 improves the computational scalability of the MILP formulation. It helps select one active control mode and one active droop segment while reducing solver complexity compared with a full binary-variable formulation.

### How does the method work with limited measurements?

The distribution network is partitioned into observable and unobservable parts. Recursive Least Squares is used to estimate unknown parameters that capture the effect of unobservable states on observable buses.

### What test systems are used?

The method is tested on the IEEE 13-bus and IEEE 123-bus distribution systems connected to an IEEE 9-bus transmission system.

### What is the main advantage of the proposed method?

The main advantage is that it provides real-time, standards-compliant, and scalable TSO-DSO reactive power coordination while respecting actual smart-inverter local controller behavior.

---

## Keywords

TSO-DSO coordination; reactive power dispatch; DER reactive power support; smart inverter optimization; IEEE 1547-2018; Volt-VAR; Volt-Watt; Watt-VAR; smart inverter droop control; inverter control modes; mixed-integer linear programming; MILP; Special Ordered Sets; SOS1; Recursive Least Squares; RLS; limited observability; LineDistOPF; LinDist3Flow; unbalanced distribution networks; multiphase distribution systems; IEEE 13-bus test feeder; IEEE 123-bus test feeder; IEEE 9-bus transmission system; OpenDSS; Gurobi; PandaPower; PowerModels; voltage regulation; PV curtailment; distributed energy resources; DERs; distribution optimal power flow.

---

## Citation

```bibtex
@misc{almomani2026tsodso,
  title         = {TSO--DSO Coordinated Reactive Power Dispatch for Smart Inverters with Multiple Control Modes -- Real-Time Implementation},
  author        = {Almomani, Mohammad and Alkhonain, Ahmed and Ajjarapu, Venkataramana},
  year          = {2026},
  eprint        = {2604.07064},
  archivePrefix = {arXiv},
  primaryClass  = {eess.SY},
  url           = {https://arxiv.org/abs/2604.07064}
}
```

---

## Links

- **arXiv page:** [https://arxiv.org/abs/2604.07064](https://arxiv.org/abs/2604.07064)
- **PDF:** [https://arxiv.org/pdf/2604.07064](https://arxiv.org/pdf/2604.07064)
- **Code repository:** Coming soon.
- **Dataset / test cases:** Coming soon.
- **Related paper:** Extended Sensitivity-Aware Reactive Power Dispatch Algorithm for Smart Inverters with Multiple Control Modes

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "TSO-DSO Coordinated Reactive Power Dispatch for Smart Inverters with Multiple Control Modes — Real-Time Implementation",
  "name": "TSO-DSO Coordinated Reactive Power Dispatch for Smart Inverters with Multiple Control Modes — Real-Time Implementation",
  "description": "A real-time TSO-DSO coordinated reactive power dispatch framework for IEEE 1547 smart inverters using MILP, SOS1, RLS, Volt-VAR, Volt-Watt, and Watt-VAR control modes.",
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
    "TSO-DSO coordination",
    "reactive power dispatch",
    "smart inverter",
    "IEEE 1547",
    "Volt-VAR",
    "Volt-Watt",
    "Watt-VAR",
    "DER",
    "MILP",
    "SOS1",
    "Recursive Least Squares",
    "RLS",
    "LineDistOPF",
    "OpenDSS",
    "IEEE 13-bus",
    "IEEE 123-bus",
    "IEEE 9-bus"
  ],
  "url": "https://mohammadalmomani.github.io/papers/tso-dso-smart-inverter-reactive-power-dispatch/",
  "sameAs": [
    "https://arxiv.org/abs/2604.07064"
  ],
  "identifier": "arXiv:2604.07064",
  "isAccessibleForFree": true
}
</script>
