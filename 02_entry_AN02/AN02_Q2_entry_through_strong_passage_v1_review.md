# AN02 Q2 entry through strong passage v1 — review note

**Status: part (e) closes; the universal-factor route in part (a) stops at a fixed-threshold obstruction.** Parts (a)–(d) are not claimed. This increment does not establish all of LCRC’s Q2 entry hypotheses.

Companion: **AN02_Q2_entry_through_strong_passage_v1.tex**. New label prefix: **an02q2epv1:**. No prior source is replaced or consolidated.

## Closed original-flow result

For the entire fixed initial Q2 ancestry, write \(N_2=\int_{\mathcal Q_2}m\). Theorem **energy** proves, on the original untied flow,
\[
\frac{N_2(t)}{M(t)}
\le \frac{8e^7C_Q}{A_q}q^3,\qquad t_m\le t\le t_h.
\]
At \(t_0=t_h\), every subcohort \(I\subseteq\mathcal Q_2\) consequently satisfies
\[
E_I(t_0)+J_I(t_0)
\le \frac{4e^7C_Q}{A_q}q^3
\le C_Jq^3,\qquad C_J=\frac{4e^7C_Q}{c_A}.
\]
Here \(C_Q\) is a single uniform upper constant for Q2E’s two aggregate target-only energy estimates, and \(c_A\le A_q\) is MOMC’s existing normalization bound.

This supplies **\(J_G(t_0)\le C_Jq^3\)** for the whole explicit Q2 cohort and **\(E_{G_+}(t_0)=o(1)\)** for its primary group. It also bounds any Q2 secondary subgroup’s total entry mass, without proving that subgroup’s profile or tail. If a future definition of \(G\) adds labels outside the initial Q2 quadrant, those additional labels are outside this theorem.

The proof uses Q2E at the moving overlap, where P’s original-versus-target radial comparison is still \(e^{O(q^u)}\). Dividing by \(M_0=A_q q^u\) gives the explicit powers
\[
A_q^{-1}\bigl(
q^{2/\omega+1/2}+q^3+
q^{4+(1-\lambda)/2}+q^5\bigr).
\]
They are all bounded by a constant times \(A_q^{-1}q^3\). The exact global radial growth inequality then compares \(N_2\) to MOMC’s strong mass:
\[
\left(\log\frac{N_2}{M}\right)'\le4M+C_*q^2,\qquad
\int_{t_m}^{t_h}M\le\frac32.
\]
This costs at most \(e^7\), independently of the subdivision at \(C_0\). It uses neither an angle bound for Q2 nor a residual-integral clock assumption.

## Exact obstruction and the two checks

The roadmap’s proposed universal angular factor is
\[
D_h^{-1}=[2(1-M_0)]^{-1/2}.
\]
Its mass integral is correct:
\[
\int_{t_m}^{t_h}M
=\log[2(1-M_0)]+O(q^2\ell^2).
\]
The issue is the remaining receiver equation.

**Check 1: diagonal drive plus small cross perturbations.** On a receiver with \(\theta=qx\), the strong cross drive contributes a relative term of order \(M/x\). At a fixed eta-zero threshold, \(x\) is large but fixed in \(q\), so this is an order-one-in-\(q\) error budget. A small fixed \(C_0\) is insufficient to turn it into \(o_q(1)\). BULK’s bounded residual-integral assumption is not available on this interval and is not invoked.

**Check 2: keep the structured leading field and test cancellation.** Lemma **field** derives, from MOMC’s original-field reduction and its already proved donor concentration,
\[
\begin{aligned}
2f_x^M&=-(1-M)x+\rho\phi(\rho x)
-\rho M F(\rho x,\rho a_\rho)+\lambda y\Phi(\rho x),\\
2f_y^M&=-(1-M)y-Ma_\rho+\rho\mathcal K(\rho x).
\end{aligned}
\]
The second row is essential. On the aligned ray \(x=y\ge a_\rho\), both rows become
\[
x'=f_0(x)+\frac M2(x-a_\rho),\quad
f_0(x)=-\omega x+g(x),\quad
g(x)=\frac{\rho}{2}\mathcal K(-\rho x)>0.
\]
The term \(-Ma_\rho/2\) survives even with zero donor spread and zero outside mass.

Proposition **obstruction** is an exact result **within this defined coherent leading system**. Start the trained and target receivers at the same value, let the target end at any fixed \(L>a_\rho\) at logistic half mass, and put \(D=\exp(\int M/2)\). Scalar comparison gives \(x\ge\widehat x\), and the exact identity is
\[
\frac{d}{dt}\log\frac{D\widehat x}{x}
=\frac{g(\widehat x)}{\widehat x}-\frac{g(x)}x
+\frac{Ma_\rho}{2x}
\ge \frac{Ma_\rho}{2x}.
\]
On the terminal logistic segment \(M\in[1/4,1/2]\), whose duration is \(\log3\), \(x\le\sqrt6L\). Therefore the exact failing inequality is
\[
\boxed{\ \int\frac{Ma_\rho}{2x}\,dt
\ge\frac{a_\rho\log3}{8\sqrt6L}>0,
\quad\text{where the proposed uniform route needs }o_q(1).\ }
\]
Equivalently,
\[
\frac{1/x(T)}{[2(1-M_0)]^{-1/2}/\widehat x(T)}
\ge \exp\!\left(\frac{a_\rho\log3}{8\sqrt6L}\right).
\]
The other term in the logarithmic identity has the same sign. There is no cancellation that restores the proposed universal factor.

This is **not presented as a proved counterexample for the exact initialized Q2 population**. Matching that specially chosen leading receiver to the initialized original flow would itself require the off-chart and crossing-layer analysis that has not been completed. The rigorous conclusion is narrower: the central small-cross-error estimate used by the proposed universal-factor route is false in its coherent limiting receiver problem, and the omitted term is present in the original field supplied by MOMC.

The fixed-threshold issue is compatible with RCET’s endpoint-regularized law:
\[
q\cot\widehat\theta(10\ell)
\asymp\left[\frac{q^\gamma(s_0+q)}{c_0+q}\right]^{(1-\lambda)/\lambda}.
\]
At \(c_0=Kq^\gamma\), with \(K\) fixed, the terminal inverse scaled angle has fixed order \(K^{-(1-\lambda)/\lambda}\). A bounded time shift involving \(A_q\) preserves this distinction. No endpoint regularization is discarded.

A growing margin \(K(q)\to\infty\) would change the specified group. A label-dependent nonlinear transition factor may instead be possible, but would require its own original-flow matching theorem. Neither repair is assumed or pursued after the stop.

## Supplied and unsupplied contracts

| Requested contract | Status in this increment |
|---|---|
| (a) Original-flow dichotomy with an explicit factor and revised threshold \(K\) | Not closed. The proposed universal \(D_h^{-1}e^{o(1)}\) route fails the displayed relative-integral check at fixed \(K\). No impossibility of every nonlinear-factor formulation is claimed. |
| (b) Positive \(z\), antisymmetric ratio, eta-zero and clock Cartesian ratios | Not supplied. Small total energy gives none of these signs or relative bounds. |
| (c) Clock seed and its \(A_q\) dependence | Not supplied. In particular no \(A_q^{-\lambda}\) amplitude factor is certified here. |
| (d) Q2 chart entry with a certified \(Z\) | Not supplied. The field estimate on a square is not a receiver-arrival theorem. |
| (e) \(J_G(t_0)\le C_Jq^3\), \(E_{G_+}(t_0)=o(1)\) | Proved for the entire explicit Q2 ancestry and its subdivisions. |

The secondary recruited tail would still need an original-flow entry displacement/radial profile about an actual same-field reference, its normalized tail and cutoff with the correct \(A_q\) factors, and the later S2 distance/gain contracts already retained by LCRC. The total mass bound above does not supply these. No secondary profile is derived here.

No weak passage, \(B_s\), core retention, capped gain, bridge, saturation tail, or consolidation is started. No statement goes beyond \(t_h\).

## Constants and parameter dependence

All constants produced or used at order one are independent of LCRC’s guards \(B,E_g,K_Y,M\).

| Constant or factor | Meaning and dependence |
|---|---|
| \(A_q=M_0/q^u\), \(c_A,C_A\) | Actual MOMC normalization and existing positive bounds. The new energy bound keeps \(A_q^{-1}\) explicitly; the uniform constant replaces it only by \(c_A^{-1}\). |
| \(C_Q\) | Uniform Q2E aggregate-energy upper constant; depends only on its proved analytic source estimates and the fixed ratio box. |
| \(2\), \(e^7\) | Early radial comparison allowance for sufficiently small \(q\), and passage mass-ratio amplification. The latter is \(e^{4(3/2)+1}\). |
| \(C_J=4e^7C_Q/c_A\) | Certified whole-Q2 entry constant; independent of \(C_0\), \(K\), and any later subdivision. |
| \(R=79/51\) | Existing MOMC strong-donor chart. No new Q2 chart radius is certified. |
| \(L\) and \(C_L\) | Arbitrary fixed receiver-square radius for the field lemma and its analytic remainder constant. This is a field domain, not a claimed Q2 entry cap. In the comparison test \(L>a_\rho\) is a fixed terminal scaled angle. |
| \(a_\rho\), \(\omega\) | Existing resident root and target outer rate; depend only on \(\rho\). The root is strictly positive. |
| \(D_h=\sqrt{2(1-M_0)}\) | Valid integrated diagonal factor. It is not the full finite-angle transport factor. |
| \(1/200\) | Lower contraction margin \(\omega-1/4\) used to keep the comparison receiver above the resident. |
| \(\log3,\sqrt6,a_\rho\log3/(8\sqrt6L)\) | Exact terminal logistic duration, elementary receiver bound, and strictly positive obstruction exponent. |
| \(C_*\), source comparison constants | Fixed analytic constants from MOMC and P; they determine only how small \(q\) must be for the displayed allowances. |
| \(K,Z,C_{\rm clk}\) | **Not produced.** Reporting certified values would presume the unclosed geometry. |

The only new proved \(A_q\) power is **\(A_q^{-1}\)** in the aggregate-energy upper bound. The retained clock identities use \(M_0=A_q q^u\), the shift \(-\log A_q\), and \(D_h=\sqrt{2(1-A_qq^u)}\). No target-only time-shift power is silently transferred to original-flow Q2 amplitudes.

## Audit points

- Exact balance, rather than alignment, identifies original mass with \(E+J\). All energies are nonnegative, so the whole-Q2 bound applies to any subgroup.
- Q2E is evaluated at \(t_m<10\ell\), inside its proved time range; it is not extrapolated to \(t_h\), which can differ from \(10\ell\) in either direction.
- P’s all-label radial comparison is used only while \(\overline S(t_m)=O(q^u)=o(1)\). No angular absolute error is used to transfer a small relative profile.
- No new first-exit bootstrap is introduced. MOMC’s completed theorem supplies its actual interval, pointwise mass defect, outside mass and donor concentration.
- Divisions by \(M\) and \(N_2\) are legitimate because their fixed cohorts have positive initial radial mass and the finite-time radial equation is multiplicative.
- The radial inequality is integrated over the fixed initial label set. No moving-mask flux is omitted.
- The receiver field lemma uses the finite-noise reduction for any fixed finite radius. Its donor replacement uses the exact bound \(|\partial_rF|\le1\). There is no derivative of an evolving label mask.
- Its integrated remainder is bounded by \(C_L[q^v+\epsilon_m+q^2(1+\ell)+q\ell^2]\). The term \(-Ma_\rho/2\) is outside this remainder.
- The coherent comparison preserves \(x,\widehat x>a_\rho>0\), making its logarithms and reciprocal variables legal.
- Gaussian gate effects are retained through \(g(x)=\rho\mathcal K(-\rho x)/2\). No fixed Gaussian tail is relabeled as \(o_q(1)\).
- The terminal \(\log3\) interval and the positive lower bound are analytic logistic identities. No integration, trajectory, sign test, or parameter sampling was performed numerically.
- No finite-noise cooperativity assumption is made. The scalar comparison is explicitly restricted to the defined coherent leading problem.
- RCET’s \((s_0+q)\), \((c_0+q)\) factors are retained. Late weak-axis crossers have not been assigned original-flow crossing times.
- RCET’s \(O(C_0)\) defect is a bounded defect for fixed \(C_0\); it cannot certify an \(e^{o_q(1)}\) multiplier.
- The diagnostic does not claim to disprove initialized S1. It identifies the failed central estimate and stops without adding a margin hypothesis.

## Source provenance and label map

The updated repository was read through the read-only GitHub connector. README and roadmap were read first; the roadmap identifies itself as **v1.5**. The source labels below refer to the actual fetched text. GitHub-reported blob identifiers are preserved verbatim.

| Source | Repository path | Reported blob identifier |
|---|---|---|
| README | README.md | a55a9b070c1e8b2053607297c52f9b2d788e0d7e |
| Roadmap v1.5 | 00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md | 4ddbf06115f364970dfeca7738ac6c640d387549 |
| H2, §0 | 00_roadmap/THEORY_HANDOFF_ANALYTICAL_A_B_v2.md | decb029fb314e96aae70e5eee68eaa969b6293ce |
| P | 01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex | cb458c933aa043cf0188fd11c46bf4246ffc91d8 |
| RCET | 03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex | 49e352002b4c699338ac99a4d55d51c60760ea86 |
| LCRC | 03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex | defc7033fb8c9f49cbfb8b9b278ca71aa34925ac |
| BULK | 03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex | 66d3e66aaf99567440a9ebe84fd38c40b047ac83 |
| Q2 | 02_entry_AN02/AN02_Q2_profiles_and_localized_tracking_v1.tex | ebbd6a20f3dfe187430bdab08b2b1d7d65ba8c6f |
| Q2E | 02_entry_AN02/AN02_Q2_boundary_layers_and_cohort_energy_v1.tex | cce55e1029cfd1ca8afb98eb649389b420d3992b |
| PROFILE | 02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex | 3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a |
| OWPT | 02_entry_AN02/AN02_overlap_window_profile_transfer_v1.tex | 8fac13f9d36255d3e2e23cc9b2196719ec602907 |

MOMC is listed in the updated README and roadmap, and the user explicitly reports it reviewed and verified. Retrieval of the expected repository path returned 404; a filename search found no result, and the extensionless path also failed. This increment therefore uses the **existing user-reviewed local MOMC source** from this conversation, rather than claiming to have fetched its current repository bytes:

**outputs/02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex**

Local SHA-256: **364a6fade2d10b95cec8c4591df42a742d3f4fcf9eb4e20ec4aabd1a339b125a**.

The source conclusions used agree with those restated in the user’s current request. No source-availability failure is used as the mathematical obstruction. The connector access is authorized by the current read-only repository instruction, which supersedes H2’s older blanket prohibition on GitHub access.

| New label, all prefixed an02q2epv1: | Scope and dependency |
|---|---|
| energy; massratio; entryenergy; earlyenergy | Exact original-flow result. Q2E prefix inc:AN02:q2completion:v1:, energy/Jupper/Hupper; P pa:targetcomparison; MOMC massclaim/radial/massintegral/outsideclaim. |
| field; coherentfield; fieldbudget | Exact original-field consequence on a prescribed square. MOMC reduction/meanintegral/decay/outsideclaim; elementary Lipschitz donor replacement. |
| obstruction; scalar; logidentity; missingbudget; failure | Exact comparison within the defined coherent leading system; analytic Gaussian and logistic identities displayed in the proof. |
| failedinequality; requested; stop | Failed uniform small-relative-error estimate and precise unresolved original-flow matching obligation. |

The proposed eventual location is an S1 Q2-entry increment: retain the proved whole-Q2 entry-energy lemma and the diagnostic of the proposed multiplier. No previous theorem is replaced; no consolidation or label migration is performed.

## Deliverable checks

The standalone TeX compiled successfully with the built-in LaTeX compiler after correcting a notation-package issue. Compilation is a typesetting check, not mathematical verification. The source remains open in the editor. All 17 new labels have the required prefix and are unique; all local references resolve. A SHA-256 comparison of all 25 pre-existing workspace files found no changes. No GitHub mutation, numerical experiment, or prior-file edit was made.
