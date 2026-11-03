# OOD Reversals in Two-Layer ReLU Networks — analytic theory

Working repository for an **analytic** theory of out-of-distribution (OOD) probe reversals in a two-layer ReLU network trained on the Structured Identity Mapping (SIM) task. The model is two Gaussian concept clusters $\mathcal N(e_1,q^2I)$ and $\mathcal N(\rho e_2,q^2I)$, identity targets, an untied bias-free two-layer ReLU network, and aligned-balanced isotropic initialization of total mass $S_0$.

The empirical phenomenon: after both concepts are learned, an off-cone probe's error first decreases and then rises. Cluster 1 (strong concept) helps the probe through the strong family's output. Cluster 2 (weak concept) harms it by rotating the strong family's inputs, driven by residual that the weak family produces. The goal is one unified theory that proves this mechanism from initialization.

**Current status.** The mechanism is proved within the leading small-noise population system. In the trained network itself, everything from initialization through strong half mass is now proved unconditionally at $S_0=q^{10}$ (S1). That covers the strong profile and every entry contract the weak passage needs. The residual-norm closure for the weak passage (S0) is proved conditionally. S2 and S3 are closed in stopped-guard form (S2CP, CFA), with a conditional CLOCK passage. The Q3 strip budgets are complete (Q3SB, PISB, LSB). The joint assembly (WPT) and the response barrier (RB) complete the **initialized deep-regime weak-passage theorem**. The selection-stage audit (SI, S4a) stopped at the original weak input return, which WBR (S4b) then proved, the matching package (MP, S4c) is closed, and the strong-reference reduction (SRR, S4d) and the weak-chart reduction with selection (WCS, S4e) are closed: **the initialized flow selects the coherent orbit at a fixed small weak mass.** The compact-window interface audit (CWI, S5a) and the probe-sector energy theorem (PSE, S5b) are done: **the full initialized probe error and source rates, background included, match the selected orbit at every fixed small weak-mass level.** The finite-window continuation (FWC, S5c) then proves **A-error-transfer on every fixed centered window**: the initialized probe error matches the selected limiting orbit at the $q^2$ scale. The rate transfer and assembly (RTA, S5d) then prove **initialized Theorem A and initialized persistence in the deep regime** ($S_0=q^{10}$, small q, parameters in the learned-witness rectangle around $\rho=2/3$). The mechanism decomposition (BC and CPD, S6) is now proved in the trained network on the learned windows, except for one sign. **Cluster-1 help equals exposure times a positive exact lag.** Cluster-2 harm has four leading-order parts: input and output rotation of the strong family, each produced partly by the target and partly by the weak family. The weak family's input part is proved harmful up to just past weak half mass (PHS); its sign later in the window is a named open problem (OP-W) on which nothing else depends. This completes the deep-regime paper core on its stated scope. The canonical-regime audit (CRA, S8a) maps where the deep proof stops applying. It first breaks where the strong family is no longer aligned to within the probe's scale when it saturates, and that points to a critical initialization scale as the natural setting for the canonical bridge. At that scale (CFS, S8b) the strong family's entry profile is explicit in the comparison flows. In the limiting system its spread survives saturation instead of collapsing to a single point. The comparison strong family is a coherent core at the resident angle plus a spread tail (RPS, S7a). Whether the tail first moves out through the probe gate or back in depends on the initialization scale. Still open: transfer to the trained network, and the bridge dynamics through weak learning (S7b). See `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` for the full status and the remaining steps.

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
| `AN02_overlap_window_profile_transfer_v1` **[OWPT]** | Exact original-flow transfer of PROFILE's strong profile at the overlap time $t_m=(2/\omega)\log(1/q)+C_m$: shapes within $e^{O(q^{\zeta})}$ and weights within $e^{O(q^{\sigma})}$ relative to a same-field reference; normalized tail sandwich (S1 step 1). |
| `AN02_strong_M_clock_passage_v1` **[SMCP]** | Obstruction increment for S1 step 2a: at fixed overlap offset, outer strong labels carry a nonvanishing nonlinear factor, so the linear M-clock multiplier cannot transfer the profile uniformly; exact leading-field test to half mass; corrected handoff normalization $A_q$. |
| `AN02_moving_overlap_M_clock_passage_v1` **[MOMC]** | Exact original-flow strong passage from a moving overlap ($C_m=\tfrac12\log(1/q)$) to strong half mass: logistic clock with shift $-\log A_q$, guard-independent chart $R=79/51$, uniform pairwise shape transport by the linear M-clock multiplier, radial weights, tail sandwich, left-ancestry mass budget; finite-noise $C^1$ field reduction (S1 step 2a). |
| `AN02_Q2_entry_through_strong_passage_v1` **[Q2EP]** | Exact original-flow Q2 entry energy at strong half mass ($J_G(t_0)\le C_Jq^3$, $E_{G_+}(t_0)=o(1)$ for every Q2 subcohort); coherent-field identification of the strong cross drive $-Ma_\rho/2$ and the resulting obstruction to an $e^{o(1)}$ universal angular factor at a fixed threshold. |
| `AN02_Q2_entry_contracts_v1` **[Q2EC]** | Exact original-flow primary Q2 entry at strong half mass with fixed constants: signs, antisymmetric ratio, Cartesian ratios ($\le C_0$; clock $\le C_{\rm clk}q^{1/8}$), clock seed with $A_q^{-\lambda}$, chart cap for the recruited group; weak-axis band matching of late crossers. |
| `AN02_secondary_entry_profile_v1` **[SEP]** | Exact original-flow entry profile at strong half mass for the recruited Q2 group $c_0<Kq^\gamma$ (LCRC's Σ, with $\mathcal D=\emptyset$): positive displacement about the actual reference, radial weights, $p_2$ tail with explicit $A_q$ powers. Completes S1's entry contracts. |
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
| `AN03_ledger_cap_residual_closure_v1` **[LCRC]** | S0 closed conditionally (Route 3): the response ledger caps the sign-good weak amplitude at every time inside a joint first-exit bootstrap, removing RCET's clock premise and the terminal cap; derived chart-group mass; secondary energy without a future cap. |
| `AN03_c_form_field_reduction_v1` **[CFR]** | Partial S3: selected-moment lemma for any cohort (value and scaled receiver derivative), closed primary selected-defect budget, exact non-core moments $V_O,K_O$ with a negative-part bound, core radial identity; stops at the S2 dependency (secondary energy, integrated outside mass). |
| `AN03_distance_envelope_and_capped_gain_v1` **[DECG]** | Partial S2: distance envelope on the c-form chart (coordinate change $u=\int\Phi(\rho v)^{-1}dv$), global signed radial bound with integrated error $4B+o(1)$, capped gain conditional on the envelope; stops at the off-chart envelope and the Q3 budget. |
| `AN03_global_envelope_signed_gate_v1` **[GESG]** | Partial S2: chart-free global distance envelope (sine bound, Duhamel, one-exit splice) with the gate-excess integral explicit; signed gate identity; constant audit; lower-side no-gain; Q3 interior frozen from initialization. Stops at the integrated gate budget, which the roadmap's v1.11 review resolves via LCRC's backward clock. |
| `AN03_S2_closure_package_v1` **[S2CP]** | S2 closed in stopped-guard form: gate budget, fixed distance constant, all-endpoint capped gain, secondary energy with the joint guard strictly improved, and strong-complement mass. Also pays CFR's secondary obstruction and $B_s=\log2+o(1)$ under retained core geometry, and audits the retained inputs (c-form, strips, CLOCK budget). |
| `AN03_c_form_assembly_v1` **[CFA]** | S3 closed in stopped-guard form: core-only c-form with capped donor mass ($T\equiv0$), two new selected-moment estimates, full value-and-derivative remainder, CLOCK forcing budget with constants independent of $c_b$ and $C_0$, and a conditional CLOCK passage. The Q3 strip budget is the only external input. |
| `AN03_Q3_strip_budgets_v1` **[Q3SB]** | Partial strip work. Proves the pre-entry cross residual and gate budget (new S1 conclusions), the regularized sine envelope from the π axis, the total-clock bound, and a frozen 3π/2 substrip. It also refutes three proposed premises: the unregularized gain, lower-side retention, and whole-strip chart entry. |
| `AN03_pi_strip_budget_v1` **[PISB]** | Pays the π strip: target-only boundary domination, a regularized boundary mass, a coarse strong-rate bridge to half mass, and capped post-entry gain. Also freezes and pays the outer and middle zones of both strips. Only the 3π/2 inner zone remains. |
| `AN03_late_strip_budget_v1` **[LSB]** | Pays the 3π/2 inner zone, completing the strip budget. Uses the exact target-only time shift from the right half's endpoint, a new single-label contraction in the strong chart, a split into early and late delay classes, and a restart of the S2 gain from actual arrival. |
| `AN03_weak_passage_theorem_v1` **[WPT]** | Joint first-exit assembly. Every energy, residual, field, core and outside guard improves, giving a two-boundary theorem: all estimates hold until the response first hits 0 or $c_b$, within $20\log(1/q)$. Stops at the lower response barrier $c\ge0$, which the sources assume but do not prove. Also corrects the hitting-time accuracy. |
| `AN03_response_barrier_v1` **[RB]** | **Completes the initialized deep-regime weak-passage theorem.** Proves the response stays positive (core response of order $q^2$, all-label input/output alignment, signed outside charge). Also proves $H(t_b)\asymp c_b$, the exact passage time, and the handoff list for S4. |
| `AN03_selection_interface_v1` **[SI]** | S4a, partial. Lists every hypothesis of the selection theorem and matches the ones the passage already supplies (core moments, weak-coordinate size, mass and phase identities). Stops at the original weak input return, whose boundary margin needs a signed weak-receiver field computation. |
| `AN03_weak_boundary_return_v1` **[WBR]** | S4b. Proves the original weak input return: the whole clock cohort keeps nonnegative weak input up to a fixed clock level, with a strict margin at the boundary. Uses an exact boundary field, an energy bound on the weak feedback, a pointwise strong-mass rate and $O(q)$ clock alignment. |
| `AN03_matching_package_v1` **[MP]** | S4c. The clock cohort carries all but $O(q^{1/4})$ of the weak mass and response, and its amplitude follows a logistic curve with vanishing phase error. Also proves the regenerated transverse bound $J\le C(q^3+q^2H)$, the initial smallness the selection theorem needs, and late core-mass defect budgets. |
| `AN03_strong_reference_reduction_v1` **[SRR]** | S4d. Puts the actual strong reference into the selection theorem's strong error form on the selection interval, with a vanishing pointwise defect, and proves that its initial error vanishes. Also fixes the weak-distance convention and the local constants the weak-chart reduction (S4e) will use. |
| `AN03_weak_chart_selection_v1` **[WCS]** | S4e. Reduces the weak cohort's original velocities on its growing chart to the selection theorem's weak error form, using only value bounds, and then applies the selection theorem at a fixed small weak mass: the strong reference and the weak cohort are both within $O(q^{1/20})$ of the selected coherent orbit. Also gives the S5 handoff state. |
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

### `07_compact_windows_AN07/` — compact-window matching (AN7)

| File | Contents |
|---|---|
| `AN07_compact_window_interface_v1` **[CWI]** | S5a, audit. Inventories every hypothesis of the window consumers (WIT, LP, LPR, H2's transfer contracts) against the state the selection stage delivers. Fixes the time centering, classifies which labels are active at the probe, and reduces the outside part of the probe comparison to one exact precision condition, listing which populations it is already proved for. Also extends WIT's leading-system transfer to weak populations without bounded support. |
| `AN07_probe_sector_energy_v1` **[PSE]** | S5b. Proves that the energy of inputs pointing into the lower half-plane (the only ones that can reach the probe) stays $o(q^2)$ for every non-core population, from initialization through the weak passage. This pays the background at the precision the probe needs, so the full initialized probe error and source rates match the selected orbit at every fixed small weak-mass level. Also states exactly what must be continued to later windows. |
| `AN07_finite_window_continuation_v1` **[FWC]** | S5c. Continues the original flow for any fixed time after the selection stage, without the weak-passage guards, by a combined transverse energy. Then shows the original state stays close to the selected limiting orbit in a mass-weighted first-moment distance, which gives error transfer of the probe at the $q^2$ scale on every fixed window. This is the premise LP's persistence argument needs. |
| `AN07_rate_transfer_and_assembly_v1` **[RTA]** | S5d. Transfers the source rates to the learned windows, proves learning of both concepts directly, and assembles **initialized Theorem A** (opposite cluster signs, ordered total rate, a rebound of order $q^2$ on an off-cone sector of width of order q) and **initialized persistence**, for $S_0=q^{10}$ on the learned-witness rectangle. Lists the full dependency chain and what S6 receives. |

### `08_mechanism_AN01/` — the original-flow mechanism (AN1, B-core)

| File | Contents |
|---|---|
| `AN01_original_flow_bcore_v1` **[BC]** | S6, first attempt; obstruction increment. Shows that the checkpoint's second-source "remainder" contains a strictly positive output-rotation term of the probe's own order on the learned windows, so the mechanism decomposition must keep that channel at leading order. Proves the two-channel (input and output rotation) form of the second source rate for the initialized flow. |
| `AN01_channel_producer_decomposition_v1` **[CPD]** | S6, revised; closed subset. Splits both source rates into input, output and radial rotation channels, and attributes each channel to the population whose residual produces it (target, strong core, selected weak family, the rest). Proves that the exact lag is positive and that cluster-1 help equals exposure times that lag. Shows that cluster-2 harm has four leading parts: target and weak contributions to input rotation and to output rotation. All signs are proved except that of the weak input part after weak half mass. |
| `AN01_post_half_mass_input_sign_v1` **[PHS]** | S6c; partial. Proves with explicit rational bounds that the weak family's input contribution stays harmful slightly past weak half mass, and records exactly why two approaches to the rest of the window fail. States the final deep-regime mechanism theorem and leaves the remaining sign as a named open problem. |

### `09_canonical_regime_AN04/` — the canonical regime (S8, S7; AN4)

| File | Contents |
|---|---|
| `AN04_canonical_regime_audit_v1` **[CRA]** | S8a; audit. Gives rational bounds for every timing and passage threshold, with the canonical initialization below all of them. Lists, for each deep-regime increment, which parts depend on the deep initialization and where the chain first breaks: the strong family is not yet aligned to the probe's scale when it saturates. Proves two comparison lemmas: the left-facing angle law for weak-side ancestry, and the weak-receiver contraction rate with all its terms. States what canonical entry and the bridge analysis still need. |
| `AN04_critical_family_strong_entry_v1` **[CFS]** | S8b. At the critical initialization scale, computes the strong family's angle profile when it saturates, with and without noise, and the fraction of it the probe sees. With noise, the profile starts at the resident angle rather than at zero. Shows, in the limiting system before the weak family grows, that an ordered spread persists through saturation and that the saturated resident is unstable to spreading. Audits what transfer to the trained network still needs. |
| `AN04_resident_phase_split_v1` **[RPS]** | S7a. Shows that, with noise, the other half of the strong family's ancestry collapses onto the resident angle. The comparison strong family is therefore a coherent core plus a spread tail, with an explicit probe-active fraction. In the limiting system before weak growth, proves that the population stays ordered, gives exact moment equations, and gives a self-consistent test under which part of the tail leaves the probe gate. It shows that for wider initial spreads the labels at the gate initially move back in instead. |

### `99_archive/` — superseded files, kept for audit only

| File | Superseded by |
|---|---|
| `AN03_two_sided_passage_and_Q2_retention_v1` (+ review) | RET2 (v2). The v1 joint-regime claim is withdrawn. |
| `AN06_learned_orbit_witnesses_v1` (+ review) | WIT (v2). |
| `THEORY_HANDOFF_ANALYTICAL_A_B.md` | H2. |
| `theorem_A_initialized_escape.pdf` | Sections 1–3 are retained in P; the numerical-reference continuation from Section 4 on is obsolete. |

---

## Reading order

- **To continue the initialized proof:** roadmap → H2 → LOC → CLOCK → BULK → RCET → LCRC → PROFILE → OWPT → MOMC → Q2E → WEAK → TAILREP, consulting F and P only for specific dependencies.
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