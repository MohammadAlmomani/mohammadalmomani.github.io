---
layout: page
title: "Modelling and Testing of a Numerical Pilot Distance Relay for Compensated Transmission Lines"
description: "Numerical pilot distance relay for FACTS-compensated transmission lines using MATLAB Simulink, five-zone mho characteristic, reverse zones, STATCOM, SSSC, UPFC, fault detection, phase selection, and compensated line protection."
permalink: /papers/numerical-pilot-distance-relay-compensated-lines/
---

# Modelling and Testing of a Numerical Pilot Distance Relay for Compensated Transmission Lines

**Authors:** Mohammad M. Almomani and Seba F. Algharaibeh  
**Research Area:** Power System Protection, Distance Relays, FACTS-Compensated Transmission Lines  
**Journal:** International Journal of Scientific Research and Engineering Development  
**Volume / Issue:** Volume 3, Issue 6, 2020  
**Pages:** 776–786

---

## Search-Friendly Title

Numerical Pilot Distance Relay for FACTS-Compensated Transmission Lines Using Five-Zone Mho Characteristic, STATCOM, SSSC, UPFC, and MATLAB Simulink

---

## Short Summary

This paper proposes and tests a numerical pilot distance protection scheme for compensated transmission lines.

The proposed relay scheme addresses the underreach and overreach problems caused by FACTS devices installed on transmission lines. The method is valid for different FACTS types, including:

- shunt FACTS devices such as STATCOM,
- series FACTS devices such as SSSC,
- compound FACTS devices such as UPFC.

The relay is modeled and tested in MATLAB 2020a / Simulink. The model includes:

- fault detection,
- phase selection,
- measured impedance calculation,
- five-zone mho characteristic,
- three traditional forward zones,
- two additional reverse zones.

---

## Abstract

FACTS technologies are widely used in high-voltage and extra-high-voltage AC transmission systems to control power flow. However, FACTS devices can cause traditional distance relays to misoperate because they modify the apparent impedance seen by the relay.

This paper presents a special pilot distance protection scheme for compensated transmission lines. The scheme is valid for shunt, series, and compound FACTS devices and for capacitive and inductive operating modes.

The proposed scheme is modeled in MATLAB 2020a / Simulink. It includes a fault detection algorithm, phase selection, measured impedance calculation, and a five-zone mho characteristic. The model is verified using single-line-to-ground faults, double-line faults, double-line-to-ground faults, and three-phase faults.

The results show that the relay operates correctly for different FACTS device types, locations, operating points, and fault scenarios.

---

## Research Gap

Traditional distance relays are designed around apparent impedance measurement. In compensated transmission lines, FACTS devices can modify both the magnitude and angle of the apparent impedance.

This can lead to:

- relay underreach,
- relay overreach,
- incorrect zone detection,
- delayed or undesired tripping,
- protection miscoordination.

Existing traditional three-zone distance relays may not reliably detect fault-zone boundaries in FACTS-compensated lines. This paper addresses that gap by proposing a pilot distance scheme with communication-assisted logic and additional reverse zones.

---

## Main Contributions

1. **Pilot distance protection scheme for compensated lines**  
   The paper proposes a communication-assisted distance relay scheme for FACTS-compensated transmission lines.

2. **Applicability to different FACTS types**  
   The method is tested with STATCOM, SSSC, and UPFC.

3. **Five-zone mho characteristic**  
   The relay includes three traditional forward zones and two additional reverse zones.

4. **Fault detection and phase selection**  
   The model includes algorithms for detecting faulty phases and selecting the correct fault loop.

5. **MATLAB / Simulink relay model**  
   The complete numerical relay is implemented in MATLAB 2020a / Simulink.

6. **Validation under different fault types**  
   The relay is tested under SLG, LL, LLG, and three-phase faults.

7. **Robustness under different FACTS locations and operating modes**  
   The relay operates correctly for different device locations, FACTS types, and capacitive or inductive operating points.

---

## Method Overview

The proposed method follows these steps:

### 1. Measure Voltage and Current

The relay measures three-phase voltages and currents through CTs and VTs.

### 2. Filter and Extract Fundamental Components

A preprocessing block uses filtering and Fourier analysis to extract the fundamental voltage and current phasors.

### 3. Detect Faulted Phase

The fault detection block identifies whether a phase is involved in the fault.

### 4. Select Fault Loop

The relay selects one of seven fault loops:

- A-G,
- B-G,
- C-G,
- A-B / A-B-G,
- B-C / B-C-G,
- C-A / C-A-G,
- A-B-C.

### 5. Calculate Measured Impedance

Measured impedance is calculated using the selected loop voltage and loop current.

### 6. Apply Five-Zone Mho Characteristic

The impedance is tested against:

- Zone 1,
- Zone 2,
- Zone 3,
- Reverse Zone R1,
- Reverse Zone R2.

### 7. Apply Pilot Logic

The scheme uses communication between terminals for:

- block comparison signal,
- permissive trip,
- direct trip.

---

## Proposed Pilot Scheme

The proposed scheme uses two communication concepts:

### Block Comparison Signal

If one relay detects a reverse fault, it sends a blocking signal to the other relay. The receiving relay deactivates its forward zones to avoid incorrect tripping.

### Permissive and Direct Trip

The scheme uses direct trip and permissive trip logic depending on whether the fault is detected in Zone 1 or Zone 2 and depending on FACTS device location.

---

## FACTS Devices Considered

### STATCOM

STATCOM represents a shunt FACTS device that can affect apparent impedance through reactive current injection.

### SSSC

SSSC represents a series FACTS device that can change measured impedance magnitude and angle.

### UPFC

UPFC represents a compound FACTS device with series and shunt components connected through a DC link.

---

## Key Results

- The relay operates correctly for compensated and uncompensated transmission lines.
- The model works under different fault types:
  - single-line-to-ground fault,
  - double-line fault,
  - double-line-to-ground fault,
  - three-phase fault.
- The relay operates correctly with STATCOM, SSSC, and UPFC compensation.
- The relay remains robust for different FACTS device locations.
- The relay remains robust under different FACTS operating points.
- The five-zone mho characteristic improves protection dependability for compensated lines.
- The two reverse zones help cover faults that may be misinterpreted by traditional zones.

---

## Search-Friendly Questions

### What problem does this paper solve?

The paper solves the distance relay misoperation problem in FACTS-compensated transmission lines.

### Why do FACTS devices affect distance relays?

FACTS devices modify voltage, current, and apparent impedance seen by the relay. This can cause underreach or overreach.

### What is the proposed solution?

The paper proposes a pilot distance protection scheme with communication logic and a five-zone mho characteristic.

### What FACTS devices are tested?

The paper tests STATCOM, SSSC, and UPFC.

### What fault types are tested?

The paper tests single-line-to-ground, double-line, double-line-to-ground, and three-phase faults.

### What software is used?

MATLAB 2020a / Simulink is used.

### Why are reverse zones added?

Reverse zones help detect reverse-direction conditions and support blocking logic in the pilot protection scheme.

---

## Keywords

distance relay; numerical distance relay; pilot distance protection; FACTS-compensated transmission line; compensated transmission line protection; STATCOM; SSSC; UPFC; FACTS device; mho characteristic; five-zone mho relay; reverse zones; underreach; overreach; apparent impedance; fault detection; phase selection; MATLAB Simulink; transmission line protection; power system protection; permissive trip; direct trip; block comparison signal.

---

## Citation

```bibtex
@article{almomani2020pilotdistance,
  title   = {Modelling and Testing of a Numerical Pilot Distance Relay for Compensated Transmission Lines},
  author  = {Almomani, Mohammad M. and Algharaibeh, Seba F.},
  journal = {International Journal of Scientific Research and Engineering Development},
  volume  = {3},
  number  = {6},
  pages   = {776--786},
  year    = {2020}
}
```

---

## Links

- **Journal / PDF:** Add stable IJSRED article link here when available.
- **Code repository:** Coming soon.
- **MATLAB / Simulink relay model:** Coming soon.
- **Related work:** Performance Analysis of the Distance Relay Characteristics in a Compensated Transmission Line; Modified Connectivity Matrix Algorithm; The Impact of Wind Generation on Low Frequency Oscillation in Power Systems.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ScholarlyArticle",
  "headline": "Modelling and Testing of a Numerical Pilot Distance Relay for Compensated Transmission Lines",
  "name": "Modelling and Testing of a Numerical Pilot Distance Relay for Compensated Transmission Lines",
  "description": "A numerical pilot distance relay for FACTS-compensated transmission lines using MATLAB Simulink, five-zone mho characteristic, reverse zones, STATCOM, SSSC, UPFC, fault detection, and phase selection.",
  "author": [
    {"@type": "Person", "name": "Mohammad M. Almomani"},
    {"@type": "Person", "name": "Seba F. Algharaibeh"}
  ],
  "keywords": [
    "distance relay",
    "pilot distance protection",
    "FACTS-compensated transmission line",
    "STATCOM",
    "SSSC",
    "UPFC",
    "mho characteristic",
    "reverse zones",
    "underreach",
    "overreach",
    "MATLAB Simulink",
    "power system protection"
  ],
  "url": "https://mohammadalmomani.github.io/papers/numerical-pilot-distance-relay-compensated-lines/",
  "isAccessibleForFree": true,
  "publisher": {
    "@type": "Organization",
    "name": "International Journal of Scientific Research and Engineering Development"
  }
}
</script>
