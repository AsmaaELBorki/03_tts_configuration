# Repo 3 — Within-Expected-Size Structural Configuration

## What Question This Repository Answers

**When residential solar systems are similarly positioned relative to their expected system size, in what meaningful and repeatable ways can their designs still differ?**

This repository isolates **design structure that is not explained by proximity to the expected-size baseline**.

---

## Why This Question Matters (Applied Context)

In real-world residential solar markets, system design decisions are shaped by
many factors beyond raw capacity.

However, absolute system size is a poor comparison frame:
- markets evolve over time
- typical system sizes shift
- raw kW comparisons conflate growth with deviation

Instead, systems must be evaluated **relative to what the market expects them to be**, given when and where they were installed.

Failing to account for this leads downstream analysis to:
- misattribute normal configuration patterns to scaling behavior
- interpret market-standard designs as anomalous
- confound deviation with temporal or contextual drift

This repository prevents that error by explicitly mapping **what can vary once expected system size is held fixed**.

---

## Analytical Posture

This repository is **structural and descriptive**.

It identifies:
- which configuration attributes remain stable
- which exhibit limited degrees of freedom
- which do *not* explain deviation once expectation is accounted for

It does **not**:
- analyze scaling behavior
- define regimes
- evaluate oversizing or undersizing
- assign risk, abnormality, or preference

---

## Reference Frame: Expected System Size

All analysis in this repository is conducted **relative to an expected-size baseline**.

Expected system size is:
- empirically derived upstream (Repo 2)
- defined as typical residential system capacity given installation year
- treated as a reference surface rather than an outcome

Systems are grouped into **expected-size deviation bands** (e.g., very close to expectation, moderately deviant), and configuration variables are analyzed **within those bands**.

Absolute observed size is allowed to vary within bands.  
What is fixed is **position relative to expectation**, not raw capacity.

---

## Inputs

This repository consumes upstream artifacts without modification:

- Canonical expected-size baselines
- System-level installation records
- Measurement constraints defined upstream

All system comparisons are conditional on **expected-size proximity**, not on absolute kW equality.

---

## What This Repository Produces

Outputs from this repository define **within-expected-size structure only**, including:

- configuration attributes that are invariant near expectation
- limited degrees of freedom that remain once expectation is satisfied
- structural constraints inherited by downstream scaling analysis

These outputs describe **what can vary without violating expected sizing behavior**, not how system size itself behaves.

---

## What This Repository Explicitly Does Not Do

This repository does not:

- compare systems by absolute capacity alone
- analyze how system size scales
- identify deviation regimes
- assess oversizing or undersizing
- assign abnormality or risk

Any analysis that relies on **meaningful variation in expected system size** belongs downstream.

---

## Relationship to Downstream Analysis

Downstream repositories use the structural constraints established here to:

- distinguish true scaling-driven deviation from configuration noise
- ensure regime formation is not confounded by design heterogeneity
- interpret deviation surfaces relative to a validated expected-size reference

Downstream analysis is not permitted to redefine or reinterpret expected-size conditioning established here.

---

## Governing Constraint

> **Expected system size is treated as fixed in this repository.  
> Systems are compared only within bands defined by deviation from that expectation.  
> Any analysis that depends on variation in expected system size is out of scope.**

---

## Status

This repository completes the **within-expected-size structural layer** of the
*Tracking the Sun* analytical program.

Its outputs are treated as **fixed structural references** by all subsequent repositories.
