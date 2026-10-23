# AN03 Q3 strip budgets v1 — review note

**Status: partial; stopped separately on both parts.** The full two-strip supremum and integrated mass budgets have not been proved. The stopped hypotheses remain those of S2CP/CFA. The new results do not import CFA's conditional passage conclusion, its strip integral, or the future weak-passage bootstrap.

The companion source is `AN03_Q3_strip_budgets_v1.tex`; every new label uses `an03q3sbv1:`. The source ZIP contains that raw TeX file and this Markdown review only.

## Task-by-task result

| Task | Status | Result / exact stopping point |
|---|---|---|
| A1: local entries and pre-entry cross residual | **Closed** for the needed estimates | `crosspre`: \(\sup_{[0,t_0]}(\|e_1\|_{P_2}+\|e_2\|_{P_1})\le C_{\rm pre}q\), derived from OWPT and MOMC. Loss alone gives local \(R_{11},R_{21}=O(q)\); \(R_{12}\) uses the derived cross residual. |
| A1: near-π drift | **Closed on each fixed scaled chart before \(t_m\)** | `pifield` has the requested \(\Phi(-\rho x)\). On the aligned ray its two leading components are \(-\rho K(-\rho x)/2<0\). This is not asserted uniformly up to \(x=2\Lambda_q\), nor as a new post-\(t_0\) c-form theorem. |
| A2: pre-entry gate budget | **Closed** | `gatepre`: \(\sup(|c|+N_-)+\int_0^{t_0}(|c|+N_-)\le C(q^u+q^2\ell^2)=o(1)\). |
| A2: sine envelope and total clock | **Closed with the necessary q seed** | `Nenv`: \(N(t)\le\min\{2,C_{\rm env}(N(0)+q)e^{\beta I_{\rm tot}(t)/2}\}\). `totalclock`: \(e^{I_{\rm tot}(t_*)}\le C E_g A_q^{-q^2}q^{-10-10q^2}\). |
| A3: proposed absolute radial gain | **Stopped: false premise** | `falsegain` uses \(N(0)^2\), which vanishes at the π-axis label. Actual mass there grows by an unbounded factor; see the explicit inequalities below. |
| A4: radial estimate after leaving the π neighborhood | **Not claimed after A3 stop** | Post-\(t_0\) strong-diagonal cost is paid by \(B\). The exact remaining pre-entry absolute-value budget is `unpaidradial`; a signed substitute would also suffice. The sine-envelope continuation does not pay this radial term. |
| A5: whole π-strip mass | **Not proved** | Neither the expected \(O(q^3\ell^{3/2})\) bound nor CFA's small fixed integrated allowance is asserted for the whole strip. |
| B1: all labels remain on lower side | **Stopped: false premise** | `lowerfailure`: the axis label is MOMC's \(-\pi/2\) endpoint and is in the positive strong chart at \(t_0\). Continuity supplies a positive-measure adjacent interval. |
| B2: extend whole-family bounded chart to the strip | **Stopped: false premise** | `falsechart`: an explicit positive-width substrip remains near \(-\pi/2\) throughout \([0,t_*]\), so \(\xi(t_0)\ge c/q\). No fixed chart cap exists for the whole strip. |
| B2–B3: frozen part | **Closed subset** | For \(F_q=[3\pi/2-7w_q/4,3\pi/2-3w_q/2]\), \(\sup\mu_{F_q}/q\le Cq^{10}\ell^{1/2}\), \(\int\mu_{F_q}/q\le Cq^{10}\ell^{3/2}=o(1)\). |
| B2–B3: remaining joined/transition labels | **Unpaid; no third route attempted** | Need `missingtail` / `missingmoment` for charted labels and an actual-arrival estimate `missingarrival` for the others, including pre-arrival mass. The frozen counterexample does not disprove a raw weighted tail or the ultimate strip budget. |

## Part A: proof audit and exact obstruction

### Pre-entry inputs are conclusions of S1

No cited S1 statement explicitly names the pre-entry cross-residual contract. The new lemma derives it:

- On \([0,t_m]\), OWPT's \(S\le q^{10}e^{(1+2q^2)t}\) implies \(\sup S+\int S=O(q^u)\), \(u\ge169/102>1\). The bound \(|f(X)|\le S|X|\) pays both cross outputs.
- On \([t_m,t_0]\), MOMC's strong donor angles are bounded by \(Rq\), with \(R=79/51\), mass \(M\le1/2\), and \(\int M\le3/2\). Their cross outputs have norm \(O(qM)\).
- MOMC's entire left-ancestry mass, including both strips, is at most \(Cq^2\ell^2M\). It pays the remaining cross outputs. This only uses a proved pre-entry mass estimate.
- On \(P_2\), a strong donor has both \(W_2=O(q\sqrt m)\) and \(U\cdot X=O(q\sqrt m)(|Z|+|V|)\). Thus its response is \(O(q^2M)\), which is stronger than the cross-output estimate and pays the signed gate integral.

Before \(t_0\), \(c\) need not be nonnegative. The proof retains \(|c|\) and obtains \(\sup|c|=o(1)\). In the signed bound,
\[
Qc+N_-=\mathbb E_{P_2}[(f_2X_2)_+]\ge0.
\]
The two GESG signed inequalities imply the stated bound for \(X\) whenever \(c\le1\). There is no implicit assumption \(c\ge0\) before entry.

### The global sine continuation does not need a radial conclusion

Until \(N=1/2\), the input remains in \(\cos\theta\le-\sqrt3/2\), so the local \(R_{11}=O(q)\) estimate applies. Duhamel produces the additive \(q\) seed. After first exit, \(N\le2\) and the total clock increases; multiplying the first-exit estimate by four covers all future re-entries. This closes the sine envelope without claiming a pre-entry bound on the global strong residual.

The source of the post-entry \(X\) budget is **S2CP's gate lemma under its current stopped inputs**, including its retained outside supremum and secondary estimate. It is not CLOCK forcing, CFA passage, or a conclusion of the desired strip budget.

The exact clock algebra is
\[
e^{I_{\rm tot}(t_0)}=A_q^{-Q}q^{-10Q}e^{o(1)},\qquad
e^{I_{\rm tot}(t_*)-I_{\rm tot}(t_0)}
 \le C E_g A_q^\lambda q^{-10(1-\lambda)}.
\]
Hence the remaining factors are \(A_q^{-q^2}\) and \(q^{-10-10q^2}\). The proof does not set \(Q=\lambda\) or \(1/\beta=1\).

### False radial inequality

The rejected statement is exactly
\[
m(t,b)\le C m(0,b)
 \max\{1,CN(0,b)^2e^{\beta I_{\rm tot}(t)}\}^{1/\beta}.
\]

At \(b=\pi\), \(N(0,b)=0\). PROFILE's exact target coordinate equation creates
\[
\widehat U_2(1)\ge cq^6,\qquad
\widehat U_2(t)\ge cq^6e^{\lambda(t-1)/2}.
\]
Q2EC's **all-label** early comparison transfers the radial lower bound at \(t_m\):
\[
\frac{m(t_m,\pi)}{m(0,\pi)}
 \ge c e^{-Cq^u}q^{2-\lambda c_m}\to\infty,\qquad
\lambda c_m-2\ge \frac{210239}{184800}>0.
\]
The proposed right side is only \(C m(0,\pi)\). For each sufficiently small fixed \(q\), continuity makes the failure hold on a positive-measure interval immediately inside Q3, not just on its endpoint.

The endpoint failure can also be seen at \(t_0\). Q2EC's band matching and second-coordinate transport apply to its included boundary label \(b=\pi\), which lies in the clock cohort. They give
\[
m(t_0,\pi)/m(0,\pi)\ge cA_q^{-\lambda}q^{2-10\lambda}\to\infty,
\quad 10\lambda-2\ge89/40.
\]
This is a use of the proved Q2 boundary contract, not an extension to Q3.

A necessary correction is an initial size comparable to \(N(0)+q\). RCET's \((s_0+q),(c_0+q)\) endpoint regularization already signals this requirement. **The corrected absolute radial gain is not proved in this increment.** The false requested estimate triggers the stop rule even though its repair may preserve the expected strip exponent.

The valid differential radial upper bound includes the projected-gate \(O(q)\) term on the lower side. A remaining cost for a direct absolute-value proof, after leaving the local π region before \(t_0\), is
\[
\sup_{b\in\mathcal S_\pi}
 \int_{\substack{0\le t\le t_0\\\cos\theta(t,b)>-c_*}}
 |R_{11}(\theta(t,b))\cos\theta(t,b)\cos\psi(t,b)|\,dt
 \le C_{\pi,\rm rad}.
\]
A signed sufficient substitute could replace this absolute-value budget. No such budget is inferred from \(\int_{t_0}^{t_*}r<B\), whose time domain is different.

## Part B: proof audit and exact remaining consumer

### Joined and frozen portions coexist

The lower-side shortcut fails at the axis label by periodicity with MOMC's right-half endpoint. Its positive scaled strong position at \(t_0\) also holds for some neighboring Q3 labels by continuity. No width uniform in \(q\) is extracted from that argument.

For the outer substrip \(F_q\), both input gates stay closed in the buffer
\[
w_q<3\pi/2-\theta<3w_q.
\]
GESG's loss-only speed lemma applies from initialization. Since
\[
e^{-k_G\Lambda_q^2}=q^3,\qquad
Cq^3t_*\le CC_{\rm dur}q^3\ell=o(w_q),
\]
the label cannot leave the buffer. The radial mass remains \(q^{10}e^{O(q^3\ell)}\), and its width is \(w_q/4\asymp q\sqrt\ell\). This proves both mass budgets for \(F_q\).

This also disproves the proposed **uniform bounded-chart entry of the entire strip** at \(t_m\) or \(t_0\). Its displacement is at least \(c/q\) on \(F_q\). It does not disprove a weighted tail: such labels are exceptionally light, and are paid separately here.

### Required correlation, not just total left mass

The existing strong tail is for the right-half ancestry. Its parameter is
\[
\epsilon_h=\sqrt2\,A_q^d(1-M_0)^\alpha q^{10d-s},
\qquad p=3/s.
\]
For a charted extension \(J_0\), the raw consumer is
\[
\eta_{J_0}\{\xi>v\}\le C_T\min\{1,(\epsilon_h/v)^p\},
\qquad d\eta_{J_0}=m(t_0,b)d\lambda_0.
\]
The TeX gives the equivalent TAILREP weighted-moment consumer at the cutoff \(d_c\). It must be proved for the new ancestry, not imported from the normalized right-half law.

For an actual arrival time \(\tau_b\), the remaining contract is the bound on \(\mathcal W_J\) in equations `arrival` and `missingarrival`: unarrived mass plus the mass at actual entry weighted by
\[
\max\{1,A_0q^2\xi_b^2
 e^{\beta[I_{\rm tot}(t)-I_{\rm tot}(\tau_b)]}\}^{1+\nu}.
\]
The gain from arrival and its aggregate supremum/integral must both be supplied. A fictitious entry at \(t_0\) is not allowed. MOMC's \(Cq^2\ell^2\) total left mass alone does not bound this weighted correlation.

After the lower-side and whole-strip chart premises fail, no further recruitment argument is attempted. The arrival consumer is recorded as unpaid, not added to a claimed full theorem.

## Constants and retained inputs

| Constant or factor | Source and dependencies |
|---|---|
| Loss/Gaussian constants; \(k_G=169/3200\) | Initial loss and ratio box only; no LCRC guards. |
| \(R=79/51\), \(c_A,C_A\), \(C_{\rm pre}\) | Proved MOMC/OWPT/S1 constants; guard-independent. |
| Fixed near-π chart constants \(C_L\) | Model and the selected fixed \(L\); no assertion on a growing \(\Lambda_q\) chart. |
| \(C_{\rm dur}\) | Retained stopped duration \(L_T\), model, bounded \(A_q\); affects the small-q threshold in the frozen proof. |
| \(C_{\rm env}\) | \(a_*=C(1+\max(C_{\rm pre},M_{\rm res}))\), \(a_0=\lambda_{\min}\min(1/2,1-c_b)/2\), and \(G=5eE_g/[9(1-c_b)]\). One choice is \(4e^{G+1}\max(1,a_*/a_0)\). No \(B\) is used in the sine proof. |
| Total-clock constant | Existing stopped-clock and entry-seed constants; \(A_q^{-q^2}\) and \(q^{-10-10q^2}\) remain explicit. |
| \(C_{\pi,\rm rad}\) | **Unpaid**, not chosen. After \(t_0\) its analogous cost is paid by \(B\). |
| \(A_0,C_m,C_T\) in the arrival/tail consumer | Existing consumer constants, not constructed for new Q3 ancestry here. Keep \(1/\beta=1+q^2/\lambda\), or the permitted fixed upper exponent \(1+\nu\). |
| CFA \(C_{\mathcal S},P_{\rm allow},\overline F_F\) | Unchanged. Only the \(F_q\) portion is now below their fixed allowance for small \(q\). No full-strip \(F_{\mathcal S}\) has been supplied. |

The retained outside supremum used in the post-entry gate lemma is not confused with a newly proved strip supremum. No new guard is added to a claimed full theorem. No core geometry, reference bound, duration improvement, selection, or passage assembly is proved here.

CFA's constant order remains unchanged. In particular the model and guard-independent chart/core constants precede \((B,K_Y,M_{\rm res})\), then the fixed field/passage allowances and small \(c_b\), then \(C_0\), entry constants, and finally \(q\). The failed estimates cannot be repaired by choosing a fixed constant after \(q\).

## Source provenance

Read from the repository without mutation on October 22, 2026. Hashes below are Git **blob** hashes returned by the repository connector, not a claim that all fetches constitute a pinned commit. The roadmap identifies itself as v1.13.

| Source | Repository blob SHA |
|---|---|
| [00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md) | `05d41d76e344bd013de846c8174c2e0245f8587c` |
| [03_passage_AN03/AN03_c_form_assembly_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_c_form_assembly_v1.tex) | `341908c228092e9a818d98de3ec26591a1050364` |
| [03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex) | `f00459b5ca412eb86b0893adb64766e2c10d5590` |
| [03_passage_AN03/AN03_S2_closure_package_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_S2_closure_package_v1.tex) | `baeb8a7eb1e36ce86319782511b665944be1afda` |
| [03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex) | `a490ea323e45e61c1a58301554b89ad84cb02605` |
| [03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex) | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| [02_entry_AN02/AN02_overlap_window_profile_transfer_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_overlap_window_profile_transfer_v1.tex) | `8fac13f9d36255d3e2e23cc9b2196719ec602907` |
| [02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex) | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| [02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex) | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` |
| [02_entry_AN02/AN02_Q2_entry_through_strong_passage_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_Q2_entry_through_strong_passage_v1.tex) | `042b3c93cf8402d10487f9e56f6f5b1d869c424a` |
| [02_entry_AN02/AN02_Q2_entry_contracts_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_Q2_entry_contracts_v1.tex) | `b149537025e130801fc55b9e49c365c158eee17b` |
| [02_entry_AN02/AN02_secondary_entry_profile_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_secondary_entry_profile_v1.tex) | `c7c857ec10b7f7b2cf42d1cdb452c50edc735587` |
| [03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex) | `49e352002b4c699338ac99a4d55d51c60760ea86` |

## Verification and packaging

- The proofs use analytic inequalities and exact rational arithmetic only. No simulations, trajectories, sign grids, or interval arithmetic were used.
- The standalone TeX compiled successfully to seven pages with no warnings or overfull boxes in the final log. All 27 labels use the new prefix; all 19 internal references resolve. Compilation is a source/syntax check, not numerical evidence for any mathematical claim.
- The final archive contains only the requested raw `.tex` and same-stem `_review.md`; it contains no PDF.
- All 39 pre-existing output files matched their pre-task SHA-256 hashes. No prior increment, foundation, checkpoint, or roadmap was edited; no GitHub write or merge was performed.

