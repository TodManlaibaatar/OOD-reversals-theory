# Review: AN03_late_strip_budget_v1

Date: 2026-10-26. New label prefix: `an03lsbv1:`.

## Result and scope

The arrival-weighted consumer requested in PISB is closed on the **retained S2CP/CFA stopped interval**, without assuming CFA's strip budget or passage conclusion:

\[
\mu_{J_3}(t)\le W_3(t),\qquad
\sup W_3/q\le C_{\rm fixed}(1+s_q)q^{769/4000},\qquad
\int W_3/q\le C_{\rm fixed}L_T\ell(1+s_q)q^{769/4000}=o(1).
\]

The more informative bound is `an03lsbv1:budget`. It retains the exact parameter-dependent powers, \(A_q\), \(E_g\), \(\beta=\lambda/(\lambda+q^2)\), the clock defect, and the fixed gain factors. The rational exponent above is only a uniform lower bound for its four positive exponents.

Together with PISB, this pays the whole CFA strip input on that stopped trajectory. It does **not** execute the joint weak-passage bootstrap or establish the retained c-form field guard from scratch.

The chosen route proves a weighted moment directly. It does not assert a two-sided raw entry profile for all of the new ancestry, nor assign these labels to the core or to G+. Very delayed labels need no pre-\(t_0\) chart contract: their mass lag pays even the arrival-weighted consumer, including its unarrived term.

## Task-by-task status

| Task | Status | Result and exact remaining inequality | Dependencies |
|---|---|---|---|
| 1. Target-only time shift | **Closed** | `delay`, `shift`, `density`, `endpoint`: positive velocity, exact shift and exact radial prefactor; prefactor \(1\le L\le e^{Cq^2T_{\max}}=e^{o(1)}\); equal-time domination; delay density at most \(CqK(-s_0)\); endpoint seed and uniform Q4 phase law. No remaining inequality for this task. | Model/ratio box, PISB's fixed \(\varepsilon\); no LCRC guard. |
| 2. Transfer at \(t_m\) | **Closed** | Q2EC's all-label early comparison; fixed chart/boundary/transit sets, all chosen from the actual state at \(t_m\). The separate delay sets are also fixed by initial labels. No moving population mask. No remaining inequality. | S1 comparison constants and \(A_q\) bounds. |
| 3a. Arbitrary-label chart transport | **Closed, with a new lemma** | `chart`, `single`: fixed-constant transport by MOMC's \(G\), for any receiver entering the fixed chart. MOMC's small-shape pair proof is **not invoked verbatim**. A global chart logarithmic-norm bound and an invariant-square check supply the missing bounded-distortion argument. No remaining inequality. | \(R=79/51\), model constants only. |
| 3b. Mass bridge | **Closed** | `entrymass`: \(m(t_0,b)\le C A_q^{-1}(q^{c_m}+q^2e^{-T(b)})\) for every delay, arrived or not. The bridge pays the full \(e^{t_0-t_m}\) factor. No remaining inequality. | Fixed PISB bridge factor \(e^6\), S1 constants. |
| 3c. Arrival and mass–shape moment | **Closed for the required consumer** | `transit`, `massshape`: all delays \(T\le(k-7/4)\ell\) arrive before \(t_0\); their shape is at most \(C A_q^d(q^{6d}e^{dT}+q^{v+du})\). The correlated moment converges with denominator \(1-2d(1+\nu)\ge16269/80000\). Later delays are paid separately, not assigned an unproved profile. No remaining inequality for the consumer. A full two-sided raw tail is neither needed nor claimed. | Model/S1 constants; fixed transit chart radius; no LCRC guard in these pre-entry estimates. |
| 4. After \(t_0\) | **Closed** | `restart`, `arrivalgain`: S2CP/DECG distance and gain restart from actual arrival with the same constants. `coarseconsumer` controls the **whole** late-label contribution by \(C C_gC_{\rm abs}m(t_0,b)e^{(1+\nu)I(t)}\). Unarrived mass remains in \(W_3\). No remaining inequality. | Existing \(C_D,A_0,C_g\), stopped field/gate/reference budgets, \(B\), duration. |
| 5. Strip budgets | **Closed as a stopped implication** | `budget`, `finalbudget`: both requested budgets vanish; PISB supplies the other strip zones. No unpaid strip inequality remains in this implication. The joint weak-passage closure is outside scope. | Fixed source gain/clock factors multiplying positive powers of \(q\); \(q\) chosen last. |

## Main proof audits

### Endpoint and exact delay normalization

Use the lift \(b_0=-\pi/2\), not a discontinuity in the angle at \(3\pi/2\). The endpoint has \(T(b_0)=0\), radial prefactor exactly one, and a nonzero first-coordinate Gaussian seed \(\widehat U_1(1)\asymp q^6\). It is not a frozen or zero-mass endpoint.

On the Q3 side of this boundary,

\[
v_q(b_0-qs)=\frac q2\{\cos(qs)K(-\sin(qs)/q)-\rho\sin(qs)K(-\rho\cos(qs)/q)\}\asymp qK(-s)>0.
\]

The delay can be much larger than a logarithmic time. This causes no loss in its radial prefactor: \(T_{\max}\le C(1+s_q)^3e^{s_q^2/2}\) is polynomial in \(\ell\), whereas the target radial rate inside the initial layer is \(O(q^2)\). The shift formula is stated for \(t\ge T\), with its backward-orbit interpretation made explicit for earlier times. The density uses absolute orientation when changing from initial angle to delay.

### The endpoint is a Q4 endpoint, with arrival at \(4\ell+O(1)\)

The target first reaches an order-one angle at \(2\ell+O(1)\), then reaches the fixed strong chart at \(4\ell+O(1)\). Its profile is

\[
\widehat m_*(t)\asymp q^{12}e^t,\qquad
a_q-\widehat\theta_*(t)/q\asymp q^{-4d}e^{-dt}.
\]

The proof uses the Q4 reciprocal-speed calculation and extends its local attraction calculation uniformly after that Q4 arrival. It does not use PROFILE's common, later Q1 time guard at an earlier time. The \(q^{6d}\) terminal endpoint scale is the Q4 specialization; it is sharper than the generic right-half/Q1 cutoff suggested in the roadmap. Replacing the exact local rate by \(d\) costs \(e^{O(q^2t)}\), which is bounded on the times used here.

### MOMC's pair proof needs an extension, not a citation alone

An extra receiver may enter the chart with order-one scaled displacement. The new chart lemma checks the full leading receiver Jacobian on \([-79/51,79/51]^2\), including the y-row. The maximum-norm logarithmic norm is at most \(-1/200\). For the x-row, its possible positive contribution is bounded by

\[
H(x)=\lambda\Phi(\rho x)/2+\rho^3(R-x)\phi(\rho x)/2,
\quad H'(x)=-\rho^5x(R-x)\phi(\rho x)/2,
\quad H(0)\le49/400+27097/255000<49/200.
\]

MOMC's finite-noise C1 reduction gives an exact-field logarithmic norm at most \(-1/400\) for small q. This argument bounds any violation of cooperativity by the C1 error; it does not assume finite-noise cooperativity. The atomic-center corner checks give inward faces, with a fixed margin surviving the vanishing donor spread, reference offset and outside error.

The resulting finite integral of the arbitrary receiver's displacement pays the nonlinear Jacobian error. Only then is the sharper central rate \(-d+M/2\) integrated to recover MOMC's mass-clock multiplier up to a **fixed** factor. A universal \(e^{o(1)}\) multiplier is not asserted for the newly admitted receivers.

### The transit estimate has its own matrix-value proof

The early delay cutoff is

\[
T_c=(k-2+\chi_{\rm lag})\ell,\qquad \chi_{\rm lag}=1/4.
\]

At \(t_m\), those labels have negative angles of magnitude at most \(Cq^{7/10}\), not angles near the initial weak axis. Their P1 gates are full. The proof derives

\[
R_{11}=(1-M)/2+O(q^2+\mu),\quad R_{22}\ge-C(q^2+\mu),\quad
|R_{12}-R_{21}|\le C(qM+\mu).
\]

The target covariance is symmetric, so it cancels from the last expression. On P2, the strong donor outputs have norms \(O(qM)\) and \(O(q^2M)\); the arbitrary complement costs \(C\mu\) in unscaled matrix values. The projected negative-side gate gives \(|R_{22}\sin\theta|\le C(q+\mu)\).

The exact misalignment equation has the correct sign:

\[
\Delta'=-(\operatorname{tr}R)\sin\Delta+(R_{12}-R_{21})\cos\Delta.
\]

It yields \(|\Delta|\le Cq^u e^{-(t-t_m)/6}+CqM(t)\). The negative-angle inequality is integrated using both \(\int z^2=O(z(t_m)^2)\) and \(\int q/z\le8/L\) before hitting \(-qL\). This keeps the arrival estimate \(4\ell+T+O(1)\), rather than losing an extra multiple of \(\ell\).

For a non-charted receiver, \(t_m\le4\ell+T+C\); thus its nontrivial arrival is no later than \((k+2+\chi_{\rm lag})\ell+C\le(321/40)\ell+C\). Here \(M\le C A_q q^{79/40}=o(1)\), so the remaining bounded-time entry is justified by the **fixed-chart** reduction and finite-time continuous dependence. No unbounded-chart C1 extension is assumed. Already charted receivers do not require this transit estimate.

### Absolute comparison error is charged, not divided by a tiny shape

The early error leaves the explicit terminal floor

\[
q^{a_e},\qquad a_e=v+du\ge841/680.
\]

The proof does not turn the absolute comparison into a relative profile assertion. This floor is paid in its own weighted moment with exponent \(\delta_F\ge9323/13600>0\). The endpoint-correlated term has exponent \(\delta_E\ge97/40\).

### Arrival weighting and delayed labels

The late class is not assumed to stay on the lower side. The coarse bridge gives its entry mass, and PISB cap one controls it up to any actual post-\(t_0\) chart arrival. Restarting S2CP's distance estimate is valid because the local estimate is stated from arbitrary start times and the gate, radial and field error budgets are nonnegative cumulative upper bounds. DECG's reference radial gain and the post-physical-exit cap restart as well.

For late labels, the **consumer** can cost \(e^{(1+\nu)I}\), not merely \(e^I\). This loss is retained. The delayed correlated mass gives the exact power

\[
q^{\chi_{\rm lag}-\nu k},\qquad \chi_{\rm lag}-\nu k\ge769/4000>0.
\]

The baseline entry mass \(q^{c_m}\) is also paid over the full strip, with exponent \(c_m-(1+\nu)k>3/2\). Neither term is discarded. These two estimates cover finite arrivals, never-arrived labels and the unarrived portion of W3 at every intermediate endpoint.

### Tail/moment calculation

For the early correlated summand the delay law is \(q^2e^{-T}\), the density is at most \(Cq\,dT\), and the growing shape is at most \(C A_q^d q^{6d}e^{dT}\). Its tail exponent is \(1/d>3\omega/d=p\). The full gain moment converges because

\[
1-2d(1+\nu)\ge16269/80000.
\]

This calculation bounds the full nonnegative weighted moment, and therefore any restriction to TAILREP's core cutoff. It avoids asserting that the separately charged comparison floor or baseline mass has the same raw-tail law. Extending this one integral to infinite delay is an upper bound on a nonnegative integrand; it does not extend the early-class shape estimate to the late class.

## Retained inputs and constant audit

The retained assumptions are precisely those of the specified S2CP/CFA stopped setting: the duration and c range, LCRC residual/energy/integrated-r guards, instantaneous core/reference controls, S1 entries, the S2CP fixed-chart c-form field allowance and its other retained non-strip inputs. S2CP's gate and stopped-clock conclusions and its improved secondary bound are then available. This result improves the strip contribution within that setting; it does not replace the retained field allowance by a proved full field theorem.

In particular S2CP's instantaneous outside guard \(\sup\mu_{\mathcal B}/q=b_B(q)=o(1)\) remains a stopped guard; its time-integrated strip counterpart is not assumed. The new quantitative strip conclusion is not a claim to improve an arbitrarily preassigned function \(b_B(q)\) for the entire outside population. The delay split parameter \(\chi_{\rm lag}=1/4\) is unrelated to TAILREP's core-cutoff exponent \(\chi=1/20\), which is unchanged.

| Constant/factor | Source or construction | Dependence and use |
|---|---|---|
| \(R=79/51\), \(a<28/51\) | MOMC | Model only; used unchanged. |
| Transit radius \(L\), transit time constant | New `transit` proof | Fixed from model matrix estimates and target attraction; no LCRC guard. |
| \(C_{\rm sh}\) | New `chart` proof | Fixed R/ratio-box constants; uses the global contraction integral, no residual guard. |
| Target sign/seed/profile/density constants | PROFILE equations plus new endpoint calculation | Model only. Dependence on fixed PISB \(\varepsilon\) is allowed in the delay-maximum bound. |
| \(c_A,C_A,A_q\) | MOMC entry | \(A_q\) is kept explicit; bounded above and below by model/S1 constants. |
| Bridge factor | PISB bridge | \(e^{6+o(1)}\); model/S1, not \(e^{CB}\). |
| \(\chi_{\rm lag}=1/4\), \(\nu\le1/100\) | Fixed analytic split and source gain allowance | No guard dependence; these give the rational positive margins. |
| \(C_D,A_0\) | S2CP `CD` and `gain` | Existing fixed stopped constants, including field allowance and residual-guard dependence. They multiply vanishing q powers only. |
| \(C_g\) | Restarted DECG/S2CP | \(e^{6B+3}\), with a fixed norm-convention enlargement if necessary. |
| \(C_{\rm abs}\) | PISB cap one | \(e^{2B+\eta_q}\), \(\eta_q=C(1+M_{res})qL_T\ell=o(1)\). |
| \(F_q\) | Stopped clock | \(C_H E_g A_q^\lambda e^{D_{clk}}\), \(D_{clk}=O(q^{1/8}+q^2\ell)\). |
| \(L_T\) | Retained duration | Multiplies the final uniform bound by \(L_T\ell\). |

The A_q powers in the final formula are:

- \(A_q^{-1}\) for the baseline no-gain term;
- \(A_q^{\lambda(1+\nu)-1}\) for the two coarse-consumer terms;
- \(A_q^{-1+(2d+\lambda\beta)(1+\nu)}\) for the two shape moments.

The noise exponent remains \(1/\beta=1+q^2/\lambda\) until it is bounded by the chosen \(1+\nu\). No fixed exponent loss is silently set to zero. The source constant order is unchanged, including S2CP's choice of CΣ after C0 and SEP entry constants. All newly introduced pre-entry constants can be fixed from the model before the LCRC guards. Choose q last, after the retained field and CFA forcing allowances are fixed. The combined strip budget then satisfies any prescribed positive CFA strip allowance.

## Source provenance

Fresh read-only GitHub reads from [TodManlaibaatar/OOD-reversals-theory](https://github.com/TodManlaibaatar/OOD-reversals-theory), 2026-10-26. The following are **file blob SHAs**, not repository commit IDs. No GitHub mutation was made.

| Source | Repository path | File blob SHA |
|---|---|---|
| Roadmap v1.15 | `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | `a4da5bcb9061ea33d7e9036729211a5beeed0d13` |
| PISB | `03_passage_AN03/AN03_pi_strip_budget_v1.tex` | `ab8a0a2a028935f5045e53e0066e30afeb69c635` |
| Q3SB | `03_passage_AN03/AN03_Q3_strip_budgets_v1.tex` | `13a024c54f10d50a454aae1006d3005d2a28051b` |
| GESG | `03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex` | `f00459b5ca412eb86b0893adb64766e2c10d5590` |
| S2CP | `03_passage_AN03/AN03_S2_closure_package_v1.tex` | `baeb8a7eb1e36ce86319782511b665944be1afda` |
| TAILREP | `03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex` | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| Q2EC | `02_entry_AN02/AN02_Q2_entry_contracts_v1.tex` | `b149537025e130801fc55b9e49c365c158eee17b` |
| PROFILE | `02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex` | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` |
| OWPT | `02_entry_AN02/AN02_overlap_window_profile_transfer_v1.tex` | `8fac13f9d36255d3e2e23cc9b2196719ec602907` |
| MOMC | `02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex` | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| DECG | `03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex` | `a490ea323e45e61c1a58301554b89ad84cb02605` |
| CFA | `03_passage_AN03/AN03_c_form_assembly_v1.tex` | `341908c228092e9a818d98de3ec26591a1050364` |

Key consumers and proof locations checked: PISB `matching`, `bridge`, `postgain`, `capone`, `lateconsumer`; PROFILE `angle`, `coordinate`, `rightcircle`, `cost`; MOMC `main`, `uniformity`, `reduction`, `jacobian`, `meanintegral`, `massintegral`; S2CP `S2`, `CD`, `gain`, the stopped-clock calculation and `latestrip`; DECG `localdistance`, `radialbudget`, `conditionalgain`; GESG's global sine and signed-gate estimates; CFA's strip allowance. TAILREP's gain-integration mechanism is used through DECG/S2CP, and its moment consumer is bounded directly here.

## Verification and delivery

Analytic proofs only. No interval arithmetic, numerical premise, sign grid, saved trajectory, or experiment was used. The rational margins follow from the displayed analytic inequalities on the parameter box.

The new TeX is standalone and compiles with ordinary pdfLaTeX; internal labels all use `an03lsbv1:`. Compilation is a document check, not mathematical validation. The source ZIP contains exactly the raw `.tex` and same-stem `_review.md`; it contains no PDF. Prior output files are checked against their pre-task hashes. No foundation, roadmap, checkpoint, previous increment, or repository source is edited.
