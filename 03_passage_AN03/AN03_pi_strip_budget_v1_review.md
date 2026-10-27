# AN03 π-strip budget v1 — review note

**Result: the requested π-strip supremum and integrated budgets close in the existing stopped setting.** The outer and middle zones of both strips are paid. The \(3\pi/2\) inner zone is left untouched, with its exact consumer recorded.

The companion source is `AN03_pi_strip_budget_v1.tex`, label prefix `an03pisbv1:`. The raw source ZIP contains this review and that TeX file only.

## Status by task

| Task | Status | Proven result / scope |
|---|---|---|
| (1) Outer zone, both strips | **Closed** | `outer`: a buffer \(C_{\rm buf}q^3\ell\) suffices inside \((\pi+w_q,3\pi/2-w_q)\). Both outer zones remain frozen, with \(m=q^{10}e^{O(q^3\ell)}\). |
| (2a) Selected entries and refined speeds | **Closed** | `table` tracks all four entries. Angular rates carry \(q\), radial rates \(q^2\), and every entry retains \(e^{-k_Gs_\theta^2}\). |
| (2b) Middle freezing | **Closed** | `travel`, `middleradial`: scaled travel is \(O((1+s_q)\ell^{-\varepsilon})=o(1)\); the logarithmic mass change is \(O(q^2(1+s_q)^2\ell^{-\varepsilon})=o(1)\). Both middle-zone budgets vanish. |
| (3) Inner π zone | **Closed for the needed mass budget** | Exact target-only boundary domination at the overlap, then a coarse original-flow mass bound through \(t_0\), pays the needed growth explicitly. No extension of Q2EC transport to Q3 is assumed. |
| (3) Post-\(t_0\) gain | **Closed** | `regularizedgain` keeps \(N(t_0)+q\) and the exact exponent \(1/\beta=1+q^2/\lambda\). The proof of the strip budget needs only its cap-one companion `capone`. |
| (4) π-strip budgets | **Closed with a weaker explicit rate** | `pibudget` proves both \(o(1)\) conclusions. Uniform power in \(\mu_{\mathcal S_\pi}/q\): \(q^{411/800}\), up to \(\sqrt{\log\ell}\) and displayed fixed factors. |
| Proposed sharper \(O(q^3(\log\ell)^{3/2})\) mass rate | **Not established** | The coarse bridge intentionally retains a strong-rate factor \(e^{t_0-t_m}\). The requested \(o(1)\) budgets do not require the sharper rate. |
| \(3\pi/2\) inner zone | **Deferred as instructed** | Only `lateconsumer` and the required supremum/integral are stated. No entry, mass–displacement, or near-reference contraction estimate is proved for this zone. |

No task was stopped by a false premise. The route changes at the inner π zone: a proved but coarser bound suffices, so the sharper unproved intermediate contract is not made a premise.

## Main bound and exact powers

Let \(c_m=4/(1-\lambda)+1/2\), \(k=10(1-\lambda)\), and
\[
\begin{aligned}
\delta_1&=c_m-k,\\
\delta_2&=(19\lambda-7)/2,\\
\delta_3&=4/\lambda+10\lambda-12.
\end{aligned}
\]
The theorem proves
\[
\sup_{[t_0,t_*]}\frac{\mu_{\mathcal S_\pi}}q
\le Cq^{10}\sqrt\ell+
C e^{2B+\Xi_q}E_gA_q^{\lambda-1}s_q
 (q^{\delta_1}+q^{\delta_2}+q^{\delta_3}),
\]
where
\[
\Xi_q=D_{\rm clk}
 +C\{q\ell+q^2\ell^2+q^u+(1+M_{\rm res})qL_T\ell\}=o(1),
\quad D_{\rm clk}\le C(q^{1/8}+q^2\ell).
\]
The exact rational margins are
\[
\delta_1\ge15259/9240,\qquad
\delta_2\ge411/800,\qquad
\delta_3\ge521/490.
\]
The first two functions increase with \(\lambda\); the third decreases on the ratio box. These are analytic monotonicity checks and exact endpoint substitutions.

The integral is bounded by \(L_T\ell\) times the same right side. Hence both budgets vanish uniformly over stopped endpoints. The resulting uniform mass rate is
\[
\mu_{\mathcal S_\pi}
=O(q^{1211/800}\sqrt{\log\ell}+q^{11}\sqrt\ell).
\]
The factor \(A_q^{\lambda-1}\) is retained. It arises from \(A_q^{-1}\) in the half-mass time shift and \(A_q^\lambda\) in the stopped weak clock. We do not substitute the stronger total-clock cancellation \(A_q^{-q^2}\), since the new proof uses a different pre-entry bound.

## Selected-entry audit for the middle zone

With \(C_*=C_{\rm model}(1+C_{\rm pre}+M_{\rm res})\), the entrywise bounds are
\[
|R_\theta|
\le C_*e^{-k_Gs_\theta^2}
\begin{cases}
\begin{pmatrix}q^2&q\\q&1\end{pmatrix},&\text{near }\pi,\\[3pt]
\begin{pmatrix}1&q\\q&q^2\end{pmatrix},&\text{near }3\pi/2.
\end{cases}
\]

- Near π, the \(P_1\) gate is exponentially closed. On \(P_2\), the coordinate norms are \(O(q),O(1)\), and the residual norms are \(O(q),O(1)\). Q3SB crosspre supplies the small residual before \(t_0\); the stopped cross-residual guard supplies it afterwards.
- Near \(3\pi/2\), the \(P_2\) gate is exponentially closed. On \(P_1\), the coordinate norms are \(O(1),O(q)\), and the residual norms are \(O(1),O(q)\). In particular \(R_{11}\) is allowed to be order one.
- Cauchy–Schwarz followed by the fourth-moment estimate supplies the gate probability to power \(1/4\) for **every** selected entry. The small residual norm and small coordinate norm are kept separately.
- Replacing \(\sin(qs)/q\) by \(s\) changes the Gaussian exponent by \(O(q^2s^4)\), uniformly \(O(q^2\ell^2)\) on \(s\le3\Lambda_q\). This retains the exact coefficient \(k_G=169/3200\) with a fixed multiplicative constant.
- The other cluster's \(e^{-c/q^2}\) tail is absorbable even into the smallest entry: \(e^{-k_Gs^2}\ge q^{27}\) on this domain.
- In the radial identity, the large diagonal has two small angular coordinates, and each cross entry has one. That yields \(q^2(1+s_\theta)(1+s_\psi)\), without a sign claim.

The freezing proof uses the label-dependent buffer
\[
\Delta(s_0)=A\ell(1+s_0)e^{-k_Gs_0^2}.
\]
Uniformly for \(s_0\ge s_q\), both \(\Delta(s_0)\) and \(s_0\Delta(s_0)\) vanish. Thus changing \(s_\theta\) within the buffer does not lose a tail constant, including at the upper end \(s_0\asymp\Lambda_q\). A first-exit argument improves the buffer by a factor two.

The middle and outer zones have total initial width \(O(q\sqrt\ell)\), and their mass remains \(q^{10}\) up to bounded factors. This gives, for each strip,
\[
\sup \mu_{\rm mid\cup out}/q\le Cq^{10}\sqrt\ell,\qquad
\int\mu_{\rm mid\cup out}/q\le CL_Tq^{10}\ell^{3/2}.
\]

## Inner π zone: why the weaker route closes

### 1. Target-only order, with no assumed original-flow cooperativity

Let \(g_q(\theta)=\mathbb E[(a_\theta\cdot X)_+^2]\). The exact equations give \(g_q'=2v_q\). The proof checks \(v_q<0\) from the resident root through \(\pi+qs_q\). Near π, the \(P_1\) positive contribution is exponentially small in \(q^{-2}\), while the negative \(P_2\) drive through \(K(-\rho s)\) is at least a fixed inverse power of \(\ell\), times \(q/(1+s_q)^2\).

Scalar uniqueness then preserves target angular order, and decreasing \(g_q\) orders the radial rates:
\[
\widehat\theta(t,b)\ge\widehat\theta(t,\pi),\qquad
\widehat m(t,b)\le\widehat m(t,\pi).
\]
The multiplicative comparison factor here is exactly at most one.

Q2EC's all-label early comparison transfers this mass inequality at \(t_m\). For original angles it gives only order up to \(O(q^u)\); exact ordering or finite-q cooperativity is **not** claimed.

### 2. The boundary seed is explicit

Before its target weak-axis crossing,
\[
\widehat U_2(t)\le Cq^6e^{\lambda t/2+Cqt+q^2t},
\]
with the nonzero \(q^6\) Gaussian seed kept. Q2E's regularized endpoint formulas give
\[
T_\times(\pi)=4\ell/\lambda+O(1),\qquad
\widehat m(T_\times,\pi)\asymp q^8.
\]
The target norm can grow afterwards at rate at most \(1+2q^2\). Combining the cases \(T_\times\le t_m\) and \(T_\times>t_m\) gives
\[
\widehat m(t_m,\pi)\le Ce^{Cq\ell}
 [q^{10}+q^{12-\lambda c_m}+q^{8-c_m+4/\lambda}].
\]

This includes the endpoint \(b=\pi\) explicitly and is consistent with both Q3SB lower bounds. In particular it never asserts that a zero initial sine means bounded mass amplification.

### 3. The pre-entry strong cost is retained as a q power

For every receiver, using only balanced flow and the output bound \(|f(X)|\le S|X|\),
\[
(\log m)'\le1+2q^2+4S,\qquad S=\int m\,d\lambda_0.
\]
MOMC's already-proved \(\int_{t_m}^{t_0}S\le3/2+O(q^2\ell^2)\) therefore gives a fixed cost at most \(e^{6+o(1)}\), in addition to the explicit factor \(e^{t_0-t_m}\). Thus
\[
m(t_0,b)\le CA_q^{-1}e^{C(q\ell+q^2\ell^2+q^u)}
 [q^{c_m}+q^{2+(1-\lambda)c_m}+q^{4/\lambda-2}].
\]

This step covers every time and quadrant after \(t_m\). It does not need a bounded \(\int r\) before \(t_0\).

**The old sharper unpaidradial inequality remains unproved, but is no longer a required premise for this mass budget.** Its logarithmic-time cost is not silently treated as constant: the factor \(q^{c_m-10}\) from \(e^{t_0-t_m}\) is carried through to the final positive exponents. Before \(t_m\), the full radial evolution is paid by the all-label early comparison and the target estimate.

No labels are reassigned to \(G_+\). Therefore no LCRC, S2CP or CFA cohort statement has to be rechecked for an enlargement. Q2EC's match/coordinatetransport statements are not extended beyond their proved Q2 domain.

### 4. After \(t_0\), both the regularized gain and its cap suffice

The regularized global sine envelope from \(t_0\) follows from the matrix values, \(\int r<B\), and S2CP's gate budget. TAILREP integration gives
\[
m(t)/m(t_0)\le e^{2B+\eta_q+1/\beta}
 \max\{1,A_N(N(t_0)+q)^2e^{\beta I(t)}\}^{1/\beta}.
\]
Here \(1/\beta=1+q^2/\lambda\) is exact.

For the final mass calculation it is more efficient to use the simultaneous direct bound
\[
m(t)/m(t_0)\le e^{2B+\eta_q}e^{I(t)}.
\]
It follows by replacing the signed weak product by its cap one; it has no extra shape constant and no loss in the clock exponent. S2CP's stopped clock then leaves the three positive powers listed above.

## Constants, assumptions and downstream scope

| Quantity | Dependencies / audit |
|---|---|
| \(k_G\), loss/Gaussian constants | Model box and initial loss only. |
| \(C_{\rm pre}\), crossing constants, resident-root constants, \(c_A,C_A\) | Proved S1/Q3SB constants, independent of LCRC guards. |
| Bridge cost \(e^6\) | Comes from \(4\int S\le6+o(1)\). It is guard-independent. |
| Middle-zone constants | \(1+C_{\rm pre}+M_{\rm res}\), the retained duration, and fixed \(\varepsilon\). They enter vanishing errors and the small-q threshold. |
| \(C_{\rm buf}\) | Loss-only speed constant and \(C_{\rm dur}\); fixed before \(q\). |
| \(C_N,A_N\) in the regularized post-entry estimate | \(B,G,M_{\rm res},c_b\), with \(G=5eE_g/[9(1-c_b)]\). They are not used in the main cap-one mass calculation. |
| Main π-budget factors | Explicit \(e^{2B}E_gA_q^{\lambda-1}\), plus \(\Xi_q\) and fixed model/S1 constants. |
| Clock defect | \(D_{\rm clk}=O(q^{1/8}+q^2\ell)\), taken from the original clock cohort; no new phase claim. |
| Existing chart/core/entry constants | Unchanged. No radius, mass cap, or \(C_0\)-dependent entry threshold is enlarged. |

The stopped setting, including retained outside supremum where S2CP's gate lemma uses it, is not confused with CFA's additional whole-strip input. The proof supplies the π part and the two frozen-zone parts. It does not supply the \(3\pi/2\) inner part or run the joint bootstrap.

The existing constant order remains valid; choose the auxiliary \(\varepsilon\) before \(q\), and \(q\) last. For any fixed CFA allowance, the proved contributions are eventually below it. A sharper asymptotic mass rate is unnecessary for that implication.

## Exact remaining consumer for the 3π/2 inner zone

Only
\[
J_3=(3\pi/2-qs_q,3\pi/2]
\]
remains unpaid there.

For a charted part, the consumer is S2CP's raw entry tail
\[
d\eta=m(t_0,b)d\lambda_0,\qquad
\eta\{\xi>v\}\le C_T\min\{1,(\epsilon_h/v)^{3/s_{\rm pr}}\},
\]
with the corresponding cutoff/tail moment, where
\[
\epsilon_h=\sqrt2 A_q^d(1-M_0)^\alpha q^{10d-s_{\rm pr}}.
\]
For later entrants the TeX's `lateconsumer` instead uses actual arrival times, actual entry mass and displacement, and includes unarrived mass. Both the arrival-valid gain and
\[
\sup\mathcal W_3/q=o(1),\qquad \int\mathcal W_3/q=o(1)
\]
(or CFA's small fixed integral allowance) remain to be supplied. Nothing about that inner zone is proved beyond recording the consumer.

## Source provenance

Fetched read-only from the default branch of `TodManlaibaatar/OOD-reversals-theory`. The roadmap identifies itself as v1.14; its repository header is dated October 23, while this increment uses the session's October 22 date. Hashes below are returned Git blob SHAs, not a claim of a commit-pinned snapshot.

| Source | Blob SHA |
|---|---|
| [00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md) | `a852c6439394f599e8555b681504be7eea79e962` |
| [03_passage_AN03/AN03_Q3_strip_budgets_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_Q3_strip_budgets_v1.tex) | `13a024c54f10d50a454aae1006d3005d2a28051b` |
| [03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex) | `f00459b5ca412eb86b0893adb64766e2c10d5590` |
| [03_passage_AN03/AN03_S2_closure_package_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_S2_closure_package_v1.tex) | `baeb8a7eb1e36ce86319782511b665944be1afda` |
| [03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex) | `a490ea323e45e61c1a58301554b89ad84cb02605` |
| [03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex) | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| [02_entry_AN02/AN02_Q2_entry_contracts_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_Q2_entry_contracts_v1.tex) | `b149537025e130801fc55b9e49c365c158eee17b` |
| [02_entry_AN02/AN02_Q2_entry_through_strong_passage_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_Q2_entry_through_strong_passage_v1.tex) | `042b3c93cf8402d10487f9e56f6f5b1d869c424a` |
| [03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex) | `49e352002b4c699338ac99a4d55d51c60760ea86` |
| [02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex) | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` |
| [03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex) | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` |
| [03_passage_AN03/AN03_c_form_assembly_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_c_form_assembly_v1.tex) | `341908c228092e9a818d98de3ec26591a1050364` |
| [02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex) | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| [02_entry_AN02/AN02_Q2_boundary_layers_and_cohort_energy_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_Q2_boundary_layers_and_cohort_energy_v1.tex) | `cce55e1029cfd1ca8afb98eb649389b420d3992b` |

## Verification and delivery

- Analytic proofs only: no simulations, saved trajectories, grid signs, interval arithmetic, or numerical premises.
- The standalone TeX compiled to eight pages with no warnings or overfull boxes in the final log. All 30 labels use the new prefix and all 33 internal references resolve. Compilation checks source syntax and references only; it is not mathematical evidence.
- The raw source ZIP contains only the requested TeX and same-stem review, with no PDF.
- All 43 pre-existing output files matched their pre-task SHA-256 hashes. No prior increment, foundation, checkpoint, or roadmap was edited; no GitHub mutation or merge was performed.

