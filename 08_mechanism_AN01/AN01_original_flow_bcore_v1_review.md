# B-core v1 review — S6 stopped at the proposed remainder budget

Companion: **AN01_original_flow_bcore_v1.tex**  
Prefix: **an01bcv1:**  
Folder: **08_mechanism_AN01/**  
Sources read: **2 November 2026**, roadmap **v1.27**.

## Outcome

**The requested full B-core theorem is not claimed.** Step 2's bound on the unchanged checkpoint remainder r2 is false, rather than merely unpaid. This increment proves the exact obstruction on the original initialized flow and stops at that step as instructed.

The checkpoint puts the strong core's cluster-2 **output rotation** inside r2. On WIT's learned windows this channel has a strictly positive leading term at the q² scale. It cannot be treated as an O(q^(2+1/20)) remainder.

This does not invalidate P's exact identities, FWC's reduction, or RTA's initialized Theorem A and persistence. P's atomicrates explicitly says that the second source contains output rotation before weak saturation. RTA retained this term in its total second-source rate. The failure is in the new request to bound *every* checkpoint remainder by a strictly higher power of q.

## Closed result, with scope

For the exact initialized population with S0 = q^10, sufficiently small q, on the unchanged \(\mathcal P_*\times J\), with the same clock and fixed core as RTA/FWC:
\[
\frac{r_2}{q^2}
=\mathcal O_*(\rho,\zeta,s)+O(q^{1/20}),\qquad
\mathcal O_*=\frac{\rho}{2}(1-n_\rho(s))
                  (\zeta-X_*)K(\rho X_*).
\]
The error is uniform and can be written before simplification as
\[
C\left(q^{1/20}+q^{1/10}+q^2+
 q^8+(1+\log(1/q))^2q^{289169/924000}\right).
\]

Let R ≥ 2 bound the fixed reached core/comparison chart and offsets. Define
\[
b_J=|s_*|+r,\qquad
\delta_n=\frac{1}{1+\exp((49/100)b_J)},\qquad
c_{\rm out}=\frac{13g_*}{160}\delta_nK(-7R/10).
\]
These are fixed before q and \(c_{\rm out}>0\). Indeed:

- \(\rho/2\ge13/40\);
- \(1-n_\rho(s)\ge\delta_n\) on J;
- \(\zeta-X_*\ge g_*/4\) by WIT;
- \(K(\rho X_*)\ge K(-7R/10)>0\), even if X* is negative.

For an explicit elementary Gaussian lower bound,
\[
K(-a)=\int_0^\infty u\phi(u+a)\,du
\ge \frac32\phi(a+2)>0,\qquad a\ge0.
\]
Therefore, for q small enough,
\[
r_2\ge\frac{c_{\rm out}}2q^2
\]
uniformly on the whole learned rectangle/window.

The closed two-channel consequence is
\[
\begin{aligned}
q^{-2}(H^{(1)}+H^{(2)})&=(X_*-Y_*)x'_{2,*}+O(q^{1/20}),\\
q^{-2}D_2^\tau&=(X_*-Y_*)x'_{2,*}+\mathcal O_*+O(q^{1/20}),\\
x'_{2,*}&=\frac{\lambda}{2}
 [n_\rho V_*-X_*+(1-n_\rho)Y_*]\Phi(\rho X_*).
\end{aligned}
\]
This is a combined input/output channel identity, **not** a producer attribution or a proof of a signed exact lag.

As in RTA, source formulas use the exact selector convention, with classical derivatives wherever defined and the a.e. time interpretation. Every core gate is strictly separated. No classical differentiability at a background gate-hit atom is asserted.

## Exact failing inequality and stop

The requested estimate includes
\[
|r_2|\le C_*q^{2+\kappa},\qquad \kappa=1/20.
\]
The proved lower bound would force
\[
\frac{c_{\rm out}}2\le C_*q^\kappa.
\]
For any fixed \(C_*\) and any \(\kappa>0\), this is impossible as q tends to zero.

The attempted approach was to evaluate P's exact source-by-motion decomposition using FWC's sourcewise velocities/reactions and RTA's background precision. It yields a **positive leading term**, not a vanishing error. No second approach can establish the contradicted inequality, so none was attempted.

The necessary revision of a future contract is to keep the core output-rotation term at leading order. This increment proves
\[
r_2-q^2\mathcal O_*=O(q^{2+1/20}),
\]
but does not silently redefine r2 or alter the checkpoint. Whether all the other requested individual remainder budgets close is not decided after this stop.

## Step status

| Requested step | Status | What was proved / remaining |
|---|---|---|
| 1. Hypothesis inventory | Closed | Exact versus leading scopes, matrix normalization, windows and sign/range conditions are listed in TeX Section 1. |
| 2. Every factorization remainder is O(q^(2+κ)) | **Stopped; false as stated** | Exact factorizations hold, but r2 has the positive q² term above. Other separate remainder evaluations are not completed after this failure. |
| 3. Signed exact lag | Not started after stop | \(r_{21}/q=L_0+o(1)\), with a signed lower bound, is not established in this increment. No norm bound is substituted for it. |
| 4. Exact help = exposure × signed lag | Not started | The required lag-relative help remainder and exposure are not newly proved. |
| 5. Producer-resolved harm | Not started | The combined input channel is identified, but target/core/selected/secondary/outside rate-weighted producer limits and signs are not established. |
| 6. Factor evolution through dominance change | Not started | RTA's rate signs remain available; attribution to evolving factors is not inferred from them. |
| 7. Full B-core / canonical handoff | Partial audit only | No full B-core theorem. Corrected deep-regime contract and canonical relative-precision needs are recorded below. |

## Hypothesis and normalization audit

The complete table is in the TeX. The following points are the ones decisive for the obstruction.

| Source | Hypotheses / domain | Supply and use |
|---|---|---|
| P motion | Exact balanced flow; finite source integrals; fixed probe; chain rule at regular states or selector/a.e. interpretation; all three derivative channels. | FWC/RTA original flow. Used with no omitted carrier. |
| P factorizations, epsilonB, epsilonH | Measurable \(C\) inside current probe-active population; positive mass; normalized current averages; signed quantities; finite moments. No remainder-smallness hypothesis or conclusion. | \(C=K\), RTA coregap, FWC \(M\ge1/2\). Exact identities retained; proposed smallness tested and refuted for r2. |
| P helpdefect | Algebraic exact Gaussian identity; its tail estimate further needs \(a_1>0\) and finite cluster-1 transverse residual norm. | Supplied on reached core chart, but not quantitatively pursued after r2 failure. |
| P projection | Exact full output; Gaussian \(E[X_1X_2]=0\); finite \(L^2(P_1)\) output; current active/inactive partition. | Identity available; it has no positive-lag conclusion and is not used as one. |
| P GLC / GLCidentity | Same core definitions and chain-rule convention; no autonomous closure. Separate sign criteria have their own explicit error margins. | Bookkeeping is valid; the proposed o(q²) absolute budget is not. |
| P producer | Exhaustive output-producer partition, integrable moments, same receiver gate, actual rate-weighted core integral. | Available but not applied to producer asymptotics after the stop. No mean-angle substitution. |
| P tracking | Fixed initial labels; Gaussian \(L^2\) projection; exact kernel evolution. Damping estimate requires an input chart below π/2; quantitative comparison additionally needs a damping lower bound and forcing upper bound. | Not invoked. No forcing estimate or positive-sign implication is assumed. |
| P lagtheorem / lag-pop / Xi-positive | Leading bounded-chart characteristic solution, \(M=1\), \(0\le N\le1\), positive measures; continuous interpretation at \(N=0\), finite coordinates for strict Xi; positive incoming lag for preservation. | Not used as exact original-flow positivity. No lag theorem is claimed here. |
| P atomicrates | Selected coherent leading branch; \(M=1\), \(0<n<1\); active strong and inactive weak probe phase. | Consistency check and combined channel formula. Original remainder asymptotics come from RTA/FWC, not from assuming an exact two-atom state. |
| RTA coregap, backgroundrate, ratetransfer | Original S0 = q^10 family; q last; original \(\mathcal P_*\times J\); matched clock; selector conventions. | Unconditional source conclusions on the exact requested window. |
| FWC corefield, distbound, background | Original deep-regime initialization; fixed finite T beyond entry, bounded offsets; q last; physical current measures and fixed labels. | Choose fixed T covering J. Source-2 scaled output velocity and full radial reaction are used separately. |
| WIT uniformtheorem | Selected coherent branch and original rectangle/common windows. | Strict comparator gap \(g_*/4\). |
| WIT regiontheorem | Ratio box and selected branch, **s ≤ 0**. | Not extended to all of J. The proof does not need X* > 0, nor any unsupported extension of the half-learning region. |

P's matrix Rp is unhalved; RTA's \(R^{(p)}=R_p/2\). Hence
\[
v_{\psi,p}=\tfrac12(b^\perp)^TR_pa,\qquad
h_p=(\log m)'_p=2g_p=b^TR_pa.
\]
FWC's source reaction is the full h, not g. This distinction fixes the factor \(1/2\) in \(\mathcal O_*\).

The exact identities themselves show
\[
H^{(1)}+H^{(2)}=\int_K vc\,v_{\theta,2}\,d\mu,\qquad
r_2=\int_K zd\,v_{\psi,2}\,d\mu
 -\int_K 2g_2zc\,d\mu+D_{2,K^c}.
\]
Here \(c=e_\xi\cdot b\) is the checkpoint's probe projection, not the weak response clock.

## Error ledger: no hidden cancellation or outside deletion

Let \(T_0=\Sigma\cup B\), \(L=1+\log(1/q)\), and \(\epsilon_{\rm bg}=q^8+L^2q^{\gamma_*}\).

| Term | Exact or proved size | Justification |
|---|---|---|
| Non-core primary direct probe output/source | Zero | FWC strict inactivity by current angle on the continued interval |
| \(\mu_{T_0}\) | \(O(q^{\gamma_*})\) | FWC fixed-label mass bounds |
| Active-probe squared input integral \(\mathcal Q_{T_0}\) | \(O(q^2\epsilon_{\rm bg})\) | FWC background |
| Full background probe output | \(|f_{T_0}|\le\sqrt{\mu_{T_0}\mathcal Q_{T_0}}\le Cq\epsilon_{\rm bg}\) | Direct Cauchy–Schwarz; \(q^{\gamma_*}\le\epsilon_{\rm bg}\) |
| Full rate versus core self-rate | \(O(q^2\epsilon_{\rm bg})\) | RTA backgroundrate, including all cross terms |
| Replacing full probe residual by core self-residual in input channel | \(O(q^2\epsilon_{\rm bg})\) | The preceding output bound times \(|\dot f_{K,2}^{\theta}|\le Cq\), from bounded scaled core source velocity |
| Core radial source-2 channel | \(O(q^4)\) | FWC \(h_2=O(q^2)\), while \(z=O(q)\), \(c^{\rm self}=O(q)\) |
| Core output source-2 channel | \(q^2\frac{\rho}{2}(1-N)\int_K(\zeta-x)K(\rho x)\,d\mu+O(q^{2+1/10}+q^4)\) | FWC sourcewise \(y'_2\), exact source derivative, compact core |
| Physical state versus coherent coefficient | \(O(q^{1/20})\) after division by q² | FWC current first-moment distance and physical mass comparison; bounded Lipschitz integrand |

In the compact core expansion, \(d^{\rm self}=1+O(q^2)\). This determines the positive sign of the output channel. It is not inferred from an absolute bound. All original training residual producers remain inside the source velocities. The argument makes no new Gaussian integration-by-parts step.

## Constants and time

Keep RTA/FWC's inherited order first. Fix T covering J and its radius R. Then choose the positive constants \(\delta_n,c_{\rm out}\) and the fixed error constant \(C_{\rm rem}\). Choose q last so that \(C_{\rm rem}q^{1/20}\le c_{\rm out}/2\). No constant depends on q.

Uniformity is exactly the unchanged \(\mathcal P_*\times J\). The clock remains
\[
\tau=\mu_1^2t_{\rm phys},\qquad
\tau_h=t_n+\lambda^{-1}\log((1-n)/n),\qquad s=\tau-\tau_h.
\]
Physical source rates and the physical r2 multiply normalized ones by \(\mu_1^2\). The lower bound is therefore \(\mu_1^2c_{\rm out}q^2/2\) in physical units.

## Provenance

Read-only fresh retrieval from TodManlaibaatar/OOD-reversals-theory:

| Path | Git blob SHA |
|---|---|
| README.md | 145b9f6e8db4377c00dee0478b8124c93dd996ed |
| 00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md (v1.27) | 6b7ee245b49877177cd1c086877f0984d1528821 |
| 01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex | cb458c933aa043cf0188fd11c46bf4246ffc91d8 |
| 07_compact_windows_AN07/AN07_rate_transfer_and_assembly_v1.tex | 1f909b9704f73c403cfd10ff35d086d6e8486b07 |
| 07_compact_windows_AN07/AN07_finite_window_continuation_v1.tex | f2c99953991d2bf8ce17d0bfb98845249e47d0bc |
| 04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex | 9e102514ad0a491066a2f9eb8eb86e9a251c2b53 |
| 00_roadmap/THEORY_HANDOFF_ANALYTICAL_A_B_v2.md | decb029fb314e96aae70e5eee68eaa969b6293ce |

Repository prefix search returned no existing an01bcv1: label. No prior increment, foundation, checkpoint or README was edited; no GitHub mutation was made.

## Revised S6 and S7/S8 handoff

A future deep-regime S6 contract must retain output rotation at leading order, then independently test the exact signed lag, help margin, and rate-weighted producer attribution. This increment does not claim that such a corrected full B-core theorem is proved.

The canonical/bridge regime still needs initialized access to its state class and error bounds relative to the exact small lag cancellation, not merely absolute O(q²) rate control. The positive output channel here does not provide those bounds, nor single out one factor as causing dominance reversal.

No continuation, quantitative horizon, checkpoint consolidation or canonical-regime theorem is attempted.

## Validation

- Standalone TeX compiles to 6 pages. The final compilation has no warnings, unresolved references, or overfull/underfull boxes. The PDF is only a compilation check and is not in the source delivery.
- All 15 labels are unique and use an01bcv1:. Internal references resolve; the prefix was absent from the fresh repository search and source snapshot.
- Both requested grep -nP commands were attempted; macOS grep lacks -P. The identical patterns returned zero matches with rg --pcre2 and independently with Python.
- Literal \rm, \tfrac, \qquad and \text survive (27, 8, 14 and 29 occurrences respectively).
- All seven Git blob hashes were verified against the retrieved contents; the scratch-save terminal newline was excluded from the hash calculation.
- All 96 pre-existing output files remain byte-for-byte unchanged by SHA-256 comparison.
- The source ZIP contains exactly the new TeX and same-stem review Markdown, with no PDF, and its members are byte-identical to the delivered files.

Compilation, text scans and archive checks are document validation only. No trajectory, numerical experiment or computational sign premise was used in the proof.
