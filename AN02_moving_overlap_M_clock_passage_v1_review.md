# AN02 moving-overlap M-clock passage v1 — review note

**Result: Parts A and B close through the first strong half-mass time.** This is a theorem for the original finite-noise initialized flow, uniformly for \(\rho\in[13/20,7/10]\) and sufficiently small \(q\), with \(S_0=q^{10}\). No new entry, clock, outside-mass, residual, or S2 contract is retained as a hypothesis.

Companion: **AN02_moving_overlap_M_clock_passage_v1.tex**. Unique prefix: **an02momcv1:**. The TeX contains the proofs. No earlier file or repository content is changed.

## Exact advance and errors

Write \(\ell=\log(1/q)\), \(u=\sigma-1/2\), \(v=\zeta-1/2=u-1\). Then

\[
t_m=(2/\omega+1/2)\ell,\quad M_0=A_q q^u,\quad
\epsilon_m=q^{s+d/2},\quad u\ge169/102,\quad v\ge67/102.
\]

The moving-overlap theorem gives OWPT’s original-versus-exact-target comparisons with angular exponent \(O(q^v)\), radial exponent \(O(q^u)\), maximum centered displacement \(O(q^{d/2})\), and normalized first absolute moment \(O(\epsilon_m)\). “Every label” here means **every fixed right-half-circle label**. The initial left half-circle is treated separately, without assuming it has charted.

The main theorem proves the following, uniformly up to the first \(M=1/2\):

| Requested part | Proved conclusion |
|---|---|
| (a) Mass clock | \(M'/M=1-M+\delta_M\), with integrated absolute defect at most \(Cq^2\ell^2\); \(t_h=10\ell-\log A_q+O(q^2\ell^2+q^u)\) |
| (b) Mean and chart | The actual reference remains \(o(1)\) from the stationary leading center; explicit convolution and integrated bounds; all strong coordinates remain in the chart \(R=79/51\) |
| (c) Shape | Every input/output pair separation changes by \(\mathcal G(M(t),M_0)e^{O(\mathcal D_q)}\), uniformly over arbitrarily close pairs and all intermediate endpoints |
| (d) Weights and tails | Relative strong radial growth factors differ by \(e^{O(q^2\ell^2)}\); the normalized tail sandwich has shape error \(O(\mathcal D_q)\) and weight error \(O(q^u+q^2\ell^2)\) |
| (e) Left ancestry | \(\mu(t)\le Cq^2\ell^2M(t)\), and \(\int\mu/q\le Cq\ell^2\); its mass is uniformly \(o(q)\) |

The tangent-error budget is

\[
\mathcal D_q=q^{d/2}+\epsilon_m+q^v+q^2(1+\ell)+q\ell^2=o(1).
\]

The terms account respectively for maximum width, donor moment, initial reference offset, finite-noise reduction, and left ancestry. In particular the nonlinear width cost is \(O(e^{-dC_m})=O(q^{d/2})\), repairing SMCP’s fixed-offset obstruction.

The actual normalization is retained:

\[
\epsilon_mM_0^d=A_q^dq^{10d-s},\qquad c_A\le A_q\le C_A.
\]

At half mass the tail parameter and cutoff scale are

\[
\sqrt2 A_q^d(1-M_0)^\alpha q^{10d-s},
\qquad \sqrt2 A_q^d(1-M_0)^\alpha q^{10d-2s},
\]

up to the stated profile comparisons and vanishing exponential errors. Neither \(A_q\) nor PROFILE’s fixed power-law comparison constants are replaced by one.

## Part A: time uniformity audit

PROFILE’s entry theorem already quantifies over terminal times satisfying

\[
T\ge(2/\omega)\ell+C,\qquad q^2T\le1.
\]

Its constants do not require a fixed additive offset. The new lemma checks the actual proof:

- The post-arrival integral of the absolute displacement is uniformly bounded by scalar contraction. Thus the nonlinear factor multiplying \(e^{-\sigma_q(T-T_L)}\) is bounded independently of elapsed time.
- Replacing \(\sigma_q=d+O(q^2)\) by \(d\) costs \(e^{O(q^2[T+\ell])}\).
- The radial argument costs \(e^{O(q^2T)}\) and a uniformly bounded own-gate integral for \(T\le q^{-2}\).
- The Q4 companion uses the same time guard and local contraction.
- The tail argument integrates those uniform comparisons.

The moving logarithmic time lies within this domain. The proof also identifies the unrestricted post-arrival formulation: keep the exact angular exponent \(\sigma_q\) and exact radial rate \(\kappa_q=2g(qa_q)\). Their nonlinear factors are bounded for all subsequent target-only times. The leading-rate expressions \(e^{-dT}\) and \(e^T\) are **not** asserted to have uniform factors as \(T\to\infty\) at fixed \(q\).

OWPT is extended through its explicit bounds

\[
\overline S(t_m)=O(q^u),\qquad q^{-1}\int_0^{t_m}\overline S=O(q^v).
\]

Its receiver-Jacobian and stochastic-propagator constants do not depend on terminal offset. A growing number is not simply substituted into fixed-offset big-O notation. Original shape comparisons stay multiplicative around the actual reference.

## New estimates that close Part B

### Whole-left-circle entry and propagation

The left-entry lemma applies PROFILE’s exact target-only Cartesian equations to every label with initial first coordinate nonpositive. Positive parts satisfy

\[
(U_1^+)'\le(1/2+q^2)U_1^++Cq\sqrt{\widehat m},\qquad
(U_2^+)'\le(\lambda/2+q^2)U_2^++Cq\sqrt{\widehat m},
\]

and negative parts grow at most at rate \(q^2\). Since \(U_1^+(0)=0\), this gives

\[
\widehat m(t,\beta)\le Cq^{10}e^{2q^2t}
\{1+e^{\lambda t}+q^2(1+t)^2e^t\}.
\]

P’s early radial comparison holds for all labels. At \(t_m\), division by \(M_0\asymp q^{10}e^{t_m}\) yields \(b_0:=\mu(t_m)/M_0\le Cq^2\ell^2\).

During the stopped passage the exact generic upper bound

\[
(\log m)'\le(1+2q^2)(1+S)
\]

applies without angular restrictions. Comparing it with the proved strong mass rate gives

\[
(\log(\mu/M))'\le4M+Cq^2,\qquad \int M\le3/2.
\]

Thus \(\mu/M\le e^7b_0\), improving the guard \(e^8b_0\). This follows the entire fixed left ancestry, including later recruited labels. It uses neither a frozen uncharted mask nor a capped radial-gain contract.

### Finite-noise value and receiver derivative

The reduction lemma proves

\[
\|\mathcal F_q-f\|_{C^1_{x,y}}\le C_Rq^2+160\mu/q,\qquad
\left|(\log m)'-(1-M)\right|\le C_Rq^2+3\mu.
\]

This is a new analytic remainder proof, not an inference from P’s formal leading-order derivation.

On \(P_1\), the own gates can be removed with exponentially small value and first-receiver-derivative errors. Boundary Gaussian moments have a fixed positive mean-to-noise margin on the chart; polynomial powers of \(q^{-1}\) are dominated by the exponential.

On \(P_2\), condition on \(V=\rho+qZ_2\), with \(X_1=qZ\) independent. The exact feature is

\[
a_x\cdot X=q\cos(qx)[Z+t_xV],\qquad t_x=\tan(qx)/q.
\]

Gaussian integration in \(Z\), followed by Taylor expansion in \(V\), gives the leading field with an \(O(q^2)\) receiver-\(C^1\) remainder. The proof explicitly checks

\[
\partial_x[VF(t_xV,t_\xi V)]
=t_x'V^3(t_\xi-t_x)_+\phi(t_xV)\quad(V\ge\rho/2).
\]

The value and first receiver derivative have uniformly bounded second \(V\)-derivatives with polynomial envelopes, even at coincident thresholds. The complementary event is exponentially small. No uniform second receiver derivative across coincident gates is presumed.

The requested \(y\)-row check is

\[
\partial_x f_y=\frac{\lambda}{2}\Phi(\rho x),\qquad
\partial_y f_y=-(1-M)/2.
\]

The collective diagonal \(-1/2\) also varies the donor mean and is a different derivative. At the atomic center, the receiver matrix is exactly \(J_{\rm sh}(M)\).

### Joint bootstrap and the tangent comparison

The chart is fixed first from the stationary root:

\[
a_\rho<28/51,\qquad R=79/51.
\]

The auxiliary stopped guards are \(e<\epsilon_*\), \(r<\epsilon_*\), and \(\mu/M<e^8b_0\), together with \(M<1/2\) and the deterministic ceiling \(3\log(1/(2M_0))\). The proof derives \(M'/M\ge1/3\) inside the guards; the ceiling is not an independent clock premise.

The actual reference satisfies

\[
D^+e\le-ge+CM\overline D+Cq^2+C\mu/q,
\]

and the receiver derivative differs from \(J_{\rm sh}\) by at most

\[
C(e+r+M\overline D+q^2+\mu/q).
\]

The local guards give contraction of each label-reference difference at rate \(1/20\). With radial-weight comparison this yields

\[
r(t)\le r(t_m)e^{-(t-t_m)/20},\qquad
\overline D(t)\le C\epsilon_m e^{-(t-t_m)/20}.
\]

The mean and radius guards improve, as does the outside guard. All estimates hold at every stopped endpoint. There is no backward inference from a terminal cap.

After closure, normalize each tangent by its exact target-only tangent at \(t_m\) and by \(\exp\int r_0(M)\):

\[
w'=\alpha\begin{pmatrix}-1&1\\1&-1\end{pmatrix}w+\mathcal E w,
\qquad w(t_m)=\boldsymbol1+O(q^v).
\]

The base propagator is row-stochastic, and the proved integral of \(\|\mathcal E\|\) is \(O(\mathcal D_q)\). Variation of constants gives positivity and \(w_j=e^{O(\mathcal D_q)}\). Possible finite-noise violations of cooperativity are bounded through \(\mathcal E\), not assumed absent. Integration over any label interval proves the uniform pairwise result. The exact logit equation converts the time multiplier to \(\mathcal G\).

## Order-one constants and guard independence

None of these constants depends on LCRC’s guards. The \(M\) here is an actual ancestry mass, not LCRC’s residual guard.

| Constant | Definition and role |
|---|---|
| Ratio box | Fixed \([13/20,7/10]\), supplying \(1-\lambda\ge51/100\) and the reviewed root/rate bounds |
| \(a_\rho,\alpha,d,\omega,s\) | Existing analytic root and rate functions |
| PROFILE’s \(L\), arrival offset and comparison constants | Used in Part A with the explicit uniformity audit |
| \(c_A,C_A\) | Positive uniform bounds obtained by integrating the radial profile |
| \(A_q\) | Actual \(M_0/q^u\), contributing \(-\log A_q\) to phase and \(A_q^d\) to shape |
| \(R=79/51\) | Passage chart chosen from \(a_\rho<28/51\), before the bootstrap constants |
| \(C_R\) | Analytically bounded Gaussian-kernel remainder constant on the fixed chart |
| \(160\) | Enlargement of PROFILE’s componentwise outside constant \(40\) for combined value/derivative norms |
| \(3\) | Radial outside bound, from \(2a_*\mu\le3\mu\) |
| \(C_0^*=724/51\) | Uniform upper bound for LOC’s \(4(a_\rho+3)\) |
| \(\gamma_*=1183/20800\), \(g=\gamma_*/2\) | Uniform collective attraction and absorbed mean decay |
| \(C\) | Fixed enlargement of the preceding kernel, Gaussian Lipschitz, and norm-conversion constants |
| \(\epsilon_*=\min\{1/4,\gamma_*/(4C_0^*),1/(80C)\}\) | Local mean/width guard selected after the chart constants |
| \(K_B=e^8\), improvement \(e^7\) | Outside mass-ratio guard and strict improvement |
| \(1/3,1/20,3/2\) | Lower mass growth, width contraction, and integrated mass bound |
| \(\sqrt2\) | Exact half-mass multiplier prefactor, since \(d+\alpha=1/2\) |
| Final error constants | Fixed combinations of the foregoing and \(1/g\), multiplying displayed vanishing scales |

The constant \(C_R\) can be chosen from finitely many polynomial Gaussian moment bounds, compact trigonometric derivative bounds, and suprema of \(q^{-k}e^{-c/q^2}/q^2\) on a fixed small \(q\)-interval. Their finiteness is established analytically. No numerical evaluation is used.

There is no freely fixed \(C_m\) here: \(C_m=\ell/2\). The actual radial normalization is kept through \(A_q\), not absorbed into an asserted zero phase.

## Proof audit points

- **Stage order:** the moving-overlap data are proved before continuation. Part B’s outside entry budget is derived from initialized coordinates.
- **Time limits:** leading-rate target comparisons retain \(q^2T\le1\); unrestricted post-arrival comparisons keep exact rates. The requested moving time satisfies the former.
- **Fixed-label bookkeeping:** both ancestry groups and the reference are fixed. No moving-mask flux or recruited mass is discarded.
- **Reference:** it remains the original characteristic launched at \(qa_q\). The stationary leading point only controls its mean error. No additive angle error is divided by a small shape.
- **Gaussian derivatives:** own-gate boundary tails and the cross-gate coincident-threshold derivative are checked. Only first receiver derivatives are needed.
- **Scaling:** each Gaussian cluster carries the mixture factor \(1/2\); angular velocities are divided by \(q\) before estimating their errors.
- **Receiver versus collective:** the donor measure and \(Y\) are held fixed in receiver derivatives. The collective matrix is a different variation.
- **Zero-coordinate cases:** positive/negative-part inequalities use upper Dini derivatives. The width norm inequality also covers vanishing coordinates and mixed signs.
- **Divisions:** \(M,\mu\) remain positive on finite intervals. Nontrivial target tangents and ordered pair separations are positive; zero reference displacement stays zero.
- **Outside propagation:** the generic radial upper rate is compared with derived strong mass growth. Entry smallness is not assumed to persist.
- **No early-comparison overreach:** \(S/q\) is used only through the overlap, where \(S\ll q\). Afterwards the full strong output is kept in the structured field and only the complement is charged at \(\mu/q\).
- **Integration:** labelwise comparisons are uniform on finite measures. Tonelli is used for nonnegative convolution bounds. Gaussian regularity justifies the receiver variational equation at fixed \(q>0\).
- **First exit:** all auxiliary guards improve. The time ceiling and positive mass-growth rate force a half-mass hit without a future cap or independent clock.
- **Width versus moment:** the largest width is \(q^{d/2}\); the normalized first moment is \(\epsilon_m\). These are not interchanged.
- **Tangent positivity:** it follows from the stochastic propagator and integrated small perturbation, without assuming exact finite-noise cooperativity.
- **Tail interpretation:** vanishing errors compare exact normalized profiles. The power-law constants and finite cutoff are retained.
- **Stopping boundary:** no argument uses dynamics after \(M=1/2\).

## Source provenance

The sources below were read directly from the private repository using read-only fetches. Git blob identifiers specify the versions used. The roadmap’s route is not a proof premise.

| Source | Git blob SHA |
|---|---|

| [README](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/README.md) | edd6f9b94ff3836087feec1b5e806f19fad10e26 |
| [Roadmap v1.4](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md) | ca0174766c9b2879b3a8155c25bef00b65574a07 |
| [OWPT](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_overlap_window_profile_transfer_v1.tex) | 8fac13f9d36255d3e2e23cc9b2196719ec602907 |
| [SMCP](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_strong_M_clock_passage_v1.tex) | c880197f1e9642f4641017fe313aa6d3d6904d31 |
| [PROFILE](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex) | 3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a |
| [LOC](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_local_rate_mean_tracking_v1.tex) | eb1fa397d1f0d9b0e3aea1698b9960726e739fa8 |
| [P](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex) | cb458c933aa043cf0188fd11c46bf4246ffc91d8 |

Dependencies by source label:

- **P:** exact balanced equations and matrix envelopes; pa:earlybounds, pa:targetcomparison, pa:resident, pa:spectra and pa:order. Its formal field derivation is not used as a remainder theorem.
- **PROFILE:** inc:AN02:profile:v1:coordinate, root, arrival, entry, rightcircle and cost (Proposition 4.1).
- **OWPT:** an02owptv1:jacobian, tangents, transfer and tail. Their explicit bounds supply the moving-time extension.
- **SMCP:** an02smcpv1:shortobstruction, leadingtest and handoff. The fixed-offset obstruction remains valid and is not re-proved.
- **LOC:** inc:AN03:local:v1:field and meanineq (Lemma 3.1), including its collective Taylor bound.
- **Roadmap:** v1.4, S0 assembly requirements, S1 step 2 and ledger items 12–14.

The roadmap is dated October 7; this increment uses the session date October 6. Dates carry no mathematical premise. Source reading and document checks are not numerical experiments.

## Supplied contracts and stopping point

This supplies S1’s original strong passage from moving overlap to half mass: a phase-accurate mass clock with explicit \(A_q\), a chart fixed independently of LCRC, a controlled actual reference, uniform pairwise profile transfer, radial-weight stability, and an integrated left-ancestry field budget.

It does not supply LCRC’s later entry time \(t_0\), its Q2 Cartesian ratios or signs, \(J_{\mathcal G}(t_0)\), the weak amplitude seed, secondary entry profile, or the later guard-independent integral of \(\lvert1-\kappa_1\rvert\). Strong saturation and every continuation beyond \(M=1/2\) are outside the increment. No capped gain, bridge, or consolidation is performed.

The intended eventual placement is a separate S1 step 2a result following OWPT, subject to mathematical review. No replacement label map is needed: this theorem uses a moving overlap and leaves the prior fixed-offset result intact. No theorem remains conditional on an unproved auxiliary budget, and no stop-rule obstruction was encountered after the displayed checks.

Document validation: the complete TeX source compiled successfully in the built-in editor. All 37 labels have the requested unique prefix, and all 29 internal references resolve. SHA-256 comparison confirmed that all 21 pre-existing workspace files remain unchanged. No experiments, numerical sign checks, or GitHub mutations were performed.
