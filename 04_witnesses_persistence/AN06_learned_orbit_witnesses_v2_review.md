# AN06 v2 review note: learning-threshold trade-off and canonical-offset witnesses

## Status and scope

**Separate revision for independent review.** This responds to the user's line-by-line AN06 v1 review and implements their learning-threshold/probe-offset observation. The initialized Theorems A and B remain unproved. No material has been merged into `THEOREM_A_ANALYTICAL_PROGRESS.tex`.

The deliverables are `AN06_learned_orbit_witnesses_v2.tex`, its compiled PDF, and this review note. Every internal label has the prefix `inc:AN06:v2:`. AN06 v1, AN02 v1, the handoff, the foundations, and the consolidated checkpoint are unchanged.

Sections 2–7 concern the **defined leading population system**. Section 8 is an exact, static Gaussian implication for a fully charted state. Neither the local witness theorem nor the static learning theorem establishes finite-noise trajectory or rate transfer.

The revision includes the exact canonical **scaled offset** `5π/9`. It does not establish coverage of the canonical trajectory at `q=0.05, S₀=2×10⁻⁴`, and it does not prove half-mass descent at that offset.

## 1. What changed

### 1.1 Theorem 3.1 is now the full descent family

The reviewed Theorem 2.2 and its coupled-region proof are unchanged apart from label prefixes. They supply, uniformly for `ρ ∈ [13/20, 7/10]` and every `s ≤ 0`,

\[
x<\frac34,\qquad v-y\le\frac85,\qquad
\Phi(\rho x)\le\frac{71}{100},\qquad
y'\le-\frac5{124}n(1-n).
\]

Applying the same completed-square estimate at general weak mass gives

\[
\mathcal E_\zeta'
\le \frac{3479}{31250}n^2
-\frac5{124}\left(\zeta-\frac34\right)n(1-n).
\]

Consequently, for any **fixed** `0 < n₀ ≤ 1/2`, strict descent holds at mass `n₀` whenever

\[
\boxed{\zeta>\zeta_{\rm req}(n_0)
=\frac34+\frac{215698}{78125}\frac{n_0}{1-n_0}.}
\]

The exact coefficient is `215698/78125 = 2.7609344`; the review's `2.761` is a rounded-up sufficient coefficient. No new invariant region or numerical trajectory is required.

Theorem 3.1 also states an explicit positive margin. Write

\[
\Delta_0=\frac5{124}(\zeta-3/4)
-\frac{3479}{31250}\frac{n_0}{1-n_0},\qquad
\Gamma_0=n_0(1-n_0)\Delta_0.
\]

Then, with `sρ(n₀)=ρ⁻² log(n₀/(1−n₀))`,

\[
\mathcal E_\zeta'(s)\le-\Delta_0 n(s)(1-n(s))<0
\quad(s\le s_\rho(n_0)),\qquad
\mathcal E_\zeta'(s_\rho(n_0))\le-\Gamma_0.
\]

These are sufficient thresholds, not exact boundaries of the reversal sector. The negative estimate for all earlier finite times does not supply a nonvanishing uniform margin as `n → 0`; the displayed fixed-mass witness does.

### 1.2 Explicit quarter-mass interval containing the exact canonical offset

Corollary 3.2 retains the former half-mass bound on `[4,5]` and adds

\[
\boxed{
\mathcal E_\zeta'(-\log(3)/\rho^2)
\le-\frac{65333}{124000000}<-\frac1{2000}
}
\]

uniformly for

\[
\rho\in[13/20,7/10],\qquad \zeta\in[87/50,7/4]=[1.74,1.75].
\]

The exact offset for the −85° unit probe at `q=1/20` is

\[
\zeta_c=\frac{5\pi}{9},\qquad q\zeta_c=\frac{\pi}{36}.
\]

The file gives elementary strict rational bounds placing `5π/9` inside this interval. At the separate rounded offset `349/200=1.745`, the displayed rate bound is

\[
\mathcal E_{349/200}'(-\log(3)/\rho^2)
\le-\frac{140041}{248000000}.
\]

The exact and rounded offsets are not treated as identical.

### 1.3 The common-window construction is recentered throughout

Section 5 now uses

\[
(\rho_c,\zeta_c)=\left(\frac23,\frac{5\pi}{9}\right),\qquad
s_a=-\frac94\log 3.
\]

The first transition to positive derivative is selected in `(s_a,t_g)`. The window radius uses `(s_*−s_a)/4`, not `s_*/4`. Every derivative supremum formerly taken over `[0,t_g]` is taken over `[s_a,t_g]` instead.

**This matters:** at the canonical offset, v2 proves `s_* > s_a`, not `s_* > 0`. It does not assume the crossover is after half-mass. The first gate hit remains after zero because the retained invariant region has `x<3/4<ζ` for all `s≤0`.

The mass slack is now

\[
\sigma=n_c(s_*-r)-\frac14>0.
\]

The positive local probe width is restricted by both distances from `5π/9` to the endpoints `87/50` and `7/4`. Thus the common-window rectangle contains the exact canonical offset in its interior and lies within the quarter-mass descent rectangle.

The parameter and time widths remain unevaluated positive analytical orbit functionals. The larger rectangle has a uniform quarter-mass witness; **common witness times are asserted only on the smaller local rectangle**. Its unevaluated width is not claimed to include the distinct rounded offset `1.745` as well.

Theorem 5.2 gives `nρ ≥ 1/4 + σ/2` on all of `J`. The conditional population theorem gives `N ≥ 1/4 + σ/4`, the same signed source margins as before, and a scaled rebound at least `γ₀r/4`.

### 1.4 Exact leading clock alignment

New Lemma 4.4 uses the exact leading mass equation `N′=λN(1−N)` to define the population's own half-mass clock:

\[
\tau_h=\tau_a+\lambda^{-1}\log\frac{1-N(\tau_a)}{N(\tau_a)},
\qquad s=\tau-\tau_h.
\]

When the trajectory extends to that time, it is the unique half-mass time. On the solution's interval,

\[
N(\tau_h+s)=n_\rho(s).
\]

For comparison with the coherent orbit at the **same ρ**, the metric is exactly

\[
\mathfrak d_{\rm al}=|M-1|
+\int(|x-X|+|y-Y_*|)\,d\mu_s
+\int(|u-U|+|v-V_*|)\,d\mu_w.
\]

AN3 need not deliver a separate weak-mass phase error. It still must deliver the strong mass, both families' angular information, and the outside-population control. Comparing orbits at different values of `ρ` still requires the weak-mass term because their logistic functions differ.

For a perturbed mass law `N′=λN(1−N)+r_N`, centering at `N(0)=1/2` instead gives the exact identity and bound

\[
\log\frac{N(s)}{1-N(s)}-\lambda s
=\int_0^s\frac{r_N(t)}{N(t)(1-N(t))}\,dt,
\]

\[
|N(s)-n_\rho(s)|\le\frac14
\left|\int_0^s\frac{r_N(t)}{N(t)(1-N(t))}\,dt\right|.
\]

This is a conditional scalar identity, not a bound on an actual finite-noise defect. All finite-noise and moving-boundary contributions must remain in `r_N`.

### 1.5 Static learning constants follow the quarter-mass threshold

The static bounds themselves are unchanged:

\[
|\mathsf m_p-M_p|\le25qR,
\qquad
\sqrt{2\mathcal L_p}\le |1-M_p|\sqrt{Q_p}+17qR.
\]

For the new population mass conclusions, assume `0<S₀≤1/2` and

\[
q\le\min\left\{1,\frac\sigma{100R},\frac1{100R},
\frac{13/20}{272R}\right\}.
\]

Proposition 8.1 then gives

\[
\boxed{\mathsf m_1\ge\frac12,\qquad \mathsf m_2\ge\frac14,
\qquad \mathcal L_p\le\frac{169}{196}\mathcal L_p(0).}
\]

The loss constant is obtained from

\[
|1-M_p|\le\frac34,\quad
\frac{17qR}{\sqrt{Q_p}}\le\frac1{16},\quad
\sqrt{2\mathcal L_p(0)}
=(1-S_0/4)\sqrt{Q_p+q^2}\ge\frac78\sqrt{Q_p}.
\]

Thus the squared ratio is `(13/14)²=169/196`, giving `κ₁=κ₂=27/196>0`. Gaussian tails are bounded, not set to zero. The earlier `25/36` loss ratio remains stated under its stronger half-mass premises; those premises are not attributed to the new canonical-offset windows.

### 1.6 Small-shape limitation and propagation arithmetic

The metric remark now contains the exact obstruction

\[
\mathfrak d\ge m_B|\bar y_B-Y_*|
\]

for every positive-mass strong subpopulation `B`. Therefore a non-small bridge cannot be hidden inside the coherent tolerance merely by estimating its moments more accurately.

Using the approximate bridge figures in the user's review only as an illustration gives `0.12 |7.2−(−0.6)|≈0.936`. That already exceeds `ε_*≤1/4`, without its input-coordinate contribution. These reported figures are not new empirical checks or proof premises. AN4 requires a split comparison object or a different nonperturbative inequality system.

Proposition 7.1 now combines its mass and distance coefficients as

\[
\max\{3,1+8R\}+32R=1+40R\le64R.
\]

The stated coarse propagation exponent `64R` is unchanged. This remains a fixed-window estimate, not the long-delay resident passage argument.

## 2. Proof contracts and dependencies

| Result | Assumptions and dependencies | Conclusion and status |
|---|---|---|
| Theorem 3.1, `familytheorem` | Reviewed v1 Theorem 2.2; selected branch and exact coherent probe law; `ρ∈[13/20,7/10]`, `0<n₀≤1/2` | Explicit descent criterion and fixed-mass margin. Exact within the defined coherent leading system. |
| Corollary 3.3, `postthreshold` | Theorem 3.1; checkpoint `pa:limitreversal` and positive lag | A competition crossover strictly after mass `n₀`, with both source signs on an interval. Leading system only. |
| Lemma 4.4, `clockalignment` | Exact leading logistic law, or explicitly perturbed scalar law; `0<N<1` | Exact own-clock equality in the leading model; conditional logit defect identity otherwise. |
| Theorem 5.2, `uniformtheorem` | Quarter-mass witness at exact central offset; smooth branch dependence; gate-aware rate estimates | Common local parameter/probe/time margins with mass strictly above `1/4`. All constants are analytical functionals. |
| Theorem 6.1, `populationtransfer` | Leading population lies in the compact chart class and satisfies the specified first-moment tolerance | Maintained source signs, opposite total-rate windows, and rebound. Conditional, not initialized. |
| Proposition 8.1, `staticproposition` | Entire exact state lies in the bounded charts; displayed mass, noise, and initialization bounds | Exact response/loss bounds. Static, not a trajectory or source-rate theorem. |

The unchanged checkpoint dependencies are `pa:branch`, `pa:weakroot`, `pa:atomiclag`, `pa:atomicrates`, `pa:limitreversal`, `pa:leading`, `pa:masslaws`, and `pa:assembly`. The relevant leading equations are restated in the standalone proof. The comparison initialization remains `f₀(X)=S₀X/4`.

## 3. Audit points

**Region and first-exit proof.** Section 2 is identical to the reviewed v1 section except for its label prefix. No face is enlarged and no v1 slack is spent a second time. In particular, the tight `x=3/4` face remains unchanged.

**Signs and divisions in the trade-off.** Division is only by `n(1−n)>0` at finite selected-orbit times with `n≤1/2`. Multiplying the negative output derivative by the lower bound `ζ−x≥ζ−3/4>0` has the correct direction. The completed-square bound does not assume `x′≥0`. Error negativity follows from `ζ>x>y`.

**Crossover selection.** The positive-derivative set is nonempty by the finite gate hit and the negative witness error. Analyticity makes the first transition an isolated finite odd-order zero. No simple-zero or uniqueness assumption is added. Every time-radius restriction is measured from the quarter-mass witness, not from zero.

**Uniformity.** The smooth parameter-dependence proof is retained. `σ>0` follows from `s_*−r>s_a`. The parameter-radius restrictions preserve both mass and gate gaps; per-source perturbation budgets still sum to at most one quarter of the total-rate margin. The local probe width is strictly positive because the exact center lies strictly inside `[1.74,1.75]`.

**Gate handling.** The existing nonunit-mass source law and gate-aware robustness proof are unchanged. Boundary atoms remain in the inactive-mass bound. The derivative-of-error identity is almost everywhere along regular characteristic solutions; no new pointwise gate regularity claim is made.

**Clock handling.** The own-clock cancellation applies to a fixed-ρ leading comparison. It does not remove mass differences when comparing different parameters. The perturbed logit identity assumes `0<N<1` on the whole integration interval; continuity supplies a positive denominator bound on each fixed compact interval, not a uniform bound over an arbitrarily long near-zero-mass sojourn.

**Static learning.** The changed threshold requires the changed loss arithmetic and the stronger `1/16` residual allowance. Both are incorporated. The reference initial loss is the isotropic initialized loss, not the zero-output loss. No mass is silently discarded from the state representation.

**No new hidden reachability assumption.** The compact support, first-moment proximity, and exact-state hypotheses remain explicit. They are the targets for AN2/AN3/AN7, not conclusions from initialization.

## 4. Open residue and the next mathematical target

The limiting witness gap is now closed at a fixed quarter-mass threshold for an interval containing the exact canonical scaled offset. Further sharpening toward half-mass at that offset is optional, not needed for the first Theorem A.

The next main task remains the coupled initialized strong-contraction and weak-capture argument. Its output must support nonlinear resident passage and control the full population, not merely one arriving cohort. AN3 should compare the leading population to the selected orbit in the population's own weak half-mass clock.

The small-shape route must meet the angular/strong-mass part of `ε_*` and supply separate budgets for uncharted population. A non-small bridge needs the separate AN4 comparison; no sharpening of the same small-deviation tolerance alone addresses that case.

Uniform finite-noise rate transfer and long-delay error control remain open. The conditional scalar clock defect shows one of the quantities that such a proof would need to bound.

AN02's Riccati refinement, bulk/reservoir transition, and capture laws are not proved or revised here. The planning assumptions

\[
\log(1/S_0)/\log(1/q)\to\infty,
\qquad q^2\log(1/S_0)\to0
\]

are retained as scale planning, not as an initialized capture theorem.

## 5. Label map and proposed integration after explicit approval

All unchanged labels map by replacing `inc:AN06:v1:` with `inc:AN06:v2:`. The exceptions or changed meanings are:

| v1 label suffix | v2 target | Change |
|---|---|---|
| `halfdescent` | `descentfamily` | Section 3 is now the threshold/offset family. |
| `halfdescenttheorem` | `familytheorem` and `halfdescenttheorem` | Theorem 3.1 is generalized; the former half-mass conclusion is retained in Corollary 3.2. |
| `posthalf` | `postthreshold` | Crossover after prescribed mass `n₀`, with half-mass as a special case. |
| `commonwindows`, `constants`, `rectangle`, `uniformtheorem` | Same suffixes | Exact canonical center and quarter-mass slack replace the old center and half-mass slack. |
| `populationtransfer`, `populationmargins` | Same suffixes | The weak mass floor changes from `1/2` to `1/4`; rate budgets and rebound form are retained. |
| `qlearn`, `learningconclusion` | Same suffixes | Quarter-mass static response threshold and `169/196` loss ratio. |

New principal labels are `tradeoffconstants`, `familytheorem`, `familyrate`, `familymargin`, `quarterrate`, `roundedrate`, `clockalignment`, `halfclock`, `aligneddistance`, and `logiterror`.

After review and explicit approval, Sections 2–3 belong after `pa:limitreversal`, updating its limiting learning-witness limitation. Preserve the broader original selected-orbit reversal result. Sections 4–7 are conditional AN3/AN6/AN8 interfaces; Lemma 4.4 specifies the preferred leading comparison clock. Section 8 belongs with AN5. AN2, AN3, AN4, and AN7 must not be marked complete by that merge.

## 6. Preparation and provenance

No GitHub access, numerical trajectory integration, reference-array comparison, interval arithmetic, or trajectory certification was used. Source comparison, exact rational arithmetic, LaTeX compilation, and rendered-page inspection were used to prepare the files. These checks do not constitute machine verification of the analytical proofs.

The retained Section 2 and the existing Section 4 rate proofs were compared directly with v1 and found unchanged apart from the new label prefix. Source hashes below identify the unchanged working inputs; they are not mathematical premises.

```text
81e1b2ec8001241b4d246a65cba09ec57e6803e92c4f158fac1e83c30d1393a0  AN06_learned_orbit_witnesses_v1.tex
b9b169764339017da37209eca84f17154b73c1a2de79d61c707cf2f550763e1b  THEOREM_A_ANALYTICAL_PROGRESS.tex
eefd557e0c725c87ea6b41d0d144b92e14f895f0b7f0095d509915b14a9de3f1  RELU_POPULATION_FOUNDATIONS_v2.tex
842806cd0ae9b7e33050fd59dd18818eed01230c188494609d7100513da39504  THEORY_HANDOFF_ANALYTICAL_A_B.md
```
