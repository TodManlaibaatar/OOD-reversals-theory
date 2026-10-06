# Review: linear contrast, limiting permanence, and the revised theorem scope

**Proof increment:** `LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex`  
**Reading copy:** `LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.pdf` (7 pages)  
**Label prefix:** `inc:LP:v1:`  
**Status:** New, separate material for independent review. No source file or consolidated checkpoint was changed. No GitHub access, numerical trajectory integration, interval arithmetic, or saved-trajectory certificate was used.

## 1. What is new, and what is not

The linear population contrast is already Proposition P10 in `RELU_POPULATION_FOUNDATIONS_v2.tex`, including the clusterwise sign. The present statement extends its initialization from scalar-isotropic covariance to any positive diagonal covariance and makes the finite-width scope and cluster assumptions explicit. It should be presented as an extension/restatement of existing progress, not as a newly discovered missing control.

The new limiting result strengthens `pa:limitreversal`: the selected coherent orbit's strong input coordinate tends to positive infinity, and every bounded probe-offset sector is eventually permanently inactive in the *defined leading system*. The principal permanence proof uses only finite downward variation and the existing arbitrary-level hitting result. It does not need a sharp asymptotic growth law.

A separate proposition proves the proposed extra claim of eventual strict increase, with an `O(sqrt(log s))` upper-growth bound. It repairs the moving-barrier gap in the proposed outline by using `x+v` as a scalar comparison variable.

The final growing-window result is explicitly conditional on original-flow convergence on every fixed centered window. It is an analytical diagonal-selection argument; it does not establish the missing convergence or its quantitative time scale.

## 2. Proof contracts

| Statement | Assumptions and dependencies | Conclusion | Scope/status |
|---|---|---|---|
| Theorem `linear-theorem` | Aligned labels, positive diagonal initial Gram, positive diagonal total data moment; diagonal individual weighted cluster moments for cluster signs | Explicit aligned logistic trajectory, strict probe-error descent, and nonpositive cluster rates | Exact finite-width/continuum linear result; direct proof supplied |
| Lemma `downward` | Locally absolutely continuous function, finite negative variation, unbounded forward limsup | Divergence to positive infinity | Elementary analytical lemma |
| Theorem `permanence` | Selected coherent orbit; analytical imports from `pa:branch`, `pa:limitreversal` | `x -> infinity` and eventual exact zero of the scaled probe-error coefficient | Leading coherent system only |
| Proposition `monotonic-theorem` | Same selected orbit | `x = O(sqrt(log(2+s)))` and eventually `x' > 0` | Leading coherent system only; comparison proof supplied |
| Proposition `uniform-clear` | Compact parameter family, continuous selected branches, uniform imported linear-growth estimate | Common finite limiting clearing time for a bounded offset sector | Analytical compactness consequence |
| Proposition `diagonal-transfer` | Analytically proved, full original-flow rescaled-error convergence on every fixed centered window | Some growing horizon and vanishing error floor | Conditional transfer implication, not an initialized result |

Internal labels have the full prefix `inc:LP:v1:`.

## 3. Linear-control audit

### Mixture normalization

The increment uses weighted moments `mathsf A_p = pi_p E_p[XX^T]`, with `A = sum_p mathsf A_p`. The foundations use raw per-cluster moments for P10. Accordingly,

\[
D_p^\tau=-2\sum_r(\mathsf A_p)_{rr}\ell_r(1-\ell_r)^2\xi_r^2
\]

is the same formula as P10's raw-cluster version for equal weights. Physical rates acquire the factor `mu1^2` when the data have been normalized.

### The assumptions needed for each conclusion

Diagonal total `A` and diagonal initial Gram establish total monotonicity. The sourcewise conclusion additionally uses that every `mathsf A_p` is diagonal in the same basis. That property holds for Gaussian SIM, but does not follow from the sum being diagonal. The proof includes an exact PSD-moment counterexample with `A = I` and `D_1 = 433/5000 > 0` if this assumption is dropped.

Strict decrease in *every* nonzero direction requires positive eigenvalues of `A` and an initial diagonal entry distinct from one in each relevant coordinate. The proposition uses `a_r > 0` and `0 < c_r < 1`, as in the user's small initialization setting.

The exact candidate solves the untied label equations. It does not impose tied weights on an off-commuting flow. The general matrix source is

\[
M'_p=R_pP_U+P_WR_p,
\]

not an automatically symmetric tied-model field. It reduces to the diagonal expression only under the stated commuting conditions.

### Finite width and positive-quadrant initialization

The result holds at finite width when the initial Gram is *exactly* diagonal. It does not prove the absence of small reversals for every random finite-width seed or every finite sample covariance.

The positive-quadrant Gram is exactly `S0 [[1/2,1/pi],[1/pi,1/2]]`. This leaves the diagonal mechanism and supplies minor entries, but nonzero minor entries alone do not prove Swing-by for every parameter choice, probe, or tied/untied architecture.

## 4. Limiting permanence audit

Write

\[
\epsilon=(1-n)(v-y)>0,\quad d=v-x>0,\quad P=\Phi(\rho x),\quad \lambda=\rho^2.
\]

The exact selected-orbit equations yield

\[
x'=\tfrac\lambda2(d-\epsilon)P,\qquad
 d'=\tfrac\lambda2[g_\rho(x)-(1+P)d+\epsilon P].
\]

The imported growth bound implies `epsilon <= C(1+s) exp(-lambda s)`. Hence `(x')_- <= lambda epsilon/2` is integrable. The previous theorem's arbitrary-level hitting property gives unbounded forward limsup. Finite negative variation then gives `x -> infinity`, which is enough for eventual permanent gate inactivity. There is no requirement to prove monotonicity before concluding permanence.

### Repair of the proposed monotonicity proof

The assertion “the vector field points downward when `d > g_rho(x)+epsilon`, therefore `d` eventually tracks that moving graph” was not justified. A time-dependent threshold needs its own derivative control.

The repaired argument bounds `d` by a fixed constant `D`, then uses

\[
(x+v)'=\tfrac\lambda2[g_\rho(x)-(1-P)d-\epsilon P]
\le\tfrac\lambda2g_\rho(x).
\]

Since `x = (x+v-d)/2`, a scalar integral transform gives `x = O(sqrt(log s))`. Restricting the Gaussian tail integral to a unit interval gives a polynomial lower bound for `g_rho(x(s))`. The equation for `d` then gives a polynomial lower bound for `d`, which eventually exceeds exponentially decaying `epsilon`. Thus `x' > 0` eventually.

The permanence proof itself is shorter and independent of this stronger proposition. Neither proof claims that the probe never re-enters immediately after its first gate hit.

### What “permanent” applies to

The exact conclusion is `mathcal E_zeta(s) = 0` for all sufficiently late times in the selected *limiting ODE*. It means the entire leading negative `q^2` coefficient is eventually returned. It is not an infinite-time assertion about the finite-noise isotropic network. In particular, an experiment ending at physical time 100 establishes persistence through that horizon, not permanent behavior at all later times.

The training system does not depend on the probe, so continuing its limiting ODE beyond the probe gate is legitimate. Applying that continued orbit to finite `q` requires new approximation estimates: eventually the scaled coordinates diverge and the bounded-chart expansion cannot be applied uniformly forever at fixed `q`.

## 5. The initialized persistence target needs a corrected interface

A lower bound `E >= 1/2 - epsilon_q q^2`, with `epsilon_q -> 0`, cannot begin at a centered time whose limiting error coefficient is still strictly negative. The start must be after an analytically selected limiting clearing or sufficiently late near-recovery time. An arbitrary fixed delay after the reversal is not automatically enough.

A growing horizon need not be guessed. If the initialized original flow converges in the **rescaled error** on every fixed centered interval, and the limit has uniform eventual zero error coefficient, an analytical diagonal argument produces some `T_q -> infinity` with a vanishing error floor. This is a conditional observation only. Theorem A's convergence restricted to its crossing windows is not enough.

It is not necessary to make every neuron inactive. The sufficient observable condition

\[
[\xi^\top f(\xi)]_+\le\epsilon_q q^2
\]

already gives the required lower bound. The exact isotropic population has positive mass in every open input-angle arc at every finite time under the established degree-one/positive-mass conditions. Background output and its training effects must therefore be bounded, not declared absent.

For the broad split limiting population, eventual persistence itself remains a separate analytical question. The coherent proof is not automatically a population theorem.

## 6. Timing-fit interpretation: distinguish total-time and entry-seed exponents

The new reported sweep fit is scientifically useful but does not identify the AN3 resident-entry seed exponent by multiplying the *total* weak-learning time slope by `rho^2`.

If at an entry time

\[
\tau_{\rm ent}=b_{\rm ent}\log(1/S_0)+O(1),\qquad
N_{\rm ent}\asymp S_0^{c_0},
\]

and the subsequent mass law is logistic to the required accuracy, then

\[
\tau_h=\tau_{\rm ent}
 +\lambda^{-1}\log\frac{1-N_{\rm ent}}{N_{\rm ent}}
 =\left(b_{\rm ent}+\frac{c_0}{\lambda}\right)\log(1/S_0)+O(1).
\]

Thus `c0 = lambda (b_h - b_ent)`, not `lambda b_h`, unless entry-time dependence has already been removed. As an illustration only, the reported slopes `b_h = 2.30`, `b_ent = 0.995`, and `lambda = 4/9` give `c0 ~= 0.58`; multiplying the total slope gives the different effective time-zero seed exponent `1.02`.

This does not determine the actual resident-entry exponent, because the correct entry clock must itself be specified and the relevant family mass measured. Also distinguish a `mathsf m_2 = 1/2` response clock from an `N = 1/2` family-mass clock. The two agree only after the needed model/observable comparison.

## 7. How this affects manuscript scope

A coherent analytical paper can pair the exact linear architecture control with the selected limiting reversal and permanence results, then use the full scaled-population identities to explain bridge effects empirically and mathematically where proved. Full analytic control of canonical-sized depth enhancement is not required to state those valid results.

However, that is not completion of the original initialized Theorem A. If initialized selection is omitted, the theorem must explicitly concern the selected limiting orbit or a conditional class of entry states. A theorem-backed mechanism, a numerical population witness, and a theorem from isotropic initialization are three different evidentiary levels.

Recommended empirical language:

- “Off-cone reversals specific to ReLU under the tested matched initialization/data regime,” not a universal exclusion for all linear networks.
- “Persistent through the long-horizon experiment,” not infinite-time permanence of the finite network.
- “Initialization geometry enables/restores compositional Swing-by in the tested controls,” not initialization as its only cause.
- Keep the reported preregistered H1 failure and corrected preregistration separate from post-hoc descriptive claims.
- The lag collapse is the dominant fading-help factor over the stated crossover window; exposure loss can remain important later. Different time windows should not be conflated.

The seed fits, depth/spread fits, producer split, and selector counts in the user's new report were not independently rerun for this increment. In particular, a small empirical residual of a depth-versus-variance fit does not imply a uniformly small perturbation of the underlying population dynamics.

## 8. Suggested integration after review only

1. Integrate the general linear statement as an extension or presentation of P10, not as a duplicate claim of novelty.
2. Place the eventual-persistence theorem after `pa:limitreversal`; retain the short finite-downward-variation proof.
3. Keep eventual monotonicity as a separate strengthening.
4. Keep the growing-window implication explicitly conditional in the future-persistence section.
5. Do not mark initialized A, B, finite-noise transfer, or large-bridge comparison complete.

## 9. Checks and limitations

The source was compiled twice with `pdflatex`. All seven pages were rendered and inspected, with the monotonicity proof inspected at reading resolution. There are no remaining LaTeX warnings or overfull boxes. The displayed cluster-source counterexample was checked with exact rational arithmetic.

No differential equation was numerically integrated for this increment, and no experimental array was re-evaluated. The proofs are analytical arguments with the stated imported dependencies, not a machine-checked formalization. Independent mathematical review is still required before merging.

SHA-256 hashes of the seven protected input files were compared before and after generation and were unchanged.
