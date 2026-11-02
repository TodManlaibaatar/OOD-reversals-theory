# AN07 compact-window interface — review note

**Version:** 1, 2 November 2026  
**Companion:** AN07_compact_window_interface_v1.tex  
**New label prefix:** an07cwiv1:  
**Destination:** 07_compact_windows_AN07/  
**Scope:** initialized deep regime, κ = 10, ρ ∈ [13/20, 7/10]; static original-flow results at the proved level t_n, and a separate theorem for P's defined leading population system.

## Result and task status

This is a completed S5a audit, not an initialized compact-window transfer theorem. The leading-system extension closes. The full original probe comparison remains unpaid for specified active cohorts, even at entry. No missing probe inequality is introduced as a hypothesis of a claimed initialized theorem.

| Task | Status | Result / exact remaining obligation |
|---|---|---|
| 1. Interface and time | **Closed as an audit** | All consumer hypotheses are inventoried below. τ_h = t_n + λ⁻¹ log((1−n)/n) is the exact center of WCS's auxiliary logistic mass, not a proved original half-mass hit. Original window continuation and compact-transfer remain open. |
| 2. Static activity | **Closed, with corrected sign scope** | Active iff θ ∈ (qζ−π, qζ) mod 2π; both boundaries have zero activation. Current Q2 inactivity requires ζ ≥ 0, which holds on WIT's rectangle. Q2 ancestry is not current Q2. All G+ are inactive at t_n by the late RCET ratio, including b = π. |
| 3. Precision ledger | **Partial closure; exact gaps delivered** | Core self-error and self-source rates have error O_n(q^(2+1/20)) + O(q⁴); G+ contribute zero directly; Q3 interior and frozen zones are paid. For T = Σ ∪ B the remaining static condition is exactly Q_T = o(q²), with Q_T defined below. The same condition suffices for source rates under the proved passage bounds. Strong complement, possible lower-side Σ, π inner strip and J_3 are unpaid by the cited estimates. |
| 4. Leading-system extension | **Closed** | WIT's constants 64R²(1+g₀⁻¹), 10R² and exp(64R·duration) remain valid with strong-only compact support and finite first weak moments. A one-sided weak receiver estimate replaces the invalid global absolute Lipschitz bound. No finite-noise continuation is claimed. |
| 5. Handoff | **Closed as an audit** | Exact quantities, norms, precision and intervals are listed below. S5b/S5c must continue the original flow and pay probe precision; S5a does neither. |

The only failed precision approach pursued is the direct use of the existing strong-complement tail, distance envelope and capped gain. Its resulting exponent is explicitly below two at the endpoint ρ = 7/10. This does not disprove the actual desired probe estimate; it identifies the loss in that available majorant. The instructions permit recording this gap and continuing the leading-model task.

## Closed statements and important distinctions

1. **Time conversion (an07cwiv1:time, center, Qtime).** Passage time is normalized τ = μ₁² t_phys. LP's physical center is τ_h/μ₁², so LP and H2 evaluate the same state at (τ_h+s)/μ₁². Source rates obey D_p^phys = μ₁²D_p^τ. The unit probe is unchanged. WCS gives

   \[
   \tau_h=t_0-Q^{-1}\log H_0+o(1),\qquad
   (Q^{-1}-\lambda^{-1})O(\ell)=O(q^2\ell)=o(1).
   \]

   The population's *physical selected mass* N_S is not made logistic by this definition. A leading comparison initialized with N_S(t_n) has its own center shifted by O_n(q^(1/8)); rescaling its initial weak measure by n/N_S(t_n) gives exactly τ_h. Both are comparison constructions. The logit defect of the original mass must still be paid on later windows. A fixed comparison interval starting before s_n also needs matching from a smaller fixed level or a separate earlier-window transfer; the common auxiliary center is unchanged algebraically.

2. **Parameter scope.** The entry audit and model estimates use the full deep ratio box. Common learned windows and LPR's combined result use only WIT's proved rectangle P_* ⊂ [13/20,7/10] × [87/50,7/4], around (2/3,5π/9). No common witness margins on the entire box are asserted. On J, n_ρ ≥ 1/4 + σ/2 > n, so the windows are a fixed time after entry. The time conversion does not move them to a wrong regime, but RB does not provide estimates there.

3. **Activity (an07cwiv1:signs).** The exact identity is a_θ·ξ_q = sin(qζ−θ). For negative ζ the endpoint θ = π is active: −sin(qζ) > 0. Thus a blanket inactivity claim over all bounded signed offsets is false. WIT has ζ > 0, so this does not prevent its use. On the current upper half-circle, only the Q1 segment θ < qζ is active. On current Q3, only θ > π+qζ is active. Current Q4 is active. Ancestry labels may have moved between these regions.

4. **Primary inactivity at entry.** SRR's restated RCET estimate gives U₂ > 0 and

   \[
   q|U_1|/U_2\le C(C_0e^{-b_*(t-t_0)/2}+q^2),\qquad
   e^{-b_*(t_s-t_0)}\le Cq^{597/320}.
   \]

   Hence U·ξ_q/U₂ ≤ Rq|U₁|/U₂ − cos(qζ) < 0 at t_n for all bounded ζ. This covers P_q as well as the selected clock. It uses the proved late ratio rather than a support assertion inferred from W_2.

5. **Endpoint audit.** Both probe-gate endpoints have zero ReLU value. The physical angle π has input −sin(qζ); 3π/2 has input cos(qζ). The initial boundary label b = π is included in RCET's regularized positive-coordinate contract. Overlapping ancestry endpoints can be assigned disjointly for integration, but their pointwise signs are checked independently. No uniform pointwise rate claim is made at a gate-hit atom.

6. **Leading extension (an07cwiv1:rate, propagation, witness).** The actual weak moments may be arbitrarily large, so bounds such as actual K_w ≤ 4R or actual source velocity ≤ 4R cannot be reused. The proof compares donor moments to the bounded coherent reference first. At a weak receiver it uses

   \[
   A'_t(u)=-\tfrac12[(u+Y)\phi(u)+\mathcal W'(u)+\lambda(1-N)]
        \le R+1\le2R
   \]

   for every real u, with nonnegative donors and retained Gaussian factor. This is an upper one-sided derivative bound; an absolute derivative bound is neither proved nor needed. The original WIT rate and propagation constants survive. Strong chart validity remains a stated hypothesis of this *leading-model* theorem, not a claimed original continuation result.

## Full interface table

E = supplied at t_n; P = supplied only on a passage subinterval ending no later than t_b; L = proved leading-model fact; O = open for the original-flow consumer.

| Consumer | Hypotheses, including domain and signs | Where supplied / what remains |
|---|---|---|
| WIT ratebound | Nonnegative finite measures; R ≥ 2; 0 < ρ ≤ 1; M,N ≤ 2; coherent masses 1 and n_* ∈ [0,1]; same ρ and ζ. | **E/L:** WCS for actual K,S masses; selected comparator has the stated masses. Exact original leading-system identification is not inferred. |
| WIT ratebound | Strong and weak supports, and comparison coordinates, in [−R,R]²; bounded offset; strict ζ−X ≥ g₀ > 0. | **E:** core support and atom coordinates; gap on WIT offsets. **O:** fixed weak support. Replaced by finite first moments in an07cwiv1:rate. Reference gap on J is **L**, WIT uniformtheorem. |
| WIT ratebound/generalrates | Correct mass-weighted first moments in both coordinates; exact leading source split; selector convention at x = ζ. | **E:** distance O_n(q^(1/20)). **L:** source definitions and a.e. chain rule. Full original error and source rates need the probe ledger. |
| WIT propagation | Two solutions of P's defined leading system at the same ρ; chart validity throughout [a,b]; masses ≤ 2; logistic reactions; fixed relative weights; regular characteristic solution and finite distance. Any probe/gap restrictions inherited from the cited compact class are those in the preceding rows; they do not enter the propagation proof. | **L:** equations only for the leading comparison; **E:** initial distance. **O:** original continuation and reduction. Current original weights are only approximately proportional, not exactly fixed. New theorem replaces weak support. |
| WIT populationtransfer | P_*; same selected half-mass clock; strong/weak chart validity on J; M,N ≤ 2; sup_J d ≤ ε_* with ε_* = min{1/4, σ/4, p_*/(8C₁), γ₀/(8C₁)}, C₁ = 64R²(1+4/g_*). | **L:** P_*, reference margins, gap g_*/4. **E:** entry metric. **O:** original uniform comparison on J. New corollary allows finite weak first moments instead of compact weak support. |
| WIT populationtransfer | Regular characteristics for a.e. total derivative; selector rates; positive window lengths r/2; n_ρ ≥ 1/4+σ/2; strict source/total margins from uniformtheorem. | **L:** all are properties of the selected leading comparison and regular leading solution. No original source rate is inferred. |
| WIT clockalignment | Exact leading logistic N; 0 < N(τ_a) < 1; same λ; existence on comparison interval and to τ_h if called an actual half-mass hit. | **L/E:** WCS auxiliary logistic and analytical center. The original family's actual half-mass hit is not claimed. |
| WIT clockalignment, perturbed clause | Absolutely continuous mass with 0 < N < 1, N(0)=1/2 and equation with defect r_N; control of ∫r_N/[N(1−N)]. | **O:** original future-window mass law and phase budget. Centering alone is not a substitute. |
| LP diagonal-transfer | Compact offsets and any included compact ratio set; common finite limiting clearing time S; actual initialized positive-noise family S₀(q); analytic physical center. | **L:** clearing from LP/LPR on their parameter set. **E:** S₀=q¹⁰, center τ_h/μ₁². |
| LP compact-transfer | Full original error convergence after dividing by q², uniform on every finite [S,T], with backgrounds and requested parameters; nonnegative original time. | **O:** convergence; **closed:** original time eventually positive because τ_h→∞. Witness-window comparison alone is insufficient. |
| LPR combinedtheorem | Selected coherent leading branch, M=1, own logistic clock, P_*; WIT uniform margins and LP uniform-clear assumptions, including branch continuity and uniform forward growth. | **L:** already established by LPR's proof. This theorem does not claim initialized transfer. Scope remains the smaller rectangle. |
| H2 A-error-transfer | Same initialized family and analytic center, every fixed centered finite interval, uniform final compact ρ/ζ set, full background and any membership flux. | **E:** entry and center. **P:** passage budgets. **O:** continuation and q² precision. Fixed cohorts have no membership flux here. |
| H2 A-rate-transfer | Normalized source rates on the gate-separated learned J; uniform q² precision or errors below exact source/total margins; no unsupported rate convergence through gate-hit atoms. | **O:** original window statement. Entry core rates and outside sufficient conditions are proved here, with passage-only scope. |
| AN7 items 1–6 | Reached-class reduction and reactions; q² probe precision; all delay terms; mass/response/amplitude phase and flux; arbitrary fixed error windows and learned rate windows; uniform parameters and explicit scale family. | Entry and phase are **E**, residual/core/outside bounds **P**. Remaining original continuation and output/rate precision are **O**. No canonical or power-band extension is made. |

## Precision ledger, with exact remaining sizes

For any fixed T set

\[
\mathcal Q_T(\zeta)=\int_T m[\sin(q\zeta-\theta)]_+^2\,d\lambda_0 .
\]

At t_n, G+ is inactive, so the exact remainder is T = Σ ∪ B. With δ_q = Cq(1+ℓ),

\[
E-E_K=-\mathcal Q_T+
O\!\left((q+\delta_q)\sqrt{\mu_T\mathcal Q_T}
                       +\mu_T\mathcal Q_T\right).
\]

Since μ_T(1+ℓ)² → 0, the statement E−E_K = o(q²) is equivalent to Q_T = o(q²), uniformly over the offsets under consideration. This is a noncancelling condition: the leading aligned contribution has the same negative sign for every cohort. That sign does not make a two-sided precision requirement disappear.

| Population/term | Proved size | Required size / status |
|---|---|---|
| Core self-output | q² times selected leading error, with error O_n(q^(2+1/20)) + O(q⁴). | **Paid** at t_n. Uses reached core chart, mass and first-moment errors. |
| Selected S and other primary P_q | Exactly zero output at t_n; strictly probe-inactive. | **Paid** as carriers. Their field/residual contributions remain in core velocities. |
| Σ | Q_Σ ≤ C(q⁵ + q^(Γν)H + q⁴); H ≍ n. | **Open:** Q_Σ = o(q²). Available divided bound is O_n(q^(Γν−2)+q²), with Γν > 3/10, not a >2 margin. |
| Currently upper-half active portion of Σ | Q ≤ Cq²μ_Σ = o(q²). | **Paid.** Exact residual gap is the integral over Σ ∩ {sin θ < 0}. SEP's t₀ chart does not supply a later sign invariant. |
| Strong complement C | Q_C ≤ μ_C ≤ Cq^(1+Δν), Δν > 3/25. | **Open:** Q_C = o(q²); mass-only divided size q^(Δν−1). Refined second-moment test below still fails. |
| Q3 interior | Q ≤ Cq¹⁰. | **Paid:** divided size O(q⁸). |
| π strip | Q ≤ Cq^(1211/800)(1+√logℓ) + Cq¹¹√ℓ. | **Open inner contribution:** divided size O(q^(−389/800)(1+√logℓ)). |
| J_3 inner zone | Q ≤ Cq^(4769/4000)(1+√logℓ). | **Open:** divided size O(q^(−3231/4000)(1+√logℓ)). |
| Frozen middle/outer zones | Q ≤ Cq¹¹√ℓ. | **Paid:** divided size O(q⁹√ℓ). Not counted again in strip totals. |
| Core–B cross output, B square, B misalignment | O(q^(21/10)), O(q^(11/5)), O(q^(21/10)(1+ℓ)). | **Paid.** These crude estimates apply to B, not automatically to Σ. For Σ retain the square-root formula. |

**Strong-complement test and failed inequality (an07cwiv1:tailtest).** From the proved raw entry tail, distance envelope and capped gain,

\[
\mathcal Q_C\le Cq^2\mu_C+
C(\epsilon_h/d_c)^p
\min(1,Ad_c^2)\max(1,Ad_c^2)^{1+\nu},
\quad A=C_{\rm fixed}q^2e^{\beta I}.
\]

The tail calculation splits at A⁻¹ᐟ² and uses p > 2 and p > 2(1+ν); it does **not** silently require p > 4+2ν. With the already justified passage endpoint powers,

\[
\Xi_\nu=p(E-\chi)-R_g-\nu(R_g)_+,\quad
E=5(1-P)-s_{\rm pr},\quad R_g=10(1-\lambda)(1-P)-2-2\chi.
\]

Here s_pr = (1−λP)/(1−λ) is PROFILE's shape exponent, distinct from centered time s; p=3/s_pr, P=Φ(ρa), a=ρK(ρa). The TeX keeps ε_h = √2 A_q^d(1−M₀)^α q^(10d−s_pr) and d_c=c_*q^(χ+kP/2), with α=λP/2, d=1/2−α, k=10(1−λ). M₀ is the moving-overlap strong mass, not the present core mass. These bounded A_q/M₀ factors do not change the missing exponent.

The secondary exponent in the table is exactly Γν = 1−5λ+2λ/(1−λ)−ν[10(1−λ)−2], with 289169/924000 ≤ Γν ≤ 481/1020 < 1/2. Its upper bound follows by differentiating the unpenalized expression and evaluating at λ=49/100. Thus its unsigned energy bound indeed has insufficient probe precision.

The desired strong-complement sufficient exponent inequality is **Ξν > 2 uniformly**. It fails for this majorant: at λ = 49/100, for every P in the proved interval [1/2,153/250], including the model's P_ρ,

\[
\Xi_\nu\le1+B(49/100,1/2)
=2967/1510-9/20=915/604<2.
\]

Here B = p(E−χ)−1−R_g decreases in P at this λ: its derivative has the positive prefactor (1−λ)/[20(1−Pλ)²] times a decreasing bracket whose value at P=1/2 is −8093/200. The exact independent-corner value is also retained in the TeX: Ξν = 54762159/43757500 at (λ,P)=(49/100,153/250). These are algebraic identities/inequalities, not numerical premises. They identify insufficient precision of the bound, not an actual lower bound for Q_C.

**Rate precision (an07cwiv1:exactrate, ratecharge, corerates).** The source output derivative is written exactly with the mixture factor 1/2 included in R^(p). The proved passage cross-residual and loss bounds imply sourcewise bounded diagonal entries and O(q) cross entries for arbitrary receivers. Together with RB alignment,

\[
|\xi_q\cdot\dot f_{T,p}|
\le C[\mathcal Q_T+q^2(1+\ell)^2\mu_T],\qquad
|\dot f_{T,p}|
\le C[\sqrt{\mu_T\mathcal Q_T}+q(1+\ell)\mu_T].
\]

Thus the same unpaid Q_T = o(q²) conditions suffice for entry source-rate precision; Q3 interior and frozen zones are directly paid. These are sufficient bounds, not an equivalence for signed rates.

Core source rates are paid separately. The TeX restates CFA's componentwise P1/P2 expansion, evaluates its **pointwise** majorant using SRR's late primary tail, S2CP energy and RB outside mass, and obtains source velocity remainder O(q^(1/10)) before coherent-state comparison. Source radial errors are O(q²+μ_B). WCS/SRR moments then give the core self-rate error O_n(q^(2+1/20)) + O(q⁴). An integrated c-form budget is never substituted for a pointwise source bound.

## Leading proof audit

The following are the exact replacements for weak compactness:

| Use of compact weak support in WIT's proof | Replacement |
|---|---|
| Bounds on actual K_w and V | Compare moments to bounded U,V_* using K's global 1-Lipschitz property. Do not claim actual moments are bounded independently of distance. |
| Product estimates using actual Y+K_w | Split with bounded actual A and bounded **reference** lag. The resulting d₁ difference costs ≤35R²d. |
| Strong receiver dependence on a large actual weak moment | Change donor moments first, then compare receivers in the bounded **reference** field. |
| Bound on ∂_tF at weak receivers | Use ∂_tF=(r−t)_+φ(t) ≥ 0 inside the one-sided scalar derivative; keep the Gaussian factor. |
| Uniform absolute weak velocity difference | Use Dini bounds for absolute deviations. The scalar derivative is ≤R+1 for all real u, including the lower side; the M−1 terms are bounded by the deviation plus a bounded-reference mass defect. |
| Differentiating weighted first moments | Positive leading measures, fixed relative weights, reactions with absolute value ≤1, and finite-moment linear growth justify truncation/domination. |
| Differentiating probe positive parts | Strong support remains compact. Weak first moments locally bound strong velocities; the same selector/a.e. chain rule applies. Gate-mismatch mass ≤D_s/g₀ includes atoms on the gate. |

The constants are unchanged:

\[
|d_p-d_{p,*}|\le64R^2(1+g_0^{-1})\mathfrak d,\quad
|\mathcal E-\mathcal E_*|\le10R^2\mathfrak d,\quad
\mathfrak d(s)\le e^{64R(s-a)}\mathfrak d(a).
\]

The d₂ calculation in the new proof gives the stricter upper bound (50+2/g₀)R²d. The propagation proof gives D⁺d ≤ (1+40R)d ≤ 64Rd. No weak positivity assumption is needed for these finite-window upper bounds; no weak contraction rate is claimed.

The WIT witness implication therefore retains ε_*, all its mass/source/total-rate margins and the rebound γ₀r/4, with strong-only compact support. It remains a theorem about the defined leading system. It is not a conditional original-flow theorem with missing probe inputs hidden in its statement.

At entry, η_s{d>1} ≤ W₂² and ∫_{d>1}d dη_s ≤ W₂² = O_n(q^(1/10)); current probabilities have the same bounds up to 1+o(1). The whole first moment is O_n(q^(1/20)). The weak tail is retained, not discarded or declared compact.

## Constant order and S5b/S5c handoff

Keep the entire WPT/RB → WBR/MP/SRR/WCS order, including the explicit fixed n. Then fix:

1. The final compact parameter/offset region and the finite centered interval. Common witnesses require P_*.
2. R ≥ 2 containing the strong chart and reference coordinates with slack, and the reference gate gap g₀ on J.
3. Rate constant 64R²(1+g₀⁻¹), unchanged ε_*, and the fixed finite-window propagation factor.
4. q last.

New leading constants depend only on R, g₀ and the existing witness margins. Entry constants may depend on the fixed n and already fixed passage guards. No earlier guard, chart or allowed forcing is enlarged after q is chosen. The A_q bounds enter the already proved clock phase and bounded constants; they do not repair a missing q exponent.

| Stage | Required quantity, interval and precision |
|---|---|
| S5b state continuation | On each fixed [s_n,T], at original normalized time τ_h+s, continue strong chart, masses, weak moments and residual bounds. Prove original-to-leading velocity **and reaction** error in a moment-stable norm, tending to zero with fixed exp(C(T−s_n)) losses. This includes full residual producers and all outside labels. |
| S5b mass/clock | Continue N_S−n_ρ=o(1), or pay the original logit defect with the O_n(q^(1/8)) entry mismatch. Keep the same analytically specified τ_h. Do not replace it by a response hit with only O(1) phase accuracy. |
| S5b weak inactivity | Preserve q|u+ζ|<π/2 or pay any activated weak inputs and source rates. Finite weak first moments in the leading model alone do not ensure exact finite-noise inactivity. |
| S5c output precision | On every fixed centered interval and final parameter/offset set, pay the exact full background remainder at o(q²). Under continued alignment, sufficient conditions are sup Q_(Σ∪B)=o(q²) and sup μ_(Σ∪B)(1+ℓ)²=o(1). The unpaid cohort moments are listed above, including transit labels and both strip sides. |
| Source-rate stage | On the learned gate-separated J, pay projected source output derivatives and cross terms at o(q²), or below fixed witness margins. Continue the matrix/alignment hypotheses of the new rate-charge lemma or replace them with direct bounds. Continue a sourcewise core reduction as well as total-field reduction. |
| H2 / LP | Error convergence is required on every fixed finite centered interval, including all backgrounds; rates only on the specified gate-separated J. LP further needs every finite [S,T] after its limiting clearing time. Physical time is (τ_h+s)/μ₁². The diagonal theorem gives no quantitative growing horizon. |

No continuation, additional outside mass theorem, gate-hit rate transfer, AN8 assembly, S6 or canonical-regime result is claimed.

## Source provenance and validation

Sources were read from the repository in read-only mode, including README and roadmap v1.23. Remote prefix search found no an07cwiv1: collision; local source-prefix checks are repeated before delivery. No GitHub mutation, merge or change to a prior increment was performed. Blob hashes below identify the exact fetched files; they are not asserted to be commit hashes.

The source-only ZIP contains exactly the new TeX and this review note. A scratch PDF is used only for compilation/layout validation and is not the downloadable source substitute.

Validation performed before packaging: TeX compilation and resolved internal references; control-byte scan equivalent to the requested PCRE pattern (with the literal grep command attempted where supported); preservation of the backslash commands rm, tfrac, qquad and text; unique labels; comparison of prior output SHA-256 hashes; and ZIP content verification. No mathematical experiments, interval arithmetic or numerical sign checks are used.

| Repository source | Fetched Git blob SHA |
|---|---|
| [README.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/README.md) | 671964a6d084ae5991407c4f4e593ead1cee7b6a |
| [00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md) | 6a66fc6c44d09b794b957730fb4d98c991e0c5ad |
| [00_roadmap/THEORY_HANDOFF_ANALYTICAL_A_B_v2.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/THEORY_HANDOFF_ANALYTICAL_A_B_v2.md) | decb029fb314e96aae70e5eee68eaa969b6293ce |
| [04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex) | 9e102514ad0a491066a2f9eb8eb86e9a251c2b53 |
| [04_witnesses_persistence/LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/04_witnesses_persistence/LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex) | 4d2744894aae8cfdd524d22d08a91fb3306bab10 |
| [04_witnesses_persistence/LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/04_witnesses_persistence/LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex) | d438e477e893414e1284b072184eb1ce12fe2f74 |
| [01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex) | cb458c933aa043cf0188fd11c46bf4246ffc91d8 |
| [03_passage_AN03/AN03_weak_chart_selection_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_weak_chart_selection_v1.tex) | 01888c1655996ad0c7fb07880bd93fa0be3efa4f |
| [03_passage_AN03/AN03_response_barrier_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_response_barrier_v1.tex) | 5312b5093f3ed4f74063347df31ae5a29155255f |
| [03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex) | f00459b5ca412eb86b0893adb64766e2c10d5590 |
| [03_passage_AN03/AN03_pi_strip_budget_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_pi_strip_budget_v1.tex) | ab8a0a2a028935f5045e53e0066e30afeb69c635 |
| [03_passage_AN03/AN03_late_strip_budget_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_late_strip_budget_v1.tex) | 4d3c0065e3b639c02db87c704a3efcfbb0738190 |
| [03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex) | 1777839da3fa10ebf66e8560f7175678753c39b9 |
| [03_passage_AN03/AN03_S2_closure_package_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_S2_closure_package_v1.tex) | baeb8a7eb1e36ce86319782511b665944be1afda |
| [02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex) | 3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a |
| [03_passage_AN03/AN03_strong_reference_reduction_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_strong_reference_reduction_v1.tex) | 6388f0192b970ebfae8604d7cab89dce37a25cfe |
| [03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex) | a490ea323e45e61c1a58301554b89ad84cb02605 |
| [02_entry_AN02/AN02_secondary_entry_profile_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_secondary_entry_profile_v1.tex) | c7c857ec10b7f7b2cf42d1cdb452c50edc735587 |
| [02_entry_AN02/AN02_Q2_entry_contracts_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_Q2_entry_contracts_v1.tex) | b149537025e130801fc55b9e49c365c158eee17b |
| [03_passage_AN03/AN03_c_form_assembly_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_c_form_assembly_v1.tex) | 341908c228092e9a818d98de3ec26591a1050364 |
