---
layout: default
title: "Chapter 25: IRT Scoring Deep Dive"
parent: "Part VI: Scoring Methodologies"
nav_order: 2
---

# IRT Scoring Deep Dive

### Learning Objectives

By the end of this chapter, you will be able to:

1. Explain the mathematical foundations of IRT models, including the logistic function
2. Interpret Item Characteristic Curves (ICCs) and understand their practical implications
3. Differentiate between 1PL (Rasch), 2PL, and 3PL models and their parameters
4. Understand Thurstonian IRT for forced-choice personality data
5. Explain the Test Information Function and its role in defining precision
6. Describe theta estimation procedures (maximum likelihood, Bayesian methods)

### The Mathematical Foundation: The Logistic Function

At the heart of IRT is a mathematical function that models the probability of a correct response (for ability tests) or endorsement (for personality items) as a function of the candidate's latent trait level (theta, θ).

The most common formulation is the **2-parameter logistic (2PL) model**:

**P(θ) = 1 / (1 + exp(-a(θ - b)))**

Where:
- **P(θ)** = Probability of a correct response (or endorsement) for a candidate with ability/trait level θ
- **a** = Discrimination parameter (how well the item differentiates between adjacent ability levels)
- **b** = Difficulty parameter (the theta value where P(θ) = 0.50)
- **exp** = Exponential function (e^x)

This equation produces an S-shaped curve known as the **Item Characteristic Curve (ICC)**.

#### Interpreting the Item Characteristic Curve

The ICC graphically represents the relationship between theta (x-axis) and probability of correct response (y-axis, ranging from 0 to 1).

**Key features**:

1. **Lower Asymptote**: For ability tests without guessing, the curve approaches 0 at very low theta values (candidates with very low ability have near-zero probability of answering correctly).

2. **Upper Asymptote**: The curve approaches 1 at very high theta values (candidates with very high ability have near-certain probability of answering correctly).

3. **Inflection Point**: The steepest part of the curve occurs at θ = b (the difficulty parameter). This is where the item provides maximum information—it effectively differentiates candidates just below and just above this ability level.

4. **Slope**: The steepness of the curve at the inflection point is determined by the discrimination parameter (a). High discrimination (steep curve) means the item sharply distinguishes between candidates with similar ability. Low discrimination (flat curve) means the item provides little differentiating information.

**Example**:
- Item A: a = 1.5, b = 0.0
  - This item has high discrimination and medium difficulty (difficulty at the population mean).
  - A candidate with θ = -1.0 has approximately 18% probability of answering correctly.
  - A candidate with θ = 0.0 has 50% probability.
  - A candidate with θ = 1.0 has approximately 82% probability.

- Item B: a = 0.5, b = 0.0
  - This item has low discrimination and medium difficulty.
  - A candidate with θ = -1.0 has approximately 38% probability of answering correctly.
  - A candidate with θ = 0.0 has 50% probability.
  - A candidate with θ = 1.0 has approximately 62% probability.
  - Notice the probabilities are much more similar across theta levels—the item differentiates poorly.

### IRT Model Variants: 1PL, 2PL, and 3PL

#### 1-Parameter Logistic Model (1PL / Rasch Model)

The Rasch model, developed by Danish mathematician Georg Rasch, is the simplest IRT model. It constrains all items to have equal discrimination (a = 1.0 for all items), estimating only the difficulty parameter (b).

**P(θ) = 1 / (1 + exp(-(θ - b)))**

**Advantages**:
- Mathematical elegance and simplicity
- Strong theoretical properties (sufficient statistics, specific objectivity)
- Easier calibration with smaller samples

**Disadvantages**:
- The equal-discrimination assumption is often violated in real data
- Poor model fit when items vary substantially in their ability to differentiate

**SHL's Experience**: During Verify development, SHL tested the Rasch model and found it fit poorly. Real test items exhibited substantial variation in discrimination, violating the model's core assumption. The Rasch model was rejected in favor of 2PL.

#### 2-Parameter Logistic Model (2PL)

The 2PL model estimates both difficulty (b) and discrimination (a) for each item, providing greater flexibility and typically better fit to real data.

**P(θ) = 1 / (1 + exp(-a(θ - b)))**

**Advantages**:
- Accommodates variation in item quality (discrimination)
- Better model fit for most real-world tests
- Allows identification and removal of poor items (low discrimination)

**Disadvantages**:
- Requires larger calibration samples (typically 500+ candidates)
- More complex estimation algorithms

**SHL's Choice**: The 2PL model was selected for Verify verbal and numerical item banks, providing robust fit and enabling effective adaptive testing algorithms.

**Parameter Estimation**:
- **a-parameter (discrimination)**: Typically ranges from 0.5 to 2.5. Values below 0.5 indicate poor items (candidates' responses are weakly related to their ability). Values above 2.0 indicate highly diagnostic items.
- **b-parameter (difficulty)**: Typically ranges from -3.0 to +3.0 on the theta scale. Items with b < -2.0 are very easy (even low-ability candidates answer correctly). Items with b > 2.0 are very hard (only high-ability candidates answer correctly).

**Item Screening**: During Verify development, items with low discrimination (a < 0.5) or extreme difficulty values (b outside the -3 to +3 range) were rejected, ensuring the retained item banks provide reliable measurement across the intended ability spectrum.

#### 3-Parameter Logistic Model (3PL)

The 3PL model adds a third parameter to account for guessing on multiple-choice items:

**P(θ) = c + (1 - c) × [1 / (1 + exp(-a(θ - b)))]**

Where:
- **c** = Lower asymptote (guessing parameter), representing the probability that a very low-ability candidate answers correctly by chance.

For a 4-option multiple-choice item, the guessing parameter theoretically approaches 0.25 (25% chance).

**Advantages**:
- More realistic for multiple-choice tests where guessing is possible
- Can improve model fit for easy items

**Disadvantages**:
- Requires even larger calibration samples (1000+ candidates)
- Estimation can be unstable, especially for the c-parameter
- Adds complexity without always improving practical utility

**SHL's Experience**: During Verify development, SHL tested 3PL models but found they offered **no substantial improvement over 2PL for most items**. Approximately 90% of items fit the 2PL model adequately. The additional complexity of estimating and maintaining guessing parameters was deemed unnecessary. SHL selected 2PL as the standard for verbal and numerical item banks.

### Thurstonian IRT for Forced-Choice Personality Data

The traditional IRT models described above were developed for dichotomous items (correct/incorrect) and later extended to polytomous items (Likert scales). However, forced-choice personality items—where respondents choose between statements (e.g., "I enjoy working with numbers" vs. "I enjoy working with people")—present a fundamentally different response structure.

Forced-choice data are **ipsative** (relative rankings), not **normative** (absolute ratings). Classical IRT models fail when applied to ipsative data because the constant-sum constraint violates independence assumptions.

#### The Thurstonian IRT Breakthrough

Brown and Maydeu-Olivares (2011) developed Thurstonian IRT models that specifically handle forced-choice data by modeling the *comparison process* underlying the respondent's choice.

**Core Logic**:
1. Each trait has a latent level (θ) for the respondent.
2. When presented with two statements (one measuring Trait A, one measuring Trait B), the respondent implicitly compares their latent levels on both traits.
3. The choice reflects which latent level is higher, adjusted for item parameters (how well each statement represents its trait).
4. By analyzing the pattern of choices across many forced-choice blocks, the algorithm can estimate the absolute (normative-equivalent) theta for each trait.

**The Multi-Unidimensional Pairwise Preference (MUPP) Model**:

The MUPP model, used in OPQ32r, extends this logic to triplet forced-choice items (three statements, select "most like me" and "least like me"). Each triplet generates three pairwise comparisons (A vs. B, A vs. C, B vs. C). The model simultaneously estimates theta for all 32 traits by analyzing all pairwise comparisons across all 104 blocks.

**Mathematical Complexity**: The Thurstonian IRT models involve multidimensional integration and are computationally intensive, requiring specialized software and algorithms. Maximum likelihood estimation is impractical for high-dimensional models, so Bayesian estimation (Markov Chain Monte Carlo, MCMC) is typically used.

**SHL's Implementation**:
- The OPQ32r contains 104 triplet blocks, yielding 312 pairwise comparisons.
- The algorithm estimates 32 trait thetas simultaneously.
- The resulting theta estimates are highly correlated (r ≈ 0.7–0.8) with scores from normative versions of the OPQ, demonstrating successful recovery of absolute trait standing.
- Marginal reliability (the IRT equivalent of Cronbach's alpha) exceeds 0.80 for most traits, confirming strong measurement precision.

**Outcome**: Thurstonian IRT solved the decades-old problem of ipsative scoring, allowing forced-choice personality tests to produce scores suitable for between-person comparison while retaining resistance to faking. This methodological innovation is cited as a significant advancement in personality assessment.

### The Test Information Function: Defining Precision

IRT introduces the concept of the **Test Information Function (TIF)**, which quantifies how much information (precision) a test provides at each point along the theta scale.

**Information (I)** is mathematically defined as:

**I(θ) = Σ [P'(θ)]² / [P(θ) × (1 - P(θ))]**

Where:
- **P'(θ)** = First derivative of the ICC (the slope of the curve at theta)
- The summation is across all items in the test

**Key Insights**:

1. **Information is highest where ICCs are steepest**: Items with high discrimination (steep slopes) provide more information than items with low discrimination.

2. **Information is highest near item difficulty**: An item provides maximum information at θ = b (its difficulty parameter). Easy items provide information about low-ability candidates; hard items provide information about high-ability candidates.

3. **Information accumulates across items**: The total test information is the sum of individual item information functions.

4. **Standard Error of Measurement (SEM) is the inverse of information**:

**SEM(θ) = 1 / √I(θ)**

Higher information = lower SEM = more precise measurement.

**Practical Implication**: By examining the TIF, test developers can identify the ability range where the test measures most precisely and where measurement is weakest. A well-designed test has high information across the intended ability range.

**Example**:
- A test designed for managerial selection should have high information at θ = 0.5 to 2.0 (above-average to very high ability), where most managerial candidates fall.
- If the TIF shows low information at θ = 1.5, the test will have large SEMs for above-average candidates, reducing decision accuracy.
- Test developers can add more items with b ≈ 1.5 to increase information in that range.

### Computer Adaptive Testing (CAT) and the Information Function

The Test Information Function is central to adaptive testing algorithms. In CAT, the system selects the next item in real-time to **maximize information** at the candidate's current estimated theta.

**CAT Algorithm** (simplified):

1. **Start**: Begin with a medium-difficulty item (b ≈ 0) or use prior information (e.g., education level) to set an initial theta estimate.

2. **Update Theta**: After the candidate responds, update the theta estimate using maximum likelihood or Bayesian methods.

3. **Select Next Item**: From the remaining item bank, select the item that provides maximum information at the current theta estimate. For 2PL models, this is typically the item with b closest to the current theta estimate and high discrimination (a).

4. **Iterate**: Repeat steps 2-3 until a stopping criterion is met (e.g., SEM falls below a threshold, a fixed number of items is administered, or a time limit is reached).

5. **Finalize**: Calculate the final theta estimate and SEM.

**Result**: CAT achieves the same measurement precision as a fixed-form test with **50% fewer items** because every item is optimally matched to the candidate's ability level. No items are wasted on being too easy or too hard.

**SHL's Verify Implementation**: Verify tests use CAT algorithms to adapt item difficulty in real-time. This produces:
- **Efficiency**: Tests are shorter (typically 20-25 items instead of 40-50), improving candidate experience.
- **Security**: Each candidate receives a unique sequence of items, making it difficult to share answers.
- **Precision**: Measurement precision is maximized where it matters most—around cutoff scores used for selection decisions.

### Theta Estimation Methods

IRT models estimate theta (the candidate's latent ability) using statistical inference. Two primary methods are used:

#### 1. **Maximum Likelihood Estimation (MLE)**

MLE selects the theta value that maximizes the likelihood of observing the candidate's specific response pattern.

**Logic**:
- Given the item parameters (a, b) and the candidate's responses (correct/incorrect or endorsement pattern), calculate the likelihood (probability) of those responses for every possible theta value.
- The theta with the highest likelihood is the MLE estimate.

**Advantages**:
- Conceptually straightforward
- Asymptotically unbiased (estimate approaches true value with large numbers of items)

**Disadvantages**:
- Undefined for extreme response patterns (e.g., all items answered correctly or all incorrect)
- Can be unstable with short tests or atypical response patterns

**SHL's Use**: MLE is used during CAT for interim theta estimates as candidates progress through items.

#### 2. **Bayesian Estimation (Expected A Posteriori, EAP)**

Bayesian methods incorporate **prior information** about the distribution of theta in the population (typically assumed to be normal with mean = 0, SD = 1). The estimate is a weighted average of the likelihood and the prior.

**Logic**:
- Start with a prior distribution (e.g., theta ~ Normal(0, 1)).
- Update the distribution using the candidate's responses (likelihood).
- The final estimate (EAP) is the mean of the posterior distribution.

**Advantages**:
- Always defined, even for extreme response patterns
- More stable with short tests
- Can incorporate population-level information (e.g., "most managerial candidates have theta between 0 and 2")

**Disadvantages**:
- Slightly biased toward the population mean (shrinkage)
- Requires assumptions about the prior distribution

**SHL's Use**: Bayesian methods (specifically MCMC) are used for Thurstonian IRT estimation in the OPQ32r due to the computational complexity of high-dimensional models.

### Precision Across the Ability Range: An Example

Consider two candidates taking a Verify Numerical Reasoning test:

**Candidate A (Low Ability)**:
- Estimated theta = -1.5
- The adaptive algorithm presented items with b = -1.8 to -1.2 (easy items).
- Candidate answered some correctly, some incorrectly.
- Final SEM(θ) = 0.28
- 95% Confidence Interval: -2.05 to -0.95

**Candidate B (High Ability)**:
- Estimated theta = 1.8
- The adaptive algorithm presented items with b = 1.5 to 2.1 (hard items).
- Candidate answered most correctly.
- Final SEM(θ) = 0.25
- 95% Confidence Interval: 1.31 to 2.29

**Candidate C (Extreme High Ability)**:
- Estimated theta = 2.8
- The adaptive algorithm ran out of sufficiently hard items (item bank b-values capped at 2.5).
- Candidate answered all items correctly (ceiling effect).
- Final SEM(θ) = 0.45 (higher due to poor item matching)
- 95% Confidence Interval: 1.92 to 3.68

**Interpretation**: IRT provides individual-level precision estimates, revealing that Candidate C's score is less precise due to ceiling effects. This information can guide decisions (e.g., recommending a more advanced test or a work sample).

### Key Takeaways

1. **The 2PL model** is the foundation of SHL Verify scoring, estimating item difficulty (b) and discrimination (a) to model the probability of correct responses as a function of latent ability (theta).

2. **Item Characteristic Curves (ICCs)** graphically represent the item-theta relationship, with steeper curves indicating better discrimination and the inflection point representing item difficulty.

3. **SHL selected the 2PL model** after empirical testing showed the Rasch model (1PL) fit poorly and the 3PL model offered no practical advantage for most items.

4. **Thurstonian IRT models** (specifically MUPP) enable the OPQ32r to extract normative-equivalent trait scores from forced-choice (ipsative) data, solving a decades-old psychometric problem.

5. **The Test Information Function (TIF)** defines where a test measures precisely (high information = low SEM) and where it measures poorly (low information = high SEM), enabling rational test design.

6. **Computer Adaptive Testing (CAT)** exploits the TIF by selecting items that maximize information at the candidate's estimated theta, achieving 50% efficiency gains over fixed-form tests.

7. **Theta estimation** uses maximum likelihood or Bayesian methods to infer latent ability from response patterns, with individual-level SEMs providing realistic confidence intervals.

8. **Understanding IRT mechanics** enables practitioners to explain why adaptive tests are shorter, why some candidates' scores are more precise than others, and why forced-choice personality tests can produce normative scores.

---

## Chapter Navigation

[← Previous: Chapter 24 - Classical Test Theory vs Item Response Theory](/psychometric-guide/chapters/24-ctt-vs-irt/)

[Next: Chapter 26 - Normative Data Strategies →](/psychometric-guide/chapters/26-normative-data/)

[↑ Back to Home](/psychometric-guide/)


### Learning Objectives

By the end of this chapter, you will be able to:

1. Explain the mathematical foundations of IRT models, including the logistic function
2. Interpret Item Characteristic Curves (ICCs) and understand their practical implications
3. Differentiate between 1PL (Rasch), 2PL, and 3PL models and their parameters
4. Understand Thurstonian IRT for forced-choice personality data
5. Explain the Test Information Function and its role in defining precision
6. Describe theta estimation procedures (maximum likelihood, Bayesian methods)

### The Mathematical Foundation: The Logistic Function

At the heart of IRT is a mathematical function that models the probability of a correct response (for ability tests) or endorsement (for personality items) as a function of the candidate's latent trait level (theta, θ).

The most common formulation is the **2-parameter logistic (2PL) model**:

**P(θ) = 1 / (1 + exp(-a(θ - b)))**

Where:
- **P(θ)** = Probability of a correct response (or endorsement) for a candidate with ability/trait level θ
- **a** = Discrimination parameter (how well the item differentiates between adjacent ability levels)
- **b** = Difficulty parameter (the theta value where P(θ) = 0.50)
- **exp** = Exponential function (e^x)

This equation produces an S-shaped curve known as the **Item Characteristic Curve (ICC)**.

#### Interpreting the Item Characteristic Curve

The ICC graphically represents the relationship between theta (x-axis) and probability of correct response (y-axis, ranging from 0 to 1).

**Key features**:

1. **Lower Asymptote**: For ability tests without guessing, the curve approaches 0 at very low theta values (candidates with very low ability have near-zero probability of answering correctly).

2. **Upper Asymptote**: The curve approaches 1 at very high theta values (candidates with very high ability have near-certain probability of answering correctly).

3. **Inflection Point**: The steepest part of the curve occurs at θ = b (the difficulty parameter). This is where the item provides maximum information—it effectively differentiates candidates just below and just above this ability level.

4. **Slope**: The steepness of the curve at the inflection point is determined by the discrimination parameter (a). High discrimination (steep curve) means the item sharply distinguishes between candidates with similar ability. Low discrimination (flat curve) means the item provides little differentiating information.

**Example**:
- Item A: a = 1.5, b = 0.0
  - This item has high discrimination and medium difficulty (difficulty at the population mean).
  - A candidate with θ = -1.0 has approximately 18% probability of answering correctly.
  - A candidate with θ = 0.0 has 50% probability.
  - A candidate with θ = 1.0 has approximately 82% probability.

- Item B: a = 0.5, b = 0.0
  - This item has low discrimination and medium difficulty.
  - A candidate with θ = -1.0 has approximately 38% probability of answering correctly.
  - A candidate with θ = 0.0 has 50% probability.
  - A candidate with θ = 1.0 has approximately 62% probability.
  - Notice the probabilities are much more similar across theta levels—the item differentiates poorly.

### IRT Model Variants: 1PL, 2PL, and 3PL

#### 1-Parameter Logistic Model (1PL / Rasch Model)

The Rasch model, developed by Danish mathematician Georg Rasch, is the simplest IRT model. It constrains all items to have equal discrimination (a = 1.0 for all items), estimating only the difficulty parameter (b).

**P(θ) = 1 / (1 + exp(-(θ - b)))**

**Advantages**:
- Mathematical elegance and simplicity
- Strong theoretical properties (sufficient statistics, specific objectivity)
- Easier calibration with smaller samples

**Disadvantages**:
- The equal-discrimination assumption is often violated in real data
- Poor model fit when items vary substantially in their ability to differentiate

**SHL's Experience**: During Verify development, SHL tested the Rasch model and found it fit poorly. Real test items exhibited substantial variation in discrimination, violating the model's core assumption. The Rasch model was rejected in favor of 2PL.

#### 2-Parameter Logistic Model (2PL)

The 2PL model estimates both difficulty (b) and discrimination (a) for each item, providing greater flexibility and typically better fit to real data.

**P(θ) = 1 / (1 + exp(-a(θ - b)))**

**Advantages**:
- Accommodates variation in item quality (discrimination)
- Better model fit for most real-world tests
- Allows identification and removal of poor items (low discrimination)

**Disadvantages**:
- Requires larger calibration samples (typically 500+ candidates)
- More complex estimation algorithms

**SHL's Choice**: The 2PL model was selected for Verify verbal and numerical item banks, providing robust fit and enabling effective adaptive testing algorithms.

**Parameter Estimation**:
- **a-parameter (discrimination)**: Typically ranges from 0.5 to 2.5. Values below 0.5 indicate poor items (candidates' responses are weakly related to their ability). Values above 2.0 indicate highly diagnostic items.
- **b-parameter (difficulty)**: Typically ranges from -3.0 to +3.0 on the theta scale. Items with b < -2.0 are very easy (even low-ability candidates answer correctly). Items with b > 2.0 are very hard (only high-ability candidates answer correctly).

**Item Screening**: During Verify development, items with low discrimination (a < 0.5) or extreme difficulty values (b outside the -3 to +3 range) were rejected, ensuring the retained item banks provide reliable measurement across the intended ability spectrum.

#### 3-Parameter Logistic Model (3PL)

The 3PL model adds a third parameter to account for guessing on multiple-choice items:

**P(θ) = c + (1 - c) × [1 / (1 + exp(-a(θ - b)))]**

Where:
- **c** = Lower asymptote (guessing parameter), representing the probability that a very low-ability candidate answers correctly by chance.

For a 4-option multiple-choice item, the guessing parameter theoretically approaches 0.25 (25% chance).

**Advantages**:
- More realistic for multiple-choice tests where guessing is possible
- Can improve model fit for easy items

**Disadvantages**:
- Requires even larger calibration samples (1000+ candidates)
- Estimation can be unstable, especially for the c-parameter
- Adds complexity without always improving practical utility

**SHL's Experience**: During Verify development, SHL tested 3PL models but found they offered **no substantial improvement over 2PL for most items**. Approximately 90% of items fit the 2PL model adequately. The additional complexity of estimating and maintaining guessing parameters was deemed unnecessary. SHL selected 2PL as the standard for verbal and numerical item banks.

### Thurstonian IRT for Forced-Choice Personality Data

The traditional IRT models described above were developed for dichotomous items (correct/incorrect) and later extended to polytomous items (Likert scales). However, forced-choice personality items—where respondents choose between statements (e.g., "I enjoy working with numbers" vs. "I enjoy working with people")—present a fundamentally different response structure.

Forced-choice data are **ipsative** (relative rankings), not **normative** (absolute ratings). Classical IRT models fail when applied to ipsative data because the constant-sum constraint violates independence assumptions.

#### The Thurstonian IRT Breakthrough

Brown and Maydeu-Olivares (2011) developed Thurstonian IRT models that specifically handle forced-choice data by modeling the *comparison process* underlying the respondent's choice.

**Core Logic**:
1. Each trait has a latent level (θ) for the respondent.
2. When presented with two statements (one measuring Trait A, one measuring Trait B), the respondent implicitly compares their latent levels on both traits.
3. The choice reflects which latent level is higher, adjusted for item parameters (how well each statement represents its trait).
4. By analyzing the pattern of choices across many forced-choice blocks, the algorithm can estimate the absolute (normative-equivalent) theta for each trait.

**The Multi-Unidimensional Pairwise Preference (MUPP) Model**:

The MUPP model, used in OPQ32r, extends this logic to triplet forced-choice items (three statements, select "most like me" and "least like me"). Each triplet generates three pairwise comparisons (A vs. B, A vs. C, B vs. C). The model simultaneously estimates theta for all 32 traits by analyzing all pairwise comparisons across all 104 blocks.

**Mathematical Complexity**: The Thurstonian IRT models involve multidimensional integration and are computationally intensive, requiring specialized software and algorithms. Maximum likelihood estimation is impractical for high-dimensional models, so Bayesian estimation (Markov Chain Monte Carlo, MCMC) is typically used.

**SHL's Implementation**:
- The OPQ32r contains 104 triplet blocks, yielding 312 pairwise comparisons.
- The algorithm estimates 32 trait thetas simultaneously.
- The resulting theta estimates are highly correlated (r ≈ 0.7–0.8) with scores from normative versions of the OPQ, demonstrating successful recovery of absolute trait standing.
- Marginal reliability (the IRT equivalent of Cronbach's alpha) exceeds 0.80 for most traits, confirming strong measurement precision.

**Outcome**: Thurstonian IRT solved the decades-old problem of ipsative scoring, allowing forced-choice personality tests to produce scores suitable for between-person comparison while retaining resistance to faking. This methodological innovation is cited as a significant advancement in personality assessment.

### The Test Information Function: Defining Precision

IRT introduces the concept of the **Test Information Function (TIF)**, which quantifies how much information (precision) a test provides at each point along the theta scale.

**Information (I)** is mathematically defined as:

**I(θ) = Σ [P'(θ)]² / [P(θ) × (1 - P(θ))]**

Where:
- **P'(θ)** = First derivative of the ICC (the slope of the curve at theta)
- The summation is across all items in the test

**Key Insights**:

1. **Information is highest where ICCs are steepest**: Items with high discrimination (steep slopes) provide more information than items with low discrimination.

2. **Information is highest near item difficulty**: An item provides maximum information at θ = b (its difficulty parameter). Easy items provide information about low-ability candidates; hard items provide information about high-ability candidates.

3. **Information accumulates across items**: The total test information is the sum of individual item information functions.

4. **Standard Error of Measurement (SEM) is the inverse of information**:

**SEM(θ) = 1 / √I(θ)**

Higher information = lower SEM = more precise measurement.

**Practical Implication**: By examining the TIF, test developers can identify the ability range where the test measures most precisely and where measurement is weakest. A well-designed test has high information across the intended ability range.

**Example**:
- A test designed for managerial selection should have high information at θ = 0.5 to 2.0 (above-average to very high ability), where most managerial candidates fall.
- If the TIF shows low information at θ = 1.5, the test will have large SEMs for above-average candidates, reducing decision accuracy.
- Test developers can add more items with b ≈ 1.5 to increase information in that range.

### Computer Adaptive Testing (CAT) and the Information Function

The Test Information Function is central to adaptive testing algorithms. In CAT, the system selects the next item in real-time to **maximize information** at the candidate's current estimated theta.

**CAT Algorithm** (simplified):

1. **Start**: Begin with a medium-difficulty item (b ≈ 0) or use prior information (e.g., education level) to set an initial theta estimate.

2. **Update Theta**: After the candidate responds, update the theta estimate using maximum likelihood or Bayesian methods.

3. **Select Next Item**: From the remaining item bank, select the item that provides maximum information at the current theta estimate. For 2PL models, this is typically the item with b closest to the current theta estimate and high discrimination (a).

4. **Iterate**: Repeat steps 2-3 until a stopping criterion is met (e.g., SEM falls below a threshold, a fixed number of items is administered, or a time limit is reached).

5. **Finalize**: Calculate the final theta estimate and SEM.

**Result**: CAT achieves the same measurement precision as a fixed-form test with **50% fewer items** because every item is optimally matched to the candidate's ability level. No items are wasted on being too easy or too hard.

**SHL's Verify Implementation**: Verify tests use CAT algorithms to adapt item difficulty in real-time. This produces:
- **Efficiency**: Tests are shorter (typically 20-25 items instead of 40-50), improving candidate experience.
- **Security**: Each candidate receives a unique sequence of items, making it difficult to share answers.
- **Precision**: Measurement precision is maximized where it matters most—around cutoff scores used for selection decisions.

### Theta Estimation Methods

IRT models estimate theta (the candidate's latent ability) using statistical inference. Two primary methods are used:

#### 1. **Maximum Likelihood Estimation (MLE)**

MLE selects the theta value that maximizes the likelihood of observing the candidate's specific response pattern.

**Logic**:
- Given the item parameters (a, b) and the candidate's responses (correct/incorrect or endorsement pattern), calculate the likelihood (probability) of those responses for every possible theta value.
- The theta with the highest likelihood is the MLE estimate.

**Advantages**:
- Conceptually straightforward
- Asymptotically unbiased (estimate approaches true value with large numbers of items)

**Disadvantages**:
- Undefined for extreme response patterns (e.g., all items answered correctly or all incorrect)
- Can be unstable with short tests or atypical response patterns

**SHL's Use**: MLE is used during CAT for interim theta estimates as candidates progress through items.

#### 2. **Bayesian Estimation (Expected A Posteriori, EAP)**

Bayesian methods incorporate **prior information** about the distribution of theta in the population (typically assumed to be normal with mean = 0, SD = 1). The estimate is a weighted average of the likelihood and the prior.

**Logic**:
- Start with a prior distribution (e.g., theta ~ Normal(0, 1)).
- Update the distribution using the candidate's responses (likelihood).
- The final estimate (EAP) is the mean of the posterior distribution.

**Advantages**:
- Always defined, even for extreme response patterns
- More stable with short tests
- Can incorporate population-level information (e.g., "most managerial candidates have theta between 0 and 2")

**Disadvantages**:
- Slightly biased toward the population mean (shrinkage)
- Requires assumptions about the prior distribution

**SHL's Use**: Bayesian methods (specifically MCMC) are used for Thurstonian IRT estimation in the OPQ32r due to the computational complexity of high-dimensional models.

### Precision Across the Ability Range: An Example

Consider two candidates taking a Verify Numerical Reasoning test:

**Candidate A (Low Ability)**:
- Estimated theta = -1.5
- The adaptive algorithm presented items with b = -1.8 to -1.2 (easy items).
- Candidate answered some correctly, some incorrectly.
- Final SEM(θ) = 0.28
- 95% Confidence Interval: -2.05 to -0.95

**Candidate B (High Ability)**:
- Estimated theta = 1.8
- The adaptive algorithm presented items with b = 1.5 to 2.1 (hard items).
- Candidate answered most correctly.
- Final SEM(θ) = 0.25
- 95% Confidence Interval: 1.31 to 2.29

**Candidate C (Extreme High Ability)**:
- Estimated theta = 2.8
- The adaptive algorithm ran out of sufficiently hard items (item bank b-values capped at 2.5).
- Candidate answered all items correctly (ceiling effect).
- Final SEM(θ) = 0.45 (higher due to poor item matching)
- 95% Confidence Interval: 1.92 to 3.68

**Interpretation**: IRT provides individual-level precision estimates, revealing that Candidate C's score is less precise due to ceiling effects. This information can guide decisions (e.g., recommending a more advanced test or a work sample).

### Key Takeaways

1. **The 2PL model** is the foundation of SHL Verify scoring, estimating item difficulty (b) and discrimination (a) to model the probability of correct responses as a function of latent ability (theta).

2. **Item Characteristic Curves (ICCs)** graphically represent the item-theta relationship, with steeper curves indicating better discrimination and the inflection point representing item difficulty.

3. **SHL selected the 2PL model** after empirical testing showed the Rasch model (1PL) fit poorly and the 3PL model offered no practical advantage for most items.

4. **Thurstonian IRT models** (specifically MUPP) enable the OPQ32r to extract normative-equivalent trait scores from forced-choice (ipsative) data, solving a decades-old psychometric problem.

5. **The Test Information Function (TIF)** defines where a test measures precisely (high information = low SEM) and where it measures poorly (low information = high SEM), enabling rational test design.

6. **Computer Adaptive Testing (CAT)** exploits the TIF by selecting items that maximize information at the candidate's estimated theta, achieving 50% efficiency gains over fixed-form tests.

7. **Theta estimation** uses maximum likelihood or Bayesian methods to infer latent ability from response patterns, with individual-level SEMs providing realistic confidence intervals.

8. **Understanding IRT mechanics** enables practitioners to explain why adaptive tests are shorter, why some candidates' scores are more precise than others, and why forced-choice personality tests can produce normative scores.

---

