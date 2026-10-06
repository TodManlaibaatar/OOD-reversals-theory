# AN03 weak transit forcing and selected-orbit tracking — review note v1

## What is new

Within the full **leading** population at M=1, the square-root weak forcing is proved from incoming moments:

|V|+K_w ≤ C_w N + sqrt(N N_*),

where N_*=N₀(E u₀,+ +3E|v₀|)². The result does not require uniformly bounded incoming weak coordinates. Its time integral up to fixed n_b is explicit and contains no initialization-delay logarithm.

For nonnegative returning inputs, a strict boundary margin keeps u≥0. All weak labels then contract pairwise at the exact factor sqrt(N₀/N). This controls weak concentration.

The file goes further: it compares the weak population with the selected orbit itself and closes the feedback with the stable strong mean. Under a supplied small strong shape/tail distance budget, the error at n_b tends to zero when sqrt(N₀) times the incoming weak angular error tends to zero. A diverging incoming weak spread is permitted.

## Scope and contracts

All labels use prefix `inc:AN03:weak:v1:`.

| Suffix | Conclusion | Assumptions beyond the leading characteristic solution |
|---|---|---|
| `forcing` | CN+sqrt(NN_*) pressure and integrated bound | M=1, Y≥0, bounded rho K_s, closed fixed weak family |
| `concentration` | Preserved u≥0 and exact pairwise contraction | u₀≥0 and a strict weak boundary margin |
| `Wineq` | Population-to-selected-orbit distance controlled by strong moment error | Nonnegative actual and selected weak inputs; exact same logistic clock |
| `selection` | Coupled strong mean and weak population approach selected orbit at n_b | Small supplied full strong first-moment distance to a same-field reference, explicit small-gain and guard conditions |

The theorems are stated in the characteristic class with bounded support on each compact time interval. The incoming support may diverge as q or S₀ varies. No separate existence theorem for arbitrary unbounded initial laws is asserted.

Dependencies: checkpoint `pa:leading`, `pa:masslaws`, `pa:overlap`, `pa:spectra`, `pa:branch`; AN06 v2 for the selected branch’s positive weak input; AN03 local-rate v1 for the same-field strong reference and fixed-core/weighted-tail framework.

## The coupled selection estimate

Let E_s be the strong reference’s Euclidean distance from the selected strong atom, W_p the weak population’s L^p distance from the selected weak atom, D_s the full normalized strong first moment about its reference, and D_s≤d₀. Set A₀=sqrt(N₀)W_p(t₀).

Theorem `selection` gives, with constants independent of N₀,

E_s(t) ≤ K₀[E₀ exp(−m₀(t−t₀)) + d₀ + A₀ sqrt(N(t))].

At N=n_b, W_p is bounded by a constant times

A₀/sqrt(n_b) + E₀ exp(−m₀ T_b) + d₀ + A₀ sqrt(n_b).

All constants and denominators are displayed in the proof. If N₀→0, A₀→0 and d₀→0, the strong mean and weak population errors at n_b vanish even when admissible E₀ is fixed and W_p(t₀) diverges.

This is not a statement that small pairwise spread determines the correct mean. The selected branch comparison is a separate part of the proof. Its phase is fixed by the population’s own logistic mass clock.

## Audit points

1. **M=1 is a hypothesis.** It removes the weak cross-dependence on v through (1−M), and permits the exact v-mean/centered decomposition. The original flow needs its M−1 defect budget.
2. **V is total mass weighted.** V=N E v. Averaging v′ gives 2vbar′=rho K_s−λvbar; centered deviations decay at λ(1−N)/2.
3. **Returning inputs.** The u-positive-part estimate holds for any sign. Actual nonnegativity needs u₀≥0 and the strict boundary margin. It is not inferred from a positive mean.
4. **Donor sign and contraction.** On u≥0, (u+Y)phi(u)≥0 and W′(u)≥0. Therefore the scalar derivative is at most −λ(1−N)/2. This is a same-field statement.
5. **Selected-orbit forcing.** The difference between W(U_*) and N K(U_*) is bounded using the donor Lipschitz constant of F, not discarded. It contributes N W_p/2 to the comparison equation.
6. **Exact half-power.** The homogeneous weak multiplier is sqrt(N(s)/N(t)) times exp((1/2)∫N). The latter is bounded by a constant depending on n_b, not by exp(C n_b T_b), which would lose the sharp initialization power.
7. **Mean closure.** The strong coherent Jacobian is symmetric near the resident. Its stability and the donor perturbation estimate give E_s′≤−gE_s+C_s(D_s+N W_p).
8. **Small gain.** The return coupling has the small factor n_b. The explicit condition Theta≤1/4 closes the mean and weak errors without assuming either mean trajectory.
9. **Time-dependent bounds.** The proof retains the decaying E₀ transient and the growing A₀sqrt(N) term, rather than paying a supremum of the large incoming W_p.
10. **Tail budget type.** This selection theorem uses a pointwise D_s≤d₀. The previous theorem’s integrated tail control is not silently promoted to this stronger hypothesis.
11. **p=infinity.** This case gives actual uniform weak-coordinate proximity at n_b. For p=1 alone, small first moment does not imply bounded support or sufficient control of every probe rate.

## Open residue

The original population still must reach a suitable return/capture regime, with its positive-input condition or an analytically controlled alternative. The law N_*≈q^[2(1−λ)/λ] is not proved here. Nor is the connection between exact growing amplitude and closed leading weak mass supplied automatically.

The strong profile/tail estimate must supply the small pointwise first-moment budget in this theorem, or a sharpened version must use the available weighted integral directly. Finite-noise and M−1 errors, changing radial label weights, recruitment, uncharted population, and final probe-rate/strip transfer remain outside this theorem.

The passage from n_b to the AN06 windows is finite and can use ordinary continuous dependence once the full relevant state is in the required chart/tail class. This increment supplies weak mean/shape closeness, not the remaining strong outside-population or high-moment hypotheses.

## Proposed later integration

Add the forcing and weak concentration results after the local-rate passage theorem. Add the coupled selection theorem as the weak-angular/strong-mean part of the AN3-to-AN06 interface. It replaces the need to assume an already close weak mean at n_b, conditional on the explicit earlier entry and strong-distance inputs. Keep the exact finite-noise matching task separate. No consolidation is performed.
