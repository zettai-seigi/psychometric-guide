---
layout: default
title: "Chapter 28: Competency Prediction Algorithms"
parent: "Part VI: Scoring Methodologies"
nav_order: 5
---

# Competency Prediction Algorithms

### Learning Objectives

By the end of this chapter, you will be able to:

1. Understand the mathematical structure of SHL's competency prediction formula
2. Explain how regression weights (β, γ) are empirically derived
3. Describe the DNV Logic (Diagrammatic, Numerical, Verbal) for cognitive moderation
4. Interpret penalty functions that reconcile conflicts between preference and capacity
5. Evaluate the differential weighting of personality vs. ability for specific competencies
6. Articulate how the algorithm synthesizes multi-source data into holistic predictions
7. Appreciate the empirical foundation and continuous refinement of prediction models

### The Competency Prediction Challenge

The Universal Competency Framework defines 20 workplace competencies (e.g., Analyzing & Interpreting, Leading & Deciding, Adapting & Coping) that predict job performance. But how do we translate raw assessment scores—32 OPQ personality traits, 3 Verify ability scores, 18 MQ motivation dimensions—into a single, interpretable competency score?

This is the role of **competency prediction algorithms**: sophisticated mathematical models that weight and combine assessment scores to produce validated predictions.

### The Core Formula: Weighted Linear Combination

At the heart of SHL's competency prediction system is a regression equation:

**Ĉ_j = α + Σ(β_ji × P_i) + Σ(γ_jk × A_k) + ε**

Where:

- **Ĉ_j** = Predicted competency score for competency *j* (one of the 20 UCF dimensions)
- **α** = Intercept (constant term)
- **P_i** = Personality score for OPQ trait *i* (one of the 32 traits, typically as a sten score)
- **β_ji** = Regression weight linking personality trait *i* to competency *j*
- **A_k** = Ability score for Verify test *k* (Numerical, Verbal, Inductive, typically as theta or sten)
- **γ_jk** = Regression weight linking ability test *k* to competency *j*
- **ε** = Error term (residual variance not explained by predictors)
- **Σ** = Summation across all relevant predictors

**Interpretation**: The competency score is a weighted sum of relevant personality traits and ability scores, where weights reflect the empirical strength of each predictor.

#### Example: Predicting "Analyzing & Interpreting" (UCF Dimension)

**Relevant Predictors** (simplified for illustration):

**Personality (P_i)**:
- Data Rational (P₁): β₁ = +0.15
- Evaluative (P₂): β₂ = +0.12
- Conceptual (P₃): β₃ = +0.10
- Detail Conscious (P₄): β₄ = +0.08
- Worrying (P₅): β₅ = -0.05 (negative predictor—high anxiety impairs analytical performance)

**Ability (A_k)**:
- Numerical Reasoning (A₁): γ₁ = +0.226
- Verbal Reasoning (A₂): γ₂ = +0.10
- Inductive Reasoning (A₃): γ₃ = +0.15

**Candidate Scores**:
- Data Rational (P₁) = 8 (sten)
- Evaluative (P₂) = 7
- Conceptual (P₃) = 6
- Detail Conscious (P₄) = 7
- Worrying (P₅) = 4 (low worry = favorable)
- Numerical Reasoning (A₁) = 8 (sten)
- Verbal Reasoning (A₂) = 7
- Inductive Reasoning (A₃) = 7

**Calculation**:

Ĉ_Analyzing = α + (0.15×8) + (0.12×7) + (0.10×6) + (0.08×7) + (-0.05×4) + (0.226×8) + (0.10×7) + (0.15×7)

(Assuming α = 0 for simplicity)

= (1.20) + (0.84) + (0.60) + (0.56) + (-0.20) + (1.808) + (0.70) + (1.05)

= **6.578**

**Interpretation**: The candidate's predicted competency score for Analyzing & Interpreting is approximately 6.6 (on a sten-like scale), indicating **above-average potential**. Notice that Numerical Reasoning (weight = 0.226) contributed more than twice as much as Data Rational (weight = 0.15), reflecting the primacy of cognitive capacity for analytical tasks.

### Deriving Regression Weights: The Empirical Foundation

The regression weights (β, γ) are not arbitrary—they are **empirically derived** through validation research.

#### Process:

1. **Criterion Definition**: Define the competency behaviorally and identify how it will be measured (e.g., supervisor ratings, 360-degree feedback, objective metrics like sales volume).

2. **Sample Collection**: Collect data from a large sample of employees (n = 500-2,000+) who:
   - Have completed the OPQ32, Verify, and/or MQ.
   - Have been rated on job performance, ideally including specific competency ratings.

3. **Regression Analysis**: Conduct multiple regression analyses predicting competency ratings from the 32 OPQ traits and 3 Verify ability scores (35 predictors total).

   **Statistical Output**:
   - Each predictor receives a regression coefficient (β or γ) indicating its unique contribution to predicting the competency, controlling for all other predictors.
   - Coefficients are tested for statistical significance (p < 0.05).
   - Non-significant predictors are typically removed or assigned zero weight.

4. **Cross-Validation**: Test the regression equation on a separate hold-out sample to ensure the weights generalize (avoiding overfitting).

5. **Operational Implementation**: The validated regression weights are incorporated into the scoring algorithm used in Universal Competency Reports (UCR).

6. **Continuous Refinement**: As SHL accumulates more validation data, regression weights are periodically updated to reflect the best available evidence.

#### Example: "Leading & Deciding" Weights

Based on validation research, SHL might find:

**Significant Positive Predictors**:
- Persuasive (β = +0.20)
- Controlling (β = +0.18)
- Outgoing (β = +0.12)
- Achieving (β = +0.10)

**Significant Negative Predictors**:
- Worrying (β = -0.08)
- Socially Confident (reverse-scored for Modest; β = -0.05 for very high scores indicating arrogance)

**Ability Predictors**:
- Verbal Reasoning (γ = +0.15; leaders need to communicate clearly)
- Numerical Reasoning (γ = +0.08; minor contribution for decision-making)

**Non-Significant Predictors** (assigned weight = 0):
- Data Rational, Artistic, Caring, Detail Conscious (not uniquely predictive of leadership after controlling for other traits)

**Result**: The algorithm focuses on the empirically validated predictors, ignoring irrelevant traits.

### DNV Logic: Cognitive Moderation and Conflict Resolution

One of the most sophisticated features of SHL's competency prediction algorithm is **DNV Logic** (Diagrammatic, Numerical, Verbal Logic), which moderates personality predictions based on cognitive ability.

#### The Conceptual Foundation: Preference vs. Capacity

**Personality (OPQ)** reflects **preference** or **typical performance**: what the individual is inclined to do, given the choice.

**Ability (Verify)** reflects **capacity** or **maximal performance**: what the individual is capable of doing, under optimal conditions.

**Critical Insight**: High performance requires **both** preference and capacity. A candidate who loves working with numbers (high Data Rational) but has low Numerical Reasoning ability will struggle with quantitative tasks. Conversely, a candidate with high numerical ability but low preference may avoid such tasks.

DNV Logic formalizes this interaction.

#### The DNV Algorithm Process

1. **Calculate Personality Baseline**: Compute a weighted average of relevant OPQ traits to establish a personality-based prediction for the competency.

   **Example (Analyzing & Interpreting)**:
   Personality Baseline = 0.15×(Data Rational) + 0.12×(Evaluative) + 0.10×(Conceptual) + ...
   = 4.0 (on a 1-10 scale)

2. **Identify Required Cognitive Capacity**: Determine which Verify ability tests are relevant for the competency.
   - Analyzing & Interpreting: Primarily Numerical Reasoning, secondarily Verbal and Inductive.

3. **Check for Conflict**: Compare the candidate's personality preference and ability level.

   **Scenario A: Alignment (High Preference, High Ability)**:
   - Data Rational = 8 (high preference)
   - Numerical Reasoning = 8 (high capacity)
   - **Result**: No conflict. The candidate both likes numbers and is good at them. Predicted competency is high.

   **Scenario B: Conflict (High Preference, Low Ability)**:
   - Data Rational = 8 (high preference)
   - Numerical Reasoning = 3 (low capacity)
   - **Result**: Conflict detected. The candidate likes numbers but lacks the cognitive capacity to process them effectively.

   **Scenario C: Conflict (Low Preference, High Ability)**:
   - Data Rational = 3 (low preference)
   - Numerical Reasoning = 8 (high capacity)
   - **Result**: Conflict detected. The candidate can do numerical work but is unlikely to seek it out or sustain motivation.

4. **Apply Penalty Function**: When a conflict is detected, the algorithm applies a **penalty** to the overall competency prediction, lowering the score to reflect the limiting factor.

   **Penalty Logic (Simplified)**:
   - If Ability is low (sten ≤ 4), apply a substantial penalty (e.g., -1.5 to -2.0 points on the 1-10 competency scale), regardless of personality.
   - If Ability is moderate (sten 5-6) but Personality is very high (sten ≥ 8), apply a modest penalty (e.g., -0.5 to -1.0 points).
   - If Personality is low (sten ≤ 4) but Ability is high, apply a moderate penalty (e.g., -1.0 points), reflecting motivational risk.

   **Example (Scenario B Calculation)**:
   - Personality Baseline = 6.0 (high Data Rational, Evaluative, Conceptual)
   - Numerical Ability = 3 (sten)
   - **Penalty Applied**: -2.0 points
   - **Final Competency Score**: 6.0 - 2.0 = **4.0 (Moderate/Weakness)**

   **Interpretation**: Despite high personality preference for analytical work, the candidate's low cognitive capacity limits their competency potential. The final score is realistic, not inflated by personality alone.

5. **Narrative Generation**: The report generation engine selects pre-written text blocks that reflect the conflict:

   **Example Narrative**:
   "*While the candidate shows a strong preference for working with data and numbers (high Data Rational), their numerical reasoning ability is below average compared to the norm group. This may limit their effectiveness in complex quantitative analysis tasks. Development focus: Consider providing additional training or tools to support data interpretation.*"

### Differential Weighting: Ability Dominates for Cognitive Competencies

A critical finding from SHL's validation research is that **ability outweighs personality for cognitively demanding competencies**.

#### Published Empirical Evidence: "Analyzing & Interpreting"

**Personality-Only Model**:
- Validity: ρ = 0.22
- Primary predictors: Data Rational, Evaluative, Conceptual

**Ability-Only Model**:
- Validity: ρ = 0.40
- Primary predictor: Numerical Reasoning

**Combined Model (Personality + Ability)**:
- Validity: **ρ = 0.44**
- **Regression Weights**:
  - Ability (Numerical Reasoning): **γ = 0.226**
  - Personality (aggregate): **β = 0.122**
  - **Ratio**: Ability weight is **1.85 times larger** than personality weight.

**Interpretation**: For analytical competencies, cognitive capacity is the dominant predictor. Personality adds incremental validity, but ability does the heavy lifting.

#### Contrast: "Interacting & Presenting"

**Personality-Only Model**:
- Validity: ρ = 0.24
- Primary predictors: Persuasive, Outgoing, Socially Confident

**Ability-Only Model**:
- Validity: ρ = 0.30
- Primary predictor: Verbal Reasoning (communication requires verbal capacity)

**Combined Model**:
- Validity: **ρ = 0.40**
- **Regression Weights**:
  - Personality (aggregate): **β = 0.18**
  - Ability (Verbal Reasoning): **γ = 0.15**
  - **Ratio**: Weights are more balanced, with personality slightly dominant.

**Interpretation**: For interpersonal competencies, personality is critical (preference for social interaction), but verbal ability (capacity to articulate clearly) adds substantial value. The model reflects balanced weighting.

#### Contrast: "Adapting & Coping"

**Personality-Only Model**:
- Validity: ρ = 0.26
- Primary predictors: Relaxed (low anxiety), Adaptable, Optimistic

**Ability-Only Model**:
- Validity: ρ = 0.15
- Ability is weakly predictive (emotional regulation is not primarily cognitive)

**Combined Model**:
- Validity: **ρ = 0.30**
- **Regression Weights**:
  - Personality (aggregate): **β = 0.25**
  - Ability (aggregate): **γ = 0.08**
  - **Ratio**: Personality dominates.

**Interpretation**: For emotionally/temperamentally driven competencies, personality is the primary driver. Ability adds marginal incremental validity.

### Practical Example: Full Competency Prediction Workflow

Let's walk through a complete example of how the algorithm generates a competency score for a candidate.

**Candidate Profile**:
- **Name**: Alex
- **Role**: Financial Analyst (target competency: Analyzing & Interpreting)

**OPQ32r Scores (Stens)**:
- Data Rational: 8
- Evaluative: 7
- Conceptual: 6
- Detail Conscious: 7
- Worrying: 6 (moderate)
- (Other traits: various, not shown for brevity)

**Verify Scores (Stens)**:
- Numerical Reasoning: 4 (below average)
- Verbal Reasoning: 6
- Inductive Reasoning: 5

#### Step 1: Calculate Personality Baseline

Using regression weights for Analyzing & Interpreting:

Personality Contribution = (0.15 × 8) + (0.12 × 7) + (0.10 × 6) + (0.08 × 7) + (-0.05 × 6)
= 1.20 + 0.84 + 0.60 + 0.56 - 0.30
= **2.90**

#### Step 2: Calculate Ability Contribution (Without Moderation)

Ability Contribution = (0.226 × 4) + (0.10 × 6) + (0.15 × 5)
= 0.904 + 0.60 + 0.75
= **2.254**

#### Step 3: DNV Logic Check (Conflict Detection)

- **Numerical Reasoning = 4** (below average, sten < 5)
- **Data Rational = 8** (high preference)
- **Conflict**: High personality preference, low cognitive capacity.

**Penalty Applied**: -1.5 points (substantial penalty due to critical ability deficiency for analytical role)

#### Step 4: Calculate Final Competency Score

Ĉ_Analyzing = α + Personality Contribution + Ability Contribution + Penalty
= 2.5 (intercept) + 2.90 + 2.254 - 1.5
= **6.154**

Rounded to sten: **Sten 6 (Above Average, but constrained)**

#### Step 5: Narrative Generation

The report engine selects text blocks based on:
- Competency score (sten 6)
- High Data Rational (sten 8)
- Low Numerical Reasoning (sten 4)
- Conflict flag

**Generated Narrative**:

"**Analyzing & Interpreting: Moderate Potential (Sten 6)**

**Contributing Factors**:
- Alex shows a strong preference for working with data and numbers (high Data Rational), indicating genuine interest in analytical tasks.
- Alex demonstrates a critical and evaluative mindset (high Evaluative), questioning assumptions and seeking evidence.

**Limiting Factors**:
- Alex's numerical reasoning ability is below average for the norm group (Financial Analysts). This may constrain effectiveness in complex quantitative analysis, financial modeling, or statistical interpretation.
- **Development Recommendation**: Consider providing structured training in quantitative methods, access to analytical software with built-in guidance, or pairing with a mentor for complex numerical tasks. Monitor for potential frustration when faced with advanced quantitative challenges."

#### Step 6: Comparison to High-Ability Scenario

**Alternative Candidate: Jordan** (same personality, higher ability):
- Data Rational: 8
- Evaluative: 7
- Conceptual: 6
- Detail Conscious: 7
- Worrying: 6
- **Numerical Reasoning: 9** (very high)
- Verbal Reasoning: 7
- Inductive Reasoning: 8

**Recalculation**:

Personality Contribution = 2.90 (same)
Ability Contribution = (0.226 × 9) + (0.10 × 7) + (0.15 × 8) = 2.034 + 0.70 + 1.20 = **3.934**
Penalty = **0** (no conflict; high preference + high capacity)

Ĉ_Analyzing = 2.5 + 2.90 + 3.934 + 0 = **9.334**

Rounded to sten: **Sten 9 (High Potential)**

**Generated Narrative**:

"**Analyzing & Interpreting: High Potential (Sten 9)**

**Contributing Factors**:
- Jordan shows a strong preference for working with data and numbers (high Data Rational) and demonstrates exceptional numerical reasoning ability (sten 9). This combination is ideal for analytical roles requiring complex quantitative problem-solving.
- Jordan's critical and evaluative mindset (high Evaluative), combined with strong conceptual reasoning (high Inductive Reasoning), enables sophisticated data interpretation and strategic insights.

**No Significant Limiting Factors Identified.**

**Recommendation**: Jordan is well-suited for advanced analytical tasks, financial modeling, data science, or strategic analysis roles. Consider opportunities for leadership in analytical projects."

**Key Insight**: The same personality profile yields vastly different competency predictions (sten 6 vs. sten 9) depending on cognitive ability, demonstrating the critical role of DNV Logic and penalty functions.

### Continuous Refinement: Machine Learning and Big Data

While the core competency prediction algorithm is based on regression equations derived from traditional validation studies, SHL has increasingly incorporated **machine learning** and **big data analytics** to refine predictions.

#### Approaches:

1. **Accumulating Validation Data**: With millions of assessments and thousands of validation studies, SHL maintains a massive database linking assessment scores to performance outcomes.

2. **Pattern Recognition**: Machine learning algorithms (e.g., random forests, gradient boosting) can identify non-linear relationships and interaction effects that traditional regression might miss.

3. **Dynamic Weighting**: For clients with large internal datasets, SHL can conduct organization-specific validation studies, generating **customized regression weights** tailored to that company's performance criteria and culture.

4. **Automated Anomaly Detection**: AI systems flag unusual response patterns (e.g., random responding, extreme faking) that might invalidate scores.

5. **Narrative Personalization**: Natural language processing (NLP) algorithms generate more nuanced, individualized narrative text based on the specific pattern of strengths and weaknesses, rather than relying solely on pre-written templates.

**Ethical Guardrails**: SHL emphasizes that machine learning models are used to *enhance* but not *replace* psychometric rigor. All algorithms are validated for fairness, transparency, and compliance with professional standards (EEOC, SIOP, ITC Guidelines).

### Key Takeaways

1. **The competency prediction formula** is a weighted linear combination: **Ĉ_j = α + Σ(β_ji × P_i) + Σ(γ_jk × A_k) + ε**, synthesizing personality (P) and ability (A) scores using empirically derived regression weights (β, γ).

2. **Regression weights are derived from validation research**, where criterion performance ratings are regressed on the 32 OPQ traits and 3 Verify ability scores, ensuring predictions are evidence-based.

3. **DNV Logic (Diagrammatic, Numerical, Verbal Logic)** moderates personality predictions based on cognitive ability, recognizing that competencies require both preference (personality) and capacity (ability).

4. **Penalty functions** are applied when conflicts are detected (e.g., high personality preference but low cognitive ability), lowering competency predictions to realistic levels and generating narratives that flag developmental needs.

5. **Ability outweighs personality for cognitively demanding competencies**: For Analyzing & Interpreting, ability is weighted **1.85 times higher** than personality (γ = 0.226 vs. β = 0.122), and combined validity reaches **ρ = 0.44**.

6. **Personality dominates for interpersonal and emotional competencies**: For Adapting & Coping, personality is weighted much higher than ability, reflecting the temperamental nature of stress resilience.

7. **Narrative generation** is automated based on competency scores, trait patterns, and conflict flags, producing personalized, actionable feedback (e.g., "While likely to enjoy working with data, the candidate may struggle with complex numerical concepts").

8. **Continuous refinement through machine learning** and big data analytics enhances prediction accuracy, identifies non-linear patterns, and enables organization-specific customization while maintaining psychometric rigor.

9. **The algorithm's sophistication** enables SHL to deliver **holistic, multi-source talent profiles** that integrate personality, ability, and motivation into validated predictions of workplace competencies, supporting selection, development, and succession planning.

---

## Chapter Navigation

[← Previous: Chapter 27 - Validity and Reliability Evidence](/psychometric-guide/chapters/27-validity/)

[Next: Chapter 29 - Industry Quality Convergence →](/psychometric-guide/chapters/29-industry-convergence/)

[↑ Back to Home](/psychometric-guide/)


### Learning Objectives

By the end of this chapter, you will be able to:

1. Understand the mathematical structure of SHL's competency prediction formula
2. Explain how regression weights (β, γ) are empirically derived
3. Describe the DNV Logic (Diagrammatic, Numerical, Verbal) for cognitive moderation
4. Interpret penalty functions that reconcile conflicts between preference and capacity
5. Evaluate the differential weighting of personality vs. ability for specific competencies
6. Articulate how the algorithm synthesizes multi-source data into holistic predictions
7. Appreciate the empirical foundation and continuous refinement of prediction models

### The Competency Prediction Challenge

The Universal Competency Framework defines 20 workplace competencies (e.g., Analyzing & Interpreting, Leading & Deciding, Adapting & Coping) that predict job performance. But how do we translate raw assessment scores—32 OPQ personality traits, 3 Verify ability scores, 18 MQ motivation dimensions—into a single, interpretable competency score?

This is the role of **competency prediction algorithms**: sophisticated mathematical models that weight and combine assessment scores to produce validated predictions.

### The Core Formula: Weighted Linear Combination

At the heart of SHL's competency prediction system is a regression equation:

**Ĉ_j = α + Σ(β_ji × P_i) + Σ(γ_jk × A_k) + ε**

Where:

- **Ĉ_j** = Predicted competency score for competency *j* (one of the 20 UCF dimensions)
- **α** = Intercept (constant term)
- **P_i** = Personality score for OPQ trait *i* (one of the 32 traits, typically as a sten score)
- **β_ji** = Regression weight linking personality trait *i* to competency *j*
- **A_k** = Ability score for Verify test *k* (Numerical, Verbal, Inductive, typically as theta or sten)
- **γ_jk** = Regression weight linking ability test *k* to competency *j*
- **ε** = Error term (residual variance not explained by predictors)
- **Σ** = Summation across all relevant predictors

**Interpretation**: The competency score is a weighted sum of relevant personality traits and ability scores, where weights reflect the empirical strength of each predictor.

#### Example: Predicting "Analyzing & Interpreting" (UCF Dimension)

**Relevant Predictors** (simplified for illustration):

**Personality (P_i)**:
- Data Rational (P₁): β₁ = +0.15
- Evaluative (P₂): β₂ = +0.12
- Conceptual (P₃): β₃ = +0.10
- Detail Conscious (P₄): β₄ = +0.08
- Worrying (P₅): β₅ = -0.05 (negative predictor—high anxiety impairs analytical performance)

**Ability (A_k)**:
- Numerical Reasoning (A₁): γ₁ = +0.226
- Verbal Reasoning (A₂): γ₂ = +0.10
- Inductive Reasoning (A₃): γ₃ = +0.15

**Candidate Scores**:
- Data Rational (P₁) = 8 (sten)
- Evaluative (P₂) = 7
- Conceptual (P₃) = 6
- Detail Conscious (P₄) = 7
- Worrying (P₅) = 4 (low worry = favorable)
- Numerical Reasoning (A₁) = 8 (sten)
- Verbal Reasoning (A₂) = 7
- Inductive Reasoning (A₃) = 7

**Calculation**:

Ĉ_Analyzing = α + (0.15×8) + (0.12×7) + (0.10×6) + (0.08×7) + (-0.05×4) + (0.226×8) + (0.10×7) + (0.15×7)

(Assuming α = 0 for simplicity)

= (1.20) + (0.84) + (0.60) + (0.56) + (-0.20) + (1.808) + (0.70) + (1.05)

= **6.578**

**Interpretation**: The candidate's predicted competency score for Analyzing & Interpreting is approximately 6.6 (on a sten-like scale), indicating **above-average potential**. Notice that Numerical Reasoning (weight = 0.226) contributed more than twice as much as Data Rational (weight = 0.15), reflecting the primacy of cognitive capacity for analytical tasks.

### Deriving Regression Weights: The Empirical Foundation

The regression weights (β, γ) are not arbitrary—they are **empirically derived** through validation research.

#### Process:

1. **Criterion Definition**: Define the competency behaviorally and identify how it will be measured (e.g., supervisor ratings, 360-degree feedback, objective metrics like sales volume).

2. **Sample Collection**: Collect data from a large sample of employees (n = 500-2,000+) who:
   - Have completed the OPQ32, Verify, and/or MQ.
   - Have been rated on job performance, ideally including specific competency ratings.

3. **Regression Analysis**: Conduct multiple regression analyses predicting competency ratings from the 32 OPQ traits and 3 Verify ability scores (35 predictors total).

   **Statistical Output**:
   - Each predictor receives a regression coefficient (β or γ) indicating its unique contribution to predicting the competency, controlling for all other predictors.
   - Coefficients are tested for statistical significance (p < 0.05).
   - Non-significant predictors are typically removed or assigned zero weight.

4. **Cross-Validation**: Test the regression equation on a separate hold-out sample to ensure the weights generalize (avoiding overfitting).

5. **Operational Implementation**: The validated regression weights are incorporated into the scoring algorithm used in Universal Competency Reports (UCR).

6. **Continuous Refinement**: As SHL accumulates more validation data, regression weights are periodically updated to reflect the best available evidence.

#### Example: "Leading & Deciding" Weights

Based on validation research, SHL might find:

**Significant Positive Predictors**:
- Persuasive (β = +0.20)
- Controlling (β = +0.18)
- Outgoing (β = +0.12)
- Achieving (β = +0.10)

**Significant Negative Predictors**:
- Worrying (β = -0.08)
- Socially Confident (reverse-scored for Modest; β = -0.05 for very high scores indicating arrogance)

**Ability Predictors**:
- Verbal Reasoning (γ = +0.15; leaders need to communicate clearly)
- Numerical Reasoning (γ = +0.08; minor contribution for decision-making)

**Non-Significant Predictors** (assigned weight = 0):
- Data Rational, Artistic, Caring, Detail Conscious (not uniquely predictive of leadership after controlling for other traits)

**Result**: The algorithm focuses on the empirically validated predictors, ignoring irrelevant traits.

### DNV Logic: Cognitive Moderation and Conflict Resolution

One of the most sophisticated features of SHL's competency prediction algorithm is **DNV Logic** (Diagrammatic, Numerical, Verbal Logic), which moderates personality predictions based on cognitive ability.

#### The Conceptual Foundation: Preference vs. Capacity

**Personality (OPQ)** reflects **preference** or **typical performance**: what the individual is inclined to do, given the choice.

**Ability (Verify)** reflects **capacity** or **maximal performance**: what the individual is capable of doing, under optimal conditions.

**Critical Insight**: High performance requires **both** preference and capacity. A candidate who loves working with numbers (high Data Rational) but has low Numerical Reasoning ability will struggle with quantitative tasks. Conversely, a candidate with high numerical ability but low preference may avoid such tasks.

DNV Logic formalizes this interaction.

#### The DNV Algorithm Process

1. **Calculate Personality Baseline**: Compute a weighted average of relevant OPQ traits to establish a personality-based prediction for the competency.

   **Example (Analyzing & Interpreting)**:
   Personality Baseline = 0.15×(Data Rational) + 0.12×(Evaluative) + 0.10×(Conceptual) + ...
   = 4.0 (on a 1-10 scale)

2. **Identify Required Cognitive Capacity**: Determine which Verify ability tests are relevant for the competency.
   - Analyzing & Interpreting: Primarily Numerical Reasoning, secondarily Verbal and Inductive.

3. **Check for Conflict**: Compare the candidate's personality preference and ability level.

   **Scenario A: Alignment (High Preference, High Ability)**:
   - Data Rational = 8 (high preference)
   - Numerical Reasoning = 8 (high capacity)
   - **Result**: No conflict. The candidate both likes numbers and is good at them. Predicted competency is high.

   **Scenario B: Conflict (High Preference, Low Ability)**:
   - Data Rational = 8 (high preference)
   - Numerical Reasoning = 3 (low capacity)
   - **Result**: Conflict detected. The candidate likes numbers but lacks the cognitive capacity to process them effectively.

   **Scenario C: Conflict (Low Preference, High Ability)**:
   - Data Rational = 3 (low preference)
   - Numerical Reasoning = 8 (high capacity)
   - **Result**: Conflict detected. The candidate can do numerical work but is unlikely to seek it out or sustain motivation.

4. **Apply Penalty Function**: When a conflict is detected, the algorithm applies a **penalty** to the overall competency prediction, lowering the score to reflect the limiting factor.

   **Penalty Logic (Simplified)**:
   - If Ability is low (sten ≤ 4), apply a substantial penalty (e.g., -1.5 to -2.0 points on the 1-10 competency scale), regardless of personality.
   - If Ability is moderate (sten 5-6) but Personality is very high (sten ≥ 8), apply a modest penalty (e.g., -0.5 to -1.0 points).
   - If Personality is low (sten ≤ 4) but Ability is high, apply a moderate penalty (e.g., -1.0 points), reflecting motivational risk.

   **Example (Scenario B Calculation)**:
   - Personality Baseline = 6.0 (high Data Rational, Evaluative, Conceptual)
   - Numerical Ability = 3 (sten)
   - **Penalty Applied**: -2.0 points
   - **Final Competency Score**: 6.0 - 2.0 = **4.0 (Moderate/Weakness)**

   **Interpretation**: Despite high personality preference for analytical work, the candidate's low cognitive capacity limits their competency potential. The final score is realistic, not inflated by personality alone.

5. **Narrative Generation**: The report generation engine selects pre-written text blocks that reflect the conflict:

   **Example Narrative**:
   "*While the candidate shows a strong preference for working with data and numbers (high Data Rational), their numerical reasoning ability is below average compared to the norm group. This may limit their effectiveness in complex quantitative analysis tasks. Development focus: Consider providing additional training or tools to support data interpretation.*"

### Differential Weighting: Ability Dominates for Cognitive Competencies

A critical finding from SHL's validation research is that **ability outweighs personality for cognitively demanding competencies**.

#### Published Empirical Evidence: "Analyzing & Interpreting"

**Personality-Only Model**:
- Validity: ρ = 0.22
- Primary predictors: Data Rational, Evaluative, Conceptual

**Ability-Only Model**:
- Validity: ρ = 0.40
- Primary predictor: Numerical Reasoning

**Combined Model (Personality + Ability)**:
- Validity: **ρ = 0.44**
- **Regression Weights**:
  - Ability (Numerical Reasoning): **γ = 0.226**
  - Personality (aggregate): **β = 0.122**
  - **Ratio**: Ability weight is **1.85 times larger** than personality weight.

**Interpretation**: For analytical competencies, cognitive capacity is the dominant predictor. Personality adds incremental validity, but ability does the heavy lifting.

#### Contrast: "Interacting & Presenting"

**Personality-Only Model**:
- Validity: ρ = 0.24
- Primary predictors: Persuasive, Outgoing, Socially Confident

**Ability-Only Model**:
- Validity: ρ = 0.30
- Primary predictor: Verbal Reasoning (communication requires verbal capacity)

**Combined Model**:
- Validity: **ρ = 0.40**
- **Regression Weights**:
  - Personality (aggregate): **β = 0.18**
  - Ability (Verbal Reasoning): **γ = 0.15**
  - **Ratio**: Weights are more balanced, with personality slightly dominant.

**Interpretation**: For interpersonal competencies, personality is critical (preference for social interaction), but verbal ability (capacity to articulate clearly) adds substantial value. The model reflects balanced weighting.

#### Contrast: "Adapting & Coping"

**Personality-Only Model**:
- Validity: ρ = 0.26
- Primary predictors: Relaxed (low anxiety), Adaptable, Optimistic

**Ability-Only Model**:
- Validity: ρ = 0.15
- Ability is weakly predictive (emotional regulation is not primarily cognitive)

**Combined Model**:
- Validity: **ρ = 0.30**
- **Regression Weights**:
  - Personality (aggregate): **β = 0.25**
  - Ability (aggregate): **γ = 0.08**
  - **Ratio**: Personality dominates.

**Interpretation**: For emotionally/temperamentally driven competencies, personality is the primary driver. Ability adds marginal incremental validity.

### Practical Example: Full Competency Prediction Workflow

Let's walk through a complete example of how the algorithm generates a competency score for a candidate.

**Candidate Profile**:
- **Name**: Alex
- **Role**: Financial Analyst (target competency: Analyzing & Interpreting)

**OPQ32r Scores (Stens)**:
- Data Rational: 8
- Evaluative: 7
- Conceptual: 6
- Detail Conscious: 7
- Worrying: 6 (moderate)
- (Other traits: various, not shown for brevity)

**Verify Scores (Stens)**:
- Numerical Reasoning: 4 (below average)
- Verbal Reasoning: 6
- Inductive Reasoning: 5

#### Step 1: Calculate Personality Baseline

Using regression weights for Analyzing & Interpreting:

Personality Contribution = (0.15 × 8) + (0.12 × 7) + (0.10 × 6) + (0.08 × 7) + (-0.05 × 6)
= 1.20 + 0.84 + 0.60 + 0.56 - 0.30
= **2.90**

#### Step 2: Calculate Ability Contribution (Without Moderation)

Ability Contribution = (0.226 × 4) + (0.10 × 6) + (0.15 × 5)
= 0.904 + 0.60 + 0.75
= **2.254**

#### Step 3: DNV Logic Check (Conflict Detection)

- **Numerical Reasoning = 4** (below average, sten < 5)
- **Data Rational = 8** (high preference)
- **Conflict**: High personality preference, low cognitive capacity.

**Penalty Applied**: -1.5 points (substantial penalty due to critical ability deficiency for analytical role)

#### Step 4: Calculate Final Competency Score

Ĉ_Analyzing = α + Personality Contribution + Ability Contribution + Penalty
= 2.5 (intercept) + 2.90 + 2.254 - 1.5
= **6.154**

Rounded to sten: **Sten 6 (Above Average, but constrained)**

#### Step 5: Narrative Generation

The report engine selects text blocks based on:
- Competency score (sten 6)
- High Data Rational (sten 8)
- Low Numerical Reasoning (sten 4)
- Conflict flag

**Generated Narrative**:

"**Analyzing & Interpreting: Moderate Potential (Sten 6)**

**Contributing Factors**:
- Alex shows a strong preference for working with data and numbers (high Data Rational), indicating genuine interest in analytical tasks.
- Alex demonstrates a critical and evaluative mindset (high Evaluative), questioning assumptions and seeking evidence.

**Limiting Factors**:
- Alex's numerical reasoning ability is below average for the norm group (Financial Analysts). This may constrain effectiveness in complex quantitative analysis, financial modeling, or statistical interpretation.
- **Development Recommendation**: Consider providing structured training in quantitative methods, access to analytical software with built-in guidance, or pairing with a mentor for complex numerical tasks. Monitor for potential frustration when faced with advanced quantitative challenges."

#### Step 6: Comparison to High-Ability Scenario

**Alternative Candidate: Jordan** (same personality, higher ability):
- Data Rational: 8
- Evaluative: 7
- Conceptual: 6
- Detail Conscious: 7
- Worrying: 6
- **Numerical Reasoning: 9** (very high)
- Verbal Reasoning: 7
- Inductive Reasoning: 8

**Recalculation**:

Personality Contribution = 2.90 (same)
Ability Contribution = (0.226 × 9) + (0.10 × 7) + (0.15 × 8) = 2.034 + 0.70 + 1.20 = **3.934**
Penalty = **0** (no conflict; high preference + high capacity)

Ĉ_Analyzing = 2.5 + 2.90 + 3.934 + 0 = **9.334**

Rounded to sten: **Sten 9 (High Potential)**

**Generated Narrative**:

"**Analyzing & Interpreting: High Potential (Sten 9)**

**Contributing Factors**:
- Jordan shows a strong preference for working with data and numbers (high Data Rational) and demonstrates exceptional numerical reasoning ability (sten 9). This combination is ideal for analytical roles requiring complex quantitative problem-solving.
- Jordan's critical and evaluative mindset (high Evaluative), combined with strong conceptual reasoning (high Inductive Reasoning), enables sophisticated data interpretation and strategic insights.

**No Significant Limiting Factors Identified.**

**Recommendation**: Jordan is well-suited for advanced analytical tasks, financial modeling, data science, or strategic analysis roles. Consider opportunities for leadership in analytical projects."

**Key Insight**: The same personality profile yields vastly different competency predictions (sten 6 vs. sten 9) depending on cognitive ability, demonstrating the critical role of DNV Logic and penalty functions.

### Continuous Refinement: Machine Learning and Big Data

While the core competency prediction algorithm is based on regression equations derived from traditional validation studies, SHL has increasingly incorporated **machine learning** and **big data analytics** to refine predictions.

#### Approaches:

1. **Accumulating Validation Data**: With millions of assessments and thousands of validation studies, SHL maintains a massive database linking assessment scores to performance outcomes.

2. **Pattern Recognition**: Machine learning algorithms (e.g., random forests, gradient boosting) can identify non-linear relationships and interaction effects that traditional regression might miss.

3. **Dynamic Weighting**: For clients with large internal datasets, SHL can conduct organization-specific validation studies, generating **customized regression weights** tailored to that company's performance criteria and culture.

4. **Automated Anomaly Detection**: AI systems flag unusual response patterns (e.g., random responding, extreme faking) that might invalidate scores.

5. **Narrative Personalization**: Natural language processing (NLP) algorithms generate more nuanced, individualized narrative text based on the specific pattern of strengths and weaknesses, rather than relying solely on pre-written templates.

**Ethical Guardrails**: SHL emphasizes that machine learning models are used to *enhance* but not *replace* psychometric rigor. All algorithms are validated for fairness, transparency, and compliance with professional standards (EEOC, SIOP, ITC Guidelines).

### Key Takeaways

1. **The competency prediction formula** is a weighted linear combination: **Ĉ_j = α + Σ(β_ji × P_i) + Σ(γ_jk × A_k) + ε**, synthesizing personality (P) and ability (A) scores using empirically derived regression weights (β, γ).

2. **Regression weights are derived from validation research**, where criterion performance ratings are regressed on the 32 OPQ traits and 3 Verify ability scores, ensuring predictions are evidence-based.

3. **DNV Logic (Diagrammatic, Numerical, Verbal Logic)** moderates personality predictions based on cognitive ability, recognizing that competencies require both preference (personality) and capacity (ability).

4. **Penalty functions** are applied when conflicts are detected (e.g., high personality preference but low cognitive ability), lowering competency predictions to realistic levels and generating narratives that flag developmental needs.

5. **Ability outweighs personality for cognitively demanding competencies**: For Analyzing & Interpreting, ability is weighted **1.85 times higher** than personality (γ = 0.226 vs. β = 0.122), and combined validity reaches **ρ = 0.44**.

6. **Personality dominates for interpersonal and emotional competencies**: For Adapting & Coping, personality is weighted much higher than ability, reflecting the temperamental nature of stress resilience.

7. **Narrative generation** is automated based on competency scores, trait patterns, and conflict flags, producing personalized, actionable feedback (e.g., "While likely to enjoy working with data, the candidate may struggle with complex numerical concepts").

8. **Continuous refinement through machine learning** and big data analytics enhances prediction accuracy, identifies non-linear patterns, and enables organization-specific customization while maintaining psychometric rigor.

9. **The algorithm's sophistication** enables SHL to deliver **holistic, multi-source talent profiles** that integrate personality, ability, and motivation into validated predictions of workplace competencies, supporting selection, development, and succession planning.

---


