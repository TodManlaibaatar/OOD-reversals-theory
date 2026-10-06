# AN02 Q2 profiles and localized tracking — v1 review

## Precise advances and status

This increment contains three distinct kinds of result; they must not be conflated.

1. **Exact finite-noise target-only results:** scalar first integral, weighted pushforward density, an outer comparison with the zero-noise target flow, and analytical weak-axis/strong-chart transit clocks.
2. **Exact zero-noise comparison profile:** the Cauchy-squared law for coordinate energy in a tangent coordinate, with explicit corrections for radial mass and for the angular chart coordinate.
3. **Exact conditional original-flow result:** a Q2-side tracking inequality with the dominant strong output isolated and the rest of the full population retained through an explicit L2 output defect.

No theorem here proves an initialized lower bound on the retained weak-chart mass. No post-saturation return, original-flow absorption, or finite-noise population-to-leading reduction is established. No repository, saved pilot arrays, numerical integration, or Gaussian numerical evaluation was used as a proof premise.

## 1. First integral and profile

Proposition 2.1 starts from the exact finite-noise target-only scalar speed v_q and full logarithmic mass rate g_q. On any angular interval with v_q nonzero, G_q' = g_q/v_q gives a first integral log m - G_q(theta), and the scalar flow's Jacobian is the ratio of endpoint and initial speeds. The exact weighted angular density is then a one-dimensional inverse-flow formula.

Division by v_q is only permitted on such a nonstationary interval. The statement does not cross an equilibrium by dividing by zero. The velocity ratio has positive sign. Restricting to an ancestry subset adds its inverse-image indicator.

Proposition 3.1 derives the elementary profile in the explicitly specified zero-noise target-only comparison. In Q2, U1 is constant and U2 grows as exp(lambda t/2). Put upsilon = U1/(q U2), b_t = exp(-lambda t/2)/q. The U2²-weighted measure is exactly

S0 exp(lambda t)/(2 pi b_t) [1 + upsilon²/b_t²]^(-2) d upsilon, upsilon < 0.

Its total coordinate energy is S0 exp(lambda t)/8. The total radial measure has the extra factor 1 + q² upsilon². The actual angular chart coordinate is u = (pi/2-theta)/q, so upsilon = tan(qu)/q. Converting the radial density to u produces sec^4(qu), while the coordinate-energy density has sec²(qu).

These are not cosmetic distinctions if the profile is used for a uniform mass or tail theorem. The current review's elementary expression is a useful outer approximation, but it cannot be used as the exact positive-noise radial profile in the angular coordinate. At fixed negative u, the finite-noise cross-gate term K(u) does not disappear as q tends to zero.

Proposition 3.2 supplies a labelwise outer comparison where both projected margins exceed qL. Its error is bounded by [3q²/4 + K(-L)/(2L)]T. A margin-doubling condition closes the first-exit guard. This is not yet a density-error theorem because it does not bound the Jacobian error.

## 2. Analytical transit clocks

Theorem 4.1 proves, for a fixed initial Q2 label alpha0 = pi/2 + d0,

T_cross = (2/lambda) log(tan(d0)/q) + C_rho + o(1),

where C_rho is given by two absolutely convergent one-dimensional integrals. It is not assigned the reported numerical value. The proof rescales tan(d)/q, subtracts the logarithmic divergence, and bounds both Gaussian remainder terms. Uniformity is proved on compact rho and initial-angle intervals.

Theorem 4.2 proves that, after weak-axis crossing, the exact target-only travel time to a fixed Q1 angle has coefficient 2/(1-lambda) in log(1/q), and the travel time to theta = qR has coefficient 4/(1-lambda). Adding the crossing coefficient gives respectively

2/[lambda(1-lambda)] and 2/lambda + 4/(1-lambda).

The strong-chart target R is fixed sufficiently large, with an explicit inequality that guarantees strictly clockwise motion on the travel interval. The proof splits into a Gaussian-tail interior and two endpoint layers using L(q) = sqrt(log(1/q)). Endpoint times are O(log L + 1), not silently discarded without bounds.

These establish some of the review's previously numerical clock coefficients **within the target-only flow**. They do not establish original-population departure or absorption: the trained residual changes at saturation. They also do not make an impossibility theorem out of the proposed global-rate regime diagram.

## 3. Localized original-flow comparison

The original output is decomposed algebraically as

f_t(X) = M_mathfrak(t) X1 e1 + g_t(X),
E(t) = sqrt(a_star) ||g_t||_L2(P),

with any chosen nonnegative comparator coefficient M_mathfrak. It is not called a learned strong mass without proof.

Lemma 5.1 proves, for an input with a1 <= 0,

|(A_theta a)_1| <= q,
|a1| ||A_theta e1|| <= 2q.

The cluster-1 contribution uses its exact truncated Gaussian trace, not a declaration that the gate is off. The cluster-2 cross coordinate contributes O(q). Cauchy–Schwarz bounds the remaining full output by E. These give

||C_f a|| <= q M_mathfrak + E,
||C_f^T b|| <= 2q M_mathfrak + a_star M_mathfrak ||b-a|| + E.

Theorem 5.2 uses these in exact alignment, angle, and radial equations. The three scalar envelopes are displayed in equation (5.4). They bound the input/output alignment error, target-only angle error, and log radial error while the original input stays left-facing and the alignment envelope stays below pi.

The main improvement is replacing an unsuppressed O(M_mathfrak) cost of the principal strong output by O(q M_mathfrak), plus the explicit full-output defect. The theorem does **not** prove that E is small through strong learning. Nor does it apply to already crossed Q2 labels on the Q1 side merely because their ancestry remains Q2.

## Dependencies

Frozen foundations: exact balanced flow and Gaussian half-space identities. Supplied checkpoint: `pa:setup`, `pa:earlybounds`, `pa:targetcomparison`. AN02 strong ancestry/tail transport v1 supplies related coordinate-growth provenance. The proofs needed here are restated in the standalone TEX. The companion local-rate passage theorem is separate.

## Audit points

- Distinguish g_q (the full log-mass rate) from the half-rate g_0 in the original comparison proof.
- Scalar first-integral and density formulas are local to intervals where v_q is nonzero.
- Coordinate energy, radial mass, tangent coordinate, and angular coordinate have different weights/Jacobians.
- The outer comparison guards both Gaussian projected margins and proves that the trajectory remains in Q2 on the specified interval.
- The crossing constant is a convergent analytical integral, not a numerical fit. Dominated convergence bounds are uniform only on compact parameter/initial-angle sets away from the endpoints.
- The Q1 target R must satisfy the explicit lower bound. This is a prescribed target-only chart arrival, not a theorem of learned strong-family membership.
- The original-flow output defect includes every label; no uncharted mass is dropped.
- The left-facing Gaussian estimate holds even at a1 = 0 without division by a1.
- The alignment first-exit is closed by Delta < pi. Left-facing persistence is a stopping condition, not proved globally.
- A small log radial error is not a retained weak-chart mass bound without angular capture and ancestry-measure control.

## What remains and proposed integration

A useful retained-seed lower bound still requires an initialized weighted bound on g_t, a matched positive-side transit/return argument, control of radial/coordinate energy under the changed residual, and a common bounded-chart entry time for passage. The elementary Cauchy profile and target-only clocks alone do not give c_w for the original population.

After review, the scalar formulas, comparison profile, and analytical clocks could be added to AN2's target-only transport subsection. The localized original-flow lemma should be used only with its explicit defect contract. It does not supersede the frozen foundation or establish the AN2 endpoint.

All labels start `inc:AN02:q2:v1:`. Main labels: `firstintegral`, `cauchy`, `outer`, `cross`, `transit`, `gaussiansuppression`, `originaltracking`, and `residue`.
