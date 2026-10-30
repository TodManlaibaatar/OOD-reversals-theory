# Review: AN03_selection_interface_v1

**Outcome: partial; stopped at the original weak-return hypothesis.** The complete TAILREP/WEAK hypothesis inventory is supplied. Core donor moment bounds and quantitative weak-coordinate size information close. The original condition u ≥ 0 with a strict inward margin does not follow from the attempted BULK absolute-ratio / residual-norm route. No selection theorem is asserted with that missing condition appended as an assumption.

New files: `AN03_selection_interface_v1.tex` and this note. Prefix: `an03siv1:`. The source ZIP contains the raw TeX and Markdown only, not a PDF.

## What is proved

1. **Core first moment and coarse donor moments.** For the positive normalized core measure, the same-reference first moment is O(q^{1/20}). For sufficiently small q, one can use 0 < Ȳ_K ≤ 3/5 and 0 < ρK̄_{s,K} ≤ 3/5. For the unnormalized core, 0 < Y_K ≤ 5/8 and ρK_{s,K} ≤ 3/5 suffice. These bounds use RB's core geometry and AN06's analytic a < φ(0) < 2/5. They do not identify the original weak field with the leading field.
2. **The precise content of BULK's weak-coordinate size bound.** On the clock cohort,

   \[
   |u|+|v|\le C\left[q^{-15/8}e^{-Q(1-c_b)(t-t_0)/4}+1\right].
   \]

   At a first hit of a fixed actual clock level H = h below a fixed lower bound for H(t_b),

   \[
   |u|+|v|\le C_h(1+q^{-p_b}),\qquad
   p_b=15/8-\tfrac14 k(1-c_b),\quad
   69/160\le p_b\le147/160.
   \]

   This permits a growing endpoint chart, for example q^{-1+1/20}; it does not give a bounded chart or a sign. At λ = 49/100, the exponent is 3/5 + 51c_b/40. The fixed positive c_b correction must not be omitted from the q-power.
3. **The correct static mass relation on a growing chart.** Exactly, N_C = H_C + A_C + J_C. For support |u|, |v| ≤ L(q) with qL(q) → 0,

   \[
   N_C/H_C=1+O(q^2L(q)^2).
   \]

   Thus L(q) = q^{-1+ε} gives O(q^{2ε}), not generally O(q²). BULK's O(q²) statement is for a bounded weak chart. The corrected error still tends to zero, but a static relation alone is not a logistic phase match.
4. **A complete inventory of the actual source hypotheses**, including the exact small-gain and initial-margin formulas, the separate return hypothesis, the strong mass-deficit terms, and the domains of the cited results.

These are interface results. They are not “Steps 1–6 closed.” The dynamic selection application stops when the return hypothesis cannot be matched.

## Notation audit

| Symbol | Required meaning | Do not identify with |
|---|---|---|
| WEAK M | Strong-family squared-radius mass; exactly one on WEAK's invariant leading surface | RB's residual constant M_res, the cap M_K = 2, or CFA's capped mass min(μ_K,1) |
| Physical core mass μ_K | Candidate original strong-family mass when all non-core labels are charged separately | A unit normalization of its measure without the resulting field defect |
| N | A leading weak mass satisfying N′ = λN(1−N) exactly | The signed response c, the clock amplitude H, or the actual cohort radial mass N_C |
| WEAK Y | Strong output-angle moment ∫y dμ_s | LCRC's transverse guard variable Y or K_Y |
| B_ρ | Bound on the strong moment \|ρK_s\| | The residual integral bound B |
| Weak coordinates | u = (π/2−θ)/q, **v = (ψ−π/2)/q** | Using the input angular convention for the output coordinate |

The last sign is essential. The weak output direction is (−sin(qv), cos(qv)), as in P `pa:charts` and BULK `weakJ`.

## Full hypothesis inventory

### WEAK's setup and forcing theorem

- The defined leading system, with strong mass **M = 1**, fixed strong and weak family labels, positive radial measures, μ_w = Nη_w, and η_w a probability with **fixed normalized label weights**.
- Characteristic solutions with bounded support on each compact time interval, finite relevant moments, and justification of the moment differentiations. A support bound may diverge as q → 0; this does not itself give uniform moment smallness.
- Exact weak field equations and exact logistic mass N′ = λN(1−N).
- 0 < N_0 < n_b ≤ 1/2 and N(t_n) = n_b.
- Y ≥ 0 and |ρK_s| ≤ B_ρ throughout the interval.
- Finite U_0^+ = E(u(t_s))_+ and V_0^abs = E|v(t_s)|, with N_* = N_0(U_0^+ + 3V_0^abs)².
- Exact constants C_u = φ(0) + φ(0)/[λ(1−n_b)] and C_w^force = C_u + B_ρ/λ.

**Matched:** model box, fixed original cohorts, positivity and boundedness of the candidate core donor moments, finite-time characteristic setting. **Unmatched:** the original-to-leading weak field and weight representation and the exact logistic mass identification. Core moment bounds alone are not that representation.

### WEAK concentration

In addition to the preceding hypotheses:

- u(t_s,b) ≥ 0 for every selected label;
- 0 ≤ Y ≤ Y_max < 2φ(0);
- the **strict** boundary margin

  \[
  \mathfrak m=\phi(0)-Y_{\max}/2-C_un_b-U_0^+\sqrt{N_0n_b}>0.
  \]

Its conclusion u ≥ 0 and its exact pair multiplier √(N(s)/N(t)) hold in the same leading field. They are not original-flow consequences of positive U2 and W2.

**Matched:** a coarse possible geometric Y_max = 5/8 for core moments, for which φ(0) − Y_max/2 > 1/16. **Unmatched / stopping point:** the original incoming sign and strict boundary inequality, as well as the incoming-moment term in the margin.

### WEAK Wineq and strong comparison

- The preceding nonnegative-input conclusion and the same full field with fixed weights.
- The selected coherent branch at the **same logistic N(t)**; its input must also be nonnegative so that the comparison segment lies in the scalar contraction region.
- Fixed 1 ≤ p ≤ ∞ and finite W_p = ‖|u−U_*| + |v−V_*|‖_{L^p(η_w)}.
- The strong moment discrepancy Δ_s = |Y−Y_*| + ρ|K_s−K(ρX_*)|.
- A local stable strong box, with δ < a/8, a + 3δ < 2φ(0), selected strong coordinates within δ of (a,a), and the displayed symmetric coherent Jacobian bounded above by −gI on the 2δ box.
- The same-field reference guard E_s < δ, pointwise strong first-moment bound D_s ≤ d_0, and valid donor Lipschitz constants C_s on that box. WEAK gives the admissible choice C_s = 20(R_*+1)² with its specified selected-coordinate bound R_*.
- In WEAK's unperturbed selection theorem specifically: Y_max = a + 3δ, B_ρ = ρφ(0) + λ(a + 3δ), and C_w^0 = (1+λ)/2 in the coupled weak error inequality. This C_w^0 differs from C_w^force above.

**Matched:** AN06 `regiontheorem` proves 0 < U_* < 1 and 0 < V_* < 11/10 on the selected leading branch for 0 < N ≤ 1/2. WEAK proves existence of its local constants analytically. RB supplies a small core radius and a fixed reference allowance. **Unmatched:** identifying the original population with the field and weight structure, its return region, and the tighter reference entry guard. The fixed allowance e ≤ 3e_*/4 does not automatically imply E_0 ≤ δ/(2K_0).

### TAILREP selection

TAILREP requires the **already established original-to-leading error inequalities**

\[
D^+E_s\le-gE_s+C_s(d_0+NW_p),
\]
\[
D^+W_p\le[-\lambda(1-N)/2+N/2+\ell_B]W_p+C_w(E_s+d_0),
\]

with nonnegative errors, d_0 ≥ 0, ℓ_B ≥ 0, fixed positive g,C_s,C_w, and a common finite budget ∫ℓ_B ≤ L_*. They hold up to E_s < δ. The theorem explicitly assumes the weak return-region hypotheses are maintained separately. It also requires exact logistic N, 0 < N_0 < n_b < 1, and the endpoint N(t_n) = n_b. For this use of WEAK/AN06 the common range is n_b ≤ 1/2.

Its constants and margins are exactly

\[
B_*=e^{L_*}(1-n_b)^{-1/(2\lambda)},\quad
a_0=\lambda(1-n_b)/2,\quad m_0=\min(g/2,a_0/2),
\]
\[
L_0=1+\frac{C_s(1+B_*)}{g-m_0},\quad K_0=2L_0,
\quad \Theta=\frac{C_sB_*C_wn_b}{(a_0-m_0)(g-m_0)}\le\frac14,
\]
\[
K_0(E_0+d_0+A_0\sqrt{n_b})\le\delta/2,
\qquad A_0=\sqrt{N_0}W_p(t_s).
\]

Terminal convergence additionally needs N_0 → 0, A_0 → 0, d_0 → 0 and a uniformly admissible E_0 and constants, including L_*.

**Unmatched:** the two original-flow differential inequalities with these budgets, separate return, logistic matching and initial smallness. These are not conclusions of TAILREP's abstract theorem.

### Core mass deficit

TAILREP explicitly retains

\[
|Y_K-Y_*|\le D_K+\mu_KE_s+|\mu_K-1||Y_*|,
\]
\[
|K_{s,K}-K(\rho X_*)|
\le\rho D_K+\rho\mu_KE_s+|\mu_K-1|K(\rho X_*).
\]

P's full leading weak field also has −(1−M)vΦ(u)/2 and −(1−M)K(u)/2. Thus the deficit has additive comparator costs and costs linear in large incoming weak coordinates. It cannot be removed by declaring the normalized core to be the full strong family. The exact late-interval sup/integrated budgets for this role are not discharged here. This is not a claim that S2CP's mass equation cannot prove them; the application has already stopped at the return contract, and no later stage is run.

## Exact failed implication and stopping point

The attempted route was: use RB/BULK's signgood and small Cartesian ratio as the original weak return condition, and use the cross-residual norm bound to preserve its strict margin.

The first implication is invalid. For the balanced algebraic state

\[
U=W=\sqrt m(-\sin q,\cos q),
\]

one has z > 0, a_- = 0 and qj/z = q tan q = O(q²), but u = −1, v = 1. This tests the asserted implication between the bounds; it is **not** a counterexample trajectory of the initialized flow.

At a potential original boundary hit u = 0, the exact angular equation is

\[
u'=\frac{R_{21}(\pi/2)\cos(qv)-R_{11}(\pi/2)\sin(qv)}q.
\]

The needed robust strict margin is

\[
\boxed{\frac{R_{21}(\pi/2,t)\cos(qv)-R_{11}(\pi/2,t)\sin(qv)}q
\ge\mathfrak m/4>0.}
\]

It must hold at every possible boundary hit on the chosen interval, together with labelwise u(t_s) ≥ 0. The existing matrix norm estimate yields only

\[
u'\ge-C_\times(1+M_{\rm res})-r(t)|v|.
\]

The q in the cross residual cancels against the scaled angular derivative. For an absolute-error argument the attempted absorption is

\[
C_\times(1+M_{\rm res})+r(t)|v|\le\mathfrak m/4.
\]

It has no vanishing q factor. With the harmless coarse convention C_× ≥ 1, its left side is at least 1 and its right side is less than φ(0)/4 < 1/10. More fundamentally, an unsigned bound on R21 cannot produce the positive boundary sign. At v = 0, the matrix-value test R21 = −a q allowed by that norm bound gives u′ = −a. No claim is made that such a residual comes from the initialized population with all its additional structure.

An integrated bound ∫r ≤ B does not give a pointwise inward margin. Making n_b small does not make the fixed residual constant M_res small. AN06's positive selected U_* is a comparator result, not the missing original sign. A weak-receiver selected-moment cancellation could repair this, but RB's c-form result is on a fixed **strong** receiver chart and does not supply it.

**Stop:** no second route is attempted; no unmatched return assumption is inserted into a purported full theorem. This is an unresolved implication, not a refutation of initialized selection.

## Status by requested step

| Step | Status | Exact disposition |
|---|---|---|
| 1: Inventory | **Complete as an audit; matching partial** | Every source hypothesis and its sign/range/margin is listed. The original return-region and error-system hypotheses remain unmatched. |
| 2: n_b and late start | **Not executed as a selection construction** | Exact small-gain formula recorded. A fixed actual H level can be placed before t_b, but no common logistic-mass endpoint or late interval satisfying all selection inputs is claimed. |
| 3: Weak return | **Size consequence proved; sign route stopped** | BULK gives the displayed absolute bound and exponent. Missing: original u(t_s,b) ≥ 0 and the boxed boundary margin. |
| 4: Weak-chart field | **Unmatched; not run after the stop** | Need the two TAILREP differential inequalities with d_0 → 0 and a common finite ∫ℓ_B. The fixed strong-chart c-form does not imply them. |
| 5: Phase match | **Static audit only** | Growing-chart N_C/H_C error is O(q²L²). Dynamic N↔H↔c matching remains unproved. |
| 6: Smallness | **Not established** | No original N_0,A_0,d_0 and admissible E_0 satisfying the complete interface are constructed. |
| 7: Selection theorem | **Not stated** | No conditional full theorem with unmatched hypotheses is substituted. |

## Further accuracy and domain checks for S4b

- **Endpoint level:** n_b ≤ c_b/2 alone does not place a first H = n_b hit before t_b. RB gives H(t_b) ≥ c_H c_b for some fixed c_H, not necessarily c_H ≥ 1/2. A clock level h < c_H c_b/2 works, but still needs identification with leading N.
- **Phase:** if a comparison logistic N starts at H(t_s), the exact identity is

  \[
  \log\frac{H(t)}{N(t)}
   =q^2\int_{t_s}^t(1-c)+\lambda\int_{t_s}^t(N-c)+\delta(t_s,t).
  \]

  The first and third terms vanish. Uniform vanishing of the signed middle integral is still needed; ∫|N−c| = o(1) is sufficient. RB's fixed O(c_b) bound on ∫c is not this phase estimate.
- **Field scope:** a receiver near θ = π/2 lies outside the c-form receiver chart |θ|,|ψ| ≤ L_cq. Its value/derivative remainder cannot be transferred merely by renaming variables. The primary C0E_g part of that existing integrated remainder is small fixed, not o(1).
- **Core deficit:** unit normalization creates the explicit terms listed above. CFA's T = 0 convention does not eliminate them.
- **Weights:** fixed original cohorts are available, but exact leading normalized weights are an additional structure. An o(1) amplitude defect and exact equality of radial weights are different claims.
- **Smallness:** J_G = O(q²) alone makes a scaled weighted transverse size √J_G/q only O(1). Additional estimates are needed for A_0 → 0; fixed-q bounded support is not enough. Higher p, especially p = ∞, also requires the corresponding moment/support control.
- **Boundary labels:** no endpoint is silently deleted to assert the original return sign. The algebraic sign test is at a regular weak-chart state, with no division by a zero second coordinate. The return contract must include the chosen cohort's endpoint labels; the AN06 branch's positivity does not settle them.

## Constant order

All WPT/RB constants stay fixed in their existing order. The closed audit results use model/core constants 3/5 and 5/8, BULK's existing bound and the fixed c_H from RB's terminal comparability. The proposed later selection order would append WEAK's analytic local constants δ,g,C_s,C_w, a **proved** common L_* for the original weak error equation, and then a fixed n_b satisfying Θ ≤ 1/4, the return margin and the correctly matched endpoint condition; q would be chosen last.

No numerical value of L_* is asserted from the current handoff, no fixed c_b-dependent error is relabeled o(1), and no earlier residual constant is changed to force the failed boundary absorption.

## S4b handoff

**Available:** the complete hypothesis checklist; the correct coordinate and mass conventions; core first-moment replacement O(q^{1/20}); coarse positive bounded core moments; the absolute weak-coordinate exponent at fixed actual clock level; and the corrected growing-chart mass comparison.

**First required new result:** an original-flow weak-return argument for a fixed cohort. It must construct a late start with u ≥ 0 and prove the boxed strict boundary estimate, or another argument giving the same invariant-return conclusion, using the actual selected moments rather than an unsigned cross-residual charge.

**Still to discharge afterward:** late mass-defect and weak-chart value/linear-error budgets, fixed-weight comparison, logistic phase matching, the local strong-reference initial guard, and N_0,A_0,d_0 smallness. This note does not prescribe these as hypotheses of a claimed full theorem.

No bootstrap is continued past t_b. No S5 retention, selection conclusion, or consolidation is attempted.

## Source provenance and checks

The current default-branch README and roadmap **v1.18** were read through the GitHub connector on 2026-10-28. The theorem files below were also fetched read-only. The roadmap is context, not a proof source. RB's handoff is the only imported source of passage facts; P, WEAK, TAILREP and AN06 are used to audit the defined leading system and its selection hypotheses, and BULK is used for the exact ratio formula expressly referenced by the handoff/task.

GitHub code search for `an03siv1:` returned no results before creation; the local prior `.tex`/`.md` search also found no collision. The identities below are file blob SHAs, not repository commit hashes.

| Source | File blob SHA |
|---|---|
| `README.md` | `d8b26e71688a607ae0f30ea19d6bb6acb045b9bf` |
| `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | `25ecb11e26d291ea84995457f13d3e857f03d11b` |
| `03_passage_AN03/AN03_response_barrier_v1.tex` | `5312b5093f3ed4f74063347df31ae5a29155255f` |
| `03_passage_AN03/AN03_response_barrier_v1_review.md` | `42d11697a897a72ad0f4429e5873c63a5a89adf7` |
| `03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex` | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| `03_passage_AN03/AN03_weak_transit_forcing_and_orbit_selection_v1.tex` | `3a937aa25253b5773424a3f165f71d476157575a` |
| `03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` |
| `04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex` | `9e102514ad0a491066a2f9eb8eb86e9a251c2b53` |
| `01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex` | `cb458c933aa043cf0188fd11c46bf4246ffc91d8` |

### Artifact verification

- The standalone TeX compiles with all local references resolved and no final-pass LaTeX warnings or overfull boxes.
- Its 35 labels are unique and all use `an03siv1:`.
- All 57 pre-existing output files recorded at task start remain byte-for-byte unchanged.
- The source ZIP contains exactly the new `.tex` and `_review.md`, with their raw bytes verified against the files. No PDF or compilation product is included.
- No experiment, numerical proof premise, GitHub mutation, prior-increment edit, or work beyond the stated stopping point was performed.

