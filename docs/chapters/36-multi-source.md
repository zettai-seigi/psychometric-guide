---
layout: default
title: "Chapter 36: Multi-Source Integration (P+A)"
parent: "Part VIII: Reports & Future"
nav_order: 4
permalink: /chapters/36-multi-source/
---

# Chapter 36: Multi-Source Integration (P+A)

---

## 36.1 Theoretical Foundation: Preference vs. Power

**The Dual Nature of Competency Prediction:**

Workplace competencies require both the inclination to engage in relevant behaviors (personality) and the capacity to execute them effectively (ability). SHL's multi-source integration acknowledges this dual requirement:

**Personality (Preference/Typical Performance):**
- Reflects what people are naturally inclined to do
- Indicates typical behavioral style under normal conditions
- Measured by OPQ32: Preferences for working styles, interpersonal approaches, thinking patterns

**Ability (Power/Maximal Performance):**
- Reflects what people are capable of doing when fully engaged
- Indicates maximal cognitive capacity
- Measured by Verify: Numerical, Verbal, Inductive reasoning

**The Necessity of Both:**

High performance requires alignment of both vectors:

- **High Preference + High Ability = Optimal Performance:** Individual both wants to and can perform the behavior effectively
- **High Preference + Low Ability = Frustrated Aspiration:** Individual enjoys the domain but lacks capacity for excellence
- **Low Preference + High Ability = Underutilized Capacity:** Individual has capability but won't voluntarily engage
- **Low Preference + Low Ability = Clear Development Need:** Both preference and capacity require building

**Example: Analytical Competencies**

**Scenario 1: Aligned Preference and Power**
- OPQ Data Rational: Sten 8 (enjoys working with numbers)
- Verify Numerical Reasoning: Sten 8 (strong quantitative capacity)
- **Prediction:** High potential for analytical work

**Scenario 2: Preference Without Power**
- OPQ Data Rational: Sten 8 (enjoys working with numbers)
- Verify Numerical Reasoning: Sten 3 (limited quantitative capacity)
- **Prediction:** Moderated potential; may enjoy data work but struggle with complex analysis

**Scenario 3: Power Without Preference**
- OPQ Data Rational: Sten 3 (prefers non-quantitative work)
- Verify Numerical Reasoning: Sten 8 (strong quantitative capacity)
- **Prediction:** Moderated potential; has capacity but unlikely to voluntarily engage in analytical tasks

## 36.2 Validity Improvement Examples: Empirical Evidence

**Meta-Analytic Foundation:**

Research consistently demonstrates that combining personality and cognitive ability predictors yields higher validity coefficients for job performance than using either source alone. SHL's validation studies provide specific examples:

**Published Validity Coefficients:**

**Analyzing and Interpreting Competency:**
- **Personality Only (OPQ):** ρ = 0.28
- **Ability Only (Verify):** ρ = 0.35
- **Combined (P+A):** ρ = 0.44

**Validity Improvement:** 57% increase over personality alone, 26% increase over ability alone

**Interacting and Presenting Competency:**
- **Personality Only (OPQ):** ρ = 0.32
- **Ability Only (Verify):** ρ = 0.18
- **Combined (P+A):** ρ = 0.40

**Validity Improvement:** 25% increase over personality alone, 122% increase over ability alone

**Creating and Conceptualizing Competency:**
- **Personality Only (OPQ):** ρ = 0.26
- **Ability Only (Verify):** ρ = 0.28
- **Combined (P+A):** ρ = 0.36

**Validity Improvement:** 38% increase over personality alone, 29% increase over ability alone

**Organizing and Executing Competency:**
- **Personality Only (OPQ):** ρ = 0.35
- **Ability Only (Verify):** ρ = 0.10
- **Combined (P+A):** ρ = 0.38

**Validity Improvement:** 9% increase over personality alone, 280% increase over ability alone

**Pattern Analysis:**

1. **Cognitive-Heavy Competencies:** For competencies like "Analyzing and Interpreting," ability weights more heavily than personality, but combining both sources still increases validity.

2. **Personality-Heavy Competencies:** For competencies like "Interacting and Presenting" or "Organizing and Executing," personality is the primary driver, but ability still adds incremental validity.

3. **Balanced Competencies:** For competencies like "Creating and Conceptualizing," both sources contribute roughly equally.

**Statistical Explanation:**

The validity improvement occurs because personality and ability:
1. **Measure different constructs:** Cognitive ability and personality traits are largely uncorrelated (r ≈ 0.10), meaning they capture independent variance
2. **Predict different aspects:** Personality predicts typical behavioral patterns; ability predicts maximal cognitive performance
3. **Interact multiplicatively:** High performance often requires both inclination and capacity, not just one or the other

**Incremental Validity Formula:**

ΔR² = R²(P+A) - R²(P only)

Where:
- R²(P+A) = Variance explained by combined personality and ability
- R²(P only) = Variance explained by personality alone

For Analyzing and Interpreting:
- R²(P only) = 0.28² = 0.078 (7.8% variance explained)
- R²(P+A) = 0.44² = 0.194 (19.4% variance explained)
- ΔR² = 0.116 (11.6% additional variance explained)

This represents a 149% increase in explained variance.

## 36.3 Ability as Cognitive Moderator

**Moderation Concept:**

In statistical terms, ability acts as a moderator of the personality-competency relationship. The strength of the relationship between personality traits and competency performance depends on the level of cognitive ability.

**Moderation Model:**

Competency Performance = β₀ + β₁(Personality) + β₂(Ability) + β₃(Personality × Ability) + ε

Where β₃ represents the interaction effect—how ability moderates the personality-competency relationship.

**Practical Example:**

**Data Rational Personality Trait and Analytical Competency:**

For individuals with **High Numerical Ability (Sten 8-10):**
- High Data Rational (Sten 8-10) → Strong analytical competency (Sten 8-10)
- Low Data Rational (Sten 1-3) → Moderate analytical competency (Sten 5-6) [ability compensates]

For individuals with **Low Numerical Ability (Sten 1-3):**
- High Data Rational (Sten 8-10) → Moderate analytical competency (Sten 4-5) [ability constrains]
- Low Data Rational (Sten 1-3) → Low analytical competency (Sten 1-3)

**Graphical Representation:**

```
Analytical Competency Prediction

High Ability │         ┌────── High Data Rational
             │      ┌──┘
             │   ┌──┘
             │┌──┘
             └───────────────────────────
                                Low Data Rational

Low Ability  │      ┌────────── High Data Rational
             │   ┌──┘
             │┌──┘
             └────────────────────────────
                                Low Data Rational
```

The slope of the personality-competency relationship is steeper for high-ability individuals, illustrating the moderation effect.

**DNV Logic (Diagrammatic, Numerical, Verbal):**

SHL's system implements this moderation through DNV Logic, which:

1. **Identifies relevant ability domain:** Each competency is mapped to relevant cognitive abilities (Numerical, Verbal, or Inductive)

2. **Checks ability level:** Assesses whether the candidate has sufficient cognitive capacity

3. **Applies moderation rule:** Adjusts personality-based prediction based on ability level

**Example DNV Logic Rule:**

```
IF Competency = "Analyzing and Interpreting" THEN
    Relevant_Ability = Numerical_Reasoning

    IF Numerical_Reasoning >= Sten 7 THEN
        Moderation_Factor = 1.0 (no penalty)
    ELSIF Numerical_Reasoning = Sten 5-6 THEN
        Moderation_Factor = 0.85 (mild penalty)
    ELSIF Numerical_Reasoning <= Sten 4 THEN
        Moderation_Factor = 0.70 (moderate penalty)
    END IF

    Competency_Score = Base_Score × Moderation_Factor
END IF
```

This logic acknowledges that personality preferences alone cannot overcome cognitive capacity limitations.

## 36.4 The Penalty Function: Addressing Preference-Ability Conflicts

![Figure 36.1: Cognitive ability as a moderator of personality-competency relationships](/psychometric-guide/images/Figure_36_01.png)

*Figure 36.1: Illustration of cognitive ability as a moderator of personality-competency relationships, showing how the DNV logic penalty function adjusts competency predictions when high personality preference is paired with low cognitive ability*

**Penalty Function Definition:**

The penalty function is an algorithmic adjustment that reduces competency predictions when there is a mismatch between personality preferences (high) and cognitive ability (low). This prevents the system from making unrealistic predictions based solely on preferences without capacity.

**Mathematical Implementation:**

**Base Prediction (Personality Only):**

Ĉⱼ = α + Σᵢ₌₁³² βⱼᵢPᵢ

**Penalty-Adjusted Prediction:**

Ĉⱼ_adjusted = Ĉⱼ × Penalty_Factor

Where:

Penalty_Factor = 1.0 - k × max(0, (P_threshold - A_score))

- k = penalty coefficient (typically 0.05-0.10)
- P_threshold = personality score requiring ability support
- A_score = relevant ability score (standardized)

**Example Application:**

**Scenario:** Candidate for analytical role
- OPQ Data Rational: Sten 9 (very high preference for data work)
- OPQ Evaluative: Sten 8 (critical thinking orientation)
- OPQ Detail Conscious: Sten 7 (attention to accuracy)

**Base Personality Prediction:**

Ĉ_Analyzing = 3.0 + (0.18 × 9) + (0.15 × 8) + (0.12 × 7) = 7.66 → **Sten 8**

**Now add Ability:**
- Verify Numerical Reasoning: Sten 3 (weak quantitative capacity)

**Penalty Calculation:**

Penalty_Factor = 1.0 - 0.08 × (9 - 3) = 1.0 - 0.48 = 0.52

**Adjusted Prediction:**

Ĉ_Analyzing_adjusted = 7.66 × 0.52 = 3.98 → **Sten 4**

The competency prediction drops from Sten 8 to Sten 4 due to the ability constraint.

**Narrative Implications:**

The penalty function triggers specific narrative text:

*"While John demonstrates strong interest in analytical work and enjoys working with data (Data Rational: High), his numerical reasoning capacity (Sten 3) may limit effectiveness in roles requiring complex quantitative analysis. He is likely to perform better in roles requiring data interpretation and presentation rather than advanced statistical modeling. Development support in quantitative methods may enhance analytical capability."*

**Ethical Considerations:**

The penalty function:
1. **Prevents Over-Prediction:** Avoids setting unrealistic expectations
2. **Identifies Development Needs:** Highlights specific capability gaps
3. **Supports Realistic Job Matching:** Helps place candidates in roles where they can succeed
4. **Maintains Validity:** Ensures predictions remain empirically grounded

**Limitations:**

1. **Threshold Sensitivity:** Penalty magnitude depends on where thresholds are set
2. **Binary Logic:** May not capture gradual degradation of effectiveness
3. **Context Dependency:** Some roles may compensate for ability limitations through other means (e.g., software tools, team support)

## 36.5 Weighted Formulas Integrating Both Sources

**Regression-Based Weighting:**

The integration of personality and ability data is formalized through regression equations derived from criterion validation studies. These equations specify precisely how much weight each predictor receives.

**General Formula:**

Ĉⱼ = α + Σᵢ₌₁³² βⱼᵢPᵢ + Σₖ₌₁³ γⱼₖAₖ + ε

Where:
- Ĉⱼ = Predicted competency score for competency j
- α = Intercept (baseline score)
- Pᵢ = OPQ personality trait score (i = 1 to 32 traits)
- Aₖ = Verify ability score (k = 1 to 3: Numerical, Verbal, Inductive)
- βⱼᵢ = Regression weight for personality trait i on competency j
- γⱼₖ = Regression weight for ability k on competency j
- ε = Error term

**Example: Analyzing and Interpreting Competency**

Based on validation research:

Ĉ_Analyzing = 2.5 +
    (0.18 × Data_Rational) +
    (0.15 × Evaluative) +
    (0.12 × Detail_Conscious) +
    (-0.10 × Variety_Seeking) +
    (-0.08 × Behavioral) +
    (0.226 × Numerical_Reasoning) +
    (0.142 × Verbal_Reasoning) +
    (0.089 × Inductive_Reasoning)

**Interpretation of Weights:**

**Numerical Reasoning (γ = 0.226):**
- Largest single predictor
- One Sten increase in Numerical Reasoning increases competency prediction by 0.226 Stens
- Reflects that analytical work is fundamentally cognitive

**Data Rational (β = 0.18):**
- Strongest personality predictor
- Reflects that preference for data work predicts engagement in analytical tasks

**Evaluative (β = 0.15):**
- Secondary personality predictor
- Critical thinking orientation supports analytical effectiveness

**Variety Seeking (β = -0.10):**
- Negative predictor
- High need for variety may undermine sustained analytical focus

**Relative Importance:**

To compare personality vs. ability contribution:

**Total Personality Contribution:** Σβ × P (varies by profile)
**Total Ability Contribution:** Σγ × A (varies by scores)

For typical high-analytical candidate:
- Personality contribution: ≈ 1.5-2.0 Stens
- Ability contribution: ≈ 2.0-3.0 Stens

Ability typically accounts for 55-65% of the prediction for cognitive competencies.

**Competency-Specific Weight Patterns:**

**Cognitive Competencies (Analyzing, Creating):**
- Ability weights > Personality weights
- Typical ratio: 60% ability, 40% personality

**Interpersonal Competencies (Interacting, Leading):**
- Personality weights > Ability weights
- Typical ratio: 75% personality, 25% ability

**Execution Competencies (Organizing, Delivering):**
- Balanced weights
- Typical ratio: 50% personality, 50% ability

**Validation and Refinement:**

Weights are derived from:
1. **Initial Validation Studies:** Regression analyses predicting supervisor ratings
2. **Cross-Validation:** Testing weight stability across different samples
3. **Ongoing Refinement:** SHL Labs analyzes accumulating data (millions of records) to refine weights
4. **Machine Learning Enhancement:** Modern systems use ML to identify previously undetected trait interactions

**Example Refinement:**

Initial weight for Data Rational on Analyzing competency: β = 0.15
After analyzing 100,000 cases with outcome data: β = 0.18
Refinement reflects that preference for data work is more predictive than initially estimated.

**Transparency and Validation:**

SHL publishes:
1. **Overall validity coefficients:** ρ values for each competency
2. **Weight magnitudes:** General indication of relative importance
3. **Methodology:** Explanation of derivation process

This transparency allows organizational psychologists to evaluate the appropriateness of the system for their specific contexts.

---

## Key Takeaways

- Workplace competencies require both preference (personality) and power (ability)
- Combining personality and ability data significantly improves predictive validity
- Ability acts as a cognitive moderator of personality-competency relationships
- The penalty function prevents over-prediction when preferences exceed capacity
- Regression-based weighting formulas optimize multi-source integration
- Weight patterns vary by competency type (cognitive, interpersonal, execution)
- Continuous validation and refinement improve prediction accuracy over time
- Transparency in methodology enables professional evaluation and trust

---

## Chapter Navigation

[← Previous: Chapter 35 - Specialized Report Types](/psychometric-guide/chapters/35-specialized-reports/)

[Next: Chapter 37 - Technology Evolution and Future →](/psychometric-guide/chapters/37-technology-future/)

[↑ Back to Home](/psychometric-guide/)
