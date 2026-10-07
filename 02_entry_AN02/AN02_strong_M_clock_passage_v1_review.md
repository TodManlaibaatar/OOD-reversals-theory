# AN02 strong M-clock passage v1 — review note

**Disposition: stop at the central tangent obstruction.** This pair does not claim the requested original-flow passage to \(M=1/2\). It proves an original-flow short-interval obstruction to the proposed uniform linear multiplier, and an exact leading-field example in which the nonlinear correction survives to half mass. No additional hypothesis is adopted.

Companion: `AN02_strong_M_clock_passage_v1.tex`. Unique label prefix: `an02smcpv1:`. The TeX is authoritative. This is a separate increment; no source, prior review, roadmap, or checkpoint is changed.

## Precise result and scope

**Theorem 2.1 — exact original initialized flow.** Keep OWPT’s fixed \(C_m\), its actual same-field reference launched at \(\beta_c=qa_q\), and fixed right-half-circle ancestry. On \([t_m,t_m+1]\), the strong mass ratio is

\[
\log\frac{M(t_m+1)}{M(t_m)}=1+O(q^2+q^\sigma).
\]

For every label in the positive-measure band \(0\le\cos\beta\le q\), both centered input and output displacements satisfy

\[
\log\frac{h_j(t_m+1,\beta)}
 {h_j(t_m,\beta)\mathcal G(M(t_m+1),M(t_m))}
\ge k e^{-dC_m}>0,\qquad j=x,y,
\]

for all sufficiently small \(q\), where \(\mathcal G\) is the requested linear mass multiplier. This follows using only PROFILE’s proved \(C^2\) scalar expansion, its two-sided cutoff law, and OWPT with terminal offset \(C_m+1\). It is a finite-\(q\), original-flow inequality, not an extrapolation of a limiting trajectory.

**Proposition 3.1 — defined leading system only.** In the exact resident donor field, an aligned same-field test characteristic above the reference has the exact equation

\[
h'=\left[-\frac{1-M}{2}+\alpha\right]h+R(h),
\qquad k_-h^2\le R(h)\le k_+h^2.
\]

For fixed \(0<h_0\le1/4\), the nonlinear logarithmic multiplier between entry and \(M=1/2\) is bounded below by \(2k_-h_0(1-e^{-1/2})>0\), uniformly as \(M_0\to0\). This field is cooperative, has exact logistic mass and no outside population, and stays in an explicitly bounded chart. It shows that cooperativity plus the centered linear rate cannot imply the proposed uniform \(e^{o(1)}\) conclusion for finite entry displacements. It is **not** a counterexample with OWPT’s full isotropic initialized donor law. No long-time original-to-atomic convergence is asserted.

**Section 4 — normalization algebra and source audit.** The actual overlap mass contains an order-one coefficient. The corrected identity is

\[
A_q=\frac{M_0}{e^{C_m}q^\sigma},\qquad
\epsilon_mM_0^d=A_q^d q^{10d-s},\qquad 0<c\le A_q\le C.
\]

The explicit exponential factors in \(C_m\) cancel. OWPT does not identify \(A_q\) with one. Under the *defined leading logistic law*, the duration to half mass is

\[
T=\sigma\log(1/q)-C_m-\log A_q+\log(1-M_0).
\]

This is not an original-flow duration theorem. In particular the order-one clock shift \(-\log A_q\) cannot be suppressed in future phase matching.

## Exact failing inequality

Let \(\mathcal A_q(t,\beta)\) denote the actual scaled receiver Jacobian, and let

\[
J_{\rm sh}(M)=
\begin{pmatrix}-(1-M)/2&\alpha\\\alpha&-(1-M)/2\end{pmatrix}.
\]

The proposed extension of OWPT’s tangent argument requires an \(o(1)\) accumulated perturbation after normalization by the scalar linear multiplier. Its direct version is

\[
\int_{t_m}^{t_{1/2}}\sup_\beta
 \|\mathcal A_q(t,\beta)-J_{\rm sh}(M(t))\|_\infty\,dt=o(1).
\tag{fails}
\]

Theorem 2.1 instead proves the lower bound \(k e^{-dC_m}\) already on \([t_m,t_m+1]\). Each row sum has a positive correction there. Reassigning the Metzler off-diagonal part while retaining the specified scalar normalization cannot remove a row-sum correction.

The reason is explicit:

\[
f_0''(x)=\frac{\rho^3}{2}\phi(\rho x)>0,
\qquad
\frac{f_q(a_q+h)}h=-d+O(q^2)+\text{a positive term of order }h.
\]

PROFILE and OWPT give \(h(t_m)\asymp e^{-dC_m}\) on the outer \(q\)-width label band. It is small for a large fixed \(C_m\), but does not tend to zero with \(q\). Its first unit of contraction contributes a fixed nonlinear logarithmic factor. An \(O(e^{-dC_m})+o_q(1)\) estimate cannot be relabeled \(o_q(1)\).

The suggestion was checked in two complementary ways, without attempting a new passage route:

1. Normalize the receiver tangent by the proposed linear rate. The row-sum defect is already nonvanishing in the exact initialized flow on a short overlap interval.
2. Check whether cooperation itself cancels that defect. The exact resident-field scalar calculation shows a strictly positive correction at the half-mass endpoint with perfect cooperation and no perturbations.

The short-interval result rules out a uniform-in-time \(e^{o(1)}\) linear transfer on the requested interval. It does **not** by itself rule out an accidental cancellation at the final endpoint in the full initialized population. No already-proved source supplies such a cancellation, and the leading example shows it is not a consequence of the advertised mechanism. The stop is at the failed central tangent budget, not a claim that all future S1 theorems are impossible.

A shrinking-core restriction, a different overlap limit with \(C_m\to\infty\), or a nonlinear, label-dependent comparison could change the statement. These are not assumptions of this increment, and no such repair is attempted.

## Audit against the requested parts

| Requested part | What is established here | What is not established |
|---|---|---|
| (a) Mass clock to \(M=1/2\) | Exact original short-interval mass ratio; leading duration algebra with the normalization coefficient retained | Original integrated logistic defect, existence/time of the half-mass hit |
| (b) Mean and guard-independent chart | Same-field reference remains the OWPT reference on the short interval; the leading test has radius \(a+1/4\) | Original chart or reference tracking through half mass |
| (c) Uniform linear shape multiplier and handoff | The central perturbative inequality fails; corrected \(q\)-power identity is exact | Requested uniform \(e^{o(1)}\) multiplier to half mass |
| (d) Relative radial weights and normalized tail | OWPT remains valid on the fixed short overlap extension | Propagation of weights, the \(3/s\) tail and cutoff through half mass |
| (e) Left-half-circle mass | On the short interval the global envelope gives its mass at most \(O(q^\sigma)=o(q)\) | Its mass or integrated \(\mu/q\) cost through half mass |

No LCRC entry or S1 half-mass contract is newly closed. The useful new conclusion is the precise obstruction and the normalization information needed when formulating a corrected step.

The source mean-mode statement also needs care in formulating (b). P’s `pa:resident` and LOC Lemma 3.1 have the **stationary leading coherent center \((a_\rho,a_\rho)\)** for every \(M\), at \(N=0\). The actual same-field reference can move due to noncoherent population forcing. A finite-\(q\) coherent equilibrium is a different object; its \(M\)-dependence is not supplied by those leading results. This audit does not reset the reference to either \(a_\rho\) or \(a_q\), and does not edit any source.

## Constants and guard independence

All constants below are inherited or defined analytically. None depends on LCRC’s residual guards \(B,M,K_Y\), or on a chart radius selected from those guards. No full-passage chart radius is produced.

| Constant | Definition/source and role |
|---|---|
| \(C_m\) | Fixed sufficiently large OWPT/PROFILE overlap offset; \(e^{-dC_m}\) is an order-one quantity in the \(q\to0\) limit, even when small |
| \(L\), \(L+1\) | PROFILE’s target chart and OWPT’s actual overlap chart; valid here only through the fixed offset \(C_m+1\) |
| \(a_\rho,\alpha,d,\omega,s\) | Previously proved analytic root and rate functions on the compact ratio box |
| \(c_P,C_P\) | PROFILE’s uniform lower/upper displacement comparison constants, which do not approach one |
| \(c_*=c_P/4\) | Lower displacement constant for the outer label band, using \(s<2\) |
| \(b>0\) | One quarter of the minimum of \(\rho^3\phi(\rho x)\) on the compact box \(\lvert x\rvert\le L+2\); curvature lower bound |
| \(k=bc_*(1-e^{-1})/4\) | An admissible positive short-interval obstruction constant, decreased if needed; independent of \(C_m\), while its factor \(e^{-dC_m}\) is retained |
| \(k_+=1/8\), \(k_->0\) | Analytic quadratic remainder bounds in the leading test; \(k_-\) is the compact minimum displayed in the TeX |
| \(1/4\), \(1/20\) | Test displacement cap and a uniform contraction rate, both proved by inward inequalities |
| \(R_{\rm test}=\sup_{\rho}a_\rho+1/4\) | Bounded chart radius for the leading example only, from its exact invariant reference and attraction; not an original half-mass radius |
| \(A_q\in[c,C]\) | Actual overlap mass normalization; contributes \(-\log A_q\) to the leading phase and \(A_q^d\) to the handoff shape |
| \(C\) in short-interval errors | Uniform constants from PROFILE’s compact \(C^2\) expansion and OWPT’s Jacobian, mass and tangent bounds; may depend on fixed \(C_m\) and \(L\) |

LOC’s existing \(C_0=4(a+3)\), \(\gamma=\alpha(1/2-\alpha)/(\alpha+1/2)\), and local mean guard are not re-proved or used to close a new passage. In particular their upper shape estimate does not turn the integral of a fixed outer width into \(o(1)\).

## Proof audit points

- **Limits:** \(q\to0\) with \(C_m\) fixed. Choosing a large constant first gives a small fixed error, not a vanishing one. No exchange of these limits occurs.
- **Finite-\(q\) expansion:** only PROFILE’s already-proved target-only \(O_{C^2}(q^2)\) expansion is used. P’s formal full-population reduction is not treated as a proved \(C^1\) finite-noise theorem.
- **Time range:** reapplying OWPT at terminal offset \(C_m+1\) is allowed because it is still fixed, with \(S=O(q^\sigma)\ll q\). The crude \(S/q\) estimate is never used after \(S\gtrsim q\).
- **Centering:** all original \(h_x,h_y\) use the actual characteristic \(\beta_c\). The exact target root is used only inside the already-proved multiplicative comparison. No additive angle error is used as a relative shape estimate.
- **Nonzero denominators:** target outer displacements stay positive by scalar uniqueness; OWPT then gives positive original displacements. The band has positive label measure for every fixed \(q\).
- **Signs:** strict Gaussian curvature gives the positive second-order term. Positivity of the leading off-diagonal entries does not force equal row sums. No finite-\(q\) Metzler property is assumed.
- **Receiver versus donor derivatives:** the Jacobian differentiates the characteristic in one fixed evolving population field, not the self-consistent population measure.
- **Mass integration:** all pointwise radial comparisons are uniform over fixed ancestry, and integration is against a fixed finite positive measure. There is no moving-mask flux.
- **Short radial rate:** the exact truncated Gaussian second moment gives \(2g=1+O_L(q^2)\). The target rate is not confused with an exact original logistic law.
- **Chart in the leading test:** at \(0<h\le1/4\), \(h'\le-h/20\) and \(h'\ge-h/2\). These prove invariance, positivity and the required integral bounds; no trajectory or sampled sign check is used.
- **Leading example scope:** massless same-field test characteristics are legitimate receivers. The coherent donor measure is not asserted to be the initialized measure. Its endpoint calculation diagnoses the route; the separate short-interval theorem supplies the original-flow obstruction.
- **Half-mass boundary:** no characteristic is continued past \(M=1/2\). The infinite scalar exponential integral in the upper bound is only an estimate of a finite-time integral.

## Source provenance

Read directly from the private repository using read-only file fetches. Git object SHAs below identify the exact source bytes. No GitHub mutation occurred. The user’s explicit authorization to read the repository supersedes H2’s older prohibition on repository access; its proof and file-preservation rules remain in force.

| Source | Git blob SHA | Use |
|---|---|---|
| [README](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/README.md) | `ff51ff81e815fd16af3480afa02f90688497a11e` | Current scope and workflow |
| [Roadmap v1.3](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/UNIFIED_ANALYTIC_THEORY_ROADMAP_v1.md) | `b9063caeabe5b0bdb277cd1d62fce606fe68cdd1` | S0 assembly, S1 step 2 route and handoff |
| [H2](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/00_roadmap/THEORY_HANDOFF_ANALYTICAL_A_B_v2.md) | `decb029fb314e96aae70e5eee68eaa969b6293ce` | Section 0 status, analytic-proof and separate-file contracts |
| [LOC](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/03_passage_AN03/AN03_local_rate_mean_tracking_v1.tex) | `eb1fa397d1f0d9b0e3aea1698b9960726e739fa8` | `inc:AN03:local:v1:field`, `localineq`, `meanineq`; scope and mean/shape distinction |
| [P](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/01_foundations/THEOREM_A_ANALYTICAL_PROGRESS.tex) | `cb458c933aa043cf0188fd11c46bf4246ffc91d8` | `pa:leading`, `pa:masslaws`, `pa:resident`, `pa:spectra`, `pa:order`; reduction caveat |
| [PROFILE](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_strong_entry_profile_and_tail_budget_v1.tex) | `3aa94adf6735ca5abcef1cfa4eb8aa1dd209fa0a` | `inc:AN02:profile:v1:root`, `entry`, `rightcircle`, `cost` (Proposition 4.1) |
| [OWPT](https://github.com/TodManlaibaatar/OOD-reversals-theory/blob/main/02_entry_AN02/AN02_overlap_window_profile_transfer_v1.tex) | `8fac13f9d36255d3e2e23cc9b2196719ec602907` | `an02owptv1:jacobian`, `tangents`, `transfer`, `tail`; all exact initialized inputs |

The listed dates follow each source’s own version header; the roadmap is dated October 7 although this increment is dated October 6. No date is a mathematical premise. The preserved local source copies were consulted for reading; current repository contents supplied the version audit.

## Stopping record

The central tangent perturbation has a proved nonvanishing lower bound. No new small-width premise is silently added, no fourth route is attempted, and no long conditional half-mass theorem is substituted. The mass normalization and mean-center observations are audits within this new pair, not consolidation edits.

No saturation tail, later strong-defect integral, Q2 entry contract, capped radial gain, bridge problem, or consolidation is started. No experiment or numerical proof premise is used. Compilation and file-integrity checks are document checks only.

Validation: the final TeX source compiled successfully in the built-in editor. All 20 labels use the requested unique prefix, and all 14 internal references resolve to labels in the document. SHA-256 comparison confirmed all 16 pre-existing workspace files remain unchanged.
