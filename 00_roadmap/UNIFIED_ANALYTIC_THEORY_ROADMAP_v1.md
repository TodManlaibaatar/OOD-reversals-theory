# Roadmap to a unified analytic theory of the ReLU SIM reversal mechanism

**Version 1.2 — October 6, 2026.** Working roadmap, not a proof and not a merge instruction. No source increment, foundations file, or checkpoint is modified by this document. It supersedes the "recommended next task" parts of `THEORY_HANDOFF_ANALYTICAL_A_B_v2.md` (H2) only where explicitly stated; H2's ground rules, file contracts, and withdrawn-claims ledger remain in force.

**Revision 1.1 (Oct 6).** Records RCET (`AN03_residual_closure_and_eta0_transport_v1`). S0 is rewritten: the v1 scalar fixed point was invalid (it dropped a regenerated $LH$ term), RCET's Volterra closure is conditional on a clock premise, and a candidate repair (Route 3) is described. S4's primary-band bullets are marked proved, with the endpoint-regularized dichotomy. New ledger items 9–11; file map updated.

**Revision 1.2 (Oct 6).** Records LCRC (`AN03_ledger_cap_residual_closure_v1`). Route 3 is proved: S0 is closed as a conditional original-flow implication, with no clock premise and no terminal cap. S0 now lists the assembly requirements its retained inputs must meet.

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
1. *Overlap window.* At κ=10, all right-half-circle labels are in the strong chart by $(2/\omega)\log(1/q)\le 7.85\log(1/q)$. At that time $S\lesssim S_0e^{(1+2q^2)t}=q^{\kappa-2/\omega+o(1)}\ll\delta$. So there is a window where the early original-to-target comparison is still valid **and** the population is already charted. Transfer the PROFILE entry state to the original flow there.
2. *Leading strong system in $M$.* From $M\approx\delta$ to $M\to1$, with $N\approx0$, run an $M$-clock version of LOC: fixed core, same-field reference, collective block $J_M$. **LOC Lemma 3.1 already proves $J_M\preceq J_1$ uniformly for $0\le M\le1$**, and the centered shape rate is $-(1-M)/2+\alpha$. The multiplier is $(M_1/M_0)^{\alpha-1/2}((1-M_0)/(1-M_1))^{\alpha}$, reproducing $\epsilon\asymp q^{-s}S_0^{1/2-\alpha}$ with no double counting of contraction.
3. *Finite-noise field in the strong chart.* Prove the original-to-leading field error is $O(q^2)$ in value and receiver derivative on bounded scaled charts. Accumulated relative-weight drift is then $O(q^2\log(1/S_0))=O(q^2\kappa\log(1/q))\to0$.
4. *Labels outside the chart.* Charge them by mass with the PROFILE $\mu/q$ cost, as in S2.
5. *Strong-learning integrability.* $\int(1-M)=\log(M_1/M_0)$ in the leading law, plus the $O(q^2\log)$ defect.

**Pitfalls.** An $O(\delta)$ early-comparison error is not $O(q)$; the target-only profile beyond $S\sim\delta$ is not a valid description of the trained flow; the center is $a_q$, not $a_\rho$.

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

### S3. The c-form field contract

**Claim.** The original strong field has CLOCK's c-form with a remainder controlled in value and receiver derivative, including the selected-residual term $\mathbb E_{P_2}[g_2X_2\mathbf 1_{\{a^\top X>0\}}]$, the outside population, and the $M-1$ terms.

**Suggested route.** On $P_2$, the charted weak output is $f_2=N X_2+O(q^2)$. So the selected defect reduces to $(c-N_{\rm chart})\,\mathbb E[X_2^2\mathbf 1]$ (CLOCK §6 identity), plus transit-cohort cross outputs (BULK forcing bound), plus $\mu_B/q$ from the complement. The task is then $|c-N_{\rm chart}|$ small, which follows from the response ledger once transit and complement responses are bounded.

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
| I | S1 strong-stage tracking | Bottleneck for Theorem A. Start with the overlap-window transfer and the $M$-clock LOC. |
| II | S2 capped gain + S3 field contract | Share the c-form envelope; S2 closes two tail estimates. |
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
| SGWR | `SIGNED_GROWTH_WEAK_RETENTION_v1.tex` |
| WIT | `AN06_learned_orbit_witnesses_v2.tex` |
| LP | `LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex` |
| LPR | `LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex` |
| Support | `SCALED_POPULATION_SPLITTING_THEORY.md`, `TWO_NEURON_SMALL_NOISE_LIMIT.md`, `LEAK_COMPENSATION_FACTORIZATION_AUDIT.md`, `SIM.md`, `main-15.tex`, frozen appendix, `theorem_A_initialized_escape.pdf` (Sections 1–3 only) |

**Workflow.** Each new result goes in a separate versioned `.tex` with a same-stem review note. Nothing is merged into the checkpoint without explicit approval. GitHub is read-only, and only when the user asks; Tod makes all commits. No new experiments by default, no computer-assisted certificates.