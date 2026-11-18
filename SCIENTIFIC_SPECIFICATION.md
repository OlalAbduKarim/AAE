# ANALYTICA AUTONOMOUS ENGINE
## Scientific Knowledge and Reasoning Specification

**Version:** 0.1  
**Status:** Initial engineering specification  
**Parent document:** MASTER_ARCHITECTURE.md

---

## 1. Purpose

This document defines the statistical knowledge, mathematical reasoning and scientific decision-making capabilities required by AAE.

AAE must not merely recognise statistical methods by name. It must understand the conditions under which methods are appropriate, their assumptions, their mathematical foundations, their limitations and the consequences of violating those assumptions.

Its scientific reasoning must combine:

- Learned statistical knowledge.
- Formal mathematical relationships.
- Structured scientific knowledge.
- Statistical diagnostics.
- Evidence from actual data.
- Independent verification.

The ultimate objective is defensible analytical decisions, not simply successful execution of statistical software.

## 2. Scientific knowledge representation

AAE must represent statistical knowledge in a structured, machine-readable form.

Each statistical method must have a knowledge record containing:

1. Method identifier and name.
2. Analytical purpose.
3. Research questions it can answer.
4. Required input variables.
5. Variable measurement scales.
6. Applicable study designs.
7. Sample structure requirements.
8. Mathematical assumptions.
9. Diagnostic procedures.
10. Computation requirements.
11. Expected outputs.
12. Interpretation rules.
13. Effect-size measures where applicable.
14. Known limitations.
15. Alternative methods.
16. Conditions under which the method must be rejected.

Knowledge must also capture relationships between methods, assumptions, distributions, variables and research objectives.

The system should eventually support a statistical knowledge graph and a formal constraint-reasoning mechanism.

## 3. Statistical knowledge domains

AAE must progressively develop competence in the following domains.

### Domain A: Data foundations

- Data types and measurement scales.
- Population and sample.
- Sampling methods.
- Data structures.
- Missing observations.
- Outliers and influential observations.
- Data distributions.
- Data quality and measurement error.
- Data transformations.
- Sampling and selection bias.

### Domain B: Probability and mathematical statistics

- Probability theory.
- Conditional probability.
- Bayes' theorem.
- Random variables.
- Probability distributions.
- Expectation and variance.
- Joint and marginal distributions.
- Sampling distributions.
- Central limit theorem.
- Law of large numbers.
- Mathematical estimation.

### Domain C: Descriptive and exploratory analysis

- Measures of central tendency.
- Measures of dispersion.
- Quantiles and percentiles.
- Distribution shape.
- Cross-tabulation.
- Correlation.
- Group comparisons.
- Exploratory visualisation.

### Domain D: Statistical inference

- Point estimation.
- Standard errors.
- Confidence intervals.
- Hypothesis testing.
- Type I and Type II errors.
- Statistical power.
- P-values.
- Effect sizes.
- Multiple testing corrections.
- Parametric and nonparametric inference.

### Domain E: Comparative analysis

- One-sample tests.
- Independent-sample tests.
- Paired-sample tests.
- Welch procedures.
- Analysis of variance.
- Chi-square tests.
- Fisher's exact test.
- Rank-based procedures.
- Repeated-measures comparisons.
- Post-hoc comparisons.

### Domain F: Regression and predictive modelling

- Simple and multiple linear regression.
- Logistic regression.
- Generalised linear models.
- Count regression.
- Regularisation.
- Model selection.
- Residual analysis.
- Multicollinearity.
- Model calibration.
- Predictive evaluation.

### Domain G: Advanced statistical analysis

- Multivariate statistics.
- Bayesian inference.
- Time-series analysis.
- Survival analysis.
- Missing-data mechanisms and methods.
- Complex survey analysis.
- Clustered and hierarchical data.
- Experimental design.
- Causal inference.
- Machine learning.

These domains form the long-term knowledge scope. They are not all implementation requirements for the first release.

## 4. Method suitability reasoning

AAE must evaluate analytical methods against the actual research situation.

The evaluation must consider:

- Research objective.
- Outcome variable.
- Predictor or grouping variables.
- Measurement scales.
- Number of groups or conditions.
- Independent or dependent observations.
- Sampling structure.
- Distributional characteristics.
- Sample size.
- Missing-data patterns.
- Relevant assumptions.
- Intended interpretation.

For every candidate method, AAE must produce:

- Suitability assessment.
- Supporting evidence.
- Assumptions requiring examination.
- Known violations or uncertainties.
- Alternative methods.
- Final recommendation.

A method must not be selected merely because it is frequently used for a particular type of question.

## 5. Assumption reasoning

Assumptions must be represented individually rather than as a single pass/fail label.

For example, an analysis may require consideration of:

- Independence of observations.
- Linearity.
- Homoscedasticity.
- Normality of residuals.
- Distributional assumptions.
- Appropriate sample structure.
- Absence of problematic multicollinearity.

AAE must distinguish:

1. Assumption supported by available evidence.
2. Assumption showing evidence of violation.
3. Assumption not adequately assessed.
4. Assumption that cannot be established from the available data.

Statistical tests must not be treated as automatic proof that assumptions hold.

A failed diagnostic does not automatically mean every alternative is valid. The engine must consider the severity, context and implications of the violation.

## 6. Scientific decision framework

Every analytical decision must be assigned one of three outcomes.

### PROCEED

The requested analysis is sufficiently specified and scientifically defensible.

### REVIEW REQUIRED

Additional information, diagnostic assessment, user clarification or approval is necessary.

### REJECT

The requested method is fundamentally inappropriate for the stated objective or the available evidence cannot support the requested conclusion.

AAE must explain its decision and identify what would be needed to proceed where possible.

## 7. Mathematical and numerical integrity

All numerical results must be produced by established scientific computation procedures.

AAE must maintain mathematical consistency across related results.

Examples include:

- Confidence intervals must correspond to the stated estimator and confidence level.
- Standard errors must correspond to the estimation procedure.
- Test statistics must correspond to the specified null hypothesis.
- Degrees of freedom must be appropriate to the method.
- Effect sizes must use appropriate definitions.
- Regression predictions and diagnostic results must be consistent with the fitted model.

Independent verification must use a genuinely independent calculation or reference where feasible.

## 8. Evidence and uncertainty

AAE must distinguish facts, estimates, assumptions and interpretations.

Every important conclusion must be traceable to:

- The dataset.
- The analytical method.
- The computed result.
- The relevant diagnostic.
- The supporting scientific rule.

The engine must communicate uncertainty honestly.

It must never convert an inconclusive result into proof of no effect, or interpret association as causation without a defensible causal design.

## 9. Benchmark requirements

Scientific competence must be measured using known-answer problems and expert-reviewed scenarios.

The benchmark library must include:

- Correctly specified analytical problems.
- Ambiguous research questions.
- Inappropriate method requests.
- Violated assumptions.
- Small samples.
- Unequal group sizes.
- Missing observations.
- Paired and independent designs.
- Clustered observations.
- Confounding and causal inference traps.
- Multiple-comparison problems.

Evaluation must measure:

1. Method selection accuracy.
2. Invalid recommendation rate.
3. Recognition of insufficient information.
4. Assumption assessment accuracy.
5. Numerical calculation accuracy.
6. Interpretation correctness.
7. Ability to recognise when analysis must stop.

Benchmark problems must be kept separate from model training data.

## 10. Initial implementation priority

The first scientific implementation should focus on a manageable but rigorous analytical scope:

1. Data types and measurement scales.
2. Dataset profiling.
3. Descriptive statistics.
4. Probability distributions.
5. Confidence intervals.
6. One-sample and two-sample inference.
7. Paired and independent comparisons.
8. Correlation.
9. Chi-square analysis.
10. Linear and logistic regression.
11. Assumption diagnostics.
12. Numerical verification.

Advanced domains will be added incrementally after the foundations pass their benchmarks.

## 11. Acceptance criteria

The scientific knowledge system is not complete merely because its method records exist.

It must demonstrate that it can:

- Distinguish research objectives.
- Identify relevant variables and study designs.
- Generate appropriate candidate methods.
- Explain method suitability.
- Detect assumption problems.
- Identify insufficient information.
- Reject scientifically invalid requests.
- Produce mathematically consistent results.
- Explain limitations and uncertainty.

**END OF SCIENTIFIC SPECIFICATION**