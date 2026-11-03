# RTA v1 review — S5d / initialized AN8 assembly

Companion: **AN07_rate_transfer_and_assembly_v1.tex**  
Prefix: **an07rtav1:**  
Read date: **2 November 2026**, roadmap **v1.26**.  
Delivery: two source files, packaged together in a source-only ZIP.

## Result and scope

**Closed:** A-rate-transfer, initialized learned reversal on WIT's fixed rectangle, both exact concept responses, the **169/196** cluster-loss ratio, and initialized persistence on a diverging unspecified horizon. There is no unmatched hypothesis in these conclusions.

The original balanced, untied, isotropic initialized family is **S0 = q^10**, for sufficiently small positive q, on WIT's unchanged analytic rectangle
\[
\mathcal P_*=[2/3-\delta_\rho,2/3+\delta_\rho]
 \times[5\pi/9-\delta_\zeta,5\pi/9+\delta_\zeta].
\]
This is not an assertion of common learned windows on the entire deep ratio box.

The main theorem gives:

- responses \(\mathsf m_1\ge1/2,\ \mathsf m_2\ge1/4\);
- exact losses \(\mathcal L_p\le(169/196)\mathcal L_p(0)\), hence reduction at least \(27/196\);
- source margins \(D_1^\tau\le-p_*q^2/2\), \(D_2^\tau\ge p_*q^2/2\) on J;
- total-rate margins \(-5\gamma_0q^2/8\) on \(J_-\), \(+5\gamma_0q^2/8\) on \(J_+\);
- an interior error minimizer, with both endpoint-to-minimum differences at least \(\gamma_0r q^2/4\);
- an off-cone sector of exact angular width \(2\delta_\zeta q\).

Source bounds are uniform for exact selector-defined formulas. Classical derivatives obey them wherever defined, and the total derivative obeys them almost everywhere. Every core probe gate is strictly separated; classical differentiability at a background gate-hit atom is not asserted.

The persistence corollary gives a common fixed \(S_{\rm clr}>s_*+r\), \(T_q\to\infty\), \(\varepsilon_q\to0\), and
\[
\sup_{\mathcal P_*,\,S_{\rm clr}\le s\le S_{\rm clr}+T_q}
 |E_{\xi_q}(\tau_h+s)-1/2|\le\varepsilon_q q^2.
\]
No horizon growth rate, or forever-in-time assertion at fixed q, is claimed.

## Task status

| Step | Status | Conclusion / audit | Remaining inequality |
|---|---|---|---|
| 1. Inventory and clocks | Closed | Same parameter and half-mass phase; \(J\subset[s_n,T_J]\). | None |
| 2. Core gate | Closed | Supremum tracking \(C_{\rm sup}q^{1/20}\); every core gap at least \(g_*/8\). | None |
| 3. Original source rates | Closed | Normalized core error \(C_{\rm core}(q^{1/10}+q^2)\); background/cross terms \(C_{\rm bg}q^2\epsilon_{\rm bg}\). | None |
| 4. Leading comparison | Closed | \(\delta_J=O(q^{1/20})\), below exact margins. | None |
| 5. Learning | Closed by direct proof | Entire-state compactness is unavailable; full-output \(L^2\) estimates replace it. | None |
| 6. Initialized Theorem A | Closed | Source signs, ordered rates, error-transfer rebound and sector. | None |
| 7. Persistence | Closed | FWC discharges LP's every-finite-window premise for the actual initialized family. | None |
| 8. Scope / S6 handoff | Closed audit | Canonical/bridge cases, lag decomposition and quantitative persistence rate excluded. | S6 tasks below are outside this theorem |

## Hypothesis matching

The TeX inventory gives the same domains. “Not applied” below is deliberate; it is not a retained hypothesis of the final theorem.

| Source | Hypotheses, including ranges and signs | Supply / disposition |
|---|---|---|
| FWC main, corefield, distbound, background, errortransfer, early | Original \(\kappa=10\) initialized family; deep ratio box; inherited constants and WCS level; fixed finite \(T>\max s_n\); bounded offsets; q last; current physical measures and fixed cohorts. | Choose fixed \(T_J>\max(s_*+r,\max s_n)\). FWC is unconditional, so no passage guard is added. For persistence use its conclusion separately for every larger fixed T. |
| WIT uniformtheorem | Selected coherent branch, leading strong mass one, logistic weak mass on its half-mass clock; original \(\mathcal P_*\), common J and positive analytical margins. | Leading comparator only. Physical masses are compared by FWC, not identified with their limits. |
| WIT populationtransfer / epsdef | Solution of the defined leading system at the same \((\rho,s)\); nonnegative measures, \(M,N\le2\); both supports in \([-R_W,R_W]^2\) throughout J; distance at most \(\varepsilon_*\); selector convention and regular characteristics for the a.e. conclusion. \(\varepsilon_*=\min(1/4,\sigma/4,p_*/(8C_1),\gamma_0/(8C_1))\), \(C_1=64R_W^2(1+4/g_*)\). | **Not applied** to the original perturbed dynamics. Weak support is not uniformly compact. Distance smallness alone would not discharge the other hypotheses. Direct rate and learning arguments replace that application. |
| WIT staticproposition | Entire exact state consists of two compact charted measures; both supports in \([-R_W,R_W]^2\), \(R_W\ge2\); \(M,N\le2\); ratio in its \(\mathcal K\subset[13/20,7/10]\); \(0<q\le1\). Learning also needs its mass conclusions, \(0<S_0\le1/2\), \(q\le\min(1,\sigma/(100R_W),1/(100R_W),(13/20)/(272R_W))\). | **Not applied.** Weak tail and outside labels violate the representation. Direct \(L^2\) estimates include both and recover the exact loss ratio with new explicit thresholds. |
| CWI rate | Leading-form rates; nonnegative measures; \(R\ge2,\ 0<\rho\le1,\ M,N\le2,\ 0\le n_*\le1\); compact strong support and comparison coordinates; finite weak first moments; \(|\zeta|\le R\); comparator gap \(\zeta-X_*\ge g_0>0\). Regular characteristics and locally bounded first moments for its chain rule. | FWC supplies physical measures, reached charts and current moments. Enlarge R only after freezing WIT's rectangle. WIT gives \(g_0=g_*/4\). Apply statically to leading-form rates at the actual state. |
| CWI exactrate / ratecharge | Exact balanced population; fixed cohorts; mixture half in each source matrix; sourcewise bounded diagonal and \(O(q)\) cross entries; \(O(qL)\) alignment; bounded offsets; selector/a.e. convention. | FWC supplies these on the continued window. The background observable is \(\mathcal Q_{\Sigma\cup B}\), not just its mass. |
| P probe-pop | Full expansion requires two compact charted populations with no outside; its simplified first-source formula uses \(M=1\). | Full-population version not applied. Core expansion is written explicitly with physical \(M-1\); background is charged separately. |
| LP uniform-clear | Compact ratio interval in \((0,1)\); selected-branch continuity on fixed windows; uniform forward growth; finite upper offset. | \(K_\rho\), WIT branchsmooth, P's growth bound as checked in LPR, and \(\max I_\zeta\). |
| LPR combinedtheorem | Same selected coherent branch and WIT rectangle/witnesses; imported P/LP continuation, invariants and common clearing. | Supplies leading-only exact \(\mathcal E_*=0\) for one common \(S_{\rm clr}>s_*+r\) and all later times. No initialized claim is borrowed. |
| LP diagonal-transfer | Compact offsets and any included compact ratio range; common clearing; actual initialized positive-noise family; analytic physical centering; uniform full-original convergence on every finite \([S_{\rm clr},T]\). | \(S_0=q^{10}\); center \(\tau_h/\mu_1^2\); same \(K_\rho,I_\zeta\); FWC errortransfer and early. No quantitative diagonal rate follows. |

The clock is
\[
\tau=\mu_1^2t_{\rm phys},\quad
\tau_h=t_n+\lambda^{-1}\log((1-n)/n),\quad
s=\tau-\tau_h,\quad n_\rho(s)=(1+e^{-\lambda s})^{-1}.
\]
Physical selected mass has FWC's \(O(q^{1/8})\) error from this logistic comparison. Since \(n\le1/8\), whereas \(n_\rho\ge1/4+\sigma/2\) on J, the whole learned window follows entry. Physical rates multiply normalized rates by \(\mu_1^2\); physical windows divide \(\tau_h+J\) by \(\mu_1^2\).

## New proof audit and exact budgets

### Core gap

At fixed actual donor measures the leading strong field is receiver-Lipschitz with constant \(L_F\) on the reached compact chart: \(\partial_1F(t,w)=(w-t)_+\phi(t)\), and FWC bounds current weak first moments. Use FWC's **value** errors, not an unproved derivative of the finite-noise remainder:
\[
D^+|z_b-z_{b'}|_1\le L_F|z_b-z_{b'}|_1+2C_Fq^{1/10}.
\]
Entry diameter is \(O(q^{1/20})\). The fixed-window diameter is at most
\[
e^{L_FD_J}(C_{\rm ent}q^{1/20}+2C_FD_Jq^{1/10}).
\]
Averaging against current core mass \(M\ge1/2\) and using FWC's first moment gives supremum tracking \(C_{\rm sup}q^{1/20}\). This does not require the reference itself to be a core label. Choosing \(C_{\rm sup}q^{1/20}\le g_*/8\) proves the gate margin, including closed endpoints.

### Source normalization and precision

Use \(h_p=(\log m)'_p=2a_\psi^TR^{(p)}a_\theta\). This is twice CWI's auxiliary scalar \(g_p\), and agrees with FWC's full source reactions. There is no additional mixture half in the output derivative.

With \(A=\int_K(\zeta-x)\,d\mu\), \(B=\int_Ky(\zeta-x)\,d\mu\), exact differentiation gives
\[
q^{-2}D_p^{K,\mathrm{self}}=(A-\zeta)A_p^{\rm act}+B_p^{\rm act}+O(q^2).
\]
Coordinate velocities **and** radial reactions enter both differentiated moments. No static remainder is differentiated. Keeping \(h_1^0=1-M\) gives the physical leading rate; the expression reduces to \(-A(Y+K_w)/2\) only at \(M=1\).

Let \(\gamma_*=289169/924000\), \(L=1+\log(1/q)\), and \(\epsilon_{\rm bg}=q^8+L^2q^{\gamma_*}\).

| Term | Proved size | Source / treatment |
|---|---|---|
| Core normalized exact-to-leading source difference | \(C_{\rm core}(q^{1/10}+q^2)\) | FWC sourcewise velocity and reaction estimates; exact core expansion |
| Primary direct output and derivative | Exactly zero | FWC strict inactivity by current angle, on the continued interval |
| Background transverse observable | \(\mathcal Q_{\Sigma\cup B}\le Cq^2\epsilon_{\rm bg}\) | FWC background |
| Background mass alongside that observable | \(\mu_{\Sigma\cup B}\le Cq^{\gamma_*}\) | FWC continued fixed-label mass bounds |
| Full background source and all cross terms | \(C_{\rm bg}q^2\epsilon_{\rm bg}\) | CWI ratecharge; \(|f_K|+|\dot f_K|\le Cq\); Young inequality |
| Leading physical state versus coherent source | \(64R^2(1+4/g_*)C_{\rm dist}q^{1/20}\) | CWI rate, FWC distbound, WIT comparator gap |

Therefore
\[
\delta_J=C_{\rm core}(q^{1/10}+q^2)+C_{\rm bg}\epsilon_{\rm bg}
 +64R^2(1+4/g_*)C_{\rm dist}q^{1/20}.
\]
Since \(\gamma_*>1/20\), \(\epsilon_{\rm bg}=o(q^{1/20})\). Require
\(\delta_J<\min(p_*/8,\gamma_0/16)\): the **sum of two errors** is then below \(\gamma_0/8\). Source coefficients are \(5/8-1/8=1/2\), and total-rate coefficients \(3/4-1/8=5/8\).

At a background gate hit, alignment gives output projection \(O(qL)\), and source angular velocity is \(O(qL)\). A selector change costs at most \(Cq^2L^2\mu_{\Sigma\cup B}\) in the projected source, already paid. This is not a classical differentiability claim at an atom.

### Direct learning

FWC gives bounded current weak first moments and \(\mu_{P_q}+\mu_\Sigma+\mu_B=O(q^{1/4})\). Core and selected feature approximations cost \(O(q)\) after integration. Weak bounds are proportional to \(q(1+|u|+|v|)\), so no fixed weak supremum is needed. Gaussian negative parts cost at most \(q|Z|\).

For omitted cohorts use the exact \(|f_A(X)|\le\mu_A|X|\) **only at the unscaled learning precision**, not to pay probe rates. This gives
\[
\|f-e_pM_pX_p\|_2\le C_{\rm out}q^{1/4},\quad
|\mathsf m_p-M_p|\le C_{\rm resp}q^{1/4},\quad
\sqrt{2\mathcal L_p}\le|1-M_p|\sqrt{Q_p}+C_{\rm loss}q^{1/4}.
\]
Masses lie in \([1/4,5/4]\). If \(C_{\rm loss}q^{1/4}\le13/320\), the current residual is at most \((13/16)\sqrt{Q_p}\). The exact initial residual is
\((1-S_0/4)\sqrt{Q_p+q^2}\ge(7/8)\sqrt{Q_p}\).
Their squared ratio is exactly \(169/196\).

### Rebound and persistence

Each length-\(r/2\) limiting interval gives drop/rise at least \(3\gamma_0r/8\). With \(C_{\rm err}q^{1/20}\le\gamma_0r/16\), two endpoint errors leave \(\gamma_0r/4\). This uses error transfer alone and excludes both endpoints as minimizers.

LP/LPR clearing gives \(X_\rho>\max I_\zeta\), hence the limiting observable is exactly zero, not merely of a favorable sign. FWC's full initialized convergence on every fixed later interval discharges LP's diagonal premise. Its uniform thresholds may be taken below \(q_0\).

## Constant order

Keep WPT/RB–WCS's entire order and n. Freeze WIT's original rectangle, windows and margins. Choose \(T_J\), FWC continuation constants and a possibly larger R; then \(L_F,C_{\rm sup},C_{\rm core},C_{\rm bg},C_{\rm dist}\) and learning constants. Enlarging R does not redefine the original rectangle.

Choose q last, below every source threshold, with:

- \(C_{\rm sup}q^{1/20}\le g_*/8\);
- \(\delta_J<\min(p_*/8,\gamma_0/16)\);
- \(C_{\rm err}q^{1/20}\le\gamma_0r/16\);
- \(C_Mq^{11/10}\le1/4\), \(C_Nq^{1/8}\le\min(1/4,\sigma/4)\);
- \(C_{\rm resp}q^{1/4}\le\min(1/4,\sigma/4)\), \(C_{\rm loss}q^{1/4}\le13/320\);
- \(q^{10}\le1/2,\ q\le1/2,\ 2qR<\pi/2\).

One positive analytic \(q_0\) exists; no numerical value is asserted. Persistence's common clearing time is fixed before its separate diagonal sequence.

## Dependencies and source provenance

Direct inputs: FWC, CWI, P's leading/source/atomic identities, WIT, LP, LPR. PSE's matrix/energy conclusions enter through FWC. H2 and the roadmap define the consumer contracts.

Inherited initialized chain, used through the proved FWC/PSE handoff: F/P; PROFILE, OWPT, MOMC, Q2/Q2E, Q2EP, Q2EC, SEP; LOC, CLOCK, TAILREP, BULK, RCET, LCRC, CFR, DECG, GESG, S2CP, CFA, Q3SB, PISB, LSB, WPT, RB; WEAK, WBR, MP, SRR, WCS; CWI, PSE, FWC. No withdrawn shortcut or obstruction-only contract is used as a theorem.

Fetched read-only from TodManlaibaatar/OOD-reversals-theory:

| Path | Git blob SHA |
|---|---|
| README.md | 6a1f6f38109428d7dcc8cd5cc7945ea0dbaff555 |
| 00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md (v1.26) | 0171fc789b42f680b4f7641f0ffce38301c7fdda |
| 07_compact_windows_AN07/AN07_finite_window_continuation_v1.tex | f2c99953991d2bf8ce17d0bfb98845249e47d0bc |
| 07_compact_windows_AN07/AN07_compact_window_interface_v1.tex | 0902c80583eabb6bc0908ffb64a396633654ae19 |
| 07_compact_windows_AN07/AN07_probe_sector_energy_v1.tex | 4e90dfeb1bb2d75ea9c0711dfaabb15a266ff1b1 |
| 04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex | 9e102514ad0a491066a2f9eb8eb86e9a251c2b53 |
| 04_witnesses_persistence/LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex | 4d2744894aae8cfdd524d22d08a91fb3306bab10 |
| 04_witnesses_persistence/LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex | d438e477e893414e1284b072184eb1ce12fe2f74 |
| 01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex | cb458c933aa043cf0188fd11c46bf4246ffc91d8 |
| 00_roadmap/THEORY_HANDOFF_ANALYTICAL_A_B_v2.md | decb029fb314e96aae70e5eee68eaa969b6293ce |

## S6 handoff and exclusions

S6 receives the matched analytic center, fixed-window physical masses and current moments, pointwise sourcewise core velocities/reactions, strict core probe gap on J, source margins, and full-background source charge at \(q^2\epsilon_{\rm bg}\) precision.

Still outside this increment: exact original-flow B-core lag/exposure and producer attribution, especially precision relative to a small cancellation (S6); non-small bridge and canonical regime (S7/S8); a quantitative persistence horizon; unique/transverse reversal; finite-width statements.

The canonical pair \((q,S_0)=(0.05,2\cdot10^{-4})\) is not in the asserted family. The unevaluated local rectangle containing \(5\pi/9\) is not asserted to contain the distinct rounded offset 1.745.

## Validation

- The standalone TeX compiles to 9 pages. The final compilation has no warnings, undefined references, or overfull/underfull boxes. The PDF is a private compilation check, not part of the source delivery.
- All 36 labels are distinct and use an07rtav1:. All internal references resolve. The prefix was absent from the repository search, the fresh source snapshot, and prior delivered TeX/Markdown.
- Both exact requested grep -nP scans were attempted. This macOS grep does not support -P. The identical patterns were therefore run with rg --pcre2 and independently with Python: both returned **zero matches**.
- The literal commands \(\backslash\mathrm{rm}\), \(\backslash\mathrm{tfrac}\), \(\backslash\mathrm{qquad}\), and \(\backslash\mathrm{text}\) survive in the source (71, 17, 20, and 45 occurrences respectively).
- All ten recorded Git blob hashes were verified against the retrieved source contents; scratch copies add one terminal newline, which was excluded from that verification.
- SHA-256 comparison confirms all **92 pre-existing output files** are unchanged.
- The ZIP is source-only: the new TeX and same-stem review Markdown, with no PDF or compilation files.

No prior increment, README, foundation or checkpoint is edited; no GitHub mutation or numerical experiment is performed. Compilation and text/archive checks are document validation, not numerical premises in the proof.
