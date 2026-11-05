# E5 residual-budget barrier: review

**Result.** The barrier through half response is not closed. There is also no proof that the actual critical trajectory exits it. The new result identifies two explicit signed exchange channels and proves that all omitted exchange has vanishing accumulated size on the actual stopped logarithmic interval. This sharpens the failure of the proof without claiming a failure of the trajectory.

## What is new

Use four exact regressions: strong response $m$, weak response $n$, strong-cluster second output $z$, and weak-cluster first output $h$. Let $Q_1=1+q^2$ and $Q=\lambda+q^2$. The complementary residual decomposes exactly as

\[
\mathcal R=Q_1[(1-m)^2+z^2]+Qh^2+\chi,
\qquad 0\le\chi\le Cq^2(1+S)^2.
\]

The bound on the within-cluster shape residual follows from the global $S$-Lipschitz bound for the network and orthogonal projection. It does not require small angles, gate separation, or a finite-time resident approximation. The estimate includes the target's transverse Gaussian fluctuations.

On RQT's actual stopped interval from the reached small hit to the first half-response or residual-boundary event, the exact exchange is

\[
\Gamma=-\frac12\left(Q_1zC_{12}+QhT_2\right)+\varepsilon_q,
\]

where

\[
C_{12}=\int(U_1)_+(U_2)_+\,dl\ge0,
\qquad
T_2=\int W_1W_2\left|\frac{\mathbb E_{P_2}[D_2D\mathbf1_{U^TD>0}]}{Q}\right|^2dl.
\]

$T_2$ is signed. Both moments use the entire current population, with its physical weights. The error is defined explicitly in `an04recv1:gamma`, not just named. Its pointwise size is at most $CqS(1+S)$. RQT's stopping bound and BRW's global mass bound give

\[
\int_{\tau_0}^{\tau}|\varepsilon_q|\,dt
\le C_cq(1+\log(1/q))^3\longrightarrow0.
\]

This is a new finite-noise estimate on a moving stopped interval. It does not extend a fixed-$s$ theorem to the weak clock, and it does not supply scaled probe precision.

## Exact missing inequality

At $\mathcal R=r_*^2$, with $r_*=\lambda/800$ and $n<1/2$, the required face condition is equivalently

\[
Q_1zC_{12}+QhT_2
\le \frac{4\|N\|^2}{Q(1-n)}+2\varepsilon_q.
\]

The dissipation on the right is the norm of the full update after removing the weak response mode. Its squared norm includes mixed terms between the strong longitudinal, strong transverse, weak transverse, and shape gradients. Dropping those mixed terms is not a lower bound. No proved comparison on the critical trajectory pays this inequality.

The first adverse channel is a positive strong-cluster second output $z$ coupled to shared positive input activation $C_{12}$. The second is the signed product of the weak-cluster first output $h$ with the gate-weighted output product $T_2$. Either sign of $h$ can be adverse if $T_2$ has the same sign. Neither a mass bound nor a magnitude bound chooses this sign.

## What an actual exit would imply

If the residual boundary is reached first, `an04recv1:exit` proves

\[
\int_{\tau_0}^{\tau}Q(1-n)(Q_1zC_{12}+QhT_2)\,dt
\ge \frac{15r_*^2}{16}+4\int_{\tau_0}^{\tau}\|N\|^2dt-o(1).
\]

For small enough $q$, at least one of the two signed channel integrals exceeds $7r_*^2/16$. Thus a fixed-size exit requires these cross-output channels to overcome the dissipation. Within-cluster shape fluctuations and the small strong-longitudinal mixed coupling cannot alone account for it.

This is a necessary condition for an exit, not evidence that it occurs. The analysis does not choose which channel would pay the exit. A first boundary hit can be tangential, so a strictly positive outward derivative is not asserted at the first hit.

## Inequality and face audit

- **Entry.** TBW/RQT supply the actual small hit with $\mathcal R(\tau_0)\le r_*^2/16$, strictly inside the cap. No new entry law is substituted.
- **Upper face.** The denominator $Q(1-n)$ is positive on the stopped region. The displayed face condition is exact, including the signed approximation error. A uniform strict margin or a scalar comparison near the face remains needed for a no-exit proof.
- **Half-response boundary and corner.** This is a target stopping boundary, not a face claimed invariant. A simultaneous residual and half-response hit has already reached the response target.
- **Lower residual boundary.** $\mathcal R\ge0$ is an algebraic projection identity. No additional lower-face assumption is made. No lower response barrier or response monotonicity is used.
- **Shape bound.** Compare to $r(\mu e_p)D_p/\mu$ and then minimize over the regression coefficient. This includes both output components. Only Gaussian second moments and the full mass $S$ are used.
- **Feature gradients.** The parameter derivative has both input- and output-layer blocks. The bound $\|J_D^Tv\|^2\le2S|D|^2|v|^2$ retains both. The data Cauchy-Schwarz estimate is applied to the operator norm before integration, so no unproved fourth-moment residual bound is used.
- **Gaussian gates.** For $v_p$, the component along $e_p$ lies in $[0,1]$; its other component is bounded by $Cq$. This holds for any input direction, including entry through a gate. No derivative of a selector and no invalid integration by parts is used.
- **Gram entries.** Strong-to-weak mixed-output coupling is $O(qS)$ because the two center directions are orthogonal. Same-output coupling equals $C_{12}+O(qS)$. The weak mixed-output entry is exactly $T_2$. Positivity of a Gram matrix does not sign its mixed entries.
- **Mass and time.** $S\le C(1+t-t_h)$ and $\tau-t_h\le C_c(1+\log(1/q))$ imply the integrated $O(q\log^3(1/q))$ bound. There is no outlier-rate premise.
- **Constants.** $r_*^2=\lambda^2/640000$ is independent of $c$. Entry choices, the stopping-time constant, and the required small-noise threshold can depend on every fixed $c>0$. No uniform conclusion as $c$ tends to zero or infinity is claimed.

## Two approaches and the stop rule

1. The angle-free Cauchy-Schwarz estimate requires $\|N\|\ge Q(1-n)\|g\|/2$ when $N\ne0$ to pay the face. A small residual supplies no such lower bound. Completing the square leaves the same unsigned comparison.
2. Orthogonal regression removes ordinary data correlations but not the selected gradient correlations. The new reduction pays their errors and isolates the two terms above. Their comparison to exact dissipation is still unpaid.

The item stops after these two approaches. There is no conditional theorem advertised as a closure of E5, and no counterexample with a substituted initialization is used to infer behavior of the critical trajectory.

## Source and scope audit

The model and gradient identities match P's original balanced Gaussian flow. BRW supplies only its global physical mass identity here. TBW supplies the reached small response, and RQT supplies the initialized residual-or-half stopping theorem. No deep-regime FWC entrance contract is assumed for the critical family. The current remote roadmap was checked read-only at version 1.40, file SHA `9940cda848e54482441aac8b2014b7d0b6336323`, including ledger items 15-43. Its empirical orientation is not used as a premise.

No COD constant is claimed at $s=t_\eta-t_h$. No learned-time scaled probe limit, half-response passage, or comparison with the coherent swing-by minimum is proved. MPB's mean-output mechanism lowers the core output; controlling the resulting cross-output exchange while weak learning proceeds is a separate requirement. The probe's perpendicular forcing would remain to be controlled even after this residual barrier closes.

All prior increments, foundations, checkpoints, synced files, and remote files remain unchanged. The proof is analytic. Compilation and document checks do not supply mathematical premises.

**Artifact validation.** Both TeX escape scans pass. All eleven labels are unique, internal references and review references resolve, and the second compilation has no warnings or overfull boxes. All four rendered pages were inspected for clipping and mathematical layout. The ZIP contains the PDF, TeX source, and this review.
