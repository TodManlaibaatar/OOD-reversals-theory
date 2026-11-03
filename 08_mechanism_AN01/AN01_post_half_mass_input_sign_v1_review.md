# Post-half-mass input sign, version 1

**Result.** S6c closes the rational fallback (4a). For every ratio in \([13/20,7/10]\), the selected orbit satisfies \(X-Y>0\) through the closed endpoint \(s_1=1/1000\) in the weak half-mass clock. CPD transfers strict positivity to the original selected-weak-produced core input rate on the learned subwindow \(J_1=J\cap(-\infty,s_1]\). Coverage of \(J\cap(s_1,\infty)\) remains open.

| Task | Status | Scope and source |
|---|---|---|
| Inventory | Closed | The TeX lists WIT and P bounds by model, time and mass range. WIT regiontheorem and its quantitative lower bound for \(T\) end at \(n=1/2\). WIT uniformtheorem applies only on the learned window. P's forward invariants apply for all finite selected-orbit times. |
| Reviewer crossing reduction | Verified | At \(z=0,\ n\ge1/2\), both signs of \(Y\) give \(2z'>n[K(U)-7/25]-Y_-\). WIT gaussianbounds gives \(\rho\phi(0)<(7/10)(2/5)=7/25\). The \(U=0\) derivative is inward exactly when \(Y<2(1-n)\phi(0)\). |
| Approach A | Partial | The positive half-mass \(T\) margin persists on the new rational interval. The forward growth bound gives a finite radius but insufficient signs in the \(T=0\) boundary derivative for a general later endpoint. |
| Approach B | Stopped | WIT does not supply \(Y(0)\ge0\). The \(Y=0\) face of the proposed nonnegative region can point outward. Keeping the positive \(V-Y\) term leaves the boundary inequality below. |
| Fallback and transfer | Closed | Explicit box, \(T\) and \(z\) margins on \([0,1/1000]\). On a nonempty \(J_1\), compactness and branchsmooth give the positive minimum required by CPD. |
| All-window mechanism sign | Partial | The signed decomposition remains valid on \(J\). The weak-produced input sign is proved on \(J_1\). Neither window placement nor positivity on the remainder has been established. |

## Quantitative proof audit

On \([-1,0]\), \(n>1/4\), \(1-n\ge1/2\), and WIT gives \(T\ge(5/62)n(1-n)\). Consequently \(z'+z/4\ge5/992\). The integrating factor gives \(z(0)\ge15/3968\). At half mass \(T(0)\ge5/248\). Both margins are independent of the probe and of the location of \(J\).

The radius \(R=\max(|X|,|Y|,|U|,|V|)\) starts at most \(11/10\). In the box \(R\le2\), the four speed bounds give \(R(s)\le11/10+4s\) up to first exit. This strictly improves the box through \(s_1\). The same box gives \(|T'|<12\), hence
\[
 T(s)\ge5/248-12/1000>0,\qquad
 z(s)\ge(15/3968)e^{-s/4}.
\]
The order of the estimates is radius, then \(T\), then \(z\). The proof does not import any probe margin into the interval before \(\inf J\).

## Exact remaining inequality

At a hypothetical first zero \(X=Y\), the unproved inward condition is
\[
 \lambda n\Phi(\rho Y)(V-Y)+Y+nK(U)>(1-n)\rho K(\rho Y).
\]
Approach A tests \(T'\) instead. Its unpaid term is \(-\lambda(1-n)\Phi(\rho X)X'\). The positive partial derivative \(\partial_nT=K(U)+\rho K(\rho X)\) holds at a fixed state. It cannot control that velocity term along the orbit. The TeX displays the exact inward test and the nonpositive lower estimate from the available forward radius bounds.

For approach B the TeX tests \(X=Y=-1/5,\ U=0,\ V=1/20,\ n=9/16\). Even with \(V>0,\ V>X,\ V>Y,\ U\ge0,\ Y>-n\) and positive leading lag, the inward condition fails at that state by strict rational inequalities. This establishes the insufficiency of those pointwise state bounds. Reachability of the test state is not asserted. The sign on the remaining time range is unresolved.

## B-core scope and corrected Theorem B item 3

On \(\mathcal P_*\times J\), the original \(S_0=q^{10}\) flow retains CPD's positive exact lag, help equal to exposure times that lag with a smaller remainder, and its rate-weighted producer decomposition with normalized error \(O(q^{1/20})\).

**Corrected item 3.** Cluster 2 rotates both the inputs and outputs of the strong probe-active carrier. The target-plus-core input term is \(-\lambda (X-Y)^2\Phi(\rho X)/2\). The selected weak producer supplies \(\lambda n(X-Y)(V-Y)\Phi(\rho X)/2\) through its two outputs. Target output rotation contributes \(T_{\rm out}>0\), and the weak response contributes \(-nT_{\rm out}\), leaving positive net output rotation. The weak-produced input term is strictly positive on \(J_1\) for the original dynamics at small q. The positive net output term carries the limiting \(d_2>0\) on any subwindow of \(J\) with \(X-Y\le0\), since both input terms there are nonpositive. This last implication requires no assertion that such a subwindow occurs.

Keep CPD's constants, rectangle and common clock first. For nonempty \(J_1\), use \(m_1=\min_{K_\rho\times J_1}W_{\rm in}>0\) and choose \(q\) last with \(Cq^{1/20}<m_1/2\). The exact normalized-time producer rate is at least \(q^2m_1/2\). Physical time rates carry an additional \(\mu_1^2\).

## S7/S8 handoff

The result concerns the initialized deep family on the stated learned subwindow. Canonical and bridge regimes require original-flow matching on their own state class and producer errors smaller than their signed exact lag cancellation. The rational interval is a guaranteed sign interval, not a measurement of crossover timing.

## Provenance and source checks

Read-only repository versions used were roadmap v1.29 (b843cb4f63057bae62da687df7b3104a7c91d41a), CPD (8ebf36f3deaffc664a76c8c5b34e796051f6c368), WIT (9e102514ad0a491066a2f9eb8eb86e9a251c2b53), and P (cb458c933aa043cf0188fd11c46bf4246ffc91d8). Repository search returned no existing an01phsv1: label. Only the new source pair is packaged. All estimates are analytic.

The standalone TeX compiles with resolved references. Both requested patterns returned zero matches in PCRE2 and an independent text scan. The local grep lacks -P. The four requested TeX command strings survived. Archive members were verified against both raw sources.
