---
layout: default
title: "Chapter 30: Personality Assessment Comparison"
parent: "Part VII: Competitive Landscape"
nav_order: 2
permalink: /chapters/30-personality-comparison/
---

# Chapter 30: Personality Assessment Comparison

## Learning Objectives

- Compare OPQ32r with competing personality assessments across format, scoring, and theoretical foundations
- Analyze methodological differences between forced-choice and normative formats
- Evaluate faking resistance mechanisms across major personality instruments
- Understand the Thurstonian IRT breakthrough and its competitive significance
- Assess validity evidence and practical trade-offs across personality measures

## Introduction

The personality assessment market features several scientifically robust instruments, each distinguished by its methodological approach to measuring workplace personality. While major vendors achieve comparable predictive validity, they differ fundamentally in format, scoring methodology, and theoretical foundation. This chapter provides a comprehensive comparison of leading personality assessments, with particular focus on the methodological innovations that differentiate them.

## Overview of Major Personality Assessments

### The Competitive Landscape

Three major personality assessments dominate the workplace assessment market:

**SHL's OPQ32r (Occupational Personality Questionnaire, revision r):**
- Developed by Saville & Holdsworth Ltd. in the 1980s, revised to forced-choice format in the mid-2000s
- Measures 32 specific workplace personality traits
- Uses forced-choice triplet format with Thurstonian IRT scoring
- Explicitly designed for occupational settings
- Links to Universal Competency Framework (UCF)

**Hogan Personality Inventory (HPI):**
- Developed by Robert and Joyce Hogan in the 1980s
- Measures 7 primary scales based on Socioanalytic Theory
- Uses normative True/False format with Classical Test Theory scoring
- Focuses on reputation (how others see you) rather than identity
- Often paired with HDS (Hogan Development Survey) and MVPI (Motives, Values, Preferences Inventory)

**Saville Wave Professional Styles:**
- Developed by Peter Saville (co-founder of SHL) in the 2000s
- Measures 36 facets aligned with the Performance Culture Framework
- Uses hybrid "Rate and Rank" format with proprietary dual scoring
- Combines normative rating and ipsative ranking
- Aims to maximize psychometric information while resisting faking

### Theoretical Foundations

Each instrument reflects distinct theoretical perspectives:

**OPQ32r - Workplace Trait Model:**
The OPQ was constructed through a pragmatic, criterion-focused approach:
- Items directly reference workplace behaviors and preferences
- Trait structure derived from factor analysis of work-relevant content
- Can be mapped to Big Five but optimized for occupational prediction
- 32 traits provide fine-grained differentiation for job matching

**Hogan HPI - Socioanalytic Theory:**
Hogan's approach emphasizes reputation over self-concept:
- Personality reflects how we manage our reputation in social contexts
- Seven scales represent fundamental dimensions of social interaction
- Focus on observable behavior that affects career success
- Theoretically grounded in evolutionary and psychoanalytic perspectives

**Saville Wave - Performance Culture Framework:**
Wave integrates traits with performance domains:
- 36 facets organized into four clusters (Thought, Influence, Adaptability, Delivery)
- Blends personality with aspects of ability and motivation
- Designed to maximize construct coverage
- Emphasizes both preference (typical behavior) and competence (capability)

## Detailed Methodological Comparison

### Format Comparison

The assessment format fundamentally shapes the measurement properties and candidate experience:

| Feature | SHL OPQ32r | Hogan HPI | Saville Wave |
|---------|-----------|-----------|--------------|
| **Format Type** | Forced-choice triplets | Normative True/False | Hybrid Rate & Rank |
| **Item Structure** | 104 blocks of 3 statements (312 items total) | 206 True/False items | Two stages: Rate 108 statements, then Rank in blocks |
| **Response Process** | Choose "Most like me" and "Least like me" from 3 options | Agree/Disagree with each statement independently | First rate each item 1-4, then rank within blocks |
| **Completion Time** | 25-30 minutes | 15-20 minutes | 35-40 minutes |
| **Ipsative Nature** | Fully ipsative (within-person comparisons) | Fully normative (independent ratings) | Dual: Normative ratings + Ipsative rankings |

**SHL OPQ32r - Forced-Choice Triplets:**

Example block:
```
Choose which statement is MOST like you and which is LEAST like you:

A. I enjoy analyzing complex data
B. I prefer working as part of a team
C. I like to be in charge of projects

Most like me: [ ]   Least like me: [ ]
```

Each block contains three statements measuring different traits. The forced-choice format prevents candidates from endorsing all desirable traits equally, forcing trade-offs that reveal relative trait standing.

**Hogan HPI - Normative True/False:**

Example items:
```
1. I enjoy being the center of attention.        [True] [False]
2. I prefer to work on my own.                   [True] [False]
3. I rarely get upset or worried.                [True] [False]
```

Candidates respond to each statement independently, allowing them to agree with all items if they choose. This transparency makes the assessment more fakeable but also more intuitive to complete.

**Saville Wave - Hybrid Rate & Rank:**

Stage 1 - Rating:
```
How well does each statement describe you?
1 = Not at all    2 = Slightly    3 = Mostly    4 = Completely

I enjoy analyzing data:                    [1] [2] [3] [4]
I prefer working in teams:                 [1] [2] [3] [4]
I like leading projects:                   [1] [2] [3] [4]
```

Stage 2 - Ranking:
```
Now rank these statements you just rated:
Which is MOST like you?    [ ]
Which is LEAST like you?   [ ]
```

This dual-response format captures both absolute endorsement (normative) and relative preference (ipsative), providing rich data for scoring algorithms.

### Scoring Methodology Comparison

Scoring methodology represents the most significant technical differentiation:

| Feature | SHL OPQ32r | Hogan HPI | Saville Wave |
|---------|-----------|-----------|--------------|
| **Scoring Theory** | Thurstonian Item Response Theory (IRT) | Classical Test Theory (CTT) | Proprietary dual-scoring algorithm |
| **Score Type** | Latent trait estimates (θ) converted to stens | Raw score summation converted to T-scores | Dual scores: Normative percentiles + Ipsative stens |
| **Calibration** | IRT parameters (discrimination, threshold) | Item-total correlations | Complex integration of ratings and rankings |
| **Norm Referencing** | θ estimates compared to norm group | Raw score compared to norm group | Separate norms for normative and ipsative scores |
| **Measurement Model** | Multidimensional IRT (traits estimated jointly) | Unidimensional CTT (traits scored independently) | Hybrid model integrating both response types |

**SHL OPQ32r - Thurstonian IRT:**

The Thurstonian IRT model represents a major psychometric breakthrough, solving the statistical problems inherent in traditional ipsative scoring:

Mathematical Foundation:
```
When a candidate chooses item i over item j in a forced-choice block:
    θᵢ - θⱼ > τᵢⱼ + εᵢⱼ

Where:
    θᵢ = latent trait level for trait i
    θⱼ = latent trait level for trait j
    τᵢⱼ = threshold difference between items
    εᵢⱼ = random error
```

The Thurstonian IRT model estimates all 32 trait scores simultaneously by modeling the pairwise comparisons across all forced-choice blocks. This allows recovery of **normative-equivalent scores** from ipsative response patterns.

Key advantages:
- Maintains faking resistance of forced-choice format
- Produces normative scores suitable for between-person comparison
- Accounts for varying item discrimination
- Provides trait-level reliability estimates

**Hogan HPI - Classical Test Theory:**

The HPI uses straightforward classical scoring:

```
Trait Score = Σ (Item Response × Item Weight)

For True/False items:
    True = 1, False = 0

Scale Score = Sum of keyed items
```

Scores are then:
1. Summed across items for each of the 7 scales
2. Converted to T-scores (M = 50, SD = 10) based on norm group
3. Interpreted using percentile bands

Advantages:
- Transparent and easily understood
- Well-established psychometric properties
- Straightforward interpretation
- No complex estimation algorithms required

Limitations:
- More susceptible to impression management
- Cannot leverage within-person comparisons
- Assumes equal item discrimination

**Saville Wave - Proprietary Dual Scoring:**

Wave's scoring integrates normative ratings with ipsative rankings:

1. **Normative Score:** Calculated from the initial 1-4 ratings, providing absolute endorsement level
2. **Ipsative Score:** Calculated from the forced-choice rankings, providing relative preference pattern
3. **Integrated Score:** Proprietary algorithm combines both sources to produce final trait estimates

Additional features:
- **Consistency Index:** Measures alignment between ratings and rankings, flagging inconsistent responding
- **Dual Interpretation:** Reports can emphasize either normative standing or ipsative pattern
- **Validity Maximization:** Aims to capture benefits of both formats

The exact algorithm is proprietary, but the approach aims to:
- Use normative data for between-person comparisons
- Use ipsative data for faking resistance
- Integrate both for maximum validity

### Faking Resistance Comparison

Response format directly determines susceptibility to impression management:

| Feature | SHL OPQ32r | Hogan HPI | Saville Wave |
|---------|-----------|-----------|--------------|
| **Faking Resistance** | Highly resistant | More prone to faking | Resistant (hybrid approach) |
| **Mechanism** | Forced choice prevents inflating all traits | No format-based protection | Rate & Rank combination provides partial resistance |
| **Social Desirability** | Cannot simultaneously endorse all desirable options | Can endorse all desirable statements | Rating stage vulnerable, ranking stage protected |
| **Validity in High-Stakes** | Maintains validity in selection contexts | May show inflation in selection contexts | Moderate protection in selection contexts |
| **Research Evidence** | Extensive evidence of faking resistance | Acknowledges potential for faking | Claims improved validity over pure normative |

**SHL OPQ32r - Forced-Choice Protection:**

The forced-choice format makes systematic faking extremely difficult:

Faking Challenge:
- To inflate one trait, you must deflate another
- Blocks mix traits in unpredictable combinations
- Optimal faking strategy would require knowing the "target profile" and the item-to-trait mapping
- Even with this knowledge, forced choices create unavoidable trade-offs

Research findings:
- Forced-choice formats show minimal score inflation in high-stakes settings
- Score distributions remain similar across applicant and development contexts
- Criterion validity is maintained in selection applications

**Hogan HPI - Limited Protection:**

The normative format offers no inherent faking resistance:

Faking Vulnerability:
- Candidates can endorse all socially desirable statements
- No trade-offs required
- Transparent item content reveals desirable responses

Mitigation strategies:
- Item writing emphasizes subtle content
- Some items use "corrective" keying
- Validity scales detect unusual response patterns
- Reliance on candidate motivation for honest responding

Research findings:
- Score inflation observed in applicant samples vs. development samples
- Criterion validity may be attenuated in high-stakes settings
- Effectiveness depends on candidate sophistication and motivation

**Saville Wave - Hybrid Protection:**

The Rate & Rank format provides intermediate protection:

Protection Mechanism:
- Rating stage (normative) is vulnerable to inflation
- Ranking stage (ipsative) forces trade-offs
- Consistency index detects discrepancies between stages
- Dual scoring can weight ipsative data more heavily when faking is suspected

Research findings:
- Claims to increase validity and reduce faking compared to pure normative
- Consistency index helps identify suspect profiles
- Effectiveness depends on proprietary algorithm calibration

### Trait Granularity Comparison

Instruments differ in the number and specificity of measured traits:

| Feature | SHL OPQ32r | Hogan HPI | Saville Wave |
|---------|-----------|-----------|--------------|
| **Number of Scales** | 32 specific traits | 7 primary scales | 36 facets |
| **Hierarchical Structure** | Flat structure (can be grouped into Big Five) | 7 primaries, 41 subscales, 6 occupational scales | 4 clusters, 12 sections, 36 facets |
| **Trait Specificity** | High specificity (e.g., "Data Rational" vs. "Conceptual") | Broader constructs (e.g., "Adjustment" encompasses multiple facets) | High specificity similar to OPQ |
| **Big Five Mapping** | Can be mapped to Big Five | Explicit Big Five structure | Can be mapped to Big Five |
| **Occupational Focus** | Optimized for work context differentiation | Balanced between personality science and work application | Optimized for work context |

**SHL OPQ32r - 32 Traits:**

The 32-trait structure provides fine-grained differentiation:

Example traits within Conscientiousness domain:
- **Detail Conscious:** Focuses on detail and accuracy
- **Conscientious:** Follows rules and procedures
- **Achieving:** Sets high goals and works hard
- **Vigorous:** Maintains high energy and fast pace

This specificity allows precise job matching and targeted development.

**Hogan HPI - 7 Primary Scales:**

The seven scales represent broader personality dimensions:

1. **Adjustment:** Emotional stability and stress tolerance
2. **Ambition:** Leadership and competitive drive
3. **Sociability:** Extraversion and social confidence
4. **Interpersonal Sensitivity:** Warmth and tact
5. **Prudence:** Conscientiousness and impulse control
6. **Inquisitive:** Openness and intellectual curiosity
7. **Learning Approach:** Academic orientation and valuing education

The HPI provides 41 subscales (homogeneous item composites) for more granular interpretation, but primary reporting focuses on the 7 scales.

**Saville Wave - 36 Facets:**

Wave's structure balances specificity with conceptual organization:

Four Clusters:
1. **Thought:** How you think and create
2. **Influence:** How you interact with and influence others
3. **Adaptability:** How you respond to change and pressure
4. **Delivery:** How you deliver results and organize work

The 36 facets are organized into 12 sections within these clusters, providing hierarchical interpretation at multiple levels.

### Theoretical Basis Comparison

| Feature | SHL OPQ32r | Hogan HPI | Saville Wave |
|---------|-----------|-----------|--------------|
| **Theoretical Foundation** | Pragmatic workplace trait model | Socioanalytic Theory | Performance Culture Framework |
| **Core Concept** | Measuring workplace behavioral preferences | Measuring reputation (how others see you) | Measuring performance potential |
| **Big Five Relationship** | Can be mapped to Big Five post-hoc | Explicitly designed around Big Five structure | Extends beyond Big Five to include ability aspects |
| **Item Content** | Work-specific behaviors and preferences | General personality statements | Mix of personality, preference, and competence |
| **Validation Focus** | Job performance prediction | Career success and derailment risk | Competency potential and role fit |

**OPQ32r - Workplace Behaviors:**

The OPQ takes a criterion-focused approach:
- Items directly describe workplace scenarios
- Content validity is paramount (items look like work)
- Traits selected based on relevance to job performance
- Factor structure emerges from content rather than driving content

Example items (illustrative):
- "I analyze data thoroughly before making decisions"
- "I enjoy persuading others to see my point of view"
- "I prefer to follow established procedures"

**Hogan HPI - Socioanalytic Theory:**

Hogan's theoretical foundation emphasizes reputation management:
- Personality evolved for social living and status attainment
- Reputation (how others see us) predicts career success better than identity (how we see ourselves)
- The HPI measures reputation by asking about typical behavior
- Focus on getting along (Interpersonal Sensitivity, Prudence, Adjustment) and getting ahead (Ambition, Sociability)

Example items (illustrative):
- "People seek me out at social gatherings"
- "I rarely lose my temper"
- "I enjoy being in charge"

**Saville Wave - Performance Culture Framework:**

Wave integrates personality with broader performance factors:
- 36 facets include some constructs that blend personality with ability or values
- Framework explicitly links traits to performance domains
- Competency Potential Profile predicts job behavior
- Emphasis on both "preference" (what you like) and "performance" (what you can do)

Example facets:
- **Evaluating Information:** Critically reviewing information (cognitive + personality)
- **Convincing People:** Persuading and influencing (interpersonal skill + extraversion)
- **Embracing Change:** Adapting to new situations (openness + resilience)

## Validity Evidence Comparison

### Criterion Validity

All three instruments demonstrate solid criterion validity, though specific coefficients vary by study:

**General Findings:**
- Personality-only predictors yield operational validities ranging from **ρ = 0.16 to 0.28** for job performance
- Conscientiousness and related traits (Detail Conscious, Achieving, Prudence) show strongest validity (ρ ≈ 0.20-0.28)
- Emotional Stability/Adjustment shows consistent validity across jobs (ρ ≈ 0.18-0.24)
- Other traits show job-specific patterns (e.g., Extraversion predicts sales performance)

**OPQ32r Validity:**
- Meta-analytic evidence across 90+ validation studies in 20+ countries
- Personality predictors achieve ρ = 0.16 to 0.28 for competency ratings
- When combined with Verify cognitive tests, validity increases significantly:
  - Analyzing & Interpreting: ρ = 0.44 (combined P+A)
  - Interacting & Presenting: ρ = 0.40 (combined P+A)
  - Creating & Conceptualizing: ρ = 0.36 (combined P+A)

**Hogan HPI Validity:**
- Extensive validation research demonstrating similar validity levels
- HPI and OPQ found to have "similar levels of reliability and validity in predicting job performance"
- Three-instrument approach (HPI + HDS + MVPI) provides comprehensive personality coverage
- Strong evidence for predicting leadership effectiveness and career derailment

**Saville Wave Validity:**
- Claims to "increase validity and reduce faking" through hybrid format
- Validation studies support criterion validity
- Consistency index adds incremental validity by identifying careless or faking respondents
- Dual scoring aims to optimize prediction by leveraging both data sources

### Reliability

Internal consistency is robust across all instruments:

| Instrument | Typical Reliability | Measurement Approach |
|------------|-------------------|---------------------|
| **OPQ32r** | Marginal reliability typically exceeds 0.80 for most scales | Theta-information from IRT model |
| **Hogan HPI** | Internal consistency (α) ranges 0.70-0.85 | Cronbach's alpha |
| **Saville Wave** | Reliability for facets typically exceeds 0.75 | Alpha for normative, IRT-like for ipsative |

All three instruments meet professional standards for reliability (α ≥ 0.70), though specific scales may occasionally fall slightly below this threshold due to brevity.

## Practical Comparison

### Use Case Suitability

Different methodologies fit different assessment contexts:

**High-Stakes Selection (e.g., external hiring):**
- **Best fit:** OPQ32r or Saville Wave
- **Rationale:** Faking resistance critical; forced-choice format maintains validity
- **Trade-off:** Longer completion time, potentially more complex interpretation

**Internal Development (e.g., coaching, 360-degree feedback):**
- **Best fit:** Hogan HPI or normative scoring from Wave
- **Rationale:** Transparency aids self-awareness; faking less concerning
- **Trade-off:** Normative format easier to understand and discuss

**Volume Recruitment (e.g., call center, retail):**
- **Best fit:** OPQ32r for efficiency + validity, or shorter normative instruments
- **Rationale:** Adaptive timing, strong validity, automated competency reports
- **Trade-off:** Cost per assessment may be higher for sophisticated systems

**Executive Assessment (e.g., C-suite selection):**
- **Best fit:** All three acceptable; often combined with interviews and simulations
- **Rationale:** Comprehensive trait coverage, sophisticated interpretation
- **Trade-off:** Assessment is one component of multi-method evaluation

### Reporting and Interpretation

Report style and framework integration differ significantly:

**OPQ32r Reports:**
- **Universal Competency Report (UCR):** Translates 32 traits into 20 competency dimensions via algorithmic mapping
- **Framework Integration:** Explicitly links to SHL's Universal Competency Framework (UCF) with 403+ validated competency models
- **Customization:** Can map to custom competency frameworks
- **Style:** Balanced narrative + graphical display
- **Automation:** Highly automated through validated algorithms

**Hogan HPI Reports:**
- **Personality Report:** Describes seven scales with percentile scores
- **Leadership Report:** Integrates HPI, HDS, MVPI for leadership evaluation
- **Competency Mapping:** Often requires consultant services to map to client-specific frameworks
- **Style:** Narrative-heavy with interpretive richness
- **Automation:** More reliant on consultant interpretation for custom applications

**Saville Wave Reports:**
- **Competency Potential Profile:** Maps 36 facets to 12 performance areas via Performance Culture Framework
- **Framework Integration:** Uses Saville's proprietary Performance Culture Framework
- **Dual Scores:** Reports can show both normative and ipsative perspectives
- **Style:** Detailed graphical displays with extensive facet-level information
- **Automation:** Automated competency prediction similar to OPQ approach

### Candidate Experience

Assessment experience varies by format and length:

**OPQ32r:**
- **Duration:** 25-30 minutes for 104 blocks
- **Experience:** Some candidates find forced-choice challenging or frustrating ("I'm both of these!")
- **Transparency:** Less transparent (harder to "game")
- **Perceived Fairness:** Generally positive if purpose is explained
- **Accessibility:** Available in 30+ languages, mobile-optimized

**Hogan HPI:**
- **Duration:** 15-20 minutes for 206 items
- **Experience:** Straightforward and intuitive (True/False format)
- **Transparency:** High transparency (clear what's being measured)
- **Perceived Fairness:** Very positive due to simplicity
- **Accessibility:** Available in 40+ languages

**Saville Wave:**
- **Duration:** 35-40 minutes for two stages (Rate + Rank)
- **Experience:** Longer but format variety maintains engagement
- **Transparency:** Moderate (rating stage transparent, ranking stage less so)
- **Perceived Fairness:** Generally positive but can feel lengthy
- **Accessibility:** Available in multiple languages

### Implementation Considerations

**OPQ32r:**
- **Cost:** Premium pricing reflecting sophisticated methodology
- **Training:** Requires BPS Level A or equivalent certification
- **Technology:** Modern online platform with strong integration capabilities
- **Support:** Global network of SHL consultants for implementation
- **Norms:** Extensive normative database stratified by country, job level, industry

**Hogan HPI:**
- **Cost:** Competitive pricing; three-instrument approach (HPI+HDS+MVPI) increases total cost
- **Training:** Certification program required for interpretation
- **Technology:** Robust online platform
- **Support:** Hogan's consultant network plus internal certification
- **Norms:** Large international normative database

**Saville Wave:**
- **Cost:** Premium pricing reflecting proprietary methodology
- **Training:** Certification required for advanced interpretation
- **Technology:** Modern online platform
- **Support:** Saville Assessment's consultant network
- **Norms:** Normative database covering key markets

## The Thurstonian IRT Breakthrough

### Historical Context

The development of Thurstonian IRT scoring for the OPQ32r represented a watershed moment in personality assessment:

**The Ipsative Scoring Problem:**
Traditional forced-choice personality tests used ipsative scoring (rank-order or simple counting):
- Scores were inherently comparative within-person
- Between-person comparisons were statistically invalid
- Trait scores were negatively correlated by construction (if one goes up, others must go down)
- This limited utility for selection decisions

**The Normative Format Alternative:**
To enable between-person comparisons, most vendors used normative Likert scales:
- Candidates rate each item independently (e.g., 1-5 scale)
- Enables valid between-person comparisons
- But sacrifices faking resistance
- Trade-off between psychometric quality and practical validity

**The Innovation:**
Thurstonian IRT, adapted from Thurstone's law of comparative judgment (1927), solved this dilemma:
- Retains forced-choice format for faking resistance
- Recovers normative-equivalent scores through multidimensional IRT modeling
- Estimates all traits simultaneously from pattern of choices
- Produces scores suitable for between-person comparison

### Technical Achievement

The Thurstonian IRT model is mathematically sophisticated:

**Key Assumptions:**
1. Each trait has a latent continuous distribution in the population (normative structure exists)
2. When choosing between items, candidates compare their latent trait levels plus random error
3. Choice probabilities can be modeled using cumulative normal distribution functions
4. All traits can be estimated simultaneously from the complete pattern of choices

**Estimation Process:**
- Complex multidimensional IRT estimation (often using Markov Chain Monte Carlo methods)
- Computationally intensive but feasible with modern computing power
- Requires large calibration samples to estimate item parameters accurately
- Produces theta estimates for all 32 traits with associated standard errors

**Validation:**
Rigorous trials confirmed that:
- Recovered scores closely approximate normative scores that would be obtained from Likert scales
- Reliability (marginal reliability) typically exceeds 0.80
- Criterion validity is maintained or improved compared to normative format
- Faking resistance is preserved

### Competitive Significance

The Thurstonian IRT breakthrough provided SHL with significant competitive advantages:

**Methodological Leadership:**
- Cited as a "key methodological enhancement" and "significant innovation"
- Demonstrated scientific leadership in psychometric innovation
- Established SHL as methodologically sophisticated

**Practical Advantages:**
- Enables use of forced-choice format in high-stakes selection
- Maintains validity in applicant contexts where faking is a concern
- Differentiates OPQ32r from normative competitors

**Market Impact:**
- Competitors had to respond with their own innovations (e.g., Saville's Rate & Rank)
- Raised industry standards for personality assessment methodology
- Demonstrated that rigorous psychometrics could solve practical problems

**Ongoing Development:**
- Continues to be refined and optimized
- Extensions to other forced-choice formats
- Ongoing research into further improvements

## Strategic Comparison

### When to Choose OPQ32r

**Optimal contexts:**
- High-stakes external selection where faking is a concern
- Organizations with sophisticated HR analytics capabilities
- Global companies needing consistent frameworks across countries
- Situations requiring integration of personality + ability data
- Organizations using competency-based talent management
- Volume recruitment with automated competency reporting needs

**Key advantages:**
- Strongest faking resistance among major instruments
- Universal Competency Framework provides unified reporting architecture
- 32 traits offer fine-grained differentiation
- Strong validity evidence for P+A integration
- 403+ validated competency models available

**Considerations:**
- Higher cost and complexity
- Requires BPS Level A certification
- Forced-choice format may frustrate some candidates
- Longer completion time than HPI

### When to Choose Hogan HPI

**Optimal contexts:**
- Executive assessment and leadership development
- Organizations valuing narrative interpretation over quantitative precision
- Coaching and development applications where transparency is beneficial
- Situations requiring derailment risk assessment (HDS)
- Organizations with strong consultant relationships for custom mapping

**Key advantages:**
- Theoretical grounding in Socioanalytic Theory provides interpretive depth
- Narrative-heavy reports facilitate coaching conversations
- Three-instrument suite (HPI, HDS, MVPI) provides comprehensive coverage
- Shorter completion time
- Easier for candidates to understand

**Considerations:**
- More vulnerable to faking in high-stakes selection
- Broader trait structure (7 scales) provides less differentiation than 32 traits
- Competency mapping often requires consultant services
- May show score inflation in applicant samples

### When to Choose Saville Wave

**Optimal contexts:**
- Organizations wanting benefits of both forced-choice and normative formats
- Situations requiring maximum psychometric information capture
- Assessment centers and comprehensive evaluations
- Organizations valuing detailed facet-level reporting

**Key advantages:**
- Hybrid format aims to combine faking resistance with normative interpretability
- 36 facets provide comprehensive trait coverage
- Consistency index detects invalid responding
- Performance Culture Framework links personality to performance domains

**Considerations:**
- Longest completion time (35-40 minutes)
- Proprietary algorithm is less transparent than OPQ's published Thurstonian IRT
- Smaller vendor with less global reach than SHL or Hogan
- Dual scoring may be complex to interpret

## Conclusion

The personality assessment market offers scientifically robust options, each distinguished by methodological approach rather than quality differences. SHL's OPQ32r, Hogan's HPI, and Saville's Wave all demonstrate solid reliability and validity, but differ fundamentally in:

**Format:**
- Forced-choice (OPQ32r) vs. Normative (HPI) vs. Hybrid (Wave)
- This choice determines faking resistance, candidate experience, and scoring complexity

**Scoring:**
- Thurstonian IRT (OPQ32r) vs. Classical (HPI) vs. Proprietary Dual (Wave)
- This choice determines psychometric sophistication and score interpretability

**Theory:**
- Workplace behaviors (OPQ32r) vs. Socioanalytic reputation (HPI) vs. Performance culture (Wave)
- This choice determines item content and interpretive framework

**Granularity:**
- 32 traits (OPQ32r) vs. 7 scales (HPI) vs. 36 facets (Wave)
- This choice determines differentiation precision and reporting detail

The Thurstonian IRT breakthrough for OPQ32r represents a significant methodological achievement, solving the long-standing trade-off between faking resistance and normative scoring. This innovation demonstrates how sophisticated psychometrics can solve practical problems, providing competitive advantage while advancing the field.

Organizations selecting personality assessments should prioritize **methodological fit** over quality differences, as all major instruments meet professional standards. The decision hinges on:
- Assessment context (selection vs. development)
- Faking concerns (high-stakes vs. low-stakes)
- Framework requirements (UCF, custom competencies, leadership models)
- Implementation resources (technology, consultants, training)
- Organizational sophistication (analytics capabilities, psychometric expertise)

## Key Takeaways

- **Comparable Quality, Different Methodology:** Major personality assessments (OPQ32r, HPI, Wave) achieve similar validity (ρ = 0.16-0.28 for job performance) but differ fundamentally in format and scoring
- **Faking Resistance Trade-off:** Forced-choice formats (OPQ32r, Wave ranking) resist impression management but sacrifice transparency; normative formats (HPI, Wave rating) are more transparent but fakeable
- **Thurstonian IRT Breakthrough:** SHL's adoption of Thurstonian IRT solved the ipsative scoring problem, enabling recovery of normative scores from forced-choice responses—a watershed methodological achievement
- **Trait Granularity Variation:** OPQ32r's 32 traits and Wave's 36 facets provide finer differentiation than HPI's 7 scales, enabling more precise job matching and development planning
- **Theoretical Foundations Matter:** OPQ32r emphasizes workplace behaviors, HPI emphasizes reputation management (Socioanalytic Theory), and Wave emphasizes performance potential—shaping item content and interpretation
- **Framework Integration Distinguishes:** OPQ32r's Universal Competency Framework provides automated competency reporting with 403+ validated models; HPI often requires consultant mapping; Wave uses Performance Culture Framework
- **Context Determines Optimal Choice:** Selection contexts favor faking-resistant formats (OPQ32r), development contexts favor transparent formats (HPI), and comprehensive assessments may benefit from hybrid approaches (Wave)
- **Validity Comparable Across Vendors:** Independent reviews confirm that OPQ32r and HPI have "similar levels of reliability and validity in predicting job performance," demonstrating industry-wide quality convergence

---

## Chapter Navigation

[← Previous: Chapter 29 - Industry Quality Convergence](/psychometric-guide/chapters/29-industry-convergence/)

[Next: Chapter 31 - Cognitive Competition →](/psychometric-guide/chapters/31-cognitive-competition/)

[↑ Back to Home](/psychometric-guide/)

