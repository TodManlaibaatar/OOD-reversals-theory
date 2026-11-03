# Channel and producer decomposition, version 1

**Scope.** Original balanced untied flow with isotropic initialization \(S_0=q^{10}\), small positive \(q\), on WIT's fixed \(\mathcal P_*\times J\). Time is \(s=\mu_1^2t_{\rm phys}-\tau_h\) with RTA's center. The formulas use normalized rates. Multiply by \(\mu_1^2\) for physical rates.

**Result.** The original six channel limits, their fixed-label producer coefficients, the signed exact lag and the help formula close on all of \(J\). The sign of the selected weak producer's input term \(W_{\rm in}\) closes on \(J\cap(-\infty,0]\). Its sign on \(J\cap(0,\infty)\) remains open. The stop is at the sign extension in Step 6 of the requested order.

| Requested step | Status | Evidence or remaining inequality |
|---|---|---|
| Inventory | Closed | Section 1 distinguishes the exact source matrices, motion and projection identities from the leading characteristic system. |
| Channel limits | Closed | The non-core rate costs \(Cq^2\epsilon_{\rm bg}\). Both source-1 input and radial totals are \(O(q^{2+1/20})\). BC supplies the two distinct source-2 rotations. |
| Producer identities and limits | Closed | Fix the full probe residual and split only the training residual. Theorem 1 gives every core channel's target, core and selected coefficients. Both other producer groups have zero limit with explicit bounds. |
| Signed exact lag | Closed | Core and selected regression moments give \(Y+nK(U)\). WIT's signed help margin gives \(c_L=5p_*/[4(7/4+R)]>0\). |
| Exposure and exact lag | Closed | Use the actual core integral. Its positive lower bound makes the error smaller than the signed margin. P's \(B_0\) agrees to the same precision. |
| Harm signs | Partial | Both output signs are strict on all of \(J\). The target-plus-core input limit is nonpositive. For the weak input sign, \(V>Y\) holds globally but the proved \(X>Y\) range is \(s\le0\). |
| B-core and handoff | Partial | The original-flow identity below and its stated signs hold. The stronger all-window weak input sign remains unmatched. |

## Original-flow mechanism at the proved accuracy

Write \(A_*=\zeta-X\), \(Z=X-Y\), and \(\Phi_x=\Phi(\rho X)\) for the selected comparator. On the whole rectangle and window, putting \(\mathcal A_q=\int_K(\zeta-x)\,d\mu\) and \(\mathcal L_q=r_{21}/q\),
\[
\begin{aligned}
\mathcal L_q&=Y+nK(U)+O(q^{1/20}),\\
q^{-2}D_1^\tau&=-\mathcal A_q\mathcal L_q/2+O(q^{1/20}),\\
q^{-2}D_2^\tau&=T_{\rm in}+W_{\rm in}+T_{\rm out}+W_{\rm out}
                 +O(q^{1/20}).
\end{aligned}
\]
Here
\[
T_{\rm in}=-\lambda Z^2\Phi_x/2,\quad
W_{\rm in}=\lambda n Z(V-Y)\Phi_x/2,\quad
T_{\rm out}=\rho A_*K(\rho X)/2,\quad
W_{\rm out}=-nT_{\rm out}.
\]
The first term groups target and core only after their rate-weighted integrals have been computed separately. Each error is uniform. Hence the sum of the two source formulas gives the original total on both ordered subwindows. RTA supplies the negative and positive margins there. The four-part identity and these margins determine the changing balance in the sum. They do not assign the crossover to one factor.

**Correction for H2 §3.3 item 3.** Cluster 2 drives input and output rotation of the active strong carrier. Target and core jointly contribute \(-\lambda Z^2\Phi_x/2\) to input rotation. Selected weak output contributes \(\lambda nZ(V-Y)\Phi_x/2\) through both its first output and its second-coordinate response. Target output rotation is positive and weak response subtracts its fraction \(n\), leaving BC's positive \((1-n)T_{\rm out}\). These are leading-order contributions in the initialized regime. Both \(T_{\rm out}\) and, where its sign closes, \(W_{\rm in}\) are on the positive side of the balance. The inequalities prove positivity for their total after the opposing terms are included. They do not establish individual dominance.

## Audit points

- P uses the unhalved \(R_p\), so both angular velocities include \(1/2\) and \(h_p=2g_p=b^TR_pa\). Every producer enters with the training-residual sign \(+X_{\rm data}\) or \(-f_j\).
- All receiver weights are evaluated at the exact state, including \(c=e_\xi\cdot b\) and \(d=-e_\xi\cdot b^\perp\). Fixed-label producer linearity applies to the matrix with those weights held fixed. The core gap covers every endpoint label. RTA's selector and almost-everywhere conventions apply to possible background hits.
- The comparison of a donor cohort with its atom costs \(Cq^{1+1/20}\) in unscaled \(L^2(P_p)\). The factor \(q\) comes from unit-vector geometry and the first-moment distance. Retaining its **actual mass** in this comparison avoids dividing a mass error by \(q\). The Gaussian calculations still depend on the individual receiver. Atom coefficients in the final table follow only after integration and the uniform receiver comparison.
- On source 1, target and core normalized radial contributions are \(-A_*Z\) and \(+A_*Z\), while their input contributions are \(-ZX/2\) and \(+ZX/2\). Cancellation occurs in the totals. The output producer limits are \(-A_*Y/2\) (target), zero (core) and \(-A_*nK(U)/2\) (selected weak). In contrast, **the lag** has regression contributions \(Y\) from the core and \(nK(U)\) from the selected weak. A lag contributor and a moving-channel producer are distinct indices.
- FWC outputenergy gives the omitted weak cross-component charges \(O(q^{1/8}+q^{\gamma_*/2})\); outside costs \(O(q^{1/10})\) after scaling, with \(\gamma_*=289169/924000\). The actual non-core probe-rate bound uses \(\epsilon_{\rm bg}=q^8+(1+\log(1/q))^2q^{\gamma_*}\) and the background output/derivative estimates. No probe-scale budget is inferred from raw weak mass alone.
- The lag compares directly with actual weighted regression. The selected weak moment error \(O(q^{2-p})\), \(p=603/640\), uses its bounded second moment and reached growing chart. P's conditional tracking equation is unnecessary. The lag lower bound follows from **signed** WIT \(d_{1,*}\) and \(A_*>0\). We use \(A_*\le7/4+R\) because \(X\ge0\) on all of \(J\) was not established.
- The \(1-M\) reaction is included in the source-1 remainder after summation. With \(\mathcal A_q\ge g_*/16\), the help error can be made at most \(g_*c_L/64\). The \(B_0\) comparison retains the full-probe cost \(O(q^2+q\epsilon_{\rm bg})\).

## Sign extension and exact stopping inequality

P's selected-branch invariants give \(V>Y\) at every finite time. WIT's half-learning region gives \(X>Y\) for \(s\le0\). At a possible first equality \(X=Y\) after half mass, set \(T=Y+nK(U)-\rho(1-n)K(\rho X)\). The direct boundary argument needs
\[
T>-\lambda n(V-Y)\Phi(\rho Y)
\]
there. The exact derivative \(2(X-Y)'=\lambda n(V-Y)\Phi(\rho Y)+T\) at the equality fixes the coefficient and sign. WIT's inward estimate on \(T\) uses \(n\le1/2\). Its definition of the common window supplies no \(s_*+r\le0\) restriction either. The missing inequality is an unresolved comparison, **not a demonstrated counterexample**. Strict limiting signs transfer uniformly on compact subsets with a positive margin. The nonpositive square by itself gives no strict finite-noise sign at a zero.

## Sources, constants and handoff

The exact source is P's motion/projection/factorization/producer bookkeeping. P's leading equations and atomicrates identify the comparator only. FWC charges, charts, distbound, massfine and background, RTA coregap/corerate/backgroundrate and BC obstructiontheorem/twoway apply to the initialized family on the matched window. WIT uniformtheorem, regiontheorem and P limitreversal supply the stated leading margins and invariant domains. Roadmap v1.28 and H2 §3.3 specify the requested consumer.

Keep the original WPT/RB–WCS order, the WIT witnesses, and RTA/FWC's fixed continuation window and radius first. Fix \(c_L\), the first-moment, Gaussian and channel error constants next. Take \(q\) small enough for all source thresholds, the exact-lag comparison error below \(c_L/2\), and the help error below \(g_*c_L/64\). No new hypothesis enters the closed results.

For S7/S8, the canonical and bridge regimes require their own initialized state control and producer errors smaller than the **actual signed lag cancellation**. The constants proved here apply on \(S_0=q^{10}\) and WIT's learned rectangle.

## Source checks

The TeX compiles with resolved references. Both requested patterns returned zero matches with PCRE2 and an independent text scan. The local grep lacks the -P option. All four required TeX commands survived. The new labels use the checked prefix an01cpdv1:. The ZIP members were checked byte for byte against the two source files.
