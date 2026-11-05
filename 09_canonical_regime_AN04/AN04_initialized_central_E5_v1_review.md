# AN04 review · Initialized central E5 from the first small hit to the learned endpoint

**Decision for review.** The draft proposes that for each fixed $c>0$, at $\rho=2/3$, $\zeta=5\pi/9$ and $S_0=cq^{18/5}$, the actual trained flow reaches half weak response and satisfies all four learning guards at $T=t_{1/2}+s_*$. It further proposes $e_q(T)\to-\infty$ for the scaled probe error, hence $e_q(T)<e_*=\min_J\mathcal E_{\rm coh}$ for sufficiently small $q$. This would put the minimum over the learned window below the central coherent minimum because that window contains $T$. It makes no claim about the location of the trained minimizer, its derivative signs, or uniformity in $c,\rho,\zeta$. The unscaled probe loss still tends to $1/2$. [Companion TeX](AN04_initialized_central_E5_v1.tex)

The pinned theory snapshot records learned-window E5 as open. Its COD theorem already gives arbitrarily negative scaled error before weak learning. The new claim needs the *same actual trajectory* to reach a learned time with enough negative vertical probe output. The passage argument is in §§2–4. The history estimate and the first-exit argument are in §§5–10. This is a proposed increment awaiting independent mathematical review. [Theory roadmap at the source revision](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/12aa3b6f48f83a097600bcf9b44d93399e2f9697/00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md)

## What each part must establish

| TeX section | Estimate to check | Where it is used |
|---|---|---|
| §2 · First small hit | $\sup_{[t_0,t_\eta]}S=O(1)$, $t_\eta-t_h=\ell/L+O(1)$ | Gives a fixed interval of dissipation and bounds the accumulated regression errors |
| §3 · Fixed loss gap | $4\mathcal L(t_\eta)\le Q-\Delta$ and $t_{1/2}-t_\eta=O(1)$ | Gives an actual measured half clock and uniform mass on fixed centered intervals |
| §4 · Axis separation | $(m,z,h,n)(t_{1/2}+s)\to(1,0,0,N(s))$ on compact intervals | Verifies both responses and both cluster losses at $s_*$ |
| §5 · Probe exposure | $\|p_T\|_2=O(q\sqrt\ell)$ and the weighted error of replacing $-W_2(T)$ by $G/2$ is $o(q^2)$ | Bounds the horizontal cost and identifies the signed history to estimate |
| §6 · Prefix estimates | $B/I$ is uniformly small after late fixed delay, and $I(t_R-1)\gg q^{3/4}$ | Pays accumulated Gaussian errors before any gate-retention assumption |
| §§7–9 · Retained labels | On most right physical mass, $W_2\le-c\cos\alpha\,I$ and $U_2\le-dq\cos\alpha\sqrt\ell$ through $T$ | Gives Q4 simultaneously negative output and positive terminal exposure |
| §10 · Signed budget | Favorable output $\gtrsim q\sqrt\ell\, I(T)$; all adverse output $\le(C\sqrt\delta+o(1))q\sqrt\ell\,I(T)$ | Pays the positive non-core output, exceptional Q4 labels and the entire horizontal cost |

Here $\ell=\log(1/q)$, $L=\rho^2/2$, $Q=\rho^2+q^2$, $t_h$ is the strong right-ancestry half-mass time and $t_\eta$ is the first subsequent hit of a fixed small measured weak response. In §§5–10, $I(t)$ integrates the positive-coordinate overlap $\int(U_1)_+(U_2)_+\,dl$ from $t_0=t_h+b_0$, $B(t)=q(1+t-t_0)$, and $t_R=t_h+\ell/L-R$. The probe weight $p_T=(U(T)^\top\xi)_+$ always uses the gate at the endpoint.

## From initialized mass to the four guards

**Small-hit mass.** For the transverse energy $E=\tfrac12\int(U_2^2+W_2^2)\,dl$, completing a clusterwise square retains the growth coefficient $Q$ in $E'\le QE+C(q\sqrt E+q^2)$. Before the first of the small hit, $S=4$, and $t_d=t_0+(2/Q)\log(d/q)$, this gives $\sqrt E\lesssim q e^{Q(t-t_0)/2}$. The time integrals of $\sqrt E$ and $E$ cost $O_{b_0}(d)$ and $O_{b_0}(d^2)$. Damping of $1-m$ then rules out $S=4$. If the hit is later than $t_d$, a positive-length initialized Q2 arc already has order-one weak amplitude there. Continued exponential growth on that arc would exceed the global linear mass upper bound within bounded time. An earlier hit needs order-one transverse energy, which also supplies the clock lower bound. See the TeX labels **smallhit**, **energy** and **envelope**; all internal labels have prefix **an04ce5v1:**.

**Loss gap and half response.** Bounded mass controls the speed of $n$, so before the first small hit the flow spends a fixed duration with $\eta/2\le n\le\eta$. On this interval the square completion for $\det F$ turns $4\mathcal L\le Q+o(1)$ and $n\ge\eta/2$ into a uniform lower singular-value bound. The output-layer gradient alone dissipates a fixed amount of loss. After the resulting gap, $1-n\ge1/2$ would force further loss dissipation at rate at least a constant times $(B_0+Cu)^{-1}$ for time $u$ after the hit. Its integral exceeds the entire loss budget at a fixed finite horizon. This step gives half response without assuming monotonic weak learning. See **gram**, **gap**, **halfclock**.

**Guard transfer.** Charge horizontal energy on a compact Q2 arc and vertical energy off it. The projected four-regression equation preserves the coefficient $Q$ in the defect inequality. On fixed-delay right ranks the discounted COD square ceiling is integrable, including the approaching vertical axis. The Q2 seed determines the remaining cost of the excluded weak arc. Taking limits in the stated order gives axis separation. In particular the weak gradient has squared norm $2n+o(1)$ and the measured half response fixes the translation of $N(s)=(1+e^{-\rho^2s})^{-1}$. At $s_*$, $m\to1$ and $N(s_*)>1/4$ by WIT. The cluster loss ratios tend to $0$ and $(1-N(s_*))^2<9/16<169/196$. The proof uses the analytic lower bound on $s_*$; a numerical value is used only in the diagnostic below. See **defect**, **logistic**.

## How the Q4 history pays the endpoint costs

Set $G_\alpha=\int_0^T[Q_1 z b_1-Q(1-n)b_2]\,dt$. Positive $G$ drives $W_2(T)$ negative. The budget keeps the signed Q4 integral, including unfavorable Q4 labels, and charges every positive vertical output outside Q4. With $H=f_{T,1}(\xi)/q$, the sufficient margin is

\[
 \underbrace{\frac{\int_{\rm Q4}p_TG\,dl-\int_{{\rm Q4}^c}p_T(-G)_+\,dl}{2q^2}}_{M_q}
 -\frac{H^2}{2}+\frac{\sin(q\zeta)}q H+e_* .
\]

A positive lower limit suffices. The candidate proof gives $M_q\gtrsim\sqrt\ell\,I(T)/q$ while $H^2=O(\ell)$ and $I(T)/q^{3/4}\to\infty$. Thus the lower bound for the signed margin diverges. The exact energy identity includes the vertical quadratic term. Since $f_{T,2}(\xi)=O(q\sqrt\ell)$, the coefficient multiplying $f_{T,2}(\xi)/q^2$ tends to one. See **budget**, **criterion**, and §10.

Three distinct comparisons produce that margin.

1. **Integrated strong response.** Damping of $z$ gives a time integral comparable from below to $I$, after charging the entrance deficit and the negative part of $z$. The Q1 band with $\cos\alpha\asymp(1+s)^{-4}$ rules out $I=O(q(1+s))$ even for slowly diverging delays $s=t-t_0$. A second band with $\cos\alpha\asymp q^{1/3}$ rules out $I(t_R-1)=O(q^{3/4})$. Both are comparisons in the finite-$q$ dynamics. See **prefix**, **earlyh**, **uniform**.
2. **Gate retention through the weak transition.** For retained right labels with $k=\cos\alpha$, $\int z b_1\gtrsim kI$. At a late fixed delay the rank ceiling and overlap lower bound make accumulated weak excitation small relative to this amount. On $U_2\le0$, further weak excitation costs $O(qk)$ per unit time. The cumulative signed output then satisfies $W_2\le-ckI$. By $t_R$, the input reaches the stronger face $U_2\le-dqk\sqrt\ell$. On the stopped centered interval a small adverse $h$ keeps the face inward. The signed approximation of $T_2-h$ supplies this last bound. See **bulk**, **wnegative**, **gate**, **deepgate**, **t2**.
3. **All returning labels.** The exceptional right labels have small *physical weight* in the norm of their time supremum. On the left, tracing the growing vertical mode backwards for the labels with $p_T>0$ makes their entire physical weight small too. This permits Cauchy–Schwarz to charge all positive output once. A fixed central Q4 subarc supplies the favorable constant independently of the truncation. See **left**, **activeleft** and §10.

An endpoint covariance sign alone would be insufficient. The two-atom test in §5 has favorable donor/core ordering but scaled error tending to zero as the two angles coalesce. Likewise, the earlier prescribed-entrance example permits an arbitrarily deep pre-weak probe and complete loss of exposure on the learned window. These examples explain why the new estimate uses initialized histories weighted by the *terminal* gate. [Learned-depth retention review](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/12aa3b6f48f83a097600bcf9b44d93399e2f9697/09_canonical_regime_AN04/AN04_learned_depth_retention_v1_review.md)

## Dependency and boundary audit

| Imported result | Specific use |
|---|---|
| HBD and BRW | Physical entrance envelopes, strong mass clock, fixed-delay tagged transfer, positive donor moment and resident mean budget. [HBD](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/12aa3b6f48f83a097600bcf9b44d93399e2f9697/09_canonical_regime_AN04/AN04_trained_half_mass_bridge_donors_v1.tex) · [BRW](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/12aa3b6f48f83a097600bcf9b44d93399e2f9697/09_canonical_regime_AN04/AN04_bridge_return_before_weak_learning_v1.tex) |
| COD and TBW | Rank ceiling, bottom-path bound, fixed-delay bulk location, initialized Q2 seed and positive cone through the first small hit. [COD](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/12aa3b6f48f83a097600bcf9b44d93399e2f9697/09_canonical_regime_AN04/AN04_core_output_descent_v1.tex) · [TBW](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/12aa3b6f48f83a097600bcf9b44d93399e2f9697/09_canonical_regime_AN04/AN04_transverse_balance_and_weak_clock_v1.tex) |
| REC, CFCR and GTM | Gaussian features, regression Gram terms, cap-free shape error and exact transverse energy identity. [REC](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/12aa3b6f48f83a097600bcf9b44d93399e2f9697/09_canonical_regime_AN04/AN04_residual_exchange_channels_v1.tex) · [CFCR](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/12aa3b6f48f83a097600bcf9b44d93399e2f9697/09_canonical_regime_AN04/AN04_cap_free_cross_response_v1.tex) · [GTM](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/12aa3b6f48f83a097600bcf9b44d93399e2f9697/09_canonical_regime_AN04/AN04_gate_transport_and_transverse_memory_v1.tex) |
| WIT v2 | Central coherent clock, local minimizing interval and strict quarter-response margin. Only the coherent orbit supplies $s_*$ and $e_*$. The initialized guards require the separate passage argument. [WIT](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/12aa3b6f48f83a097600bcf9b44d93399e2f9697/04_witnesses_persistence/AN06_learned_orbit_witnesses_v2.tex) |

**Where I would start the proof review.**

- **§6, moving band.** Check the lower comparison for *both* layers at entrance on the shrinking Q1 band, including the integrated wrong-gate tail. Then check the discounted vertical perturbation on every prefix. Fixed-rank convergence alone cannot justify either shrinking band. Failure of the stronger $q^{3/4}$ bound would leave the deep-gate speed and final rate unpaid.
- **§9, order of choices.** First fix $R$ to damp the incoming negative part of $h$. Next choose the discarded right strip $\delta$ small enough for both the centered error $C_R\sqrt\delta$ and the terminal adverse-output cost. Only then take the compact-specific entrance delay $b$ large and $q$ small. Verify that the constants for retained labels are relative to $\cos\alpha$ and that the favorable coefficient on the central Q4 subarc survives these choices.
- **§§4 and 7, norms and limits.** Check the transition from fixed-delay vertical energy to centered axis separation, in the order $q\downarrow0$, then large fixed delay, then exhaustion of Q2. Separately check the upgrade from a supremum of label norms to the label norm of a time supremum on the right and on the terminally active left. A small exceptional *measure* by itself does not control probe output.
- **§§2–3, independence from the endpoint.** The mass stop is removed using the cone and transverse budget before using the loss gap. The determinant bound is needed for a fixed interval before $t_\eta$, and the continuation horizon after it is fixed before absorbing shape errors. These sections can be reviewed as a half-response result independently of §§6–10.

## Numerical cross-check from the session [empirical]

The following rounded values use the central population model with $c=1$ at the first measured half response plus $s_*\simeq9.910670$ in normalized time. The Q4 entries are contributions to **vertical output divided by $q^2$**. Consequently a negative strong-cluster entry is favorable. “Other positive” sums positive output outside Q4. The last column uses the full probe vector, including the favorable output outside Q4.

| $q$ | $H$ | Q4 strong source | Q4 weak source | Q4 net incl. initial | Other positive | $e_q(T)$ |
|---:|---:|---:|---:|---:|---:|---:|
| 0.025 | 2.390 | −8.96 | +3.41 | −5.57 | 0.007 | −9.19 |
| 0.0125 | 3.062 | −15.33 | +4.36 | −10.99 | 0.010 | −17.61 |
| 0.00625 | 3.771 | −27.75 | +5.28 | −22.48 | 0.018 | −36.67 |

The refined runs used respectively 2,048 / 4,096, 3,072 / 8,192, and 3,072 / 16,384 label / angular grid points and normalized time step 0.045. Against the coarser comparisons with time step 0.09 the Q4 net changed by less than 0.006. The split integrates the two cluster contributions to the physical output-weight velocity, then applies each label's final exposure. These are exploratory session measurements. Three finite values cannot settle an asymptotic claim or the uniformity needed in §§6–9. The archived C2 trajectory and coherent-orbit summary provide the experiment context. [Archived C2 trajectory](https://github.com/TodManlaibaatar/Swing-by-TwoLayerReLU/blob/e095413c44bd5698b29882c19a066e998b17284f/theory_regime/results/C2/timeseries.csv) · [Coherent orbit summary](https://github.com/TodManlaibaatar/Swing-by-TwoLayerReLU/blob/e095413c44bd5698b29882c19a066e998b17284f/theory_regime/results/orbit/orbit_summary.json)
