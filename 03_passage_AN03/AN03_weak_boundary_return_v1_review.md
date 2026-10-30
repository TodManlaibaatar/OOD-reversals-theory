# Review: AN03 weak boundary return v1

Companion: `AN03_weak_boundary_return_v1.tex`  
Prefix: `an03wbrv1:`  
Date: 30 October 2026  
Scope: S4b only, on the already completed RB passage. GitHub and prior increments were read-only.

## Result and status

**Steps 1–6 close, up to a fixed small clock level.** The selected cohort is the entire closed clock cohort

\[
S=\mathcal C_q=\{b\in[\pi/2,\pi]:-\cos b\ge q^{1/4}\}.
\]

There is no sign-based deletion and no excluded weak mass. The endpoint (b=\pi) and the threshold endpoint are included.

With all WPT/RB constants already fixed, choose a fixed sufficiently small (h>0), then (q). Set

\[
t_s=\inf\{t\ge t_0:H(t)=q^{1/8}\},\qquad
t_e=\inf\{t\ge t_0:H(t)=h\}.
\]

Then (t_s-t_0\to\infty), (t_s<t_e<t_b), and every selected original characteristic has (u\ge0) on ([t_s,t_e]). In fact the proof preserves (u>0) from (t_0). At the boundary, uniformly on the reached chart,

\[
u'|_{u=0}\ge g_0/4\ge\mathfrak m_q/4>0,
\qquad g_0=\phi(0)-5/16>1/16.
\]

Here (\mathfrak m_q) is WEAK's displayed margin evaluated with actual incoming normalized radial data and the valid selected-mass cap (n_b=2h). It is at least (3g_0/4). The endpoint is **(H=h)**; no equality between actual weak mass, response, and leading logistic mass is claimed.

| Requested step | Status | Closed result / remaining inequality |
|---|---|---|
| 1. Exact boundary field | Closed | `exact`, `R21`, `R11`, `leading`. P's boundary coefficient is reproduced, including (-(1-M)v/2) in (2u'). No mismatch. |
| 2. Pointwise boundary budget | Closed | `budget`, `energycharge`, `remainder`, `finalremainder`. No integrated budget is used as a pointwise margin. |
| 3. Strong-mass term | Closed | `mass`, `massproduct`: (\sup|1-M|L\le Cq^{101/640}\le\mathfrak m_q/16). |
| 4. Weak-sender term | Closed at fixed level | `weakvalue`: (0\le\mathcal W_{G_+}^q(0)\le C_W(H+K_Y\sqrt H)). Covers selected and non-selected primary senders together. |
| 5. Incoming sign | Closed | `incomingpre`, `nocross`: regularized positive entry seed, clock alignment (O(q)), fixed-time initial protection, then the inward boundary inequality. Excluded mass is exactly zero. |
| 6. Return theorem | Closed | `main`, `return`; no additional hypothesis is introduced. |

There is no unmatched inequality within S4b and no failed-route obstruction. The exact inequalities still needed for the later stages are listed under the S4c handoff below; they are not hypotheses of this theorem.

## Why the two principal difficulties are paid

### Exact signed leading term, not an unsigned residual norm

At (\theta=\pi/2), the receiver event is (A=\{X_2>0\}). Integration by parts is in (X_1), so it does not differentiate this gate. For each sender, write

\[
A_1=\mathbb E_{P_1}[(U\cdot X)_+1_A],\quad
p_i=\mathbb P_{P_i}(U\cdot X>0,A).
\]

Then the exact (P_1) moment is (A_1+q^2U_1p_1), and the exact (P_2) moment is (q^2U_1p_2). In particular the latter is not charged by a generic (O(q)) estimate before division by (q). The target moments give (q\phi(0)/2) in (R_{21}) and ((1+q^2)/4+q^2\Phi(\rho/q)/2) in (R_{11}). Both mixture coefficients are retained.

Core donors give (\mathcal W_K^q(0)=Y_K/2+O(q^2M)) after the exponentially small donor tail. The exact leading field is therefore

\[
2u'=\phi(0)-Y_K/2-\mathcal W_{G_+}^q(0)-(1-M)v/2+\mathcal R.
\]

This agrees with P `pa:pop-u`, where (M=\mu_K) is the physical, unnormalized core mass. It is not the residual constant (M_{\rm res}), and CFA's truncated mass is not substituted for it.

The exact finite-(q) weak-output functional is retained for all (G_+). Its identification with P's (int F(0,\widetilde u)\,d\mu_w) is made only for compact sender charts and only to check the coefficient. The proof does not extend a compact-chart approximation to uncharted primary senders.

### Pointwise energy controls the original weak feedback

The new one-sided estimate is

\[
0\le\mathcal W_{G_+}^q(0)
\le C E_{G_+}+C\frac{\sqrt{J_{G_+}}}{q}\sqrt{E_{G_+}}
\le C_W(H+K_Y\sqrt H).
\]

The sign uses only the proved (W_2>0) on (G_+). The value/coefficient bound uses Cauchy–Schwarz, RB's primary-to-clock comparison and the pointwise transverse budget. It requires neither (u\ge0) for senders nor WEAK's leading contraction. It applies separately to (S) and (G_+\setminus S), with their **sum** bounded by the displayed allowance. It is stronger for this boundary task than charging weak mass times the supremum of weak coordinates.

Thus the fixed level can be chosen to satisfy (C_W(h+K_Y\sqrt h)\le g_0/8). The potentially large fixed (K_Y) merely makes (h) smaller; it does not change an earlier guard or create a (q)-dependent endpoint. The proposed vanishing-level threshold (a'>4p_b/(3+c_b)) is confirmed for the crude clock size product, but that fallback is not used.

## Pointwise budget ledger

All entries below hold on the certified RB interval; the late rates use ([t_s,t_e]). No use is made of (\int r), (\int\mu_B/q), or (\int\varepsilon_F) to infer a pointwise bound.

| Contribution | Exact form or bound | Type after scaling | Proved source and scope |
|---|---|---|---|
| Target and core boundary coefficient | (\phi(0)-Y_K/2) | Signed leading value | New exact Gaussian calculation; RB core chart and SI `coremoments` give (Y_K\le5/8). |
| Core donor (P_1) gate | (Ce^{-c/q^2}/q) | Additive; absorbed by (Cq^2) | Core projection has mean at least (1/2); receiver indicator has magnitude at most one. |
| Core trigonometry and (P_2) Stein term | (C_Rq^2M) | Additive in (2R_{21}/q) | Exact `R21`; compact core geometry, (M\le2). |
| Core first-moment replacement | Zero when actual (Y_K) is kept; otherwise (D_K=O(q^{1/20})) | Additive | RB retention and SI `Dcore`. The proof keeps actual (Y_K). |
| Unit-core comparator replacement | (C|1-M|), if performed | Additive | New pointwise `massrate`; not needed in the main calculation. |
| Physical mass defect | (-(1-M)v/2) in (2u') | Linear in (v) | New `masseq`, from CFR `radialbound` and RB pointwise states. Product (O(q^{101/640})). |
| Primary weak output | (C_W(H+K_Y\sqrt H)) | Nonnegative feedback, subtracted | New `weakvalue`; RB `primaryclock`, LCRC `signgood`, (J_G\le q^2K_Y^2). |
| Primary (P_2) / Stein correction | (Cq\sqrt{E_{G_+}J_{G_+}}=O(q^2)) | Additive | Exact Gaussian identity, not a full-gate assumption. |
| Secondary | (C(E_\Sigma+K_Y\sqrt{E_\Sigma})) | Additive | RB's proved (E_\Sigma\le C_\Sigma(q^5+q^{\Gamma_\nu}H)), (J_\Sigma\le q^2K_Y^2). |
| Entire outside population | (C\mu_B/q) | Additive | RB `massconclusions`: (\sup\mu_B/q=o(q^{1/10})). Both strips/transit labels are included; no new chart or sign assumption. |
| First-row remainder | (C(q^2+\mu_B)) | Multiplies (v) | Exact `R11` and (J_G+q\sqrt{E_GJ_G}=O(q^2)). |
| Receiver cosine/sine expansion | (Cq^2(1+L^2)+C|1-M|Lq^2L^2) | Additive | Applied only after (qL\to0) is established, or at an actual early boundary with (|v|\le C_\Delta). |

The late chart has (L=C_L(1+q^{-603/640})). The explicit controlling powers are

\[
qL=O(q^{37/640}),\quad q^2L^2=O(q^{37/320}),\quad
\mu_BL=O(q^{101/640}),\quad |1-M|L=O(q^{101/640}).
\]

Since (\Gamma_\nu/2>3/20), the retained-actual-moment boundary remainder is (O_{\rm fixed}(q^{1/10})). If one elects to replace the actual core moment by a reference moment, the separate (O(q^{1/20})) error must be added; the stronger rate is not claimed for that altered representation.

## Pointwise mass rate and incoming sign

CFR `radialbound` is used in its actual state form, not by importing its originally open c-form theorem. Its hypotheses are residual bounds, charted core donors with a fixed mass cap, and a charted receiver. RB proves each of these throughout the passage, including for every core receiver. Averaging its radial identity gives

\[
(\log M)'=1-M+\eta(t),\qquad
|\eta(t)|\le C(q^2+\mu_B)\le C_\eta q^{11/10}.
\]

With (1/3\le M\le2) and (M(t_0)<1), variation of constants gives

\[
|1-M(t)|\le C_me^{-(t-t_0)/3}+6C_\eta q^{11/10},\quad
(M-1)_+\le6C_\eta q^{11/10}.
\]

This quantitative conclusion is not inferred from S2CP's integrated (d_q=o(1)). The proof of CFR's state identity also gives (e_1=(1-\kappa_1)X_1-g_1) on (P_1), with (\|g_1\|_{P_1}\le C(q^2+\mu_B)). Positivity of the selected (X_1^2) moment and the (P_2) cross residual then imply (R_{11}(\theta)\ge-Cq^{11/10}) for every receiver gate.

For the clock, BULK's already proved input gate margin gives (R_{22}\ge507/6400). Consequently the trace is positive uniformly, even before input return is proved. The exact alignment equation and RB's (O(q)) entry alignment give (|\theta-\psi|\le C_\Delta q) on the entire clock passage. At a possible weak-input boundary this implies (|v|\le C_\Delta), regardless of the large size estimate elsewhere.

The regularized entry dichotomy, transferred by Q2EC, gives

\[
q\cot\theta(t_0,b)\asymp
\left[q^\gamma\frac{s_0+q}{c_0+q}\right]^{(1-\lambda)/\lambda},\qquad
\cos\theta(t_0,b)\ge c_{\rm in}q^{1-2079/13520}.
\]

At (b=\pi), (s_0+q=q). Removing this term would invalidate the uniform incoming-seed argument. Q2EC's matched sector and fixed-time-shift check justify applying the target regularization at (t_0=10\ell-\log A_q+o(1)); no relative early angle error is substituted.

On an initial fixed interval of length (T_*), the exact matrix equations imply ((\cos\theta)'\ge-C_1\cos\theta-C_2q) while (\cos\theta\ge0). The positive regularized seed dominates the (O(q)) loss. Choose (T_*) large enough that the remaining mass deficit times the boundary bound (C_\Delta) is small. Thereafter any first input escape has positive inward derivative by the exact boundary budget. This covers the whole interval from (t_0), so there is no implicit assumption about the sign at the later starting level.

## Hypothesis matching (ledger 21)

| Cited result / calculation | Every hypothesis used here | Where supplied |
|---|---|---|
| RB `completed` and S4 handoff | Original balanced isotropic initialization; (\kappa=10); stated closed (\rho) box; WPT fixed constant order; sufficiently small (q). | Current model. RB supplies (0<c\le c_b), finite (t_b<t_0+20\ell), all residual/core/secondary/outside conclusions. No extra sign premise is added. |
| RB `primaryclock` | Fixed primary and clock subsets; positive entry amplitudes; original Q2EC matched sectors and regularization; RCET's range, residual, duration, learning and entry-ratio hypotheses. | Already verified in RB. Its fixed constant supplies (E_{G_+}\le C_EH); this is a conclusion, not a proposed guard. |
| SI `coremoments` | RB core radius (O(q^{1/20})), reference allowance (e\le3e_*/4\le3/16), positive core coordinates, core mass bounded away from zero and at most (1+o(1)), resident bound on the model box. | SI's closed conclusion gives the actual (Y_K\le5/8), not only its normalized version. |
| CFR `radialbound` and its proof | Diagonal loss bound, cross residual (M_{\rm res}q), fixed donor chart and mass cap, receiver chart with fixed (L_c\ge R). | RB gives all throughout the passage for core labels. (J_G,E_G,\mu_B) in its right side have pointwise RB bounds. No unproved remainder or strip contract from the original CFR theorem is reused. |
| S2CP `Bs` equation | Core geometry, radial state identity, explicit transverse/energy and outside bounds on a stopped passage. | RB has discharged the stopped inputs. Only the equation's identification is cited; the new pointwise rate is derived explicitly from CFR. |
| LCRC signgood / RCET transport | Fixed positive-amplitude cohort; (0\le c\le c_b<1); logarithmic duration; bounded diagonal and (O(q)) cross residuals; (\int r\le B); original (z>0, |a|/z\le1/4), ratio entry (\le C_0); admissibly small fixed (C_0), then (q). | RB handoff and its Q2EC entry verification. Gives (U_2,W_2>0), (E_S\le10H_S/9), and fixed-distortion primary transport. It does not supply the new first-coordinate sign. |
| BULK Theorem 4.1 and `R22tail` | Same response/duration/residual/learning bounds; fixed cohort; finite positive (H(t_0)); original positive (z), (|a|/z\le1/4); clock entry ratio (\le C_{\rm clk}q^{1/8}), with (0<1/8<1). Gate-tail calculation additionally uses positive input second component. | RB and Q2EC. Positive (U_2) is BULK's conclusion, before (U_1)'s sign is known. No weak-input-return hypothesis is present. Uniform comparison and continuous label dependence include endpoints. |
| RB `entryalignment` | Original S1 flow, moving-overlap state and all-receiver Q2EC matrix bounds before (t_0). | It is a proved all-label lemma in RB, including (\pi). Its conclusion is used directly; no arbitrary-receiver extension of a chart lemma is made here. |
| RCET `regularized` | Target-only aligned Q2 labels with endpoint factors (s_0+q,c_0+q), after crossing and before arrival at a fixed large strong chart, at (10\ell). | Q2EC's primary proof keeps clock labels in the controlled pre-chart sector, proves all crossings precede (t_0), and gives the fixed-time-shift extension below. |
| Q2EC `transport`, `match`, `targetcontracts` | Original initialized S1 passage; fixed large matching band; positive matched coordinates after crossing; receiver angle above (qL), target above (16qL); fixed primary threshold and small (q). | Its proved primary-sector bootstrap applies to the whole clock. Its explicit time-domain check covers (t_0-10\ell=O(1)) and preserves the regularizers; (A_q) is bounded above/below by MOMC. |
| RB exact clock and integral of response | (t_0\le s\le t\le t_b), fixed clock cohort and the completed passage. | The first hits are within that interval by (H_0\asymp A_q^{-\lambda}q^k), (H(t_b)\ge c_Hc_b), continuity, and the fixed level choices. Only the clock timing uses the response integral. |
| P `pa:leading` | Leading measures and coordinates as defined there. | Used for algebraic coefficient comparison only. No leading equation is imposed on the original population. |
| WEAK margin formula | (n_b<1), bounded strong moment (Y\le Y_{\max}), finite incoming positive first moment. | We set (n_b=2h<1/2), use (Y_{\max}=5/8), and bound the actual incoming moment by Cauchy–Schwarz. No WEAK forcing, concentration, or contraction theorem is invoked. |

## Constants, levels and accuracy

Retain WPT/RB's entire order first. The new order is: the model gap and local constants; the fixed constants inherited from the pointwise states and the new scalar comparisons; start exponent (a_s=1/8); a fixed (h) satisfying the following inequalities; then (q):

\[
0<h<\min\{1/4,c_b/2,c_Hc_b/2\},\qquad
C_W(h+K_Y\sqrt h)\le g_0/8,
\]

\[
2\phi(0)(1+2/\lambda_{\min})h+
2\sqrt2K_Y\sqrt{2h}\le g_0/4,
\quad\lambda_{\min}=169/400.
\]

The scalar waiting time (T_*) is fixed through (C_mC_\Delta e^{-T_*/3}/2\le g_0/8). It is not a new stopping guard.

| Constant | Dependency / use |
|---|---|
| (R=79/51,M_K=2,c_b,B,K_Y,M_{\rm res},C_0,C_\Sigma) | Existing WPT/RB constants, unchanged. |
| (g_0,\lambda_{\min},b_c=507/6400,\sigma_*=2079/13520) | Model-only analytic constants. |
| (C_E) | Fixed RB primary-to-clock comparison, including its fixed entry and RCET distortion constants. |
| (C_W) | Gaussian Cauchy–Schwarz constants and (C_E); (K_Y) remains explicit in its bound. |
| (C_\eta,C_m) | Existing chart, residual, energy and outside constants. Used in (q^{11/10}) and exponential relaxation. |
| (C_\Delta) | (C_{\rm al,0}+4C_\times/b_c+1); (C_{\rm al,0}) is S1-only and (C_\times) depends on the fixed cross residual bound. Multiplies (q). |
| (c_{\rm in}) | Fixed Q2EC matching and RCET regularized-dichotomy constants, bounded (A_q) factors. |
| (T_*) | (g_0,C_m,C_\Delta), independent of (q). |
| (C_L) | BULK/SI size constant and fixed seed/clock phase bounds. It may be chosen from the start level; no new earlier guard is selected. |
| (h,n_b=2h) | Depend on the already fixed (K_Y,C_W,c_H,c_b) and model margin. Fixed independently of (q). |
| (\mathfrak m_q) | Actual incoming data, but uniformly (3g_0/4\le\mathfrak m_q\le g_0). |

The clock-level times are

\[
t_s-t_0=\frac{(k-1/8)\ell+\lambda\log A_q+O_{\rm fixed}(1)}Q,
\quad
t_e-t_0=\frac{k\ell+\lambda\log A_q+\log h+O_{\rm fixed}(1)}Q.
\]

The denominator is (Q), not (Q(1-c_b)). The fixed-factor seed and bounded response integral give an (O(1)) phase here, not an (o(1)) phase. RB's exact clock still retains its separate (O(q^{1/8}+q^2\ell)) subinterval defect. No phase matching through (t_b) is performed.

## S4c handoff and work not claimed

| Supplied output | Accuracy and consumer limitation |
|---|---|
| Fixed selected cohort (S=\mathcal C_q) | Entire closed cohort; no missing-mass charge. No time-dependent sign mask. |
| Original input return | (u\ge0) on ([t_s,t_e]), with strict uniform inward boundary derivative. This discharges SI `missingreturn` on this interval. |
| Reached weak chart | (L(q)=C_L(1+q^{-603/640})), (qL\to0). Not a bounded scaled chart. |
| Physical strong-mass fit | Pointwise (|1-M|L=O(q^{101/640})), with its source and rate. A later integrated coefficient estimate must still be checked in the full weak field. |
| Exact boundary field | Exact (P_1/P_2) and cohort identities, correct mass-linear term; actual-moment remainder (O(q^{1/10})) at (u=0). Does not give the field or its derivative for general (u). |
| Weak-output boundary charge | (C_W(H+K_Y\sqrt H)), including non-selected primary senders; sufficient for fixed small (h). Not WEAK's contraction-based (K_w) theorem. |
| Incoming margin | Actual (U_0^+\sqrt{N_0}\le2\sqrt2K_Y), valid mass cap (N_S\le n_b=2h). Does not prove the later (\sqrt{N_0}W_p(t_s)\to0) condition. |
| End and timing | First (H=h<t_b); bounded phase timing with explicit (A_q) dependence. No assertion (N_S(t_e)=h), (c(t_e)=h), or logistic phase. |

Still to prove in the later stages: the full weak-chart perturbed field and TAILREP's specified additive/integrated error inequalities; their derivative/coefficient control; logistic matching and (\int(N-c)); the required (W_p) initial smallness; selection. This increment makes no continuation beyond (t_b), no S5 retention claim, and no use of those future conclusions.

## Source provenance and integrity

README and roadmap were re-read from the read-only GitHub connector. The roadmap fetched for this request is v1.19. Source identifiers below are the file SHAs returned by the connector, not a claim that a new commit was made. Stable prefixes/suffixes in the TeX identify the exact mathematical statements.

| Source | Repository path | Fetched file SHA |
|---|---|---|
| README | `README.md` | `16b4bc0726ae3476c3c0abfd7d2d0bafbde2d628` |
| Roadmap v1.19 | `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | `08374b9ce5f203b695d28004c122fd40724b98bf` |
| P | `01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex` | `cb458c933aa043cf0188fd11c46bf4246ffc91d8` |
| RB | `03_passage_AN03/AN03_response_barrier_v1.tex` | `5312b5093f3ed4f74063347df31ae5a29155255f` |
| SI | `03_passage_AN03/AN03_selection_interface_v1.tex` | `9c984392caa650505b5c961796529fb4acc751ea` |
| S2CP | `03_passage_AN03/AN03_S2_closure_package_v1.tex` | `baeb8a7eb1e36ce86319782511b665944be1afda` |
| CFR | `03_passage_AN03/AN03_c_form_field_reduction_v1.tex` | `d6e92da35a9d510201946fa6851c2c55740c1ff0` |
| LCRC | `03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex` | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` |
| BULK | `03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` |
| RCET | `03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex` | `49e352002b4c699338ac99a4d55d51c60760ea86` |
| Q2EC | `02_entry_AN02/AN02_Q2_entry_contracts_v1.tex` | `b149537025e130801fc55b9e49c365c158eee17b` |
| CFA (representation cross-check) | `03_passage_AN03/AN03_c_form_assembly_v1.tex` | `341908c228092e9a818d98de3ec26591a1050364` |
| MOMC (entry cross-check) | `02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex` | `539427063c4a08551ce4cb8efe41dab61cde609c` |

The new prefix was checked against the available prior local TeX/Markdown files and a read-only repository code search; no collision was found. This is a standalone increment. No prior source, checkpoint, foundation, or repository content was edited. Verification consists of source inspection, analytic inequalities, TeX compilation, label/reference checks, and prior-file integrity checks. There were no experiments, sampled trajectories, interval calculations, grid signs, or numerical premises. The delivery ZIP contains only the raw `.tex` and `_review.md` pair, not a PDF.
