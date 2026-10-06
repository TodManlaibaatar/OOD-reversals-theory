# AN03 bulk clock and secondary Q2 energy — review note v1

## New advance

This increment separates the **clock cohort** from the **output-producing population**. It proves a concrete target-only bulk-subcohort seed and angular margin, integrates the secondary tail against the same proposed capped mass gain used for the strong complement, and derives a Cartesian transverse-energy propagation estimate that permits the unavoidable regenerated weak-chart energy.

The preceding sources, reviews, foundations, and checkpoint are unchanged. This file is not an initialized Theorem A claim or a merge instruction.

The quantitative conclusions are:

1. With the fixed initial-label clock set `C_q = {alpha in Q2: -cos(alpha) >= q^(1/4)}`, the target-only flow at `S0=q^10`, `T=10 log(1/q)` has `H_Cq(T) ≍ q^[10(1−lambda)]` and `sin(theta)/q >= c q^(−1/8)` from each crossing until T.
2. A conditional original-flow ratio bootstrap closes the bulk input gate margin and bounds every subinterval clock defect by `C[q^(1/8)+q^2 log(1/q)]`, from Cartesian entry ratios, bounded cross residual norms in q units, and an integrated R11 bound. It also controls relative amplitudes of fixed bulk subsets.
3. Under transferred joint entry profile, pre-exit distance control, and the proposed capped radial-gain bound with exponent `1+nu`, secondary Q2 energy is bounded by `C[q^5 + q^Gamma_nu H]`, where `Gamma_nu = gamma − nu[10(1−lambda)−2] >= 289169/924000 > 3/10` for `0 <= nu <= 1/100`. H is the separate bulk-clock amplitude.
4. Given explicit residual-entry bounds, an entry transverse bound `J_G(t0) <= Cq^3` propagates to `J_G(t) <= C[q^3 + q^(2+sigma)H(t)]` when `E_G <= C[q^5 + q^sigma H]`. The resulting forcing is `C[q^3 + q^sigma H + q^((1+sigma)/2)sqrt(H)]`, with its displayed clock integral. No clock-defect estimate for the entire output cohort is used.

The radial-gain and initialized Cartesian entry/residual-norm hypotheses remain unproved. The new clock theorem derives, rather than assumes, the bulk defect once those original-field inputs are supplied. The energy-from-gain proposition is an implication from those dynamical inputs, not their verification.

## Statements and labels

All labels have prefix `inc:AN03:bulkclock:v1:`.

| Label suffix | Statement | Scope |
|---|---|---|
| `cohortchange`, `ratioidentity` | Difference of aggregate clock defects equals the change of the logarithmic amplitude ratio | Exact original-flow identity for fixed cohorts |
| `floormodel` | Explicit logarithmic defect in a frozen-floor plus exponentially growing bulk model | Exact scalar calculation; not an original-flow saturation theorem |
| `bulkseed`, `gap`, `pointseed` | Fixed q^(1/4) cutoff has a bulk seed and a polynomial projected margin from the strong chart | Exact positive-noise target-only comparison |
| `middleband`, `twobulks` | A non-clock, non-captured initial band has relative target-only weak energy of order q^(1/4) | Comparison result |
| `bulkclockclosure`, `bulkentryratios`, `bulkdefectconclusion` | Cartesian ratio bootstrap closes the input gate margin and gives an o(1) bulk subinterval defect | Conditional original-flow theorem from residual norms and entry ratios |
| `bulkweights` | Relative amplitudes of fixed subsets satisfying the bulk bootstrap retain their entry ratios up to exp(o(1)) | Conditional original-flow transport |
| `moments` | Truncated secondary tail has moments of order q^3 h1^p2 above its tail index | Measure-theoretic implication; source target-only profile supplies this law |
| `gainenergy`, `labelenergy` | Pre-exit joint-distance and capped mass-gain inputs imply a weak-coordinate energy bound before and after exit | Conditional original-flow estimate |
| `secondary`, `secondarydetail`, `gammamargin` | Secondary energy relative to a separate bulk clock, retaining the gain-power loss | Conditional implication and exact rational algebra |
| `weakJ` | Bounded weak-chart coordinates generate transverse energy of order q^2 times weak energy | Static original-state expansion |
| `transverse`, `jineq` | Square-root transverse energy satisfies a residual-entry differential inequality | Exact original-flow inequality |
| `forcing`, `Jprop`, `Fpoint`, `Fintegral` | Propagated transverse energy and integrated output pressure using another cohort's clock | Conditional original-flow theorem |
| `residualinputs` | Sufficient L2 residual norms for the required off-diagonal and integrated diagonal matrix bounds | Exact original-state inequalities; dynamical norm bounds remain inputs |

## 1. Clock correction and its exact scope

For disjoint fixed cohorts C and S,

\[
\int_s^t(\varepsilon_{C\cup S}-\varepsilon_C)
=\log\frac{1+H_S(t)/H_C(t)}{1+H_S(s)/H_C(s)}.
\]

The response clock I is the same for both. This identity requires only positivity of H_C and the exact aggregate clock equation; it does not divide by an individual label amplitude.

In the scalar model H_C=b exp(I), H_S=a, the union has defect

\[
\int_{t_0}^t\varepsilon_{C\cup S}
=\log\frac{a e^{-I(t)}+b}{a+b}.
\]

With a comparable to q^5 and b comparable to q^k, this loses `(k−5)log(1/q)` once the growing component becomes comparable. At k=10(1−lambda), k−5 ranges from 1/10 to 31/40. The endpoint passage multiplier is exactly invariant after including the actual defect. A naive full-cohort forcing estimate charging exp(D_osc) can lose a negative q power.

The target-only entry energy theorem alone does **not** prove that the trained original-flow captured strip subsequently freezes, or that the bulk defect is two-sided O(1). The source explicitly distinguishes the exact cohort identity from that proposed dynamical mechanism.

## 2. The clock cohort and the intermediate primary band

The concrete choice gamma'=1/4 is uniform because gamma >= 6481/18480 > 7/20. For every cutoff-cohort label after crossing,

\[
q\cot\widehat\theta\le C q^{\delta(\lambda)},\qquad
\delta(\lambda)=5\lambda-15/4+3/(4\lambda),
\]

with `1861/13520 <= delta <= 113/490`. The proof uses the exact uniform Q2 crossing formula and the post-crossing first-coordinate estimate from Q2E, not an interior crossing asymptotic at the negative strong-axis endpoint. The projected margin makes the post-crossing extra U2 logarithmic rate integrable with vanishing error. Crossing-layer effects remain bounded multiplicative factors.

The band `q^(1/4)/2 <= c0 < q^(1/4)` lies outside the clock set and is not in the strong chart at entry. Its target-only weak energy is comparable to `q^[k+1/4]`, while the clock's is comparable to q^k.

Therefore “primary bulk energy” and “clock-subcohort energy” should be named separately. If the latter is used as the former, the secondary-tail q^gamma estimate does not account for all omitted labels. At the entry clock the extra band is hidden below the q^5 floor; its later primary growth must still be transported or included in a larger primary-bulk definition. This increment does not claim a later original-flow lower bound for that band from its entry size alone.

## 3. The original-flow bulk clock no longer needs to be assumed separately

For each bulk label use

\[
z=(U_2+W_2)/2,\quad a=(U_2-W_2)/2,\quad
j=\sqrt{(U_1^2+W_1^2)/2},\quad x=qj/z,\quad y=|a|/z.
\]

The required entry ratios are `z0>0`, `y0<=1/4`, `x0<=C0 q^eta`, with `0<eta<1`. The target-only cutoff has eta=1/8, but an original-flow relative Cartesian transfer is needed to use it.

The field inputs are bounded diagonal residual norms, `O(q)` cross residual norms, `0<=c<=c_b<1`, a logarithmic horizon, and a bounded integral of the cohort supremum of `|R11|`. The cross norms imply `|R12|,|R21|<=Lq`. On a positive-input gate guard,

\[
|R_{22}-Q(1-c)/2|\le Cq^2+C\exp[-\rho^2 a_{\theta,2}^2/(8q^2)].
\]

The proof uses the guards `x<X_q=O(q^eta)`, `y<1/2`, and `z>0` to get `a_{theta,2}/q>=c q^(−eta)`. Thus the displayed diagonal error is `O(q^2)` on the guarded interval. For sufficiently small q take that error at most `b_*/8` and `L X_q < b_*/4`, where `b_*=Q(1−c_b)/2`. The quotient inequalities reduce to

\[
x'\le(r-b_*/2)x+2Lq^2,\quad
y'\le-3b_*y/2+Lx,\quad z'/z\ge b_*/2.
\]

The bounded integral of r gives `x<=C(q^eta exp(−b_*t/2)+q^2)`, closing x with a factor-two margin. The y estimate stays below 1/3, and z cannot reach zero. The individual logarithmic amplitude defect is bounded by `2|R22-b|+2Lx`; its integral is `O(q^eta+q^2 log(1/q))`. Current amplitude weighting transfers that estimate to every aggregate subset without assuming constant radial label weights.

When these hypotheses hold on the union of the clock cohort and the omitted band, the exact clocks imply their amplitude ratio retains its entry order q^(1/4). Thus the intermediate-band warning also has a precise conditional transport formulation. This is not a claim that the initialized flow already meets the residual and entry assumptions, and the projected margin alone is not bounded weak-chart support at the later clock.

## 4. What the capped gain actually supplies for the secondary tail

The secondary entry tail is finite-cutoff, not a globally untruncated law. The upper radial pushforward tail and the fixed support cap imply, by Tonelli,

\[
\int z^2\,d\eta\lesssim q^3h_1^{p_2},\qquad
\int z^{2(1+\nu)}\,d\eta\lesssim q^3h_1^{p_2}.
\]

The energy-from-gain proof keeps a necessary pre-exit angular input. It splits using the **monotone comparison threshold** `X=q^2 z^2 exp(beta I)`, not an assumption that the actual displacement or H is increasing. While X is small, the distance envelope closes the physical chart guard, mass gain is bounded, and weak energy costs `m0(q^2+X)`. When X is above a fixed threshold, weak energy is at most radial mass and costs `Cm0 X^(1+nu)`. This yields a bound at every endpoint without assuming a completed weak return.

The gain is stated as an absolute current-mass bound relative to entry mass. If obtained first for a ratio to a core characteristic, a bounded core radial multiplier is needed to put it in this form.

For beta<=1, the separate clock's lower defect bound controls `exp(beta I)` by `C H/H0`. With H0 comparable to q^k, the energy estimate becomes

\[
E_{\rm sec}\lesssim q^5+q^{\gamma_\kappa}H+
q^{\gamma_\kappa-\nu(k-2)}H^{1+\nu}.
\]

The exact identity is

\[
5-k+p_2(\kappa d-2s)=\gamma_\kappa
=1-\frac\lambda2\left(\kappa-\frac4{1-\lambda}\right).
\]

At a bounded clock amplitude, this gives the stated Gamma_nu. Exactly gamma is the quadratic-gain exponent. A fixed positive nu costs a q power; an O(q^2) nu costs only a bounded factor tending to one. The general-kappa formula is conditional algebra, not an extension of the supplied target-only profile theorem to every kappa.

## 5. Correction to the raw transverse-energy target

The earlier `J_Q2 <= Cq^3` target can be used at target-only strong entry. It should not be imposed unchanged through a fixed positive weak-learning level. In a bounded weak chart,

\[
J=\tfrac12q^2\int m(u^2+v^2)+O(q^4\int m(u^4+v^4)),\qquad E\asymp N.
\]

A positive weak mass with nonzero limiting angular coordinates regenerates O(q^2E) first-coordinate energy. Allowing this does not spoil the forcing calculation.

The exact inequality is

\[
D^+\sqrt{J_G}\le r_G\sqrt{J_G}+\ell_G\sqrt{E_G},
\]

where r_G is the supremum of |R11| over that cohort and ell_G the supremum of max(|R12|,|R21|). This r_G is a matrix-entry envelope, **not** the signed logarithmic radial rate used in the gain problem.

If ell_G<=Cq, its integrated diagonal envelope is bounded, and `E_G <= C(q^5+q^sigma H)`, the separate clock integrates the square-root source and gives `J_G <= C(q^3+q^(2+sigma)H)`. The exact output-energy inequality then yields the desired forcing, including both the q^3 floor and the regenerated-transverse term.

For the whole Q2 cohort use sigma=0; for the secondary cohort use sigma=Gamma_nu. A constant `q^3 log(1/q)` term is retained. No whole-Q2 amplitude clock is invoked. With the bulk seed H0 comparable to q^k, the amplitude cap and lower clock-defect bound also imply a logarithmic time horizon directly.

The residual-norm proposition gives explicit sufficient hypotheses for the entry envelopes. Those original residual norms have not been bounded dynamically here. Their dependence on the full population must be preserved in a later coupled argument.

## Dependencies and unresolved estimates

Sources used: Q2E's `crossing`, `uncrossed`, `profile`, `axisU1upper`, and `energy`; CLOCK's exact aggregate equation, response ledger, and cross-energy estimate; TAIL's capped-gain integration and right-half-circle exponent margin. Selected weak-chart coordinates are used only to explain the regenerated transverse-energy term.

The shared missing original-flow package remains: the c-form all-label distance envelope and signed capped radial gain, including the strong diagonal term and all radial defects. Its successful proof supplies both right-half-circle mass charging and the secondary energy estimate proved here.

The new bulk clock theorem reduces the subinterval-defect problem to explicit original residual norms and relative Cartesian entry ratios. The shared radial-gain estimate does not automatically supply those inputs, joint profile transfer, the primary transit-band energy comparison, an antisymmetric/response cap, or residual norms needed for transverse propagation. Other ancestry, especially initial Q3, is not deleted. Selected-residual field errors and q^2-scale probe transfer remain separate.

## Verification and integration status

The new source was compiled as standalone LaTeX, and its PDF reading copy was rendered for layout inspection. Algebraic identities and rational constants were checked with symbolic simplification and exact fractions, not sampled trajectories. Compilation and symbolic simplification are not formal proof verification. The displayed proofs are for independent review.

This increment does not overwrite any prior theorem. It refines the proposed application of Q2E Section 5 and supplies a separate-clock route that no longer asks the full Q2 cohort to have a uniform subinterval defect. Its new transverse-energy allowance replaces the earlier raw q^3 **future target**, not Q2E's proved target-only entry result.
