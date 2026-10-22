# AN03 c-form field reduction v1 — review note

**Status: stopped at an unlisted S2 dependency. The requested full c-form theorem is not proved.** The pair contains a closed primary-cohort selected-gate estimate, explicit candidate non-core moments with a negative-part bound, and a radial state identity. It does not assume the missing secondary or outside budgets to turn these into a conditional passage theorem.

Companion: **AN03_c_form_field_reduction_v1.tex**. New label prefix: **an03cfrv1:**. The source ZIP contains the TeX and this review note.

## Exact obstruction

The Oct 21 route proposes charging the secondary cohort using
\[
E_\Sigma(t)\le C_\Sigma\{q^5+q^{\Gamma_\nu}H(t)\},
\qquad \Gamma_\nu>3/10,\quad t_0\le t\le t_*.
\]
In LCRC this is the **secondary** lemma, whose proof explicitly retains all three contracts:

1. The original entry profile.
2. The pre-exit distance envelope on the same stopped interval.
3. The capped radial gain at every intermediate endpoint.

SEP proves the first and explicitly leaves the other two open. The guards in this task control \(J_{G_+}+J_\Sigma\), \(E_{G_+}\), the integrated first residual entry, and the cross residual. They do **not** include either S2 contract or the secondary energy estimate.

The unclosed integrated quantity exposed by the proved estimates is
\[
\mathcal U_\Sigma(t_*)=
\int_{t_0}^{t_*}\left(E_\Sigma+K_Y\sqrt{E_\Sigma}\right)dt
\stackrel{\text{needed by this charge}}{=}o_q(1).
\]
If the cited secondary energy estimate were available, \(H\le E_g\) and \(t_*-t_0=O(\ell)\) would give
\[
\mathcal U_\Sigma\le
C(t_*-t_0)\left[
q^5+q^{\Gamma_\nu}E_g+
K_Y(q^{5/2}+q^{\Gamma_\nu/2}\sqrt{E_g})
\right]=o(1).
\]
The positive powers are adequate. The failure is the unavailable premise, not the exponent or a bounded factor. An entry estimate \(E_\Sigma(t_0)=O(q^5)\) does not itself supply the required estimate at later endpoints.

There is a separate outside-budget distinction. The generic full angular-field and receiver-derivative charge is \(C\mu_{\mathcal B}/q\), requiring an integrated budget. LCRC retains only \(\sup\mu_{\mathcal B}/q=o(1)\). On a logarithmic interval this does not imply \(\int\mu_{\mathcal B}/q=o(1)\): the scalar budget \(\mu_{\mathcal B}/q=\ell^{-1/2}\) on an interval of length \(\ell\) has integral \(\sqrt\ell\). This is a counterexample to that **budget inference**, not an asserted initialized network trajectory. MOMC's integrated outside bound ends at \(t_h=t_0\).

Even granting LCRC's retained core chart and mass budget does not repair the secondary dependency. Those state budgets are themselves separate from the four residual guards. Likewise LCRC's improved \(H_{G_+}\le(9/8)c_b+o(1)\) uses the secondary charge; it cannot be imported from the energy guard alone to conclude \(\int c=O(c_b)\).

This is **not** a claim that the desired initialized theorem is false, or that no different proof can follow from the dynamics. It records the exact unlisted hypothesis encountered in the suggested source-based route. The stop rule applies at that point, so no attempt was made to prove S2, run another passage, or substitute an assumed budget.

## What is rigorously closed

| Requested part | Result in this increment |
|---|---|
| (a) \(V,K_w\) | Exact receiver-independent candidate moments \(V_O=-\mathbb E_{P_2}[(f_O)_1X_2]/(qQ)\), \(K_O=\mathbb E_{P_1}[(f_O)_2X_1]/q\), with signs and mixture factors checked. The primary contribution has exponentially small negative part. The secondary/outside negative part is bounded explicitly but its integral remains unpaid. |
| (b) Selected residual | A value-and-scaled-receiver-derivative estimate for every cohort; an integrable small-fixed primary estimate under the stated guards; and a total decomposition with the secondary term retained. Global regression orthogonality never removes the selector. |
| (c) Full field remainder | **Not closed.** No bound \(\int\epsilon_F\le\kappa(C_0,c_b)+o(1)\) is asserted for the complete two-component field or its induced \(\ell^1\) derivative norm. The primary selected-moment bound is only a subset of this requirement. |
| (d) Strong radial equation | An exact original-flow state reduction \((\log m)'=1-\kappa_1+\delta_m\), with explicit error whenever the core donors and receiver are in the stated fixed charts. Its integrated remainder retains \(E_\Sigma\) and outside mass. Neither continued core geometry nor \(B_s\) is inferred. |

### Selected-moment calculation

For any cohort \(S\), define
\[
c_S=Q^{-1}\mathbb E_{P_2}[X_2(f_S)_2],\qquad
g_S=(f_S)_2-c_SX_2,\qquad
\mathcal D_S(x)=\mathbb E_{P_2}[g_SX_2\,1_{\{a_{qx}\cdot X>0\}}].
\]
On a fixed receiver chart,
\[
|c_S|+\|\mathcal D_S\|_{W^{1,\infty}_x}
\le C_{L_c}(E_S+q\sqrt{E_SJ_S}).
\]
The notation in the TeX uses the equivalent supremum of value plus first derivative. The bound is independent of donor signs or angles.

The derivative is obtained directly by writing \(X=(qZ,V)\), \(V\sim N(\rho,q^2)\), and \(t_x=\tan(qx)/q\):
\[
\frac{d}{dx}\mathbb E[(f_S)_2X_2\,1_{\{Z+t_xV>0\}}]
=t_x'\mathbb E_V[V^2(f_S)_2(-qt_xV,V)\phi(t_xV)].
\]
At this boundary,
\[
|(f_S)_2(-qt_xV,V)|
\le2|V|(E_S+q|t_x|\sqrt{E_SJ_S}).
\]
This bounds the scaled receiver derivative without an untracked \(1/q\) loss. Gaussian domination justifies differentiation.

For \(G_+\), the full-gate decomposition is kept exact:
\[
(f_{G_+})_2=A_+X_2+B_+X_1+N_+,\quad
A_+=\int W_2U_2,\quad B_+=\int W_2U_1,\quad
N_+=\int W_2(U\cdot X)_-.
\]
RCET gives \(W_2>0\), so \(N_+\ge0\), and
\[
c_{G_+}=A_++\tau_+,\quad
g_{G_+}=B_+X_1+N_+-\tau_+X_2,\quad
\tau_+=Q^{-1}\mathbb E[X_2N_+].
\]
The selected \(X_1X_2\) moment and its scaled derivative are \(O_{L_c}(q)\), giving \(O(q\sqrt{E_{G_+}J_{G_+}})\).

The negative-gate value is bounded by RCET's growing-margin tail. For its derivative, choose \(C_0\) small enough that \(q|t_xU_1|\le U_2/2\) throughout the receiver chart. On the receiver boundary the negative part then vanishes for \(V\ge0\). Its derivative costs only the Gaussian event \(V<0\). This proves
\[
\|\mathcal D_{G_+}(t)\|_{W^{1,\infty}_x}
\le C_{L_c}\left[
q\sqrt{E_{G_+}J_{G_+}}+\mu_{G_+}\mathcal T_+(t)
\right],
\]
where
\[
\int\mathcal T_+\le C_{\rm RCET}(C_0+q^2(t_*-t_0)).
\]
Thus, under the requested guards,
\[
\int\|\mathcal D_{G_+}\|_{W^{1,\infty}_x}
\le C_{L_c}C_{\rm RCET}E_g C_0+o_q(1).
\]
This proof uses RCET on the stopped interval, not LCRC's conditional secondary conclusion.

The coefficient difference is exactly
\[
A_+-c=-(c_\Sigma+c_{\mathcal K}+c_{\mathcal B}+\tau_+).
\]
Summing cohort regression defects gives the total selected term. A charted core contributes \(O(q^2\mu_{\mathcal K})\) through its **second** output. Its first output is not discarded: it remains in MOMC's order-one strong overlap term.

### Non-core sign audit

For \(O=G_+\cup\Sigma\cup\mathcal B\), the exact moment definitions above agree with LOC's leading moments for weak coordinates
\[
U/\sqrt m=(qu,1)+O(q^2),\qquad
W/\sqrt m=(-qv,1)+O(q^2).
\]
No bounded weak chart is assumed for the actual non-core population.

The negative-part estimate is
\[
(K_O)_-\le C\left[
q^{-1}\mu_{G_+}e^{-c/q^2}
+E_\Sigma+\frac{\sqrt{E_\Sigma J_\Sigma}}q
+\frac{\mu_{\mathcal B}}q
\right].
\]
It follows from \(W_2>0\) on the primary group, Gaussian negative-\(X_1\) tails, and cancellation-free output norm estimates for the other groups. Also
\[
|V_\Sigma|\le C\left[J_\Sigma+\frac{\sqrt{E_\Sigma J_\Sigma}}q\right].
\]
Taking \(K_w=(K_O)_+\) is permissible algebraically, but puts \((K_O)_-/2\) into the \(y\)-remainder. This operation does not prove a small integral. Defining \(V_O\) by regression similarly leaves selected moments of its residual; the full c-form is not obtained merely by naming the moment.

### Radial identity

At a charted core state with \(\mu_{\mathcal K}\le\overline M_{\mathcal K}\), the exact radial equation gives
\[
(\log m)'=1-\kappa_1+\delta_m,
\]
\[
|\delta_m|\le C_{L_c,R}\left[
q^2(1+\overline M_{\mathcal K}+M_{\rm res})
+J_G+q\sqrt{E_GJ_G}+\mu_{\mathcal B}
\right].
\]
Here \(M_{\rm res}\) is the task's cross-residual guard constant, renamed to distinguish it from strong mass. The diagonal loss bound controls receiver-gate removal on \(P_1\). The \(P_2\) contribution to \(R_{11}\) is \(O(M_{\rm res}q^2)\). The remaining angular factors are expanded only on the fixed receiver chart.

On an interval with that state geometry, the integral is bounded by
\[
C_{L_c,R}\left[
q^2(1+\overline M_{\mathcal K}+M_{\rm res}+K_Y^2)(t_*-t_0)
+q^2K_Y\int\sqrt{E_g+E_\Sigma}
+\int\mu_{\mathcal B}
\right].
\]
This is an explicit radial input for a future learning-integrability argument, not a proof of \(B_s\) or of a mass law after \(t_h\).

## Constants and guard dependence

| Quantity | Status and allowed dependence |
|---|---|
| \(\rho\in[13/20,7/10]\), \(Q\ge169/400\) | Fixed model box. |
| \(L_c\ge79/51\), core donor radius \(R\) | Fixed before all residual guards. No radius \(R(M_{\rm res})\) is introduced. |
| \(C_{L_c}\), \(C_{L_c,R}\), Gaussian tail constants | Depend only on the displayed radii, ratio box, and fixed Gaussian moments; the radial estimate additionally uses the initialization/loss constant. |
| \(\overline M_{\mathcal K}\) | An explicit state-premise in the radial lemma, not proved here. A later trajectory application must provide it independently of residual guards. |
| \(B,E_g,K_Y,M_{\rm res}\) | Exactly the stated fixed guards. They do not bound \(E_\Sigma\) by definition. |
| RCET \(C_*,C_{\rm RCET}\), \(b_*=Q(1-c_b)/2\) | Proved stopped-interval constants. Guard dependence occurs in the coefficient of \(C_0\) or vanishing terms. |
| Admissible \(C_0\) | Small enough for RCET and for the fixed receiver-boundary margin \(q|t_xU_1|\le U_2/2\); may depend on the previously fixed guards and \(L_c\). |
| \(L_T\) | The prescribed logarithmic duration constant. |
| \(V_O,K_O\) | Exact state moments, not assumed uniform constants or small forcings. Unpaid contributions remain visible. |
| \(C_\Sigma,C_D,C_m,C_g,\beta_0,\nu\) | Belong to the unproved-on-this-interval S2 package; they are displayed only to identify the missing source hypotheses, not adopted. |
| \(\kappa(C_0,c_b)\) | No complete-field function with the requested limiting property has been proved. Only the primary selected-term coefficient is closed. |

No guard dependence is hidden in an order-one Gaussian or chart constant. The core mass bound, full forcing budget, and outside integral are not manufactured from the residual guards.

## Source provenance

Roadmap **v1.8**, S0 assembly requirements and S3's Oct 21 refined route, was read from the repository, along with the requested proof sources. GitHub access was read-only. The S2 text was inspected solely to audit the hypotheses of the secondary charge, not to start S2.

Repository: **TodManlaibaatar/OOD-reversals-theory**, default branch **main**. Git blob identifiers:

| Source | Git blob SHA |
|---|---|
| Roadmap v1.8 — 00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md | 34973d788af38ca77f23bf5cebf570ef9972e124 |
| CLOCK — 03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex | 8de0d85c64a3d51f3bd9c3662baf2efae0737373 |
| LCRC — 03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex | defc7033fb8c9f49cbfb8b9b278ca71aa34925ac |
| RCET — 03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex | 49e352002b4c699338ac99a4d55d51c60760ea86 |
| BULK — 03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex | 66d3e66aaf99567440a9ebe84fd38c40b047ac83 |
| MOMC — 02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex | 539427063c4a08551ce4cb8efe41dab61cde609c |
| Q2EC — 02_entry_AN02/AN02_Q2_entry_contracts_v1.tex | b149537025e130801fc55b9e49c365c158eee17b |
| SEP — 02_entry_AN02/AN02_secondary_entry_profile_v1.tex | c7c857ec10b7f7b2cf42d1cdb452c50edc735587 |
| LOC — 03_passage_AN03/AN03_local_rate_mean_tracking_v1.tex | eb1fa397d1f0d9b0e3aea1698b9960726e739fa8 |

The weak-chart signs were also checked against the existing local checkpoint P, equation **pa:charts**. No numerical calculation, grid, experiment, saved trajectory, or interval arithmetic is a premise. The proof uses Gaussian integration, boundary differentiation with domination, cohort Cauchy--Schwarz bounds, and the already proved RCET margin.

No prior file was modified. No consolidation, GitHub mutation, evolution of the complement moment, S2 gain/distance proof, CLOCK passage application, or selection argument was performed.

Artifact checks: the final TeX compiled successfully; all 27 labels are unique and use the requested prefix, and all internal references resolve. SHA-256 checks confirm that all 40 pre-existing workspace files are unchanged. The source ZIP is checked to contain exactly this review and its companion TeX, byte-for-byte, with no PDF. These are artifact checks, not numerical proof premises.

