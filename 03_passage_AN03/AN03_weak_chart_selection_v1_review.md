# Review: weak-chart reduction and selection v1

Companion: AN03_weak_chart_selection_v1.tex  
Prefix: an03wcsv1:  
Date: 1 November 2026  
Scope: S4e, ending at a fixed logistic level inside the completed original weak passage.

## Result

**Parts A and B close.** The new original-flow weak inequality, for SRR's unchanged fixed-incoming-law norm, is

\[
D^+W_2\le[-\lambda(1-N)/2+N/2+\ell_B]W_2
            +20(E_s+d_0^{(w)}),
\qquad d_0^{(w)}=C_{\rm wcs}q^{1/20}.
\]

The coefficient is nonnegative, and its integral tends to zero uniformly over terminal levels below the fixed level \(h\). Thus \(L_*=1\) works for small \(q\), before choosing \(n\). Combining this with SRR's unchanged strong inequality and TAILREP's selection theorem gives

\[
E_s(t_n)+W_2(t_n)=O_n(q^{1/20}).
\]

The local strong guard is propagated by TAILREP only after both inequalities and its initial guard have been verified. No new assumption is retained in this selection theorem. The conclusion is \(p=2\) selection; it is not a uniform labelwise bound or a claim past \(t_n\).

| Step | Status | Result / limitation |
|---|---|---|
| 1. Inventory and weights | Closed | Consumer hypotheses are listed in TeX inventory. The fixed incoming measure is unchanged. There is no derivative-weight term in this norm calculation. |
| 2. Exact receiver field | Closed | Exact angular contractions and tangential Gaussian integration by parts give the growing-chart value reduction. All gate and polynomial terms are charged. |
| 3. Donors, moments and sign | Closed | The actual core moment is positive; non-core contributions remain explicit remainders. Current positive clock donors convert to the fixed incoming law with coefficient \(1+o(1)\). |
| 4. Weak error | Closed | Model-only \(C_w=20\); pointwise \(d_0^{(w)}=C_{\rm wcs}q^{1/20}\); nonnegative \(\ell_B\) with uniform integral \(o(1)\). |
| 5. Selection | Closed | An explicit fixed choice of \(n<h\) gives \(\Theta\le1/4\); every TAILREP hypothesis is discharged. Both terminal errors are \(O_n(q^{1/20})\). |
| 6. S5 interface | Closed within scope | Mass, moments, current-weight conversion, omitted fields and actual-clock phase are tabulated. Continuation and uniform selection remain out of scope. |

There is no unmatched inequality within the stated theorem, and no obstruction is reported. The audit below records two potentially invalid shortcuts that the proof explicitly avoids.

## Objects and hypotheses

The strong reference is the same actual characteristic used by MOMC, CFA and SRR. Neither the reference nor the comparator clock is reset. The norm is exactly

\[
\eta_s(db)=\frac{m(t_s,b)}{N_S(t_s)}d\lambda_0(b),\qquad
W_2(t)=\big\||u-U_*(N)|+|v-V_*(N)|\big\|_{L^2(\eta_s)}.
\]

The input and output conventions remain \(u=(\pi/2-\theta)/q\), \(v=(\psi-\pi/2)/q\). The selected set is the entire closed clock cohort, including its endpoint labels. WBR proves \(u>0\) on the entire required interval; no endpoint is discarded and no sign is inferred from the chart size.

| Invoked result or calculation | Complete operative hypotheses | Where supplied |
|---|---|---|
| RB completed passage | Original balanced initialized deep flow, \(\kappa=10\), closed ratio box, the fixed WPT/RB constant order and small \(q\). | Existing theorem; supplies positive response, completed guards, fixed populations, core geometry, outside and secondary budgets on \([t_0,t_b]\). |
| WBR return and late chart | Same original flow, closed clock cohort, admissible fixed upper level \(h\); interval ending at its first clock hit. | SRR retains an admissible smaller \(h\). MP places \(t_n<t_e<t_b\). Return and reached chart hold for every selected endpoint. |
| MP matching | Fixed \(S\), start at \(H=q^{1/8}\), WBR range and chart, exact auxiliary logistic mass, late interval \([t_s,t_e]\). | Used only on that interval. Its actual-clock phase and transverse theorem supply the necessary norms, rather than a supremum estimate alone. |
| SRR strong inequality | Its fixed reference and fixed incoming probability; model local constants; exact same logistic \(N\); admissible \(h\), fixed \(n<h\); up to the first exit \(E_s<\delta\). | All conventions retained. The weak inequality is proved on the same first-exit interval, and TAILREP later closes that guard. SRR is not altered. |
| Gaussian integration by parts | Exact Gaussian clusters; balanced ReLU output with finite mass; receiver gate independent of the integration variable; dominated integrability. | The new tangent rotation makes the receiver gate independent of \(Z_\perp\). Outputs have linear growth, and all Gaussian moments used are finite. |
| Removing the \(P_2\) receiver gate | Positive projected mean bounded away from zero; bounded total radial mass. | WBR's reached chart gives \(\cos(qu)\ge1/2\); RB gives bounded total mass. The absolute failed-gate contribution is exponentially small. |
| Core donor moments | Positive fixed core measure; bounded physical core chart; bounded mass. | RB core geometry and mass, plus the MOMC/CFA compact Gaussian moment calculation. No compact receiver hypothesis is imported into the weak chart. |
| PROFILE outside value cost | Exact balanced state, arbitrary receiver direction, finite outside mass, \(0<q\le1\), \(0<\rho<1\). | RB outside supremum. The matrix-value estimate is global; the bounded-coordinate derivative part is not used. |
| WEAK scalar comparison | Nonnegative comparison segment; positive donor measure; \(u+Y\ge0\); same-time receiver field; bounded comparator values. | WBR \(u>0\), AN06 \(U_*>0\), actual positive radial measure on \(S\), and \(Y\ge3/320\). |
| WEAK donor comparison | Donor Lipschitz constant one for \(F\); linear weak output moment; positive normalized probability; finite norm. | Exact kernel identity from P. Current measure is converted by SRR's value ratio, not differentiated. |
| AN06 selected branch | Defined leading selected branch, ratio box, \(0<N\le1/2\). | Exact \(N<2h<1/2\), hence \(0<U_*<1\) and \(0<V_*<11/10\). |
| TAILREP strongerror and weakerror | Nonnegative absolutely continuous errors; fixed positive \(g,C_s,C_w\); common pointwise \(d_0\); inequalities up to strong first exit; nonnegative integrable \(\ell_B\). | SRR and the new weakerror theorem; take the maximum of their pointwise additive constants. The norm has fixed labels and bounded support for each fixed \(q\). |
| TAILREP selection | Exact logistic mass, \(0<N_0<n<1\), terminal hit; return maintained separately; \(\int\ell_B\le L_*\); its exact small-gain and initial-guard inequalities. | Explicit constants and level choice below; WBR return; uniform \(L_*=1\); SRR \(E_0\), MP \(A_0\), and shared \(d_0\to0\). |

WEAK's original route to return additionally assumes unit leading strong mass, fixed normalized weights, \(Y\ge0\), bounded \(\rho K_s\), \(0\le Y\le Y_{\max}<2\phi(0)\), initial \(u\ge0\), and the strict margin

\[
C_u n+U_0^+\sqrt{N_0n}<\phi(0)-Y_{\max}/2,\qquad
C_u=\phi(0)+\frac{\phi(0)}{\lambda(1-n)}.
\]

That leading return theorem is not applied to the original flow. WBR has already proved original return with its own strict boundary argument. The new proof invokes the scalar derivative calculation inside WEAK's Wineq proof, whose hypotheses are checked separately above. The original \(M\ne1\) terms are retained and budgeted, rather than assuming unit physical mass.

## Exact field and signed terms

Let \(a=(\sin qu,\cos qu)\), \(p=(\cos qu,-\sin qu)\), \(b=(-\sin qv,\cos qv)\). The two exact velocity contractions are given in TeX exact, with the mixture factor two intact.

At \(u=0\), WBR integrates by parts in \(X_1\), since the receiver gate does not depend on \(X_1\). At general \(u\), that independence is false. The valid extension rotates to

\[
T=\sin(qu)Z_1+\cos(qu)Z_2,\qquad
Z_\perp=\cos(qu)Z_1-\sin(qu)Z_2.
\]

These variables are independent, the receiver gate is \(T>-\sin(qu)/q\), and integration by parts in \(Z_\perp\) leaves that gate untouched. At \(u=0\), this is exactly WBR's old integration variable. The resulting four projected target moments and the donor Stein identity are displayed and proved in TeX IBP.

The exact full \(P_2\) response coefficient is \(Q(1-c)\). Its replacement by \(\lambda(1-c)\) costs \(q^2\) times a coordinate. The other three global matrix entries are computed:

\[
B_{11}=q^2\left(1-\int W_1U_1P_{\rm gate}\right)=O(q^2),\quad
B_{21}=-q^2\int W_2U_1P_{\rm gate}=O(q^3),
\]
\[
B_{12}=-q\rho K_c+qQV_O+O(q^3).
\]

This retains the signs of the own-cluster drive and the core/weak linear moments. After the separate \(P_1\) calculation the leading values are exactly

\[
2u'=\phi(u)-\mathcal W_S(u)-Y\Phi(u)
 -(1-M)v\Phi(u)-\lambda(1-c)u+\mathcal R_u,
\]
\[
2v'=\rho K_c-\lambda\mathcal V_S-\lambda(1-c)v
 -(1-M)K(u)+\mathcal R_v.
\]

Here \(M=\mu_K\) is physical mass, \(Y=\int_Kmy\), \(K_c=\int_KmK(\rho x)\), \(\mathcal W_S=\int_SF(u,\widetilde u)d\mu_S\), and \(\mathcal V_S=\int_S\widetilde v\,d\mu_S\). The remainder bound is

\[
|\mathcal R_u|+|\mathcal R_v|
\le C_{\rm fixed}\{q^{1/10}+q(1+|u|+|v|)
                    +q^2(1+|u|+|v|)^3\}.
\]

This is a value estimate on the reached growing chart. No derivative of this remainder is claimed or needed.

### Growth and gate audit

The exact chart exponent is \(p_*=603/640\).

| Term | Allocation | Integral or pointwise size |
|---|---|---|
| \(q(1+\vert u\vert +\vert v\vert )\) | Additive \(Cq\) plus \(Cq\) times distance | Coefficient integral \(O(q\ell)\). |
| \(q^2\) times quadratic coordinate monomials | Additive \(Cq^2\) plus \(Cq^2(1+L)\) times distance | \(O(q^{677/640}\ell)\), with harmless faster powers. |
| \(q^2\) times cubic coordinate monomials | Additive \(Cq^2\) plus \(Cq^2(1+L^2)\) times distance | \(O(q^{37/320}\ell)\). |
| Apparent \(q^2vu^3\) from a crude \(\Phi\) estimate | Not used | Gaussian saturation gives \(\lvert\Phi(\sin(qu)/q)-\Phi(u)\rvert=O(q^2)\), so this contribution is only \(O(q^2\vert v\vert )\). |
| Receiver \(P_2\) failed gate | Absolute Gaussian moment, both sides | \(Cq^{-j}e^{-c/q^2}\), uniformly since \(\cos(qu)\ge1/2\). |
| Core \(P_1\) failed donor gate | Absolute Gaussian moment with the receiver indicator retained | Exponentially small on the fixed core chart. |
| Selected \(P_1\) gate | Kept exactly, then compared by conditional Gaussian integration | \(C[q+q^2L+q\vert u\vert +q^2\vert u\vert ^3]\). |
| Non-selected weak gates | Generic absolute selected-functional bound | Uniform in receiver; no sign or chart assumption on these donors. |
| All outside labels, including both strips | Global matrix-value cost | \(C\mu_B/q\le Cq^{1/10}\). |

The potentially inadmissible quartic is a bookkeeping hazard, not an obstruction: for \(u\ge0\) and \(qu\le1/2\), \(\sin(qu)/q\) lies between \(u/2\) and \(u\). The mean value theorem with the Gaussian derivative, rather than its global Lipschitz constant, gives the uniform \(O(q^2)\) estimate. Only \(K\), whose derivative does not decay at positive infinity, keeps the cubic error. That cubic is admissible. This proof uses boundedness of polynomial times Gaussian functions, not numerical checks.

## Donors, moments and sign

The selected overlap calculation keeps the exact joint receiver/donor Gaussian representation until a controlled value comparison. MP's transverse theorem supplies

\[
\int_Sm(1+|\widetilde u|+|\widetilde v|+\widetilde u^2+\widetilde v^2)
\le C_{\rm fixed}.
\]

Thus donor cubic errors cost \(q^2L=O(q^{677/640})\); they are not estimated using mass times the entire supremum cubed. The receiver-gate change is controlled by conditioning on \(Z_1\) and integrating the Gaussian density between the two thresholds.

For the omitted cohorts the nonlinear \(P_1\) functional is bounded by

\[
C\left(E_T+q^{-1}\sqrt{E_TJ_T}\right).
\]

Together with SRR's linear moment estimates, \(P_q\) costs \(O(q^{1/8})\), \(\Sigma\) costs \(O(q+q^{\Gamma_\nu/2})\), and \(B\) costs \(O(q^{1/10})\). The \(q^2\) transverse contribution to \(\mu_{P_q}\) is kept. MP's accounting statement alone is not treated as a field estimate.

The actual core moment satisfies \(Y\ge(9/320)M\ge3/320\). The unexpanded moment \(q^{-1}\int_KW_2U_1\) differs by \(O(q^2)\), so it is positive as well. Non-core strong-output terms are explicitly charged in the field remainder; no sign is assigned to them. This is sufficient because contraction uses a comparator built from the actual positive core moment, with every omitted original contribution paid.

At the comparator input, the exact donor Lipschitz estimate and linear output moment give coefficient one before the factor \(1/2\). This coefficient is kept rather than importing SRR's coarser \(8NW_2\) bound:

\[
\int_S\bigl(|\widetilde u-U_*|+\lambda|\widetilde v-V_*|\bigr)d\mu_S
\le N(1+\epsilon_w)W_1(\eta_s)\le N(1+\epsilon_w)W_2,
\]
\[
\epsilon_w=
\left[\frac{N_S}{N}\|\omega\|_\infty-1\right]_+
\le C[D_q+d_{\rm ph}+q^2(1+L^2)].
\]

The bounded comparator mass error \(O(|N_S-N|)\) is additive. The \(o(1)\) excess coefficient is assigned to \(\ell_B\).

## Weak inequality and its budgets

The comparator input derivative is

\[
-\frac12\left[(u+Y)\phi(u)
 +\phi(u)\int_S(\widetilde u-u)_+d\mu_S+\lambda(1-c)\right]
\le-\lambda(1-c)/2
\]

on the segment between actual and selected nonnegative inputs. The donor measure is the actual positive radial measure. This derivative belongs to the leading-form comparator; the finite-noise remainder needs only value bounds.

A concrete allocation is

\[
\ell_B=\frac{\lambda}{2}|c-N|+\frac N2\epsilon_w
 +C_{\rm fixed}\{|1-M|+q+q^2(1+L^2)\},
\qquad d_0^{(w)}=C_{\rm wcs}q^{1/20}.
\]

| Budget | Proved source / allocation |
|---|---|
| Pointwise core moment \(O(q^{1/20})\) | SRR corecollapse and RB core radius. |
| Core moment error proportional to \(E_s\) | At most \(3E_s\) before the velocity factor \(1/2\), since \(M\le2\) and \(\lambda\le49/100\). Model-only \(C_w=20\) suffices. |
| Physical mass defect | MP: coefficient integral \(O(q^{11/10}\ell)\), bounded comparator error \(O(q^{11/10})\). |
| Response versus logistic mass | MP: pointwise \(O(q^{1/8}+q^2\ell)\), integrated \(o(1)\). |
| Weight value excess | SRR plus MP; multiplied by \(N\), whose integral is bounded by the exact logistic formula. |
| Polynomial value errors | The growth table above; all coefficient integrals vanish on a duration at most \(20\ell\). |
| Omitted populations and finite moment corrections | Pointwise \(O(q^{1/10})\) or smaller; into the additive constant. |
| Derivative of normalized weights | No named term requires it. The norm has fixed labels. No such budget is constructed or asserted. |

The prefactors in \(d_0^{(w)}\) and the vanishing coefficient budgets may depend on already fixed passage constants and \(h\), but not on \(n\). The coefficient of \(E_s\), \(C_w=20\), is model-only. No integrated allowance is substituted for a pointwise \(d_0\).

All integrals are bounded first on \([t_s,t_e]\), not by a bound involving \(t_n\). Hence the uniform \(o(1)\) integral permits \(L_*=1\) before \(n\) is selected.

## Selection constants and hypothesis discharge

Keep SRR's \(\delta\), \(g=g_W\), \(C_s=980\), and admissible \(h\) unchanged. Set

\[
\lambda_{\min}=169/400,\quad g_{\min}=1183/41600,\quad
C_w=20,\quad L_*=1,\quad B_{\max}=e\,2^{1/(2\lambda_{\min})},
\]
\[
n=\frac12\min\left\{h,\frac14,
\frac{\lambda_{\min}g_{\min}}{64C_sB_{\max}C_w}\right\}.
\]

Then define TAILREP's constants with their exact coefficients:

\[
B_*=e(1-n)^{-1/(2\lambda)},\quad a_0=\lambda(1-n)/2,\quad
m_0=\min(g/2,a_0/2),
\]
\[
L_0=1+\frac{C_s(1+B_*)}{g-m_0},\quad K_0=2L_0,\quad
\Theta=\frac{C_sB_*C_wn}{(a_0-m_0)(g-m_0)}.
\]

The denominators satisfy \(a_0-m_0\ge\lambda_{\min}/8\), \(g-m_0\ge g_{\min}/2\). Thus

\[
\Theta\le\frac{16C_sB_{\max}C_wn}{\lambda_{\min}g_{\min}}\le1/4.
\]

The level is fixed, positive and strictly below \(h\). For small \(q\), \(N_0=q^{1/8}<n\), the logistic hit lies before \(t_e<t_b\), and WBR return remains valid. Set

\[
d_0=\max\{C_{\rm srr},C_{\rm wcs}\}q^{1/20}.
\]

SRR gives \(E_0=O(q^{1/20})\); MP gives \(A_0=O(q^{1/16})\) with the same incoming probability. Hence the exact initial guard holds for small \(q\). The new weak inequality and SRR's strong inequality have the same first-exit scope and the same additive constant after taking the maximum. This discharges every hypothesis of TAILREP selection.

The constant order is:

**WPT/RB → WBR → \(a_s=1/8,p=2\) → SRR's \(\delta,g_W,C_s\) → \(h\) → \(C_w,L_*\) → \(n\) → \(q\).**

The exact terminal bounds are reproduced as TeX Econclusion and Wconclusion. Since

\[
t_n-t_s=\frac{\ell}{8\lambda}
       +\frac1\lambda\log\frac n{1-n}+o(1),
\]

the initial-error term has rate \(q^{1/20+m_0/(8\lambda)}\). The additive defect is \(q^{1/20}\), and the incoming-spread term is \(q^{1/16}\). This proves the stated terminal rate \(O_n(q^{1/20})\).

## S5 handoff

| Quantity | Proved accuracy at \(t_n\) |
|---|---|
| Actual strong reference | \(E_s(t_n)=O_n(q^{1/20})\); local guard closed to \(\delta/2\). |
| Strong core first moment about selected atom | \(O_n(q^{1/20})\), using the unchanged core radius and reference selection. |
| Physical strong core mass | \(1+O(q^{11/10})\). |
| Weak distance under fixed incoming law | \(W_2(\eta_s)=O_n(q^{1/20})\). |
| Weak distance under current radial law | At most \(\\vert \omega\\vert _\infty^{1/2}W_2(\eta_s)=(1+o(1))W_2(\eta_s)\). |
| Selected radial mass and response | \(N_S/n=1+O_n(q^{1/8})\), \(c=n+O_n(q^{1/8})\). |
| Non-selected weak mass | \(O_n(q^{1/4})\), with the secondary and outside bounds separately retained. |
| Non-selected moment and overlap charges | \(O(q^{1/8})\) for \(P_q\), \(O(q+q^{\Gamma_\nu/2})\) for \(\Sigma\), \(O(q^{1/10})\) for \(B\). Other receiver-dependent transverse terms retain the explicit polynomial budget. |
| Outside mass | \(\sup\mu_B/q\le q^{1/10}\), and on this interval \(\int\mu_B/q\le20q^{1/10}\ell=o(1)\). |
| Actual-clock phase | \(t_n-t_0=Q^{-1}\log\{n/[(1-n)H_0]\}+o(1)\), with exact \(H_0\). |
| Entry-scale time | \(Q^{-1}[k\ell+\lambda\log A_q+\log(n/(1-n))+O(1)]\), because the entry seed is known only up to fixed constants in this expression. |

For the phase, SRR's pre-start bound retains \(c\le C(H+q^2+\mu_B)\), so its integral before \(t_s\) is \(o(1)\) by the backward clock and outside supremum. After \(t_s\), MP supplies \(\int|c-N|=o(1)\). Combining exact logistic integration with RB's exact clock and vanishing clock defect proves the table's \(o(1)\) timing statement. It does not pass through the terminal time \(t_b\).

S5 must handle compact-window transfer and continuation. Nothing here establishes a supremum-in-label selection bound, finite-noise pairwise contraction, or retention after \(t_n\). There is no new retained hypothesis for the theorem proved here.

## Provenance and artifact checks

README and roadmap v1.22 were re-read from the read-only repository for this task. The proof sources were fetched from the current default branch; their content SHAs are listed below. Repository prefix search returned no match for an03wcsv1:. Local prior files are checked separately for collisions and unchanged content.

Verification consists of analytic source and hypothesis inspection, reference and escape checks, compilation, and source archive integrity checks. No simulations, interval arithmetic, grid sign checks, saved trajectories or numerical premises were used. Existing increments, foundations, the checkpoint and GitHub are not modified. The downloadable source ZIP contains only the new raw TeX and review Markdown.

| Source path | Fetched content SHA |
|---|---|
| README.md | 5e7cab6fa255d8fcd2a2a54ba820208588885eea |
| 00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md | 1d9382bd10d8233c601e366e74cf3591209733cd |
| 03_passage_AN03/AN03_strong_reference_reduction_v1.tex | 6388f0192b970ebfae8604d7cab89dce37a25cfe |
| 03_passage_AN03/AN03_weak_transit_forcing_and_orbit_selection_v1.tex | 3a937aa25253b5773424a3f165f71d476157575a |
| 03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex | 1777839da3fa10ebf66e8560f7175678753c39b9 |
| 03_passage_AN03/AN03_weak_boundary_return_v1.tex | c1f18203cc99ca5ddcda9481ca1281d7debffa9a |
| 03_passage_AN03/AN03_matching_package_v1.tex | 9491bba4ec10f79acca277b1f0c4ddd92180a7aa |
| 01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex | cb458c933aa043cf0188fd11c46bf4246ffc91d8 |
| 03_passage_AN03/AN03_response_barrier_v1.tex | 5312b5093f3ed4f74063347df31ae5a29155255f |
| 03_passage_AN03/AN03_c_form_assembly_v1.tex | 341908c228092e9a818d98de3ec26591a1050364 |
| 03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex | 66d3e66aaf99567440a9ebe84fd38c40b047ac83 |
| 04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex | 9e102514ad0a491066a2f9eb8eb86e9a251c2b53 |
| 02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex | 3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a |
| 02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex | 539427063c4a08551ce4cb8efe41dab61cde609c |
