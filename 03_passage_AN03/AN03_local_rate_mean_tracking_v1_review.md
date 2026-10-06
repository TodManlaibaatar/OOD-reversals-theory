# AN03 local-rate passage with mean tracking — v1 review

## What is new

This increment proves a nonlinear local-rate passage theorem in the full leading population, with collective mean control proved simultaneously rather than assumed as a prescribed mean path. Its principal amplification is N0^(-alpha/lambda), not N0^(-1/2). The result includes a fixed core, the remaining strong population through a weighted first moment, and full weak feedback through N + |V| + K_w.

It does not prove isotropic entry, retained seed, weak angular condensation, chart validity of the original population, or finite-noise transfer. No experiment or repository inspection was performed. All proof constants are analytical.

## Main contract

Fix rho in (0,1), lambda = rho², a = rho K(rho a), P = Phi(rho a), and alpha = lambda P/2. The population follows the exact defined leading equations, has logistic M and N, constant normalized label weights, and bounded support on compact time intervals. Require 0 < M <= 1 and 0 < N <= 1/2.

Choose a fixed positive-weight strong core C and a reference characteristic (c,d) evolving in the **same full field**. Put D = |x-c| + |y-d|, r = ess sup_C D, T = integral over C-complement of D under the normalized full strong-label law, and f_budget = N + |V| + K_w + T. No label is removed from the field. T is a first absolute moment, not a tail-mass fraction.

Theorem 4.1 uses an interval from N = N0 to a fixed N = n_b <= 1/2. Its hypotheses are an explicitly small entry reference error e0, an explicitly small integral F_b of f_budget, and an explicitly small product

A = r0 exp(C0 e0/g + K0 F_b) (n_b/N0)^(alpha/lambda).

All constants and guards are given in equations (1.4), (4.1), and (4.2). The conclusion is

r(t_b) <= 2 exp(C0 e0/g + K0 F_b) (n_b/N0)^(alpha/lambda) r0,

with the mean error bounded by its stable convolution, and explicit time-integrated mean and radius bounds. The proof closes both first-exit guards.

A sufficiently small fixed n_b and a bound |V| + K_w <= C_w N + w make the N part of the forcing integral small; the remaining integral of w + T is still a hypothesis. The small threshold n_b can be very conservative. No useful numerical value is asserted.

## Proof structure and statements

### Lemma 2.1 — all-order local coefficient

The exact same-field derivative and lower-side donor cancellation give, for arbitrary signs of both coordinate differences,

D+ r <= [alpha(1-N) + C0(e + r + f_budget)] r.

This retains the local Gaussian gate Phi(rho(c+r)). It does not substitute an unproved fixed mean for c. Lower- and mixed-order labels are included. The core is selected at entry and held fixed.

### Lemma 3.1 — stable collective mode

The collapsed, no-weak field G_M has (a,a) stationary for all 0 <= M <= 1. Its Jacobian is

J_M = [[-(1-M)/2 - M alpha, alpha], [alpha, -1/2]].

J_M is bounded above by J_1 as a symmetric quadratic form. The smallest eigenvalue of -J_1 is at least gamma = alpha(1/2-alpha)/(alpha+1/2). Explicit Hessian estimates and the overlap kernel's Lipschitz donor coordinate give

D+ e <= -gamma e + C0 e² + C0(r + f_budget).

The actual reference stays in the full field. It does not follow G_M exactly. The discrepancy from G_M is displayed component by component and includes all tail and weak moments.

### Theorem 4.1 — coupled nonlinear closure

Integrate the stable mean estimate into the radius estimate. A Riccati denominator gives r <= r0 L/Q. The multiplier L, not the actual radius, obeys L' >= alpha(1-n_b)L. Hence integral L <= L_b/[alpha(1-n_b)] without paying an additional log(1/N0). The stated smallness conditions ensure Q >= 1/2, r <= 1/2, and e <= 3e*/4, strictly improving the bootstrap guards.

This corrects a potential gap in the proposed heuristic: an upper growth inequality for a radius does not imply that the actual radius grows exponentially or that its integral is bounded by its endpoint divided by a growth rate.

### Proposition 5.1 — later bounded continuation

A fixed logistic interval from n_b to 1/2 only costs a multiplicative constant if all relevant strong and weak coordinates and the reference remain in a fixed bounded set. That continuation and compactness are additional hypotheses. They are not derived from the local resident theorem. Core spread is controlled; proximity to the selected AN06 orbit also requires weak-angle and mean selection estimates.

### Corollary 5.2 — explicit joint powers

At a common chart-valid entry time suppose

r0 <= C_s q^(-s_sh) S0^(beta_sh),
N0 >= c_w q^(s_seed) S0^(gamma_seed),

with uniform forcing and continuation bounds. Then the radius product is bounded by a constant times

q^(-s_sh - s_seed alpha/lambda) S0^(beta_sh - gamma_seed alpha/lambda).

For S0 = q^kappa, its strict positive-power test is stated in the source. This is a conditional passage corollary, not an initialized parameter-region theorem.

With the user's proposed, still-unproved matching powers, the test becomes

E_loc = kappa(1-P)/2 - (1-lambda P)/(1-lambda).

For rho in [13/20,7/10] and kappa = 15/2, elementary rational bounds give E_loc > 4193/51000. This is an analytically nonempty **algebraic** window. It is not a proof that the weak population is already charted at the strong-learning clock. The later common-clock matching costs must still be established; no U2²-to-logistic-N substitution is authorized.

## Dependencies

Supplied checkpoint: `pa:leading`, `pa:masslaws`, `pa:overlap`, `pa:resident`, `pa:spectra`. All needed equations and matrix/overlap derivatives are restated. The mixed-order algebra is consistent with the separately repaired AN03 v2. The current user's review motivates the local-rate question but provides no numerical proof premise.

## Audit points

- All donor contributions remain in the full field. Small tail mass alone does not bound T.
- The reference is a same-field characteristic; stability of the collapsed comparison does not compare different populations by order.
- The essential supremum is handled via the common labelwise integral inequality and uniform Lipschitz bounds on compact intervals.
- Absolute values at coordinate equality use cross velocities; exact coincidence is preserved.
- The stable norm estimate uses symmetric quadratic forms, so it remains valid for time-dependent M without differentiating eigenvectors.
- The mean error is Euclidean, while D is l1; sqrt(2) is included where needed.
- The core radius is not assumed monotone. The only required exponential lower bound is for the explicitly defined majorant L.
- The denominator Q and both mean/radius first-exit guards are checked explicitly.
- Integrated T does not imply a pointwise bound on the full strong barycentre. The core mean is within e + r of (a,a); the full mean costs T as well.
- The late bounded interval, weak-angle convergence, and finite-noise perturbation are not hidden in the local theorem.

## Open residue and proposed integration

The initialized entry law, the weighted tail/weak forcing integral, the transit/return matching clock, and original finite-noise estimates remain open. A next useful step is a source-resolved estimate that makes |V| + K_w and the tail first moment integrable during transit and return, together with the matched joint input/output core radius.

After independent review, this file could supply the nonlinear local-rate portion of AN3 following the existing exact mean/shape spectra and multipliers. It does not replace AN2 or AN7. Every new label starts `inc:AN03:local:v1:`. Principal labels are `localineq`, `meanineq`, `main`, `late`, `joint`, and `rationalwindow`.
