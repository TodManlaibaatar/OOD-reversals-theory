# Review increment: signed growth and weak-coordinate retention

**Proof file:** `SIGNED_GROWTH_WEAK_RETENTION_v1.tex`  
**Reading copy:** `SIGNED_GROWTH_WEAK_RETENTION_v1.pdf` (7 pages)  
**Label prefix:** `inc:SGWR:v1:`  
**Status:** analytical proofs supplied for independent review; not merged into the checkpoint. Initialized A/B remain open.

## 1. What changes

The main retention interface now retains the **signed** integrated log-mass rate. The old negative-budget proposition remains a valid corollary, but it should not be used to estimate the amplification that generates the weak seed: it has discarded that amplification by construction.

A new exact weak-coordinate amplitude

\[
z_\alpha=(U_{\alpha,2}+W_{\alpha,2})/2,\qquad h_\alpha=z_\alpha^2
\]

avoids treating the geometric factor in radial growth as a permanent loss in the exponent. At aligned initialization it equals `S0 sin²(alpha)`. Its finite-noise equation retains signed residual-matrix defects and does not assume that the input and output vectors remain aligned.

There are also two supporting results: an exact Gaussian sector bound for the amplitude defect, and a uniform contraction estimate for the **frozen** resident weak equations. These expose the quantities the actual capture proof must control; they do not themselves prove those trajectory bounds.

## 2. Sources and availability

The exact equations, balance, global labeled regularity and positive mass come from `RELU_POPULATION_FOUNDATIONS_v2.tex`, P1–P2 and P5. The earlier retention inequality is in `LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex`, Proposition 5.1. The root statement is `pa:weakroot` in `THEOREM_A_ANALYTICAL_PROGRESS.tex`. The ratio interval and elementary resident estimate are from `AN06_learned_orbit_witnesses_v2.tex`.

The user identified the additional source as:

- `AN02_strong_ancestry_and_tail_transport_v1.tex`;
- Theorem 5.1, `inc:AN02:tail:v1:profiletheorem`;
- equation `inc:AN02:tail:v1:globalG`.

That file was not located in available Files results or the mounted runtime. Some earlier uploads have expired. Only the formula in the current message is used here, as a **conditional premise**. The full theorem, its one-sided norm, center definition, `b_c`, and any `U_c` hypothesis still need review after re-upload. The present file does not purport to reproduce or correct that source.

## 3. Statements and proof contracts

| Label suffix | Statement | Status |
|---|---|---|
| `jensen` | Initial-mass-weighted signed Jensen bound, plus the exact current-weight log-mass identity | Exact original-flow implication for a fixed set of labels |
| `ampflow` | Signed evolution of `(U2+W2)²/4`, relative to a rank-one weak comparison field | Exact original-flow identity under positive weak-coordinate amplitude |
| `ampcohort` | Cohort lower bound retaining weak growth and the initial `sin²(alpha)` amplitude | Conditional original-flow estimate; angular and integrated-defect guards remain to prove |
| `gaussiandefect` | Full residual-matrix defect bound on an interior quadrant-II sector | Exact static Gaussian estimate; no trajectory smallness is asserted |
| `contraction` | Global attraction of the frozen resident weak equations, and uniform exponential contraction on the AN06 ratio interval | Result within the explicitly specified frozen scaled system, with a forced-equation extension |
| `globalexponent` | Net exponent and loss budget using the quoted global profile multiplier | Conditional algebra; not a re-verification of the unavailable tail theorem |

### Signed mass identity

For a fixed label set `C`, put

\[
I_\alpha=\int_{\tau_a}^{\tau_b}r_\alpha(t)\,dt,\qquad
 d\pi_a=\frac{m_\alpha(\tau_a)1_Cd\lambda_0}{N_C(\tau_a)}.
\]

Then

\[
N_C(\tau_b)=N_C(\tau_a)\int e^{I_\alpha}\,d\pi_a
\ge N_C(\tau_a)e^{\int I_\alpha d\pi_a}.
\]

The exact log-ratio instead uses the **evolving** mass-weighted law: `log(Nb/Na) = integral <r>_(pi_t) dt`. These should not be confused. A captured subset needs its own fixed-label estimate and initial mass fraction; a bound for the entire reservoir is not automatically a bound for that subset.

### Weak-coordinate amplitude

Write exactly

\[
R_\alpha=\frac\lambda2(1-c)e_2e_2^\top+\mathcal B_\alpha,
\qquad c(t)\in[0,1].
\]

With `chi = (a2+b2)/2 > 0`,

\[
(\log h_\alpha)'=\lambda(1-c)+\varepsilon_\alpha,
\]

\[
\varepsilon_\alpha=2\mathcal B_{22}
 +\frac{\mathcal B_{12}W_1+\mathcal B_{21}U_1}{z_\alpha}.
\]

If `chi >= k > 0`, then `|epsilon_alpha| <= 2 ||B_alpha|| / k`. In particular, with a uniform integrable matrix bound `d(t)`,

\[
N_C(\tau_b)\ge H_C(\tau_a)
\exp\left(\lambda\Delta\tau-\lambda\int c-\frac2k\int d\right).
\]

At initialization,

\[
H_C(0)=S_0\int_C\sin^2\alpha\,d\lambda_0.
\]

The scalar `c` is a comparison response. It is not defined to be a weak mass. Choosing `c=N` must be accompanied by the required residual estimates.

### Exact Gaussian matrix bound

On `a1 <= -eta < 0`, `a2 >= s_* > 0`, let

\[
\epsilon_2(c)=\|f-cX_2e_2\|_{L^2(P_2)}.
\]

The proof supplies

\[
\|\mathcal B_\alpha\|\le\frac12\left[
(1+S)(1+2q^2)\Phi(-\eta/q)+q^2
+(\lambda+2q^2)\Phi(-\rho s_*/q)
+\sqrt{\lambda+2q^2}\,\epsilon_2(c)\right].
\]

This retains all labels through the total output and total mass. The residual norm is a genuine remaining quantity to bound. Signed cross contractions can improve the conservative norm bound and should not be thrown away when their sign is favorable.

### Frozen weak attraction

For `M=1, N=0` and a coherent strong resident at `(a,a)`,

\[
u'=F_\rho(u)=\frac12[\phi(u)-a\Phi(u)-\lambda u],
\qquad v'=\frac12(a-\lambda v).
\]

The root lemma gives global scalar attraction for every fixed `0<rho<1`. On `rho in [13/20,7/10]`,

\[
F_\rho'(u)\le-69/800 \qquad(u\in\mathbb R).
\]

The proof uses `(t-a)phi(t) <= t phi(t) <= phi(1) < 1/4`, not a numerical derivative bound. Additive forcing is handled by a displayed variation-of-constants estimate.

This is global in the real coordinate of the **frozen leading ODE**, not a uniform justification of that ODE for original input angles a fixed distance from the weak axis. The latter would require `u = O(1/q)`, outside a bounded-chart expansion.

## 4. Global-multiplier exponent bookkeeping

From the formula quoted in the message,

\[
G_\infty=\sqrt{M_a/M_b}\sqrt{N_b/N_a}\,e^{\int b_c},
\]

and the conditional common-time entry bounds

\[
N_a\ge c_0S_0^{1-\lambda+b},\qquad
\delta_a\le C_sS_0^{1/2-\alpha-b_s},
\]

an integrated center cost `integral b_c <= B_p + b_p log(1/S0)` leads to the power

\[
\eta_{\rm eff}=\frac\lambda2(1-P_\rho)-\frac b2-b_s-b_p.
\]

The base margin exceeds `16393/200000` on AN06's ratio interval. With no other costs, the global-rate seed-loss budget is `b < lambda(1-P_rho)`; the frozen-rate budget is `b < (1-P_rho)/P_rho`.

This improves the bookkeeping **provided the quoted profile theorem applies**. Ordered entry, a lower-tail counterpart, center accumulation, weak-angle information, background control, and the conversion to the desired full population distance must remain explicit. A one-sided profile result cannot be marked as complete two-sided passage.

The exact leading identities

\[
\int N\,d\tau=\lambda^{-1}\log\frac{1-N_a}{1-N_b},\qquad
\int(1-M)\,d\tau=\log(M_b/M_a)
\]

show how a proved center majorant could yield an `O(1)` integral. Merely knowing that `U_c` vanishes at the resident, or is numerically small, does not yet give that uniform integral bound over arbitrarily long residence.

## 5. Remaining bottleneck

The next original-flow proof should establish the integrated signed defect and angular retention for a fixed quadrant-II cohort, then its capture into a bounded weak chart while the strong population is already sufficiently controlled.

The new inequality does **not** prove that the weak seed has scale `S0^(1-lambda)`. It identifies a way to preserve the target weak growth rather than artificially lose it through a fixed lower bound on `sin²(theta)`.

The bulk and backward-reservoir routes use different initial-label sets and joint parameter regimes. Their masses and phase durations must not be silently combined. In particular, growth already included in an ancestry estimate must not be counted again in the time interval.

An `O(1)` signed deficit loses no power and only a constant prefactor. A deficit `o(log(1/S0))` permits arbitrarily small power losses, but may have an unbounded prefactor. All `q`-dependent constants and finite-noise long-delay errors remain visible.

## 6. Checks and integration policy

The proofs were checked algebraically against the imported Cartesian field, including the transpose in the weak-coordinate equation and the mixture factor in the Gaussian bound. The rational exponent and contraction constants are proved in the text. No simulation or numerical quadrature was used.

The LaTeX was compiled twice; the final build has no undefined-reference or overfull-box warnings. The seven-page reading copy was rendered and inspected. These are writing checks, not independent mathematical approval.

Keep this increment separate. Upon explicit approval, the signed Jensen statement supersedes the **choice of main retention interface**, not the correctness of the old negative-budget proposition. The weak-coordinate estimate and frozen contraction should be considered tools for the pending capture proof. The global-profile section remains conditional until the missing ancestry/tail source and its hypotheses are checked.
