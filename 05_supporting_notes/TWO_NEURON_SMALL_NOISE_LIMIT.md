# Two-neuron small-noise SIM theory: explicit equations and an analytic reversal argument

## Status

This document is new analytical work prompted by the supplied `few_neuron.py`, `check_laws.py`, and `q_scaling.py` and the user's small-initialization/noise experiments.

It contains:

1. The six-dimensional leading vector field in noise-scaled angular coordinates, retaining both neuron masses and the two training-cluster sources.
2. An exact probe-error formula and its leading expansion.
3. A selected weak-learning orbit of the limiting ODE, characterized by a resident saddle rather than fitted numerical entry data.
4. An analytic reversal argument for that limiting orbit, including an invariant sign for the strong-cluster contribution.
5. The two unresolved bridges to an initialized isotropic-population theorem: condensation/selection and uniform finite-noise transfer.

The finite-dimensional limiting-ODE results are NOT yet Theorems A and B for the initialized continuum population. In particular, two-atom invariance is not condensation. No saved numerical trajectory or interval arithmetic is used as a premise of the analytical argument. Numerical checks are reported separately and are not proof certificates.

The companion file `two_neuron_limit.py` implements the derived system and diagnostic checks without importing `population_pilot` or accessing GitHub. The original uploaded scripts are unchanged.

## 1. Setup, coordinates, and units

Use normalized Gaussian distributions

\[
P_1=\mathcal N(e_1,q^2I_2),\qquad
P_2=\mathcal N(\rho e_2,q^2I_2),\qquad P=(P_1+P_2)/2.
\]

The target is the identity and the loss is \(\frac12\mathbb E_P\|f(X)-X\|^2\). Time below is normalized: \(\tau=\mu_1^2t_{\rm phys}\). Physical rates equal normalized rates times \(\mu_1^2\).

For two balanced atoms, write

\[
f(X)=m b_s(a_s^\top X)_++n b_w(a_w^\top X)_+,
\]

\[
\begin{aligned}
a_s&=(\cos(qx),\sin(qx)),&b_s&=(\cos(qy),\sin(qy)),\\
a_w&=(\sin(qu),\cos(qu)),&b_w&=(-\sin(qv),\cos(qv)).
\end{aligned}
\]

Thus \(x=\vartheta_s\), \(y=\chi_s\), \(u=\vartheta'_w\), \(v=\chi'_w\) in the user's notation. A positive \(u\) means the weak input points below \(90^\circ\); a positive \(v\) means its output points above \(90^\circ\). The variables \(m,n\) are actual atom masses, not the log-mass variables used internally by the supplied integrator.

Let

\[
\phi(z)=(2\pi)^{-1/2}e^{-z^2/2},\quad
\Phi(z)=\int_{-\infty}^{z}\phi(s)\,ds,\quad
K(z)=\phi(z)+z\Phi(z).
\]

Then \(K(z)=\mathbb E(Z+z)_+\), \(K'(z)=\Phi(z)\), and

\[
g(z):=K(z)-z=\mathbb E[-(Z+z)]_+>0.
\]

The training dynamics contain \(\rho\), but not the probe offset \(\zeta\).

## 2. Exact two-atom equations before taking the noise limit

For \(e(X)=X-f(X)\), define raw cluster moments

\[
R_{p,i}=\mathbb E_{P_p}[e(X)X^\top1_{\{a_i^\top X>0\}}].
\]

For each atom \(i\), the cluster-\(p\) contributions, including mixture weight \(1/2\), are

\[
(\theta_i')_p=\frac12 b_i^\top R_{p,i}a_i^\perp,
\quad
(\psi_i')_p=\frac12(b_i^\perp)^\top R_{p,i}a_i,
\quad
(m_i')_p=m_i b_i^\top R_{p,i}a_i.
\]

For the weak input coordinate use \(u'=-\theta_w'/q\), not \(+\theta_w'/q\). For the other scaled angles divide the corresponding angular derivative by \(q\).

A finite atomic initial measure remains atomic under these characteristic equations. This establishes that the two-atom model is exact within its own invariant class; it does not show that isotropic initialization approaches that class.

## 3. Deriving the leading residuals

Take independent standard normals \(Z_1,Z_2\). On bounded scaled-angle/mass sets, the atom associated with a cluster is active on that cluster except for exponentially small Gaussian tails. The other atom's gate remains a nontrivial truncated-normal gate.

### Cluster 1

For \(X=(1+qZ_1,qZ_2)\),

\[
(a_s^\top X)_+=1+qZ_1+O_{L^p}(q^2),
\qquad
(a_w^\top X)_+=q(Z_2+u)_++O_{L^p}(q^2),
\]

with the own-gate tail understood separately. Consequently

\[
e_1=(1-m)(1+qZ_1)+O_{L^p}(q^2),
\qquad
e_2=q[Z_2-my-n(Z_2+u)_+]+O_{L^p}(q^2).
\]

### Cluster 2

For \(X=(qZ_1,\rho+qZ_2)\),

\[
(a_s^\top X)_+=q(Z_1+\rho x)_++O_{L^p}(q^2),
\qquad
(a_w^\top X)_+=\rho+qZ_2+O_{L^p}(q^2),
\]

and

\[
e_1=q[Z_1-m(Z_1+\rho x)_++n\rho v]+O_{L^p}(q^2),
\qquad
e_2=(1-n)(\rho+qZ_2)+O_{L^p}(q^2).
\]

These expansions are local in the scaled chart. They are not uniform at an initial weak angle of \(120^\circ\), for which \(u=-\pi/(6q)\) diverges as \(q\to0\).

Use

\[
\mathbb E1_{\{Z+a>0\}}=\Phi(a),\qquad
\mathbb E[Z1_{\{Z+a>0\}}]=\phi(a),\qquad
\mathbb E(Z+a)_+=K(a).
\]

## 4. The explicit six-dimensional leading ODE

The resulting limiting equations are

\[
\boxed{m'=m(1-m),\qquad n'=\rho^2n(1-n).}
\]

\[
\boxed{
x'=\frac12\left[
-(1-m)x+\rho(1-m)\phi(\rho x)
+\rho^2\{nv-mx+(1-n)y\}\Phi(\rho x)
\right].
}
\]

\[
\boxed{
y'=\frac12[-y-nK(u)+\rho(1-n)K(\rho x)].
}
\]

\[
\boxed{
u'=\frac12\left[
(1-n)\phi(u)-\{nu+my+(1-m)v\}\Phi(u)-\rho^2(1-n)u
\right].
}
\]

\[
\boxed{
v'=\frac12[\rho mK(\rho x)-\rho^2v-(1-m)K(u)].
}
\]

The full finite-noise scaled vector field has this leading field on compact scaled-state sets. A conservative local remainder target is \(O(q)\); the independent diagnostic evaluations below show \(O(q^2)\) behavior at the checked states. That observed rate should not replace a proved uniform estimate. The required Gaussian truncation estimates can be obtained in the rotating input frame, where the gate coordinate is a one-dimensional Gaussian and the orthogonal coordinate is independent. Differentiating an unscaled pointwise gate is not a valid shortcut.

On a fixed time interval staying in a compact scaled chart, a uniform field estimate plus ordinary ODE stability supplies finite-noise convergence. It does not, by itself, provide convergence over the diverging initialization delay or justify the order of the small-noise and small-initialization limits.

### Cluster decomposition of the angular field

For the strong atom,

\[
 x'_1=-\frac12(1-m)x,
\quad
 y'_1=-\frac12[y+nK(u)],
\]

\[
 x'_2=\frac12\left[\rho(1-m)\phi(\rho x)
 +\rho^2\{nv-mx+(1-n)y\}\Phi(\rho x)\right],
\quad
 y'_2=\frac\rho2(1-n)K(\rho x).
\]

For the weak atom,

\[
 u'_1=\frac12[(1-n)\phi(u)-\{nu+my+(1-m)v\}\Phi(u)],
\quad v'_1=-\frac12(1-m)K(u),
\]

\[
 u'_2=-\frac{\rho^2}{2}(1-n)u,
\quad v'_2=\frac12[\rho mK(\rho x)-\rho^2v].
\]

Only cluster 1 contributes to the leading strong mass equation and only cluster 2 to the leading weak mass equation.

## 5. The exact error formula and the mass correction

Use the unit probe

\[
\xi_q=(\sin(q\zeta),-\cos(q\zeta)).
\]

At bounded scaled states and small positive \(q\), the weak atom is inactive:

\[
a_w^\top\xi_q=-\cos(q(u+\zeta))<0.
\]

When \(\zeta>x\) with a positive scaled margin, the strong atom is active. Exactly,

\[
a_s^\top\xi_q=\sin(q(\zeta-x)),
\qquad
b_s^\top\xi_q=\sin(q(\zeta-y)).
\]

Therefore

\[
\boxed{
E_{\xi_q}-\frac12
=\frac{m^2}{2}\sin^2(q(\zeta-x))
-m\sin(q(\zeta-x))\sin(q(\zeta-y)).
}
\]

Its compact-state expansion is

\[
E_{\xi_q}-\frac12
=q^2\left[\frac{m^2}{2}(\zeta-x)^2-m(\zeta-x)(\zeta-y)\right]+O(q^4).
\]

For \(m=1\), this is

\[
\boxed{
\mathcal E_\zeta(x,y)
=-\frac12\zeta^2+\frac12x^2+y(\zeta-x),
\qquad
E_{\xi_q}-\frac12=q^2\mathcal E_\zeta+O(q^4).
}
\]

For \(x\ge\zeta\), the corresponding limiting observable is zero, because both atoms are inactive at the probe. Equivalently, for all \(x\),

\[
\mathcal E_\zeta=\frac12(\zeta-x)_+^2-(\zeta-x)_+(\zeta-y).
\]

The general mass formula must be used before strong learning. Keeping \(m\) only in the compensation term is not the general leading expansion. The supplied `check_laws.py` uses the simplified geometry with a comment that the strong mass is approximately one; that is a late-regime check, not a global error identity.

## 6. Selected weak-learning orbit: a precise entrance condition

After strong learning, the leading system has the invariant surface \(m=1\). Retain \(n\): setting \(n=1\) prematurely removes the weak-learning clock.

With \(\lambda=\rho^2\), the five-dimensional system is

\[
 n'=\lambda n(1-n),
\]

\[
 x'=\frac\lambda2[nv-x+(1-n)y]\Phi(\rho x),
\]

\[
 y'=\frac12[-y-nK(u)+\rho(1-n)K(\rho x)],
\]

\[
 u'=\frac12[(1-n)(\phi(u)-\lambda u)-(nu+y)\Phi(u)],
\]

\[
 v'=\frac12[\rho K(\rho x)-\lambda v].
\]

For \(0<\rho\le1/\sqrt2\), let \(a_\rho>0\) solve

\[
a_\rho=\rho K(\rho a_\rho).
\]

It is unique: the derivative of \(a-\rho K(\rho a)\) is at least \(1-\rho^2>0\), the value at zero is negative, and the expression tends to infinity. Also

\[
a_\rho\le\frac{\rho\phi(0)}{1-\rho^2}<2\phi(0).
\]

Let \(u_\rho>0\) solve

\[
\phi(u_\rho)-a_\rho\Phi(u_\rho)-\rho^2u_\rho=0.
\]

Existence follows from a positive value at zero and a negative limit at infinity; strict monotonicity on \([0,\infty)\) follows from derivative

\[
-(u+a_\rho)\phi(u)-\rho^2<0.
\]

The resident saddle is

\[
\boxed{
P_\rho=(n,x,y,u,v)=
\left(0,a_\rho,a_\rho,u_\rho,\frac{a_\rho}{\rho^2}\right).
}
\]

The zero-mass weak atom's angles here are incoming directions in the scaled/blown-up system, not identifiable parameters of a physical zero-mass neuron.

### Why the orbit is selected rather than fitted

Put \(P=\Phi(\rho a_\rho)\) and \(\alpha=\rho^2P/2\). The resident \((x,y)\) Jacobian is

\[
\begin{pmatrix}-\alpha&\alpha\\\alpha&-1/2\end{pmatrix},
\]

which is negative definite. The other two transverse eigenvalues are

\[
-\tfrac12[(u_\rho+a_\rho)\phi(u_\rho)+\rho^2],
\qquad -\rho^2/2.
\]

The weak-mass eigenvalue is \(+\rho^2\). Hence the saddle has a one-dimensional unstable manifold, with a unique positive-\(n\) branch up to time translation. Its local existence/uniqueness is the ordinary finite-dimensional unstable-manifold statement for this smooth vector field. Fix the translation by

\[
n(s)=\frac1{1+e^{-\rho^2s}},
\]

so \(s=0\) is weak half learning. This defines the candidate universal weak-learning orbit analytically.

**Unproved bridge:** the isotropic population flow has not yet been shown to select this orbit after the strong and weak escape stages. Nor has the supplied two-neuron initialization at \(0^\circ,120^\circ\) been analytically matched to it.

## 7. An invariant compensation-lag sign in the five-dimensional system

Define the scaled cluster-1 lag

\[
L=y+nK(u),\quad Q=\Phi(u),\quad g(u)=K(u)-u.
\]

For \(m=1\), \(r_{21}/q=L+o(1)\) in the compact-state expansion. Direct differentiation gives

\[
\boxed{
\begin{aligned}
L'={}&-\frac{1+nQ^2}{2}L
+\frac\rho2(1-n)K(\rho x)\\
&+\frac{n(1-n)}2
\left[\rho^2(K(u)+\phi(u))+Q\phi(u)\right]
+\frac{n^2}{2}g(u)Q^2.
\end{aligned}
}
\]

Every forcing term is nonnegative, and the total forcing is strictly positive at finite states for \(0<n<1\). The identity follows by substituting

\[
u'=\frac12[(1-n)(\phi(u)-\rho^2u)+ng(u)Q-LQ]
\]

into \(L'=y'+n'K(u)+nQ u'\). In simplifying, use

\[
\rho^2K(u)-\frac{\rho^2uQ}{2}
=\frac{\rho^2}{2}[K(u)+\phi(u)].
\]

The resident value is \(L=a_\rho>0\). A first-exit or integrating-factor argument proves

\[
\boxed{L(s)>0\text{ along the selected orbit at every finite time}.}
\]

The leading normalized cluster-1 probe rate is therefore

\[
\boxed{d_1:=\lim D_1/q^2=-\frac12(\zeta-x)L<0}
\]

whenever \(x<\zeta\). This is a dynamical sign law, not an instantaneous exact-compensation assumption.

The other leading cluster rate is

\[
\boxed{
d_2=\frac{\rho^2}{2}(x-y)
[nv-x+(1-n)y]\Phi(\rho x)
+\frac\rho2(\zeta-x)(1-n)K(\rho x).
}
\]

Exactly on the limiting orbit, \(\mathcal E_\zeta'=d_1+d_2\). The second term in \(d_2\) is weak-cluster-driven output rotation of the strong atom; it is not negligible solely because \(q\to0\). It becomes small when \(n\to1\).

## 8. Analytic reversal of the selected limiting orbit

### Proposition (limit-orbit reversal)

Fix \(0<\rho\le1/\sqrt2\). On the positive-\(n\) unstable branch of \(P_\rho\), for every \(\zeta>a_\rho\), the observable \(\mathcal E_\zeta\) decreases strictly at some finite early times and increases strictly at some later finite times before the first loss of strong-probe activation. There is a sign-changing zero of \(\mathcal E_\zeta'\) in the active phase with \(d_1<0<d_2\), and these individual cluster signs persist on a neighborhood of that zero.

This is a theorem about the analytically specified limiting orbit, not yet about isotropic initialization of the full population. It does not provide the numerical crossing time, uniqueness of the crossing, a numerical lower bound such as \(n\ge1/2\) at the crossover, or canonical finite-parameter constants.

### Proof, part 1: global forward existence and controlled growth

For \(s\ge s_0\), let

\[
R(s)=\max(|x|,|y|,|u|,|v|),\qquad \lambda=\rho^2.
\]

Use \(0<K(r)\le r_++\phi(0)\). At an active maximum of \(|x|\), the negative self term and convex combination of \(v,y\) give a nonpositive upper derivative. At an active maximum of \(|y|\) or \(|v|\), the derivative is at most \(\phi(0)/2\). For \(|u|\), it is at most

\[
\frac{1-n}{2}[\phi(0)+(1-\lambda)R].
\]

Hence

\[
D^+R\le \frac{\phi(0)}2+\frac{1-\lambda}{2}(1-n)R.
\]

Since \(1-n\) is integrable forward in time, Gronwall gives \(R(s)=O(1+s-s_0)\), precluding finite-time blowup. In particular, \((1-n)R\to0\).

### Proof, part 2: strict initial decrease on the positive weak branch

Expand the unstable manifold as

\[
x=a_\rho+Xn+O(n^2),\qquad y=a_\rho+Yn+O(n^2).
\]

Let \(a=a_\rho\), \(u_*=u_\rho\), \(P=\Phi(\rho a)\), \(\alpha=\lambda P/2\). The invariance equation gives

\[
\begin{pmatrix}\lambda+\alpha&-\alpha\\-\alpha&\lambda+1/2\end{pmatrix}
\begin{pmatrix}X\\Y\end{pmatrix}
=
\begin{pmatrix}a(1-\lambda)P/2\\-(a+K(u_*))/2\end{pmatrix}.
\]

Its determinant \(\Delta=(\lambda+\alpha)(\lambda+1/2)-\alpha^2\) is positive and

\[
Y=-\frac{\lambda}{4\Delta}
\left[(2+P)(a+K(u_*))-a(1-\lambda)P^2\right]<0.
\]

The inequality follows from \(K(u_*)>0\) and \((1-\lambda)P^2<1<2+P\). Therefore

\[
\mathcal E_\zeta'
=(x-y)x'+(\zeta-x)y'
=(\zeta-a)\lambda Y n+O(n^2)<0
\]

for small positive \(n\) and \(\zeta>a\). Also

\[
\lim_{s\to-\infty}\mathcal E_\zeta(s)
=-\frac12(\zeta-a)^2<0.
\]

### Proof, part 3: the strong input eventually reaches any finite scaled probe edge

First, \(v>0\) is invariant because at \(v=0\), \(v'=\rho K(\rho x)/2>0\).

Next \(v-y>0\) is invariant. At a possible first boundary \(v=y>0\),

\[
(v-y)'=\frac12[\rho nK(\rho x)+(1-\rho^2)y+nK(u)]>0.
\]

Likewise \(v-x>0\) is invariant. At \(v=x\),

\[
(v-x)'=\frac{\rho^2}{2}
\left[\frac{K(\rho x)}\rho-x+(1-n)(x-y)\Phi(\rho x)\right]>0,
\]

using the previous invariant and \(K(\rho x)-\rho x>0\). All three inequalities hold at the resident saddle and hence on its positive branch.

Suppose, for contradiction, that \(x(s)<\zeta\) for all later times. Then the stable linear equation for \(v\) bounds \(v\) above. Since \((1-n)y\to0\), the \(x\)-equation prevents \(x\) from tending to negative infinity: below a fixed negative barrier its bracket is positive for all sufficiently large times. Thus \(x\) lies eventually in a compact interval \([x_-,\zeta]\).

Put \(d=v-x>0\), \(P_x=\Phi(\rho x)\), and

\[
g_\rho(x)=K(\rho x)/\rho-x>0.
\]

Then

\[
d'=\frac{\rho^2}{2}
\left[g_\rho(x)-(1+P_x)d+(1-n)(v-y)P_x\right].
\]

The last term is nonnegative and \(g_\rho(x)\ge g_\rho(\zeta)>0\). Hence, since \(d>0\), comparison with a scalar linear equation gives an eventual strictly positive lower bound on \(d\). On the other hand, \((1-n)(v-y)\to0\). Therefore

\[
x'=\frac{\rho^2}{2}[d-(1-n)(v-y)]P_x
\]

has an eventual positive lower bound because \(P_x\ge\Phi(\rho x_-)>0\). This contradicts \(x<\zeta\). Thus a finite first hit \(x=\zeta\) occurs.

### Proof, part 4: reversal and exact cluster competition

At this first hit, \(\mathcal E_\zeta=0\). Earlier it is negative and, by part 2, strictly decreasing at some times. Consequently it has positive derivative at some later point before the hit. On the active interval the vector field and observable are analytic. Their derivative is not identically zero, so a sign-changing zero between a negative and a positive derivative can be selected. At that zero,

\[
d_2=-d_1>0
\]

because Section 7 gives \(d_1<0\). Continuity gives a neighborhood with \(d_1<0<d_2\), and shorter ordered subintervals with strictly negative and strictly positive total rates. This proves the proposition.

The mechanism includes a quantitative scaled rebound: the minimum is below \(-\frac12(\zeta-a)^2\), while the value at the first hit is zero. Before the gate itself, a late point can be chosen with rebound at least \(\frac14(\zeta-a)^2\). Transfer to finite noise should use interior witness times with a strict gate margin, not the closing-gate point itself.

For example, \(\rho\in[0.6,0.7]\) and \(\zeta\in[1,2]\) satisfy \(\zeta>a_\rho\). The proposition gives per-parameter existence, not a common numerical pair of time windows across that entire box. Strict witnesses at a selected pair persist on a local parameter/probe neighborhood by ordinary continuous dependence.

The weak mass is positive at every finite witness time. A useful explicit learning threshold (for instance, weak mass at least 1/2 near the crossover) still requires a quantitative estimate; it should not be inferred from the numerical 0.988 value.

## 9. The fully learned four-dimensional subsystem and the two Mills corridors

Setting \(m=n=1\) is an additional late-learning reduction, not a consequence of \(q\to0\) by itself. Put \(c=-y\). Then

\[
x'=\frac{\rho^2}{2}(v-x)\Phi(\rho x),\qquad
v'=\frac\rho2[K(\rho x)-\rho v],
\]

\[
u'=\frac12(c-u)\Phi(u),\qquad
c'=\frac12[K(u)-c].
\]

With \(X=\rho x,V=\rho v\), the first pair and the second pair have the same form, at different clock rates:

\[
r'=\frac\lambda2(z-r)\Phi(r),\qquad
z'=\frac\lambda2[K(r)-z].
\]

The region \(0\le r<z<K(r)\) is forward invariant. At \(z-r=0\), the gap derivative is \(\lambda[K(r)-r]/2>0\). At \(K(r)-z=0\), its derivative is \(\lambda\Phi(r)^2(z-r)/2>0\). Both coordinates increase inside the region, and they cannot converge to a finite equilibrium because that would require \(K(r)=r\).

These are genuinely dynamical versions of the Mills sign laws. They retain the output-compensation lag instead of setting it to zero.

In this subsystem,

\[
d_1=-\frac12(\zeta-x)[K(u)-c]<0,
\]

\[
d_2=\frac{\rho^2}{2}(x+c)(v-x)\Phi(\rho x)>0
\]

under the displayed corridor and \(\zeta>x\). The harmful contribution is entirely input rotation. A finite weak-learning error adds the terms retained in Sections 4 and 7.

## 10. Correct interpretation of the selected-residual formula

The general leading cluster-2 moment of the strong atom is

\[
\boxed{
\frac{T_{2,1}}q
=\rho(1-m)\phi(\rho x)
+\rho^2(nv-mx)\Phi(\rho x)+o(1).
}
\]

The full strong input velocity also includes the second-coordinate residual:

\[
\frac{b_s^\top R_2a_s^\perp}{q}
=\rho(1-m)\phi(\rho x)
+\rho^2[nv-mx+(1-n)y]\Phi(\rho x)+o(1).
\]

For \(m=n=1\), the moment becomes \(\rho^2(v-x)\Phi(\rho x)\). The Mills-only expression

\[
\rho[K(\rho x)-\rho x]\Phi(\rho x)
\]

requires the additional instantaneous substitution \(\rho v=K(\rho x)\). This is the weak output nullcline; it is not an invariant evolving compensation state when \(x'\ne0\). The uploaded `check_laws.py` prints the mass-retaining law and the Mills-nullcline law as separate columns.

Likewise, the weak cluster-1 driver has leading term

\[
\frac{b_w^\top R_1a_w^\perp}{q}
=(n-1)\phi(u)+[nu+my+(1-m)v]\Phi(u)+o(1).
\]

Dropping the \((1-n)\) terms near the weak-learning transition can lose the leading sign. The signs are consequences of the dynamically reached region, not automatic consequences of the positivity of \(K(r)-r\) at arbitrary states.

## 11. Independent numerical checks of the newly derived system

These checks use `two_neuron_limit.py`, not the uploaded `few_neuron.py` and not the continuum archive. The required `population_pilot.py` dependency is not present in the active local runtime, and no GitHub calls were made.

For \(\rho=2/3\), the resident saddle has

\[
a_\rho\simeq0.3512850353,\quad
u_\rho\simeq0.3443062179,\quad
v_\rho\simeq0.7903913293.
\]

Numerically approximating its positive weak branch from a large negative shifted time, with \(n(0)=1/2\), gives at the first detected up-crossing for \(\zeta=1.74532925199\):

| Quantity | Derived-limit integration |
|---|---:|
| \(s_{\rm rev}\), normalized time after weak half learning | 9.9106696884 |
| Physical delay for \(\mu_1=3\) | 1.1011855209 |
| Weak mass \(n\) | 0.9879282503 |
| Strong input \(x\) | 0.6367690892 |
| Strong output \(y\) | -0.6214330466 |
| Weak input offset \(u\) | 0.5221080674 |
| Weak output offset \(v\) | 0.8874855775 |
| Scaled error \(\mathcal E\) | -2.0092455817 |
| Scaled normalized \(d_1,d_2\) | -0.0460756010, +0.0460756010 |

No coefficient or entry state was fitted to the quoted crossing data. Nevertheless, finite-start approximation to the unstable branch and the ODE integration itself are numerical here. The analytic proof above does not rely on these decimal values.

The same code compares the six leading cluster-source equations against an independent conditional Gaussian quadrature at four fixed scaled states, for \(q=0.1,0.05,0.025,0.0125,0.00625\). All checked discrepancies decrease by approximately four when \(q\) is halved. The quadrature conditions on the receiving input projection; it integrates the orthogonal Gaussian analytically and truncates the remaining standard-normal diagnostic integral at 12 standard deviations. These are consistency tests, not certified error estimates or proof of global reduction.

## 12. What remains to prove for initialized Theorems A and B

### A. Condensation and phase selection

Prove that the aligned isotropic continuum, after an explicitly specified learning-time translation, approaches the appropriate two-atom trajectory. This must control the full relevant joint input/output angular measure and residual moments, not only a strong-family standard deviation or output plot.

The incoming two-atom orbit cannot be chosen solely to match a numerical reversal. The resident-saddle branch in Section 6 is an analytical candidate. Showing that the population actually selects it is the major unresolved step.

Early alignment is not enough: the proof must cover strong saturation, survival/amplification of a weak-learning population, and the selected later interaction. For fixed positive noise, the data are not orthogonal sample vectors and no training half-space has exactly zero Gaussian tail mass. Existing orthogonal-input or separated-class alignment results are templates, not direct theorems for this setting.

### B. Specify the order and strength of the limits

At fixed time, \(S_0\to0\) gives the zero solution rather than a learned orbit. Time must be recentered. A regular finite-time perturbation estimate in \(q\) does not automatically cover a delay of order \(\log(1/S_0)\); products such as \(q\log(1/S_0)\) or \(q^2\log(1/S_0)\) can matter depending on the actual remainder.

A defensible target is a sequential or explicitly coupled limit: for sufficiently small positive \(q\), choose \(S_0<S_*(q)\) so that the centered population approximation is sufficiently accurate in scaled observables, then transfer the limiting reversal. An alternative order requires its own matching argument.

### C. Uniform finite-noise and population-to-atom transfer

The signal scale is \(q^2\) in error/rates and \(q\) in probe angle. An unscaled \(o(1)\) approximation is not sufficient. Prove uniform approximation of the rescaled error and exact cluster rates on a fixed centered time interval, including a scaled gate margin \(\zeta-x\ge\delta>0\) at the witnesses and control of the remaining population.

Once those estimates are available, strict limiting signs persist by ordinary analytical stability, giving finite positive \(q,S_0\) reversals with rebound \(\ge c q^2\) and sector width \(\ge c_Iq\). This is not a computer-assisted proof route.

### D. Scope and canonical parameters

A theorem for sufficiently small \(q,S_0\) is not automatically the old canonical-parameter Theorem A. Unless proved constants include \(q=0.05,S_0=2\times10^{-4}\), describe it as an analytical small-noise/small-initialization theorem explaining the limiting mechanism. The canonical bridge cohort and its amplitude enhancement remain empirical finite-initialization phenomena until analytically controlled.

The observed approximately 1.1 physical-time delay is not a universal constant for all parameters. The theorem should have a limit \(\Delta(\rho,\zeta)/\mu_1^2\), with \(\Delta\) determined by the selected limiting orbit. Proving a simple or unique crossing and its quantitative timing is additional work.

## 13. Practical checks on the supplied scripts

- `few_neuron.py` correctly stores a per-atom mass \(m_i\) via log\((L m_i)\). Its tests pass `[S0/8,S0/8]`, whose total mass is \(S_0/4\), not \(S_0\). This does not itself invalidate event-centered comparisons, but it is not matched isotropic initialization.
- The two-atom runs initialize specified directions, typically \(0^\circ,120^\circ\); they are not a proof of isotropic condensation.
- `check_laws.py` reports \(T_{2,1}/q\), not raw \(T_{2,1}\). The quoted values near 0.07066 are scaled moments.
- `q_scaling.py` reparses angles from a two-decimal display string. At \(q=0.0125\), that can introduce about 0.007 uncertainty in a scaled angle. Use raw state columns for convergence claims.
- The default saved interval in `few_neuron.py` is \(2(0.05)/9\simeq0.01111\) physical time units. Its summary takes the first sampled positive total rate and first sampled weak response above one half. Use interpolation or root events before claiming higher clock precision.
- The three files do not by themselves include the continuum small-\(S_0\) sweep outputs. The plateau and condensation figures in the user's message remain reported numerical evidence, not independently reproduced by this note.

## 14. Literature boundary

Boursier, Pillaud-Vivien, and Flammarion, *Gradient flow dynamics of shallow ReLU networks for square loss and orthogonal inputs* (NeurIPS 2022), analyze orthogonal-input square-loss dynamics, including alignment and saddle-to-saddle behavior.

Min, Mallada, and Vidal, *Early Neuron Alignment in Two-layer ReLU Networks with Small Initialization* (arXiv:2307.12851; ICLR 2024), analyze binary classification with separation/correlation conditions.

These results motivate analytical techniques. Neither may be invoked as though it already proves two-atom condensation for vector-valued identity regression on overlapping Gaussian populations.

## 15. Next proof objective

The explicit limiting ODE and the analytic argument above should replace the trajectory-certificate plan. The next major objective is an initialized two-stage condensation/selection theorem that reaches this limiting orbit with a sufficiently strong, correctly scaled approximation. In parallel, turn the local Gaussian expansion into a uniform finite-noise lemma and quantify the limiting witness's weak-learning threshold and rate margins. Do not restart global numerical continuation.
