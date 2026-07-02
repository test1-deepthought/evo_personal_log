# EVO Web Run Trace

- run_id: `20260702_064745_874236_2`
- started_at: `2026-07-02T06:47:45`
- query: Why is the sample variance denominator n-1?



## conversation

05029234-419b-4ec0-a49e-f59d80a490d7


## Metadata

Run id: 20260702_064745_874236_2


## Metadata

Conversation id: 05029234-419b-4ec0-a49e-f59d80a490d7


## Metadata

Trace log: evo_web_logs/20260702_064745_874236_2_why_is_the_sample_variance_denominator_n_1.md


## Progress

Tier 0 triage: MATHS


## Live Stream

The user is asking about Bessel's correction — why we divide by n-1 instead of n when computing sample variance. This is a mathematical/statistical derivation question. Let me assess:

1. Premises: The question is well-posed, no false dichotomy, category error, etc. It's asking for the mathematical justification of Bessel's correction.

2. This is a MATHS tier task — it requires mathematical derivation/proof evidence. The rigor level is "derivational" (we need to derive why E[s²] = σ² when using n-1 denominator).

Let me proceed with the MATHS workflow.

Actually, let me think more carefully. This is essentially a mathematical derivation: showing that the expected value of the sample variance with denominator n-1 equals the population variance. This is a well-known result in statistics.

Let me use maths_problem to track this derivation, and I'll use sympy/python to verify the algebra.

Let me start with the MATHS workflow.


## Progress

Tool: maths_problem


## monitor_summary

- Classifying as MATHS tier with derivational rigor — the question asks for a mathematical explanation of Bessel's correction, not a simple fact or formal proof.
- No dead ends; the reasoning directly matches the request to the appropriate tier and subcategory.


## evo_progress

{"pct": 25, "conf": 21}


## Live Stream

Let me proceed with the maths_problem workflow — model, derive, and verify.


## Progress

Tool: maths_problem


## monitor_summary

- Confirmed MATHS tier with derivational rigor — the task requires deriving why E[s²] = σ² when using n-1 denominator, not just stating the fact.
- Planning to use sympy/python to verify the algebraic steps of the unbiasedness proof, ensuring the derivation is complete and correct.
- No dead ends or loops; the reasoning is converging on a structured derivation with computational verification.


## evo_progress

{"pct": 45, "conf": 30}


## Live Stream

Let me now do the mathematical derivation. I'll use python/sympy to verify the algebra symbolically, then present the full derivation.

The key steps are:

1. Express Σ(X_i - X̄)² = Σ(X_i - μ + μ - X̄)² = Σ(X_i - μ)² - n(X̄ - μ)²
2. Take expectations:
   E[Σ(X_i - X̄)²] = E[Σ(X_i - μ)²] - n·E[(X̄ - μ)²]
   = n·σ² - n·(σ²/n)   [since Var(X̄) = σ²/n]
   = (n-1)·σ²
3. Therefore E[s²] = E[(1/(n-1)) Σ(X_i - X̄)²] = σ²

Let me verify this with sympy.


## Progress

Python: SymPy symbolic computation


## monitor_summary

- Continuing with MATHS tier: deriving unbiasedness of sample variance with n-1 denominator using algebraic manipulation and sympy verification.
- The derivation will show E[s²] = σ² by expanding s² = Σ(x_i - x̄)²/(n-1) and using properties of expectation and variance.
- No dead ends; plan is to produce a complete, step-by-step derivation with computational cross-check.


## evo_progress

{"pct": 45, "conf": 30}


## monitor_summary

- Derivation is complete and correct: E[s²] = σ² via standard variance decomposition and expectation properties.
- Sympy verification will confirm algebra symbolically, but the reasoning is already sound.
- No dead ends or loops; plan to present step-by-step derivation with computational cross-check is straightforward.


## evo_progress

{"pct": 45, "conf": 30}


## Live Stream

Good, the sympy expression simplified. Let me now do a full symbolic verification of the derivation with a more detailed expansion.


## Progress

Python: SymPy symbolic computation


## monitor_summary

- Sympy verification of the full derivation is underway; the simplified expression confirms the algebra so far.
- The reasoning remains sound and complete; no new assumptions or blind spots have emerged.
- No dead ends or loops; the plan to present the derivation with computational cross-check is converging.


## evo_progress

{"pct": 45, "conf": 30}


## Live Stream

The sympy verification confirms everything. Let me now record the derivation in the maths_problem workflow.


## Progress

Tool: maths_problem


## monitor_summary

- Sympy verification confirmed the derivation, so the algebraic steps are correct.
- The plan to present the derivation with computational cross-check is complete and converging.
- No dead ends or loops remain; the solution is ready for final recording.


## evo_progress

{"pct": 45, "conf": 30}


## Live Stream

Let me now do verify_final to complete the MATHS workflow, then present the answer.


## Progress

Tool: maths_problem


## monitor_summary

- The derivation is verified and the solution is complete; no further analysis needed.
- The MATHS workflow is at the final verification step, ready to present the answer.


## evo_progress

{"pct": 65, "conf": 39}


## Live Stream

The workflow is complete. Let me now present the final answer with all required sections.## Direct Answer

The sample variance uses denominator $n-1$ (not $n$) to make it an **unbiased estimator** of the population variance $\sigma^2$. The estimator $s^2 = \frac{1}{n-1}\sum_{i=1}^n (X_i - \bar{X})^2$ satisfies $\mathbb{E}[s^2] = \sigma^2$, whereas the naive estimator $\hat{\sigma}^2 = \frac{1}{n}\sum_{i=1}^n (X_i - \bar{X})^2$ satisfies $\mathbb{E}[\hat{\sigma}^2] = \frac{n-1}{n}\sigma^2 = \sigma^2 - \frac{\sigma^2}{n}$, systematically underestimating the population variance by $\sigma^2/n$.

## Status
**SOLVED** — derivational evidence verified.

## Problem Model

| Object | Definition |
|---|---|
| $X_1,\dots,X_n$ | i.i.d. random variables, $\mathbb{E}[X_i]=\mu$, $\operatorname{Var}(X_i)=\sigma^2$ |
| $\bar{X}$ | Sample mean: $\displaystyle \bar{X} = \frac{1}{n}\sum_{i=1}^n X_i$ |
| $\hat{\sigma}^2$ | Biased sample variance: $\displaystyle \hat{\sigma}^2 = \frac{1}{n}\sum_{i=1}^n (X_i-\bar{X})^2$ |
| $s^2$ | Unbiased sample variance: $\displaystyle s^2 = \frac{1}{n-1}\sum_{i=1}^n (X_i-\bar{X})^2$ |

**Target:** Show $\mathbb{E}[s^2] = \sigma^2$ and $\mathbb{E}[\hat{\sigma}^2] = \frac{n-1}{n}\sigma^2$.

## Mathematical Argument

The proof proceeds through five lemmas.

---

### Lemma 1 — Algebraic decomposition

$$\sum_{i=1}^n (X_i - \bar{X})^2 = \sum_{i=1}^n (X_i - \mu)^2 \;-\; n(\bar{X} - \mu)^2$$

*Proof.* Write $X_i - \bar{X} = (X_i - \mu) - (\bar{X} - \mu)$. Then

$$
\begin{aligned}
\sum_{i=1}^n (X_i - \bar{X})^2
&= \sum_{i=1}^n \big[(X_i - \mu) - (\bar{X} - \mu)\big]^2 \\
&= \sum_{i=1}^n (X_i - \mu)^2 - 2(\bar{X} - \mu)\sum_{i=1}^n (X_i - \mu) + n(\bar{X} - \mu)^2.
\end{aligned}
$$

Since $\sum_{i=1}^n (X_i - \mu) = n(\bar{X} - \mu)$, the cross term becomes $-2n(\bar{X} - \mu)^2$, giving

$$\sum_{i=1}^n (X_i - \bar{X})^2 = \sum_{i=1}^n (X_i - \mu)^2 - n(\bar{X} - \mu)^2.$$

---

### Lemma 2 — Expected sum of squared deviations from $\mu$

$$\mathbb{E}\!\left[\sum_{i=1}^n (X_i - \mu)^2\right] = n\sigma^2$$

*Proof.* By definition $\operatorname{Var}(X_i) = \mathbb{E}[(X_i - \mu)^2] = \sigma^2$ for each $i$. Linearity of expectation gives the result.

---

### Lemma 3 — Expected squared deviation of the sample mean

$$\mathbb{E}\!\left[(\bar{X} - \mu)^2\right] = \operatorname{Var}(\bar{X}) = \frac{\sigma^2}{n}$$

*Proof.* For i.i.d. variables, $\operatorname{Var}(\bar{X}) = \frac{1}{n^2}\sum_{i=1}^n \operatorname{Var}(X_i) = \frac{n\sigma^2}{n^2} = \frac{\sigma^2}{n}$. Since $\mathbb{E}[\bar{X}] = \mu$, we have $\mathbb{E}[(\bar{X} - \mu)^2] = \operatorname{Var}(\bar{X})$.

---

### Lemma 4 — Expected sum of squared deviations from $\bar{X}$

$$\mathbb{E}\!\left[\sum_{i=1}^n (X_i - \bar{X})^2\right] = (n-1)\sigma^2$$

*Proof.* Take expectations of Lemma 1 and substitute Lemmas 2 and 3:

$$
\begin{aligned}
\mathbb{E}\!\left[\sum_{i=1}^n (X_i - \bar{X})^2\right]
&= \mathbb{E}\!\left[\sum_{i=1}^n (X_i - \mu)^2\right] - n\,\mathbb{E}\!\left[(\bar{X} - \mu)^2\right] \\[4pt]
&= n\sigma^2 - n\cdot\frac{\sigma^2}{n} \\[4pt]
&= (n-1)\sigma^2.
\end{aligned}
$$

---

### Lemma 5 — Unbiasedness of $s^2$ and bias of $\hat{\sigma}^2$

$$\mathbb{E}[s^2] = \sigma^2, \qquad \mathbb{E}[\hat{\sigma}^2] = \frac{n-1}{n}\sigma^2 = \sigma^2 - \frac{\sigma^2}{n}$$

*Proof.* From Lemma 4 and the definitions:

$$
\mathbb{E}[s^2] = \mathbb{E}\!\left[\frac{1}{n-1}\sum_{i=1}^n (X_i - \bar{X})^2\right]
= \frac{(n-1)\sigma^2}{n-1} = \sigma^2.
$$

$$
\mathbb{E}[\hat{\sigma}^2] = \mathbb{E}\!\left[\frac{1}{n}\sum_{i=1}^n (X_i - \bar{X})^2\right]
= \frac{(n-1)\sigma^2}{n} = \sigma^2 - \frac{\sigma^2}{n}.
$$

Thus $s^2$ is unbiased, while $\hat{\sigma}^2$ systematically underestimates $\sigma^2$ by $\sigma^2/n$.

## Verification

SymPy symbolic verification confirms every algebraic step:

```
E[Σ(X_i - X̄)²] = σ²·(n - 1)
E[s²] = E[Σ(X_i - X̄)²/(n-1)] = σ²          ✓ unbiased
E[σ̂²] = E[Σ(X_i - X̄)²/n] = σ² - σ²/n      ✓ biased downward
```

The key insight: the sample mean $\bar{X}$ is "closer" to the data than the true mean $\mu$ is, because $\bar{X}$ is itself computed from the same data. Specifically, $\sum (X_i - \bar{X})^2 \le \sum (X_i - \mu)^2$, with the gap being exactly $n(\bar{X} - \mu)^2$. Dividing by $n$ would therefore undercount the true variability. The correction factor $n-1$, known as **Bessel's correction**, compensates for this exactly.

## Assumptions Used

| Assumption | Justification |
|---|---|
| $X_1,\dots,X_n$ are i.i.d. | Standard statistical inference setting |
| $\mathbb{E}[X_i] = \mu$ exists | Finite first moment |
| $\operatorname{Var}(X_i) = \sigma^2$ exists and is finite | Finite second moment |
| $n \ge 2$ | Otherwise division by $n-1$ is undefined |

## Remaining Limits

- The derivation assumes **finite second moments**. For heavy-tailed distributions without a finite variance, Bessel's correction is not meaningful.
- The proof establishes **unbiasedness** only — it does not address **efficiency** (minimum variance among unbiased estimators) or other optimality properties. In fact, for normal data, the unbiased estimator $s^2$ is not the minimum MSE estimator; the biased MLE $\hat{\sigma}^2$ has lower mean-squared error.
- The derivation does not cover the **degrees of freedom** interpretation (one degree lost by estimating $\mu$), though this offers helpful intuition: with $n$ data points and 1 estimated parameter, $n-1$ independent "pieces of information" remain for estimating variance.


## Progress

Synthesizing final answer


## monitor_summary

- The derivation is verified and the solution is complete; no further analysis needed.
- The MATHS workflow is at the final verification step, ready to present the answer.


## evo_progress

{"pct": 80, "conf": 48}


## Progress

Groundedness check: deterministic ledger pass, no unstructured evidence.


## evo_progress

{"pct": 80, "conf": 48}


## Final Synthesis

## Status
SOLVED

## Direct Answer

The sample variance uses denominator $n-1$ (not $n$) to make it an **unbiased estimator** of the population variance $\sigma^2$. The estimator $s^2 = \frac{1}{n-1}\sum_{i=1}^n (X_i - \bar{X})^2$ satisfies $\mathbb{E}[s^2] = \sigma^2$, whereas the naive estimator $\hat{\sigma}^2 = \frac{1}{n}\sum_{i=1}^n (X_i - \bar{X})^2$ satisfies $\mathbb{E}[\hat{\sigma}^2] = \frac{n-1}{n}\sigma^2 = \sigma^2 - \frac{\sigma^2}{n}$, systematically underestimating the population variance by $\sigma^2/n$.


## Problem Model

| Object | Definition |
|---|---|
| $X_1,\dots,X_n$ | i.i.d. random variables, $\mathbb{E}[X_i]=\mu$, $\operatorname{Var}(X_i)=\sigma^2$ |
| $\bar{X}$ | Sample mean: $\displaystyle \bar{X} = \frac{1}{n}\sum_{i=1}^n X_i$ |
| $\hat{\sigma}^2$ | Biased sample variance: $\displaystyle \hat{\sigma}^2 = \frac{1}{n}\sum_{i=1}^n (X_i-\bar{X})^2$ |
| $s^2$ | Unbiased sample variance: $\displaystyle s^2 = \frac{1}{n-1}\sum_{i=1}^n (X_i-\bar{X})^2$ |

**Target:** Show $\mathbb{E}[s^2] = \sigma^2$ and $\mathbb{E}[\hat{\sigma}^2] = \frac{n-1}{n}\sigma^2$.

## Mathematical Argument

The proof proceeds through five lemmas.

---

### Lemma 1 — Algebraic decomposition

$$\sum_{i=1}^n (X_i - \bar{X})^2 = \sum_{i=1}^n (X_i - \mu)^2 \;-\; n(\bar{X} - \mu)^2$$

*Proof.* Write $X_i - \bar{X} = (X_i - \mu) - (\bar{X} - \mu)$. Then

$$
\begin{aligned}
\sum_{i=1}^n (X_i - \bar{X})^2
&= \sum_{i=1}^n \big[(X_i - \mu) - (\bar{X} - \mu)\big]^2 \\
&= \sum_{i=1}^n (X_i - \mu)^2 - 2(\bar{X} - \mu)\sum_{i=1}^n (X_i - \mu) + n(\bar{X} - \mu)^2.
\end{aligned}
$$

Since $\sum_{i=1}^n (X_i - \mu) = n(\bar{X} - \mu)$, the cross term becomes $-2n(\bar{X} - \mu)^2$, giving

$$\sum_{i=1}^n (X_i - \bar{X})^2 = \sum_{i=1}^n (X_i - \mu)^2 - n(\bar{X} - \mu)^2.$$

---

### Lemma 2 — Expected sum of squared deviations from $\mu$

$$\mathbb{E}\!\left[\sum_{i=1}^n (X_i - \mu)^2\right] = n\sigma^2$$

*Proof.* By definition $\operatorname{Var}(X_i) = \mathbb{E}[(X_i - \mu)^2] = \sigma^2$ for each $i$. Linearity of expectation gives the result.

---

### Lemma 3 — Expected squared deviation of the sample mean

$$\mathbb{E}\!\left[(\bar{X} - \mu)^2\right] = \operatorname{Var}(\bar{X}) = \frac{\sigma^2}{n}$$

*Proof.* For i.i.d. variables, $\operatorname{Var}(\bar{X}) = \frac{1}{n^2}\sum_{i=1}^n \operatorname{Var}(X_i) = \frac{n\sigma^2}{n^2} = \frac{\sigma^2}{n}$. Since $\mathbb{E}[\bar{X}] = \mu$, we have $\mathbb{E}[(\bar{X} - \mu)^2] = \operatorname{Var}(\bar{X})$.

---

### Lemma 4 — Expected sum of squared deviations from $\bar{X}$

$$\mathbb{E}\!\left[\sum_{i=1}^n (X_i - \bar{X})^2\right] = (n-1)\sigma^2$$

*Proof.* Take expectations of Lemma 1 and substitute Lemmas 2 and 3:

$$
\begin{aligned}
\mathbb{E}\!\left[\sum_{i=1}^n (X_i - \bar{X})^2\right]
&= \mathbb{E}\!\left[\sum_{i=1}^n (X_i - \mu)^2\right] - n\,\mathbb{E}\!\left[(\bar{X} - \mu)^2\right] \\[4pt]
&= n\sigma^2 - n\cdot\frac{\sigma^2}{n} \\[4pt]
&= (n-1)\sigma^2.
\end{aligned}
$$

---

### Lemma 5 — Unbiasedness of $s^2$ and bias of $\hat{\sigma}^2$

$$\mathbb{E}[s^2] = \sigma^2, \qquad \mathbb{E}[\hat{\sigma}^2] = \frac{n-1}{n}\sigma^2 = \sigma^2 - \frac{\sigma^2}{n}$$

*Proof.* From Lemma 4 and the definitions:

$$
\mathbb{E}[s^2] = \mathbb{E}\!\left[\frac{1}{n-1}\sum_{i=1}^n (X_i - \bar{X})^2\right]
= \frac{(n-1)\sigma^2}{n-1} = \sigma^2.
$$

$$
\mathbb{E}[\hat{\sigma}^2] = \mathbb{E}\!\left[\frac{1}{n}\sum_{i=1}^n (X_i - \bar{X})^2\right]
= \frac{(n-1)\sigma^2}{n} = \sigma^2 - \frac{\sigma^2}{n}.
$$

Thus $s^2$ is unbiased, while $\hat{\sigma}^2$ systematically underestimates $\sigma^2$ by $\sigma^2/n$.

## Verification

SymPy symbolic verification confirms every algebraic step:

```
E[Σ(X_i - X̄)²] = σ²·(n - 1)
E[s²] = E[Σ(X_i - X̄)²/(n-1)] = σ²          ✓ unbiased
E[σ̂²] = E[Σ(X_i - X̄)²/n] = σ² - σ²/n      ✓ biased downward
```

The key insight: the sample mean $\bar{X}$ is "closer" to the data than the true mean $\mu$ is, because $\bar{X}$ is itself computed from the same data. Specifically, $\sum (X_i - \bar{X})^2 \le \sum (X_i - \mu)^2$, with the gap being exactly $n(\bar{X} - \mu)^2$. Dividing by $n$ would therefore undercount the true variability. The correction factor $n-1$, known as **Bessel's correction**, compensates for this exactly.

## Assumptions Used

| Assumption | Justification |
|---|---|
| $X_1,\dots,X_n$ are i.i.d. | Standard statistical inference setting |
| $\mathbb{E}[X_i] = \mu$ exists | Finite first moment |
| $\operatorname{Var}(X_i) = \sigma^2$ exists and is finite | Finite second moment |
| $n \ge 2$ | Otherwise division by $n-1$ is undefined |

## Remaining Limits

- The derivation assumes **finite second moments**. For heavy-tailed distributions without a finite variance, Bessel's correction is not meaningful.
- The proof establishes **unbiasedness** only — it does not address **efficiency** (minimum variance among unbiased estimators) or other optimality properties. In fact, for normal data, the unbiased estimator $s^2$ is not the minimum MSE estimator; the biased MLE $\hat{\sigma}^2$ has lower mean-squared error.
- The derivation does not cover the **degrees of freedom** interpretation (one degree lost by estimating $\mu$), though this offers helpful intuition: with $n$ data points and 1 estimated parameter, $n-1$ independent "pieces of information" remain for estimating variance.

---
**[EVO gates: SOLVED - no gates triggered]**


---
Finished at `2026-07-02T06:48:52`
