# AN06 v1 review note: learned limiting-orbit witnesses

## Status

**New proof increment for independent review.** The initialized Theorems A and B are **not proved**. This increment addresses the user's recommended first step: finish the learned witnesses and their robustness for the selected coherent limiting orbit before attempting coupled strong contraction and weak capture.

Deliverables:

- `AN06_learned_orbit_witnesses_v1.tex`: standalone proof, unique prefix `inc:AN06:v1:`.
- `AN06_learned_orbit_witnesses_v1.pdf`: compiled reading copy.
- This review note.

No source document or AN02 file was modified. Nothing was merged into the checkpoint. No GitHub access, numerical trajectory integration, saved-array comparison, or validated numerical continuation was used. LaTeX compilation and elementary exact-rational simplification were used for preparation; neither is a formal verification of the proof.

## 1. What is new

### 1.1 A quantitative half-learning descent theorem

For the selected coherent branch, uniformly on

\[
\rho\in[13/20,7/10],\qquad s\le0,\qquad n(s)=(1+e^{-\rho^2s})^{-1},
\]

Theorem 2.2 proves

\[
-n<y<a_\rho<2/5,\quad y<x<3/4,\quad 0<u<1,\quad 0<v<11/10.
\]

Define

\[
A=\rho K(\rho x),\quad L=y+nK(u),\quad T=L-(1-n)A=-2y'.
\]

It also proves

\[
T(s)\ge\frac5{62}n(s)(1-n(s)),\qquad y'(0)\le-\frac5{496}.
\]

This is not the old `Y_1<0` result only as `n -> 0`. It controls the branch all the way to weak half-mass.

Theorem 3.1 then proves

\[
\mathcal E'_\zeta(0)
\le-\frac{152833}{31000000}<-\frac1{250}
\qquad(\zeta\in[4,5]).
\]

The cancellation that makes this estimate useful is

\[
(x-y)x'=\frac\lambda2Pz[n(v-y)-z]
\le\frac{\lambda Pn^2(v-y)^2}{8},\quad z=x-y.
\]

Bounding `z` and `x'` separately would give a considerably poorer probe-offset requirement. No assumption that `x'` is positive is made.

### 1.2 A crossover after a fixed learning level

Corollary 3.2 combines the half-learning witness with the existing finite gate-hit proof. The error at half-mass is negative, and the error at the finite hit is zero. Thus a negative-to-positive zero occurs strictly after `s=0`, before the gate closes.

The selected common interval around that zero satisfies `n > 1/2` everywhere. The source signs `d_1 < 0 < d_2` hold on the entire interval, not merely at the zero. A simple or unique crossing is not assumed.

### 1.3 Common parameter/probe/time margins

Section 5 constructs a common interval `J`, ordered windows `J_-`, `J_+`, and a positive-width parameter rectangle around

\[
(\rho_c,\zeta_c)=(2/3,9/2).
\]

The window radius, source margin, total-rate margin, and parameter widths are defined by exact analytic functionals of the selected orbit. The proof shows those constants are positive and finite. Their numerical values are **not evaluated**.

The parameter rectangle is local; the proof does not claim common witness times over the entire `[13/20,7/10] × [4,5]` rectangle. Only the half-learning inequality is proved uniformly over that entire rectangle.

### 1.4 Explicit leading-population robustness

Section 4 derives the source rates for `M != 1`, retaining the strong reaction correction. It proves that the mass-weighted first-moment distance

\[
\begin{aligned}
\mathfrak d={}&|M-1|+|N-n_*|\\
&+\int(|x-X|+|y-Y_*|)\,d\mu_s
+\int(|u-U|+|v-V_*|)\,d\mu_w
\end{aligned}
\]

controls each leading source rate by

\[
|d_p-d_{p,*}|\le64R^2(1+g_0^{-1})\mathfrak d,
\]

provided both supports are inside `[-R,R]^2`, masses are at most two, and the coherent reference has scaled gate gap at least `g_0`.

This does not require every strong population label to be active. Gate mismatches, including labels exactly at the gate, are paid for with

\[
\mu_s\{x\ge\zeta\}\le\frac1{g_0}\int|x-X|\,d\mu_s.
\]

Section 6 specifies a positive tolerance `epsilon_*` which preserves the common source signs, total-rate windows, and mass margins. It yields a leading scaled rebound of at least `gamma_0 r / 4`.

### 1.5 Finite-window propagation and exact static learning

Proposition 7.1 proves, **conditional on the same compact chart class**, the coarse leading-system estimate

\[
\mathfrak d(s)\le e^{64R(s-a)}\mathfrak d(a).
\]

This is used only on the fixed witness interval. It is not an AN3 long-delay passage estimate.

Proposition 8.1 gives an exact Gaussian **state** estimate for a fully charted network:

\[
|\mathsf m_p-M_p|\le25qR,\qquad
\sqrt{2\mathcal L_p}\le|1-M_p|\sqrt{Q_p}+17qR.
\]

Combining it with the witness mass margins and its explicit small-`q` condition gives

\[
\mathsf m_1,\mathsf m_2\ge1/2,\qquad
\mathcal L_p\le(25/36)\mathcal L_p(0).
\]

This prevents the interpretation of mass as learning without an observable comparison. It does not establish that an initialized finite-noise trajectory has reached such a state, or that its exact rates track the leading rates.

## 2. Proof contract and dependencies

| Result | Assumptions | Conclusion | Status |
|---|---|---|---|
| Lemma 2.1 | Selected resident roots; ratio in `[13/20,7/10]` | `a < phi(0)`, `0 < u_* < 1` | Defined limiting-system result |
| Theorem 2.2 | Selected coherent branch, `s <= 0` | Coupled invariant region and quantitative `T` lower bound | Defined limiting-system result |
| Theorem 3.1 | Same branch; scaled offset in `[4,5]` | Negative total rate at weak half-mass | Defined limiting-system result |
| Corollary 3.2 | Above plus imported global continuation/gate hit | Crossover strictly after half-mass | Defined limiting-system result |
| Lemma 4.1 | General leading population with reaction and characteristic chain rule | Source rates including `1-M` correction | Leading-system identity |
| Proposition 4.2 | Compact chart supports, bounded masses, coherent reference gate gap | Explicit first-moment rate and observable errors | Conditional leading-state estimate |
| Lemma 5.1 | Selected branch and uniform resident hyperbolicity on compact ratio interval | Smooth parameter dependence | Finite-dimensional result |
| Theorem 5.2 | Analytically defined local rectangle | Common learned mass, source, gate, and total-rate margins | Selected-orbit result |
| Theorem 6.1 | Population distance at most `epsilon_*` on `J`, compact charts | Common population margins and scaled rebound | Conditional leading-flow result |
| Proposition 7.1 | Common compact chart class throughout a finite interval | Gronwall bound for the weighted distance | Conditional leading-flow result |
| Proposition 8.1 | Entire exact state charted, bounded masses/support, small positive `q` | Exact response and cluster-loss inequalities | Conditional static original-model result |

The working checkpoint dependencies are `pa:branch`, `pa:weakroot`, `pa:atomiclag`, `pa:atomicrates`, `pa:limitreversal`, `pa:leading`, `pa:masslaws`, and the initialization identity `f_0(X)=S_0 X/4`. The new file restates the needed equations. It does not import initialized selection, condensation, chart entry, or any empirical coefficient.

## 3. Audit points

### 3.1 The first-exit argument is simultaneous

The signs of `T`, `x-y`, and the weak coordinate `u` are closed together; none is assumed globally in order to prove itself.

The resident expansion starts `T>0` and `x-y>0`. The latter follows from

\[
(\lambda+\alpha)(X_1-Y_1)
=\alpha(a/\lambda-a)-\lambda Y_1>0.
\]

The bound `y <= a` is obtained by integrating `y'=-T/2`, not by incorrectly assigning an independent sign to its vector field at `y=a` for arbitrary states.

At `x-y=0`, the imported invariant `v>y` and `T>=0` point strictly inward. At `u=0`, the bound `a<phi(0)` matters. At `u=1`, the lower bound `y>=-n` matters. The lower `y=-n` boundary uses the derivative of the moving boundary, namely `y'+n'`.

### 3.2 Forcing and rational constants

The exact `T` identity is equation (2.6). Its coefficient `lambda-Q^2/2` is at least `7/400`, so discarding that term preserves a lower bound.

The remaining forcing constant is exactly

\[
\frac{27902493}{250000000}>\frac1{10}.
\]

The estimate uses `P<=71/100`, `Q in [1/2,9/10]`, `v-y<=8/5`, `K(u)+phi(u)>=3/4`, and `Q phi(u)/2>=1/20`. All hold on the simultaneous region.

Replacing the damping by `-3T/4` is justified only because `T>=0`, which is retained as part of the bootstrap. At its boundary the positive forcing excludes exit.

### 3.3 Integration from minus infinity

The selected branch supplies `T=O(n)` at the resident end. The integrating-factor initial term tends to zero and has nonnegative sign. The comparison

\[
n(t)(1-n(t))\ge n(s)(1-n(s))e^{-\lambda(s-t)}
\]

uses both `n'/n<=lambda` and monotonicity of `n`. No interchange of an unbounded signed integral is needed.

### 3.4 Crossover and uniformity

The first transition to positive total rate occurs strictly inside the active interval, after zero. Analyticity gives a finite odd multiplicity, not necessarily multiplicity one. The Taylor radius explicitly retains this multiplicity.

The common-parameter interval uses bounded derivatives of the **analytically selected branch**, not a generic arbitrary orbit whose initialization might change with the parameter. Lemma 5.1 gives a local contraction argument in the mass coordinate and continuation at the fixed logistic phase.

The constants defining the parameter interval are implicit analytic orbit functionals. Their positivity is proved, but the file does not claim rational/numerical side lengths or canonical coverage.

### 3.5 Rate stability and probe gates

The strong reaction correction must not be omitted when `M != 1`. The exact leading formula is equation (4.2).

The metric is mass-weighted and unnormalized, and explicitly includes mass differences. The gate estimate includes `x=zeta` in the mismatch set. There is no assumed bounded projected density or assumption that the population's input-angle map is monotone.

At gate atoms, rates are defined with the displayed selector. The total positive-part chain rule holds almost everywhere along compact regular characteristics. No pointwise exact finite-noise source transfer at such atoms is asserted.

### 3.6 Compact charts and omitted population

Compact support is a genuine hypothesis in the robustness and propagation statements. A small first moment alone does not force compact support. The theorem can permit a small inactive tail **inside** the compact strong chart, but it does not cover an uncharted population with arbitrary scaled coordinates.

No part of this increment proves that third/fourth-quadrant labels, early weak pass-through labels, or the canonical inactive bridge meet the error budget.

### 3.7 Static exact learning

The static estimate compares the full charted network with `M X_1 e_1` on cluster 1 and `N X_2 e_2` on cluster 2. It keeps the unused target-coordinate error and bounds negative Gaussian tails by `q|Z|`; it does not set a Gaussian gate tail to zero.

The initial loss in the comparison is the exact isotropic initial loss, not the zero-output loss. The loss ratio uses `S_0<=1` explicitly. The proposition is a static implication and cannot replace AN7.

## 4. Scope changes and open residue

The concrete offset interval `[4,5]` is a deliberate restriction. The new half-learning proof **does not establish the same bound at the canonical scaled offset near 1.745**. It is useful for an existence theorem in a small-noise regime, not a canonical theorem.

The next initialized targets still are coupled strong contraction and weak capture, followed by nonlinear resident passage with quantitatively useful entry laws. Their output should control the masses, both angular means and fluctuations, and the outside-population contribution strongly enough to meet the explicit witness tolerance. The coarse finite-window Gronwall exponent must not be substituted for the competing resident rates.

The exact finite-noise derivative transfer and its `q^2`-scale error budget are also still open. The static learning proposition only closes the interpretation of a sufficiently close, fully charted state.

The Riccati refinement proposed in review point A remains unproved here. AN02 v1 remains unchanged. Its cohort definition is independent of `R`; that clarification and the notation cleanup can be incorporated into a separately approved future AN02 revision. The bulk-versus-reservoir distinction remains important for canonical-facing capture.

### Joint-scaling correction

The review's statement that `q^2 log(1/S_0) -> 0` forces the reservoir regime needs an additional condition. It does not even imply the proposed timing inequality `log(delta/S_0) >= (2/lambda) log(1/q)`.

At `rho=2/3`, choosing `S_0=q^3` gives both `q^2 log(1/S_0)->0` and `S_0/q^2->0`, but the logarithmic timing ratio tends to `3`, below `2/lambda=9/2`.

A compatible stronger scale separation is

\[
\log(1/S_0)/\log(1/q)\to\infty,
\qquad q^2\log(1/S_0)\to0,
\]

for example `S_0=exp(-1/q)`. This is a correction to the parameter planning, not a new proof that such a sequence is captured or that the heuristic reservoir crossover formula has already been established.

## 5. Proposed integration after review and explicit approval

Insert the half-learning region and descent theorem after `pa:limitreversal`; update its learning-witness limitation only for the proved probe range. Keep the original general-ratio selected-orbit reversal statement intact.

Place the general leading-rate identity, quantitative gate-aware tolerance, common-window construction, and finite-window propagation as conditional AN3/AN6/AN8 interfaces. The static Gaussian learning estimate belongs with AN5.

Do not mark AN2, AN3, AN7, Theorem A, or Theorem B complete. Do not automatically include this file in the checkpoint.
