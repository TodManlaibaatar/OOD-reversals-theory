# Scaled population theory: reciprocal compensation, resident splitting, and analytical proof obligations

## Status and scope

This note responds to the new `split_mode_checks.py` and the accompanying experimental report. It replaces the **two-atom-only reduction strategy**, not the exact finite-parameter foundations. No repository was accessed or changed. No interval arithmetic or numerical trajectory certificate is used as a proof.

The main mathematical additions are:

1. An explicit nonlocal, noise-scaled population system whose atomic restriction is the previous six-dimensional system.
2. A derivation separating stable strong-family mean motion from unstable centered shape motion.
3. Exact linearized strong-stage and resident-stage amplification factors.
4. A positive compensation-lag law for an **arbitrary weak distribution**, not only a weak atom, and an exact limiting help factorization.
5. A distributional probe-error identity, including a negative covariance correction at fixed barycentre.
6. An explicit second-order response system specifying the small-splitting enhancement coefficient. Its numerical sign is checked, but its analytic positivity along the selected orbit remains to be proved.

These are not yet initialized theorems for the original isotropic population. Global arrival/capture into the scaled charts, entry seed/tail estimates, uniform finite-noise transfer over long delays, and canonical finite-parameter coverage remain open.

The reported snapshot experiments are treated as experimental evidence. The independent computations recorded in `scaled_population_splitting_checks.json` are diagnostics only. They do not reproduce the saved isotropic trajectories or the checks against `population_pilot.Model`, whose implementation and arrays are not mounted here.

---

## 1. Conventions

Use normalized data and time:

\[
P_1=\mathcal N(e_1,q^2 I_2),\qquad
P_2=\mathcal N(\rho e_2,q^2 I_2),\qquad
P=(P_1+P_2)/2,\qquad \tau=\mu_1^2t_{\rm phys}.
\]

Write \(\lambda=\rho^2\), \(0<\rho<1\), and let \(\phi,\Phi\) be the standard normal density and CDF. Define

\[
K(r)=\phi(r)+r\Phi(r)=\mathbb E(Z+r)_+.
\]

The strong and weak scaled coordinates are

\[
a_s=(\cos(qx),\sin(qx)),\qquad
b_s=(\cos(qy),\sin(qy)),
\]
\[
a_w=(\sin(qu),\cos(qu)),\qquad
b_w=(-\sin(qv),\cos(qv)).
\]

Let \(\mu_s(dx\,dy)\) and \(\mu_w(du\,dv)\) be their squared-radius-weighted finite measures. Define the **total**, not normalized, moments

\[
M=\int d\mu_s,\quad N=\int d\mu_w,
\quad Y=\int y\,d\mu_s,\quad V=\int v\,d\mu_w,
\]
\[
K_s=\int K(\rho x)\,d\mu_s,
\qquad K_w=\int K(u)\,d\mu_w.
\]

All equations below are for the leading scaled system. They apply while the relevant population is represented in bounded scaled charts; they do **not** assert that isotropic initialization starts in those charts. A population outside the charts must be tracked or bounded during an entry argument.

## 2. The Gaussian overlap kernel

Set

\[
\boxed{F(t,r)=\mathbb E[(Z+r)_+1_{\{Z+t>0\}}]
=\phi(\min(t,r))+r\Phi(\min(t,r)).}
\]

This follows by integrating from \(Z>\max(-t,-r)\). In particular,

\[
F(t,t)=K(t),\qquad
\partial_tF(t,r)=(r-t)_+\phi(t),\qquad
\partial_rF(t,r)=\Phi(\min(t,r)).
\]

The first derivatives agree across \(t=r\). On bounded sets the kernel is \(C^{1,1}\), but it is not generally \(C^2\) across the diagonal. Second-order shape expansions must therefore use the explicit one-sided formula or pair symmetrization, rather than an unspecified classical Hessian at coincident atoms.

Define

\[
\mathcal S(x)=\int F(\rho x,\rho\widetilde x)\,d\mu_s(\widetilde x,\widetilde y),
\qquad
\mathcal W(u)=\int F(u,\widetilde u)\,d\mu_w(\widetilde u,\widetilde v).
\]

## 3. The full leading scaled population system

The characteristic velocities are

\[
\boxed{
\begin{aligned}
x'={}&\frac12\left[-(1-M)x+\rho\phi(\rho x)-\rho\mathcal S(x)
+\lambda\{V+(1-N)y\}\Phi(\rho x)\right],\\
y'={}&\frac12\left[-(1-M)y-Y-K_w+\rho(1-N)K(\rho x)\right],\\
u'={}&\frac12\left[\phi(u)-\mathcal W(u)
-\{Y+(1-M)v\}\Phi(u)-\lambda(1-N)u\right],\\
v'={}&\frac12\left[\rho K_s-\lambda V-\lambda(1-N)v-(1-M)K(u)\right].
\end{aligned}}
\]

The corresponding transport–reaction equations are

\[
\partial_\tau\mu_s+\partial_x(x'\mu_s)+\partial_y(y'\mu_s)
=(1-M)\mu_s,
\]
\[
\partial_\tau\mu_w+\partial_u(u'\mu_w)+\partial_v(v'\mu_w)
=\lambda(1-N)\mu_w.
\]

Therefore

\[
\boxed{M'=M(1-M),\qquad N'=\lambda N(1-N).}
\]

The normalized weights of fixed labels within each family are constant in this leading system. The family distributions still move; neither is assumed atomic or coherent. Although the velocity at a prescribed point is affine in the measures through the displayed integrals, the coupled transport evolution is nonlinear.

### Derivation from training residuals

On cluster 1 write \(X=(1+qZ_1,qZ_2)\). The leading residuals are

\[
e_1(X)=(1-M)(1+qZ_1)+O(q^2),
\]
\[
e_2(X)=q\left[Z_2-Y-\int(Z_2+u)_+\,d\mu_w\right]+O(q^2).
\]

On cluster 2 write \(X=(qZ_1,\rho+qZ_2)\). Then

\[
e_1(X)=q\left[Z_1-\int(Z_1+\rho x)_+\,d\mu_s+\rho V\right]+O(q^2),
\]
\[
e_2(X)=(1-N)(\rho+qZ_2)+O(q^2).
\]

Insert these into the exact radial and angular gradient equations. Gaussian expectations use \(K\) and \(F\). The remainders here describe the expansion mechanism; a uniform finite-noise field/remainder proposition on the chosen chart class must still be supplied.

### Training-cluster source split

For the strong characteristics,

\[
x'_1=-\tfrac12(1-M)x,
\quad
y'_1=-\tfrac12[(1-M)y+Y+K_w],
\]
\[
x'_2=\tfrac12[\rho\phi(\rho x)-\rho\mathcal S(x)
+\lambda\{V+(1-N)y\}\Phi(\rho x)],
\quad
y'_2=\tfrac\rho2(1-N)K(\rho x).
\]

Strong mass growth is sourced by cluster 1 to leading order; weak mass growth by cluster 2. These conventions already include the mixture factor one half. Physical probe rates acquire a factor \(\mu_1^2q^2\) relative to the scaled rates below.

### Exact restrictions of the leading system

For \(\mu_s=M\delta_{(x,y)}\), \(\mu_w=N\delta_{(u,v)}\), the system reduces to the previous six-dimensional ODE. For \(M=1\), multiple strong sub-atoms, and one weak atom, it reduces to the `caricature` equations in the supplied `split_mode_checks.py`, including the minimum-overlap kernel. These are restrictions of one population equation, not different phenomenological models.

## 4. The resident curve during strong learning

Let \(a=a_\rho>0\) be the unique solution

\[
a=\rho K(\rho a).
\]

The derivative of \(a-\rho K(\rho a)\) is at least \(1-\rho^2>0\), and its values at zero and positive infinity have opposite signs.

When \(N=0\), the measure

\[
\mu_s=M(\tau)\delta_{(a,a)},\qquad M'=M(1-M)
\]

is an exact invariant curve of the scaled system. Substitution gives

\[
x'=\frac{1-M}{2}[-a+\rho K(\rho a)]=0,
\qquad y'=\frac12[-a+\rho K(\rho a)]=0.
\]

This proves a fixed-direction logistic **reference solution**. It does not assert that an arbitrary finite-width family or the full isotropic population is exactly at this direction during strong learning.

## 5. Mean motion and shape motion have different spectra

Put

\[
P=\Phi(\rho a),\qquad \alpha=\frac{\lambda P}{2}.
\]

Let a normalized strong-label law have mean-zero perturbations

\[
x_\beta=a+\varepsilon\xi_\beta,\quad
y_\beta=a+\varepsilon\eta_\beta,
\quad \mathbb E\xi=\mathbb E\eta=0.
\]

At first order \(\partial_tF(t,t)=0\) and \(\partial_rF(t,t)=\Phi(t)\). The donor-field variation depends only on the perturbation mean and therefore disappears for centered perturbations.

The centered linearized dynamics are

\[
\boxed{
\binom{\xi}{\eta}'
=J_{\rm sh}(M)\binom{\xi}{\eta},\qquad
J_{\rm sh}(M)=
\begin{pmatrix}
-(1-M)/2&\alpha\\
\alpha&-(1-M)/2
\end{pmatrix}.}
\]

The directions \((1,1)\), \((1,-1)\) have rates

\[
\sigma_+(M)=-(1-M)/2+\alpha,
\qquad \sigma_-(M)=-(1-M)/2-\alpha.
\]

In contrast, displacing the entire atom changes the residual. The mean block is

\[
\boxed{
J_{\rm mean}(M)=
\begin{pmatrix}
-(1-M)/2-M\alpha&\alpha\\
\alpha&-1/2
\end{pmatrix}.}
\]

At \(M=1\), the mean matrix is negative definite because \(0<\alpha<1/2\), while the centered shape rates are \(+\alpha,-\alpha\).

Thus stability of the coherent two-atom angular block does not imply stability of condensation. The new splitting calculation identifies a genuine missing transverse population sector.

For a continuum of labels, this is not literally a single additional unstable coordinate: every admissible centered label profile times \((1,1)\) is an unstable first-order shape perturbation. "Weak growth and strong splitting" describes two types of growth, not a proved two-dimensional unstable manifold of the full measure flow. Label-weight and zero-mass chart degeneracies must also be treated in any function-space manifold statement.

At \(\rho=2/3\), numerical evaluation of the explicit scalar constants gives

\[
a\approx0.3512850353,\quad
\alpha\approx0.1316847267,\quad
1-2\alpha\approx0.7366305466.
\]

The exact sign threshold is \(M>1-2\alpha\); the decimals are not needed for that proposition.

## 6. The moving split matrix during weak learning

About a coherent state with masses \(M,N\) and angles \((x,y,u,v)\), centered strong perturbations obey

\[
\boxed{
J_{\rm sh}(\tau)=
\begin{pmatrix}
-(1-M)/2+\beta(\tau)&A(\tau)\\
A(\tau)&-(1-M)/2
\end{pmatrix},}
\]

where

\[
A=\frac\lambda2(1-N)\Phi(\rho x),
\qquad
\beta=\frac{\rho^3}{2}[Nv+(1-N)y-x]\phi(\rho x).
\]

The \(N=0,x=y=a\) formula is recovered exactly. During the weak-learning orbit, however, there is an additional diagonal term and \(\Phi(\rho x)\) varies. A frozen \(\alpha(1-N)\) is the resident approximation, not the full moving coefficient.

In particular, the eigendirections need not remain at 45 and 135 degrees throughout weak learning. This is consistent with the reported rotation of the measured shape axis.

### Nonlinear ordering, not merely linear eigenvectors

At a fixed evolving population field,

\[
\partial_y x'=\partial_x y'
=\frac\lambda2(1-N)\Phi(\rho x)\ge0
\quad (0\le N\le1).
\]

Therefore two strong characteristics that are ordered in both \(x\) and \(y\) remain componentwise ordered while the solution exists in the chart. At the first equality of one coordinate, the other ordered coordinate cannot push its difference negative. A standard first-exit argument, or its strict-barrier version, proves the claim.

For a pairwise co-ordered strong distribution, normalized mass weights remain fixed and

\[
\operatorname{Cov}(x,y)
=\frac12\mathbb E_{\beta,\gamma}
[(x_\beta-x_\gamma)(y_\beta-y_\gamma)]\ge0.
\]

The observed one-sidedness is a separate entry-distribution question. A symmetric splitting matrix alone does not produce an asymmetric tail from symmetric data in the local coordinates.

## 7. Exact linearized passage multipliers

For a centered eigenmode \(h_\pm\) along the resident strong-learning curve,

\[
\frac{h_\pm(\tau_1)}{h_\pm(\tau_0)}
=e^{\pm\alpha(\tau_1-\tau_0)}\sqrt{\frac{M_0}{M_1}}.
\]

This follows by integrating \(\int(1-M)d\tau=\log(M_1/M_0)\).

For the slow \((1,1)\) mode,

\[
\boxed{
\frac{h_+(M_1)}{h_+(M_0)}
=\left(\frac{M_1}{M_0}\right)^{\alpha-1/2}
\left(\frac{1-M_0}{1-M_1}\right)^\alpha.}
\]

Thus, for a fixed final mass less than one, \(M_0\asymp S_0\) gives the factor \(S_0^{1/2-\alpha}\), **provided** entry into the local chart and the initial mode amplitude have been established.

For the frozen resident approximation during weak growth,

\[
h_+'=\alpha(1-N)h_+,\qquad N'=\lambda N(1-N),
\]

so

\[
\boxed{h_+(N)=h_+(N_0)(N/N_0)^{\alpha/\lambda}.}
\]

At weak half-learning the amplification is \((2N_0)^{-\alpha/\lambda}\). On the actual moving orbit the matrix from Section 6 replaces the frozen one. Proving that the leading power survives with bounded multiplicative corrections is a saddle-passage estimate, not a direct substitution.

If strong-stage entry estimates yield mode size \(S_0^{1/2-\alpha}\) and weak seed \(N_0\asymp S_0^{c_0}\), the formal combined exponent is

\[
\eta=\frac12-\alpha-c_0\frac\alpha\lambda.
\]

For \(\rho=2/3,c_0=1\), this is approximately \(0.07202464\). The scalar equation for the formal zero with \(c_0=1\),

\[
(1+\rho^2)\Phi(\rho a_\rho)=1,
\]

has numerical root approximately \(0.75976119\). This is an exponent-balance prediction conditional on the entry laws and the passage estimates, **not a proved phase transition** of the isotropic population.

## 8. The weak attractor is generated during learning

For \(M=N=0\), a weak-chart equilibrium would require

\[
v=-K(u)/\lambda,
\qquad
\phi(u)+K(u)\Phi(u)/\lambda-\lambda u=0.
\]

There is no real root when \(0<\lambda<1\). For \(u\le0\), every term in the first expression for the scalar equation is nonnegative and the density term is positive. For \(u>0\), its left-hand side is at least its value at \(\lambda=1\):

\[
\phi(u)+K(u)\Phi(u)-u
=(1+\Phi(u))[K(u)-u]>0.
\]

For a frozen resident mass \(M\), with strong direction \((a,a)\), eliminating the weak output coordinate gives

\[
\boxed{
F_M(u)=\phi(u)-Ma\left(1+\frac{1-M}{\lambda}\right)\Phi(u)
+\frac{(1-M)^2}{\lambda}K(u)\Phi(u)-\lambda u.}
\]

A saddle-node candidate solves \(F_M=\partial_uF_M=0\). Numerical solution at \(\rho=2/3\) gives \(M\approx0.47682779,u\approx1.60506815\), consistent with the reported onset. This is a numerical check of a frozen-parameter bifurcation condition, not yet an analytical capture theorem for the time-varying mass.

The weak seed must be derived from the arrival/capture of labels under the evolving residual field. Assuming a pre-existing weak attractor from time zero would not be a valid initialization argument.

## 9. Removing the artificial rho restriction in the two-atom theorem

The earlier \(\rho\le1/\sqrt2\) restriction was used to guarantee \(u_\rho>0\) through a convenient upper bound on \(a_\rho\). It was not essential to the subsequent lag and reversal arguments.

For any \(0<\rho<1\), allow \(u_\rho\) to be a real root of

\[
F(u)=\phi(u)-a_\rho\Phi(u)-\lambda u=0.
\]

Define \(r(u)=\phi(u)/\Phi(u)\). Then

\[
\frac{F(u)}{\Phi(u)}=r(u)-a_\rho-\lambda\frac u{\Phi(u)}.
\]

Here

\[
r'(u)=-r(u)[u+r(u)]<0,
\]

because \(u+r(u)=K(u)/\Phi(u)>0\). Also

\[
\left(\frac u{\Phi(u)}\right)'
=\frac{\Phi(u)-u\phi(u)}{\Phi(u)^2}>0.
\]

For negative \(u\) the numerator is plainly positive; for nonnegative \(u\) it starts at one half and has derivative \(u^2\phi(u)\ge0\). Thus \(F/\Phi\) is strictly decreasing from positive infinity to negative infinity. The real root is unique, and \(F'(u_\rho)<0\).

This supplies the negative weak angular eigenvalue without assuming positive \(u_\rho\). The remaining selected-orbit reversal argument uses \(\lambda<1\), positivity of \(K\) and \(K-r\), not positive \(u_\rho\). Its pointwise-in-parameter conclusion therefore extends to \(0<\rho<1\) with this corrected root convention. No uniform constants up to \(\rho=1\) are claimed; \(a_\rho\) grows as that boundary is approached.

The scripts' fixed positive root bracket must be changed before testing the extended range. The real weak root becomes negative at sufficiently large rho.

The old lower-barrier step for strong \(x\) can also be replaced by the integrable-negative-part argument: the invariant \(v-x>0\) and the forward linear-growth bound imply

\[
(x')_-\le \frac\lambda2(1-N)(v-y),
\]

whose right-hand side is integrable. Hence \(x\) is bounded below. The remainder of the gate-hit contradiction is unchanged.

## 10. A distributional positive-lag theorem

This is stronger than the old two-atom lag law.

Assume \(M=1\) in the leading system. Let \(\eta_w=\mu_w/N\) for \(N>0\); its normalized weights are constant along characteristics. Put

\[
L=Y+K_w=Y+N\mathbb E_{\eta_w}K(u),\qquad
Q(u)=\Phi(u).
\]

Define

\[
\Xi(\eta_w)
=\mathbb E[Q\phi]
+\mathbb E[K]\,\mathbb E[Q^2]
-\mathbb E_{u,r}[Q(u)F(u,r)].
\]

Direct differentiation of \(L\), including weak mass growth and weak angular transport, gives

\[
\boxed{
\begin{aligned}
L'={}&-\frac{1+N\mathbb E[Q^2]}2L
+\frac\rho2(1-N)K_s\\
&+\frac{N(1-N)}2
\left[\lambda\mathbb E(K+\phi)+\mathbb E(Q\phi)\right]
+\frac{N^2}{2}\Xi(\eta_w).
\end{aligned}}
\]

### The last forcing has a positive pair-kernel representation

Let \(r_- =\min(u,r)\), \(r_+=\max(u,r)\), and \(g(t)=K(t)-t>0\). Symmetrizing in the two independent weak labels gives

\[
\boxed{
\begin{aligned}
\Xi(\eta_w)=\frac12\mathbb E_{u,r}\Big[&
 g(r_+)\{\Phi(r_-)^2+\Phi(r_+)^2\}\\
&+[K(r_+)-K(r_-)]\Phi(r_+)[1-\Phi(r_+)]\Big]>0.
\end{aligned}}
\]

Every term is nonnegative and the first is strictly positive for finite coordinates.

To check the algebra, suppose \(u\le r\). Then \(F(u,r)=\phi(u)+r\Phi(u)\), \(F(r,u)=K(u)\). Twice the symmetrized integrand reduces to

\[
\Phi(r)\phi(r)+[K(r)-r]\Phi(u)^2-K(u)\Phi(r)[1-\Phi(r)],
\]

which equals the displayed positive expression after adding and subtracting \(K(r)\Phi(r)[1-\Phi(r)]\).

Thus every forcing term in the lag equation is nonnegative for \(0\le N\le1\). For a positive incoming lag,

\[
\boxed{L(\tau)>0}
\]

through every finite chart-valid interval. At \(N=0\) the formula is interpreted by continuity and the terms multiplied by \(N\) disappear. At a weak Dirac measure, \(\Xi=[K(u)-u]\Phi(u)^2\), recovering the previous identity.

This sign result requires neither strong condensation nor weak condensation.

## 11. Exact scaled population probe error and source rates

For \(\xi_q=(\sin(q\zeta),-\cos(q\zeta))\), bounded weak coordinates are inactive for sufficiently small positive \(q\). Define

\[
A_\zeta=\int(\zeta-x)_+\,d\mu_s,
\qquad
B_\zeta=\int y(\zeta-x)_+\,d\mu_s.
\]

Static Taylor expansion on bounded chart support gives

\[
f_1(\xi_q)=qA_\zeta+O(q^3),\qquad
f_2(\xi_q)=q^2B_\zeta+O(q^4),
\]

and hence

\[
\boxed{
E_{\xi_q}-\frac12
=q^2\mathcal E_\zeta+O(q^4),\qquad
\mathcal E_\zeta=\frac12A_\zeta^2-\zeta A_\zeta+B_\zeta.}
\]

The leading formula automatically retains an inactive bridge, using the positive part rather than a fixed all-active approximation.

For \(M=1\), strong-cluster source velocities satisfy

\[
x'_1=0,\qquad y'_1=-L/2.
\]

Thus the exact **scaled population** help law is

\[
\boxed{d_1=-\frac12A_\zeta L.}
\]

As long as \(A_\zeta>0\), the distributional positive-lag theorem proves \(d_1<0\). This is an exact exposure-times-lag law in the leading system, not a fitted product of mean angles.

The other source rate is

\[
\boxed{
d_2=\int_{x<\zeta}(\zeta-A_\zeta-y)x'_2\,d\mu_s
+\frac\rho2(1-N)\int(\zeta-x)_+K(\rho x)\,d\mu_s.}
\]

Exactly, \(\mathcal E_\zeta'=d_1+d_2\) wherever the chain rule holds, and almost everywhere in time under the usual characteristic regularity. The second term retains weak-sourced output rotation before weak saturation.

Proving \(d_2>0\) and its takeover for broad split distributions remains a dynamical task. The formula does not assign that sign to arbitrary states.

## 12. The covariance mechanism is explicit at fixed barycentre

Assume \(M=1\) and every strong label is active at the probe. Put

\[
\bar x=\int x\,d\mu_s,\quad \bar y=\int y\,d\mu_s,
\quad C_{xy}=\int(x-\bar x)(y-\bar y)\,d\mu_s.
\]

Then

\[
\boxed{
\mathcal E_\zeta
=-\frac12\zeta^2+\frac12\bar x^2+
\bar y(\zeta-\bar x)-C_{xy}.}
\]

Proof: \(A_\zeta=\zeta-\bar x\) and \(B_\zeta=\bar y(\zeta-\bar x)-C_{xy}\), which give the result by substitution.

Thus a positive input/output covariance improves the scaled probe error relative to the coherent state with the same mass and barycentre. A centered split along \((1,1)\) contributes exactly \(-\operatorname{Var}(x)\) at that fixed state.

For a partially active strong family, let \(M_A\), \(\bar x_A,\bar y_A,C_A\) denote the mass, normalized means, and covariance restricted to \(x<\zeta\). The more general exact formula is

\[
\mathcal E_\zeta
=\frac{M_A^2}{2}(\zeta-\bar x_A)^2
-M_A(\zeta-\bar x_A)(\zeta-\bar y_A)-M_A C_A.
\]

Do not apply the full-mass all-active identity to a canonical-sized inactive bridge. The positive-part law in Section 11 covers it directly.

The empirical rms in `tail_stats` is around a weighted median, not around the mean:

\[
\mathbb E[(x-\mathrm{median}(x))^2]
=\operatorname{Var}(x)+(\bar x-\mathrm{median}(x))^2.
\]

For an asymmetric tail those can differ substantially. A coefficient measured against that rms squared need not equal a coefficient measured against centered variance.

## 13. A second-order response system for small centered splits

A fixed-state covariance identity does not by itself prove a positive change in the trained minimum: splitting also perturbs the mean trajectory. This section specifies both effects without treating the mean shift as negligible.

Assume \(M=1\), one weak atom, and let \((X,Y,U,V)\) be the selected two-atom weak-learning orbit with prescribed logistic \(N(s)\). Consider strong-label perturbations

\[
x_\gamma=X+\varepsilon p(s)h_\gamma+O(\varepsilon^2),\quad
y_\gamma=Y+\varepsilon r(s)h_\gamma+O(\varepsilon^2),
\]

where \(\mathbb E h=0\), \(\mathbb E h^2=1\), and the profile is bounded. Then

\[
\begin{pmatrix}p\\r\end{pmatrix}'=J_{\rm sh}(s)\begin{pmatrix}p\\r\end{pmatrix}
\]

with the matrix from Section 6.

Write the second-order mean changes as

\[
\bar x=X+\varepsilon^2X_2+o(\varepsilon^2),\quad
\bar y=Y+\varepsilon^2Y_2+o(\varepsilon^2),
\]

and similarly \(u=U+\varepsilon^2U_2+o(\varepsilon^2)\), \(v=V+\varepsilon^2V_2+o(\varepsilon^2)\).

Let \(F=NV+(1-N)Y-X\), \(P=\Phi(\rho X)\), \(Q=\Phi(U)\). The coherent angular Jacobian is

\[
J_c=\begin{pmatrix}
\frac\lambda2[-P+\rho F\phi(\rho X)]&\frac\lambda2(1-N)P&0&\frac\lambda2NP\\
\frac\lambda2(1-N)P&-1/2&-NQ/2&0\\
0&-Q/2&-\frac12[(U+Y)\phi(U)+NQ+\lambda(1-N)]&0\\
\lambda P/2&0&0&-\lambda/2
\end{pmatrix}.
\]

Then the second-order response obeys

\[
\boxed{
\begin{pmatrix}X_2\\Y_2\\U_2\\V_2\end{pmatrix}'
=J_c\begin{pmatrix}X_2\\Y_2\\U_2\\V_2\end{pmatrix}
+\frac{\rho^3\phi(\rho X)}4
\begin{pmatrix}
-[1+\rho^2XF]p^2+2(1-N)pr\\
(1-N)p^2\\
0\\
p^2
\end{pmatrix}.}
\]

### Why no extra unspecified kernel Hessian appears

For bounded offsets \(a,b\), at small \(\varepsilon\),

\[
F(t+\varepsilon a,t+\varepsilon b)
=K(t)+\varepsilon\Phi(t)b
+\frac{\varepsilon^2\phi(t)}2[b^2-(b-a)_+^2]+O(|\varepsilon|^3)
\]

when \(\varepsilon>0\); a signed perturbation uses the corresponding one-sided expression. For two independent, identically distributed centered offsets,

\[
\mathbb E(b-a)_+^2=\operatorname{Var}(b).
\]

Thus the second-order correction of the double-averaged overlap vanishes at fixed mean. The remaining elementary Taylor terms give the displayed forcing. For a bounded profile on a finite chart-valid window, the locally Lipschitz first derivatives and these explicit expansions supply the usual variation-of-constants justification of the second-order mean equation.

### Minimum-depth coefficient

At an interior unperturbed minimum \(s_*\), with all perturbed strong labels still active,

\[
\mathcal E_\varepsilon(s_*)
=\mathcal E_0(s_*)+\varepsilon^2\left[
(X-Y)X_2+(\zeta-X)Y_2-pr\right]_{s_*}+o(\varepsilon^2).
\]

The \(-pr\) term is the direct covariance benefit. The other two terms are mean backreaction. Defining \(\sigma_{\rm half}^2=\varepsilon^2p(0)^2\), the candidate enhancement coefficient is

\[
\boxed{
\kappa(\rho,\zeta)=
\frac{[pr-(X-Y)X_2-(\zeta-X)Y_2]_{s_*}}{p(0)^2}.}
\]

A negative error correction at the unperturbed minimum already gives an improvement lower bound by evaluating there. An equality expansion for the perturbed minimizing value needs a controlled minimizer selection, for example an isolated nondegenerate minimum and uniform expansions.

**Analytical positivity of this coefficient has not been established here.** Hyperbolic passage does not supply its sign. The direct covariance term has the right sign, but mean response is of the same perturbative order.

For the numerical check at \(\rho=2/3,\zeta=1.745329\ldots\), with a centered incoming \((1,1)\) split, the response equations give \(\kappa\approx1.75053\) per unit strong-input variance at weak half-learning. The scaled error correction decomposes approximately as

\[
-1.68219\quad\text{(direct covariance)},\qquad
-0.09671\quad\text{(mean input)},\qquad
+0.02837\quad\text{(mean output)}.
\]

This numerically agrees with the reported small-split coefficient, without fitting a new coefficient. It is not a proof that \(\kappa>0\) throughout a parameter interval, and is not an extrapolation to the canonical broad tail.

## 14. Long sojourns and the order of limits

Suppose a proved bounded-chart finite-noise expansion gives

\[
(\log m_i)'=1-M+q^2r_i,\qquad |r_i|\le C.
\]

For two strong labels,

\[
\left|\log\frac{m_i(\tau)/m_j(\tau)}{m_i(0)/m_j(0)}\right|
\le 2Cq^2\tau.
\]

The analogous weak estimate holds. This explains the cumulative \(q^2\log(1/S_0)\) issue, rather than removing it. A sufficient joint scaling could impose

\[
q^2\log(1/S_0)\to0,
\]

along with the entry/shape conditions. For example \(S_0=e^{-1/q}\) meets this scale condition and \(S_0/q^2\to0\). This is not interchangeable with taking \(S_0\to0\) at a fixed \(q\).

One must also propagate finite-noise corrections through the unstable splitting sector. A useful structural fact is that exactly coincident atoms remain coincident for the finite-noise equations: finite noise does not spontaneously create a shape split from exact equality. Using a consistent finite-q reference can therefore turn an apparent additive split forcing into a multiplicative perturbation of the split dynamics. This cancellation needs to be preserved in the long-time proof.

The \(q^2\log\) condition alone does not establish chart entry, a weak seed, tail control, or probe-rate convergence at the \(q^2\) scale.

## 15. A correct conditional passage target

The useful conditional small-shape parameter is of the form

\[
\varepsilon_{\rm shape}
=\delta_{\rm ent}N_{\rm ent}^{-\alpha/\lambda},
\]

with explicit allowances for mean/weak-angular entry errors, uncharted mass, and finite-noise errors. A tail condition by itself is not a complete hypothesis.

A suitable analytical lemma would establish that, under quantified entry and passage conditions, the scaled measure trajectory is close enough to the selected weak branch on fixed interior witness windows to preserve

\[
d_1<0<d_2,\qquad d_1+d_2<0\text{ early},\qquad
 d_1+d_2>0\text{ late}.
\]

The old two-atom reversal proof supplies strict interior witnesses. The new population lag theorem supplies the helpful sign without condensation. Ordinary analytic continuous dependence on finite windows can transfer the remaining strict margins once the entry/passage norm is controlled.

The baseline depth should be denoted \(\mathcal A_0(\rho,\zeta)\), not the rounded constant 2.009. A conditional robustness theorem first gives a positive \(cq^2\) rebound or a comparison \(q^2[\mathcal A_0+O(\varepsilon)]\). The stronger formula

\[
q^2[\mathcal A_0+\kappa\operatorname{Var}+o(\operatorname{Var})]
\]

needs the second-order response and an analytic sign argument for \(\kappa\). It must not be appended automatically to a first-order passage theorem.

## 16. Revised analytical roadmap

1. **Scaled population reduction.** Formalize the compact-chart finite-noise expansion, exact leading transport–reaction system, and normalized-rate transfer. Track all uncharted mass explicitly.
2. **Global isotropic entry.** Use the earlier analytical escape machinery plus a genuine global angular/capture argument. Produce the strong local shape, weak incoming seed, and fixed-label/moving-boundary bookkeeping without assuming an early weak attractor.
3. **Strong-learning contraction and resident passage.** Establish nonlinear versions of the explicit mode multipliers, including mean backreaction and weak angular relaxation. Determine the actual entry exponent or inequalities; do not assume measured \(c_0\).
4. **Weak-learning mechanism and crossover.** Combine the population lag sign, exact probe law, selected weak branch, and controlled shape evolution. Prove strict cluster signs and quantitative reversal on interior windows.
5. **Finite-initialization enhancement.** Establish positivity of the small-shape response coefficient, then decide whether broader split distributions can be handled by nonperturbative inequalities. A local variance expansion does not automatically cover the canonical inactive bridge.
6. **Final initialized A and B.** Remove all entry hypotheses by composition of the preceding lemmas, state the genuine joint parameter region, and distinguish proven finite-parameter coverage from empirical agreement at the canonical point.

This is one analytical system containing the coherent weak-growth edge and the split-enhanced trajectories. It does not yet prove that the canonical isotropic trajectory lies in a quantitatively controlled portion of that system.

## 17. Diagnostic provenance

The supplied `split_mode_checks.py` provides a two-atom field comparison, test-particle split checks, saved-label shape measurements, and a prescribed two-sub-atom experiment. Its final small-split minimum is selected on a finite time grid, and its canonical rms is taken about a median. Those definitions must be respected when comparing coefficients.

`scaled_population_splitting.py` supplies independent calculations based on the equations derived in this note. The recorded checks include:

- 100 random one-strong/one-weak reductions, maximum source-resolved discrepancy about \(2.2\times10^{-16}\).
- Centered multi-atom shape derivatives, including the moving diagonal correction, agreeing with finite differences to about \(1.4\times10^{-8}\) at difference step \(10^{-6}\).
- The exact covariance observable identity, agreement about \(5.6\times10^{-17}\).
- 300 arbitrary weak-distribution lag checks, maximum direct/formula discrepancy about \(6.5\times10^{-16}\).
- Independent conditioned-Gaussian quadrature at two multi-atom states. Source-field discrepancies decrease by factors close to four under successive halving of q. This quadrature is truncated at twelve standard deviations for diagnostics and is not a rigorous error enclosure.

No saved isotropic population run was integrated or re-evaluated in this step. Numerical decimals in this note are checks, not premises of the analytical identities.
