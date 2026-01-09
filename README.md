# Repo 3 — Structural Constraints & Configuration Space

## Purpose

Repo 3 identifies **structural degrees of freedom at fixed system size** and formalizes **configuration equivalence classes** for residential solar installations.

This repository answers one question only:

> **Given the same system size, which configuration dimensions are structurally fixed, and which vary freely?**

Repo 3 **does not**:
- estimate scaling laws
- define regimes
- measure deviation
- assign likelihood or risk
- compare across system sizes

Those operations are explicitly deferred to downstream repositories.

---

## Conceptual Scope

### Fixed Size as Conditioning

System size (`system_size_kw`) is treated as **given**, not modeled.

All analysis conditions on size by restricting attention to **narrow size windows**, interpreted as *measurement-tolerance equivalence*, not analytical stratification.

> Size bins represent systems that are indistinguishable at the resolution of measurement — not categories of size.

No normalization, regression, or cross-size comparison is permitted in this repository.

---

### Structural Degrees of Freedom

A **structural degree of freedom** is a configuration dimension that can vary independently **once size is fixed**.

Conversely, a dimension is **structurally constrained** if it is effectively determined by system size and does not meaningfully vary within a fixed-size window.

The classification of dimensions as *constrained* or *free* is:
- empirical, not theoretical
- distributional, not correlational
- based on within-bin variation only

---

### Configuration Equivalence

A **configuration** is the structural realization of system size through components and layout.

Two systems are **configuration-equivalent** if and only if:

> They are equal on all configuration dimensions that are empirically constrained at fixed size.

Differences along dimensions shown to vary freely are explicitly ignored.

Equivalence is **deterministic**, not probabilistic:
- no similarity metrics
- no clustering
- no tolerance thresholds

Each system belongs to **exactly one configuration class**.

---

## Inputs

Repo 3 consumes:

- **Repo 2 outputs** (sealed, read-only):
  - `size_baselines.parquet`
  - `size_dispersion.parquet`
  - system-level size representation

- **Select raw configuration columns**, reintroduced explicitly and minimally, subject to eligibility rules:
  - physical realization variables only
  - discrete or categorical
  - non-administrative
  - non-derived
  - non-scaling

The analytical grain remains **one row per system** at all times.

---

## Outputs

### 1. `structural_constraints.parquet`

A system-size–conditioned summary of configuration dimensions, including:

- size bin identifier
- configuration variable name
- number of distinct values
- dominance ratio
- entropy / diversity metrics
- empirical classification:
  - `constrained`
  - `free`
  - `ambiguous`

This table documents **which dimensions are structurally fixed or free once size is held constant**.

---

### 2. `configuration_classes.parquet`

A system-level mapping that assigns each installation to a **configuration equivalence class**, defined by equality on constrained dimensions.

Includes:
- system identifier
- size bin
- constrained configuration keys
- deterministic `configuration_class_id`

Each configuration class corresponds to a **distinct structural realization of fixed size**.

---

## Repository Structure

## Repository Structure

- `README.md` — Repository scope, constraints, and outputs
- `notebooks/`
  - `01_structural_degrees_of_freedom.ipynb` — Identify constrained vs free configuration dimensions and assign configuration classes
- `outputs/`
  - `structural_constraints.parquet` — Empirical classification of configuration dimensions at fixed size
  - `configuration_classes.parquet` — Deterministic configuration equivalence class assignments
- `requirements.txt` — Python dependencies


---

## Epistemic Constraints

Repo 3 explicitly forbids:

- any modeling of size as a variable
- regime detection or breakpoint logic
- deviation or residual analysis
- probabilistic reasoning
- normative interpretation of configurations
- importance ranking of components

The role of this repository is **structural characterization only**.

---

## Downstream Dependency

Repo 3 outputs feed directly into:

- **Repo 4** — Scaling characterization & regime detection  
  (first point where cross-size structure is allowed)

Repo 3 must be **complete and sealed** before Repo 4 begins.

---

## Repository Status

**Active (in progress)**  
Scope is locked. Outputs are not yet finalized.

