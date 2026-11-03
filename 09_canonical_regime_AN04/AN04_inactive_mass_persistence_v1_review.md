# S7c review — inactive mass, bottom ranks and the weak gate

**Scope.** The resident results use the normalized, unclamped critical right-half law with \(M=1,N=0\) in the defined leading system. The weak gate is an instantaneous calculation at prescribed strong and weak measures. The candidate time scale is used only to evaluate a bound from the resident system.

| Task | Status | Result and range |
|---|---|---|
| Inactive mass | Closed on the requested logarithmic horizon with an inverse-logarithmic lower bound | For every fixed \(b>0,\zeta>a_\rho\), a fixed ancestry set of mass at least \(C_*/(1+T)\) stays inactive for every \(s\in[0,T]\). The ancestry set can depend on \(T\). |
| Uniform fraction | Open | No time-independent positive lower bound is obtained. The diagonal face of the proposed wedge points out at entry for every scale. The second-route contact inequality is displayed below. |
| Return | Partial, parameter resolved | Above GOE's initial threshold \(b_c\), a positive initially inactive band returns inside at short time. Below it the local crossing goes outward. The equality case needs higher-order information. All initially inactive mass cannot have returned by any finite horizon. |
| Bottom ranks | Closed initially for all scales and through zero for an explicit large-scale range | The Q4 atom moves down in both coordinates for every \(b>0\), as does a neighboring Q1 band. An explicit mean threshold forces the atom to cross \(x=0\) by a fixed time. Long-time bottom behavior otherwise remains open. |
| Weak field | Closed | Exact coupled entry threshold and a forced per-rank comparison on its stated mass range. Positivity of the weak increment is distinguished from the total gate sign. |
| Handoff | Partial terminal information | Co-order, the atom's rank weight and the horizon-dependent surviving set are supplied. A matched terminal state with a nonvanishing inactive fraction and a proved weak switch is still needed. |

## Persistence on the resident scale

The entry inactive fraction is \(\frac12[1-F_b(H(\zeta))]\) of the whole normalized right half. The proof follows *the same labels* through the interval, so it also bounds the instantaneous inactive mass at every intermediate time.

The refinement of GOE is to retain its upper-mass dependence before integrating over ranks. For a rank with upper fraction \(f\), the per-rank growth ceiling is \(Lw_f\), where \(L=\lambda/2\), \(w_f=(\sqrt{4+f^2}-f)/2\). Its positive eigenvector comparison gives a uniform prefactor times \(1+\xi(f)\), the initial quantile plus one. Using \(\xi(f)\lesssim1+f^{-1/3}\) and \(Lw_f\le L-\lambda f/8\) gives
\[
 \max(\rho K_s,Y)<B e^{Ls}(1+s)^{-2/3}.
\]
All donors, including the protected upper mass, are charged in this estimate. The sign of \(Y\) used in GOE follows from its exact resident mean equation and positive entry mean.

For horizon \(T\), take entry radius
\[
 R_T=\zeta+1+3B[(1+T)^{1/3}-1].
\]
On the faces of \(x,y\ge w(s)\), the kernel and signed-mean costs are strictly covered by the derivative of
\[
 w(s)=e^{Ls}\{R_T-3B[(1+s)^{1/3}-1]\}.
\]
It stays above \(\zeta\) throughout. The entry tail above \(R_T\), or just the band \([R_T,2R_T]\), has mass bounded below by \(C_* /(1+T)\). Thus \(T=(2/\lambda)\ell\) gives the explicit lower bound \(C_* /[1+(2/\lambda)\ell]\) on the candidate time scale. The constants may depend on the fixed entry law, ratio and offset. This does not establish that a fixed positive fraction survives as \(q\downarrow0\). Large scaled radii in this proof have only the status of leading-system coordinates.

**Two unpaid fixed-fraction arguments.** In the proposed wedge the diagonal face requires \(\rho S(x)-Y\ge0\) at \(y=x\). At entry \(S\le K_s\) and \(\rho K_s<Y\) for every \(b>0\), since \(x>a\) has positive mass. The weakened orthant closes at the stated horizon cost. Its normalized donor majorant has a divergent time integral. Divergence of the majorant is not proof of divergence of the actual normalized donor integral.

The output-speed alternative sets \(G=\rho K(\rho x)-Y\). At \(G=0\) its inward test requires
\[
 2\lambda\Phi(\rho x)U+Y\ge\rho K_s.
\]
Even if the test held at a rank, the input velocity must be inward toward \(x\ge\zeta\) on its gate face. Order and the CFS output-gap bound do not pay both tests. GOE's sustained exponential escape obstruction alone gives neither return nor persistence above a fixed gate.

## Lower-rank behavior

For \(m=\mathbb E X_b>a\), the entry input-speed zero is strictly below the entry output-speed zero \(\rho K(\rho x)=m\). At the bottom atom the current equations simplify exactly to
\[
 2x_a'=\lambda\Phi(\rho x_a)(y_a-X_m),\qquad
 2y_a'=\rho K(\rho x_a)-Y .
\]
All donor inputs are above or equal to \(x_a\), which makes the simplification valid even at a plateau. At entry the two doubled velocities are \(-\lambda\Phi(\rho a)(m-a)\) and \(-(m-a)\). The atom thus leaves the resident downward immediately.

One sufficient explicit crossing set uses \(C=100e^7,\ h=1/(4C)\) and
\[
 m>\max\{1,4a,8a/(\lambda h)\}.
\]
The mean \(m\) is the GOE entry integral and grows as \(b/\pi\). The first absolute moment bound gives \(|X_m'|,|Y'|\le Cm\) on the unit interval. Both means stay above \(3m/4\) through \(h\). Both upper faces of the bottom rectangle \(x_a,y_a\le a\) point inward there. While \(x_a\ge0\), \(x_a'\le-\lambda m/8\), so the atom crosses before \(h\) and remains negative at \(h\), as does a positive neighboring Q1 band. This sufficient range makes no prediction of eventual sign for smaller \(b\).

## Weak-coupled gate and ceiling

At an aligned gate with strong law \(M\langle\cdot\rangle_b\),
\[
 2U=\rho K(\rho\zeta)-(1-M)\zeta+
 \lambda(V-N\zeta)\Phi(\rho\zeta)-\rho M S_b(\zeta).
\]
The weak increment is outward iff \(V>N\zeta\). Call the first three terms \(D_{\rm gate}\). For \(D_{\rm gate}\le Ma\), motion is inward for every \(b>0\). For \(D_{\rm gate}>Ma\), there is one positive root \(S_{b_*}=D_{\rm gate}/(\rho M)\), with outward, stationary and inward initial motion below, at and above the root. This comparison varies the strong scale at fixed weak moments. Later gates need the actual receiver output and current donor field.

The doubled output velocity is \(-(1-M)y-Y-K_w+\rho(1-N)K(\rho x)\). The weak overlap functional acts in the weak receiver equations. It is not an extra direct strong-gate term.

For \(M>0,\ 0\le N\le1\), the strong positive-part comparison uses the symmetric matrix with diagonal entries \(-(1-M)-\lambda Mf,\ -(1-M)\) and off-diagonal entries \(\lambda(1-N)\), all divided by two. The largest eigenvalue is
\[
 r=-(1-M)/2+(\lambda/4)[\sqrt{(Mf)^2+4(1-N)^2}-Mf].
\]
The forcing vector is \((\rho\phi(0)+\lambda V_+,\ \rho(1-N)\phi(0)+(Y+K_w)_-)/2\). A norm comparison integrates this forcing against \(\exp(\int r)\); one cannot treat the homogeneous eigenvalue as the growth rate with unbudgeted forcing. The sign-safe input bound uses \(V_+\). The output negative-part charge is needed because \(2Y'=(1-2M)Y-MK_w+\rho(1-N)K_s\). The off-diagonal sign used for order and the positive-part proof requires \(N\le1\).

## S7d and trained-flow handoff

At the end of the specified finite resident horizon the mass remains co-ordered, with the Q4 atom retaining half the normalized rank weight. A guaranteed initially inactive subcohort survives with the stated mass. Its terminal law, fixed-order inactive fraction, terminal exposure, exact lag and true weak-entry time are not yet determined.

S7d needs the actual weak seed, moments, clock and field coupling; changes in the active gate, strong and weak weights; and lag-relative, rate-weighted producer estimates. Trained-flow transfer additionally requires the actual critical strong-entry clock and profiles, precision on the noise-scaled angles or equivalent weighted observables, the other-sector and tail charges, and outer matching where physical angles become order one.

Read-only provenance: roadmap v1.34 (3bc6ccc9b3eeccf00141d0e3983a0f63d6a9a8f6), GOE (ea0dd2f0950dbb8bbfda4c6492287f87c22313b8), RPS, CFS, WIT and P. The new prefix is **an04impv1:**.

Standalone TeX compilation and reference checks passed. Both requested patterns gave zero matches with PCRE2 and an independent scan; the local grep lacks -P. The four required literal TeX commands survived. Both ZIP members were checked against the raw sources.
