# Repo 3 — Within-Size Structural Configuration

## What Question This Repository Answers

When two residential solar systems are similar in size, **in what meaningful and repeatable ways can their designs still differ?**

This repository exists to isolate **design structure that is not explained by system size alone**.

---

## Why This Question Matters (Applied Context)

In real-world residential solar markets, system size does not uniquely determine system design.

Even when capacity (kW) is held constant, installations may differ in:
- inverter count and allocation
- component redundancy
- design conventions associated with installers or programs
- technical configuration choices permitted within reporting constraints

Failing to account for these within-size differences leads downstream analysis to incorrectly attribute configuration-driven effects to scaling or deviation.

This repository prevents that error by explicitly mapping the **degrees of freedom that exist at fixed size**.

---

## Analytical Posture

This repository is **structural and descriptive**.

It identifies **how systems of comparable size can differ**, not whether those differences are preferable, risky, or abnormal.

No scaling behavior is analyzed here.
No regimes are defined here.
No evaluative judgments are made.

---

## Inputs

This repository consumes upstream artifacts without modification:

- Canonical system size baselines
- Contextual fields permitted by measurement constraints
- Installation records filtered to comparable size bands

System size is treated as fixed or tightly bounded for all analysis in this repository.

---

## What This Repository Produces

Outputs from this repository define **within-size structure only**, including:

- Structural degrees of freedom at fixed size
- Configuration equivalence classes
- Admissible variation space for residential systems of comparable capacity

These outputs describe **what can vary without changing system size**, not how size itself behaves.

---

## What This Repository Explicitly Does Not Do

This repository does not:

- analyze scaling behavior
- identify deviation regimes
- assess oversizing or undersizing
- assign risk or abnormality
- interpret deviations from expected size

Any analysis that allows system size to vary meaningfully belongs downstream.

---

## Relationship to Downstream Analysis

Downstream repositories may use the configuration structures defined here to:

- distinguish configuration-driven variation from scaling-driven deviation
- ensure that regime formation and risk evaluation are not confounded by design degrees of freedom
- interpret deviation surfaces in a configuration-aware manner

Downstream analysis is not permitted to redefine or reinterpret configuration structure established here.

---

## Governing Constraint

> **System size is treated as fixed in this repository.  
Any analysis that depends on size variation is out of scope.**

---

## Status

This repository completes the **within-size structural layer** of the Tracking the Sun analytical program.

Its outputs are treated as fixed structural references by all subsequent repositories.

