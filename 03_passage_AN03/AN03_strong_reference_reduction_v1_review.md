# Review: strong-reference reduction v1

Companion: `AN03_strong_reference_reduction_v1.tex`  
Prefix: `an03srrv1:`  
Date: 30 October 2026  
Scope: S4d's strong error inequality and vanishing initial error, inside the certified weak passage.

## Result and task status

**Steps 1–6 close.** With CFA's actual reference, the fixed incoming weak probability, and the model-only local choices below, the new theorem proves

\[
D^+E_s\le-g_WE_s+C_s(d_0^{(s)}+NW_2),\qquad
g_W=\frac12\frac{\alpha(1/2-\alpha)}{\alpha+1/2},\quad C_s=980,
\]

up to the first exit from $E_s<\delta$, on $[t_s,t_n]$. It also proves

\[
d_0^{(s)}=C_{\rm srr}q^{1/20}\to0,\qquad
E_0=E_s(t_s)=O(q^{1/20})\to0.
\]

MP's $A_0=O(q^{1/16})$ uses exactly the same incoming probability. Thus, for any fixed finite $K_0$ and fixed $n<h$, the **strong-part** initial inequality $K_0(E_0+d_0^{(s)}+A_0\sqrt n)\le\delta/2$ holds for small $q$. The eventual shared constant must be $d_0=\max\{d_0^{(s)},d_0^{(w)}\}$; the full initial guard follows once S4e supplies $d_0^{(w)}\to0$ and fixed selection constants.

| Requested step | Status | Closed output / exact limitation |
|---|---|---|
| 1. Inventory and reference identity | Closed | TeX `inventory`, `reference`, `W`: one actual reference; Euclidean errors; fixed incoming $W_2$; consumer hypotheses listed. The full selection theorem is not applied. |
| 2$a$. Pointwise remainder lines | Closed | `pointwise`, `majorant`, `epslate`: every canonical CFA remainder line is paid pointwise; late $\sup\varepsilon_F=O(q^{1/10})$. Core collapse is separately $O(q^{1/20})$. |
| 2$b$. Primary tail | Closed | `tail`: $\mathcal T\le Ce^{-cq^{-597/320}}+Ce^{-c/q^2}$ after $t_s$. No fixed $C_0E_g$ term is put into $d_0^{(s)}$. |
| 2$c$–3. Weak moment and weight conversion | Closed | `finiteweak`, `weights`, `weakmoments`: exact finite-$q$ functionals; $\omega=1+o(1)$; coefficient $C_1=8$, model-only, on $NW_2$; additive $O(q^{1/10})$. No derivative of $\omega$ is controlled here. |
| 4. Local box | Closed | `delta`, `branch`, `hbound`, `Jacobian`: both branch proximity and Jacobian negativity proved for $N\le2h$, before using the local inequality. |
| 5. Initial guard | Closed in its requested strong scope | `preforcing`, `E0`: pre-$t_s$ pointwise forcing, then CFA's original rate $g_c$, give $E_0=O(q^{1/20})$. No WEAK rate or box is used before $t_s$. |
| 6. Strong-error theorem | Closed | `main`: TAILREP's strong form with no extra hypothesis and no remaining $\ell(t)E_s$ term. Guard propagation and selection remain for S4e. |

There is no unmatched inequality within this strong reduction. The deferred weak inequality, derivative-weight budget and selection conditions are listed separately below and are not hypotheses of a claimed selection theorem.

## One reference and one weak norm

The object $(c_s,d_s)=(x_c,y_c)$ is MOMC's original characteristic retained by CFA. It is never reset to $(a,a)$, never replaced by a weighted barycenter, and never evolved under $G_M$. The two errors are

\[
e=|(x_c,y_c)-(a,a)|_2,\qquad E_s=|(x_c,y_c)-(X_*,Y_*)(N)|_2.
\]

The actual core mass is $M=\mu_K$; CFA's capped donor mass is $\widetilde M=\min(M,1)$. Neither is the residual constant $M_{\rm res}$. Normalization preserves the core probability, but it does not erase physical mass errors.

The norm for this increment and S4e is

\[
\eta_s(db)=m(t_s,b)d\lambda_0(b)/N_S(t_s),\qquad
W_2(t)=\big\||u(t,b)-U_*(N(t))|+|v(t,b)-V_*(N(t))|\big\|_{L^2(\eta_s)}.
\]

The probability $\eta_s$ is fixed on the closed clock labels. It is **not** the normalized current radial law $\eta_t$. All endpoint labels are retained. Finite moments hold for each fixed $q$ on WBR's reached chart.

## Pointwise remainder audit

The calculation starts from CFA's proved exact representation, not a new derivation of the original receiver field. Its canonical remainder is estimated using the following restated pointwise sources. No integrated budget is substituted for a supremum.

| Remainder or replacement | Pointwise price on $[t_s,t_n]$ | Justification |
|---|---|---|
| Target/core compact Gaussian kernels | $Cq^2(1+M_K)$ | MOMC's compact-kernel estimates already used in CFA; fixed receiver and donor radii. |
| Core second output and its response coefficient | $Cq^2M_K$ | CFA's assembly and compact core Gaussian moments. |
| Core mass capping | $C(M-1)_+=O(q^{11/10})$ | Subtraction of capped and uncapped measures; WBR's pointwise overshoot bound. |
| Explicit $P_1$ transverse terms | $C(J_G+q\sqrt{E_GJ_G})=O(q^2)$ | Exact Stein moments, $J_G\le q^2K_Y^2$, $E_G=O(1)$. |
| Finite-$q$ moment coefficients | $Cq^2(1+\vert V_O\vert +\vert K_O\vert )=O(q^2)$ | Balance/Gaussian moment bounds, uniformly bounded moments under RB states. |
| Primary selected residual | $C\{J_{G_+}+q\sqrt{EJ}+\mu_{G_+}\mathcal T\}$ | Exact removal of the linear regression term; Gaussian negative-part moments and RCET margin. Tail is superpolynomially small after $t_s$. |
| Secondary selected residual and negative $K_O$ charge | $C(E_\Sigma+q^{-1}\sqrt{E_\Sigma J_\Sigma})=O(q^{5/2}+q^{\Gamma_\nu/2})$ | Generic selected integrals, $J_\Sigma\le q^2K_Y^2$, RB's $E_\Sigma$, $\Gamma_\nu>3/10$. |
| Complement, Q3 interior, both strips and all other $B$ labels | $C\mu_B/q\le Cq^{1/10}$ | PROFILE's exact field cost and RB's proved outside supremum. All are included, without a new ancestry classification or gate assumption. |
| Primary negative $K_O$ part | $C\mu_{G_+}q^{-1}e^{-c/q^2}$ | $W_2>0$ on $G_+$; only $X_1<0$ contributes a negative $P_1$ moment. |
| Fixed-chart receiver gate tails | $C\mu_Gq^{-j}e^{-c/q^2}$ | CFA's compact Gaussian boundary estimate, fixed $j$. |
| Collapse of the normalized core to the actual reference | $C\bar D_K=O(q^{1/20})$ | Donor Lipschitz constant of $F$ is one; the $y$-moment is linear; SI/RB core radius. This is separate from CFA's canonical remainder. |
| $\widetilde M\mapsto1$ at the reference | $C\vert M-1\vert =O(q^{11/10})$ | MP's pointwise mass rate on the compact reference chart. |

The first ten rows give $\sup\varepsilon_F=O(q^{1/10})$. The last two explain why the final strong additive error is $O(q^{1/20})$. Constants in these vanishing-error budgets may depend on the fixed passage guards; the coefficient of $NW_2$ does not.

### Primary tail rate, including both sides of the gate

The increment restates and proves the bound that previously appeared inside CFA's proof:

\[
\mathcal T(t)\le C\exp\!\left[-\frac{c_*}{q^2+C_*C_0^2e^{-b_*(t-t_0)}}\right]+Ce^{-c_*/q^2},
\qquad b_*=Q(1-c_b)/2.
\]

The value estimate retains the factor $q$ in the Gaussian negative-part norm before the $1/q$ scaling. On the fixed receiver boundary, CFA's already chosen $C_0$ makes $U_2-qt_xU_1\ge U_2/2$; the negative part vanishes for $X_2\ge0$, and the $X_2<0$ contribution is an exponentially small Gaussian moment. Thus the other gate side is explicitly paid.

WBR's exact time scaling, including the bounded $A_q$ shift, gives

\[
e^{-b_*(t-t_0)}\le Cq^{(1-c_b)(k-1/8)/2},\qquad
(1-c_b)(k-1/8)/2\ge597/320.
\]

Since $597/320<2$, the denominator is at most $Cq^{597/320}$. The late tail is therefore $Ce^{-cq^{-597/320}}+Ce^{-c/q^2}$, not a fixed $C_0E_g$ error. Superpolynomial smallness follows analytically from boundedness of $x^re^{-cx}$.

## Weak moments: finite noise, omitted populations and weights

For an arbitrary cohort, balance and Gaussian moments give

\[
|V_T|+|K_T|\le C\left(\mu_T+q^{-1}\sqrt{\mu_TJ_T}\right).
\]

This is the estimate used for $P_q$ and $\Sigma$. In particular, the $q^2$ transverse contribution to $\mu_{P_q}\le C(q^{1/4}H+q^2)$ is retained. The resulting moment charges are $O(q^{1/8})$ for $P_q$, $O(q+q^{\Gamma_\nu/2})$ for $\Sigma$, and $O(q^{1/10})$ for $B$. MP's relative-mass bound alone is not divided by $q$.

On the reached selected chart, the $P_2$ gate tail yields

\[
V_S=\int_Sm\frac{\sin(qv)}q\cos(qu)+O(\mu_Sq^{-1}e^{-c/q^2}).
\]

For the other moment, an exact Gaussian/Stein identity is

\[
K_S=\int_Sm\cos(qv)\left[
K\!\left(\frac{\sin(qu)}q\right)+q\sin(qu)\Phi\!\left(\frac{\sin(qu)}q\right)\right].
\]

The centered Gaussian inside the $P_1$ activation has variance exactly one. With $K$ 1-Lipschitz, the two finite-noise errors are at most

\[
Cq^2(1+L^2)\int_Sm(1+|u|+|v|)+C\mu_Sq^{-1}e^{-c/q^2}.
\]

MP's pointwise transverse bound makes the integral $O(H+\sqrt{qH})$, so the value error is $O(q^{37/320})$. This is a computation on the reached growing chart, not an invocation of a bounded-chart error order outside its domain.

For weights, BULK's individual/aggregate defects give the amplitude-density ratio in $[e^{-2D_q},e^{2D_q}]$. Per-label balance and the chart give

\[
m/z^2=1+O(q^2(1+L^2)),
\]

and MP gives the aggregate $N_S/H=1+O(q^2)$. Therefore

\[
\omega(t,b)=\frac{d\eta_t}{d\eta_s}(b),\qquad
\sup|\omega-1|\le C[D_q+q^2(1+L^2)]=o(1).
\]

The moment comparison keeps deviations from the bounded selected atom inside $W_2$, instead of multiplying a weight error by the divergent supremum $L$. Once $N_S/N\le2$ and $\omega\le2$, it gives a coefficient at most four on $NW_2$, with a vanishing bounded-comparator error. The statement takes the conservative model constant $C_1=8$:

\[
|V_O-NV_*|+|K_O-NK(U_*)|\le8NW_2+C_{\rm fixed}q^{1/10}.
\]

Since $NK(U_*)\ge0$, the 1-Lipschitz positive-part map gives the same comparison for $(K_O)_+$. The negative part does not need a new separate charge at this comparison step. The derivative of $\omega$ is **not** estimated; it remains in S4e.

## Local model box and constants

The coherent strong field is written explicitly with the selected weak atom held fixed. Its symmetric Jacobian is WEAK's matrix. Let $L_J\ge1$ be a model-only bound on its first derivatives in $x,y,N$ on the compact box $|x-a|,|y-a|\le1/4$, $0\le N\le1/2$, $0\le V_*\le11/10$. The explicit Gaussian formula proves finiteness. Comparing at fixed $V_*$ with $N=0$ avoids any derivative of the selected weak atom in this Jacobian estimate.

With $a_{\min}=39/160$, $a_{\max}=2/5$, $\gamma_*=1183/20800$, the new choice is

\[
\delta=\frac12\min\left\{a_{\min}/8,\ (2\phi(0)-a_{\max})/3,\ 1/8,\ \gamma_*/(8L_J)\right\}>0.
\]

P's $C^1$ unstable branch gives model constants $n_{\rm br}>0,C_{\rm br}<\infty$ such that $|Z_*(N)-(a,a)|_2\le C_{\rm br}N$ for $N\le n_{\rm br}$. Uniformity on the ratio box follows from the same finite-dimensional parameter-dependent unstable-manifold theorem: the vector field and resident data are smooth, and all stable and unstable spectral gaps have positive model lower bounds. This introduces no numerical or original-flow hypothesis.

The explicit new upper bound on the fixed level is

\[
h\le\min\{h_{\rm WBR},\ n_{\rm br}/2,\ \delta/(2C_{\rm br}),\ \gamma_*/(8L_J)\},\qquad h<1/4.
\]

It ensures **both** branch proximity for $N\le2h$ and $J_*\le-g_WI$ on the $2\delta$ box. The branch segment and the actual reference segment are used only up to the first exit from $E_s<\delta$. Core donor replacement uses the fixed chart and the first moment; it does not require an unproved local box for every donor.

For the strong comparison, all remaining reference coefficients on $|x_c|,|y_c|<1$ are conservatively bounded by ten. The weak moment term is therefore at most $80NW_2$. WEAK permits $R_*=6>2+a+|u_\rho|+a/\lambda$ and $C_s=20(R_*+1)^2=980$, which dominates this coefficient. The additive constants, including passage-dependent core-radius constants, are put in $d_0^{(s)}=C_{\rm srr}q^{1/20}$. No model coefficient is enlarged in response to a residual guard, and no $\ell(t)E_s$ term remains to absorb. The rate remains $g=g_W$, with no additional factor loss.

## Initial guard: the earlier regime is kept separate

Before $t_s$, no late weak chart, logistic phase or WEAK local rate is used. RB's primary-to-clock comparison is valid on the **entire** passage, by its original entry/RCET proof, so $E_{G_+}\le CH$. At the first start hit, $H\le q^{1/8}$ on $[t_0,t_s]$.

The exact absolute charges imply

\[
c\le C(H+q^2+\mu_B).
\]

The suggested simplification $c\le C(H+q^2)$ is not inferred from the coarse outside supremum: $\mu_B\le q^{11/10}$ alone does not justify absorbing it into $q^2$. Keeping it explicit is sufficient, because the whole right side is $O(q^{1/8})$ on this interval. This is a correction to an unnecessary intermediate simplification, not a missing input to the argument.

The global balance/Gaussian moment bounds give $|V_O|+|K_O|=O(q^{1/16})$. For the primary remainder use only $\mathcal T\le C$, so $\mu_{G_+}\mathcal T\le C(H+q^2)$. All other majorant lines are bounded pointwise as above, with WBR's global overshoot rate; hence $\varepsilon_F=O(q^{1/10})$. Thus $f_*=O(q^{1/16})$ on the whole earlier interval, stronger than the requested final-stretch estimate.

CFA's certified inequality, with its own $g_c=\gamma_*/2$, gives

\[
e(t_s)\le e^{-g_c(t_s-t_0)}e(t_0)+C\int_{t_0}^{t_s}e^{-g_c(t_s-s)}(q^{1/20}+q^{1/16})\,ds.
\]

MOMC/CFA supplies bounded $e(t_0)=o(1)$. The start time gives exponent

\[
g_c(k-1/8)/Q\ge235417/832000>1/20,
\]

so $e(t_s)=O(q^{1/20})$. Branch proximity adds $O(q^{1/8})$, proving $E_0=O(q^{1/20})$. One can take the requested final stretch $T_q=(t_s-t_0)/2\to\infty$, but no integrated fixed allowance is used to claim pointwise smallness. The capped mass stays within CFA's proved range, and its stationary center is independent of that mass.

## Hypothesis audit and deferred consumer conditions

| Source / condition | Required hypotheses and domain | Supplied here / status |
|---|---|---|
| RB completed passage | Original balanced isotropic initialization, deep exponent 10, closed ratio box, WPT constant order, small $q$. | Certified interval, all residual/core/outside/secondary conclusions; no reopened sign hypothesis. |
| CFA representation and assembly | Fixed positive core labels and weights, core/reference fixed chart, capped mass $0<\widetilde M\le1$, response range, residual and transverse guards, secondary and outside inputs. | RB has discharged its stopped inputs and both strip budgets. The canonical field and pointwise majorant, not just `fullbudget`, are used. |
| CLOCK/CFA earlier local inequality | Same-field reference, Euclidean $e$, $e<e_*$, core radius below one, c-form value/derivative bound, $0\le c\le c_b<1$, nonnegative $K_w$, fixed positive donors. | RB gives $e\le3e_*/4$, $r_K=O(q^{1/20})$, actual c-form; $K_w=(K_O)_+$. Applied before $t_s$ with $g_c$, never WEAK's rate. |
| RCET margin / primary cancellation | Fixed $G_+$, positive $U_2,W_2$; original entry signs/ratios, response/duration/residual/learning budgets; fixed admissible small $C_0$. | RB/Q2EC as certified in CFA. Existing chart choice of $C_0$ also gives the receiver-boundary inequality. Tail is restated and proved with both sides. |
| MP late statements | Original passage, fixed $S$, start $H=q^{1/8}$, fixed admissible $h$, reached chart, auxiliary logistic mass. | Applied only on $[t_s,t_n]\subset[t_s,t_e]$. Not used for pre-start response. |
| BULK individual/relative amplitude bounds | Fixed positive-amplitude clock; original Cartesian entry ratios with exponent $1/8$; response and residual range; learning/duration bounds. | RB/WBR. Uniform individual statements, or the proof of `bulkweights`, imply the density ratios including endpoints. |
| PROFILE outside field | Fixed finite-mass outside output, bounded strong receiver chart, exact Gaussian flow. | RB's fixed $B$, chart $L_c$, and pointwise supremum. No per-mass weak-chart assumption is imposed on $B$. |
| P branch / AN06 region | Defined leading selected branch; model ratio box; $0<N\le1/2$. | Exact auxiliary logistic $N<2h<1/2$. Used only for comparator dynamics, positivity/boundedness and local $C^1$ proximity. |
| WEAK `strongineq` structural input | Euclidean same-field reference error; positive measures; unit leading strong mass; pointwise strong moment $D_s$; fixed normalized weak law; same logistic comparator; finite $W_p$; local box and negative symmetric Jacobian. | Same reference and norm fixed. Actual mass and donor moments are charged; radial weights converted to fixed $\eta_s$; $p=2$; local box proved. The original inequality is derived by subtraction, not asserted by treating actual $M$ as one. |
| WEAK return / small gain / guard | Returned inputs, $U_*>0$, strict moment margin; $0<n\le1/2$; bounded strong moments; fixed $g,C_s,C_w$; $Theta\le1/4$ and $K_0(E_0+d_0+A_0\sqrt n)\le\delta/2$. | Original return supplied independently by WBR. Full small gain and weak inequality deferred. The strong-part initial expression tends to zero for any fixed $K_0$. |
| TAILREP `selection` | Exact logistic mass and terminal hit; nonnegative errors; both differential inequalities up to the strong first exit; common pointwise $d_0\ge0$; $ell_B\ge0$, finite common $L_*$; separately maintained return; stated $\Theta$ and initial guard; smallness for convergence. | Logistic, return, $A_0$ already proved; strong inequality and $E_0,d_0^{(s)}$ proved here. `weakerror`, $d_0^{(w)}$, derivative-weight budget, $C_w,L_*,n,Theta$ and selection remain S4e. No full theorem is claimed with these as hidden inputs. |

## Constant order and S4e handoff

The order is

**WPT/RB → WBR → $(a_s=1/8,p=2)$ → model local constants $(\delta,g_W,C_s)$ → fixed smaller $h$ → [S4e: $C_w,L_*,n$] → $q$.**

The analytic branch constants $n_{\rm br},C_{\rm br}$, Gaussian derivative constant $L_J$, $C_1=8$, and $C_s=980$ are model-only. The prefactors in $\varepsilon_F$, $d_0^{(s)}$ and $E_0$ may depend on already fixed passage constants and on the fixed level, but multiply positive powers of $q$; they choose no earlier guard. No comparison uses an unproved mass range or rate across the $t_s$ boundary.

| S4e input | Delivered value / convention |
|---|---|
| Rate | $g=g_W=\gamma/2$; no extra absorption loss. |
| Strong coefficient | Model-only $C_s=980$, using $R_*=6$. |
| Local radius | Explicit $\delta$ above; $delta<a/8$, $a+3\delta<2\phi(0)$. |
| Level upper bound | $h\le\min\{h_{\rm WBR},n_{\rm br}/2,\delta/(2C_{\rm br}),\gamma_*/(8L_J)\}$, $h<1/4$. Further fixed decreases are allowed. |
| Strong additive defect | Pointwise $d_0^{(s)}=C_{\rm srr}q^{1/20}\to0$. It is not a time integral. |
| Initial error | $E_0=O(q^{1/20})\to0$, derived with CFA's earlier $g_c$. |
| Weak norm | $p=2$ distance to $(U_*,V_*)(N(t))$ under the fixed actual incoming $\eta_s=m(t_s)d\lambda_0/N_S(t_s)$. |
| Weight value conversion | $\omega=1+O(D_q+q^2(1+L^2))$; no derivative estimate yet. |
| Incoming smallness | Same convention as MP: $A_0=O(q^{1/16})$. |
| Reference identity | CFA/MOMC's unchanged actual same-field characteristic; Euclidean $e,E_s$. |
| Scope | Up to the first exit from $E_s<\delta$ and no later than any fixed logistic hit $t_n<t_e<t_b$. |

Remaining work is precisely S4e: the weak-chart reduction, derivative normalized-weight defect and common $\ell_B$ budget, $d_0^{(w)}\to0$, $C_w,L_*$, the small-gain choice and selection. Until those are proved, this increment does not propagate the local strong guard to the terminal hit or claim terminal selection. Once $d_0^{(w)}\to0$ is available, the shared $d_0=\max(d_0^{(s)},d_0^{(w)})$ also tends to zero and the initial expression vanishes for fixed finite $K_0$.

## Source provenance and verification

README and roadmap **v1.21** were re-read from the read-only repository. The accompanying source statements were fetched for this request; source SHAs are recorded below. The prefix was checked with repository code search and local prior-source inspection; no collision was found. Verification is analytic source/hypothesis inspection, TeX compilation and reference/integrity checks, not numerical certification. No interval arithmetic, experiments, trajectories, grid signs or numerical premises were used. No prior increment, foundation, checkpoint or GitHub content was modified. The source ZIP contains only the raw new TeX and review Markdown.

| Source | Repository file | Fetched SHA |
|---|---|---|
| README | `README.md` | `5c2dbb64cf1ee12a163cd2a9e5080a3d94650146` |
| Roadmap v1.21 | `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | `8d7fe941d58c0e7a3eb8bd6dd19730eede29ecae` |
| CFA | `03_passage_AN03/AN03_c_form_assembly_v1.tex` | `341908c228092e9a818d98de3ec26591a1050364` |
| CLOCK | `03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex` | `8de0d85c64a3d51f3bd9c3662baf2efae0737373` |
| MP | `03_passage_AN03/AN03_matching_package_v1.tex` | `9491bba4ec10f79acca277b1f0c4ddd92180a7aa` |
| WBR | `03_passage_AN03/AN03_weak_boundary_return_v1.tex` | `c1f18203cc99ca5ddcda9481ca1281d7debffa9a` |
| WEAK | `03_passage_AN03/AN03_weak_transit_forcing_and_orbit_selection_v1.tex` | `3a937aa25253b5773424a3f165f71d476157575a` |
| TAILREP | `03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex` | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| RB | `03_passage_AN03/AN03_response_barrier_v1.tex` | `5312b5093f3ed4f74063347df31ae5a29155255f` |
| LOC | `03_passage_AN03/AN03_local_rate_mean_tracking_v1.tex` | `eb1fa397d1f0d9b0e3aea1698b9960726e739fa8` |
| RCET | `03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex` | `49e352002b4c699338ac99a4d55d51c60760ea86` |
| BULK | `03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` |
| SI | `03_passage_AN03/AN03_selection_interface_v1.tex` | `9c984392caa650505b5c961796529fb4acc751ea` |
| PROFILE | `02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex` | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` |
| MOMC | `02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex` | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| P | `01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex` | `cb458c933aa043cf0188fd11c46bf4246ffc91d8` |
| AN06 | `04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex` | `9e102514ad0a491066a2f9eb8eb86e9a251c2b53` |
| LCRC | `03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex` | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` |
