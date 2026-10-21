# AN02 secondary entry profile v1 — review note

**Result: S1 step 7 closes at \(t_0=t_h\), with fixed two-sided constants and no new retained hypothesis.** The theorem concerns the exact original initialized flow, uniformly for \(\rho\in[13/20,7/10]\), \(S_0=q^{10}\), and sufficiently small \(q\). All new labels use **an02sepv1:**.

Companion: **AN02_secondary_entry_profile_v1.tex**. The source ZIP contains this .tex and this review note, not a PDF.

## Result and normalization

Keep Q2EC's fixed \(K=K(C_0)\), and use the entire fixed ancestry group
\[
\Sigma=\{\beta\in[\pi/2,\pi]:c_0<Kq^\gamma\},\qquad \mathcal D=\emptyset.
\]
The reference is MOMC's actual characteristic launched at \(\beta_c=qa_q\), never reset. Displacement is the sum of absolute input and output scaled differences from that reference. The measure is **raw radial mass**, \(m(t_h,\beta)\,d\beta/(2\pi)\), pushed forward by this displacement on the fixed group. Q2E's target strong-mass normalization is not silently imported.

Write
\[
h_A=A_q^d q^{10d-2s},\quad D_h=\sqrt{2(1-M_0)},\quad
B_q=A_q^{-1}D_h^{-2},\quad p_2=\frac{1-3\lambda/2}{d}.
\]

| Requested part | Supplied result |
|---|---|
| (a) Cap and mass | \(\xi\le Z_\Sigma=Z+2R\), \(R=79/51\); raw mass at most \(4e^7C_Q A_q^{-1}q^3\), directly from Q2EC/Q2EP. |
| (b) Displacement | Each signed component relative to the actual reference is positive and comparable to \(h_A[(c_0+q)/(q(s_0+q))]^{2d/\lambda}\). |
| (b) Weight | \(m(t_h,\beta)\asymp B_q q^{2/\lambda}(c_0+q)^{2-2/\lambda}(s_0+q)^{2/\lambda}\). More precisely \(m/\widehat m=D_h^{-2}e^{O(\mathcal R_q)}\) at the same time \(t_h\). |
| (c) Tail | \(\eta\{\xi>w\}\le C B_q q^3\min\{1,(h_A/w)^{p_2}\}\) for all \(w>0\), with two-sided comparison on \(C_1h_A\le w\le z_0\). Total mass is \(\asymp B_q q^3\). |
| (d) Handoff | Supplies LCRC's entry profile for this whole fixed \(\Sigma\). Later distance and capped gain remain S2 inputs. |

Here
\[
\mathcal R_q=q^{1/1000}+q^{4/51}+q^{v_m}+q\ell^2+q^2\ell^2=o(1),
\qquad v_m=10-2/\omega-3/2\ge67/102.
\]
The displacement comparison retains bounded nonlinear distortion. It is not an asymptotically exact universal angular multiplier. After the label's matched chart-entry time \(t_a\), the explicit linear factor relative to target contraction is
\[
\exp\left(\frac12\int_{t_a}^{t_h}M\right)
\in[1,\sqrt2\,e^{O(q^2\ell^2)}].
\]
The additional nonlinear factor is bounded above and below, as requested.

All surviving \(A_q\) powers are explicit:

- Clock: \(t_h=10\ell-\log A_q+O(q^2\ell^2+q^{u_m})\), \(u_m=10-2/\omega-1/2\).
- Displacement scale: \(A_q^d\).
- Raw weight and total mass: \(A_q^{-1}D_h^{-2}\).
- Power-tail coefficient: \(D_h^{-2}A_q^{dp_2-1}=D_h^{-2}A_q^{-3\lambda/2}\).
- Last-label scale: \(h_A(Kq^{\gamma-1})^{2d/\lambda}=A_q^dK^{2d/\lambda}\).

These occur inside fixed two-sided profile inequalities; an exact numerical tail prefactor is not claimed. The lower tail stops below the last-label cutoff, as in Q2E.

## Central proof audit

1. **Early tangent domain.** OWPT states its tangent lemma on the initial right half-circle. Its Jacobian proof uses global receiver-angle bounds, P's global early comparison, and a nonnegative target transverse quadratic form. The new lemma checks these on the entire arc \([qa_q,\pi]\). The normalized target tangent has a row-stochastic leading propagator, with error integral \(O(q^{v_m})\). Integrating the positive derivative comparison from the reference label gives relative displacement control at \(t_m\), even for separations smaller than the reference offset. No absolute error is divided by a tiny displacement.

2. **Target profile domain.** Q2E prints its profile at \(10\ell\) for charted labels. Q2EC gives a fixed target cap \(Z_T(K)\) at \(t_h\). The new proof enlarges PROFILE's fixed chart to contain this cap and checks \(f_q=f_0+O_{C^2}(q^2)\), \(b_q\ge\omega/2\), and \(\int\widehat h\le2\widehat h(t_a)/\omega\). Arrival and radial formulas change only by fixed constants. Substitution of \(t_h\) gives \(A_q^d\) and \(A_q^{-1}\). No target evolution after \(t_h\) is needed.

3. **No late weak-axis layer for this group.** For \(\Sigma\), Q2E gives \(T_\times\le(10-2/\omega)\ell+O_K(1)\). Target travel from the axis to \(\pi/4\) takes \(\omega^{-1}\ell+O(1)\). The margin before \(t_m\) is at least \((137/154)\ell-O_K(1)\). Q2EC's off-chart transport therefore starts at \(t_m\) with a fixed first-coordinate margin. Its second-coordinate relative match is used only when the target angle exceeds \(2qL\). No new crossing premise is introduced.

4. **Homogeneous same-field error.** MOMC's finite-noise \(C^1\) reduction, donor replacement, and subtraction at the actual reference give
   \[
   V'=f^M((a,a)+V)-f^M(a,a)+E(t,V)V,\qquad
   \|E(t,V)\|\le C_B(q^2+\mu/q+e+\overline D).
   \]
   The integral is \(O(C_B\mathcal E_q)=o(1)\), where
   \[
   \mathcal E_q=q^{v_m}+q^{s+d/2}+q^2(1+\ell)+q\ell^2.
   \]
   The threshold derivative \(F_t(t,r)=(r-t)_+\phi(t)\) is Lipschitz in the donor threshold, including equality. The coherent field is \(C^{1,1}\) on each fixed chart. These justify the derivative comparison and shifting both coherent arguments by the actual reference offset. There is no additive error floor.

5. **Finite-noise cooperativity is not assumed.** Only the coherent field has proved nonnegative off-diagonal derivatives. Its positive-cone maximum contracts at rate at least \(1/200\); the exact perturbation leaves \(1/400\). The coherent secant matrix is Metzler. After removing \(r_0=-d+M/2\), its row sums are \(O(H)\), with \(\int H\le400H_*\). Its positive propagator bounds normalized components above and below by fixed factors. Duhamel's formula makes the exact non-Metzler error \(o(1)\) relative to the initial displacement. This closes positivity and the fixed chart by first exit. Large but finite distortion constants are allowed.

6. **Both entry cases.** If the target angle is at most \(2qL\) at \(t_m\), the relative early lemma provides the chart data, including tiny displacements. Otherwise Q2EC is used until the first original or target \(qL\) hit. Both input angles are then in \([qL,4qL]\), and Q2EC's angle-difference bound makes both displacements positive and comparable to \(L\). The same homogeneous chart lemma covers the remainder.

7. **Radial factor.** Before chart entry Q2EC controls \(U_1/\widehat U_1\). At entry both cosine factors are \(1+O_B(q^2)\), so balance converts this to \(e^{-\int M}\). After entry MOMC gives \((\log m)'=1-M+O_B(q^2)+O(\mu)\), while the target rate is \(1+O_B(q^2)\). Combining the pieces yields \(D_h^{-2}e^{O(\mathcal R_q)}\). This is an original-flow comparison, not normalization to a probability.

8. **Tail without final-angle ordering.** In \(y=1+c_0/q\),
   \[
   \xi\asymp h_Ay^b,\qquad d\eta\asymp B_q q^3y^{-a_2}dy,
   \qquad 1\le y<1+Kq^{\gamma-1}.
   \]
   These pointwise sandwiches suffice; monotonicity of the final displacement is not assumed. Upper tails follow by integrating to infinity; the lower tail uses a fixed-ratio interval contained below the cutoff. Endpoint regularizations are retained until \(s_0\asymp1\) is justified on \(\Sigma\).

## Fixed constants and order of choice

The table lists the order-one constants introduced or inherited. Generic comparison constants are grouped by their exact source estimate. Their finiteness and positivity are analytic, not numerical.

| Constant | Origin and dependence |
|---|---|
| \(C_0,K(C_0),Z(C_0)\) | Fixed Q2EC choices, not reselected here. |
| \(R=79/51,\ a_{\max}=28/51,\ \omega_{\min}=51/200\) | MOMC's donor/reference radius and analytic box bounds. |
| \(a,\alpha,d,s,b,a_2,p_2\) and compact extrema | Analytic functions of the ratio box; in particular \(b_->0\), \(a_2-1>0\), \(0<p_2<1\). |
| \(c_A,C_A,A_q\) | MOMC's actual normalization and bounds. |
| \(D_h,B_q\) | Explicit factors above, bounded above and below. |
| \(C_Q,C_{\rm ent}=4e^7C_Q\) | Q2EP's specified target energy constant and original half-mass bound; independent of the Q2 subdivision. |
| \(Z_T(K),L_T\) | Q2EC's target cap and a fixed larger target chart. |
| Target profile, arrival, radial and gate constants | Q2E/PROFILE, enlarged for the fixed chart and bounded shift \(\lvert\log A_q\rvert\). |
| Early Jacobian/tangent constants | P/PROFILE/OWPT's global bounds; independent of label separation. |
| \(C_\Delta\), Q2EC transport constants and original threshold | Proved full-gate coordinate and difference estimates, fixed before the auxiliary \(L\) is enlarged. |
| \(L\) | At least Q2EC's threshold, \(Z_T(K)+1\), and \(4(C_\Delta+R+a_{\max}+2)\). Enlargement does not change \(K\) or \(\Sigma\). |
| \(H_*=8L,\ c_*=1/8,\ B=R+8L+2\) | Matched-entry size, component ratio, and auxiliary receiver radius. This \(B\) is **not** LCRC's integrated residual guard. |
| \(C_B,\ 160\) | Compact-chart Gaussian, \(C^1\), and Lipschitz constants; MOMC's outside derivative constant. \(C_B\) can be enlarged to dominate all chart estimates. |
| \(1/200,\ 1/400,\ 400\) | Leading contraction, weakened original contraction, and its integral bound. |
| \(L_*=400C_BH_*,\ c_*'=c_*e^{-L_*}/2,\ C_*'=e^{L_*+1}\) | Explicit fixed chart-distortion constants. They need not be small; \(q\) is chosen afterward. |
| \(Z_\Sigma=Z+2R,\ R_\Sigma=R\) | Final displacement cap and entry reference radius. The auxiliary proof chart does not replace the strong donor radius. |
| \(c_h,C_h,c_w,C_w\) | Positive shape/density sandwich constants obtained from the preceding matched comparisons and the initial-label Jacobian. |
| \(A_*=\max\{2,(2/c_h)^{1/b_-}\},\ C_1=2,\ z_0\) | Lower-tail constants. \(z_0\) is the displayed positive compact minimum of \(A^d(K/(4A_*))^b/2\), capped by one. No numerical minimization. \(A_*\) is distinct from \(A_q\). |
| Final mass/tail constants | Combinations of the density constants, \(1/(a_2-1)\), compact bounds for \(b\), and the positive fixed-ratio integration factor. |

All choices use the model, ratio box, proved source constants, and prescribed \(C_0\) through \(K,Z\). **No value of LCRC's \(B,E_g,K_Y,M\), or any residual bound, is used.** The small-\(q\) threshold may depend on the fixed source and chart constants. The actual reference radius remains \(79/51\).

## Contract accounting

There are **no new retained inputs** to this entry theorem. Its initialization and parameter restrictions are those of MOMC/Q2EC. Every dynamical budget used is an already-proved consequence of those sources.

Supplied:

- LCRC Section 1, **an03lcrcv1:profile**: fixed cohort, joint displacement cap, raw \(O(q^3)\) mass, and secondary upper tail. The interior lower tail is additional.
- The entry hypotheses of BULK Lemma 5.1, so its moment estimates apply directly.
- The entry reference bound \(R_\Sigma=79/51\), for the actual same-field characteristic.
- The proposed whole-\(\Sigma\) partition with \(\mathcal D=\emptyset\), making the separate \(\mathcal D\) retention budget vacuous.

Not supplied:

- **an03lcrcv1:distance** after \(t_0\), with its response clock and first-exit convention.
- **an03lcrcv1:gain** for the same fixed cohort at every intermediate endpoint, including any post-exit regime required by BULK.
- Later boundedness of the reference, core retention, weak-passage \(B_s\), or other S2/S3 trajectory budgets.
- Unconditional applicability of BULK Proposition 5.2 or its secondary corollary. The later distance/gain and clock inputs remain open.

The auxiliary chart lemma is used only on \([t_m,t_h]\); it is not a proof of the later LCRC distance envelope or a capped-gain law. Work stops at \(t_h\).

## Repository provenance and verification

**Roadmap v1.7 and Q2EC were re-fetched and read from the repository after the user confirmed the push.** The earlier availability discrepancy is resolved. This increment does not substitute the stale v1.6 roadmap or an unpublished local Q2EC for the updated repository sources.

Repository: **TodManlaibaatar/OOD-reversals-theory**, default branch **main**. Access was read-only. The following Git blob hashes identify the contents used.

| Source | Repository path | Git blob SHA |
|---|---|---|
| README | README.md | f8bff1b8d3716cd5dd1e8d739a8b3a522eedc467 |
| Roadmap v1.7 | 00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md | 52d013b703f4e8a011a9b57e95186f7ed3d99508 |
| Q2EC | 02_entry_AN02/AN02_Q2_entry_contracts_v1.tex | b149537025e130801fc55b9e49c365c158eee17b |
| Q2E | 02_entry_AN02/AN02_Q2_boundary_layers_and_cohort_energy_v1.tex | cce55e1029cfd1ca8afb98eb649389b420d3992b |
| Q2EP | 02_entry_AN02/AN02_Q2_entry_through_strong_passage_v1.tex | 042b3c93cf8402d10487f9e56f6f5b1d869c424a |
| MOMC | 02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex | 539427063c4a08551ce4cb8efe41dab61cde609c |
| OWPT | 02_entry_AN02/AN02_overlap_window_profile_transfer_v1.tex | 8fac13f9d36255d3e2e23cc9b2196719ec602907 |
| PROFILE | 02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex | 3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a |
| BULK | 03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex | 66d3e66aaf99567440a9ebe84fd38c40b047ac83 |
| LCRC | 03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex | defc7033fb8c9f49cbfb8b9b278ca71aa34925ac |

P's global early comparison is used through OWPT's displayed receiver-Jacobian proof and Q2EC's reviewed input statement. No numerical premise, experiment, grid sign check, interval arithmetic, or saved trajectory is used. Compilation checks typesetting only. Prior files are preserved; there is no consolidation or GitHub mutation.

Completed artifact checks: the final TeX compiled successfully with the desktop LaTeX compiler; all 26 new labels have the requested prefix, are unique, and all internal references resolve. SHA-256 checks confirm that all 32 pre-existing workspace files are unchanged. The freshly fetched Q2EC content matches the previously reviewed local copy. The ZIP is checked to contain exactly the two source files, with bytes identical to the delivered pair.

