# OOD Reversals in Two-Layer ReLU Networks — analytic theory

Working repository for an **analytic** theory of out-of-distribution (OOD) probe reversals in a two-layer ReLU network trained on the Structured Identity Mapping (SIM) task. The model is two Gaussian concept clusters $\mathcal N(e_1,q^2I)$ and $\mathcal N(\rho e_2,q^2I)$, identity targets, an untied bias-free two-layer ReLU network, and aligned-balanced isotropic initialization of total mass $S_0$.

The empirical phenomenon: after both concepts are learned, an off-cone probe's error first decreases and then rises. Cluster 1 (strong concept) helps the probe through the strong family's output. Cluster 2 (weak concept) harms it by rotating the strong family's inputs, driven by residual that the weak family produces. The goal is one unified theory that proves this mechanism from initialization.

**Current status.** The mechanism is proved within the leading small-noise population system. Every step of the initialized, finite-noise connection has a proved conditional implication, but the inputs to those implications are not yet derived from initialization. See `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` for the full status and the remaining steps.

> This repository contains unpublished research. Keep it private unless you intend to share it.

---

## Ground rule: analytic proof only

Every theorem, constant and parameter region must be established by **displayed analytic proof**: Gaussian identities, invariant regions, differential inequalities, first-exit bootstraps, comparison arguments, and hand-proved rational bounds.

**Not allowed as proof premises:** interval arithmetic, validated numerics, grid sign checks, saved trajectories, fitted exponents, or anything whose truth is checked by running code.

Numerics may motivate or falsify a conjecture. Symbolic algebra and exact fractions are checking aids only. Decimals in the documents are tagged **[rational]** (backed by a hand-proved bound) or **[eval]** (orientation only; no theorem may depend on it).

---

## Folder guide

Each proof increment is a `.tex` file with a same-stem `_review.md` (where one exists). The review note gives scope, assumptions, audit points and open residue; it does not supersede the `.tex`. The short keys in brackets (e.g. **[LOC]**) are how the roadmap and increments cite each other.

### `00_roadmap/` — start here

| File | Contents |
|---|---|
| `UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | Current roadmap: what is proved by scope, remaining steps S0–S9 in dependency order, the regime gap between the theorem regime and the canonical run, the analytic-proof rules, numerical-claim audit, withdrawn claims, file map. |
| `THEORY_HANDOFF_ANALYTICAL_A_B_v2.md` **[H2]** | Handoff v2: locked setting and notation, Theorem A/B contracts, finite-noise matching contract (AN7), the AN0–AN9 roadmap, file contracts, withdrawn-claims ledger, workflow rules. |
| `THEORY_HANDOFF_ANALYTICAL_A_B_v2_CHANGELOG.md` | What changed from the first handoff to v2. |

### `01_foundations/` — exact model and checkpoint

| File | Contents |
|---|---|
| `RELU_POPULATION_FOUNDATIONS_v2.tex` **[F]** | Exact finite-parameter foundations: untied characteristic flow, balance, Gaussian calculus, exact cluster-sourced rates, regularity, learning observables, P10 linear control. Frozen. |
| `THEOREM_A_ANALYTICAL_PROGRESS.tex` **[P]** | Checkpoint 1.0 with stable `pa:*` labels: early escape, target-only comparison, factorizations, leading scaled population system, resident curve, spectra, positive-lag theorem, selected-orbit reversal. Predates all AN02/AN03/AN06/LP/LPR increments. |

### `02_entry_AN02/` — initialized entry: early dynamics, ancestry, target-only profiles

| File | Contents |
|---|---|
| `AN02_weak_side_arrival_v1` **[ARR]** | Original-flow incoming weak-side reservoir from analytically predetermined labels; a small mass, not the captured weak seed. |
| `AN02_strong_ancestry_and_tail_transport_v1` **[TAIL]** | Positive-coordinate ancestry lower bound; zero-noise outer transport; one-sided upper-tail profile theorem. |
| `AN02_Q2_profiles_and_localized_tracking_v1` **[Q2]** | Q2 target-only first integral and density; crossing and transit clocks; conditional left-facing original-flow tracking with an explicit full-output defect. |
| `AN02_strong_entry_profile_and_tail_budget_v1` **[PROFILE]** | Exact attracting strong center $a_q$; uniform Q1 arrival; strong entry profile with tail index $3/s$ and finite cutoff; Q4 companion; outside-population cost $O(\mu/q)$; tail-inclusive κ=10 power test. |
| `AN02_Q2_boundary_layers_and_cohort_energy_v1` **[Q2E]** | Uniform Q2 crossing through both endpoints; secondary recruited Q2 tail (index $p_2<1$); whole-Q2 transverse and amplitude energies at κ=10. |

### `03_passage_AN03/` — nonlinear passage, response clock, weak selection

| File | Contents |
|---|---|
| `AN03_two_sided_passage_and_Q2_retention_v2` **[RET2]** | Two-sided and mixed-order all-label passage with Riccati closure; Q2 ancestry vs late arrivals; conditional retention. Use v2, not v1. |
| `AN03_local_rate_mean_tracking_v1` **[LOC]** | Local-rate passage with collective mean tracking in the full leading field; explicit guards; conditional joint-power test. |
| `AN03_exact_amplitude_clock_and_c_passage_v1` **[CLOCK]** | Exact weak-amplitude identity and response clock; amplitude/response ledger; cross-output energy bound; c-form passage theorem. |
| `AN03_weak_transit_forcing_and_orbit_selection_v1` **[WEAK]** | Square-root weak forcing; weak concentration; coupled strong-mean/weak-orbit selection at fixed weak mass (leading system). |
| `AN03_mass_charged_tail_and_selection_defects_v1` **[TAILREP]** | Capped-gain clock integration; tail-moment lemma; uniform κ=10 margin; selection theorem with core moment and outside defects. |
| `AN03_bulk_clock_and_secondary_Q2_energy_v1` **[BULK]** | Cohort-change identity; bulk clock subcohort; conditional original-flow bulk-clock bootstrap; secondary-tail energy from the capped gain; regenerated transverse energy and forcing with a separate clock. |
| `AN03_residual_closure_and_eta0_transport_v1` **[RCET]** | Small-constant (η=0) bulk transport; endpoint-regularized target-only threshold dichotomy at $c_0\asymp q^\gamma$; output bounds and Volterra residual closure conditional on an independent clock bound; the obstruction that remains (S0). |
| `SIGNED_GROWTH_WEAK_RETENTION_v1` **[SGWR]** | Signed Jensen retention; weak-coordinate amplitude equation; interior-Q2 defect bound; frozen resident contraction. |

### `04_witnesses_persistence/` — learned limiting witnesses, persistence, linear contrast

| File | Contents |
|---|---|
| `AN06_learned_orbit_witnesses_v2` **[WIT]** | Learned descent witnesses at quarter-mass covering the canonical scaled offset $5\pi/9$; common windows; gate-aware population tolerance; own-half-mass clock; static learning bounds. |
| `LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1` **[LP]** | Linear architecture contrast (extends P10); eventual zero benefit on the selected orbit; compact-parameter clearing; conditional growing-window transfer. User-checked. |
| `LIMIT_LEARNED_PERSISTENCE_RETENTION_v1` **[LPR]** | Combined learned reversal and clearing on WIT's rectangle; all-coordinate $\sqrt{\log}$ growth; conditional exponent algebra. User-checked. |

### `05_supporting_notes/` — derivations and background, not current proof sources

| File | Contents |
|---|---|
| `SCALED_POPULATION_SPLITTING_THEORY.md` | Full scaled population system, mean vs shape spectra, positive-lag theorem, probe/covariance identities, small-split response. |
| `TWO_NEURON_SMALL_NOISE_LIMIT.md` | Six-dimensional leading atom system and the selected-orbit reversal argument (use later corrections for the ρ range and real weak root). |
| `LEAK_COMPENSATION_FACTORIZATION_AUDIT.md` | Exact source-by-motion factorization with complete remainders, plus a numerical audit (diagnostic only). |
| `SIM.md` | Reference summary of the original Swing-by paper (Yang et al., ICLR 2025). Do not import its tied linear dynamics into the untied ReLU model. |

### `06_paper_drafts/` — historical drafts

| File | Contents |
|---|---|
| `main-15.tex` | Historical research notebook. Reuse only checked statements with their exact assumptions. |
| `main-appendix-frozen-theory-selfcontained.tex` | Historical appendix with conditional and certificate-era arguments. Do not infer initialized entry from its conditional results. |

### `99_archive/` — superseded files, kept for audit only

| File | Superseded by |
|---|---|
| `AN03_two_sided_passage_and_Q2_retention_v1` (+ review) | RET2 (v2). The v1 joint-regime claim is withdrawn. |
| `AN06_learned_orbit_witnesses_v1` (+ review) | WIT (v2). |
| `THEORY_HANDOFF_ANALYTICAL_A_B.md` | H2. |
| `theorem_A_initialized_escape.pdf` | Sections 1–3 are retained in P; the numerical-reference continuation from Section 4 on is obsolete. |

---

## Reading order

- **To continue the initialized proof:** roadmap → H2 → LOC → CLOCK → BULK → RCET → PROFILE → Q2E → WEAK → TAILREP, consulting F and P only for specific dependencies.
- **For the completed limiting and linear results:** F (P10) → LP → WIT → LPR.

## Status labels used in every document

1. Exact original-flow result.
2. Exact comparison result (target-only flow, not the trained population).
3. Result within the defined leading system.
4. Conditional estimate (proved implication; inputs open).
5. Derived expansion (regularity and remainder obligations stated).
6. Empirical evidence or conjecture (never a proof premise).

## Workflow

- Each new result is a **new versioned pair**: `ANxx_topic_vN.tex` + `ANxx_topic_vN_review.md`, with a unique LaTeX label prefix. Put it in the matching group folder.
- **Never overwrite** an earlier increment. When a version is replaced, move the old pair to `99_archive/` and record what superseded it.
- **No automatic merges** into the checkpoint. Consolidation happens only after review and explicit approval, with a changelog and label map.
- Simulation scripts and data are not part of this repository; they are diagnostic provenance, not proof premises.