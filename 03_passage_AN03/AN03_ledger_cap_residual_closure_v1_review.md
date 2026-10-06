# Review: ledger-cap residual closure, v1

**Disposition: Route 3 closes in the stated conditional original-flow scope.** The new theorem removes RCET's independent backward-clock premise and externally supplied terminal amplitude cap. Original-entry transfer, strong learning, and the stated S1/S2 and instantaneous-state budgets remain inputs. Stage 2 was not started.

The paired source is `AN03_ledger_cap_residual_closure_v1.tex`. All 29 new labels use **`an03lcrcv1:`**. Prior files, including RCET, are unchanged. The user reports that RCET Theorem 2.1, Proposition 3.1, Lemma 4.1, Theorem 4.2 and the two-route obstruction have been reviewed and verified; that review status is recorded, not presented as a new independent review.

## Precise advance

Theorem 4.1 (`closure`) proves, uniformly on the prescribed passage interval,

\[
\|e_1\|_{P_1}+\|e_2\|_{P_2}=O(1),\qquad
\|e_2\|_{P_1}+\|e_1\|_{P_2}=O(q),
\]
\[
\int\sup_\theta|R_{11}|\le C\int|1-\kappa_1|+o(1),
\qquad H(t)\le H_{G_+}(t)\le\frac98c_b+o(1).
\]

In particular, `H(t_b) <= (9/8)c_b + o(1)` is a conclusion. The proof also gives `E_G+ <= (5/4)c_b + o(1)` and `J_G <= Cq^2`. The latter is an adequate residual-closure bound, not a replacement for BULK's sharper regenerated-energy statements.

The clock remains the eta=`1/8` cohort and retains its `o(1)` defect. The larger sign-good union only needs bounded defect. The change from RCET is that its endpoint cap is obtained from the response ledger **at the current stopped endpoint**. No information after that endpoint is used.

## Four preliminary checks

### (a) Ledger identity and tail sign: proved

Lemma 2.1 (`ledger`) defines `v_- = (-v)_+ >= 0` and derives directly

\[
c_S=H_S-A_S+\tau_S,\qquad
\tau_S=Q^{-1}\int_SW_2\,\mathbb E_{P_2}[X_2(U\cdot X)_-].
\]

This is exactly CLOCK's positive-negative-part convention. Its rearrangement is CLOCK's `H_S = c - c_(S complement) - tau_S + A_S`; there is no sign change in the definition of tau.

For `W2 >= 0`, the only negative contribution is from `X2 < 0`. The displayed Cauchy–Schwarz estimate and Gaussian Chernoff bound give

\[
\tau_S\ge-C\mu_S e^{-\rho^2/(4q^2)}.
\]

This is a lower bound, not an absolute-value estimate; it requires no angular margin. A separate Lipschitz comparison of `(U1 X1 + U2 X2)_+` with `(U2 X2)_+` proves

\[
|c_S|\le E_S+\frac{2q}{\sqrt Q}\sqrt{E_SJ_S}
\]

for arbitrary donor signs. This preserves coefficient one on `E_S`.

Lemma 2.2 (`pointcap`) uses these identities, `A_G+ <= H_G+/9`, and absolute charges for all complementary groups to give the requested cap. Core response is `O(q^2)`, outside response is `O(mu_B)`, and rest means the disjoint chart and secondary groups.

### (b) Stopped applicability: verified

Lemma 3.1 (`localclock`) distinguishes the hypotheses as follows.

| Hypothesis of BULK 4.1 / RCET 2.1 | Time dependence and use here |
|---|---|
| Fixed cohort and balanced original flow | Structural; the same initial labels are used at every endpoint. |
| Positive entry amplitude, `z(t0)>0`, `abs(a)/z <= 1/4`, Cartesian entry ratio | Anchored at `t0`, retained S1 data; not reinitialized at a moving time. |
| Compact ratio box; fixed constants; sufficiently small `q` and `C0` | Global parameter choices, independent of the stopped endpoint. |
| `0 <= c(t) <= c_b < 1` | Pointwise on the interval under consideration. |
| Diagonal residual norm bound | Pointwise, supplied globally by loss monotonicity. |
| Cross residual norm bound `Mq` | Pointwise; used provisionally and improved by the same bootstrap. |
| `int_(t0)^(t*) r <= B` | Integral over the controlled past; restriction of a nonnegative integral, with no future input. |
| `t* - t0 <= L_T log(1/q)` | Inherited from the prescribed interval length. |

Neither source theorem requires a future amplitude cap, future residual information, or a pre-existing backward clock estimate. Their all-subinterval defect conclusions are proved on the current stopped interval. The corrected conservative y-comparison is used when choosing `C0`.

### (c) Chart mass: derived from retained chart geometry and S1 entry

Lemma 3.2 (`chartmass`) retains the instantaneous budget `abs(theta)+abs(psi) <= Zq` on the fixed chart group. Its persistence is not proved here. The mass itself is **not** an additional input:

\[
(\log m)'\le2r+Cq^2(MZ+Z^2),\qquad
\mu_{\rm chart}(t_0)\le2J_G(t_0)\le2C_Jq^3,
\]
\[
\mu_{\rm chart}(t)\le4C_Je^{2B}q^3.
\]

The constants `Z,M,B` are fixed before decreasing `q`. The integrated correction `Cq^2(MZ+Z^2)L_T log(1/q)` tends to zero. Strong-learning integrability controls the `r` guard when the joint bootstrap closes.

Thus `Z mu_chart = O_Z(q^3) = o(1)` and `Z^2 q^2 mu_chart = O_Z(q^5) = o(1)`. The chart cross pressure is at most `C(Z+Z^2 q)mu_chart`. No large `Z(C0)` coefficient enters the constants that must be fixed before `C0`.

### (d) Secondary energy on the stopped interval: verified with S1/S2 contracts retained

Lemma 3.3 (`secondary`) checks the transferred finite-cutoff radial profile, original clock seed, bounded reference, first-exit distance envelope, and gain bound at **every intermediate endpoint**. These are exactly the retained source contracts; chart-entry displacement alone does not establish them.

The clock defect comes from BULK on the same stopped interval. Before its terminal-cap simplification, BULK's proof gives

\[
E_{\rm sec}\le C\bigl(q^5+q^\gamma H+q^{\Gamma_\nu}H^{1+\nu}\bigr).
\]

The raw-energy guard supplies `H <= H_G+ <= E_G+ < E_g` even before any y-bound is known. Hence `H^(1+nu) <= E_g^nu H`, proving

\[
E_{\rm sec}\le C_\Sigma(q^5+q^{\Gamma_\nu}H),\qquad
\Gamma_\nu\ge\frac{289169}{924000}>\frac3{10}.
\]

No terminal cap is used. The rational exponent bound is imported from BULK, not recomputed numerically.

## Retained inputs and their type

These are all the nonstructural inputs. All parameter-uniform conclusions require their constants and little-o budgets to be uniform on the given rho box.

| Retained input | Type / source contract |
|---|---|
| Prescribed logarithmic passage interval and `0 <= c <= c_b < 1` | Existing passage-interval specification and instantaneous response guard. |
| Fixed core chart `abs(theta)+abs(psi) <= Rq`, bounded core mass | Instantaneous-state budgets already used by RCET S0. |
| `sup_t mu_B/q -> 0`, with all outside/background labels charged | Instantaneous-state mass budget already used by RCET; no stronger logarithmic budget is added. |
| Fixed chart group's continued `Zq` joint chart | Instantaneous-state geometry budget. Small mass is derived, not retained separately. |
| `J_G(t0) <= C_Jq^3`, `E_G+(t0)=o(1)`, `H_Cl(t0) ~ q^(10(1-lambda))` | Existing original S1 entry-energy and seed contracts. `C_J` is the whole explicit-cohort constant, independent of later subdivision. |
| `z>0`, `abs(a)/z <= 1/4`, ratio at most `C0` on `G+`, stronger `C_clk q^(1/8)` ratio on the clock | Existing original Cartesian S1 entry contracts from BULK/RCET. |
| `int abs(1-kappa1) <= B_s` | Existing S1 strong-learning contract. |
| Secondary initial mass `O(q^3)`, finite displacement cutoff and `p2` tail | Existing transferred S1 profile contract, BULK Lemma 5.1 / Proposition 5.2. |
| Bounded same-field reference, pre-exit distance envelope, capped actual mass gain at every endpoint | Existing S2 contracts, stated explicitly in equations `distance` and `gain`. They are not proved here. |

The partition is fixed and disjoint; `G+` is a union, so labels in both descriptions are counted once. Chart and secondary labels are fixed initial sets, not moving masks. Every remaining label must belong to the core or charged outside group. There is no independent residual bound, backward clock premise, uniform amplitude bound, terminal cap, or smallness assumption on `c_b` beyond `c_b<1`.

## Bootstrap and constant audit

The principal guards are `Y<K_Y`, `int r<B`, and **`E_G+<E_g`**. Guarding raw energy fixes the residual constant without first presuming `E_G+ <= (10/9)H_G+`.

The proof orders choices as

\[
(B,E_g,K_Y,M)\quad\longrightarrow\quad C_0
\quad\longrightarrow\quad K(C_0),Z\quad\longrightarrow\quad q.
\]

It sets `B=C_r B_s+2`, `E_g=2+2c_b`, and a loose anticipated cap `h_*=(9/8)c_b+1`. The numerical coefficient in `h_*` comes from the exact ledger, not a numerical calculation. The integral bounds used to choose `K_Y` depend only on this loose cap, the fixed response gap, and the core/model constants. Geometry-dependent floors vanish after the geometric constants are fixed.

On a stopped interval:

1. The local ratio theorems give the signs and bounded `G+` defect.
2. Chart and secondary estimates make `E_rest=o(1)`; `J_rest <= q^2 K_Y^2` makes its mixed response charge small. The ledger improves the raw-energy guard.
3. The cap holds at the current endpoint. The **same group's own** bounded defect then gives `int H_G+ <= e H_G+(t*)/b0`, and the corresponding square-root integral bound.
4. Consequently `sup E_G`, `int E_G`, and `int sqrt(E_G)` have constants fixed before `C0`. RCET's Volterra kernel is reused unchanged; Gronwall improves `Y` to `K_Y/2` and the strong-remainder estimate improves `int r` to `C_r B_s+o(1)<B-1`.

There is one subsidiary continuity stop at cross residual sum `Mq` when deriving secondary energy from the S2 package. This avoids assuming its clock conclusion before the residual bound is available. It is a proof device, not an extra retained premise: entry estimates start it strictly, and RCET's instantaneous pressure estimate under `E_G+<E_g`, `Y<K_Y`, and `E_rest=o(1)` improves it to `Mq/2`. Thus the provisional `M` used in the local ratio lemmas is independently improved in the same stopped argument. This is part of Route 3, not a fourth attempted route.

The coefficient of the regenerated `LH` feedback is never discarded. It remains inside the Volterra coefficient `C E_G(t)`. The ledger supplies its integrability without requiring `C H_b<1`.

## Other analytic audit points

- The sign-good ledger uses a one-sided estimate on tau; replacing it by CLOCK's margin-dependent absolute tail bound would lose the reason this route works.
- The Gaussian event is `X2<0`, not the receiver's inactive gate. The tail exponent follows from an analytic Gaussian Chernoff bound and Cauchy–Schwarz.
- The chart mass calculation divides by `m>0`. Positivity follows from the original positive initialization and the bounded-coefficient characteristic flow on finite intervals. Clock logarithms divide only by the amplitudes whose positivity the local ratio theorem proves. At zero transverse norm, use BULK's norm Dini derivative, not division by `sqrt(J)`.
- All label integrals are over fixed sets. Finite mass and Gaussian second/fourth moments justify Fubini, domination and differentiation. No moving-label flux is omitted.
- The constants in the source ratio theorems are independent of `t_*`. Duration and integral guards restrict to the past. No estimate invokes a future interval `[t_*,t_b]`.
- The integrated strong remainder is `O(q^2 log(1/q)) + O(sup(mu_B) log(1/q)) = o(1)`. The original `mu_B=o(q)` budget suffices.
- Geometry-dependent secondary constants multiply `q^5` or `q^Gamma`; with fixed `Gamma>3/10`, they do not create a `C0` loop.
- The theorem is a conditional original-flow implication. It does not establish S1 entry, bounded-chart retention, or S2 gain from initialization. The source's exact comparison results are not silently transferred.

## RCET consolidation notes — no edits made to RCET

These three items are recorded for a later authorized consolidation only.

1. **Theorem 2.1, y-comparison.** Use the conservative bound
   \[
   y\le\frac14+\frac{2LX}{3b_*},
   \]
   rather than `1/4 + LX/(3b_*)`. A smaller admissible `C0` still gives `y<=1/3`. The new theorem chooses its constants using this conservative bound.

2. **Proposition 3.1, target-only first-coordinate growth.** For `u1>=0`, Stein and convexity give, on `P1`,
   \[
   \mathbb E[X_1(u\cdot X)_+]
   =\mathbb E[(u\cdot X)_+]+q^2u_1\mathbb P(u\cdot X>0)
   \ge u_1.
   \]
   On `P2`, the contribution is `q^2 u1 P(u·X>0)>=0`. Mixture weight `1/2` yields `U1hat' >= U1hat/2`. This is the missing one-line justification after crossing.

3. **Proposition 3.1, target-only second-coordinate rate.** For `a2=u2/|u|>0`, put `v=rho a2/q` and
   \[
   d_q=\frac{q^2}{2}[\Phi(a_1/q)+\Phi(v)],\qquad0\le d_q\le q^2.
   \]
   The exact Stein form displaying the gate deficit is
   \[
   \frac{\widehat U_2'}{\widehat U_2}-\frac\lambda2
   =d_q-\frac\lambda2\Phi(-v)+\frac{\rho q}{2a_2}\phi(v).
   \]
   In particular,
   \[
   -\frac\lambda2\Phi(-v)
   \le\frac{\widehat U_2'}{\widehat U_2}-\frac\lambda2
   \le q^2+\frac{\rho q}{2a_2}\phi(v),
   \]
   and its absolute value is bounded by the sum of `q^2`, the gate-deficit term, and the positive Gaussian term. Equivalently the correction is `d_q + (rho q/(2a2))K(-v)`, where the identity `K(-v)=phi(v)-v Phi(-v)` includes the deficit. Thus that compact positive expression is consistent, but the two-sided rate justification must retain the deficit explicitly. Before strong-chart arrival, both Gaussian terms have the integrable tails used in the source's reciprocal-speed argument; the `d_q` integral is `O(q^2 log(1/q))`.

No target-only result is re-proved or revised in the new `.tex` for these consolidation points.

## Source provenance and proposed location

The roadmap was fetched read-only from the updated repository on October 6, 2026. Its filename remains `UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md`, while its heading is **Version 1.1**. S0 Route 3 and ledger items 9–11 were read. Current RCET, BULK, CLOCK and foundations source bytes were also fetched read-only.

| Repository path | Git blob SHA | Main dependency |
|---|---|---|
| `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | `f2422212f79228d0b298b8e569f17974c82e387f` | S0 Route 3; withdrawn-claim ledger 9–11 |
| `03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex` | `49e352002b4c699338ac99a4d55d51c60760ea86` | `an03rcetv1:eta0`, `outputs`, `closure`, `volterra`, `failingendpoint` |
| `03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` | `inc:AN03:bulkclock:v1:` + `bulkclockclosure`, `moments`, `gainenergy`, `secondarydetail`, `gammamargin`, `transverse`, `residualinputs` |
| `03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex` | `8de0d85c64a3d51f3bd9c3662baf2efae0737373` | `inc:AN03:clock:v1:` + `identity`, `endpoint`, `endpointidentity`, `Hcap` |
| `01_foundations/RELU_POPULATION_FOUNDATIONS_v2.tex` | `a5c557d56fe5753532a600f8f238a74f8091da9b` | P5 loss, balance and characteristic regularity |

The new theorem belongs after RCET's conditional residual lemma and obstruction, as the explicit Route 3 resolution under its retained contracts. It does not invalidate the earlier two-route obstruction or restore the withdrawn scalar shortcut. No old theorem is replaced, so no replacement label map or merge is made.

## Validation and stop

The final `.tex` compiled successfully with the built-in LaTeX compiler. The static reference audit found 29 unique labels with the requested prefix and no unresolved local references. These are typesetting checks, not proof premises. No numerical experiment, interval arithmetic, grid sign check, saved trajectory, fitted exponent, or numerical premise was used. No subagent or independent new mathematical reviewer was used.

The four checks hold with the retained inputs above, and the theorem is written. Work stops here under the requested rule. Stage 2, the M-clock passage, a capped-gain proof, and the bridge problem remain untouched.
