# Analytical-only theory handoff — Theorems A/B, local passage, and limiting persistence

**Version 2.0 — updated after the AN03 v2 repairs, local-rate/collective-mode theorem, and Q2 profile/transit increment.**

**This is a replacement handoff, not a new proof or an approved mathematical merge.** The earlier handoff and `THEOREM_A_ANALYTICAL_PROGRESS.tex` remain unchanged. The latter is still checkpoint 1.0 and does not automatically contain the later review increments listed here.

## Executive status: read this before opening an older roadmap

The objective remains **one unified analytical theory** of the initialized ReLU population, not a computer-assisted proof of a saved trajectory.

There are three connected workstreams:

| Workstream | Current status | What remains |
|---|---|---|
| **Initialized Theorem A and its mechanism B** | Exact foundations, early original-flow ancestry/arrival bounds, limiting witnesses, and conditional nonlinear passage tools are available. **Initialized A and initialized B are not proved.** | A common-clock original-flow entry/retention theorem, useful joint input/output shape and weak/tail budgets, weak-angle/orbit selection, and finite-noise matching with all background labels retained. Non-small canonical-bridge closure is a further quantitative obligation. |
| **Linear architecture contrast** | **Proof complete for its stated hypotheses; the user reports checking it by hand.** It extends P10 to positive diagonal initial Gram matrices and records the per-cluster diagonal hypothesis and its counterexample. | Manuscript integration after approval. A quantitative random finite-width/finite-sample perturbation theorem is optional and not presently supplied. |
| **Limiting permanence and learned limiting reversal** | **Selected coherent limiting-orbit results are proved in the supplied increments; the user reports checking them by hand.** They include common learned windows, eventual zero scaled benefit, compact-parameter clearing, all-coordinate square-root-logarithmic growth, and the conditional diagonal-transfer implication. | Original initialized-network persistence requires the strengthened AN7 compact-window transfer below. A specified growth rate for the horizon and permanence for broad split populations remain optional/unproved extensions. |

### The most recent correction controls the roadmap

**The global-rate result has no established compatible initialized joint regime. The local-rate result has a useful conditional joint-power window, but its common-clock entry, retention, forcing, and smallness hypotheses remain to be proved.**

Do not restore either withdrawn inference:

- A positive initialization exponent by itself does not prove that seed, shape prefactor, chart validity, and Riccati smallness hold on one joint sequence.
- Local rates do not merely improve constants; retaining the local Gaussian gate factor may be essential once all powers of `q` and the transit delay are counted.

Conversely, no source proves that the global estimate closes nowhere. Target-only absorption does not imply absorption under the changed trained residual. The numbers `6.5`, `8.1`, and `11.7` are not an initialized admissible-region theorem.

The new, source-backed matching target is **conditional**: with the displayed candidate entry powers and uniform budgets, `S₀=q^(15/2)` gives a strictly positive local joint power on `ρ∈[13/20,7/10]`. Establishing those entry laws on that same sequence is still the central missing connection.

**Recommended next task:** prove a common-clock entry/retention sublemma that provides the inputs to the new local passage theorem. The exact amplitude can be useful, but its proposed response-clock closure has not yet been proved. Do not redo the completed linear or selected-orbit permanence arguments.

---

## 0. Non-negotiable instructions for the next chat

### 0.1 Analytical proof only

Prove theorems, lemmas, and quantitative estimates by displayed mathematics. Allowed methods include exact Gaussian integration, invariant regions, differential inequalities, analytic comparison flows, characteristic transport, first-exit bootstraps, saddle passage, and perturbation arguments with proved errors and parameter uniformity.

An analytically specified orbit, an unevaluated convergent integral, or constants defined by derivatives/suprema of an analytically controlled orbit are legitimate. A closed elementary solution is not required.

**Do not use** interval arithmetic, validated numerical continuation, saved-array interpolation, numerical eigenvalue envelopes, discretized sign checks, numerical trajectory tubes, or a certificate-first/mechanism-later strategy. No theorem may depend on `labels.npz`, a pilot run, or a program checking sampled points. Ordinary analytical stability is allowed; it is not permission to return to numerical certification.

Numerics may motivate or falsify a conjecture. They do not verify its hypotheses on the exact initialized flow. Symbolic algebra, exact arithmetic, source reading, and LaTeX compilation are aids, not substitutes for the proof.

**Do not access or modify GitHub.** The user handles commits and supplies the files. Do not launch new experiments by default. Do not modify the foundations, notebook, historical appendix, consolidated checkpoint, or prior increments while exploring a proof.

### 0.2 Keep every mathematical status explicit

Use the following scope labels in new work:

1. **Exact original-flow result:** holds for the positive-noise, untied, isotropically initialized model under its actual stated hypotheses.
2. **Exact analytical comparison result:** for example, the target-only flow, not the trained population.
3. **Result within the defined leading system:** rigorous within that system; no automatic finite-noise transfer.
4. **Conditional estimate:** a proved implication whose entry, guard, or forcing hypotheses are still unverified for the initialized population.
5. **Derived expansion/response calculation:** state its regularity, scaling, and remainder obligations.
6. **Empirical evidence or conjecture:** not a proof premise.

A proof supplied by another agent is not independent verification. LP, LPR, and SGWR have explicit user-reported hand checks. The newest Q2, local-passage, and repaired AN03 v2 files supply analytical proofs for review; this handoff records their contracts without claiming a fresh exhaustive audit. Report any error found, with its effect on dependent results.

### 0.3 Separate review files; no automatic merge

Every substantive proof increment must be delivered in separate, versioned files, for example:

```text
AN02_common_clock_retained_seed_v1.tex
AN02_common_clock_retained_seed_v1_review.md
```

Prefer standalone compilable LaTeX. Give all statements and equations unique label prefixes. A PDF is a reading copy of the same proof, not a separate authority.

The accompanying review note must contain:

- Precise new advance, not another overview.
- Assumptions, conclusion, parameter dependence, and dependencies by source label.
- Scope/status of each statement.
- Every first-exit guard, division, sign, differentiation under an integral, gate convention, and limit exchange that carries weight.
- The exact unresolved inequality, including failed approaches rather than hiding them in new assumptions.
- What the increment unlocks and its proposed eventual location in the checkpoint.
- Corrections to any earlier source and an explicit label map when replacing a proof.

**Do not overwrite earlier increments or insert new work into `THEOREM_A_ANALYTICAL_PROGRESS.tex`. Do not automatically `\input` unreviewed files.** First obtain mathematical review and explicit user approval. Only then produce a new consolidated version, changelog, and label map. The user's statement that a proof checks out is a review record, not a blanket instruction to modify all existing files.

### 0.4 Source availability

Use actual uploaded bytes and source labels. Some older attachment references have expired in this long conversation; re-upload a specifically needed source if a new chat cannot read it. Do not infer its contents from a filename or silently substitute a different version. The files used to prepare this handoff were available in the working container, including the re-uploaded ancestry/tail source and all three newest increments.

---

## 1. File map and source/version hierarchy

A paired `*_review.md` explains scope, audit points, and open residue; it does not supersede the `.tex` proof. Historical statements of “not found” or “not yet independently checked” in older review notes describe their preparation time, not permanent source unavailability.

### 1.1 Essential current files

| Key | File | What it is / how to use it |
|---|---|---|
| H2 | `THEORY_HANDOFF_ANALYTICAL_A_B_v2.md` | This handoff: current objectives, corrections, source map, completed additions, and updated analytical roadmap. |
| F | `RELU_POPULATION_FOUNDATIONS_v2.tex` | Frozen exact finite-parameter foundations: untied flow, balance, Gaussian calculus, exact rates, regularity, learning observables, and P10 linear control. General estimates remain useful; earlier numerical-certificate priorities do not. |
| P | `THEOREM_A_ANALYTICAL_PROGRESS.tex` | Post-foundations checkpoint 1.0, with numbered proofs/status distinctions. It predates the later AN02/AN03/AN06/LP/LPR/SGWR increments. Read its status ledger; do not treat missing later results as absent from the project. |

### 1.2 Current initialized-entry and passage increments

| Key | File (and its same-stem review note) | Main role and limitation |
|---|---|---|
| ARR | `AN02_weak_side_arrival_v1.tex` | Original-flow incoming weak-side reservoir from analytically predetermined initial labels. Gives a small mass in a fixed Q2-side terminal sector at the early envelope time. This is not the dominant amplified Q2 ancestry and not a captured weak seed. |
| TAIL | `AN02_strong_ancestry_and_tail_transport_v1.tex` | Positive-coordinate ancestry domination, outer target-only transport, ancestral tail profiles, and a same-field **upper-tail** propagation theorem with `G_∞`. Now available. Its one-sided theorem must not be used as the two-sided population theorem. |
| RET2 | `AN03_two_sided_passage_and_Q2_retention_v2.tex` | Repaired source for mixed-order/all-label bounds, normalized first-moment/Riccati passage, Q2 ancestry versus late arrivals, conditional retention and exponent tests. **Use v2, not v1.** The joint-regime applicability claim from v1 is withdrawn. |
| LOC | `AN03_local_rate_mean_tracking_v1.tex` | New nonlinear local-rate passage and collective reference tracking in the same full leading field. Controls a fixed strong core and retains the other strong labels through a weighted first moment. Gives the local power `α/λ`, closes both local guards, but still assumes entry/forcing/continuation conditions. |
| Q2 | `AN02_Q2_profiles_and_localized_tracking_v1.tex` | Exact finite-noise target-only first integral/density; exact zero-noise coordinate-energy profile; analytic target-only crossing/transit coefficients; exact conditional original-flow left-facing tracking with an explicit full-output defect. No retained weak-chart mass constant is yet established. |
| SGWR | `SIGNED_GROWTH_WEAK_RETENTION_v1.tex` | Checked signed Jensen, exact weak-coordinate amplitude, conditional cohort growth bound, interior-Q2 Gaussian defect estimate, and frozen resident attraction. Its old unavailable-`G_∞` discussion is superseded by TAIL/RET2/LOC. The proposed response-normalized amplitude clock is not proved in this file. |

### 1.3 Learned witnesses and the two completed additions

| Key | File (and its same-stem review note) | Role / current completion |
|---|---|---|
| WIT | `AN06_learned_orbit_witnesses_v2.tex` | Leading coherent learned witnesses, quarter-mass descent at the exact canonical scaled offset, local common windows/rectangle, gate-aware conditional population robustness, own-half-mass clock, and static exact-Gaussian learning bounds. Not initialized selection or canonical finite-noise coverage. |
| LP | `LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex` | **Checked linear extension of P10**, including diagonal-moment assumptions and counterexample; **checked limiting permanence**, eventual strong-input monotonicity/sqrt-log growth, uniform clearing, and conditional growing-window transfer. |
| LPR | `LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex` | **Checked combined learned limiting reversal and clearing on WIT's rectangle**; weak-coordinate sqrt-log growth; all-coordinate growth corollary; scalar saturated-mass damping; earlier negative-budget retention; conditional exponent algebra. The negative-only budget is no longer the preferred seed-generation estimate. |
| REV | `AN02_AN06_review_addendum_v1.tex` and `AN02_AN06_independent_review_v1.md` | Review deductions: conditional conservative-power compatibility, finite-time angular surjectivity, static learning with an explicit background budget. Not a captured seed or original-flow rate-transfer result. |

### 1.4 Supporting derivations and history

| File | Role and restriction |
|---|---|
| `LEAK_COMPENSATION_FACTORIZATION_AUDIT.md` | Exact source-by-motion factorization and complete remainders, plus numerical audits. Later exact-lag distinctions supersede a naive finite-q use of the leading lag. Snapshot fits are not uniform bounds. |
| `TWO_NEURON_SMALL_NOISE_LIMIT.md` | Six-dimensional leading atom system and selected-orbit reversal. Use later real-root/rho-range and population splitting corrections. Two-atom invariance does not prove condensation. |
| `SCALED_POPULATION_SPLITTING_THEORY.md` | Full scaled population, coherent-versus-shape spectra, lag positivity, probe/covariance identities, and small-split response. LOC now supplies conditional nonlinear local passage beyond its original linear multipliers. |
| `theorem_A_initialized_escape.pdf` | Retain Sections 1–3 for analytical early escape. Its numerical-reference continuation from Section 4 onward is obsolete as the current strategy. Relevant retained mathematics is in P. |
| `SIM.md` | Reference to the original SIM/Swing-by setting, linear theory, assumptions, experiments, and caveats. Do not import tied linear dynamics into the untied ReLU model. |
| `main-15.tex` | Historical research notebook; selectively reuse checked statements with exact assumptions. Not the current unified theory or a completed initialized proof. |
| `main-appendix-frozen-theory-selfcontained.tex` / `ood_reversals-appendix.tex` | Historical appendix with separate regimes and conditional/certificate arguments. No inference of initialized entry from its conditional learned-state result. |
| `THEORY_HANDOFF_ANALYTICAL_A_B.md` | Previous handoff; superseded as a roadmap by H2, not modified. |
| `AN03_two_sided_passage_and_Q2_retention_v1.tex` | Historical version. Use RET2's repaired mixed-order/moment proofs and corrected scope; retain v1 only to audit changes. |
| `population_law_checks.py`, `split_mode_checks.py`, `pilot_mechanism_analysis.py`, CSVs | Diagnostic provenance, not mathematical proof premises. No need for simulation arrays to start an analytical increment. |

### 1.5 Reading order

For the next initialized lemma: **H2 → LOC contract/closure → Q2 profile/tracking → RET2 ancestry/retention and repaired passage → TAIL ancestry → SGWR**, consulting F/P only for actual dependencies. WIT specifies the eventual learned-window tolerance. LP/LPR need not be re-proved.

For paper integration of the completed additions: **F P10 → LP → WIT → LPR**. Do not conflate presentation work with the still-open initialized proof.

---

## 2. Locked setting, notation, and units

We specialize the SIM task to **two informative concepts in the plane**, with no origin cluster:

\[
P_1=\mathcal N(e_1,q^2I_2),\qquad
P_2=\mathcal N(\rho e_2,q^2I_2),\qquad
P=(P_1+P_2)/2,
\quad 0<\rho<1,\ q>0.
\]

The targets are `y = X`. The network is bias-free, two-layer ReLU, with both layers trained independently:

\[
f_h(X)=\sum_{i=1}^h w_i(u_i^\top X)_+,
\qquad \mathcal L=\tfrac12\mathbb E_P\|f(X)-X\|^2.
\]

The initialization is **aligned-balanced isotropic**, not merely norm-balanced:

\[
u_i(0)=w_i(0)=\sqrt{S_0/h}\,a_{\alpha_i},
\quad a_\theta=(\cos\theta,\sin\theta),
\quad \alpha_i\sim\mathrm{Unif}[0,2\pi).
\]

The continuum label law is `λ₀(dα)=dα/(2π)`, with

\[
U_\alpha=\sqrt{m_\alpha}a_{\theta_\alpha},\quad
W_\alpha=\sqrt{m_\alpha}b_{\psi_\alpha},\quad
\nu=\int m_\alpha\delta_{(\theta_\alpha,\psi_\alpha)}\,d\lambda_0,
\]

\[
\theta_0=\psi_0=\alpha,\qquad m_0=S_0,\qquad
f_\nu(X)=\int b_\psi(a_\theta^\top X)_+\,d\nu.
\]

Thus `S₀ = h ε_h²` is fixed in the width limit and

\[
f_0(X)=S_0X/4.
\]

Balance is preserved; vector alignment generally is not. Use `s = d = 2` only for the number of concepts and dimension; do not reuse `s` for initialization mass. In the limiting equations below, `λ = ρ²` is a scalar growth rate, not the label law `λ₀`. A shifted weak-learning clock is denoted `s` when explicitly introduced.

Physical normalization:

\[
\rho=\mu_2/\mu_1,\quad q=\sigma/\mu_1,\quad
\tau=\mu_1^2t_{\rm phys}.
\]

There is no additional time factor from width. For a fixed numerical unit probe,

\[
D_p^{\rm phys}=\mu_1^2D_p^\tau.
\]

Do not additionally rescale the probe while using that formula. The canonical physical scaling has `μ₁ = 3`, so `τ = 9t_phys`.

Use target-minus-output residual `e(X)=X−f(X)`:

\[
R_p(\theta)=\mathbb E_{P_p}[e(X)X^\top\mathbf1_{a_\theta^\top X>0}],
\quad R=(R_1+R_2)/2.
\]

Then

\[
\theta'=b^\top Ra^\perp,\quad
\psi'=(b^\perp)^\top Ra,\quad
(\log m)'=2b^\top Ra.
\]

The exact cluster decomposition is

\[
V_p(\xi)=\int\left[(a^\top\xi)_+R_pa
+\mathbf1_{a^\top\xi>0}bb^\top R_p\xi\right]d\nu,
\quad
D_p^\tau=-\tfrac12 e_\xi^\top V_p(\xi),
\]

\[
E_\xi'=D_1^\tau+D_2^\tau.
\]

The factor `1/2` is the equal mixture weight. Every neuron and both actual selectors are included. Interpret derivatives almost everywhere unless the required pointwise regularity and boundary conditions are proved.

Learning must be measured by exact observables, for example

\[
\mathsf m_p=\frac{\mathbb E_{P_p}[X_pf_p(X)]}{\mathbb E_{P_p}[X_p^2]},
\qquad
\mathcal L_p=\tfrac12\mathbb E_{P_p}\|f(X)-X\|^2.
\]

A mass called “weak” is not by itself a proof of weak learning.

---

### Additional notation guards introduced by the new increments

- `λ₀` is the initial-label probability law; `λ=ρ²` is a scalar growth rate.
- `α_sh=λΦ(ρaρ)/2` is the splitting coefficient; do not confuse it with an initial label `α₀`.
- `κ=log(1/S₀)/log(1/q)` (or a fixed power in `S₀=q^κ`) is a joint-scaling exponent. It is unrelated to the small-split enhancement coefficient often also called `κ`; name the latter `κ_enh` in new work.
- In LOC, `(c_ref,d_ref)` is a same-field reference characteristic. In SGWR, `c_cmp(τ)` is a scalar comparison response. In the proposed new clock, `c_q=mathsf m₂` is the exact cluster-2 response. These three uses of `c` must never be interchanged.
- `N` is radial mass in the closed leading weak family. `c_q` is an exact regression response. `H_C=∫_C hα dλ₀` is a fixed-cohort coordinate-amplitude integral. None is identical to another without a proof.
- `r_core` is an essential-supremum joint input/output displacement; `rα=(log mα)'` is a signed radial rate. `T_tail` is a weighted tail first moment; `Tδ`, `t_b`, and `τ_h` are times.
- `L₀=Y+K_w` is a leading mean lag; `L_{1,q}^{mean}=E_{P1}f₂/q` is its exact finite-noise counterpart; `r₂₁=E_{P1}[X₁(f₂-X₂)]/(1+q²)` is a different projection.
- `υ=U₁/(qU₂)=tan(qu)/q` is a tangent coordinate, not exactly the angular coordinate `u`.
- `g_q` in Q2 is the **full** target-only logarithmic mass rate; older `g₀` denotes half that rate.
- Keep clocks distinct: deterministic early-envelope time; strong response/mass threshold; target-only weak-axis crossing; common chart-entry time; leading weak half-mass time; exact response half-learning time. A numerical similarity between clocks does not identify them analytically.

---

## 3. Theorem contracts and the strengthened finite-noise deliverable

### 3.1 Theorem A — initialized signed competition and quantitative reversal (open)

Prove an explicitly specified, nonempty admissible **joint** parameter family near a moderate ratio, preferably a neighborhood of `ρ=2/3`, with positive noise and positive aligned-isotropic initialization. The parameter family and all prefactors must be justified by the same entry/passage/transfer argument. No interval for κ is currently established as an initialized A regime.

For a positive-length scaled-probe interval I, let

\[
\xi_q(\zeta)=(\sin(q\zeta),-\cos(q\zeta)).
\]

Prove an analytically defined time centering `τ_h(q,S₀,ρ)` and common finite centered windows J with ordered subintervals J₋,J₊, reached from time-zero initialization, on which the **exact original** population has:

\[
\mathsf m_1\ge c_1^{\rm learn}>0,\qquad
\mathsf m_2\ge c_2^{\rm learn}>0,\qquad
\mathcal L_p\le(1-\kappa_p)\mathcal L_p(0),\quad \kappa_p>0;
\]

\[
D_1^\tau\le-c_1q^2<0,\qquad D_2^\tau\ge c_2q^2>0\quad\text{on }J;
\]

\[
D_1^\tau+D_2^\tau\le-\gamma_-q^2\text{ on }J_-,\qquad
D_1^\tau+D_2^\tau\ge\gamma_+q^2\text{ on }J_+.
\]

The learning and rate constants must be nonvanishing in the claimed joint limit. Integration gives rebound at least `c_rev q²` on an angular sector of width at least `|I|q`.

WIT now supplies a limiting route with weak mass strictly above `1/4`; under its exact static hypotheses it gives responses `mathsf m₁≥1/2`, `mathsf m₂≥1/4` and a fixed loss reduction. A stronger half-learning threshold is optional, not a missing prerequisite for the first A.

Keep opposite source signs local to the learned interval. The earlier empirical `D₂` changes sign. Do not demand or claim opposite signs at all times. Unique/transverse crossing, exact decimal timing, finite width, and arbitrary dimension are not prerequisites.

### 3.2 Required companion to A: finite-noise matching on every fixed centered window (open)

**Build this requirement into AN7 now.** It is stronger than control only near the reversal and is what the already-proved persistence corollary requires.

For an analytically selected joint family, a proved centering, and every fixed finite centered interval K on which the selected limiting family is compared, prove

\[
\sup_{\rho\in\mathcal K_*,\ \zeta\in I,\ s\in K}
\left|
\frac{E_{q,S_0,\rho}(\tau_h+s,\xi_q(\zeta))-1/2}{q^2}
-\mathcal E_{\rho,\zeta}(s)
\right|\longrightarrow0.
\tag{A-error-transfer}
\]

Here E is indexed by normalized time; the physical time is `(τ_h+s)/μ₁²`. Keep all background/outside labels and any family-membership flux in the transfer. Ensure the original time is nonnegative for the intervals considered.

On the fixed **gate-separated learned witness windows**, also prove

\[
\sup_{\rho,\zeta,s\in J}
\left|D_{p,q,S_0,\rho}^{\tau}(\tau_h+s,\xi_q)/q^2-d_{p,\rho,\zeta}(s)\right|
\longrightarrow0,
\tag{A-rate-transfer}
\]

or explicit errors below the source and total-rate margins. No uniform pointwise rate convergence across a limiting gate-hit atom is asserted without a separate argument; use the continuous error observable on arbitrary late windows and a.e./integrated rates where appropriate.

The original centering may be a response-defined clock if that clock is analytically proved to exist and matched to the limiting half-mass phase. Do not define it by an empirical lookup or equate a response with chart mass.

For a broad split limiting family, replace the coherent comparator explicitly; the existing coherent persistence theorem then does not automatically apply. The first initialized near-coherent result and a later non-small-bridge result belong to one population model but have different quantitative obligations.

### 3.3 Theorem B — the analytical mechanism (initialized version open)

The same proof should show why A occurs, rather than attach a post-hoc interpretation to an independently certified crossing:

1. Cross-output leakage shapes the residual and generates compensation in the population seen by the off-cone probe.
2. Cluster-1 help is exposure times a **signed exact lag** plus explicitly controlled finite-noise corrections. The small lag is a cancellation; control must be relative to its sign margin.
3. Cluster 2 induces harmful input rotation of the active strong population through a selected first-coordinate residual; weak-family output may be the residual producer while the strong family is the carrier.
4. The evolving lag, exposure, alignment, and selected residual force the change of dominance with complete remainder control.

**B-core** is the mechanism sufficient for an initialized small-shape theorem. **B-bridge** is the non-small inactive-cohort comparison explaining the canonical depth enhancement. The latter may remain a separate open/empirical extension in a first paper theorem, but must not be advertised as proved by B-core. Small variance perturbation is not the canonical mechanism theorem.

### 3.4 Initialized persistence — conditional implication proved; premise open

LP already proves: if A-error-transfer holds on every fixed late window, uniformly over the stated compact parameter/probe set, and the selected limiting orbit clears at one common S, then along the proved joint family there exist

\[
T_q\to\infty,\qquad\varepsilon_q\to0,
\]

such that

\[
\sup_{\rho,\zeta,\ S\le s\le S+T_q}
\left|E_{q,S_0,\rho}(\tau_h+s,\xi_q)-\frac12\right|
\le\varepsilon_q q^2.
\tag{P-initialized}
\]

The diagonal implication itself is proved and user-checked. Its original-flow convergence premise is not. This conclusion belongs on the same parameter family actually established by A/AN7, not on the unproved `(6.5,11.7)` regime and not automatically at the canonical E6 parameters.

The left endpoint S must be after uniform limiting clearing, not an arbitrary short delay after the minimum. A lower-bound-only route can instead bound `[ξᵀf(ξ)]₊`; it does not require every label to switch off.

Adding this requirement to the contract now avoids forgetting it, but **proving it is not free**: it requires estimates on every fixed post-learning window beyond the crossing windows.

---

## 4. Existing checkpoint results — stable labels, not the full later status ledger

The LaTeX checkpoint labels below are stable reference points in P. Later increments extend several rows; consult Sections 6–10 below. “Proved within the leading system” means exactly that, not initialized finite-noise validity.

| Result | Status / scope | Checkpoint label |
|---|---|---|
| Exact flow/rates/learning and linear control | Imported from foundations; no initialized late signs | `pa:setup` |
| Spectral residual bound, mass/alignment/radius envelopes | Analytical from isotropic initialization | `pa:earlybounds` |
| Exact target-only comparison | Analytical finite-time comparison, not a numerical reference | `pa:targetcomparison` |
| Canonical early mass escape | `S(6)>16S₀=.0032` in normalized time; not weak learning | `pa:canonicalescape` |
| Full source-by-motion rate decomposition | Exact finite-parameter identity | `pa:motion` |
| Gaussian projection compensation | `c_A = −ℓ_I + r₂₁` exactly | `pa:projection` |
| Help/harm factorization with all errors | Exact finite-parameter identities, errors not yet bounded along initialized flow | `pa:factorizations` |
| Fixed-label lag tracking equation | Exact identity and conditional comparison; forcing/sign closure open | `pa:tracking` |
| Truncated-Gaussian overlap kernel | Exact, `C¹,¹` on compact sets, not generally `C²` | `pa:overlap` |
| General scaled population equations | Derived leading system; uniform finite-noise transfer open | `pa:leading` |
| Logistic family masses / fixed-label relative weights | Exact within the closed leading family system | `pa:masslaws` |
| Fixed-direction resident curve | Exact within leading system | `pa:resident` |
| Stable coherent block, unstable centered shape | Exact linearization, not nonlinear condensation | `pa:spectra` |
| Moving splitting matrix | Exact first-order shape equation | `pa:moving-shape` |
| Strong-stage and frozen-resident passage multipliers | Exact linearized formulas | `pa:multipliers` |
| Same-field ordering and covariance sign | Conditional on ordered entry, common field, and chart validity | `pa:order` |
| No weak-chart equilibrium at initial zero-mass state | Proved within leading system | `pa:noweakeq` |
| Positive lag for arbitrary weak distribution at `M=1` | Proved within leading system; no condensation required | `pa:lagtheorem` |
| Population probe error and source rates | Exact leading identities; static finite-q expansion has chart assumptions | `pa:probe-pop` |
| Partial-activity/covariance/inactive compensation identities | Exact within leading observable | `pa:active-error` |
| Real weak saddle coordinate for `0<ρ<1` | Proved; old positive-root restriction removed | `pa:weakroot` |
| Distinguished coherent weak-growth branch | Analytical orbit defined by saddle, not fitted angles | `pa:branch` |
| Reversal on that selected orbit | Analytical theorem, not yet isotropic selection | `pa:limitreversal` |
| Exact finite-q mean lag and Stein relation | Exact original-state identities | `pa:Lex` |
| Explicit tail-moment error from mean lag to leading lag | Exact bound, potentially too large at canonical parameters | `pa:lagerror` |
| Finite-q same-field cross derivatives | Exact equality; positivity open in reached regime | `pa:finiteqorder` |
| Non-small instantaneous bridge displacement signs | Exact in leading field; coupled trajectory comparison open | `pa:bridge-force` |
| Small-split second-order response functional | Derived finite-window response; incoming limit and analytical positive coefficient open | `pa:response-eq`, `pa:kappa` |
| Window-to-rebound implication | Proved elementary assembly; initialized hypotheses still open | `pa:assembly` |

The frozen weak-attractor saddle-node near `M≈.4768`, the coefficient `κ≈1.75053`, the seed exponent, and the threshold near `.76` are **not** analytical initialized conclusions.

---

## 5. The unified scaled population model

These equations are worth retaining in the handoff because they define the common analytical object. Let `λ=ρ²` and

\[
K(r)=\phi(r)+r\Phi(r),\qquad K(r)-r>0.
\]

Strong and weak chart coordinates are

\[
a_s=(\cos(qx),\sin(qx)),\ b_s=(\cos(qy),\sin(qy)),
\]
\[
a_w=(\sin(qu),\cos(qu)),\ b_w=(-\sin(qv),\cos(qv)).
\]

For weighted distributions `μ_s(dx dy)` and `μ_w(du dv)`, define total, not normalized, moments

\[
M=\int d\mu_s,\ N=\int d\mu_w,\ Y=\int y\,d\mu_s,\ V=\int v\,d\mu_w,
\]
\[
K_s=\int K(\rho x)d\mu_s,\quad K_w=\int K(u)d\mu_w.
\]

The overlap kernel is

\[
F(t,r)=\phi(\min(t,r))+r\Phi(\min(t,r)),
\]

\[
\partial_tF=(r-t)_+\phi(t),\quad \partial_rF=\Phi(\min(t,r)).
\]

Set

\[
\mathcal S(x)=\int F(\rho x,\rho\widetilde x)d\mu_s,
\qquad
\mathcal W(u)=\int F(u,\widetilde u)d\mu_w.
\]

The leading characteristic system is

\[
\begin{aligned}
x'&=\tfrac12[-(1-M)x+\rho\phi(\rho x)-\rho\mathcal S(x)
+\lambda\{V+(1-N)y\}\Phi(\rho x)],\\
y'&=\tfrac12[-(1-M)y-Y-K_w+\rho(1-N)K(\rho x)],\\
u'&=\tfrac12[\phi(u)-\mathcal W(u)-\{Y+(1-M)v\}\Phi(u)-\lambda(1-N)u],\\
v'&=\tfrac12[\rho K_s-\lambda V-\lambda(1-N)v-(1-M)K(u)].
\end{aligned}
\]

The reaction rates are `(1−M)μ_s` and `λ(1−N)μ_w`, so

\[
M'=M(1-M),\qquad N'=\lambda N(1-N).
\]

One atom in each family is an invariant restriction. The canonical bridge is represented by a spread-out strong distribution, not a separate phenomenological mechanism.

**Do not overlook the scope:** these are bounded noise-scaled charts. The isotropic population does not start there; labels outside them and labels entering them must be controlled. Constant relative family weights are a leading-system statement for fixed labels. They do not justify ignoring mass-rate differences at finite noise or flux through changing masks.

### The stable mean and unstable shape

The resident direction solves

\[
a_\rho=\rho K(\rho a_\rho),\quad
P=\Phi(\rho a_\rho),\quad \alpha=\lambda P/2.
\]

The curve `μ_s=Mδ_(a,a), N=0` has fixed angles for every logistic `M`. Its mean and centered shape matrices are

\[
J_{\rm mean}(M)=
\begin{pmatrix}-(1-M)/2-M\alpha&\alpha\\\alpha&-1/2\end{pmatrix},
\]

\[
J_{\rm sh}(M)=
\begin{pmatrix}-(1-M)/2&\alpha\\\alpha&-(1-M)/2\end{pmatrix}.
\]

The centered `(1,1)` direction becomes unstable at `M>1−2α`. At `M=1` the coherent block is stable but centered splitting grows at `α`. In the continuum there is a family of unstable shape profiles, not literally just one extra scalar dimension.

During weak learning the shape matrix has an additional diagonal term:

\[
J_{\rm sh}(\tau)=
\begin{pmatrix}-(1-M)/2+\beta&A_{\rm sh}\\A_{\rm sh}&-(1-M)/2\end{pmatrix},
\]

\[
A_{\rm sh}=\tfrac\lambda2(1-N)\Phi(\rho x),\quad
\beta=\tfrac{\rho^3}{2}[Nv+(1-N)y-x]\phi(\rho x).
\]

The resident linear multipliers are

\[
\frac{h_+(M_1)}{h_+(M_0)}=
\left(\frac{M_1}{M_0}\right)^{\alpha-1/2}
\left(\frac{1-M_0}{1-M_1}\right)^\alpha,
\]

and, in the separately defined frozen weak-growth approximation,

\[
h_+(N)=h_+(N_0)(N/N_0)^{\alpha/\lambda}.
\]

A nonlinear passage proof must retain moving coefficients and mean feedback. The relevant entry ratio is of the form

\[
\delta_{\rm ent}N_{\rm ent}^{-\alpha/\lambda},
\]

plus mean, weak-angle, outside-population, and finite-noise errors. A small entry shape alone is not sufficient if the weak seed is extremely small.

### Population help and partially active error

At `M=1`, the leading lag is `L₀=Y+K_w`. The positive-lag theorem gives an equation with damping and explicitly nonnegative forcing, including the symmetrized overlap term `Ξ>0`. Consequently positive incoming `L₀` stays positive without assuming condensation.

Set

\[
A_\zeta=\int(\zeta-x)_+d\mu_s,\quad
B_\zeta=\int y(\zeta-x)_+d\mu_s.
\]

Then

\[
\mathcal E_\zeta=\tfrac12A_\zeta^2-\zeta A_\zeta+B_\zeta,
\qquad d_1=-\tfrac12A_\zeta L_0,
\]

\[
d_2=\int_{x<\zeta}(\zeta-A_\zeta-y)x'_2\,d\mu_s
+\tfrac\rho2(1-N)\int(\zeta-x)_+K(\rho x)d\mu_s.
\]

The second term in `d₂` is weak-sourced output rotation. Do not discard it merely because `q→0`. The sign of `d₂` and its takeover for broad split populations remain to be proved.

For active strong mass `M_A`, normalized active means and covariance, and `h=ζ−x̄_A`,

\[
\mathcal E_\zeta=\tfrac12M_A^2h^2-M_Ah(\zeta-\bar y_A)-M_A C_A.
\]

If `Y_B` is the total output-angle moment of the inactive strong population,

\[
\mathcal E_\zeta=
\tfrac12A_\zeta^2-\zeta A_\zeta+h(L_0-K_w-Y_B)-M_A C_A.
\]

This retains the inactive bridge. The all-active simplification with `−Cov(x,y)` is not valid unchanged for a partially active canonical population.

---

### Coherent orbit and the now-completed limiting witness problem

On M=1 with one weak atom, write the leading masses/coordinates `(n,x,y,u,v)`:

\[
n'=\lambda n(1-n),\qquad n(s)=(1+e^{-\lambda s})^{-1},
\]
\[
\begin{aligned}
x'&=\frac\lambda2[nv-x+(1-n)y]\Phi(\rho x),\\
y'&=\frac12[-y-nK(u)+\rho(1-n)K(\rho x)],\\
u'&=\frac12[(1-n)(\phi(u)-\lambda u)-(nu+y)\Phi(u)],\\
v'&=\frac12[\rho K(\rho x)-\lambda v].
\end{aligned}
\]

The selected branch tends as s→−∞ to `(0,aρ,aρ,u*,aρ/λ)`, where

\[
a_\rho=\rho K(\rho a_\rho),\qquad
\phi(u_*)-a_\rho\Phi(u_*)-\lambda u_*=0.
\]

The root u* is real and unique for every `0<ρ<1`; it need not be positive over that whole range. The earlier artificial `ρ≤1/√2` restriction is removed. The branch is specified by the resident saddle and half-mass clock, not fitted entry angles.

While x<ζ,

\[
\mathcal E_\zeta=-\frac12\zeta^2+\frac12x^2+y(\zeta-x),
\quad
\mathcal E_\zeta'=(x-y)x'+(\zeta-x)y',
\]
\[
L=y+nK(u)>0,\qquad d_1=-\frac12(\zeta-x)L,
\]
\[
d_2=(x-y)x'+\frac\rho2(\zeta-x)(1-n)K(\rho x).
\]

P's selected-orbit proof gives reversal and source-sign witnesses. WIT upgrades them to a fixed learned mass and common local parameter/time windows. LP/LPR add eventual zero benefit. None supplies isotropic population selection.

---

## 6. What is now proved toward initialized entry (AN02)

### 6.1 Early comparison remains an early comparison

With `a*=1/2+q²`, the actual isotropic flow has

\[
\overline S(\tau)=S_0e^{2a_*\tau},\quad
\epsilon_{\rm al}=\overline S-S_0,\quad
H=S_0(2e^{2a_*\tau}-3e^{a_*\tau}+1).
\]

While the alignment guard holds, P/ARR give mass, input/output angle, and logarithmic radial comparisons to the exact target-only flow. At

\[
T_\delta=\frac{\log(\delta/S_0)}{1+2q^2},\qquad 0<S_0<\delta\le1/100,
\]

these have `S≤δ`, `H≤2δ`, and angle error at most `3δ`. Tδ is not a strong-learning hitting time. Error O(δ) is not automatically O(q). An O(1) learned-stage comparison cannot be obtained by continuing this estimate after its smallness condition is lost.

Sources: P `pa:earlybounds`, `pa:targetcomparison`; ARR `inc:AN02:arrival:v1:comparison`.

### 6.2 Two different cohorts must not be merged conceptually

**ARR terminal-sector reservoir.** For `ρ∈[3/5,3/4]`, `q≤1/20`, the backwards target-only interval `C_T=φ_{−T}([2π/3,3π/4])` gives actual endpoint angles in `[7π/12,5π/6]` and

\[
M_{\rm in}\ge\frac q{3000}S_0(S_0/\delta)^{1/16}.
\]

Its partial weak response is at least `M_in/5`; Gaussian leakage is bounded but nonzero. This is an incoming sector, not a bounded weak scaled chart, not a full response bound, and not the main amplified Q2 seed.

**TAIL/RET2 fixed positive-coordinate ancestry.** Starting from a fixed initial label α₀,

\[
m_\tau(\alpha_0)\ge e^{-2H}S_0
\left[e^\tau(\cos\alpha_0)_+^2+e^{\lambda\tau}(\sin\alpha_0)_+^2\right].
\]

For any fixed C⊂Q2 in **initial-label space**, RET2 gives

\[
\int_Cm_{T_\delta}\,d\lambda_0
\ge e^{-4\delta}\delta^\lambda S_0^{1-\lambda}
 e^{-2\lambda q^2T_\delta}\int_C\sin^2\alpha_0\,d\lambda_0.
\tag{ancestry}
\]

For all Q2 ancestry, the last integral is 1/8. This is an original-flow lower bound on ancestral mass at an early time. It is not a matching asymptotic law, current weak-mask mass, retained weak-chart seed, or statement of output learning.

RET2 also proves that the Q2 portion of ARR's fixed-sector arriving cohort is at most `O_δ(S₀^(1+λ/2))` when `q²Tδ→0`. Its initial sin² weight shrinks with T. Therefore the global Q2 ancestral amplification cannot be applied uniformly to that late-arriving subset to manufacture the larger seed.

Sources: TAIL `inc:AN02:tail:v1:weightedmass`; RET2 `Q2mass`, `arrivalupper`, prefix `inc:AN03:ret:v2:`.

### 6.3 Existing exact ancestry-to-capture interface

RET2 defines a terminal capture functional using fixed Q2 ancestry, terminal membership in a prescribed weak chart, and net radial growth. It proves

\[
N_2^{\rm cap}(\tau_e)\ge e^{-4\delta}\delta^\lambda S_0^{1-\lambda}
 e^{-2\lambda q^2T_\delta}\,\mathcal R_2(\tau_e).
\]

The functional includes `sin²α₀ min{1,exp∫ r_rad}` and a terminal chart indicator. This is an exact implication; it does not bound `mathcal R₂` away from zero. No moving-indicator derivative is taken, hence no flux is silently omitted. Persistent chart membership after capture is still separate.

Sources: RET2 `retentionfunctional`, `retention`, `retentionbound`.

### 6.4 New exact target-only profiles and the corrected weights

In Q2, the exact finite-noise **target-only** flow has

\[
\widehat\theta'=v_q(\widehat\theta),\quad
(\log\widehat m)'=g_q(\widehat\theta),
\]
\[
v_q(\theta)=\frac q2[-\sin\theta K(\cos\theta/q)+\rho\cos\theta K(\rho\sin\theta/q)].
\]

On a nonstationary interval, choose `G_q'=g_q/v_q`. Then

\[
\log\widehat m-G_q(\widehat\theta)=\text{constant},\qquad
\partial_{\alpha_0}\varphi_t=\frac{v_q(\varphi_t)}{v_q(\alpha_0)}.
\]

The exact radial pushforward density is

\[
\frac{d\widehat\nu_t}{d\theta}=
\frac{S_0}{2\pi}e^{G_q(\theta)-G_q(\alpha_0)}
\frac{v_q(\alpha_0)}{v_q(\theta)},\quad \alpha_0=\varphi_{-t}(\theta).
\]

No division at a stationary speed is allowed.

In the **zero-noise target-only comparison** (q below is a coordinate scale),

\[
\overline U_1=\sqrt{S_0}\cos\alpha_0,\qquad
\overline U_2=\sqrt{S_0}\sin\alpha_0e^{\lambda t/2}.
\]

With `b_t=e^(−λt/2)/q` and `υ=overline U₁/(q overline U₂)<0`, the exact **coordinate-energy** density is

\[
d\nu_{2,t}(\upsilon)=\frac{S_0e^{\lambda t}}{2\pi b_t}
(1+\upsilon^2/b_t^2)^{-2}d\upsilon,
\quad \nu_{2,t}(\mathbb R_-)=S_0e^{\lambda t}/8.
\]

Radial mass and angular coordinate require

\[
d\nu_{m,t}=(1+q^2\upsilon^2)d\nu_{2,t},\qquad
\upsilon=\tan(qu)/q,
\]
\[
\frac{d\nu_{m,t}}{du}=\frac{S_0e^{\lambda t}}{2\pi b_t}
\left(1+\frac{\tan^2(qu)}{q^2b_t^2}\right)^{-2}\sec^4(qu).
\]

The coordinate-energy angular density has sec² instead. Do not call the simple Cauchy-squared profile an exact positive-noise radial law in u. At fixed negative u, the cross-gate term K(u) remains nonzero in the small-noise scaling.

Q2 also supplies a labelwise outer comparison with error `[3q²/4+K(−L)/(2L)]T` under two projected-margin guards and a first-exit smallness condition. It is not yet a Jacobian/density approximation theorem.

Sources: Q2 `firstintegral`, `cauchy`, `outer`, prefix `inc:AN02:q2:v1:`.

### 6.5 New analytical target-only transit clocks

For fixed initial `α₀=π/2+d₀`, `0<d₀<π/2`,

\[
T_\times(q,\alpha_0)=\frac2\lambda\log\frac{\tan d_0}{q}+C_\rho+o(1),
\]
\[
C_\rho=\int_0^1\frac{2\,dz}{K(-z)+\lambda z}
+\int_1^\infty\left[\frac{2}{K(-z)+\lambda z}-\frac{2}{\lambda z}\right]dz.
\]

Q2 proves convergence uniformly on compact ratio/initial-angle ranges. After including that crossing time:

\[
\frac{T_{\theta_b}}{\log(1/q)}\to\frac2{\lambda(1-\lambda)}
\quad\text{for fixed }0<\theta_b<\pi/2,
\]
\[
\frac{T_R}{\log(1/q)}\to\frac2\lambda+\frac4{1-\lambda}
\quad\text{for the sufficiently large prescribed target }\theta=qR.
\]

At λ=4/9 the crossing, fixed-Q1-angle, and strong-chart coefficients are 4.5, 8.1, and 11.7. These are now analytical **target-only** coefficients. They are not initialized population absorption/return thresholds. The trained residual changes at strong saturation; a later return can occur.

Sources: Q2 Theorems 4.1–4.2, `cross`, `transit`.

### 6.6 New conditional original-flow left-facing comparison

Decompose the **actual full output**

\[
f_t(X)=\mathfrak M(t)X_1e_1+g_t(X),\qquad
\mathcal E_{\rm out}(t)=\sqrt{a_*}\|g_t\|_{L^2(P)},\quad\mathfrak M\ge0.
\]

`mathfrak M` is a chosen comparator coefficient, not a proven learned mass. For a unit input with a₁≤0, Q2 proves

\[
|(A_\theta a)_1|\le q,\qquad |a_1|\|A_\theta e_1\|\le2q,
\]
\[
\|C_fa\|\le q\mathfrak M+\mathcal E_{\rm out},\quad
\|C_f^Tb\|\le2q\mathfrak M+a_*\mathfrak M\|b-a\|+\mathcal E_{\rm out}.
\]

The corresponding zero-initial-data scalar envelopes are

\[
\begin{aligned}
\Delta'&=a_*\mathfrak M\Delta+3q\mathfrak M+2\mathcal E_{\rm out},\\
H_Q'&=a_*H_Q+a_*(1+\mathfrak M)\Delta+2q\mathfrak M+\mathcal E_{\rm out},\\
L_Q'&=2a_*(\Delta+H_Q)+2q\mathfrak M+2\mathcal E_{\rm out}.
\end{aligned}
\]

While the **actual input** remains left-facing and Δ<π,

\[
|\psi-\theta|\le\Delta,\quad |\theta-\widehat\theta|\le H_Q,
\quad |\psi-\widehat\theta|\le\Delta+H_Q,
\quad |\log(m/\widehat m)|\le L_Q.
\]

The dominant strong output costs O(q mathfrak M), not O(mathfrak M), in these contractions. The full-output defect remains unbounded along the initialized learned stage. Its weighted time integrals must be established; crossed Q2 ancestry in Q1 needs a new positive-side transit/return estimate. “Q2 ancestry” does not satisfy the left-facing guard after it crosses.

Sources: Q2 Lemma 5.1 / Theorem 5.2, `gaussiansuppression`, `originaltracking`.

---

## 7. Current nonlinear passage results (AN03)

### 7.1 RET2: repaired two-sided global estimate, not initialized applicability

TAIL's profile theorem controls upper-ordered deviations. RET2 supplies all-label upper, lower, and mixed-order inequalities and corrects the first-moment differentiation using uniform labelwise Lipschitz bounds and the fixed label law. Do not use the co-ordered identity as an equality for a mixed-order pair.

For `Dα=|xα−c_ref|+|yα−d_ref|`, RET2 gives

\[
D^+D_\alpha\le\left[-\frac{(1-\lambda)(1-M)}2+
\frac\lambda2(1-N)+b_c\right]D_\alpha,
\quad b_c\le c_\rho(\mathcal B_++R_1).
\]

The two-sided direct strong-mass factor is `(M₀/M)^((1−λ)/2)`, **not** the upper-only TAIL factor `sqrt(M₀/M)`.

With normalized first moments R₁ and

\[
L(t)=\sqrt{N(t)/N_0}\exp\left(c_\rho\int\mathcal B_+\right),\qquad
Q(t)=1-c_\rho R_1(t_0)\int_{t_0}^tL,
\]

RET2 Theorem 4.2 proves `D(t), R_p(t) ≤ (L/Q)` times their entry values while Q>0. A stated smallness condition closes Q≥1/2 to N=1/2. The mean-imbalance integral is still a hypothesis, and chart-valid evolution is required. The initial distance is joint input/output, not input spread alone.

Its conditional exponent algebra remains valid. On the reviewed ratio interval,

\[
\eta_{\rm glob}=\frac\lambda2(1-P)>\frac{16393}{200000}.
\]

**This is not a nonempty initialized joint-regime theorem.** All q-dependent entry factors and all simultaneous guard conditions must be supplied. Do not repeat the former inference that local rates are merely a constant improvement. Nor assert global impossibility without a proof.

Sources: RET2 `alllabel`, `halfpassage`, `exponent`, `uniformeta`, prefix `inc:AN03:ret:v2:`. Use TAIL's `profiletheorem/globalG` only in its actual one-sided scope.

### 7.2 LOC: nonlinear local-rate control and collective tracking together

This is the main new passage tool.

Work in the **full defined leading system**, with fixed family labels, bounded support on compact intervals, `0<M≤1`, `0<N≤1/2`. Let η be the normalized full strong-label law. Choose a fixed positive-weight strong core C and a reference characteristic `(c_ref,d_ref)` evolving in the **same full field**; it need not be an atom carrying mass.

Define

\[
D_\beta=|x_\beta-c_{\rm ref}|+|y_\beta-d_{\rm ref}|,\quad
r=\operatorname*{ess\,sup}_{\beta\in C}D_\beta,
\]
\[
T_{\rm tail}=\int_{C^c}D_\beta\,d\eta,\quad
\mathfrak f=N+|V|+K_w+T_{\rm tail},
\]
\[
e_{\rm ref}=\sqrt{(c_{\rm ref}-a)^2+(d_{\rm ref}-a)^2},
\quad C_0=4(a+3),
\]
\[
\gamma=\frac{\alpha(1/2-\alpha)}{\alpha+1/2}>0,
\quad g=\gamma/2,\quad e_* =\min\{1,\gamma/(2C_0)\}.
\]

All remaining strong labels are retained through a **first absolute moment**, not their mass alone. The weak moments V,K_w are unnormalized totals. Population outside the physical noise-scaled charts needs an additional original-flow error budget and is not automatically covered by calling it a tail.

**Shape, all coordinate orders (Lemma 2.1).** While e_ref≤1 and r≤1,

\[
D^+r\le[\alpha(1-N)+C_0(e_{\rm ref}+r+\mathfrak f)]r.
\tag{local-shape}
\]

The proof keeps Φ(ρ(c_ref+r)) near Φ(ρa), uses the lower-side donor cancellation, and covers mixed-order labels. It does not assume pointwise ordering of core labels.

**Collective mode (Lemma 3.1).** The collapsed no-weak comparison has `(a,a)` stationary for every M, with

\[
J_M=\begin{pmatrix}-(1-M)/2-M\alpha&\alpha\\\alpha&-1/2\end{pmatrix}
\preceq J_1.
\]

The reference does not follow that collapsed field; its full-field defect is bounded using the actual donors. This gives

\[
D^+e_{\rm ref}\le-\gamma e_{\rm ref}+C_0e_{\rm ref}^2+C_0(r+\mathfrak f).
\tag{local-mean}
\]

Inside e_ref≤e*,

\[
e_{\rm ref}(t)\le e_0e^{-g(t-t_0)}+
C_0\int_{t_0}^t e^{-g(t-s)}(r+\mathfrak f)(s)\,ds.
\]

This proves control of the **same-field reference and core mean** rather than prescribing a numerical mean path. The full strong barycentre additionally costs T_tail pointwise; a bound on ∫T_tail alone does not give a pointwise full-mean estimate.

**Coupled passage (Theorem 4.1).** Fix `0<N₀<n_b≤1/2`, with n_b fixed independently of N₀, and let t_b be the leading logistic time when N=n_b. Suppose the solution/reference are defined in the stated class and

\[
\int_{t_0}^{t_b}\mathfrak f\le F_b.
\]

Set

\[
K_0=C_0(1+C_0/g),\quad a_b=\alpha(1-n_b),\quad
\mathcal A=r_0e^{C_0e_0/g+K_0F_b}(n_b/N_0)^{\alpha/\lambda}.
\]

The explicit sufficient conditions are

\[
e_0\le e_*/4,\quad F_b\le e_*/(4C_0),\quad
\mathcal A\le\min\{1/4,a_b/(2K_0),ge_*/(8C_0)\}.
\tag{local-guards}
\]

Then throughout the interval,

\[
e_{\rm ref}\le3e_*/4,\quad r\le2\mathcal A\le1/2,
\]
\[
r(t_b)\le 2e^{C_0e_0/g+K_0F_b}(n_b/N_0)^{\alpha/\lambda}r_0,
\quad\int_{t_0}^{t_b}r\le\frac{2\mathcal A}{a_b}.
\tag{local-passage}
\]

The comparison multiplier, not the actual radius, satisfies a positive lower growth rate. The Riccati denominator closes at Q≥1/2 without an extra log(1/N₀). Do not replace this proof by the invalid assertion that an upper growth inequality forces the actual radius to grow.

If `|V|+K_w≤C_wN+w`, a fixed sufficiently small n_b makes the N part of F_b small; **∫(w+T_tail) remains to be bounded**. A merely O(1) forcing budget is not enough when the theorem requires the explicit small threshold above.

**After n_b (Proposition 5.1).** A bounded continuation to N=1/2 costs only a multiplicative factor over the fixed time `λ⁻¹ log[(1−n_b)/n_b]`. The uniform strong/weak coordinate and reference bound on that interval is an additional hypothesis. Small core radius does not by itself imply weak angular condensation, selected-orbit matching, or WIT's full population distance.

Sources: LOC `localineq`, `meanineq`, `main`, `late`; prefix `inc:AN03:local:v1:`.

### 7.3 Conditional joint powers — retain every q cost

At **one common chart-valid entry time**, suppose the eventual entry theorem supplies

\[
r_0\le C_s q^{-s_{\rm sh}}S_0^{\beta_{\rm sh}},\qquad
N_0\ge c_wq^{s_{\rm seed}}S_0^{\gamma_{\rm seed}},
\]

with positive C_s,c_w independent of q,S₀ and with LOC's mean, forcing, smallness, and later-continuation requirements satisfied uniformly. Passage then costs

\[
q^{-s_{\rm sh}-s_{\rm seed}\alpha/\lambda}
S_0^{\beta_{\rm sh}-\gamma_{\rm seed}\alpha/\lambda}.
\]

For S₀=q^κ, the strict algebraic test is

\[
\kappa(\beta_{\rm sh}-\gamma_{\rm seed}\alpha/\lambda)
-s_{\rm sh}-s_{\rm seed}\alpha/\lambda>0.
\tag{joint-test}
\]

With the **candidate, not initialized-proved**, powers

\[
\beta_{\rm sh}=1/2-\alpha,\quad\gamma_{\rm seed}=1-\lambda,\quad
s_{\rm sh}=\frac{1-2\alpha}{1-\lambda},\quad s_{\rm seed}=0,
\]

this becomes

\[
E_{\rm loc}(\rho,\kappa)=\frac\kappa2(1-P)-\frac{1-\lambda P}{1-\lambda}.
\]

LOC proves that on `ρ∈[13/20,7/10]`, κ=15/2 yields

\[
E_{\rm loc}>\frac{4193}{51000}>0,\qquad
\frac2\lambda<\frac{15}{2}<\frac2{\lambda(1-\lambda)}.
\]

This is a nonempty **algebraic matching window**. It is not an A regime. The dominant weak ancestry may be in transit, not in a fixed weak chart, at the strong-learning clock. Prove a later common clock and count its seed, shape, angular, forcing, and q costs before applying the test.

At λ=4/9, the older heuristic window `(6.5,11.7)` must not be treated as a theorem. The now-proved target-only coefficients 4.5/8.1/11.7 do not prove trained-flow nonabsorption, retention, or a sharp admissible boundary.

---

## 8. Signed amplitude retention: proved identities versus proposed clock closure

### 8.1 Checked SGWR identities

For a fixed initial-label set C,

\[
r_\alpha=(\log m_\alpha)'=2b_\alpha^TR(\theta_\alpha)a_\alpha.
\]

With `dπ_a=mα(τ_a)1_C dλ₀/N_C(τ_a)`,

\[
N_C(\tau_b)=N_C(\tau_a)\int e^{\int_{\tau_a}^{\tau_b}r_\alpha}\,d\pi_a
\ge N_C(\tau_a)e^{\int\!\int r_\alpha\,d\pi_a}.
\]

The exact log-mass identity instead integrates the current-mass-weighted average rate. The old negative-budget estimate remains valid but throws away the growth that creates the seed.

Define the weak amplitude

\[
z_\alpha=(U_{\alpha,2}+W_{\alpha,2})/2,\quad
h_\alpha=z_\alpha^2=m_\alpha\chi_\alpha^2\le m_\alpha,
\quad\chi_\alpha=(a_{\alpha,2}+b_{\alpha,2})/2.
\]

Initially

\[
H_C(0)=\int_Ch_\alpha(0)d\lambda_0
=S_0\int_C\sin^2\alpha_0\,d\lambda_0,
\quad H_{Q2}(0)=S_0/8.
\]

For the exact split

\[
R=\frac\lambda2(1-c_{\rm cmp})e_2e_2^T+\mathcal B_\alpha,
\]

SGWR proves, while χ>0,

\[
(\log h_\alpha)'=\lambda(1-c_{\rm cmp})+\varepsilon_\alpha,
\]
\[
\varepsilon_\alpha=2\mathcal B_{22}
+\frac{\mathcal B_{12}W_1+\mathcal B_{21}U_1}{z_\alpha}.
\tag{amplitude}
\]

`B11` is absent **from this algebraic rate**. It may still affect other coordinates and future defects through the coupled dynamics. If χ≥k>0, `|εα|≤2||Bα||/k`. Signed averaging yields a stronger cohort estimate than discarding all positive corrections. Persistent U=W is not assumed.

SGWR also proves the rank-one comparison ancestry formula and frozen resident contraction. The frozen contraction is not an original-flow transit/capture theorem; in particular a changed mass factor or unbounded scaled coordinate requires a new bound.

Sources: SGWR `jensen`, `ampflow`, `ampcohort`, `gaussiandefect`, `contraction`; prefix `inc:SGWR:v1:`.

### 8.2 Proposed exact-response normalization (not yet a closed clock theorem)

The user proposes choosing

\[
c_q(\tau)=\mathsf m_2(\tau)
=\frac{\mathbb E_{P_2}[X_2f_2(X)]}{\lambda+q^2}
\]

and the comparison matrix

\[
\frac{\lambda+q^2}{2}(1-c_q)e_2e_2^T.
\]

Rewriting the amplitude identity with this chosen coefficient is algebraic. The hard conclusions are not: positivity/control of χ through transit, integrated entrywise defect bounds, response-versus-cohort lower bounds, imbalance control, and existence/matching of the response half-learning clock.

The empirical report finds H_Q2 close to

\[
H_{Q2}(0)\exp\left((\lambda+q^2)\int(1-c_q)\right)
\]

with a small positive correction in sampled runs. That is a useful candidate inequality, not a proof of zero retention loss or a uniform sign for every label.

A potential closure would establish, with explicitly bounded errors,

\[
c_q\ge\int_CU_2W_2\,d\lambda_0-\epsilon_{\rm rest},
\quad U_2W_2=h_\alpha-[(U_2-W_2)/2]^2,
\]

together with imbalance and signed-defect estimates. Only then could H_C bound the integrated `(1−c_q)` clock and replace some separate seed/phase estimates. Do not assert the inequality for arbitrary states: omitted labels and output signs matter. The relevant c_q range must itself be established; an exact response is not automatically in [0,1].

The proposed ideal bound at c_q=1/2 has main term `log(4/S₀)` for C=Q2. Until the errors, weights, signs, captured fraction, and clock existence are proved, this is a target, not an available AN03 substitution.

### 8.3 Guard and outer-chart obligations

The large cluster-1 B11 does not enter (amplitude), so entrywise estimates may be far better than the old full-matrix norm bound. But O(q) off-diagonal forcing is not automatically integrable to a useful constant over a logarithmically long delay. Favorable signs must be proved, not taken from the pilot.

A compact-Q2 guard `χ≥k` can fail during the return transit unless controlled. A parameter-dependent guard such as `χ≥q^ε` adds an explicit q cost. Retained amplitude is not the same as weak-chart radial mass or the selected weak angular law.

The user's suggested extension to an outer chart `|u|≤δ₀/q` is a proposal requiring uniform remainders and appropriate norms. Small physical angle qu does not by itself make every scaled field residual small relative to a cancellation or near a zero. The newly supplied Q2 paper proves specific outer target-only estimates and left-facing original-flow bounds; it does not yet prove the proposed amplitude-clock theorem through Q1 return.

A single coupled proof can use amplitude estimates and localized Q2 tracking together. Do not force an artificial choice between them, but do not replace the leading logistic N law by the exact response c_q inside LOC/RET2 without deriving all additional terms.

---

## 9. Still-essential mechanism correction: exact finite-noise lag and a non-small inactive bridge

### 9.1 Keep the cancellation-defining observable exact

There are three different quantities:

\[
L_0=Y+K_w,
\]

\[
L_{1,q}^{\rm mean}=\frac{\mathbb E_{P_1}f_2(X)}q,
\]

\[
r_{21}=\frac{\mathbb E_{P_1}[X_1(f_2(X)-X_2)]}{1+q^2}.
\]

The first belongs to the leading model; the other two are exact finite-noise observables. Gaussian integration gives

\[
L_{1,q}^{\rm mean}=\int b_2 K(a_1/q)\,d\nu,
\]

and the exact Stein relation is

\[
\frac{1+q^2}{q}r_{21}
=L_{1,q}^{\rm mean}+q\mathbb E_{P_1}[\partial_1f_2(X)].
\]

They are not interchangeable names for the same lag. The helpful product can be built with either appropriate exact observable, but its change of coordinates and all geometric/rate errors must be retained.

On scaled charts,

\[
\begin{aligned}
L_{1,q}^{\rm mean}={}&
\int_s\sin(qy)K(\cos(qx)/q)\,d\mu_s\\
&+\int_w\cos(qv)K(\sin(qu)/q)\,d\mu_w+L_{\rm outside}.
\end{aligned}
\]

An exact bound on its difference from `L₀` is

\[
\begin{aligned}
|L_{1,q}^{\rm mean}-L_0|\le{}&
q^2\int_s\left(\frac{|y|^3}{6}+\frac{|y|x^2}{2}\right)d\mu_s\\
&+q^2\int_w\left(\frac{v^2K(u)}2+\frac{|u|^3}{6}\right)d\mu_w\\
&+\int_s|\sin(qy)|[K(\cos(qx)/q)-\cos(qx)/q]d\mu_s
+|L_{\rm outside}|.
\end{aligned}
\]

See `pa:Lex` and `pa:lagerror`. A generic `O(q²)` error with a large high-moment coefficient can overwhelm a small lag. A canonical theorem may need an exact finite-`q` lag differential inequality rather than a coarse transfer from `L₀`.

The empirical relation using the exact lag is approximately

\[
\frac{D_1^{\rm phys}}{\mu_1^2q^2}
\approx-\tfrac12 A_{q,\xi}L_{1,q}^{\rm mean}.
\]

It is **not an exact finite-noise identity without a remainder**. AN1 must define the exposure precisely, derive the remainder, and prove it is smaller than the lag-dependent margin. The scaled population law at `M=1` remains exactly true in its own scope.

### 9.2 The bridge has analytical instantaneous forcing signs

At a fixed state of the leading model, move strong mass `ε` from `(r₀,s₀)` to `(r_B,s_B)` with `r_B≥r₀`, `s_B≥s₀`, holding total strong mass and weak measure fixed. At a fixed strong receiver `(x,y)`,

\[
\Delta x'=-\tfrac{\epsilon\rho}{2}
[F(\rho x,\rho r_B)-F(\rho x,\rho r_0)]\le0,
\]

\[
\Delta y'=-\tfrac\epsilon2(s_B-s_0)\le0.
\]

If the receiver lies below both donor inputs, this becomes

\[
\Delta x'=-\tfrac{\epsilon\lambda}{2}(r_B-r_0)\Phi(\rho x).
\]

There is no small donor displacement assumption. These are the exposure push and the added output-compensation forcing. But weak receivers also change:

\[
\Delta u'=-\tfrac\epsilon2(s_B-s_0)\Phi(u),
\quad
\Delta v'=\tfrac{\epsilon\rho}{2}[K(\rho r_B)-K(\rho r_0)].
\]

The resulting change in weak compensation feeds back into the strong field. Therefore a global trajectory comparison requires a **coupled inequality system**, not just the instantaneous signs. See `pa:bridge-force`.

### 9.3 Ordering is not a shortcut to comparing different populations

Within a common leading field,

\[
\partial_yx'=\partial_xy'=\tfrac\lambda2(1-N)\Phi(\rho x)\ge0,
\]

so two ordered strong characteristics remain ordered. However, donor couplings between distinct strong atoms are

\[
\partial_{x_j}x_i'=-\tfrac{\lambda m_j}{2}\Phi(\rho\min(x_i,x_j))<0,
\quad \partial_{y_j}y_i'=-m_j/2<0.
\]

Thus the full particle/population evolution is not cooperative in all its coordinates. Comparing a main block with a two-atom run means comparing different residual fields and needs additional control.

At exact finite noise, holding the residual field fixed,

\[
\partial_\psi\theta'=\partial_\theta\psi'
=(b^\perp)^\top R(\theta)a^\perp.
\]

The equality follows from `R′(θ)a=0`. Its positivity on a reached regime is still an obligation. Ordered or approximately ordered entry should be proved from the relevant initialized labels, not taken from a plot.

---

## 10. The two additions: completed limiting/linear content and the exact remaining dependency

### 10.1 Linear contrast — done under its stated assumptions

LP extends F's P10. Let the identity-activation two-layer network have aligned labels, diagonal positive initial Gram `G₀=diag(c_r)` with `0<c_r<1`, and diagonal positive data moment `A=diag(a_r)`. Then

\[
\ell_r'=2a_r\ell_r(1-\ell_r),\qquad
\ell_r(\tau)=\frac{1}{1+(c_r^{-1}-1)e^{-2a_r\tau}},
\]
\[
U_\alpha=W_\alpha=T(\tau)U_\alpha(0),\quad
T_{rr}=\sqrt{\ell_r/c_r},\quad M(\tau)=\operatorname{diag}(\ell_r).
\]

For every nonzero probe,

\[
E_\xi'=-2\sum_r a_r\ell_r(1-\ell_r)^2\xi_r^2<0,
\qquad E_\xi=E_{-\xi}.
\]

If **every weighted cluster moment** `mathsf A_p=π_p E_p[XXᵀ]` is diagonal in the same basis,

\[
D_p^\tau=-2\sum_r(\mathsf A_p)_{rr}\ell_r(1-\ell_r)^2\xi_r^2\le0.
\]

Diagonal total A alone does not imply the sourcewise signs: LP's exact counterexample has `D₁=433/5000>0` on an actual aligned diagonal trajectory. With raw unweighted cluster moments the mixture factor must be inserted; do not mix the conventions.

For the isotropic planar continuum `G₀=S₀I/2`. Positive-quadrant initialization gives `S₀[[1/2,1/π],[1/π,1/2]]`, leaving the commuting class. This supplies minor entries, not a general theorem of Swing-by for every parameter choice. Finite width is covered when the Gram is **exactly** diagonal, not merely close in expectation.

**Remaining:** present this as an extension of P10. Optional random finite-width/sample perturbation bounds are not proved and do not automatically certify a `10⁻⁵` rise threshold from an O(1/√h) scaling. No new linear proof work is required for initialized ReLU A.

Sources: F P10; LP `inc:LP:v1:linear-theorem` and its sourcewise counterexample. The user explicitly checked the derivation by hand.

### 10.2 WIT learned limiting witnesses — done in the leading scope

On `ρ∈[13/20,7/10]`, WIT proves for s≤0

\[
x<3/4,\quad v-y\le8/5,\quad\Phi(\rho x)\le71/100,
\quad y'\le-\frac5{124}n(1-n).
\]

The exact coherent error then satisfies

\[
\mathcal E_\zeta'\le\frac{3479}{31250}n^2
-\frac5{124}(\zeta-3/4)n(1-n).
\]

At fixed n₀≤1/2, descent follows if

\[
\zeta>\frac34+\frac{215698}{78125}\frac{n_0}{1-n_0}.
\]

For quarter-mass,

\[
\mathcal E_\zeta'(-\log3/\rho^2)
\le-\frac{65333}{124000000}<-1/2000
\quad\text{on }\zeta\in[87/50,7/4].
\]

That interval includes the **exact** canonical scaled offset `5π/9`, not just rounded 1.745. WIT builds a smaller nonempty rectangle P* about `(2/3,5π/9)`, positive analytical source/total-rate margins, and common centered windows J,J₋,J₊. The crossover is after quarter-mass; no half-mass lower bound on its time is claimed at this offset. The half-mass descent result for ζ∈[4,5] is separate.

WIT's gate-aware moment-distance theorem conditionally transfers those witnesses to a sufficiently close **leading** population. It includes all masses and both angles of both families. A non-small bridge cannot be hidden in its small tolerance: `d≥m_B|ȳ_B−Y_ref|`. A bound on core spread alone does not meet it.

Static learning in a fully charted exact state obeys

\[
|\mathsf m_p-M_p|\le25qR,\qquad
\sqrt{2\mathcal L_p}\le|1-M_p|\sqrt{Q_p}+17qR.
\]

With the supplied mass/noise slack it gives `mathsf m₁≥1/2`, `mathsf m₂≥1/4`, and `L_p≤169 L_p(0)/196`. These conservative sufficient bounds do not cover q=.05. REV extends them by the explicit L² background output, but supplies no dynamical estimate for that background.

Sources: WIT labels `familytheorem`, `quarterrate`, `uniformtheorem`, `populationtransfer`, `clockalignment`, `staticproposition`; prefix `inc:AN06:v2:`.

### 10.3 Limiting permanence — done; original-network transfer not yet done

On the selected coherent orbit, for every fixed `0<ρ<1`, LP proves

\[
x(s)\to+\infty,
\qquad \mathcal E_\zeta(s)=0\quad(s\ge S_\zeta)
\]

for each finite offset ζ, with a common clearing time on compact parameter sets and bounded offset intervals. The proof combines arbitrary-level hitting with finite total downward variation. It does not assert no re-entry immediately after the first hit.

LP additionally proves `x=O(sqrt(log(2+s)))` and eventual x'>0. LPR proves the weak-coordinate analogue in the full five-dimensional orbit, retaining 1−n terms, and hence

\[
\max\{|x|,|y|,|u|,|v|\}=O(\sqrt{\log(2+s)}).
\]

These are limiting-system claims; they do not permit s→∞ at fixed q under a bounded-chart expansion. Limiting zero is the zero of `(E−1/2)/q²`, not zero original network loss.

**LPR Theorem 2.1 combines the results:** on WIT's P*, leading strong mass is 1, weak mass is bounded above 1/4 on J, the source signs and total-rate windows hold, decrease/rebound is at least `3γ₀r/8`, and one common S gives zero scaled benefit thereafter. This combined learned theorem has WIT's ratio/offset scope, not all ρ∈(0,1). Permanence alone has the larger pointwise ratio range.

LP's analytical diagonal-transfer implication, LPR's scalar saturated-mass damping, and the weak/strong growth results are complete **as their displayed statements** and checked by the user. Their hypotheses involving the original flow remain hypotheses.

Sources: LP `permanence`, `monotonic-theorem`, `uniform-clear`, `diagonal-transfer`; LPR `combinedtheorem` and Proposition 3.1/Corollary 3.2/Lemma 4.1. Consult the actual label for a new citation rather than inventing one.

### 10.4 What remains beyond these additions

- **Required for initialized persistence:** A-error-transfer on every fixed centered late window including background, as now specified in Section 3.2 and AN7. It is not a new independent permanence proof once that premise holds.
- **Optional quantitative horizon:** geometric chart validity needs `q sqrt(log(2+T_q))→0`, but this does not imply dynamical approximation. A bound Cq²T only allows vanishing errors when q²T_q→0, not T_q≈q⁻². Total mass can be damped; relative label weights/angular errors require separate control.
- **Optional broad-population permanence:** a coherent clearing theorem does not prove eventual clearance or rate of lost benefit for a finite-spread distribution. This can remain empirical for a first theorem.
- **Background control:** there is no exactly dead Gaussian sector at q>0. Proving some fixed ancestry remains nearly inert is an independent estimate, not an available fact. Complete removal of all background labels is impossible at finite time under the angular surjectivity result. Do not call an unproved background lemma “easy” or assume mass≤CS₀ automatically.

---

## 11. Updated dependency-ordered lemma roadmap

The roadmap identifiers AN0–AN9 are work packages, not an instruction to finish all variants sequentially. Prefixes such as AN02 and AN03 in supplied filenames refer to increments within those packages.

### AN0 — Interfaces, versions, and status (available)

Use F and P plus the later increments with their actual scope. RET2 replaces RET1's repaired proofs/discussion. LOC is a new theorem, not a relabeling of RET2. Q2's comparison profiles are not original trained profiles. LP/LPR are finished at their limiting/linear scope.

**Immediate audit:** before applying LOC, read its exact smallness conditions and identify the variables in the intended original-flow entry theorem. Do not spend an increment expanding unrelated foundations.

### AN1 — Exact finite-noise signed lag and source-rate closure (open)

**Available:** P's exact projection, rate decomposition, finite-q mean-lag formula, Stein relation, and limiting population positive-lag law. Empirical exposure×exact-lag agreement motivates the variable.

**Required:** an original-flow positive-lag/tracking estimate and a source-resolved remainder bound below that lag's signed margin. Retain all derivative channels and all labels. Upper bounds on absolute lag or total training loss are not positive-sign estimates.

**Unlocks:** original cluster-1 help, mechanistic B, and improved rate transfer. Can be developed in parallel with entry.

### AN2 — Original initialized ancestry → transit/return → common chart entry (central open connection)

**Available sublemmas:** ARR's reservoir; TAIL/RET2 positive-coordinate Q2 amplification; Q2's exact comparison density/profile and target-only clocks; Q2's localized original left-facing estimate; SGWR signed amplitude identities and frozen attraction; RET2's exact conditional ancestry-to-capture functional.

**What is not available:** a retained seed with a uniform c_w; a common time with weak and strong charts simultaneously valid; joint input/output core shape with the full q-prefactor; weak angular selection; enough control of the full output defect and all outside labels.

**Next recommended proof contract:** from the actual uniform aligned initialization and a specified prospective joint family, construct a fixed ancestry set/core and an analytical common time t₀ such that the following are proved together, not borrowed from different clocks:

\[
0<M(t_0)\le1\ \text{in the leading comparison (with original-flow defect accounted for)},
\quad 0<N_0<n_b,
\]
\[
e_0\le e_*/4,\quad
r_0\le C_s q^{-s_{\rm sh}}S_0^{\beta_{\rm sh}},\quad
N_0\ge c_wq^{s_{\rm seed}}S_0^{\gamma_{\rm seed}},
\]

plus weak-coordinate information, weighted tail/weak feedback budgets sufficient for F_b, and controlled original population outside the charts. If these are quantities of an analytically constructed leading comparison, specify its initialization from the actual flow and the full matching error; do not silently call original family masses exactly logistic.

A useful smaller first increment could bound the time-weighted `||g_t||` in Q2's envelopes on a precisely delimited initialized strong-learning phase, or prove entrywise amplitude and response/imbalance control on a fixed Q2 subset through a rigorously delimited transit. It must unlock an actual entry condition, not merely restate conditional tracking.

For already crossed ancestry, prove a Q1 transit/return estimate under the changed residual. Target-only phase coefficients identify candidate times but do not settle this. A frozen weak root is useful **after** a valid matching argument; it cannot be invoked at u=O(1/q) without a uniform extension.

### AN3 — Nonlinear resident/local passage (substantial conditional progress; initialized use open)

**Now proved in the defined leading system:** RET2 two-sided/mixed-order moment and Riccati passage with a mean budget; LOC local-rate passage with collective reference control and explicit guard closure.

**Remaining for applicability:** supply AN2's entry and joint prefactors, prove F_b satisfies the required small bound, control chart support and later bounded continuation, obtain the weak angular distribution and mean alignment needed for orbit selection, and incorporate original finite-noise perturbations.

The main planned route uses LOC's `N₀^(−α/λ)` amplification. The global RET2 bound remains a useful tool, not an established initialized regime or a theorem of impossibility. Do not double-count strong-learning contraction already included in r₀.

**AN3 output:** a whole leading population sufficiently near the selected weak branch on the half-mass-centered fixed interval, or a non-small controlled split class for AN4, together with explicit outside/matching errors. A small core radius alone is not this output.

### AN4 — Non-small bridge/lag dynamical comparison (open; scope-dependent)

**Available:** exact partial-active error formula; same-field ordering; signed instantaneous bridge displacements; covariance effect at fixed barycentre; small-split response functional.

**Required for canonical enhancement:** coupled evolution of the active core, inactive bridge, weak residual producer, exact lag, and exposure. Retain backreaction. Same-field order does not compare separate self-consistent populations. The bridge is not necessarily a perturbation that meets WIT's coherent tolerance.

For a first initialized small-shape A, full canonical amplitude enhancement may remain empirical/optional. Do not then claim B-bridge or canonical trajectory coverage.

### AN5 — Substantial concept learning (static interface supplied; initialized application open)

WIT gives exact Gaussian state bounds and fixed learning/loss thresholds under fully charted hypotheses; REV adds an explicit L² background budget. They close the former limiting “positive mass but maybe unlearned” gap once their hypotheses hold.

Prove those state/background conditions for the reached original population. Family names, positive ancestry mass, and response-clock regression are not sufficient. No need to improve quarter-mass to half-mass at the canonical scaled offset for the first A.

### AN6 — Learned signed crossover (coherent/nearby limiting interface supplied)

WIT supplies rational quarter-mass descent, a later sign-changing zero, common local parameter/probe/time windows, and a gate-aware leading-population tolerance. LP/LPR add common limiting clearing and combined learned reversal/permanence.

**Remaining:** establish the actual entered population meets the tolerance after centering, or prove a direct split-population rate comparison. Retain the full source decomposition and all residual-producer effects. Do not turn leading source rates into original rates without AN7.

### AN7 — Finite-noise matching and post-learning compact windows (open; expanded contract)

This step must deliver **both A-error-transfer and A-rate-transfer from Section 3.2**, with the same actual initialization and analytically matched clock. In particular:

1. Prove the original-to-leading reduction on the reached state class, not only at selected test states. Keep total/relative mass-rate differences, full residuals, and outside labels.
2. Prove the q-scaled precision required for an O(q²) probe effect. Unscaled o(1) state error is not enough.
3. Control the long initialization/transit delay, including every q² log(1/S₀), q log(1/S₀), or worse term actually generated by the selected norm and signed estimates. A single scale condition is not a proof of entry.
4. Prove exact-response/family-mass/amplitude clock matching. Own-half-mass centering cancels leading logistic phase only. Exact c_q need not be logistic or monotone without proof; moving-family flux belongs in its defect if chart masses are used.
5. For every fixed finite centered interval after matching, prove rescaled **error** convergence with background. Rates need uniform sign-margin accuracy on the gate-separated learned windows; handle gate-hit rates separately rather than assuming nonexistent uniform differentiability.
6. Give uniformity over the final compact rho/offset region. For a sequence S₀(q), explicitly state that sequence and all constraints. To claim an open finite-parameter region or a band of powers, prove that wider uniformity rather than substituting a single formal power.

**Once these premises are proved**, LP's diagonal argument yields some growing late horizon and vanishing error coefficient with no further limiting permanence theorem. A quantitative horizon or broad-split permanence is optional. No original infinite-time conclusion follows merely from the limiting zero.

### AN8 — Final initialized assembly (open)

Combine AN2/AN3 matching, AN5 learning, AN6 strict windows, and AN7 original-rate errors to eliminate every entry hypothesis in A. Derive finite positive rebound by integration and a positive-width off-cone sector. Use the same reached residual inequalities for B.

Then state the initialized persistence corollary under the stronger AN7 error convergence. Make the parameter scope explicit: no current proof covers the canonical `(q,S₀)=(.05,2e−4)` simply because WIT contains the canonical scaled offset.

### AN9 — Optional refinements, not prerequisites

- Analytical sign/uniformity of `κ_enh`; its approximate value 1.75053 is numerical evaluation of a response functional, not a proved decimal coefficient or a broad-bridge law.
- Quantitative growing horizon; finite-width/sample lifting; explicit linear perturbation bound; higher-dimensional or more-concept extension.
- Full non-small split permanence and a rate explaining gradual empirical loss of benefit.
- Exact timing asymptotics beyond the analytically selected crossing and clock matching; uniqueness/transversality of a crossing is not established by its observed shape.
- A near-dead-background estimate on a stated joint finite horizon; no exactly frozen Gaussian tail assumption.

---

## 12. Current empirical evidence — motivation only, with the needed interpretation guards

These entries are user-reported or recorded in previous diagnostic notes. This handoff update did not access the repository, reproduce the pilot, or independently refit the sweeps.

### Architecture and geometry

The reported matched architecture controls support ReLU off-cone reversals versus no above-threshold linear reversals in the tested wide isotropic runs. The compositional probe was essentially monotone, but one preregistered H1 exception must remain a formal failure under its criterion. Positive-quadrant initialization restores compositional Swing-by in the tested controls; do not state that initialization alone is a universal cause of all such dynamics.

P10/LP explain the exact isotropic diagonal **population** control. Finite width and finite sample fluctuations require a perturbation proof before attaching a universal numerical rise threshold.

### Canonical mechanism

The canonical learned window has strong-cluster help and weak-cluster harm carried mostly by strong-family output and input rotation, respectively. Weak-family output shapes the residual despite being directly probe-inactive under the diagnostic mask. The approximately 95%/99.5% attribution and factorization fits are sampled numerical facts, not proof hypotheses.

Use “source = training cluster, carrier = moving neuron population, producer = output shaping the residual.” A split at the mean input angle is not automatically the rate-weighted producer attribution.

The helpful lag collapses through the crossover interval while exposure is relatively steady there; exposure decreases later and input rotation remains the harmful channel. Do not claim every interval is explained mainly by exposure loss.

### Exact lag and non-small bridge

At canonical noise, the exact lag can be a small difference of much larger terms. The leading `Y+K_w` can have a large relative error even when a product using an exact finite-noise lag fits well. Preserve mean versus X₁-weighted lag distinctions.

A non-small inactive bridge mainly affects the active population's exposure and compensation; within-active covariance is not the entire depth enhancement. The small-split coefficient and canonical broad-tail response need different quantitative arguments within the same population model.

### Weak-amplitude report

For fixed Q2 ancestry the user reports H_Q2 close to its `(λ+q²)∫(1−mathsf m₂)` prediction with a positive few-percent integrated correction, including a return transit. This supports pursuing an entrywise signed-amplitude estimate. It does not prove all-label defect positivity, a uniform guard, radial weak-chart capture, or the amplitude/response clock substitution.

The empirical exponent about 0.576 was measured directly from an **instantaneous weak-family mask at strong half-mass**, not inferred from a clock. Do not apply the earlier clock-subtraction criticism to that measurement. It is still not a retained fixed-label seed. Clock fits and the estimated extra loss near 0.006 are additional consistency checks with their own response-versus-mass caveat.

### Timing, depth, and persistence

The reported delay of roughly 1.12–1.15 physical units after weak learning is close to the numerical evaluation about 1.10 of the analytically specified coherent orbit. No source proves those decimals or uniqueness of the crossing. Depth at canonical initialization is several times the coherent limiting value; this is not explained quantitatively by small-shape robustness alone.

E6 establishes persistence **through physical time 100** in the reported finite runs, not infinite-time permanence. LP/LPR establish eventual zero benefit only in the selected leading system. The parameter ratio `log(1/S₀)/log(1/q)` is about 2.8 at the canonical point, but neither its inclusion nor exclusion from a future true initialized regime follows from the candidate `(6.5,11.7)` discussion.

Coordinate energy, radial mass, current masks, fixed ancestry, tangent coordinates, angular coordinates, standard deviations around a mean versus RMS around a median, and snapshot-nearest-crossing versus exact event times are distinct. Keep their definitions when using empirical figures.

---

## 13. Withdrawn claims and shortcuts not to reintroduce

1. **Withdrawn:** positive global exponent proves a compatible initialized joint regime. All entry, q-prefactor, forcing, and smallness hypotheses must coexist at one clock.
2. **Withdrawn:** local passage changes only constants. It changes the weak amplification power and can determine whether joint powers are favorable.
3. **Not proved:** global passage is useless in every regime. The current sources establish no compatible initialized regime, not a universal impossibility theorem.
4. **Not proved:** `(6.5,11.7)` or κ=15/2 is the initialized A window. κ=15/2 is an analytically positive **conditional matching test**; target-only coefficients do not settle trained-flow return or absorption.
5. **Invalid substitution:** count Q2 ancestry mass as captured weak radial mass; multiply the late ARR reservoir by the uniform Q2 amplification; equate a tangent coordinate-energy profile with angular radial mass.
6. **Invalid extension:** use a leading compact-chart field uniformly for u=O(1/q) without new error estimates; continue left-facing tracking after the label moves into Q1.
7. **Not supplied:** replace LOC's full tail first-moment budget by small tail mass, or its small F_b condition by an unspecified O(1) bound; assume small core radius supplies weak-angle/orbit selection.
8. **Invalid differential inference:** an upper radius-growth inequality does not force growth or bound the integral by the endpoint. Use the proved multiplier/Riccati construction.
9. **Invalid comparison:** same-field ordering of two characteristics is not order between two populations with changed residuals.
10. **Not exact:** finite-q help equals exposure times exact lag with no remainder; c_q=N; c_q=H_C; or `U₂²`, `U₂W₂`, and `(U₂+W₂)²/4` are identical after alignment breaks.
11. **Not proved:** empirical positive amplitude corrections eliminate all retention loss uniformly. SGWR identities alone do not control χ, imbalance, or defect integrals.
12. **Not proved:** all original labels enter two compact charts or the Gaussian dead sector is exactly frozen. Retain background and every induced residual/rate effect.
13. **Not proved:** q√log T small establishes dynamical fidelity to T; q²T=O(1) supplies an o(q²) error; saturated total mass necessarily drifts linearly.
14. **Wrong scope:** original infinite-time permanence from E6 or from coherent limiting clearance; no re-entry after the first hit; learned theorem over all 0<ρ<1 rather than WIT's smaller rectangle.
15. **Not automatic:** a rounded numerical crossing, phase boundary, enhancement coefficient, or registry threshold is an analytically proved constant.
16. **Workflow violation:** automatically merge new increments, revise protected files, or access GitHub. Keep work separate for review.

---

## 14. Immediate next deliverable and proof acceptance criteria

### Recommended next increment

A useful title is:

```text
AN02_common_clock_entry_and_signed_amplitude_v1.tex
AN02_common_clock_entry_and_signed_amplitude_v1_review.md
```

This title is a proposal, not a requirement to prove the entire entry theorem in one response. A narrower rigorously closed sublemma is preferable to a long conditional theorem whose key new condition is still assumed.

**Start from the original initialized flow.** Choose a specific missing connection between the proven Q2/SGWR tools and LOC. State a quantitative contract, then prove it. Good targets include a weighted full-output-defect estimate before/through strong saturation, a controlled positive-side transit/return segment, or a fixed-cohort amplitude/imbalance comparison that yields a retained radial fraction and valid chart coordinates at a common time.

For any proposed final entry result, report at one t₀:

- Which labels form the fixed core and weak cohort, and how they were selected analytically.
- Joint input/output core radius and same-field reference error, including exact q costs.
- Radial weak mass and weak angular information, not merely ancestral coordinate energy.
- The weak/tail forcing integral that will meet LOC's explicit threshold.
- All outside-chart mass/output/residual budgets and any family recruitment flux.
- Which clock is used and how it relates to strong saturation, the target-only transit phases, and the later half-learning phase.
- The actual joint regime in which **all** inequalities hold, or the exact remaining condition preventing that conclusion.

If a direct amplitude-clock theorem succeeds, derive the revised passage inequality from the original equations and preserve every induced correction. Do not merely replace N by mathsf m₂ inside a theorem proved for the leading logistic mass law.

### Acceptance standard

A lemma counts as solved only for its actual stated model, hypotheses, and uniformity. A useful conditional tool counts as progress but not initialized closure. Do not report a completed AN2/AN3 or A because a strict power would be positive if unproved matching inputs were true.

The paper's unity comes from the same residual/transport mechanism supplying the learning, signs, and crossover. It does not require a fictitious exact finite-dimensional closure, but it does require every discarded population or term to have a proved budget.

---

## 15. Opening prompt to paste into a new chat

> Read `THEORY_HANDOFF_ANALYTICAL_A_B_v2.md` first. We are proving an analytical unified theory of initialized ReLU SIM reversal, not a computer-assisted certificate. Do not access GitHub, run new experiments by default, or modify the foundations/checkpoint. Deliver each new proof and its review note as separate versioned files for checking before any merge.
>
> The linear contrast and selected-coherent limiting permanence additions are proved and user-checked; do not redo them. WIT provides learned limiting windows at the canonical scaled offset, and LPR combines them with common clearing. Original persistence needs AN7 to prove rescaled error convergence on every fixed centered late window, including background—not only on the crossing windows.
>
> Use the repaired `AN03_two_sided_passage_and_Q2_retention_v2.tex`, the new `AN03_local_rate_mean_tracking_v1.tex`, and `AN02_Q2_profiles_and_localized_tracking_v1.tex`. The old inference of an initialized joint regime from the global exponent has been withdrawn. LOC proves a nonlinear local-rate/collective-mean estimate with explicit entry and forcing hypotheses. κ=15/2 is a positive conditional algebraic matching target, not an established A regime.
>
> The central missing step is a common-clock original-flow entry/retention estimate: convert the actual Q2 ancestry and transit history into retained radial weak mass, a joint strong-core shape bound with its q-prefactor, weak angular selection, and weighted weak/tail/background budgets. SGWR's signed amplitude is an available identity; its exact-response clock closure is still a proposal requiring sign/imbalance/guard estimates. Read only the dependencies needed, identify a precise next sublemma, and begin its analytical proof rather than producing another overview.

## 16. Upload bundles and provenance

**For the next entry/passage chat:** upload this handoff, F, P, TAIL, RET2, LOC, Q2, SGWR, and WIT, preferably with the review notes for the newest increments. Include ARR when its reservoir construction is used. Include REV for the background/surjectivity distinction.

**For the completed additions and final persistence interface:** also upload LP and LPR with their review notes. Their PDFs are optional reading copies. The new chat need not inspect simulation arrays to use the analytical statements.

**Background/history as needed:** the factorization audit, scaled-population note, two-neuron note, SIM.md, main-15, and the old appendix. Do not reconstruct the whole notebook before starting a current quantitative lemma.

### Preparation record

This handoff was prepared by reading the latest uploaded source/review files and the previous analytical checkpoint/handoff. It preserves their terminology and scope; it is not an independent proof audit of all the new increments. The latest user's explicit withdrawal of the AN03 v1 joint-regime inference is incorporated. Prior user-reported hand checks of LP/LPR/SGWR are recorded as review history, not machine verification.

Only new handoff/change-record files were written. No proof source, review increment, foundation, notebook, or checkpoint was edited. No repository was accessed, no trajectory was integrated, and no numerical certificate was used. Source references in this portable file use filenames, theorem numbers, and LaTeX labels instead of conversation-specific citation tokens.
