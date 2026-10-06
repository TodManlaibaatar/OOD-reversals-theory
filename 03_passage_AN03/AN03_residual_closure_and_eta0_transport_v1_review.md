# Review: residual closure and eta=0 transport, v1

**Disposition: Stage 1 is incomplete; stop before Stage 2.** The paired `.tex` contains two completed proof increments, a narrower conditional residual theorem, and the exact obstruction after two attempted residual closures. No initialized S0 theorem is claimed. The obstruction is a failure of the two deductions examined, not a counterexample to the original dynamics.

All new LaTeX labels use `an03rcetv1:`. No prior source is changed, replaced, merged, or re-proved. The repository was read through its GitHub connector as explicitly requested; no remote mutation was made.

## New results and their scope

1. **Theorem 2.1, `eta0`: conditional original-flow implication.** Retains BULK Theorem 4.1's response, duration, diagonal/cross residual, and integrated `R11` hypotheses. Replaces `x(t0) <= C0 q^eta` by `x(t0) <= C0`, where `C0` is sufficiently small relative to those fixed constants. The fixed guard is `X = 4 exp(B) C0`. It proves
   \[
   x(t)\le C(C_0e^{-b_*\tau/2}+q^2),\qquad
   a_{\theta,2}/q\ge c\min\{q^{-1},C_0^{-1}e^{b_*\tau/2}\},
   \]
   and the all-subinterval absolute defect bound, hence
   `D_osc = O(C0 + q^2 log(1/q))`. Relative subset amplitudes change by factors between `exp(-2D)` and `exp(2D)`. Raw energies are between `H` and `(10/9)H`.
2. **Proposition 3.1, `dichotomy`: exact target-only comparison.** Proves the threshold split at `c0 ~ q^gamma`. Near that threshold it proves the requested power law. The uniform pre-arrival version retains the endpoint factor:
   \[
   q\cot\widehat\theta(T)\asymp
   \left[q^\gamma\frac{s_0+q}{c_0+q}\right]^{(1-\lambda)/\lambda}.
   \]
   For any fixed small `C0`, a sufficiently large fixed `K` puts `c0 >= K q^gamma` under the comparison entry-ratio bound. Every remaining label has a fixed strong-chart displacement cap `Z(C0)`. The two classes can consequently use the respective original-flow tools **only after** their existing transfer and gain hypotheses are supplied. The cap alone does not establish BULK Proposition 5.2's distance envelope or capped gain.
3. **Lemma 4.1, `outputs`: instantaneous original-state estimate.** Gives cross residuals as `q` times the explicit output pressure plus the strong-core and outside contributions. With `Y = sqrt(J)/q`, the pressure is bounded by
   `C[1 + E + q^2 Y^2 + sqrt(E)Y + mu_B/q]`.
   On `P1`, the decomposition `f1 = kappa1 X1 + g1` has
   `||g1|| <= C[q^2 + q^2Y^2 + q^2Y sqrt(E) + mu_B]`.
4. **Theorem 4.2, `closure`: narrower conditional estimate.** Given an *independent* backward clock bound, the existing energy/core/outside/strong-learning budgets imply bounded diagonal residuals, `O(q)` cross residuals, and
   \[
   \int\sup_\theta|R_{11}|\le C\int|1-\kappa_1|+o(1).
   \]
   A Volterra comparison retains regenerated-energy feedback and needs no smallness assumption on fixed `H_b`. It does **not** independently close the clock premise, so it is not the requested full S0 result.

The eta=`1/8` cohort remains the phase clock. The eta=0 estimate gives bounded distortion; a fixed small `C0` does not give a vanishing phase defect.

## Exact obstruction and failed approaches

### Route 1: scalar residual fixed point

Keeping the trial residual constant `L` explicit in BULK's transverse estimate gives
\[
\sqrt J\lesssim q^{3/2}+Lq\sqrt H,
\qquad
\mathfrak F_G\lesssim q^3+H+\sqrt{qH}+LH+L^2q^2H.
\]
The proposed constant improvement therefore contains `C L H_b`:
\[
L_{\rm new}\le A+C H_b L+o_q(1)L<L.
\]
Small `q` does not make `C H_b` small. S0's suggested `H_b + L sqrt(q H_b) + q^3` expression omits the regenerated contribution. The `.tex` includes an exact balanced-state example exhibiting pressure at least `LE` when `J=q^2L^2E`; this is not asserted to be an initialized trajectory. Adding `C H_b < 1` would be an extra hypothesis, so it is not done.

### Route 2: Volterra feedback and simultaneous clock bootstrap

The repaired integral estimate is
\[
Y(t)\le A_*+C e^B\int_{t_0}^t E(s)Y(s)\,ds
          +C e^Bq^2\int_{t_0}^t\sqrt{E(s)}Y(s)^2\,ds.
\]
It closes with `int E = O(1)` and `int sqrt(E) = O(1)`. A globally controlled clock and terminal amplitude cap supply those bounds. On a first-exit interval ending at `t_*`, however, the established clock gives only
\[
\int_{t_0}^{t_*}H\le eH(t_*)/b_0.
\]
The exact missing inequality is **`H(t_*) <= e H_b` at every possible first-exit endpoint** (`failingendpoint`). The cap `H(t_b) <= H_b` controls a later endpoint. To bound the earlier amplitude by it requires the clock defect on the uncontrolled future interval `[t_*,t_b]`. Invoking BULK there invokes the residual bound still being proved.

An added guard `H <= e H_b` does not improve itself from the terminal cap. Nor does total loss monotonicity directly control the cohort's symmetric amplitude: CLOCK's response ledger retains complementary signed response, antisymmetric energy, and the negative-gate term. The `.tex` gives an explicit positive scalar amplitude with power-law entry, a fixed endpoint cap, and a logarithmically divergent integral. It only refutes the scalar endpoint-to-integral inference, not the original-flow theorem.

An independent uniform amplitude/response-ledger estimate, an independent all-subinterval clock bound, or a suitable signed transverse estimate might repair the gap. This increment does not assume or prove one. Under the user's two-failed-routes rule, no further closure route or Stage 2 is attempted.

## Retained inputs

The eta=0 result retains precisely BULK's residual hypotheses and original Cartesian entry. The narrower residual theorem retains:

- A fixed bounded strong chart with bounded core mass and `sup_t mu_B/q -> 0`.
- Original entry data and the aggregate energy input `E_G <= C_E(q^5 + H)`, `J_G(t0) <= C_J q^3`, for all explicit-output cohorts. Target-only membership does not provide these original-flow inputs.
- For deriving that energy input by the proposed partition: primary entry-amplitude comparison and transport; secondary transferred profile, pre-exit distance envelope, and capped gain. Those remain existing open obligations.
- Response and logarithmic-duration bounds, a terminal amplitude cap, and `int |1-kappa1| <= B_s`.
- **Additionally retained and unresolved for S0:** the independent all-subinterval backward clock bound. This is displayed openly; it is not counted as a hypothesis-free closure.

All constants may depend on the fixed budgets and the compact rho interval. The eta=0 threshold for `C0` depends on the residual constants and `B`; no uniformity in arbitrarily large trial constants is asserted. The conditional residual theorem has no `H_b` smallness assumption.

## Analytic audit points

- **First exits:** eta=0 uses `x<X`, `y<1/2`, `z>0`, with strict improvements. The residual lemma uses `Y<K` and `int r<B`; the independent global clock bound is available throughout that narrower lemma. It is not claimed to improve a simultaneous amplitude guard.
- **Divisions:** divide only by the guarded positive `z`, by positive cohort amplitude in clock identities, and by `q>0`. At `j=0` or `J=0`, use the norm upper Dini derivative.
- **Gate margin:** `U2 >= z/2` makes the projected component positive even if `U1` has either sign. Gaussian inactive-gate tails use projection onto the unit input vector. The refined growing margin, not a constant tail integrated over a logarithmic interval, gives the defect bound.
- **Signs:** positive post-crossing target coordinates justify the ratio estimates. The target-only `U1` lower bound uses the created positive seed and `U1' >= U1/2`; the `U2` correction is nonnegative and has a bounded integral before chart arrival. No signed cross-output cancellation is assumed.
- **Endpoint qualification:** at the label `alpha=pi`, the unregularized formula misses a factor `q^((1-lambda)/lambda)`. Near the threshold `s0~1` and `c0>>q`, so the intended threshold and finite-cap partition survive. This corrects the domain of the roadmap's informal two-sided formula, not Q2E's regularized result.
- **Integrals:** all cohorts are fixed sets of initial labels. Finite-horizon characteristic bounds justify differentiation and domination. Output estimates use Minkowski/Cauchy–Schwarz. There are no moving-mask derivatives, numerical limits, or unproved exchanges with an infinite-time limit.
- **Remainders:** once `Y` is bounded, the integrated error is controlled by `q^2 log(1/q) + sup(mu_B) log(1/q) = o(1)`. The assumption `mu_B=o(q)` is sufficient; no stronger logarithmic mass assumption is inserted.
- **Analytic-only:** no interval arithmetic, sampled signs, saved trajectories, numerical premises, or experiments were used. Compilation is only a typesetting check.

## Source dependencies and provenance

Read in the requested order: README, roadmap, H2 §0. Actual source bytes were then fetched. Relevant immutable blob identifiers:

| Source | Blob SHA | Used labels / results |
|---|---|---|
| BULK v1 | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` | `inc:AN03:bulkclock:v1:` + `bulkclockclosure`, `R22tail`, `bulkweights`, `gainenergy`, `secondary`, `transverse`, `forcing`, `residualinputs` |
| Q2E v1 | `cce55e1029cfd1ca8afb98eb649389b420d3992b` | `inc:AN02:q2completion:v1:` + `crossing`, `axisU1upper`, `profile` |
| PROFILE v1 | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` | `inc:AN02:profile:v1:` + `root`, `arrival`, `outerdecomposition`, `cost` |
| CLOCK v1 | `8de0d85c64a3d51f3bd9c3662baf2efae0737373` | `inc:AN03:clock:v1:` + `endpoint`, `Hcap`, `crossenergy` |
| Foundations v2 | `a5c557d56fe5753532a600f8f238a74f8091da9b` | P5 loss dissipation and characteristic bounds |

No earlier proof is replaced, so there is no replacement label map. The completed eta=0 result would eventually follow BULK Theorem 4.1/Corollary 4.2; the threshold qualification belongs beside its primary-cohort partition. The conditional residual lemma and obstruction belong beside S0's residual-input reduction. These are proposed locations only; no consolidation is authorized or performed.

## Validation

Mathematical validation consists of the displayed analytic arguments and this dependency audit. The final source compiled successfully with the built-in LaTeX compiler. The first attempt timed out while downloading compiler fonts/resources; the retry succeeded. A static reference audit found 24 unique labels, all using the stated prefix, with no unresolved local references. These checks establish typesetting and reference consistency, not mathematical validity. No independent human or agent mathematical review is claimed.
