---
layout: default
title: "Chapter 12: Item Response Theory in Verify"
parent: "Part III: Verify Ability Tests"
nav_order: 3
permalink: /chapters/12-irt-verify/
---

# Chapter 12: Item Response Theory in Verify

---

## Introduction: The Psychometric Revolution

The mid-2000s introduction of the Verify suite coincided with a fundamental shift in cognitive assessment methodology. For decades, ability tests relied on **Classical Test Theory (CTT)**—a straightforward framework where scores equaled the number of items answered correctly, adjusted by normative comparison. While CTT served adequately for paper-and-pencil tests administered under standardized conditions, it proved inadequate for the digital age.

The move to online, unsupervised testing created new challenges: How could organizations ensure score comparability when candidates received different items? How could tests adapt to individual ability levels to maximize efficiency? How could measurement precision be quantified at the individual rather than group level? These questions demanded a more sophisticated psychometric framework.

**Item Response Theory (IRT)** provided the answer. Developed in the 1950s-1960s by pioneers like Allan Birnbaum, Frederic Lord, and Georg Rasch, IRT offers a probabilistic model of test performance that mathematically separates **item properties** (difficulty, discrimination) from **person properties** (ability). This separation enables revolutionary capabilities: adaptive testing, flexible test assembly, precise ability estimation, and rigorous item banking.

This chapter explores the IRT methodology underlying Verify, with particular focus on SHL's selection of the **2-parameter logistic (2PL) model** after empirical evaluation of alternatives. We examine why the Rasch model showed poor fit, why the 3-parameter model offered no substantial improvement, and how item calibration with over 8,000 participants produced the psychometrically sound item banks that power Verify's adaptive algorithms.

Understanding IRT is not merely academic—it explains why Verify achieves the same reliability as traditional tests with 50% fewer items, why scores from different item sequences are directly comparable, and why the assessment can provide individualized precision estimates. IRT is the mathematical engine driving modern psychometric assessment.

---

## The Limitations of Classical Test Theory

### The CTT Framework

Classical Test Theory conceptualizes an observed test score (X) as the sum of a person's true score (T) and random measurement error (E):

**X = T + E**

This elegantly simple model leads to fundamental psychometric concepts:
- **Reliability:** The ratio of true score variance to observed score variance
- **Standard Error of Measurement (SEM):** The standard deviation of measurement errors, assumed constant across all ability levels
- **Validity:** The correlation between observed scores and criterion measures

For decades, CTT served as the foundation for test development, providing practical guidance on item analysis, scale construction, and reliability estimation.

### Why CTT Fails for Modern Assessment

Despite its historical success, CTT suffers from fundamental limitations that became critical as testing moved online:

**1. Sample Dependence of Item Parameters**

In CTT, item difficulty is defined as the proportion of candidates answering correctly in a particular sample. This creates a circular problem:
- Item difficulty depends on the sample tested
- A "hard" item in a low-ability sample may appear "easy" in a high-ability sample
- Comparing item parameters across samples is problematic
- Building comparable test forms requires carefully matched samples

This sample dependency makes item banking—maintaining large pools of calibrated items—difficult. Each item's properties are bound to the specific sample used for analysis.

**2. Test Dependence of Ability Estimates**

Similarly, a person's ability estimate (their test score) depends on which items they encounter:
- An individual taking easy items appears less able than when taking hard items (even if both tests are "normed")
- Raw scores from tests of different difficulty are not directly comparable
- Creating parallel forms of equal difficulty is challenging
- Any difference in item difficulty distribution produces non-comparable scores

This test dependency makes adaptive testing impossible—if each person receives different items, how can their scores be compared?

**3. Constant Standard Error of Measurement**

CTT assumes that measurement error is constant across the ability range. The SEM applies equally to low-, medium-, and high-ability candidates. This is psychometrically unrealistic:
- Tests are most precise near average difficulty
- Measurement precision degrades for extreme ability levels
- No way to quantify individual-level precision
- Cannot optimize test precision for specific ability ranges

This assumption prevents targeting measurement where it's most needed—for example, achieving high precision near a cut-score for selection decisions.

**4. Group-Level Focus**

CTT statistics (reliability, item-total correlations) are computed at the group level. The framework provides:
- Population average reliability (e.g., α = 0.85)
- Population average SEM
- No individual-level precision estimates

For high-stakes selection, knowing that reliability is 0.85 "on average" is insufficient. Decision-makers need to know: "How precisely did we measure *this particular candidate*?"

**5. Inability to Support Adaptive Testing**

The limitations above converge to make Computer Adaptive Testing impossible under CTT:
- Cannot compare scores from different item sets
- Cannot quantify individual precision
- Cannot predict which item would be most informative for a particular candidate

As organizations demanded shorter, more efficient tests customized to individual ability levels, CTT proved inadequate. A new framework was needed.

---

## Item Response Theory: The Probabilistic Framework

### The IRT Paradigm Shift

Item Response Theory reconceptualizes test performance probabilistically. Rather than assuming a deterministic relationship between ability and score, IRT models the **probability** of a correct response as a function of ability and item characteristics.

**Core IRT Principle:**
The probability that person *j* with ability θ_j correctly answers item *i* with parameters (a_i, b_i) is given by a mathematical function:

**P(θ) = Probability of correct response given ability level**

This probability function is called the **Item Characteristic Curve (ICC)** or **Item Response Function (IRF)**. The shape of this curve is determined by item parameters, while a person's position on the θ (theta) scale determines their probability of success.

### Key IRT Assumptions

IRT models rest on several assumptions:

**1. Unidimensionality**
The items measure a single underlying latent trait (θ). For Verify, this means:
- Numerical items measure numerical reasoning ability
- Verbal items measure verbal reasoning ability
- Inductive items measure inductive reasoning ability

Each test is unidimensional, though the three domains can be combined to estimate general mental ability (g).

**2. Local Independence**
After controlling for ability (θ), item responses are statistically independent. A person's response to one item doesn't influence their response to another. This assumes:
- No item-to-item cueing effects
- No fatigue or practice effects within the test
- Item order doesn't systematically affect performance

**3. Monotonicity**
Higher ability always produces higher probability of correct response. The ICC is a monotonically increasing function—as θ increases, P(θ) increases. This aligns with our intuition: more able candidates are more likely to answer correctly.

These assumptions can be empirically tested. If violated, they suggest the model doesn't fit the data adequately.

### The Latent Trait: Theta (θ)

In IRT, ability is represented as **θ** (theta), a continuous latent variable typically scaled to have:
- Mean = 0
- Standard deviation = 1
- Range from approximately -3 to +3 (covering 99.7% of the distribution)

This standardized metric is analogous to a z-score. A person with θ = 0 has average ability; θ = +1 is one standard deviation above average; θ = -2 is two standard deviations below average.

**Key Insight:** Unlike CTT where "ability" is defined relative to a specific test, θ is test-independent. A person's theta is a property of the person, not the items they encountered. Different item sets can estimate the same θ, enabling direct comparison.

---

## The 2-Parameter Logistic (2PL) Model

### Model Specification

After testing multiple IRT models with approximately 9,000 candidates, SHL selected the **2-parameter logistic (2PL) model** for Verify's verbal and numerical item banks. The 2PL model specifies the probability of a correct response as:

**P(θ) = 1 / (1 + e^(-a(θ - b)))**

Where:
- **θ** (theta) = person ability parameter
- **a** = item discrimination parameter
- **b** = item difficulty parameter
- **e** = mathematical constant (approximately 2.718)

This logistic function produces an S-shaped (sigmoid) curve, capturing the intuitive relationship between ability and success probability.

### The Difficulty Parameter (b)

**Definition:**
The **b parameter** represents item difficulty, defined as the θ level at which the probability of correct response equals 0.50.

**Interpretation:**
- **b = 0:** The item is of average difficulty. A person with θ = 0 (average ability) has a 50% chance of answering correctly
- **b = +1:** A difficult item. It takes θ = +1 (one SD above average ability) to have a 50% chance of success
- **b = -1:** An easy item. Someone at θ = -1 (one SD below average) still has a 50% chance of succeeding

**Typical Range:**
In Verify item banks, b parameters typically range from approximately -2 to +2, covering easy to very difficult items.

**Practical Implications:**
- Items with b close to a candidate's θ provide maximum information
- A well-designed test includes items spanning the b-parameter range to measure diverse ability levels
- Adaptive testing works by selecting items with b ≈ current θ estimate

**Example:**
A Numerical Reasoning item showing a complex multi-variable chart might have b = +1.5 (quite difficult). A Verbal Reasoning item requiring simple deductive inference from a short passage might have b = -0.5 (relatively easy).

### The Discrimination Parameter (a)

**Definition:**
The **a parameter** represents item discrimination—how well the item differentiates between ability levels. Mathematically, it's proportional to the slope of the ICC at the point b.

**Interpretation:**
- **Higher a:** The item sharply distinguishes between those slightly below and slightly above the threshold. High-ability candidates almost always answer correctly; low-ability candidates rarely do
- **Lower a:** The item is less discriminating. The probability of correct response increases gradually with ability
- **a = 0:** No discrimination—the item doesn't measure ability at all (guessing or other factors dominate)

**Typical Range:**
In cognitive ability tests, discrimination parameters typically range from 0.5 to 2.5. Verify items selected for operational use generally show:
- **a > 0.8:** Acceptable discrimination
- **a > 1.0:** Good discrimination
- **a > 1.5:** Excellent discrimination

Items with a < 0.5 are flagged for review or removal, as they contribute little to ability estimation.

**Relationship to CTT:**
The discrimination parameter is conceptually related to the **item-total correlation** in CTT. Both measure how well an item aligns with the overall construct. However, a is more precise because it's estimated while controlling for item difficulty and ability distribution.

**Practical Implications:**
- Highly discriminating items (high a) provide more information and are prioritized in adaptive testing
- Items with very high discrimination (a > 2.5) may be too sensitive to small ability differences, risking test anxiety effects
- A mix of discrimination levels provides robust measurement across the ability range

**Example:**
Consider two Inductive Reasoning items, both with b = 0 (average difficulty):
- **Item A (a = 0.8):** Candidates at θ = -1 have ~30% success; those at θ = +1 have ~70% success (40-point spread)
- **Item B (a = 1.8):** Candidates at θ = -1 have ~15% success; those at θ = +1 have ~85% success (70-point spread)

Item B discriminates more sharply, making it more valuable for precise ability estimation.

### The Logistic Function Shape

The 2PL model produces a smooth, S-shaped curve:

**Lower Asymptote (θ → -∞):**
As ability approaches negative infinity, P(θ) approaches 0. Extremely low-ability candidates have near-zero success probability.

**Inflection Point (θ = b):**
At the difficulty parameter, P(θ) = 0.50. This is where the curve's slope is steepest—where the item discriminates most effectively.

**Upper Asymptote (θ → +∞):**
As ability approaches positive infinity, P(θ) approaches 1. Extremely high-ability candidates almost always succeed.

The **steepness** of the curve is determined by the discrimination parameter (a). Higher discrimination produces a steeper transition from low to high success probability.

---

## Model Selection: Why 2PL?

SHL didn't arbitrarily choose the 2PL model. During Verify's development, researchers empirically tested multiple IRT models using data from approximately **9,000 candidates**. Let's examine why they rejected alternatives.

### The 1-Parameter (Rasch) Model: Poor Fit

The **Rasch model** (also called the 1-parameter logistic or 1PL model) is a simplified IRT model:

**P(θ) = 1 / (1 + e^(-(θ - b)))**

Note the absence of the discrimination parameter (a). The Rasch model assumes **all items discriminate equally** (implicitly setting a = 1 for all items).

**Theoretical Appeal:**
The Rasch model has elegant measurement properties:
- **Specific objectivity:** Person ability estimates are independent of which items were administered
- **Sufficient statistics:** The raw score is a sufficient statistic for θ
- **Additive measurement:** Interval-scale properties

These properties make the Rasch model theoretically attractive, especially in educational measurement.

**Empirical Reality:**
However, when SHL fit the Rasch model to Verify pilot data, it **showed poor fit**. Real items don't discriminate equally:
- Some items are sharper discriminators (steep ICC slopes)
- Others are flatter (gradual ICC slopes)
- Forcing all a = 1 produces systematic misfit

**Practical Consequence:**
Misfit means the model doesn't accurately describe item performance. Using a poorly fitting model produces:
- Biased ability estimates
- Inaccurate standard errors
- Suboptimal item selection in adaptive testing
- Reduced measurement precision

While the Rasch model is elegant in theory, real cognitive ability items violate its equal-discrimination assumption. Verify required a model that accommodates varying item discrimination.

### The 3-Parameter Logistic Model: No Added Value

The **3-parameter logistic (3PL) model** adds a "guessing" parameter (c):

**P(θ) = c + (1 - c) / (1 + e^(-a(θ - b)))**

Where:
- **c** = lower asymptote (pseudo-guessing parameter)

The 3PL recognizes that even candidates with very low ability have some probability of success through random guessing. For a 4-option multiple-choice item, pure guessing yields c = 0.25.

**When 3PL Matters:**
The guessing parameter becomes important when:
- Items have few response options (more guessing)
- Items include implausible distractors (easier to eliminate options)
- Candidates employ test-taking strategies (strategic guessing)

**SHL's Finding:**
After testing the 3PL model, SHL found it offered **no substantial improvement over 2PL for most items**. Approximately 90% of Verify items showed:
- Estimated c parameters near 0
- Model fit statistics similar to 2PL
- No meaningful difference in ability estimation

**Why No Guessing Effect?**
Several factors minimize guessing in Verify items:
- **Complex scenarios:** Items require interpretation of business data or logical passages, not simple factual recall
- **Constructed difficulty:** Distractors are carefully designed to appear plausible, reducing effectiveness of elimination strategies
- **Time pressure:** Candidates are motivated to work efficiently rather than randomly guess
- **High engagement:** Workplace relevance and realistic content maintain candidate motivation

**Parsimony Principle:**
In psychometrics, we prefer simpler models unless added complexity demonstrably improves fit (Occam's Razor). Since 3PL offered no substantial improvement, SHL selected the more parsimonious 2PL model.

**Exception:**
Some specialized Verify tests (e.g., Checking, Mechanical Comprehension) might use classical scoring or different IRT models if their item characteristics differ from the core reasoning tests.

### The 2PL Goldilocks Solution

The 2PL model proved "just right":
- More flexible than Rasch (accommodates varying discrimination)
- More parsimonious than 3PL (avoids unnecessary complexity)
- Adequate empirical fit to pilot data
- Sufficient for operational needs (adaptive testing, score comparability, information functions)

This evidence-based selection reflects SHL's commitment to rigorous psychometric methodology.

---

## Item Calibration: From Pilot Data to Parameters

### The Calibration Process

**Item calibration** is the process of estimating item parameters (a and b) from empirical response data. This is a one-time intensive process (though parameters may be recalibrated as new data accumulates).

**Step 1: Item Authoring**
Psychometricians and content experts write items following the measurement taxonomy—ensuring workplace relevance, appropriate difficulty range, and construct validity.

**Step 2: Pilot Testing**
Items are administered to large, diverse samples. For Verify, SHL used **approximately 8,000+ participants** in calibration studies. Large samples are critical because:
- Parameter estimates stabilize with sample size
- Rare response patterns become observable
- Confidence in item properties increases

**Step 3: Parameter Estimation**
Statistical software uses **maximum likelihood estimation (MLE)** or **Bayesian methods** to estimate a and b for each item. The algorithm:
- Assumes a provisional ability distribution for the sample
- Estimates item parameters that maximize the likelihood of observed responses
- Iteratively refines estimates until convergence

This produces a set of (a, b) parameters for each item, placed on a common θ metric.

**Step 4: Model Fit Evaluation**
Psychometricians assess whether the 2PL model adequately describes item performance:
- **Item fit statistics:** Do observed success rates match predicted probabilities across θ levels?
- **Residual analysis:** Are there systematic patterns in prediction errors?
- **Differential Item Functioning (DIF):** Do items function equivalently across demographic groups?

Items showing poor fit or DIF are revised or discarded.

**Step 5: Banking**
Items with acceptable parameters and fit statistics enter the operational item bank, ready for test assembly or adaptive administration.

### Why 8,000+ Participants?

The large calibration sample (approximately 9,000 participants mentioned in sources, with 8,000+ for specific item banks) serves multiple purposes:

**1. Precision**
Parameter standard errors decrease with √n. Larger samples produce more stable estimates, ensuring items function as expected in operational testing.

**2. Coverage**
To calibrate items across the full b-parameter range (-2 to +2), the sample must include candidates across the full ability distribution. A sample of 8,000+ ensures adequate representation at all levels.

**3. Subgroup Analysis**
Large samples enable DIF analysis across demographic subgroups (gender, ethnicity, education level), ensuring item fairness.

**4. Rare Events**
Some response patterns are rare. Large samples make them observable, improving parameter estimation for difficult items or low-frequency interactions.

**5. Statistical Power**
Hypothesis tests for model fit, item quality, and parameter significance require adequate power, which increases with sample size.

The substantial investment in large-sample pilot testing reflects SHL's commitment to psychometric rigor—this is part of the "huge R&D effort in the mid-2000s" mentioned in sources.

### Continuous Calibration

Item calibration isn't a one-time event. As operational testing accumulates data:
- **Parameter drift** may occur (items become easier or harder due to practice effects, changes in educational background, etc.)
- **New items** are added to expand the bank or replace retired items
- **Updated norms** require recalibration to current populations

The sources note that Verify's **IRT calibration is continuously updated** to ensure accuracy. This ongoing maintenance preserves measurement quality over time.

---

## Theta Estimation: Measuring Latent Ability

### From Item Parameters to Ability Estimates

Once items are calibrated, operational testing shifts to estimating θ for each candidate. This is the inverse problem:
- **Calibration:** Given θ distribution and responses, estimate item parameters (a, b)
- **Scoring:** Given item parameters (a, b) and responses, estimate individual θ

### Maximum Likelihood Estimation (MLE)

The most common method for θ estimation is **Maximum Likelihood Estimation**. The algorithm seeks the θ value that maximizes the likelihood of the observed response pattern.

**Intuition:**
Suppose a candidate answers 7 out of 10 items correctly. The MLE algorithm asks: "What θ value makes this specific pattern of correct/incorrect responses most probable?"

**Mathematical Approach:**
For a response pattern (u_1, u_2, ..., u_n) where u_i = 1 if correct and 0 if incorrect, the likelihood function is:

**L(θ) = ∏ P_i(θ)^u_i × [1 - P_i(θ)]^(1-u_i)**

The algorithm searches for the θ that maximizes L(θ), typically by iterative methods (Newton-Raphson, Fisher scoring).

**Starting Value:**
The algorithm begins with a provisional θ estimate (often θ = 0, representing average ability) and iteratively refines it until convergence.

**Convergence:**
After several iterations (typically 5-10), the estimate stabilizes. The final θ represents the candidate's ability on the standardized latent scale.

### Bayesian Methods (EAP, MAP)

Alternative estimation methods incorporate **prior information** about the θ distribution:

**Expected A Posteriori (EAP):**
EAP treats θ as having a prior distribution (typically normal with μ = 0, σ = 1) and computes the expected value of θ given the response data and prior. This produces:
- More stable estimates for extreme scores
- Shrinkage toward the population mean (Bayesian regularization)
- Defined estimates even for perfect scores

**Maximum A Posteriori (MAP):**
MAP finds the θ value that maximizes the posterior distribution, incorporating both the likelihood and the prior.

**Trade-offs:**
- **MLE:** Unbiased but can produce extreme estimates (θ → ±∞ for perfect/zero scores)
- **EAP/MAP:** Biased toward the prior mean but more stable, especially for short tests

Verify likely uses MLE for operational scoring due to its unbiased properties, possibly with EAP for extreme scores or very short tests.

### The Standard Error of θ

Unlike CTT's constant SEM, IRT provides **individual-specific standard errors**. Each θ estimate has an associated SE(θ), quantifying precision for that particular candidate.

**Calculation:**
The standard error is computed from the **information function** (discussed below):

**SE(θ) = 1 / √I(θ)**

Where I(θ) is the test information at the estimated θ level.

**Interpretation:**
- **SE = 0.3:** High precision. The 95% confidence interval for θ is approximately ±0.6 (two standard errors)
- **SE = 0.5:** Moderate precision. 95% CI ≈ ±1.0
- **SE = 0.7:** Lower precision. 95% CI ≈ ±1.4

**Adaptive Testing Termination:**
CAT algorithms often continue until SE(θ) drops below a predetermined threshold (e.g., SE < 0.4), ensuring adequate precision before stopping.

---

## Information Functions: Quantifying Precision

![Figure 12.1: Item Characteristic Curves and Test Information Function](/psychometric-guide/images/Figure_12_01.png)

*Figure 12.1: Item Characteristic Curves showing probability of correct response by ability level (top), and Test Information Function showing measurement precision across the ability range (bottom)*

### Item Information

IRT's most powerful concept is the **item information function**, which quantifies how much an item contributes to measurement precision at each θ level.

**Formula (2PL):**

**I_i(θ) = a_i² × P_i(θ) × [1 - P_i(θ)]**

Where:
- **a_i** = item discrimination
- **P_i(θ)** = probability of correct response at ability θ

**Key Insights:**

1. **Information is highest near b:**
   The product P(θ) × [1 - P(θ)] is maximized when P = 0.5, which occurs at θ = b. Items provide most information when their difficulty matches the candidate's ability.

2. **Discrimination amplifies information:**
   Information is proportional to a². An item with a = 2.0 provides **four times** the information of an item with a = 1.0 (holding other factors constant).

3. **Information drops at extremes:**
   When θ is far from b, P(θ) approaches 0 or 1, making the product P × (1-P) small. The item provides little information when it's too easy or too hard for the candidate.

**Practical Application:**
In adaptive testing, the algorithm selects the next item by computing I_i(θ̂) for all available items and choosing the one with maximum information at the current θ estimate. This ensures each item contributes maximally to precision.

### Test Information

The **test information function** is simply the sum of item information functions:

**I(θ) = ∑ I_i(θ)**

Test information quantifies the overall precision of the entire test at each θ level.

**Properties:**
- Higher I(θ) = greater precision at that ability level
- I(θ) determines the standard error: **SE(θ) = 1 / √I(θ)**
- Test information is additive: adding items increases information

**Visualizing Test Information:**
A plot of I(θ) vs. θ reveals where the test measures most precisely:
- **Peaked distribution:** Maximum precision near the peak, less precision at extremes
- **Flat distribution:** Consistent precision across the ability range (achieved by selecting items with diverse b values)

**Design Implications:**
Test developers can engineer the information function shape by selecting items strategically:
- **Selection test with cut-score:** Maximize I(θ) near the cut-score
- **Comprehensive assessment:** Distribute I(θ) evenly across the expected ability range
- **High-stakes decisions:** Ensure I(θ) exceeds a minimum threshold across the relevant range

### The Efficiency Claim: 50% Fewer Items

The sources repeatedly state that CAT achieves **"the same reliability as a fixed-form test with 50% fewer items."** Information functions explain why:

**Fixed-Form Test:**
A 30-item fixed test administers all 30 items to all candidates. Some items are too easy (low information for high-ability candidates), others too hard (low information for low-ability candidates). Average information per item is suboptimal.

**Adaptive Test:**
A 15-item adaptive test selects each item to maximize information at the candidate's current θ estimate. Every item is well-targeted, providing near-maximum information. Average information per item is much higher.

**Mathematical Equivalence:**
If adaptive item selection doubles average information per item, then 15 adaptively selected items provide the same total information as 30 randomly selected items:

**I_adaptive (15 items) ≈ I_fixed (30 items)**

Since reliability is determined by test information, the shorter adaptive test achieves equivalent reliability.

**Empirical Evidence:**
The 50% efficiency gain is an empirical finding from Verify validation studies, not just theoretical. Real data confirms that adaptive administration achieves target reliability with approximately half the items of fixed forms.

---

## Advantages of IRT Over Classical Test Theory

### 1. Item-Invariant Person Measurement

**CTT Problem:** Ability estimates depend on test difficulty. Taking an easy vs. hard test produces non-comparable scores.

**IRT Solution:** θ estimates are item-invariant. As long as items are calibrated on the same scale, different item sets estimate the same θ. This enables:
- Adaptive testing with unique item sequences per candidate
- Score comparability across test administrations
- Flexible test assembly without matched-forms requirements

### 2. Person-Invariant Item Calibration

**CTT Problem:** Item difficulties depend on the sample tested. An item is "hard" or "easy" only relative to a specific group.

**IRT Solution:** Item parameters (a, b) are person-invariant. Once calibrated, parameters remain stable regardless of who takes the item (assuming no parameter drift). This enables:
- Building large item banks with stable parameters
- Continuous item banking and gradual bank expansion
- Precise targeting of specific ability levels

### 3. Individualized Precision Estimates

**CTT Problem:** Reliability and SEM are group-level statistics. No way to quantify precision for a specific candidate.

**IRT Solution:** SE(θ) is computed for each individual, reflecting the precision of their specific ability estimate. This enables:
- Confidence intervals tailored to each candidate
- Adaptive algorithms that terminate when precision is adequate
- High-stakes decisions informed by measurement uncertainty

### 4. Optimal Test Design

**CTT Problem:** Limited ability to quantify how much each item contributes to measurement quality.

**IRT Solution:** Item information functions quantify each item's contribution to precision at every ability level. This enables:
- Strategic test assembly (maximize information where needed)
- Item selection algorithms (choose most informative item)
- Test blueprinting (ensure adequate information across ability range)

### 5. Sophisticated Scoring Algorithms

**CTT Problem:** Scoring is simple but crude (number correct, possibly normed).

**IRT Solution:** Scoring incorporates item parameters to produce precise ability estimates. This enables:
- Appropriate weighting of item difficulties
- Down-weighting of low-discrimination items
- Correction for guessing (if using 3PL)
- Continuous-scale ability estimates (not just discrete scores)

### 6. Adaptive Testing Foundation

**CTT Problem:** Cannot support adaptive administration (scores not comparable if items differ).

**IRT Solution:** IRT mathematically enables CAT by ensuring comparability and quantifying information. This enables:
- Real-time item selection based on current ability estimate
- Efficient testing (maximum information per item)
- Termination based on precision criteria
- Security through unique item sequences

---

## Key Takeaways

1. **CTT Limitations:** Classical Test Theory suffers from sample-dependent item parameters, test-dependent ability estimates, constant SEM, and inability to support adaptive testing—motivating the shift to IRT

2. **Probabilistic Framework:** IRT models the probability of correct response as a function of ability (θ) and item parameters, mathematically separating person and item properties

3. **2PL Model Selection:** After testing with ~9,000 candidates, SHL selected the 2-parameter logistic model, rejecting Rasch (poor fit) and 3PL (no added value for most items)

4. **Difficulty Parameter (b):** Represents the θ level at which P(correct) = 0.50. Items with b near a candidate's θ provide maximum information

5. **Discrimination Parameter (a):** Reflects how sharply the item differentiates ability levels. Higher a produces steeper ICC and greater information contribution

6. **Large-Sample Calibration:** Item parameters estimated from 8,000+ participants ensure precision, stability, and adequate coverage of the ability distribution

7. **Theta as Latent Ability:** θ represents ability on a standardized continuous scale (mean 0, SD 1), enabling direct comparability across item sets and administrations

8. **Information Functions:** Item information I(θ) = a² × P(θ) × [1-P(θ)] quantifies precision contribution. Test information determines SE(θ) = 1 / √I(θ)

9. **50% Efficiency Gain:** Adaptive item selection targeting maximum information enables same reliability with half the items, validated empirically

10. **IRT Advantages:** Item-invariant person measurement, person-invariant item calibration, individualized precision, optimal test design, and CAT foundation make IRT essential for modern assessment

---

## Chapter Navigation

[← Previous: Chapter 11 - Cognitive Domains and the g Factor](/psychometric-guide/chapters/11-cognitive-domains/)

[Next: Chapter 13 - Computer Adaptive Testing →](/psychometric-guide/chapters/13-cat/)

[↑ Back to Home](/psychometric-guide/)
