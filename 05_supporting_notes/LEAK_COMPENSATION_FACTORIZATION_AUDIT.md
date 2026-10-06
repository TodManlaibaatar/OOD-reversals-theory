# Leak–compensation factorization: exact identities and numerical audit

## Status and provenance

This note derives static identities from the balanced two-layer ReLU population flow and audits the user-supplied CSV outputs. It does **not** certify initialized reachability, continuous-time sign intervals, a parameter neighborhood, or a continuum quadrature error. No new training trajectory was integrated. No repository commit was made.

Primary numerical source: `residuals_-85.csv`, 17 snapshots at physical times 2, 2.25, ..., 6. Supporting source: `counterfactual_-85.csv`. The ratios and bounds below refer to this single canonical trajectory and these snapshots.

The repository script retrieved during this review is an older version without the residuals subcommand. The uploaded original/reviewed scripts also do not contain the latest factorization implementation. This note verifies the exported formulas algebraically and numerically from the CSV; it does not claim to have inspected the latest merged implementation.

## 1. Fixed notation and units

Use normalized data
\[
P_1=\mathcal N(e_1,q^2I_2),\qquad
P_2=\mathcal N(\rho e_2,q^2I_2),
\]
and equal cluster weights. All expectations below use these normalized laws. The residual is \(e(x)=x-f(x)\). The output at a unit probe is unchanged by input normalization.

All rates in this note are **physical** rates. Thus set
\[
k_0=\mu_1^2/2.
\]
The factor combines the conversion from normalized time and the cluster mixture weight; it must not be applied twice.

The balanced angular measure is squared-radius weighted:
\[
f(x)=\int b(a^\top x)_+\,d\nu,\qquad
a=(\cos\theta,\sin\theta),\quad b=(\cos\psi,\sin\psi).
\]
Write \(a^\perp=(-a_2,a_1)\), \(b^\perp=(-b_2,b_1)\).

At a fixed time let \(C\) be the probe-active strong core, with \(M=\nu(C)>0\), and define
\[
\langle v\rangle_C=M^{-1}\int_C v\,d\nu,\qquad
\bar v=\langle v\rangle_C.
\]
These are instantaneous state identities and allow a state-dependent core. Differentiating core observables in time requires separately accounting for membership changes, or using fixed labels.

For \(\xi\) and \(e_\xi=\xi-f(\xi)\), put
\[
z=a^\top\xi>0,\quad
v=-(a^\perp)^\top\xi,\quad
d=-e_\xi^\top b^\perp,\quad
c=e_\xi^\top b.
\]
Keep \(v,d\) signed in general. On the intended sector, positivity of \(v,d\) makes them equal to the absolute-value factors used by the CSV. Their signs must be established wherever the factorization is used in a theorem. Do not assume \(c>0\) pointwise merely because its average is positive.

## 2. Exact source-by-motion identities

Let
\[
R_p(\theta)=\mathbb E_{P_p}
[e(X)X^\top 1_{\{a^\top X>0\}}],
\quad G_1(\theta)=R_1(\theta)a,\quad
T_2(\theta)=R_2(\theta)a^\perp.
\]
Define
\[
\Lambda_1=-b^\perp{}^\top G_1,\qquad
j=b_1T_{2,1},\qquad j_2=b_2T_{2,2}.
\]
The physical cluster-sourced angular velocities are
\[
(\dot\psi)_1=-k_0\Lambda_1,\qquad
(\dot\theta)_2=k_0(j+j_2).
\]

The exact help and input-rotation terms are
\[
B=k_0M\langle zd\Lambda_1\rangle_C,
\]
\[
H_1=k_0M\langle vcj\rangle_C,\qquad
H_2=k_0M\langle vcj_2\rangle_C,\qquad H=H_1+H_2.
\]
Here \(B\) is minus the core's cluster-1 output-rotation rate, while \(H\) is the core's cluster-2 input-rotation rate. With all omitted motion components and labels retained in \(r_1,r_2\),
\[
D_1=-B+r_1,\qquad D_2=H_1+H_2+r_2.
\]

**Proof.** The core output is an integral of \(b(a^\top\xi)_+\). Output-angle motion contributes \(z b^\perp(\dot\psi)_1\); input-angle motion contributes \(b(a^\perp{}^\top\xi)(\dot\theta)_2\). Contract with \(-e_\xi\), insert the displayed velocities, and integrate. The mass-growth terms and all other contributions define the explicit residual rates \(r_1,r_2\). No differentiation of a group matrix or assumption of a coherent block is used.

## 3. Exact help factorization and its error

Set
\[
Q_1=1+q^2,\qquad
r_{21}=\frac{\mathbb E_{P_1}[X_1(f_2(X)-X_2)]}{Q_1},
\]
so \(\mathbb E_{P_1}[e_2(X)X_1]=-Q_1r_{21}\).

Define the predictor
\[
B_0=k_0M Q_1\bar z\,\bar d\,r_{21}.
\]
Then
\[
B=B_0+\epsilon_B,
\]
with the exact correction
\[
\boxed{
\frac{\epsilon_B}{k_0M}
=Q_1r_{21}\operatorname{Cov}_C(z,d)
+\langle zd(\Lambda_1-Q_1r_{21})\rangle_C.
}
\]
Consequently
\[
|\epsilon_B|\le k_0M\left[
Q_1|r_{21}|\sigma_C(z)\sigma_C(d)
+\langle |zd|\,|\Lambda_1-Q_1r_{21}|\rangle_C
\right].
\]

**Proof.** Add and subtract \(Q_1r_{21}\langle zd\rangle_C\), then use the covariance identity and Cauchy–Schwarz.

### Why the correction is not only within-core spread

Let
\[
R^{\rm full}_{1,22}=\mathbb E_{P_1}[e_2(X)X_2],
\quad
\tau_1(\theta)=\mathbb E_{P_1}[e_2(X)(-a^\top X)_+].
\]
Since \((a^\top X)_+=a_1X_1+a_2X_2+(-a^\top X)_+\),
\[
G_{1,2}=-a_1Q_1r_{21}+a_2R^{\rm full}_{1,22}+\tau_1(\theta).
\]
Thus
\[
\boxed{
\Lambda_1-Q_1r_{21}
=Q_1r_{21}(a_1b_1-1)
-b_1a_2R^{\rm full}_{1,22}
-b_1\tau_1(\theta)
+b_2G_{1,1}(\theta).
}
\]
This retains finite mean tilt, the second-coordinate residual on cluster 1, the wrong-gate tail, and the first-coordinate residual. The observed small aggregate error does not prove that every term is separately small or that cancellations are absent.

For \(a_1>0\), a useful tail bound is
\[
|\tau_1(\theta)|
\le \|e_2\|_{L^2(P_1)}
\left[(a_1^2+q^2)\Phi(-a_1/q)-a_1q\phi(a_1/q)\right]^{1/2}.
\]
This is Cauchy–Schwarz and the negative-part second moment of
\(a^\top X\sim\mathcal N(a_1,q^2)\). Evaluating the difference numerically requires stable tail arithmetic. Replacing the bracket by
\((a_1^2+q^2)\Phi(-a_1/q)\) gives a conservative nonnegative upper bound.

## 4. Exact first-coordinate harm factorization

Define
\[
H_{1,0}=k_0M\,\bar v\,\bar c\,\bar j,\qquad
\bar j=\langle b_1T_{2,1}\rangle_C.
\]
Then
\[
H_1=H_{1,0}+\epsilon_H
\]
with
\[
\boxed{
\frac{\epsilon_H}{k_0M}
=\operatorname{Cov}_C(vc,j)
+\bar j\,\operatorname{Cov}_C(v,c).
}
\]
In particular
\[
|\epsilon_H|
\le k_0M\left[
\sigma_C(vc)\sigma_C(j)
+|\bar j|\sigma_C(v)\sigma_C(c)
\right].
\]

**Proof.** Expand
\(\langle vcj\rangle=\langle vc\rangle\bar j+\operatorname{Cov}(vc,j)\)
and \(\langle vc\rangle=\bar v\bar c+\operatorname{Cov}(v,c)\).

This identity does not divide by \(T_{2,1}\) or its average. It remains valid when that average crosses zero, which is why absolute errors are the right proof quantities near the early sign change.

Retain \(\langle b_1T_{2,1}\rangle_C\), rather than silently replacing it by
\(\langle T_{2,1}\rangle_C\). A positive lower bound on \(b_1\) justifies the optional \(\chi=-b_2/b_1\) notation, but does not make \(b_1=1\).

## 5. A scalar rate balance with a complete remainder

Define the new statistic
\[
\boxed{
\mathfrak G_{\rm LC}
=\bar v\,\bar c\,\langle b_1T_{2,1}\rangle_C
-Q_1\bar z\,\bar d\,r_{21}.
}
\]
Then
\[
\boxed{
\dot E_\xi=k_0M\mathfrak G_{\rm LC}+\mathcal R,
\qquad
\mathcal R=\epsilon_H-\epsilon_B+H_2+r_1+r_2.
}
\]

The common factor \(k_0M>0\) cancels from the *leading* balance. That does not imply that changing mass or initialization leaves the state or reversal time unchanged.

A sufficient absolute error budget is
\[
|\mathcal R|\le
|\epsilon_H|+|\epsilon_B|+|H_2|+|r_1|+|r_2|.
\]
If the leading negative or positive rate exceeds this budget on suitable intervals, its sign transfers to the true derivative.

Individual cluster signs require their own inequalities:
\[
B_0>|\epsilon_B|+|r_1|,
\quad
H_{1,0}>|\epsilon_H|+|H_2|+|r_2|.
\]

This is not yet an initialized theorem. Reaching a region where these bounds hold and proving them uniformly in time/probe/parameters remain necessary. No equality with the older archived timing statistic \(G\) has been established.

## 6. Residual-producer decomposition of the harm

For a partition of the whole population into output-producing groups \(g\), write
\(f=\sum_g f^g\). Define
\[
T_{2,1}^{\rm tar}(\theta)
=\mathbb E_{P_2}[X_1(a^\perp{}^\top X)1_{\{a^\top X>0\}}],
\]
\[
T_{2,1}^{g}(\theta)
=-\mathbb E_{P_2}[f_1^g(X)(a^\perp{}^\top X)1_{\{a^\top X>0\}}].
\]
Exactly,
\[
T_{2,1}=T_{2,1}^{\rm tar}+\sum_gT_{2,1}^g.
\]
Equivalently, with the Gaussian feature kernel \(C_2\),
\[
T_{2,1}^g(\theta)
=-\int_g b'_1\partial_\theta C_2(\theta,\theta')\,d\nu'.
\]
The rate-level attribution is
\[
H_1^g=k_0M\langle vc\,b_1T_{2,1}^g(\theta)\rangle_C,
\quad
H_1=H_1^{\rm tar}+\sum_gH_1^g.
\]

The CSV's `T21_*` columns evaluate the residual decomposition at the core's **mean input angle**. They do not yet contain these integrated rate-level producer terms. The distinction matters: averaging \(T_{2,1}(\theta)\) and evaluating it at the average angle are different operations.

A positive gate-weighted residual moment does not, by itself, imply a pointwise positive residual on the whole selected training region. The signed test function also matters.

## 7. Numerical audit of supplied snapshots

Calculated directly from the uploaded `residuals_-85.csv`:

- 17 snapshots, physical times 2 through 6.
- Maximum leakage-identity residual: \(5.1174\times10^{-17}\).
- \(B/B_0\) range: 0.986979 to 1.015298 on all 17 snapshots.
- \(H_1/H_{1,0}\) range: 0.945552 to 1.051954 on snapshots from 3.25 through 6.
- Minimum `core_min_b1`: 0.533442.
- Recomputed predictor products match the exported values to below \(10^{-16}\) absolute.
- `T21_target + T21_minus_core + T21_minus_bridge + T21_minus_weak + T21_minus_other` matches `T21_at_core_mean` to about \(2.2\times10^{-16}\).

These are internal arithmetic and sampled-state checks, not continuum certification.

### Cancellation-free sampled rate budgets

Each budget below is the sum of the five absolute remainder terms, not just the absolute value of their sum.

| Physical time | \(H_{1,0}-B_0\) | Recorded \(D_1+D_2\) | Sum of absolute remainders | Leading margin after budget |
|---:|---:|---:|---:|---:|
| 3.25 | -2.52678516e-03 | -2.71852038e-03 | 6.50654445e-04 | 1.87613072e-03 |
| 3.50 | -5.90227326e-04 | -7.92760723e-04 | 3.05447501e-04 | 2.84779825e-04 |
| 3.75 | +4.41224997e-04 | +2.48807524e-04 | 1.92417473e-04 | 2.48807524e-04 |
| 4.00 | +1.01301609e-03 | +8.41018818e-04 | 2.12223671e-04 | 8.00792416e-04 |
| 4.25 | +1.36417618e-03 | +1.21736208e-03 | 2.24264776e-04 | 1.13991140e-03 |

At the sampled times 3.5 and 4.0, the leading balance exceeds the cancellation-free remainder budget on opposite sides. This supplies useful *targets* for a uniform certificate. It does not prove the same inequalities between samples, in a tube, or at nearby parameters.

Linear interpolation on the same 0.25-spaced snapshot grid gives:
\[
t_{\rm leading}\simeq3.643057,\qquad
t_{\rm recorded\ total}\simeq3.690281.
\]
The fine-trace reference crossing reported by the run is 3.675245. Do not compare these as though all three had identical time resolution. Nor does a leading-statistic zero imply a unique true-rate zero.

### A correction supplied by the new counterfactual residual columns

At physical time 3.75, the normalized cluster-1 coordinate losses are:

| Statistic | Actual state | Full three-block state |
|---|---:|---:|
| \(\frac12\mathbb E_{P_1}(f_1-X_1)^2\) | \(8.35368\times10^{-7}\) | \(1.39398\times10^{-4}\) |
| \(\frac12\mathbb E_{P_1}(f_2-X_2)^2\) | \(1.81456\times10^{-4}\) | \(4.24829\times10^{-5}\) |
| \(r_{21}\) | 0.002917704 | 0.004728748 |
| \(\mathbb E[X_2f_2]/q^2\) | 0.703052 | 0.938431 |

Thus the earlier suggestion that this collapse worsens the second-coordinate fit on cluster 1 is not supported at this snapshot: that coordinate loss improves while the first-coordinate loss increases about 167-fold. Total cluster-1 loss is nearly unchanged. The residual is redistributed; this table does not isolate which changed term is solely responsible for the counterfactual rate.

The weak-family residual-producer term at the mean core angle is decisive in the reported sign ledger. At 3.75:
\[
T_{2,1}(\bar\theta)
=(-0.001296386)+(0.006344093)=0.005047707,
\]
where the first parenthesis includes the target, core, bridge and other terms, and the second is the weak output term. But the core mean \(\langle T_{2,1}\rangle_C=0.004389837\) is different, and the signed rate needs the full carrier-weighted donor decomposition in Section 6.

## 8. Proof priorities

1. Use the exact \(B,H_1,H_2,r_1,r_2\) formulas on an initialized reachable tube near the learned crossing window.
2. Bound the help reduction defect \(\Lambda_1-Q_1r_{21}\), including residual-coordinate and gate terms, not only angular covariance.
3. Bound the harm factorization error and the rate-weighted weak-family residual contribution.
4. Establish the opposing leading margins on nonzero time intervals, together with the individual cluster signs and substantial concept learning.
5. Treat parameter robustness and finite-horizon persistence as explicit subsequent obligations.

The positive sampled `core_min_b1` is useful evidence for a tube guard, not a continuous-time lower-bound theorem. The formulas above avoid division by \(b_1\) entirely.

The new scalar balance is a mechanism-based timing coordinate. Its state variables remain functionals of the full population, and it is not yet an autonomous reduced ODE.

## File integrity

- `residuals_-85.csv` SHA-256: `df841f65cc006cf7aefcf9eef0d2e73f7c081f796251986816713fce51f671ff`
- `counterfactual_-85.csv` SHA-256: `c6b76474e2e72cb6bf8c73a64b7333bcf0dc714d934131e849f05deec68dae24`
- `ledger_-85.csv` SHA-256: `a4da7ce21c497e2106f8aaa53038d91fcccd3c8375f0e8cc5cf8aa648817e2b6`
- `p12_integrals.csv` SHA-256: `79dc11b315dc5446edfc89d5b3cd7f75e55631518c849710a2062e4e86e6e236`
- `p12_rates.csv` SHA-256: `537b1db5ba51413fa1f5598dbb25365729fb564532a1d43391a8d253b00f5721`
- `sweep_ledger.csv` SHA-256: `2188513e7f3121ed5ffd2e7a12fa57f6e6eea4135f6fe68bd1b21f94ba781fb1`
