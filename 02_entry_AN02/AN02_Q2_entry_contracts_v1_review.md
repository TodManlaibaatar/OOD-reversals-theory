# AN02 Q2 entry contracts v1 — review note

**Result: the requested fixed-constant primary Q2 entry contracts close at \(t_0=t_h\).** The theorem concerns the exact original, balanced untied flow with \(S_0=q^{10}\), uniformly on \(\rho\in[13/20,7/10]\) for sufficiently small \(q\). No additional residual, clock, crossing, sign, or entry hypothesis is retained.

Companion: **AN02_Q2_entry_contracts_v1.tex**. All new labels use **an02q2ecv1:**. This is a separate increment; Q2EP and all earlier sources remain unchanged.

## New advance

For a fixed prescribed \(C_0>0\), choose \(K=K(C_0)\) as specified below. At strong half mass, the primary group \(c_0\ge Kq^\gamma\) has
\[
z>0,\qquad |a_{\rm as}|/z\le1/4,\qquad qj/z\le C_0.
\]
The clock \(\mathcal C_q=\{c_0\ge q^{1/4}\}\) is contained in that group for small \(q\), and
\[
qj/z\le C_{\rm clk}q^{1/8}.
\]
The clock seed has its actual normalization retained:
\[
H_{\mathcal C_q}(t_h)
=A_q^{-\lambda}\widehat H_{\mathcal C_q}(10\ell)\,e^{o(1)}
\asymp A_q^{-\lambda}q^{10(1-\lambda)}.
\]
Every complementary Q2 label \(c_0<Kq^\gamma\) satisfies
\[
|\theta(t_h)|+|\psi(t_h)|\le Z(C_0)q.
\]

Q2EP’s already verified \(J_G(t_h)\le C_Jq^3\) and \(E_{G_+}(t_h)=o(1)\) are cited and not reproved. Together these results supply LCRC’s **primary entry** contracts and the fixed Q2 chart cap at the proposed common time.

| Requested part | Supplied result |
|---|---|
| (a) Off-chart field | Exact full-gate decomposition, explicit selected Gaussian matrices, diagonal and cross-entry remainder bounds, and the retained \(-qMa_\rho/2\) cross drive. |
| (b) Two-sided transport | \(q\cot\theta=D_h^{-1}q\cot\widehat\theta\,\exp[O(1/x_{\min})+O(\eta_q)]\); the exponent is bounded in absolute value. This yields fixed \(K\) and the clock ratio. |
| (c) Signs and antisymmetry | A damped exact angle-difference estimate, positive matched coordinates, and the stated \(z,a_{\rm as}\) inequalities. Late crossings differ from target crossings by \(o(1)\), hence by \(O(1)\). |
| (d) Clock seed | The formula above, with \(A_q^{-\lambda}\) explicit and a uniform vanishing error relative to the exact target seed. |
| (e) Chart group | A fixed square is invariant through half mass; entry into it follows from stopped two-sided transport or early absolute comparison. |

Here
\[
\ell=\log(1/q),\quad
u=10-2/\omega-1/2,\quad
D_h=\sqrt{2(1-M_0)},\quad
\eta_q=q^{1/1000}+q^{4/51}+q^{u-1}+q\ell^2+q^2\ell=o(1).
\]
For the primary group, \(x_{\min}=\min_{[t_m,t_h]}\theta/q\). This is a scaled angle; it is **not** BULK’s Cartesian ratio \(X_B=qj/z\).

The theorem retains the bounded cross correction at a fixed cutoff. It does not restore the universal \(e^{o(1)}\) claim withdrawn in roadmap ledger item 15. On the clock the scaled-angle minimum diverges, so the same correction does vanish.

## What closes the crossing layer

A direct integration of a relative weak-coordinate error before a weak seed exists is avoided. Instead, first match the original and target receivers through a narrow band around the weak axis.

Fix
\[
\varepsilon=1/1000,\qquad r_q=q^{1-\varepsilon},\qquad
T_b=(19/2)\ell+C_b^0.
\]
The physical width \(r_q\) tends to zero, while \(r_q/q\) tends to infinity. \(C_b^0\) is a fixed band-exit allowance, unrelated to LCRC’s response cap.

Q2E supplies target crossing by \((1600/169)\ell+O(1)\). The subsequent target cosine grows at logarithmic rate at least \(\omega/2\) until it reaches \(2r_q\). The strict analytic margin is
\[
\frac{1600}{169}+\frac{400\varepsilon}{51}
=\frac{1600}{169}+\frac2{255}<\frac{19}{2}.
\]
Thus every relevant target exits this band before \(T_b<t_h\), while MOMC gives
\[
M(T_b)\le C A_q q^{1/2},\qquad M'/M\ge3/4
\]
on that early part of the strong passage.

The full-gate strong angular field in this band is bounded by
\[
C M\big((\cos\theta)_++q+|\Delta|\big)+C\mu,
\qquad \Delta=\psi-\theta.
\]
On the Q2 side, the factor \(|\cos\theta|\Phi(\cos\theta/q)\) is \(O(q)\). On the Q1 side of this band, the cosine is at most \(3r_q\). The bound therefore respects the weak-axis geometry instead of paying the global \(O(M)\) angular cost.

The exact target field has Lipschitz constant \(a_*=1/2+q^2\). Combining this with the angle-difference estimate gives
\[
|\theta-\widehat\theta|
\le Cq^u e^{a_*(t-t_m)}+Cr_qM(t).
\]
Consequently the angular error divided by \(q\) is
\[
O(q^{4/51}+q^{1/2-\varepsilon})=o(1).
\]
The first exponent follows from
\[
u-1-\tfrac12(19/2-c_m)
=17/4-c_m/2\ge4/51,\qquad c_m\le851/102.
\]

The fixed crossing layer has strictly nonzero clockwise scaled speed:
\[
q^{-1}v_0(\pi/2+qw)
=-\tfrac12[\mathcal K(-w)+\lambda w]+O(q^2).
\]
The bracket is positive for every finite \(w\), with a uniform positive minimum on each fixed compact layer. This transfers the original crossing with a vanishing time error. For late crossers,
\[
M(T_\times^{\rm o})\le C A_q q^{90/169},\qquad
90/169=10-1600/169.
\]
The reduction in the P1 push therefore does not create a growing delay.

Radial comparison on the same band has a vanishing logarithmic defect. At its exit, the first direction coordinate is comparable to \(r_q\), the second to one, and both original Cartesian coordinates match the same-time target coordinates relatively. The subsequent transport proof divides only by these positive coordinates.

## Field and transport audit

The full-gate matrix identity is
\[
R_\theta=\tfrac12\big[(I-T_s)A_\theta^{(1)}
+A_\theta^{(2)}-B_\theta^{(2)}\big]
+O(\mu+Me^{-c/q^2}),
\]
where \(T_s=\int_{\mathcal R}W U^T\), and \(B^{(2)}\) retains the selected strong output on P2. Strong donor gates are removed only on P1, where MOMC’s fixed donor chart gives an exponential margin. The receiver gate is retained.

For a Gaussian with mean \(b\), the selected second-moment matrix is displayed exactly:
\[
A_b=(bb^T+q^2I)\Phi(t)
+q\phi(t)(ba^T+ab^T)-q^2t\phi(t)aa^T,\qquad t=b\cdot a/q.
\]
This gives diagonal drives \((1-\kappa_1)/2,\lambda/2\), with explicit gate remainders. The target cross entry
\[
a_{12}=\frac q2\big[\sin^3\theta\,\phi(t_1)
+\rho\cos^3\theta\,\phi(t_2)\big]
\]
is retained separately. At fixed gate margin it need not be \(O(qM)\) when \(M\) is small. The **training** cross contribution is \(O(qM)\); both cross entries carry the coherent term \(-qMa_\rho/2\), with donor-spread, gate and finite-noise remainders.

The exact difference equation is
\[
\Delta'=-\operatorname{tr}(R_\theta)\sin\Delta
+(C_{\theta,12}-C_{\theta,21})\cos\Delta.
\]
On the stopped upper sector, the trace is uniformly positive and the skew forcing is \(O(qM+\mu)\). Therefore
\[
|\Delta(t)|\le C_\Delta\big[q^u e^{-c_\Delta(t-t_m)}+qM(t)\big],
\qquad c_\Delta=169/6400.
\]
This uses no finite-noise cooperativity assumption.

After the weak-axis band, stop before either input angle reaches \(qL\), with \(L\) fixed and sufficiently large. The relative coordinate estimates show
\[
(\log\cot\theta)'\ge1/1000.
\]
Thus the input angle decreases and the first-coordinate margin cannot close. The two coordinate comparisons are
\[
\log(U_1/\widehat U_1)=-\tfrac12\int M+O(\eta_q),
\qquad
|\log(U_2/\widehat U_2)|
\le C/\underline x+O(\eta_q),
\]
where \(\underline x\) is initially the smaller original/target scaled-angle minimum. The resulting two-sided cotangent bound makes those minima comparable, giving the theorem’s original-only \(x_{\min}\).

The Gaussian gate deficit near the fixed strong-side margin is integrated using the decreasing sine, rather than multiplied by the full logarithmic duration:
\[
\int \mathcal T(\rho\sin\theta/q)
\le \frac2b\int_{2\rho x_*/\pi}^{\infty}\mathcal T(w)\frac{dw}{w}
+O(\ell e^{-c/q^2})
\le C/x_*.
\]
Here \(b=1/1000\) and \(\mathcal T(w)=(1+w^6)e^{-w^2/16}\). This is a Gaussian integral estimate, with no numerical evaluation.

The signed correction identified by Q2EP is therefore bounded, not discarded. The proof uses general untied coordinate estimates; it does not apply the aligned-ray scalar identity to an unproved aligned original trajectory.

## Constant choices and independence from LCRC

All constants below are fixed before the LCRC residual guards are introduced. Dependence on the prescribed \(C_0\) occurs only through the cutoff and its chart cap. The small-\(q\) threshold may depend on these fixed constants.

| Constant or factor | Definition and role |
|---|---|
| \(R=79/51\) | MOMC’s existing strong donor radius. |
| \(a_\rho\), \(a_{\max}=28/51\), \(\omega_{\min}=51/200\) | Resident root and existing analytic box bounds. |
| \(A_q\in[c_A,C_A]\) | Actual MOMC normalization, never reset to one. |
| \(B_A=1+\max(|\log c_A|,|\log C_A|)\) | Fixed allowance for extending target entry statements from \(10\ell\) to \(t_h\). |
| \(C_1,C_{\rm tr},C_\Delta\) | Analytic moment, relative-transport and angle-difference constants from the displayed estimates. They depend on the fixed ratio box and donor radius, not a residual guard or \(L\). They are fixed before \(L\). |
| \(c_\Delta=169/6400\) | Explicit weakened damping coefficient for the angle difference. |
| \(b=1/1000\) | Explicit lower logarithmic cotangent rate after the band. |
| \(\varepsilon=1/1000\) | Auxiliary band exponent; separate from the preceding rate despite having the same convenient value. |
| \(C_b^0\) | Finite target crossing/post-crossing-layer time allowance used in \(T_b\). |
| \(L\) | Fixed large receiver margin. Choose it to make the displayed \(C_1/L\), Gaussian gate errors, \(C_\Delta/L\), and \(C_{\rm tr}/L\) smaller than the stated fixed margins. Gaussian decay proves existence. |
| \(C_T\) | Target primary-ratio constant, including a fixed \(e^{CB_A}\) time-shift allowance. |
| \(C_B^T\) | Target clock-ratio constant with the same bounded-time extension. |
| \(Z_T(K)\) | RCET’s finite target chart cap, enlarged for the bounded time shift. |
| \(K(C_0)\) | \(2[\max\{1,16C_T/C_0,32C_TL\}]^{49/51}\). The exponent uses \(r_\lambda\ge51/49\). |
| \(C_{\rm clk}\) | \(4C_B^T\), independent of \(C_0\). |
| \(B\), \(Z\) | \(B=8[L+Z_T(K)+C_\Delta+1+a_{\max}/\omega_{\min}]\), \(Z=2B\). These are Q2 chart constants; \(B\) is not LCRC’s residual-integral guard. |
| \(C_B\) in the square-field remainder | Analytic finite-noise constant for the fixed square radius \(B\). It affects the allowed smallness of \(q\), not any earlier constant choice. |
| \(C_J\) | Existing Q2EP constant \(4e^7C_Q/c_A\), independent of the subdivision at \(C_0\). It is cited, not reproved. |

The order-one \(A_q\) dependence is:

- The actual entry mass is \(M_0=A_q q^u\), and the half-mass time is \(10\ell-\log A_q+o(1)\).
- The diagonal factor is \(D_h^{-1}=[2(1-A_qq^u)]^{-1/2}\).
- The clock amplitude carries **\(A_q^{-\lambda}\)** relative to the target amplitude at \(10\ell\).
- The early strong-mass estimates retain a factor \(A_q\), including \(M(T_\times^{\rm o})\le C A_q q^{90/169}\).
- Q2EP’s aggregate energy retains its earlier **\(A_q^{-1}\)** upper factor.
- \(K\) and \(Z\) may depend on the fixed bounds \(c_A,C_A\) through \(B_A\); no unproved precise time-shift power is assigned to the primary threshold.

In particular none depends on LCRC’s \(B,E_g,K_Y,M\) guard choices. The chart radius arises from the leading field’s inward-pointing fixed square and the transferred target cap.

## Signs, divisions and continuation checks

- All groups are fixed initial-label sets. No moving-mask integral is differentiated.
- Balance is used throughout; original alignment is never assumed.
- The first-coordinate logarithms start only after positive seeds have been matched. No division by a zero crossing coordinate occurs.
- Before the band exit, estimates use angle and radial errors, not \(qj/z\) at a nearly zero seed.
- The upper-sector and angle-difference guards in the band improve strictly; the original cosine cannot reach \(3r_q\) before the target reaches \(2r_q\).
- On the off-chart interval, \(\sin\theta\ge2qL/\pi\) and \(\cos\theta\ge r_q/2\). The angle-difference estimate makes both output coordinates positive as well.
- The positive cotangent rate improves the cosine guard. A hypothetical primary hit of \(qL\) contradicts the target ratio bound and the two-sided transport.
- The antisymmetric bound follows from the exact sine ratio, with \(|\Delta|/\sin\theta\le1/8\), not from small absolute energy.
- The chart-square argument proves inward pointing first for the leading field, then uses the uniform finite-noise value error to preserve strict signs. It assumes no sign for the finite-noise Jacobian.
- Its upper-corner contraction is at least \(1/200\); its lower-corner inequalities are displayed. This use concerns Q2 chart entry and control only through \(t_h\).
- Uniform labelwise bounds justify integration of the clock seed. Its fixed-cohort measure is finite; the lower seed constant comes from a fixed interior Q2 interval.
- Endpoint regularization \((s_0+q),(c_0+q)\) is retained in the source crossing and target-dichotomy inputs.
- Source hypotheses requiring \(\int r\le B\) are never invoked on the strong passage.
- Gaussian tails are integrated analytically or bounded by explicit exponential moments; no sampled signs, numerical trajectories, interval arithmetic or experiments are used.

## What remains outside this increment

This supplies the requested primary entry geometry and clock seed at the proposed \(t_0=t_h\). It does not prove LCRC’s later retained inputs or complete initialized S1 in its entirety.

The secondary recruited population still needs its original-flow entry displacement/radial profile and normalized tail about an actual same-field reference. A fixed chart cap and the whole-Q2 \(q^3\) mass bound do not supply that profile. Its later pre-exit distance and capped radial-gain contracts also remain separate.

No weak passage, \(B_s\), core retention after \(t_h\), secondary-tail transfer, capped gain, bridge analysis, or consolidation is undertaken. The proof stops at half mass.

## Source provenance and label map

All requested source files were available from the updated repository through read-only access, including MOMC and Q2EP. The current roadmap identifies itself as **v1.6**. Its revised S1 step 6 and ledger item 15 control the accuracy target; the older universal-\(e^{o(1)}\) wording retained later in that section is not used as a contract.

GitHub-reported blob identifiers are recorded verbatim:

| Source | Repository path | Blob identifier |
|---|---|---|
| README | README.md | f8bff1b8d3716cd5dd1e8d739a8b3a522eedc467 |
| Roadmap v1.6 | 00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md | abc105ac969118864d8761960436f9828dbcce7d |
| Q2EP | 02_entry_AN02/AN02_Q2_entry_through_strong_passage_v1.tex | 042b3c93cf8402d10487f9e56f6f5b1d869c424a |
| MOMC | 02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex | 539427063c4a08551ce4cb8efe41dab61cde609c |
| RCET | 03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex | 49e352002b4c699338ac99a4d55d51c60760ea86 |
| LCRC | 03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex | defc7033fb8c9f49cbfb8b9b278ca71aa34925ac |
| BULK | 03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex | 66d3e66aaf99567440a9ebe84fd38c40b047ac83 |
| Q2 | 02_entry_AN02/AN02_Q2_profiles_and_localized_tracking_v1.tex | ebbd6a20f3dfe187430bdab08b2b1d7d65ba8c6f |
| Q2E | 02_entry_AN02/AN02_Q2_boundary_layers_and_cohort_energy_v1.tex | cce55e1029cfd1ca8afb98eb649389b420d3992b |
| PROFILE | 02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex | 3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a |
| OWPT | 02_entry_AN02/AN02_overlap_window_profile_transfer_v1.tex | 8fac13f9d36255d3e2e23cc9b2196719ec602907 |
| P | 01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex | cb458c933aa043cf0188fd11c46bf4246ffc91d8 |

| New label, prefix an02q2ecv1: | Scope and dependencies |
|---|---|
| main; primary; clockratio; transport; seed; chartentry | Exact original-flow entry result; assembled from the new lemmas and the source target-only dichotomy/seed. |
| field; fullgates; entries; signedcross; deltaineq; delta | Exact original-field identities and analytic estimates from Gaussian truncation, MOMC’s donor chart and PROFILE’s complement bound. |
| crossing; earlymass; latemass; weakangular; weakh; match | Original-flow crossing and band matching, using P’s exact target Lipschitz bound, Q2E’s endpoint-uniform crossings, and MOMC’s mass clock. |
| offtransport; relative; coordinatetransport | Two-sided original-versus-target coordinate transport with the bounded cross correction retained. |
| square | Exact original receiver-square invariance through \(t_h\), using Q2EP’s field lemma/MOMC’s reduction and displayed leading-field boundary signs. |
| targetcontracts; constants; Z | Bounded-time target extension and guard-independent choices of the fixed entry constants. |

No old label is replaced or remapped. The intended location is a separate S1 step-6 primary-entry increment, available for review before any eventual assembly.

## Deliverable verification

The standalone TeX compiled successfully with the built-in LaTeX compiler and remains open in the editor. Compilation checks typesetting, not the mathematical claims. All 30 labels are unique and use the required prefix; all local references resolve. A SHA-256 audit of all 28 pre-existing workspace files found no changes. No GitHub mutation, numerical experiment, or prior-file edit was performed.
