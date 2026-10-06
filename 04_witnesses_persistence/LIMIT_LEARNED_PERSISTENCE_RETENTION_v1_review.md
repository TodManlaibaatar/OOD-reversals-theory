# Review increment: learned limiting persistence and the retention interface

**Proof:** `LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex`  
**Reading copy:** `LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.pdf` (8 pages)  
**Label prefix:** `inc:LPR:v1:`  
**Status:** separate analytical work for independent review; not merged.

## 1. Scope and new results

This increment responds to the user's checked linear/persistence results and their three proposed extensions. The initialized Theorems A and B remain open. No GitHub access, numerical trajectory, interval arithmetic, Gaussian numerical quadrature, or pilot-derived sign is a premise.

| Result | Precise status |
|---|---|
| Theorem 2.1: common learned reversal and eventual zero benefit on the AN06 rectangle | Analytical corollary of the supplied AN06 and LP results, within the selected coherent leading system |
| Proposition 3.1: weak-coordinate divergence, square-root-logarithmic growth, and eventual positive input velocity | New analytical proof for the full five-dimensional selected orbit, retaining the weak-mass transient |
| Corollary 3.2: all four scaled angles are `O(sqrt(log(2+s)))` | Combines Proposition 3.1 with LP's strong-coordinate estimate |
| Lemma 4.1: damping of an explicitly perturbed saturated mass | Conditional scalar estimate; does not supply the actual finite-noise defect |
| Proposition 5.1: fixed-label retention from a mean negative-growth budget | Exact original-flow implication; obtaining a captured set and bounding the budget remain open |
| Proposition 6.1: positive passage exponent with a retained `S0^(1-rho^2)` seed | Conditional algebraic consequence of unproved entry and nonlinear passage estimates |

## 2. What is imported

- `THEOREM_A_ANALYTICAL_PROGRESS.tex`: selected branch, global forward growth, and exact leading equations.
- `LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex`: divergence of the strong input, finite total downward variation, `x=O(sqrt(log(2+s)))`, bounded `v-x`, and common clearing on compact parameter ranges.
- `AN06_learned_orbit_witnesses_v2.tex`: common learned source-sign and crossover windows on its analytically defined rectangle centered at `(rho,zeta)=(2/3,5*pi/9)`; smooth branch dependence; resident root estimate.
- `RELU_POPULATION_FOUNDATIONS_v2.tex`: exact original-flow positive-mass characteristic equation and its normalization.
- The scaled-population and AN02 notes supply scope and roadmap context, not missing capture estimates.

The combined statement does **not** enlarge AN06's rho range. Limiting permanence alone has the full `0<rho<1` range; learned common witnesses use the smaller AN06 rectangle. Leading weak mass is not silently renamed an exact finite-noise response or a measured empirical learning clock.

## 3. The new weak-coordinate proof

Write `c=-y`, `w=c-u`, `Q=Phi(u)`, and `r_n=1-n`. Exact rearrangement of the full selected system gives

\[
 u'=wQ/2+f,\qquad c'=(g(u)-w)/2-e,
\]

\[
 f=\frac{r_n}{2}[K(u)-\lambda u]\ge0,\quad
 e=\frac{r_n}{2}[K(u)+\rho K(\rho x)]\ge0,
\]

\[
 w'=g(u)/2-a(s)w-h,\qquad
 a=(1+Q)/2\in[1/2,1],\quad h=e+f.
\]

The imported linear growth implies `h <= C(1+s) exp(-lambda*s)`.

### Steps carrying the argument

1. `(w_-)' <= -w_-/2+h` gives integrable and bounded negative gap.
2. `(u')_- <= w_-/2` gives finite total downward variation and a finite lower bound on `u`.
3. The gap equation bounds positive `w` using that `g` is decreasing, so `|w|` is bounded.
4. If `u` were bounded above, `g(u)` would stay bounded below while `h` vanishes. The gap would then become bounded positively away from zero, forcing `u'` positively away from zero. Contradiction. Finite downward variation upgrades unboundedness to `u -> infinity`; bounded gap gives `c -> infinity`.
5. The corrected sum
   \[
   \widetilde W=u+c+\frac12\int_s^\infty w_-(t)\,dt
   \]
   satisfies `tilde W' <= g(u)/2` eventually. This avoids assuming the moving Mills corridor has already been reached.
6. Since `u >= (tilde W - constant)/2` and `g(u) <= phi(u)` for `u>=0`, integrating an exponential barrier gives the square-root-logarithmic upper bound.
7. `g(u) >= phi(u+2)` and the upper bound produce a polynomial positive lower forcing. Variation of constants shows that this beats the exponentially decaying negative initial term and `h`. Thus `w>0` and `u'>0` eventually.

No step sets `n=1`; no eventual membership in the fully learned Mills corridor is assumed. The first-exit argument in step 4 uses a *constant* positive gap threshold, not a moving barrier. The weak output `c` is proved to diverge with bounded separation from `u`; eventual positivity of `c'` is not asserted.

These are pointwise-in-rho estimates. The file does not claim numerically evaluated constants or a new uniform weak-growth theorem up to `rho=1`.

## 4. Horizon caveats

The all-angle growth result implies a **geometric** condition

\[
 q\sqrt{\log(2+T_q)}\longrightarrow0.
\]

It does not establish finite-noise trajectory fidelity to `T_q`, a remainder bound uniform in the growing chart radius, or background control. Geometrically one can allow `T_q=exp(q^-beta)` for `0<beta<2`, but this is not a valid approximation horizon without further dynamics.

If the only available accumulated error is `C q^2 T`, then `T` comparable to `q^-2` gives an order-one bound, not a vanishing bound. With that argument alone, `q^2 T_q -> 0` is needed, and growing chart constants can add logarithmic restrictions.

The total mass need not accumulate this error linearly: if `N >= n_* > 0` and

\[
 N'=\lambda N(1-N)+q^2r,
\]

then `N-1` has restoring coefficient `lambda N`; a bounded forcing leaves an `O(q^2)` error after the transient. Relative label weights and angular variables require their own analysis. No experimental horizon, such as physical time 44 or 100 at `q=.05`, is certified or ruled out here.

## 5. The retention interface and the actual open estimate

For a **fixed label set** C, use the original exact rate

\[
 r_\alpha=2b_\alpha^T R(\theta_\alpha)a_\alpha=(\log m_\alpha)'.
\]

The file defines the negative integrated-growth cost per label and averages it against the population's mass distribution at the initial time of the retention interval. Jensen gives

\[
 N_C(\tau_b)\ge N_C(\tau_a)\exp(-\overline B_C).
\]

The averaging measure is fixed at `tau_a`, not the evolving mass-normalized measure. The uniform labelwise version follows as a special case. The full residual field remains in `R`; no omitted population is set to zero.

What has **not** been proved is:

- which fixed labels are retained/captured;
- how much of the measured early weak-sector mass they contain;
- that they reach the bounded weak chart;
- a useful upper bound on `B_C` during that passage;
- compatible strong mean/shape and outside-population bounds.

A generic fixed-label lower mass bound is not a weak-capture theorem. An instantaneous angular-mask mass can lose labels by transport even when their individual radii grow.

## 6. The revised exponent inference

The user clarified that the empirical exponent near `0.576` is a direct weak-mask mass measurement at strong half-mass, not a clock regression. That correction is accepted. No clock-subtraction correction is applied to that measured quantity.

Conditional on a *retained* seed lower bound `N_ent >= c S0^(1-lambda)`, a same-entry-time strong shape upper bound `delta_ent <= C S0^(1/2-alpha)`, and the nonlinear passage inequality with amplification `N_ent^(-alpha/lambda)`, the resulting exponent is

\[
 \eta=\frac12-\alpha-(1-\lambda)\frac\alpha\lambda
 =\frac{1-\Phi(\rho a_\rho)}2>0.
\]

This is pointwise positive for every fixed `rho<1`, and uniformly positive on compact subintervals. On AN06's interval its stated resident bound gives `eta>97/500`.

The proof does not assert the three input estimates. In particular, the strong-stage contraction must not be counted twice by choosing different entry times for the seed and the shape. A capture loss `exp[-B_0-b log(1/S0)]` adds `b` to the seed exponent. Small errors in seed/shape exponents reduce the margin by the displayed explicit formula in Proposition 6.1. The actual nonlinear moving split coefficients and accumulated finite-noise error remain open.

The specific note containing the user's `G_infinity` bound was not located among the accessible source files; some earlier uploads are expired. This increment therefore **does not use or reinterpret that bound**. It uses the displayed resident rates and spells out its stronger entry assumptions instead. That note should be re-uploaded before its actual result is used.

## 7. Proposed integration after review

- Theorem 2.1 belongs after AN06's common witnesses, referring to LP for uniform clearing.
- Proposition 3.1 and Corollary 3.2 belong with LP's strong-coordinate growth results.
- Lemma 4.1 is a finite-noise-transfer planning tool, not completion of AN7.
- Proposition 5.1 belongs in the AN02 retention/capture work as an exact interface.
- Proposition 6.1 updates the conditional exponent ledger; it does not supersede AN02's proved conservative reservoir result or establish its much larger measured seed.

Do not modify or automatically include these results in the consolidated checkpoint. Independent proof review and explicit user approval are required.

## 8. Checks performed

The proof was reviewed algebraically from the displayed ODE. No new trajectory was integrated. The source was compiled twice after its final edit; the last compile had no warnings or overflowing boxes. All eight pages were rendered and inspected. SHA-256 checks confirm that the foundations, consolidated checkpoint, AN06 v2, and LP v1 were unchanged.

These checks are not formal machine verification and do not replace independent mathematical review of the new weak-coordinate proof.
