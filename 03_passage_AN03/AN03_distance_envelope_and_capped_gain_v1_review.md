# AN03_distance_envelope_and_capped_gain_v1 — review note

**Status: partial original-flow implication; stopped at the off-chart distance comparison.** This is the requested S2a increment, with label prefix `an03decgv1:`. It does not claim that the full S2a theorem or either tail-energy conclusion is proved. The source ZIP contains this note and the standalone TeX source, not a PDF.

## Results proved

1. **Fixed-chart distance envelope** (Proposition 2.1, `local` / `localdistance`). For any receiver and actual same-field reference remaining in the prescribed square,
   \[
   D(t)\le p_*^{-1}e^{C_TF_b}D(s)e^{\beta(I(t)-I(s))/2},
   \qquad p_*=\Phi(-7L_c/10).
   \]
   The change of input coordinate \(u=\int_0^x\Phi(\rho v)^{-1}\,dv\) removes the common \(V\) forcing from the receiver Jacobian. Its leading transformed Jacobian is Metzler, has nonpositive diagonals, and has column sums at most \(\lambda(1-c)/2\). The finite-noise remainder is charged through its supplied derivative norm; finite-noise cooperativity is not assumed. No integral bound on \(e+r+f_*\) is needed for this lemma.

2. **All-receiver signed radial estimate** (Lemma 3.1 and Proposition 3.2, `projected` / `radial`). Under the stopped residual guards,
   \[
   (\log(m_\alpha/m_c))'
   \le I'\min\{1,q^2D_\alpha(t)^2\}
       +4r+C(1+M_{\rm res})q.
   \]
   The last two terms integrate to \(4B+o(1)\), uniformly over labels and intermediate endpoints. The lower-side weak gate is handled by its projected Gaussian margin and the factor \(|\sin\theta|\) in the radial expression. It is not declared identically closed. The same-field reference mass increases by at most \(e^{2B+o(1)}\).

3. **Precise remaining premise for capped gain** (Corollary 3.3, `conditionalgain`). If the distance envelope holds up to fixed physical exit, the all-endpoint raw-mass estimate follows:
   \[
   \frac{m_\alpha(t)}{m_\alpha(t_0)}
   \le e^{6B+1/\beta+o(1)}
      \max\{1,A_0q^2\xi_\alpha^2e^{\beta I(t)}\}^{1/\beta},
   \quad
   A_0=C_D^2\max\{1,\delta_0^{-2}\}.
   \]
   Here \(1/\beta=1+q^2/\lambda\le1+1/100\) for sufficiently small \(q\). The proof invokes TAILREP's completed gain-integration lemma rather than reproving it. The missing distance premise is displayed and explicitly **not** claimed as a consequence of the supplied fixed-chart hypothesis.

## Stop rule and exact unpaid inequality

For a label leaving the fixed scaled square at \(\tau_L\), the missing comparison is
\[
\sup_{\tau_L\le t\le\tau_\delta\wedge t_*}
\frac{D_\alpha(t)}{D_\alpha(\tau_L)}
 e^{-\beta[I(t)-I(\tau_L)]/2}
\le C_{\rm ext}e^{CB}.
\]
Here \(\tau_\delta\) is the first \(qD_\alpha=\delta_0\), and \(C_{\rm ext}\) must have the prescribed guard-independent dependence. An initially exterior label needs the corresponding estimate from \(t_0\).

What was tried and why it does not close:

- **C-form comparison:** the coordinate change closes the comparison on the supplied square. At square exit, however, \(qD\le2q(L_c+R_c)=O(q)\), not \(\delta_0\). Extending this proof to distance \(\delta_0/q\) would assume a field/derivative contract on a larger region than the one given.
- **Full-gate continuation:** the weak diagonal is indeed \(Q(1-c)/2\) up to the projected-gate error on the positive side. That matrix-value statement does not control the needed pairwise angular comparison. A fixed projected margin \(L\) gives an absolute integrated error bounded only by \(CL_Te^{-kL^2}\log(1/q)\), which is not uniform for fixed \(L\). Receiver differentiation also produces the boundary trace displayed in `an03decgv1:boundary`; an \(L^2\) residual bound alone is not that trace estimate. A growing-margin proof or a signed off-chart comparison would be additional work not supplied by the stated sources.

Q2EC's transport lemma cannot simply be restarted at \(t_h\): its proof uses MOMC's strong-state, donor-spread, mass-growth and outside-mass estimates on \([t_m,t_h]\). In particular, the \(M\) in its integrable \(O(M/x)\) term is structured strong mass, not the arbitrary cross-residual guard \(M_{\rm res}\).

This identifies a missing estimate in the attempted implication. It does **not** establish a counterexample to the initialized original flow, nor claim that no analytic extension can exist. The stop occurs here; no extra off-chart hypothesis is silently retained in a full theorem.

## Task-by-task contract audit

| Requested part | Delivered status |
|---|---|
| (a) Distance envelope for every complement and Sigma label until physical exit | Proved only while receiver and reference stay in the fixed scaled chart. The extension above is unpaid. SEP's fixed cap is also not automatically contained in the prescribed square. |
| (b) Capped radial gain, all endpoints | Signed radial error and reference gain proved globally. The desired initial-displacement capped gain is proved as a consequence of the still-unpaid distance envelope. |
| (c) Secondary energy and integrated complement mass | Not asserted. BULK and TAILREP retain their distance/gain prerequisites. Existing rational margins are cited, not reproved or promoted to original-flow conclusions. |
| (d) Constants | Explicit for all proved statements. No finite \(C_{\rm ext}\) is asserted. |

SEP supplies the original secondary **entry profile**. It does not supply the evolving distance envelope. MOMC supplies the strong **entry profile** and its half-mass-time normalization, not its future mass-charged tail. The stopped clock can still be used under its existing entry/residual hypotheses; it does not resolve the missing angular estimate.

### Left-half outside ancestry

Q3, including neighborhoods of \(\pi\) and \(3\pi/2\), is not part of either the right-half strong tail law or SEP's Q2 law. MOMC's coarse left-ancestry entry estimate gives at most \(Cq^2\ell^2\). Combining that estimate with the global radial cap and the stopped clock gives only an upper bound of size
\[
C e^{2B}E_gA_q^\lambda q^{1-10(1-\lambda)}\ell^3
\]
for its integrated mass divided by \(q\). This does not vanish. It is an inadequate upper bound, not evidence that the actual mass grows at that rate. The exact unpaid contribution is \(\int_{t_0}^{t_*}\mu_{Q3}/q=o(1)\), or a sharper entry/gain argument that implies it. No Q3 labels have been hidden inside another cohort's tail law.

## Constant and normalization audit

- \(M_{\rm res}\) is the cross-residual guard. \(M_s\) is the positive donor mass in CLOCK's c-form contract, with \(M_s\le1\). This mass restriction is explicitly carried from that contract; it is not proved here.
- \(L_c\) is the supplied fixed chart radius. \(R_c=79/51\) bounds each reference coordinate under \(e<e_*\le1\). Neither is chosen after the residual guards.
- \(p_*=\Phi(-7L_c/10)>0\); \(h_*=(7/10)\phi(0)/p_*\); \(C_T=2+p_*^{-1}+h_*\). These are analytic constants; no numerical minimum or sign test is used.
- \(C_{D,\mathrm{loc}}=p_*^{-1}e^{C_TF_b}\) depends only on the fixed chart, ratio box and the supplied field-error budget.
- \(k=(13/20)^2/8\) is the Gaussian exponent used in the projected-gate bound.
- The remaining Gaussian constants depend only on the ratio box, initial loss and \(R_c\). \(L_T\) is the already prescribed logarithmic duration constant.
- The radial defect budget is \(4B+C(1+M_{\rm res})qL_T\ell\); reference growth is \(e^{2B+C(1+M_{\rm res})q^2L_T\ell}\).
- In the conditional all-endpoint gain, \(A_0=C_D^2\max(1,\delta_0^{-2})\), and the raw-mass prefactor is \(e^{6B+1/\beta+o(1)}\). The fixed physical cutoff enters a multiplicative constant. No additional radial geometric power is required by this estimate; any geometric exponent loss from a future off-chart distance proof remains to be audited.
- \(M_{\rm res}\) appears only with vanishing scales in the proved constants. \(K_Y\) does not appear. \(B\) has the allowed fixed exponential cost.
- \(E_g\), \(A_q\), Q2EC's cutoff \(K\), and SEP's \(Z_\Sigma\) are not used to define local metric/radial constants. Their existing bounded values appear only in the cited entry/clock and Q3 audits. The Q3 coarse clock factor is \(E_gA_q^\lambda\).
- \(\xi=D(t_0)\) is scaled displacement; \(D_0=q\xi\) is physical displacement in TAILREP's capped integration formula. Equivalent joint norms change only fixed constants.

## Proof audit points

1. The transformed scalar decomposition uses the **total donor mass** exactly; the factor \(1-M_s\) must remain nonnegative.
2. For \(x\le r_0\), the transformed donor contribution is the constant \(-\lambda r_0/2\). For \(x>r_0\), its derivative is proportional to \(\mathcal K(\rho r_0)-\mathcal K(\rho x)\le0\). Both one-sided derivatives agree.
3. The transformed off-diagonal derivatives are \(\lambda(1-c)/2\) and \(\lambda(1-c)\Phi(\rho x)^2/2\), including the second-row chain factor. The column-sum calculation uses the induced \(\ell^1\) norm specified in the question.
4. The remainder transformation includes \(-p'\mathcal R_x/p\) in its first diagonal derivative. Omitting it would undercount the supplied value error.
5. The reference is never reset and no radial population weights are differentiated in the pair comparison.
6. TAILREP permits an arbitrary common \(r_1\). Choosing \(r_1=R_{11}(\theta_c)\) requires recombining its \(11\) splitting defect. The total strong-diagonal difference costs \(4r\).
7. The projected-gate estimate is signed: on the negative side \(R_{22}\) itself is small, while \(R_{22}-Q(1-c)/2\) need not be. The proof never charges that latter difference in absolute value on the lower side.
8. Gaussian Cauchy--Schwarz/Hölder bounds give a fourth-root probability cost, hence the displayed exponent \(k\). Multiplication by \(|\sin\theta|\) turns it into a uniform \(O(q)\) radial error.
9. The gain uses the increasing clock \(I\), not monotonicity of \(H\). The larger coefficient \(A_0\) ensures the cap stays active after first physical exit, including reentry.
10. A fixed scaled square is not a physical exit region. Neither growing the square with \(q^{-1}\) nor choosing it after \(M_{\rm res}\) is allowed by the given contract.

## Source provenance

Read-only GitHub retrieval from [TodManlaibaatar/OOD-reversals-theory](https://github.com/TodManlaibaatar/OOD-reversals-theory), October 21, 2026. The roadmap file identifies revision **1.9**. Git blob hashes below identify the exact retrieved text; they are not commit hashes.

| Source path | Git blob SHA |
|---|---|
| `00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md` | `e3dc8676928965190827a732e627f0bf646a81dc` |
| `03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex` | `1777839da3fa10ebf66e8560f7175678753c39b9` |
| `03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex` | `66d3e66aaf99567440a9ebe84fd38c40b047ac83` |
| `03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex` | `8de0d85c64a3d51f3bd9c3662baf2efae0737373` |
| `03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex` | `defc7033fb8c9f49cbfb8b9b278ca71aa34925ac` |
| `02_entry_AN02/AN02_Q2_entry_contracts_v1.tex` | `b149537025e130801fc55b9e49c365c158eee17b` |
| `02_entry_AN02/AN02_secondary_entry_profile_v1.tex` | `c7c857ec10b7f7b2cf42d1cdb452c50edc735587` |
| `02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex` | `539427063c4a08551ce4cb8efe41dab61cde609c` |
| `02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex` | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` |

CFR's expected repository path returned HTTP 404 on two read attempts, although roadmap v1.9 records its reviewed status. The reviewed local `outputs/03_passage_AN03/AN03_c_form_field_reduction_v1.tex` was used instead, SHA-256:
`2251a714337f4b382cc19f5f2451fc48573d236660d6cfc4fc56ebd9a50d2cd1`.
This retrieval discrepancy is not the mathematical obstruction. No repository content was changed.

## Validation and scope

The standalone TeX compiled successfully with the desktop LaTeX compiler. Compilation is a typesetting check only. All mathematical premises are analytic. Label/reference checks, preservation checks and the source archive are verified separately during packaging.

No joint bootstrap, CLOCK passage application, c-form derivation, complement-moment evolution, weak-passage assembly, selection or consolidation was performed. Prior theory files are left unchanged.

