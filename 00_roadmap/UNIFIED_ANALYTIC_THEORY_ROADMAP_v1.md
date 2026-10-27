# Roadmap to a unified analytic theory of the ReLU SIM reversal mechanism

**Version 1.16 — October 27, 2026.** Working roadmap, not a proof and not a merge instruction. No source increment, foundations file, or checkpoint is modified by this document. It supersedes the "recommended next task" parts of `THEORY_HANDOFF_ANALYTICAL_A_B_v2.md` (H2) only where explicitly stated; H2's ground rules, file contracts, and withdrawn-claims ledger remain in force.

**Revision 1.1 (Oct 6).** Records RCET (`AN03_residual_closure_and_eta0_transport_v1`). S0 is rewritten: the v1 scalar fixed point was invalid (it dropped a regenerated $LH$ term), RCET's Volterra closure is conditional on a clock premise, and a candidate repair (Route 3) is described. S4's primary-band bullets are marked proved, with the endpoint-regularized dichotomy. New ledger items 9–11; file map updated.

**Revision 1.2 (Oct 6).** Records LCRC (`AN03_ledger_cap_residual_closure_v1`). Route 3 is proved: S0 is closed as a conditional original-flow implication, with no clock premise and no terminal cap. S0 now lists the assembly requirements its retained inputs must meet.

**Revision 1.3 (Oct 7).** Records OWPT (`AN02_overlap_window_profile_transfer_v1`): S1 step 1 is proved as an exact original-flow result. S1 step 2 now starts at $M_0=M(t_m)\asymp e^{C_m}q^\sigma$ rather than $M\approx\delta$, and the $C_m$-free handoff identity is recorded.

**Revision 1.4 (Oct 7).** Records SMCP (`AN02_strong_M_clock_passage_v1`), an obstruction increment. At fixed $C_m$ the linear multiplier fails on the outer band. Step 2 now records: the stationary leading center, the $A_q^d$ handoff and its clock shift, the moving-overlap repair, and the exact $J_{\rm sh}$ tangent structure. New ledger items 12–14.

**Revision 1.5 (Oct 7).** Records MOMC (`AN02_moving_overlap_M_clock_passage_v1`): S1 step 2a is proved unconditionally through strong half mass. Proposes $t_0:=t_h$. Adds S1 step 6 (Q2 entry at $t_0$) as next. Moves $B_s=\log2+o(1)$ and core retention to the weak-passage bootstrap.

**Revision 1.6 (Oct 7).** Records Q2EP (`AN02_Q2_entry_through_strong_passage_v1`): the Q2 entry energy is proved. The $e^{o(1)}$ universal-factor obstruction is reclassified as a contract overreach, because LCRC needs only fixed constants. Ledger item 15 adds the accuracy rule for contracts.

**Revision 1.7 (Oct 7).** Records Q2EC (`AN02_Q2_entry_contracts_v1`): the primary Q2 entry contracts at $t_0$ are proved with fixed constants. Adds S1 step 7 (secondary entry profile) with the suggested partition $\Sigma=\{c_0<Kq^\gamma\}$, $\mathcal D=\emptyset$.

**Revision 1.8 (Oct 21).** Records SEP (`AN02_secondary_entry_profile_v1`): S1's entry contracts are complete and unconditional. S3 gains a refined route, which uses the linearity of $G_+$ on $P_2$ and treats the c-form passage as a local passage to a small fixed $c_b$. S3a, the c-form field reduction, is next.

**Revision 1.9 (Oct 21).** Records CFR (`AN03_c_form_field_reduction_v1`), which proves part of S3 and stops at the S2 dependency. Ledger 16 records the sequencing error and the integrated outside budget. S2 is reordered: S2a (envelope and gain from a c-form hypothesis) comes next, then the joint weak-passage assembly. The strong diagonal term is downgraded from a sign problem to a budget controlled by LCRC's $\int r$ guard.

**Revision 1.10 (Oct 21).** Records DECG (`AN03_distance_envelope_and_capped_gain_v1`): the chart envelope, the signed radial bound and the conditional gain are proved. Ledger 17 records the over-restricted contract. S2a' (global ℓ¹ envelope with signed gate cancellation; Q3 split) is next.

**Revision 1.11 (Oct 22).** Records GESG (`AN03_global_envelope_signed_gate_v1`).
- Proved: the global sine envelope and its splice onto the chart lemma, the signed gate identity (without the proposed cap), the constant audit, lower-side no-gain, and a Q3 interior frozen from initialization.
- Stopped at the integrated gate budget $\int(Qc+N_-)$.
- The review finds that this budget is payable from proved sources, LCRC's backward clock and GESG's own cohort charge, under one joint guard on $E_\Sigma$. S2's closure package is next.
- Ledger 18 records the wrong budget sources in my prompt.

**Revision 1.12 (Oct 23).** Records S2CP (`AN03_S2_closure_package_v1`).
- S2 is closed in stopped-guard form: gate budget, fixed $C_D$, all-endpoint capped gain, $E_\Sigma$ with the joint guard strictly improved, and complement mass $\int\mu_{\mathcal C}/q\le Cq^{\Delta_\nu}\ell$.
- Also proved: CFR's secondary obstruction $\mathcal U_\Sigma=o(1)$, and $\int|1-\kappa_1|\le\log2+o(1)$ under retained core geometry.
- The outside population is exactly $\mathcal C\cup\mathcal Q_{3,\rm int}\cup\mathcal S_\pi\cup\mathcal S_{3\pi/2}$. Only the strips are unpaid.
- Ledger 19 records two coefficient and order errors in my prompt. S3b (full c-form assembly, then the CLOCK budget) is next.

**Revision 1.13 (Oct 23).** Records CFA (`AN03_c_form_assembly_v1`).
- S3 is closed in stopped-guard form:
  - the core-only c-form ($T\equiv0$) with donor mass capped at one;
  - two new selected moments, $A_1$ and $B_2$;
  - the full value-and-derivative remainder $\int\epsilon_F\le C\,C_0E_g+C_{\rm out}F_{\mathcal S}+o(1)$;
  - CLOCK constants independent of $c_b$ and $C_0$, and the forcing budget;
  - a conditional CLOCK passage.
- Every guard of the weak-passage bootstrap is now strictly improvable except the **Q3 strip budget**, which is the only external input left. The strips come next, then the joint assembly.

**Revision 1.14 (Oct 23).** Records Q3SB (`AN03_Q3_strip_budgets_v1`). It is partial and stopped on two false premises in my prompt (ledger 20).
- *Proved:*
  - the pre-entry cross residual $\le C_{\rm pre}q$ on $[0,t_0]$, a new S1 conclusion;
  - the pre-entry gate budget;
  - the regularized sine envelope $N\le C(N(0)+q)e^{\beta I_{\rm tot}/2}$;
  - the total-clock bound $e^{I_{\rm tot}(t_*)}\le CE_gA_q^{-q^2}q^{-10-10q^2}$;
  - a frozen 3π/2 substrip.
- *Revised strip route:* split each strip by scaled offset into an outer frozen zone, a middle zone (frozen in scaled coordinates), and an inner zone of physical width $O(q\sqrt{\log\ell})$. Do the π strip first, then 3π/2.

**Revision 1.15 (Oct 23).** Records PISB (`AN03_pi_strip_budget_v1`).
- **The π strip is paid,** with $\sup\mu_{\mathcal S_\pi}/q\lesssim q^{411/800}\sqrt{\log\ell}$.
- **Both strips' outer and middle zones are frozen and paid.**
- The only external input left in the weak passage is the 3π/2 inner zone $J_3=(3\pi/2-qs_q,3\pi/2]$, of physical width $O(q\sqrt{\log\ell})$. A time-shift route is recorded for it.

**Revision 1.16 (Oct 27).** Records LSB (`AN03_late_strip_budget_v1`).
- $J_3$ is paid: $\sup W_3/q\le C(1+s_q)q^{769/4000}$.
- With PISB, **CFA's whole-strip input is supplied**. Every guard of the weak-passage bootstrap now has a proved strict improvement and no external input remains.
- Next: the joint weak-passage assembly.

---

## 0. Ground rule: analytic proof only

The theory is to be established by **displayed analytic proofs**. This applies to every theorem, every constant used in a theorem, and every parameter region claimed.

**Allowed**

- Exact Gaussian integration and identities; truncated-moment formulas; Stein relations.
- Invariant regions, differential inequalities, first-exit bootstraps, comparison principles, Grönwall, Riccati comparison, saddle passage with proved error terms.
- Characteristic transport, fixed-label bookkeeping, Tonelli/Fubini with stated domination.
- Elementary rational bounds (e.g. $\phi(0)<2/5$, $P_\rho<153/250$) proved by hand, and monotonicity arguments in one or two variables.
- Constants defined as unevaluated functionals of an analytically specified orbit (derivatives, suprema, crossing times), provided they are proved finite and positive.
- Symbolic algebra and exact-fraction arithmetic **as checking aids** for identities that are also displayed. LaTeX compilation is a typesetting check only.

**Not allowed as proof premises**

- Interval arithmetic, validated numerics, numerical continuation, numerical eigenvalue enclosures.
- Sign checks on grids, sampled parameter sweeps, or partitions of a parameter box fine enough to amount to interval arithmetic. (A few explicit case splits with proved monotonicity are fine; the κ=10 margin in `TAILREP` is the model: combine exponents first, then use monotonicity.)
- Saved trajectories, pilot runs, fitted exponents, or any statement whose truth is checked by running code.

**Numerics may motivate or falsify.** Any decimal quoted below is either (i) a rounded value of an expression that also has a displayed rational bound, marked **[rational]**, or (ii) a numerical evaluation used only for orientation, marked **[eval]**. No theorem may depend on an **[eval]** value.

Every statement keeps H2's scope labels: exact original-flow result; exact comparison result (target-only); result within the defined leading system; conditional estimate; derived expansion; empirical evidence.

---

## 1. What "a unified theory explaining the empirical mechanism" means

### 1.1 Target statements

| Name | Content | Current status |
|---|---|---|
| **Theorem A** | From aligned-isotropic initialization, on an analytically specified joint family $(q,S_0(q))$ near $\rho=2/3$: substantial learning of both concepts, strict opposite cluster signs $D_1<0<D_2$ on a common learned window, and an ordered negative-then-positive total rate, giving a rebound $\ge c\,q^2$ on an off-cone sector of width $\ge c\,q$. | Open. Limiting version proved. |
| **B-core** | The same proof shows *why*: cluster-1 help = exposure × signed exact lag; cluster-2 harm = input rotation of the strong carrier driven by a residual that the weak family produces; the evolving lag/exposure/residual force the change of dominance, with complete remainders. | Proved in the leading system; original-flow version open. |
| **B-bridge** | The canonical depth enhancement: a non-small inactive strong bridge changes exposure and compensation. | Open (AN4). |
| **Persistence** | After the rebound, the scaled benefit is eventually zero on growing windows. | Proved in the limiting system; the original-flow version follows from AN7 by LP's diagonal argument. |
| **Linear contrast** | Commuting aligned linear networks have monotone probe error and clusterwise help. | Complete (LP, extending P10). |

### 1.2 Empirical facts the theory must account for

| # | Empirical fact (user-reported) | Theory component | Status |
|---|---|---|---|
| E1 | ReLU off-cone reversals; no above-threshold linear reversals in matched controls | LP linear contrast + Theorem A | Contrast done; A open |
| E2 | Help from cluster 1 via strong-family output; harm from cluster 2 via strong input rotation; weak output is the residual producer | Leading identities $d_1=-\tfrac12A_\zeta L$, $d_2$ formula; positive-lag theorem | Leading done; original needs AN1 + AN7 |
| E3 | Lag collapses through the crossover while exposure is roughly steady | Lag ODE; WIT windows | Signs proved; a quantitative "collapse" statement is not |
| E4 | Crossover ≈1.10–1.15 physical time after weak learning | Selected-orbit timing | Existence proved; the decimal is **[eval]**; two-sided analytic timing optional |
| E5 | Canonical depth several times the coherent limiting value | B-bridge (AN4) | Open |
| E6 | Persistence through physical time 100 | LP/LPR + AN7 | Limiting done; original open |
| E7 | Weak amplitude $H_{Q2}$ tracks $(\lambda+q^2)\int(1-\mathsf m_2)$ with a small positive correction | CLOCK amplitude identity; BULK bulk clock | Exact identity done; defect bound conditional |
| E8 | Weak mass exponent ≈0.576 at strong half-mass (instantaneous mask) | Seed law; compare $1-\lambda=5/9$ at $\rho=2/3$ | Conditional |
| E9 | Positive-quadrant initialization restores compositional Swing-by | Not in current scope | Out of scope for A/B |

---

## 2. Notation and the exponent dictionary

$\lambda=\rho^2$, $K(z)=\phi(z)+z\Phi(z)$, $a_\rho=\rho K(\rho a_\rho)$, $P=\Phi(\rho a_\rho)$, $\alpha=\lambda P/2$,
$$\omega=\tfrac{1-\lambda}{2},\qquad d=\tfrac12-\alpha,\qquad s=\frac d\omega=\frac{1-\lambda P}{1-\lambda},\qquad p=\frac3s,$$
$$\kappa=\frac{\log(1/S_0)}{\log(1/q)},\qquad E_{\rm loc}(\kappa)=\frac\kappa2(1-P)-s,\qquad \gamma_\kappa=1-\frac\lambda2\Big(\kappa-\frac4{1-\lambda}\Big).$$

**Ratio box.** $\rho\in[13/20,7/10]$, so $\lambda\in[169/400,49/100]$ and $1/2<P<153/250$ **[rational]**.

### 2.1 Target-only timing thresholds in κ (exact comparison results)

| Threshold | Meaning (target-only flow) | Range on the box |
|---|---|---|
| $2/\lambda$ | Bulk Q2 ancestry crosses the weak axis | $[4.08,4.74]$ |
| $2/\omega=4/(1-\lambda)$ | Every Q1 label reaches the strong chart | $[6.93,7.85]$ |
| $2/(\lambda(1-\lambda))$ | Bulk Q2 passes every fixed Q1 angle | $[8.00,8.20]$ |
| $4/\lambda$ | Every Q2 label (including near $\pi$) has crossed | $\le 1600/169<10$ **[rational]** |
| $2/\lambda+4/(1-\lambda)$ | Bulk Q2 reaches the strong chart; $\gamma_\kappa=0$ | $[11.66,11.92]$ |

Ranges are endpoint evaluations of monotone expressions; the only inequality used in a proof so far is the marked one.

### 2.2 Passage thresholds (conditional on candidate entry laws)

| Threshold | Meaning | Value |
|---|---|---|
| $E_{\rm loc}>0$, i.e. $\kappa>2s/(1-P)$ | Local core shape stays small through weak half-mass | ≈6.3–7.0 on the box **[eval]** |
| $pE_{\rm loc}>1$, i.e. $\kappa>8s/(3(1-P))$ | Mass-charged escaped tail costs $o(1)$ at fixed core radius | ≈8.4–9.3 **[eval]** |
| κ=10, χ=1/20 | $E_{\rm loc}>3616/6375$; $p(E-\chi)-1-r_m\ge4561/35006$; $\Delta_\nu>3/25$ for $\nu\le1/100$ | **[rational]** (PROFILE, TAILREP) |
| κ=10 secondary tail | $\gamma\ge6481/18480$; $\Gamma_\nu\ge289169/924000>3/10$ | **[rational]** (BULK) |

### 2.3 The canonical point, analytically

At $(q,S_0)=(1/20,\,2\cdot10^{-4})$, $\kappa=\log 5000/\log 20$. Since $20^2=400<5000<8000=20^3$, we have $2<\kappa<3$ **[rational]**. On the box $2/\lambda\ge 200/49>4$ and $2s/(1-P)>2\cdot 1.28/(1/2)>5$ (using $s\ge s(169/400,153/250)>1.28$) **[rational]**.

So, **at the level of exponents**, the canonical point lies in the regime where (i) bulk Q2 ancestry has not crossed the weak axis at strong entry, and (ii) the candidate local passage makes the strong shape non-small. These are asymptotic-in-$q$ comparisons. At the fixed value $q=0.05$ the $O(1)$ constants are not controlled, so this is a regime identification, not a theorem about the canonical run.

---

## 3. What is established

### 3.1 Exact identities and estimates for the original flow

| Result | Source |
|---|---|
| Untied flow, balance, regularity, learning observables, exact rate decomposition $E'_\xi=D_1+D_2$ | F, P |
| Source-by-motion factorizations with complete remainders; exact mean lag and Stein relation | P (`pa:factorizations`, `pa:Lex`) |
| Early comparison, initialized escape, positive-coordinate ancestry lower bound, Q2 ancestry vs late arrivals | P, TAIL, RET2, ARR |
| Aggregate amplitude identity $H_C'=Q(1-c)H_C+\mathcal D_C$, response ledger, cross-output energy bound | CLOCK |
| Cohort-change identity; transverse inequality $D^+\sqrt{J_G}\le r_G\sqrt{J_G}+\ell_G\sqrt{E_G}$; residual-norm entry bounds | BULK |
| Outside-group cost: value $a_*\mu_B/q$, receiver derivative $\le 34\mu_B/q$ | PROFILE |
| Signed Jensen and weak-amplitude equation | SGWR |
| Overlap-window strong profile at $t_m=(2/\omega)\log(1/q)+C_m$: full right-half-circle chart; shapes $\widehat h\,e^{O(q^{\zeta})}$ and weights $\widehat m\,e^{O(q^{\sigma})}$ relative to the same-field reference at $\alpha_c=qa_q$; reference offset $O(q^\zeta)$; normalized tail sandwich with cutoff | OWPT |
| Strong passage from the moving overlap to half mass: logistic clock defect $O(q^2\ell^2)$, $t_h=10\ell-\log A_q+o(1)$, chart $R=79/51$, reference $\to(a_\rho,a_\rho)$, uniform pairwise shapes $\mathcal G\,e^{o(1)}$, relative weights $e^{O(q^2\ell^2)}$, tail sandwich, left-ancestry mass $\le Cq^2\ell^2M$; finite-noise $C^1$ reduction on the chart | MOMC |
| Whole-Q2 entry energy at strong half mass: $N_2/M\le CA_q^{-1}q^3$, hence $J_G(t_0)\le C_Jq^3$, $E_{G_+}(t_0)=o(1)$ | Q2EP |
| Primary Q2 entry at $t_0=t_h$ with fixed constants: signs, $|a|/z\le\frac14$, $qj/z\le C_0$ (clock $\le C_{\rm clk}q^{1/8}$), clock seed $\asymp A_q^{-\lambda}q^{10(1-\lambda)}$, chart cap Z for $c_0<Kq^\gamma$; weak-axis band matching of late crossers | Q2EC |
| Secondary (recruited) Q2 entry profile at $t_0$: positive displacement $\asymp h_A[(c_0+q)/(q(s_0+q))]^{2d/\lambda}$ about the actual reference, weights $D_h^{-2}\hat m\,e^{o(1)}$, tail $\le CB_qq^3\min\{1,(h_A/w)^{p_2}\}$; homogeneous same-field chart comparison | SEP |

### 3.2 Exact comparison results (positive-noise target-only flow)

| Result | Source |
|---|---|
| Q2 first integral and density; zero-noise coordinate-energy profile; fixed-interior crossing/transit clocks | Q2 |
| Exact attracting strong center $a_q=a_\rho+O(q^2)$; uniform Q1 arrival with $(c_0+q)$ regularization; entry profile $h_T\asymp\epsilon(c_0+q)^{-s}$, weight $\asymp S_0e^T(c_0+q)^2$; tail index $3/s$ with finite cutoff; Q4 companion | PROFILE |
| Uniform Q2 crossing through both endpoints; secondary recruited tail with index $p_2=(1-3\lambda/2)/d\in(0,1)$; whole-Q2 energies $J\asymp q^3$, $H\asymp q^5$ at κ=10 | Q2E |
| Bulk clock cohort $\{c_0\ge q^{1/4}\}$: seed $\asymp q^{10(1-\lambda)}$, angular margin $\sin\theta/q\ge cq^{-1/8}$; intermediate band | BULK |
| Threshold dichotomy before chart arrival: $q\cot\widehat\theta(T)\asymp[q^\gamma(s_0+q)/(c_0+q)]^{(1-\lambda)/\lambda}$; $c_0\ge Kq^\gamma$ gives $q\hat j/\hat z\le C_0$; the rest are in the chart with displacement $\le Z(C_0)$ | RCET |

### 3.3 Results within the defined leading system

| Result | Source |
|---|---|
| Scaled population equations, resident curve, mean/shape spectra, positive-lag theorem, probe and source-rate identities | P, SCALED |
| Selected coherent orbit and its reversal for $0<\rho<1$ | P |
| Learned witnesses at quarter-mass covering the exact canonical scaled offset $5\pi/9$; common windows; gate-aware population tolerance; own-half-mass clock; static learning bounds | WIT |
| Eventual zero benefit, compact-parameter clearing, $\sqrt{\log}$ growth; combined learned reversal + clearing | LP, LPR |
| Two-sided all-label passage with Riccati closure | RET2 |
| Local-rate passage with collective mean tracking | LOC |
| Square-root weak forcing, weak concentration, coupled strong-mean/weak-orbit selection at fixed $n_b$ | WEAK |

### 3.4 Conditional original-flow implications (proved implications; inputs open)

| Implication | Inputs still to be proved | Source |
|---|---|---|
| c-form local passage with exact response clock, multiplier $(H_b/H_0)^{\alpha/Q}$ | c-form field contract on the trajectory; endpoint amplitude cap; signed defect bound | CLOCK |
| Left-facing Q2 tracking with explicit full-output defect | Weighted time integral of the defect | Q2 |
| Bulk-clock bootstrap: $D_{\rm osc}=O(q^\eta+q^2\log(1/q))$, gate margin, relative amplitude transport | Residual norms; Cartesian entry ratios | BULK |
| Small-constant ($\eta=0$) transport: $D_{\rm osc}=O(C_0+q^2\log(1/q))$, growing margin, relative transport $e^{\pm2D}$, $E\le\frac{10}{9}H$ | Residual norms; Cartesian entry ratio $\le C_0$ | RCET |
| Residual closure: bounded diagonal norms, $O(q)$ cross norms, $\int\sup\lvert R_{11}\rvert\le C\int\lvert1-\kappa_1\rvert+o(1)$, no $H_b$ smallness | Energy/core/outside budgets; independent backward clock bound (superseded by LCRC) | RCET |
| **S0 closed (Route 3):** the same residual conclusions plus $H\le H_{G_+}\le\frac98c_b+o(1)$, $E_{G_+}\le\frac54c_b+o(1)$, $J_G\le Cq^2$, chart-group mass $O(q^3)$. No clock premise, no terminal cap | S1 entry contracts and $\int\lvert1-\kappa_1\rvert\le B_s$; core chart $R$; chart-group retention $Z$; $\mu_B=o(q)$; S2 secondary contracts (distance envelope, capped gain) | LCRC |
| Mass-charged complement with gain law; κ=10 margin | Capped radial gain; transferred entry profile | TAILREP |
| Secondary Q2 energy $\lesssim q^5+q^{\Gamma_\nu}H$ | Pre-exit distance envelope; capped gain | BULK |
| Forcing with a separate clock: $\mathfrak F\lesssim q^3+q^\sigma H+q^{(1+\sigma)/2}\sqrt H$ | Energy inputs; residual norms | BULK |
| Perturbed selection theorem with core moment and outside defects | Weak return region; matching | TAILREP |
| Growing-window persistence | AN7 compact-window error transfer | LP |

---

## 4. Remaining steps for the deep-regime theorem (κ = 10 target)

The steps are listed in dependency order. Each entry states the claim to prove, the tools in hand, a suggested analytic route, and what it unlocks.

### S0. Residual-norm closure (closed conditionally: RCET + LCRC)

**Claim.** On the passage interval: diagonal residual norms are bounded; cross norms are $O(q)$; $\int\sup_G|R_{11}|$ is bounded.

**Proved in RCET.**
- *Diagonal norms.* The loss is nonincreasing, so $\|e\|_{L^2(P_p)}^2\le4\mathcal L(0)$.
- *Instantaneous output bounds* (RCET Lemma 4.1). With $Y=\sqrt{J_G}/q$: cross norms$/q\le C\{1+E_G+q^2Y^2+\sqrt{E_G}\,Y+\mu_B/q\}$, and $f_1=\kappa_1X_1+g_1$ on $P_1$ with $\|g_1\|\le C\{q^2+q^2Y^2+q^2Y\sqrt{E_G}+\mu_B\}$.
- *Volterra closure* (RCET Theorem 4.2). BULK's transverse inequality gives
  $$Y(t)\le A_*+Ce^B\!\int E\,Y+Ce^Bq^2\!\int\sqrt E\,Y^2 .$$
  If $\sup E$, $\int E$ and $\int\sqrt E$ are bounded, Grönwall gives bounded $Y$, $O(q)$ cross norms and $\int\sup|R_{11}|\le C\int|1-\kappa_1|+o(1)$. No smallness of $H_b$ is needed.

**RCET's open premise (now removed by LCRC).** RCET bounds $\int E$ using an *independent* backward clock bound $H(s)\le e^DH(t)e^{-b_0(t-s)}$. Taking it from BULK would use the residual bounds being proved. On a stopped interval $[t_0,t_*]$ the missing inequality is $H(t_*)\le eH_b$ at every first-exit endpoint. The terminal cap $H(t_b)\le H_b$ does not give it, and RCET shows the scalar endpoint-to-integral inference is false.

**Route 3, a pointwise ledger cap inside a joint guard: proved (LCRC Theorem 4.1).** The sketch below is what LCRC carries out. LCRC also derives the chart-group mass $\mu_{\rm chart}\le4C_Je^{2B}q^3$ from $(\log m)'\le2r+Cq^2(MZ+Z^2)$, so the mass is not a separate input. It obtains $E_{\rm sec}\le C(q^5+q^{\Gamma_\nu}H)$ from the raw guard $H\le E_{G_+}<E_g$ rather than from a terminal cap.
- *Exact identity.* $\mathbb E_{P_2}[X_2(U\!\cdot\!X)_+]=QU_2+\mathbb E_{P_2}[X_2(U\!\cdot\!X)_-]$, so for any fixed cohort $S$,
  $$c_S=H_S-A_S+\tau_S,\qquad \tau_S=Q^{-1}\!\int_SW_2\,\mathbb E_{P_2}[X_2(U\!\cdot\!X)_-].$$
  If $W_2\ge0$ on $S$, then $\tau_S\ge-C\mu_Se^{-\rho^2/(4q^2)}$, because the only negative contribution comes from $\{X_2<0\}$. No angular margin is needed.
- *Sign-good group.* Let $G_+$ be the clock cohort together with RCET's $\eta=0$ group ($c_0\ge Kq^\gamma$). Under the stopped guards, BULK 4.1 and RCET Theorem 2.1 hold on $[t_0,t_*]$ and give $|a|\le z/3$ on $G_+$. So $W_2\ge\frac23z>0$ and $A_{G_+}\le H_{G_+}/9$.
- *Charge everything else in absolute value.* $|c_S|\le E_S+Cq\sqrt{E_SJ_S}$ for any cohort; $|c_K|=O(q^2)$; $|c_B|\le C\mu_B$.
- *Resulting cap.* With $c\le c_b$, this gives, at every $t\le t_*$,
  $$\tfrac89H_{G_+}\le c_b+E_{\rm rest}+Cq\sqrt{E_{\rm rest}J_{\rm rest}}+Cq^2+C\mu_B+\text{exp. small}.$$
  Here rest $=$ chart group $\cup$ secondary tail. If $E_{\rm chart}\le CZ^2q^2\mu_{\rm chart}=o(1)$ and $E_{\rm sec}\le C(q^5+q^{\Gamma_\nu}H)$ (BULK's secondary implication), then $H\le H_{G_+}\le\frac98c_b+o(1)$.
- *Closing the bootstrap.* Use joint guards $Y<K_Y$, $\int r<B$, $E_{G_+}<E_g$. The cap improves the third guard. Every $G_+$ label has a defect bound on $[t_0,t_*]$, so $\int_{t_0}^{t_*}H_{G_+}\le eH_{G_+}(t_*)/b_0$. RCET's Volterra step then improves the first two guards.
- *What it removes and what it costs.* It removes both the independent clock premise and the terminal cap, which becomes a conclusion. The only inputs left are instantaneous-state budgets (chart-group mass and displacement; secondary energy), of the same type as those already open.
- *Constant order.* Fix $(B,E_g,K_Y,M)$ before $C_0$. Then $C_0<C_{\rm adm}(M,B)$, and $K,Z$ depend on $C_0$. $Z(C_0)$, which grows as $C_0\to0$, enters only through $Z\mu_{\rm chart}$ (cross outputs) and $Z^2q^2\mu_{\rm chart}$. So no loop arises provided $\mu_{\rm chart}=o(1)$ along the passage.

**Withdrawn.** The v1 shortcut "$\mathfrak F\lesssim H_b+L\sqrt{qH_b}+q^3$, so $L$ has a fixed point" (§8, item 9).

**Retained inputs (LCRC).**
- S1 entry contracts at $t_0$: $z>0$, $|a|/z\le1/4$, ratio $\le C_0$ on $G_+$ and $\le C_{\rm clk}q^{1/8}$ on the clock, $J_G(t_0)\le C_Jq^3$, $H(t_0)\asymp q^{10(1-\lambda)}$, and the secondary entry profile.
- $\int|1-\kappa_1|\le B_s$.
- Core chart $|\theta|+|\psi|\le Rq$ with $\mu_{\mathcal K}\le M_{\mathcal K}$; chart-group retention $|\theta|+|\psi|\le Zq$; $\sup\mu_B/q\to0$.
- S2 secondary contracts: the distance envelope and the capped gain at every intermediate endpoint.

**Assembly requirements (for S1–S3).** LCRC fixes $(B,E_g,K_Y,M)$ before $C_0$ and $q$. Two conditions keep that order valid once the retained inputs are proved.
1. *Stopped form.* Every retained trajectory budget (core chart, chart retention, $\int|1-\kappa_1|$, distance envelope, gain) must be proved as an implication on $[t_0,t_*]$ from LCRC's guards, never as a global statement that itself assumes S0. Otherwise RCET's circularity returns one level down.
2. *Guard-independent $O(1)$ constants.* Only $R$, $M_{\mathcal K}$, $B_s$ and $c_b$ enter LCRC's constants at order one, through $C_x$, $C_r$, $C_v$ and $B=C_rB_s+2$. These must not depend on $(B,M,K_Y)$ except through $o(1)$ terms. Every other constant ($C_J$, $Z$, $F$, $C_\Sigma$, the S2 constants) multiplies a positive power of $q$ and may depend on anything fixed before $q$.
   - Watch $R$. The core's own cross output feeds $C_x$, and the cross residual drives the core's scaled rotation. A crude bound $R=R(M)$ would create an $R$–$M$ loop. Get $R$ from the leading strong field's fixed point (S3, LOC) instead.
   - Watch $B_s$. Its strong-learning proof should give $B_s=B_s^0+o(1)$, with the guard-dependent residual entering only through $q^2\log(1/q)$ terms.

**Unlocks.** Removes the residual-norm hypotheses of BULK Theorems 4.1 and 6.2, the independent clock premise, and CLOCK's endpoint amplitude cap. What remains is the S1/S2 entry, chart and gain inputs above.

### S1. Strong-stage tracking — **the main bottleneck**

**Claim.** From the end of the early comparison ($S\le\delta$) through strong learning to a common entry time $t_0$, the original strong family reproduces the target-only entry state. That means: the exact center $a_q$; the joint input/output profile with tail index $3/s$ and its cutoff; the radial weights; the Cartesian entry ratios for the Q2 bulk; and $\int|1-\kappa_1|<\infty$. All with explicit $q$-dependence.

**Why it is the bottleneck.** Every downstream theorem (c-passage, mass charging, bulk clock, secondary energy, selection) consumes this entry state.

**Suggested route (matched comparisons).**
1. *Overlap window — **proved (OWPT Theorem 3.1), exact original-flow result.*** At $t_m=(2/\omega)\log(1/q)+C_m$ every right-half-circle label is charted, $S(t_m)\asymp e^{C_m}q^\sigma$ with $\sigma=10-2/\omega\in[110/51,710/231]$, and relative to the actual characteristic launched at $\alpha_c=qa_q$:
   - pairwise shapes are $\widehat h\,e^{O(q^\zeta)}$, $\zeta=\sigma-1\ge59/51$;
   - radial weights are $\widehat m\,e^{O(q^\sigma)}$;
   - the reference itself is $a_q+O(q^\zeta)$ (mean-mode data, kept separate from shape).

   The proof normalizes the label tangent by the target-only tangent. The unperturbed generator $h\begin{pmatrix}-1&1\\1&-1\end{pmatrix}$ has a row-stochastic propagator, so there is no logarithmic-time loss. The $O(S/q)$ coupling to the network output enters only through $\int S/q=O(q^\zeta)$.
2. *Leading strong system in $M$.* **Start at $M_0=M(t_m)$, not at $M\approx\delta$.** Step 1's crude bound on the network-output coupling, $O(S/q)$ in scaled units, is useful only while $S\ll q$. On $q\lesssim S\lesssim\delta$, only the structured $O(M)$ coupling of the leading field is accurate enough. Run an $M$-clock version of LOC to $M\to1$ with $N\approx0$: fixed core, same-field reference, collective block $J_M$. **LOC Lemma 3.1 already proves $J_M\preceq J_1$ uniformly for $0\le M\le1$**, and the centered shape rate is $-(1-M)/2+\alpha$. The linear multiplier is $\mathcal G=(M_1/M_0)^{-d}((1-M_0)/(1-M_1))^{\alpha}$.
   - *Leading center.* At $N=0$ the coherent leading center is **stationary** at $(a_\rho,a_\rho)$ for every $M$ (`pa:resident`, LOC Lemma 3.1). The P2 coupling term $-\rho M F(\rho x,\rho a)$ cancels the loss of P1 restoring force exactly at $x=a_\rho$. A finite-$q$ coherent equilibrium during the passage would be a separate object, not yet defined. The actual reference is tracked relative to $(a_\rho,a_\rho)$, never reset.
   - *Handoff (corrected in SMCP).* With $A_q:=M_0/(e^{C_m}q^\sigma)\in[c,C]$, one has $\epsilon_mM_0^d=A_q^d\,q^{10d-s}$. The factors $e^{C_m}$ cancel, but the order-one coefficient $A_q^d$ stays. The leading half-mass duration from $t_m$ is $\sigma\log(1/q)-C_m-\log A_q+o(1)$, so strong half mass is reached at $10\log(1/q)-\log A_q+o(1)$. That clock shift must be carried into phase matching.
   - *Obstruction at fixed $C_m$ (SMCP Theorem 2.1, original flow).* Labels in the outer band $\cos\beta\le q$ have $h(t_m)\asymp e^{-dC_m}$, which is order one, not $o(1)$. Because $f_0''=\frac12\rho^3\phi(\rho x)>0$, their first unit of contraction already deviates from $\mathcal G$ by a factor $\ge e^{ke^{-dC_m}}$. So a uniform-over-labels transfer by the **linear** multiplier is false at fixed $C_m$. Cooperativity does not remove the deviation: SMCP Prop 3.1 shows it survives to $M=\frac12$ in the exact atomic leading field.
   - ***Proved (MOMC Theorem 1.1), exact original-flow result through strong half mass.*** With $C_m=\frac12\log(1/q)$ and no retained inputs:
     - mass clock $M'/M=1-M+\delta_M$ with $\int|\delta_M|=O(q^2\ell^2)$, and half mass at $t_h=10\ell-\log A_q+o(1)$;
     - chart $R=79/51$ (from $a_\rho<28/51$), with the reference within $o(1)$ of $(a_\rho,a_\rho)$;
     - pairwise shapes $\mathcal G(M(t),M_0)e^{O(\mathcal D_q)}$ uniformly over all pairs, where $\mathcal D_q=q^{d/2}+\epsilon_m+q^{v}+q^2\ell+q\ell^2$;
     - relative radial weights $e^{O(q^2\ell^2)}$, and the normalized tail sandwich with index $3/s$ and cutoff;
     - left ancestry $\mu\le Cq^2\ell^2M$, so $\int\mu/q=O(q\ell^2)$.

     At half mass the tail parameter is $\sqrt2A_q^d(1-M_0)^\alpha q^{10d-s}$, the target-only entry scale $q^{-s}S_0^d$ times the order-one factor $\sqrt2A_q^d$. The finite-noise $C^1$ reduction ($\|\mathcal F_q-f\|_{C^1}\le C_Rq^2+160\mu/q$) and the exact leading receiver Jacobian, with $\partial_yf_y=-(1-M)/2$, are proved there and reusable.
   - *The repair as proposed (now carried out):* take $C_m=C_m(q)\to\infty$ with $e^{C_m}q^\zeta\to0$, e.g. $C_m=\frac12\log(1/q)$. Then:
     - $S(t_m)\lesssim q^{\sigma-1/2}\ll q$;
     - OWPT's errors become $e^{O(e^{C_m}q^\zeta)}$ and $e^{O(e^{C_m}q^\sigma)}$, which still vanish;
     - every label has $h(t_m)\lesssim e^{-dC_m}=q^{d/2}\to0$;
     - the nonlinear correction is $\le k_+\int h=O(e^{-dC_m})=o(1)$;
     - the handoff and the half-mass time are $C_m$-free.

     What must be checked is that PROFILE's comparison constants are uniform for all times $t\ge t_{\rm arr}+C$ (it suffices that the target-only contraction after arrival has a bounded nonlinear factor).
   - *Alternative repair.* Transfer relative to the nonlinear atomic test flow $h'=r_0(M)h+R(h)$ label by label, as OWPT did relative to the nonlinear target-only flow. This is exact at fixed $C_m$, but its terminal profile is then a nonlinear image of the entry profile.
   - *Tangent route (for either repair).* At the atomic center the leading receiver Jacobian is $J_{\rm sh}(M)=\begin{pmatrix}-(1-M)/2&\alpha\\\alpha&-(1-M)/2\end{pmatrix}$, and at aligned displacement $h$ it is $J_{\rm sh}+O(h)$. (In the $x$-row, the $\pm\rho^3\phi$ terms cancel at $x=y$ and $\partial_xF=0$ for $x\ge a$; the session should check the $y$-row.) So $J_{\rm sh}-r_0I=\alpha\begin{pmatrix}-1&1\\1&-1\end{pmatrix}$ has a row-stochastic propagator, as in OWPT. The perturbations to integrate are:
     - the nonlinear $O(h)$ term;
     - the donor spread $O(\epsilon_m)$;
     - the reference offset;
     - finite-$q$ corrections $O(q^2)$;
     - the outside population, $O(\mu/q)$.
3. *Finite-noise field in the strong chart.* **Proved on the chart $R=79/51$ through half mass (MOMC Lemma 4.1).** Beyond $t_h$ it must be re-verified for any larger chart that later stages use.
4. *Labels outside the chart.* **Proved through half mass by mass charging (MOMC).** This charges them by mass only; it does not give their geometry.
5. *Strong-learning integrability.* Proposed entry time: $t_0:=t_h$, the first strong half-mass time. LCRC/BULK seeds are evaluated at strong entry, $H(t_0)\asymp q^{10(1-\lambda)}$, so $t_0\approx10\log(1/q)$ is the intended time. With this choice:
   - in the leading law $\int_{t_0}^\infty(1-M)=\log2$, so the expected guard-independent constant is $B_s=\log2+o(1)$;
   - its proof belongs to the stopped-form weak-passage bootstrap, i.e. with S3;
   - the c-form field contract (S3) must then carry the $-(1-M)/2$ contraction explicitly, not as a small remainder. Dropping it only for an upper bound costs a factor $e^{\int(1-M)/2}=2^{1/2}$.
6. *Q2 entry at $t_0=t_h$ — **proved for the primary group (Q2EP + Q2EC), exact original flow, fixed constants.***
   - **Q2EC Theorem 1.1.** For the primary group $c_0\ge K(C_0)q^\gamma$:
     - $z>0$, $|a|/z\le\frac14$ and $qj/z\le C_0$;
     - the clock lies inside the primary group, with $qj/z\le C_{\rm clk}q^{1/8}$;
     - two-sided transport $q\cot\theta=D_h^{-1}q\cot\hat\theta\,e^{O(1/x_{\min})+o(1)}$;
     - clock seed $H_{\mathcal C_q}(t_0)=A_q^{-\lambda}\hat H_{\mathcal C_q}(10\ell)e^{o(1)}\asymp A_q^{-\lambda}q^{10(1-\lambda)}$;
     - every $c_0<Kq^\gamma$ label lies in the chart, $|\theta|+|\psi|\le Zq$, at $t_0$.

     Key devices:
     - a weak-axis band of physical width $q^{1-\varepsilon}$, crossed while $M=O(q^{1/2})$, giving a relative Cartesian match before diagonal transport;
     - the exact angle-difference equation $\Delta'=-\mathrm{tr}R\sin\Delta+(C_{12}-C_{21})\cos\Delta$, so that $|a|/z$ is controlled through angles, not through Cartesian ratios;
     - an inward-pointing fixed receiver square. The bulk clock exponent is $\delta_*=\min_{\rm box}[\frac3{4\lambda}+5\lambda-\frac{15}4]=\frac{1861}{13520}>\frac18$ **[rational]**, attained at $\lambda=169/400$.
   - **Proved (Q2EP Theorem 2.1, exact original flow):** $N_2/M\le8e^7C_QA_q^{-1}q^3$ on $[t_m,t_h]$. Hence $J_G(t_0)\le C_Jq^3$ and $E_{G_+}(t_0)=o(1)$ for every subcohort of the initial Q2 ancestry.
   - **Obstruction to the $e^{o(1)}$ form (Q2EP Prop 4.1, leading system).** Off the chart the strong cross drive contributes $-Ma_\rho/2$ in scaled units. On the aligned ray, $x'=f_0(x)+\frac M2(x-a_\rho)$, so the universal factor $D_h^{-1}=[2(1-M_0)]^{-1/2}$ carries a relative correction $\int Ma_\rho/(2x)$. That correction is bounded below by $a_\rho\log3/(8\sqrt6L)$ for a receiver ending at scaled angle L.
   - **This does not obstruct LCRC.** LCRC's Q2 contracts are fixed-constant inequalities. The same identity bounds the correction above by $\frac34a_\rho/x_{\min}$ plus a Gaussian-small term. So $q\cot\theta(t_0)=D_h^{-1}q\cot\hat\theta(t_0)\,e^{O(1/x_{\min})+o(1)}$, where $1/x_{\min}\asymp q\cot\theta\lesssim C_0$ on the $\eta=0$ group: a bounded factor, absorbed by enlarging K.
   - Late crossers: Q2EC matches them through the weak-axis band, using $T_\times\le\frac{1600}{169}\log(1/q)+O(1)$ and $M(T_\times)=O(A_qq^{90/169})$. The worry recorded in v1.6, that the antisymmetric drive scales like $M\cdot x$ before crossing, is moot: $|a|/z=|\sin\theta-\sin\psi|/(\sin\theta+\sin\psi)$ with $|\Delta|\le C(q^u+qM)$.

   Original specification (historical; its "$e^{o(1)}$" claim is withdrawn by ledger item 15) — supply LCRC's left-half entry contracts in the original flow:
   - the $\eta=0$ group and clock: $z>0$, $|a|/z\le\frac14$, $x=qj/z\le C_0$ (resp. $\le C_{\rm clk}q^{1/8}$);
   - $H_{\mathcal C_q}(t_0)\asymp q^{10(1-\lambda)}$ with its $A_q$ dependence;
   - the chart group in the strong chart;
   - $J_G(t_0)\le C_Jq^3$ and $E_{G_+}(t_0)=o(1)$.

   Route: at $t_m$, labels at angle $\theta\gg q$ transfer by the absolute early comparison, since the relative error $\overline S/\theta\to0$. Chart-scale labels need OWPT's multiplicative transfer. On $[t_m,t_h]$ a Q2 receiver off the chart sees P1 drive $\approx(1-\kappa_1)/2$ on $U_1$, P2 drive $\approx\lambda/2$ on $U_2$, and cross terms $O(q)$. So $q\cot\theta$ equals its target-only value times $e^{-\int M/2}=(2(1-M_0))^{-1/2}$, up to $e^{o(1)}$, together with the $-\log A_q$ time shift. The dichotomy threshold $K$ moves by an explicit order-one factor. $\int_{t_m}^{t_h}r$ is **not** bounded, because $r\approx(1-M)/2$ for most of the interval, so the $U_1$ growth must be tracked explicitly rather than through BULK's $\int r\le B$. The secondary recruited tail is a separate later step.
7. *Secondary (recruited) entry profile at $t_0$ — **proved (SEP Theorem 1.1), exact original flow, fixed constants.*** The partition is $\Sigma=\{c_0<Kq^\gamma\}$ and $\mathcal D=\emptyset$. Displacements are measured from MOMC's actual reference, with $h_A=A_q^dq^{10d-2s}$ and $B_q=A_q^{-1}D_h^{-2}$:
   - $\xi\le Z+2R$;
   - each component $V_i\asymp h_A[(c_0+q)/(q(s_0+q))]^{2d/\lambda}$;
   - $m/\hat m=D_h^{-2}e^{o(1)}$;
   - $\eta\{\xi>w\}\le CB_qq^3\min\{1,(h_A/w)^{p_2}\}$, two-sided on Q2E's interior range.

   Key device: the same-field subtraction makes the chart error homogeneous, $V'=f^M((a,a)+V)-f^M(a,a)+E\,V$, with no additive floor. A cooperative secant propagator then gives bounded two-sided distortion, $e^{\frac12\int M}\in[1,\sqrt2]$ times fixed factors. The coefficient $p_2<1$ follows from $\lambda(3-P_\rho)>100893/100000$ **[rational]**.

   **With this, S1 supplies every LCRC entry contract at $t_0=t_h$** (OWPT, MOMC, Q2EP, Q2EC, SEP), unconditionally. What remains of LCRC's inputs are trajectory budgets on $[t_0,t_b]$: core retention, $\mu_B=o(q)$, $B_s$, and the S2 distance/gain contracts for Σ and for the strong complement. All of them must be proved in stopped form.

   Original specification of step 7 (historical): Q2E's recruited set consists of the Q2 labels already in the strong chart at strong entry, i.e. $c_0\lesssim q^\gamma$. This is the same set as Q2EC's $c_0<Kq^\gamma$ group.
   - *Suggested partition.* Put all of it in LCRC's $\Sigma$ and take $\mathcal D=\emptyset$. Its later control is then by the S2 contracts (distance envelope, capped gain) that the strong complement needs anyway, and LCRC's separate chart-retention budget for $\mathcal D$ disappears.
   - *Contract (fixed constants, relative to MOMC's actual reference):*
     - entry displacement $\xi\le Z_\Sigma$ (from Q2EC);
     - total mass $\eta([0,Z_\Sigma])\le Cq^3$ (from Q2EP);
     - the tail $\eta\{\xi>u\}\le Cq^3\min\{1,(h_1/u)^{p_2}\}$, with $h_1\asymp q^{10d-2s}$ and the $A_q$ factors made explicit, plus a two-sided version on Q2E's range.
   - *Route.* Transfer Q2E's two-sided displacement $h\asymp h_1[(c_0+q)/(q(s_0+q))]^{2d/\lambda}$ and weight laws with bounded factors:
     - inside the chart, compare $h'=f_0(a+h)+\frac M2h$ with the target equation. The ratio changes by $e^{\int M/2}\in[1,\sqrt2]$ times $e^{O(\int h)}$;
     - radial weights change by $e^{-\int M\cos^2\theta}$, which is bounded;
     - Q2EC's band matching and off-chart transport cover the labels before arrival.

**Pitfalls.** An $O(\delta)$ early-comparison error is not $O(q)$. The target-only profile is not a valid description of the trained flow once $S\gtrsim q$, and transfer through the absolute early-comparison error fails even sooner: at the box corner its scaled size $q^\zeta$ exceeds the core scale $q^s$ (OWPT Remark 4.1). Before strong learning the finite-$q$ target-only center is $a_q=a_\rho+O(q^2)$, not $a_\rho$. The original core sits at the actual reference $a_q+O(q^\zeta)$, which must not be reset when measuring shape. During the $M$-passage the leading coherent center is stationary at $a_\rho$; it does not move with $M$. Order-one displacements at fixed $C_m$ make linear-multiplier statements fail on the outer band (SMCP).

### S2. Capped signed radial gain along escaping labels

**Claim.** For each strong-complement and secondary-Q2 label, the relative log-mass rate obeys
$$(\log R_\alpha)'\le I'\min\{1,A_0D_0^2e^{\beta I}\}+b_\alpha,\qquad \int b_\alpha\le B,$$
uniformly at every intermediate endpoint, with $\beta=\lambda/Q$ and a gain exponent at most $1+\nu$, $\nu\le1/100$.

**Inputs to supply.**
- The sign or budget of the strong diagonal term $2r_1(a_1b_1-a_1^cb_1^c)$.
- The c-form all-label distance envelope up to physical chart exit.
- The radial defect $2b^\top\mathcal B a-2(b^c)^\top\mathcal B^ca^c$.
- The lower-side cluster-2 gate at $q>0$, via a projected-margin estimate (not a quadrant label).

**Unlocks.** One proof closes both the mass-charged complement (TAILREP, margin $\Delta_\nu>3/25$) and the secondary-Q2 energy (BULK, $\Gamma_\nu>3/10$).

**Update (Oct 21, after CFR).**
- *The strong diagonal term is a budget, not a sign problem.* In TAILREP's exact identity
  $$\tfrac{d}{dt}\log\tfrac{m_\alpha}{m_c}=2r_1(a_1b_1-a_1^cb_1^c)+Q(1-c)(a_2b_2-a_2^cb_2^c)+2b^\top\mathcal B_\theta a-2(b^c)^\top\mathcal B_{\theta^c}a^c,$$
  one has $|a_1b_1-a_1^cb_1^c|\le2$, so $|2r_1(\cdots)|\le4|r_1|$. LCRC's stopped guard $\int\sup|R_{11}|<B$ then puts this term into $b_\alpha$ with $\int\le4B$, at a fixed cost $e^{4B}$ that is harmless against TAILREP's power margins. The session should verify how TAILREP defines $r_1$.
- *Where the real work is:*
  - the distance envelope $D\le C_D\xi e^{\beta I/2}$ until $qD=\delta_0$. Inside a fixed scaled chart this is a log-norm bound on the c-form Jacobian, whose row sums are at most $\lambda(1-c)/2+O(\cdot)$. Off the chart it follows from the full-gate Cartesian rates, where $R_{22}=Q(1-c)/2$ up to gate tails because the selected moment equals the global one under a full gate;
  - the radial defect $\mathcal B_\theta$;
  - the lower-side $P_2$ gate.
- *Order.*
  - **S2a (next):** prove the envelope and the gain as stopped implications from a **c-form hypothesis**, i.e. CFR's field with remainder $\int\epsilon_F\le F_b$ taken as a guard. Then derive $E_\Sigma\le C(q^5+q^{\Gamma_\nu}H)$ (BULK) and the complement mass with $\int\mu_{\mathcal B}/q=o(1)$ (TAILREP).
  - **Weak-passage assembly:** one joint first-exit bootstrap. Its guards are LCRC's guards plus $E_\Sigma$, $\int\mu_{\mathcal B}/q$, the core radius and $\int\epsilon_F$, and its ingredients are CFR, S2a, CLOCK's passage, LCRC and BULK.

**Update (Oct 21, after DECG `AN03_distance_envelope_and_capped_gain_v1`).**
- *Proved, all of it reusable:*
  - the **chart envelope** $D(t)\le p_*^{-1}e^{C_TF_b}D(s)e^{\beta\Delta I/2}$, via $u=\int_0^x\Phi(\rho v)^{-1}dv$. This change of coordinate removes the V forcing and makes the leading Jacobian Metzler with column sums at most $\lambda(1-c)/2$;
  - a **global signed radial bound**, $(\log m_\alpha/m_c)'\le I'\min\{1,q^2D^2\}+4r+C(1+M_{\rm res})q$, with lower-side gates handled by projected margin times $|\sin\theta|$;
  - the **capped gain conditional on the envelope**, with prefactor $e^{6B+1/\beta}$.
- *Stopped at:* the envelope between scaled-chart exit and physical exit ($L_cq\le|\theta|\le\delta_0$), and $\int\mu_{Q3}/q$.
- *Repair (S2a', next). Proposed, not proved.* Part of each stop comes from restrictions the assembly does not need (ledger 17).
  - *A global envelope needs no chart.* Let $N=|\sin\theta|+|\sin\psi|$.
    - The exact angle equations give $N'\le(|R_{11}|+|R_{22}|+C(1+M_{\rm res})q)N+C(1+M_{\rm res})q$. Only matrix values enter, so no boundary trace is needed.
    - Write $|R_{22}|\le d_2+X(t)$ with $d_2=I'/2$. Apply Duhamel against $e^{-\beta\Delta I/2}$, which decays at rate at least $\lambda(1-c_b)/2$. The cross forcing then costs only an additive $C(1+M_{\rm res})/(\lambda(1-c_b))$ in D.
    - Use DECG's chart lemma up to the first exit $\tau_L$ and this bound afterwards, re-entries included, so no chart switching is needed. This gives $C_D\le p_*^{-1}e^{C_TF_b}e^{B+\int X+o(1)}(1+C(1+M_{\rm res})/(L_c-R_c))$.
  - *Gate excess by signed cancellation.* The only off-chart unknown is $\int X$, with $X=(|R_{22}|-d_2)_+$. Exactly:
    - $R_{22}-d_2=\tfrac12E_{P_1}[e_2X_2\mathbf 1_A]-\tfrac12E_{P_2}[e_2X_2\mathbf 1_{A^c}]\le\tfrac12M_{\rm res}q^2+\tfrac12E_{P_2}[(f_2X_2)_+]$;
    - $-R_{22}-d_2\le\tfrac12M_{\rm res}q^2-\tfrac12Q(1-2c)+\tfrac12N_-$, where $N_-=E_{P_2}[(f_2X_2)_-]$.
    - So $X\le\tfrac12(Qc+N_-)+o(1)$ uniformly in θ, and $\int X\le\tfrac Q2\int c+\tfrac12\int N_-+o(1)$.
    - To check: whether CLOCK's passage budget $\int f^*\le F_b$ (it contains c) and CFR's negative-part bound control $\int N_-$.
  - *$M_{\rm res}$ in $C_{\rm ext}$.* Either show that $C_D$ multiplies only vanishing powers of q downstream (tail moments, $E_\Sigma$, $\int\mu_{\rm comp}/q$), or choose $L_c$ after $M_{\rm res}$ and audit every $L_c$-dependent constant.
  - *Q3.*
    - While $\sigma<0$, DECG's negative gate gives $2R_{22}\sin\theta\sin\psi\le Cq+CM_{\rm res}q^2$, with no $I'$. DECG's coarse bound used the positive-part form, which charges $e^{I}$ when both sines are negative.
    - In the Q3 interior, $|R_{11}(\theta)|$ and $|R_{22}|$ are $O(M_{\rm res}q^2)$ up to Gaussian tails, so labels there barely move. Their cost is $\int\mu/q\le Ce^{2B}q\ell^3$, provided they are in the interior at $t_0$, which needs a pre-$t_0$ version of the same speed bound.
    - The strips near π and 3π/2 are not leakage. They belong to the weak (Q2-like) family and the strong family (late joiners), so SEP's and MOMC's entry contracts must be extended to them.

**Update (Oct 22, after GESG `AN03_global_envelope_signed_gate_v1`).**
- *Proved:*
  - the **global sine envelope** $D^+N\le(r+d_2+X+a_*q)N+a_*q$ and its Duhamel form. Comparability with D is checked on the physical strong branch ($|\theta|,|\psi|\le1/2$).
  - the **one-exit splice**, with explicit $\mathcal C_D(t_*)=\sec(1/2)\,p_*^{-1}e^{C_T\overline F_F}e^{B+\mathfrak X+\varepsilon_q}(1+W_*/(L_c-R_c))$, where $\mathfrak X=\int\sup_\theta(|R_{22}|-I'/2)_+$. Re-entries cost nothing.
  - the **signed gate bound** $X\le\tfrac12M_{\rm res}q^2+\tfrac12(Qc+N_-)$. It holds without the cap $N_-\le Q(1-2c)$, because the lower-side bound is smaller by $Q(1-c)/2$.
  - the **cohort charge** $N_-\le C[q^2\mu_{\mathcal K}+E_\Sigma+q\sqrt{E_\Sigma J_\Sigma}+\mu_{\mathcal B}+\mu_{G_+}e^{-k_1/q^2}]$.
  - the **constant audit:** a fixed $M_{\rm res}$-dependent $C_D$ is harmless downstream, and $L_c=R_c+1$ suffices.
  - **Q3:** the lower-side no-gain lemma, and a frozen interior proved from initialization. When both gates are closed, every $|R_{ij}|\le Ce^{-k\Lambda^2}$, with $k=169/3200$; taking $\Lambda_q=\sqrt{3\ell/k}$ gives $\int\mu_{\rm int}/q\le Cq^9\ell$. Only two initial strips of width $2\arcsin(q\Lambda_q)=O(q\sqrt\ell)$ remain, and their consumer contracts are stated.
- *Stopped at:* $\int_{t_0}^{t_*}(Qc+N_-)\le B_{\rm gate}$, uniformly in q.
- *Resolution found in review (verified against the cited proved statements):*
  - The proved source for $\int c$ is **LCRC's backward clock** (eq. `an03lcrcv1:backward` in Lemma `an03lcrcv1:localclock`), $H_{G_+}(s)\le eH_{G_+}(t)e^{-b_0(t-s)}$ with $b_0=Q(1-c_b)$. It needs only the hypotheses of BULK Theorem 4.1 and RCET Theorem 2.1: response, duration, residual norms, $\int r\le B$ and the entry ratios. It needs neither $E_\Sigma$ nor the terminal cap.
  - Hence $\int H_{G_+}\le eE_g/b_0$. With LCRC's response charge and $E_{G_+}\le\tfrac{10}9H_{G_+}$, this gives $\int|c_{G_+}|\le\tfrac{10e}9E_g/b_0+o(1)$.
  - The $\Sigma$, core and $\mathcal B$ parts of c and of $N_-$ are $o(1)$ after integration. This needs a **joint guard** $E_\Sigma<2C_\Sigma(q^5+q^{\Gamma_\nu}H)$ and LCRC's retained core geometry and $\sup\mu_{\mathcal B}/q\to0$.
  - Therefore $\mathfrak X\le\tfrac{5e}9E_g/(1-c_b)+o(1)$, and $C_D$ is fixed.
  - The joint guard then closes by strict improvement through LCRC's secondary lemma, because $C_\Sigma$ depends on $C_D$ but not on the guard's own constant.
- *Side benefit for CLOCK.* The same bound gives $\int c\le\tfrac{10e}9E_g/(Q(1-c_b))+o(1)$; the factor $1/Q$ was missing in v1.11 (ledger 19). With $E_g=2c_b$, this is $O(c_b)$, which is the small passage budget CLOCK needs.
- *Next (S2 closure package):* write the gate-budget lemma and the S2 package as one stopped-guard theorem, covering:
  - the envelope;
  - the capped gain;
  - $E_\Sigma$, with the joint guard closed;
  - the complement mass via TAILREP.

  Then tabulate what the joint weak-passage bootstrap still retains:
  - the fixed-chart c-form remainder;
  - $\int\mu_{\mathcal B}/q$ by ancestry cohort, including the strips;
  - core geometry via CLOCK;
  - $B_s$.

**Status (Oct 23, after S2CP `AN03_S2_closure_package_v1`): closed in stopped-guard form.**
- *Hypotheses retained:*
  - the stopped guards $c\le c_b$, duration, $\int r<B$, $J_G<q^2K_Y^2$, $E_{G_+}<E_g$ and cross residual $\le M_{\rm res}q$;
  - LCRC's core chart and mass bound, and $\sup\mu_{\mathcal B}/q=o(1)$;
  - the S1 entry contracts;
  - for distance and gain only, the fixed-chart c-form guard $\int\epsilon_F\le\overline F_F$ on $[-L_c,L_c]^2$, $L_c=R_c+1$.
- *Proved:*
  - the gate budget $\int(Qc+N_-)\le\tfrac{10e}9E_g/(1-c_b)+o(1)$;
  - the fixed constant $C_D=\sec(1/2)\,C_{\rm loc}\exp(B+\tfrac{5eE_g}{9(1-c_b)}+1)(1+W_*/(L_c-R_c))$;
  - the envelope through re-entries;
  - the gain $m_b\le e^{6B+3}m_b(t_0)\max\{1,A_0q^2\xi^2e^{\beta I}\}^{1+\nu}$ at every endpoint;
  - $E_\Sigma\le C_\Sigma(q^5+q^{\Gamma_\nu}H)$, with the joint guard strictly improved;
  - $\sup\mu_{\mathcal C}/q\le Cq^{\Delta_\nu}$ and $\int\mu_{\mathcal C}/q\le Cq^{\Delta_\nu}\ell$, with $\Delta_\nu>3/25$.
- *Constant order (corrected by S2CP):* $(\text{model},R,M_K,B_s,c_b,\nu,\delta_0,c_*)\to(B,E_g,K_Y,M_{\rm res})\to(L_c,\overline F_F,C_D,A_0,C_m)\to C_0\to(K(C_0),Z_\Sigma,\text{entry})\to C_\Sigma\to q$. $C_\Sigma$ must come after $K(C_0)$ because SEP's constants depend on it.
- *$E_g=2c_b$ is admissible.* After the secondary bound, pointcap gives $E_{G_+}\le\tfrac54c_b+o(1)<2c_b$.

### S3. The c-form field contract

**Claim.** The original strong field has CLOCK's c-form with a remainder controlled in value and receiver derivative, including the selected-residual term $\mathbb E_{P_2}[g_2X_2\mathbf 1_{\{a^\top X>0\}}]$, the outside population, and the $M-1$ terms.

**Suggested route.** On $P_2$, the charted weak output is $f_2=N X_2+O(q^2)$. So the selected defect reduces to $(c-N_{\rm chart})\,\mathbb E[X_2^2\mathbf 1]$ (CLOCK §6 identity), plus transit-cohort cross outputs (BULK forcing bound), plus $\mu_B/q$ from the complement. The task is then $|c-N_{\rm chart}|$ small, which follows from the response ledger once transit and complement responses are bounded.

**Refined route (Oct 21; next session).** No weak chart is needed. Use LCRC's partition $\mathcal K,G_+,\Sigma,\mathcal B$ (with $\mathcal D=\emptyset$).
- *$G_+$ is linear on $P_2$.* $G_+$ labels have angular margin, so their $P_2$ gates are full up to RCET's gate tail, whose integral is $O(C_0+q^2\ell)$. There $f_{G_+,2}=(\sum W_2U_2)X_2+(\sum W_2U_1)X_1$.
  - Its $X_1$ part has selected moment $O(q\sqrt{E_GJ_G})=O(q^2Y\sqrt{E_G})$.
  - Its $X_2$ coefficient differs from c only by $c_\Sigma+c_{\mathcal K}+c_{\mathcal B}+\tau$, all of which LCRC's ledger already charges in absolute value.
- *The other groups.* Σ is charged through $E_\Sigma\le C(q^5+q^{\Gamma_\nu}H)$. The core's own output stays in the strong donor terms (MOMC's reduction). $\mathcal B$ is charged at $\mu_B/q$.
- *Target accuracy is small-fixed, not $o(1)$.* CLOCK's passage needs $\int f_*\le F_b\le e_*/(4C)$, and $f_*=c+|V|+K_w+T+\epsilon_F$ contains c itself. So the c-form passage is a **local** passage to a small fixed $c_b$; there $\int c\lesssim c_b/b_0$. Beyond $c_b$ the selection stage (WEAK, TAILREP) takes over. So $\int\epsilon_F\le\kappa(C_0,c_b)+o_q(1)$ with $\kappa\to0$ is the right contract.
- *Not in S3.* The term T (the strong first moment outside the fixed core) needs the S2 capped gain for the complement.

**Status after CFR (`AN03_c_form_field_reduction_v1`, Oct 21).**
- *Proved:*
  - a selected-moment lemma for any cohort, $|c_S|+\|\mathcal D_S\|_{W^{1,\infty}}\le C(E_S+q\sqrt{E_SJ_S})$, including the scaled receiver derivative;
  - the closed primary budget $\int\|\mathcal D_{G_+}\|_{W^{1,\infty}}\le C\,C_0E_g+o(1)$, from the exact linearity of $G_+$ on $P_2$ and its negative-gate margin;
  - the exact moments $V_O=-\mathbb E_{P_2}[(f_O)_1X_2]/(qQ)$ and $K_O=\mathbb E_{P_1}[(f_O)_2X_1]/q$, with a negative-part bound for $K_O$;
  - the core radial identity $(\log m)'=1-\kappa_1+\delta_m$, which is the input for $B_s$.
- *Stopped at:* the Σ charge needs S2 (ledger 16), and $\int\mu_{\mathcal B}/q$ is unpaid. Everything else needed for the c-form is in hand, given those two budgets.

**Status after S2CP (Oct 23).**
- *Paid:*
  - the secondary charge, $\mathcal U_\Sigma=o(1)$;
  - the complement and the Q3 interior, at PROFILE's $\mu/q$ cost including the receiver derivative;
  - $B_s=\log2+o(1)$, under retained core geometry;
  - the candidate moments, $\int(|V_O|+(K_O)_+)\le C(E_g+K_Y\sqrt{E_g})/b_0+C\int\mu_{\mathcal B}/q+o(1)$ and $\int(K_O)_-\le C\mathcal U_\Sigma+C\int\mu_{\mathcal B}/q+o(1)$.
- *Retained:*
  - the full fixed-chart contract, $\int\sup_{[-L_c,L_c]^2}(|F_{\rm orig}-F_c|_1+\|DF_{\rm orig}-DF_c\|_{1\to1})\le\overline F_F$;
  - pointwise $M_s\le1$;
  - the T representation;
  - the strip budgets.
- *Proposed route for S3b (reviewer; not yet proved):*
  - *Take the c-form's strong family to be the fixed core $\mathcal K$.* Then $T\equiv0$ by definition, and the complement and Q3 interior go into $\epsilon_F$ at their paid $\mu/q$ cost. CLOCK's `cfield` allows any fixed strong family.
  - *Renormalize the donor measure.* Use $\tilde\mu_s=\mu_s\min(1,1/\mu_{\mathcal K})$, and charge the overshoot $(\mu_{\mathcal K}-1)_+$ in value and derivative. S2CP's $B_s$ proof gives $\int(\mu_{\mathcal K}-1)_+\le d_q=o(1)$, so pointwise $M_s\le1$ holds for the renormalized family.
  - *Take $V:=V_O$ and $K_w:=(K_O)_+$,* with $(K_O)_-$ in $\epsilon_F$.
  - Expected result: $\int\epsilon_F\le C\,C_{L_c}C_{\rm RCET}C_0E_g+C\int\mu_{\mathcal S}/q+o(1)$, where $\mathcal S$ is the two strips.
  - Then $\int f_*\le\tfrac{10e}9\tfrac{E_g}{Q(1-c_b)}+\tfrac C{b_0}(E_g+K_Y\sqrt{E_g})+C\,C_0E_g+C\int\mu_{\mathcal S}/q+o(1)$. With $E_g=2c_b$ and $K_Y$ fixed uniformly over small $c_b$ (S2CP), this is below $e_*/(4C)$ once $c_b$ and $C_0$ are small, provided $e_*$ and C do not depend on them (to check).
- *CLOCK's passage then needs* $e_0\le e_*/4$ at $t_0$ and $r_0L_b\le\min\{1/4,a_b/(2K),ge_*/(8C)\}$, with $L_b\propto(H_b/H_0)^{\alpha/Q}\asymp q^{-k\alpha/Q}$. TAILREP's cutoff $d_c=c_*q^{\chi+kP/2}$ is designed to supply that margin.

**Status after CFA (`AN03_c_form_assembly_v1`, Oct 23): closed in stopped-guard form.**
- *Representation.* The strong family is the fixed core $\mathcal K$, so $T\equiv0$. The capped donor measure $\tilde\mu_s=\mu_s\min(1,1/\mu_{\mathcal K})$ costs $C_{L_c,R}(\mu_{\mathcal K}-1)_+$, whose integral is at most $C\,d_q=o(1)$.
- *Selected moments.* Besides CFR's $A_2$, the full angular expansion needs $A_1=q^{-1}E[g_1VI_x]$ and $B_2=E[g_2ZI_x]$. Both are proved:
  - generic bounds $C(J+\sqrt{EJ}/q)$ and $C(E+q\sqrt{EJ})$;
  - the primary cost $C\,C_{L_c}C_{\rm RCET}C_0E_g$, using the $q$ factor in $E(u\cdot X)_-^2$ and RCET's growing margin.
- *Full remainder.* $\int\epsilon_F\le C_FC_{L_c}C_{\rm RCET}C_0E_g+C_{\rm out}F_{\mathcal S}+o(1)$. A term-by-term ledger includes the $P_1$ Stein identities, the $P_2$ expansion $T_1+xT_2=\rho K(\rho x)+O_{C^1}(q^2)$, and the outside moment substitutions. No selected residual is removed by orthogonality.
- *Forcing.*
  - $\int f_*\le\tfrac{10e}9\tfrac{E_g}{Q(1-c_b)}+\tfrac{C_V(E_g+K_Y\sqrt{E_g})}{Q(1-c_b)}+C\,C_0E_g+C_{\mathcal S}F_{\mathcal S}+o(1)$.
  - CLOCK's constants are $g=\gamma_*/2$ with $\gamma_*=1183/20800$, and $e_*=\min\{1/4,\gamma_*/(2C_{\rm pass})\}$. They do not depend on $c_b$, $C_0$ or the guards.
  - LCRC's constants can be fixed uniformly for $c_b\le\bar c=1/4$. Its formulas are monotone in $c_b$ with no $1/c_b$, which I checked against LCRC's closure proof.
- *Conditional passage.* $e_0=o(1)$ (MOMC's mean claim at $t_h$), $r_0\le d_c$, $H_b=\tfrac54c_b$ and $D_-=o(1)$ give $r_0L_b\le Cq^{\chi+kPq^2/(2Q)}=O(q^\chi)$. CLOCK then gives $e\le3e_*/4$ and $r_{\mathcal K}\le2\mathcal A=O(q^\chi)$. This strictly improves the retained core-geometry and reference guards.
- *Constant order:* $(\text{model},R,M_K,B_s,L_c,\bar c,C_{\rm pass},g,e_*)\to(B,K_Y,M_{\rm res})\to(\overline F_F,c_b,E_g=2c_b,C_D,A_0,C_m)\to C_0\to(K(C_0),Z_\Sigma,\text{entry},C_\Sigma)\to q$, with a small fixed $F_{\mathcal S}$ chosen before q.

**Weak-passage bootstrap: what is left. (After LSB, Oct 27: the strip budget is paid, so only the assembly remains; see "Joint assembly" below.)**
- Every guard now has a proved strict improvement, conditional on the others:
  - LCRC: $Y$, $\int r$, $E_{G_+}$ and the cross residual;
  - S2CP: $E_\Sigma$;
  - CFA: $\int\epsilon_F$, core geometry and the reference;
  - S2CP's $B_s$ argument: core mass, since $\mu_{\mathcal K}\le e^{d_q}$;
  - $\sup\mu_{\mathcal B}/q$, except for the strips.
- The only external input is the **strip budget** $\sup\mu_{\mathcal S}/q=o(1)$ and $C_{\mathcal S}\int\mu_{\mathcal S}/q\le$ a small fixed allowance.
- The joint assembly must also show that $c$ reaches $c_b$ within $L_T\ell$. This needs the lower clock bound $c\ge\tfrac89H_{G_+}-o(1)$ and $H_{G_+}\ge e^{-D}H_0e^{I}$.

**Q3 strips: first proposal (superseded by the status after Q3SB below).**
- *π strip, $[\pi,\pi+2w_q)$.* Near π the scaled field mirrors the c-form, with gate factor $\Phi(-\rho x)$ and drift toward Q2. Q3-side labels either stay frozen or cross into Q2 as late weak recruits that lag the bulk.
  - Proposed *direct lag bound:* GESG's global sine envelope is axis-agnostic and also measures distance from the π axis. On the left half, the P1 gate is closed, so the local $|R_{11}|$ is $O(q)$ by loss alone.
  - Combine it with the absolute radial identity, the signed gate excess and the weak clock from initialization. Expected result: $\mu_{\mathcal S_\pi}\lesssim q^{10}|\mathcal S_\pi|\cdot q^2\Lambda_q^2e^{I_{\rm tot}}\approx O(q^3\ell^{3/2})$, hence $\mu/q=o(1)$.
  - Inputs to verify: a cross-residual bound $\|e_1\|_{P_2}=O(q)$ before $t_0$, which no S1 file states explicitly, and the handling of labels after they rotate toward π/2.
- *3π/2 strip, $(3\pi/2-2w_q,3\pi/2]$.* These labels are strong late joiners. MOMC's chart claim collapses the whole right half into the strong chart by $t_m$, and these labels likely follow.
  - Near the strong axis, their post-$t_0$ weak gain is of order $q^2\xi^2e^{\beta I}$. The crude left mass $Cq^2\ell^2$, or even a lag bound $q^3\ell^{3/2}$, is therefore not enough.
  - They need the joint mass–displacement tail `latestrip`, obtained by extending MOMC and PROFILE across $\beta=-\pi/2$. The cheap alternative, proving that they stay on the lower side, should be checked first but probably fails.

**Q3 strips: status after Q3SB (`AN03_Q3_strip_budgets_v1`, Oct 23) and revised route.**
- *Proved:*
  - **The pre-entry cross residual,** $\sup_{[0,t_0]}(\|e_1\|_{P_2}+\|e_2\|_{P_1})\le C_{\rm pre}q$. It follows from OWPT's mass bound on $[0,t_m]$, and on $[t_m,t_0]$ from MOMC's chart, its $\int M\le3/2$, and its left mass $\le Cq^2\ell^2M$.
  - **The pre-entry gate budget,** $\sup+\int_0^{t_0}(|c|+N_-)=O(q^u+q^2\ell^2)$.
  - **The regularized envelope** from the π axis, $N(t)\le\min\{2,C_{\rm env}(N(0)+q)e^{\beta I_{\rm tot}/2}\}$.
  - **The total clock,** $e^{I_{\rm tot}(t_*)}\le CE_gA_q^{-q^2}q^{-10-10q^2}$.
  - **A frozen substrip** $F_q\subset\mathcal S_{3\pi/2}$, with $\int\mu_{F_q}/q=O(q^{10}\ell^{3/2})$.
- *Refuted (premises from my prompt; ledger 20):*
  - **The unregularized gain** $m\le Cm(0)\max\{1,CN(0)^2e^{\beta I}\}^{1/\beta}$ fails at $b=\pi$. That label lies in Q2EC's clock cohort and grows by $q^{2-\lambda c_m}\to\infty$ by $t_m$.
  - **Lower-side retention of the whole 3π/2 strip** fails: $b=3\pi/2\equiv-\pi/2$ is MOMC's right-half endpoint and lies in the positive strong chart at $t_0$.
  - **A whole-strip chart extension** fails: $F_q$ stays at angular distance of order one from the strong axis.
- *Unpaid:*
  - before $t_0$, the radial term $\int_{\cos\theta>-c_*}|R_{11}\cos\theta\cos\psi|$ for π-strip labels that leave the π neighborhood;
  - for the joined part of the 3π/2 strip, the arrival-weighted mass–displacement law.
- *Revised route (reviewer proposal, to verify).* Split each strip by its scaled offset s from the boundary (π, resp. 3π/2) into three zones.
  - **Outer zone, $s\ge(1+\epsilon)\Lambda_q$.** GESG's both-gates-closed buffer argument applies, since travel is $O(q^3\ell)\ll w_q$, so these labels are frozen. This covers each strip's outer part, not only $F_q$.
  - **Middle zone, $s_q\le s\le(1+\epsilon)\Lambda_q$ with $s_q\asymp\sqrt{\log\ell/k_G}$.** In the gate layer every term of θ′ and ψ′ carries an explicit factor q:
    - near π: $X_1=qZ$ on $P_2$, $\|e_1\|_{P_2}=O(q)$ (crosspre or the guard), and $\sin\theta,\sin\psi=O(q)$;
    - near 3π/2: $\cos\theta,\cos\psi=O(q)$, $X_2=qZ$ on $P_1$, and $\|e_2\|_{P_1}=O(q)$;
    - times a Hölder gate tail $e^{-k_Gs^2}$.
    So the scaled travel is $\lesssim\ell(1+s)e^{-k_Gs^2}=o(1)$ and the radial rate is $o(1/\ell)$. These labels are frozen in scaled coordinates with mass $q^{10}e^{o(1)}$.
  - **Inner zone, $s<s_q$ (physical width $O(q\sqrt{\log\ell})$).**
    - **π side.** Transfer to the target-only flow at $t_m$ via Q2EC's all-label early comparison, and compute from PROFILE's exact equation with seed regularization $(N(0)+q)$. On $[t_m,t_0]$, use Q2EC/RCET transport or the regularized radial bound while $\cos\theta\le-c_*$, and settle the unpaid radial term. After $t_0$ the regularized absolute gain from $t_0$ holds, since $\int r\le B$ pays the strong diagonal. Expected: $\mu_{\mathcal S_\pi}=O(q^3(\log\ell)^{3/2})$. Alternatively, show the inner zone meets $G_+$'s entry contracts (extending Q2EC's boundary label $b=\pi$) and reassign it.
    - **3π/2 side.** The joined labels continue the right half's endpoint. Compute their target-only state at $t_m$, including mass lag and actual-reference displacement, and transport the charted ones with MOMC.
      - After $t_0$, the λ-rate envelope may be too lossy. A single-receiver version of CLOCK's α-rate shape inequality near the reference would make them cheap.
      - Expected: inner-zone mass $\approx q^3$ and displacement $\ll1$, giving a post-$t_0$ cost of order $q^{1+}$ under the α-rate.
- *Order:* the π strip (one session), then the 3π/2 strip (one or two), then the joint weak-passage assembly.

**Status after PISB (`AN03_pi_strip_budget_v1`, Oct 23).**
- *Proved:*
  - **Outer zones (both strips).** The buffer argument inside $(\pi+w_q,3\pi/2-w_q)$ gives mass $q^{10}e^{O(q^3\ell)}$.
  - **Middle zones (both strips).** Every selected entry retains its gate tail $T(s)=e^{-k_Gs^2}$ (`table`):
    - near π: $|R|\le C_*T\left(\begin{smallmatrix}q^2&q\\q&1\end{smallmatrix}\right)$;
    - near 3π/2: $|R|\le C_*T\left(\begin{smallmatrix}1&q\\q&q^2\end{smallmatrix}\right)$.
    Hence angular speeds are $O(q(1+s)T)$, radial rates $O(q^2(1+s)^2T)$, scaled travel $O((1+s_q)\ell^{-\epsilon})$, and the labels are frozen.
  - **Inner π zone.**
    - *Target-only domination at $t_m$.* $v_q<0$ on $(qa_q,\pi+qs_q]$ and $g_q'=2v_q$, so $\hat\theta(t,b)\ge\hat\theta(t,\pi)$ and $\hat m(t,b)\le\hat m(t,\pi)$. The comparison factor is at most one.
    - *Transfer.* Q2EC's all-label early comparison carries this to the original flow at $t_m$.
    - *Regularized boundary mass.* $\hat m(t_m,\pi)\le C(q^{10}+q^{12-\lambda c_m}+q^{8-c_m+4/\lambda})$.
    - *Coarse bridge.* $(\log m)'\le1+2q^2+4S$ and $\int_{t_m}^{t_0}S\le3/2$, so $e^{t_0-t_m}$ is paid explicitly. This avoids the unpaid pre-entry radial term.
    - *After $t_0$.* Cap-one gain $m\le m(t_0)e^{2B}e^I$.
    - *Result.* Exponents $\delta_1=c_m-k$, $\delta_2=(19\lambda-7)/2\ge411/800$ and $\delta_3=4/\lambda+10\lambda-12$ are all positive.
- *Remaining:* only the 3π/2 inner zone $J_3$. Its consumer is S2CP's raw tail `latestrip` for charted labels, plus the arrival-weighted bound `lateconsumer` for the rest.
- *Why crude bounds fail for $J_3$.* These labels reach the strong chart with per-label mass up to about $q^2$ at $t_0$, and the post-$t_0$ weak gain is of order $q^2\xi^2e^{\beta I}\sim q^{2-k}\xi^2$. The budget therefore depends on the actual correlation between mass and displacement. Uniform bounds such as MOMC's $\max\xi\le Cq^{d/2}$, even after contraction, miss by small powers of q.
- *Proposed route for $J_3$ (reviewer; verify first).*
  - **Time-shift structure.** The aligned target-only flow is a scalar autonomous ODE. On $[3\pi/2-qs_q,3\pi/2]$ followed by $(-\pi/2,qa_q)$, $v_q>0$ (mirror of PISB's sign lemma). So
    - $\hat\theta(t,b)=\hat\theta(t-\tau(b),-\pi/2)$ exactly, with delay $\tau(b)=\int_b^{-\pi/2}d\vartheta/v_q>0$;
    - $\hat m(t,b)\le e^{o(1)}\hat m(t-\tau,-\pi/2)$, and also $\le\hat m(t,-\pi/2)$ by domination.
    The $J_3$ measure per unit delay is $\le Cq\,K(-s(\tau))$, which continues the right half's endpoint density.
  - **Transfer at $t_m$** via Q2EC's all-label early comparison.
  - **Delay classes.**
    - *Charted at $t_m$:* transport by MOMC's chart contraction from $t_m$.
    - *Arriving in $(t_m,t_0]$:* a single-label contraction from arrival. In the strong passage $J_{\rm sh}$ contracts at rate $\ge d-M/2\ge d-1/4>0$; fixed constants suffice (ledger 15). This also yields M-clock contraction $\xi(t_0)\lesssim\xi_{\rm arr}(M_{\rm arr}/M(t_0))^d$.
    - *Arriving after $t_0$, or never:* coarse mass, lower-side no-gain until arrival, then the gain from arrival with $\xi=O(1)$.
  - **Expected structure.** Mass $\propto e^{-T}$ and $\xi\propto e^{dT}$ in the extra delay T, so $J_3$'s tail exponent is $1/d>p=3s^{-1}>2$. The weighted moment converges because $2d<1$; its size is about $q^3\cdot q^{2-k}\xi_0^2$ with endpoint displacement $\xi_0\approx q^{10d-2s}$. This gives $\mu/q$ of order roughly $q^{1/2}$ at $\lambda=169/400$; verify the exact exponents.
- *Then:* the joint weak-passage assembly.

**Status after LSB (`AN03_late_strip_budget_v1`, Oct 27): $J_3$ paid; strips complete.**
- *Proved:*
  - **Time shift.** $v_q>0$ on the layer and on $(-\pi/2,qa_q)$. The aligned target flow from $b\in J_3$ is the endpoint orbit delayed by $T(b)$, with radial prefactor $1\le L\le e^{Cq^2T_{\max}}=e^{o(1)}$, where $T_{\max}$ is polynomial in ℓ. The delay density is $\le CqK(-s_0)$.
  - **Endpoint profile.** $\hat m_*\asymp q^{12}e^t$; the endpoint arrives in the strong chart at $4\ell+O(1)$, after which $a_q-\hat\theta_*/q\asymp q^{-4d}e^{-dt}$.
  - **Single-label chart contraction (new; MOMC's pair proof does not apply verbatim).** On $[-79/51,79/51]^2$ the leading Jacobian has max-norm log-norm $\le-1/200$; the x-row bound reduces to $H(0)<49/200$. The square is invariant, and $\int\xi$ is bounded. The sharper central rate $-d+M/2$ then recovers MOMC's multiplier G up to a fixed factor, for any receiver entering the chart.
  - **Delay split $T_c=(k-7/4)\ell$.**
    - Early labels arrive before $t_0$ with $\xi(t_0)\le CA_q^d(q^{6d}e^{dT}+q^{v+du})$ and mass $\le CA_q^{-1}(q^{c_m}+q^2e^{-T})$.
    - Late labels are paid by mass lag alone, through the coarse consumer $m(t_0)e^{(1+\nu)I}$, including those that never arrive.
  - **Restart.** S2CP's distance and gain restart from the actual arrival with the same constants.
  - **Exponents.** $\delta_B>3/2$, $\delta_L=1/4-\nu k\ge769/4000$, $\delta_E\ge97/40$, $\delta_F\ge9323/13600$. The moment converges because $1-2d(1+\nu)\ge16269/80000$.
- *Reviewer checks.* All of the following were re-derived:
  - the Jacobian, the row sums and $H'(x)=-\rho^5x(R-x)\phi(\rho x)/2$;
  - the conversion $\exp\int(-d+M/2)=G$;
  - the shift and the density;
  - the exponent of $q^{6d}e^{dT}$;
  - the coarse consumer, using $\beta\le1$ and $I(\tau_b)\le I(t)$.

**Joint assembly (next; the weak-passage theorem).**
- *Target.* For $\kappa=10$ and $\rho\in[13/20,7/10]$, from $t_0=t_h$ until $t_b$, the first time $c=c_b$, show $t_b\le t_0+L_T\ell$ with all the conclusions below.
- *Guards, improved together by one first exit,* each with its proved improvement:
  - $Y<K_Y$, $\int r<B$, $E_{G_+}<E_g=2c_b$, cross residual $<M_{\rm res}q$ (LCRC);
  - $E_\Sigma<2C_\Sigma(q^5+q^{\Gamma_\nu}H)$ (S2CP);
  - $\int\epsilon_F<\overline F_F$ (CFA);
  - core chart, $\mu_{\mathcal K}<M_K$ and reference $e<e_*$ (CFA's passage and the $B_s$ identity);
  - $\sup\mu_{\mathcal B}/q<b_B(q)$, with a fixed function such as $b_B=q^{1/10}$. The proved rates are $q^{\Delta_\nu}$ with $\Delta_\nu>3/25$ for the complement, $q^9$ for the Q3 interior, $q^{411/800}$ polylog for the π strip, $q^{769/4000}$ polylog for $J_3$, and frozen-zone rates; all lie below $\tfrac12q^{1/10}$ for small q.
- *Duration.* $c\ge c_{G_+}-|c_\Sigma|-|c_{\mathcal K}|-|c_{\mathcal B}|\ge\tfrac89H_{G_+}-o(1)$ and $H_{G_+}\ge H\ge e^{-D}H_0e^{I}$, with $I'\ge Q(1-c_b)$. Hence $t_b\le t_0+[\log(9c_b/(8H_0))+D+1]/(Q(1-c_b))$, so a fixed $L_T=k/(\lambda_{\min}(1-\bar c))+1$ suffices; $L_T$ enters only vanishing errors.
- *Constant order:* CFA's order, with $b_B$ and $L_T$ fixed at the start.
- *Handoff to S4.* Record the state at $t_b$:
  - core retained ($r_{\mathcal K}=O(q^\chi)$, $e\le3e_*/4$);
  - clock $H(t_b)$ and response $c_b$, with $o(1)$ clock defect;
  - $E_\Sigma$, the complement and the outside budgets;
  - residual bounds.

### S4. Weak return and matching to the leading weak family

**Claim.** The Q2 bulk, which is on the strong side at angle $\approx q^{0.52}$ at κ=10 strong entry (target-only), returns into a bounded weak chart with $u\ge0$. Its evolution there matches a closed leading weak family with $\sqrt{N_0}\,W_p(t_0)\to0$, and its response clock matches the logistic half-mass phase to $o(1)$.

**Observation: most of the geometry is already in BULK Theorem 4.1.** Its ratio $x=qj/z\approx q\cot\theta/\sqrt2$ satisfies $x\le C[q^\eta e^{-b_*\tau/2}+q^2]$. Once $x\lesssim q^2$, $\cot\theta\lesssim q$, so the weak input coordinate $u=(\pi/2-\theta)/q$ is bounded. Labels arriving from the strong side have $\theta<\pi/2$, i.e. $u\ge0$. The output coordinate $v$ is bounded by the same $j$ control. The entry time is $\approx\frac{2(2-\eta)}{b_*}\log(1/q)$.

**What remains.**
- (a) BULK's inputs (S0 and the entry ratios from S1).
- (b) The bounded-chart finite-noise weak field ($O(q^2)$ error).
- (c) Closed-family approximation. Use the fixed bulk cohort; by BULK Corollary 4.2 its relative amplitudes, hence normalized weights, drift only by $e^{O(q^\eta)}$.
- (d) $N\leftrightarrow H\leftrightarrow c$. In the chart $m=U_2^2(1+O(q^2))$, so $N_{\rm cohort}=H_{\rm cohort}(1+O(q^2))$. The logistic law then follows from the response ledger with the $o(1)$ bulk defect.

**Primary-band bookkeeping.**
- **Proved (RCET Theorem 2.1, conditional original flow).** BULK Theorem 4.1 closes with $\eta=0$ when the entry ratio is at most a small constant $C_0$. Keep the guard $x<X=4e^BC_0$, then use the growing margin $a_{\theta,2}/q\ge c\min\{q^{-1},e^{b_*\tau/2}/C_0\}$ in the gate tail. This gives $D_{\rm osc}=O(C_0+q^2\log(1/q))$: bounded, not $o(1)$.
- **Proved (RCET Prop 3.1, comparison scope).** Before chart arrival,
  $$q\cot\widehat\theta(T)\asymp\Big[q^\gamma\,\frac{s_0+q}{c_0+q}\Big]^{(1-\lambda)/\lambda}.$$
  This reduces to $(q^\gamma/c_0)^{(1-\lambda)/\lambda}$ when $c_0\gg q$ and $s_0\asymp1$, in particular at the threshold. At $\alpha=\pi$ there is an extra factor $q^{(1-\lambda)/\lambda}$; the v1 unregularized formula is not uniform over Q2. Q2 splits at $c_0\asymp q^\gamma$:
  - labels with $c_0\ge K(C_0)q^\gamma$ have $q\hat j/\hat z\le C_0$ and are $\eta=0$ transported once entry is transferred (S1), giving $E\le CH_{\mathcal C_q}$ through the entry ratio;
  - labels with $c_0<K(C_0)q^\gamma$ are in the chart with displacement $\le Z(C_0)$. A displacement cap alone does not supply BULK Prop 5.2's distance envelope or capped gain.
- Keep $\mathcal C_q$ ($\eta=1/8$, $o(1)$ defect) as the clock, because phase matching for A-error-transfer needs $o(1)$; use $\eta=0$ only for transport (and in S0 Route 3, where bounded distortion suffices).

### S5. Finite-noise matching on compact windows (AN7)

**Claim.**
- **A-error-transfer:** $\sup_{\rho,\zeta,s\in K}|q^{-2}(E_{q,S_0}(\tau_h+s,\xi_q)-\tfrac12)-\mathcal E_{\rho,\zeta}(s)|\to0$ on every fixed centered window $K$, including background and outside labels.
- **A-rate-transfer:** on WIT's gate-separated windows, either uniform convergence or explicit errors below the source and total-rate margins.
- **Clock:** $o(1)$ phase match between the response clock and the leading half-mass clock (S4(d)).
- **Q3/background:** a mass budget. Initial Q3 is $O(S_0)$ before leakage; labels near $\pi$ and $3\pi/2$ leak out and must be followed.
- **Probe-gate strips.**

**Unlocks.** Theorem A by WIT + LPR; initialized persistence by LP's diagonal argument with no further limiting work.

### S6. The exact finite-noise lag (AN1)

**Claim.** The original-flow help channel $D_1^{\rm phys}/(\mu_1^2q^2)=-\tfrac12A_{q,\xi}L^{\rm mean}_{1,q}+\text{remainder}$, with the remainder smaller than the lag's signed margin on the learned windows, and a positive-lag estimate for the exact lag.

**Route.** Start from the exact Stein relation and P's lag-tracking identity. Transfer the leading positive-lag forcing (symmetrized $\Xi>0$) with remainders measured relative to the lag, not in absolute $O(q^2)$, since the lag is a small cancellation at canonical noise.

**Unlocks.** B-core in the original flow: help = exposure × signed exact lag, harm = producer-attributed input rotation.

### Deliverable of S0–S6

Initialized Theorem A and the original-flow B-core on a joint family around $S_0\approx q^{10}$, $\rho\in[13/20,7/10]$, together with growing-window persistence. This is an asymptotic theorem. It does not cover the canonical run (Section 5).

---

## 5. The regime gap: explaining the canonical mechanism

### 5.1 The gap

The canonical run has $2<\kappa<3$ (Section 2.3), while the theorem targets κ=10. At the level of exponents:

- **Entry geometry differs.** For $\kappa<2/\lambda$, bulk Q2 ancestry is still **left-facing** at strong entry, with $\theta-\pi/2\asymp q^{\kappa\lambda/2}$. So the weak seed enters the weak chart from the Q2 side ($u<0$), after strong saturation removes the cluster-1 leakage that drove crossing. The κ=10 transit-and-return route does not apply.
- **The shape is non-small.** $E_{\rm loc}(\kappa)<0$ for $\kappa<2s/(1-P)$, and $2s/(1-P)>5>3$ on the box **[rational]**. With the candidate entry exponents, the local passage multiplier therefore drives the strong spread to $O(1)$ before weak half-mass. **This is a non-small bridge**, consistent with E5.

### 5.2 Unifying interpretation

The leading population system is the single analytic object. With a small-shape entry it produces the coherent reversal (the theorem regime). With an $O(1)$-shape entry it produces a split strong family with an inactive bridge (the canonical regime). The sign of $E_{\rm loc}(\kappa)$ is the exponent-level boundary between the two. This should be stated as a **regime map**: exponent comparisons that identify which mechanism applies, not a claim about constants at $q=0.05$.

### 5.3 Remaining steps for the canonical mechanism

**S7. Non-small bridge comparison (AN4).**

*Claim.* A non-perturbative coupled estimate for the active core, the inactive bridge, the weak residual producer, the exact lag, and the exposure, giving the source signs and a quantitative depth comparison with the coherent orbit.

*Tools in hand.* The partial-active error formula $\mathcal E_\zeta=\tfrac12A_\zeta^2-\zeta A_\zeta+h(L_0-K_w-Y_B)-M_AC_A$; the instantaneous bridge forcing signs (`pa:bridge-force`); same-field cooperativity.

*Suggested route: a quantile formulation.* The target-only entry state is co-ordered (labels are ordered by initial angle, and $x=y$ in the aligned comparison). Same-field cooperativity, $\partial_yx'=\partial_xy'\ge0$, preserves co-ordering within the population (`pa:order`). So the strong family stays a **monotone curve** parameterized by entry rank $\sigma\in[0,1]$, with $x(\sigma,t)$ and $y(\sigma,t)$ nondecreasing in $\sigma$. Its donor field ($\mathcal S$, $Y$, $A_\zeta$, $B_\zeta$) is then a functional of two monotone functions. This turns AN4 into a one-dimensional nonlocal transport problem with monotone structure, where exposure, compensation and bridge mass are quantile integrals.

*Caution.* Cross-population comparison is still invalid (donor couplings are negative). The monotone structure is used *within* one population.

**S8. Canonical-regime entry.**

*Claims.*
- (a) A left-facing weak seed. Q2 localized tracking (Q2 Theorem 5.2) supplies the conditional tool; its full-output defect integral must be bounded through strong learning.
- (b) Entry into the weak chart from $u<0$.
- (c) A split-population entry state for S7.

*Analytic note for (b).* On $u<0$ with $Y\ge0$, $(u+Y)\phi(u)\ge u\phi(u)\ge-\phi(1)$, so
$$\partial_uu'\le-\tfrac12[\lambda(1-N)-\phi(1)],\qquad \lambda\ge169/400>1/4>\phi(1).$$
On $[-Y,0]$ the full rate $\lambda(1-N)/2$ holds. So WEAK's contraction extends to $u\ge-Y$ unchanged, and to all $u<0$ at a reduced rate. The rate loss accrues only while a label is below $-Y$.

**S9. Canonical-parameter coverage (optional, analytic only).** A theorem for "sufficiently small $q,S_0$" says nothing at $q=0.05$ unless every constant is explicit. Explicit analytic constants are allowed, but current sufficient conditions are far from $q=0.05$ (e.g. WIT's $q\le\sigma/(100R)$). The realistic claim is: an asymptotic theorem, plus the regime map, plus the canonical run as empirical evidence in the predicted bridge regime.

---

## 6. Numerical statements currently in the narrative, and their analytic status

| Statement | Status | Analytic action |
|---|---|---|
| $E_{\rm loc}$ root ≈6.5, $pE$ root ≈8.7 at $\rho=2/3$ | **[eval]** | Use only through rational bounds; κ=10 margins and canonical $E_{\rm loc}<0$ are already **[rational]** |
| κ ≈ 2.84 at canonical | **[eval]** | Use $2<\kappa<3$ **[rational]** |
| Crossover delay ≈1.10 physical | **[eval]** of the selected orbit | Existence and a quarter-mass descent bound are analytic; a two-sided timing bound would need WIT-style invariant regions past half-mass (optional) |
| $\kappa_{\rm enh}\approx1.75053$ | **[eval]** of a response functional | Analytic sign is open (AN9, optional) |
| Frozen saddle-node $M\approx0.4768$ | **[eval]** | Not needed by any theorem |
| Seed exponent ≈0.576 | Empirical | Proved: lower laws only (ARR $S_0^{17/16}$; conditional amplitude $S_0^{1-\lambda}$) |
| Mechanism attribution fractions (95%, 99.5%) | Empirical | Replaced by exact source/producer identities |
| Earlier spot values for $r_m$ across ρ | Superseded | TAILREP proves the uniform κ=10 margin by combining exponents first |
| WIT window widths and margins | Analytic orbit functionals, unevaluated | Allowed as is |

---

## 7. Suggested work plan

Tracks that can run in parallel:

| Track | Steps | Notes |
|---|---|---|
| I | S1 strong-stage tracking | Bottleneck for Theorem A. Steps 1–2a done unconditionally (OWPT, MOMC; SMCP records the fixed-offset obstruction). Steps 6–7 done (Q2EP, Q2EC, SEP). **S1's entry contracts are complete.** $B_s$, core retention and $\mu_B$ move to the weak-passage bootstrap (S2/S3). |
| II | S2 capped gain + S3 field contract | Mutually dependent (ledger 16). CFR has proved the primary and radial parts of S3. DECG has proved the chart envelope, the radial bound and the conditional gain. GESG has proved the global envelope and the Q3 interior. **S2CP closes S2 and CFA closes S3, both in stopped-guard form, with a conditional CLOCK passage.** Only the Q3 strip budget remains external. Q3SB proved the pre-entry inputs, PISB paid the π strip and the frozen zones, and **LSB paid $J_3$; the strips are complete**. No external input remains. Next: the joint weak-passage assembly, which produces the weak-passage theorem. |
| III | S0 + S4 weak return/matching | S0 closed conditionally (RCET + LCRC); $\eta=0$ variant and dichotomy done. S4 is now mostly bookkeeping on top of BULK Theorem 4.1 and LCRC. |
| IV | S6 exact lag | Independent; needed for B-core. |
| V | S7 + S8 bridge and canonical entry | Bottleneck for explaining the empirics. Start with the quantile formulation. |
| — | S5 AN7 | Assembles I–IV. Error transfer on every fixed window, not only the crossing windows. |

**Dependency sketch**

```text
S0 ──┐
S1 ──┼──> S2, S3 ──> c-passage (CLOCK) ──┐
     └──> S4 (BULK bootstrap) ──> selection (WEAK/TAILREP) ──┤
S6 ──────────────────────────────────────────────────────────┼──> S5 (AN7) ──> Theorem A, B-core, persistence
S8 ──> S7 (AN4) ──> B-bridge, canonical mechanism ───────────┘ (regime map links the two)
```

**Paper-level milestones**

1. **Deep-regime paper core.** Initialized Theorem A and B-core at $S_0\approx q^{10}$, $\rho\in[13/20,7/10]$; persistence corollary; linear contrast; limiting mechanism.
2. **Regime map.** Analytic exponent statements ($E_{\rm loc}$, $pE$, $\gamma_\kappa$, target-only timing thresholds) identifying the coherent and bridge regimes, with the canonical run placed in the bridge regime by rational inequalities.
3. **B-bridge.** AN4 and canonical-regime entry, or an explicit statement that they remain open, with the canonical depth enhancement marked empirical.

---

## 8. Carry-forward ledger: withdrawn claims and invalid shortcuts

H2 §13 remains in force. Additional items from the October 3–6 increments and reviews:

1. **Withdrawn:** using the whole Q2 cohort as the amplitude clock. Its strong-captured strip makes the subinterval defect of order $(\kappa(1-\lambda)-5)\log(1/q)$ in the frozen-floor picture. Use a bulk subcohort; the clock $I=Q\int(1-c)$ is cohort-independent.
2. **Withdrawn:** a raw future target $J_{Q2}\lesssim q^3$ through weak learning. The correct allowance is $J\lesssim q^3+q^2H$ (weak-chart regeneration); the forcing estimate is unchanged.
3. **Withdrawn:** the "opposite-corner" κ≈15 estimate. $A$ and $R$ both decrease in $\lambda,P$; bound $\min\{A,A-R\}$ first.
4. **Withdrawn:** "Q2 labels near $\pi$ cross arbitrarily late" at fixed $q$. Target-only crossing is uniform, with maximum $(4/\lambda)\log(1/q)+O(1)$.
5. **Invalid:** putting the secondary Q2 tail into the mass-charged moment lemma. Its index $p_2<1$; it belongs in the explicit-output ledger, where its cost is $q^{\Gamma_\nu}H$.
6. **Invalid:** freezing labels uncrossed at $t_0$ and keeping their before-crossing mass bound afterwards, or selecting "currently crossed" labels without flux.
7. **Invalid:** inferring a transport bound from clock-cohort membership. Membership in $H_C$ or $c$ does not remove a label's transverse output or selected-residual contribution.
8. **Invalid:** treating an upper growth bound as proof that labels outside the safe core escape. The complement is charged as potentially adverse, with no lower escape claim.
9. **Withdrawn (roadmap v1, S0):** "$\mathfrak F\lesssim H_b+L\sqrt{qH_b}+q^3$, so the residual constant $L$ has a fixed point for small $q$." The regenerated transverse energy gives $\mathfrak F\lesssim q^3+H+\sqrt{qH}+LH+L^2q^2H$. The $CLH_b$ term is not absorbed by small $q$, and the balanced donor $U=W=(qL\sqrt E,\sqrt E)$ shows the $LE$ scale is real (RCET). Use the Volterra form instead.
10. **Domain correction:** the two-sided formula $q\cot\widehat\theta(T)\asymp(q^\gamma/c_0)^{(1-\lambda)/\lambda}$ holds only for $c_0\gg q$, $s_0\asymp1$. Use RCET's $(c_0+q)$, $(s_0+q)$ regularized form over all of Q2.
11. **Invalid:** inferring $H(t_*)\lesssim H_b$ at an interior first-exit time from the terminal cap $H(t_b)\le H_b$ without clock control on $[t_*,t_b]$ (RCET's scalar counterexample).
12. **Invalid:** a uniform-over-labels strong shape transfer by the *linear* $M$-clock multiplier from a fixed overlap offset $C_m$. Outer labels with $h\asymp e^{-dC_m}$ pick up a nonvanishing convex correction (SMCP Theorem 2.1; leading-field persistence in SMCP Prop 3.1). Use a moving overlap $C_m(q)\to\infty$ or a nonlinear same-field comparison.
13. **Withdrawn (SMCP prompt):** "the leading strong center moves with $M$ and equals $a_q$ at $M=0$." At $N=0$ the leading coherent center is stationary at $(a_\rho,a_\rho)$ for every $M$.
14. **Correction:** the overlap handoff is $\epsilon_mM_0^d=A_q^dq^{10d-s}$ with an order-one $A_q\in[c,C]$, not exactly $q^{10d-s}$. The half-mass clock carries the shift $-\log A_q$.
15. **Invalid (Q2EP prompt):** an $e^{o(1)}$ universal angular factor for Q2 labels at a fixed threshold. The strong cross drive $-Ma_\rho/2$ gives a relative correction $\Theta(Ma_\rho/x)$ (Q2EP Prop 4.1).
    - *General rule for contracts:* request $e^{o(1)}$ accuracy only where the consumer needs it, i.e. the response-clock phase and core shape transfer. Q2 entry ratios, signs and seeds are fixed-constant contracts, and $e^{O(C_0)}$ is acceptable there.
    - SMCP (item 12) was the same overreach.
16. **Sequencing error (CFR prompt):** S3's refined route charged Σ through $E_\Sigma\le C(q^5+q^{\Gamma_\nu}H)$. That bound is LCRC's `secondary` lemma, which itself assumes the S2 distance and gain contracts. So S3 cannot close before S2.
    - *Outside budget.* The c-form remainder needs $\int\mu_{\mathcal B}/q$ small. LCRC's retained $\sup\mu_{\mathcal B}/q=o(1)$ does not give this on a logarithmic interval: $\mu/q=\ell^{-1/2}$ over length ℓ integrates to $\sqrt\ell$. LCRC itself needs only the supremum.
    - *Consequence.* S2 and S3 are mutually dependent and must close in one joint stopped bootstrap (see S2).
17. **Over-restricted contract (DECG prompt):** two restrictions in the S2a prompt were not needed.
    - *The c-form chart was fixed before the guards.* Only R, $M_{\mathcal K}$, $B_s$ and $c_b$ must be guard-independent, and chart-dependent constants multiply only $C_0$ or powers of q.
    - *A pair comparison off the chart.* Once the reference is $O(q)$ away, a global bound that uses only matrix values suffices (S2 update after DECG).
    - DECG's off-chart stop and its Q3 estimate both follow from these restrictions, plus applying the generic gain to lower-side labels. *Rule:* fix a constant before the guards only when it enters an order-one LCRC constant.
    - *My first v1.10 repair sketch was also wrong, and was corrected the same day.*
      - The single-label $\log\tan\theta$ bound with good and bad periods hid the gate-layer excess: the gate tail enters $\theta'$ multiplied by $\sin\psi$, not $\sin\theta$. This is DECG's obstruction, which the signed-cancellation bound now targets.
      - The sketch's Q3 sentence missed the 3π/2 side. It also treated the π strip as leakage, but it belongs to the weak family.
18. **Wrong budget sources (GESG prompt).**
    - I pointed $\int c$ at CLOCK's passage budget $\int f_*\le F_b$. That is a *hypothesis* of the passage theorem, not a stopped guard.
    - I pointed $\int N_-$ at CFR's negative-part bound. That bound concerns $K_O$, a $P_1$ moment of output 2, which is a different quantity.
    - GESG correctly refused both. The proved sources are LCRC's backward clock (for $\int c$) and GESG's cohort charge (for $N_-$).
    - The pointwise cap $N_-\le Q(1-2c)$ I proposed was unnecessary.
    - *Rule:* before naming a budget source in a prompt, check that it is a proved conclusion under the current guards, not a hypothesis of a later theorem.
19. **Coefficient and order slips (S2CP prompt).** S2CP corrected both.
    - The v1.11 side benefit wrote $\int c\le\tfrac{10e}9E_g/(1-c_b)$. Dividing the $\int Qc$ budget gives $\tfrac{10e}9E_g/(Q(1-c_b))$. The $O(c_b)$ conclusion survives, since $Q\ge169/400$.
    - The suggested order put $C_\Sigma$ before $C_0$. SEP's cap and tail constants depend on $K(C_0)$, so $C_\Sigma$ must come after them. This is acyclic, because $C_\Sigma$ enters the gate only at vanishing scales.
20. **False premises (Q3SB prompt).**
    - *The unregularized gain.* I proposed $m\le Cm(0)\max\{1,CN(0)^2e^{\beta I}\}^{1/\beta}$ and dropped the additive seed. GESG's own Duhamel exhibits that seed, and RCET's $(s_0+q)$ regularization signals it. The bound fails at $b=\pi$, which grows by $q^{2-\lambda c_m}$. The correct form uses $(N(0)+q)^2$, and my expected order $q^3\ell^{3/2}$ had implicitly used it.
    - *Whole-strip contracts.* I proposed lower-side retention, then a whole-strip chart extension, for the 3π/2 strip. Both fail because the strip contains both a joined endpoint ($b=-\pi/2\in\mathcal R$) and a frozen substrip.
    - *Rules:*
      - near a boundary or separatrix, include the regularization seed and check the endpoint label explicitly;
      - before extending a family contract to a boundary layer, split the layer into frozen, transitional and joined parts.

---

## 9. File map (current increments)

| Key | File |
|---|---|
| H2 | `THEORY_HANDOFF_ANALYTICAL_A_B_v2.md` (+ changelog) |
| F | `RELU_POPULATION_FOUNDATIONS_v2.tex` |
| P | `THEOREM_A_ANALYTICAL_PROGRESS.tex` (checkpoint 1.0) |
| ARR | `AN02_weak_side_arrival_v1.tex` |
| TAIL | `AN02_strong_ancestry_and_tail_transport_v1.tex` |
| Q2 | `AN02_Q2_profiles_and_localized_tracking_v1.tex` |
| PROFILE | `AN02_strong_entry_profile_and_tail_budget_v1.tex` (+ review) |
| Q2E | `AN02_Q2_boundary_layers_and_cohort_energy_v1.tex` (+ review) |
| RET2 | `AN03_two_sided_passage_and_Q2_retention_v2.tex` |
| LOC | `AN03_local_rate_mean_tracking_v1.tex` |
| CLOCK | `AN03_exact_amplitude_clock_and_c_passage_v1.tex` (+ review) |
| WEAK | `AN03_weak_transit_forcing_and_orbit_selection_v1.tex` (+ review) |
| TAILREP | `AN03_mass_charged_tail_and_selection_defects_v1.tex` (+ review) |
| BULK | `AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` (+ review) |
| RCET | `AN03_residual_closure_and_eta0_transport_v1.tex` (+ review), prefix `an03rcetv1:` |
| LCRC | `AN03_ledger_cap_residual_closure_v1.tex` (+ review), prefix `an03lcrcv1:` |
| OWPT | `AN02_overlap_window_profile_transfer_v1.tex` (+ review), prefix `an02owptv1:` |
| SMCP | `AN02_strong_M_clock_passage_v1.tex` (+ review), prefix `an02smcpv1:` — obstruction increment |
| MOMC | `AN02_moving_overlap_M_clock_passage_v1.tex` (+ review), prefix `an02momcv1:` |
| Q2EP | `AN02_Q2_entry_through_strong_passage_v1.tex` (+ review), prefix `an02q2epv1:` — part (e) proved; obstruction to the $e^{o(1)}$ form |
| Q2EC | `AN02_Q2_entry_contracts_v1.tex` (+ review), prefix `an02q2ecv1:` |
| SEP | `AN02_secondary_entry_profile_v1.tex` (+ review), prefix `an02sepv1:` |
| CFR | `AN03_c_form_field_reduction_v1.tex` (+ review), prefix `an03cfrv1:` — partial; stops at the S2 dependency |
| DECG | `AN03_distance_envelope_and_capped_gain_v1.tex` (+ review), prefix `an03decgv1:` — partial; stops at the off-chart envelope |
| GESG | `AN03_global_envelope_signed_gate_v1.tex` (+ review), prefix `an03gesgv1:` — partial; stops at the integrated gate budget, which the review resolves via LCRC's backward clock |
| S2CP | `AN03_S2_closure_package_v1.tex` (+ review), prefix `an03s2cpv1:` — S2 closed in stopped-guard form; $\mathcal U_\Sigma$ and $B_s$ paid; retained-input audit |
| CFA | `AN03_c_form_assembly_v1.tex` (+ review), prefix `an03cfav1:` — S3 closed in stopped-guard form; core-only c-form, full remainder, CLOCK forcing, conditional passage |
| Q3SB | `AN03_Q3_strip_budgets_v1.tex` (+ review), prefix `an03q3sbv1:` — partial; pre-entry cross residual and gate budget, regularized envelope, total clock, frozen 3π/2 substrip; refutes three proposed premises |
| PISB | `AN03_pi_strip_budget_v1.tex` (+ review), prefix `an03pisbv1:` — π strip paid; outer and middle zones of both strips frozen and paid; $J_3$ consumer recorded |
| LSB | `AN03_late_strip_budget_v1.tex` (+ review), prefix `an03lsbv1:` — $J_3$ paid via time shift, single-label chart contraction and delay split; strips complete |
| SGWR | `SIGNED_GROWTH_WEAK_RETENTION_v1.tex` |
| WIT | `AN06_learned_orbit_witnesses_v2.tex` |
| LP | `LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex` |
| LPR | `LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex` |
| Support | `SCALED_POPULATION_SPLITTING_THEORY.md`, `TWO_NEURON_SMALL_NOISE_LIMIT.md`, `LEAK_COMPENSATION_FACTORIZATION_AUDIT.md`, `SIM.md`, `main-15.tex`, frozen appendix, `theorem_A_initialized_escape.pdf` (Sections 1–3 only) |

**Workflow.** Each new result goes in a separate versioned `.tex` with a same-stem review note. Nothing is merged into the checkpoint without explicit approval. GitHub is read-only, and only when the user asks; Tod makes all commits. No new experiments by default, no computer-assisted certificates.