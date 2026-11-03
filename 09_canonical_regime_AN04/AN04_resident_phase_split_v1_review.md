# S7a review — the critical right-half profile and its resident-phase evolution

**Result.** The positive-noise comparison Q4 population converges to an aligned atom at \(a_\rho\). Together with CFS's distributed Q1 law this completes the comparison state for right-half ancestry. In the \(N=0\) leading system, co-order and the exact moment equations hold for compact entry. A finite-time escape region certifies a positive mass of **new** outward gate crossings on an explicit range of truncated critical profiles. The corresponding unrestricted claim remains open. The exact gate velocity can point inward for other critical profiles.

| Task | Status | Model and range |
|---|---|---|
| 1(a), Q4 | Closed | Positive-noise aligned target-only flow at \(T_A\). Two-sided rate on compact interiors, quantitative shrinking-strip charge and weak mass limit on the closed sector. |
| 1(b), right half | Closed | Positive-noise comparison Q4 plus Q1. Q2 and Q3 excluded. Offsets stay strictly above \(a_\rho\). |
| 2, co-order and cutoff | Closed | Compact, co-ordered \(N=0\) leading state, \(0<M_0\le1\), every finite chart-valid interval. Mass and first-moment costs are charged at the instant of truncation. |
| 3(a), moments | Closed | Exact mass, output and input first moments, \(K_s\) and exposure, including the mass reaction and gate-atom convention. |
| 3(b), growth | Closed on the parameter range below; stopped in general | Both lower faces of a moving orthant are inward through a specified time. Positive mass initially on the active side crosses. Arbitrary entry parameters can violate the exact input-face inequality. |
| 3(c), monotonicity | Direction depends on state | At regular initial gates the active rank decreases for one family and increases for another. A long-time monotonicity claim for an individual trajectory needs an additional sign estimate. |
| 4, handoff | Partial split supplied | The explicit resident-phase state description and escape certificate have finite-time scope. The weak switch and trained entry remain open. |

## Right-half comparison state

Write \(b=(c/A)^\omega\). On a compact interior Q4 angle interval the first hit of \(-qL\) takes \(2\ell+O(1)\). The exact remaining time has leading coefficient \(1/\omega-2\) in \(\ell\). Bounded-chart attraction to the exact root \(a_q=a+O(q^2)\) gives
\[
 a-\widehat\theta(T_A)/q\asymp q^{d(1/\omega-2)},\qquad
 \widehat m(T_A)=A\cos^2\beta\,(1+o(1)).
\]
The sign relative to \(a\) uses the lower displacement bound, since the root shift is smaller. Outside a strip of mass \(O(Aq^{1/4})\), the absolute scaled displacement is \(O(q^{d(1/\omega-5/2)}+q^2)\). The total Q4 mass is \(A/8+O(Aq^{1/4})\). Each endpoint strip of initial length \(\eta\) costs \(O(A\eta)\). No assertion of compact-interior arrival time at the negative vertical endpoint is needed. The full-chart time guard in PROFILE's rightcircle corollary would fail; the proof uses the exact Q4 speed and a fresh travel-time estimate instead.

The right-half limiting measure has mass \(A/4\). Half is the atom at \((a,a)\); half has the CFS density on \(y=x>a\). With \(H\) the CFS quadrature, the active fraction for \(\zeta>a\) is
\[
 \boxed{\frac12+\frac2\pi\int_0^{H(\zeta)/b}\frac{dt}{(1+t^2)^2}}.
\]
The gate uses the current input angle. The mass of the Q1 equality label vanishes, and the Q4 atom is strictly inside the gate. Uniformity is on compact positive ranges of \(A,c\), the ratio box and compact offsets separated above the resident. No full-population denominator is used.

## Co-order, truncation and moments

Normalized radial weights are fixed along rank labels. The two off-diagonal receiver derivatives are \(\lambda\Phi(\rho x)/2>0\) in one common donor field. Pairwise order therefore holds simultaneously across ranks and the strict active set is an initial segment; a plateau at the gate is excluded. This does not imply temporal monotonicity of the cutoff rank.

For a large cutoff \(R>\zeta\), \(h_R=H(R)\), the removed raw comparison mass and each first moment are bounded by \(Ab^3/(6\pi h_R^3)\) and \(Ab^3/(2\pi h_R^2)\), respectively. The two donor functions are charged explicitly by their linear growth and their Lipschitz dependence on the donor input. Clamping at \(R\) preserves mass and the initial active fraction. The escape theorem uses a prescribed compact leading state. The estimates for deletion or clamping are instantaneous and do not transfer trajectories between different fields.

The moment equations include \(2Y'=(1-2M)Y+\rho K_s\). Thus the signed mean receives a forcing from the entire distribution even when \(M=1\). The exposure equation is \(A_\zeta'=(1-M)A_\zeta-\int_{x<\zeta}U\,d\mu\) almost everywhere; the pointwise right derivative also charges \(\int_{x=\zeta}(-U)_+d\mu\). Here \(U=x'\).

## Escape criterion, growth rate and exact obstruction

For a leading state prescribed at time zero put
\[
 g=\rho K(\rho\zeta)-\max\{\rho K_s(0),Y(0)\}-(1-M_0)(\zeta+1).
\]
Theorem 2 (label an04rpsv1:cone) gives its constants explicitly. For \(g>0\), \(k=g/[8(\zeta+1)]\). Through the theorem's time \(h>0\), the upper orthant \(x,y\ge \xi e^{kt}\) is forward-invariant for every initial level \(\xi\in[\zeta-\delta,\zeta]\). The initial active labels in that band cross by \(h/2\) and stay outside through \(h\). For the normalized aligned critical shape, a fraction at least
\[
 \frac4A\int_{\zeta-\delta}^{\zeta} f_b(x)\,dx>0
\]
is certified. These labels are in addition to comparison mass already above the gate. The full chart radius is at most \((1+R_0)e^2\) during the proof. This is an exponential lower barrier over a finite interval, not a universal asymptotic exponent \(\lambda/2\).

For fixed \(R>\zeta\), at \(M_0=1\) a concrete range with \(g>0\) is
\[
 0<b<H(r)\left(\frac{3\pi[\rho K(\rho\zeta)-r]}{2R}\right)^{1/3},
 \qquad r=\frac{a+\rho K(\rho\zeta)}2.
\]
The proof bounds the mass above \(r\) and its contribution after clamping. For any fixed \(b,M_0,R\) the moment test can instead be checked by the explicit entry integrals. Strictness persists for sufficiently close subunit masses.

**Self-consistency.** The proof first bounds \(D=1+\int(|x|+|y|)d\mu\) by \(D_0e^{7t}\), including all escaping mass. The moment identities then bound both donor changes before any escape estimate is used. On the input face the exact positive target kernel is retained; on the output face the signed \(Y(t)\) charge remains. Both velocities exceed the boundary speed, including at the corner.

**Where the unrestricted argument stops.** At an aligned initial gate and \(M=1\), outward speed requires \(S(\zeta)<K(\rho\zeta)\). For large cutoff and then large finite \(b\), half the normalized mass approaches the clamped upper donor. The limit of \(S(\zeta)\) is \([K(\rho a)+\phi(\rho\zeta)+\rho R\Phi(\rho\zeta)]/2\), which can exceed \(K(\rho\zeta)\). Increasing the cutoff at this fixed scale preserves the failure while making the entry tail charge small. No outward constant-speed lower face through this gate can follow from the unrestricted entry assumptions. This is not evidence that the entire population is captured, or that no later crossing occurs.

More generally the sign for nonincrease of the active rank requires
\[
 \rho\phi(\rho\zeta)-\rho S(\zeta)+\lambda y(\sigma_*)\Phi(\rho\zeta)
 \ge(1-M)\zeta.
\]
Each initial sign example uses its own self-consistent donor law. Opposite signs for two entry states do not show that one trajectory reverses its direction in time.

## S7b handoff

The specified objects are the right-half **comparison** state, a compact leading entry and its rank/moment evolution, and a certified inactive band at the finite terminal time \(h\) for the stated range. There is no established universal end-of-resident-phase profile for arbitrary critical scales. S7b needs a matched weak switch, a proved seed and weak distribution (\(N_0\asymp S_0^{1-\lambda}\) is the candidate law), coupled passage and donor feedback, and rate-weighted producer and exact signed-lag precision. For the trained flow one still needs the entry clock, angular or weighted-profile precision at the \(q\) scale, radial weights and other-sector/tail control, and transfer through saturation.

Read-only provenance: roadmap v1.32 (f2655344b60cf9349fdceefdf93aa10e6c11d840), CFS (019410693b5363d80343b5a5e25f246d222b7165), PROFILE, WIT, P and CRA. The TeX inventory identifies model/time/chart domains. The new label prefix is **an04rpsv1:**.

The standalone TeX compiles with resolved references. Both ledger-25 patterns returned zero matches under PCRE2 and an independent scan; the local grep lacks -P. All four literal TeX commands survived. The ZIP members were verified byte for byte against the two sources.
