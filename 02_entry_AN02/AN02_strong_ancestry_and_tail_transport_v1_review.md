# Review note: strong ancestry and nonlinear upper-tail transport, v1

Companion proof: `AN02_strong_ancestry_and_tail_transport_v1.tex`.
Unique label prefix: `inc:AN02:tail:v1:`.

The consolidated checkpoint, foundations, AN02 weak-side arrival v1, and AN06 v1/v2 are unchanged. This is a new review increment, not a claim that the coupled initialized strong-learning/capture lemma has been completed.

## 1. What is new

**Theorem 2.1 is an original finite-noise initialized result.** It strengthens the early mass input by retaining the positive initial-coordinate weights:

\[
m_\tau(\alpha)\ge e^{-2H(\tau)}S_0
\left[e^\tau(\cos\alpha)_+^2+e^{\rho^2\tau}(\sin\alpha)_+^2\right].
\]

This holds on the checkpoint's established early comparison interval. It gives a lower bound for every measurable fixed ancestral label set, not only a specially selected central cohort. At the early envelope time, the initial right half-circle carries at least

\[
\frac{e^{-4\delta}\delta}{4}
\exp\left[-\frac{2q^2}{1+2q^2}\log(\delta/S_0)\right].
\]

Thus the drift condition directly produces an order-\(\delta\) strong-ancestry mass bound. It does not prove that this mass is charted or that its output fits the strong cluster.

**Section 3 solves the entire outer comparison relevant to the proposed one-sided tail.** In the *defined zero-noise target-only model*, Q1 and Q4 contract at different rates. The exact finite-time mass is a leading \(\cos^2\alpha\) term plus a retained \(\sin^2\alpha\) term. Both the initial-label tail and its angular pushforward are computed. This supplies a checked analytical comparison, not a claim of finite-noise matching through saturation.

**Theorem 4.1 is a nonlinear, not merely linearized, resident-field result.** For a passive strong characteristic on the upper diagonal, the exact equation along the coherent resident strong-learning curve is

\[
h'=\left[-\frac{1-M}{2}+\mathcal B(h)\right]h,
\qquad
\mathcal B(h)=\frac{\rho K(\rho(a+h))-a}{2h}.
\]

The rate increases strictly from the local shape rate \(\alpha_{\rm sh}\) to \(\lambda/2\). This gives two-sided nonlinear amplification bounds, explicit hitting-time bounds, and an exact correction to the proposed far-field separatrix.

**Theorem 5.1 propagates a full upper-tail profile in a self-consistent leading population.** It compares labels with a core characteristic in the *same* time-dependent residual field. It yields both an instantaneous tail bound and a bound on the labels that ever leave a fixed core neighborhood over the entire interval. The latter is the relevant quantity for resident passage and potential recruitment. Unlike Section 4, this theorem retains the full population in the field; its assumptions include an ordered entry set and a same-field reference.

**Section 6 records source and clock consequences.** The total weak mass is logistic only for a closed family. Continuing recruitment changes the mass law and source proportions through explicit defects. The AN3/AN7 convention is the population's own half-mass clock, with local logit error integrated only over the bounded clock-to-witness hull.

## 2. Two corrections to the structural heuristics

### 2.1 The stated tail power is 5/6, not 4/3

At \(\rho=2/3\), \(\lambda=4/9\), and

\[
\frac{3(1-\lambda)}2=\frac56.
\]

Accordingly, a proposed mass law \(S_0^{3(1-\lambda)/2}q^{-3}\) is not smaller than an \(S_0\)-scale seed at those parameters. Its ratio to \(S_0\) is proportional to \(S_0^{-1/6}q^{-3}\).

Corollary 3.3 proves that exact power **for the outer comparison's angular tail at its nominal strong-scale time**. The comparison gives a concrete check on the exponent, but it does not establish the original trajectory's saturation tail or the amount later captured into a weak chart.

This distinction matters in both directions. One cannot dismiss recruitment as subdominant using the displayed power. One also cannot replace the actual seed exponent by \(5/6\), or claim that the actual recruited population dominates, without the missing matching and capture theorem. The already-proved reservoir lower bound remains valid. A larger additional weak seed could reduce the resident delay, but would require control of its angular distribution and feedback.

### 2.2 The far-field linear intercept is not a separatrix

For a passive characteristic above a coherent resident core with \(M=1,N=0\), the upper diagonal is exactly invariant. Along it,

\[
x'=y'=\tfrac12[\rho K(\rho x)-a]>0\quad (x=y>a).
\]

At \(x=y=a/\lambda\), the exact velocity is

\[
\frac\rho2[K(a/\rho)-a/\rho]>0.
\]

The saddle at \((a/\lambda,a/\lambda)\) belongs to the *large-input linear approximation*, not to the exact finite-coordinate field. It cannot define a safe initial tail cutoff. A finite-horizon exit threshold, such as the one in Theorem 5.1, is a better object for the contract.

The result does not characterize a global separatrix for arbitrary off-diagonal states. Nor does it prove that adding positive tail mass leaves the core's field unchanged. That last issue is why the full same-field theorem is stated separately.

## 3. Proof contracts and statuses

| Result | Assumptions and dependencies | Conclusion | Status |
|---|---|---|---|
| Theorem 2.1 | Prescribed isotropic initialization; original Gaussian flow; checkpoint `pa:targetcomparison`, `pa:earlybounds`; \(\epsilon_{\rm al}<\pi\) | Labelwise and setwise positive-coordinate mass lower bounds | Exact original-flow initialized result |
| Corollary 2.2 | \(0<S_0<\delta\le1/100\); same comparison | Order-\(\delta\) ancestral mass with explicit \(q^2\log\) drift factor | Exact original-flow initialized result |
| Equations (2.9)–(2.12) | Fixed Q1 ancestral set defined by initial tangent threshold | Explicit weight integrals and retained finite-time weak-coordinate term | Exact original-flow lower bound and elementary integrals |
| Propositions 3.1–3.2 | Explicitly defined zero-noise target-only field | Exact Q1/Q4 transport, mass weighting, and angular tails | Exact auxiliary-model results |
| Corollary 3.3 | Same auxiliary model; \(q\to0\), \(r/q\to0\) at nominal clock | Cubic angular-tail asymptotic and \(5/6\) power at \(\rho=2/3\) | Exact asymptotic of auxiliary model only |
| Theorem 4.1 / Corollary 4.2 | Defined leading system; prescribed coherent resident field; passive initial \(x=y>a\) | Nonlinear scalar law, amplification, finite hits, no second diagonal threshold | Exact prescribed-field limiting-system results |
| Theorem 5.1 | Full leading characteristic solution; bounded support on finite interval; closed families; same-field reference; co-ordered initial subset | Full profile propagation and first-exit mass bound | Conditional, nonlinear, self-consistent leading-system theorem |
| Proposition 6.1 | Absolutely continuous source masses with displayed reaction/defect equations | Source fractions and logit identities; closed-source special case | Exact accounting identity; flux estimates not supplied |
| Section 6.2 | Own half-mass clock; bounded clock-to-witness hull and mass guard | Phase-aligned contract and local mass-defect bound | Interface using the reviewed AN06 clock identity |

There is no new theorem of isotropic angular entry, order-one strong learning, weak capture, small-shape passage, or finite-noise rate transfer. Canonical offset witnesses in AN06 remain available; canonical positive-noise trajectory coverage has not been added.

## 4. Audit points

### Original-flow mass bound

The finite-noise target-only coordinate field includes both clusters' covariance term

\[
d_q=\frac{q^2}{2}[\Phi(\widehat a_1/q)+\Phi(\rho\widehat a_2/q)].
\]

It is not dropped from the equation. It has a favorable sign on an initially positive coordinate. The coordinate cannot first reach zero because its derivative there is strictly positive. The target-only radius is nondecreasing, so the divisions by its norm and the zero-boundary check are legitimate.

The estimate is first proved for the target-only vector, then transferred through the *existing exact* logarithmic mass comparison. No assertion is made that the actual input/output vectors remain aligned. Set integration is always over fixed initial labels, so no mask flux is lost.

The total lower bound at time zero is weaker than the exact initial mass. This is intentional: initially negative coordinates are omitted, not assigned zero mass in the actual model.

### Tail integrals and limit order

The exact integrals use \(d\alpha=dt/(1+t^2)\). The leading weighted density becomes \((1+t^2)^{-2}\), while the retained term becomes \(t^2(1+t^2)^{-2}\). These are different tails.

At any fixed finite comparison time, taking the ancestral threshold \(R\to\infty\) makes the retained \(r^2 I_s(R)\) term eventually dominate the \(I_c(R)\) term. Thus a global pure cubic law at finite time is **not** asserted.

At a small current angular edge \(q\zeta\), in the asymptotic regime of Corollary 3.3, their ratio instead tends to \(3\tan^2(q\zeta)\to0\). That calculation, not an implicit exchange of limits, justifies the cubic angular-tail asymptotic.

The comparison clock \(\tau_A=\log(A/S_0)\) is not called the original saturation time. The parameter \(q\) in Section 3 specifies a small angular edge of a separately defined zero-noise model. No finite-noise convergence theorem is smuggled into this notation.

The normalized limiting weight is \((2/\pi)\cos^2\alpha\,d\alpha\) on the initial right half-circle. A continuous individual label does not have positive point mass; “weight” means density or the mass of a label interval.

### Passive resident theorem

The identity \(F(\rho x,\rho a)=K(\rho a)\) requires \(x\ge a\). It is used only on the upper half-diagonal, which the scalar equation preserves. The integral representation of \(\mathcal B\) removes its apparent singularity at zero.

The exact rate bounds do not assume \(h\) is infinitesimal. Positivity and global finite-time continuation follow from the displayed linear upper and lower growth bounds. The hitting-time denominator is positive for every \(z>a\). The far-field intercept correction uses the strictly positive Mills gap, not a decimal Gaussian evaluation.

The passive particles do not alter the donor measure. Applying their scalar law to a positive-mass tail of the full flow without an error bound would be invalid.

### Full same-field theorem

The reference is a characteristic of the same evolving population field. It is not automatically the barycenter and is not a coherent orbit from a different population.

For ordered differences \(h,k\ge0\), the receiver derivative of the overlap is

\[
\mathcal S'(r)=\rho^2\phi(\rho r)\int(\widetilde x-r)_+\,d\mu_s.
\]

Multiplication by the \(-\rho\) in the input field produces the negative donor-tail term in equation (5.7). The coefficient is \(\rho^3\), not \(\rho^2\). Kernel \(C^1\) regularity suffices; no classical Hessian at coincident atoms is assumed.

The cross derivatives are nonnegative at fixed field, which preserves the two-coordinate order. This does not imply cooperation between different population trajectories. The core imbalance budget \(b_c\) pays only for the positive part of \(V+(1-N)y_c-x_c\); the donor tail and receiver displacement terms have favorable signs and are dropped only in an upper bound.

The sum-difference inequalities do not divide by a zero displacement. Coincident characteristics remain coincident. The local coefficient is used only until a first hit of the specified displacement radius. The maximum \(G_H^*(T)\), not just \(G_H(T)\), is essential when initial contraction precedes later amplification.

First-exit events are fixed sets of initial labels. The mass after exit is weighted with the common closed-leading-family reaction factor \(M(T)/M(\tau_0)\). The measure on labels is denoted \(\mathfrak m_\tau\), while \(\mu_s\) is its coordinate pushforward; no invertibility of the label-to-angle map is assumed.

Leaving a chosen small core neighborhood is not necessarily leaving all scaled charts. If the label leaves the physical range on which a finite-noise expansion is controlled, this theorem supplies no replacement finite-noise estimate. An outside-population budget or chart transition is still required.

### Source and clock accounting

The original fixed-source mass identity is exact. The sourced logistic form defines a defect; its smallness is not assumed to have been proved. A moving mask can add flux even in a leading description. If that flux is singular in time, the absolutely continuous proposition is not applicable without its measure-valued extension.

Source proportions are constant only when all source defects vanish. Recruiting strong-tail labels during the resident interval cannot be combined with an unchanged closed-family logistic law merely by relabeling them.

The clock-to-witness hull is \(\operatorname{conv}(\{0\}\cup J)\). If zero lies outside the witness interval, integrating from the half-mass time to a witness uses more than \(J\) itself, but still only a bounded interval. A uniform margin from both zero and one is the quantitative denominator guard. Long-delay relative mass errors affect the aligned entry/profile data and event control, not a separately accumulated early-centered phase error on the witness interval.

## 5. What this unlocks, and what remains open

The early ancestral measure lower bound can replace a crude constant lower bound on individual target-only masses wherever the fixed initial-coordinate weights are useful. It gives a useful order-\(\delta\) input before attempting strong-learning continuation.

The outer comparison makes the asymmetric ancestry mechanism precise in its own model and exposes the finite-time correction. To use it in AN2, one still needs a finite-noise, nonlinear-residual matching argument for the spatial profile, including the upper tail and the intermediate angular region.

Theorem 5.1 gives the requested kind of **trajectory-level tail output** for AN3: an initial profile is propagated into an upper bound on the mass that ever escapes a small core neighborhood. To apply it from initialization, AN2 must supply the same-field core, its mean/imbalance control, ordered entry or a controlled ordering defect, and the profile itself. The theorem does not create those inputs.

The global tail exponent uses the \(\lambda/2\) rate. Recovering the favorable \(\alpha_{\rm sh}\) core exponent requires the local profile/exit decomposition and control of the escaping labels. Substituting the global bound into the small-shape power test is generally too costly.

The weak seed must be split by source without presuming dominance. The corrected outer proxy is a warning against dismissing the recruited source, not a proof of its eventual contribution. At a minimum, the later argument needs either a quantitative upper bound on recruitment/flux or a proof that the recruited population joins a controlled weak angular law.

The half-mass convention is now explicit in the contract. Any eventual rate transfer must additionally control the finite-noise mass defect over the bounded hull and all outside-chart contributions to the \(q^2\)-scale observables.

## 6. Proposed integration location

No integration is performed now.

Theorem 2.1 and Corollary 2.2 belong immediately after checkpoint `pa:targetcomparison`. The tail-weight corollary belongs with the early ancestral transport estimates.

Section 3 is a separately labeled outer comparison, not a replacement for the original Gaussian flow. It belongs in the entry-analysis section with its nonuniform finite-time tail qualification.

The nonlinear resident test-particle result belongs after `pa:resident` and the linear shape spectrum, before the passage multipliers. The full same-field profile theorem belongs alongside `pa:order`, with explicit links to AN2 entry and AN3 exit obligations.

The source/flux identities and clock convention belong in the AN2/AN3/AN7 interface. AN06's probe containment caps can be removed during a later authorized consolidation; they are not changed in AN06 v2 here.

## 7. Stable label map

| Main label suffix after `inc:AN02:tail:v1:` | Content |
|---|---|
| `weightedmass` | Original-flow positive-coordinate ancestral mass theorem |
| `earlyfraction` | Early strong-ancestry mass fraction |
| `ancestraltail` | Exact original-flow ancestral tail lower bound |
| `quadrants` | Zero-noise Q1/Q4 comparison solution |
| `angulartail` | Exact comparison angular-tail pushforward |
| `exponent` | Corrected reference tail exponent |
| `nonlineardiagonal` | Nonlinear upper-diagonal resident equation |
| `noseparatrix` | Exact finite hitting and intercept correction |
| `profiletheorem` | Self-consistent same-field profile and exit theorem |
| `exactpair` | Receiver-difference identity retaining donor-tail forcing |
| `sourceclock` | Source reaction/flux and logit identities |
| `windowclockbound` | Bounded clock-to-witness mass-defect estimate |
| `remaining` | Exact open initialized obligations |

## 8. Build and provenance

The LaTeX is standalone and uses no numerical arrays or automatic inclusion of other proof files. No training trajectory, quadrature, or numerical sign test was run. The proof does not depend on evaluating the resident root or any Gaussian CDF numerically.

The displayed constants and equations are justified in the text. LaTeX compilation and page rendering check document production only; independent mathematical review is still required.

Source SHA-256 values recorded at delivery:

```text
eefd557e0c725c87ea6b41d0d144b92e14f895f0b7f0095d509915b14a9de3f1  RELU_POPULATION_FOUNDATIONS_v2.tex
b9b169764339017da37209eca84f17154b73c1a2de79d61c707cf2f550763e1b  THEOREM_A_ANALYTICAL_PROGRESS.tex
842806cd0ae9b7e33050fd59dd18818eed01230c188494609d7100513da39504  THEORY_HANDOFF_ANALYTICAL_A_B.md
ad7165416efe2b7730ce1da29c66afe32e8509c9ff9a864f2e175700c5d016bf  AN02_weak_side_arrival_v1.tex
ee67a2c8dba1e3dac791b141abbbc8d4b7fdefb2564877b0fb121fb917a2c5d4  AN06_learned_orbit_witnesses_v2.tex
```
