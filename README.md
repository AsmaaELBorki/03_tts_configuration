# 02 — Tracking the Sun: Regime and Scaling Structure

## Purpose

This repository characterizes **how residential PV system size behavior deviates from canonical baselines under different configurations**.

It consumes the baseline and expected size artifacts produced in **Repo 1** and examines how **scaling behavior and residual structure organize themselves** across time and geography. The objective is to identify **structural regimes** and **stable deviation patterns**, not to explain or predict outcomes.

---

## Position in the Program

This repository sits downstream of:

- **Repo 0 — Program-Level Substrate**
  - schemas, contracts, and dataset definitions  
- **Repo 1 — Baselines and Expected Size Function**
  - admissible baseline populations  
  - discrete expected size function  
  - residualized baseline observations  

and upstream of any work that would attempt likelihood estimation, risk scoring, or abnormality detection.

No upstream artifacts are modified or reinterpreted here.

---

## Scope

This repository:

- conditions baseline residential system size behavior on configuration variables  
- examines how residuals vary across time and geography  
- identifies structural regimes where scaling behavior differs  
- defines regime boundaries suitable for downstream use  

This repository explicitly does **not**:

- explain causal drivers of system size variation  
- predict future installations or trends  
- optimize system size or policy outcomes  
- redefine baseline validity or expected size  

All analysis is **descriptive and structural**.

---

## Inputs

Consumed canonical artifacts from **Repo 1**:

- `baseline_residential_system_sizes.csv`  
- `expected_system_size_by_year.csv`  
- `baseline_with_expected_size.csv`  

Additional configuration features (e.g. geography, policy era) may be attached within this repository but do not alter upstream definitions.

---

## Outputs

Canonical outputs produced by this repository:

- **`deviation_surfaces.csv`**  
  Structured deviation metrics conditioned on configuration variables, suitable for downstream analysis.

- **`regime_assignments.csv`**  
  Explicit mapping of observations to identified structural regimes.

- **`regime_boundaries.md`**  
  Human-readable definitions of regime criteria, boundaries, and scope limits.

All other materials are diagnostic and non-canonical.

---

## Repository Structure

