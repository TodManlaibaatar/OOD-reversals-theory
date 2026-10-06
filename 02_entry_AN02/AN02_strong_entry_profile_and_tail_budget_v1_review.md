# AN02 strong entry profile and tail budget — review note v1

## What is new

The increment proves the strong-side two-stage matching law for the **exact positive-noise target-only flow**, including initial Q1 labels all the way up to the weak axis. It does not just insert the outer and inner rates into an ansatz.

Let ω=(1−λ)/2, d=1/2−α, s=d/ω, p=3/s, and ε=q^(−s)e^(−dT). At a late target-only time T with T≥(2/ω)log(1/q)+C and q²T≤1, the upper Q1 sector obeys

- input displacement from the **exact** attracting scaled direction a_q: comparable to ε(cos θ₀+q)^(−s);
- radial weight: comparable to S₀e^T(cos θ₀+q)²;
- normalized upper tail: comparable to (ε/z)^p on a specified intermediate range, with a finite cutoff at order εq^(−s).

The rest of Q1 is within O(ε). A companion Q4 comparison has s₋=2d, a smaller prefactor ε₋=q^(−s₋)e^(−dT), and a steeper tail index 3/s₋. Consequently the same upper/lower tail theorem applies after normalizing over the full initial right half-circle. This still excludes any recruited ancestry from the initial left half-circle. The exact center satisfies a_q=a_ρ+O(q²), but that shift must not be included in the centered shape radius.

The increment also proves an original-state bound on an arbitrary outside population: scaled angular field and receiver derivative are at most 40μ_B/q. This is an instantaneous bound on its **current radial mass**, not a bound on how that mass evolves.

Finally, it restates the escaped-tail power test as a conditional theorem. At κ=10 and a vanishing output core radius q^(1/20), the tail-inclusive exponent has the uniform lower bound 4561/35006 on ρ∈[13/20,7/10]. This is a compatible algebraic matching target, not an initialized parameter region.

## Proof contracts and labels

| Label suffix under `inc:AN02:profile:v1:` | Result | Scope |
|---|---|---|
| `root` | Exact target-only attracting center, σ_q=d+O(q²), and uniform exponential approach | Exact finite-noise target-only flow |
| `arrival` | T_L=ω^(−1)log[1/(q(cos θ₀+q))]+O(1), uniformly through the initial weak-axis layer | Exact finite-noise target-only flow |
| `entry` | Radial ancestry weight, full-Q1 core bound, and upper-sector two-sided tail profile | Exact finite-noise target-only flow |
| `rightcircle` | Q4 matching and the combined initial right-half-circle profile | Exact finite-noise target-only flow |
| `cost` | Outside mass μ_B costs O(μ_B/q) in the exact scaled field and its receiver derivative | Exact original-state estimate |
| `rational` | Tail-inclusive κ=10, χ=1/20 arithmetic | Conditional transfer/power test |

Dependencies: foundational P1/P4/P5; the exact coordinate and angular formulas in `AN02_Q2_profiles_and_localized_tracking_v1.tex`; the local passage multiplier in `AN03_local_rate_mean_tracking_v1.tex`. No numerical trajectory, fitted slope, or repository access is used.

## Important qualifications

The tail law is not globally a pure power. At cos θ₀≲q, positive Gaussian leakage regularizes both its weight and its arrival clock. The finite cutoff is part of the theorem.

The initial “cos²” description is recovered away from that layer, but is not a uniform relative approximation there. Likewise, centering at a_ρ rather than a_q can create an O(q²) apparent radius larger than the true centered radius.

An upper growth bound does **not** imply that every label above δ/G leaves the local region. The proof uses the cutoff only to identify a sufficient safe core and bounds all other labels as a potentially adverse complement. No lower escape claim is made.

The exponent pE>1 is sufficient for the proposed uniform μ/q charging scheme. It is not a necessary threshold for the dynamics, and does not exclude sharper signed or time-resolved estimates.

## Audit points

1. **Uniform angular error integration.** The outer speed correction is integrated as K(−z)/z². A merely small constant relative error multiplied by log(1/q) would not prove the displayed exponent.
2. **Initial weak-axis endpoint.** The rescaled speed tends to [K(z)−λz]/2, strictly positive on a fixed compact z-interval. The radial lower bound at cos θ₀=0 is obtained by a positive source over a short interval, not by dividing by U₁(0).
3. **Exact center.** The C² local expansion and strict derivative bound justify the root and rate. Exponent replacement costs O(q²[T+log(1/q)]), bounded under the time guard.
4. **Radial bound.** The gate-source time integral is uniformly bounded, with the long final interval paid by an exponentially small Gaussian tail times T≤q^(−2).
5. **Profile normalization.** Radial mass is normalized only after proving total Q1 mass is comparable to S₀e^T. The power p=3/s comes from the weighted initial-label integral, not the unweighted angular law.
6. **Outside field.** The polar angular weight is bounded by 16/q for each cluster, and both gate endpoints are included in its derivative. Receiver differences therefore pay a multiplicative shape defect rather than an arbitrary additive split source.
7. **Rational extrema.** The function p(E−χ)−1 is minimized jointly in λ and P. The value of s at maximal P is not its independent maximum; the proof does not combine incompatible extrema.
8. **Tail mass transport.** A uniform bound on the complement’s future radial mass relative to its entry fraction is a separate assumption. Recruitment can violate an unchanged strong-family mass law.

## Open residue

The main missing initialized estimates are: tracking the original field through strong learning closely enough to transfer the target-only radius and radial profile; controlling distortion of the radial weights; bounding the future mass of excluded/recruited ancestry; supplying the amplitude and selected-residual clock defects; and controlling other outside sources. The target-only theorem itself does not establish strong learning in the original flow.

If excluded mass acquires a factor q^(−r_m), that power must be subtracted from the tail budget. The κ=10 statement does not conceal such a factor in its constant.

## Proposed later integration

Place the target-only theorem after the current AN02 target-only coordinate/arrival section. Put the exact outside-field estimate with the AN7 field-defect budget. Replace the κ=15/2 *conditional matching example* by the tail-inclusive κ=10 example only after stating all additional transport hypotheses. Do not replace the earlier theorem itself or merge this increment without approval.
