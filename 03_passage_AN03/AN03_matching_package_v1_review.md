# Review: AN03 matching package v1

Companion: `AN03_matching_package_v1.tex`  
Label prefix: `an03mpv1:`  
Date: 30 October 2026  
Scope: S4c matching inputs, entirely inside RB's completed weak passage.

## Result

**All six requested steps close.** Take the whole closed clock cohort (S=\mathcal C_q), start at the first (H=q^{1/8}), and end at the first (H=h), where (h>0) is fixed and satisfies WBR's upper bounds. No labels are removed, and no additional hypothesis is imposed.

The new matching theorem proves, uniformly on that interval:

\[
\frac{H_{G_+\setminus S}}H\asymp q^{1/4},\qquad
H_{G_+\setminus S}+\mu_\Sigma+\mu_B=O(q^{1/4}H),
\]

\[
c=H(1+O(q^{1/4}))+O(q^2),\qquad
\sup\left|\log\frac HN\right|
\le C\left(q^{1/8}+q^2\ell+\frac{q^{1/4}h}{Q(1-c_b)}\right)=o(1),
\]

where (N'=\lambda N(1-N)) and (N(t_s)=H(t_s)=q^{1/8}). It also proves

\[
N_S/H=1+O(q^2),\qquad N_{\rm nc}/H=1+O(q^{1/4}),\qquad
J_S\le C(q^3+q^2H),\qquad
A_0=\sqrt{N_0}W_2(t_s)=O(q^{1/16}).
\]

Here (N_S=\mu_S), and (N_{\rm nc}=\mu_{G_+}+\mu_\Sigma+\mu_B) is the entire non-core radial mass. Proving the stronger statement with all of (B) avoids choosing or differentiating a weak-side mask. Any weak population containing (S) and contained in the fixed non-core population has the same relative mass conclusion.

The mass-deficit estimates include

\[
\sup|1-\mu_K|=O(q^{11/10}),\qquad
\sup|1-\mu_K|L=O(q^{101/640}),
\]

with the explicit integrated bounds below. These are matching inputs; the field reductions, local strong guard and selection theorem are still S4d.

## Step-by-step status

| Step | Status | Result and source labels |
|---|---|---|
| 1. Population accounting | Closed | `band`, `accounting`: the primary band is a vanishing fraction (\asymp q^{1/4}); all omitted non-core mass is (O(q^{1/4}H)); exact response ledger gives `response`. |
| 2. Logistic phase | Closed | `phase`: a sign-contracting equation for (\log(H/N)), the absolute BULK defect budget, and the proved response error give uniform (o(1)) phase and (\int|N-c|=o(1)). |
| 3. Mass identities | Closed | `masses`: exact balance and WBR alignment; the coarse bound is obtained first, then sharpened using step 4 without circularity. |
| 4. Initial smallness | Closed, (p=2) | `transverse`, `smallness`: BULK `forcing/Jprop` applies with (G=S,\sigma=0); (A_0\le C(q^{1/2}+q^{1/16})). |
| 5. Late mass defects | Closed | `massbudgets`: pointwise and integrated scalar, large-coordinate and bounded-comparator costs. |
| 6. Matching theorem | Closed | `main`: no retained extra hypothesis. The statement does not apply TAILREP selection. |

There is no unmatched inequality in the matching theorem. The coarse supremum route proposed in step 4 is insufficient on part of the parameter box, as detailed below, but the independently proved transverse theorem closes that step.

## Population accounting: definitions and endpoint audit

The exact primary set is (G_+=\{b\in Q2:c_0\ge Kq^\gamma\}), the recruited set is (\Sigma=\{c_0<Kq^\gamma\}), and the clock is (S=\{c_0\ge q^{1/4}\}\subset G_+). The union defining (G_+) is counted only once. Since (\gamma>7/20>1/4), for small (q) the omitted primary band is

\[
P_q=\{Kq^\gamma\le c_0<q^{1/4}\}.
\]

Its angular measure is comparable to (q^{1/4}): the density in (c_0) is ((2\pi\sqrt{1-c_0^2})^{-1}), bounded above and below on this band. There (s_0\asymp1).

RB `primaryseed` and Q2EC's two-sided original coordinate transport imply

\[
U_2(t_0,b)^2\asymp A_q^{-\lambda}q^k(s_0+q)^2\quad(b\in G_+).
\]

The entry bound (|a_-|/z\le1/4) converts (U_2^2) to (z^2) by fixed factors. Thus (H_{P_q}(t_0)\asymp A_q^{-\lambda}q^{k+1/4}), whereas (H(t_0)\asymp A_q^{-\lambda}q^k). The (A_q^{-\lambda}) factor cancels in their ratio. RCET's transport multiplies it only by fixed factors (e^{\pm2D_+}), so it stays (\asymp q^{1/4}). A fixed distortion does preserve a vanishing ratio; no (D_+=o(1)) assertion is needed.

This use of the seed keeps both regularizers (s_0+q,c_0+q) and Q2EC's matched crossing sector. At (b=\pi), (s_0+q=q); the original clock endpoint is not omitted and its zero initial (U_2) is not placed inside a coordinate logarithm. The threshold endpoints are likewise included. All cohorts are fixed initial label sets; endpoints have zero integration measure, but WBR's return remains labelwise on the closed set.

For (H\ge q^a), (a=1/8), the remaining mass charges are

\[
\mu_\Sigma/H\le C(q^{\Gamma_\nu}+q^{5-a}+q^{2-a}),\qquad
\mu_B/H\le q^{11/10-a}=q^{39/40}.
\]

Every displayed exponent exceeds (1/4). The (J_{P_q}\le q^2K_Y^2) contribution also becomes (O(q^{15/8}H)). This proves the whole non-core accounting, including the strong complement and both strips inside the existing (B) budget. No new outside-entry or gate assumption is made.

For the response, the selected ledger is used as an identity:

\[
c_S=H-A_S+\tau_S.
\]

WBR alignment gives (A_S\le Cq^2N_S). Its reached weak chart implies (\sin\theta\ge1/2), so a Gaussian projected-tail bound gives the **absolute** estimate (|\tau_S|\le CN_Se^{-c_*/q^2}). LCRC's one-sided lower bound on (\tau_S) is not incorrectly used for an upper error. The other groups are charged in absolute value using

\[
|c_T|\le E_T+\frac{2q}{\sqrt Q}\sqrt{E_TJ_T}
\le2E_T+\frac{q^2}{Q}J_T.
\]

The core contributes (O(q^2)), and the whole outside response is at most (C\mu_B). This yields the stated response error with the (O(q^2)) term kept separate.

## Phase and hitting-time audit

The exact error equation, with (x=\log(H/N)), is

\[
x'=\lambda N(1-e^x)+q^2(1-c)+\lambda(H-c)+\varepsilon_H.
\]

The first term always opposes the sign of (x). Therefore (D^+|x|\le q^2|1-c|+\lambda|H-c|+|\varepsilon_H|). The proof uses the **absolute** integral bound on (\varepsilon_H) from BULK. A bound on the primitive (\delta(s,t)) alone would not justify bounding its total variation.

The backward clock estimate gives (\int H\le e^{D_q}h/[Q(1-c_b)]), so

\[
\int|H-c|\le Cq^{1/4}h/[Q(1-c_b)]+Cq^2\ell.
\]

This avoids an artificial factor (e^{Ch\ell}). It proves uniform (o(1)) phase, then (\int|N-c|=o(1)) as a consequence. The (q^2\int(1-c)) term and the exact coefficient (\lambda\int(N-c)) are retained.

For any fixed (n\in(0,h)), both the actual clock hit and the auxiliary logistic hit occur strictly before (t_e). Exact logistic integration gives their time difference as

\[
\frac1\lambda\left[-x(t_H(n))+
\log\frac{1-n}{1-ne^{-x(t_H(n))}}\right]=o(1).
\]

At (n=h), the auxiliary logistic hit may fall just after (t_e). The same scalar identity is valid, but it is not used to extend any original-flow estimate. For S4d a fixed (n=h/2), or any fixed (n<h), avoids this endpoint issue entirely. No matching is made through the (O(1)) phase of (t_b).

## Why (A_0\to0) is now proved

BULK's separate-clock theorem `forcing` is an original Cartesian energy result, not a bounded weak-chart theorem. With (G=S) and (\sigma=0), all of its inputs hold:

\[
E_S\le10H/9\le C_E(q^5+H),\quad
J_S(t_0)\le C_Jq^3,\quad
\ell_S\le L_\times q,\quad \int r_S\le B.
\]

The positive clock, response range, logarithmic duration and subinterval lower defect bound also hold by RB/BULK. The entry energy is Q2EP's proved whole-Q2 bound restricted to (S). Thus `Jprop` gives

\[
J_S(t)\le C(q^3+q^2H(t)).
\]

This is not inferred from the weaker (J_G\le q^2K_Y^2) guard. The exact identity (N_S=H+A_S+J_S) and (A_S\le Cq^2N_S) now give

\[
N_S/H=1+O(q^2+q^3/H)=1+O(q^2)
\]

on the chosen interval. The earlier accounting and phase arguments used only the coarse (N_S\le CH), so there is no circularity.

At entry choose the actual probability (d\eta_s=m(t_s,b)d\lambda_0/N_S(t_s)). The definition of (W_2) is WEAK's distance to the selected branch at the **auxiliary** mass (N_0=H(t_s)). AN06 bounds its coordinates by (0<U_*<1), (0<V_*<11/10) for (0<N\le1/2). On the reached chart,

\[
\int_Sm(u^2+v^2)\le C J_S/q^2,
\]

so (N_0W_2(t_s)^2\le C(q+q^{1/8})). This proves (A_0=O(q^{1/16})) for (p=2). The incoming normalized measure is defined here; no claim that the original normalized radial weights remain constant is used.

### Audit of the coarse supremum route

For a hypothetical start (H=q^{\widetilde a}), the quoted BULK size gives

\[
p(\widetilde a)=15/8-(k-\widetilde a)(1-c_b)/4.
\]

The simultaneous sufficient conditions (p(\widetilde a)<1) and (\widetilde a/2-p(\widetilde a)>0) require

\[
\frac{15/2-k(1-c_b)}{1+c_b}<\widetilde a
<k-\frac7{2(1-c_b)},
\]

which is possible on this box only if

\[
k>\frac{11}{2}+\frac{7c_b}{2(1-c_b)}.
\]

Thus the proposed (k>5.5) count is a necessary limiting condition; for fixed positive (c_b) it is not the exact sufficient threshold. The displayed interval is empty at (\rho=7/10), where (k=51/10). This is the exact failing inequality of the coarse alternative, not a gap in the matching theorem. The regenerated transverse route closes the whole ratio box.

## Late mass-defect ledger

WBR's pointwise rate is used as a proved conclusion:

\[
|1-M(t_s+w)|\le C(q^{\alpha_M}e^{-w/3}+q^{11/10}),\quad
\alpha_M=(k-1/8)/(3Q)\ge199/60.
\]

BULK's decaying size gives (L_t=C(1+q^{-603/640}e^{-b_0w/4})). Retaining this time decay avoids paying a logarithmic factor on its large-coordinate part.

| Defect | Supremum | Integral on ([t_s,t_e]) |
|---|---|---|
| (|1-M|) | (Cq^{11/10}) | (C(q^{\alpha_M}+q^{11/10}\ell)) |
| (|1-M|L_t) | (Cq^{101/640}) | (C(q^{\alpha_M-603/640}+q^{101/640}+q^{11/10}\ell)=O(q^{101/640})) |
| (|M-1||Y_*|) | (C_*q^{11/10}) | (C_*(q^{\alpha_M}+q^{11/10}\ell)) |
| (|M-1|\mathsf K(\rho X_*)) | (C_*q^{11/10}) | Same as the preceding row |

The comparator bounds use AN06's selected half-learning region, since the matched (N\le2h<1/2). The mass terms alone can be charged entirely as a value error (O(q^{101/640})), or split into an additive bounded-comparator error (O(q^{11/10})) and a linear coefficient (\ell_M=C|1-M|), whose integral is (O(q^{11/10}\ell)). These are alternative allocations of the same terms. They do not claim that all other terms in TAILREP's error inequalities have been paid.

## Hypothesis-matching table

| Source used | Hypotheses used, including range/sign conditions | Where supplied |
|---|---|---|
| RB `completed`, S4 handoff | Original balanced isotropic initialization, (\kappa=10), closed (\rho) box, WPT constant order, sufficiently small (q). | Current model. RB supplies (0<c\le c_b), finite passage, residual/core/secondary/outside states. |
| WBR `main`, `clockalignment`, `massrate`, `latechart` | RB passage; whole closed clock; WBR fixed constants and upper bounds on (h); start (H=q^{1/8}); sufficiently small (q). | Exactly the selected cohort and levels here. Its input-return theorem is not extended to the omitted primary group. |
| Q2EC matching and coordinate transport, as used by RB `primaryseed` | Original S1 flow, regularized closed Q2 sector, fixed large matched band, positive coordinates after crossing, actual angle above (qL) and target above (16qL) until (t_0), bounded shift from (10\ell). | Q2EC's primary-sector proof and RB's explicit seed verification. These include the late boundary label (b=\pi). |
| RCET `transport` | Two fixed positive-amplitude subsets of (G_+); (0\le c\le c_b<1); logarithmic duration; diagonal residual bound and (O(q)) cross residual; (\int r\le B); positive entry (z), antisymmetric ratio at most (1/4), entry (qj/z\le C_0); admissible small fixed (C_0), then (q). | RB/Q2EC and the fixed sets (P_q,S\subset G_+). The distortion is bounded, not assumed to vanish. |
| LCRC `identity`, `responsecharge`, `signgood` | Fixed measurable cohorts with finite mass; the identity/absolute charge allow arbitrary signs; signgood requires the already matched localclock inputs. | RB's completed states. Positive (W_2,U_2) on (G_+) is inherited. The selected absolute negative-gate error is proved separately using its reached chart. |
| RB secondary and outside bounds | Entire fixed (Sigma,B), all prior stopped inputs discharged in RB, including both strips. | Used as conclusions with (\Gamma_\nu>3/10) and (\sup\mu_B/q=o(q^{1/10})). No strip field or weak-side mask is newly assumed. |
| BULK `bulkdefectconclusion`, clock proof | Fixed clock, (0<\eta=1/8<1), positive finite entry amplitude, original Cartesian entry ratios, response/residual/learning/duration bounds. | RB/Q2EC. Supplies the absolute defect integral and monotonicity of (H), not merely a primitive-error bound. |
| BULK `forcing`, `Jprop` | Positive separate clock; (b_0>0); subinterval lower defect bound; (E_G\le C_E(q^5+q^\sigma H)), (\sigma\ge0); (J_G(t_0)\le C_Jq^3); cross matrix (\ell_G\le Lq); (\int r_G\le B); logarithmic duration and fixed constants. | Take (G=S,\sigma=0). Signgood gives the energy input independently of (J_S); Q2EP gives entry (J_S); RB gives residual and integral budgets; BULK `residualinputs` converts residuals to matrix entries. |
| Q2EP `entryenergy` | Original S1 flow at (t_0=t_h), fixed subcohort of Q2, bounded (A_q), model box and small (q). | (S\subset Q2), unchanged initialization and entry time. No labels outside Q2 are added to this use. |
| AN06 `regiontheorem` | Selected leading branch, ratio box, (0<N\le1/2). | Applied only to comparator coordinates; phase matching gives (N<2h<1/2). No original strong-reference closeness is inferred. |
| WEAK (W_p) definition / TAILREP error inventory | Probability of fixed labels, finite (L^p) entry coordinates; bounded selected comparator at the same auxiliary (N_0). TAILREP's actual differential inequalities and local guard are separate hypotheses. | Actual incoming (\eta_s), reached finite chart for fixed (q), (p=2). Only the norm and mass-defect contract are used; neither WEAK nor TAILREP selection is invoked. |

## Constants and order

The order is **WPT/RB → WBR → start exponent (a=1/8) and (p=2) → fixed admissible (h) → (q)**. The newly displayed constants are determined by already fixed bounds and do not select an earlier guard.

- The band constants use Q2EC's fixed matching factors, the bounded (A_q) interval and RCET's fixed (e^{2D_+}). The common (A_q^{-\lambda}) seed factor cancels in the ratio.
- (C_J') in (J_S\le C_J'(q^3+q^2H)) uses fixed (B,L_\times,C_J,b_0), a fixed upper bound for (D_q), and the independent signgood energy constant. It is independent of any proposed (A_0) bound and of a future selection guard.
- Phase constants retain (1/b_0=1/[Q(1-c_b)]) in the integral bound and (1/[\lambda(1-h)]) in the first-hit comparison. The time normalization uses (Q) in the original clock and (\lambda) in the logistic equation.
- The late rate keeps (\alpha_M=(k-a)/(3Q)), including the actual (Q=\lambda+q^2). The uniform rational lower bound is used only after choosing (q) small enough that (Q\le1/2).
- AN06 supplies model-only bounded comparator constants on the half-learning region. No local strong stability radius or small-gain constant is selected here.
- WBR's conditions on (h) are upper bounds. S4d may decrease (h) after fixing its new constants; each fixed smaller choice preserves this package. Uniformity as an unspecified (q)-dependent (h\to0) is not claimed.

## S4d handoff and unmatched future work

| Supplied matching input | Proved accuracy / limitation |
|---|---|
| Full clock cohort and original return | WBR's entire closed (S), no discarded relative mass, reached chart (qL=O(q^{37/640})), strict boundary margin. |
| Primary population accounting | Omitted amplitude is exactly of fixed-factor order (q^{1/4}H). No return for (G_+\setminus S) is needed for this mass/response accounting. |
| Whole non-core accounting | (N_{\rm nc}=H(1+O(q^{1/4}))); includes all (B) as an upper charge. A field cost divided by (q) is not automatically small from this statement. |
| Response matching | (c=H(1+O(q^{1/4}))+O(q^2)); selected negative-gate error is absolutely exponentially small on the reached chart. |
| Logistic matching | Uniform (o(1)) logarithmic phase, (\int|N-c|=o(1)), fixed interior levels have (o(1)) hitting-time difference. |
| Exact radial mass identity | (N_S=H+A_S+J_S), (A_S=O(q^2N_S)), (N_S/H=1+O(q^2)). No exact logistic law is assigned to (N_S). |
| Initial smallness | (p=2), (N_0=q^{1/8}\to0), (A_0=O(q^{1/16})\to0), with the actual incoming probability. |
| Mass-deficit terms | Pointwise and integrated bounds in the ledger above; both bounded comparator and large-coordinate terms retained. |
| Safe later endpoint | Any fixed logistic level (n<h), for example (n=h/2), occurs strictly before (t_e<t_b). |

Still unmatched, by design and out of scope: the full original weak-chart and strong-reference field reductions to TAILREP `strongerror/weakerror`; the common additive (d_0\to0) and integrated coefficient (\int\ell_B\le L_*) after all field and weight terms are included; the local strong-reference initial guard and its small-gain condition; the selection theorem. Fixed labels do not imply constant normalized original radial weights. This package does not supply their derivative defect by definition, nor does mass accounting alone give the required weak field reduction.

No missing item is inserted as a hypothesis of the matching theorem. No result beyond (t_b), no consolidation and no selection conclusion is claimed.

## Provenance and checks

README, roadmap **v1.20**, and the sources below were fetched read-only from `TodManlaibaatar/OOD-reversals-theory` for this request. SHAs are file identifiers returned by the connector. The new prefix was checked against local prior TeX/Markdown files and repository code search; no collision was found.

| Source | Repository path | Fetched file SHA |
|---|---|---|
| README | `README.md` | `3844b1a5c5a287f1f214cc9b58b32ca3e17fa6b4` |
| Roadmap v1.20 | `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | `26af8ac58130927ba3bec1c57ec45d8180826b8e` |
| WBR | `03_passage_AN03/AN03_weak_boundary_return_v1.tex` | `c1f18203cc99ca5ddcda9481ca1281d7debffa9a` |
| RB | `03_passage_AN03/AN03_response_barrier_v1.tex` | `5312b5093f3ed4f74063347df31ae5a29155255f` |
| SI | `03_passage_AN03/AN03_selection_interface_v1.tex` | `9c984392caa650505b5c961796529fb4acc751ea` |
| BULK | `03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` |
| LCRC | `03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex` | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` |
| RCET | `03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex` | `49e352002b4c699338ac99a4d55d51c60760ea86` |
| TAILREP | `03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex` | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| WEAK | `03_passage_AN03/AN03_weak_transit_forcing_and_orbit_selection_v1.tex` | `3a937aa25253b5773424a3f165f71d476157575a` |
| Q2EC | `02_entry_AN02/AN02_Q2_entry_contracts_v1.tex` | `b149537025e130801fc55b9e49c365c158eee17b` |
| Q2EP | `02_entry_AN02/AN02_Q2_entry_through_strong_passage_v1.tex` | `042b3c93cf8402d10487f9e56f6f5b1d869c424a` |
| AN06 | `04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex` | `9e102514ad0a491066a2f9eb8eb86e9a251c2b53` |

Verification is source/hypothesis inspection, displayed analytic inequalities, TeX compilation, reference/label checks and prior-file integrity checks. Compilation is a typesetting check, not mathematical certification. There were no experiments, numerical premises, trajectories, grid checks or interval arithmetic. The delivery archive contains only the new raw `.tex` and `_review.md` files. No prior increment, foundation, checkpoint or GitHub content was modified.
