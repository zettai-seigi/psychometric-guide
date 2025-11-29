---
layout: default
title: "Chapter 24: Classical Test Theory vs Item Response Theory"
parent: "Part VI: Scoring Methodologies"
nav_order: 1
permalink: /chapters/24-ctt-vs-irt/
---

# Classical Test Theory vs Item Response Theory

### Learning Objectives

By the end of this chapter, you will be able to:

1. Understand the fundamental assumptions and limitations of Classical Test Theory (CTT)
2. Recognize how CTT's constant Standard Error of Measurement creates measurement imprecision
3. Appreciate the paradigm shift introduced by Item Response Theory (IRT)
4. Explain how IRT calculates individual-level precision through latent trait estimation
5. Articulate why SHL transitioned from CTT to IRT for its flagship instruments
6. Compare the methodological approaches of CTT (sum scores) versus IRT (theta estimation)

### The Classical Test Theory Paradigm

Classical Test Theory, developed in the early 20th century, dominated psychometric practice for decades. Its fundamental equation is elegantly simple:

**X = T + E**

Where:
- **X** = Observed score (what the candidate actually scores)
- **T** = True score (the candidate's "real" ability level, unknowable but theoretically stable)
- **E** = Error (random measurement noise)

CTT's core assumptions include:

1. **Error is Random**: Measurement error is normally distributed with a mean of zero. If you could test someone infinite times, errors would cancel out, revealing their true score.

2. **Constant Standard Error of Measurement (SEM)**: CTT assumes that the precision of measurement is identical across all ability levels. A test is assumed to be equally accurate whether assessing low-ability or high-ability candidates.

3. **Sample Dependency**: Item difficulty and test reliability statistics are defined relative to the specific sample tested. If you calibrate items using university graduates, the difficulty estimates may not generalize to operational workers.

4. **Simple Scoring**: Scores are typically calculated as the sum (or average) of correct responses or Likert ratings. A test with 40 items yields a raw score ranging from 0 to 40.

5. **Test-Level Analysis**: Reliability (e.g., Cronbach's alpha) is calculated at the test level, providing a single coefficient that describes overall consistency.

### Critical Limitations of Classical Test Theory

While CTT is mathematically straightforward and intuitive, it suffers from several profound limitations that become problematic in modern, high-stakes assessment contexts:

#### 1. **Constant SEM is Psychometrically Naive**

Real-world tests do not measure all candidates with equal precision. Consider a cognitive ability test designed for graduate-level candidates. Such a test typically includes many difficult items. When administered to a low-ability candidate (e.g., someone with limited education), the test provides poor differentiation—most items are simply too hard, and the candidate answers them randomly or incorrectly. The resulting score has high uncertainty.

Conversely, if the same test is given to a very high-ability candidate, they answer nearly all items correctly, and the test again fails to differentiate effectively—it "hits the ceiling." The precision of measurement is highest for candidates near the middle of the test's difficulty range and progressively worse at the extremes.

CTT's assumption of constant SEM across all ability levels is demonstrably false. Yet, because CTT provides no mechanism for estimating precision at the individual level, users are forced to apply the same confidence interval to all candidates, regardless of where they fall on the ability spectrum.

#### 2. **Sample Dependency Limits Generalizability**

Item difficulty in CTT is defined as the proportion of a sample who answer correctly. If 70% of candidates answer Item 5 correctly, its difficulty is 0.70. But this statistic is fundamentally tied to the specific sample tested.

If the sample consists of high-ability candidates, many items will appear "easy" (high difficulty values). If the sample is low-ability, the same items will appear "hard" (low difficulty values). This sample dependency means that:

- **Item parameters cannot be compared across studies** unless samples are identical.
- **Test equating is complex**, requiring elaborate statistical adjustments.
- **Adaptive testing is impossible**, because item difficulty is not an inherent property of the item—it's a property of the sample.

#### 3. **Sum Scores Lack Interval Properties**

A raw score of 30 on a 50-item test does not necessarily represent twice as much ability as a score of 15. The relationship between raw scores and underlying ability is nonlinear. Furthermore, the "distance" between scores is not psychologically meaningful. Moving from 20 to 25 may represent a different magnitude of ability change than moving from 40 to 45, yet CTT treats all 5-point increases as equivalent.

This limitation complicates:
- **Cut-score setting**: Determining that "candidates who score 35 or higher are qualified" lacks a scientific basis for why 35 is the threshold.
- **Score interpretation**: Explaining what a raw score "means" requires extensive normative reference groups.

#### 4. **Ipsative Scoring is Incompatible with CTT**

When SHL introduced forced-choice formats for the OPQ to combat faking, it created an ipsative (relative ranking) response structure. In forced-choice items, candidates compare statements and indicate which they prefer, effectively ranking traits relative to each other.

The ipsative format produces a **constant-sum constraint**: all trait scores sum to the same total. This distortion violates the assumptions of CTT. Candidates cannot be compared meaningfully across a normative reference group because someone who scores high on one trait *must* score low on others, regardless of their absolute standing.

For years, this limitation meant that forced-choice personality tests (including early OPQ versions) produced scores that were statistically invalid for between-person comparisons—a critical flaw in selection contexts.

### The Item Response Theory Revolution

Item Response Theory emerged in the 1950s and 1960s (with foundational work by Frederic Lord, Georg Rasch, and others) as a probabilistic alternative to CTT. Rather than treating the test as a monolithic unit, IRT models the relationship between each item's characteristics and the candidate's latent ability.

#### Core Conceptual Shift: From Observed Scores to Latent Traits

IRT introduces the concept of **theta (θ)**, representing the candidate's latent ability on a continuous scale (typically standardized with mean = 0, SD = 1). Theta is not directly observable; instead, it is *estimated* from the pattern of item responses using maximum likelihood or Bayesian methods.

The fundamental IRT insight: **Each item provides probabilistic information about theta.** The probability that a candidate with a given theta value answers an item correctly (for ability tests) or endorses a statement (for personality tests) can be mathematically modeled.

#### Key IRT Advantages

##### 1. **Individual-Level Precision (SEM)**

IRT calculates the **Standard Error of Measurement** for each individual candidate based on the specific items they encountered and their response pattern. Candidates who receive items well-matched to their ability level have lower SEM (higher precision). Those who receive poorly matched items have higher SEM (lower precision).

This capability is transformative for:
- **Confidence intervals**: Each candidate's score report can include a personalized confidence interval reflecting the actual precision of their measurement.
- **Cut-score applications**: Organizations can set decision thresholds with explicit attention to measurement error, flagging borderline cases for additional assessment.

##### 2. **Item Parameters are Sample-Independent**

IRT separates item properties (difficulty, discrimination) from candidate properties (theta). Once items are calibrated using a sufficiently large and representative sample, the item parameters are considered invariant. A difficult item remains difficult regardless of who takes the test in the future.

This property enables:
- **Item banking**: Large pools of calibrated items can be maintained, with new items continuously added after calibration studies.
- **Test equating**: Different test forms (composed of different items) can be placed on the same theta scale, allowing direct comparability.
- **Adaptive testing**: Items can be selected in real-time to match the candidate's estimated ability, because item difficulty is an inherent property.

##### 3. **Interval-Level Measurement**

Theta scores are on an interval scale where equal differences represent equal differences in the underlying construct (within the constraints of the model). A theta of 1.0 represents the same distance above the mean as a theta of -1.0 represents below the mean.

This property simplifies:
- **Score interpretation**: Theta values can be meaningfully compared and aggregated.
- **Statistical analysis**: Researchers can apply parametric statistics with greater confidence.

##### 4. **Solving the Ipsative Problem**

Advanced IRT models, specifically **Thurstonian IRT models** (developed by Brown & Maydeu-Olivares, 2011), can extract normative-equivalent trait estimates from forced-choice (ipsative) data. These models treat forced-choice responses as comparisons between latent trait levels, using sophisticated algorithms to estimate absolute trait standing.

This breakthrough allowed SHL to retain the faking resistance of forced-choice formats while recovering statistically valid scores suitable for between-person comparison—a methodological holy grail.

### SHL's Transition to IRT

Recognizing these advantages, SHL invested heavily in IRT methodologies across its product portfolio:

#### **OPQ32r (Personality): Thurstonian IRT**

The current version of the Occupational Personality Questionnaire, **OPQ32r**, introduced around 2010-2013, uses a refined triplet forced-choice format (104 blocks of three statements, where candidates select "most like me" and "least like me").

The scoring algorithm applies a **Thurstonian IRT model** (specifically, the Multi-Unidimensional Pairwise Preference or MUPP model). This model treats each forced-choice decision as a comparison between latent trait levels. By modeling all 104 blocks simultaneously, the algorithm estimates a **theta (θ) score** for each of the 32 traits.

**Result**: The IRT-based scores closely approximate what normative (Likert-scale) scores would be, effectively recovering the "absolute" trait standing of candidates without sacrificing faking resistance. The rank-ordering of individuals on each trait correlates very strongly (r ≈ 0.7–0.8) with rankings from fully normative tests.

**Standardization**: The theta estimates are converted into **sten scores** (1–10 scale, mean = 5.5, SD = 2.0) by referencing an appropriate norm group, providing familiar interpretive anchors.

#### **Verify (Cognitive Ability): 2-Parameter Logistic Model**

For the Verify cognitive ability suite, SHL adopted IRT from the mid-2000s onward, coinciding with the shift to online, adaptive testing.

**Model Selection**: During development, SHL tested 1-parameter (Rasch), 2-parameter (2PL), and 3-parameter (3PL) IRT models with approximately 9,000 candidates. The Rasch model fit poorly (its assumption of equal discrimination across items was violated). The 3PL model (which adds a guessing parameter) offered no substantial improvement over 2PL for most items.

**Result**: SHL selected the **2-parameter logistic model (2PL)** for verbal and numerical item banks. This model estimates:
- **a-parameter (discrimination)**: How well the item differentiates between candidates just below and just above the item's difficulty level.
- **b-parameter (difficulty)**: The theta value at which the probability of answering correctly is 0.50.

**Outcome**: IRT-calibrated item banks enabled **Computer Adaptive Testing (CAT)**, where the test algorithm selects items in real-time to maximize information at the candidate's estimated theta. This produces the same measurement precision as fixed-form tests but with **50% fewer items**, significantly improving efficiency and candidate experience.

#### **MQ (Motivation): Remaining with CTT**

Interestingly, the **Motivation Questionnaire (MQ)** continues to use **Classical Test Theory** with simple sum-score averaging across items.

**Rationale**: The MQ is positioned primarily as a **development and coaching tool** rather than a high-stakes selection instrument. The emphasis is on producing a personalized motivational profile to guide career conversations and engagement strategies, not on making fine-grained selection distinctions. The additional complexity of IRT was deemed unnecessary for this purpose, and classical reliability coefficients (Cronbach's alpha) remain robust for MQ scales.

### Comparing Methodologies: A Practical Example

Consider a numerical reasoning test containing 20 items.

**CTT Approach**:
- A candidate answers 14 items correctly.
- Raw score = 14/20 = 70%.
- The test manual reports an overall SEM of 2.5 raw score points.
- Confidence interval (95%): 14 ± (1.96 × 2.5) = approximately 9 to 19.
- Interpretation: "We are 95% confident the candidate's true score is between 45% and 95%."
- This same confidence interval is applied to all candidates, regardless of whether they scored 5, 14, or 18.

**IRT Approach (2PL)**:
- The candidate encounters 20 items selected from a calibrated bank of 300 items.
- Each item has a known difficulty (b) and discrimination (a).
- After each response, the algorithm updates the theta estimate using maximum likelihood estimation.
- Final theta estimate: θ = 0.85 (indicating above-average ability).
- The algorithm calculates the **individual SEM** based on the specific items encountered and the response pattern: SEM(θ) = 0.32.
- Confidence interval (95%): θ = 0.85 ± (1.96 × 0.32) = 0.22 to 1.48.
- Interpretation: "We are 95% confident the candidate's true theta is between 0.22 and 1.48."
- A different candidate who scored at the extremes (very low or very high) would have a *larger* SEM, reflecting lower measurement precision.
- The theta estimate can be converted to percentiles or T-scores by referencing appropriate norms.

### CTT vs. IRT: When Each is Appropriate

**Use CTT when**:
- The test is short and fixed-form.
- High-stakes precision is not critical (e.g., development feedback, low-volume recruitment).
- Resources for IRT calibration (large pilot samples, specialized software) are unavailable.
- Simplicity and transparency are prioritized over psychometric sophistication.

**Use IRT when**:
- High-stakes selection decisions require maximum precision and defensibility.
- Adaptive testing is desired to improve efficiency and security.
- Large item banks are maintained, requiring test equating across forms.
- Forced-choice formats are used (requiring Thurstonian IRT).
- Individual-level confidence intervals and differential precision are important.

### Key Takeaways

1. **Classical Test Theory** dominated psychometrics for much of the 20th century, offering simplicity but suffering from critical limitations: constant SEM, sample dependency, and inability to handle ipsative data.

2. **Item Response Theory** revolutionized measurement by modeling the probabilistic relationship between items and latent ability, enabling individual-level precision, sample-independent item parameters, and adaptive testing.

3. **SHL's transition to IRT** for the OPQ32r (Thurstonian IRT) and Verify (2PL model) represents a commitment to methodological rigor and measurement precision, addressing the limitations of CTT while maintaining practical usability.

4. **Thurstonian IRT** solved the decades-old ipsative problem, allowing forced-choice personality tests to produce normative-equivalent scores—a significant innovation in faking-resistant assessment.

5. **The MQ continues to use CTT** because its developmental purpose does not require the precision and complexity of IRT, demonstrating that methodology should match the assessment's goals.

6. **Understanding CTT vs. IRT** is essential for practitioners to interpret score reports, explain measurement precision, and justify assessment choices to stakeholders and legal reviewers.

---

## Chapter Navigation

[← Previous: Chapter 23 - UCF as Translation Engine](/psychometric-guide/chapters/23-ucf-engine/)

[Next: Chapter 25 - IRT Scoring Deep Dive →](/psychometric-guide/chapters/25-irt-deep-dive/)

[↑ Back to Home](/psychometric-guide/)


### Learning Objectives

By the end of this chapter, you will be able to:

1. Understand the fundamental assumptions and limitations of Classical Test Theory (CTT)
2. Recognize how CTT's constant Standard Error of Measurement creates measurement imprecision
3. Appreciate the paradigm shift introduced by Item Response Theory (IRT)
4. Explain how IRT calculates individual-level precision through latent trait estimation
5. Articulate why SHL transitioned from CTT to IRT for its flagship instruments
6. Compare the methodological approaches of CTT (sum scores) versus IRT (theta estimation)

### The Classical Test Theory Paradigm

Classical Test Theory, developed in the early 20th century, dominated psychometric practice for decades. Its fundamental equation is elegantly simple:

**X = T + E**

Where:
- **X** = Observed score (what the candidate actually scores)
- **T** = True score (the candidate's "real" ability level, unknowable but theoretically stable)
- **E** = Error (random measurement noise)

CTT's core assumptions include:

1. **Error is Random**: Measurement error is normally distributed with a mean of zero. If you could test someone infinite times, errors would cancel out, revealing their true score.

2. **Constant Standard Error of Measurement (SEM)**: CTT assumes that the precision of measurement is identical across all ability levels. A test is assumed to be equally accurate whether assessing low-ability or high-ability candidates.

3. **Sample Dependency**: Item difficulty and test reliability statistics are defined relative to the specific sample tested. If you calibrate items using university graduates, the difficulty estimates may not generalize to operational workers.

4. **Simple Scoring**: Scores are typically calculated as the sum (or average) of correct responses or Likert ratings. A test with 40 items yields a raw score ranging from 0 to 40.

5. **Test-Level Analysis**: Reliability (e.g., Cronbach's alpha) is calculated at the test level, providing a single coefficient that describes overall consistency.

### Critical Limitations of Classical Test Theory

While CTT is mathematically straightforward and intuitive, it suffers from several profound limitations that become problematic in modern, high-stakes assessment contexts:

#### 1. **Constant SEM is Psychometrically Naive**

Real-world tests do not measure all candidates with equal precision. Consider a cognitive ability test designed for graduate-level candidates. Such a test typically includes many difficult items. When administered to a low-ability candidate (e.g., someone with limited education), the test provides poor differentiation—most items are simply too hard, and the candidate answers them randomly or incorrectly. The resulting score has high uncertainty.

Conversely, if the same test is given to a very high-ability candidate, they answer nearly all items correctly, and the test again fails to differentiate effectively—it "hits the ceiling." The precision of measurement is highest for candidates near the middle of the test's difficulty range and progressively worse at the extremes.

CTT's assumption of constant SEM across all ability levels is demonstrably false. Yet, because CTT provides no mechanism for estimating precision at the individual level, users are forced to apply the same confidence interval to all candidates, regardless of where they fall on the ability spectrum.

#### 2. **Sample Dependency Limits Generalizability**

Item difficulty in CTT is defined as the proportion of a sample who answer correctly. If 70% of candidates answer Item 5 correctly, its difficulty is 0.70. But this statistic is fundamentally tied to the specific sample tested.

If the sample consists of high-ability candidates, many items will appear "easy" (high difficulty values). If the sample is low-ability, the same items will appear "hard" (low difficulty values). This sample dependency means that:

- **Item parameters cannot be compared across studies** unless samples are identical.
- **Test equating is complex**, requiring elaborate statistical adjustments.
- **Adaptive testing is impossible**, because item difficulty is not an inherent property of the item—it's a property of the sample.

#### 3. **Sum Scores Lack Interval Properties**

A raw score of 30 on a 50-item test does not necessarily represent twice as much ability as a score of 15. The relationship between raw scores and underlying ability is nonlinear. Furthermore, the "distance" between scores is not psychologically meaningful. Moving from 20 to 25 may represent a different magnitude of ability change than moving from 40 to 45, yet CTT treats all 5-point increases as equivalent.

This limitation complicates:
- **Cut-score setting**: Determining that "candidates who score 35 or higher are qualified" lacks a scientific basis for why 35 is the threshold.
- **Score interpretation**: Explaining what a raw score "means" requires extensive normative reference groups.

#### 4. **Ipsative Scoring is Incompatible with CTT**

When SHL introduced forced-choice formats for the OPQ to combat faking, it created an ipsative (relative ranking) response structure. In forced-choice items, candidates compare statements and indicate which they prefer, effectively ranking traits relative to each other.

The ipsative format produces a **constant-sum constraint**: all trait scores sum to the same total. This distortion violates the assumptions of CTT. Candidates cannot be compared meaningfully across a normative reference group because someone who scores high on one trait *must* score low on others, regardless of their absolute standing.

For years, this limitation meant that forced-choice personality tests (including early OPQ versions) produced scores that were statistically invalid for between-person comparisons—a critical flaw in selection contexts.

### The Item Response Theory Revolution

Item Response Theory emerged in the 1950s and 1960s (with foundational work by Frederic Lord, Georg Rasch, and others) as a probabilistic alternative to CTT. Rather than treating the test as a monolithic unit, IRT models the relationship between each item's characteristics and the candidate's latent ability.

#### Core Conceptual Shift: From Observed Scores to Latent Traits

IRT introduces the concept of **theta (θ)**, representing the candidate's latent ability on a continuous scale (typically standardized with mean = 0, SD = 1). Theta is not directly observable; instead, it is *estimated* from the pattern of item responses using maximum likelihood or Bayesian methods.

The fundamental IRT insight: **Each item provides probabilistic information about theta.** The probability that a candidate with a given theta value answers an item correctly (for ability tests) or endorses a statement (for personality tests) can be mathematically modeled.

#### Key IRT Advantages

##### 1. **Individual-Level Precision (SEM)**

IRT calculates the **Standard Error of Measurement** for each individual candidate based on the specific items they encountered and their response pattern. Candidates who receive items well-matched to their ability level have lower SEM (higher precision). Those who receive poorly matched items have higher SEM (lower precision).

This capability is transformative for:
- **Confidence intervals**: Each candidate's score report can include a personalized confidence interval reflecting the actual precision of their measurement.
- **Cut-score applications**: Organizations can set decision thresholds with explicit attention to measurement error, flagging borderline cases for additional assessment.

##### 2. **Item Parameters are Sample-Independent**

IRT separates item properties (difficulty, discrimination) from candidate properties (theta). Once items are calibrated using a sufficiently large and representative sample, the item parameters are considered invariant. A difficult item remains difficult regardless of who takes the test in the future.

This property enables:
- **Item banking**: Large pools of calibrated items can be maintained, with new items continuously added after calibration studies.
- **Test equating**: Different test forms (composed of different items) can be placed on the same theta scale, allowing direct comparability.
- **Adaptive testing**: Items can be selected in real-time to match the candidate's estimated ability, because item difficulty is an inherent property.

##### 3. **Interval-Level Measurement**

Theta scores are on an interval scale where equal differences represent equal differences in the underlying construct (within the constraints of the model). A theta of 1.0 represents the same distance above the mean as a theta of -1.0 represents below the mean.

This property simplifies:
- **Score interpretation**: Theta values can be meaningfully compared and aggregated.
- **Statistical analysis**: Researchers can apply parametric statistics with greater confidence.

##### 4. **Solving the Ipsative Problem**

Advanced IRT models, specifically **Thurstonian IRT models** (developed by Brown & Maydeu-Olivares, 2011), can extract normative-equivalent trait estimates from forced-choice (ipsative) data. These models treat forced-choice responses as comparisons between latent trait levels, using sophisticated algorithms to estimate absolute trait standing.

This breakthrough allowed SHL to retain the faking resistance of forced-choice formats while recovering statistically valid scores suitable for between-person comparison—a methodological holy grail.

### SHL's Transition to IRT

Recognizing these advantages, SHL invested heavily in IRT methodologies across its product portfolio:

#### **OPQ32r (Personality): Thurstonian IRT**

The current version of the Occupational Personality Questionnaire, **OPQ32r**, introduced around 2010-2013, uses a refined triplet forced-choice format (104 blocks of three statements, where candidates select "most like me" and "least like me").

The scoring algorithm applies a **Thurstonian IRT model** (specifically, the Multi-Unidimensional Pairwise Preference or MUPP model). This model treats each forced-choice decision as a comparison between latent trait levels. By modeling all 104 blocks simultaneously, the algorithm estimates a **theta (θ) score** for each of the 32 traits.

**Result**: The IRT-based scores closely approximate what normative (Likert-scale) scores would be, effectively recovering the "absolute" trait standing of candidates without sacrificing faking resistance. The rank-ordering of individuals on each trait correlates very strongly (r ≈ 0.7–0.8) with rankings from fully normative tests.

**Standardization**: The theta estimates are converted into **sten scores** (1–10 scale, mean = 5.5, SD = 2.0) by referencing an appropriate norm group, providing familiar interpretive anchors.

#### **Verify (Cognitive Ability): 2-Parameter Logistic Model**

For the Verify cognitive ability suite, SHL adopted IRT from the mid-2000s onward, coinciding with the shift to online, adaptive testing.

**Model Selection**: During development, SHL tested 1-parameter (Rasch), 2-parameter (2PL), and 3-parameter (3PL) IRT models with approximately 9,000 candidates. The Rasch model fit poorly (its assumption of equal discrimination across items was violated). The 3PL model (which adds a guessing parameter) offered no substantial improvement over 2PL for most items.

**Result**: SHL selected the **2-parameter logistic model (2PL)** for verbal and numerical item banks. This model estimates:
- **a-parameter (discrimination)**: How well the item differentiates between candidates just below and just above the item's difficulty level.
- **b-parameter (difficulty)**: The theta value at which the probability of answering correctly is 0.50.

**Outcome**: IRT-calibrated item banks enabled **Computer Adaptive Testing (CAT)**, where the test algorithm selects items in real-time to maximize information at the candidate's estimated theta. This produces the same measurement precision as fixed-form tests but with **50% fewer items**, significantly improving efficiency and candidate experience.

#### **MQ (Motivation): Remaining with CTT**

Interestingly, the **Motivation Questionnaire (MQ)** continues to use **Classical Test Theory** with simple sum-score averaging across items.

**Rationale**: The MQ is positioned primarily as a **development and coaching tool** rather than a high-stakes selection instrument. The emphasis is on producing a personalized motivational profile to guide career conversations and engagement strategies, not on making fine-grained selection distinctions. The additional complexity of IRT was deemed unnecessary for this purpose, and classical reliability coefficients (Cronbach's alpha) remain robust for MQ scales.

### Comparing Methodologies: A Practical Example

Consider a numerical reasoning test containing 20 items.

**CTT Approach**:
- A candidate answers 14 items correctly.
- Raw score = 14/20 = 70%.
- The test manual reports an overall SEM of 2.5 raw score points.
- Confidence interval (95%): 14 ± (1.96 × 2.5) = approximately 9 to 19.
- Interpretation: "We are 95% confident the candidate's true score is between 45% and 95%."
- This same confidence interval is applied to all candidates, regardless of whether they scored 5, 14, or 18.

**IRT Approach (2PL)**:
- The candidate encounters 20 items selected from a calibrated bank of 300 items.
- Each item has a known difficulty (b) and discrimination (a).
- After each response, the algorithm updates the theta estimate using maximum likelihood estimation.
- Final theta estimate: θ = 0.85 (indicating above-average ability).
- The algorithm calculates the **individual SEM** based on the specific items encountered and the response pattern: SEM(θ) = 0.32.
- Confidence interval (95%): θ = 0.85 ± (1.96 × 0.32) = 0.22 to 1.48.
- Interpretation: "We are 95% confident the candidate's true theta is between 0.22 and 1.48."
- A different candidate who scored at the extremes (very low or very high) would have a *larger* SEM, reflecting lower measurement precision.
- The theta estimate can be converted to percentiles or T-scores by referencing appropriate norms.

### CTT vs. IRT: When Each is Appropriate

**Use CTT when**:
- The test is short and fixed-form.
- High-stakes precision is not critical (e.g., development feedback, low-volume recruitment).
- Resources for IRT calibration (large pilot samples, specialized software) are unavailable.
- Simplicity and transparency are prioritized over psychometric sophistication.

**Use IRT when**:
- High-stakes selection decisions require maximum precision and defensibility.
- Adaptive testing is desired to improve efficiency and security.
- Large item banks are maintained, requiring test equating across forms.
- Forced-choice formats are used (requiring Thurstonian IRT).
- Individual-level confidence intervals and differential precision are important.

### Key Takeaways

1. **Classical Test Theory** dominated psychometrics for much of the 20th century, offering simplicity but suffering from critical limitations: constant SEM, sample dependency, and inability to handle ipsative data.

2. **Item Response Theory** revolutionized measurement by modeling the probabilistic relationship between items and latent ability, enabling individual-level precision, sample-independent item parameters, and adaptive testing.

3. **SHL's transition to IRT** for the OPQ32r (Thurstonian IRT) and Verify (2PL model) represents a commitment to methodological rigor and measurement precision, addressing the limitations of CTT while maintaining practical usability.

4. **Thurstonian IRT** solved the decades-old ipsative problem, allowing forced-choice personality tests to produce normative-equivalent scores—a significant innovation in faking-resistant assessment.

5. **The MQ continues to use CTT** because its developmental purpose does not require the precision and complexity of IRT, demonstrating that methodology should match the assessment's goals.

6. **Understanding CTT vs. IRT** is essential for practitioners to interpret score reports, explain measurement precision, and justify assessment choices to stakeholders and legal reviewers.

---

