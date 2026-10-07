# Review: overlap-window profile transfer, v1

**Disposition: S1, step 1 closes using the proved PROFILE and early-comparison results.** The new theorem is an exact original-flow result for the initialized model at the overlap time. It does not assume the open LCRC/S1 entry contracts. Work stops after this first link: no M-clock passage, capped radial gain, bridge argument, or consolidation was undertaken.

The paired source is `AN02_overlap_window_profile_transfer_v1.tex`, with unique label prefix **`an02owptv1:`**. All prior files remain unchanged. The user reports LCRC reviewed and verified; that status is recorded without claiming a new independent review.

## Main result and explicit powers

Fix the same ratio box and `S0=q^10`, and choose a fixed sufficiently large `C_m` from PROFILE's common arrival/time guard:

\[
t_m=\frac2\omega\log(1/q)+C_m,\qquad
\sigma=10-\frac2\omega,\qquad\zeta=\sigma-1.
\]

Theorem 3.1 (`transfer`) selects the actual original-flow reference characteristic with initial label `alpha_c=q a_q`. Its target-only counterpart stays at the exact angle `q a_q`. The actual reference is allowed to move and become unaligned.

For every right-half-circle label, let `h_x,h_y` be the two scaled original angular displacements from this same-field reference and `h_hat` the target-only displacement from `a_q`. Then

\[
h_x=\widehat h\,e^{\varepsilon_x},\qquad
h_y=\widehat h\,e^{\varepsilon_y},\qquad
|\varepsilon_x|,|\varepsilon_y|\le Cq^\zeta,
\]
\[
m(t_m,\alpha)=\widehat m(t_m,\alpha)e^{\varepsilon_m},
\qquad |\varepsilon_m|\le Cq^\sigma.
\]

At the reference both displacements are exactly zero. The same relative bound holds for **every pair** of initial labels; there is no minimum-separation assumption.

| Quantity at `t_m` | Explicit scale |
|---|---|
| Total-mass upper envelope | `e^(C_m) q^sigma exp(2q^2 t_m)` |
| Right-half-circle radial mass | `~ e^(C_m) q^sigma` |
| Original / exact target radial-weight distortion | `exp(O(q^sigma))` |
| Original / exact target pairwise angular distortion | `exp(O(q^zeta))` |
| Scaled actual-reference shift from `a_q` | `O(q^zeta)` in each coordinate |
| Q1 profile scale `epsilon_m` | `e^(-d C_m) q^s` |
| Q1 upper-half displacement profile | `~ e^(-d C_m) q^s (cos(alpha)+q)^(-s)` |
| Whole-right-half-circle radial weight per label | `~ e^(C_m) q^sigma (cos(alpha)+q)^2` |
| Radial weight for labels with `cos(alpha)=O(q)` | `~ e^(C_m) q^(sigma+2)` |
| Q1 / full-family maximal displacement | `O(e^(-d C_m))` |
| Q4 profile scale | `e^(-d C_m) q^((1+lambda)s)` |
| Q4 displacement profile | `~ e^(-d C_m) q^((1+lambda)s) (cos(alpha)+q)^(-(1-lambda)s)` |
| Q4 maximal displacement | `O(e^(-d C_m) q^(2lambda s))` |
| Full-family tail exponent | `p=3/s` |
| Q4 upper-tail exponent | `3/((1-lambda)s)` |

Here `~` means the source's two-sided comparison `asymp`, not asymptotic equality with coefficient one. The multiplicative errors tending to one are relative to the **exact target-only profile and weights**. PROFILE's existing fixed comparison constants are retained in the explicit power laws.

The rational endpoint bounds are

\[
\frac{110}{51}\le\sigma\le\frac{710}{231},\qquad
\frac{59}{51}\le\zeta\le\frac{479}{231}.
\]

They follow by monotonicity of `4/(1-lambda)` and direct endpoint substitution, without numerical checks. Thus the mass is much smaller than any fixed positive early-comparison threshold `delta`, and the multiplicative distortion vanishes uniformly on the box.

## Central analytic argument

The physical receiver field is `F=F^0-F^f`, with target matrix `A_theta` and output matrix `C_f`. PROFILE Proposition 4.1 supplies the global matrix estimates

\[
\|C_f\|\le a_*S,\qquad \|\partial_\theta C_f\|\le32S/q.
\]

Consequently its scaled velocity and receiver derivative are `O(S/q)`. Its unscaled receiver derivative has the same `O(S/q)` bound globally, so the proof covers the interval **before** all labels enter the chart as well.

The target boundary identity `A'_theta a_theta=0`, symmetry of `A_theta`, and the polar estimate `||A'_theta||<=32/q` give the following target-aligned receiver Jacobian at the comparison angle:

\[
J_0=\begin{pmatrix}-g&h\\h&-g\end{pmatrix},\qquad
g=a^TAa,\quad h=(a^\perp)^TAa^\perp\ge0.
\]

The already-proved absolute early comparison is used **only to compare Jacobian coefficients**. The off-alignment boundary term is `(b-a)^T A'_theta a_perp`, bounded by `C|psi-theta|/q`; no second derivative of `A` is needed. Hence the original Jacobian along each label differs from `J_0` by `O(Sbar/q)`.

Let `p_hat=partial_alpha theta_hat>0`. It satisfies `p_hat'=(h-g)p_hat`. Dividing the original two-component label tangent by `p_hat` gives

\[
w'=h\begin{pmatrix}-1&1\\1&-1\end{pmatrix}w+\mathcal E w,
\qquad w(0)=(1,1),\qquad \|\mathcal E\|_\infty\le C\overline S/q.
\]

The unperturbed propagator has nonnegative entries and row sums one. Its infinity norm is exactly one, irrespective of the length of the logarithmic interval. Variation of constants therefore gives

\[
\|w-\boldsymbol1\|_\infty
\le\exp\!\left(\int\|\mathcal E\|_\infty\right)-1.
\]

This is the displayed proof of the central multiplicative inequality. Integrating positive label derivatives between any two labels transfers their separation. It does not presume positivity of the original field's cross derivatives, nor a cross-population comparison principle.

The initially convenient envelope budget is

\[
\int_0^{t_m}\overline S/q
=\frac{\overline S(t_m)-q^{10}}{q(1+2q^2)}=O(q^\zeta).
\]

The new source also checks the suggested actual-mass budget: PROFILE's positive first-coordinate growth on a fixed Q1 subinterval and the early radial comparison give `Sbar<=32 S` on this interval for small `q`. Thus the same distortion is `exp(O(int S/q))`. No later strong-stage mass law is used.

## Reference and probability-profile audit

- The reference is the actual characteristic launched at the analytically specified, fixed initial label `q a_q`. It is in the original population's field; no external comparison force is substituted for its evolution.
- Its scaled position is `a_q+O(q^zeta)` in each component. This additive displacement is retained as reference data, not absorbed into the multiplicative profile error.
- At `rho=7/10`, `zeta=59/51`. PROFILE's rational bound `P_rho<153/250` gives `s>17503/12750>14750/12750=59/51`. Thus the available absolute-error budget decays more slowly than the core scale `q^s`. This is a statement about what that upper budget can prove, not a lower bound on the actual angle error.
- Actual input and output angles are not assumed equal. Each centered displacement is compared multiplicatively to the same exact target displacement; the original joint profile is therefore controlled without imposing alignment.
- Corollary 3.2 (`tail`) states a precise normalized-measure sandwich. If `D=|h_x|+|h_y|`, `D_hat=2|h_hat|`, and `r_m=O(q^sigma)`, then
  \[
  e^{-2r_m}\widehat\nu\{\widehat D>e^{\eta_m}z\}
  \le\nu\{D>z\}
  \le e^{2r_m}\widehat\nu\{\widehat D>e^{-\eta_m}z\}.
  \]
  The `2r_m` accounts for both label weights and their normalizing masses. This is stronger and more precise than asserting an unchanged fitted density.
- The lower power tail is claimed only on PROFILE's finite range, with fixed range constants adjusted once. It is not asserted arbitrarily close to the cutoff. The tail is zero beyond a fixed multiple of `epsilon_m q^(-s)`.

## LCRC/S1 contract ledger

The user reports LCRC reviewed and verified as a conditional implication. This increment supplies the following **earlier-time data**, not its later passage-entry contracts wholesale.

| Contract or datum | What this increment supplies |
|---|---|
| Original strong joint profile | Supplied at `t_m`, relative to an actual same-field reference, including Q1/Q4 branches, finite cutoff, and tail index `3/s`. |
| Strong radial weighting | Supplied at `t_m`, with pointwise `exp(O(q^sigma))` comparison and normalized-measure control. |
| Strong family in a bounded joint chart | Supplied at `t_m`, with `abs(theta)+abs(psi)<=2(L+1)q`; continued chart retention is not proved. |
| Exact-center reference data | The target reference uses exact `a_q`; the original reference has the explicitly retained `O(q^zeta)` displacement. It is not asserted to equal `a_q`. |
| Strong mass | `M_R(t_m) ~ e^(C_m)q^sigma`, still small. No saturation, strong-learning clock, or passage mass law is supplied. |
| Cartesian ratio `<=C0` on later `G+` and `<=C_clk q^(1/8)` on the weak clock | Not supplied at LCRC's `t0`; those groups involve Q2 entry and subsequent strong-stage dynamics. |
| `z>0`, `abs(a)/z<=1/4` on LCRC cohorts at `t0` | Not supplied as LCRC entry data. The present reference/profile theorem concerns the original right-half-circle strong family at `t_m`. |
| `J_G(t0)<=C_J q^3` | Not supplied. No whole-Q2 transverse-energy transfer or later transport is performed. |
| `H_Cl(t0) ~ q^(10(1-lambda))` | Not supplied. No weak seed or Q2 amplitude calculation is added. |
| Secondary entry profile at `t0` | Not supplied. The right-half-circle strong profile here is not the recruited Q2 secondary profile. |
| `int abs(1-kappa1)<=B_s` with guard-independent order-one constant | Not supplied; the M-clock/strong-learning stage remains open. |
| Later core chart and core mass budgets | Only their overlap starting data are supplied. Later retention and mass control remain to be proved in stopped form. |
| Chart-group retention, outside `mu_B=o(q)`, S2 distance/gain | Not supplied; no later escaping-label or outside-population budget is inferred. |

In particular `t_m` is not silently relabeled `t0`. The mass at `t_m` is still `q^sigma`, while the later strong-stage transition is essential to the missing entry contracts.

## Order-one constants for later assembly

The roadmap's assembly requirements were read before the proof. All constants in this increment arise before LCRC's guards and are independent of `(B,M,K_Y)`. The order-one quantities that must be carried, rather than discarded as part of an `o(1)` error, are:

1. **The deterministic time offset `C_m`.** It contributes the explicit order-one factors `e^(C_m)` in radial mass and `e^(-d C_m)` in both profile scales and cutoffs. Its value must stay fixed as `q` tends to zero. It is chosen from PROFILE's arrival guard, not from a trial residual constant.
2. **The overlap chart constant `L` and joint radius `R_m=2(L+1)`.** They come from PROFILE and the fixed overlap offset. They are guard-independent. This supplies a valid initial radius; it does not license a later radius `R=R(M)` or prove that this radius persists through strong learning.
3. **The exact center and fixed ratio-dependent coefficients.** `a_q`, its limiting `a_rho`, `omega`, `d`, `s`, and the tail exponents are retained explicitly. The same-field reference retains its two coordinates; it cannot be reset to the target center when measuring fine shape.
4. **PROFILE's order-one comparison and range constants.** These include upper/lower displacement and radial-weight constants, the tail constants, the lower-tail range thresholds, and the finite-cutoff constant. Their ratios can enter later normalized entry laws and tail budgets. They are not shown to converge to one.
5. **The radial normalization coefficient.** `Mhat_R/(S0 e^(t_m))` stays between fixed positive bounds by PROFILE. Its order-one value is not identified here and is not replaced by one. Original-to-target normalization changes it only by `exp(O(q^sigma))`.
6. **Any fixed later choice of a strong core from this profile.** A cutoff multiplier or fixed quantile chosen later can enter its initial radius, mass fraction, and tail prefactors at order one. This increment makes no such later choice and assigns no invented value to it.

The universal Gaussian/Jacobian comparison constants, `a_*`, and the constants in the early comparison enter the **new transport defects** only multiplied by `q^zeta`, `q^sigma`, or `q^2 log(1/q)`; they do not introduce a new order-one shape drift. Nevertheless their uniformity is stated and proved. PROFILE's fixed comparison constants remain separate from these vanishing distortions.

For LCRC specifically, the roadmap identifies `R`, `M_K`, `B_s`, and `c_b` as the order-one assembly inputs. The present proof is independent of the residual guards and supplies overlap chart/mass data, but it neither fixes nor proves the later `R,M_K,B_s,c_b` budgets. Future proofs must supply those budgets on stopped intervals with guard dependence only in `o(1)` terms. Nothing here removes that obligation or hides it in a constant.

## Analytic and regularity audit

- **Early-comparison guard:** `Sbar(t_m)=o(1)` verifies the source alignment guard before it is used. PROFILE's time condition and `q^2 t_m<=1` are verified analytically at the chosen time.
- **Tangent smallness:** the only new perturbation smallness is `int ||E||<=C Lambda(t_m)<=1/4`, deduced from the displayed positive power of `q`; it is not an added trajectory hypothesis.
- **Same-field differentiation:** initial-label differentiation evaluates different receivers in the same actual time-dependent population field. No derivative of the donor measure with respect to its own perturbation is introduced.
- **No hidden cooperativity:** the target-normalized two-state generator is contractive because `A_theta` is positive semidefinite. The original cross derivatives need not be nonnegative. Their sign is not assumed.
- **No unbounded Hessian requirement:** the Jacobian comparison uses `A'_theta a_theta=0` and one `O(1/q)` derivative bound; it does not use an uncontrolled second receiver derivative near a Gaussian gate layer.
- **Divisions:** `p_hat>0` follows from its scalar variational exponential. Pair differences are divided only when initial labels differ; the exact zero at the reference is handled separately. Positive initialized radial mass justifies the logarithmic weight comparison and nonzero normalizing masses.
- **Integrals:** receiver differentiation follows the Gaussian boundary formula with continuous angular integrands. Standard finite-horizon characteristic regularity yields the label variational equation. All cohort integrals use fixed initial labels and finite positive radial mass. There is no moving-mask flux or unproved infinite-time exchange.
- **Uniformity:** all estimates are uniform for rho in the fixed compact box, after fixing `C_m`. The q-dependent reference label is selected analytically at initialization and then held fixed in time.
- **No numerical premise:** rational endpoint substitutions and displayed analytic inequalities establish the parameter margins. No interval arithmetic, grid checks, saved trajectories, numerical integration, experiments, or fitted exponents were used.

## Source provenance

The updated roadmap was fetched read-only from the repository. Its filename remains `UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md`; the fetched content is **Version 1.2**. S0's retained inputs and assembly requirements, followed by S1, were read. Proof-source bytes were fetched and their versions identified before use.

| Repository path | Git blob SHA | Dependency |
|---|---|---|
| `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | `e21d831258c6e73df4f0632ae8d6cddc11fd89c6` | v1.2 S0 retained inputs / assembly requirements; S1 step 1 |
| `02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex` | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` | `inc:AN02:profile:v1:` + `root`, `arrival`, `entry`, `rightcircle`, `cost` |
| `01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex` | `cb458c933aa043cf0188fd11c46bf4246ffc91d8` | `pa:earlybounds`, `pa:targetcomparison`, `pa:finiteqorder`; exact analytic portions only |
| `01_foundations/RELU_POPULATION_FOUNDATIONS_v2.tex` | `a5c557d56fe5753532a600f8f238a74f8091da9b` | Balanced angular characteristic equations and finite-noise gate-boundary regularity |
| `03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex` | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` | Section 1 and Theorem 4.1 define later contracts; not a premise to the overlap proof |

The proposed eventual location is after PROFILE's target-only entry law, as its original-flow overlap transfer, before the still-open strong-learning continuation. No prior result is replaced, so no replacement label map or consolidation is made.

## Validation and stop

The final `.tex` compiled successfully with the built-in LaTeX compiler. A static audit found 26 unique labels, all with prefix `an02owptv1:`, and no unresolved local references. Compilation and reference checks are typesetting aids, not mathematical evidence. No subagent or new independent mathematical review was used.

The central inequality closes without an unlisted hypothesis. The theorem and review pair are delivered, and work stops at S1 step 1 as requested.
