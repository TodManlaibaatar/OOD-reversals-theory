# E5 projected cross dissipation

**Decision.** The actual critical trajectory has not been proved to satisfy the dissipation comparison through half response. No violation or residual exit has been proved either. This increment removes the strong-response adjustment from the unresolved part of the argument and identifies the remaining signed correlation, including the obstruction to transporting its covariance bound.

## New closed subset

Work on the reached interval from the initialized small response hit to the first half-response or residual-boundary event. This interval has length at most logarithmic in inverse noise, by TBW/RQT. It is not assumed to end at half response.

Let $P$ be orthogonal projection away from $g_m=\nabla m$, the strong-response gradient. This projection is well defined everywhere on the stopped interval: the residual cap gives $m>1/2$, and homogeneity proves $\|g_m\|^2\ge2m^2/S>0$.

With $g=\nabla n$, define

\[
V_0=Q_1zP\nabla z+QhP\nabla h,\qquad
\mathcal C_\perp=\langle Pg,V_0\rangle,\qquad
\mathcal D_\perp=\|V_0\|^2.
\]

Completing the strong-response square gives the exact identity

\[
\mathcal R'=Q(1-n)\mathcal C_\perp-\mathcal D_\perp-\beta^2+\mathcal E_q.
\]

$\beta$ is the explicitly defined strong-response component after square completion. Its square is nonnegative. All approximation errors are written with their signs in `an04pcdv1:main`, and

\[
\int|\mathcal E_q|dt
\le C_c\{q(1+\log(1/q))^3+q^2(1+\log(1/q))^4\}\to0.
\]

The source correlation agrees with the previous two terms to paid precision:

\[
\mathcal C_\perp=Q_1zC_{12}+QhT_2+O(qS(1+S)).
\]

Thus the exact unresolved upper-face comparison is

\[
Q(1-n)\mathcal C_\perp
\le\mathcal D_\perp+\beta^2-\mathcal E_q.
\]

The unpaid correlation is **the weak-target gradient with the cross-output correction after removing the strong-response direction**. The new calculation accounts for the strong-response mixed dissipation without assuming its sign or replacing a squared sum by a sum of squares.

## First approach: joint Gram comparison

The projected cross-gradient Gram matrix is a Schur complement. Writing $p=(Q_1z,Qh)$, $A=\|g_m\|^2$, $T_1=\langle g_m,\nabla z\rangle$, and $B_m=\langle g_m,\nabla h\rangle$, its quadratic form contains

\[
-\frac{(p_zT_1+p_hB_m)^2}{A}.
\]

This subtraction is essential. The original cross gradients are nearly orthogonal, but the projected ones have the mixed entry $-T_1B_m/A$ in addition to the small original entry. In particular, paying each source against its unprojected diagonal dissipation is unjustified.

The sharp joint Cauchy-Schwarz bound is $|\mathcal C_\perp|\le\sqrt{\mathcal D_\perp\kappa}$, where $\kappa$ is the squared norm of the weak-target gradient projected onto the two projected cross gradients. The resulting upper bound $Q^2(1-n)^2\kappa/4$ can be positive. Neither the small residual nor the proved small-hit entrance supplies the additional magnitude or signed-angle comparison. This is a failure to close the estimate, not a counterexample to the critical path.

Singular Gram matrices are included. The source vector lies in the Gram matrix's range, so the Moore-Penrose formula is a pointwise projection identity; no inverse is differentiated and no unproved lower eigenvalue bound is used.

## Second approach: covariance transport

The overlap moment has an a.e. transport formula with all current gates retained. It contains the source

\[
Q(1-n)\int_{\{U_1>0,U_2>0\}}\theta_2(U)U_1W_2\,dl.
\]

This overlap-restricted covariance is not the total measured cross regression $z$. Small total $z$ does not exclude signed cancellation with other labels. No fixed ancestry is substituted for the current overlap set.

The weak output moment has an additional exact gate-motion term:

\[
T_2'=\int(W_1'W_2+W_1W_2')|v_2|^2dl+\mathfrak G_2,
\]

\[
\mathfrak G_2=2\int\gamma_q(U)W_1W_2
(v_2\cdot t_U)(U'\cdot t_U)\,dl.
\]

Here $t_U$ is the unit tangent to the input direction. The Gaussian curvature coefficient is calculated exactly:

\[
\gamma_q(U)=\frac{\rho t_{U,2}^2(\lambda t_{U,2}^2+3q^2)}{Qq|U|}
\phi(\rho a_{U,2}/q)\ge0.
\]

Its positivity does not fix the sign of the product of output weights, tangent feature, and tangent input velocity. The available bound is

\[
|\mathfrak G_2|\le\frac Cq\int|W_1W_2|\phi(\rho a_{U,2}/q)dl\le CS/q.
\]

That estimate cannot pay the budget on the logarithmic interval. A sufficiently sharp signed estimate for this moving-gate correlation is missing. Initial alignment and fixed-resident-time limits do not supply it at the moving small-response hit. This identifies a concrete gap in the covariance-transport route; it does not establish that the gate term actually causes an exit, nor that it is the only possible obstruction.

## Face, mass, and quantifier checks

- The initialized entry satisfies $\mathcal R(\tau_0)\le r_*^2/16$ with $r_*=\lambda/800$. The upper residual face is the only invariant-boundary test requested. Its sign remains open.
- Half response is a stopping target. A simultaneous half-response and residual event has reached the target; no invariant half-response face is claimed. The nonnegative lower residual boundary follows algebraically from regression. No response monotonicity is used.
- The projection denominator is bounded below by homogeneity and the actual strong-response lower bound on the stopped interval. All label norms and moments retain their mass factors.
- The overlap product vanishes on both input-coordinate faces. Its a.e. positive-part chain rule includes entries and corners without a missing flux. This is not a claim that a quadrant is invariant.
- The derivative of the Gaussian gate is retained in full when differentiating $T_2$. Conditioning on the gate gives a one-dimensional Gaussian third moment, not a numerical certificate or an invalid integration by parts. The exact formula holds on the weak-gate direction as well.
- Every input vector remains nonzero at finite times by positive initial radii, balance, and bounded receiver matrices. The derivative of $v_2$ has a factor $1/|U|$, canceled by the bound on $|U'|$ for fixed $q$. The resulting label integral is controlled by $CS/q$, so differentiating the moment does not assume a uniform positive radius.
- The error integrals use the global physical mass bound and RQT's proved stopping horizon. They do not extrapolate a fixed-$s$ limiting theorem.
- The constants and small-noise threshold may depend on fixed $c>0$, $\rho$, and prior entry choices. No uniform statement as $c$ tends to zero or infinity is made. The residual cap itself remains $r_*^2=\lambda^2/640000$.
- No COD constant is claimed at $s=t_\eta-t_h$. No statement is uniform up to an unreached weak clock, and no learned probe-depth comparison is concluded.

## What would constitute an exit, and what remains open

If the residual face is reached first, then

\[
\int_{\tau_0}^{\tau}\bigl[Q(1-n)\mathcal C_\perp-\mathcal D_\perp\bigr]dt
\ge15r_*^2/16+\int_{\tau_0}^{\tau}\beta^2dt-o(1).
\]

This is a necessary integrated payment for an exit. A residual can grow inside its cap without violating the barrier; monotone residual decrease on the entire interval is a stronger requirement than the upper-face test. Neither requirement has been proved here. No specific original source is declared the cause of an exit that has not been established.

The two attempted closures are now stopped. The proved subset is the dissipation-preserving projection, its integrated error estimate, and the exact covariance transport formulas. Half response and E5 remain open. Even closing this training-residual barrier would leave the scaled probe's signed motion to be controlled. MPB's mean-output mechanism continues to explain how the core output can be lowered, but does not by itself control these training-residual correlations.

The sources used are REC's exact finite-noise regression and feature estimates, RQT's initialized stopping theorem, TBW's reached small hit, and BRW's global physical mass identity. No deep-family continuation theorem is transferred across entrances. Prior increments, synced sources, foundations, checkpoints, and GitHub are unchanged. No simulations, fitted rates, empirical values, or computer-assisted inequalities are used as premises.

**Artifact checks.** The TeX escape scans pass. All seventeen labels are unique and every internal and review reference resolves. The second compilation has no warnings or overfull boxes. All five rendered pages were inspected. The archive contains the PDF, TeX source, and this review, with archive integrity and byte-for-byte contents checked.
