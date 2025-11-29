---
layout: default
title: "Chapter 3: Psychometric Foundations"
parent: "Part I: Foundations"
nav_order: 3
---

# Chapter 3: Psychometric Foundations

## Learning Objectives

By the end of this chapter, you will be able to:
- Explain the fundamental differences between Classical Test Theory (CTT) and Item Response Theory (IRT)
- Understand why SHL transitioned from CTT to IRT for OPQ32 and Verify
- Describe the role of normative data in making scores interpretable
- Recognize the importance of psychometric rigor in high-stakes assessment
- Explain the relationship between measurement precision and decision quality

## The Evolution from Classical Test Theory to Item Response Theory

The history of psychometric assessment reflects a steady progression toward greater precision, efficiency, and validity. SHL's assessment suite exemplifies this evolution, demonstrating a decisive pivot from Classical Test Theory (CTT) to sophisticated Item Response Theory (IRT) methods for its core instruments.

### Classical Test Theory: The Traditional Foundation

Classical Test Theory, developed in the early 20th century, provided the original mathematical framework for psychological measurement.

**Core Principles of CTT:**

1. **Observed Score Model:**
   - Observed Score = True Score + Error
   - The observed score is what we measure
   - The true score is what we want to measure
   - Error is random measurement noise

2. **Reliability:**
   - Reliability = True Score Variance / Observed Score Variance
   - Assessed through internal consistency (Cronbach's alpha)
   - Test-retest correlation
   - Parallel forms correlation

3. **Standard Error of Measurement (SEM):**
   - SEM = SD × √(1 - reliability)
   - Assumed constant across all ability levels
   - Same precision for all examinees

4. **Item Analysis:**
   - Item difficulty = proportion who answer correctly
   - Item discrimination = correlation with total score
   - Both are sample-dependent statistics

**Strengths of CTT:**
- Conceptually simple and intuitive
- Minimal assumptions about the data
- Straightforward calculation of reliability
- Well-understood by practitioners
- Sufficient for many low-stakes applications

**Limitations of CTT:**
- Sample-dependent statistics (item difficulty varies by sample)
- Test-dependent measurement (ability estimates tied to specific test)
- Constant SEM assumption (unrealistic across ability range)
- Inefficient measurement (requires many items for precision)
- Cannot support adaptive testing
- Problematic for ipsative (forced-choice) data

### The Transition to Item Response Theory

Item Response Theory, developed from the 1950s onward, provides a more sophisticated probabilistic framework that addresses the limitations of CTT.

**Core Principles of IRT:**

1. **Latent Trait Model:**
   - Assumes an underlying latent trait (θ, theta)
   - Observed responses probabilistically related to theta
   - Person and item parameters estimated separately

2. **Item Characteristic Curve:**
   - Probability of correct response as a function of ability
   - Mathematically modeled relationship
   - Logistic function shape (S-curve)

3. **Sample-Independent Parameters:**
   - Item difficulty is a property of the item, not the sample
   - Person ability is measured on the same scale regardless of which items were administered
   - Enables item banking and adaptive testing

4. **Information Function:**
   - Test information varies across ability levels
   - Maximum information where items match ability
   - Precision is ability-dependent

**The 2-Parameter Logistic Model (2PL):**

The probability of a correct response is modeled as:

**P(θ) = 1 / (1 + e^(-a(θ - b)))**

Where:
- θ (theta) = person's ability level
- a = item discrimination parameter (slope)
- b = item difficulty parameter (location where P = 0.50)

**Advantages of IRT Over CTT:**

1. **Invariance Properties:**
   - Item parameters don't depend on the sample tested
   - Person parameters don't depend on which items were administered
   - Enables equating across test forms

2. **Precision:**
   - Information function shows where measurement is most precise
   - Can target precision where needed most (e.g., near cutoff scores)
   - Standard error varies appropriately by ability level

3. **Efficiency:**
   - Adaptive testing achieves same reliability with 50% fewer items
   - Item banking allows for secure, randomized test forms
   - Optimal item selection maximizes information

4. **Flexibility:**
   - Supports computer adaptive testing (CAT)
   - Handles partial credit and polytomous responses
   - Can model complex item formats (e.g., forced-choice)

### Why SHL Transitioned to IRT

The transition to IRT for Verify and OPQ32 was driven by specific methodological needs that CTT could not address.

**For Verify (Cognitive Ability Tests):**

**The Challenge:**
- Need for secure, unsupervised online testing
- Desire for shorter tests without sacrificing reliability
- Requirement for precision across wide ability range
- Support for adaptive test administration

**The IRT Solution:**
SHL selected the 2-parameter logistic model (2PL) for verbal and numerical item banks after extensive testing:

1. **Model Selection Process:**
   - Tested 1-parameter (Rasch), 2-parameter (2PL), and 3-parameter (3PL) models with ~9,000 candidates
   - Found Rasch model showed poor fit (discrimination varies across items)
   - Found 3PL offered no substantial improvement over 2PL for ~90% of items
   - Selected 2PL as optimal balance of fit and parsimony

2. **Item Calibration:**
   - Large item banks calibrated with estimated a and b parameters
   - Items with low discrimination (flat ICCs) rejected
   - Items with extreme difficulty (outside -3 to +3 theta range) rejected
   - Continuous calibration updates ensure accuracy

3. **Adaptive Testing Implementation:**
   - After each response, algorithm updates theta estimate
   - Uses Maximum Likelihood Estimation (MLE) through iterative process
   - Selects next item providing maximum Fisher Information at current theta
   - Test terminates when Standard Error drops below threshold

4. **Benefits Achieved:**
   - Same reliability with 50% fewer items
   - No two candidates see identical item sequences (security)
   - Precise measurement across entire ability range
   - Individual-level standard errors for each examinee

**For OPQ32 (Personality Assessment):**

**The Challenge:**
The OPQ32 faced a unique psychometric problem stemming from its forced-choice format designed to reduce faking:

1. **The Ipsative Problem:**
   - Forced-choice format required selecting between equally desirable statements
   - Classical ipsative scoring produced interdependent scores (constant-sum constraint)
   - Scores indicated relative standing within the person, not between people
   - Distorted reliability and validity estimates
   - Made factor analysis and regression statistically invalid
   - Impossible to assess absolute standing on traits

**The IRT Solution:**
SHL applied Thurstonian Item Response Theory, specifically the Multi-Unidimensional Pairwise Preference (MUPP) model:

1. **Theoretical Foundation:**
   - Treats forced-choice responses as comparisons between latent trait levels
   - Models the probability of choosing statement A over statement B based on theta differences
   - Estimates theta for each of 32 traits simultaneously

2. **The Breakthrough:**
   - Recovers normative scale scores from ipsative response patterns
   - Solves the constant-sum problem through multidimensional IRT
   - Estimates absolute trait standing while preserving faking resistance
   - Enables valid between-person comparisons

3. **Scoring Process:**
   - Considers all responses across all items and traits simultaneously
   - Uses large optimization problem to triangulate absolute trait levels
   - Produces theta estimate for each trait
   - Rank-orderings correlate strongly (r ≈ 0.7-0.8) with fully normative tests

4. **Benefits Achieved:**
   - Maintains resistance to impression management
   - Recovers normative comparability
   - Reduced assessment length by 40-50% (triplet vs. quad format)
   - Valid for factor analysis, regression, and criterion validation

**For MQ (Motivation Questionnaire):**

**The Decision to Retain CTT:**
The MQ continues to use Classical Test Theory scoring because:

1. **Assessment Purpose:**
   - Primarily used for development and coaching, not high-stakes selection
   - Emphasis on profile generation rather than precise cutoff discrimination
   - Focus on relative strength of motivators within the person

2. **Construct Nature:**
   - Motivation is measured through self-reported preferences
   - Profile interpretation (top motivators vs. demotivators) more important than precise theta estimates
   - Less concern about faking given development context

3. **Methodological Sufficiency:**
   - Likert-type summated ratings provide adequate precision
   - Cronbach's alpha (0.75-0.85) confirms strong internal consistency
   - Classical approach is simpler and more transparent for feedback

This demonstrates that methodology should match purpose - not all assessments require the complexity of IRT.

## The Importance of Normative Data

Whether using CTT or IRT, raw scores are meaningless without context. Normative data provides the essential reference frame for interpretation.

### The Purpose of Norms

**Fundamental Problem:**
A raw score or theta estimate has little interpretive value by itself. What does θ = 0.5 mean? What about 12 out of 20 correct on a numerical reasoning test?

**Normative Solution:**
Norms translate scores into relative standing by comparing an individual to a designated reference group. This enables meaningful interpretation:
- "Scored at the 72nd percentile compared to IT professionals"
- "Sten score of 7 on Data Rational - higher than 77% of managers"

### Standardization Through Stens

SHL primarily uses Sten scores (Standard Ten scores) as the standardized metric for reporting:

**Sten Score Characteristics:**
- Scale: 1 to 10
- Mean (μ): 5.5
- Standard Deviation (σ): 2.0
- Conversion: Sten = (z × 2) + 5.5

**Sten Distribution and Interpretation:**

| Sten Score | Interpretation | Percentage | z-score range |
|------------|----------------|------------|---------------|
| 1 | Very Low | ~2% | Below -2.25 |
| 2 | Very Low | ~5% | -2.25 to -1.75 |
| 3 | Low | ~9% | -1.75 to -1.25 |
| 4 | Below Average | ~15% | -1.25 to -0.75 |
| 5 | Average | ~19% | -0.75 to -0.25 |
| 6 | Average | ~19% | -0.25 to +0.25 |
| 7 | Above Average | ~15% | +0.25 to +0.75 |
| 8 | High | ~9% | +0.75 to +1.25 |
| 9 | Very High | ~5% | +1.25 to +1.75 |
| 10 | Very High | ~2% | Above +1.75 |

**Advantages of Stens:**
- Prevents over-interpretation of small differences
- Familiar to HR professionals
- Adequate granularity for decision-making
- Clear interpretive thresholds (e.g., Sten 4-7 = Average)

### Normative Strategy by Assessment

**OPQ32 Norms:**

SHL maintains extensive normative databases stratified by:

1. **Job Level:**
   - General Population
   - Graduate/Professional
   - Manager
   - Executive
   - Specific occupational groups (directors, sales, banking, manufacturing)

2. **Geography and Language:**
   - Available in over 30 languages
   - Local norms in each country to capture cultural response tendencies
   - International aggregates across 30+ languages and 39 countries

3. **Industry:**
   - Sector-specific norms where sample sizes permit
   - Recognizes that personality profiles vary by industry

**Major Norm Update (2011):**
Following the transition to OPQ32r and IRT scoring, SHL conducted a massive norm update:
- Gathered data from millions of test-takers across 37 countries
- Computed 92 distinct norm groups based directly on IRT theta-scaled data
- Replaced older norms carried over from OPQ32i era
- Ensured norms reflected current talent markets

**Verify Norms:**

The Verify normative strategy emphasizes stratification by job level and industry to ensure fairness:

1. **Extensive Stratification:**
   - 70+ comparison groups available
   - Structured by job level (6 tiers from Operatives to Manager/Professional)
   - Organized by industry sector (Banking/Finance, Engineering/Science, Retail, Government)

2. **Fairness Rationale:**
   - A score average for general population might be below average for IT engineers
   - Prevents unfair comparison of specialized candidates to general population
   - Ensures appropriate reference group for role requirements

3. **Development:**
   - 8,436 participants for verbal/numerical reasoning calibration
   - 7,969 participants for inductive reasoning
   - Mapped to job levels based on education attainment

4. **Adaptive Test Support:**
   - Same underlying theta scale used across levels
   - Norm group selection determines interpretation
   - Supports "one test for all levels" philosophy of Verify G+

**MQ Norms:**

The MQ uses a simpler normative approach:
- Primarily referenced against general working population norm
- Regional benchmarks to account for cultural differences in motivator ratings
- Focus on relative strength of motivators (Sten 8-10 = highly motivating, 1-3 = demotivating)
- Ipsative interpretation within profile (top 3 motivators, bottom 3 demotivators)

### Norm Quality Control

Maintaining norm quality is essential for long-term validity:

**Quality Control Requirements:**

1. **Sample Requirements:**
   - Sufficiently large sample sizes (thousands to millions)
   - Representative of target population
   - Balanced demographics (gender, age) where possible
   - Appropriate stratification by relevant variables

2. **Dynamic Review Cycles:**
   - Regular refresh to reflect evolving labor markets
   - Population characteristics change over time (ability inflation, cultural shifts)
   - SHL periodically reviews item difficulty calibrations and norm shifts
   - Reports have 18-24 month "shelf-life" before reconsideration needed

3. **Transparent Documentation:**
   - Norm composition and date clearly documented
   - Allows users to assess relevance for their specific talent pool
   - Supports informed norm selection

4. **Client Selection Responsibility:**
   - Organizations must select most specific norm group matching their candidate pool
   - Balance between standardization and individualization
   - Critical for meaningful percentile and Sten score interpretation

## Measurement Precision and Decision Quality

The transition to IRT and sophisticated normative strategies directly impacts the quality of talent decisions.

### Precision Advantages of IRT

**Ability-Dependent Standard Errors:**
Unlike CTT's constant SEM, IRT provides precision that varies appropriately:
- Maximum precision near cutoff scores (where decisions are made)
- Lower precision at extremes (where decisions are clearer)
- Efficient allocation of measurement resources

**Individual-Level Confidence:**
IRT provides standard error for each examinee:
- Can calculate confidence intervals around each theta estimate
- Supports evidence-based decision-making
- Identifies when scores are too close to call with confidence

**Adaptive Testing Efficiency:**
CAT achieves precision faster:
- Reaches target reliability with 50% fewer items
- Reduces testing time and candidate fatigue
- Maintains or increases precision while improving experience

### Implications for High-Stakes Assessment

The psychometric rigor of IRT-based assessment is particularly critical in high-stakes contexts:

**Legal Defensibility:**
- IRT-based tests have strong technical documentation
- Item-level statistics support validity arguments
- Adaptive administration ensures appropriate difficulty for all candidates
- Detailed norm stratification demonstrates fairness considerations

**Security:**
- Item banking and adaptive selection reduce cheating opportunity
- No two candidates see identical item sequences
- Makes "test prep" much less effective
- Verification procedures detect inconsistencies

**Fairness:**
- Appropriate norm group selection prevents adverse impact
- Precision across ability range ensures equal measurement quality
- DIF (Differential Item Functioning) analysis identifies biased items
- Continuous calibration maintains accuracy across populations

## Key Takeaways

1. **CTT to IRT Evolution:** SHL's transition from Classical Test Theory to Item Response Theory represents a fundamental methodological advancement, moving from sample-dependent statistics to invariant measurement.

2. **IRT Enables Innovation:** The adoption of IRT made possible computer adaptive testing (Verify), recovery of normative scores from forced-choice data (OPQ32r), and modern item banking approaches.

3. **The 2PL Model:** SHL selected the 2-parameter logistic model for Verify after rigorous testing, finding it optimal for balancing fit and parsimony - the 3PL offered little additional benefit.

4. **Thurstonian IRT Breakthrough:** The application of Thurstonian IRT to the OPQ32r solved the ipsative problem, recovering normative scale scores while maintaining faking resistance - a methodological breakthrough.

5. **Norms Provide Context:** Raw scores and theta estimates are meaningless without normative data. Sten scores provide standardized interpretation by comparing individuals to appropriate reference groups.

6. **Stratification Ensures Fairness:** Both OPQ32 and Verify maintain extensively stratified norms (92 groups for OPQ, 70+ for Verify) to ensure fair comparison across job levels, industries, and cultures.

7. **Methodological Appropriateness:** The MQ's retention of CTT demonstrates that methodology should match purpose - not all assessments require IRT's complexity when simpler approaches suffice.

8. **Norm Maintenance:** Norms require continuous review and refresh to reflect evolving populations, with reports having an 18-24 month shelf-life before reconsideration.

9. **Measurement Precision Matters:** IRT's ability-dependent precision and individual-level standard errors enable more confident decision-making, particularly important in high-stakes assessment contexts.

10. **Validity Rests on Rigor:** The psychometric sophistication of IRT-based assessment provides the technical foundation for legal defensibility, fairness, and predictive validity.

---

**Navigation:**
- [← Previous Chapter: Chapter 2 - Assessment Framework Structure](02-framework-structure.html)
- [Next Chapter: Chapter 4 - OPQ32 Origins and Work-Focused Design →](04-opq32-origins.html)
- [Back to Home](index.html)
