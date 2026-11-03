# Roadmap to a unified analytic theory of the ReLU SIM reversal mechanism

**Version 1.29 — November 2, 2026.** Working roadmap, not a proof and not a merge instruction. No source increment, foundations file, or checkpoint is modified by this document. It supersedes the "recommended next task" parts of `THEORY_HANDOFF_ANALYTICAL_A_B_v2.md` (H2) only where explicitly stated; H2's ground rules, file contracts, and withdrawn-claims ledger remain in force.

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

**Revision 1.17 (Oct 28).** Records WPT (`AN03_weak_passage_theorem_v1`).
- Every non-response guard improves on one joint stopped interval. This yields a **two-boundary theorem:** all assembled estimates hold until c first hits 0 or $c_b$, and one of the two is hit within $20\ell$.
- The single remaining gap is **the lower response barrier** $c\ge0$. Every source assumes it, and none proves it. My v1.16 claim that no input remained was wrong (ledger 21).
- WPT also corrects my hitting-time formula: the denominator is Q, not $Q(1-c_b)$.
- Next: a signed response-barrier lemma, which completes the weak-passage theorem.

**Revision 1.18 (Oct 28).** Records RB (`AN03_response_barrier_v1`): **the deep-regime weak-passage theorem is complete.**
- **Barrier:** $c\ge\tfrac{\kappa_0}2q^2\mu_{\mathcal K}+\tfrac12H_{G_+}>0$, with $\kappa_0=351/102400$, so $\tau=t_b$.
- **Terminal amplitude and time:** $H(t_b)\asymp c_b$ and $t_b-t_0=[\log(c_b/H_0)+O(1)]/Q$.
- **Next: S4,** revised to run the selection stage inside the passage interval.

**Revision 1.19 (Oct 28).** Records SI (`AN03_selection_interface_v1`, S4a): partial.
- **Proved:** the full TAILREP/WEAK hypothesis inventory with exact constants; core donor moments; BULK's bound in weak coordinates ($|u|+|v|\le C_h(1+q^{-p_b})$ at a fixed clock level); the growing-chart mass relation; and the logistic phase identity.
- **Stops at the original weak input return.** The boundary margin needs a signed weak-receiver computation. Norm bounds and BULK's ratio give size only.
- **Corrects my S4 picture (ledger 22):**
  - BULK gives size, not sign;
  - the bounded weak chart is never reached inside the passage;
  - $N_C=H_C(1+O(q^2))$ holds only on a bounded chart;
  - $n_b\le c_b/2$ does not place a hit before $t_b$;
  - the phase needs $\int(N-c)\to0$.
- **Next:** S4 is split into S4b–S4d. S4b is the weak-receiver boundary field and input return.

**Revision 1.20 (Oct 30).** Records WBR (`AN03_weak_boundary_return_v1`, S4b): **closed.**
- **Return.** Every label of the clock cohort keeps $u>0$ from $t_0$ up to a fixed clock level, with a uniform strict inward margin $g_0/4$ at the boundary.
- **New pointwise tools:** exact boundary moments; an energy bound on the weak feedback; a strong-mass relaxation rate; and $O(q)$ clock alignment.
- **New obligations, found in this review:**
  - the selected cohort must carry all but $o(H)$ of the weak mass and response;
  - WBR does not supply $A_0\to0$.
- **Next:** S4c, the matching package. S4d (field reductions and selection) follows.

**Revision 1.21 (Oct 30).** Records MP (`AN03_matching_package_v1`, S4c): **closed.**
- **Population accounting.** The omitted primary band is $\asymp q^{1/4}$ of H.
- **Response:** $c=H(1+O(q^{1/4}))+O(q^2)$.
- **Phase:** uniform $o(1)$ logistic phase, and $\int|N-c|=o(1)$.
- **Transverse energy and smallness:** $J_S\le C(q^3+q^2H)$, so $A_0=O(q^{1/16})$ with $p=2$.
- **Mass defects:** late budgets, pointwise and integrated.
- **Remaining S4:**
  - **S4d**, the strong-reference reduction and the local guard;
  - **S4e**, the weak-chart reduction and the selection theorem.

**Revision 1.22 (Oct 31).** Records SRR (`AN03_strong_reference_reduction_v1`, S4d): **closed.**
- **Strong error form.** On $[t_s,t_n]$, up to the first exit from $E_s<\delta$, CFA's actual reference satisfies TAILREP's `strongerror` with $g=g_W=\gamma/2$, the model-only $C_s=980$, and a pointwise $d_0^{(s)}=O(q^{1/20})$.
- **Initial error.** $E_0=O(q^{1/20})$. It comes from CFA `localineq` (rate $g_c=\gamma_*/2$) on $[t_0,t_s]$; WEAK's box and rate are used only after $t_s$.
- **Fixed for S4e:** $W_2$ under the fixed incoming law $\eta_s$; the weight value conversion $\omega=1+o(1)$; an explicit δ and a new upper bound on h.
- **Reviewer corrections:** ledger 23 (the S4d prompt's regime-crossing errors, found in my audit), 24 (a coefficient slip in my corrected prompt, caught by SRR) and 25 (eaten TeX escapes in SRR and five committed increments; typesetting only).
- **Next: S4e,** the weak-chart reduction and selection at a fixed level $n<h$.

**Revision 1.23 (Nov 2).** Records WCS (`AN03_weak_chart_selection_v1`, S4e): **closed. S4 is complete.**
- **Weak error form.** On $[t_s,t_n]$, up to the strong first exit, the fixed-incoming-law $W_2$ satisfies TAILREP's `weakerror` with $C_w=20$, a pointwise $d_0^{(w)}=O(q^{1/20})$, and $\int\ell_B=o(1)$ uniformly in the level, so $L_*=1$.
- **Selection.** With the explicit level $n=\tfrac12\min\{h,\tfrac14,\lambda_{\min}g_{\min}/(64C_sB_{\max}C_w)\}$, all of TAILREP `selection`'s hypotheses are discharged: $E_s(t_n)+W_2(t_n)=O_n(q^{1/20})$.
- **Meaning.** The initialized original flow reaches a fixed small weak mass with its strong reference and selected weak cohort close to the selected coherent orbit (weak part in $L^2$ of the incoming law), and with an $o(1)$ actual-clock phase.
- **Reviewer additions:** ledger 26 (an integration-by-parts instruction in my S4e prompt that was not valid away from $u=0$), and an S5 plan that starts with an interface and probe-precision audit (S5a; two risks recorded in S5).
- **Next: S5a.**

**Revision 1.24 (Nov 2).** Records CWI (`AN07_compact_window_interface_v1`, S5a): **audit complete; leading extension closed.**
- **Interface and clock.** Every consumer hypothesis is inventoried. The centering $\tau_h=t_n+\lambda^{-1}\log((1-n)/n)$ is admissible, and $\tau=\mu_1^2t_{\rm phys}$.
- **Exact precision criterion.** $E-E^{\mathcal K}=o(q^2)\iff\mathcal Q_{\Sigma\cup\mathcal B}=o(q^2)$, where $\mathcal Q_T=\int_Tm[\sin(q\zeta-\theta)]_+^2$. The core's static error and source rates at entry are paid.
- **Unpaid at entry:** Σ's lower-half slice, the strong complement, the inner π strip and $J_3$. The existing tail majorant fails ($\Xi_\nu\le915/604<2$ at $\lambda=49/100$).
- **Leading extension.** WIT's transfer, rate and propagation results hold with strong-only compact support and finite weak first moments, with unchanged constants.
- **Reviewer additions:**
  - ledger 27 (four errors in my S5a prompt and the v1.23 plan);
  - a proposed lower-half transverse-energy route that would pay every unpaid cohort at once;
  - the S5 sessions reordered so that probe precision comes before continuation.
- **Next: S5b,** probe-sector energy and entry precision.

**Revision 1.25 (Nov 2).** Records PSE (`AN07_probe_sector_energy_v1`, S5b): **closed.**
- **Lower-half energy.** For every fixed cohort, $\mathfrak E_T(t)\le e^{31}\mathfrak E_T(0)+31e^{31}C_Eq^2L^2\sup\mu_T$ on $[0,t_b]$, with $L=1+\log(1/q)$.
- **Cohort masses before entry.** A new backward radial comparison gives $m(t)\le e^5m(t_0)$ for $t\le t_0$.
- **Background paid.** $\mathcal Q_{\Sigma\cup\mathcal B}\le Cq^2(q^8+L^2q^{\gamma_*})$, so the full probe error and source rates equal the core's own to $o(q^2)$ throughout $[t_s,t_b]$.
- **Entry comparison.** The initialized probe error and source rates match the selected orbit at every fixed level $n'$ in a compact subset of $(0,n]$, with error $O(q^{1/20})$. Consequently A-error-transfer already holds on every fixed window inside $(-\infty,s_n]$ (reviewer corollary).
- **Continuation criterion.** An explicit conditional energy inequality lists what S5c must continue past $t_b$.
- **Reviewer additions:** the reviewer's proposed route (v1.24) is now proved as stated. Ledger 25 gains six more garbled-escape locations (a dropped `\q` in `\quad`) and a scan for them.
- **Next: S5c,** finite-window continuation and A-error-transfer after entry.

**Revision 1.26 (Nov 2).** Records FWC (`AN07_finite_window_continuation_v1`, S5c): **closed. A-error-transfer holds on every fixed centered window.**
- **Continuation without the passage guards.** A combined transverse energy $\mathcal Z=E_{\mathcal K}+J_G$ propagates the cross residuals for any fixed time from the state at $t_n$. From it follow the alignment, the bounded core chart, the reached weak chart, primary probe inactivity and the physical mass laws. No small $c_b$ or $E_g$ guard is continued.
- **Reduction and propagation.** The original-to-leading reduction errors (core by source, selected weak by value, reactions weighted by distance) are $O(q^{1/10})$ in the first-moment norm. CWI's propagation therefore holds for the original flow: $\mathfrak d=O_T(q^{1/20})$ on $[s_n,T]$.
- **A-error-transfer.** $\sup|q^{-2}(E_{\xi_q}(\tau_h+s)-\tfrac12)-\mathcal E_{\rho,\zeta}(s)|\le C_Tq^{1/20}$, uniformly over the deep box and every bounded nonnegative offset range. This is H2's A-error-transfer on every fixed window and LP's `compact-transfer` premise.
- **Reviewer additions:**
  - ledger 28 (my S5c prompt's suggested continuation order was circular);
  - the observation that the reversal itself (rebound and the ordered integrated error change) now follows from A-error-transfer plus WIT, while the source signs $D_1<0<D_2$ need A-rate-transfer.
- **Next: S5d,** A-rate-transfer on WIT's learned windows and the AN8 assembly (Theorem A and persistence).

**Revision 1.27 (Nov 2).** Records RTA (`AN07_rate_transfer_and_assembly_v1`, S5d): **closed. Initialized Theorem A and initialized persistence are proved in the deep regime.**
- **Family.** Aligned-balanced isotropic initialization with $S_0=q^{10}$, $0<q\le q_0$ (an analytic, unevaluated $q_0$), and $(\rho,\zeta)$ in WIT's rectangle $\mathcal P_*$ around $(2/3,5\pi/9)$.
- **Theorem A** (`theoremA`):
  - responses $\mathsf m_1\ge1/2$, $\mathsf m_2\ge1/4$, and exact cluster losses $\mathcal L_p\le(169/196)\mathcal L_p(0)$;
  - source signs $D_1^\tau\le-p_*q^2/2<0<p_*q^2/2\le D_2^\tau$ on J;
  - total rate $\le-5\gamma_0q^2/8$ on $J_-$ and $\ge5\gamma_0q^2/8$ on $J_+$;
  - an interior error minimizer with rebound $\ge\gamma_0rq^2/4$ on both sides;
  - an off-cone sector of width $2\delta_\zeta q$.
- **Persistence** (`persistence`). There are a common $S_{\rm clr}$, a horizon $T_q\to\infty$ and $\varepsilon_q\to0$ with $|E-\tfrac12|\le\varepsilon_qq^2$ on $[S_{\rm clr},S_{\rm clr}+T_q]$. No rate for $T_q$ is given.
- **Not covered:** the original-flow B-core decomposition (S6); the canonical and bridge regimes (S7/S8); a quantitative horizon.
- **Next: S6,** the original-flow B-core on WIT's windows. Before any merge, an independent read of the complete chain is advisable.

**Revision 1.28 (Nov 2).** Records BC (`AN01_original_flow_bcore_v1`, S6 first attempt): **stopped at an obstruction to my prompt's contract, not to B-core.**
- **Obstruction.** P's factorization puts the strong core's cluster-2 **output rotation** into its remainder $r_2$. On WIT's windows, $q^{-2}r_2=\mathcal O_*+O(q^{1/20})$ with $\mathcal O_*=\tfrac\rho2(1-n_\rho)(\zeta-X_*)\mathsf K(\rho X_*)\ge c_{\rm out}>0$. So my prompt's demand that every factorization remainder be $O(q^{2+\kappa})$ is false (ledger 29).
- **Closed two-channel identity.** $q^{-2}D_2^\tau=(X_*-Y_*)x'_{2,*}+\mathcal O_*+O(q^{1/20})$, with input rotation in the first term and output rotation in the second. This agrees with P `pa:atomicrates`, which already states that the second source contains output rotation before weak saturation.
- **Correction to the mechanism statement.** H2's Theorem B item 3 describes cluster-2 harm as input rotation only. At leading order in the deep regime, harm has two channels. The input channel has a weak-produced part $\tfrac\lambda2n(X-Y)(V-Y)\Phi$ and a target-plus-core part $-\tfrac\lambda2(X-Y)^2\Phi\le0$. The output channel has a target part $\tfrac\rho2(\zeta-X)\mathsf K(\rho X)>0$ and a weak-response part $-\tfrac\rho2n(\zeta-X)\mathsf K(\rho X)$. Which part dominates on J is not yet known.
- **Next: S6, revised.** A channel-and-producer decomposition with a signed exact lag.

**Revision 1.29 (Nov 2).** Records CPD (`AN01_channel_producer_decomposition_v1`, S6 revised): **closed subset; one sign open.**
- **Closed on $\mathcal P_*\times J$, all at $O(q^{1/20})$:**
  - the input, output and radial channel limits of both source rates, and every fixed-label producer's contribution to each;
  - the signed exact lag $\mathcal L_q=r_{21}/q=Y+n\mathsf K(U)+O(q^{1/20})$, with $Y+n\mathsf K(U)\ge c_L>0$;
  - help $q^{-2}D_1^\tau=-\tfrac12\mathcal A_q\mathcal L_q+O(q^{1/20})$, with the error below half the margin;
  - the four-part harm identity $q^{-2}D_2^\tau=T_{\rm in}+W_{\rm in}+T_{\rm out}+W_{\rm out}+O(q^{1/20})$, with $T_{\rm in}\le0<T_{\rm out}$ and $W_{\rm out}<0$ on J, and $W_{\rm in}>0$ on $J\cap(-\infty,0]$.
- **Open.** The sign of $W_{\rm in}$ on $J\cap(0,\infty)$. It needs $X>Y$ after weak half mass, beyond the reach of WIT's region theorem. The exact failing inequality is $T>-\lambda n(V-Y)\Phi(\rho Y)$ at any zero of $X-Y$ after $s=0$.
- **Mechanism statement corrected.** H2 Theorem B item 3 (harm = weak-produced input rotation) is replaced by the four-part split. Target plus core opposes harm in the input channel. The target's own output pull is a positive harm term. The weak family adds input-channel harm (proved up to half mass) and removes the fraction n of the output-channel harm.
- **My errors (ledger 30–31).** My lag bound $5p_*/7$ silently assumed $X\ge0$ on J. My prompt and v1.28 also called the lag's regression split a "producer split".
- **Next: S6c.** The post-half-mass input sign. This is one bounded attempt; S8 is the alternative.

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
| **Theorem A** | From aligned-isotropic initialization, on an analytically specified joint family $(q,S_0(q))$ near $\rho=2/3$: substantial learning of both concepts, strict opposite cluster signs $D_1<0<D_2$ on a common learned window, and an ordered negative-then-positive total rate, giving a rebound $\ge c\,q^2$ on an off-cone sector of width $\ge c\,q$. | **Proved (deep regime, Nov 2; RTA):** $S_0=q^{10}$, $0<q\le q_0$, $(\rho,\zeta)\in\mathcal P_*$. |
| **B-core** | The same proof shows *why*: cluster-1 help = exposure × signed exact lag; cluster-2 harm = input rotation of the strong carrier driven by a residual that the weak family produces; the evolving lag/exposure/residual force the change of dominance, with complete remainders. | Proved in the leading system. **Original flow (CPD, deep regime): help = exposure × positive exact lag, proved.** Harm = four leading producer parts (target/weak × input/output rotation); all signs proved except the weak input part on $J\cap(0,\infty)$ (S6c). The item-3 description "harm = weak-produced input rotation" is corrected accordingly. |
| **B-bridge** | The canonical depth enhancement: a non-small inactive strong bridge changes exposure and compensation. | Open (AN4). |
| **Persistence** | After the rebound, the scaled benefit is eventually zero on growing windows. | **Proved for the initialized family (RTA, via FWC and LP's diagonal argument)**, on a diverging horizon with no rate. |
| **Linear contrast** | Commuting aligned linear networks have monotone probe error and clusterwise help. | Complete (LP, extending P10). |

### 1.2 Empirical facts the theory must account for

| # | Empirical fact (user-reported) | Theory component | Status |
|---|---|---|---|
| E1 | ReLU off-cone reversals; no above-threshold linear reversals in matched controls | LP linear contrast + Theorem A | Contrast done; A proved in the deep regime (RTA) |
| E2 | Help from cluster 1 via strong-family output; harm from cluster 2 via strong input rotation; weak output is the residual producer | Leading identities $d_1=-\tfrac12A_\zeta L$, $d_2$ formula; positive-lag theorem | Help proved in the original flow (CPD, deep regime). Deep-regime harm also has a leading target output-rotation part. The empirical "input rotation" attribution (canonical run) needs reconciling with this split |
| E3 | Lag collapses through the crossover while exposure is roughly steady | Lag ODE; WIT windows | Signs proved; a quantitative "collapse" statement is not |
| E4 | Crossover ≈1.10–1.15 physical time after weak learning | Selected-orbit timing | Existence proved; the decimal is **[eval]**; two-sided analytic timing optional |
| E5 | Canonical depth several times the coherent limiting value | B-bridge (AN4) | Open |
| E6 | Persistence through physical time 100 | LP/LPR + AN7 | Limiting done; initialized persistence proved (RTA), diverging horizon, no rate |
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

**Status after WPT (`AN03_weak_passage_theorem_v1`, Oct 28).**
- *Proved (two-boundary theorem).* Let $t_\pm$ be the first times c hits $c_b$ and 0, and $\tau=\min(t_-,t_+)$. With constants fixed in CFA's order ($L_T=20$, $b_B=q^{1/10}$, $M_K=2$, $E_g=2c_b$):
  - $c(t_0)=a^2q^2/(2\lambda)+o(q^2)>0$ and $t_0<\tau<t_0+20\ell$;
  - on $[t_0,\tau]$, every assembled estimate holds: residuals, $J_G$, $\int r$, $\int|1-\kappa_1|\le\log2+o(1)$, $\mu_{\mathcal K}\le e^{d_q}$, $H_{G_+}\le\tfrac98c_b+o(1)$, $E_\Sigma$, core retention $r_{\mathcal K}=O(q^{1/20})$ with $e\le3e_*/4$, outside rates, $\int\epsilon_F<\overline F_F/2$, $\int f_*\le e_*/(4C_{\rm pass})$, and the clock with its $o(1)$ defect;
  - duration margin $20\cdot\tfrac{507}{1600}-\tfrac{231}{40}=\tfrac9{16}>0$.
- *The gap.* $c(t)\ge0$ for $t_0\le t\le\min(t_+,t_0+20\ell)$. Here c is a signed regression coefficient, not a mass.
  - The absolute ledger gives only $c\ge\tfrac89H_{G_+}-\epsilon_q$. This is too weak at entry, where $H_{G_+}=O(q^3)$ while the core response $c_{\mathcal K}\asymp q^2$ is positive.
  - A **signed** bound is needed: $c_\Sigma+c_{\mathcal K}+c_{\mathcal B}>-\tfrac89H_{G_+}+(\text{tail})$ at any putative first zero.
- *Clock correction.* The exact identity is $t-t_0=[\log(H/H_0)-\delta]/Q+\int c$, with $\int c=O(c_b)$. So $t_b-t_0=[\log(c_b/H_0)+O(1)]/Q$, given $H(t_b)\asymp c_b$; the $Q(1-c_b)$ form is only an upper bound.
- *Proposed route for the barrier (reviewer; verify first).* Decompose $c=c_{\mathcal K}+c_{G_+}+c_\Sigma+c_{\mathcal B}$.
  - **Core is positive and of order $q^2$.** Under the guards the core sits at $x,y\ge a-3e_*/4-r_{\mathcal K}$. Since $a\ge\rho\phi(0)\ge0.259>3/16\ge3e_*/4$, this gives $x,y\ge0.07$. The exact Gaussian moment then gives $c_{\mathcal K}\ge\kappa_0q^2\mu_{\mathcal K}$ with explicit $\kappa_0>0$, where $c_{\mathcal K}\approx(q^2/Q)\int y\rho K(\rho x)\,d\mu$. Also $\mu_{\mathcal K}\ge(\tfrac12-o(1))e^{-d_q}$.
  - **$G_+$:** $c_{G_+}\ge\tfrac89H_{G_+}-C\mu e^{-\rho^2/(4q^2)}$ (LCRC ledger).
  - **Σ:** $|c_\Sigma|\le C(q^5+q^{\Gamma_\nu}H)+Cq^2K_Y\sqrt{q^5+q^{\Gamma_\nu}H}\le\tfrac19H+o(q^2)$.
  - **Outside:** show $(c_{\mathcal B})_-\le\tfrac{\kappa_0}4q^2\mu_{\mathcal K}+\tfrac19H_{G_+}$. Two possible routes:
    - an *energy route*, using $|c_S|\le E_S+2q\sqrt{E_SJ_S/Q}$ with weak energies rather than masses. Near the strong axis, $E\sim q^2\xi^2m$. The complement's weighted second moment gives $E_{\mathcal C}\ll H$, the π strip has $\mu\ll H$ at all times, the Q3 interior has a closed $P_2$ gate, and $J_3$ satisfies $\mu_{J_3}(t_0)=O(q^3)$ with near-core labels of positive sign;
    - or a *sign-alignment route*, using $\Delta'=-\operatorname{tr}R\sin\Delta+(R_{12}-R_{21})\cos\Delta$. This would confine negative-response states ($\sin\theta>0>\sin\psi$) to $|\theta|,|\psi|\le Cq$, where the response is $O(q^2m)$.
  - Then $c\ge\tfrac{\kappa_0}2q^2\mu_{\mathcal K}+\tfrac12H_{G_+}>0$ on the whole interval, so $\tau=t_+$.

**Status after RB (`AN03_response_barrier_v1`, Oct 28): weak passage complete.**
- *Theorem (initialized deep-regime weak passage).* For κ=10, ρ∈[13/20,7/10], fixed constants in WPT's order, and small q:
  - the original flow reaches $c=c_b$ at $t_b<t_0+20\ell$, with $c>0$ throughout;
  - all of WPT's estimates hold on $[t_0,t_b]$;
  - $H(t_b)\asymp c_b$, and $t_b-t_0=[\log(c_b/H_0)+O(1)]/Q$, where the clock has an $o(1)$ subinterval defect and the phase error is a bounded constant.
- *Proof checked:*
  - **Core sign.** $\phi(0)>3/8$ gives $a\ge39/160$, and $39/160-3/16-9/320=9/320$. The core moment $(q^2/Q)\int y\rho K(\rho x)$ gives $\kappa_0=351/102400$. Mass stays at least $(\tfrac12-o(1))e^{-d_q}$ by a last-crossing argument.
  - **Entry alignment.** Q2EC's all-receiver decomposition gives $(\operatorname{tr}R)_-\le C(q^2M+\mu)$ and $|R_{12}-R_{21}|\le C(qM+\mu)$. The trace is nonnegative because $M\le1/2$.
  - **Alignment after $t_0$.** $(R_{22})_-\le\tfrac12M_{\rm res}q^2+\tfrac12(Qc+N_-)$, and S2CP's gate budget makes the negative-trace integral at most $B+G_b$. This gives $|\theta-\psi|\le C_{\rm al}q(1+\ell)$.
  - **Exact Stein moment.** $E_{P_2}[X_2(a_\theta\cdot X)_+]=\rho qK(\rho s/q)+q^2s\Phi(\rho s/q)$. Three sign cases then give $(c_S)_-\le C(q+\delta)^2\mu_S$, so $(c_{\mathcal B})_-=O(q^{31/10}\ell^2)=o(q^2)$.
  - **Terminal comparison.** $H_{G_+}(t_b)\ge\tfrac9{10}c_b-o(1)$, and RCET's fixed-distortion transport carries this to the clock cohort.

**Joint assembly (done in WPT except the response barrier; outline kept for reference).**
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

**Revised plan (Oct 28, after RB; reviewer proposal, to verify).**
- *Structure of the remaining deep-regime proof:*
  - $t_0\to t_b$: the weak passage (done);
  - $t_s\to t_{n_b}$: the **selection stage** (S4);
  - from $n_b$ to the reversal windows: finite time, by compact-window matching (S5).
- *Run the selection inside the passage.* Choose a fixed $n_b\in(0,c_b/2]$, small enough for WEAK's small-gain condition $\Theta\le1/4$. Then $t_{n_b}<t_b$, and every WPT/RB estimate is available, so no continuation of the bootstrap past $t_b$ is needed. The core's retention after $n_b$ comes from finite-time matching in S5.
- *Tool:* TAILREP's perturbed selection theorem (`selection`, `Econclusion`, `Wconclusion`), which builds on WEAK's forcing, concentration and `Wineq` results. Its error system is
  $E_s'\le-gE_s+C_s(d_0+NW_p)$, $W_p'\le[-\lambda(1-N)/2+N/2+\ell_B]W_p+C_w(E_s+d_0)$.
  Its conclusion: if $N_0\to0$, $A_0=\sqrt{N_0}W_p(t_s)\to0$ and $d_0\to0$, then the strong-mean and weak-population errors at $n_b$ vanish.
- *Inputs to match:*
  - **(i) Weak return.** For a fixed weak cohort (the clock $\mathcal C_q$ or $G_+$), inputs satisfy $u\ge0$ with WEAK's strict margin from some start $t_s$. Labels arrive from the strong side. BULK's $x=qj/z\le C(q^\eta e^{-b_*\tau/2}+q^2)$ suggests $u(t_{n_b})\lesssim q^{-0.6}$, so a growing weak chart $|u|\le q^{-1+\epsilon}$ is needed, and WEAK allows divergent incoming spread.
  - **(ii) Weak-chart field.** The weak family's field in (u,v), with finite-noise errors of order $q^2(1+u^2)$, the M−1 defect (where $\int_{t_s}(1-M)$ is small once $t_s-t_0\to\infty$), and strong/outside contributions from existing budgets. These must be cast as TAILREP's additive $d_0$ and integrated $\ell_B$.
  - **(iii) Clock matching** N↔H↔c with $o(1)$ phase. RB's exact clock and BULK give $N_{\rm cohort}=H_{\rm cohort}(1+O(q^2))$ in the chart.
  - **(iv) Smallness.** $A_0\to0$ (for example $\sqrt{H(t_s)}\,W_p(t_s)$), and $d_0\lesssim q^\chi+q^{\Delta_\nu}+\dots$ from WPT/RB.
  - **(v) Leading-system hypotheses:** $Y\ge0$ (RB's core has $y\ge9/320$), bounded $\rho K_s$, and positivity of the selected branch's weak input (AN06).
- *First session (S4a):* match all of these hypotheses and close what follows directly. Stop at the first unmatched one.
- *Corrections:* items (i) and (iii) above, the `Observation` below, and items (b) and (d) of `What remains` are corrected by SI (ledger 22).

**Status after SI (`AN03_selection_interface_v1`, S4a, Oct 28): partial; stopped at weak return.**
- *Proved (interface facts):*
  - **Core donor moments.** $\bar D_{\mathcal K}=O(q^{1/20})$. Normalized: $0<\bar Y_{\mathcal K},\rho\bar K_{s,\mathcal K}\le3/5$. Unnormalized: $Y_{\mathcal K}\le5/8$. The geometric margin is $\phi(0)-5/16>1/16$.
  - **BULK in weak coordinates.** $|u|+|v|\le C[q^{-15/8}e^{-Q(1-c_b)(t-t_0)/4}+1]$. At the first hit of a fixed clock level $h<c_Hc_b/2$, which comes before $t_b$, this gives $|u|+|v|\le C_h(1+q^{-p_b})$, with $p_b=15/8-k(1-c_b)/4\in[69/160,147/160]$.
    - The bounded weak chart is never reached inside the passage, but a growing chart $q^{-1+1/20}$ is.
  - **Growing-chart mass.** $N_C/H_C=1+O(q^2L^2)$ for $|u|,|v|\le L$ with $qL\to0$.
  - **Phase identity.** If the comparison logistic starts at $N(t_s)=H(t_s)$, then $\log(H/N)=q^2\int(1-c)+\lambda\int(N-c)+\delta$. The logistic phase therefore needs the signed $\int(N-c)\to0$, which is a response–mass matching statement.
  - **Inventory and notation.** The full inventory with exact constants ($\Theta$, $B_*$, $K_0$, $\mathfrak m$). Notation audit: WEAK's M is the strong-family squared-radius mass, and $v=(\psi-\pi/2)/q$.
- *Gap: the original weak input return.* At $u=0$, $qu'=R_{21}(\pi/2)\cos(qv)-R_{11}(\pi/2)\sin(qv)$, and the needed margin is $qu'/q\ge\mathfrak m/4$. Two available bounds give size, not sign:
  - the cross-residual norm bound $|R_{21}|\le M_{\rm res}q$ leaves an order-one, sign-indefinite remainder after dividing by q;
  - BULK's ratio bound also gives only size: the balanced state with $u=-1$ meets all of its conditions.
  
  The sign must come from a signed weak-receiver computation, the weak-chart analogue of the c-form.
- *Also open (from the inventory):*
  - **Mass-linear terms.** $-(1-M)v\Phi(u)/2$ and $-(1-M)\mathsf K(u)/2$ multiply v, which can be as large as $q^{-p_b}$, so pointwise late control of the strong mass is needed.
  - **Fixed weights.** The fixed-weight comparison is not yet done.
  - **Chart scope.** The c-form chart $|\theta|,|\psi|\le L_cq$ does not cover weak receivers.
  - **WEAK's local initial guard.** RB's $e\le3e_*/4$ does not give $E_0\le\delta/(2K_0)$.
  - **Smallness** of $N_0$, $A_0$ and $d_0$.
- *Revised S4 sequence (estimate 3–4 sessions; was 1–2):*
  - **S4b**, the weak-receiver boundary field and input return: the boundary margin, late strong-mass control, the weak-sender term and the incoming sign.
  - **S4c**, the weak-chart reduction to TAILREP's error inequalities: value vs linear separation, placement of the finite-noise $q^2(1+u^2)$ term, weights, mass deficit, and a common $\ell_B$ budget $L_*$.
  - **S4d**, the logistic phase ($\int(N-c)=o(1)$), initial smallness, the local guard, and the selection theorem at a fixed level.
  - *Superseded after WBR; see the next block.*

**Status after WBR (`AN03_weak_boundary_return_v1`, S4b, Oct 30): closed.**
- *Theorem (original input return to a fixed clock level).*
  - **Setting.** The selected cohort is the whole closed clock cohort $S=\mathcal C_q$; no labels are removed, and endpoint labels are included. $t_e$ is the first hit of a fixed small level $H=h$, which comes before $t_b$.
  - **Conclusion 1.** $u>0$ on $[t_0,t_e]$.
  - **Conclusion 2.** At every boundary hit on $[t_s,t_e]$, where $t_s$ is the first hit of $H=q^{1/8}$, we have $u'\ge g_0/4$, with $g_0=\phi(0)-5/16>1/16$. This holds uniformly over the reached chart $|v|\le L=C_L(1+q^{-603/640})$.
- *Ingredients (checked):*
  - **Exact boundary moments** $R_{21}$ and $R_{11}$ at $\theta=\pi/2$, by Gaussian integration by parts in $X_1$, with no gate differentiated. They reproduce P's `pa:pop-u` at $u=0$, including $-(1-M)v/2$, where M is the physical core mass.
  - **One-sided weak feedback:** $0\le\mathcal W^q_{G_+}(0)\le C_W(H+K_Y\sqrt H)$, from $W_2>0$, Cauchy–Schwarz and pointwise energies. It needs no sender sign and no contraction.
  - **Strong-mass law:** $(\log M)'=1-M+\eta$ with $|\eta|\le Cq^{11/10}$, from CFR `radialbound` under RB's states. Hence $|1-M|\le C_me^{-(t-t_0)/3}+6\varepsilon_q$, and $|1-M|L=O(q^{101/640})$ after $t_s$.
  - **Clock alignment:** $|\theta-\psi|\le C_\Delta q$, with no log loss. It comes from $\operatorname{tr}R\ge b_c/2$: BULK's gate margin gives $R_{22}\ge Q(1-c_b)/4$, and $R_{11}\ge-C\varepsilon_q$ for every gate.
  - **Regularized entry seed:** $\cos\theta(t_0)\ge c_{\rm in}q^{1-\sigma_*}$, with $\sigma_*=2079/13520$, including $b=\pi$, where $s_0+q=q$.
- *New facts for later stages:*
  - $A_S=O(q^2N_S)$ on the clock, from the alignment.
  - $N_S=H+A_S+J_S$.
  - $U_0^+\sqrt{N_0}\le2\sqrt2K_Y$. This is order one, so it does not give $A_0\to0$.
- *New obligation (reviewer, Oct 30): population accounting.* TAILREP/WEAK's weak population is the **whole** weak family. So the selected cohort must carry all but $o(H)$ of the weak mass and response on the selection interval:
  - $H_{G_+\setminus\mathcal C_q}+E_\Sigma+(\text{weak part of }\mu_{\mathcal B})=o(H)$;
  - $c=H(1+o(1))+O(q^2)$.
  
  Otherwise $G_+\setminus\mathcal C_q$ must join the selected population, with its own return. If accounting holds, the logistic phase should follow from the exact clock and a Gronwall argument on $\log(H/N)$. This is unverified.
- *$A_0\to0$:* WBR does not supply it.
  - A likely source is a pointwise transverse bound $J_S\lesssim q^3+q^2H$ at $t_s$ with $p=2$. Whether it is proved under the current guards still has to be checked (ledger 18).
  - The crude BULK-size route needs a start level that is both on a chart and has $\sqrt{N_0}\sup|u|\to0$. By my count such a level exists only for $k>5.5$, so this route fails on part of the ρ box. This count is unverified.
- *Remaining S4 (2–3 sessions):*
  - **S4c, the matching package:** population accounting, logistic phase, mass identities, $A_0$, and late mass-defect budgets.
  - **S4d:** field reductions (weak chart and strong reference) to TAILREP's error inequalities, the local strong guard $E_0$, and the selection theorem.
  - *S4c is done (MP, next block). S4d is split into S4d and S4e.*

**Status after MP (`AN03_matching_package_v1`, S4c, Oct 30): closed.**
- *Theorem (matching package).* On $[t_s,t_e]$ (the first hits of $H=q^{1/8}$ and $H=h$), with $S=\mathcal C_q$:
  - **Population.** The omitted primary band $P_q=G_+\setminus\mathcal C_q$ has $H_{P_q}/H\asymp q^{1/4}$, and $H_{P_q}+\mu_\Sigma+\mu_{\mathcal B}=O(q^{1/4}H)$.
  - **Response.** $c=H(1+O(q^{1/4}))+O(q^2)$.
  - **Phase.** For the logistic N with $N(t_s)=H(t_s)$:
    - $\sup|\log(H/N)|\le C(q^{1/8}+q^2\ell+q^{1/4}h/b_0)=o(1)$;
    - $\int|N-c|=o(1)$;
    - interior hitting times differ by $o(1)$.
  - **Masses.** $N_S/H=1+O(q^2)$ and $N_{\rm nc}/H=1+O(q^{1/4})$.
  - **Transverse energy.** $J_S\le C(q^3+q^2H)$, from BULK `forcing`/`Jprop` with $G=S$ and $\sigma=0$; the inputs come from RB and Q2EP.
  - **Smallness.** With $p=2$: $N_0=q^{1/8}$ and $A_0=O(q^{1/16})$.
  - **Mass defects.** $\sup|1-M|=O(q^{11/10})$ and $\sup|1-M|L=O(q^{101/640})$, with matching integrated budgets.
- *Checked:*
  - $\gamma(169/400)=6481/18480>7/20$;
  - the band measure;
  - the seed ratio, where the $A_q^{-\lambda}$ factors cancel;
  - RCET's fixed distortion;
  - the ledger identity $c_S=H-A_S+\tau_S$, with the absolute bound $|\tau_S|\le C\mu_Se^{-c/q^2}$ on the reached chart;
  - the Young bound;
  - the sign-contracting phase equation;
  - the logistic hitting-time formula;
  - $\int m(u^2+v^2)\le CJ_S/q^2$;
  - the sup-route window. Its exact necessary condition is $k>11/2+7c_b/(2(1-c_b))$; my "$k>5.5$" was only the $c_b\to0$ limit.
- *Remaining S4 (2 sessions, possibly 3):*
  - **S4d, the strong reference.**
    - Reduce the strong reference to TAILREP's `strongerror` form, with pointwise $d_0\to0$.
    - The weak influence on strong receivers must appear as leading weak moments (N, and the weak population's moments compared through $W_p$), not as CFA's fixed $C_0E_g$ remainder.
    - Establish WEAK's local box for $N\le2h$, and $E_0\to0$ at $t_s$.
  - **S4e, the weak chart and selection.**
    - Reduce the selected cohort's (u,v) field on the reached chart to TAILREP's `weakerror` form: value vs coefficient, the normalized-weight defect, and a common $L_*$.
    - Then apply TAILREP's selection at a fixed logistic level $n<h$ (for example $h/2$).
  - *S4d is done (SRR, next block).*

**Status after SRR (`AN03_strong_reference_reduction_v1`, S4d, Oct 31): closed.**
- *Theorem (strong-reference part of the selection system).* Fix any $0<n<h$. On $[t_s,t_n]$, up to the first exit from $E_s<\delta$:
  - $D^+E_s\le-g_WE_s+C_s(d_0^{(s)}+NW_2)$, with $g_W=\gamma/2$, $\gamma=\alpha(1/2-\alpha)/(\alpha+1/2)$, $C_s=980$;
  - $d_0^{(s)}=C_{\rm srr}q^{1/20}$, pointwise; its size is set by the core first moment $\bar D_{\mathcal K}$;
  - $E_0=E_s(t_s)=O(q^{1/20})$. With MP's $A_0=O(q^{1/16})$, the strong part of TAILREP's initial guard holds for any fixed $K_0$ once q is small.
- *Checked (reviewer, Oct 31):*
  - **Primary tail.** $b_*(t_s-t_0)=(1-c_b)(k-1/8)\ell/2+O(1)$; the factor Q cancels. With $c_b\le1/4$ and $k\ge51/10$ the exponent is at least $\tfrac34\cdot\tfrac{199}{40}\cdot\tfrac12=597/320<2$. So after $t_s$, $\mathcal T\le Ce^{-cq^{-597/320}}+Ce^{-c/q^2}$, and CFA's fixed $C_0E_g$ never enters $d_0$.
  - **Start exponent.** $g_c(k-1/8)/Q\ge\tfrac{1183}{41600}\cdot\tfrac{199}{40}\cdot2=235417/832000>1/20$.
  - **Chart order.** $q^2L^2=O(q^{2-1206/640})=O(q^{37/320})$, and $37/320>1/10$.
  - **Exact selected moments.** $V_S=\int_Sm\sin(qv)\cos(qu)/q$ up to an exponentially small gate tail. On $P_1$ the gate variable is $q[\sin(qu)/q+G]$ with $G\sim N(0,1)$ exactly, so Stein gives $K_S=\int_Sm\cos(qv)[\mathsf K(r)+q\sin(qu)\Phi(r)]$, $r=\sin(qu)/q$.
  - **Non-selected charges.** $|V_T|+|K_T|\le C(\mu_T+q^{-1}\sqrt{\mu_TJ_T})$ from balance: $P_q$ costs $O(q^{1/8})$, Σ costs $O(q+q^{\Gamma_\nu/2})$, and $\mathcal B$ costs $O(q^{1/10})$.
  - **Coefficient.** $N_S/N\le2$ and $\omega\le2$ give $4NW_2$. The field coefficients are at most 10, giving $80NW_2\le C_sNW_2$. WEAK's $R_*=6$ is admissible: $2+a+|u_*|+a/\lambda<2+\tfrac25+1+\tfrac{160}{169}$.
  - **Local box.** $\|J_*-J_1\|\le L_J(|x-a|+|y-a|+N)$, with $V_*$ frozen; it drops out at $N=0$. Then $\delta\le\gamma_*/(16L_J)$ and $h\le\gamma_*/(8L_J)$ give $J_*\le-(\gamma/2)I$ on the 2δ box for $N\le2h$, using $\gamma\ge\gamma_*$.
  - **Before $t_s$.** RB `primaryclock` ($H\le H_{G_+}\le C_{\rm ent}e^{2D_+}H$) holds on the whole passage, so $E_{G_+}\le CH<Cq^{1/8}$. Then $f_*=O(q^{1/16})$, dominated by $K_Y\sqrt H$, and $r_{\mathcal K}=O(q^{1/20})$.
- *New constants:* $\delta=\tfrac12\min\{a_{\min}/8,(2\phi(0)-a_{\max})/3,1/8,\gamma_*/(8L_J)\}$, with $a_{\min}=39/160$, $a_{\max}=2/5$, and model-only $L_J$, $n_{\rm br}$, $C_{\rm br}$. **New upper bound on the level:** $h\le\min\{h_{\rm WBR},n_{\rm br}/2,\delta/(2C_{\rm br}),\gamma_*/(8L_J)\}$, $h<1/4$.
- *Conventions handed to S4e:* $\eta_s=m(t_s)\,d\lambda_0/N_S(t_s)$, transported with fixed labels; $W_2$ is the $p=2$ distance to $(U_*,V_*)(N(t))$; $\omega=d\eta_t/d\eta_s=1+O(D_q+q^2L^2)$, a value bound only.
- *Reviewer notes for S4e (to verify, not established):*
  - **Weight derivative.** SRR lists a "derivative normalized-weight defect" for S4e. Because $W_2$ is defined on fixed labels, $D^+W_2$ involves only per-label velocities. The actual-weight donor terms then need only ω's value bound. This obligation may therefore be empty; S4e should decide rather than build it by default.
  - **Value-only route.** TAILREP's remark after `weakerror` says population-to-orbit comparison needs value bounds at actual receivers, while receiver derivatives are needed only for pairwise contraction. So the weak reduction can compare each receiver's velocity with a leading-form field built from the actual positive donor measures, and take the contraction from that field on $u\ge0$.
  - **Admissible growth.** On the reached chart, a per-label error of size $q^j\times$(degree-$i$ monomial in $|u|,|v|$) splits into $\ell_B(|u-U_*|+|v-V_*|)$ plus an additive $o(1)$ term exactly when $j>\tfrac{603}{640}(i-1)$. Any other term needs its signed leading value (ledger 22).
- *Remaining S4:* S4e (1 session, possibly 2).
  - *S4e is done (WCS, next block).*

**Status after WCS (`AN03_weak_chart_selection_v1`, S4e, Nov 2): closed. S4 complete.**
- *Theorem A' (weak error form).* On $[t_s,t_n]$, up to the first exit from $E_s<\delta$: $D^+W_2\le[-\lambda(1-N)/2+N/2+\ell_B]W_2+20(E_s+d_0^{(w)})$, with $d_0^{(w)}=C_{\rm wcs}q^{1/20}$, $\ell_B=\tfrac\lambda2|c-N|+\tfrac N2\epsilon_w+C\{|1-\mu_{\mathcal K}|+q+q^2(1+L^2)\}\ge0$, and $\int_{t_s}^{t_e}\ell_B=o(1)$, bounded without reference to $t_n$, so $L_*=1$ is fixed before n.
- *Theorem (initialized $L^2$ selection inside the weak passage).* Constant order WPT/RB → WBR → $(a=1/8,p=2)$ → $(\delta,g_W,C_s)$ → h → $(C_w,L_*)$ → n → q. With the explicit n above, $E_s(t_n)+W_2(t_n)=O_n(q^{1/20})$ and the strong guard closes to $\delta/2$.
- *Checked (reviewer, Nov 2):*
  - **Exact velocities.** The θ-direction of $a=(s_u,c_u)$ is $-p$ and the ψ-direction of $b$ is $b^\perp$, so $2u'=q^{-1}\sum_j\mathbb E_{P_j}[(b\cdot(X-f))(p\cdot X)1_A]$ and $2v'=q^{-1}\sum_j\mathbb E_{P_j}[(b^\perp\cdot(X-f))(a\cdot X)1_A]$, with the mixture factor ½.
  - **Tangent integration by parts.** On $P_1$, $a\cdot X=q(r+T)$ and $p\cdot X=c_u+qZ_\perp$, with $T,Z_\perp$ independent; the receiver gate depends on T only, and $\partial_{Z_\perp}(U\cdot X)=qU\cdot p$. All four projected target moments re-derived, including $\mathbb E(T+r)_+^2-r\mathsf K(r)=\Phi(r)$.
  - **$P_2$ matrix.** $B_{22}=Q(1-c)$ by the definition of c; $B_{12}=-q\rho K_c+qQV_O+O(q^3)$ from $\mathbb E_V[V\mathsf K(t_xV)]$ with $V\sim N(\rho,q^2)$; $B_{11}=O(q^2)$, $B_{21}=O(q^3)$. The leading coefficients reproduce `pa:pop-u` and `pa:pop-v` exactly, which also checks the normalization.
  - **Growth.** Gaussian saturation ($s_u/q\in[u/2,u]$ for $qu\le1/2$) gives $|\Phi(s_u/q)-\Phi(u)|=O(q^2)$, removing the apparent $q^2|v|u^3$. Admissibility exponents $j-\tfrac{603}{640}(i-1)$: 1, 677/640 and 37/320, all positive.
  - **Contraction.** $F_t=(r-t)_+\phi(t)\ge0$ makes $\mathcal W_S'\ge0$, so the comparator derivative is at most $-\lambda(1-c)/2$ on $u\ge0$ with $Y\ge3/320$; only value bounds of the remainder are used.
  - **Constants.** $(1+\lambda)\mu_{\mathcal K}\le3$ gives the $\tfrac32E_s$ coefficient. For Θ: $B_*\le e\,2^{1/(2\lambda_{\min})}$, $a_0-m_0\ge\lambda_{\min}/8$, $g-m_0\ge g_{\min}/2$ (since $g_W\ge\gamma_*/2$), so $\Theta\le16C_sB_{\max}C_wn/(\lambda_{\min}g_{\min})\le1/8$.
  - **Times.** $T_n=\ell/(8\lambda)+\lambda^{-1}\log(n/(1-n))+o(1)$; $t_n-t_0=Q^{-1}\log\{n/[(1-n)H_0]\}+o(1)$ from RB's exact clock identity with the pre-$t_s$ $\int c=o(1)$.
- *Weight derivative:* not needed (the norm is on fixed labels), as the v1.22 note expected.
- *Handoff at $t_n$ (WCS `handoff`):* $|z_c-Z_*(n)|=O_n(q^{1/20})$; core first moment about the atom $O_n(q^{1/20})$, $\mu_{\mathcal K}=1+O(q^{11/10})$; $W_2(\eta_s)=O_n(q^{1/20})$ and $(1+o(1))$ that under current weights; $N_S/n=1+O_n(q^{1/8})$, $c(t_n)=n+O_n(q^{1/8})$; non-selected weak mass $O_n(q^{1/4})$ with field charges $O(q^{1/8})$, $O(q+q^{\Gamma_\nu/2})$, $O(q^{1/10})$; $\sup\mu_{\mathcal B}/q\le q^{1/10}$.
- *Limits:* $p=2$, not $p=\infty$; no bounded weak support; nothing past $t_n$.

**Original claim (v1; "bounded chart" superseded by SI).** The Q2 bulk, which is on the strong side at angle $\approx q^{0.52}$ at κ=10 strong entry (target-only), returns into a bounded weak chart with $u\ge0$. Its evolution there matches a closed leading weak family with $\sqrt{N_0}\,W_p(t_0)\to0$, and its response clock matches the logistic half-mass phase to $o(1)$.

**Observation (superseded by SI; ledger 22: BULK gives size, not sign, and the bounded chart is not reached inside the passage). Original text:** Its ratio $x=qj/z\approx q\cot\theta/\sqrt2$ satisfies $x\le C[q^\eta e^{-b_*\tau/2}+q^2]$. Once $x\lesssim q^2$, $\cot\theta\lesssim q$, so the weak input coordinate $u=(\pi/2-\theta)/q$ is bounded. Labels arriving from the strong side have $\theta<\pi/2$, i.e. $u\ge0$. The output coordinate $v$ is bounded by the same $j$ control. The entry time is $\approx\frac{2(2-\eta)}{b_*}\log(1/q)$.

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

**Revised plan (Nov 2, after WCS; reviewer proposal, to verify).**
- *Starting point.* WCS's state at $t_n$, a fixed small weak mass, inside the weak passage.
- *Consumers:*
  - WIT `populationtransfer` (tolerance $\varepsilon_*$ in the first-moment distance `distance`) and `propagation`;
  - WIT `ratebound` and `clockalignment`;
  - LP `diagonal-transfer` (persistence);
  - LPR `combinedtheorem`;
  - H2 §3.2 and the AN7 contract, items 1–6.
- *Risk 1: compact support.*
  - WIT `populationtransfer` and `propagation` assume chart supports in $[-R,R]^2$ for both families, and `propagation` has coefficient $e^{64R(s-a)}$.
  - At $t_n$ no proved bound gives the selected weak cohort a bounded support. WBR/BULK give only $|u|+|v|\le Cq^{-p}$ with $p>9/10$ even after BULK's time decay ($603/640$ less at most $\tfrac1{32}\cdot\tfrac Q\lambda$). WEAK's multiplier from MP's incoming support gives $W_\infty(t_n)\lesssim q^{1/16}L\to\infty$.
  - What looks available, to verify:
    - `ratebound` uses the weak family only through $K_w,V,N$, which are Lipschitz in the first moment without support bounds;
    - $\eta_s$-mass beyond unit distance from the branch is at most $W_2^2$;
    - the selected weak family is probe-inactive on the whole reached chart, since $a_w\cdot\xi_q=-\cos(q(u+\zeta))<0$ whenever $q|u+\zeta|<\pi/2$.
  - So a version of WIT's transfer with compact strong support and first-moment weak control is plausible.
- *Risk 2: $q^{-2}$ precision for probe-active outside labels.*
  - With $\xi_q=(\sin q\zeta,-\cos q\zeta)$, a label is probe-active iff its input angle lies in $(q\zeta-\pi,q\zeta)$. Q1 above the probe offset, Q2 and the whole weak family are inactive.
  - Active non-core populations:
    - the strong complement below or near the axis;
    - the Q3 interior;
    - the 3π/2 strip, adjacent to the probe direction $-\pi/2+q\zeta$;
    - the part of the π strip beyond $\pi+q\zeta$.
  - An active label contributes $-(W\cdot\xi)(U\cdot\xi)_+$ to $E-\tfrac12$, which can be as large as its mass m.
  - The proved outside budgets are mass rates: complement $\mu\lesssim q^{1+\Delta_\nu}$ ($\Delta_\nu>3/25$); Q3 interior $\mu\lesssim q^{10}$; π strip $\mu\lesssim q^{1+411/800}$ (polylog); $J_3$ $\mu\lesssim q^{1+769/4000}$ (polylog). In total $\mu_{\mathcal B}\le q^{11/10}$, while A-error-transfer needs these contributions to be $o(q^2)$.
  - The crude charge therefore fails by up to $q^{-9/10}$. S5 needs probe-sector mass or second-moment bounds, or the signed geometry (for aligned labels the contribution is $\le0$), and the same for their rates.
- *Risk 3: continuation past $t_b$.* Every passage estimate is proved for $0\le c\le c_b$. WIT's windows lie a fixed time after $t_n$, where $N\ge1/4$, so a finite-time bootstrap must carry residual, core, outside and weak bounds past $t_b$ with fixed $e^{CT}$ losses.
- *Clock.* An analytic original centering is available: $\tau_h:=t_n+\lambda^{-1}\log((1-n)/n)$, the half-mass time of the same exact logistic N. WCS gives its $o(1)$ actual-clock phase.
- *Sessions (estimate 4, possibly 5):*
  - **S5a.** Interface and probe-precision audit: inventory, static probe-activity classification, the precision ledger, and a leading-system transfer lemma with non-compact weak support.
  - **S5b.** Finite-time original-flow continuation from $t_n$ to the windows, and the original-to-leading reduction there.
  - **S5c.** Outside and background probe budgets, and A-error-transfer on every fixed window.
  - **S5d.** A-rate-transfer on the gate-separated windows; the AN8 assembly (Theorem A via WIT + LPR, persistence via LP).
  - *Reordered in v1.24; see the next block.*

**Status after CWI (`AN07_compact_window_interface_v1`, S5a, Nov 2): audit complete; leading extension closed.**
- *Closed:*
  - **Clock.** $\tau=\mu_1^2t_{\rm phys}$. $\tau_h=t_n+\lambda^{-1}\log((1-n)/n)$ is the exact center of WCS's auxiliary logistic, equal to $t_0-Q^{-1}\log H_0+o(1)$. It is not an original half-mass hit.
  - **Activity** (`signs`). $a_\theta\cdot\xi_q=\sin(q\zeta-\theta)$, so a label is active iff $\theta\in(q\zeta-\pi,q\zeta)$, with both endpoints at zero. $G_+$ (S and $P_q$) is inactive at $t_n$ by the late RCET ratio. Q2 inactivity needs $\zeta\ge0$.
  - **Exact split** (`split`, `equivalence`). $E-E^{\mathcal K}=-\mathcal Q_T+\mathcal A_T+f_{\mathcal K}\cdot f_T+\tfrac12|f_T|^2$ with $T=\Sigma\cup\mathcal B$, and it is $o(q^2)$ iff $\mathcal Q_T=o(q^2)$.
  - **Core at entry** (`corestatic`, `corerates`). Static error and source rates $O_n(q^{2+1/20})+O(q^4)$.
  - **Outside rate charge** (`ratecharge`). $|\xi_q\cdot\dot f_{T,p}|\le C(\mathcal Q_T+q^2(1+\ell)^2\mu_T)$.
  - **Leading extension** (`rate`, `propagation`, `witness`). The constants $64R^2(1+g_0^{-1})$, $10R^2$ and $e^{64R(s-a)}$ are unchanged, with strong-only compact support and finite weak first moments. A one-sided weak receiver derivative bound $\le R+1$ replaces the absolute Lipschitz bound.
- *Gaps at entry (after division by $q^2$):*
  - Σ: only its lower-half slice remains unpaid;
  - strong complement: the tail test gives exponent $\Xi_\nu\le915/604<2$ at $\lambda=49/100$;
  - inner π strip: $q^{-389/800}$;
  - $J_3$: $q^{-3231/4000}$.
- *Checked (reviewer):*
  - the activity identity, the split algebra and the Young step;
  - $G_+$ inactivity from the RCET ratio;
  - $\Gamma_\nu\le481/1020$ (derivative $-5+2/(1-\lambda)^2>0$ on the box);
  - the tail-test rationals: $B(49/100,1/2)=311/604$, so $\Xi_\nu\le1+B=915/604$; bracket $-8093/200$; corner $54762159/43757500$ with $R_g=-303/2500$;
  - the exponents $1211/800-2=-389/800$ and $4769/4000-2=-3231/4000$;
  - the one-sided derivative bound ($|u|\phi(u)\le\phi(1)<1$, $\phi\le\phi(0)<2/5$, $\lambda|1-N|\le1$);
  - the exact rate formula ($m'=2gm$, $\theta'=v_\theta$, $\psi'=v_\psi$).
- *Reviewer observation: a proposed lower-half energy route.* The static part is checked; the dynamics are not verified.
  - **Static.** $U\cdot\xi_q=U_1\sin q\zeta-U_2\cos q\zeta\le q\zeta|U_1|+(U_2)_-$ for $\zeta\ge0$. Hence, for every state, $\mathcal Q_T\le2q^2\zeta^2\mu_T+2\mathfrak E_T$, where $\mathfrak E_T=\int_T(U_2)_-^2$.
  - **Dynamics.** $U_2'=W_1R_{12}+W_2R_{22}$ with $R_{ij}=\mathbb E_{\rm mix}[(X-f)_iX_j1\{U\cdot X>0\}]$, and:
    - $R_{12}=O(q)$ for every receiver;
    - $R^{(1)}_{22}=O(q^2)$;
    - for $U_2<0$ the $P_2$ gate is open with probability only about $\Phi(-\rho|\sin\theta|/q)$;
    - labels enter $\{U_2<0\}$ only through $U_2=0$.
    
    So $\mathfrak E_T$ should grow only through terms Young absorbs at weight $1/\ell$ over the $O(\ell)$ duration: $\mathfrak E_T(t)\le C[q^{10}+q^2(1+\ell)^j\sup\mu_T]=o(q^2)$ for $T=\Sigma\cup\mathcal B$. That would pay every unpaid cohort at once, including transit labels.
  - **Why the tail test failed.** Its majorant multiplied the full mass gain by $\min(1,A\xi^2)$; the energy route keeps angle and gain together.
- *Reviewer observation: entry at smaller levels.* WCS's bound $\Theta\le16C_sB_{\max}C_wn'/(\lambda_{\min}g_{\min})$ holds for every $n'\le1/2$. So its selection theorem should apply at every fixed $n'\in(0,n]$, with constants uniform on compact level sets (to verify in S5b). That would give entry comparisons for every window $s\le s_n$.
- *S5 sessions, reordered (estimate 3, possibly 4):*
  - **S5b (next): probe-sector energy and entry precision.**
    - The static and dynamic $\mathfrak E_T$ bounds on $[0,t_b]$, paying $\mathcal Q_{\Sigma\cup\mathcal B}=o(q^2)$ on $[t_s,t_b]$.
    - The entry error and rate comparison at every fixed $n'\le n$.
    - The exact list of bounds to continue past $t_b$.
    
    This is risk-first: under continued matrix bounds, $\mathcal Q_T$ changes over a fixed window only by $e^{\pm CT}$ factors plus $O(q^2(1+\ell)^2\mu_T)$, so entry precision is effectively necessary.
  - **S5c: continuation.** From $t_n$ through the windows: passage-internal up to $t_b$, then a finite-time bootstrap past $t_b$ for the masses, the matrix and alignment bounds S5b needs, the original-to-leading reduction in CWI's first-moment norm, and the mass/logit phase.
  - **S5d: transfer and assembly.** A-error-transfer on every fixed window, A-rate-transfer on WIT's $J$, then AN8 (Theorem A via WIT + LPR, persistence via LP).

**Status after PSE (`AN07_probe_sector_energy_v1`, S5b, Nov 2): closed.**
- *Theorems (all on the original initialized flow, constants in the fixed order, q last):*
  - **Energy** (`energy`). For every fixed cohort, $\mathfrak E_T(t)\le e^{31}\mathfrak E_T(0)+31e^{31}C_Eq^2L^2\sup_{[0,t]}\mu_T$ on $[0,t_b]$. Here $\mathfrak E_T(0)\le q^{10}$, and $\mathfrak E_\Sigma(0)=0$.
  - **Masses** (`backmass`). $m(t)\le e^5m(t_0)$ for every label and $t\le t_0$, so RB's passage mass budgets extend to $[0,t_b]$.
  - **Background** (`Qpaid`, `lateprecision`). $\sup_{[0,t_b]}\mathcal Q_{\Sigma\cup\mathcal B}\le C_{R_\zeta}q^2\epsilon_{\rm bg}$, with $\epsilon_{\rm bg}=q^8+L^2q^{\gamma_*}$ and $\gamma_*=289169/924000$. On $[t_s,t_b]$, the full error, the background output rates and the total source rates differ from the core's own by $O(q^2\epsilon_{\rm bg})$.
  - **Entry** (`levels`, `entry`). For n′ in a compact $\mathcal N\subset(0,n]$: $E_s+W_2=O_{\mathcal N}(q^{1/20})$, $q^{-2}(E-\tfrac12)(t_{n'})=\mathcal E_{\rho,\zeta}(s_{n'})+O_{\mathcal N}(q^{1/20})$, and the same for $q^{-2}D_p^\tau$. This holds uniformly over the ratio box and $\zeta\in[87/50,7/4]$, with the single center $\tau_h$.
  - **Continuation criterion** (`conditional`). On a future window, the energy continues under four matrix-value and alignment bounds: $|R_{12}|\le C_{12}q$, $|R^{(1)}_{22}|\le C_1q^2$, the lower-gate bound on $R^{(2)}_{22}$, and $|W_2-U_2|\le d_{\rm al}\sqrt m$.
- *Checked (reviewer, Nov 2):*
  - **Cross residual.** PSE's input $\|e_2\|_{P_1}+\|e_1\|_{P_2}\le C_\times q$ is exactly WPT/RB's $M_{\rm res}q/2$ guard (WPT lines 104–105, RB 610–611) and Q3SB `crosspre` on $[0,t_0]$; same norm.
  - **Loss.** $\mathcal L(0)\le1$ and $\mathbb E_{P_j}\le2\,\mathbb E_{\rm mix}$, so $\|e_f\|_{L^2(P_j)}\le2$ at all times.
  - **Lower gate.** Under $P_2$, $a_\theta\cdot X\sim N(\rho\sin\theta,q^2)$, so the gate probability is exactly $\Phi(-\rho s/q)$. Hölder with $\mathbb EX_2^4=\rho^4+6\rho^2q^2+3q^4\le43/16$ and Chernoff give $C_G=2$ and $k_G=\rho^2/8\ge169/3200$.
  - **Energy step.** $(v_-^2)'=-2v_-v'$; $U_2'=R_{12}W_1+R_{22}W_2$; one Young step at weight $1/L$; Gaussian maxima $1/(ek)$ and $1/\sqrt{2ek}$. Since $t_b<30\ell+O(1)\le31L$, the integrating factor is $e^{31}$.
  - **Backward masses.** Polarization gives $a_\psi^TAa_\theta\ge-\tfrac14\|A\|\,|a_\psi-a_\theta|^2$. $\|A_\theta\|\le\|\mathbb E_{\rm mix}XX^T\|=a_*$, and $\|C_f\|\le a_*S$ by Cauchy–Schwarz on the mixture (not per cluster). $\int_0^{t_0}S\le\log2+o(1)$ and $\int|\theta-\psi|^2\le Cq^2L$ then give $e^5$.
  - **Static bound and inactivity.** The static inequality holds. The late primary ratio needs only $I'\le Q$.
  - **Core gap and Θ.** $87/50-21/34=477/425$. $\Theta(n')\le1/8$ for every $n'\le1/2$.
- *Reviewer corollary.* Because $t_{n'}=\tau_h+s_{n'}$ exactly and the entry comparison is uniform on compact level sets, H2's A-error-transfer, and an entry source-rate comparison, already hold on every fixed window $K\subset(-\infty,\min_\rho s_n]$. WIT's J and LP's late windows lie after $s_n$, so this does not yet give Theorem A or persistence.
- *Remaining S5 (2 sessions, possibly 3):*
  - **S5c (next): finite-window continuation and A-error-transfer after entry.**
    - A finite-time bootstrap from $t_n$ for PSE `conditional`'s matrix and alignment bounds, plus core chart, primary inactivity, weak reached chart and transverse energy, past $t_b$.
    - The original-to-leading reduction in CWI's first-moment norm, and a perturbed version of CWI `propagation`.
    - Then A-error-transfer on every fixed window $[s_n,T]$.
  - **S5d: rates and assembly.** A-rate-transfer on WIT's gate-separated J, then AN8: Theorem A via WIT + LPR (on $\mathcal P_*$), and persistence via LP `diagonal-transfer`.

**Status after FWC (`AN07_finite_window_continuation_v1`, S5c, Nov 2): closed.**
- *Theorem* (`main`). For every fixed $T>\max_\rho s_n$ and $R_\zeta<\infty$, on $[t_n,\tau_h+T]$, with no retained hypothesis:
  - the primitive continuation (`primitive` through `masslogistic`);
  - the reduction bound `reductionnorm`;
  - the first-moment distance $\mathfrak d\le e^{64R(s-s_n)}[\mathfrak d(s_n)+\int\mathcal R]=O_{T,n}(q^{1/20})$ (`distbound`);
  - **A-error-transfer** at rate $q^{1/20}$, uniformly over $\rho\in[13/20,7/10]$ and $\zeta\in[0,R_\zeta]$ (`errortransfer`).
  
  With the early-window corollary (`early`), this covers every fixed centered window.
- *Mechanism.*
  - **Masses.** Loss gives $\|R\|\le4$, hence fixed-label masses within $e^{\pm8D}$ of their values at entry.
  - **Combined energy.** $\mathcal Z=E_{\mathcal K}+J_G$ satisfies $\mathcal X\le C[q(1+\bar S)+\sqrt{\bar S\mathcal Z}+\mu_{\mathcal B}]$ and $D^+\mathcal Z\le C(\mathcal Z+q^2+\mu_{\mathcal B}^2)$. So $\mathcal Z=O(q^2)$ and $\mathcal X=O(q)$, with no chart or response hypothesis.
  - **Consequences**, in non-circular order: alignment $O(qL)$; core chart $O(q)$; selected chart $q^{1-p}$; primary $\sin\theta\ge cq^{43/640}$ (hence inactivity and full $P_2$ donor gates); then the physical mass laws.
- *Checked (reviewer, Nov 2):*
  - the balance output bounds and the cross-residual estimate;
  - the Cartesian energy derivatives $(U_2^2+W_2^2)'/2=2R_{22}U_2W_2+R_{12}U_2W_1+R_{21}W_2U_1$ and the $J_G$ analogue;
  - $|R_{12}|+|R_{21}|\le C(q+\mathcal X)$ at every receiver;
  - the angular equations near each axis;
  - $(\sin\theta)'\ge-C\sin\theta-C_DqL$ for primary labels ($1-43/640=597/640>0$);
  - $c=N+O(q^{1/4})$ and $g_S=\lambda(1-N)+\epsilon_S$;
  - the reduction-norm powers ($2-p=677/640$);
  - the gap-free static comparison with $A_*=(\zeta-X)_+$, which gives $4R|A-A_*|+|B-B_*|\le10R^2\mathfrak d$;
  - the background via PSE `conditional` with $w=1$.
  
  The .tex passes both escape scans.
- *Reviewer observation, for S5d.* WIT `uniformtheorem` gives $\mathcal E'\le-\tfrac34\gamma_0$ on $J_-$ and $\ge\tfrac34\gamma_0$ on $J_+$ in the limit. Since A-error-transfer is uniform at the $q^2$ scale, the original error therefore decreases by at least $(\tfrac38\gamma_0r-o(1))q^2$ across $J_-$ and increases by the same across $J_+$, giving a rebound of order $\gamma_0rq^2$ on the offset sector of $\mathcal P_*$ (physical width $2\delta_\zeta q$), with no rate transfer. The cluster source signs $D_1<0<D_2$ on J, part of Theorem A's statement, do need A-rate-transfer.
- *Remaining (1 session, possibly 2):* **S5d.** A-rate-transfer on WIT's J (sourcewise core field and reactions from FWC, CWI `rate` with $g_0=g_*/4$, background rate charges), then AN8: initialized Theorem A on $\mathcal P_*$ and the persistence corollary via LP `diagonal-transfer`. After that: S6 (exact lag, B-core) and S7/S8 (canonical regime).

**Status after RTA (`AN07_rate_transfer_and_assembly_v1`, S5d, Nov 2): closed. S5 (AN7) and AN8 are complete for the deep regime.**
- *Theorems:*
  - **Core gap** (`coregap`). Supremum core tracking $C_{\rm sup}q^{1/20}$, so every core label is at least $g_*/8$ from the probe gate on J.
  - **Rate transfer** (`ratetransfer`). On J, $|q^{-2}D_p^\tau-d_{p,\rho,\zeta}|\le\delta_J=O(q^{1/20})$ uniformly on $\mathcal P_*$.
  - **Learning** (`learning`). Responses and the 169/196 loss ratio, proved directly from full-output $L^2$ estimates, since WIT `staticproposition` does not apply.
  - **Theorem A** (`theoremA`) and **persistence** (`persistence`) as in Revision 1.27.
- *Checked (reviewer, Nov 2):*
  - **Pairwise core comparison.** $D^+|z_b-z_{b'}|\le L_F|z_b-z_{b'}|+2C_Fq^{1/10}$ in the same leading field, with FWC's pointwise value errors and receiver Lipschitz $\partial_1\mathsf F=(w-t)_+\phi(t)$; averaging gives sup tracking.
  - **Rate algebra.** The core rate expansion $f_{\mathcal K,1}=qA+O(q^3)$, $f_{\mathcal K,2}=q^2B+O(q^4)$ and $\xi_q=(\sin q\zeta,-\cos q\zeta)$ give $q^{-2}D_p=(A-\zeta)A_p+B_p+O(q^2)$, which matches WIT `generalrates` with the $1-M$ reaction kept.
  - **Rate margins.** $5/8-1/8=1/2$ for sources and $3/4-1/8=5/8$ for totals, with $\delta_J<\min(p_*/8,\gamma_0/16)$.
  - **Learning arithmetic.**
    - $f_0=S_0X/4$, since $\mathbb E[aa^T1\{a\cdot X>0\}]=I/4$.
    - $\|X\|_{P_p}^2=Q_p+q^2$.
    - With masses in $[1/4,5/4]$, $|1-M_p|\le3/4$; the condition $C_{\rm loss}q^{1/4}\le\tfrac{13}{320}\le\sqrt{Q_p}/16$ gives the residual ratio $(13/16)/(7/8)=13/14$.
  - **Rebound.** A drop of $3\gamma_0r/8$ across each half-window, less two endpoint errors of at most $\gamma_0r/16$ each, leaves $\gamma_0r/4$; both endpoints are excluded as minimizers.
  - **Persistence.** LP `diagonal-transfer`'s premise is FWC `errortransfer` for every finite T, with LPR's exact clearing.
  - **Escapes.** The .tex passes both escape scans.
- *The deep-regime chain.* Every increment from F/P through RB, WBR–WCS, CWI, PSE, FWC and RTA is now a proved conclusion with no retained hypothesis on its stated scope. The consolidation into a checkpoint 2.0 (with changelog and label map) awaits Tod's explicit approval, and preferably an independent read first.
- *Remaining:*
  - **S6 (next): original-flow B-core on WIT's windows.** P's exact factorizations evaluated for the original flow, with a signed exact lag and producer attribution.
  - **S7/S8:** bridge and canonical regime.

**Status after BC (`AN01_original_flow_bcore_v1`, S6 attempt 1, Nov 2): stopped; obstruction to my prompt's contract.**
- *Theorem* (`obstructiontheorem`). On $\mathcal P_*\times J$, $|q^{-2}r_2-\mathcal O_*|\le C_{\rm rem}q^{1/20}$ and $r_2\ge\tfrac12c_{\rm out}q^2$, with $c_{\rm out}=\tfrac{13g_*}{160}\delta_n\mathsf K(-7R/10)$ and $\delta_n=1/(1+e^{(49/100)(|s_*|+r)})$. Hence $|r_2|\le C_*q^{2+\kappa}$ is false for every $\kappa>0$.
- *Also closed* (`twoway`). $q^{-2}(H^{(1)}+H^{(2)})=(X_*-Y_*)x'_{2,*}+O(q^{1/20})$ for the full core input-rotation channel, and $q^{-2}D_2^\tau=(X_*-Y_*)x'_{2,*}+\mathcal O_*+O(q^{1/20})$.
- *Checked (reviewer, Nov 2):*
  - **Channels.** P `motion` gives three source channels: input $\int vc\,v_{\theta,p}$, output $\int zd\,v_{\psi,p}$ and radial $-\int2g_pzc$. P's $H^{(1)}+H^{(2)}$ is exactly the input channel, so $r_2$ = output + radial + non-core.
  - **Output limit.** On the core, $d=-e_\xi\cdot b^\perp=1+O(q^2)$, since $\xi_q\cdot b^\perp=-\cos(q(\zeta-y))$, and $v_{\psi,2}=qy'_2$ with $y'_2=\tfrac\rho2(1-N)\mathsf K(\rho x)+O(q^{1/10})$. Together these give $\mathcal O_*$.
  - **Agreement.** The two-channel form is WIT `generalrates`' $d_2$ at the atom (there $\zeta-A-y=X-Y$), and is P `pa:atomicrates`.
  - **Positivity.** $\mathsf K(-a)\ge\int_1^2u\phi(u+a)\,du\ge\tfrac32\phi(a+2)$; $\rho X_*\ge-7R/10$; $1-n_\rho\ge\delta_n$ on J; gap $\ge g_*/4$.
  - **Escapes.** The .tex passes both escape scans.
- *Reviewer analysis of the producers* (leading system, from P `pa:leading` and the cluster residuals; to verify in S6). On a strong receiver:
  - **Input velocity**, $2x'_2=\rho\phi(\rho x)-\rho\mathcal S(x)+\lambda[V+(1-c)y]\Phi(\rho x)$. The target supplies $\rho\phi(\rho x)+\lambda y\Phi$, the core $-\rho\mathcal S$, and the weak family $\lambda(V-cy)\Phi$, through its first output and its response.
  - **Output velocity**, $2y'_2=\rho(1-c)\mathsf K(\rho x)$. The target supplies $\rho\mathsf K$ and the weak response $-c\rho\mathsf K$.
  - **At the atom.** Target plus core equals $-\lambda(X-Y)\Phi$, so the harm's four parts are $W_{\rm in}=\tfrac\lambda2n(X-Y)(V-Y)\Phi$, $T_{\rm in}=-\tfrac\lambda2(X-Y)^2\Phi$, $T_{\rm out}=\tfrac\rho2(\zeta-X)\mathsf K$ and $W_{\rm out}=-\tfrac\rho2n(\zeta-X)\mathsf K$.
  - **Signs.** $T_{\rm in}\le0$, $T_{\rm out}>0$, $W_{\rm out}\le0$. The sign of $W_{\rm in}$ needs $X_*>Y_*$ and $V_*>Y_*$ on J; AN06 `regiontheorem` gives $y<x$ only for $s\le0$.
  - **Help.** It is the source-1 **output** channel: $B_0=(M/2)Q_1\bar z\bar d\,r_{21}$, with $\Lambda_1\approx Q_1r_{21}$ on the core, and the lag $L_0=Y+K_w$ has core and weak (cross-output leakage) parts. The source-1 input and radial channels carry $1-M=O(q^{11/10})$, so the original small-remainder contract should hold for $D_1$.
- *Next: S6 revised* (prompt in the v1.28 review). Channel-and-producer limits for both sources, the signed exact lag, help = exposure × lag, and the signs of the producer parts on J.

**Status after CPD (`AN01_channel_producer_decomposition_v1`, S6 revised, Nov 2): closed subset; one sign open.**

Notation: $A_*=\zeta-X$, $Z=X-Y$, $\Phi_x=\Phi(\rho X)$, $\mathsf K_x=\mathsf K(\rho X)$, $\mathsf K_u=\mathsf K(U)$, $n=n_\rho$.
- *Theorem* (`table`). Each exact channel divided by $q^2$ converges uniformly at $O(q^{1/20})$. The channels are $I_p=\int_Kvc\,v_{\theta,p}$, $O_p=\int_Kzd\,v_{\psi,p}$ and $P_p=-\int_Kh_pzc$, and the target, core and selected-weak producers contribute as follows:
  - **Source 1.** Input: $-ZX/2$, $ZX/2$, $0$. Output: $-A_*Y/2$, $0$, $-A_*n\mathsf K_u/2$. Radial: $-A_*Z$, $A_*Z$, $0$. So $I_1,P_1=O(q^{2+1/20})$, and the output total is $-A_*(Y+n\mathsf K_u)/2$.
  - **Source 2.** Input: $Z[\rho\phi(\rho X)+\lambda Y\Phi_x]/2$, $-Z\rho\mathsf K_x/2$, $Z\lambda n(V-Y)\Phi_x/2$. Output: $A_*\rho\mathsf K_x/2$, $0$, $-A_*\rho n\mathsf K_x/2$. Radial: all $0$.
  - **The rest.** $P_q\cup\Sigma$ costs $O(q^{1/8}+q^{\gamma_*/2})$ and B costs $O(q^{1/10})$. The non-core rate is $|D_{p,K^c}|\le Cq^2\epsilon_{\rm bg}$.
- *Theorem* (`help`). $\mathcal L_q=Y+n\mathsf K(U)+O(q^{1/20})$ and $L_0\ge c_L=5p_*/[4(7/4+R)]$. $q^{-2}D_1^\tau=-\tfrac12\mathcal A_q\mathcal L_q+O(q^{1/20})$ with $\mathcal A_q=\int_K(\zeta-x)\,d\mu\ge g_*/16$, and the error is at most $g_*c_L/64$. P's $q^{-2}B_0=\tfrac12\mathcal A_q\mathcal L_q+O(q^2+q\epsilon_{\rm bg})$.
- *Signs* (Section 4). $T_{\rm in}=-\tfrac\lambda2Z^2\Phi_x\le0$; $T_{\rm out}=\tfrac\rho2A_*\mathsf K_x>0$; $W_{\rm out}=-nT_{\rm out}<0$; $W_{\rm in}=\tfrac\lambda2nZ(V-Y)\Phi_x>0$ on $J\cap(-\infty,0]$. Strict limiting signs transfer to the original producer contributions for small q.
- *Open* (`missing`). At a zero of $z=X-Y$ after half mass, $2z'=\lambda n(V-Y)\Phi(\rho Y)+T$ with $T=Y+n\mathsf K(U)-\rho(1-n)\mathsf K(\rho X)=-2Y'$. The proof needs $T>-\lambda n(V-Y)\Phi(\rho Y)$ there. This is an unresolved comparison, not a counterexample.
- *Checked (reviewer, Nov 2):*
  - **Donor Gaussian tables.** I re-derived all 18 entries with:
    - data $(1+qZ_1,qZ_2)$ on $P_1$ and $(qZ_1,\rho+qZ_2)$ on $P_2$, with $a^\perp\approx(-qx,1)$ and $b^\perp\approx(-qy,1)$;
    - core donor output $Mb_Y(a_X\cdot X)_+$;
    - weak donor output $(0,qN(Z_2+U)_+)$ on $P_1$ and $(-qN\rho V,NX_2)$ on $P_2$.
    The core's own output entry $M(y-Y)$ vanishes at the atom because $b^\perp\cdot b_Y=\sin(q(Y-y))$. The source-2 rows reproduce WIT `popsystem`, with $F(t,r)=\phi(\min)+r\Phi(\min)$.
  - **Channel weights.** On the core, $c=q(\zeta-\mathcal A-y)$, $d=1$, $z=q(\zeta-x)$ and $v=1$ to leading order. So the normalized integrands are $(\zeta-\mathcal A-y)x'_p$, $(\zeta-x)y'_p$ and $-h_p(\zeta-x)(\zeta-\mathcal A-y)$, and at the atom $\zeta-\mathcal A-Y\to Z$.
  - **$T_{\rm in}$.** Target plus core is $Z[\rho\phi+\lambda Y\Phi-\rho\mathsf K(\rho X)]/2=-\lambda Z^2\Phi/2$, by $\mathsf K(t)=\phi(t)+t\Phi(t)$.
  - **Totals.** The input total $\tfrac\lambda2Z\Phi[nV-X+(1-n)Y]$ plus the output total $(1-n)T_{\rm out}$ is WIT's $d_2$ and BC's $\mathcal O_*$. The source-1 totals are WIT `popsystem`'s $x'_1,y'_1$ and $d_1=-\tfrac12A_*L$.
  - **Weak lag coefficient.** $a_w\cdot X=q(w+G)$ with G standard normal on $P_1$, so by Stein $\mathbb E[(a_w\cdot X)_+X_1]=q\mathsf K(w)+q^2\sin(qu)\Phi(w)$ exactly. The $O(q^{2-p})$ charge uses the bounded second moment and sup $O(q^{-p})$.
  - **Lag lower bound and margin.** $c_L$ follows from WIT's $d_{1,*}\le-5p_*/8$ and $A_*\le7/4+R$. With $\mathcal A_q\ge g_*/16$ and $\mathcal L_q\ge c_L/2$, the leading help is at least $g_*c_L/64$.
  - **Invariants.** $V>0$, $V>Y$, $V>X$ re-derived from WIT `orbit`. At $V=X$ one has $X=V>Y$, so the $(1-n)(X-Y)\Phi$ term is positive.
  - **The stop is real.** WIT's $z=0$ check uses $T>0$, which is proved only under $n\le1/2$ (via $P\le71/100$, $Q\ge1/2$, $v-y\le8/5$ and the $x=3/4$ boundary). WIT `commonwindows` gives $s_*>s_a=-\tfrac94\log3$ and nothing about the sign of $s_*+r$.
  - **Escapes and prefix.** The .tex passes both escape scans; prefix `an01cpdv1:` is unique.
- *Reviewer reduction for S6c* (unverified; for the session to check). At a zero of z with $n\ge1/2$, drop $\lambda n\Phi(V-Y)>0$. Use $Y(1-(1-n)\lambda\Phi)\ge0$ when $Y\ge0$, and $\rho\mathsf K(\rho Y)\le\rho\phi(0)<7/25$ when $Y<0$. Then
  $$2z'>n[\mathsf K(U)-7/25]-Y_-,\qquad Y_-=\max(-Y,0).$$
  So $U\ge0$ and $Y\ge0$ at the crossing suffice, since $\mathsf K(0)=\phi(0)>3/8$. Also, at $u=0$, $u'=\tfrac12[(1-n)\phi(0)-y/2]$, which is inward whenever $y<2(1-n)\phi(0)$.
- *Remaining:*
  - **S6c (next):** $X>Y$ on $[0,\sup J]$, or the largest analytic closed subset.
  - **Consolidation** (checkpoint 2.0) awaits Tod's approval.
  - **S7/S8.**

### S6. The exact finite-noise lag (AN1)

**Claim.** The original-flow help channel $D_1^{\rm phys}/(\mu_1^2q^2)=-\tfrac12A_{q,\xi}L^{\rm mean}_{1,q}+\text{remainder}$, with the remainder smaller than the lag's signed margin on the learned windows, and a positive-lag estimate for the exact lag.

**Route.** Start from the exact Stein relation and P's lag-tracking identity. Transfer the leading positive-lag forcing (symmetrized $\Xi>0$) with remainders measured relative to the lag, not in absolute $O(q^2)$, since the lag is a small cancellation at canonical noise.

**Unlocks.** B-core in the original flow: help = exposure × signed exact lag, harm = producer-attributed input rotation. *(Corrected in v1.28–1.29: harm has input and output channels at leading order. See "Status after CPD".)*

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
| II | S2 capped gain + S3 field contract | Mutually dependent (ledger 16). CFR has proved the primary and radial parts of S3. DECG has proved the chart envelope, the radial bound and the conditional gain. GESG has proved the global envelope and the Q3 interior. **S2CP closes S2 and CFA closes S3, both in stopped-guard form, with a conditional CLOCK passage.** Only the Q3 strip budget remains external. Q3SB proved the pre-entry inputs, PISB paid the π strip and the frozen zones, and **LSB paid $J_3$; the strips are complete**. WPT assembled a two-boundary theorem, and **RB proved the response barrier: the deep-regime weak passage is a theorem.** Track II is complete; next is S4 (track III). |
| III | S0 + S4 weak return/matching | S0 is now unconditional inside the completed weak passage. S4a (SI) completed the hypothesis inventory and stopped at the original weak input return. **S4b (WBR) proved that return** for the whole clock, up to a fixed level. **S4c (MP) closed the matching package** (population accounting, logistic phase, $A_0$, mass defects). **S4d (SRR) closed the strong-reference reduction**, and **S4e (WCS) closed the weak-chart reduction and selection**: $E_s(t_n)+W_2(t_n)=O_n(q^{1/20})$ at a fixed small weak mass. **Track III is complete.** |
| IV | S6 exact lag | Needed for B-core. Attempt 1 (BC) stopped at a wrong remainder contract and closed the two-channel identity for $D_2$. **CPD (S6 revised) closed the channel and producer tables, the signed exact lag and the help law**, and the four-part harm identity with every sign except $W_{\rm in}$ after half mass. **Next: S6c,** the post-half-mass input sign. |
| V | S7 + S8 bridge and canonical entry | Bottleneck for explaining the empirics. Start with the quantile formulation. |
| — | S5 AN7 | Assembles I–IV. Error transfer on every fixed window, not only the crossing windows. Starts from WCS's state at $t_n$. **S5a (CWI) done:** interface, exact precision criterion, leading first-moment extension. **S5b (PSE) closed:** background paid on the passage; full error and rates match at every fixed level $n'\le n$, so A-error-transfer holds on windows inside $(-\infty,s_n]$. **S5c (FWC) closed:** continuation by combined transverse energy; **A-error-transfer on every fixed window**. **S5d (RTA) closed:** rate transfer on J; **initialized Theorem A and persistence**. |

**Dependency sketch**

```text
S0 ──┐
S1 ──┼──> S2, S3 ──> c-passage (CLOCK) ──┐
     └──> S4b return ──> S4c matching ──> S4d–e selection ───┤
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
21. **Missed domain hypothesis and wrong clock formula (WPT prompt).**
    - Roadmap v1.16 said every guard had a strict improvement and no external input remained. But every source (LCRC, RCET, BULK, S2CP, CFA, CLOCK) assumes $0\le c\le c_b$, and my guard list stopped only at the upper boundary. The response c is a signed regression coefficient, and nothing proves $c\ge0$.
    - My prompt asked for $t_b-t_0=[\log(c_b/H_0)+O(1)]/(Q(1-c_b))$ as an asymptotic equality. The exact identity $t-t_0=[\log(H/H_0)-\delta]/Q+\int c$ with $\int c=O(c_b)$ gives denominator Q. The $Q(1-c_b)$ form is only an upper bound.
    - *Rule:* before declaring an assembly complete, list every hypothesis of every cited theorem, including sign and range conditions on observables, not only the guards the roadmap tracks.
22. **Size taken for sign, and an unreached chart assumed (S4 section since v1, the v1.18 plan, the S4a prompt).** SI corrected all of these.
    - *Size is not sign.* The S4 `Observation` said that once BULK's ratio satisfies $qj/z\lesssim q^2$, u is bounded, and since labels arrive from the strong side, $u\ge0$. BULK bounds |u|, not its sign: the balanced state $U=W=\sqrt m(-\sin q,\cos q)$ meets every BULK condition and has $u=-1$.
    - *The bounded chart is never reached.* The $q^2$ floor is not reached inside the passage. At a fixed clock level, $|u|\le Cq^{-p_b}$ with $p_b\ge69/160$.
    - *Chart-specific errors.* So the "bounded-chart $O(q^2)$ weak field" and "$N_{\rm cohort}=H_{\rm cohort}(1+O(q^2))$" do not apply in the passage. On a growing chart the mass error is $O(q^2L^2)$.
    - *Conflated levels.* v1.18 said $n_b\le c_b/2$ puts $t_{n_b}$ before $t_b$. This conflated the leading N with the clock H, and RB gives only $H(t_b)\ge c_Hc_b$.
    - *Wrong phase quantity.* I asked for an "$o(1)$ phase through the clock H". The logistic phase actually needs the signed $\int(N-c)\to0$.
    - *Rules:*
      - A size or norm bound is not a sign. If a quantity's leading value is $O(q)$ and its error bound is also $O(q)$, then dividing by q leaves an order-one remainder of unknown sign. The sign must come from computing the signed leading term.
      - Before using a chart's error orders, check that the chart is actually reached on the interval.
23. **Regime-crossing and budget-type errors (my S4d draft prompt; found in the reviewer audit of Oct 30, before the run).**
    - *A rate outside its regime.* Step 5 applied WEAK's $-gI$ rate on $[t_0,t_s]$. That bound is proved only on the 2δ box, at $M=1$, for $N\le n_b$. The inequality proved there is CFA `localineq`, with rate $g_c=\gamma_*/2$ and target $(a,a)$, uniform in $\widetilde M$ (ledger 13).
    - *An object outside its domain.* It used the logistic N before $t_s$, where N is not defined and MP's estimates do not hold. Before $t_s$ the right quantity is the clock, $H<q^{1/8}$.
    - *The wrong budget type.* It allowed CFA's integrated budgets as $d_0$ sources, but TAILREP's $d_0$ is a pointwise constant shared by both error inequalities.
    - *A mass bound used as a field bound.* It charged non-selected weak senders by MP's mass bound. MP itself says that bound does not control field costs divided by q.
    - *A missing moment and a misstated risk.* It listed only $P_1$ weak moments and omitted the $P_2$ moment $V_O$. It also described the $C_0E_g$ risk as $O(h)$. In fact the integrated primary part is small but fixed, and pointwise it is $\mu_{G_+}\mathcal T$, which is superpolynomially small after $t_s$.
    - *Rules:*
      - Use a rate or estimate only on the box, mass range and interval where it was proved. Across a regime boundary, use the earlier regime's inequality and match at the boundary.
      - An integrated budget is not a pointwise $d_0$ source.
      - Charge a population's field by its mass only when its per-mass field is bounded on a reached chart; otherwise use transverse energy.
24. **Coefficient slip (my corrected S4d prompt).** Step 5 said $c\le C(H+q^2)$ while also listing $c_{\mathcal B}\le C\mu_{\mathcal B}$. RB's guard gives only $\mu_{\mathcal B}\le q^{11/10}$, which is not $O(q^2)$. SRR kept $c\le C(H+q^2+\mu_{\mathcal B})$, and the conclusion is unaffected. The same prompt also asked for $H_{G_+}\lesssim H$ before $t_s$ to be checked through RCET; RB `primaryclock` already proves it on the whole passage. *Rule:* as in item 19, do not absorb a term into a smaller power without the inequality that justifies it, and cite the proved conclusion rather than re-deriving it.
25. **Eaten TeX escapes (artifact; found while reviewing SRR).** In some delivered files a backslash escape became a control character: `\r` became CR or LF (from `\rm`), `\t` became TAB (from `\tfrac`), and one `\qquad` lost its backslash. TeX compiles these without warnings, so compile checks miss them, but the typeset formulas read wrong (for example "−frac12Q(1−2c)").
    - *Locations:*
      - SRR (committed unchanged): lines 323–324 (`d_{\rm ph}`);
      - SI: line 319;
      - WPT: lines 465 and 475;
      - RB: lines 335, 429, 513, 515 (also `qquad`) and 516;
      - GESG: lines 231 and 238;
      - LSB: line 181.
      - Dropped `\q` (`\quad` printed as "quad"; added Nov 2): RB lines 106, 107, 108 and 111 (twice); LSB line 214.
    - These are typesetting defects only; no statement's mathematics changes. Prior increments are frozen, so they are recorded here rather than edited. Fix them only by an explicitly approved errata-only commit.
    - *Rule:* before delivery, every work session scans its .tex with `grep -nP '[\x00-\x09\x0b-\x1f]'` and with `grep -nP '(?<![\\A-Za-z])q{1,2}uad(?![a-z])'` (a backslash dropped without a control character), and checks that `\rm`, `\tfrac`, `\qquad` and `\text` survive.
26. **An integration-by-parts instruction that does not extend (my S4e prompt).** I asked S4e to extend WBR's integration by parts in $X_1$ from $u=0$ to the whole chart. At $u\ne0$ the $P_1$ receiver gate $\{a\cdot X>0\}$ depends on $X_1$, so integrating by parts in $X_1$ would differentiate the gate. WCS used instead the rotated variable $Z_\perp=c_uZ_1-s_uZ_2$, which is tangent to the gate's level sets and equals $Z_1$ at $u=0$. WCS also avoided a spurious inadmissible term $q^2|v|u^3$ by using Gaussian saturation in place of a global Lipschitz bound.
    - *Rules:*
      - Integrate by parts only in a variable on which the receiver gate does not depend; at a general receiver this is the direction tangent to the gate's level set.
      - Before declaring a growth term inadmissible, bound it using the Gaussian factor it carries (a polynomial times a Gaussian is bounded), not a global Lipschitz constant.
27. **Activity and precision misstatements (my S5a prompt and the v1.23 S5 plan).** CWI corrected all four.
    - *A sign claim stated for both signs of a parameter.* I asked for Q2 inactivity for all $|\zeta|\le R$. For $\zeta<0$ the label at $\theta=\pi$ is active, since its input is $-\sin(q\zeta)>0$. WIT's offsets are positive, so nothing downstream breaks.
    - *Ancestry taken for current angle.* I wrote that "the whole weak family" is probe-inactive. Inactivity is proved only for $G_+$ (S and $P_q$), via the late RCET ratio. Recruited Σ labels can sit in the strong chart or on the lower side.
    - *Mass used as the precision measure.* Risk 2 compared outside masses with $q^2$. The exact criterion is the mass-weighted squared active input $\mathcal Q_T$; mass is only an upper bound.
    - *A sign offered as payment.* I suggested the aligned contribution being $\le0$ might help. A one-signed term still needs two-sided $o(q^2)$ precision.
    - *Rules:*
      - Classify activity by current angle, not ancestry, and check every sign claim at both signs of each parameter.
      - State a precision requirement in the exact observable, not in a majorant such as mass.
      - A one-signed contribution is not paid by its sign.
28. **A circular continuation order (my S5c prompt).** I suggested reducing the cross residuals to "the transverse energy J, the core chart and the outside masses". But continuing the core chart itself needs O(q) cross residuals, so that chain is circular. FWC closed it with a single combined energy $\mathcal Z=E_{\mathcal K}+J_G$, whose inequality uses only the a priori total-mass bound. The other bounds then follow in a fixed order.
    - *Rule:* when continuing coupled bounds, look for one quantity whose differential inequality uses only a priori bounds, and derive the rest from it in a stated non-circular order. Choose each guard constant only after the bound it depends on.
29. **A remainder that is not small (my S6 prompt).** I asked for every remainder in P's factorizations to be $O(q^{2+\kappa})$. P's $r_2$ is defined as everything in $D_2$ except core input rotation, so it contains the core's cluster-2 output rotation, which is of order $q^2$ and strictly positive on J. P `pa:atomicrates` already says so, and my own Goal (4) listed that channel separately, so the prompt contradicted itself. BC proved the obstruction and stopped correctly.
    - *Rule:* a remainder is a name, not a size. Before demanding that a remainder be small, compute its leading term on the comparator orbit.
30. **A sign hidden in a range bound (my S6-revised prompt).** I offered $L_0\ge5p_*/7$ from $\zeta-X_*\le7/4$. That bound needs $X_*\ge0$ on J, which is not proved. CPD used $A_*\le7/4+R$ and $c_L=5p_*/[4(7/4+R)]$ instead.
    - *Rule:* bounding a difference by an endpoint is a sign claim on the subtracted term. Check that sign, on the whole window, before using the bound.
31. **Regression contributor vs. channel producer (my S6-revised prompt and v1.28).** I called $L_0=Y+n\mathsf K(U)$ the lag's "producer split", core plus weak. But in the moving help channel the core's own output contribution is zero at the atom; the target residual supplies $-A_*Y/2$ and the selected weak $-A_*n\mathsf K(U)/2$. The core and weak terms are regression moments of the fitted output, not producers of motion. CPD kept the two indices separate.
    - *Rule:* a moment's contributors and a channel's producers are different decompositions. Do not carry an attribution from one to the other.

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
| WEAK | `AN03_weak_transit_forcing_and_orbit_selection_v1.tex` (+ review), prefix `inc:AN03:weak:v1:` |
| TAILREP | `AN03_mass_charged_tail_and_selection_defects_v1.tex` (+ review), prefix `inc:AN03:tailrepair:v1:` |
| BULK | `AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` (+ review), prefix `inc:AN03:bulkclock:v1:` |
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
| WPT | `AN03_weak_passage_theorem_v1.tex` (+ review), prefix `an03wptv1:` — two-boundary theorem with all non-response guards improved; stops at the lower response barrier $c\ge0$; corrects the hitting-time denominator |
| RB | `AN03_response_barrier_v1.tex` (+ review), prefix `an03rbv1:` — **response barrier; completed initialized deep-regime weak-passage theorem**; $H(t_b)\asymp c_b$, exact time relation, S4 handoff |
| SI | `AN03_selection_interface_v1.tex` (+ review), prefix `an03siv1:` — S4a, partial: full selection-hypothesis inventory with exact constants; core donor moments; BULK size in weak coordinates ($p_b$); growing-chart mass relation and logistic phase identity. Stops at the original weak-return margin. |
| WBR | `AN03_weak_boundary_return_v1.tex` (+ review), prefix `an03wbrv1:` — S4b, closed: exact weak-boundary moments; one-sided weak feedback by energy; pointwise strong-mass rate; $O(q)$ clock alignment; original input return of the whole clock to a fixed level |
| MP | `AN03_matching_package_v1.tex` (+ review), prefix `an03mpv1:` — S4c, closed: population accounting (band $\asymp q^{1/4}$); response $c=H(1+O(q^{1/4}))+O(q^2)$; uniform $o(1)$ logistic phase; $J_S\le C(q^3+q^2H)$; $A_0=O(q^{1/16})$ ($p=2$); late mass-defect budgets |
| SRR | `AN03_strong_reference_reduction_v1.tex` (+ review), prefix `an03srrv1:` — S4d, closed: CFA's actual reference in TAILREP `strongerror` form on $[t_s,t_n]$ ($g_W=\gamma/2$, $C_s=980$, pointwise $d_0^{(s)}=O(q^{1/20})$); $E_0=O(q^{1/20})$ via CFA `localineq` before $t_s$; superpolynomial late primary tail; fixed-label $W_2$ convention and weight value conversion; explicit δ and h bound |
| WCS | `AN03_weak_chart_selection_v1.tex` (+ review), prefix `an03wcsv1:` — S4e, closed: exact weak-receiver velocities by tangent Gaussian integration by parts; growing-chart value reduction with admissible linear/cubic growth; value-only weak error form ($C_w=20$, $d_0^{(w)}=O(q^{1/20})$, $L_*=1$); explicit level n with $\Theta\le1/8$; **initialized $L^2$ selection** $E_s(t_n)+W_2(t_n)=O_n(q^{1/20})$; S5 handoff |
| CWI | `07_compact_windows_AN07/AN07_compact_window_interface_v1.tex` (+ review), prefix `an07cwiv1:` — S5a, audit: consumer interface; centering $\tau_h$ and time units; exact probe-activity classification; precision criterion $\mathcal Q_{\Sigma\cup\mathcal B}=o(q^2)$ with paid and unpaid cohorts; core entry error and rates; outside rate charge; leading WIT extension with strong-only compact support |
| PSE | `07_compact_windows_AN07/AN07_probe_sector_energy_v1.tex` (+ review), prefix `an07psev1:` — S5b, closed: lower-half transverse energy $\mathfrak E_T$ on $[0,t_b]$; backward pre-entry mass comparison ($e^5$); background $\mathcal Q_{\Sigma\cup\mathcal B}=O(q^2\epsilon_{\rm bg})$; full error and source-rate comparison at every fixed level $n'\le n$; conditional continuation criterion for S5c |
| FWC | `07_compact_windows_AN07/AN07_finite_window_continuation_v1.tex` (+ review), prefix `an07fwcv1:` — S5c, closed: combined transverse energy continuation from $t_n$ (cross residuals, alignment, charts, primary inactivity, physical mass laws) with no passage guard; sourcewise core and signed weak value reductions; perturbed first-moment propagation with current weights; gap-free static comparison; **A-error-transfer on every fixed centered window**; LP `compact-transfer` |
| RTA | `07_compact_windows_AN07/AN07_rate_transfer_and_assembly_v1.tex` (+ review), prefix `an07rtav1:` — S5d, closed: sup core tracking and strict probe gap; A-rate-transfer on WIT's J; direct learning (responses, 169/196 loss ratio); **initialized Theorem A** on $\mathcal P_*$ ($S_0=q^{10}$); **initialized persistence** on a diverging horizon; dependency ledger and S6 handoff |
| BC | `08_mechanism_AN01/AN01_original_flow_bcore_v1.tex` (+ review), prefix `an01bcv1:` — S6 attempt 1, obstruction increment: P's $r_2$ contains the positive cluster-2 output-rotation term $q^2\mathcal O_*$ on J, so a small-remainder contract for $D_2$ is false; closed two-channel identity for $D_2$ |
| CPD | `08_mechanism_AN01/AN01_channel_producer_decomposition_v1.tex` (+ review), prefix `an01cpdv1:` — S6 revised, closed subset: input/output/radial channel limits for both sources with fixed-label producer tables; signed exact lag $\mathcal L_q=Y+n\mathsf K(U)+O(q^{1/20})\ge c_L$; help = exposure × lag; four-part harm identity with signs, $W_{\rm in}>0$ only on $J\cap(-\infty,0]$; corrected Theorem B item 3 |
| SGWR | `SIGNED_GROWTH_WEAK_RETENTION_v1.tex` |
| WIT | `AN06_learned_orbit_witnesses_v2.tex` |
| LP | `LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex` |
| LPR | `LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex` |
| Support | `SCALED_POPULATION_SPLITTING_THEORY.md`, `TWO_NEURON_SMALL_NOISE_LIMIT.md`, `LEAK_COMPENSATION_FACTORIZATION_AUDIT.md`, `SIM.md`, `main-15.tex`, frozen appendix, `theorem_A_initialized_escape.pdf` (Sections 1–3 only) |

**Workflow.** Each new result goes in a separate versioned `.tex` with a same-stem review note. Nothing is merged into the checkpoint without explicit approval. GitHub is read-only, and only when the user asks; Tod makes all commits. No new experiments by default, no computer-assisted certificates.