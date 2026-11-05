# Appendix rewrite map · Parts I and II

Part I proves the limiting reversal, explains its mechanism, and proves the linear and critical-scale theorems. **§H states the one deep-regime transfer theorem used in Part I.** Part II supplies its proof from initialization at $S_0=q^{10}$. The critical-scale proof in §G has its own trained-flow argument.

**Page budget.** The individual §A–J ranges add to 39–52 pages. A 45-page working allocation is A 2, B 3, C 5, D 7, E 5, F 2, G 9, H 6, I 5, J 1. With 70–100 pages for Part II, that allocation gives 115–145 appendix pages in the submission PDF. These are writing targets.

## Part I · Reader’s appendix

### A. Reader’s guide · 2–3 pages

| Main result | Read in Part I | Where to check the trained-network step |
|---|---|---|
| Thm 1 · Deep reversal and persistence | §D proves the orbit result. §H applies transfer to it. | §H, with the initialization-to-window proof in §§R2–R5. |
| Thm 2 · Mechanism and timing | §E proves the decomposition, signs, and timing using the window from §D. | §E uses the cohort and background estimates stated in §H. |
| Thm 3 · Linear control | §F, after the model in §B. | The exact linear flow is solved in §F. |
| Thm 4 · Critical versus deep | §G proves critical pre-weak descent. §D identifies the deep comparator. | §G proves critical trained transfer. §H supplies the deep comparison on fixed centered windows. |

**Dependency graph.** B → C. B/C → D, F, G. D + H → initialized Thm 1. B/C + D + H → initialized Thm 2 in E. R1 → R2 → R3 → R4 → R5 supplies H. In this graph H denotes the trajectory and transfer estimates; D supplies the limiting signs used in the final application. §I compares predictions with measurements. §J states the learned-depth question left open by G.

**Notation table.** Reserve a row each for the learned responses $\mathsf m_p$, radial masses $M,N$, comparison mass $n$, error $E_\xi$, scaled error $e_q$, and cluster rates $D_p$. Give the two time origins separate rows. Use [PAPER · `PAPER_theory_section_v1.tex`][PAPER] for the notation inventory. Its mechanism and critical-regime status paragraphs predate PB and COD.

### B. Setup and exact identities · 3–4 pages · full proof

- [F · `RELU_POPULATION_FOUNDATIONS_v2.tex`][F], propositions P1–P7. Define the two Gaussian clusters, loss, aligned-balanced isotropic initialization, normalized time, and angular/radial representation. Derive the population flow, the probe error, the exact two source rates including mixture weights, and the cluster-learning observables.
- [P · `THEOREM_A_ANALYTICAL_PROGRESS.tex`][P], labels `pa:representation`, `pa:exactflow`, `pa:exactrates`, `pa:charts`, and `pa:overlap`. Fix the chart orientation and Gaussian kernel conventions here. Define $e_q=(E_\xi-1/2)/q^2$ so “below baseline” means $e_q<0$.
- [RTA · `AN07_rate_transfer_and_assembly_v1.tex`][RTA] gives the deep orbit’s phase-matched weak clock. [HBD · `AN04_trained_half_mass_bridge_donors_v1.tex`][HBD] gives the critical clock from the actual strong half-mass hit. Use distinct symbols in the rewrite, even where the standalone files reuse one.

### C. Toolbox · 4–6 pages · full proofs of the shared lemmas

| Lemma to extract once | Source and proof boundary |
|---|---|
| Early-time comparison and physical coordinates | [P][P], `pa:earlybounds` and `pa:targetcomparison`. For the physical second-coordinate bound use [HBD][HBD], `an04hbdv1:physical`, and [BRW · `AN04_bridge_return_before_weak_learning_v1.tex`][BRW]’s delay argument. State the time range and initialization hypotheses of each bound. |
| Gaussian tails, donor kernels, and endpoint strips | [F][F], P4 and P11; [MOMC · `AN02_moving_overlap_M_clock_passage_v1.tex`][MOMC], `donorkernels`; [COD · `AN04_core_output_descent_v1.tex`][COD], proof of `trained`. Extract the compact-chart kernel expansion and the elementary strip bound. The long-time deep Q3 strip budgets have their own proof in §R3. |
| Path-law extraction and same-field order | [HBD][HBD] and [BRW][BRW]. Give the compactness argument on a fixed horizon, the label measure retained in the limit, and the order comparison for labels evolving in the same field. §G verifies the bounds for the critical trajectory. |
| Two-face barriers and fixed-time probe transfer | [PB · `AN01_post_half_mass_barrier_v1.tex`][PB] and [COD][COD] supply the first-contact arguments. COD’s `trained` proof supplies the compact-sector plus endpoint-strip passage to the two scaled probe components. State each tool with explicit hypotheses. Keep its model-specific signs and sector checks in §E or §G. |

### D. Limiting system and Theorem 1 on the orbit · 6–8 pages · full proof

1. **Equations and selected branch.** [P][P], `pa:branch`, `pa:weakclock`, `pa:atomicerror`, `pa:atomiclag`, and `pa:limitreversal`. Derive the coherent orbit, its scaled error, and its source rates. §R4 later proves that the initialized flow selects this branch.
2. **Learned witness and timing.** [WIT · `AN06_learned_orbit_witnesses_v2.tex`][WIT], `inc:AN06:v2:quarterrate`, `postthreshold`, and `uniformtheorem`. Establish the parameter rectangle and common windows with strict margins. Record the mass threshold that §E will cite.
3. **Below-baseline corollary.** Display the signed error value on the active orbit. In the notation $A=\zeta-X$, $Z=X-Y$, it is $-AZ-A^2/2$. WIT supplies the gate gap. For a proof using $Z>0$ throughout the window, prove the orbit gap lemma from [PB][PB] here and cite it again in §E. This avoids a D → E → D dependency. The full trained producer-sign conclusion still belongs in §E.
4. **Persistence.** [LP · `LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex`][LP], orbit-clearing and `uniform-clear` results, plus [LPR · `LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex`][LPR], `combinedtheorem`. Prove late clearing on the limiting orbit here. The initialized diagonal argument and its growing horizon belong to the application of §H.

### E. Mechanism and Theorem 2 · 4–5 pages · full proof using §H

- **Separate source, carrier, and producer.** [BC · `AN01_original_flow_bcore_v1.tex`][BC], `an01bcv1:channels` and `twoway`, then [CPD · `AN01_channel_producer_decomposition_v1.tex`][CPD], `an01cpdv1:table` and `help`. Derive the strong cluster’s exposure times its positive lag, with the signed remainder. For the weak cluster keep input and output rotation of the strong core. In the four-term table the target/core input term is nonpositive, the weak-produced input term positive, the target output term positive, and the weak-produced output term negative.
- **Full-window sign.** [PB][PB], `an01pbv1:sign` and `transfer`. Apply the orbit gap to the weak-produced input term and carry the strict sign to the trained window. [PHS · `AN01_post_half_mass_input_sign_v1.tex`][PHS] supplies the earlier local argument if a bound from it is used. Cite §H for the gate margins, cohort tracking, and background estimates used to control the channel remainders. Convergence of the two total source rates alone cannot identify four signed pieces.
- **Timing.** Cite §D’s WIT corollary. At $\zeta=5\pi/9$ the proved crossover is after **weak quarter mass** on the reference orbit. For the trained network state the ordered rate windows and the response threshold given by §H. Put any comparison to an empirically defined saturation time in §I.

### F. Linear control and Theorem 3 · 2 pages · full proof

[LP][LP], labels `inc:LP:v1:linear-theorem`, `logistic`, `linear-error`, and `linear-SIM`. Show preservation of diagonal dynamics, solve the scalar logistic equations, then differentiate the error for an arbitrary nonzero probe. Retain equal initial input/output weights, simultaneous diagonality of the initial Gram and data second moment, and $0<c_r<1$, $a_r>0$. If reporting per-cluster signs, add the per-cluster diagonality hypothesis from `linear-source`. LP’s ReLU persistence pages have their home in §D.

### G. Critical scale and Theorem 4 · 8–10 pages · full trained proof

| Proof step | Write from these sources |
|---|---|
| Critical exponent | [RMS · `AN04_canonical_regime_map_synthesis_v1.tex`][RMS] and [CRA · `AN04_canonical_regime_audit_v1.tex`][CRA]. Derive $1/\omega$ from the comparison spread $(S_0/A)^\omega/q$ at fixed nominal mass $A$. Keep the distinction between locating the scale and proving the behavior of training there. |
| Actual entry and strong half mass | [CFS · `AN04_critical_family_strong_entry_v1.tex`][CFS] and [RPS · `AN04_resident_phase_split_v1.tex`][RPS] for the Q1 spread and Q4 core, [CTE · `AN04_critical_trained_entry_v1.tex`][CTE] for trained small-cap entry, then [HBD][HBD] for `clock`, `incoming`, `outer`, and `physical`. Apply the shared kernels from §C. |
| Resident interval before weak learning | [BRW][BRW], `an04brwv1:delay`, `field`, and `budget`. Obtain fixed-horizon extraction and delay of the measured weak response. Distinguish the initially inactive band that returns from the far tail that drives the moment estimate. |
| Core descent and trained transfer | [COD][COD], `an04codv1:ceiling`, `mean`, `exposure`, `positive`, `main`, and `trained`. Show that the core’s negative term dominates the positive contribution from the remaining active labels. Verify the critical Q2 and Q3 sector estimates using CRA’s `outer`, [PROFILE · `AN02_strong_entry_profile_and_tail_budget_v1.tex`][PROFILE]’s angular field, and P’s early comparison. Apply §C at fixed time. |
| Comparison to the deep orbit | Cite §D for the orbit and §H for deep convergence on fixed centered windows. Give the numerical orbit evaluation near $-2.0$ and the finite-width observation near $-7.2$ their provenance in §I. |

Keep COD’s quantifiers visible: fix allowed $\rho,\zeta$ and $c>0$; for each desired depth $K>0$, choose a finite delay, then take $q$ sufficiently small. At that time $e_q<-K$ and the weak response is still below the prescribed level. This establishes the **pre-weak** comparison. §J defines the distinct learned-window question.

### H. Deep-regime transfer · 5–7 pages · statement, outline, one full proof

**State one theorem with numbered conclusions** for the initialized $S_0=q^{10}$ flow. Use [FWC · `AN07_finite_window_continuation_v1.tex`][FWC] for fixed-window error transfer, [RTA][RTA] for the clock, learned responses/losses, background and source-rate precision, and [PSE · `AN07_probe_sector_energy_v1.tex`][PSE] for the underlying probe-sector estimate. Include the fixed-cohort moment tracking and gate separation invoked in BC/CPD. §D uses signed-error and late-window control. §E uses the stronger cohort-level conclusions. Keep the channel algebra in E.

| Stage | Input → output to state in H | Full proof |
|---|---|---|
| S1 | Aligned isotropic initialization → strong profile at half mass, primary weak seed and clock cohort, secondary tail bounds | §R2 |
| S2–S3 | S1 entry → closed clock, energy, residual, field, and strip estimates up to a fixed **positive** weak response | §R3 and the barrier lemma in §H |
| S4 | Reached small response → matched weak clock and selected coherent orbit at fixed small weak mass | §R4 |
| S5 | Selected entry → fixed-window error, source rates, learning thresholds, and late error transfer | §R5 |

**Full proof chosen for H: the response barrier (RB).** Use [WPT · `AN03_weak_passage_theorem_v1.tex`][WPT] for the two-boundary stopped interval and [RB · `AN03_response_barrier_v1.tex`][RB] to exclude the zero boundary on that interval. The core retains a positive response of order $q^2$. Alignment and the outside-mass bound make the negative outside contribution $o(q^2)$, and the primary weak contribution absorbs the secondary error. Prove the barrier from WPT’s explicit hypotheses here. §R3 proves those hypotheses and invokes this lemma exactly once. Close H by applying the transfer conclusions to §D’s margins and clearing time to obtain the initialized rebound and persistence on $[S,S+T_q]$, $T_q\to\infty$.

### I. Experiments · 4–5 pages · empirical

| Question | Files to open |
|---|---|
| Does the population flow converge to the deep orbit, and how do companion runs compare? | [Theory-regime protocol][exp-protocol], [aligned comparison table][exp-table], and [numerical orbit trace][exp-orbit]. |
| How do width, depth, robustness, and the $\kappa=3.6$ sweep affect the measurements? | [Depth/robustness protocol][exp-depth] and [local follow-up protocol](depth_robustness_v2/PROTOCOL.md). Report width and sample size separately. Use the recorded time-step and quadrature checks when assigning numerical status. |
| Which sources drive the composition probes, and what changes under linear controls? | [Composition-probe definitions and runs][exp-comp] and [architecture-control report][exp-arch]. Separate off-cone and composition probes, and tied and untied controls. |
| Which events does the timing table compare? | Use the suite-specific definitions above for each row. The [archived timing summary][exp-time] concerns the $G$ timing statistic. Label the clock and event explicitly for the measured crossover, quarter response, and any saturation criterion. |

### J. Open problem E5 and context · 1–2 pages · statements only

For parameters on the learned rectangle, let $e_*=\min_{s\in J}\mathcal E_{\rm coh}(s)$. In the **critical trained family**, does a time in the learned window attain scaled error strictly below $e_*$ for sufficiently small $q$? Use DRR’s definition of the candidate set: center the window at the measured weak half-response hit and impose both response and cluster-loss criteria. Establishing a learned candidate time is part of the problem.

| What remains to be shown | Where to find the sharpest statement for the rewrite |
|---|---|
| Retain enough of a pre-weak depth advantage | [DRR · `AN04_learned_depth_retention_v1.tex`][DRR], `an04drrv1:test` and `missing`. The exact displacement identity gives the strict comparison required at a learned time. |
| Bound the net signed probe motion to that time | [SPM · `AN04_signed_probe_motion_v1.tex`][SPM]. The favorable longitudinal term and the transverse regression term must be compared with their signs. |
| Continue the critical weak clock to the learned regime | [TBW · `AN04_transverse_balance_and_weak_clock_v1.tex`][TBW] proves a small positive response hit. [RQT · `AN04_response_quarter_half_transfer_v1.tex`][RQT] gives the later half-response-or-residual-boundary alternative. [CFRsp · `AN04_cap_free_cross_response_v1.tex`][CFRsp] identifies a remaining signed forcing integral. State these as partial results. |

For a short context paragraph use [IMP · `AN04_inactive_mass_persistence_v1.tex`][IMP] and [FFP · `AN04_fixed_fraction_persistence_v1.tex`][FFP] for finite-horizon survival and eventual return of fixed tail ranks, [SWP · `AN04_split_weak_passage_v1.tex`][SWP] and [MPB · `AN04_mass_preserving_bridge_depth_v1.tex`][MPB] for the prescribed split and bridge effect, and [GOE · `AN04_gate_threshold_and_outlier_escape_v1.tex`][GOE] for gate-crossing direction. Keep the E5 discussion separate from the completed COD proof.

## Part II · Complete reference proof of §H

The rows below give a rewrite order. A named estimate can cite an earlier numbered lemma in the same PDF. Inventories and earlier versions are useful for tracing a bound during drafting; the final proof should point to the section that actually establishes it.

### R1. Additional setup for deep entry

Start with [RTA][RTA]’s `inventory` and the “How the initialized theorem is assembled” section of [PAPER][PAPER]. Fix the deep-only conventions that are cumbersome in §§B–C: label partitions by ancestry, the clock subcohort, primary and secondary energies, stopping times, and the order of choosing constants. For exact dynamics and early comparison cite §§B–C. Introduce later strip partitions in §R3 where their boundaries matter.

### R2. S1 · Entry from initialization to strong half mass

| Proof block | TeX files in reading order | Result carried into §R3 |
|---|---|---|
| Strong ancestry, profile, and passage | [TAIL · `AN02_strong_ancestry_and_tail_transport_v1.tex`][TAIL], [PROFILE][PROFILE], [OWPT · `AN02_overlap_window_profile_transfer_v1.tex`][OWPT], [MOMC][MOMC] | Strong core and tail at actual strong half mass, with control of the moving clock. [SMCP · `AN02_strong_M_clock_passage_v1.tex`][SMCP] explains why a fixed overlap needed refinement. |
| Weak-side arrival and boundary layers | [ARR · `AN02_weak_side_arrival_v1.tex`][ARR], [Q2 · `AN02_Q2_profiles_and_localized_tracking_v1.tex`][Q2], [Q2E · `AN02_Q2_boundary_layers_and_cohort_energy_v1.tex`][Q2E] | Incoming weak labels, the Q2 comparison profile, and endpoint energy estimates. |
| Primary and secondary weak entry | [Q2EP · `AN02_Q2_entry_through_strong_passage_v1.tex`][Q2EP], [Q2EC · `AN02_Q2_entry_contracts_v1.tex`][Q2EC], [SEP · `AN02_secondary_entry_profile_v1.tex`][SEP] | Primary seed and clock cohort with controlled angles and energy, plus the recruited secondary-tail profile. End with one joint S1 statement. |

### R3. S2–S3 · Weak passage to a fixed small response

1. **Clock, energy, residual.** [TAILREP · `AN03_mass_charged_tail_and_selection_defects_v1.tex`][TAILREP], [BULK · `AN03_bulk_clock_and_secondary_Q2_energy_v1.tex`][BULK], [RCET · `AN03_residual_closure_and_eta0_transport_v1.tex`][RCET], [LCRC · `AN03_ledger_cap_residual_closure_v1.tex`][LCRC]. Establish the bulk clock and the residual/energy inequalities on the common stopped interval. [RET2 · `AN03_two_sided_passage_and_Q2_retention_v2.tex`][RET2] and [SGWR · `SIGNED_GROWTH_WEAK_RETENTION_v1.tex`][SGWR] supply earlier retention estimates where cited.
2. **Tail control and strong field.** [DECG · `AN03_distance_envelope_and_capped_gain_v1.tex`][DECG] and [GESG · `AN03_global_envelope_signed_gate_v1.tex`][GESG] lead to [S2CP · `AN03_S2_closure_package_v1.tex`][S2CP]. [LOC · `AN03_local_rate_mean_tracking_v1.tex`][LOC], [CLOCK · `AN03_exact_amplitude_clock_and_c_passage_v1.tex`][CLOCK], and [CFR · `AN03_c_form_field_reduction_v1.tex`][CFR] lead to [CFA · `AN03_c_form_assembly_v1.tex`][CFA]. Preserve the joint stopping conditions when using these estimates.
3. **Boundary strips.** [Q3SB · `AN03_Q3_strip_budgets_v1.tex`][Q3SB], [PISB · `AN03_pi_strip_budget_v1.tex`][PISB], and [LSB · `AN03_late_strip_budget_v1.tex`][LSB]. Account for both endpoints and the late inner strip. Cite §C for the elementary kernel and tail bounds.
4. **One closing argument.** [WPT][WPT] improves the guards up to the first zero or positive response boundary. Apply the **RB lemma proved in §H** to exclude zero. Record the reached mass, clock accuracy, and surviving core estimates consumed by §R4. This invocation uses only H’s standalone barrier lemma; H’s transfer conclusion comes later.

### R4. S4 · Selection of the coherent orbit

[WBR · `AN03_weak_boundary_return_v1.tex`][WBR] restores the weak input sign. [MP · `AN03_matching_package_v1.tex`][MP] matches the actual cohort, weak mass, and logistic clock. [SRR · `AN03_strong_reference_reduction_v1.tex`][SRR] reduces the strong reference field. [WCS · `AN03_weak_chart_selection_v1.tex`][WCS] reduces the weak chart and applies the selection theorem. Use [WEAK · `AN03_weak_transit_forcing_and_orbit_selection_v1.tex`][WEAK] and [TAILREP][TAILREP] for the selection criterion and its error bounds. [SI · `AN03_selection_interface_v1.tex`][SI] is a checklist of the hypotheses. End with one estimate at a fixed small weak mass, in the phase convention of §B.

### R5. S5 · Transfer of probe error and rates

- [CWI · `AN07_compact_window_interface_v1.tex`][CWI] identifies the precision required of the background. [PSE][PSE] proves the probe-sector energy bound at entry. State the bound for the full probe, including the labels outside the selected cohorts.
- [FWC][FWC] propagates the selected masses, moments, and error on each fixed centered window. [RTA][RTA] supplies gate separation, both source rates, and learning bounds. Preserve the intermediate estimates that §E cites for the four-term decomposition.
- Match these results item by item to §H. RTA’s `theoremA` and `persistence` are the checks on the final trained statement. The short arguments integrating the rate windows and extending late clearing to a growing horizon appear once in §H.

---

**Source versions.** Theory-repository links point to the revision used for the original map. COD and the later critical-regime follow-ups link to TeX files beside this map in the Research project. Experimental links point to the inspected experiment revision or a labeled local protocol.

[PAPER]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/PAPER_theory_section_v1.tex
[F]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/01_foundations/RELU_POPULATION_FOUNDATIONS_v2.tex
[P]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex
[RTA]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/07_compact_windows_AN07/AN07_rate_transfer_and_assembly_v1.tex
[HBD]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_trained_half_mass_bridge_donors_v1.tex
[BRW]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_bridge_return_before_weak_learning_v1.tex
[MOMC]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_moving_overlap_M_clock_passage_v1.tex
[COD]: 09_canonical_regime_AN04/AN04_core_output_descent_v1.tex
[PB]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/08_mechanism_AN01/AN01_post_half_mass_barrier_v1.tex
[WIT]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex
[LP]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/04_witnesses_persistence/LINEAR_CONTRAST_LIMIT_PERSISTENCE_v1.tex
[LPR]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/04_witnesses_persistence/LIMIT_LEARNED_PERSISTENCE_RETENTION_v1.tex
[BC]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/08_mechanism_AN01/AN01_original_flow_bcore_v1.tex
[CPD]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/08_mechanism_AN01/AN01_channel_producer_decomposition_v1.tex
[PHS]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/08_mechanism_AN01/AN01_post_half_mass_input_sign_v1.tex
[RMS]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_canonical_regime_map_synthesis_v1.tex
[CRA]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_canonical_regime_audit_v1.tex
[CFS]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_critical_family_strong_entry_v1.tex
[RPS]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_resident_phase_split_v1.tex
[CTE]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_critical_trained_entry_v1.tex
[PROFILE]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex
[FWC]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/07_compact_windows_AN07/AN07_finite_window_continuation_v1.tex
[PSE]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/07_compact_windows_AN07/AN07_probe_sector_energy_v1.tex
[WPT]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_weak_passage_theorem_v1.tex
[RB]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_response_barrier_v1.tex
[DRR]: 09_canonical_regime_AN04/AN04_learned_depth_retention_v1.tex
[SPM]: 09_canonical_regime_AN04/AN04_signed_probe_motion_v1.tex
[TBW]: 09_canonical_regime_AN04/AN04_transverse_balance_and_weak_clock_v1.tex
[RQT]: 09_canonical_regime_AN04/AN04_response_quarter_half_transfer_v1.tex
[CFRsp]: 09_canonical_regime_AN04/AN04_cap_free_cross_response_v1.tex
[IMP]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_inactive_mass_persistence_v1.tex
[FFP]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_fixed_fraction_persistence_v1.tex
[SWP]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_split_weak_passage_v1.tex
[MPB]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_mass_preserving_bridge_depth_v1.tex
[GOE]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/09_canonical_regime_AN04/AN04_gate_threshold_and_outlier_escape_v1.tex
[TAIL]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_strong_ancestry_and_tail_transport_v1.tex
[OWPT]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_overlap_window_profile_transfer_v1.tex
[SMCP]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_strong_M_clock_passage_v1.tex
[ARR]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_weak_side_arrival_v1.tex
[Q2]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_Q2_profiles_and_localized_tracking_v1.tex
[Q2E]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_Q2_boundary_layers_and_cohort_energy_v1.tex
[Q2EP]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_Q2_entry_through_strong_passage_v1.tex
[Q2EC]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_Q2_entry_contracts_v1.tex
[SEP]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/02_entry_AN02/AN02_secondary_entry_profile_v1.tex
[TAILREP]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_mass_charged_tail_and_selection_defects_v1.tex
[BULK]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_bulk_clock_and_secondary_Q2_energy_v1.tex
[RCET]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_residual_closure_and_eta0_transport_v1.tex
[LCRC]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_ledger_cap_residual_closure_v1.tex
[RET2]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_two_sided_passage_and_Q2_retention_v2.tex
[SGWR]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/SIGNED_GROWTH_WEAK_RETENTION_v1.tex
[DECG]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_distance_envelope_and_capped_gain_v1.tex
[GESG]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_global_envelope_signed_gate_v1.tex
[S2CP]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_S2_closure_package_v1.tex
[LOC]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_local_rate_mean_tracking_v1.tex
[CLOCK]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_exact_amplitude_clock_and_c_passage_v1.tex
[CFR]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_c_form_field_reduction_v1.tex
[CFA]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_c_form_assembly_v1.tex
[Q3SB]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_Q3_strip_budgets_v1.tex
[PISB]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_pi_strip_budget_v1.tex
[LSB]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_late_strip_budget_v1.tex
[WBR]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_weak_boundary_return_v1.tex
[MP]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_matching_package_v1.tex
[SRR]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_strong_reference_reduction_v1.tex
[WCS]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_weak_chart_selection_v1.tex
[WEAK]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_weak_transit_forcing_and_orbit_selection_v1.tex
[SI]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/03_passage_AN03/AN03_selection_interface_v1.tex
[CWI]: https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/d179abc2db004413a612612ad577861ec8c8942c/07_compact_windows_AN07/AN07_compact_window_interface_v1.tex
[exp-protocol]: https://github.com/TodManlaibaatar/Swing-by-TwoLayerReLU/blob/e095413c44bd5698b29882c19a066e998b17284f/theory_regime/PROTOCOL.md
[exp-table]: https://github.com/TodManlaibaatar/Swing-by-TwoLayerReLU/blob/e095413c44bd5698b29882c19a066e998b17284f/theory_regime/results/compare/compare_table.md
[exp-orbit]: https://github.com/TodManlaibaatar/Swing-by-TwoLayerReLU/blob/e095413c44bd5698b29882c19a066e998b17284f/theory_regime/results/orbit/orbit.csv
[exp-depth]: https://github.com/TodManlaibaatar/Swing-by-TwoLayerReLU/blob/e095413c44bd5698b29882c19a066e998b17284f/depth_robustness_v1/depth_robustness/PROTOCOL.md
[exp-comp]: https://github.com/TodManlaibaatar/Swing-by-TwoLayerReLU/blob/e095413c44bd5698b29882c19a066e998b17284f/composition_probes_v1/composition_probes/README.md
[exp-arch]: https://github.com/TodManlaibaatar/Swing-by-TwoLayerReLU/blob/e095413c44bd5698b29882c19a066e998b17284f/arch_control_summary/REPORT.md
[exp-time]: https://github.com/TodManlaibaatar/Swing-by-TwoLayerReLU/blob/e095413c44bd5698b29882c19a066e998b17284f/swing_grid_preregistered/evaluation_v1_postspecialization/G_timing_summary.csv
