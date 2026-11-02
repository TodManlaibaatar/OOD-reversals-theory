# AN07 finite-window continuation — review note

**Version:** 1, 2 November 2026  
**Companion:** `AN07_finite_window_continuation_v1.tex`  
**Label prefix:** `an07fwcv1:`  
**Destination folder:** `07_compact_windows_AN07/`  
**Regime:** original initialized flow, κ = 10, ρ ∈ [13/20,7/10], q sufficiently small after the existing constant choices and the new fixed window.

## Outcome

The requested finite-window continuation and A-error-transfer close. No new original-flow hypothesis is retained. The argument does **not** extend the passage theorem beyond its response range: it proves new finite-time estimates from the state at t_n.

| Task | Status | Result |
|---|---|---|
| 1. Inventory and early-window corollary | **Closed** | Exact clock conversion and uniform compact-level argument. The static comparison extends to every bounded nonnegative offset range without a probe-gap hypothesis. |
| 2. Post-passage scope audit | **Closed** | Small c_b and E_g are not used in the new value estimates. Physical core mass and signed moments replace the capped mass and positive-part representation. Original weak-input positivity is not continued or assumed. |
| 3. Primitive continuation (A) | **Closed** | Combined transverse energy, O(q) cross residuals, O(qL) alignment, bounded core chart, reached weak chart, primary inactivity, physical mass laws and fixed-cohort mass bounds. |
| 4. Original-to-leading reduction (B) | **Closed** | Core sourcewise value/reaction errors and selected weak value errors; their current-mass-weighted first-moment and reaction-distance norms are O_T(q^(1/10)). |
| 5. Perturbed propagation (C) | **Closed** | The coefficient remains 64R. Current radial weights are differentiated with their actual reactions; weighted reaction defects are included explicitly. The physical selected mass/logit is matched. |
| 6. A-error-transfer (D) | **Closed** | Full original normalized error differs from the selected orbit by O_(T,n,Rζ)(q^(1/20)) on [s_n,T], uniformly over the deep ratio box and bounded nonnegative offsets. Together with the early corollary, this covers every fixed centered window. |
| 7. S5d handoff | **Supplied; rate theorem not asserted** | Sourcewise core reductions, distance, background source charges and phase are available on the window. S5d must assemble them on WIT's exact learned windows and compare errors with its margins. |

There is no failing inequality or unmatched input for A–D. No A-rate-transfer conclusion, AN8 assembly, persistence diagonal argument, S6 result or canonical-regime statement is included.

## The theorem and time convention

Keep WCS's existing fixed level n and the original analytically defined center

\[
\tau_h=t_n+\lambda^{-1}\log\frac{1-n}{n},\qquad
n_\rho(s)=\frac1{1+e^{-\lambda s}},\qquad
s_n(\rho)=\lambda^{-1}\log\frac n{1-n}.
\]

For each fixed T > max_ρ s_n and finite R_ζ, the new theorem gives

\[
\sup_{\rho,\,s_n(\rho)\le s\le T,\,0\le\zeta\le R_\zeta}
\left|q^{-2}\big(E_{\xi_q}(\tau_h+s)-\tfrac12\big)
             -\mathcal E_{\rho,\zeta}(s)\right|
\le C_{T,n,R_\zeta}q^{1/20}\longrightarrow0.
\]

The physical core and selected measures satisfy

\[
\mathfrak d(s)\le e^{64R(s-s_n)}
\left[\mathfrak d(s_n)+\int_{s_n}^s\mathcal R(\tau_h+v)\,dv\right],
\qquad \mathcal R\le C_Tq^{1/10}.
\]

Here M = μ_K and N = μ_S are the actual masses. N is not declared logistic: its exact radial equation proves N′ = λN(1−N) + O_T(q^(1/4)+q²), starting with the proved entry phase. On each fixed window the comparison logistic is bounded away from zero and one; the actual mass has the same property for small q, and its logit difference vanishes.

Physical time is (τ_h+s)/μ₁². LP's physical centering is therefore t_h = τ_h/μ₁². The inherited Q-versus-λ discrepancy over the long entry delay is O(q² log(1/q)) = o(1); no O(1)-accuracy t_b formula is used as a phase.

For the early corollary, set n′ = n_ρ(s). On a fixed compact K below min_ρ s_n, all these levels lie in one compact subset of (0,n]. PSE's uniform entry comparison and the exact identity t_(n′) = τ_h+s apply simultaneously. For a general fixed window, use this level argument on its portion s ≤ s_n(ρ), and the new theorem on the rest. Original times are positive for small q because τ_h → ∞.

## Source and hypothesis matching

The TeX inventory is part of the proof. This table highlights the domain checks that prevent a later-regime assumption from entering the argument.

| Source / calculation | Required hypotheses | Supply and interval |
|---|---|---|
| PSE `levels`, `entry` | Initialized deep regime; the fixed WCS level; compact terminal levels in (0,n]; same auxiliary logistic; q last. The source-rate statement uses WIT's offset range and selector convention. | Used at t_n and for the early compact-level corollary only. |
| WCS `handoff`, CWI `entrydistance` | Reached core and selected weak charts, positive current measures, incoming-law L² selection and its weight conversion, physical mass/phase estimates. | All are proved at t_n. They give the initial current-weight first-moment distance O_n(q^(1/20)). Relative weights are not assumed fixed afterwards. |
| RB/MP/PSE entry budgets | Completed passage, with its proved response sign and original guard closure, at a time ≤ t_b. | Used only at t_n: J_G ≤ Cq², μ_B ≤ q^(11/10), μ_Pq ≤ Cq^(1/4), μ_Σ ≤ Cq^γ*, alignment and probe-sector energy. No stopped theorem is cited on a later interval. |
| Exact flow and loss | Gaussian mixture with its halves, balanced positive radii, finite label measure, normalized time. | Exact Cartesian/radial equations and loss monotonicity on the finite continuation. Bounded matrices give finite-time characteristic existence. |
| PSE primary margin at entry | RB/RCET valid through t_n, including regularized boundary labels and positive primary U₂,W₂. | q|U₁|/U₂ ≤ Cq^(597/640) at t_n; this is converted into a positive sine lower bound and propagated directly. |
| CFA/SRR core value calculations | Compact strong donor and receiver chart, bounded mass/moments, primary P₂ margin, absolute secondary/outside charges. | Newly proved finite-window chart, transverse energy and masses supply these. The value calculation is repeated with physical M and signed K_O. No cap, small response, small weak mass, or CLOCK attraction is used. |
| WCS `IBP`, `P2`, `overlap` | Reached weak chart; positive current donor measure; bounded selected second moment; bounded core chart; exact Gaussian distributions; absolute omitted-population charges. | All supplied anew. The tangent integration by parts remains exact for signed u; Gaussian saturation and overlap bounds are proved on both signs. |
| WCS value remainder | The preceding structural conditions and q·sup(|u|+|v|) → 0. | Re-proved on the new window with q|u|, q|v| ≤ C_Tq^(37/640). Its old u≥0 and small-response theorem is not invoked. |
| CWI leading propagation calculation | Positive measures, M,N≤2, bounded strong support and comparison coordinates, R≥2, 0<ρ≤1, finite weak first moments; leading velocity and reaction formulas. | The first five properties are independently proved. The formulas hold with explicit defects. Their weighted integrals are added to the distance inequality; no direct application to an exact leading solution is claimed. |
| PSE `conditional` | R₁₂=O(q); R₂₂^(1)=O(q²); lower-side Gaussian R₂₂^(2) bound; coordinate alignment O(qL√m); finite masses and a fixed cohort. | All hold on the new interval by the combined transverse energy, loss and exact difference equation. The initial negative-input energy is the proved PSE value at t_n. |
| CWI `split` / `ratecharge` | Exact balanced decomposition; fixed cohorts; inactive primary carriers; bounded core output; sourcewise bounded diagonal and O(q) cross entries; alignment O(qL); selector/a.e. rate convention. | Verified throughout the new interval. The static split needs no source-rate convention. The background rate charge is recorded only as an ingredient. |
| CWI static part of `rate` | M≤2, bounded strong support and atom, bounded offsets. The full rate theorem also assumes ζ−X≥g₀>0. | The energy proof is restated with A_*=(ζ−X)_+. It proves the same 10R² distance bound without the rate-gap hypothesis, including equality at the gate. |
| H2 A-error-transfer | Actual initialized family; all populations included; analytically matched center; every fixed finite window; uniform compact parameters/offsets; nonnegative original time. | Supplied by the main theorem and early-window corollary, in normalized time. |
| LP `compact-transfer` | Same actual family and physical centering, full error convergence on each [S,T], uniform on the chosen compact parameters/offsets. | Supplied for bounded nonnegative offsets. LP's common clearing time and diagonal conclusion are not invoked or re-proved. |

For S5d, WIT's `uniformtheorem` is restricted to its analytically defined rectangle 𝒫_* and its common windows J,J_−,J_+. It supplies n_ρ ≥ 1/4+σ/2 and gap ≥g_*/4 there. CWI's leading rate comparison additionally needs the chart/comparator bound R, masses ≤2, positive measures, finite weak first moments and the selector convention. These are distinct from the present gap-free static theorem. WIT's `populationtransfer` is a leading-system theorem, not a theorem to apply verbatim to original velocities: S5d must include the sourcewise defects before comparing with its tolerance ε_* and margins.

## The new continuation mechanism

Let D = T−min_ρ s_n. Loss gives a conservative matrix norm bound 4, hence

\[
m(t,b)\le e^{8D}m(t_n,b),\qquad
\mu_A(t)\le e^{8D}\mu_A(t_n),\qquad
S_{\rm tot}\le\bar S=3e^{8D}
\]

for every unchanged cohort A. This already propagates the small outside and omitted masses; it does not by itself propagate a scaled chart or a cross residual.

The missing control comes from the combined transverse energy

\[
\mathcal Z=E_K+J_G
=\frac12\int_K(U_2^2+W_2^2)
 +\frac12\int_G(U_1^2+W_1^2).
\]

The exact output energy bounds imply, with 𝒳=‖e₂‖_(P₁)+‖e₁‖_(P₂),

\[
\mathcal X\le C\{q(1+\bar S)+\sqrt{\bar S\mathcal Z}+\mu_B\}.
\]

Differentiating 𝒵 in Cartesian coordinates gives

\[
D^+\mathcal Z\le C\mathcal Z
 +C(q+\mathcal X)\sqrt{\bar S\mathcal Z}
\le C_{\bar S}(\mathcal Z+q^2+\mu_B^2).
\]

Entry has 𝒵=O(q²), and μ_B²≤e^(16D)q^(11/5)≤e^(16D)q². Therefore 𝒵≤C_Tq² and 𝒳≤C_Tq. No primary gate, c sign, weak energy guard, or scaled-chart hypothesis is used to close this inequality.

Consequences are then proved in a non-circular order:

1. The exact Δ equation gives |θ−ψ|≤C_TqL.
2. Exact angular equations near either axis give a bounded scaled core chart and a selected chart |u|+|v|≤C_Tq^(−603/640). Thus q(|u|+|v|)→0 and ∫_S m(u²+v²)≤CJ_S/q²≤C_T.
3. The primary entry ratio implies sinθ≥cq^(43/640). Its exact sine derivative is bounded below by −C sinθ−C_TqL. It stays ≥c_Tq^(43/640)>0, as does sinψ. This proves full P₂ donor gates up to a superpolynomial tail and strict probe inactivity. Endpoint labels are included.
4. Core radial contractions give g_K=1−M+O_T(q²+μ_B). Selected radial contractions give g_S=λ(1−N)+O_T(q^(1/4)+q²r²), r=1+|u|+|v|.
5. Integrating against current weights yields the physical logistic mass comparisons; M,N<3/2 follows independently of the later distance argument.

The first-exit guard constants are twice independent majorants in this order. Every initial guard is strict; continuous integral and supremum quantities cannot attain a first exit because each bound improves its own guard. q is chosen last. No small c_b or E_g guard is continued.

## Remainder ledger and powers

All charges below are pointwise on the new fixed window, unless an integral is displayed. They are not inherited integrated passage allowances.

| Term | New bound / mechanism |
|---|---|
| Core compact Gaussian and trigonometric corrections | O_T(q²) times bounded masses and moments on the reached fixed chart. |
| G transverse terms in the strong field | J_G+q√(E_GJ_G)+q²E_G = O_T(q²); E_G only needs a fixed bound. |
| Primary failed P₂ gate | Margin ≥c_Tq^(−597/640); every polynomially weighted tail is bounded by a fixed polynomial times exp(−c_Tq^(−597/320)). |
| P_q omitted functionals/moments | C(μ_Pq+q^(−1)√(μ_Pq J_Pq)) = O_T(q^(1/8)). No μ_Pq/q estimate is used. |
| Σ omitted functionals and selected moments | C(E_Σ+J_Σ+q^(−1)√(E_ΣJ_Σ)) = O_T(q^(γ*/2)+q²). E_Σ≤μ_Σ≤C_Tq^γ* and J_Σ≤C_Tq² are enough. |
| B | Exact total quadratic-energy cost C(E_B+J_B)/q = Cμ_B/q = O_T(q^(1/10)). This follows from |f_B(X)|≤μ_B|X| and Gaussian matrix moments, not a bounded per-mass scaled field on an unreached chart. |
| Physical core mass | |M−1|≤C_Tq^(11/10). The physical leading equations retain M, so there is no artificial mass-capping remainder. |
| Response replacement | c−N=O_T(q^(1/4)); in a weak velocity its cost is O_T(q^(1/4)r), retained until integration. |
| Selected finite-noise V and K moments | O_T(q²∫_S r³dμ)=O_T(q^(2−p)), p=603/640. |
| Weak receiver value errors | C_T[q^(1/10)+qr+q²r³+q^(1/4)r]. The signed Gaussian saturation prevents a spurious quartic. |
| Integrated weak velocity errors | ∫r²dμ≤C_T, sup r≤C_Tq^(−p), so q∫r+q²∫r³≤C_T(q+q^(677/640)). Together with omitted terms this is O_T(q^(1/10)). |
| Weak reaction times distance | (1+d_w)|ε_S| integrates to C_T(q^(1/4)∫r+q²∫r³)=o(1). This term is necessary when using current weights. |
| Background probe moment | PSE conditional energy gives Q_(Σ∪B)≤C_Tq²[q⁸+L²q^γ*], γ*=289169/924000. All current-angle slices and transit labels are included. |

The weak signed extension uses |sin(qu)/q−u|≤q²|u|³/6 and the Gaussian factor along the segment between u and sin(qu)/q. Both have the same sign and comparable magnitude. Thus the Φ and φ errors are O(q²) for either sign, while the K error is O(q²|u|³). No growth term is rejected before retaining its Gaussian factor.

Integration by parts is only in the rotated normal variable perpendicular to the receiver input. The receiver gate is independent of that variable. The overlap estimate is valid for signed receiver and donor coordinates and uses the actual mass-weighted second moment.

## Propagation and probe precision audit

The original family is not treated as an exact leading-system solution. Its core and selected weak velocities equal the leading formulas plus ε_s,ε_w, and its radial reactions equal 1−M and λ(1−N) plus ε_K,ε_S. The forcing norm is

\[
\mathcal R=
\int_K\{|\varepsilon_s|_1+(1+d_s)|\epsilon_K|\}\,d\mu
+\int_S\{|\varepsilon_w|_1+(1+d_w)|\epsilon_S|\}\,d\mu.
\]

The displayed remainder ledger proves 𝓡≤C_Tq^(1/10). In particular, a small integral of the unweighted reaction error alone is not substituted for the reaction-distance term.

CWI's one-sided weak derivative bound is valid for every real u because the donor measure is positive and

\[
\mathcal W'(u)=\phi(u)\int(\widetilde u-u)_+\,d\mu\ge0.
\]

With bounded strong moments and M,N≤2, it gives the same leading distance coefficient. Differentiating the original current-weight integrals adds exactly the weighted reaction terms above. Thus D⁺𝔡≤64R𝔡+𝓡, including both mass differences. No derivative of a value-only weight-ratio estimate is taken.

For the observable, primary labels remain strictly inactive, so f=f_K+f_(Σ∪B). The exact CWI split, all misalignment and cross terms included, is paid by PSE's continued negative-input energy. The core expansion uses positive parts and is valid at a gate-hit atom. Replacing A_* by (ζ−X)_+ in the static comparison proves the 10R² distance estimate without a gap assumption. This is why A-error-transfer covers all bounded nonnegative offsets, while rate transfer still needs the separate gate-separated window audit.

Finally, γ*>1/20 gives

\[
q^{-1/20}\{q^8+L^2q^{\gamma_*}\}\to0,
\]

so the full background is smaller than the inherited q^(1/20) entry error. No one-signed contribution is discarded because of its sign.

## Constants and S5d handoff

The fixed order is the existing WPT/RB → WBR/MP/SRR/WCS order, then n as already fixed, followed by

\[
(T,R_\zeta,D)\to\bar S\to
C_Z,C_X,C_\Delta,R_A,A_D\to R\to C_{\rm red},C_{\rm bg}\to q.
\]

R covers the original core, the selected leading comparator on the fixed horizon and the offsets. The leading comparator bound follows from its displayed linear-growth differential inequality, not a saved trajectory. Every new constant is fixed independently of q; it may depend on the fixed horizon. No uniformity as T→∞ is claimed, and no explicit growing horizon is produced.

| S5d item | Supplied now | Remaining action |
|---|---|---|
| Same parameter and phase | Current physical masses and first moments, with 𝔡=O_T(q^(1/20)); exact τ_h and physical-time conversion. | Use the same center on WIT's J; do not re-center at an approximate passage hit. |
| Strong source velocities and reactions | Pointwise sourcewise core velocity defects O_T(q^(1/10)); reaction defects O_T(q²+μ_B). Full residual producers are included. | Differentiate the probe observable on the gate-separated windows and keep the source normalization. |
| Leading rates | CWI's finite-first-moment rate robustness is available with coefficient 64R²(1+g₀^(−1)). | Use g₀=g_*/4 and WIT's precise 𝒫_* and J. Compare resulting errors with p_* and γ₀. |
| Background rates | Continued sourcewise matrix values, alignment and Q_(Σ∪B) pay CWI `ratecharge`; the relevant projected charge is O_T(q²ε_bg). | Include all cross terms in the complete source-rate calculation, retaining its selector/a.e. convention away from the learned windows. |
| Primary direct carriers | Strictly inactive throughout the fixed window. | They remain in the training residual; do not remove them from the field. |
| Static error / persistence input | H2 A-error-transfer on every fixed window and LP `compact-transfer` on bounded nonnegative offsets. | S5d/AN8 may assemble the already proved limiting witnesses and persistence implications. That assembly is not done here. |

All analytic inputs for the finite-window source calculation are supplied; the A-rate-transfer conclusion itself is deliberately left to S5d. No additional unmatched inequality remains within the present A–D scope.

## Provenance and delivery validation

README, roadmap v1.25 and the cited source files were fetched read-only from the updated repository. The prefix was searched in the repository and checked locally for collisions. This table records Git **blob** hashes rather than commit hashes.

| Read-only source | Git blob SHA |
|---|---|
| [README.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/README.md) | `ad1d108a1d41471dd05ab9795940b415655f67f6` |
| [00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md) | `af479cbe7a048076ed8f3665fb17468125b87067` |
| [07_compact_windows_AN07/AN07_probe_sector_energy_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/07_compact_windows_AN07/AN07_probe_sector_energy_v1.tex) | `4e90dfeb1bb2d75ea9c0711dfaabb15a266ff1b1` |
| [07_compact_windows_AN07/AN07_compact_window_interface_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/07_compact_windows_AN07/AN07_compact_window_interface_v1.tex) | `0902c80583eabb6bc0908ffb64a396633654ae19` |
| [03_passage_AN03/AN03_weak_chart_selection_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_weak_chart_selection_v1.tex) | `01888c1655996ad0c7fb07880bd93fa0be3efa4f` |
| [03_passage_AN03/AN03_strong_reference_reduction_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_strong_reference_reduction_v1.tex) | `6388f0192b970ebfae8604d7cab89dce37a25cfe` |
| [01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex) | `cb458c933aa043cf0188fd11c46bf4246ffc91d8` |
| [03_passage_AN03/AN03_c_form_assembly_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_c_form_assembly_v1.tex) | `341908c228092e9a818d98de3ec26591a1050364` |
| [03_passage_AN03/AN03_matching_package_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_matching_package_v1.tex) | `9491bba4ec10f79acca277b1f0c4ddd92180a7aa` |
| [03_passage_AN03/AN03_weak_boundary_return_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_weak_boundary_return_v1.tex) | `c1f18203cc99ca5ddcda9481ca1281d7debffa9a` |
| [03_passage_AN03/AN03_response_barrier_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_response_barrier_v1.tex) | `5312b5093f3ed4f74063347df31ae5a29155255f` |
| [04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex) | `9e102514ad0a491066a2f9eb8eb86e9a251c2b53` |
| [04_witnesses_persistence/LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/04_witnesses_persistence/LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex) | `4d2744894aae8cfdd524d22d08a91fb3306bab10` |
| [00_roadmap/THEORY_HANDOFF_ANALYTICAL_A_B_v2.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/THEORY_HANDOFF_ANALYTICAL_A_B_v2.md) | `decb029fb314e96aae70e5eee68eaa969b6293ce` |

Validation completed before delivery:

- Two final LaTeX passes compiled the 11-page document without warnings, overfull boxes or unresolved references. Rendered proof, inventory and handoff pages were inspected.
- All 39 internal labels are unique, use `an07fwcv1:`, and every internal reference resolves. The prefix has no match in the fetched prior sources or the repository search.
- Both requested regular-expression scans returned no matches using PCRE2 and an independent Python check. The literal `grep -nP` commands were attempted; this macOS `grep` does not support `-P`, so the identical patterns were run with `rg --pcre2`. No control bytes or bare `quad`/`qquad` tokens remain.
- Literal `\rm`, `\tfrac`, `\qquad` and `\text` are intact.
- All 88 pre-existing output files retain their original SHA-256 hashes. No prior increment, foundation, checkpoint or README was changed; no GitHub mutation or experiment was performed.
- The source ZIP contains exactly the raw `.tex` and this `_review.md`, with byte-identical contents. The compiled PDF is scratch validation only and is not included.

