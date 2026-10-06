# AN02 v1 review: initialized weak-side arrival

**Date:** October 2, 2026  
**Proof:** `AN02_weak_side_arrival_v1.tex`  
**Compiled reading copy:** `AN02_weak_side_arrival_v1.pdf` (8 pages)  
**Label prefix:** `inc:AN02:arrival:v1:`  
**Review status:** Proof supplied and internally checked; independent mathematical review and integration approval are pending. No existing theory source was modified.

## 1. What is new

The new result is a quantitative **incoming weak-side reservoir in the original, positive-noise population flow**, starting from the prescribed uniform aligned-balanced initialization. It does not start from a weak atom or a learned state.

For

\[
\frac35\le\rho\le\frac34,\qquad 0<q\le\frac1{20},\qquad
0<S_0<\delta\le\frac1{100},
\]

let

\[
a_* = \frac12+q^2,\qquad
T_\delta=\frac{\log(\delta/S_0)}{1+2q^2}.
\]

There is an initial-label interval \(C_{T_\delta}\), defined analytically from the parameters before following the nonlinear flow, such that at \(T_\delta\)

\[
\theta,\psi\in[7\pi/12,5\pi/6],\qquad
m(\alpha)\ge e^{-4\delta}S_0\quad(\alpha\in C_{T_\delta}),
\]

and

\[
\boxed{
M_{\rm in}:=\int_{C_{T_\delta}}m_{T_\delta}\,d\lambda_0
\ge\frac q{3000}S_0\left(\frac{S_0}{\delta}\right)^{1/16}.}
\]

The sharper estimate is

\[
M_{\rm in}\ge
\frac{\rho qK(-R)}{72a_*}e^{-4\delta}
S_0\left(\frac{S_0}{\delta}\right)^{\varepsilon_R},
\]

where \(R\ge1\), \(qR\le\rho^2/2\), and

\[
\begin{aligned}
\kappa_R&=\frac12\left[
(1+2q^2)\Phi\!\left(-\frac1{2q}\right)
+(\rho^2+2q^2)\Phi(-R)\right],\\
\varepsilon_R&=\frac{\kappa_R}{1+2q^2}.
\end{aligned}
\]

The main advance is the **backward angular-compression estimate**. A global bound \(|v_0'|\le a_*\) would cost a factor \((S_0/\delta)^{1/2}\) in initial-label length. The new argument uses a tail-localized, one-sided bound on \(v_0'\), plus an exact scalar-flow speed ratio. This replaces the exponent \(1/2\) by \(\varepsilon_R\), while retaining the \(qK(-R)\) prefactor. For \(R=1\), \(\varepsilon_1<1/16\).

The exact early comparison is imported, not claimed as new. The backward-transport estimates, their quantitative initialized mass consequence, and the cohort-specific observable bounds are the new statements.

## 2. Proof contract and dependencies

### Original-flow contract

The distributions, loss, normalized time, initialization, and untied balanced dynamics are exactly those in the handoff. The label probability measure is \(\lambda_0(d\alpha)=d\alpha/(2\pi)\); \(\lambda=\rho^2\) is a different, scalar quantity. Population mass includes the squared radius.

The proof assumes only the displayed parameter restrictions and the supplied original-flow existence and early-comparison results. It has **no learned-state, capture, small-shape, coherent-population, or source-sign hypothesis**.

### Imported results

| Source | Dependency | Use |
|---|---|---|
| `RELU_POPULATION_FOUNDATIONS_v2.tex` | P1–P2; labels `proposition-p1-exact-gradient-field-and-balance`, `proposition-p2-exact-angular-state-and-transportreaction-flow` | Exact untied balanced characteristic equations and population representation. |
| Same | P4, formula (6.7); label `proposition-p4-exact-one-dimensional-gaussian-calculus` | Exact Gaussian feature expectation; angular field and partial-response calculations. |
| Same | P5; label `proposition-p5-global-characteristic-existence-dissipation-and-bounds` | Global positive-mass characteristic solution and finite-horizon integrability. |
| `THEOREM_A_ANALYTICAL_PROGRESS.tex` | `pa:setup`, `pa:earlybounds`, `pa:targetcomparison` | Normalization, total-mass envelope, alignment control, and target-only comparison. The needed estimates are restated and verified in Lemma 2.1. |
| `THEORY_HANDOFF_ANALYTICAL_A_B.md` | AN2–AN3 contracts | The distinction between incoming mass and a captured weak seed; the required later seed/shape interface. |

### New statements and status

All labels below have prefix `inc:AN02:arrival:v1:`.

| Statement | Label suffix | Status and scope |
|---|---|---|
| Theorem 1.1: initialized incoming mass and angular sector | `main` | Exact original-flow result under the stated parameters; proof supplied. |
| Lemma 2.1: early target-only comparison | `comparison` | Imported exact estimate, rechecked here; not a new theorem. |
| Lemma 3.1: upstream barrier, speed bound, tail-curvature bound | `barrier` | Exact result for the explicitly defined analytical target-only field. No limiting-system approximation. |
| Lemma 3.2: backward Jacobian and label length | `jacobian` | Exact scalar comparison-flow result, used to construct fixed initial labels. |
| Proposition 4.1: rational uniform constants | `rational` | Analytic bounds from elementary Gaussian and exponential inequalities. |
| Proposition 5.1: partial weak response, strong-tail output, and probe inactivity | `observables` | Exact original-flow statements at the single time \(T_\delta\). |
| Equations (6.1)–(6.2): later capture and scaled chart | `openmass`, `openchart` | Unproved next targets, not hypotheses smuggled into Theorem 1.1. |
| Conditional use of the seed exponent in AN3 | Section 6 | Future implication only, contingent on capture and nonlinear passage. |

## 3. The construction and its central estimate

Let \(\varphi_\tau\) be the scalar flow of

\[
\widehat\theta'=v_0(\widehat\theta),\qquad
v_0(\theta)=\frac q2\left[
-\sin\theta\,K(\cos\theta/q)
+\rho\cos\theta\,K(\rho\sin\theta/q)\right].
\]

Define

\[
I=[2\pi/3,3\pi/4],\qquad C_T=\varphi_{-T}(I).
\]

For a fixed terminal time \(T\), this is a fixed initial-label interval. It depends on the parameters and analytical reference, not on an observed specialization or the actual trained endpoint. The proof never differentiates the true cohort mass while changing \(T\) in its label definition.

Set

\[
\beta=\pi+\arcsin(qR/\rho),\quad B=4\pi/3,\quad
b_R=\rho qK(-R)/6.
\]

The proof establishes \(-v_0\ge b_R\) on \([2\pi/3,\beta]\), \(v_0'\le\kappa_R\) on \([\beta,B]\), and \(v_0(B)>0\). A first equilibrium \(\theta_*\in(\beta,B)\) bounds the backward characteristic. Neither a unique equilibrium nor its hyperbolicity is assumed.

With \(w=-v_0\), the exact Jacobian is

\[
\partial_\theta\varphi_{-T}(\theta)
=\frac{w(\varphi_{-T}(\theta))}{w(\theta)}.
\]

The faster portion of the backward path costs only a speed ratio. Once it crosses \(\beta\), the logarithm of the numerator decreases at rate at most \(\kappa_R\). Since \(w(\theta)\le a_*/2\),

\[
\partial_\theta\varphi_{-T}(\theta)
\ge\frac{\rho qK(-R)}{3a_*}e^{-\kappa_RT},
\qquad
\lambda_0(C_T)\ge\frac{\rho qK(-R)}{72a_*}e^{-\kappa_RT}.
\]

The original-flow comparison then gives the mass and angular conclusions. Every population label remains in the residual matrix used by that comparison.

## 4. Audit points

### Time and first-exit conditions

\(T_\delta\) is an **upper-envelope time**, not a hitting time of the actual mass. Throughout \([0,T_\delta]\), \(\overline S\le\delta\), so the alignment first-exit guard \(\epsilon_{\rm al}<\pi\) closes analytically. At the endpoint, \(H\le2\delta\) and \(H+\epsilon_{\rm al}\le3\delta<\pi/12\). Nothing in the proof extends this comparison to the learned competition window.

### Sign direction in the tail estimate

The estimate is \(v_0'\le\kappa_R\), **not** \(|v_0'|\le\kappa_R\). For the backward equation \(\chi'=w(\chi)\),

\[
\frac d{dT}\log w(\chi)=-v_0'(\chi)\ge-\kappa_R.
\]

The sign reversal is essential to the lower Jacobian bound.

### Gaussian gate differentiation

The identity \(A_\theta'a_\theta=0\) follows because the boundary term contains \(X^Ta_\theta=0\). Positive noise gives smooth Gaussian angular integrals. The proof uses this identity before estimating \(v_0'\); it does not differentiate an unintegrated discontinuous gate as an ordinary smooth function. The trace estimate retains the signed truncated-Gaussian term before dropping it in a valid upper bound.

### Every division and boundary

The mass logarithms use positive masses supplied by original-flow existence. \(q\), \(a_*\), and \(K(-R)\) are strictly positive. The speed ratio and \(\log w\) are used only below \(\theta_*\), where \(w>0\). Smooth uniqueness prevents a finite-time hit of that equilibrium. The backward characteristic crosses \(\beta\) at most once because it is strictly increasing. No estimate divides by \(v_0\) at a root.

### Labels and possible folds

Only the scalar analytical comparison map is used as a diffeomorphism. No monotonicity or bounded projected density is assumed for the true input-angle map. The cohort is integrated against initial labels, not a projected angular density. The interval lies in a single real lift below \(4\pi/3\), so no wrap-around or duplicate labels enter the length calculation.

### Normalization

The factor \(1/2\) for the equal training mixture is present in \(v_0\) and \(\kappa_R\). The label interval has probability \(|I|/(2\pi)=1/24\). These factors give the denominator \(72a_*\). The time is normalized time; physical time is \(T_\delta/\mu_1^2\). No width factor is added.

### Integrals and limit exchanges

All flow arguments are at finite times for fixed positive parameters. There is no passage to a weak, zero-noise, zero-initialization, or infinite-time limit inside an integral. Gaussian moments and finite-time mass bounds justify the displayed feature integrals and Minkowski estimate. The statements are parameter-uniform inequalities, but do not constitute a learned-regime joint-limit theorem.

### Exact observable scope

The partial weak response satisfies \(\mathsf m_{2,C}\ge M_{\rm in}/5\). This is not a full-population lower bound: omitted labels need not contribute positively. The cohort has strictly positive Gaussian leakage onto cluster 1, with an explicit upper bound; it is not exactly frozen or isolated. Positivity of that partial mean leakage is not positivity of the full compensation lag or a helpful source rate. Fourth-quadrant probe inactivity is proved only at \(T_\delta\).

### Constants and small-parameter dependence

The rational simplification uses

\[
\varepsilon_1\le149/2560<1/16,
\qquad
\frac{\rho e^{-4\delta}K(-1)}{72a_*}\ge1/2680>1/3000.
\]

The sharper estimate keeps both \(qK(-R)\) and the positive-noise contribution \(\Phi(-1/(2q))\) to the exponent. Raising \(R\) improves the exponent at a prefactor cost. Neither factor should be omitted in later joint scalings. The angular comparison error is \(O(\delta)\), not automatically \(O(q)\).

## 5. Exact open residue

The result supplies an incoming cohort with positive weak response, low strong-cluster exposure, and explicit mass. It **does not supply the captured weak seed \(N_{\rm ent}\)** needed by AN3.

A possible next capture lemma would prove an analytically defined later time \(T_{\rm ent}\) and a subcohort \(C_{\rm cap}\subset C_{T_\delta}\) with

\[
\int_{C_{\rm cap}}m_{T_{\rm ent}}\,d\lambda_0
\ge c_{\rm cap}M_{\rm in},
\]

and

\[
\left|\frac{\pi/2-\theta_{T_{\rm ent}}}{q}\right|
+\left|\frac{\psi_{T_{\rm ent}}-\pi/2}{q}\right|
\le R_w
\quad\text{on }C_{\rm cap}.
\]

It must simultaneously establish strong learning, its centered shape bounds, and control of the background residual. The constants must have quantitatively useful dependence on \(q,S_0\). The present cohort has angles a fixed distance above \(\pi/2\), so it cannot already be inserted into the bounded weak chart.

Only if later capture loses no additional adverse initialization power could \(1+\varepsilon_R\), or conservatively \(17/16\), become a useful seed exponent. A true strong-shape bound and nonlinear passage would still be required to test

\[
\beta_{\rm shape}-(1+\varepsilon_R)\alpha_{\rm sh}/\lambda>0.
\]

No value of \(\beta_{\rm shape}\), capture fraction, canonical late-time margin, or phase boundary is proved by this increment. No exact finite-noise lag positivity, harmful selected-residual sign, crossover, or quantitative late rebound is claimed.

### Shortcuts explicitly not used

A global Jacobian Gronwall estimate produces a valid but much weaker initialization exponent; it does not address the intended quantitative passage problem as effectively. Conversely, extending the early comparison until strong saturation, calling a positive mass a learned weak concept, or identifying incoming mass with a captured seed would be unjustified. These gaps are preserved rather than converted into additional final hypotheses.

## 6. Proposed integration location

After independent review and explicit user approval, insert the accepted new transport lemmas and initialized reservoir theorem after `pa:targetcomparison`, in the early-escape/AN2 portion of a new checkpoint. The cohort-observable proposition can immediately follow the new theorem. Existing early estimates remain valid and are not superseded.

Keep the later capture interface in the open-obligations ledger. Do not mark AN2, AN3, A, or B complete. No consolidation or automatic `\input` is proposed before approval; an eventual merge needs its own changelog and label map.

## 7. Checks performed

The LaTeX source compiled twice with `pdflatex`, with no remaining warnings, undefined references, or overfull-box messages. The eight-page PDF was rendered; all-page layout and the main theorem page were visually inspected. Exact rational arithmetic checks verified the displayed exponent bound, prefactor, weak-response coefficient, and exponential-series bounds.

These are writing and arithmetic checks, not a machine-checked proof or independent mathematical review. No training trajectory, saved-array continuation, numerical Gaussian quadrature, interval certificate, or repository access was used. The analytical arguments, including the Gaussian inequalities, are displayed in the proof.

The four protected source hashes were checked before and after the work and match. Their values are recorded below.

```text
eefd557e0c725c87ea6b41d0d144b92e14f895f0b7f0095d509915b14a9de3f1  RELU_POPULATION_FOUNDATIONS_v2.tex
b9b169764339017da37209eca84f17154b73c1a2de79d61c707cf2f550763e1b  THEOREM_A_ANALYTICAL_PROGRESS.tex
71aae8f7a313f0c550718cd5741df6da05b2ad85421c7feedd20a24b3bfbda92  main-15.tex
cf3bd493c05c74b1aa4051c5685559a31fffcb5e6e28a6ddc05690438c6d0e86  main-appendix-frozen-theory-selfcontained.tex
```
