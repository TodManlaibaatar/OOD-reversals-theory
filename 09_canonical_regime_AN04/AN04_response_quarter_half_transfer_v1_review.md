# E5 continuation · quarter and half response

**Result.** Partial. The actual critical trajectory reaches either half response or a precisely quantified complementary-residual event within an additional logarithmic time after its proved small-response hit. The analysis does not decide which happens. A learned depth advantage remains unproved.

## The initialized alternative

Choose the small fixed response level and its entry constants in TBW so that the complementary residual is at most one sixteenth of the proposed cap. The complementary residual is the full data loss after subtracting the least-squares error explained by the weak response. It includes the entire strong-cluster residual, weak-cluster cross output, and weak-cluster orthogonal second-output error.

With $r_*=\lambda/800$, the trajectory reaches either $n=1/2$ or $\mathcal R=r_*^2$ by time $\tau_0+k\log(1/q)$ for every fixed $k>8/\lambda$, for sufficiently small noise. If half response comes first, both response and cluster-loss criteria hold at the quarter and half crossings. If the complementary residual exits first, its increase is exactly accounted for by the signed exchange in `an04rqtv1:paidexit`, and the weak response has made a further fixed positive increment. This is an unconditional reached alternative for the initialization. See `an04rqtv1:alternative`.

The vertical Q2 cone is verified until the first stopping event. The input second-coordinate fraction stays at least $1/\sqrt2$, permitting the receiver's weak Gaussian wrong-gate bound. Both first-component signs, both antisymmetric faces, the positive symmetric amplitude, and every corner are checked. Its squared amplitude grows faster than the global radial-mass upper bound if neither event occurs.

## The first unresolved sign

Let $g=\nabla_\Theta\mathsf m_2$ and let $N$ be the remainder of the true parameter update after removing the measured weak residual mode. The exact equations are
\[
 n'=Q(1-n)\|g\|^2/2+\Gamma,\qquad
 \mathcal R'=-4\|N\|^2-2Q(1-n)\Gamma,\qquad
 \Gamma=\langle g,N\rangle .
\]
At the residual boundary the nonoutward condition is
\[
 \Gamma\ge-\frac{2\|N\|^2}{Q(1-n)}.
\]
The true initialized sign on that face is unknown. Its two Gaussian kernel terms are written explicitly in `an04rqtv1:coupling`. Neither weak regression orthogonality nor positivity of the kernel removes the selected mixed correlation.

Restarting the loss inequality at small successive response increments gives the same identity by telescoping. It would require the actual dissipation to pay the released weak-regression error at every intermediate time. Cauchy–Schwarz bounds do not establish that payment. See `an04rqtv1:face` and `an04rqtv1:reset`. This is an unpaid sufficient barrier test; no claim is made that the actual trajectory violates it.

## The second unresolved sign

After projecting the two probe gradients onto $g$, the longitudinal and transverse motion each split into a response-associated term and $\langle h_i,N\rangle$ with $h_i\perp g$. The first barrier would control the component of $N$ parallel to $g$. It does not determine these perpendicular components, which retain all current gates and both training sources. Their exact learned-depth test is `an04rqtv1:depth`.

Consequently even a proof that the half-hit alternative holds would not yet prove the learned swing-by depth. The probe value at the moving small hit is also not given by the fixed-time pre-weak theorem. Reaching individual response thresholds, reaching the benchmark learned window, and retaining the probe advantage are distinct obligations.

**Checks and scope.** All equations use the critical trained trajectory. The small response level is fixed before noise. The alternative uses an exact measured response and full cluster losses. The analysis uses no substituted initialization, learned-chart assumption, generated trajectory, or empirical premise. No earlier increment is edited.
