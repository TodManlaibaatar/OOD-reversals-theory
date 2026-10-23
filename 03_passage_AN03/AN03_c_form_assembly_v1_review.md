# AN03 c-form assembly v1 — review note

Companion: **AN03_c_form_assembly_v1.tex**. New label prefix: **an03cfav1:**. The source ZIP contains the TeX and this review only.

**Result:** All four tasks close as stopped-form implications with the specified retained strip budget. The increment constructs the core-only c-form, proves the complete value and induced receiver-derivative remainder bound, budgets CLOCK's full forcing, and checks the actual entry data for a conditional passage corollary. It does not prove the strip budgets or run the joint weak-passage bootstrap.

The proof uses S2CP's conclusions on its stated stopped interval, including its coarse c-form guard. It then derives the explicit representation and a stricter field allowance. This is a refinement suitable for a joint bootstrap, not an independent unconditional removal of the S2/S3 dependency. The retained guards are listed below.

## Task status

| Task | Status | Result / remaining inequality | Constant dependencies |
|---|---|---|---|
| 1. Representation | **Closed** | Fixed strong family and core are both \(\mathcal K\), hence \(T=0\). Uniform mass capping preserves the normalized label law. Value/derivative error is \(C_{L_c,R}(\mu_K-1)_+\), with integral \(C_{L_c,R}d_q=o(1)\). No remaining representation inequality. | Fixed radii, Gaussian/model bounds; no residual guards in the leading normalization constant. |
| 2. Full remainder | **Closed on the prescribed stopped interval** | \(\int\epsilon_F\le C_FC_{L_c}C_{\rm RCET}C_0E_g+C_{\rm out}F_{\mathcal S}+o(1)\), where \(\epsilon_F\) bounds the sum of value and induced \(\ell^1\) receiver-derivative norms. No unlisted term remains. The strip bound is retained, not proved. | Fixed chart/core constants; RCET constants may depend on fixed residual guards. Remaining guard dependence multiplies vanishing scales. |
| 3. CLOCK forcing | **Closed with explicit small-strip condition** | Correct \(1/Q\) retained: \(\int f_*\le \frac{10eE_g}{9Q(1-c_b)}+\frac{C_V(E_g+K_Y\sqrt{E_g})}{Q(1-c_b)}+C_FC_{L_c}C_{\rm RCET}C_0E_g+C_{\mathcal S}F_{\mathcal S}+o(1)\). With \(E_g=2c_b\), constants can be fixed uniformly and the non-strip part tends to zero. | CLOCK \(C_{\rm pass},g,e_*\) are independent of \(c_b,C_0\). Explicit uniform LCRC guard construction is given. |
| 4. Passage hypotheses | **Closed conditionally** | \(e_0=o(1)\), clock defect \(D_-=o(1)\), \(H_b=5c_b/4\) from pointcap, and \(r_0L_b=O(q^\chi)\). The c-form now supplies the actual mean/shape inequalities. CLOCK gives \(e\le3e_*/4\), \(r_K\le2\mathcal A=O(q^\chi)\), \(\int r_K\le2\mathcal A/a_b\). | Conditional on the other S2CP/LCRC stopped inputs and sufficiently small retained strip budget. No assertion that all those guards continue to \(t_b\). |

There is no stopped task caused by a false reviewer premise. Two selected-moment estimates not present in CFR's displayed statement were needed; they are proved here rather than added as hypotheses.

## 1. Why core-only donors and normalization are legitimate

CLOCK cfield allows any fixed strong family with positive instantaneous radial weights. Its proof uses LOC's donor cancellation and coherent \(G_M\) comparison pointwise, and explicitly does not require a logistic mass law or constant normalized weights. Choose that family to be the fixed TAILREP core \(\mathcal K\).

Set
\[
\widetilde\mu_s=\mu_s\min(1,\mu_K^{-1}),\qquad
\widetilde M=\min(\mu_K,1).
\]
The core has entry mass \(1/2-o(1)>0\), and its positive weights remain positive. Moreover
\(\widetilde\mu_s/\widetilde M=\mu_s/\mu_K\).
Thus the essential supremum defining the core radius and the normalized label law are unchanged. The complement of the core *within the chosen strong family* is empty, so \(T\equiv0\). Physical complementary labels are still charged in the actual field.

For \(\delta=(\mu_K-1)_+\) and \(\nu_s=\mu_s/\mu_K\), twice the field correction is exactly
\[
\left(\delta x-\rho\delta\int F(\rho x,\rho\xi)\,d\nu_s,\quad
\delta y-\delta\int\eta\,d\nu_s\right).
\]
Both the kernel and its first receiver derivative are bounded on the fixed donor/receiver squares. This proves the value and induced derivative cost \(C_{L_c,R}\delta\). S2CP's positive-part identity pays its integral. No derivative of the normalization factor is taken. The rescaled weights are a donor representation of the field with its difference charged to the remainder; they are not asserted to satisfy the original radial ODE.

The reference remains MOMC's actual original characteristic. It is not reset to \((a_\rho,a_\rho)\) or evolved under \(G_M\).

## 2. The additional selected moments

Under \(P_2\), write \(X=(qZ,V)\), \(V\sim N(\rho,q^2)\), and \(I_x=1_{\{Z+t_xV>0\}}\), \(t_x=\tan(qx)/q\). For \(p_{i,S}=Q^{-1}\mathbb E[(f_S)_iV]\), define \(g_{i,S}=(f_S)_i-p_{i,S}V\). The full angular expansion requires
\[
A_{1,S}=q^{-1}\mathbb E[g_{1,S}VI_x],\qquad
A_{2,S}=\mathbb E[g_{2,S}VI_x],\qquad
B_{2,S}=\mathbb E[g_{2,S}ZI_x].
\]
Only \(A_2\) is CFR's displayed selected moment.

For arbitrary cohorts, balance gives
\[
|(f_S)_1(qZ,V)|\le2qJ_S|Z|+2\sqrt{E_SJ_S}|V|,\quad
|(f_S)_2(qZ,V)|\le2q\sqrt{E_SJ_S}|Z|+2E_S|V|.
\]
The receiver derivatives are boundary moments:
\[
\partial_x\mathbb E[hVI_x]
=t_x'\mathbb E[V^2h(-qt_xV,V)\phi(t_xV)],
\]
\[
\partial_x\mathbb E[hZI_x]
=-t_xt_x'\mathbb E[V^2h(-qt_xV,V)\phi(t_xV)].
\]
Polynomial Gaussian domination therefore proves
\[
\|A_{1,S}\|_{1,\infty}\le C(J_S+\sqrt{E_SJ_S}/q),\quad
\|A_{2,S}\|_{1,\infty}+\|B_{2,S}\|_{1,\infty}
\le C(E_S+q\sqrt{E_SJ_S}).
\]
For \(\Sigma\), S2CP \(U_\Sigma\) pays these integrals.

For \(G_+\), use exact linearization in both output components:
\[
(f_{G_+})_i=L_{i1}X_1+L_{i2}X_2+N_i,\qquad
N_i=\int_{G_+}W_i(U\cdot X)_-.
\]
Regression removes \(L_{i2}X_2\). The linear \(X_1\) parts cost \(J_+\) in \(A_1\) and \(q\sqrt{E_+J_+}\) in \(A_2,B_2\).

The important first-output scaling is
\[
\mathbb E(u\cdot X)_-^2=q^2H_2(-\rho u_2/q)
\le Cq^2e^{-c(u_2/q)^2}.
\]
Cauchy–Schwarz against \(V\) or \(Z\) cancels the explicit \(1/q\) in \(A_1\). No sign of \(W_1\) is assumed. On the receiver boundary, RCET's margin makes \(U_2-qt_xU_1\ge U_2/2\). Hence the negative part vanishes for \(V\ge0\); the derivative remainder is paid by the exponentially small event \(V<0\), even after division by \(q\).

RCET's growing margin yields the same integrable tail type as CFR, with possibly enlarged fixed constants:
\[
\int\mathcal T\le C_{\rm RCET}(C_0+q^2L_T\ell).
\]
The combined primary selected cost is therefore
\(C_{L_c}C_{\rm RCET}C_0E_g+o(1)\).
Global regression orthogonality never removes a receiver selector.

## 3. Full field term ledger

MOMC's core kernel proof extends from \(M\le1\) to a fixed mass bound \(M_K\) by linearity in the donor measure. Its error becomes \(C_{L_c,R}q^2(1+M_K)\). The order-one first core output stays in the overlap kernel; only the core's second \(P_2\) output and its response coefficient have \(O(q^2\mu_K)\) cost.

For the non-core \(P_1\) terms, the key exact identities are
\[
\mathbb E_{P_1}[(f_G)_iX_2]
=q^2\int_G W_iU_2\,\mathbb P_{P_1}(U\cdot X>0)\,d\lambda_0,
\]
and \(|\mathbb E_{P_1}[(f_G)_1X_1]|\le C(J_G+q\sqrt{E_GJ_G})\).
Receiver gate removal has exponentially small value/derivative cost on the fixed chart. Thus the \(P_1\) leading non-core contribution to \(2F_y\) is exactly \(-K_G\); the other terms vanish after integration.

For \(P_2\), write \(T_2=\mathbb E[V^2I_x]\), \(T_1=\mathbb E[VZI_x]\). Then \(T_2=\lambda\Phi(\rho x)+O_{C^1}(q^2)\) and \(T_1=\rho\phi(\rho x)+O_{C^1}(q^2)\). The expansion is
\[
2(F_G^{P_2})_x=V_GT_2-yc_GT_2-A_{1,G}-yA_{2,G}+\mathcal E_x,
\]
\[
2(F_G^{P_2})_y=-c_G(T_1+xT_2)-B_{2,G}-xA_{2,G}+\mathcal E_y.
\]
Its trigonometric error is \(O_{C^1}(q^2[E_G+J_G+\sqrt{E_GJ_G}/q])\). Since \(T_1+xT_2=\rho K(\rho x)+O_{C^1}(q^2)\), these are precisely the response terms required by cfield, with all selected defects accounted for.

| Contribution | Integrated value and induced receiver-derivative budget |
|---|---|
| Target and core finite-noise kernels | \(Cq^2(1+M_K)L_T\ell\). |
| Core second output and replacement of \(c-c_K\) by \(c\) | \(Cq^2M_KL_T\ell\). |
| Donor-mass cap | \(C_{L_c,R}d_q=o(1)\). |
| Primary selected residuals | \(C_FC_{L_c}C_{\rm RCET}C_0E_g+o(1)\). |
| \(P_1\) transverse moments and chart corrections | \(Cq^2\ell(1+M_K+M_{\rm res}+K_Y^2+K_Y\sqrt{E_g+1})+o(1)\). |
| Secondary moments | \(C\mathcal U_\Sigma+o(1)\). |
| Strong complement | \(Cq^{\Delta_\nu}\ell\), from S2CP and PROFILE. |
| Original Q3 interior | \(Cq^9\ell\), from GESG and PROFILE. |
| Two strips | \(C_{\rm out}F_{\mathcal S}\), retained. |
| \((K_O)_-\) | Primary Gaussian error, \(C\mathcal U_\Sigma\), and \(C\int\mu_B/q\), from CFR negative. |

The outside output itself and the substitution of its moment contributions \(V_B,K_B,c_B\) are both bounded at PROFILE's \(\mu_B/q\) cost. This prevents double counting a missing leading contribution as a small error.

Bare \(O(M_{\rm res}q)\) cross entries are not discarded after division by \(q\). Their order-one contributions are the retained moments and selected terms. Only the extra chart/trigonometric factors leave \(O(q^2M_{\rm res})\) errors.

## 4. Forcing constants and entry audit

Choose \(V=V_O\), \(K_w=(K_O)_+\), and put \((K_O)_-/2\) in the second field remainder. The exact original-flow forcing is now
\[
f_*=c+|V_O|+(K_O)_++\epsilon_F,\qquad T=0.
\]
S2CP's c budget retains the coefficient \(1/Q\); its VKbudget and the new remainder theorem give
\[
\int f_*\le
\frac{10eE_g}{9Q(1-c_b)}
+\frac{C_V(E_g+K_Y\sqrt{E_g})}{Q(1-c_b)}
+C_FC_{L_c}C_{\rm RCET}C_0E_g+C_{\mathcal S}F_{\mathcal S}+o(1).
\]

LOC's \(G_M\) matrix has a uniform spectral bound
\(\gamma\ge\gamma_*=1183/20800\).
Take a fixed enlargement \(C_{\rm pass}\) of the uniform LOC coefficient \(724/51\) and the remainder norm conversions, and set
\[
g=\gamma_*/2,\quad
e_*=\min(1/4,\gamma_*/(2C_{\rm pass})),\quad
K_{\rm pass}=C_{\rm pass}(1+C_{\rm pass}/g).
\]
These are independent of \(c_b,C_0\), and of the residual guards. The local core/reference neighborhood fits inside the chosen \(L_c=79/51+1\).

Uniformity of LCRC's residual constants is explicit: fix \(\bar c=1/4\), use \(B_s>\log2\), replace its conservative old energy budget by \(2+2\bar c\), its \(h_*\) by \(1+9\bar c/8\), and its lower clock rate by \((169/400)(1-\bar c)\). Its displayed formulas then choose fixed \(B,K_Y,M_{\rm res}\) valid for every \(0<c_b\le\bar c\). No \(1/c_b\) enters. RCET uses the same positive lower rate. The smaller actual energy guard \(E_g=2c_b\) has S2CP's pointcap slack.

Let \(P_{\rm allow}=e_*/(4C_{\rm pass})\). Choose \(c_b\) so that the first two forcing terms are at most \(P_{\rm allow}/4\). Choose admissible \(C_0\) so that the primary remainder term is at most \(\min(P_{\rm allow}/4,\overline F_F/4)\). Require
\[
C_{\mathcal S}F_{\mathcal S}\le
\min(P_{\rm allow}/4,\overline F_F/4).
\]
Choose \(q\) last for the remaining quarter. Then \(\int f_*\le P_{\rm allow}\) and \(\int\epsilon_F\le3\overline F_F/4\). If a retained strip budget is larger, the two quantitative budget theorems still hold, but the small-forcing passage corollary is not asserted.

The complete order is
\[
(\text{model},R,M_K,B_s,L_c,\bar c,C_{\rm pass},g,e_*)
\to(B,K_Y,M_{\rm res})
\to(\overline F_F,c_b,E_g,C_D,A_0,C_m)
\to C_0
\to(K(C_0),Z_\Sigma,\text{entry constants},C_\Sigma)
\to q.
\]
The small fixed upper bound on \(F_{\mathcal S}\) is specified before \(q\). The dependence of \(C_\Sigma\) on \(C_0\) is retained, as required by ledger 19.

At \(t_0\), MOMC gives the actual reference \(e_0=o(1)\). The fixed cutoff gives \(r_0\le c_*q^{\chi+kP/2}\). LCRC/BULK supply the clock cohort's \(\int\epsilon_{\mathcal C_q}\ge-D_-\) with \(D_-=O(q^{1/8}+q^2\ell)=o(1)\); the eta-zero cohort is not substituted for the clock.

S2CP and LCRC pointcap give \(H(t_*)\le9c_b/8+o(1)\), so use \(H_b=5c_b/4\). Together with \(H_0\asymp A_q^{-\lambda}q^k\),
\[
r_0L_b\le
Cc_*H_b^{\alpha/Q}A_q^{\lambda\alpha/Q}
q^{\chi+kP/2-k\alpha/Q}
=Cc_*H_b^{\alpha/Q}A_q^{\lambda\alpha/Q}
q^{\chi+kPq^2/(2Q)}
=O(q^\chi).
\]
The \(Q\)-versus-\(\lambda\) correction has the favorable sign and is kept explicitly. All three CLOCK radius thresholds are fixed positive constants, so this verifies them for small \(q\).

Finally, the mean and shape inequalities now follow from cfield for the *actual* common field. The passage corollary applies CLOCK at a stopped endpoint \(t_*\); it does not prove that other guards survive to the prescribed \(t_b\).

## Retained inputs and limits of the result

- The two fixed strip bounds remain \(\sup\mu_{\mathcal S}/q=o(1)\), \(\int\mu_{\mathcal S}/q\le F_{\mathcal S}\), with the displayed smallness for passage. No strip entry, gain or classification is proved.
- S2CP's other stopped residual, response, duration, core geometry/mass and reference conditions remain the working inputs. Its coarse field allowance is used to obtain S2 conclusions before the present explicit refinement. This dependency is exposed rather than asserted to disappear.
- The passage corollary strictly improves its local radius/reference bounds while those other inputs hold. Extending all guards together is the later joint bootstrap and is not performed here.
- The actual reference and all cohorts are fixed in label space. Artificial donor normalization is paid in the field and never used as an original radial mass law.
- No foundation, checkpoint or prior increment is modified; no selection, consolidation, GitHub mutation or numerical experiment is part of this work.

## Source provenance

The requested sources were read from the repository's default branch, read-only. The retrieved roadmap identifies itself as **v1.12 — October 23, 2026**; its S2/S3 updates and ledger 15–19 were checked. The following Git blob identifiers pin the actual texts used. External statements in the TeX are named source references, not unresolved cross-file LaTeX labels.

| Source | Git blob SHA |
|---|---|
| [00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md) | `43b3368548fd7a4b45a45858e955b0d942ea3ee8` |
| [03_passage_AN03/AN03_S2_closure_package_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_S2_closure_package_v1.tex) | `baeb8a7eb1e36ce86319782511b665944be1afda` |
| [03_passage_AN03/AN03_c_form_field_reduction_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_c_form_field_reduction_v1.tex) | `d6e92da35a9d510201946fa6851c2c55740c1ff0` |
| [03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex) | `8de0d85c64a3d51f3bd9c3662baf2efae0737373` |
| [03_passage_AN03/AN03_local_rate_mean_tracking_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_local_rate_mean_tracking_v1.tex) | `eb1fa397d1f0d9b0e3aea1698b9960726e739fa8` |
| [02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex) | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| [02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex) | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` |
| [03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex) | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| [03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex) | `a490ea323e45e61c1a58301554b89ad84cb02605` |
| [03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex) | `f00459b5ca412eb86b0893adb64766e2c10d5590` |
| [03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex) | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` |
| [03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex) | `49e352002b4c699338ac99a4d55d51c60760ea86` |
| [03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex) | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` |

## Artifact validation

The final TeX compiles to nine pages with no compiler warnings or overfull boxes. All 32 labels are unique and use the requested prefix; all 32 internal reference occurrences resolve. SHA-256 checks confirm all 35 pre-existing output files are unchanged. The source ZIP is verified to contain exactly the companion TeX and this review, byte-for-byte, without a PDF or auxiliary files. Compilation and file checks are artifact validation only, not mathematical proof premises.
