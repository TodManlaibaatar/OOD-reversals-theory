# SIM: Reference to the Original Swing-by Paper

## Source and scope

**Paper:** *Swing-by Dynamics in Concept Learning and Compositional Generalization*  
**Authors:** Yongyi Yang, Core Francisco Park, Ekdeep Singh Lubana, Maya Okawa, Wei Hu, and Hidenori Tanaka.  
**Publication:** ICLR 2025.  
**Version reviewed:** arXiv:2410.08309v2, dated March 13, 2025.  
**Source file:** `2410.08309v2.pdf`, 32 pages.  
**Purpose:** A standalone research reference to the original paper's setting, terminology, equations, theoretical assumptions, lemma structure, experiments, and stated limitations.

All page numbers below refer to the printed pages of this PDF, which coincide with its PDF page numbers. References such as “§4.2, Eq. (4.3)” refer to the original paper, not to sections of this file.

This document summarizes the supplied paper. It does **not** incorporate results from the later two-layer ReLU project, its repository, research notebooks, proposed population theorems, or subsequent literature. Mathematical statements from Appendix D are recorded as the paper's stated results; this reference is not an independent certification of every proof. Important scope and transcription issues are explicitly identified rather than silently repaired.

---

## Contents

1. [Central question and contributions](#1-central-question-and-contributions)
2. [Notation and model distinctions](#2-notation-and-model-distinctions)
3. [The Structured Identity Mapping task](#3-the-structured-identity-mapping-task)
4. [Empirical phenomena in SIM](#4-empirical-phenomena-in-sim)
5. [Linear loss reduction and the data matrix](#5-linear-loss-reduction-and-the-data-matrix)
6. [One-layer linear theory](#6-one-layer-linear-theory)
7. [Symmetric two-layer linear dynamics](#7-symmetric-two-layer-linear-dynamics)
8. [The original Swing-by mechanism](#8-the-original-swing-by-mechanism)
9. [Appendix D assumptions](#9-appendix-d-assumptions)
10. [Appendix D lemma stack and proof strategy](#10-appendix-d-lemma-stack-and-proof-strategy)
11. [Initialization, dimension, multiple descents, and failure modes](#11-initialization-dimension-multiple-descents-and-failure-modes)
12. [SIM experimental protocols and controls](#12-sim-experimental-protocols-and-controls)
13. [Diffusion-model validation](#13-diffusion-model-validation)
14. [Scope of the original ReLU results and future directions](#14-scope-of-the-original-relu-results-and-future-directions)
15. [Source-reading cautions for mathematical reuse](#15-source-reading-cautions-for-mathematical-reuse)
16. [Figure and appendix lookup guide](#16-figure-and-appendix-lookup-guide)
17. [Related-work pointers and bibliographic record](#17-related-work-pointers-and-bibliographic-record)
18. [Essential facts to preserve in a follow-up](#18-essential-facts-to-preserve-in-a-follow-up)

---

## 1. Central question and contributions

### 1.1 Why introduce SIM?

The paper seeks a tractable explanation of compositional learning dynamics previously observed in diffusion models. In the motivating experiments, a conditioning input specifies primitive concepts, a model generates an image, and a classifier maps the image back to a vector of concept values. An ideal generator followed by an ideal concept classifier would implement the identity map in this concept space.

SIM abstracts that construction into supervised identity regression on a structured Gaussian mixture. The important feature is the organization of training concepts and held-out compositions, rather than the semantic identity of concepts such as color, shape, or size.

**Source:** Abstract and §1, pp. 1–3; Fig. 1, p. 2.

### 1.2 Main contributions and their evidence

| Contribution | Content | Evidence in the paper |
|---|---|---|
| A tractable concept-space task | Gaussian clusters arranged along concept coordinates; identity targets; held-out compositions | Formal SIM definition, §2.1 |
| Reproduction of earlier phenomenology | Concept-learning order, signal/diversity dependence, terminal slowing, and hierarchical generalization | MLP experiments, §3 and Appendices B/F |
| A simple explanation of learning rates | The coordinate rate depends on both mean strength and variance | One-layer analytical solution, Theorem 4.1 |
| A mechanism for transient OOD deterioration | Growth and later suppression of off-diagonal responses can temporarily undo apparent generalization | Symmetric two-layer linear analysis, §4.2 and Appendix D |
| Predictions beyond a single descent | Repeated growth/suppression stages can produce multiple test-loss descents | Selected symmetric-model examples, Appendix E.1 |
| Connection back to generative models | Analogous trajectory bends, non-monotonic concept-space error, and slowing | Conditional diffusion experiments, §5 and Appendix G |

The paper's theoretical centerpiece is the **symmetric two-layer linear model**, not a rigorous two-layer ReLU analysis. ReLU models are included empirically, and their theoretical treatment is identified as future work.

**Source:** Contribution summary, p. 3; §§4–5, pp. 5–10; Appendix E.4, p. 27.

---

## 2. Notation and model distinctions

The following notation follows the paper, with $e_p$ used for the standard basis vector that the paper denotes by $\mathbf 1_p$.

| Symbol | Meaning |
|---|---|
| $d$ | Ambient input and output dimension |
| $s\le d$ | Number of nonzero-mean concept clusters / informative concept directions |
| $n$ | Samples per concept cluster; the basic training set has $sn$ samples |
| $p\in[s]$ | Concept-cluster index |
| $\mu_p\ge0$ | Distance of cluster $p$'s center from the origin; concept signal strength |
| $\sigma_j$ | Noise standard deviation along coordinate $j$, shared across clusters |
| $\Sigma=\operatorname{diag}(\sigma)^2$ | Common covariance of each Gaussian cluster |
| $x_k^{(p)}$ | Sample $k$ from cluster $p$ |
| $\widehat x$ | Principal OOD probe, the sum of concept-cluster means |
| $\theta$ | General trainable parameter vector |
| $W_\theta$ | Input-output Jacobian / effective matrix of a linear model |
| $A$ | Empirical or population uncentered second-moment matrix used in the loss |
| $a_p$ | Diagonal entry of population $A$ |
| $U\in\mathbb R^{d\times d'}$ | Trainable factor in the symmetric two-layer linear model |
| $d'\ge d$ | Width / factor dimension in that model; distinct from $d$ |
| $W=UU^\top$ | Symmetric positive-semidefinite effective matrix |
| $G_{ij},S_{ij},N_{ij}$ | Growth, suppression, and interaction (“noise”) terms in the entry dynamics |
| $\eta$ | Discrete step size in Appendix D |
| $\omega$ | Scale of entries of the initial effective matrix in Appendix D |
| $\alpha,\gamma,\beta,P,K,\kappa,C$ | Constants in the Appendix D assumptions |

**Important distinctions.** $s$ is the number of concepts, not initialization mass. $d$ and $d'$ are different dimensions. $W=UU^\top$ is an effective linear map, not the second-layer matrix of a general untied network. $\sigma_j$ is coordinate-indexed, not a separate isotropic standard deviation assigned only to cluster $j$.

**Source:** §2, pp. 3–4; §4, pp. 6–8; Appendix D.1, p. 19.

---

## 3. The Structured Identity Mapping task

### 3.1 Training distributions

There are $s$ concept clusters in $\mathbb R^d$, with $s\le d$. For each $p\in[s]$,

$$
x_k^{(p)}\overset{\mathrm{iid}}{\sim}
P_p=\mathcal N(\mu_p e_p,\Sigma),
\qquad k=1,\ldots,n,
$$

where

$$
\Sigma
=\operatorname{diag}(\sigma_1^2,\ldots,\sigma_s^2,0,\ldots,0).
$$

The basic dataset is

$$
\mathcal D=\bigcup_{p=1}^s\{x_k^{(p)}:k\in[n]\}.
$$

Every cluster has the same covariance matrix. The first $s$ coordinates are informative; the remaining coordinates are called non-informative. In the coordinate-aligned formulation, the training samples have zero components in the non-informative directions.

The paper also allows an **optional additional cluster centered at the origin**. Its principal displayed loss and population formula are written for the $s$ specified concept clusters. The source does not give one universal revised weighting formula covering every use of the optional cluster; its inclusion should therefore be stated separately in any adopted model.

**Source:** §2.1, pp. 3–4.

### 3.2 Identity-regression objective

The target for every sample is itself:

$$
y_k^{(p)}=x_k^{(p)}.
$$

The intended cluster-indexed empirical objective in Eq. (2.1) is

$$
\mathcal L(\theta)
=
\frac{1}{2sn}
\sum_{p=1}^s\sum_{k=1}^n
\left\|f(\theta;x_k^{(p)})-x_k^{(p)}\right\|_2^2.
$$

The displayed Eq. (2.1) prints superscript $(s)$ inside the summand despite summing over $p$; the expression above uses the sample index consistent with the dataset definition and Appendix C.1. This is a notation clarification, not a change of task.

For the equally weighted mixture of the $s$ concept clusters,

$$
P=\frac1s\sum_{p=1}^s P_p,
$$

the corresponding population objective is

$$
\mathcal L_{\mathrm{pop}}(\theta)
=
\frac12\mathbb E_{X\sim P}\|f(\theta;X)-X\|_2^2.
$$

**Source:** Eq. (2.1), p. 4; Appendix C.1, pp. 17–18.

### 3.3 Principal compositional evaluation point

The main test composition is

$$
\widehat x=\sum_{p=1}^s\mu_p e_p.
$$

The paper motivates this through a Gaussian test cluster centered at the combined concept means. With sufficiently small test variance, its expected loss is approximated by the loss at its center, so the analysis and trajectory plots focus on the single point $\widehat x$.

The **output trajectory** is

$$
t\longmapsto f(\theta(t);\widehat x).
$$

It is an output-space trajectory at a fixed test input, not the trajectory of a neuron or a training sample.

The principal test point is a nonnegative combination of concept directions. A sweep over negative-coordinate or off-cone probes is not part of the paper's main evaluation definition.

**Source:** §2.1–§3, p. 4.

### 3.4 Hierarchy of compositions

Appendix B considers all binary combinations. For $v\in\{0,1\}^s$,

$$
\widehat x^{(v)}=\sum_{p=1}^s v_p\mu_p e_p.
$$

If $v$ has one nonzero entry, this is a training-cluster center. The all-ones vector gives the principal compositional probe. The zero vector gives the origin.

The indices carry the componentwise partial order

$$
u\preceq v
\quad\Longleftrightarrow\quad
u_j\le v_j\ \text{for every concept coordinate }j.
$$

The paper reports an empirical order-preserving loss pattern:

$$
u\preceq v
\quad\Longrightarrow\quad
\ell(\widehat x^{(u)})\le\ell(\widehat x^{(v)}).
$$

It interprets this as a topological constraint: more complex combinations are learned after their predecessors. This is explicitly presented as an **empirical observation**, not as a general theorem for every architecture or initialization.

Figure 7 uses a two-layer ReLU MLP with $\mu=(1,2,3,4)$ and $\sigma_j=1/2$ for the four concept coordinates. The diagrams show epochs 1, 3, and 5; displayed losses are clipped at 1 to use a common color scale.

**Source:** Appendix B, Eqs. (B.1)–(B.2), pp. 16–17; Fig. 7, p. 17.

---

## 4. Empirical phenomena in SIM

### 4.1 Learning order depends on signal strength and diversity

With equal coordinate variances, the tested models learn stronger-mean directions earlier. Increasing the diversity in a weaker-mean direction can change or reverse this ordering.

Figure 2(a) varies the means through $(1,2)$, $(2,2)$, and $(3,2)$ with $\sigma_{:2}=(0.05,0.05)$. Figure 2(b) fixes $\mu_{:2}=(1,2)$ and increases $\sigma_1$ while keeping $\sigma_2=0.05$. These panels use one-layer linear models, with ambient dimension 64.

The theoretical quantity unifying these effects is

$$
a_p=\frac{\mu_p^2}{s}+\sigma_p^2.
$$

Therefore “stronger” in the learning-rate sense is not determined by $\mu_p$ alone when variances differ.

**Source:** §3.1, p. 4; Fig. 2, p. 5; §4.1, pp. 6–7.

### 4.2 Terminal slowing

Equal-time markers become closer together late in an output trajectory. The paper interprets this as declining speed of concept learning. Its one-layer solution gives an exponential explanation; its two-layer discussion attributes late slowing to self-suppression as major diagonal entries approach their learned values.

**Source:** §3.2, p. 4; §4.1, p. 6; §4.2.1, p. 8.

### 4.3 Swing-by: the defining trajectory pattern

The characteristic sequence is:

1. The test output initially moves toward the held-out composition.
2. It turns toward a training-cluster configuration associated with an earlier-learned / stronger concept.
3. With additional training, it moves back toward the correct held-out composition.

The middle stage can produce an increase in test loss, followed by a further decrease. The authors call this **Swing-by Dynamics** and distinguish it from an explanation based on noisy-label fitting or the usual in-distribution overparameterization picture of double descent.

In the displayed examples, deeper models and lower dimensions make the effect more pronounced. Figure 2(c) compares four-layer linear models at $d=64$ and $d=2$ with $\mu_{:2}=(1,2)$ and $\sigma_{:2}=(0.05,0.05)$. In the reported high-dimensional example, test-loss decrease slows but does not actually reverse.

These are architecture- and initialization-dependent observations, not a theorem that every deep model must show Swing-by or that every shallow model must have monotone test error.

**Source:** §3.3 and footnote 2, p. 5; Figs. 2(c) and 3.

---

## 5. Linear loss reduction and the data matrix

### 5.1 Effective linear map

Throughout the main theoretical section, the model is linear in its input:

$$
f(\theta;x)=W_\theta x,
\qquad
W_\theta=\frac{\partial f(\theta;x)}{\partial x}.
$$

The parameterization can nevertheless be nonlinear in $\theta$: one may train $W$ directly, or train factors whose product is $W_\theta$. The paper emphasizes that identical linear representational capacity does not imply identical training dynamics.

**Source:** §4, p. 6.

### 5.2 Loss as a weighted matrix-regression objective

Define

$$
A_n=
\frac1{sn}\sum_{p=1}^s\sum_{k=1}^n
x_k^{(p)}x_k^{(p)\top}.
$$

Then

$$
\mathcal L(\theta)
=
\frac12\left\|(W_\theta-I)A_n^{1/2}\right\|_F^2.
$$

The derivation is a trace rearrangement of the samplewise squared errors.

**Source:** Eq. (4.1), p. 6; Eqs. (C.1)–(C.6), p. 17.

### 5.3 Population second moment

A population draw is represented as

$$
X=\mu_\eta e_\eta+\operatorname{diag}(\sigma)Z,
\qquad
\eta\sim\operatorname{Unif}([s]),
\qquad
Z\sim\mathcal N(0,I_d),
$$

with $\eta$ independent of $Z$. Consequently,

$$
A=\mathbb E[XX^\top]
=
\frac1s\sum_{p=1}^s\mu_p^2e_pe_p^\top+\Sigma
=\operatorname{diag}(a_1,\ldots,a_d),
$$

where

$$
a_p=
\begin{cases}
\sigma_p^2+\mu_p^2/s,&p\le s,\\
0,&p>s.
\end{cases}
$$

The large-sample theory replaces $A_n$ by this population matrix. The paper does not provide a quantitative finite-sample transfer theorem for the full stagewise mechanism.

**Terminology:** The source calls $A$ a covariance matrix, but its explicit definition is the **uncentered second moment** $\mathbb E[XX^\top]$. The individual Gaussian covariance remains $\Sigma$.

**Source:** §4, p. 6; Appendix C.1, Eqs. (C.7)–(C.13), p. 18.

---

## 6. One-layer linear theory

### 6.1 Model and gradient

For $f(W;x)=Wx$,

$$
\mathcal L(W)=\frac12\|(W-I)A^{1/2}\|_F^2,
\qquad
\nabla\mathcal L(W)=(W-I)A.
$$

The gradient-flow equation is

$$
\dot W=-(W-I)A.
$$

The proof solves the rowwise linear differential equation, using the diagonal form of $A$.

**Source:** Theorem 4.1, p. 6; Appendix C.2, Eqs. (C.14)–(C.21), p. 18.

### 6.2 Theorem 4.1: analytical solution

The main text prints

$$
f(W(t);z)_k
=
\underbrace{\mathbf1_{\{k\le s\}}(1-e^{-a_kt})z_k}_{\widetilde G_k(t)}
+
\underbrace{\sum_{i=1}^s e^{-a_it}w_{ki}(0)z_i}_{\widetilde N_k(t)}.
$$

This is Eq. (4.2). For the intended compositional probes, $z$ is supported on the first $s$ coordinates, so this is the directly relevant expression.

At the principal probe $\widehat x$, the growing target-aligned contribution is

$$
\widetilde G_k(t)
=\mathbf1_{\{k\le s\}}(1-e^{-a_kt})\mu_k,
$$

and the initialization-dependent contribution is

$$
\widetilde N_k(t)=\sum_{i=1}^s e^{-a_it}w_{ki}(0)\mu_i.
$$

**Scope caution:** The theorem's prose says “any $z\in\mathbb R^d$,” but its displayed sum stops at $s$. For a probe with nonzero coordinates beyond $s$, untrained columns need separate treatment. Appendix C.2 also contains summation-index inconsistencies. Do not extend the printed formula beyond informative-subspace probes without checking the full matrix solution.

### 6.3 Interpretation

Small initialization makes the $\widetilde N_k$ contribution small, leaving the target-aligned growth dominant. Larger $a_k$ produces faster learning; the factor $e^{-a_kt}$ also gives exponential slowing late in training.

The “noise” here refers to dependence on initial matrix entries, not noisy labels. The task's target is still exactly $x$.

The main text describes the one-layer theory as insufficient for the observed Swing-by mechanism because the dynamics lack the interacting growth/suppression structure of the factorized model. This should not be read as an unrestricted theorem of OOD monotonicity for every possible one-layer initialization and test point.

**Source:** §4.1, pp. 6–7.

---

## 7. Symmetric two-layer linear dynamics

### 7.1 Architecture

The analyzed model is

$$
f(U;x)=UU^\top x,
\qquad
U\in\mathbb R^{d\times d'},
\qquad d'\ge d.
$$

Write

$$
W(t)=U(t)U(t)^\top.
$$

Thus $W$ is symmetric positive semidefinite, and $w_{ii}\ge0$. The model is tied and linear; it is not the general untied model $W_2W_1x$, nor a model with a ReLU inserted between the two factors.

**Source:** §4.2, p. 7.

### 7.2 Matrix equation used by the paper

The matrix vector field underlying Eq. (4.3), and displayed in Appendix D as Eq. (D.2), is

$$
\mathcal V(W)
=
WA+AW
-\frac12\left(AW^2+W^2A+2WAW\right).
$$

The main text discusses this as continuous-time entry evolution. Appendix D works with the displayed recurrence

$$
\frac{W(t+1)-W(t)}{\eta}=\mathcal V(W(t)).
$$

The coefficients here are retained as printed. They should not be silently transplanted into a different loss normalization, tied-factor gradient convention, or finite-step optimizer; see Section 15 below.

**Source:** Eq. (4.3), p. 7; Eqs. (D.1)–(D.6), p. 19.

### 7.3 Exact entry decomposition as stated

The paper writes

$$
\dot w_{ij}=G_{ij}-S_{ij}-N_{ij},
$$

where

$$
G_{ij}=w_{ij}(a_i+a_j),
$$

$$
S_{ij}
=
\frac12w_{ij}
\left[w_{ii}(3a_i+a_j)
+\mathbf1_{\{i\ne j\}}w_{jj}(3a_j+a_i)\right],
$$

and

$$
N_{ij}
=
\frac12\sum_{k\notin\{i,j\}}
 w_{ki}w_{kj}(a_i+a_j+2a_k).
$$

For the Appendix D recurrence, replace $\dot w_{ij}$ by $(w_{ij}(t+1)-w_{ij}(t))/\eta$.

The growth term has the same sign as $w_{ij}$ and increases its magnitude. Since the diagonal entries are nonnegative, the suppression term also has the same sign as $w_{ij}$ but is subtracted. The sign of $N_{ij}$ is not fixed in general. It is a deterministic interaction term, not stochastic noise and not the Gaussian input-noise parameter $\sigma$.

For a diagonal entry, the displayed growth-minus-suppression contribution simplifies to

$$
G_{ii}-S_{ii}=2a_iw_{ii}(1-w_{ii}).
$$

The remaining $N_{ii}$ interaction must still be controlled; this scalar expression alone is not the full coupled diagonal dynamics.

**Source:** §4.2, Eq. (4.3), p. 7; Eq. (D.36), p. 22.

### 7.4 Major, minor, and irrelevant entries

**Major entries:** The first $s$ diagonal entries $w_{11},\ldots,w_{ss}$.

**Minor entries:** Off-diagonal entries lying in an informative row or column. Their growth and suppression provide cross-coordinate responses that can affect the compositional probe.

**Irrelevant entries:** The remaining entries, which do not directly contribute to $W\widehat x$. This label describes their direct contribution at the chosen probe; it should not be confused with a general assertion that every such parameter is dynamically decoupled.

The $p$-th minor group consists of the off-diagonal entries in row or column $p$. For an entry connecting two informative coordinates, this means membership in both associated groups.

**Source:** §4.2.1 and Fig. 4, pp. 7–8.

---

## 8. The original Swing-by mechanism

### 8.1 Stage I: initial growth

Suppose effective-matrix entries start at a small scale $\omega$. The linear growth terms are of order $\omega$, whereas the suppression and interaction terms are quadratic in this scale. Initially, growth dominates and entry magnitudes increase at rates governed by $a_i+a_j$.

The diagonal entry associated with the largest effective signal is expected to become significant first. The paper's upper/lower growth estimates are stated in Lemmas D.1–D.3.

**Source:** §4.2.1, p. 8; Appendix D.2, pp. 20–21.

### 8.2 Stage II: suppression of associated minor entries

Once an earlier-learning major entry becomes large, it strengthens the suppression term for minor entries sharing that coordinate. Sufficient separation between effective signals can make the net drift of those minor entries oppose their earlier growth.

Lemma D.7 supplies the stated suppression bound after an associated diagonal entry exceeds 0.8. Its precise conclusion is a magnitude cap, not a standalone exact convergence-to-zero statement.

**Source:** §4.2.1, p. 8; Lemma D.7, pp. 23–24.

### 8.3 Stage III: subsequent major growth and repeated stages

The next major entry grows, its associated minor responses are suppressed, and additional stages are possible with additional concepts. The major entries eventually enter a neighborhood of 1 under the stated discrete-time estimates.

The narrative describes a sequence of growth and suppression phases. It does not mean every slower coordinate has identically zero velocity until the faster coordinate has finished learning.

**Source:** §4.2.1, p. 8; Lemmas D.4–D.8, pp. 22–25.

### 8.4 Why removing an incorrect response can worsen OOD error

At the compositional probe,

$$
f(U(t);\widehat x)_k=\sum_{p=1}^s w_{kp}(t)\mu_p.
$$

The correct identity map requires the appropriate diagonal response and no cross-coordinate leakage. Nevertheless, during training, a positive off-diagonal term can move a missing output coordinate toward its target. Test loss can therefore decrease because of a response that is not part of the final identity solution.

When learning of a major entry subsequently suppresses that minor response, the temporary benefit disappears. The output moves back toward a simpler training composition and test loss can rise. Later learning of the missing major response supplies the coordinate correctly and restores improvement.

The causal sequence proposed by the original paper is

$$
\begin{gathered}
\text{Minor-entry growth: apparent OOD improvement}\\
\Downarrow\\
\text{Major-entry learning: suppression of the minor response}\\
\Downarrow\\
\text{Transient OOD deterioration}\\
\Downarrow\\
\text{Later major learning: recovery}
\end{gathered}
$$

The signs and magnitudes of the initialized minor entries matter. Figure 5 is an $s=2$ example with all entries of $W$ initialized positive. The multiple-descent examples also use selected initialization seeds.

**Source:** §4.2.2, p. 9; Fig. 5, p. 8; Appendix E.1, pp. 25–26.

### 8.5 What is—and is not—the original attribution

The original decomposition is by **entries of the effective matrix** and their growth/suppression terms. It is not the exact decomposition of an OOD derivative into training-cluster-sourced contributions $D_1,D_2$.

Likewise, the original mechanism is not a theorem about ReLU selector switches, neuron-family covariance, a radius-weighted angle measure, or a ReLU population normal form. None of those constructions is developed in this paper.

### 8.6 OOD separation and interpretation

The source argues that a pronounced Swing-by requires the test composition to be sufficiently separated from training clusters. It associates large variances and weak separation with an effectively more in-distribution test situation and weaker Swing-by.

This is a distributional interpretation plus empirical evidence; the paper does not prove that monotone total training loss forces monotone error at every individual nearby point. Its Gaussian distributions are not defined by a hard exclusion region around the test point; Appendix F.3 separately tests a truncated version.

**Source:** §4.2.2, p. 9; Appendix F.3, pp. 29–30.

---

## 9. Appendix D assumptions

**Source for this entire section:** Appendix D.1, p. 19, Eqs. (D.7)–(D.10).

These are the source's explicit hypotheses for its stagewise matrix analysis. They are not an isotropic random-initialization theorem. The main text calls the assumptions mild or practically motivated, but the exact inequalities—not that characterization—determine the formal scope.

### D.1: bounded initialization and signal strength

There exist $\alpha>0$, $\gamma>1$, and $\beta>1$ such that

$$
\alpha\le a_k\le\gamma\alpha,
$$

and

$$
\omega\le|w_{ij}(0)|\le\beta\omega.
$$

The condition controls **every indexed initial matrix entry in the statement**, including a nonzero lower bound on off-diagonal magnitudes. It is stronger than merely requiring a small total norm or small independent factor weights.

### D.2: small step size

For a constant $K\ge20$,

$$
\eta\le\frac1{9K\gamma\alpha}.
$$

### Definition D.1: initial phase

An entry $(i,j)$ is in its initial phase at time $t$ if

$$
|w_{ij}(t)|\le P\beta\omega.
$$

### D.3: small initial phase

$$
P\omega\beta\le0.4.
$$

### D.4: small initialization

The printed bound is

$$
\omega\le
\min\left\{
\frac{\min\{\kappa-1,\,1-\kappa^{-1/2}\}}
{PK\gamma d\beta^2},
\frac1{\sqrt{2\beta}}
\right\},
$$

with

$$
\kappa>1.1,
\qquad
\kappa\le1+\frac12KC^{-1},
\qquad
P\ge2.
$$

The dimension factor $d$ appears explicitly in the first initialization bound.

### D.5: significant effective-signal separation

For the ordering written in the source, namely $i>j$,

$$
\frac{a_i+a_j}{2a_i}
\le
\frac{\log P}
{10\kappa^2\log\!\left(1/(P\beta\omega)\right)+\log(P\beta)},
$$

and there exists $C>1$ such that

$$
a_i-3a_j\ge C^{-1}\alpha.
$$

This is substantially stronger than merely requiring distinct means or $\mu_i>\mu_j$. The exact index ordering has a conflict with the descending-order convention in the main narrative; see Section 15. These inequalities are retained as printed, without silently reordering the indices or asserting that a particular later experimental parameter pair satisfies them.

---

## 10. Appendix D lemma stack and proof strategy

### 10.1 Bootstrap structure

Appendix D introduces the temporary assertion

$$
\text{Assertion D.1:}\qquad
|w_{ij}(t)|\le P\beta\omega
\quad\text{for all }i\ne j\text{ and all }t.
$$

It uses this assertion while developing estimates and closes it at the end. The authors explicitly describe this as a way of organizing an induction, not as an additional final trajectory assumption.

The reported proof structure is

```text
Appendix D assumptions
          |
          v
Temporary off-diagonal initial-phase assertion
          |
          v
Interaction-term bound (Corollary D.1)
          |
          +--> Upper growth (D.1)
          +--> Early lower growth and sign control (D.2–D.3)
          +--> Post-initial diagonal growth (D.4)
          +--> Diagonal bounds and persistence (D.5–D.6)
          |
          v
Suppression after a major response is large (D.7)
          |
          v
Compare diagonal learning time with off-diagonal escape time (D.8)
          |
          v
Close Assertion D.1
```

For a reusable proof, the dependencies must be interpreted as one simultaneous induction / bootstrap closure. Merely assuming the all-time assertion without the final closure would not prove the initialized result.

**Source:** Appendix D.2, p. 20; Lemma D.8, pp. 24–25.

### 10.2 Corollary D.1: interaction control

Under the bootstrap, the paper states

$$
|N_{ij}(t)|\le2P\gamma\alpha d\beta^2\omega^2.
$$

This is the small forcing budget used in the subsequent comparisons. The bound is recorded here as stated; derivation of its constants must be checked when adapting the proof.

**Source:** Corollary D.1, p. 20.

### 10.3 Lemma D.1: upper-bounded growth

For every entry and time, the stated envelope is

$$
|w_{ij}(t)|
\le
|w_{ij}(0)|\exp\!\bigl(\eta t(a_i+a_j)\kappa\bigr).
$$

The proof uses the linear growth contribution, the sign of suppression, the interaction budget, and smallness of initialization to absorb the error into the multiplicative factor $\kappa$.

**Role:** An upper clock for growth, especially the time before a minor entry could escape its permitted regime.

**Source:** Lemma D.1, Eq. (D.11), p. 20.

### 10.4 Lemma D.2: lower-bounded initial growth

Define

$$
T_1=\frac{\log P}{2\eta\gamma\alpha\kappa}.
$$

The paper states that through this initial window every entry remains in the initial phase, preserves its initial sign, and satisfies

$$
|w_{ij}(t)|
\ge
|w_{ij}(0)|\exp\!\bigl(\eta t(a_i+a_j)\kappa^{-1}\bigr),
$$

$$
w_{ij}(t)w_{ij}(0)>0.
$$

The lower estimate bounds suppression and interactions while all entries are small; the upper estimate verifies that the initial-phase premise remains valid on the stated window.

**Role:** Establishes actual early growth rather than just a permissible upper bound.

**Source:** Lemma D.2, Eq. (D.22), p. 21.

### 10.5 Lemma D.3: refined initial diagonal growth

For diagonal entry $(i,i)$, define

$$
T_1^{(i)}
=
\frac{\log\!\left(P\beta\omega/w_{ii}(0)\right)}
{2\eta a_i\kappa}.
$$

The stated initial-window lower bound is

$$
w_{ii}(t)\ge w_{ii}(0)e^{2\eta ta_i\kappa^{-1}}.
$$

The source says the proof is analogous to Lemma D.2 and omits its details.

**Role:** Replaces the global effective-signal envelope by a coordinate-specific clock. The printed horizon is an initial-phase guarantee; a separate hitting-time inference must respect the upper/lower exponent distinction.

**Source:** Lemma D.3, Eq. (D.34), p. 21.

### 10.6 Lemma D.4: diagonal growth beyond initialization

Suppose $w_{ii}(t_0)\ge P\beta\omega$. While that entry remains below a chosen

$$
\lambda\in(P\beta\omega,1-K^{-1}),
$$

the paper states

$$
w_{ii}(t_0+t)
\ge
w_{ii}(t_0)
\exp\!\bigl(2\eta ta_i(1-\lambda)\kappa^{-1}\bigr).
$$

The comparison uses the logistic-type contribution $2a_iw_{ii}(1-w_{ii})$, together with the interaction budget. Positive semidefiniteness supplies nonnegative diagonals.

**Role:** Converts a small learned seed into a substantial major response before saturation.

**Source:** Lemma D.4, Eq. (D.35), p. 22.

### 10.7 Lemma D.5 and Corollary D.2: diagonal upper control

The stated all-time bound is

$$
0\le w_{ii}(t)\le1+2K^{-1}.
$$

The corresponding one-step bound is

$$
|w_{ii}(t+1)-w_{ii}(t)|\le K^{-1}.
$$

The proof separates states above and below a neighborhood of 1. Above that neighborhood, self-suppression produces a downward drift; the small-step bound limits overshoot.

**Role:** Prevents uncontrolled diagonal growth and permits a terminal-region persistence argument.

**Source:** Lemma D.5, pp. 22–23; Corollary D.2, p. 23.

### 10.8 Lemma D.6: persistence of a learned diagonal

If

$$
w_{ii}(t_0)\ge1-2K^{-1},
$$

then the paper states

$$
w_{ii}(t)\ge1-2K^{-1}
\qquad\text{for all }t\ge t_0.
$$

Together with Lemma D.5, this retains a learned diagonal in a small band around 1 after it enters that band.

**Source:** Lemma D.6, p. 23.

### 10.9 Lemma D.7: suppression

For an off-diagonal entry with the source's ordering $i>j$, if

$$
w_{ii}(t_0)>0.8,
$$

then the stated conclusion is

$$
|w_{ij}(t)|
\le
\max\{|w_{ij}(t_0)|,\omega\}
\qquad(t\ge t_0).
$$

The proof compares the growth and suppression coefficients once $w_{ii}>0.8$, uses the strong signal-gap assumption to obtain a negative drift outside the small floor, and controls the interaction term and possible discrete overshoot.

**Role:** Stops a minor entry from escaping after its associated major response becomes substantial.

**Precision:** This lemma establishes a cap of the displayed form. It is not, by itself, a proof that every minor entry reaches exactly zero or that an OOD derivative necessarily changes sign.

**Source:** Lemma D.7, Eq. (D.56), pp. 23–24.

### 10.10 Lemma D.8: closure of the off-diagonal bootstrap

The stated conclusion is exactly Assertion D.1:

$$
|w_{ij}(t)|\le P\beta\omega
\qquad\text{for every }i\ne j\text{ and all }t.
$$

The proof seeks a time $t_*$ when $w_{ii}$ has reached 0.8 but the associated off-diagonal entry has not exceeded $P\beta\omega$. It combines diagonal lower-growth estimates with the off-diagonal upper envelope and the signal-separation condition. Lemma D.7 is then used for later times.

**Role:** Closes the premise supporting the earlier interaction estimates.

**Source:** Lemma D.8, Eqs. (D.72)–(D.81), pp. 24–25.

### 10.11 What this stack delivers in the paper

The stack is designed to justify a multistage description of the effective matrix: early entry growth, ordered major learning, suppression of minor entries, and terminal diagonal control. The main text combines this description with the signs of contributions at a compositional probe to explain Swing-by.

Do not replace these statements by a stronger claim that Appendix D already supplies an explicit open parameter box, high-probability isotropic initialization, sector-uniform ReLU reversal, a clusterwise competition theorem, or a certified reversal-time formula. Those are not its stated results.

---

## 11. Initialization, dimension, multiple descents, and failure modes

### 11.1 Comparable major/minor initialization is important

The matrix analysis assumes that diagonal and off-diagonal initial magnitudes are all comparable to $\omega$. A generic Gaussian factor initialization need not yield that property in a wide factorization.

If rows of $U$ are independent with

$$
u_i\sim\mathcal N(0,\tau^2I_{d'}),
\qquad
w_{ij}=\langle u_i,u_j\rangle,
$$

Appendix E.2 records

$$
\mathbb E[w_{ij}]
=
\begin{cases}
0,&i\ne j,\\
d'\tau^2,&i=j.
\end{cases}
$$

The authors use this distinction to discuss breakdown of the assumption that major and minor entries start at comparable scales. They connect less pronounced Swing-by in larger-dimensional settings to initialization effects as well as to the availability of favorable minor-entry signs.

This is not a universal “large dimension eliminates Swing-by” theorem. The argument involves the factor width $d'$, which is constrained by $d'\ge d$ in the analyzed model, and the particular initialization law.

**Source:** Appendix E.2, pp. 25–26, Eq. (E.1).

### 11.2 More than two concepts and multiple descents

Appendix E.1 gives selected examples of repeated growth/suppression cycles:

| Figure | Model | Dimensions | Mean strengths | Coordinate standard deviations | Reported phenomenon |
|---|---|---|---|---|---|
| 8 | Symmetric two-layer linear | $d=s=3$ | $(1.0,1.5,2.2)$ | $(0.05,0.05,0.05)$ | Triple descent |
| 9 | Symmetric two-layer linear | $d=s=4$ | $(1.0,1.5,2.2,2.7)$ | $(0.05,0.05,0.05,0.5)$ | Quadruple descent |

The paper explicitly says these examples require a subtle choice of signals and specific initialization conditions, and that the random seed was tuned. The time axis is logarithmic to expose stages at different time scales.

**Source:** Appendix E.1, p. 25; Figs. 8–9 and captions, p. 26.

### 11.3 Failure to learn every concept

The proposed failure mode is that a minor entry grows too large before it is suppressed. It can then strongly suppress a corresponding major entry, leaving the model at a partial composition rather than the desired full composition.

Figure 10 uses

$$
d=s=3,
\qquad
\mu=(0.7,1.7,3),
\qquad
\sigma=(0.05,0.05,0.05).
$$

The plotted $w_{11}$ fails to grow and the OOD loss plateaus above zero. The authors describe this as a failure mode outside their assumptions and identify systematic characterization of such cases as future work. The example is not a complete theorem classifying all asymptotic failures.

**Source:** Appendix E.3, p. 26; Fig. 10, p. 27; Appendix E.4, pp. 26–27.

---

## 12. SIM experimental protocols and controls

### 12.1 Defaults reported in Appendix F.1

| Setting | Reported value |
|---|---|
| Samples per Gaussian cluster | 5,000 |
| Architectures | MLPs with linear or ReLU activations |
| Optimizer | Stochastic gradient descent |
| Batch size | 128 |
| Learning rate | 0.1 |
| Training duration | 40 epochs |
| Default input/output dimension | $d=64$ |
| Default hidden dimension | 64 |
| Coordinate orientation | A common random rotation of train and test points, unless otherwise specified |

These are the source's stated general SIM defaults. Some specialized matrix-evolution plots use different displayed iteration scales; the PDF does not supply a complete per-figure implementation manifest resolving every special case. Do not infer unspecified initialization details or reproduce specialized runs solely from this default table.

**Source:** Appendix F.1, pp. 27–28.

### 12.2 Two-layer linear and ReLU comparisons

Figures 11 and 12 repeat the learning-order experiments using two-layer models:

- **Figure 11:** linear activations.
- **Figure 12:** ReLU activations.

Both use $s=2$. The left panels fix $\mu_{:2}=(1,2)$ and vary coordinate noise; the right panels fix $\sigma_{:2}=(0.05,0.05)$ and vary means through $(1,2)$, $(2,2)$, and $(3,2)$.

The captions establish which architecture is which. The preceding prose reverses “with” and “without” ReLU relative to those captions; this reference follows the captions.

These experiments support the qualitative robustness of learning-order and slowing observations. They are not a theorem for the trained ReLU feature distribution.

**Source:** Appendix F.2 and Figs. 11–12, p. 28.

### 12.3 Low-dimensional, deeper linear examples

Figures 13–14 use three-layer linear models with three hidden dimensions and

$$
d=3,\quad s=2,\quad \sigma_{:2}=(0.05,0.05).
$$

The two mean configurations are $(1,2)$ and $(2,4)$. These data are not randomly rotated. The output trajectories and corresponding loss curves show pronounced Swing-by.

**Source:** Appendix F.2, p. 28; Figs. 13–14, p. 29.

### 12.4 Training/test separation control

Figure 15 replots the low-dimensional trajectory with the training points visible. Figure 16 repeats the experiment with training points excluded from the ball of radius

$$
\frac12\min_{p\in[s]}\mu_p
$$

around the compositional test point. The stated procedure rejects points in that ball and resamples until the desired training-set size is reached.

The source reports that only a few samples are affected and that the output dynamics change little. The purpose is to check that the reported Swing-by is not an artifact of training samples lying unusually near the test composition.

**Source:** Appendix F.3 and footnote 5, p. 29; Figs. 15–16, p. 30.

### 12.5 Training loss and training-center trajectories

Figure 17 adds training loss to the symmetric-model example from Fig. 5: the displayed training loss decreases monotonically while the test loss is non-monotonic.

Figure 18 adds output trajectories evaluated at the training-cluster centers. Those trajectories can also bend, at stages different from the compositional test trajectory. The origin is omitted because the linear model outputs zero there.

**Source:** Appendix F.4, pp. 29–30; Figs. 17–18, p. 30.

---

## 13. Diffusion-model validation

### 13.1 Purpose and train/test compositions

The diffusion experiments test whether the simplified SIM phenomenology appears in a more complex image-generation model. The task involves circles with two concepts: size and color.

The four compositions are

| Code | Composition | Split |
|---|---|---|
| 00 | Red, big | Training |
| 01 | Red, small | Training |
| 10 | Blue, big | Training |
| 11 | Blue, small | OOD evaluation |

The generated image is mapped back into concept space by a separately trained classifier. This yields a concept-space output trajectory analogous to the SIM trajectory at a fixed compositional input.

Although the main discussion uses text-conditioned / prompt-to-image language, the implementation described in Appendix G conditions on an explicit four-dimensional size/RGB vector. It should not be summarized as requiring a language-model text encoder.

**Source:** §5, p. 10; Appendix G.1–G.3, pp. 30–32.

### 13.2 Data-generating process and signal manipulation

Big and small circles have diameters equal to 70% and 30% of the image, respectively. The experiments vary the absolute red/blue color difference from 0.2 to 0.7 to change color signal strength.

Circle position and background color are randomized, and noise is added to avoid an excessively narrow image distribution. Further details are delegated to Park et al. (2024).

Figure 6 labels concept-signal values approximately $0.137$, $0.247$, $0.358$, $0.468$, $0.579$, and $0.689$. These labels and the raw color-difference range are separately reported quantities; the paper refers to earlier work for the full concept-space construction.

**Source:** §5 and Fig. 6, p. 10; Appendix G.1 and Fig. 19, pp. 30–31.

### 13.3 Generative model and training settings

| Component | Specification in Appendix G.2 |
|---|---|
| Model family | Conditional variational diffusion model |
| Output | $3\times32\times32$ image |
| Conditioning | Four-dimensional vector: one size value and three RGB values |
| Backbone | Conditional U-Net |
| Hidden dimensions | $[64,128,256]$ before downsampling layers |
| Residual blocks | Two ResNet layers per level |
| Conditioning injection | Two-layer MLP transforms conditioning to hidden dimensions; added after each downsampling layer |
| Bottleneck | Self-attention layer |
| Normalization | LayerNorm |
| Activation | GELU |
| Noise schedule | Learned linear schedule, initialized with $\gamma_{\max}=10$, $\gamma_{\min}=-5$ |
| Assumed data noise | $10^{-3}$ |
| Sampling | 100 inference diffusion steps |
| Optimizer | AdamW |
| Learning rate | $10^{-3}$ |
| Weight decay | 0.01 |
| Batch size | 128 |
| Training duration | 20,000 steps |

The variational diffusion formulation does not fix a discrete number of diffusion steps at training time.

**Source:** Appendix G.2, p. 31.

### 13.4 Concept-space evaluation

The evaluation classifier uses a U-Net backbone followed by max pooling and an MLP to classify color and size. The source reports training it for 10,000 steps and obtaining 100% accuracy on a held-out test set.

The reported concept-space representation averages over 32 generated images and five model-run seeds. Concept-space error is measured by MSE; speed $|dC/dt|$ is estimated by finite differences in the same concept space.

The paper calls the classifier perfect in its description, but the concrete evidence given is the reported held-out classification accuracy, not a mathematical guarantee on every generated image.

**Source:** Appendix G.3, pp. 31–32.

### 13.5 Reported outcomes

Figure 6 reports three correspondences with SIM:

**Order:** Changing color signal changes the learning order of color and size.

**Swing-by:** Some trajectories bend temporarily toward the stronger concept and later reach the correct blue-small composition; concept-space MSE can show a double-descent-like curve.

**Slowing:** The estimated traversal speed decreases, broadly matching the exponential-slowing prediction used in the paper's interpretation.

These are empirical correspondences. They do not establish that a diffusion model literally obeys the symmetric linear matrix equation or the Appendix D assumptions.

**Source:** §5 and Fig. 6, p. 10.

---

## 14. Scope of the original ReLU results and future directions

### 14.1 What the paper does contain about ReLU

The original paper includes two-layer ReLU MLP experiments on SIM. Figure 7 uses a ReLU model for the hierarchy-of-compositions observation, and Figure 12 shows its output trajectories under mean and variance changes.

Appendix E.4 explicitly identifies extending the analysis to **two-layer ReLU networks**, deeper linear networks, and NTK-regime models as future directions. It suggests investigating early neuron alignment as a possible starting point for a ReLU analysis, citing Maennel et al. (2018) and Min et al. (2023).

**Source:** Appendix B, pp. 16–17; Appendix E.4, p. 27; Appendix F.2, p. 28.

### 14.2 What the paper does not establish

The paper does not provide a rigorous initialized ReLU theorem on SIM, nor does it establish that ReLU neurons can be replaced by two perfectly coherent families throughout the relevant learned regime.

It does not specify the aligned-balanced isotropic continuum law used in the later project, prove preservation of such a law, derive a joint input/output angular transport equation, or analyze covariance-driven ReLU competition.

It also does not provide an exact training-cluster decomposition of an OOD derivative, a theorem for off-cone reversal sectors, or a finite-width/finite-sample lift of an initialized ReLU population mechanism.

Those absences are important when using the paper as a predecessor: inherit its task and motivation, but do not attribute later conjectures or proofs to it.

### 14.3 Broader future directions named in the paper

The authors call for systematic analysis beyond the Appendix D assumptions, especially the conditions leading to failed OOD generalization. They also emphasize identifying and simplifying higher-order interactions in deeper models while preserving the useful stagewise organization of the two-layer analysis.

**Source:** Appendix E.4, pp. 26–27.

---

## 15. Source-reading cautions for mathematical reuse

This section records places where scope, notation, or equations require care. It does not replace the paper with a newly repaired theory.

### 15.1 Data and parameter meanings

The Gaussian covariance is shared across clusters, with noise only on informative coordinates. The matrix $A$ is explicitly $\mathbb E[XX^\top]$, despite the paper's use of “covariance.” The original $s$ counts concepts, $d$ is ambient dimension, and $d'$ is symmetric-model width. None of these should be silently reused for a different quantity.

**Source:** §2.1, pp. 3–4; §4, pp. 6–7.

### 15.2 Arbitrary-input wording in Theorem 4.1

Equation (4.2) sums initialization contributions only over informative coordinates but is introduced for arbitrary $z\in\mathbb R^d$. The compositional probes satisfy the support restriction needed for the displayed form. A result about arbitrary ambient probes must address the untrained columns explicitly.

**Source:** Theorem 4.1, p. 6; Appendix C.2, p. 18.

### 15.3 Gradient-flow normalization versus the displayed finite-step recurrence

The main text uses continuous-time language, whereas Appendix D defines a recurrence for $W$. Do not identify that recurrence with ordinary finite-step gradient descent on $U$ merely because $W=UU^\top$: updating a factor and then forming its Gram matrix has a second-order step contribution that the displayed recurrence does not show.

Similarly, a fresh derivation must track the loss coefficient and tied-factor differentiation before adopting the printed vector-field coefficient. This reference retains the paper's equation and its time convention rather than declaring a corrected normalization.

**Source:** Eq. (4.1), p. 6; Eq. (4.3), p. 7; Eqs. (D.1)–(D.2), p. 19.

### 15.4 Signal ordering and non-informative coordinates

The main stage narrative uses descending effective-signal order. Appendix D.5 instead prints, for $i>j$, the condition $a_i-3a_j\ge C^{-1}\alpha$, which points in the opposite direction under that convention.

Also, Appendix D.1 prints $\alpha\le a_k$ for every $k$, while the general setup gives $a_k=0$ for $k>s$. Applying those assumptions with $d>s$ therefore requires an explicit index restriction or revised formulation. The PDF does not reconcile this automatically.

**Source:** §4, p. 6; §4.2.1, p. 8; Assumptions D.1 and D.5, p. 19.

### 15.5 Growth windows are not interchangeable with hitting times

Lemma D.3 gives a lower-growth estimate on a stated initial-phase window, with different factors of $\kappa$ in the window and the growth exponent. The later closure proof uses a time of that form as a diagonal progress threshold. Before reusing that inference, check the hitting-time argument rather than assuming the earlier lemma supplies it unchanged.

This reference preserves the stated formulas and describes the intended dependency; it does not silently repair the timing step.

**Source:** Lemma D.3, p. 21; Lemma D.8, pp. 24–25.

### 15.6 Narrative convergence versus the exact lemma conclusions

The main narrative describes learned diagonals approaching 1 and minor entries being pushed toward zero. The displayed finite-step lemmas give an invariant diagonal band and off-diagonal caps. Those quantitative conclusions should not be replaced by a stronger exact-limit claim without additional argument.

Likewise, matrix growth and suppression alone do not supply every sign, amplitude, and uniformity condition that a separate quantitative OOD-reversal theorem might require.

**Source:** §4.2.1–§4.2.2, pp. 8–9; Lemmas D.5–D.8, pp. 22–25.

### 15.7 Local notation and cross-reference issues

The PDF contains smaller inconsistencies as well: Eq. (2.1) uses a cluster superscript inconsistent with its sum; the suppression discussion includes a strongest-column coefficient inconsistent with the preceding exact output sum; a sentence in the proof of Lemma D.5 prints $K\le10$ although D.2 assumes $K\ge20$; and the “with/without ReLU” wording before Figs. 11–12 conflicts with the captions.

For reuse, rely on the explicit dataset definition, exact output expression, assumption block, and figure captions, while marking any local correction. Do not treat this digest as a proof audit resolving all such issues.

**Source:** pp. 4, 9, 22, and 28.

---

## 16. Figure and appendix lookup guide

### 16.1 Figures

| Figure | Page | Content and reason to consult it |
|---|---:|---|
| 1 | 2 | Concept-space motivation, SIM geometry, and schematic non-monotonic OOD learning |
| 2 | 5 | Mean/noise effects on learning order; low/high-dimensional trajectory comparison |
| 3 | 5 | Test-loss curves for the dimensional comparison |
| 4 | 8 | Major, minor, irrelevant entries, and minor-group organization |
| 5 | 8 | Central two-concept symmetric-model example linking entry evolution, test loss, and trajectory stages |
| 6 | 10 | Diffusion-model learning order, non-monotonic concept-space MSE, and slowing |
| 7 | 17 | ReLU experiment on the partial order of binary concept compositions |
| 8 | 26 | Selected three-concept symmetric-model triple descent |
| 9 | 26 | Selected four-concept symmetric-model quadruple descent |
| 10 | 27 | Partial-composition failure example with a suppressed major response |
| 11 | 28 | Two-layer linear MLP trajectories under signal/diversity changes |
| 12 | 28 | Two-layer ReLU MLP trajectories under the same kinds of changes |
| 13 | 29 | Low-dimensional three-layer linear output trajectories |
| 14 | 29 | Test losses corresponding to Fig. 13 |
| 15 | 30 | Training samples shown alongside the trajectory |
| 16 | 30 | Training-distribution truncation around the test point |
| 17 | 30 | Monotone training loss versus non-monotone OOD loss in the central example |
| 18 | 30 | Training-center output trajectories compared with the compositional trajectory |
| 19 | 31 | Diffusion data-generating process and manipulation of concept signals |

### 16.2 Appendices

| Appendix | Pages | Main content |
|---|---|---|
| A | 16 | Related work: compositional generalization and deep linear dynamics |
| B | 16–17 | Binary composition hierarchy and empirical topological ordering |
| C | 17–18 | Linear loss reduction, population second moment, and Theorem 4.1 proof |
| D | 18–25 | Symmetric two-layer matrix recurrence, assumptions, and lemma stack |
| E | 25–27 | Multiple descents, initialization/dimension effects, failure modes, and future directions |
| F | 27–30 | SIM experiment defaults, additional architectures, separation controls, and training trajectories |
| G | 30–32 | Diffusion data, architecture, optimization, and concept-space evaluation |

The main paper occupies pp. 1–10; acknowledgments and references occupy pp. 11–15.

---

## 17. Related-work pointers and bibliographic record

### 17.1 Prior concept-space work emphasized by the paper

**Okawa et al. (2023), *Compositional Abilities Emerge Multiplicatively: Exploring Diffusion Models on a Synthetic Task*.** The paper presents this as a key predecessor for synthetic compositional diffusion experiments.

**Park et al. (2024), *Emergence of Hidden Capabilities: Exploring Learning Dynamics in Concept Space*.** The paper borrows concept-space motivation and much of the diffusion experimental setup from this work.

**Source:** Introduction, pp. 1–3; §5, p. 10; references, pp. 13–14; Appendix G, pp. 30–32.

### 17.2 Linear-dynamics and matrix-factorization connections

Appendix A situates the work relative to deep linear learning dynamics and matrix factorization, including Saxe et al., Arora et al., Ji and Telgarsky, Advani et al., Li et al., Stöger and Soltanolkotabi, and Jin et al.

The paper's stated distinction is its focus on interacting effective-matrix entries and their transient OOD behavior, rather than solely the final implicit bias or a diagonally decoupled trajectory. These are the source's positioning claims, not an independent survey of the cited literature.

**Source:** §4.2 and §4.2.2, pp. 7 and 9–10; Appendix A, p. 16.

### 17.3 ReLU starting points named in the paper

**Maennel, Bousquet, and Gelly (2018), *Gradient Descent Quantizes ReLU Network Features*.**

**Min, Mallada, and Vidal (2023), *Early Neuron Alignment in Two-Layer ReLU Networks with Small Initialization*.**

Appendix E.4 cites these in suggesting early alignment as a starting point for a future ReLU analysis. Their full hypotheses and results are not reproduced in the SIM paper and should be consulted directly before use.

**Source:** References, p. 13; Appendix E.4, p. 27.

### 17.4 Minimal citation record

The following record is constructed from the supplied PDF's title page; the citation key is only a suggested local key.

```bibtex
@inproceedings{yang2025swingby,
  title     = {Swing-by Dynamics in Concept Learning and
               Compositional Generalization},
  author    = {Yang, Yongyi and Park, Core Francisco and
               Lubana, Ekdeep Singh and Okawa, Maya and
               Hu, Wei and Tanaka, Hidenori},
  booktitle = {International Conference on Learning Representations},
  year      = {2025},
  note      = {Reference version: arXiv:2410.08309v2,
               March 13, 2025}
}
```

---

## 18. Essential facts to preserve in a follow-up

The task is **identity regression on a structured Gaussian mixture**, not class-label prediction. Cluster means occupy distinct concept directions. Every cluster shares the same coordinate-indexed covariance, and noise is confined to informative coordinates. The main compositional probe is the sum of training means; Appendix B adds only binary nonnegative combinations.

The data-dependent linear learning rate is $a_p=\mu_p^2/s+\sigma_p^2$. The original mechanism theory analyzes the **tied symmetric linear model** $UU^\top x$. Its central explanation is that an initially helpful but ultimately incorrect minor response grows, is suppressed by major-response learning, and temporarily worsens OOD error before later recovery.

The Appendix D proof is organized around explicit initialization/signal assumptions and a closed off-diagonal bootstrap. Its assumptions are not equivalent to arbitrary small random initialization, and its displayed bounds should not be promoted to stronger quantitative reversal claims without further proof.

The paper already includes ReLU experiments, but explicitly leaves a rigorous ReLU mechanism analysis to future work. Its diffusion results provide empirical analogies, not a theorem identifying diffusion training with the linear matrix flow.

**Bottom line:** The predecessor supplies the SIM task, an empirical concept-space phenomenology, and a stagewise growth–suppression explanation for a symmetric linear model. Any initialized, exact-cluster, angular-distribution, or off-cone theorem for an untied two-layer ReLU network must be established separately.

**Sources:** §2.1, pp. 3–4; §4, pp. 6–9; Appendix D, pp. 19–25; Appendix E.4, p. 27; Appendix F.2, p. 28.
