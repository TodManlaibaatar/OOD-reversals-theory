# AN03 v1 review: two-sided passage and Q2 ancestry retention

**Proof source:** `AN03_two_sided_passage_and_Q2_retention_v1.tex`  
**Compiled review copy:** `AN03_two_sided_passage_and_Q2_retention_v1.pdf`  
**Unique label prefix:** `inc:AN03:ret:v1:`  
**Date:** October 3, 2026  
**Status:** separate proof increment for independent review. Neither the checkpoint nor any reviewed increment is changed.

## 1. What is new

The main result is an **all-label nonlinear spread estimate through weak half-mass in the full leading population**, including lower-side and mixed-order labels. It does not replace the population by a passive tail in a coherent field.

The receiver and donor terms are combined before estimating the lower side. This gives the exact cancellation

\[
\Pi(r)-\Lambda_-(r)=M(X_s-r),
\]

and ultimately

\[
D^+D\le\left[-\frac{(1-\lambda)(1-M)}2+\frac\lambda2(1-N)
+c_\rho(\mathcal B_++R_1)\right]D,
\]

where `D` is the joint input/output distance to a characteristic evolving in the same field, `R_1` is its normalized mean distance, and

\[
\mathcal B=V+(1-N)Y_s-X_s,\qquad c_\rho=\rho^3\phi(0)/2.
\]

A scalar nonlinear comparison closes the `R_1` contribution without an additional logarithmic loss. Under a bounded integral of `B_+`, the amplification is a constant times `N_ent^(-1/2)` for all labels and every moment for which an entry estimate is supplied. The estimate also transports a first-exit profile.

With the proposed entry powers `S0^(1/2-alpha)` and `S0^(1-lambda)`, this gives a **conditional nonlinear**, rather than merely frozen-linear, exponent

\[
\eta_{\rm glob}=\lambda/2-\alpha=\frac\lambda2\Phi(-\rho a_\rho)>0.
\]

The initial strong shape, weak retention, mean budget, and chart validity are still hypotheses. The positive exponent is not an initialized theorem.

There are two original-flow additions. First, the reviewed ancestry inequality is specialized to obtain an explicit Q2 ancestral lower bound of order `S0^(1-lambda)` at the early envelope clock. Second, a new upper bound shows why this cannot be assigned automatically to AN02's fixed-sector arriving cohort: each arriving label has only `O(S0)` mass when `q²T` is bounded, and its Q2 ancestral fraction shrinks. The growing mass must be retained or recaptured from earlier Q2 labels. A weighted **net-retention functional** specifies the missing original-flow estimate without discarding transit and return.

## 2. Precise contracts and dependencies

### Proposition 2.1 — `Q2mass`

**Assumptions.** Original Gaussian population, prescribed aligned isotropic initialization, `0 < S0 < delta <= 1/100`. Use the proved early comparison until

\[
T_\delta=\log(\delta/S_0)/(1+2q^2).
\]

**Conclusion.** For every fixed measurable ancestral subset `C` of Q2,

\[
\int_Cm_{T_\delta}\,d\lambda_0
\ge e^{-4\delta}\delta^\lambda S_0^{1-\lambda}
 e^{-2\lambda q^2T_\delta}\int_C\sin^2\alpha_0\,d\lambda_0.
\]

For all Q2 the last integral is `1/8`. This is a lower bound on ancestral mass, not a two-sided asymptotic law, current family membership, or a response bound.

**Dependencies.** Reviewed AN02 ancestry Theorem 2.1; checkpoint `pa:earlybounds`, `pa:targetcomparison`.

### Theorem 2.2 — `arrivalupper`

**Assumptions.** Exact finite-noise target-only flow; terminal sector `I = [2pi/3,3pi/4]`; analytical initial-label set `C_T = phi_{-T}(I)`. The original-flow conclusions additionally require the reviewed early comparison interval.

**Conclusions.**

\[
\widehat m_T\le4S_0\cos^2\alpha_0\,e^{3q^2T/2},
\]

and for the Q2 portion,

\[
\tan(\pi-\alpha_0)\le\sqrt3\,e^{-(\lambda/2-3q^2/4)T}.
\]

Thus the original Q2 arriving mass is at most

\[
\frac{2\sqrt3}{\pi}e^{2H(T)}S_0e^{-\lambda T/2+9q^2T/4}.
\]

At `T_delta`, fixed `delta,rho`, and `q²T_delta -> 0`, this is `O_delta(S0^(1+lambda/2))`. It is an upper bound, not a claim of sharp asymptotics or positive Q2 arrivals in every regime.

**New ingredient.** Terminal negativity of the first target-only coordinate forces negativity throughout the preceding path. Its magnitude grows at most at rate `3q²/4`, because the first projected Gaussian CDF is at most `1/2`. The terminal angle then bounds the radius by that negative coordinate. No original-flow inverse angle map is used.

**Interpretive qualification.** The `sin²(alpha0) e^(lambda T)` term can improve a finite-parameter bound. It cannot be treated as a free, uniform `S0^(-lambda)` gain for this particular backward cohort: its initial sine shrinks with `T`.

### Proposition 2.3 — `retention`

**Assumptions.** Original flow at a prescribed later time and a prescribed bounded weak chart. Define Q2 captured mass by ancestry and final chart membership.

**Conclusion.**

\[
N_2^{\rm cap}(\tau_e)\ge
 e^{-4\delta}\delta^\lambda S_0^{1-\lambda}
 e^{-2\lambda q^2T_\delta}\mathcal R_2(\tau_e),
\]

where

\[
\mathcal R_2=\int_{Q_2}1_{\text{in weak chart at }\tau_e}\sin^2\alpha_0
 \min\left\{1,\exp\int_{T_\delta}^{\tau_e}(\log m)'dt\right\}\,d\lambda_0.
\]

This is an exact inequality. It does **not** prove a nonzero lower bound on `R_2` (it may be zero). It isolates the required lower bound in a physically meaningful weighted net-retention quantity. Temporary loss followed by regrowth is retained in the net exponent.

A loss-dissipation argument supplies the unconditional radial floor `(log m)' >= -2 C_E`, with `C_E` in (2.12). A delay of order `log(1/q)` then costs at most a polynomial factor on bounded parameters; a delay of order `log(1/S0)` may cost an additional initialization power under that crude estimate. Geometry remains unproved in both cases.

### Lemma 3.1 / Proposition 3.2 — `jacobian`, `averagedpair`

**Assumptions.** Defined leading population, finite chart-valid interval, bounded supports and fixed families, `0<M<=1`, `0<=N<=1`; reference characteristic in the same field. Ordered identities are stated for upper or lower co-ordered pairs.

**Conclusions.** Exact derivatives, full donor cancellation, and both receiver-preserving pair identities. The upper mismatch term is

\[
\frac\lambda2[(1-N)k-h](P_+-\bar P_+),
\]

and the lower mismatch term is

\[
\frac\lambda2[(1-M)h-(1-N)k](\bar P_--P_-).
\]

At `M=1`, the lower mismatch is nonpositive. For a diagonal upper pair at `N=0`, the upper mismatch vanishes and the averaged rate reproduces the reviewed passive-diagonal law. Neither fact assumes that a finite-mass bridge leaves the residual unchanged.

**Dependencies.** Checkpoint `pa:leading`, `pa:overlap`, `pa:masslaws`; AN02 upper-pair formula is independently rederived in the proof.

### Theorem 4.1 — `alllabel`

**Assumptions.** Same leading solution and same-field reference. No order assumption on any actual label.

**Conclusion.** The all-label Dini inequality (4.1), the barycentric budget (4.2), and the integrated factor (4.3). The lower-side estimate pays the extra strong-learning term `lambda(1-M)/2`, so its combined damping is `-(1-lambda)(1-M)/2`. This is not a new proof of the desired initialized strong contraction. The weak-stage global rate remains `lambda/2`.

**Mixed-order justification.** At fixed sign of `x-c`, taking the absolute value of the other coordinate bounds the cross terms by their co-ordered analogues because the off-diagonal derivatives are nonnegative. At either coordinate equality the upper derivative is the absolute cross velocity. At total equality, same-field uniqueness preserves coincidence.

### Theorem 4.2 — `halfpassage`

**Assumptions.** Leading solution and same-field reference through its own weak half-mass time; `0<N0<1/2`. Define

\[
L(t)=\sqrt{N(t)/N_0}\exp\left(c_\rho\int\mathcal B_+\right),
\quad Q(t)=1-c_\rho R_1(\tau_0)\int_{\tau_0}^tL.
\]

**Conclusion.** On a positive-denominator interval,

\[
D(t)\le [L(t)/Q(t)]D(\tau_0),\quad
R_p(t)\le [L(t)/Q(t)]R_p(\tau_0).
\]

Because `N<=1/2`, `L' >= lambda L/4`, which implies

\[
\int_{\tau_0}^t L\le4[L(t)-1]/\lambda.
\]

The explicit smallness condition `(4 c_rho/lambda) R_1(entry) L(half) <= 1/2` ensures `Q>=1/2` throughout. There is no extra sojourn-length logarithm. Radius about the actual strong barycentre is at most twice radius about the same-field reference.

**Important remaining hypothesis.** A small entry shape is insufficient by itself. `integral B_+` is a population mean/weak-feedback quantity that can grow over the sojourn. A useful sufficient estimate is `B_+ <= C_B N + r_B` with an integrable, bounded remainder. The coherent branch meets a bound of that form; the initialized population is not shown to do so here.

### Corollary 4.3 — `exitprofile`

The same monotone factor transports a normalized profile for every label and bounds all first exits up to a fixed time. An exit beyond the chosen core radius is not automatically exit from the physical chart; if actual chart exit occurs, the theorem's continued applicability must be justified or the label must be retained in another budget.

### Proposition 5.1 / Corollary 5.2 — `clockconversion`, `exponent`

The initial-clock-to-entry-clock conversion uses the full logit defect. In a closed logistic comparison, initial power `1` and strong clock slope `1` give entry power `1-lambda`. A changing mask or a family not yet in its chart does not have that law without proof.

With entry estimates

\[
N_0\ge c_w(q)S_0^{1-\lambda},\quad
R_p(\tau_0)\le C_s(q)S_0^{1/2-\alpha},\quad
\int\mathcal B_+\le B_0(q),
\]

Theorem 4.2 proves the conditional bound

\[
R_p(\tau_h)\le2A(q)S_0^{\lambda/2-\alpha},\qquad
A(q)=C_s(q)e^{c_\rho B_0(q)}/\sqrt{2c_w(q)}.
\]

It needs the displayed denominator smallness condition. The positive exponent is uniform on the reviewed compact ratio interval, with elementary bound `4901/80000`. It is not uniform up to either endpoint of `(0,1)`.

## 3. Scope ledger

| Statement | Status |
|---|---|
| Q2 ancestral mass lower bound at `T_delta` | Exact original-flow initialized consequence |
| Fixed-sector arrival mass and label-measure upper bounds | Exact target-only theorem; original-flow transfer on the proved early interval |
| Ancestry-to-captured-mass inequality | Exact original-flow identity/inequality; retention lower bound still missing |
| Upper/lower receiver-preserving pair laws | Exact within the defined full leading system |
| All-label, two-sided distance bound | Exact within the leading system; no co-ordering premise |
| Nonlinear spread bound through weak half-mass | Conditional leading-system theorem with denominator and mean-budget inputs |
| First-exit profile | Conditional leading-system consequence; does not discard exited labels |
| Positive exponent with entry power `1-lambda` | Proved conditional consequence of the new nonlinear theorem |
| Actual initialized `N_ent >= c(q) S0^(1-lambda)` | Not proved |
| Initialized joint input/output entry-shape law | Not proved |
| Uniform mean-feedback integral from initialization | Not proved |
| Isotropic selection of the AN06 orbit | Not proved |
| Finite-noise long-time/rate/strip transfer | Not proved |
| Reported sweep exponents and deeper-regime extrapolation | User-reported empirical evidence; no independent reproduction here |

## 4. Audit points

1. **No hidden clock conversion.** `T_delta` is the early envelope time, not strong half-mass. The desired learned entry time can be later. The defect in Proposition 5.1 belongs to derivation of the entry law, not to a later early-centered witness phase error.
2. **Positive coordinates and the arrival bound.** At zero the target-only coordinate derivative is strictly positive. A terminal negative first coordinate therefore cannot previously have been nonnegative. On this path `d_q <= 3q²/4`, not merely `q²`.
3. **Arrival exponent arithmetic.** The pointwise radial factor is `e^(3q²T/2)` and the Q2 label-length factor is `e^(-lambda T/2+3q²T/4)`. Their product gives `9q²T/4`, while substituting `T_delta` adds `lambda q²T_delta` in the remainder exponent.
4. **Ancestral weights.** Q2 has total `sin²` weight `1/8` in the normalized full-circle label law. A parameter-dependent arriving cohort does not retain a constant sine weight.
5. **Retention is net, not total negative variation.** The capped multiplier is `min(1,exp(integral radial rate))`. Replacing it by `exp(-integral negative radial rate)` is valid but can unnecessarily lose a return/recovery mechanism.
6. **No moving-mask derivative.** Proposition 2.3 is a fixed-time integral. It supplies no logistic law for a moving captured family and no automatic absence of subsequent recruitment flux.
7. **Full donor population retained.** The identity `Pi-Lambda_-=M(X_s-r)` includes all strong donors. The lower-side calculation must use it before dropping a nonnegative tail term.
8. **Mixture and scaling factors.** `lambda=rho²`; `S'(r)=rho² phi(rho r) Pi(r)` produces the `rho³` field coefficient. All rates use normalized time.
9. **Averaged receiver rate.** On the upper side, the integration-by-parts term is `h(P_+-Pbar_+)`; on the lower side it is `h(Pbar_--P_-)`. Both are nonnegative. Their signs in (3.5) and (3.6) differ.
10. **Mixed signs.** The final all-label theorem uses absolute-value cross-term inequalities, not an unjustified extension of a co-ordered identity. It treats both coordinate-equality cases.
11. **Barycentric budget.** Both `Uc` and `Uc^-` are at most `B + |d-Y_s| + |c-X_s|`. Jensen gives the sum of the two absolute deviations at most `R1`. No extra factor of two is needed.
12. **Normalized weights.** Their constancy is a hypothesis supplied by the closed leading transport-reaction law. It is not asserted for finite-noise labels or moving masks.
13. **Scalar comparison.** The denominator must stay positive. The quantitative smallness condition is sufficient on the whole interval because `L` and its integral are monotone. A zero initial spread remains zero by common-field uniqueness.
14. **No logarithmic loss.** `L' >= lambda L/4` uses the entire interval being before or at weak half-mass. The same lower-rate bound is not asserted after that time.
15. **Moment interpretation.** `R_p` is a joint input/output moment; an input IQR or a marginal standard deviation is not the same input. Each high-moment or supremum claim needs its own initial bound.
16. **Existence versus approximation.** The leading system may remain algebraically defined outside a small chart, but bounded physical-chart validity and finite-noise error control are not consequences of the algebraic estimate.
17. **Smallness and q-costs.** Positivity of `lambda/2-alpha` does not control `A(q)`. An exponentially small retention coefficient can defeat the proposed joint scaling.
18. **Sector and learning scope.** Neither all-rho positivity of a conditional exponent nor a half-mass shape bound extends AN06's proved common witness rectangle or proves exact learning responses.

## 5. Corrections, failed shortcuts, and open residue

The user's revised entry-clock accounting is algebraically correct: replacing an **entry** exponent `1` by `1-lambda` changes the frozen balance to `Phi(-rho a)/2` and the global balance to `lambda Phi(-rho a)/2`. The new theorem makes the latter a genuine sufficient nonlinear passage estimate, provided the mean-feedback integral is controlled. The earlier statement that a local-core/exit decomposition was necessary for the sign of the formal balance is therefore not retained under these new entry hypotheses. Such a decomposition can still improve constants and handle outside-chart labels.

The previous `c0=1` formula itself was not an algebra error; it was conditional on a different unproved entry law. The reported extrapolated initial-clock mass and measured resident-entry mass cannot be assigned the same exponent without a time conversion. The note records that conversion, including a mass-law defect.

The weighted ancestry theorem does not uniformly upgrade the arriving AN02 cohort by a free exponential mass factor. Theorem 2.2 makes the reason quantitative. This is compatible with a useful finite-parameter improvement and with the user's proposed retention interpretation. It does not refute the proposed total captured-seed law.

The original-flow bottleneck is now the concrete lower bound on `R_2(tau_e)`, with q-dependence strong enough for `A(q) S0^eta -> 0`, coupled to the joint strong entry-shape and mean estimates. This requires a geometric transit/return argument. A lower bound on total Q2 mass is not that argument. The new theorem does not continue the early comparison to saturation.

Even with a retained seed, the mean-feedback budget needs proof. For example, establishing

\[
[V+(1-N)Y_s-X_s]_+\le C_B N+r_B,\qquad \int r_B\le B_{\rm err}
\]

would make the current nonlinear spread theorem usable. Mean tracking, weak-angle relaxation, and chart/outside-population bookkeeping remain coupled tasks. The same-field comparison characteristic is not automatically the selected coherent trajectory.

For recruitment, the `5/6` versus `5/9` comparison gives the proposed `5/18` power advantage at `rho=2/3`. The threshold `10.8` additionally neglects the q-dependence of the retained seed coefficient and compares an auxiliary target-only tail law to a still-unproved capture law. It is not an established regime boundary.

## 6. Integration proposal and provenance

After independent review and explicit consolidation approval, place Proposition 2.1, Theorem 2.2, and Proposition 2.3 in the AN2 entry/retention section. Retain the reviewed AN02 arrival lower bound: the new upper bounds clarify its scope rather than replace it.

Place Section 3 after the reviewed AN02 same-field upper-tail formula. It adds the lower side and retains the averaged receiver term. Place Theorems 4.1–4.2 and the exit corollary in AN3, distinguishing spread about a same-field reference from orbit tracking. Place the clock conversion and conditional exponent after the passage interface. Amend only the conditional interpretation of the old `c0=1` scenario, not the old algebra.

Stable label map:

| New item | Label suffix |
|---|---|
| Proposition 2.1, Q2 ancestral mass | `Q2mass` |
| Theorem 2.2, arriving-cohort upper bounds | `arrivalupper` |
| Proposition 2.3, net-retention interface | `retention` |
| Lemma 3.1, field and donor identities | `jacobian` |
| Proposition 3.2, averaged pair identities | `averagedpair` |
| Theorem 4.1, all-label inequality | `alllabel` |
| Theorem 4.2, nonlinear half-mass passage | `halfpassage` |
| Corollary 4.3, first-exit profile | `exitprofile` |
| Proposition 5.1, entry-clock conversion | `clockconversion` |
| Corollary 5.2, positive conditional exponent | `exponent` |

The LaTeX source compiles standalone. Compilation and rendered-page inspection check presentation, not mathematical correctness. No trajectory, sweep, quadrature experiment, interval continuation, or numerical sign certificate was run. No GitHub access or modification was performed. The empirical report is attributed to the user, not presented as independently reproduced evidence.

### Dependency hashes (unchanged)

```text
842806cd0ae9b7e33050fd59dd18818eed01230c188494609d7100513da39504  THEORY_HANDOFF_ANALYTICAL_A_B.md
b9b169764339017da37209eca84f17154b73c1a2de79d61c707cf2f550763e1b  THEOREM_A_ANALYTICAL_PROGRESS.tex
eefd557e0c725c87ea6b41d0d144b92e14f895f0b7f0095d509915b14a9de3f1  RELU_POPULATION_FOUNDATIONS_v2.tex
248c4d6c4a1c064ed7556b9d51b51381e7f9ce360588cde89660e53bbd51b387  AN02_strong_ancestry_and_tail_transport_v1.tex
ad7165416efe2b7730ce1da29c66afe32e8509c9ff9a864f2e175700c5d016bf  AN02_weak_side_arrival_v1.tex
ee67a2c8dba1e3dac791b141abbbc8d4b7fdefb2564877b0fb121fb917a2c5d4  AN06_learned_orbit_witnesses_v2.tex
```
