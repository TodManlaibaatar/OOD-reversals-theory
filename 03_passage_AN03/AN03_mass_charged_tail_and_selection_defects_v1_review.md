# AN03 mass-charged tail and selection defects — review note v1

## New advance and scope

This increment closes the **algebra and integration** of the proposed excluded-mass route, conditional on its actual radial-growth hypothesis. It does not establish that hypothesis along an original-flow escaping label.

The combined exponent at κ = 10 is uniformly positive even on the independent rectangle

\[
\lambda\in[169/400,49/100],\qquad P\in[1/2,153/250].
\]

No additional analytic relation P(ρ) is needed for this conclusion. A loss obtained by separately maximizing the mass-growth exponent and minimizing the entry-tail exponent is unnecessary.

The increment also supplies a perturbed coupled-selection estimate using a **core moment plus explicit outside/value/derivative errors**, rather than a full strong first moment that would require chart coordinates for escaped labels.

## Statements and labels

All labels have prefix `inc:AN03:tailrepair:v1:`.

| Suffix | New statement | Status |
|---|---|---|
| `gainintegration`, `minintegral`, `labelgain` | Integrates quadratic pre-exit and capped post-exit radial growth using the monotone compensated clock | Proved scalar implication; the labelwise radial inequality is an application hypothesis |
| `moment`, `massbound` | Integrates a power-law entry tail against a quadratic-power mass gain | Proved measure estimate, requiring `p > 2(1+ν)` |
| `rational`, `margin0`, `marginnu` | Uniform κ = 10 margin, including a small geometric gain loss | Proved exact rational algebra; not an initialized regime |
| `selection`, `Econclusion`, `Wconclusion` | Coupled mean/orbit selection under explicit additive and integrated multiplicative defects | Conditional error-system theorem; weak return-region and clock/matching premises remain separate |

## Combined exponent and exact margins

Set

\[
E=\frac\kappa2(1-P)-s,\quad s=\frac{1-\lambda P}{1-\lambda},\quad p=\frac3s,
\]
\[
R=\kappa(1-\lambda)(1-P)-2-2\chi,\quad R_+=\max\{R,0\},
\]
\[
\Delta_\nu=p(E-\chi)-1-(1+\nu)R_+.
\]

For κ = 10 and χ = 1/20, the proof establishes

\[
\Delta_0\ge\frac{4561}{35006}>0.
\]

The identity `Δ₀ = min{A, A−R}`, where `A = p(E−χ)−1`, is used before taking parameter bounds. The first branch has the earlier minimum `4561/35006`. The second branch has the independent-rectangle lower bound

\[
A-R\ge\frac{11004659}{43757500}>\frac14.
\]

The proof displays both derivative calculations and their rational signs. It does not use a grid or numerical extrema.

For `0 ≤ ν ≤ 1/100`,

\[
p-2(1+\nu)\ge\frac{49}{7550}>0,
\qquad
\Delta_\nu\ge\frac{17141311}{140024000}>\frac3{25}.
\]

Thus the proposed `1+O(δ₀²)` gain must be made quantitatively small enough; it is not silently set to one. A separate factor `q^(−σ)` from the unresolved radial defect subtracts σ from this margin.

## Radial-gain contract and unresolved step

The scalar lemma uses

\[
I(t)=Q\int_{t_0}^t(1-c),\qquad
\exp I=(H/H_0)\exp(-\int\varepsilon_H).
\]

I is monotone; H need not be. If a mass-ratio logarithmic derivative is bounded by

\[
I'\min\{1,A_0D_0^2e^{\beta I}\}+b_\alpha,
\]

then its gain is at most

\[
e^{\int b_\alpha+1/\beta}
\max\{1,A_0D_0^2e^{\beta I(t_b)}\}^{1/\beta}.
\]

The intended `β = λ/Q` produces `1/β = 1 + q²/λ`. Bounded pre-exit comparison factors and endpoint clock defects must be proved before absorbing them into constants. To obtain a pointwise-in-time outside budget, the required bounds must hold at all intermediate endpoints as well.

The exact original-flow relative radial-rate identity is displayed at the end of the source. The following are still unproved there: the sign or budget for the strong diagonal term, the c-form all-label envelope through outer exit, and the integrated signed radial-rate defect. At positive Gaussian noise a lower-side training gate is not identically closed. Its negligible contribution requires a projected-margin estimate, not only a quadrant label.

The heavy secondary Q2 tail is excluded from the p > 2 moment argument. A clock-cohort or explicit-output decomposition must handle that ancestry separately.

## Selection modification and its scope

The core distance is taken only over labels possessing strong chart coordinates. Omitted mass also creates a mass-deficit term; setting core mass equal to one is not automatic.

After deriving a valid field representation, the errors can be placed in

\[
E_s'\le-gE_s+C_s(d_0+NW_p),
\]
\[
W_p'\le[-\lambda(1-N)/2+N/2+\ell_B]W_p+C_w(E_s+d_0).
\]

The homogeneous multiplier keeps the exact half-power and gains `exp(∫ℓ_B)`. A uniform bound on that integral yields the same small-gain closure with `B_b` replaced by `B_b exp(L_*)`.

For the conditional mass law above, the correct additive budget includes

\[
d_0\lesssim q^\chi+q^{\Delta_\nu}+\text{other errors},
\]

not the unamplified tail exponent if r_m is nonzero. The outside derivative costs `O(q^{Δν})`, whose integral over a logarithmic sojourn tends to zero. Mere pointwise `ℓ_B = o(1)` without an integral bound is insufficient for this uniform-multiplier argument.

A uniform outside-field **value** bound at every actual receiver may instead be charged additively in orbit comparison, without a derivative loss there. Pairwise same-field contraction still uses the derivative. This distinction is stated explicitly.

The theorem assumes the weak return-region hypotheses needed for its error inequalities. It closes the strong-reference guard, not the original weak capture/nonnegative-input problem. Its logistic N and fixed weak-label comparison also need original-flow matching; recruitment and changing radial weights are not absent by definition.

## Dependencies

- `AN02_strong_entry_profile_and_tail_budget_v1.tex`: right-half-circle entry tail, exact outside-field cost, and earlier unamplified rational exponent.
- `AN03_exact_amplitude_clock_and_c_passage_v1.tex`: exact aggregate clock and its signed defect convention; endpoint and subinterval hypotheses are kept distinct.
- `AN03_weak_transit_forcing_and_orbit_selection_v1.tex`: unperturbed coupled mean/orbit inequalities and small-gain closure.
- `AN03_two_sided_passage_and_Q2_retention_v2.tex`: only as an available all-label comparison to be adapted; no automatic c-form original-flow extension is invoked.

## Audit points

The clock integral is split analytically, including zero and already-supercritical cases. Tail-moment integration uses Tonelli with p strictly larger than the gained moment order. The core is fixed in initial labels. The exact 1/q outside-field cost is included once. Joint parameter extrema are taken only after combining the exponents. All denominators in the perturbed selection closure are strictly positive. A weak return guard, a strong mass deficit, or changing label weights is never removed by a name change. No original-flow closed-family mass law is assumed implicitly.

## Proposed later integration and verification

Place the clock-integration and tail-moment lemmas next to the mass-transport obligation, and replace an opposite-corner κ ≈ 15 estimate by the proved conditional κ = 10 margin. Add the core/outside selection variant as an explicitly perturbed interface. No earlier result is overwritten or merged.

The source was compiled as standalone LaTeX. The rational algebra was checked symbolically and by exact fractions. No numerical trajectory or sampled sign certificate was used; compilation is not formal proof verification. The new proofs are provided for independent mathematical review.
