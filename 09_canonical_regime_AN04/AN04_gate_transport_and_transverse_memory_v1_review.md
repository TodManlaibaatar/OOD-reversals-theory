# E5 gate transport and transverse error

**Result.** The projected dissipation inequality remains unproved on the actual critical trajectory through half response. This note proves two controls, identifies why they do not close the barrier, and gives an exact equation for the remaining weak cross-output amplification. It neither proves nor predicts an exit of the initialized trajectory.

## Signed gate transport is improved

The exact identity $T_2'=A_2+\mathfrak G_2$ gives, for an absolutely continuous time weight $\chi$,

\[
\int_a^b\chi\mathfrak G_2
=[\chi T_2]_a^b-\int_a^b\chi'T_2-\int_a^b\chi A_2.
\]

The endpoint terms and both integrals are retained. The global physical mass and loss-dissipation bounds prove, on every subinterval of the reached stopping interval,

\[
\left|\int\mathfrak G_2\right|\le C_c(1+\ell),\qquad
\left|\int wh\mathfrak G_2\right|\le C_c(1+\ell)^2,
\quad \ell=\log(1/q).
\]

This removes the inverse-noise loss of the previous pointwise bound. It does not bound the integral of the absolute value or the positive part, does not tend to zero, and does not supply a pointwise barrier sign. The integration by parts is in time, with the exact Gaussian gate derivative already included. No derivative of a data selector is silently dropped.

## Overlap and output covariances share a controlling energy

Define

\[
\Delta=\frac12\int\left((U_2)_-^2+[W_2-(U_2)_+]^2\right)dl\ge0.
\]

This is a current-state physical energy, including all populations. It is not a zero-noise trajectory or an ancestry-restricted moment. The actual finite-noise estimates are

\[
|C_{12}-z|+|T_2-h|+|O_{12}-z|
\le C\sqrt{S\Delta}+CqS,
\]

where $O_{12}$ is the overlap-restricted covariance that regenerates $C_{12}$. The proof retains the mass factors and works at every input gate, including entry. Gaussian smoothing is paid by the uniform bounds on $b_p,v_p,\theta_p$ and boundedness of $t_+\Phi(-t)$.

The exact second-component energy obeys

\[
E_2'=Q(1-n)n-\frac12(Q_1z^2+Qh^2)+\epsilon_E,
\qquad |\epsilon_E|\le C[qS+q^2(1+S)^2].
\]

Consequently, uniformly up to the stopping event,

\[
\Delta(T)=\Delta(\tau_0)+\int_{\tau_0}^TQ(1-n)n
-[n(T)-\eta_0]-\frac12\int_{\tau_0}^T(Q_1z^2+Qh^2)+o(1).
\]

The integral of the error is bounded by $C_c[q(1+\ell)^2+q^2(1+\ell)^3]$. The positive logistic-energy integral is retained. Identifying it with the response increase would assume a clock match that has not been proved. The moving entrance value $\Delta(\tau_0)$ is also not controlled by the small residual cap. Thus these estimates do not prove that the covariance defects are small throughout the interval.

## Why controlling gate motion and overlap would still be insufficient by itself

The note includes an exact algebraic audit in the auxiliary zero-noise two-center model. It is **not** the critical initialization and is **not** a counterexample to the requested actual-trajectory theorem.

There are balanced states on the residual boundary with strict, locally fixed gates, zero overlap, $m=1$, $z=0$, $n=1/4$, $h=-ab$, and $T_2=h$. Their gate-motion term is zero, all three covariance defects are zero, and $\Delta$ can be arbitrarily small. Yet

\[
\mathcal R'=\lambda^2h^2(1-2n-a^2)>0,
\qquad a^2=\lambda/160000.
\]

For those states, dissipation dominance would require the false inequality $a^2+2n\ge1$. The normalization is explicit: two effective rank-one contributions are realized by probability label weights $1/2$ and vector scaling by $\sqrt2$. No mass factor or time factor is lost.

This audit refutes only the generic implication from balance, small covariance defects, frozen gates, and small residual to the projected sign. It shows that a weak transverse error can amplify below half response even when gate motion is absent. The actual critical trajectory may have much smaller inherited tilt or favorable signed forcing; neither has been bounded sufficiently here. No auxiliary entrance or zero-noise theorem is applied to that trajectory.

## Exact remaining bound on the actual trajectory

Using PCD's projection away from $\nabla m$, the actual cross-output regression satisfies

\[
h'=a_hh+F_h,\qquad
a_h=\frac Q2(1-n-H_{hh}),
\]

\[
F_h=\frac{B_m}{A}m'-\frac{Q_1z}{2}H_{hz}
+\frac{Q(1-n)}2(k_h-h)+\langle Pg_h,PN_{\rm sh}\rangle.
\]

Every signed term is retained. The first comes from strong-response adjustment, the second from the projected cross-gradient correlation, the third from the weak covariance defect, and the fourth from within-cluster shape residuals. The denominator $A=\|\nabla m\|^2$ stays positive by the actual residual cap and homogeneity.

With $J(T)=\int_{\tau_0}^Ta_h$, variation of constants gives

\[
h(T)=e^{J(T)}\left[h(\tau_0)+\int_{\tau_0}^Te^{-J(t)}F_h(t)dt\right].
\]

The cap implies the necessary inequality

\[
\left|h(\tau_0)+\int_{\tau_0}^Te^{-J(t)}F_h(t)dt\right|
\le\frac{r_*}{\sqrt Q}e^{-J(T)}.
\]

On an already stopped interval this follows from the cap and cannot be used circularly to continue it. What is missing is an independent strict budget for this signed expression. One concrete sufficient component allocation would replace $r_*$ by $r_*/2$, giving $Qh^2\le r_*^2/4$ while the initialized value uses at most $r_*^2/16$. This allocation is not claimed necessary and does not by itself control the remaining residual components. Neither the integrated forcing estimate nor a suitable bound on the amplification $J$ has been proved.

The exact aggregate upper-face inequality is still

\[
Q(1-n)\mathcal C_\perp\le\mathcal D_\perp+\beta^2-\mathcal E_q.
\]

The new estimates do not establish it. No assertion is made that the actual path violates it. The two approaches, signed gate integration and covariance-energy control, stop here.

## Checks and scope

- **Entry and faces.** The actual residual entry is strict. Its upper-face sign is unresolved. Half response is a stopping target; a simultaneous event reaches that response. Nonnegativity of $\Delta$ is algebraic, covers both signs of $W_2$, and includes $U_2=0$. No quadrant invariance is assumed.
- **No hidden absolute-value inference.** Signed gate integral bounds do not control repeated positive gate flux. Bounds on covariance magnitudes do not determine their signs. The logistic-energy term and all four terms of $F_h$ remain present.
- **Energy calculation.** The exact formula for $E_2'$ uses both layers and both mixture halves. Euler's identity is applied a.e. to the positively homogeneous network. The Gaussian derivative terms are bounded using the global Lipschitz constant $S$ and the decreasing loss. The within-cluster shape residuals use their proved $L^2$ bound.
- **Initialized scope.** All moving-interval estimates are on TBW/RQT's reached stopping interval. BRW supplies the global mass bound. REC and PCD supply exact finite-noise quantities. No full weak-clock or half-response arrival is presumed.
- **Dependence on $c$.** Constants, entry choices, and small-noise thresholds may depend on every fixed $c>0$. The cap remains $r_*^2=\lambda^2/640000$. No uniform conclusion as $c\to0$ or $c\to\infty$ is claimed.
- **Resident limits.** No COD constant is claimed at $s=t_\eta-t_h$. Fixed-time bounds are not substituted at the moving small hit. The auxiliary state audit is isolated from all initialized conclusions.
- **E5.** Half response and the learned probe minimum below the coherent comparator remain open. MPB's core-output mechanism does not itself supply the amplified weak-transverse forcing budget. Closing the residual barrier would still leave signed probe motion to control.
- **Ground rules.** Prior increments, synced sources, foundations, checkpoints, and GitHub remain unchanged. The mathematics is analytic; no empirical data, trajectory integration, fitted exponent, or numerical inequality is a premise.

**Artifact validation.** The TeX escape scans pass, all fourteen labels are unique, and all references resolve. The final compilation has no warnings or overfull boxes. All five rendered pages were inspected, including the changed pages after the final wording audit. The ZIP contains the PDF, source, and review, with archive integrity and byte-for-byte contents checked.
