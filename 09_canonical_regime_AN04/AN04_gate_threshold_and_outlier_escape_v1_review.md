# S7b review — initial gate threshold and resident-phase escape

**Scope.** The entry shape is the normalized, unclamped CFS/RPS right-half comparison law. It is prescribed as aligned data for the defined leading system. Gate tests use \(0<M_0\le1\). The resident evolution results use \(M=1,\ N=0\). All clocks are normalized. The input family fixes \(c,A,\rho\) before \(q\) tends to zero.

| Item | Result | Scope |
|---|---|---|
| H1 | Closed. Unique saturated threshold \(b_c\), continuous in the parameters and strictly increasing in offset. | Initial aligned gate only. |
| Subunit mass and sufficient test | Closed. Both threshold sets have explicit integral descriptions and separate mass cutoffs. | Initial direction versus RPS's finite-time sufficient condition. |
| Large-input field | Closed. Affine receiver part, full common donor terms, and Gaussian error bounds are given separately. | Current finite-moment state at \(M=1,N=0\). |
| H2 upper bound | Closed as a growth envelope. Isolated ceiling \(\lambda/2\) is sharp for a passive receiver in the coherent field. Positive upper mass \(f\) lowers the per-rank ceiling to \(r_+(f)\). | Fixed finite initial coordinates. |
| Positive segment escape | Closed for each fixed horizon on an explicit fraction range. Sustained fixed-\(f\), positive-rate exponential escape on diverging horizons is contradicted for the continuous upper tail. | The finite-horizon rate depends on both \(f\) and the horizon. Slower or intermittent growth remains open. |
| Edge clock | A first-hit lower bound and candidate-clock comparison close. A two-sided escape clock for a fixed positive fraction is unavailable. | Scaled geometry requires \(qR_q\to0\). Uniform finite-noise transfer on growing charts remains open. |

## Initial threshold and parameter sets

Use \(L=H^{-1}\) from CFS and \(t=\rho\zeta\). For the unit-mass input law,
\[
 \langle j\rangle_b=\tfrac12 j(a)+\frac2\pi
     \int_0^\infty j(L(bu))(1+u^2)^{-2}\,du .
\]
The raw CFS density satisfies \(f_b(x)\sim Ab^3/(2\pi x^4)\), and the unit-mass density on its continuous part has tail coefficient \(2b^3/\pi\). First and second moments are finite. In particular \(\mathbb E X_b/b\to1/\pi\) as \(b\to\infty\).

Define \(S_b(\zeta)=\langle F(t,\rho x)\rangle_b\) by the displayed integral. Then \(S_b\) increases continuously and strictly from \(K(\rho a)\) to infinity. The saturated critical scale is the unique solution \(S_{b_c}(\zeta)=K(t)\). Gate motion is outward below it and inward above it. The initial velocity is zero at equality. To check the offset dependence, the equation at a root bounds \(\mathbb E(r-t)_+\le K(t)/\Phi(t)\) for \(r=\rho X_b\). The offset derivative at every root is strictly positive for \(K(t)-S_b\) by the strictly positive variance of a truncated normal. This gives strict increase of \(b_c\) with \(\zeta\). Continuity in \((\rho,\zeta)\) follows by bracketing the unique root. No monotonicity in \(\rho\) is required.

For \(M_0<1\), form
\[
 m_{\rm gate}=(\zeta-\rho K(t))/(\zeta-a).
\]
If \(M_0\le m_{\rm gate}\), every \(b>0\) gives inward motion. Above it, the threshold solves \(S_b=[\rho K(t)-(1-M_0)\zeta]/(\rho M_0)\); the same below/at/above sign rule applies. The threshold increases with \(M_0\).

The RPS \(g>0\) range instead requires
\[
 M_0>\frac{\zeta+1-\rho K(t)}{\zeta+1-a},\qquad
 \mathbb E X_b<\frac{\rho K(t)-(1-M_0)(\zeta+1)}{M_0}.
\]
The second inequality gives \(0<b<b_g\) with a unique equality endpoint whenever the mass condition holds. At fixed \(M_0\) this is a strict subset of the outward-gate range whenever nonempty. These signs are instantaneous. A zero initial velocity does not specify subsequent gate motion.

## Escape at saturation

With \(t=\rho x\), the exact common forces in \(2U,2V\) are \(-\rho K_s,-Y\). The linear receiver terms are \(\lambda y,\lambda x\). The errors are respectively \(\rho\phi(t)-\lambda y\Phi(-t)+\rho(K_s-S(x))\) and \(\rho K(-t)\), with \(0\le K_s-S(x)\le\rho\Phi(-t)\int \tilde x_+d\mu\) for \(x\ge0\). No smallness of the escaping donors is presumed.

**Finite lower barrier.** Let \(D_0=1+\int(|x|+|y|)d\mu_0\), \(C_h=2D_0e^{7h}\), and \(\xi_f\) be the initial \(1-f\) input quantile. For \(0<f<1/2\) with \(\lambda\xi_f>C_h\),
\[
 r_-(f,h)=\frac{\lambda-C_h/\xi_f}{2}>0 .
\]
The upper \(f\) fraction has both coordinates at least \(\xi_f e^{r_-(f,h)s}\) through \(s=h\). The proof first bounds all first absolute moments, including the escaping labels, then checks each face and the corner of the moving orthant. As the horizon increases the sufficient range of \(f\) shrinks. This statement concerns growth of upper labels which may already be probe-inactive.

**Upper bound.** For a rank with upper mass at least \(f>0\), the donor inequality \(S(x)\ge fK(\rho x)\) and the exact mean law \(2Y'=-Y+\rho K_s\) give
\[
 r_+(f)=\lambda(\sqrt{4+f^2}-f)/4<\lambda/2,\qquad
 \max(x_+,y_+)\le C_fe^{r_+(f)s}.
\]
This upper comparison accounts for the actual upper mass and gives a ceiling. It does not identify a realized exponent. The passive zero-mass aligned receiver above the coherent resident does attain a two-sided \(\lambda/2\) exponential law after a fixed initial time.

**Exact long-time failure.** A fixed positive upper segment of the specified law contains two distinct finite ranks \(i<j<1\) with a positive initial gap. If the lower input grows at least as \(c_0e^{rs}\) for fixed \(r>0\), the whole segment joining their two receiver states has exponentially large input. The donor-dependent receiver derivative error is bounded by \(C_{ij}e^{8s}\phi(\rho c_0e^{rs})\). Hence both off-diagonal gap coefficients approach \(\lambda/2\), and the diagonal error vanishes. Co-order gives, for any sufficiently small fixed \(\epsilon>0\),
\[
 c_{ij}e^{(\lambda/2-2\epsilon)s}\le x_j-x_i
 \le C_j e^{r_+(1-j)s}.
\]
Choose \(\lambda/2-2\epsilon>r_+(1-j)\). The displayed inequality fails on intervals of unbounded length. This rules out the proposed sustained lower barrier on the time scale proportional to \(\log(1/q)\) for fixed entry parameters and fixed positive upper mass. It does not rule out individual finite-time gate crossings or imply capture. A top atom of a clamped state has a different internal-rank structure.

## Chart and candidate-clock audit

There is no largest \(R_q=o(1/q)\). This is a necessary small-angle condition and by itself proves no field-error control. The unclamped entry already contains \(O(R_q^{-3})\) mass beyond \(R_q\), so an edge clock must specify the starting ranks.

For \(\log R_q=\beta\ell+o(\ell)\), \(\ell=\log(1/q)\), a **two-sided** rate \(r\) would yield a clock coefficient \(\beta/r\). A lower rate alone bounds the hitting time from above only while its barrier persists. The proved upper rate bounds it from below by \((\log R_q-O_f(1))/r_+(f)\).

The candidate seed \(N_0\asymp S_0^{1-\lambda}=c^{1-\lambda}q^2\) gives a candidate logistic delay \((2/\lambda)\ell+O(1)\). At a near-edge radius with \(\beta=1\), every fixed positive upper-mass rank has a strictly later earliest coefficient in the continued \(N=0\) system. The isolated ceiling gives the same coefficient as the candidate clock; a matching time is proved only for the stated passive coherent-field example. At general \(\beta\), the no-earlier condition is \(f\ge(1-\beta^2)/\beta\), if feasible. Below that cutoff the ceiling does not determine before/during/after. No positive-fraction long-time lower rate was substituted for a two-sided clock.

## S7c/S8 handoff

Needed quantities are a controlled outer angular system for order-one angles, matching of the appropriate ranks and their weights across the inner/outer boundary, the actual weak seed and its clock, weak coupling and producer feedback, and the resulting exposure, compensation, exact signed lag and rate contributions. The leading gate threshold and zero-weak-mass ceilings do not supply an original-flow transfer or the weak passage.

Read-only provenance: roadmap v1.33 (4a2d4d52b57321280e7f119a09931d5948a8bf53), RPS (64d1bfa247207a13c4e52f6e3e91ca3fcd4b5f2e), CFS (019410693b5363d80343b5a5e25f246d222b7165), P and WIT. Prefix **an04goev1:** was checked against the repository.

The TeX compiles with resolved references. Both required patterns returned zero matches under PCRE2 and an independent scan (system grep lacks -P). All four required TeX commands survived. The two archive members were checked against the raw sources.
