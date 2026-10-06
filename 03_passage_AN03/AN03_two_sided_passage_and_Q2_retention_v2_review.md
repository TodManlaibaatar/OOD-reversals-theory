# AN03 two-sided passage and Q2 retention — v2 review

## Status and changes

This is a repaired version of the previously reviewed AN03 v1, not a new initialized theorem. The supplied v1, all other prior increments, the foundations, and the consolidated checkpoint are unchanged. No repository or experimental arrays were accessed. No training run or Gaussian numerical evaluation is used as a proof premise.

The repairs are local to the proof and scope discussion:

1. **Theorem 4.1, mixed order.** The co-ordered identity is no longer used as though it were an identity for a mixed pair. The upper-input and lower-input absolute-value inequalities are written separately for either sign of the output difference. The lower-side donor cancellation is applied before estimating. Coordinate equality uses the absolute cross velocity; complete coincidence uses uniqueness.
2. **Theorem 4.2, differentiating the first moment.** On compact intervals with bounded support, the label distances are uniformly Lipschitz. Their integral is Lipschitz, and Fubini transfers the almost-everywhere scalar derivative inequality under the fixed probability measure. A bounded-difference-quotient/reverse-Fatou argument gives the corresponding upper-derivative formulation. No density of the projected angular measure is needed.
3. **Corollary 5.2, rational constant.** The uniform global-rate exponent is sharpened from 4901/80000 to a strict lower bound 16393/200000. Set z = rho a_rho. Since z - lambda K(z) is strictly increasing, K(z) <= 2/5 + z/2 + z²/5, and (49/100)[2/5 + 7/50 + 49/3125] < 7/25, the resident root satisfies z < 7/25. Thus Phi(z) < 153/250. This supplies the requested sharpening without a floating-point Gaussian value or the proposed z = 0.2845 test.
4. **Joint-regime inference withdrawn.** Corollary 5.2 is a conditional implication. A positive formal initialization exponent and the algebraic requirement log A(q) = o(log(1/S0)) do not establish that the entry seed, shape, and forcing hypotheses hold on the same sequence. The prior suggestion that local rates merely improve constants is withdrawn. Local-rate control may be essential after the q-costs and transit stage are matched.

The algebraic exponent implication is not retracted. Nor does the repair replace it with an unproved claim that the global-rate theorem cannot apply in any actual initialized regime. That stronger conclusion requires matching and retention estimates not supplied by the numerical table or by target-only transit alone.

## Proof contract

Theorem 4.1 and Theorem 4.2 remain results for the full **defined leading population**, on a chart-valid finite interval with constant normalized strong-label weights and logistic family masses. They retain the same-field comparison convention. They are not comparisons between different self-consistent residual fields.

The global nonlinear passage needs:

- a common entry time, 0 < N0 < 1/2;
- the joint input/output initial distance moment R_p;
- a bound on the integral of the positive mean imbalance;
- the Riccati smallness condition;
- chart-valid evolution to weak half-mass.

Corollary 5.2 additionally assumes the specified retained seed and entry shape laws. None of these entry estimates is promoted to an initialized conclusion.

## Dependencies

Unchanged dependencies: checkpoint `pa:leading`, `pa:masslaws`, `pa:overlap`, `pa:earlybounds`, `pa:targetcomparison`, `pa:resident`, and `pa:spectra`; AN02 strong ancestry/tail transport v1; AN02 weak-side arrival v1; AN06 learned orbit witnesses v2. Needed formulas are restated in the standalone TEX.

The new local-rate and collective-mode result is in the separate `AN03_local_rate_mean_tracking_v1.tex`, not silently inserted into this repaired source.

## Audit points

The common normalized label weights are essential for moment integration. The result is stopped before physical chart exit; it cannot keep using a fixed chart after escape. The lower-input receiver term must be combined with the donor term before the favorable estimate. The absolute-value inequalities hold at mixed output signs but the earlier co-ordered identities do not. The Riccati denominator must remain positive. The factor that grows at a positive rate is the scalar comparison multiplier, not necessarily the actual population radius.

The exact-clock conversion before capture still needs a mass-law defect and moving-mask flux budget. Centering at the population's own weak half-mass time removes phase mismatch only for the closed leading logistic law; it does not derive an entry seed or eliminate finite-noise mass-rate defects.

## Label map and integration

Every old label

`inc:AN03:ret:v1:<suffix>`

maps to

`inc:AN03:ret:v2:<suffix>`.

The suffixes and theorem numbering are unchanged. Thus `alllabel`, `halfpassage`, `exponent`, `uniformeta`, and `clocks` retain their roles. This version supersedes v1 only as a proposed repaired review source. A later approved consolidation should replace those proofs and the regime discussion, not change the frozen foundations.

## Open residue

The Q2 retained-seed lower bound, a common chart-valid entry clock, entry joint shape with its q-prefactor, population mean/weak/tail budgets, weak angular selection, and finite-noise transfer remain unproved. The original initialized Theorems A and B remain open.
