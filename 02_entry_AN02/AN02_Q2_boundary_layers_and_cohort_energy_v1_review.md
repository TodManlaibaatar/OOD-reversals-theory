# AN02 Q2 boundary layers and full-cohort energy — review note v1

## New advance and scope

This increment is **exact analytical comparison work for the positive-noise target-only flow**, not an original residual-flow entry or capture theorem. It establishes three results that were not supplied by the earlier fixed-interior Q2 clock and right-half-circle profile theorems.

1. The Q2 weak-axis crossing clock is uniform through both initial endpoints, including α = π. Gaussian leakage regularizes the initially vanishing second coordinate there. The maximal crossing time is `(4/λ) log(1/q) + O(1)`. At κ = 10 all target-only Q2 labels have crossed before the strong comparison clock, uniformly on the reviewed ratio box.
2. Q2 ancestry that has reached the strong chart has its own radial profile and secondary tail. Its total mass relative to the right-half-circle mass is comparable to q³; its tail beyond the old Q1 cutoff has index `p₂ = (1 − 3λ/2)/d ∈ (0,1)` on an explicitly restricted range. This does not cover Q2 labels still outside the strong chart.
3. On the **entire fixed Q2 ancestry**, at `S₀ = q¹⁰`, `T = log(1/S₀)`, the target-only transverse energy is comparable to q³ and the symmetric weak-coordinate amplitude is comparable to q⁵. A compact interior Q2 bulk does not determine these aggregate scales.

## Statements and labels

All labels have prefix `inc:AN02:q2completion:v1:`.

| Suffix | Result | Scope |
|---|---|---|
| `crossing`, `crossclock`, `crossamplitude` | Uniform crossing clock and crossing/post-crossing coordinate amplitudes | Exact target-only flow, entire closed initial Q2 sector |
| `uncrossed` | Before-crossing radial bound `m ≤ C S₀/q²`; all-Q2 crossing by κ = 10 | Exact target-only flow; not a bound after a frozen excluded label crosses |
| `profile`, `displacement`, `weight`, `tail` | Recruited strong-chart Q2 profile and secondary tail | Exact target-only flow at κ = 10, with a fixed strong-chart cutoff and intermediate tail range |
| `energy`, `Jupper`, `Hupper`, `energylaws` | Whole-Q2 energy bounds and endpoint asymptotic orders | Exact target-only flow, `0 ≤ t ≤ 10 log(1/q)` |

The label set `R_q = {π/2 + d₀ : q ≤ d₀ ≤ 2q}` depends on q but is fixed in time. This strip gives the energy lower bounds.

## Exact consequences and corrections

**At a crossing of θ = π/2, U₁ is exactly zero.** A first coordinate comparable to `sqrt(S₀)(−cos α + q)` is created after a fixed positive post-crossing layer time. This corrects the literal “at crossing” wording without changing the proposed entry-weight exponents.

The fixed-interior formula `(2/λ) log(tan d₀/q) + O(1)` must not be extrapolated to `d₀ → π/2` at fixed positive q. The uniform replacement is

\[
T_\times(\alpha)=\frac2\lambda\log\frac{-\cos\alpha+q}{q(\sin\alpha+q)}+O(1).
\]

There is no inference that all original residual-flow Q2 labels have crossed at that clock. There is also no contradiction with finite-time angular surjectivity of the entire circle: this statement concerns only the initial Q2 sector of the target-only flow.

The whole-Q2 estimate `J_C ≤ q² H_*` requires `H_* ≳ q` at the target-only strong-entry clock. The bulk candidate `q^(2/λ−2)` is `o(q)` and therefore cannot bound this entire cohort. Likewise, a lower seed law `H_C ≳ S₀^(1−λ)` remains compatible with the result, but a two-sided full-cohort law at that scale does not hold in this comparison at κ = 10.

The original cross-energy tool can still be useful with `H_* = O(q)` **if that bound is transferred and propagated in the original flow**. It produces `H_C + sqrt(q H_C) + q³`; its square-root clock integral has order `sqrt(q H_b)` and the constant term costs `q³ log(1/q)`. These original-flow premises are not proved here.

## Dependencies

- `AN02_Q2_profiles_and_localized_tracking_v1.tex`: exact coordinate and angular equations (`coordinates`, `angular`, prefix `inc:AN02:q2:v1:`). Its crossing theorem is uniform only on compact interior initial-angle sets; the current crossing lemma extends that scope analytically.
- `AN02_strong_entry_profile_and_tail_budget_v1.tex`: exact attracting center/local rate, uniform Q1 axis arrival, first-coordinate gate-integral argument, and right-half-circle normalizing mass (`root`, `arrival`, `gateintegral`, `rightcircle`, prefix `inc:AN02:profile:v1:`).
- `AN03_exact_amplitude_clock_and_c_passage_v1.tex`: definitions of symmetric/transverse energies and the conditional cross-output/clock interface; used only for consequences, not as a premise of target-only dynamics.

## Audit points

- Both Q2 endpoint speeds are strictly positive for q > 0. The reciprocal-speed error is integrated; no fixed relative error is multiplied by a divergent logarithmic time.
- The negative strong-axis layer creates U₂ before division by U₂. At α = π, no logarithmic derivative at the initial zero is used.
- Crossing time and radial amplification are computed together. The factors `(−cos α + q)` and `(sin α + q)` are both retained.
- Target-only alignment is explicit. No preservation of U = W in the original nonlinear residual flow is asserted.
- The secondary tail is a normalized **submeasure** of already-arrived Q2 labels, not the original Q1 probability law and not an unbounded global power law.
- The lower tail bound stays away from the final chart cutoff. An instantaneous chart indicator is never differentiated.
- The whole-Q2 upper bound uses the first-coordinate estimate even before strong-chart arrival. It does not assume every Q2 label has entered that chart.
- The aggregate H upper bound retains both `S₀ exp(λt)` and `q⁵ S₀ exp(t)`. The latter dominates at κ = 10 on the stated ratio box.
- Minkowski is used with finite label measure and bounded finite-time characteristic states. The `exp(Cqt)` factor is bounded only on the displayed logarithmic horizon.
- A before-crossing mass bound is not propagated automatically for a fixed set of late labels after they cross.

## Unresolved original-flow estimates

The original population still requires a positive-noise target-to-residual tracking theorem through strong learning; transverse- and antisymmetric-energy bounds after the actual residual changes; signed amplitude-clock and selected-residual defect estimates; a fixed returned weak cohort and its mass/clock matching; and complete field/probe accounting for every other ancestry group.

Including a group in H_C or c does not itself remove its angular field. A field decomposition must either retain that output explicitly or charge its current mass/output. An overlap between an ancestry set and an accounting set is not permission to count an output twice.

## Proposed later integration

Add the uniform Q2 endpoint lemma after the existing target-only crossing theorem. Add the secondary tail beside the initial-right-half-circle entry law, explicitly marking the ancestry difference. Add the whole-Q2 energy result to the transit-energy input ledger. No earlier theorem source is overwritten or automatically merged.

## Verification record

The source was compiled as standalone LaTeX. The rational endpoint inequalities were checked by exact arithmetic; no trajectory, numerical sign sampling, interval certificate, or saved simulation array was used. Compilation is a typesetting check, not formal proof verification. This is a new proof for independent mathematical review.
