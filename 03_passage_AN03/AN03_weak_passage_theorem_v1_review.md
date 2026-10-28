# Review: AN03_weak_passage_theorem_v1

New prefix: `an03wptv1:`. Source snapshot: roadmap v1.16 and the file blobs listed below.

## Status: the requested upper-boundary theorem is stopped

The joint audit finds one unmatched source hypothesis: **preservation of nonnegative response**. LCRC, RCET, BULK, S2CP, CFA and CLOCK explicitly assume \(0\le c\le c_b\). Their conclusions do not prove the lower inequality. The proposed first-exit list and duration argument do not exclude departure through the lower response boundary.

This is a gap in the assembly from the cited results, **not** a counterexample to positivity of the initialized response. No new positivity assumption is added to a claimed full weak-passage theorem. The supplied TeX instead proves a narrower, initialized two-boundary theorem and stops at the exact missing barrier.

Strict positivity is not imposed as an unnecessarily strong contract: touching zero and remaining nonnegative would be acceptable. The exact missing domain condition is

\[
\boxed{c(t)\ge0\quad\text{for }t_0\le t\le\min(t_+,t_0+20\ell),
\qquad t_+=\inf\{t\ge t_0:c(t)=c_b\}.}
\]

Excluding the first zero \(t_-\le t_+\) would be one sufficient way to supply it, but is not necessary if a valid nonnegative invariant-region argument permits touching.

## The theorem actually proved

For the original initialized flow at \(\kappa=10\), uniformly on \(\rho\in[13/20,7/10]\), fix the constants in CFA's acyclic order, with \(L_T=20\), \(b_B(q)=q^{1/10}\), \(M_K=2\), \(E_g=2c_b\), and sufficiently small fixed \(c_b,C_0\). Let

\[
t_-:=\inf\{t\ge t_0:c(t)=0\},\qquad
t_+:=\inf\{t\ge t_0:c(t)=c_b\},\qquad
\tau=\min(t_-,t_+).
\]

Then \(c(t_0)=a_\rho^2q^2/(2\lambda)+o(q^2)>0\), and
\(t_0<\tau<t_0+20\ell\). On \([t_0,\tau]\):

- The diagonal residuals are bounded; cross residuals are at most \(M_{res}q/2\); \(J_G\le K_Y^2q^2/4\).
- \(\int|1-\kappa_1|\le\log2+o(1)\), \(\int r\le C_r\log2+o(1)\), and \(\mu_K\le e^{d_q}=1+o(1)\).
- \(H\le H_{G+}\le(9/8)c_b+o(1)\), \(E_{G+}\le(5/4)c_b+o(1)\), and \(E_\Sigma\le C_\Sigma(q^5+q^{\Gamma_\nu}H)\).
- The core stays in its fixed chart, with \(r_K=O(q^{1/20})\) and \(e\le3e_*/4\).
- The strong-complement and outside estimates have the explicit positive powers in `an03wptv1:outside`; both their supremum and integrated \(\mu/q\) budgets are controlled.
- CFA's canonical remainder satisfies \(\int\epsilon_F\le C_FC_{L_c}C_{RCET}C_0E_g+o(1)<\bar F_F/2\), and \(\int f_*\le e_*/(4C_{pass})\), with \(1/Q\) retained in the response budget.
- The actual clock has subinterval defect \(O(q^{1/8}+q^2\ell)=o(1)\). The eta-zero group's distortion is only fixed \(e^{O(C_0)}\), as appropriate.

The theorem does not choose between \(c(\tau)=0\) and \(c(\tau)=c_b\). All claims advertised specifically at \(t_b=t_+\) remain blocked by the missing response barrier.

The quantity \(\log2+o(1)\) is an **upper budget** for the learning integral. Equality of that integral with \(\log2+o(1)\) is not asserted at a possible early lower-boundary stop.

## Task status

| Requested task | Status | Exact boundary |
|---|---|---|
| 1. Constants, guards, strict entry, continuity | **Closed** for the explicit joint domain, including a short signed entry check | Entry response is positive; this does not establish future nonnegativity. |
| 2. Strict improvements | **Closed for every listed non-response guard; partial for full continuation** | The domain hypothesis \(c\ge0\) has no matched improving/barrier source. |
| 3. Duration | **Closed for the two-boundary theorem; stopped for guaranteed upper arrival** | A trajectory cannot stay in \([0,c_b]\) for \(20\ell\), but it could leave through zero. |
| 4. Conclusions and handoff | **Closed at \(\tau\); stopped at the requested \(t_b\)** | Need the boxed response barrier. The proposed hitting-time equality also has the wrong leading denominator at fixed \(c_b>0\). |

## Hypothesis-matching table

All source applications below take place on **one joint stopped interval**. Its domain includes \(0\le c\le c_b\); this is explicitly retained until the lower-boundary issue is resolved. The non-response improvements are evaluated before taking any first-exit contradiction.

| Guard or input | Improving source | Its hypotheses | Where supplied; independence/slack |
|---|---|---|---|
| Diagonal residual norms | Foundational dissipation, as used by LCRC | Initialized finite loss | Original initialization. No future guard used. |
| Primary signs, ratios, backward estimate | LCRC `localclock`; RCET Thm 2.1; BULK Thm 4.1 | Fixed entry cohorts, positive entry z, Cartesian ratios, response domain, duration, cross residual, \(\int r\le B\), diagonal loss bounds | Q2EC/Q2EP entries and current guards. No EΣ conclusion, terminal cap, or independent clock premise is used. LCRC's conservative correction to RCET's y-comparison is retained. |
| Signed gate budget | S2CP `gate` | The preceding localclock conclusions, temporary secondary guard, core chart/mass, outside supremum, residual and duration guards | All are current guards or just-proved localclock conclusions. Its leading coefficient is independent of the temporary secondary constant. |
| EΣ guard | S2CP Theorem `S2`, using DECG local distance/gain and GESG splice | Coarse c-form value/derivative guard, bounded actual reference, gate budget, S1 profiles, clock seed and residual guards | Canonical field remainder guard supplies the field; current e guard supplies reference; SEP supplies Sigma profile; MOMC supplies strong tail. Output CΣ is selected independently of the temporary factor-two guard coefficient. Improvement to CΣ rather than 2CΣ. |
| Learning budget needed by LCRC | S2CP Proposition `Bs` | Current core geometry and mass bound, current residual/energy/outside guards, core entry mass | Core state guards; MOMC entry tail; current EΣ bound or temporary bound for E_G. Gives \(\int|1-\kappa_1|\le\log2+o(1)<B_s^0\). This does not first assume future core retention. |
| \(\mu_K<M_K=2\) | S2CP Bs positive-part identity | Same inputs as above | \((\log\mu_K)_++\int(\mu_K-1)_+\le d_q=o(1)\), hence \(\mu_K\le e^{d_q}<3/2\). No smallness of a core-mass guard is used to select itself. |
| \(E_{G+}<E_g=2c_b\) | LCRC `pointcap`, after S2CP energy conclusion | Sign-good G+, response upper cap, absolute rest/core/outside charges | Localclock signs; D is empty; EΣ improved; current core/outside budgets. Gives \((5/4)c_b+o(1)<(3/2)c_b\). Uniform conservative constants are those checked in S2CP/CFA. |
| \(Y<K_Y\) | LCRC closure's unchanged Volterra step | S1 transverse entry, current integral-r and residual bounds, bounded integrals of E_G and sqrt(E_G), outside smallness | Backward primary clock plus pointcap and EΣ supply energy integrals. Gives \(Y\le K_Y/2\). The kernel is not changed. |
| Cross residual \(<M_{res}q\) | LCRC/RCET instantaneous output estimates | Fixed core chart/mass, E_G, Y, outside supremum | E_G bounded by \(E_g+o(1)\), Y current guard, outside current guard. Model/core coefficient fixed before Mres; Mres chosen with factor-two slack and at least 2Cpre. |
| \(\int r<B\) | LCRC residual reduction plus S2CP Bs | Same state bounds and \(\int|1-\kappa_1|\le B_s^0\) | Bs supplied above; guard-dependent errors multiply \(q^2\ell\) or \(q b_B\ell\). Improvement \(C_r\log2+o(1)<B-1\). |
| Strong-complement outside | S2CP `compmass` | MOMC/PROFILE raw entry tail, fixed core cutoff, proved distance/gain, stopped clock | All supplied on the current interval. \(\mu_C/q\le Cq^{\Delta_\nu}\), \(\Delta_\nu>3/25\). |
| Original Q3 interior | GESG `Q3split`, `frozen` | Initial angular buffer, loss bounds, logarithmic total duration | Fixed ancestry; MOMC t0 and chosen LT. Gives \(O(q^9)\) after division by q. No current-angle masking. |
| π strip | PISB `main` | Current S2CP stopped inputs, Q3SB pre-entry cross bound | Current guards and proved S1; no CFA strip or passage conclusion. Rate \(q^{411/800}\) times polylog. |
| 3π/2 strip | PISB frozen zones plus LSB `main` | Same current stopped inputs, S1, actual-arrival gain | LSB's consumer dominates current mass, including unarrived labels. Rate \(q^{769/4000}\) times polylog, plus frozen zones. |
| Total outside supremum | The four preceding rows | Fixed outside partition | Each component is at most \(b_B/8\) for q small; sum at most \(b_B/2\). No coefficient involves an inverse power of the outside guard function. |
| CFA strip input | PISB + LSB integrated budgets | Current stopped inputs only | Multiplying the uniform rates by LT ℓ gives \(F_S(q)=o(1)\); this pays any fixed CFA small strip allowance. |
| \(\int\epsilon_F<\bar F_F\) | CFA `assembly` | Coarse field guard when invoking S2CP; retained core geometry; primary estimates; UΣ; outside integrated budget; overshoot | S2CP U/Bs and the paid outside rows supply every input. Primary coefficient fixed independently of the field allowance; other allowance/secondary dependence occurs in vanishing errors. Gives \(\int\epsilon_F<\bar F_F/2\). |
| Forcing budget | CFA `forcing` | S2CP c and VK budgets, assembled remainder, T=0, strip budget | All supplied above; exact \(1/Q\) kept. cb and C0 selected small with KY uniform over small cb. No future CLOCK forcing hypothesis is cited as its own proof. |
| e, rK, core coordinate chart | CFA `passage` and its entry audit | Actual c-form, small forcing, clock lower-defect bound, pointwise cap, small r0 Lb, e0 small | Canonical representation and assembly; localclock; pointcap; MOMC entry and TAILREP cutoff. Gives e ≤ 3e*/4, rK = O(q^χ), then strict coordinate-chart inclusion. |
| Response upper boundary/duration | LCRC ledger + BULK clock | Response strip and the just-matched guards | Gives the explicit duration upper bound, hence rules out the LT horizon. Does not rule out lower exit. |
| **Response lower boundary** | **No matched source** | **Need nonnegative response preservation for the exact original flow** | **Unpaid.** The sources assume it. The absolute ledger lower bound is not a relative error bound at the weak seed. |

## Strict entry and continuity audit

The entry checks use pre-entry conclusions, not the same outside or field guard being started:

- MOMC gives \(e_0=o(1)\), the right-half tail, mass 1/2 and the original reference. The fixed core cutoff gives \(r_0\le d_c\), \(\mu_K(t_0)=1/2-o(1)\), and an entry complement rate at least as strong as the later S2CP exponent.
- Q2EC/Q2EP give \(J_G(t_0)=O(q^3)\), \(E_{G+}(t_0)=o(1)\), the primary Cartesian signs/ratios and the clock seed. SEP gives \(E_\Sigma(t_0)=O(q^5)\); CΣ is chosen above that fixed entry coefficient.
- Q3SB `crosspre` starts the auxiliary residual guard strictly after the single model-dependent enlargement of Mres.
- The pre-entry pieces of PISB/LSB, rather than their conditional post-entry conclusions, give the strip entry masses. In particular LSB `entrymass` and `density` yield \(\mu_{J_3}(t_0)=O(q^3)\). GESG supplies the original-label interior. Thus outside entry is strictly below \(q b_B/2\).
- To check response entry explicitly, all right-half donors at t0 have scaled state \((a,a)+o(1)\). The compact Gaussian moment gives
  \[
  c_{\mathcal R}(t_0)=\frac{a\rho K(\rho a)}{2\lambda}q^2+o(q^2)
  =\frac{a^2}{2\lambda}q^2+o(q^2).
  \]
  Whole-Q2 and Q3 entry masses are O(q³), so their absolute responses are O(q³). Hence c(t0) is strictly positive. This is an entry fact only.
- The field is defined canonically using CFA's capped core donors and its exact V and K moments; εF is the actual difference norm. It is finite at entry and its cumulative integral is zero. No pre-existing small pointwise field error is required to start an integrated field guard.

For fixed positive q, finite-horizon characteristic regularity gives uniform continuity in the initial label. Fixed-cohort energies, the signed response and residual norms are continuous by dominated Gaussian/label integration. Essential suprema on the fixed core and receiver-circle suprema are continuous by uniform-in-label continuity. The capped core measure and positive-part K moment remain continuous at their kinks. Thus the canonical C1 remainder has a continuous cumulative integral; cumulative outside suprema are also continuous. No differentiability of a moving mask is needed.

## Constant order

1. Fix model bounds, \(\bar c=1/4\), \(L_T=20\), \(b_B(q)=q^{1/10}\), \(R=79/51\), \(M_K=2\), \(B_s^0=\log2+1\), \(L_c=R+1\), the core cutoff constant c*, and admissible ν.
2. Fix CFA's model-uniform \(C_{pass},g,e_*,K_{pass}\). Account for the norm convention: LCRC's summed-angle radius is \(R_{LCRC}=2R\); this is fixed now, not enlarged in response to a residual guard.
3. Use CFA's conservative \(2+2\bar c\), \(\bar h_*=(9/8)\bar c+1\), \(\underline b=(169/400)(1-\bar c)\) in LCRC's formulas. Fix \(B=C_rB_s^0+2\), then KY and Mres. Enlarge Mres once to exceed 2Cpre. These choices are uniform in the later small cb.
4. Fix a positive coarse \(\bar F_F\); choose small fixed cb, set Eg=2cb, and then fix CD, A0, Cm. The first two CFA forcing terms are made ≤ Pallow/4, where Pallow=e*/(4Cpass).
5. Choose C0 within RCET's admissibility and CFA's receiver-boundary margin, with the primary remainder term at most \(\min(\bar F_F/4,P_{allow}/4)\).
6. Fix K(C0), SEP geometry/entry constants, then CΣ. This preserves ledger 19's corrected order.
7. Choose q last. Strip and other positive-power errors then pay the remaining field/forcing allowances. Each outside component is ≤ bB/8.

No guard-dependent core radius or B_s is used. The coarse field allowance may affect S2 tail/gain constants, but those enter CFA's field improvement through vanishing terms. The order-one primary remainder coefficient is independent of the guard it improves. The fixed field/forcing allowances are not claimed to vanish with q when cb and C0 remain fixed.

The duration choice is independent of the guards:

\[
20\,(169/400)(1-1/4)-231/40=9/16>0.
\]

It therefore dominates the worst weak-seed logarithmic coefficient with a fixed positive margin.

## Exact obstruction and why the proposed ledger argument is insufficient

The exact missing inequality is the boxed domain condition at the start of this note (`an03wptv1:gap`). A sufficient signed ledger estimate at a putative first zero s is

\[
c_\Sigma(s)+c_K(s)+c_B(s)
>-(8/9)H_{G+}(s)+C\mu_{G+}(s)e^{-\rho^2/(4q^2)}.
\]

It would imply c(s)>0 and rule out that zero. An invariant-region argument allowing a zero touch could instead suffice; none is cited as already proved.

What the cited absolute estimates actually give is

\[
c\ge(8/9)H_{G+}-\epsilon_q,\qquad
\epsilon_q=O\big(q^2+q b_B+q^5+q^{\Gamma_\nu}E_g
 +q^2K_Y\sqrt{q^5+q^{\Gamma_\nu}E_g}\big)+o(1).
\]

At c=0 this only bounds H_G+ from above by a vanishing quantity. It is compatible with the positive small seed. It is not a contradiction.

The sufficient absolute-domination inequality

\[
(8/9)H_{G+}>|c_\Sigma|+|c_K|+|c_B|+\text{Gaussian tail}
\]

cannot be imposed uniformly: at entry \(H_{G+}\le\mu_{Q2}=O(q^3)\), whereas \(c_K\asymp q^2\). The actual response is positive there because the core response has a positive sign, which that proposed absolute lower bound discards. Future outside response is also only absolutely bounded by the matched contracts. Paying its mass at scale o(q) is not the signed estimate above.

Q3SB's pre-entry estimate is for \(|c|+N_-\), and its signed-excess proof explicitly permits slightly negative response before t0. It does not supply the missing post-t0 barrier. Positive radial weights and loss monotonicity do not, by themselves, make the untied signed regression c a nonnegative mass.

The work stops here. No extension of the source theorems to negative response is attempted, and no unproved positivity assumption is hidden in a theorem advertised as unconditional passage to cb.

## Clock and hitting-time accuracy

On every certified interval,

\[
t-t_0=\frac{\log(H(t)/H_0)-\delta(t_0,t)}Q+\int_{t_0}^t c,
\qquad |\delta|\le D_{clk}=o(1).
\]

S2CP supplies
\(0\le\int c\le(10e/9)E_g/[Q(1-c_b)]+o(1)\). Thus the amplitude cap gives

\[
t-t_0\le[\log(c_b/H_0)+O_{fixed}(1)]/Q.
\]

The requested formula with denominator Q(1−cb) is valid as the weaker **duration upper bound**, not as an equality with additive O(1) numerator at fixed cb. Such an equality would exceed the sharper proved upper bound by

\[
\frac{c_b k}{Q(1-c_b)}\ell+O_{fixed}(1),
\]

which diverges. If a later proof supplies upper arrival and \(H(t_b)\asymp c_b\), the fixed-constant phase formula would have denominator **Q**. Without that terminal comparison, retain the exact identity in H(t_b). The o(1) amplitude-clock defect is distinct from the O(1) seed and terminal-response comparison factors.

## Handoff to S4

At the certified τ, the following are supplied, at the stated accuracy:

| Item | Accuracy | Intended consumer |
|---|---|---|
| Residual bounds, regenerated transverse energy, integrated r | Fixed constants; J_G=O(q²); integrated-r error o(1) | BULK weak return and subsequent receiver transport |
| Primary Cartesian ratios/signs and eta-zero relative amplitudes | Fixed \(e^{O(C_0)}\) distortion | Q2 primary family bookkeeping |
| Separate clock identity and seed | Subinterval clock defect o(1); seed only \(\asymp A_q^{-\lambda}q^k\) | Phase matching; must preserve the distinction between clock error and unknown order-one seed factor |
| Core and actual reference | rK=O(q^χ), e≤3e*/4, mass upper bound 1+o(1) | Strong-family retention/input to the next forcing analysis |
| Secondary energy, distance and capped gain | Explicit positive q powers, fixed constants | Explicit weak-output estimates and Sigma charging |
| Complement and outside budgets | Supremum and integrated μ/q vanish with displayed powers | Field remainders and later small-defect estimates |
| Canonical c-form and forcing | Small fixed integrated budgets, not generally o(1) | Local passage/field control up to the certified endpoint |
| **Upper-response endpoint c=cb** | **Not supplied** | Required before advertising this state as the S4 entry at tb |

No weak return, matching beyond cb, or selection is performed. The requested full handoff is blocked only at the explicitly identified response-domain obligation within this assembly audit; no claim is made that resolving it requires a new assumption rather than a new proof.

## Source provenance

Fresh read-only reads from [TodManlaibaatar/OOD-reversals-theory](https://github.com/TodManlaibaatar/OOD-reversals-theory). The identifiers below are file blob SHAs, not repository commit IDs. Roadmap v1.16 is a plan/status document; its claim that no input remains is not used as a proof premise.

| Source | Repository path | Blob SHA |
|---|---|---|
| Roadmap v1.16 | `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | `811950cec09716cb018570af8328d97f45849e27` |
| LCRC | `03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex` | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` |
| RCET | `03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex` | `49e352002b4c699338ac99a4d55d51c60760ea86` |
| BULK | `03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` |
| S2CP | `03_passage_AN03/AN03_S2_closure_package_v1.tex` | `baeb8a7eb1e36ce86319782511b665944be1afda` |
| GESG | `03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex` | `f00459b5ca412eb86b0893adb64766e2c10d5590` |
| DECG | `03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex` | `a490ea323e45e61c1a58301554b89ad84cb02605` |
| CFA | `03_passage_AN03/AN03_c_form_assembly_v1.tex` | `341908c228092e9a818d98de3ec26591a1050364` |
| Q3SB | `03_passage_AN03/AN03_Q3_strip_budgets_v1.tex` | `13a024c54f10d50a454aae1006d3005d2a28051b` |
| PISB | `03_passage_AN03/AN03_pi_strip_budget_v1.tex` | `ab8a0a2a028935f5045e53e0066e30afeb69c635` |
| LSB | `03_passage_AN03/AN03_late_strip_budget_v1.tex` | `4d3c0065e3b639c02db87c704a3efcfbb0738190` |
| MOMC | `02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex` | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| Q2EC | `02_entry_AN02/AN02_Q2_entry_contracts_v1.tex` | `b149537025e130801fc55b9e49c365c158eee17b` |
| SEP | `02_entry_AN02/AN02_secondary_entry_profile_v1.tex` | `c7c857ec10b7f7b2cf42d1cdb452c50edc735587` |
| PROFILE | `02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex` | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` |
| CLOCK | `03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex` | `8de0d85c64a3d51f3bd9c3662baf2efae0737373` |
| Q2EP | `02_entry_AN02/AN02_Q2_entry_through_strong_passage_v1.tex` | `042b3c93cf8402d10487f9e56f6f5b1d869c424a` |

## Verification and delivery

Analytic inequalities only; no numerical experiment, interval arithmetic, sign grid or saved trajectory. Source arguments are cited and their hypotheses matched rather than re-proved. The short entry response calculation and the duration/phase algebra are displayed explicitly.

The standalone TeX is compiled as a typesetting check, not mathematical validation. Labels and references are checked for uniqueness and the required prefix. All 50 pre-existing output files are compared with their pre-task hashes. No prior source, foundation, roadmap, checkpoint, or increment is modified; no GitHub mutation is made. The delivered source ZIP contains only the new `.tex` and same-stem `_review.md`, with no PDF.
