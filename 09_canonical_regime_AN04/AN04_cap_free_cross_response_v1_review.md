# E5 cap-free cross-response estimate

**Decision.** The desired small bound for $h$ through half response remains open. The homogeneous entrance term and the finite-noise error are now controlled independently of a residual cap. The exact remaining term is a signed weak-target forcing convolution along the actual trajectory. No claim is made that this term is large or that the trajectory exits the proposed cap.

## The interval is no longer residual-stopped

Start at the reached fixed-delay time $t_b=t_h+b$. For any fixed $K>0$, work until the earlier of the first half-response hit and $t_b+K\log(1/q)$. There is no stop when $h$, the complementary residual, or an angular chart leaves a proposed region. The half-response hit is allowed to be infinite. The earlier residual-stopped hitting theorem is not used to infer a cap-free hitting time.

Global loss and mass bounds suffice on this interval. They imply bounded regressions and $S(t_b+s)\le C_b+Cs$. With $b$ fixed and sufficiently large, they also prove

\[
\mathcal R\le31/80,\qquad m\ge1-\sqrt{31/80}>1/3
\]

before half response. This is a derived order-one estimate. It is much weaker than the small cap $r_*^2=\lambda^2/640000$ and is not being substituted for it. The argument allows negative or nonmonotone weak response.

## First approach: exact scalar damping

The unprojected exact flow gives

\[
h'+\frac Q2\|\nabla h\|^2h
=\frac12\{Q(1-n)T_2+Q_1(1-m)C_{12}\}+\varepsilon_h.
\]

The error is written explicitly in the proof. Its integral over the deterministic logarithmic horizon is at most $C_{b,K,c}q(1+\log(1/q))^3$. The scalar homogeneous propagator lies in $(0,1]$. Thus the fixed-delay entrance $h(t_b)=O_b(q)$ contributes only $O_b(q)$ throughout this interval. At literal initialization, isotropy gives $f_0(D)=S_0D/4$ and $h(0)=0$ exactly.

This does not disprove the amplification seen in the previous representation. Splitting $T_2=h+(T_2-h)$ had placed a self-consistent piece in a possibly positive coefficient. The current formula keeps that piece inside the forcing. Physical feedback can still grow the cross output. The new result controls the homogeneous term in this exact representation, not the sensitivity of the nonlinear trajectory to changes of initialization.

The scalar route leaves both the weak-target covariance and the strong-overlap contribution unpaid. Their signed convolution cannot be bounded by the homogeneous damping estimate alone.

## Second approach: coupled regression contraction

Define the three exact regression errors

\[
e=(\sqrt{Q_1}(m-1),\sqrt{Q_1}z,\sqrt Qh)^T.
\]

Their full two-layer Gram matrix $\mathsf G$ is positive semidefinite. All regression couplings, including strong-response relaxation and the strong-overlap coupling, can therefore be retained in

\[
e'=-\frac12\mathsf G e+rac{Q(1-n)}2
\begin{pmatrix}0\\\sqrt{Q_1}C_{12}\\\sqrt Q T_2\end{pmatrix}
+\varepsilon.
\]

The exact error vector is specified component by component; $|\varepsilon|\le CqS(1+S)$ without a small residual assumption. No mixed terms of a squared norm have been dropped.

The fundamental matrix $\mathsf U(T,t)$ of the homogeneous equation satisfies $\|\mathsf U(T,t)\|\le1$. This holds for noncommuting, time-dependent, possibly singular Gram matrices and uses no positive lower eigenvalue bound. It is evaluated along the actual trajectory. It is not a linearized sensitivity equation for a perturbed trajectory.

Variation of constants then gives

\[
e(T)=\mathsf U(T,t_b)e(t_b)+\mathcal F(T)+\mathcal Z(T),
\]

with

\[
\sup_T|\mathsf U(T,t_b)e(t_b)|\le1-M(b)+o_b(1),
\qquad \sup_T|\mathcal Z(T)|\le C_{b,K,c}q(1+\ell)^3\to0.
\]

The fixed entrance error can be made arbitrarily small by choosing $b$ large before taking small noise. Both controls hold without stopping at the residual boundary.

## Exact remaining term

The unpaid contribution to the scaled regression component $\sqrt Qh$ is

\[
\mathcal F_h(T)=\frac12\int_{t_b}^TQ(1-n(t))
\left[\sqrt{Q_1}\mathsf U_{32}(T,t)C_{12}(t)
+\sqrt Q\mathsf U_{33}(T,t)T_2(t)\right]dt.
\]

The strong-overlap term has been absorbed into coupled damping, but the transmitted $C_{12}$ source is still present. Neither term in this integral is discarded or assumed favorable. Norm contraction does not imply entrywise positivity of $\mathsf U$; $C_{12}\ge0$ does not sign its transported contribution. $T_2$ is itself signed.

For a concrete sufficient component budget, choose fixed $b$ so that the entrance term is below $r_*/8$, and then $q$ so the error is below $r_*/8$. The missing independent estimate

\[
\sup_{t_b\le T\le T_K}|\mathcal F_h(T)|\le r_*/4
\]

would imply $Qh^2\le r_*^2/4$. This allocation is sufficient, not necessary, and would not alone control the other residual components. The exact target could instead be imposed on the signed sum of entrance, forcing, and error. Neither estimate is proved here.

The rough triangle bound is $O((1+\ell)^2)$. Decreasing loss improves the full forcing vector to

\[
|\mathcal F(T)|\le\sqrt{31/80}+1-M(b)+o(1).
\]

This remains order one, whereas the sufficient component budget is $r_*/4=\lambda/3200$. The comparison is a failure of the available upper estimate to prove smallness. It is not evidence that the actual forcing is order one or that the target inequality is false.

## Dependency, boundary, and scope audit

- **Actual entrance.** HBD/BRW supply the fixed-delay state and physical mass bound. SPM supplies the fixed-delay cross-regression estimate. The initialization formula is P's exact aligned isotropic formula. None is extrapolated to a moving weak clock.
- **Cap independence.** The shape residual bound comes directly from the globally $S$-Lipschitz network and orthogonal Gaussian regression. The mixed-Gram estimates use uniform Gaussian feature moments. Bounded regression coefficients come from decreasing loss. These proofs do not use the old small cap.
- **Time interval.** The cutoff is deterministic for each fixed $K$. A half-response event later than this horizon is not covered by the vanishing uniform error estimate. Finiteness of the half-response hit is not proved, and RQT's residual-stopped alternative is not used circularly.
- **Faces.** There is no proposed invariant face in the new argument. The interval ends at a response target or a deterministic time. All Gaussian input gates, including entries and corners, are covered by the uniform feature estimates. No sign or monotonicity of $n$, $z$, $h$, or $T_2$ is assumed.
- **Damping versus nonlinear feedback.** Homogeneous contraction is a pathwise linear-algebra fact. The weak-target forcing depends on the same actual trajectory and retains the physical amplification mechanism. The statement is not a contraction theorem between two initialized nonlinear solutions.
- **Mass and precision.** All Gram matrices and moment bounds use the physical label measure. Integrated errors retain their logarithmic time cost. No isolated-outlier exponent, unproved moment, or fitted growth rate is used.
- **Constants.** The order is fixed $c,\rho,b,K$, then small $q$. The entrance can be made small by choosing fixed $b$ before $q$. Constants may depend on these fixed choices. No uniformity in $c\to0$ or $c\to\infty$ is claimed.
- **Limits and E5.** No COD constant is claimed at $s=t_\eta-t_h$. The result neither proves the small $h$ bound through half response nor the learned probe minimum below the coherent comparator. MPB's mean-output mechanism does not supply the signed forcing bound. Other residual components and the probe-motion comparison would remain after a bound for $h$.

The scalar and coupled-regression approaches stop at the displayed forcing convolution. All prior increments, foundations, checkpoints, synced sources, and GitHub remain unchanged. Every proof step is analytic, with no numerical trajectory, empirical value, or computer-assisted inequality as a premise.

**Artifact validation.** Both TeX escape scans pass. All sixteen labels are unique and all references resolve. The final compilation has no warnings or overfull boxes. All four pages were visually inspected, with the changed page rechecked after the final wording edit. The ZIP contains the PDF, TeX source, and review, with archive integrity and byte-for-byte contents checked.
