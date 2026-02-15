# Phase 1 — Corpus Profiling Methodological Decisions

## Objective

This document defines the methodological decisions governing execution of Phase 1 (Corpus Profiling).

It specifies:

- Dataset boundaries used during profiling
- Sampling limits for manual inspection
- Structural analysis constraints
- Explicit exclusions within this phase

This file formalises how Phase 1 is conducted.

It does not:

- Present empirical findings (see `corpus_profiling.ipynb`)
- Interpret structural implications (see `summary.md`)
- Define design choices for later phases

---

## 1. Dataset Scope and Size Constraints

### 1.1 Working Corpus Size

**Decision:**  
The working corpus is capped at approximately 200 ICU progress notes.

**Rationale:**  
- Sufficient for structural pattern discovery  
- Sufficient for deterministic rule development  
- Sufficient for small-scale supervised validation  
- Avoids unnecessary scale inflation  
- Aligns with project scope (design demonstration, not population inference)

This project prioritises architectural clarity over dataset magnitude.

---

### 1.2 Inclusion Criteria

**Decision:**  
- Only ICU progress notes meeting predefined selection criteria are included.
- Detailed filtering logic is documented in the profiling notebook.

**Constraint:**  
- Corpus composition is frozen for the duration of Phase 1.

---

## 2. Quantitative Profiling Strategy

### 2.1 Full-Corpus Analysis

**Decision:**  
Quantitative profiling is performed on the full working corpus (n ≈ 200).

**Constraint:**  
- No subsampling is used for distributional measurements.

**Rationale:**  
- Computationally inexpensive  
- Ensures complete structural visibility  
- Eliminates sampling bias in distributional measurements  

---

## 3. Manual Inspection Strategy

### 3.1 Manual Inspection Cap

**Decision:**  
Manual inspection is capped at approximately 40–50 notes.

**Rationale:**  
- Structural pattern saturation expected within this range  
- Manual review beyond this threshold yields diminishing returns  
- Prevents disproportionate allocation of effort to qualitative review  

---

### 3.2 Sampling Method

**Decision:**  
- Manual inspection uses stratified sampling to capture variability in length and structure.
- Exact stratification parameters are determined after corpus loading.

**Rationale:**  
- Ensures coverage of short, medium, and long notes  
- Captures variation in section density and formatting  
- Reduces risk of overfitting rule design to homogeneous samples  

Specific sampling parameters will be finalised after corpus access.

---








---

## 4. Analytical Boundaries Within Phase 1

Phase 1 is restricted to structural and surface-level linguistic analysis.

The following are explicitly excluded:

- Entity extraction
- Rule drafting
- Schema design
- Negation implementation
- Model experimentation
- Annotation

These activities belong to subsequent phases.

---

## 5. Phase 1 Execution Freeze

At the conclusion of Phase 1:

- Corpus size remains fixed.
- Quantitative profiling has been performed on all notes.
- Manual inspection has been completed within defined limits.
- No rule construction or modelling has been initiated.

Any deviation from these constraints requires formal revision of this document.