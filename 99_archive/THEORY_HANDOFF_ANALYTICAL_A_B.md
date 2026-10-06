# Analytical-only theory handoff: initialized ReLU population reversal

**Companion checkpoint:** `THEOREM_A_ANALYTICAL_PROGRESS.tex` (version 1.0).

**Goal:** prove Theorems A and B rigorously by a **unified analytical argument**. Theorem A is initialized signed competition and OOD reversal. Theorem B is the reciprocal leakage–compensation mechanism that forces that competition. The canonical bridge and the coherent small-initialization limit belong to one population system.

**Current status:** the initialized theorems are **not proved**. There are exact finite-parameter identities, analytical early-escape estimates, an analytical reversal theorem on the selected coherent limiting orbit, and several population-level sign/shape results. Global initialized entry, nonlinear resident passage, non-small bridge dynamics, and sufficiently sharp finite-noise signed estimates remain open.

This handoff supersedes the numerical-certificate route in the old `THEORY_HANDOFF_THEOREMS_A_B.md` and the continuation sections of `theorem_A_initialized_escape`.

---

## 0. Instructions to the next chat — read before doing mathematics

### The proof objective

Work on **analytical proofs**, not a computer-assisted proof of a numerical trajectory. The final proof must stand without `labels.npz`, a reference run, floating-point sign tests, or a program that verifies a discretized trajectory.

Allowed methods include exact Gaussian integration, differential inequalities, invariant regions, first-exit bootstraps, analytic comparison flows, perturbation theory with proved remainders, characteristic transport, and saddle-passage arguments whose hypotheses are checked analytically. An implicitly defined analytical orbit is allowed; a closed elementary formula for every trajectory is not required.

Do **not** switch to interval arithmetic, validated numerics, cellwise interpolation around saved states, reference-array-dependent error tubes, numerical eigenvalue envelopes, or a certificate-first/theory-later strategy. Ordinary analytical stability is allowed when its comparison object and needed properties are established analytically. The word “stability” does not authorize a return to the old numerical certificate program.

Default to mathematics, not new experiments or diagnostic scripts. Existing computations may motivate a conjecture or falsify a proposed inequality; they do not discharge a lemma. Symbolic simplification, source inspection, and LaTeX compilation are tools for writing/checking work, not substitutes for the displayed proof. Do not report numerical evaluations such as `κ ≈ 1.75053` or `ρ_c ≈ 0.76` as analytically proved constants or phase transitions.

The mechanism must do the work: derive the learning, leakage, compensation, exposure, and input-rotation inequalities that imply the crossover. Do not assume the reached state already has the desired signs and call that an initialized theorem. Conditional intermediate lemmas are legitimate, but their entry assumptions must be removed in the final theorem.

**Do not access or modify GitHub.** The user handles commits and supplies files. Do not modify the foundation file, the notebook, the old appendix, or the consolidated checkpoint while exploring a new proof.

### Deliver new mathematics in separate review files

Every substantive proof increment must be delivered as separate, versioned files, for example:

```text
AN02_isotropic_entry_v1.tex
AN02_isotropic_entry_v1_review.md
```

The `.tex` should be standalone or have a clearly declared dependency on the supplied foundations/checkpoint, with every statement and proof readable without numerical arrays. Prefer standalone compilation for review. Use a unique label prefix, such as `inc:AN02:v1:`.

The accompanying review note must contain:

1. **What is new:** the precise mathematical advance, not only a restatement of the plan.
2. **Proof contract:** assumptions, conclusion, dependencies by label, and the next lemma it unlocks.
3. **Status:** exact original-flow result; result within the defined limiting system; conditional estimate; formal/derived expansion; conjecture; or numerical evidence.
4. **Audit points:** every first-exit condition, sign margin, division, limit exchange, differentiation under an integral, gate boundary, and uniformity claim that carries weight.
5. **Open residue:** the exact inequality or argument still missing. If an attempt fails, preserve the failed step and its reason rather than quietly adding an assumption.
6. **Proposed integration location:** where the result would go in a later checkpoint, and what it supersedes or depends on.

Do not overwrite an earlier increment. Do not add it to `THEOREM_A_ANALYTICAL_PROGRESS.tex` or automatically `\input` it there. **First the user and/or another agent checks it. Only after explicit user approval should a new consolidated version be produced**, with a changelog and an old-to-new label map. A proof claim made by the producing chat is not itself approval to merge.

The present checkpoint is a consolidation **for review**. Treat its recorded proofs as the working analytical base, but report any error found explicitly. Do not silently repair a source statement and then attribute the repaired theorem to the unchanged source.

### What to do first

Read this handoff, then the notation/status ledger and relevant sections of the checkpoint, then the required foundation propositions. Pick the first unresolved quantitative lemma in the initialized dependency chain and begin an actual proof. The central missing step is **AN2: isotropic entry and weak-seed capture**, designed to provide the inputs required by AN3. AN1, the exact finite-noise lag closure, is a useful parallel mechanism problem.

Do not spend the response producing yet another broad overview or expanding foundations unrelated to the bottleneck. A narrowly stated sublemma with a rigorous proof is useful; a stronger claim with an unproved reachability/sign assumption is not completion.

---

## 1. Source hierarchy and what each file means

### Essential files

| File | Role |
|---|---|
| `THEORY_HANDOFF_ANALYTICAL_A_B.md` | Current objective, review protocol, correction ledger, and proof roadmap. |
| `RELU_POPULATION_FOUNDATIONS_v2.tex` | Frozen finite-parameter foundations: exact flow, balance, Gaussian calculus, exact rates, learning observables, gate-aware regularity, linear control, and other structural propositions. |
| `THEOREM_A_ANALYTICAL_PROGRESS.tex` | New consolidation of post-foundations analytical progress. It contains numbered statements/proofs and explicit open obligations. It is not a completed proof of initialized A or B. |

### Supporting mathematical sources

| File | Use and limitation |
|---|---|
| `LEAK_COMPENSATION_FACTORIZATION_AUDIT.md` | Exact source-by-motion factorizations and remainder identities. Its old numerical-continuation priorities are superseded. |
| `TWO_NEURON_SMALL_NOISE_LIMIT.md` | Derived six-dimensional leading system and selected-orbit reversal proof. Use the later real weak-root correction and the population splitting correction in the checkpoint. |
| `SCALED_POPULATION_SPLITTING_THEORY.md` | Full scaled population, stable means/unstable shapes, population lag positivity, error/covariance law, and second-order response. Finite-noise and initialized applications remain open. |
| `theorem_A_initialized_escape.pdf` or its source | Retain **Sections 1–3 only** as the analytical early-escape layer. The numerical-reference construction from Section 4 onward is not the current proof strategy. |
| `SIM.md` and the original SIM paper | Data model, terminology, and historical growth–suppression intuition. The predecessor’s tied linear matrix dynamics are not the untied ReLU dynamics. |
| `main-15.tex` | Historical research notebook, not a finished unified theory or the current source of truth for initialized competition. |
| `main-appendix...tex` / `ood_reversals-appendix.tex` | Historical appendix with incomplete/conditional theory. Do not import its learned-state entry assumptions as if proved from initialization. |

### Empirical material

`population_law_checks.py`, `split_mode_checks.py`, `pilot_mechanism_analysis.py`, the CSVs, and the user’s reports are diagnostics and experimental provenance. The new chat does not need trajectory arrays to begin analytical proofs. Do not claim to have reproduced runs when only their scripts or summaries are available.

If source versions disagree, the latest explicitly documented correction takes precedence for the working plan, but record the discrepancy. A newer prose summary must not silently promote an older formal derivation into a uniform theorem.

---

## 2. Locked setting, notation, and units

We specialize the SIM task to **two informative concepts in the plane**, with no origin cluster:

\[
P_1=\mathcal N(e_1,q^2I_2),\qquad
P_2=\mathcal N(\rho e_2,q^2I_2),\qquad
P=(P_1+P_2)/2,
\quad 0<\rho<1,\ q>0.
\]

The targets are `y = X`. The network is bias-free, two-layer ReLU, with both layers trained independently:

\[
f_h(X)=\sum_{i=1}^h w_i(u_i^\top X)_+,
\qquad \mathcal L=\tfrac12\mathbb E_P\|f(X)-X\|^2.
\]

The initialization is **aligned-balanced isotropic**, not merely norm-balanced:

\[
u_i(0)=w_i(0)=\sqrt{S_0/h}\,a_{\alpha_i},
\quad a_\theta=(\cos\theta,\sin\theta),
\quad \alpha_i\sim\mathrm{Unif}[0,2\pi).
\]

The continuum label law is `λ₀(dα)=dα/(2π)`, with

\[
U_\alpha=\sqrt{m_\alpha}a_{\theta_\alpha},\quad
W_\alpha=\sqrt{m_\alpha}b_{\psi_\alpha},\quad
\nu=\int m_\alpha\delta_{(\theta_\alpha,\psi_\alpha)}\,d\lambda_0,
\]

\[
\theta_0=\psi_0=\alpha,\qquad m_0=S_0,\qquad
f_\nu(X)=\int b_\psi(a_\theta^\top X)_+\,d\nu.
\]

Thus `S₀ = h ε_h²` is fixed in the width limit and

\[
f_0(X)=S_0X/4.
\]

Balance is preserved; vector alignment generally is not. Use `s = d = 2` only for the number of concepts and dimension; do not reuse `s` for initialization mass. In the limiting equations below, `λ = ρ²` is a scalar growth rate, not the label law `λ₀`. A shifted weak-learning clock is denoted `s` when explicitly introduced.

Physical normalization:

\[
\rho=\mu_2/\mu_1,\quad q=\sigma/\mu_1,\quad
\tau=\mu_1^2t_{\rm phys}.
\]

There is no additional time factor from width. For a fixed numerical unit probe,

\[
D_p^{\rm phys}=\mu_1^2D_p^\tau.
\]

Do not additionally rescale the probe while using that formula. The canonical physical scaling has `μ₁ = 3`, so `τ = 9t_phys`.

Use target-minus-output residual `e(X)=X−f(X)`:

\[
R_p(\theta)=\mathbb E_{P_p}[e(X)X^\top\mathbf1_{a_\theta^\top X>0}],
\quad R=(R_1+R_2)/2.
\]

Then

\[
\theta'=b^\top Ra^\perp,\quad
\psi'=(b^\perp)^\top Ra,\quad
(\log m)'=2b^\top Ra.
\]

The exact cluster decomposition is

\[
V_p(\xi)=\int\left[(a^\top\xi)_+R_pa
+\mathbf1_{a^\top\xi>0}bb^\top R_p\xi\right]d\nu,
\quad
D_p^\tau=-\tfrac12 e_\xi^\top V_p(\xi),
\]

\[
E_\xi'=D_1^\tau+D_2^\tau.
\]

The factor `1/2` is the equal mixture weight. Every neuron and both actual selectors are included. Interpret derivatives almost everywhere unless the required pointwise regularity and boundary conditions are proved.

Learning must be measured by exact observables, for example

\[
\mathsf m_p=\frac{\mathbb E_{P_p}[X_pf_p(X)]}{\mathbb E_{P_p}[X_p^2]},
\qquad
\mathcal L_p=\tfrac12\mathbb E_{P_p}\|f(X)-X\|^2.
\]

A mass called “weak” is not by itself a proof of weak learning.

---

## 3. Theorems A and B: target statements, not completed results

### Theorem A — initialized population signed competition and reversal

Prove a nonempty, explicitly specified admissible parameter region with moderate concept ratio, a positive-length interval of scaled probe offsets `I = [ζ₋,ζ₊]`, and a learned time interval `J` reached from the exact isotropic initialization such that:

\[
\xi_q=(\sin(q\zeta),-\cos(q\zeta)),\qquad \zeta\in I.
\]

On `J`, both concepts satisfy a genuinely nontrivial response threshold and preferably a fixed cluster-loss reduction:

\[
\mathsf m_p\ge c_{\rm learn}>0,
\qquad
\mathcal L_p\le(1-\kappa_p)\mathcal L_p(0),\quad \kappa_p>0.
\]

The constants must not degenerate with vanishing initialization in the claimed regime. A threshold such as `1/2` is a useful target, but is not already proved.

Uniformly over the stated probe/parameter set,

\[
D_1^\tau\le-c_1q^2<0,\qquad D_2^\tau\ge c_2q^2>0
\quad\text{on }J,
\]

and there are ordered positive-width windows `J₋` and `J₊` inside `J` with

\[
D_1^\tau+D_2^\tau\le-\gamma_-q^2\quad\text{on }J_-,
\]

\[
D_1^\tau+D_2^\tau\ge\gamma_+q^2\quad\text{on }J_+.
\]

Integration then gives a quantitative OOD rebound `≥ c_rev q²` on a sector of angular width `≥ c_I q`.

**Scope guards:**

- The trajectory starts at time zero, but the opposite-sign conclusion is local to a learned interval. The actual weak-cluster rate becomes briefly negative earlier in training.
- The final theorem must remove any learned-state entry assumptions by proving them from initialization.
- A small-noise/small-initialization theorem is a legitimate intermediate result, but it must not be advertised as covering `(ρ,q,S₀)=(2/3,.05,2e−4)` unless its bounds include that point.
- The coherent limit and canonical bridge share one mechanism/model; this does not make finite-parameter coverage automatic.
- No unique crossing, permanent non-recovery, exact timing constant, finite-width lift, or arbitrary-dimensional extension is required for the first A.

### Theorem B — reciprocal compensation and the inactive-bridge mechanism

Along the same initialized population evolution, prove:

1. Gaussian cross-output leakage from probe-inactive labels produces a compensating response in the active strong population.
2. Cluster-1 help is controlled by **exposure × an exact compensation lag**, with every finite-parameter correction bounded below the relevant sign margin.
3. The selected cluster-2 residual rotates the active population’s inputs in the harmful direction. Training source, motion carrier, and residual producer are distinguished.
4. A non-small inactive bridge affects the active population through overlap forcing and output compensation, together with its induced weak-family feedback. It need not be directly active at the probe.
5. The analytical time evolution of these quantities forces the dominance switch in A.

The leading population help identity is exact within that model. Its finite-`q` counterpart is a representation **with a remainder**, not automatically an exact identity after substituting an exact lag.

The small-split `κ Var` formula is an optional local corollary. It is not the primary explanation of the canonical run, where the inactive bridge is outside the small-splitting regime.

---

## 4. What is already available — use the checkpoint labels

The LaTeX checkpoint labels below are stable reference points. “Proved within the leading system” means exactly that, not initialized finite-noise validity.

| Result | Status / scope | Checkpoint label |
|---|---|---|
| Exact flow/rates/learning and linear control | Imported from foundations; no initialized late signs | `pa:setup` |
| Spectral residual bound, mass/alignment/radius envelopes | Analytical from isotropic initialization | `pa:earlybounds` |
| Exact target-only comparison | Analytical finite-time comparison, not a numerical reference | `pa:targetcomparison` |
| Canonical early mass escape | `S(6)>16S₀=.0032` in normalized time; not weak learning | `pa:canonicalescape` |
| Full source-by-motion rate decomposition | Exact finite-parameter identity | `pa:motion` |
| Gaussian projection compensation | `c_A = −ℓ_I + r₂₁` exactly | `pa:projection` |
| Help/harm factorization with all errors | Exact finite-parameter identities, errors not yet bounded along initialized flow | `pa:factorizations` |
| Fixed-label lag tracking equation | Exact identity and conditional comparison; forcing/sign closure open | `pa:tracking` |
| Truncated-Gaussian overlap kernel | Exact, `C¹,¹` on compact sets, not generally `C²` | `pa:overlap` |
| General scaled population equations | Derived leading system; uniform finite-noise transfer open | `pa:leading` |
| Logistic family masses / fixed-label relative weights | Exact within the closed leading family system | `pa:masslaws` |
| Fixed-direction resident curve | Exact within leading system | `pa:resident` |
| Stable coherent block, unstable centered shape | Exact linearization, not nonlinear condensation | `pa:spectra` |
| Moving splitting matrix | Exact first-order shape equation | `pa:moving-shape` |
| Strong-stage and frozen-resident passage multipliers | Exact linearized formulas | `pa:multipliers` |
| Same-field ordering and covariance sign | Conditional on ordered entry, common field, and chart validity | `pa:order` |
| No weak-chart equilibrium at initial zero-mass state | Proved within leading system | `pa:noweakeq` |
| Positive lag for arbitrary weak distribution at `M=1` | Proved within leading system; no condensation required | `pa:lagtheorem` |
| Population probe error and source rates | Exact leading identities; static finite-q expansion has chart assumptions | `pa:probe-pop` |
| Partial-activity/covariance/inactive compensation identities | Exact within leading observable | `pa:active-error` |
| Real weak saddle coordinate for `0<ρ<1` | Proved; old positive-root restriction removed | `pa:weakroot` |
| Distinguished coherent weak-growth branch | Analytical orbit defined by saddle, not fitted angles | `pa:branch` |
| Reversal on that selected orbit | Analytical theorem, not yet isotropic selection | `pa:limitreversal` |
| Exact finite-q mean lag and Stein relation | Exact original-state identities | `pa:Lex` |
| Explicit tail-moment error from mean lag to leading lag | Exact bound, potentially too large at canonical parameters | `pa:lagerror` |
| Finite-q same-field cross derivatives | Exact equality; positivity open in reached regime | `pa:finiteqorder` |
| Non-small instantaneous bridge displacement signs | Exact in leading field; coupled trajectory comparison open | `pa:bridge-force` |
| Small-split second-order response functional | Derived finite-window response; incoming limit and analytical positive coefficient open | `pa:response-eq`, `pa:kappa` |
| Window-to-rebound implication | Proved elementary assembly; initialized hypotheses still open | `pa:assembly` |

The frozen weak-attractor saddle-node near `M≈.4768`, the coefficient `κ≈1.75053`, the seed exponent, and the threshold near `.76` are **not** analytical initialized conclusions.

---

## 5. The unified scaled population model

These equations are worth retaining in the handoff because they define the common analytical object. Let `λ=ρ²` and

\[
K(r)=\phi(r)+r\Phi(r),\qquad K(r)-r>0.
\]

Strong and weak chart coordinates are

\[
a_s=(\cos(qx),\sin(qx)),\ b_s=(\cos(qy),\sin(qy)),
\]
\[
a_w=(\sin(qu),\cos(qu)),\ b_w=(-\sin(qv),\cos(qv)).
\]

For weighted distributions `μ_s(dx dy)` and `μ_w(du dv)`, define total, not normalized, moments

\[
M=\int d\mu_s,\ N=\int d\mu_w,\ Y=\int y\,d\mu_s,\ V=\int v\,d\mu_w,
\]
\[
K_s=\int K(\rho x)d\mu_s,\quad K_w=\int K(u)d\mu_w.
\]

The overlap kernel is

\[
F(t,r)=\phi(\min(t,r))+r\Phi(\min(t,r)),
\]

\[
\partial_tF=(r-t)_+\phi(t),\quad \partial_rF=\Phi(\min(t,r)).
\]

Set

\[
\mathcal S(x)=\int F(\rho x,\rho\widetilde x)d\mu_s,
\qquad
\mathcal W(u)=\int F(u,\widetilde u)d\mu_w.
\]

The leading characteristic system is

\[
\begin{aligned}
x'&=\tfrac12[-(1-M)x+\rho\phi(\rho x)-\rho\mathcal S(x)
+\lambda\{V+(1-N)y\}\Phi(\rho x)],\\
y'&=\tfrac12[-(1-M)y-Y-K_w+\rho(1-N)K(\rho x)],\\
u'&=\tfrac12[\phi(u)-\mathcal W(u)-\{Y+(1-M)v\}\Phi(u)-\lambda(1-N)u],\\
v'&=\tfrac12[\rho K_s-\lambda V-\lambda(1-N)v-(1-M)K(u)].
\end{aligned}
\]

The reaction rates are `(1−M)μ_s` and `λ(1−N)μ_w`, so

\[
M'=M(1-M),\qquad N'=\lambda N(1-N).
\]

One atom in each family is an invariant restriction. The canonical bridge is represented by a spread-out strong distribution, not a separate phenomenological mechanism.

**Do not overlook the scope:** these are bounded noise-scaled charts. The isotropic population does not start there; labels outside them and labels entering them must be controlled. Constant relative family weights are a leading-system statement for fixed labels. They do not justify ignoring mass-rate differences at finite noise or flux through changing masks.

### The stable mean and unstable shape

The resident direction solves

\[
a_\rho=\rho K(\rho a_\rho),\quad
P=\Phi(\rho a_\rho),\quad \alpha=\lambda P/2.
\]

The curve `μ_s=Mδ_(a,a), N=0` has fixed angles for every logistic `M`. Its mean and centered shape matrices are

\[
J_{\rm mean}(M)=
\begin{pmatrix}-(1-M)/2-M\alpha&\alpha\\\alpha&-1/2\end{pmatrix},
\]

\[
J_{\rm sh}(M)=
\begin{pmatrix}-(1-M)/2&\alpha\\\alpha&-(1-M)/2\end{pmatrix}.
\]

The centered `(1,1)` direction becomes unstable at `M>1−2α`. At `M=1` the coherent block is stable but centered splitting grows at `α`. In the continuum there is a family of unstable shape profiles, not literally just one extra scalar dimension.

During weak learning the shape matrix has an additional diagonal term:

\[
J_{\rm sh}(\tau)=
\begin{pmatrix}-(1-M)/2+\beta&A_{\rm sh}\\A_{\rm sh}&-(1-M)/2\end{pmatrix},
\]

\[
A_{\rm sh}=\tfrac\lambda2(1-N)\Phi(\rho x),\quad
\beta=\tfrac{\rho^3}{2}[Nv+(1-N)y-x]\phi(\rho x).
\]

The resident linear multipliers are

\[
\frac{h_+(M_1)}{h_+(M_0)}=
\left(\frac{M_1}{M_0}\right)^{\alpha-1/2}
\left(\frac{1-M_0}{1-M_1}\right)^\alpha,
\]

and, in the separately defined frozen weak-growth approximation,

\[
h_+(N)=h_+(N_0)(N/N_0)^{\alpha/\lambda}.
\]

A nonlinear passage proof must retain moving coefficients and mean feedback. The relevant entry ratio is of the form

\[
\delta_{\rm ent}N_{\rm ent}^{-\alpha/\lambda},
\]

plus mean, weak-angle, outside-population, and finite-noise errors. A small entry shape alone is not sufficient if the weak seed is extremely small.

### Population help and partially active error

At `M=1`, the leading lag is `L₀=Y+K_w`. The positive-lag theorem gives an equation with damping and explicitly nonnegative forcing, including the symmetrized overlap term `Ξ>0`. Consequently positive incoming `L₀` stays positive without assuming condensation.

Set

\[
A_\zeta=\int(\zeta-x)_+d\mu_s,\quad
B_\zeta=\int y(\zeta-x)_+d\mu_s.
\]

Then

\[
\mathcal E_\zeta=\tfrac12A_\zeta^2-\zeta A_\zeta+B_\zeta,
\qquad d_1=-\tfrac12A_\zeta L_0,
\]

\[
d_2=\int_{x<\zeta}(\zeta-A_\zeta-y)x'_2\,d\mu_s
+\tfrac\rho2(1-N)\int(\zeta-x)_+K(\rho x)d\mu_s.
\]

The second term in `d₂` is weak-sourced output rotation. Do not discard it merely because `q→0`. The sign of `d₂` and its takeover for broad split populations remain to be proved.

For active strong mass `M_A`, normalized active means and covariance, and `h=ζ−x̄_A`,

\[
\mathcal E_\zeta=\tfrac12M_A^2h^2-M_Ah(\zeta-\bar y_A)-M_A C_A.
\]

If `Y_B` is the total output-angle moment of the inactive strong population,

\[
\mathcal E_\zeta=
\tfrac12A_\zeta^2-\zeta A_\zeta+h(L_0-K_w-Y_B)-M_A C_A.
\]

This retains the inactive bridge. The all-active simplification with `−Cov(x,y)` is not valid unchanged for a partially active canonical population.

---

## 6. What the coherent limiting reversal theorem already proves

The coherent `M=1` orbit retains logistic weak mass and four angles. Its resident saddle is

\[
(n,x,y,u,v)=\left(0,a_\rho,a_\rho,u_\rho,a_\rho/\lambda\right),
\]

where `u_ρ` is the unique **real** solution of

\[
\phi(u)-a_\rho\Phi(u)-\lambda u=0.
\]

The old restriction `ρ≤1/√2` was only used to get a convenient positive weak root. The real-root formulation extends this selected-orbit result to every fixed `0<ρ<1`; it does not prove population selection across that entire range.

Within the coherent manifold the saddle has one unstable weak-mass direction. Its positive branch is defined analytically, up to translation; set

\[
n(s)=\frac1{1+e^{-\lambda s}}
\]

to put weak half-mass at `s=0`. This is not a fitted initial condition. In the full population there are also unstable centered shapes.

For `ζ>a_ρ`, the existing analytical proof establishes:

- global forward continuation of the selected finite-dimensional orbit, with at most linear coordinate growth;
- positive compensation lag;
- early decrease of the probe observable from the sign of the unstable-branch slope `Y₁<0`;
- invariants `v>0`, `v>y`, `v>x`;
- eventual finite first hit of the strong probe gate `x=ζ`, via an integrable negative part of `x′` and the strictly positive Mills gap;
- a later positive derivative before that hit, hence a sign-changing zero with `d₁<0<d₂` in a common neighborhood;
- a quantitative interior rebound, with a possible lower bound `(ζ−a_ρ)²/4` in scaled error.

See `pa:limitreversal` for the full proof. No numerical root time is used in it.

**Still missing:** matching the actual isotropic population to an admissible coherent-or-split weak-learning evolution; a specified substantial weak-learning threshold at the selected witness; finite-noise transfer; canonical-sized splitting control; and explicit common sector/parameter/time margins. Do not relabel the selected-orbit theorem “Theorem A proved.”

The numerical values `E_scaled,min≈−2.0092456`, `N_cross≈.987928`, and delay `≈1.10119` physical units for `μ₁=3` describe the evaluated orbit. The theorem proves neither a unique/simple crossing nor those decimal values.

---

## 7. Latest correction: exact finite-noise lag and a non-small inactive bridge

### 7.1 Keep the cancellation-defining observable exact

There are three different quantities:

\[
L_0=Y+K_w,
\]

\[
L_{1,q}^{\rm mean}=\frac{\mathbb E_{P_1}f_2(X)}q,
\]

\[
r_{21}=\frac{\mathbb E_{P_1}[X_1(f_2(X)-X_2)]}{1+q^2}.
\]

The first belongs to the leading model; the other two are exact finite-noise observables. Gaussian integration gives

\[
L_{1,q}^{\rm mean}=\int b_2 K(a_1/q)\,d\nu,
\]

and the exact Stein relation is

\[
\frac{1+q^2}{q}r_{21}
=L_{1,q}^{\rm mean}+q\mathbb E_{P_1}[\partial_1f_2(X)].
\]

They are not interchangeable names for the same lag. The helpful product can be built with either appropriate exact observable, but its change of coordinates and all geometric/rate errors must be retained.

On scaled charts,

\[
\begin{aligned}
L_{1,q}^{\rm mean}={}&
\int_s\sin(qy)K(\cos(qx)/q)\,d\mu_s\\
&+\int_w\cos(qv)K(\sin(qu)/q)\,d\mu_w+L_{\rm outside}.
\end{aligned}
\]

An exact bound on its difference from `L₀` is

\[
\begin{aligned}
|L_{1,q}^{\rm mean}-L_0|\le{}&
q^2\int_s\left(\frac{|y|^3}{6}+\frac{|y|x^2}{2}\right)d\mu_s\\
&+q^2\int_w\left(\frac{v^2K(u)}2+\frac{|u|^3}{6}\right)d\mu_w\\
&+\int_s|\sin(qy)|[K(\cos(qx)/q)-\cos(qx)/q]d\mu_s
+|L_{\rm outside}|.
\end{aligned}
\]

See `pa:Lex` and `pa:lagerror`. A generic `O(q²)` error with a large high-moment coefficient can overwhelm a small lag. A canonical theorem may need an exact finite-`q` lag differential inequality rather than a coarse transfer from `L₀`.

The empirical relation using the exact lag is approximately

\[
\frac{D_1^{\rm phys}}{\mu_1^2q^2}
\approx-\tfrac12 A_{q,\xi}L_{1,q}^{\rm mean}.
\]

It is **not an exact finite-noise identity without a remainder**. AN1 must define the exposure precisely, derive the remainder, and prove it is smaller than the lag-dependent margin. The scaled population law at `M=1` remains exactly true in its own scope.

### 7.2 The bridge has analytical instantaneous forcing signs

At a fixed state of the leading model, move strong mass `ε` from `(r₀,s₀)` to `(r_B,s_B)` with `r_B≥r₀`, `s_B≥s₀`, holding total strong mass and weak measure fixed. At a fixed strong receiver `(x,y)`,

\[
\Delta x'=-\tfrac{\epsilon\rho}{2}
[F(\rho x,\rho r_B)-F(\rho x,\rho r_0)]\le0,
\]

\[
\Delta y'=-\tfrac\epsilon2(s_B-s_0)\le0.
\]

If the receiver lies below both donor inputs, this becomes

\[
\Delta x'=-\tfrac{\epsilon\lambda}{2}(r_B-r_0)\Phi(\rho x).
\]

There is no small donor displacement assumption. These are the exposure push and the added output-compensation forcing. But weak receivers also change:

\[
\Delta u'=-\tfrac\epsilon2(s_B-s_0)\Phi(u),
\quad
\Delta v'=\tfrac{\epsilon\rho}{2}[K(\rho r_B)-K(\rho r_0)].
\]

The resulting change in weak compensation feeds back into the strong field. Therefore a global trajectory comparison requires a **coupled inequality system**, not just the instantaneous signs. See `pa:bridge-force`.

### 7.3 Ordering is not a shortcut to comparing different populations

Within a common leading field,

\[
\partial_yx'=\partial_xy'=\tfrac\lambda2(1-N)\Phi(\rho x)\ge0,
\]

so two ordered strong characteristics remain ordered. However, donor couplings between distinct strong atoms are

\[
\partial_{x_j}x_i'=-\tfrac{\lambda m_j}{2}\Phi(\rho\min(x_i,x_j))<0,
\quad \partial_{y_j}y_i'=-m_j/2<0.
\]

Thus the full particle/population evolution is not cooperative in all its coordinates. Comparing a main block with a two-atom run means comparing different residual fields and needs additional control.

At exact finite noise, holding the residual field fixed,

\[
\partial_\psi\theta'=\partial_\theta\psi'
=(b^\perp)^\top R(\theta)a^\perp.
\]

The equality follows from `R′(θ)a=0`. Its positivity on a reached regime is still an obligation. Ordered or approximately ordered entry should be proved from the relevant initialized labels, not taken from a plot.

---

## 8. Detailed lemma roadmap — analytical proof contracts

The order below describes dependencies, not a demand to solve every sublemma sequentially. AN1 and the local part of AN7 can be developed in parallel with global entry. The entry and passage estimates must be designed together so the former is quantitatively useful to the latter.

### AN0 — Fix interfaces and reuse existing results

**Status:** available as the working checkpoint, subject to review of any needed statement.

Use the exact foundations, early escape, exact lag/projection/rate formulas, and the stated leading system. Do not rename a formal reduction “uniform convergence proved.” Do not expand the foundation package indefinitely.

**Unlocks:** precise proof contracts for the remaining steps.

### AN1 — Exact finite-noise lag evolution and helpful-rate closure

**Status:** exact state formulas and conditional tracking are available; signed dynamic closure is open.

**Inputs:** original Gaussian flow; exact mean or weighted lag; a candidate learning region expressed in analytically controllable moments. Candidate regional assumptions may be temporary bootstrap conditions, not final initialized assumptions.

**Required conclusion:** a signed lag differential inequality or exact evolution identity with controlled forcing; a positive lag margin; an exact help decomposition whose remainder is smaller than that margin. Retain the distinction between stored compensation and the current beneficial update.

**Available tools:** `pa:projection`, `pa:tracking`, `pa:Lex`, `pa:lagerror`, exact source-by-motion rates, and the leading population positive-forcing identity.

**Failure to avoid:** an upper bound on `|lag|` is not a proof of positive lag. Large leakage components can each be approximated well while their difference is wrong. Do not close this with the observed 4% product error.

**Unlocks:** analytic strong-help sign and the help side of the dominance comparison, including finite noise.

### AN2 — Global isotropic transport, strong learning, and weak-seed capture

**Status:** central open initialized step; early escape covers only its beginning.

**Inputs:** exactly the uniform aligned initialization and original flow. No pre-existing weak atom, retrospectively selected helpful cohort, or measured entry state.

**Required conclusion:** analytically defined phase/entry times and a decomposition with quantitative bounds on:

- strong response and its mean direction;
- the strong centered shape and the relevant high/tail moments;
- incoming weak mass and weak angular distribution;
- all uncharted/background population and its contributions to output and residuals;
- ordering or almost-ordering where needed, with fixed-label or explicit moving-boundary accounting.

The weak attractor appears during learning. A frozen bifurcation computation near `M=.4768` does not prove capture by the time-varying flow. The seed is produced by the transport of still-arriving labels and must be derived quantitatively.

**Available tools:** `pa:earlybounds`, `pa:targetcomparison`, `pa:canonicalescape`, Gaussian angular formulas from the foundations, and `pa:noweakeq` / the frozen weak equation.

**Unlocks:** AN3 and the initialized version of the mechanism. This is the recommended first main target; isolate a provable angular/arrival sublemma and start there.

### AN3 — Nonlinear contraction and resident passage with competing rates

**Status:** linear rates/multipliers are known; the nonlinear passage estimate is open.

**Inputs:** AN2 entry data, including `N_ent`, `δ_ent`, strong mean error, weak angular error, and outside-population bounds.

**Required conclusion:** propagate this state through resident residence and weak amplification, accounting for the moving split matrix, nonlinear mean feedback, weak relaxation, and nonuniform finite-noise mass rates. Produce either a small-shape exit bound or a bounded non-small ordered-shape class suitable for AN4.

For the small-shape route a schematic target is

\[
\delta_{\rm half}\le
C\delta_{\rm ent}N_{\rm ent}^{-\alpha/\lambda}
+\text{explicit controlled errors}.
\]

A pure-power entry estimate would be useful only if it proves the needed exponent inequality. For example, if analytically established bounds are

\[
N_{\rm ent}\ge c(q)S_0^\gamma,
\qquad \delta_{\rm ent}\le C(q)S_0^\beta,
\]

then the decisive sign is `β−γα/λ`, with the `q`-dependence and nonlinear corrections retained. Do not assume measured `c₀≈1`, `η≈.07`, or the predicted phase boundary.

**Available tools:** `pa:spectra`, `pa:moving-shape`, `pa:multipliers`, kernel `C¹,¹` regularity, and analytic first-exit/variation-of-constants estimates.

**Unlocks:** a reached weak-learning population. Linear stability of the coherent mean does not settle this step because the centered shape is unstable.

### AN4 — Coupled inactive-bridge comparison in a non-small population

**Status:** exact static error and instantaneous displacement identities available; the dynamical comparison is open.

**Inputs:** a reached ordered or almost-ordered population class, including active strong mass, inactive bridge moments, and weak residual moments.

**Required conclusion:** control the bridge-driven exposure push and compensation, the induced weak-family response, and the resulting changes in the active population over a provably long enough interval. Prove a maintained region or comparison, not a state-by-state verbal analogy.

**Available tools:** `pa:active-error`, `pa:order`, `pa:bridge-force`, the full overlap kernel, and exact finite-q lag bookkeeping.

**Failure to avoid:** same-field order is not between-population order. A frozen weak field may give the right instantaneous sign but the wrong accumulated comparison. A large inactive bridge is not replaced by a `κ Var` expansion.

**Unlocks:** the canonical-facing mechanism inequalities. A small-shape stability theorem can be an intermediate result within this same model, but does not automatically cover the canonical tail.

### AN5 — Substantial learning of both concepts

**Status:** open at the reached crossover regime for the original initialized population.

**Inputs:** phase, population, and residual estimates from AN2–AN4.

**Required conclusion:** bounds on exact `𝔪₁,𝔪₂` and a meaningful loss reduction, preferably on the same learned interval used for the source signs. Connect family mass to useful output and residual error. Obtain thresholds that do not vanish with initialization.

**Failure to avoid:** positive mass at a finite selected-orbit time does not justify “weak learning is 99% complete.” Total loss dissipation does not prove monotonicity of every concept response or cluster loss. If a hitting-time clock is used, prove its relevant existence and ordering properties.

**Unlocks:** the part of A that prevents reduction to a dominant-concept theorem.

### AN6 — Harmful selected residual and forced dominance crossover

**Status:** coherent limit reversal proved; reached broad-population and finite-parameter crossover open.

**Inputs:** exact help/lag control and the dynamically reached population class.

**Required conclusion:** a positive harmful contribution, exact source attribution, and early/late inequalities exceeding a complete remainder budget. The controlled regime must survive until the late witness; an unspecified-duration invariant estimate is not enough.

The existing exact decomposition is

\[
D_1^\tau=-B+r_1,\qquad
D_2^\tau=H^{(1)}+H^{(2)}+r_2.
\]

The mechanism-based factorization has

\[
E_\xi'=\frac{M_C}{2}\mathfrak G_{\rm LC}
+\epsilon_H-\epsilon_B+H^{(2)}+r_1+r_2.
\]

A finite-noise exact-lag variant can be used instead if derived consistently. Every nonleading term and omitted label must remain in the estimates.

**Available tools:** `pa:limitreversal`, `pa:pop-help`, `pa:pop-harm`, `pa:factorizations`, `pa:producer`, and the coupled bridge inequalities to be established in AN4.

**Failure to avoid:** signs at mean angles are not signs of weighted rate integrals. At a zero of an averaged residual, covariance need not vanish. Weak harm need not increase monotonically throughout training. Source signs are required only on a common learned interval.

**Unlocks:** the dynamical heart of A and B.

### AN7 — Finite-noise matching and long-time error control

**Status:** leading coefficients and static lag/probe formulas available; uniform initialized transfer open.

**Inputs:** a precise chart/moment class and analytically established entry/passage evolution, or exact finite-noise inequalities that avoid the approximation.

**Required conclusion when using a limit:** uniform control of

\[
(E_{q,S_0}-1/2)/q^2-\mathcal E,
\qquad D_{p,q,S_0}^\tau/q^2-d_p
\]

on relevant centered windows and probe sectors, including gate-boundary and outside-population terms. The errors must be below signed margins and, for help, below the small exact lag margin.

Local fixed-state field tests showing `O(q²)` are not sufficient for a delay of order `log(1/S₀)`. Relative mass corrections can accumulate as `q² log(1/S₀)`. Define the admissible joint regime and track the amplification of errors in the splitting sector.

A condition such as `q² log(1/S₀)→0` may be useful, but is not a theorem by itself and excludes arbitrary fixed-`q`, arbitrarily small-`S₀` sequences. Preserve exact coincidence: finite noise does not generate a shape split from identical atoms under identical equations. A consistent finite-q analytical reference may turn an apparent additive split error into a multiplicative one.

**Failure to avoid:** using unscaled `o(1)` state convergence to preserve an `O(q²)` signal, or discarding Gaussian tails as exactly zero.

**Unlocks:** a statement for actual positive `q` and `S₀`, not only a leading formal model.

### AN8 — Uniform sector/parameter assembly and quantitative rebound

**Status:** elementary integration implication proved; initialized premises open.

**Inputs:** the preceding analytical conclusions, including learning, individual source signs, and early/late total-rate margins.

**Required conclusion:** remove every entry hypothesis, specify the actual admissible parameter set, obtain a nonzero sector and common windows, and integrate to prove rebound. The canonical point is covered only if the inequalities include it.

For normalized windows `[a,b]` then `[c,d]`, the existing assembly lemma gives

\[
E_\xi(a)-E_\xi(\tau_*)\ge\gamma_-q^2(b-a),
\qquad
E_\xi(d)-E_\xi(\tau_*)\ge\gamma_+q^2(d-c).
\]

Source signs and substantial learning are separate premises, not consequences of a total-rate reversal.

**Available:** `pa:assembly`, exact rate identity, and analytic continuous dependence with the necessary gate control.

### AN9 — Optional refinements, not blockers for A

Analytical positivity of the small-split coefficient; a uniform broad-bridge enhancement theorem; timing uniqueness/transversality; long-horizon persistence; finite-width/sample lifting; more concepts/dimensions.

Do not make A wait for these unless a particular estimate is genuinely required in its proof. Conversely, do not append them as corollaries without discharging their additional hypotheses.

---

## 9. Scientific and empirical facts to preserve, without turning them into assumptions

All numerical statements in this section are diagnostic evidence from supplied files or explicitly reported experiments. They are not premises of the analytical proof.

### Canonical signed competition

The fine-trace crossing is near physical time `3.675245` at `−85°`; weak response is reported near `.99`. On saved snapshots:

| Physical time | Total rate |
|---:|---:|
| 3.5 | approximately `−7.93e−4` |
| 4.0 | approximately `+8.41e−4` |

Both cluster signs are as desired there. The actual `D₂` is **negative** near time `2.75`, so the old all-time claim was corrected.

Most of the local swing comes from strong help fading rather than a globally monotone increase of weak harm. The strong outputs become more negatively tilted even as their probe activation decreases: stored compensation can increase while the probe benefits less from it.

### Finite-parameter product and remainder diagnostics

The source-by-motion help product fitted the sampled canonical help within about 1.5%; the first-coordinate harm product within about 5.4% on a later interval. These fits have nontrivial complete remainders. Near the crossover the remainder can matter even when it is small relative to each individual cluster rate.

The source code computes mean-angle residual-producer columns; a theorem about the harmful rate needs the full carrier-weighted producer integral. A static “no-leak” operation was a composite centroid surgery: it changed both residuals and the probe carrier, and did not remove all Gaussian leakage.

### Coherent limit and split enhancement

The selected coherent orbit numerically has scaled minimum about `−2.0092456` and delay about `1.10119` physical units after weak half-mass. Its analytic reversal theorem is independent of those decimals.

The centered small-split response is defined by an explicit variational integral and evaluates numerically to `κ≈1.75053`; independent sub-atom tests agree. Its analytical positivity still needs proof. The direct covariance is most of the small-split coefficient, but is only a minority of reported canonical excess depth. Even some very small initialization runs can have a non-small inactive tail in the relevant scaled coordinates.

### Exact versus leading lag

Latest reported crossing values:

| Initialization mass | Exact mean lag | Leading lag `Y+K_w` |
|---:|---:|---:|
| `2e−8` | .082 | .116 |
| `2e−6` | .083 | .211 |
| `2e−4` | .059 | .363 |
| `2e−3` | .073 | .486 |

The exact-lag exposure product agrees much better with measured help than the leading lag. This is the reason to retain exact Gaussian expectations and control higher moments. It is not evidence that the finite-noise product has zero remainder.

### Non-small bridge and ordering

Reported canonical bridge mass is about `.12`, scaled output angle around `7.2`, and the active block has much more negative input/output means than the coherent orbit. The reported direct active covariance explains only about 12–20% of excess depth across those runs. The large-bridge feedback interpretation is supported by these decompositions and the analytical instantaneous-force signs, but a trajectory theorem remains open.

Sampled strong labels are co-ordered. This supports deriving an ordered/approximately ordered entry class. It does not prove continuum ordering or a comparison between different population residual fields.

### Diagnostic definition guards

- “Weak `u>3`” means below 90° toward the strong axis by more than `3q`. The printed statistic is absolute mass, not automatically a weak-mass percentage.
- Exact lag includes all labels; leading strong/weak moments may exclude background masks.
- Density bins are finite-window averages, not supremum bounds.
- Median-centered RMS is not centered variance.
- Depth below `1/2` differs from improvement from the actual initialization by `(S₀/4−S₀²/32)/q²`.
- The depth formula may be evaluated at the snapshot nearest the crossing while the reported minimum is from a finer trace.
- The exponent `η` and the proposed `ρ_c≈.76` depend on an unproved isotropic entry law.

---

## 10. Things the next chat must not do

Do not infer any of the following:

- “The coherent two-atom angular saddle is stable, so the population condenses.” The centered shape has an unstable sector.
- “There are two unstable directions, therefore the full population has a two-dimensional unstable manifold.” There are many shape profiles.
- “`L₀>0` in the leading model, therefore the exact finite-q lag has the same sign.” Transfer needs lag-relative accuracy or a direct finite-q argument.
- “Using the exact lag makes the finite-q help product exact.” Other rate/geometric terms remain.
- “The population is ordered, therefore adding a bridge preserves an order versus a two-atom run.” The residual field changes and donor cross-couplings are not all nonnegative.
- “Gaussian population training has no gate issue.” Gaussian integration smooths training fields; probe-rate stability still depends on neuron mass near probe gates.
- “No atoms at finite time” or “background exactly frozen” without proof. Gaussian tails are nonzero.
- “Positive family mass means the concept is substantially learned.” Use actual responses/losses.
- “A static coherent collapse proves what a coherent network would learn dynamically.” It does not integrate a counterfactual trajectory.
- “The old appendix’s learned-state entry holds because the pilot reaches it.” Numerical evidence is not the initialized analytical lemma.
- “An asymptotic theorem already explains the canonical amplitude quantitatively.” Prove the canonical bounds or state the limitation.
- “A plot shows persistence, so no eventual recovery is possible.” Finite-horizon persistence and asymptotics are distinct.

The point of these guards is to keep the proof honest and useful, not to block analytical attempts. A conditional lemma is valuable when its missing hypotheses are explicitly linked to earlier open tasks.

---

## 11. Suggested opening prompt to paste into the new chat

> Read `THEORY_HANDOFF_ANALYTICAL_A_B.md`, the supplied `RELU_POPULATION_FOUNDATIONS_v2.tex`, and `THEOREM_A_ANALYTICAL_PROGRESS.tex`. Our goal is to prove initialized Theorems A and B by one analytical mechanism argument. Do not pursue computer-assisted proofs, interval continuation, or sign certificates around saved numerical trajectories. Use the full population model, exact finite-noise lag bookkeeping, and the inactive-bridge mechanism; the two-atom orbit is an analytically solved special case, not an assumed stable reduction.
>
> Identify the first unresolved quantitative sublemma in AN2/AN3, state its assumptions and required conclusion precisely, and begin its proof. Coordinate its required error/seed bounds with AN1 and AN4 so the result is useful for the later crossover. Do not replace proof work with another broad overview. A rigorously completed narrower lemma is preferable to an unjustified stronger result.
>
> Keep the foundational propositions and the consolidated checkpoint unchanged. Give every new proof increment in a separate versioned `.tex` file and a companion review `.md`, with unique labels, dependencies, scope, proof status, and remaining gaps. We will check those files first. Only after my explicit approval should the accepted material be transferred into a new version of the theorem A LaTeX document. Do not call GitHub; I handle commits.

---

## 12. Build and provenance

The checkpoint is a standalone LaTeX document; it does not `\input` the foundations or any unreviewed increment. Compile twice for references:

```bash
pdflatex -interaction=nonstopmode -halt-on-error THEOREM_A_ANALYTICAL_PROGRESS.tex
pdflatex -interaction=nonstopmode -halt-on-error THEOREM_A_ANALYTICAL_PROGRESS.tex
```

Compilation checks typesetting, not theorem correctness. The checkpoint contains the post-foundations progress needed to begin work, so the original exploratory notes are supporting references rather than mandatory prerequisites for every sublemma.

Full source hashes for this consolidation follow. No source file was modified.

```text
eefd557e0c725c87ea6b41d0d144b92e14f895f0b7f0095d509915b14a9de3f1  RELU_POPULATION_FOUNDATIONS_v2.tex
fed996786979ed1051cb55183be3353948af239ef8a86094bc94ba6654082acb  RELU_POPULATION_FOUNDATIONS_v2.md
6112f8fd549adab4ba1f2226a65e66d1aefdf0a449fd15a0568a4f6ed2372fdb  LEAK_COMPENSATION_FACTORIZATION_AUDIT.md
7f4e2f74b83e0c8c7331d985671c12829e2bfe727f21d2cdbec8a173641b036b  TWO_NEURON_SMALL_NOISE_LIMIT.md
68043ab7b75be2b64f445fbc39bbce00dd111f2f07cf9b1a6d97d89e69c55815  SCALED_POPULATION_SPLITTING_THEORY.md
d7fedf43821b4cc13ba9bb8e51cb67fa6f3d0d35ab48f08f05a1238d7e5791c5  theorem_A_initialized_escape.pdf
672a8d492237c0508dea37f9af89b8da9946ecc777608a30a00f33fcbc68efa7  SIM.md
32e6f576432c6e2f9c91c329e9bfbe3a7acb43cb032f3fcf628aadaa3f9914d1  population_law_checks.py
411081436c9bccf946ce6b7ea9c71056a2f755067b6ee5101b3247edec078c70  split_mode_checks.py
```

The exact finite-noise mean-lag/Stein/tail-bound and bridge-displacement proofs were developed in the latest conversation and are consolidated under `pa:Lex`, `pa:lagerror`, and `pa:bridge-force`. Use these stable labels rather than relying on section numbers after future approved merges.
