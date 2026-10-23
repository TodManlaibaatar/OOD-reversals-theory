# AN03 S2 closure package v1 — review note

Companion: **AN03_S2_closure_package_v1.tex**. Label prefix: **an03s2cpv1:**. The source ZIP contains these two source files only.

**Result:** Tasks 1–2 close in the requested stopped-guard form. The gate budget is proved, the global envelope and all-endpoint gain follow, the joint secondary energy guard is strictly improved, and the fixed right-half strong complement has an integrable mass-over-q cost. Task 3 is a partial assembly audit: the secondary obstruction is paid, and a short additional argument pays \(B_s\) under retained core geometry; the complete c-form contract, Q3 strip budgets and full CLOCK forcing contract remain open.

This is not an unconditional joint weak-passage theorem. The c-form value/derivative contract and its donor hypotheses, core geometry, reference guard and outside supremum remain explicit inputs. No conclusion of CLOCK or the future assembly supplies a premise.

## Task status and remaining inequalities

| Task | Status | Result or exact remaining inequality | Source/dependencies |
|---|---|---|---|
| 1. Gate budget | **Closed** | \(\int(Qc+N_-)\le(10e/9)E_g/(1-c_b)+o(1)\), hence \(\mathfrak X\le(5e/9)E_g/(1-c_b)+o(1)\). | LCRC localclock and responsecharge; GESG signed/Ncohorts; temporary secondary guard; retained core and outside supremum. No c-form or CLOCK forcing budget is used. |
| 2a. Global distance | **Closed under inherited c-form guard** | DECG missingdistance with the displayed fixed \(C_D\), through chart exits and reentries until physical exit. | DECG local estimate, GESG splice, Task 1; actual same-field reference. |
| 2b. Capped gain | **Closed on that interval** | DECG Corollary 3.3 at every endpoint, including after exit; \(1/\beta\le1+\nu\), \(A_0=C_D^2\max(1,\delta_0^{-2})\), \(C_m=e^{6B+3}\). | 2a, DECG radial estimate and TAILREP integration. No off-chart receiver derivative is assumed. |
| 2c. Secondary energy | **Closed; guard strictly improved** | \(E_\Sigma\le C_\Sigma(q^5+q^{\Gamma_\nu}H)\), with entry and first-exit continuity checked. | SEP, bounded reference, 2a–b, LCRC secondary and stopped clock. \(C_\Sigma\) is independent of the trial guard coefficient. |
| 2d. Strong complement | **Closed for the specified fixed cutoff** | \(\sup\mu_{\mathcal C}/q\le Cq^{\Delta_\nu}\), \(\int\mu_{\mathcal C}/q\le Cq^{\Delta_\nu}\ell\), \(\Delta_\nu>3/25\). | MOMC/PROFILE entry tail, proved gain, TAILREP moment and rational margin. Excludes unclassified Q3 strips. |
| 3a. CFR \(U_\Sigma\) | **Closed** | \(\int(E_\Sigma+K_Y\sqrt{E_\Sigma})=o(1)\), with explicit powers. | 2c, \(H<E_g\), duration. |
| 3b. Full c-form | **Partial; retained** | Still need \(\int\sup_{[-L_c,L_c]^2}(|F_{\rm orig}-F_c|_1+\|D F_{\rm orig}-D F_c\|_{1\to1})\le\overline F_F\), with the specified donor representation. | Secondary charges paid; primary selected terms paid in CFR. Complete assembly, strip costs and representation/normalization defects remain. |
| 3c. Outside budgets | **Partial** | Strong complement and original Q3 interior paid. Need \(\sup(\mu_{\mathcal S_\pi}+\mu_{\mathcal S_{3\pi/2}})/q=o(1)\) and its integrated counterpart, or proved family reassignment with entry/gain contracts. | TAILREP, GESG; strip contracts restated below. |
| 3d. CLOCK geometry/reference | **Partial; no passage application** | Need \(\int(c+|V|+K_w+T+\epsilon_F)\le\overline F_{\rm pass}\le e_*/(4C_{\rm pass})\), plus its remaining entry/donor conditions. | Newly paid \(c\) term is \(O(c_b)\); primary candidate moments are \(O(c_b+K_Y\sqrt{c_b})\). Actual full field, strips and \(T\) representation remain. |
| 3e. \(B_s\) | **Closed under retained geometry** | \(\int|1-\kappa_1|\le\log2+o(1)\); any fixed \(B_s>\log2\) is guard-independent. | CFR radial state identity, paid secondary bound, retained core chart/mass and outside supremum, MOMC/PROFILE entry mass. Does not prove core retention. |

## Gate proof and coefficient audit

LCRC **localclock** uses the entry ratios and signs, response, duration, loss-monotonicity diagonal bounds, cross residual and \(\int r\le B\). It invokes BULK Theorem 4.1 and RCET Theorem 2.1, and requires neither \(E_\Sigma\), a terminal cap, an independently supplied backward clock nor LCRC's closure theorem.

It gives
\[
E_+\le\frac{10}{9}H_+,\qquad
H_+(s)\le eH_+(t)e^{-b_0(t-s)},\qquad b_0=Q(1-c_b),
\]
and consequently
\[
\int E_+\le\frac{10eE_g}{9b_0},\qquad
\int\sqrt{E_+}\le\frac{2\sqrt{10e/9}\sqrt{E_g}}{b_0}.
\]

Use an arbitrary fixed trial coefficient \(A\) in \(E_\Sigma\le2A(q^5+q^{\Gamma_\nu}H)\), and put \(S_q=2A(q^5+q^{\Gamma_\nu}E_g)\). Responsecharge bounds \(Q|c_{G_+}|\) by \(QE_+\) plus an integrated \(O(q^2K_Y\sqrt{E_g}/b_0)\) error. The secondary charge is \(O(S_q+q^2K_Y\sqrt{S_q})\), core charge \(O(q^2M_K)\), and outside charge \(O(qb_B(q))\), where \(b_B=\sup\mu_B/q=o(1)\). GESG Ncohorts gives the same scales and an exponentially small primary term for \(N_-\).

All non-primary terms vanish after multiplication by the logarithmic duration. Thus the trial coefficient affects only vanishing errors, not the leading gate budget or \(C_D\). The signed bound needs no extra pointwise cap on \(N_-\). A supremum outside budget suffices here, but does not supply the field's \(\int\mu_B/q\) budget.

**Correction to the proposed unweighted c inference.** Direct division gives
\[
\int c\le\frac{10e}{9}\frac{E_g}{Q(1-c_b)}+o(1).
\]
The roadmap's proposed side-benefit drops \(1/Q\); that numerical coefficient does not follow from the displayed backward-clock calculation. The new proof keeps it. Since \(Q\ge169/400\), \(E_g=2c_b\) still gives
\[
\int c\le\frac{20e}{9(169/400)}\frac{c_b}{1-c_b}+o(1)=O(c_b).
\]
This correction leaves the gate-excess coefficient and \(C_D\) unchanged. It does not establish the full CLOCK forcing budget.

## Envelope, gain and the acyclic energy guard

The explicit distance constant is
\[
C_D=\sec(1/2)C_{\rm loc}
\exp\!\left(B+\frac{5eE_g}{9(1-c_b)}+1\right)
\left(1+\frac{W_*}{L_c-R_c}\right),
\]
\[
R_c=79/51,\quad L_c=R_c+1,\quad
C_{\rm loc}=p_*^{-1}e^{C_T\overline F_F},\quad
p_*=\Phi(-7L_c/10),\quad
C_T=2+p_*^{-1}+(7/10)\phi(0)/p_*,
\]
\[
W_*=4R_c+\frac{C_R(1+M_{\rm res})}{\lambda(1-c_b)/2}.
\]
The extra \(1\) absorbs vanishing gate/Duhamel errors after all fixed coefficients are chosen. It is not a \(q\)-dependent allowance.

The displacement \(\xi\) is scaled; \(q\xi\) is physical. Hence \(q^2\xi^2\), not \(\xi^2\), enters the raw gain. Choose \(0<\delta_0<1/4\); before physical exit the actual reference is \(O(q)\), so the receiver remains on GESG's physical strong branch. SEP's cap can exceed \(L_c\); GESG's initially exterior case covers it. After first chart exit, reentries do not restart the estimate.

DECG gives \(A_0=C_D^2\max(1,\delta_0^{-2})\), defect integral at most \(4B+o(1)\), and raw mass multiplier \(e^{6B+1/\beta+o(1)}\le e^{6B+3}\). Fix \(0<\nu\le1/100\), then take \(q^2/\lambda\le\nu\). There is no extra geometric gain exponent.

LCRC's secondary lemma now has all its premises: SEP entry, bounded reference, distance, gain and the stopped clock. Its output constant depends on these fixed constants and \(E_g\), not the trial coefficient \(A\). Choose
\[
C_\Sigma\ge\max(1,C_{\rm out},C_{\rm ent}+1),\qquad A=C_\Sigma,
\]
then choose \(q\). Entry is strict because \(E_\Sigma(t_0)\le C_{\rm ent}q^5\). At a proposed first equality \(2C_\Sigma\), continuity of \(E_\Sigma/(q^5+q^{\Gamma_\nu}H)\) contradicts the improved coefficient \(C_\Sigma\). No other guard is declared closed by that argument.

### Constant order

Use
\[
(\text{model},R,M_K,B_s,c_b,\nu,\delta_0,c_*)
\to(B,E_g,K_Y,M_{\rm res})
\to(L_c,\overline F_F,C_D,A_0,C_m)
\to C_0
\to(K(C_0),Z_\Sigma,\text{entry constants})
\to C_\Sigma\to q.
\]

The suggested example \(C_\Sigma\to C_0\) overlooks SEP's dependence on \(K(C_0)\). Moving \(C_\Sigma\) after those entry constants is acyclic because it never enters the leading gate constant. LCRC's \(C_0<C_{\rm adm}(B,M_{\rm res})\) remains unchanged; CFR's receiver-boundary margin can require a further decrease after the chart is fixed.

| Constant | Role and dependency |
|---|---|
| Model box, Gaussian constants, loss bound | Independent of all residual guards. |
| \(R,M_K,R_c\) | Retained order-one core/reference budgets; no enlargement to absorb \(M_{\rm res}\). |
| \(B_s,c_b\) | Fixed before residual guards. New radial argument allows \(B_s=\log2+1\), or any preselected \(B_s>\log2\). |
| \(B,E_g,K_Y,M_{\rm res}\) | Fixed stopped guards. \(C_D\) may depend on them; its downstream energy/mass factors multiply positive powers of \(q\). |
| \(L_c,p_*,C_T,\overline F_F\) | Fixed local field contract. \(C_{\rm loc}\) need only be finite for S2; CLOCK forcing smallness is separate. |
| \(A_0,C_m,\eta_*\) | Gain/BULK constants; \(0<\eta_*<(\delta_0/(2C_D))^2\), \(C_m=e^{6B+3}\). |
| \(A_q\in[c_A,C_A]\), \(M_0\) | Actual MOMC normalization. Strong scale \(\epsilon_h=\sqrt2 A_q^d(1-M_0)^\alpha q^{10d-s}\), secondary scale \(h_A=A_q^dq^{10d-2s}\), clock \(H_0\asymp A_q^{-\lambda}q^{10(1-\lambda)}\). Bounds are guard-independent. |
| \(c_*,\chi=1/20,d_c=c_*q^{\chi+kP/2}\) | TAILREP fixed-label core cutoff. Selecting it does not prove continued geometry. |
| \(C_\Sigma\), entry tail constants | Chosen after \(C_0\); enter gate errors only at vanishing scales. |

LCRC literally chooses \(E_g^{\rm old}=2+2c_b\). The smaller \(2c_b\) requires a slack check: once the secondary estimate is paid, pointcap gives \(H_+\le9c_b/8+o(1)\), and signgood gives \(E_+\le5c_b/4+o(1)<2c_b\). The conservative old \(B,K_Y,M_{\rm res}\) values remain valid upper bounds. The gap is \(3c_b/4+o(1)\), not an arbitrary fixed half-unit. This is compatibility checking, not running the joint residual bootstrap.

## Complement and the two quick consequences

The complement is \(\mathcal C=\{b\in\mathcal R:\xi_b>d_c\}\). The normalized entry law is \(d\eta_0=2m(t_0,b)d\lambda_0\), because MOMC gives right-half mass exactly \(1/2\). Its tail has \(p=3/s\) and scale \(\epsilon_h\). The raw factor \(1/2\) is retained in the mass constant.

The stopped clock gives \(e^I\le C E_g A_q^\lambda q^{-k}\), \(k=10(1-\lambda)\), hence \(A_0q^2e^{\beta I}\le Cq^{2-k}\). TAILREP's moment lemma yields
\[
\Delta_\nu=p[5(1-P)-s-\chi]-1
 -(1+\nu)[k(1-P)-2-2\chi]_+.
\]
Its already proved rational bounds give
\(\Delta_\nu\ge17141311/140024000>3/25\) and
\(p-2(1+\nu)\ge49/7550\).
No numerical premise or second displacement charge is introduced.

The secondary consequence pays precisely CFR's obstruction:
\[
\mathcal U_\Sigma\le L_T\ell\left[
C_\Sigma(q^5+q^{\Gamma_\nu}E_g)
+K_Y\sqrt{C_\Sigma}(q^{5/2}+q^{\Gamma_\nu/2}\sqrt{E_g})
\right]=o(1).
\]

For \(B_s\), CFR's proved radial state identity gives
\[
(\log m)'=1-\kappa_1+\delta_m,\qquad
\int\sup_{\mathcal K}|\delta_m|=o(1),
\]
using \(J_G\le q^2K_Y^2\), \(E_G\le E_g+o(1)\), and
\(\int\mu_B\le qb_B L_T\ell=o(1)\).
Retained core geometry gives \(|\kappa_1-\mu_K|\le C_Rq^2\mu_K\).
Averaging and using the entry tail gives
\[
(\log\mu_K)'=1-\mu_K+\eta,\qquad
\int|\eta|=d_q=o(1),\qquad\mu_K(t_0)=\tfrac12-o(1).
\]
For \(w=\log\mu_K\), the positive-part identity yields
\[
w_+(t)+\int(\mu_K-1)_+\le d_q,\qquad
\int|1-\mu_K|\le-\log\mu_K(t_0)+4d_q.
\]
Adding the vanishing \(\kappa_1-\mu_K\) error proves
\(\int|1-\kappa_1|\le\log2+o(1)\).
Only vanishing error coefficients depend on the fixed guards, so \(B_s\) may be chosen before \(B=C_rB_s+2\). This proves neither core retention nor the exact pointwise \(M_s\le1\) donor condition from an integrated overshoot estimate.

## Remaining outside and forcing contracts

For the prescribed initialized circle,
\[
\mathcal B=\mathcal C\ \dot\cup\ \mathcal Q_{3,\mathrm{int}}^0
\ \dot\cup\ \mathcal S_\pi\ \dot\cup\ \mathcal S_{3\pi/2}.
\]
There is no other ancestry. GESG's original-label Q3 interior uses
\(k_G=169/3200\), \(\Lambda_q=\sqrt{3\ell/k_G}\),
\(w_q=\arcsin(q\Lambda_q)\), and interval
\([\pi+2w_q,3\pi/2-2w_q]\).
It has mass \(O(q^{10})\) throughout the stopped interval, paying \(O(q^9\ell)\). This is the initialization-based frozen interior, not an unlocated moving mask.

The two strips are not automatically recruited, retained on the negative side, or charted at \(t_0\). A **π-side** extension must classify its labels. A primary part needs \(z>0\), \(|a|/z\le1/4\), \(qj/z\le C_0\), \(J(t_0)\le Cq^3\), \(E(t_0)=o(1)\). A secondary part needs \(\xi\le Z_\pi\), raw mass \(O(q^3)\), and
\[
\eta_\pi\{\xi>u\}\le Cq^3\min\{1,(A_q^dq^{10d-2s}/u)^{p_2}\}.
\]
A **3π/2-side** strong extension needs a bounded actual-reference entry chart and the raw \(3/s\) upper tail at scale \(\epsilon_h\), together with the cutoff or TAILREP tail moment. Later arrivals need an arrival-matched contract and paid pre-arrival gain. Any unassigned remainder still needs both supremum and integrated mass-over-q budgets. No strip is reassigned here.

CFR's primary selected value/derivative cost is already \(C_{L_c}C_{\rm RCET}C_0E_g+o(1)\). Its secondary cost is now paid. The core second output costs \(O(q^2M_K\ell)\); its order-one first output stays in the donor field. The full c-form, including induced receiver derivative, remains retained until those pieces, donor normalization and strip costs are assembled.

For CFR's candidate moments
\[
V_O=-\mathbb E_{P_2}[(f_O)_1X_2]/(qQ),\qquad
K_O=\mathbb E_{P_1}[(f_O)_2X_1]/q,
\]
proved cross-output bounds give
\[
\int(|V_O|+(K_O)_+)\le
\frac{C}{b_0}(E_g+K_Y\sqrt{E_g})+C\int\mu_B/q+o(1),
\]
and \(\int(K_O)_-\le C\mathcal U_\Sigma+C\int\mu_B/q+o(1)\).
Choosing \(K_w=(K_O)_+\) transfers the negative part into the remainder. Defining \(V_O\) by regression does not remove selected residuals.

The literal CLOCK \(T=\int_{K^c}D\,d\eta_t\) requires matching the donor measure, normalization and coordinates of escaped labels. The new complement bound pays its original angular field at PROFILE's \(\mu/q\) cost. Charging it instead to a constructed field remainder is not silently identified with the literal \(T\) convention. The remaining consumer inequality is \(\int T\le F_T\) in that representation. No differential equation for \(T\) is used.

With \(E_g=2c_b\), the paid \(c\) contribution is \(O(c_b)\), and primary candidate moments are \(O(c_b+K_Y\sqrt{c_b})\). Conservative residual constants can be fixed uniformly over a small fixed \(c_b\) interval. These terms are compatible with a small passage allowance. The complete inequality \(\int f_*\le e_*/(4C_{\rm pass})\) still needs strips, full c-form reduction and the donor/first-moment representation. The audit stops there.

## Source provenance

Sources were re-read from **TodManlaibaatar/OOD-reversals-theory**, default branch **main**, on October 22, 2026, with GitHub read-only. Roadmap v1.11's S2 update, assembly requirements and ledger 15–18 govern this increment. Paths and fetched Git blob identifiers follow. No prior increment, foundation or checkpoint is edited. No numerical experiment, sign grid, saved trajectory or interval arithmetic is a premise.

| Source | Git blob SHA |
|---|---|
| [00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md) | `39a45bf78d2c47f5868c63918937c6079395caae` |
| [03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex) | `f00459b5ca412eb86b0893adb64766e2c10d5590` |
| [03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex) | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` |
| [03_passage_AN03/AN03_c_form_field_reduction_v1_review.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_c_form_field_reduction_v1_review.md) | `9d1a9fbb91f25821363c0d2a3ef2b38e6f88faf6` |
| [03_passage_AN03/AN03_c_form_field_reduction_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_c_form_field_reduction_v1.tex) | `d6e92da35a9d510201946fa6851c2c55740c1ff0` |
| [03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex) | `a490ea323e45e61c1a58301554b89ad84cb02605` |
| [03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex) | `8de0d85c64a3d51f3bd9c3662baf2efae0737373` |
| [03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex) | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` |
| [03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex) | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| [03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex) | `49e352002b4c699338ac99a4d55d51c60760ea86` |
| [02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex) | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| [02_entry_AN02/AN02_secondary_entry_profile_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_secondary_entry_profile_v1.tex) | `c7c857ec10b7f7b2cf42d1cdb452c50edc735587` |
| [02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex) | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` |
| [03_passage_AN03/AN03_local_rate_mean_tracking_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_local_rate_mean_tracking_v1.tex) | `eb1fa397d1f0d9b0e3aea1698b9960726e739fa8` |
| [02_entry_AN02/AN02_Q2_entry_contracts_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_Q2_entry_contracts_v1.tex) | `b149537025e130801fc55b9e49c365c158eee17b` |

Q2EC was additionally checked for the explicit clock-seed power of (A_q). External named statements in the TeX are intentionally cited by source name rather than unresolved cross-file LaTeX references.

## Artifact validation

The final TeX compiles successfully to nine pages with no compiler warnings or overfull boxes. All 39 labels are unique and have the requested prefix; all 42 internal reference occurrences resolve. SHA-256 checks confirm all 58 pre-existing workspace files are unchanged. The source ZIP is verified to contain exactly the TeX and this review note, byte-for-byte, with no PDF or auxiliary files. These are artifact checks, not mathematical or numerical proof premises. GitHub was not modified.
