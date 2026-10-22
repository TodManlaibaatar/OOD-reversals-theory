# AN03_global_envelope_signed_gate_v1 — review note

**Scope:** S2a′, roadmap v1.10. New label prefix: `an03gesgv1:`. This is a partial analytic increment, not a full global-envelope or joint-bootstrap theorem.

The matrix-value route removes DECG's off-chart derivative obstacle. The remaining issue is an integrated signed-output budget. Independently, the Q3 interior is now paid by a proof valid from initialization; only the two boundary strips need entry classification and contracts.

## Task status and exact remaining inequalities

| Task | Status | Remaining item |
|---|---|---|
| (1) Global \(\ell^1\) envelope | **Partial.** The global sine inequality, Duhamel estimate, physical-angle conversion, and one-exit splice are proved. | A fixed bound for \(\mathfrak X=\int\sup_\theta(|R_{22}|-I'/2)_+\). The displayed distance coefficient still contains \(e^{\mathfrak X}\). |
| (2) Signed gate excess | **Stopped at the budget inference.** All proposed signed identities and inequalities are proved; the proposed pointwise cap on \(N_-\) is unnecessary. | \(\int(Qc+N_-)\le B_{\rm gate}\), uniformly in \(q\) and stopped endpoints. If the full CLOCK forcing budget is explicitly guarded, only \(\int N_-\le B_-\) remains. |
| (3) Constant audit | **Closed for the specified consumers.** | No obstruction from a fixed \(M_{\rm res}\)-dependent \(C_D\). This does not provide the missing integrated gate budget. |
| (4a) Lower-side no-gain | **Closed.** | None while the input sine remains negative. It is not extended across a later upper-side interval. |
| (4b–c) Interior speed, pre-\(t_0\) location and mass | **Closed.** A stronger pure Gaussian-tail bound supplies the pre-entry argument as well. | None for the explicitly defined interior cohorts. |
| (4d) Two boundary strips | **Consumer obligations stated; entry proofs not attempted.** | Actual classification and entry contracts for the \(\pi\) and \(3\pi/2\) strips, or a separately paid remainder. |

### Exact envelope produced

Let \(a_*=C_R(1+M_{\rm res})\), \(a_0=\lambda(1-c_b)/2\),
\(W_*=4R_c+a_*/a_0\), and choose \(L_c>R_c\). For the same physical strong branch used by BULK, the proof gives
\[
D(t)\le \mathcal C_D(t_*)\,\xi e^{\beta I(t)/2},
\]
where
\[
\mathcal C_D(t_*)=
\sec(1/2)\,p_*^{-1}e^{C_T\overline F_F}
e^{B+\mathfrak X(t_0,t_*)+\varepsilon_q}
\left(1+\frac{W_*}{L_c-R_c}\right),
\quad
\varepsilon_q=(a_*q+q^2/2)L_T\ell=o(1).
\]
This is an exact estimate with an exposed time integral, not a claim that \(\mathcal C_D\) is uniform in \(q\).

The first chart exit has \(D\ge L_c-R_c\), so the global additive forcing can be absorbed into that displacement. The proof uses the global estimate thereafter, including all reentries. An initially exterior label has the same separation at \(t_0\). No repeated switching factor, boundary trace, or off-chart derivative estimate is needed.

Comparability is checked rather than assumed:
\[
D\le \sec(1/2)\,N/q+2R_c,\qquad N/q\le D+2R_c,
\]
while the physical-exit condition keeps both angles within \(1/2\) of the strong axis. This is not a comparison for Q3 angles near \(\pi\); Q3 uses its own argument.

### The precise budget stop

The signed calculation gives, without assuming \(N_-\le Q(1-2c)\),
\[
X\le \tfrac12M_{\rm res}q^2+\tfrac12(Qc+N_-).
\]
The bound on \(-R_{22}-d_2\) is smaller than the common upper bound by \(Q(1-c)/2\), which explains why the proposed pointwise restriction is not needed.

Two similarly named budgets must remain distinct:

- The inherited c-form guard is \(\int\epsilon_F\le\overline F_F\).
- CLOCK's passage theorem assumes \(\int f_*\le\overline F_{\rm pass}\), with \(f_*=c+|V|+K_w+T+\epsilon_F\).

If the second is explicitly imposed as a stopped guard, then \(\int c\le\overline F_{\rm pass}\) immediately. It does not follow merely from the first. Without that added full-forcing guard, the stated response bound gives only \(\int c\le c_bL_T\ell\).

CFR controls the negative part of the signed \(P_1\) moment
\[
K_O=q^{-1}\mathbb E_{P_1}[(f_O)_2X_1],
\]
whereas
\[
N_-=\mathbb E_{P_2}[(f_2X_2)_-].
\]
Its \(V_O\) uses output component 1. These are different quantities; neither the signed moments nor their named positive/negative parts supply the negative part before integration that is needed here.

The new note also exposes the state-level charge
\[
N_-\le C\left[q^2\mu_{\mathcal K}
+E_\Sigma+q\sqrt{E_\Sigma J_\Sigma}
+\mu_{\mathcal B}+\mu_{G_+}e^{-k_1/q^2}\right]
\]
when the stated instantaneous core geometry and mass bound hold. Under \(J_\Sigma\le q^2K_Y^2\), the unpaid secondary contribution is
\(E_\Sigma+q^2K_Y\sqrt{E_\Sigma}\).
The primary term is exponentially small because its output coefficient \(W_2\) is positive. This charge does not assume the desired S2 energy theorem to prove itself.

A fixed bound, rather than \(o(1)\), would suffice for this envelope. No such bound is added as a hypothesis of a claimed full theorem. This is a source/guard budget gap, not a counterexample to the initialized flow.

## Q3 split and stronger interior result

Let
\[
k=169/3200,\quad
\Lambda_q=\sqrt{3\ell/k},\quad
w_q=\arcsin(q\Lambda_q).
\]
The fixed initial-label interior is
\[
[\pi+2w_q,\;3\pi/2-2w_q].
\]
For these labels, both input gates remain closed with projected margins at least \(q\Lambda_q\) throughout \([0,t_*]\). Loss monotonicity bounds every residual component on both clusters, so
\[
\max_{ij}|R_{ij}|\le C e^{-k\Lambda_q^2}=Cq^3.
\]
The same bound controls both angular speeds and the absolute radial rate. The total travel is \(O(q^3\ell)=o(w_q)\), which closes the buffer argument from initialization. Therefore
\[
m(t,b)=q^{10}e^{O(q^3\ell)},\qquad
\int_{t_0}^{t_*}\mu_{\mathrm{int}}/q\le Cq^9\ell=o(1).
\]
No pre-\(t_0\) cross-residual guard is needed. This is stronger than retaining an \(O(M_{\rm res}q^2)\) error after discarding one of the closed gates.

For the larger fixed subset of Q3 ancestry that happens to lie in the same buffered interior at \(t_0\), MOMC's whole-left entry mass gives \(Cq^2\ell^2\). The same retention proof gives the requested
\[
\int\mu_{\mathrm{int}(t_0)}/q\le Ce^{2B}q\ell^3.
\]
MOMC's mass estimate alone does not locate its labels; the new pre-entry speed argument supplies that location for the initial-label interior.

The uncovered initial strips have width \(2w_q=O(q\sqrt\ell)\) on **both** sides:
\[
[\pi,\pi+2w_q),\qquad(3\pi/2-2w_q,3\pi/2].
\]

### What the strip consumers need

**Near \(\pi\):** a weak-family extension first needs actual fixed-label classification. A primary portion must satisfy LCRC's entry signs, antisymmetry and Cartesian ratio, together with its transverse/weak entry energy bounds. The existing clock can be kept unchanged. Any portion assigned to the recruited secondary group must supply SEP/BULK's raw mass-weighted contract:
\[
\xi\le Z_\pi,\quad \eta_\pi(\mathbb R_+)\le Cq^3,\quad
\eta_\pi\{\xi>u\}\le Cq^3\min\{1,(A_q^dq^{10d-2s}/u)^{p_2}\}.
\]
Only the upper tail is needed by BULK. SEP currently treats the Q2 secondary group near \(\pi/2\); it cannot be applied literally to the entire strip near \(\pi\). In particular, primary weak labels need not have bounded strong-chart displacement.

**Near \(3\pi/2\):** a strong late-joiner extension must supply a bounded same-reference entry chart and the raw, mass-weighted tail with exponent \(3/s\) and scale
\(\epsilon_h\asymp A_q^d q^{10d-s}\), or the equivalent weighted tail-moment bound displayed in the TeX. Safe-core admission also needs its cutoff. A label joining only after \(t_0\) needs an arrival-time version with a justified match; it cannot be treated as charted at \(t_0\) by definition.

Any unassigned labels require a separate integrated outside budget, or proved negative-input retention to use the no-gain lemma. Neither strip is silently folded into an existing family.

## Constant audit

| Constant | Dependence and use |
|---|---|
| \(R_c=79/51\), loss/Gaussian constants, \(k=169/3200\) | Guard-independent model/reference bounds. |
| \(L_T,C_{\rm dur}\) | Prescribed passage duration and MOMC's bounded half-mass-time shift. |
| \(a_*=C_R(1+M_{\rm res})\) | Cross-entry bound; enters the fixed additive forcing and a vanishing \(q\ell\) term. |
| \(a_0=\lambda(1-c_b)/2\), \(W_*=4R_c+a_*/a_0\) | Duhamel denominator and reference conversion. |
| \(p_*=\Phi(-7L_c/10)\), \(C_T=2+p_*^{-1}+(7/10)\phi(0)/p_*\) | Reused DECG metric constants, fixed after the chart is chosen. No numerical evaluation is required. |
| \(p_*^{-1}e^{C_T\overline F_F}\) | Local-envelope factor; reaches the consumers through \(C_D\). |
| \(A_0=C_D^2\max(1,\delta_0^{-2})\) | DECG's capped-gain coefficient. It changes constants, not \(q\)-powers. |
| \(C_m=e^{6B+1/\beta+o(1)}\) | Reused DECG raw-mass gain constant. |
| \(\eta_*<(\delta_0/(2C_D))^2\) | BULK's fixed energy comparison threshold. Its reciprocal changes only the coefficients of \(q^5\) and \(q^{\Gamma_\nu}H\). |
| Tail-moment constant | Depends on \(A_0,C_m\) and the entry tail; multiplies \(q^{\Delta_\nu}\ell\), with \(\Delta_\nu>3/25\). |
| \(K_Y,E_g\) | Existing stopped constants; they multiply the vanishing secondary terms in the downstream estimates. They do not enter the Q3 freezing lemma. |
| \(\int X,\int N_-\) | No uniform value has been proved or assigned. Their potential \(q\)-dependence cannot be hidden inside a “fixed” constant. |

**Conclusion of the audit:** a fixed \(M_{\rm res}\)-dependent \(C_D\) is admissible in the stated TAILREP/BULK/LCRC uses. Its dependence reaches only vanishing contributions. Thus it does not require choosing the residual guards again. The order-one core radius, core mass bound, \(B_s\), and \(c_b\) are not altered.

There is no need to enlarge \(L_c\) to absorb \(M_{\rm res}\); one can use \(L_c=R_c+1\) when specifying the c-form guard. If a larger fixed chart is chosen after the residual guards and before \(C_0\), its c-form validity must be part of the actual guard, not inferred from a smaller chart. Its constants remain finite. The tail consumers require only bounded \(C_T\overline F_F\), not a small value. If a multiplier at most \(e\) is desired, choose \(\overline F_F\le1/C_T\). CLOCK separately requires \(\overline F_{\rm pass}\le e_*/(4C_{\rm pass})\). A later common-budget construction can use the smaller target. This increment proves no forcing-budget closure.

## Proof audit points

1. The derivative of \(N\) is interpreted as an upper Dini derivative at sine zeros; no division by a sine occurs.
2. \(d_2=I'/2\) differs from \(\beta I'/2\) by \(q^2(1-c)/2\). Its integrated cost is retained in \(\varepsilon_q\).
3. The Duhamel forcing is paid by \(\beta I'/2\ge a_0>0\), with a fixed denominator. It is not bounded by the passage duration.
4. Only one local-to-global splice occurs. Reentries introduce no repeated constant.
5. The common signed bound for both signs of \(R_{22}\) is valid without \(N_-\le Q(1-2c)\).
6. A bound on the negative part of an integrated moment is not a bound on the integral of its negative part.
7. Lower-side no-gain uses \(|\sin\theta|\) times the negative-gate tail, including when both input and output sines are negative. No factor \(e^I\) is charged there.
8. The interior freezing proof uses both closed input gates and all-component loss bounds, valid before \(t_0\). It does not assume output alignment or a pre-entry \(O(q)\) cross residual.
9. Interior and strip cohorts are fixed in initial labels or fixed by their state at \(t_0\); no moving-mask flux is omitted.
10. A small initial strip width is not itself a useful mass-weighted entry profile. Its consumer contracts remain explicit.

## Source provenance

Read-only GitHub retrieval on October 22, 2026, from [TodManlaibaatar/OOD-reversals-theory](https://github.com/TodManlaibaatar/OOD-reversals-theory). The roadmap identifies revision **1.10** and its corrected proposals. DECG and CFR were both available in the repository on this read; no local fallback was needed.

These are Git blob hashes of the retrieved source text, not commit hashes.

| Path | Git blob SHA |
|---|---|
| `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | `401d09104aa125f6c46c5613bd713aeef4cb8e77` |
| `03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex` | `a490ea323e45e61c1a58301554b89ad84cb02605` |
| `03_passage_AN03/AN03_c_form_field_reduction_v1.tex` | `d6e92da35a9d510201946fa6851c2c55740c1ff0` |
| `03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex` | `8de0d85c64a3d51f3bd9c3662baf2efae0737373` |
| `03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex` | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` |
| `03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex` | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| `03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` |
| `02_entry_AN02/AN02_secondary_entry_profile_v1.tex` | `c7c857ec10b7f7b2cf42d1cdb452c50edc735587` |
| `02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex` | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| `02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex` | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` |


## Validation and scope

The standalone TeX compiled successfully with the desktop LaTeX compiler. This is a typesetting check, not a mathematical premise. The delivered archive contains only the raw TeX and this review note.

All displayed estimates are analytic: exact equations, Gaussian inequalities, Dini/first-exit arguments, and integrations. No experiments, numerical trajectories, interval calculations or sampled sign checks were used. No CLOCK passage application, full S2 theorem, joint weak-passage assembly, new strip entry theorem, selection or consolidation is claimed. Previous sources, foundations and checkpoint are unchanged; no GitHub mutation was made.

