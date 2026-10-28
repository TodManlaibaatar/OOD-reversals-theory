# Review: AN03_response_barrier_v1

**Status:** the response barrier closes, and WPT's two-boundary theorem becomes the initialized weak-passage theorem. No additional response-sign, alignment, strip, or energy hypothesis is retained.

**Files:** `AN03_response_barrier_v1.tex` and this note. Label prefix: `an03rbv1:`. The source ZIP contains these two raw source files only; it contains no PDF.

## The theorem and the main new argument

For κ = 10, ρ ∈ [13/20, 7/10], WPT's fixed constants, and sufficiently small q, the original initialized flow reaches its first upper response boundary t_b < t_0 + 20 log(1/q), with t_0 = t_h. On the whole closed passage,

\[
c(t)\ge \frac{\kappa_0}{2}q^2\mu_{\mathcal K}(t)
             +\frac12 H_{G_+}(t)>0,
\qquad \kappa_0=\frac{351}{102400}.
\]

Thus WPT's τ equals t_+ = t_b, and t_- > t_b. Every conclusion of WPT `twoboundary` holds there. In addition,

\[
H(t_b)\asymp c_b,\qquad
t_b-t_0=\frac{\log(c_b/H_0)+O_{\rm fixed}(1)}{Q},
\qquad H_0\asymp A_q^{-\lambda}q^{10(1-\lambda)}.
\]

The exact clock retains its O(q^{1/8} + q² log(1/q)) = o(1) subinterval defect. The bounded hitting-time error is not claimed to be o(1), and the denominator is Q, not Q(1 − c_b).

The signed outside estimate is obtained by a weaker version of the alignment route than the proposed fixed-Cq region:

\[
\sup_{b,t\in[t_0,\tau]}|\theta-\psi|
 \le C_{\rm al}q(1+\ell),\qquad
(c_S)_-\le C[(q+C_{\rm al}q(1+\ell))^2+e^{-\rho^2/(4q^2)}]\mu_S.
\]

Together with WPT's existing μ_B ≤ q^{11/10} guard, this gives (c_B)_- = O_fixed(q^{31/10}(1+ℓ)²) = o(q²). A fixed-Cq alignment strip is neither assumed nor asserted. The weaker proved estimate already supplies the required consumer inequality. The energy route is unnecessary and is not claimed as a separate result.

## Task-by-task outcome

| Task | Status | Result / exact remaining inequality | Constant dependencies |
|---|---|---|---|
| (1) Core response and lower mass | **Closed** | x,y ≥ 9/320; c_K ≥ (351/102400)q²μ_K; μ_K ≥ μ_K(t_0)e^{-d_q} = (1/2 − o(1))e^{-d_q}. No remaining inequality. | The coordinate and response constants are model-only. The threshold for q can depend on WPT's fixed constants through its improved radius and d_q. |
| (2) Primary and secondary | **Closed** | c_{G+} ≥ 8H_{G+}/9 − Cμ_{G+}exp(−ρ²/(4q²)); \|c_Σ\| ≤ H/9 + C(q⁵ + q^{9/2} + q^{4+Γν}). No remaining inequality. | Secondary remainder coefficient depends on C_Σ, K_Y and the fixed ratio box. These multiply powers strictly above two. |
| (3) Signed outside | **Closed by the alignment route at sufficient accuracy** | (c_B)_- = o(q²) ≤ κ₀q²μ_K/4, stronger than the requested allowance with H_{G+}/9. Component bounds are in the TeX table. No remaining consumer inequality. | C_al depends on B, M_res, E_g, c_b; it appears only with vanishing scales. Pre-entry C_al,0 is S1-only. |
| (4) Barrier, terminal amplitude, theorem | **Closed** | Strict positivity at a putative first lower hit contradicts c(τ)=0. Terminal H_{G+} ≥ 9c_b/10 − o(1), and fixed-distortion comparison gives H(t_b) ≍ c_b. No residual hypothesis. | Terminal comparison uses fixed primary-entry/matching constants and RCET's fixed distortion; no earlier guard is chosen using this constant. |

The new results are `core`, `explicit`, `entryalignment`, `postalignment`, `donorsign`, `outside`, `barrier`, `clockcomparison`, and `completed` under the new prefix. The proof does not re-run the joint weak-passage bootstrap.

## Proof audits that matter

### Core sign uses the improved radius

The raw guard r_K < 1 alone does not imply positive core coordinates. WPT has already proved, on its two-boundary interval, e ≤ 3e_*/4 ≤ 3/16 and r_K = O(q^{1/20}). With the analytic bound φ(0) > 3/8,

\[
a\ge \rho\phi(0)\ge39/160,
\qquad x,y\ge39/160-3/16-9/320=9/320
\]

after choosing q so that r_K ≤ 9/320. The exact compact-chart P2 moment is

\[
c_K=\frac{q^2}{Q}\int_K y\,\rho\mathsf K(\rho x)\,d\mu
            +O_R(q^4\mu_K).
\]

For Q ≤ 1, its leading coefficient is at least 351/51200. Half absorbs the uniform q⁴ correction. All estimates are analytic; the elementary bound on φ(0) is proved by an integral inequality, not a numerical premise.

For the lower core mass, use the last crossing below its entry mass in the exact S2CP Bs equation (log μ_K)' = 1 − μ_K + η. Below the entry mass, which is less than one, the logistic term is nonnegative. Thus log μ_K cannot fall by more than ∫|η| = d_q. Integrating the pointwise upper overshoot for a logarithmic time would introduce an unjustified d_qℓ loss; that argument is not used.

### The all-label pre-entry alignment is proved, not imported outside its range

Q2EC `early` is explicitly all-label, so |θ − ψ|(t_m) = O(q^u), u ≥ 169/102 > 1. MOMC then supplies right-half donors on a fixed chart with M ≤ 1/2, ∫M ≤ 3/2, and complementary mass μ ≤ Cq²ℓ²M.

Using Q2EC's **all-receiver** `fullgates` decomposition gives

\[
\sup_\theta(\operatorname{tr}R_\theta)_-
 \le C_R(q^2M+\mu+Me^{-c/q^2}),
\quad
\sup_\theta|R_{12}-R_{21}|
 \le C_R(qM+\mu+Me^{-c/q^2}).
\]

The P1 diagonal coefficients are positive because M ≤ 1/2; its selected off-diagonal second moment is O(q), and the strong off-diagonal donor moments are O(qM). Their trace cost is therefore O(q²M). P2's strong trace charge is also O(q²M). The target covariance is symmetric, so it makes no antisymmetric contribution. These are matrix-value calculations for arbitrary receivers, not an extension of MOMC's receiver-chart reduction.

Their integrated costs are O(q²ℓ²) and O(q), respectively. The exact angle-difference equation yields uniform |θ − ψ|(t_0) ≤ C_al,0 q. No angular-sector hypothesis or finite-q cooperativity is needed.

### Post-entry negative trace is paid by the proved gate budget

The needed estimate is for the negative diagonal, not merely the excess of |R22| above I'/2. Directly from the selected residual,

\[
-R_{22}(\theta)
 \le\tfrac12 M_{\rm res}q^2+\tfrac12\mathbb E_{P_2}(f_2X_2)_+
 =\tfrac12 M_{\rm res}q^2+\tfrac12(Qc+N_-).
\]

S2CP `gate` therefore gives

\[
\int\sup_\theta(\operatorname{tr}R_\theta)_-
 \le B+\frac{5\mathrm e}{9}\frac{E_g}{1-c_b}+o(1).
\]

With |R12 − R21| ≤ a_*q, a_* = C(1+M_res), the exact equation for Δ = θ − ψ gives the explicit choice

\[
C_{\rm al}=\exp\!\left(B+\frac{5\mathrm e E_g}{9(1-c_b)}+1\right)
             (C_{\rm al,0}+20a_*).
\]

The temporary |Δ| < 1 guard improves to |Δ| < 1/2 for small q. S2CP's gate budget is a proved conclusion on WPT's interval; CLOCK's future forcing allowance is not used as its source. CFR's negative K_O moment is not confused with N_-.

### Exact signed donor moment, with zero-sine endpoints included

For s = sin θ and v = sin ψ,

\[
A_q(s)=\mathbb E_{P_2}[X_2(a_\theta\cdot X)_+]
=\rho q\mathsf K(\rho s/q)+q^2s\Phi(\rho s/q).
\]

The per-mass response is vA_q(s)/Q. If v ≥ 0, only X2 < 0 can contribute negatively. If v < 0 ≤ s, then s and |v| are at most |Δ|. If v < 0 and s < 0, the positive part of A_q(s) is at most ρq K(−ρ|s|/q), which gives the q² + q|Δ| bound. These three cases prove the signed response estimate without dividing by sin θ or sin ψ.

This covers b = π, b = 3π/2 = −π/2, all intermediate crossing states, and joined/frozen/transitional J3 labels. The endpoint cases are not removed as null sets in the pointwise argument.

### Exact secondary powers and the small clock

The response charge gives

\[
|c_\Sigma|\le C_\Sigma q^5+C_\Sigma q^{\Gamma_\nu}H
       +Cq^{9/2}+Cq^{2+\Gamma_\nu/2}\sqrt H.
\]

Young's inequality uses H/18 + Cq^{4+Γν}; C_Σq^{Γν} ≤ 1/18 gives the other H/18. There is no assertion that the absolute secondary remainder is o(H_0). It is o(q²), which is absorbed by the positive core response. This is what avoids WPT's failed absolute-domination route.

### Primary-to-clock comparison and clock accuracy

Q2EC's threshold proof keeps primary Q2 labels outside a fixed qL chart through t_0, after their matched weak-axis band. Q2E's regularized crossing seed and exact U2 rate then imply

\[
\widehat U_2(t_0,b)^2\asymp A_q^{-\lambda}q^k(s_0+q)^2.
\]

The post-crossing gate integral is uniformly bounded in this sector, by a Gaussian half-line integral after changing variables using the positive cotangent rate. Q2EC's coordinate transport and entry signs transfer the upper bound to z². Integrating gives H_{G+}(t_0) ≤ C_ent H_0. At b = π the regularized seed is s_0 + q = q; no logarithm is taken at its initial zero U2.

RCET transports the ratio with a fixed e^{2D_+} factor, D_+ = O(C0 + q²ℓ). At c = c_b the upper response ledger gives H_{G+} ≥ 9c_b/10 − o(1), so the clock itself has H(t_b) ≍ c_b. This uses the primary cohort, not the whole-Q2 q⁵ energy floor.

The exact time identity is

\[
t_b-t_0=\frac{\log(H(t_b)/H_0)-\delta(t_0,t_b)}Q+\int c,
\quad
0\le\int c\le\frac{10\mathrm e E_g}{9Q(1-c_b)}+o(1).
\]

The factor 1/Q is kept. Replacing H(t_b) by c_b costs an O(1) logarithm, while δ = o(1). No asymptotic equality with denominator Q(1 − c_b) is claimed.

## Hypothesis matching and domain conditions

| Cited result | Hypotheses used, including sign/range | Supply on the interval used |
|---|---|---|
| WPT `twoboundary` | Original balanced isotropic initialization, κ = 10, ratio box, fixed constant order, small q. | The present model. This theorem is unconditional and supplies [t_0, τ], with 0 ≤ c ≤ c_b even at its closed endpoint. |
| MOMC `main`; Q2EC `early` | Initialized flow before t_h; moving t_m; the S1 parameter box. | Unconditional S1 conclusions. No post-entry sign condition is invoked before t_0. |
| Q2EC `fullgates` and moment bounds | Strong donors in their chart, M ≤ 1/2, arbitrary complement of mass μ; arbitrary receiver angle. | MOMC on [t_m, t_0]. The source is uniform over receiver gates. |
| LCRC `identity`, `responsecharge`, `taulower` | Fixed cohorts, balanced finite radial mass; taulower additionally W2 ≥ 0. | Fixed partition; original balanced flow; WPT/LCRC signgood for G+. No angular margin is needed by taulower. |
| LCRC `localclock`; RCET Theorem 2.1 / BULK Theorem 4.1 | 0 ≤ c ≤ c_b < 1, logarithmic duration, diagonal/cross residual norms, ∫r ≤ B, positive entry z, antisymmetry ratio ≤ 1/4, Cartesian entry ratio, small admissible C0. Clock uses η = 1/8. | WPT on [t_0, τ], Q2EC entry, unchanged constant choices. No secondary cap or future endpoint cap is used to obtain localclock. |
| S2CP `gate` | Response range, duration, residual/clock guards, Y < K_Y, E_{G+} < E_g, joint secondary guard, core chart/mass, outside supremum, fixed S1 entry, D empty. | WPT's simultaneous guards and strict improvements. This conclusion pays the negative-trace integral. |
| S2CP S2 / Bs | Same stopped inputs; S2 also coarse c-form value/derivative budget, reference bound and entry profiles; Bs core radial identity, current geometry and instantaneous outside bound. | WPT's fully matched two-boundary bootstrap and its S1 sources. We inherit the improved secondary energy, masses and logistic equation. |
| GESG / PISB / LSB | Fixed ancestry partition, pre-entry cross bound where required, post-entry duration/residual/clock guards. | WPT `outside`, using Q3SB `crosspre`. No unproved whole-strip chart or lower-side condition. |
| Q2E crossing / Q2EC matching and transport | Closed target Q2 sector, regularized endpoints; original positive-coordinate matched sector before fixed qL entry. | Q2EC's primary-threshold proof, including the b = π band. |
| CFA representation and passage | Core-only normalized positive donors, c range, stopped residual/secondary/outside/geometry inputs, entry clock and forcing smallness. | Already matched in WPT. This increment inherits its conclusions, and does not assume a later passage to prove the barrier. |

**Circularity check:** every sign-dependent estimate is applied only on WPT's already certified [t_0, τ]. Positivity is then proved at τ itself, excluding τ = t_-. There is no invocation of these sources on an interval that crosses a negative response state.

## Constant order and new constants

The order remains WPT/CFA's:

1. Model box, c̄ = 1/4, L_T = 20, b_B(q) = q^{1/10}, R = 79/51, R_LCRC = 2R, M_K = 2, B_s^0 = log 2 + 1, L_c = R + 1, χ = 1/20 and fixed admissible cutoff/gain parameters.
2. Model passage constants C_pass, g, e_* and the conservative B, K_Y, M_res, with M_res > 2C_pre. These are uniform over small c_b.
3. Coarse field allowance F̄_F, small c_b, E_g = 2c_b; S2 distance/gain constants.
4. C0 within LCRC/RCET and CFA requirements.
5. K(C0), SEP cap and entry constants, then C_Σ.
6. q last, now also small enough for the finite new inequalities in this increment.

| New constant | Dependency | Use |
|---|---|---|
| y_min = 9/320 | Model-only rational lower bound | Positive core coordinates |
| κ₀ = 351/102400 | Model-only; compact-chart correction absorbed by choosing q | Positive core response |
| C_al,0 | S1/model constants | Entry angle difference C_al,0 q |
| a_* = C(1+M_res) | Fixed cross-residual guard | Antisymmetric matrix forcing |
| G_b = 5e E_g/[9(1−c_b)] | Fixed energy/response constants | Negative-trace integral |
| C_al = exp(B+G_b+1)(C_al,0+20a_*) | Fixed guards | Only C_al q(1+ℓ) and its squared, mass-weighted vanishing cost |
| Secondary remainder C | C_Σ, K_Y, Q lower bound | q⁵, q^{9/2}, q^{4+Γν} |
| C_ent | Fixed Q2EC threshold/matching constants, S1 seed bounds | Fixed primary/clock ratio |
| C_ent exp(2D_+) | Above plus RCET fixed distortion | Terminal H(t_b) ≍ c_b; bounded phase error |

No new constant chooses an earlier guard, chart radius, response cap or forcing allowance. A_q remains the original S1 normalization, bounded above and below; its clock factor is A_q^{-λ}, and its time contribution is +λ log A_q/Q to t_b − t_0.

## S4 handoff

| Input | Certified conclusion | Accuracy / limitation |
|---|---|---|
| Response endpoint | c(t_b) = c_b; strict positive barrier through t_b | Exact first upper hit, now unconditional |
| Clock | All-subinterval log(H(t)/H(s)) = I(t) − I(s) + δ; δ = O(q^{1/8}+q²ℓ) | o(1) defect |
| Seed and terminal amplitude | H_0 ≍ A_q^{-λ}q^k, H(t_b) ≍ c_b | Fixed comparisons, no exact seed coefficient or terminal ratio |
| Passage time | Exact identity with terminal H; [log(c_b/H_0)+O(1)]/Q after replacement | Bounded phase error, not o(1); Q(1−c_b) only supports an upper-bound estimate |
| Primary state | Positive z, signgood, RCET Cartesian ratios and fixed relative-amplitude transport | Fixed e^{O(C0)} accuracy; clock cohort separately has o(1) defect |
| Residuals/transverse energy | Diagonal residuals O(1), cross residual ≤ M_res q/2, J_G ≤ q²K_Y²/4, ∫r ≤ C_r log2 + o(1) | Original-flow bounds |
| Learning/core mass | ∫\|1−κ1\| ≤ log2 + o(1); (1/2−o(1))e^{-d_q} ≤ μ_K ≤ e^{d_q} | d_q = o(1); not a claim of exact terminal mass one |
| Core/reference | r_K = O(q^{1/20}), e ≤ 3e_*/4, fixed chart | Vanishing core radius; fixed reference allowance, not selection |
| Secondary | E_Σ ≤ C_Σ(q⁵+q^{Γν}H), all-endpoint distance/capped gain | Fixed constants and explicit positive powers |
| Complement/outside | WPT's individual positive-power mass bounds and their integrated μ/q budgets | All paid through t_b, including both Q3 strips |
| Strong c-form | CFA core-only representation, T = 0; small fixed integrated value/derivative remainder and forcing | Primary C0E_g and forcing √E_g terms are not relabeled o(1) |

No weak return, selection, matching after c_b, or consolidation is undertaken.

## Source provenance

The repository was read through the GitHub connector, without mutation, on 2026-10-28. The source identities below are GitHub **file blob SHAs**, not repository commit hashes. Roadmap v1.17 and the named statements were read from the current default branch. These identities allow a reviewer to distinguish this source snapshot from later updates.

| Source path | File blob SHA |
|---|---|
| `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` (v1.17) | `f5b2124e2ae0f5569db66c308628e0e6f3c57187` |
| `03_passage_AN03/AN03_weak_passage_theorem_v1.tex` | `c1ff996972ad471c27aefd1bfd66391e6feb6d79` |
| `03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex` | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` |
| `03_passage_AN03/AN03_S2_closure_package_v1.tex` | `baeb8a7eb1e36ce86319782511b665944be1afda` |
| `03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex` | `f00459b5ca412eb86b0893adb64766e2c10d5590` |
| `03_passage_AN03/AN03_pi_strip_budget_v1.tex` | `ab8a0a2a028935f5045e53e0066e30afeb69c635` |
| `03_passage_AN03/AN03_late_strip_budget_v1.tex` | `4d3c0065e3b639c02db87c704a3efcfbb0738190` |
| `03_passage_AN03/AN03_c_form_assembly_v1.tex` | `341908c228092e9a818d98de3ec26591a1050364` |
| `02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex` | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| `03_passage_AN03/AN03_Q3_strip_budgets_v1.tex` | `13a024c54f10d50a454aae1006d3005d2a28051b` |
| `03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex` | `a490ea323e45e61c1a58301554b89ad84cb02605` |
| `03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex` | `49e352002b4c699338ac99a4d55d51c60760ea86` |
| `02_entry_AN02/AN02_Q2_entry_contracts_v1.tex` | `b149537025e130801fc55b9e49c365c158eee17b` |
| `03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex` | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| `02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex` | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` |
| `03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` |
| `02_entry_AN02/AN02_Q2_boundary_layers_and_cohort_energy_v1.tex` | `cce55e1029cfd1ca8afb98eb649389b420d3992b` |

## Artifact checks

- The standalone TeX compiles in two passes, with no unresolved references, LaTeX warnings, or overfull boxes on the final pass.
- All 43 local labels are unique and use `an03rbv1:`; every local reference resolves.
- The 53 pre-existing output files recorded at the start of this task remain byte-for-byte unchanged.
- The ZIP is a source archive containing only the new `.tex` and `_review.md`; compilation products stay in scratch storage.
- No numerical experiments, interval arithmetic, grid sign checks, saved trajectories, GitHub changes, prior-source edits, or S4 work were performed.

