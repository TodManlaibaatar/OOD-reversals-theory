# AN07 probe-sector energy — review note

**Version:** 1, 2 November 2026  
**Companion:** AN07_probe_sector_energy_v1.tex  
**New label prefix:** an07psev1:  
**Folder:** 07_compact_windows_AN07/  
**Regime:** original initialized flow, κ = 10, ρ ∈ [13/20,7/10], sufficiently small q in the unchanged WPT/RB and WCS constant order.

## Result and status

All requested estimates through t_b close from the proved sources. No additional original-flow hypothesis is retained on that interval.

| Task | Status | Result |
|---|---|---|
| 1. Inventory | **Closed** | Consumer and budget hypotheses are matched by interval below and in the TeX. Pre-entry estimates are not borrowed from the weak passage. |
| 2. Static bound | **Closed** | For 0 ≤ ζ ≤ R_ζ and qR_ζ ≤ π/2, Q_T ≤ 2q²ζ²μ_T + 2𝔈_T. Current-angle and endpoint checks are explicit. |
| 3. Energy identity | **Closed** | (h²)′ = −2h(W₁R₁₂+W₂R₂₂), h=(U₂)_−. The squared negative part is C¹; no boundary flux occurs. |
| 4. Dynamic estimate | **Closed, j = 2** | For every fixed cohort and t ≤ t_b, 𝔈_T(t) ≤ e³¹𝔈_T(0) + 31e³¹C_E q²(1+ℓ)² sup_[0,t] μ_T. |
| 5. All-time masses | **Closed** | A new direct radial comparison gives μ_T(t) ≤ e⁵μ_T(t₀) for every fixed cohort and 0 ≤ t ≤ t₀. It extends the already proved passage mass bounds to initialization. |
| 6(B). Late passage precision | **Closed** | Q_(Σ∪B) ≤ Cq²[q⁸+(1+ℓ)²q^γ_*] uniformly even on [0,t_b], γ_* = 289169/924000. On [t_s,t_b] this pays the full background error and source-rate charges. |
| 6(C). Smaller fixed-level entry | **Closed** | For each compact level set 𝒩 ⊂ (0,n], full normalized error and source-rate comparisons at t_(n′) have error O_𝒩(q^(1/20)), uniformly over n′ ∈ 𝒩 and the stated parameters/offsets. |
| 7(D). Continuation form | **Closed as a conditional inequality** | An explicit matrix/alignment/mass criterion is proved. Its future cross-residual and matching hypotheses are **not** discharged here. No trajectory is continued beyond t_b. |

There is no failing inequality or unmatched estimate through t_b. The old CWI mass-only/tail-moment gap is paid by the **actual lower-half transverse energy**, not by improving the old decoupled tail exponent.

## Main estimates

For each fixed cohort T, with h=(U₂)_−, define

\[
\mathfrak E_T(t)=\int_T h^2\,d\lambda_0,\qquad
\mathcal Q_T(t,\zeta)=\int_Tm[\sin(q\zeta-\theta)]_+^2\,d\lambda_0.
\]

The proved all-time inequality is

\[
\mathfrak E_T(t)\le
e^{31}\mathfrak E_T(0)
 +31e^{31}C_Eq^2L^2\sup_{0\le v\le t}\mu_T(v),
\qquad L=1+\log(1/q),\qquad \mathfrak E_T(0)\le q^{10}.
\]

For Σ the initial lower-half energy is exactly zero because its initial inputs are in Q2. All other cohorts use the safe q¹⁰ initial bound.

The constants can be chosen as

\[
C_\times=\max(C_{\rm pre},M_{\rm res}),\quad
C_{12}=1+C_\times,\quad C_1=C_\times/2,\quad
C_G=2,\quad k_G=169/3200,
\]

\[
C_E=C_{12}^2+2C_1+
\frac{2C_G}{e k_G}
+\frac{2C_GC_{\rm a}}{\sqrt{2e k_G}},
\]

where C_a is the already justified all-label angular alignment constant in δ ≤ C_a qL.

For T=Σ∪B, set

\[
\epsilon_{\rm bg}(q)=q^8+L^2q^{\gamma_*},
\qquad \gamma_*=\frac{289169}{924000}>\frac3{10}.
\]

Then uniformly on the late passage and bounded nonnegative offsets,

\[
|E_{\xi_q}-E_{\xi_q}^{K}|
+|\xi_q\cdot\dot f_{T,p}|
+|D_p^\tau-D_p^{K,\mathrm{self}}|
\le C_{R_\zeta}q^2\epsilon_{\rm bg}(q).
\]

Here the core self-output is evaluated using its **actual velocities in the full training field**. It is not a separately trained core-only network. Selected weak labels contribute no direct probe output there, but remain residual producers.

## Hypothesis matching, including signs and time ranges

| Source / consumer | Required hypotheses | Where supplied |
|---|---|---|
| Exact flow, balance, loss | Positive balanced initialized radii; Gaussian model; normalized time; regular characteristic flow with finite moments. | Original model through the proved endpoint. The loss derivative is displayed in the TeX; the initial loss is ≤1 for q≤1/2, hence each cluster residual has L² norm ≤2. |
| P earlybounds | Aligned initialization; S₀=q¹⁰; alignment statement requires S̄−S₀<π. | On [0,t_m], S̄(t_m)=O(q^u), u=19/2−4/(1−λ)≥169/102>1. Thus the range condition is verified, and alignment is O(q^u). |
| MOMC main | Initialized deep regime; small q; fixed right-half ancestry; positive weights; interval to its first half-mass time. | On [t_m,t₀], strong mass M_R≤1/2, donors in chart 79/51, left mass ≤Cq²ℓ²M_R, and the integrated mass-law defect is O(q²ℓ²). |
| MOMC integral used here | Positive M_R≤1/2, its mass equation and integrated defect. | Restated and proved: ∫M_R = log[(1−M₀)/(1−1/2)] − ∫M_Rδ_M/(1−M_R) ≤ log 2 + o(1). No bound is merely imported from an unquoted proof. |
| Q3SB crosspre | Initialized early envelope and MOMC conclusions; arbitrary receivers; no pre-entry response sign or strip-entry contract. | On [0,t₀], both cross residual norms are O(q). Before t_m, output ≤S|X| with S=o(q); after t_m, compact strong donors cost qM_R and all remaining donors cost their small mass. |
| Q2EC fullgates / RB pretrace | Strong donors in a reached chart, M_R≤1/2, absolute complementary-mass charge; receiver angle unrestricted. | On [t_m,t₀]. The matrix decomposition and its trace/antisymmetry bounds are restated and justified. They imply intermediate-time Cq alignment, not just the endpoint bound. |
| RB completed passage | Initialized regime, unchanged fixed constant order and small q. Its c≥0 barrier is proved. | On [t₀,t_b], all residual, mass, core, clock and alignment conclusions are available. No new guard or independent clock premise is used. |
| S2CP / strip and complement budgets | Their original stopped hypotheses, including c range, entry, geometry, field and residual bounds. | Used only as **proved conclusions inherited by RB** on [t₀,t_b]. The new backward radial lemma, rather than an out-of-regime application, supplies pre-t₀ masses. |
| CWI split | Exact balanced output; fixed T=Σ∪B; G+ inactive; bounded core chart giving f_K=O(q); all-label alignment. | Verified on [t_s,t_b]. Late primary inactivity is proved directly from the RCET ratio and RB clock; it is not inferred from ancestry. |
| CWI equivalence | Split hypotheses and μ_TL²→0. | All-time cohort masses below supply this. The stronger quantitative estimate is used, so no sign cancellation is assumed. |
| CWI ratecharge | Sourcewise bounded diagonal matrix entries and O(q) cross entries; alignment CqL; fixed cohorts; bounded offsets; selector/a.e. rate convention. | All supplied by the new matrix lemma and RB alignment on [t_s,t_b]. No outside chart or receiver derivative is required. |
| CWI corestatic | Reached core chart; mass and first moments close to the selected branch; same parameter and mass phase. | WCS restricted to each n′ in a compact subset of (0,n], with MP mass/phase and RB radius. |
| CWI corerates | Corestatic hypotheses plus a fixed positive core probe gap; sourcewise CFA field expansion; pointwise late remainder; SRR moment comparison; correct source normalization. | Same entry times. These source statements hold on the smaller interval. The offset range gives a reference gap >477/425 and hence an actual core gap ≥1 for small q. No integrated forcing allowance is treated as a pointwise source estimate. |
| TAILREP selection at n′ | Exact logistic N; 0<N₀<n′<1; nonnegative regular errors; original weak return maintained; positive actual donor/core moments; local strong box; finite incoming-law L²; common pointwise d₀; ℓ_B≥0 with integral≤1; small gain and strict initial guard. | All field/return conditions are already proved by WCS on [t_s,t_n] and persist on restriction. Small gain and initial guard are checked uniformly below. |

The resulting energy proof does **not** require a sign for R₂₂, a sign for W₂ on the lower input side, weak compact support, or a chart for the outside labels. The c-range is used only through the already proved passage sources, not as a new assumption in the energy identity.

## Dynamic proof audit

### Exact static signs and endpoints

For 0≤qζ≤π/2, both sin(qζ) and cos(qζ) are nonnegative:

\[
(U\cdot\xi_q)_+
\le |U_1|\sin(q\zeta)+(U_2)_-\cos(q\zeta).
\]

Squaring and integrating yields Q_T≤2q²ζ²μ_T+2𝔈_T. At current θ=0 the first inequality is equality; at θ=π the activation is zero; at θ=3π/2 it is equality with value √m cos(qζ). At ζ=0, θ=0 and π are gate endpoints. These are current-angle statements; no cohort ancestry supplies a sign. No unrestricted negative-offset version of the displayed one-sided trigonometric inequality is used.

### Matrix values, regime by regime

R^(j) includes the mixture factor 1/2. On every interval:

- The P₁ part of R₁₂ is O(q) by bounded residual norm and X₂=qZ₂.
- The P₂ part is O(q) because the **first residual** has norm O(q), while X₂ has bounded norm. This is exactly the cross-residual input.
- R₂₂^(1)≤(1/2)‖e₂‖_(P₁)‖X₂‖_(P₁)=O(q²). The P₁ second output is correspondingly O(q) in L²; it is not allowed an order-one size.
- For U₂<0, writing s=−sin θ, the P₂ gate probability is exactly Φ(−ρs/q). Hölder and Cauchy–Schwarz give

  \[
  |R_{22}^{(2)}|
  \le\tfrac12\|e_2\|_{P_2}
       (\mathbb E X_2^4)^{1/4}\mathbb P(A)^{1/4}
  \le2e^{-169s^2/(3200q^2)}.
  \]

Only an L² residual bound is used; no residual L⁴ estimate or independence from the receiver gate is assumed.

Before t_m the early envelope supplies cross residuals and alignment. On [t_m,t₀], MOMC and Q2EC supply the reached donor geometry and complementary mass. After t₀ the completed RB conclusions supply them. No interval is filled by a bound proved only in a later regime.

### Alignment on the intermediate interval

The proof-level RB estimate is needed for every time before t₀, so it is restated and justified:

\[
(\operatorname{tr}R)_-\le C(q^2M_R+\mu_{R^c}+M_Re^{-c/q^2}),
\]

\[
|R_{12}-R_{21}|\le C(qM_R+\mu_{R^c}+M_Re^{-c/q^2}).
\]

The exact Δ equation then has negative-trace integral O(q²ℓ²) and antisymmetric integral O(q+q²ℓ²)=O(q). Starting with O(q^u) at t_m, Gronwall gives Cq uniformly to t₀. RB supplies CqL after t₀. In coordinates, |W₂−U₂|≤C_a qL√m.

### Why j=2, not a positive power loss in q

The only Young absorption is

\[
2C_{12}qh\sqrt m\le L^{-1}h^2+C_{12}^2q^2Lm.
\]

The P₁ diagonal costs 2C₁q²m. For P₂, with δ=|θ−ψ|,

\[
2h|W_2||R_{22}^{(2)}|
\le2C_Gm(s^2+\delta s)e^{-k_Gs^2/q^2}
\le2C_Gm\left(\frac{q^2}{ek_G}
             +\frac{\delta q}{\sqrt{2ek_G}}\right).
\]

Thus 𝔈′_T≤L⁻¹𝔈_T+C_Eq²Lμ_T. The total duration is at most 31L, so the integrating factor is at most e³¹ and the accumulated forcing is q²L²μ_T^*. This proves the fixed exponent j=2.

The suggested explicit split also works: K_lay²=12800/169 gives small-layer h²≤K_lay²q²ℓm and large-layer matrix tail≤2q⁴. The global Gaussian maxima used in the proof are sharper and cover both sides of that split, including s=0. No integration by parts is used.

## Cohort masses and precision now paid

The pre-entry comparison is an exact radial argument:

\[
(\log m)'\ge-a_*|\theta-\psi|^2-2a_*S,\qquad a_*=\tfrac12+q^2.
\]

P/MOMC give ∫₀^(t₀)S≤2; the pre-entry alignment proof gives ∫₀^(t₀)|θ−ψ|²≤1 for small q; a_*≤1. Hence m(t)≤e⁵m(t₀) for every t≤t₀ and every label. This is derived, not an independent backward-clock premise. It applies to any fixed q-dependent cohort.

| Cohort | Supremum on the entire [0,t_b], with fixed constants |
|---|---|
| Σ | C(q⁵ + q^(Γν)E_g + q²K_Y²), Γν≥γ_*=289169/924000 |
| Strong complement C | Cq^(1+Δν), Δν≥17141311/140024000>3/25 |
| π strip | C[q^(1211/800)(1+√logℓ)+q¹¹√ℓ] |
| J_3 inner zone | Cq^(4769/4000)(1+√logℓ) |
| Q3 interior | Cq¹⁰ |
| Frozen zones | Cq¹¹√ℓ; already included where whole-strip bounds are used |
| Entire B, or a remaining subcohort | e⁵q^(11/10) for small q |

Each bound times L² tends to zero. For Σ∪B, the aggregate bound is Cq^γ_*, because γ_*<11/10<2<5 and Γν≥γ_*. Applying the new energy inequality and the exact static bound pays every Q_T previously left open by CWI, including the lower-side Σ slice and transit labels in both strips.

On [t_s,t_b], the RCET ratio gives

\[
q|U_1|/U_2\le C(C_0q^{597/640}+q^2)=o(1),\qquad U_2>0.
\]

The time exponent follows directly from RB's exact clock and I′≤Q, so it is valid up to t_b, not just to the former selection endpoint. It proves strict primary inactivity, including the regularized boundary label b=π.

The CWI algebra and matrix-value rate bound then apply on the entire late interval. All cross terms are charged using the square-root output bound √(μ_TQ_T); for example

\[
L\sqrt{\mu_T\epsilon_{\rm bg}}
\le C(q^4L\sqrt{\mu_T}+L^2\mu_T)
\le C(q^8+L^2q^{\gamma_*}).
\]

Nothing is discarded because it has a favorable sign. In particular the aligned negative contribution −Q_T is now small in its exact observable norm.

## Fixed-level uniformity and phase

Let 𝒩⊂(0,n] be compact with n_->0, fixed before q. Use the same WCS auxiliary logistic, N(t_s)=q^(1/8). Each t_(n′) lies inside the already proved [t_s,t_n].

For the endpoint constants,

\[
\Theta(n')\le\frac{16C_sB_{\max}C_wn'}{\lambda_{\min}g_{\min}}
\le\frac18<\frac14.
\]

Moreover a₀−m₀≥λ_min/8, g−m₀≥g_min/2, B_*≤B_max, and K₀ is uniformly bounded. WCS's E₀=O(q^(1/20)), d₀=O(q^(1/20)), A₀=O(q^(1/16)) make the initial guard uniformly strict. TAILREP's terminal weak estimate has only the additional denominator √n′≥√n_−. This proves E_s+W₂=O_𝒩(q^(1/20)); it does not assert uniformity as the terminal level approaches zero with q.

MP's mass/phase bounds and SRR's weight and moment bounds already hold on [t_s,t_e], so CWI's core error and source-rate calculations apply at all these entries. In particular μ_K=1+O(q^(11/10)); the source calculations retain the full residual and use pointwise late estimates. The reference gap on WIT's offset range exceeds 87/50−21/34=477/425>1, and the actual core gap is at least one for small q.

The same center works exactly for every auxiliary level:

\[
\tau_h=t_n+\lambda^{-1}\log((1-n)/n),\qquad
t_{n'}=\tau_h+s_{n'},\quad
s_{n'}=\lambda^{-1}\log(n'/(1-n')).
\]

The entry comparisons are

\[
q^{-2}(E_{\xi_q}-1/2)(t_{n'})
=\mathcal E_{\rho,\zeta}(s_{n'})+O_{\mathcal N}(q^{1/20}),
\]

\[
q^{-2}D_p^\tau(t_{n'},\xi_q)
=d_{p,\rho,\zeta}(s_{n'})+O_{\mathcal N}(q^{1/20}).
\]

These are uniform over the deep ratio box and ζ∈[87/50,7/4]. Common learned-window margins still require WIT's smaller P_* and later continuation. Rates use the selector/a.e. convention; no pointwise gate-hit-atom claim is added.

The new background error is smaller than the core entry error because q^(−1/20)ε_bg→0. The phase uses the actual clock seed H₀ and the proven O(q²ℓ)=o(1) Q-versus-λ correction, never RB's O(1)-accuracy terminal hitting time. Physical time remains (τ_h+s)/μ₁² and D_p^phys=μ₁²D_p^τ.

## S5c handoff: precise conditional requirements

The TeX proves the following conditional bound on a proposed future interval [a,a+𝒯]. For any w>0,

\[
\mathfrak E_T(t)\le e^{w(t-a)}
\left[\mathfrak E_T(a)+q^2
\left\{\frac{C_{12}^2}{w}+2C_1+\frac{2C_G}{ek_G}
+\frac{2C_Gd_{\rm al}}{q\sqrt{2ek_G}}\right\}
\int_a^t\mu_T(v)\,dv\right].
\]

Its hypotheses are matrix **value** bounds and a coordinate alignment bound, not a receiver-derivative contract. They require no c-range or strong mass equal to one.

| Quantity | Exact requirement / conditional deduction |
|---|---|
| Cross residual norms | On the future fixed interval, continue ‖e₂‖_(L²(P₁))+‖e₁‖_(L²(P₂))≤C_𝒯q. This is the main unpaid residual requirement for the energy mechanism. |
| Diagonal loss bounds | Bounded cluster L² residual norms. For the exact initialized gradient flow these follow from loss monotonicity on any interval where the trajectory exists. They give bounded matrix values. |
| Lower-side gate moment | The same Gaussian distributions and ρ≥13/20 plus bounded ‖e₂‖_(P₂) give the exponential R₂₂^(2) estimate; no extra sign or chart hypothesis is needed. |
| Alignment | It suffices that |W₂−U₂|≤C_𝒯qL√m. Conditional on the continued cross-residual norms and bounded matrix values, the exact Δ equation propagates RB's O(qL) entry alignment with a fixed exp(C𝒯) loss. |
| Fixed-cohort mass | For the energy alone, L sup μ_T→0 is sufficient on a fixed window. For full CWI error/rate cross terms with O(qL) alignment, retain L² sup μ_T→0. Conditional bounded matrices give μ_T(t)≤exp(C𝒯)μ_T(t_b) for the same fixed cohort, so the already paid masses have only a fixed-time loss. |
| Core/primary direct carriers | For full background separation continue a bounded scaled core chart and f_K, ḟ_(K,p)=O_𝒯(q), plus primary inactivity. Otherwise pay any newly active primary output and rate explicitly. These are separate from the negative-input energy identity. |
| Original-to-leading reduction | Continue velocity and reaction errors in CWI's first-moment norm, mass/logit phase, weak activity and all actual residual-producer effects. This is not proved by the energy inequality. |
| Rate precision on windows | Use only gate-separated learned windows for uniform source comparisons; keep the selector/a.e. convention elsewhere. No gate-hit-atom rate transfer has been added. |

No joint bootstrap after t_b is run. No S5c residual guard is asserted to hold automatically. No later-window original-to-leading theorem or AN8 assembly is claimed.

## Constants, source scope and validation

The existing WPT/RB → WBR/MP/SRR/WCS order is unchanged. The new constants k_G=169/3200, C_G=2, K_lay²=12800/169 and duration factor 31 are model-only. The pre-entry factor e⁵ uses only S1. C_×, C_a and C_E depend at most on already fixed passage constants and multiply the displayed vanishing scales. Then fix R_ζ and 𝒩, and choose q last. Future constants may depend on the fixed window length, never on q.

No new numerical or experimental premise is used. The Gaussian maxima and all exponents are established by displayed analytic calculations. No prior increment, foundation, checkpoint or README is modified; GitHub remains read-only.

Repository sources were re-read, including roadmap v1.24 and the committed CWI. The new prefix was checked against the repository. The following table records fetched Git blob hashes, not commit hashes.

| Read-only repository source | Git blob SHA |
|---|---|
| [README.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/README.md) | `b58ebe0893b059224f01e1ac97330b3c067c2ab2` |
| [00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md) | `370585b7eaf6f7b10e79b58b93dd48f801e76361` |
| [07_compact_windows_AN07/AN07_compact_window_interface_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/07_compact_windows_AN07/AN07_compact_window_interface_v1.tex) | `0902c80583eabb6bc0908ffb64a396633654ae19` |
| [03_passage_AN03/AN03_response_barrier_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_response_barrier_v1.tex) | `5312b5093f3ed4f74063347df31ae5a29155255f` |
| [03_passage_AN03/AN03_weak_chart_selection_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_weak_chart_selection_v1.tex) | `01888c1655996ad0c7fb07880bd93fa0be3efa4f` |
| [03_passage_AN03/AN03_Q3_strip_budgets_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_Q3_strip_budgets_v1.tex) | `13a024c54f10d50a454aae1006d3005d2a28051b` |
| [02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex) | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| [01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex) | `cb458c933aa043cf0188fd11c46bf4246ffc91d8` |
| [03_passage_AN03/AN03_strong_reference_reduction_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_strong_reference_reduction_v1.tex) | `6388f0192b970ebfae8604d7cab89dce37a25cfe` |
| [03_passage_AN03/AN03_S2_closure_package_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_S2_closure_package_v1.tex) | `baeb8a7eb1e36ce86319782511b665944be1afda` |
| [02_entry_AN02/AN02_Q2_entry_contracts_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_Q2_entry_contracts_v1.tex) | `b149537025e130801fc55b9e49c365c158eee17b` |
| [03_passage_AN03/AN03_matching_package_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_matching_package_v1.tex) | `9491bba4ec10f79acca277b1f0c4ddd92180a7aa` |
| [03_passage_AN03/AN03_weak_boundary_return_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_weak_boundary_return_v1.tex) | `c1f18203cc99ca5ddcda9481ca1281d7debffa9a` |
| [03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex) | `1777839da3fa10ebf66e8560f7175678753c39b9` |

Validation completed: two final LaTeX passes produced no warnings or undefined references; all 34 labels are unique and every internal reference resolves. The control-byte pattern `[\x00-\x09\x0b-\x1f]` returned no matches using PCRE2 and a separate byte-level check; `\rm`, `\tfrac`, `\qquad` and `\text` are intact. All 84 pre-existing output files retain their original SHA-256 hashes. Rendered pages were inspected. The source ZIP contains exactly the TeX and review files, with byte-identical contents; the compiled PDF remains scratch validation only.
