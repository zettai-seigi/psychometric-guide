---
layout: default
title: "Chapter 17: MQ Construction and CTT Scoring"
parent: "Part IV: Motivation Questionnaire"
nav_order: 3
permalink: /chapters/17-mq-scoring/
---

# Chapter 17: MQ Construction and CTT Scoring

---

## Introduction: The MQ Measurement Approach

The Motivation Questionnaire (MQ) takes a fundamentally different measurement approach compared to SHL's personality and ability assessments. While the OPQ32r employs sophisticated Thurstonian IRT to overcome ipsative scoring limitations, and Verify leverages Computer Adaptive Testing (CAT) for maximal precision, the MQ retains a Classical Test Theory (CTT) foundation with straightforward Likert-type scaling.

This methodological choice is deliberate and purposeful. The MQ is primarily used for coaching and development rather than high-stakes selection, and measures self-reported preferences and values rather than maximal performance or behavioral tendencies. In this context, the simplicity, transparency, and interpretability of CTT scoring are not only sufficient but advantageous.

This chapter explores the MQ's construction methodology, scoring approach, reliability assessment, and standardization procedures, positioning these choices within the broader SHL assessment ecosystem and explaining why CTT remains the appropriate methodology for measuring workplace motivation.

---

## The Likert-Type Item Format

### Structure and Response Scale

The MQ uses a classic Likert-type self-report format where test-takers rate short statements about workplace scenarios or conditions. Each item is designed to tap into one of the 18 motivational dimensions, and respondents indicate how motivating or demotivating they find each described situation.

**The Standard 5-Point Scale**:
1. **Very Demotivating** - This factor would significantly decrease my motivation
2. **Demotivating** - This factor would somewhat decrease my motivation
3. **Neither Motivating nor Demotivating** - This factor has no impact on my motivation
4. **Motivating** - This factor would increase my motivation
5. **Very Motivating** - This factor would significantly increase my motivation

This bipolar scale captures both the strength and direction of motivational response, allowing the MQ to distinguish between factors that actively demotivate (scores of 1-2), factors that are neutral or unimportant (score of 3), and factors that motivate to varying degrees (scores of 4-5).

### Example Items (Illustrative)

While actual MQ items are proprietary, the format follows patterns like:

- **Achievement dimension**: "Having the opportunity to set and reach challenging goals"
- **Autonomy dimension**: "Working independently with minimal supervision"
- **Affiliation dimension**: "Being part of a close-knit, collaborative team"
- **Material Reward dimension**: "Receiving substantial bonuses tied to performance"
- **Status dimension**: "Working for a prestigious, well-respected organization"

Respondents rate each statement on the 5-point scale based on how much that factor would motivate or demotivate them at work.

### Advantages of the Likert Format for Motivation Measurement

The Likert-type format offers several advantages for measuring workplace motivation:

1. **Face Validity**: The direct, transparent nature of the questions is appropriate for a development tool; test-takers understand exactly what is being measured
2. **Normative Scoring**: Unlike forced-choice formats, Likert scales allow for direct between-person comparisons on each dimension
3. **Simplicity**: The rating task is intuitive and cognitively straightforward, minimizing measurement error from format confusion
4. **Granularity**: The 5-point scale provides sufficient differentiation without over-interpretation of small differences
5. **Speed**: The format allows for efficient administration, with approximately 150 items completed in about 25 minutes

### Potential Limitations

The Likert format does have acknowledged limitations:

- **Social Desirability**: Test-takers may present idealized motivational profiles, though this is less problematic for development than selection
- **Response Styles**: Some individuals may exhibit acquiescence bias (tendency to agree) or extreme response style (overuse of scale endpoints)
- **Self-Awareness Requirements**: Accurate responses require reasonable self-insight into one's motivational drivers

However, these limitations are acceptable given the MQ's primary use case (coaching and development) and the nature of motivation as a self-reported, subjective construct.

---

## Classical Test Theory (CTT) Scoring Methodology

### Foundations of CTT

Classical Test Theory, also known as True Score Theory, is the traditional psychometric framework that predates modern Item Response Theory. CTT is based on several core assumptions:

**The Basic CTT Equation**:
```
Observed Score = True Score + Error
X = T + E
```

This simple model posits that any test score has two components:
- **True Score (T)**: The individual's actual level on the construct being measured
- **Error (E)**: Random measurement error from various sources

**Key CTT Assumptions**:
1. Errors are random and uncorrelated with true scores
2. Errors are uncorrelated across individuals
3. The standard error of measurement (SEM) is constant across all score levels
4. Reliability is the ratio of true score variance to observed score variance

### Raw Score Calculation for MQ Dimensions

The MQ applies CTT scoring in a straightforward manner:

**Step 1: Item-to-Dimension Mapping**
Each of the approximately 150 MQ items is assigned to one of the 18 motivational dimensions. Typically, each dimension is measured by 6-10 items to ensure adequate reliability.

**Step 2: Raw Score Summation**
For each dimension, the raw score is calculated by summing (or averaging) the respondent's ratings across all items assigned to that dimension:

```
Raw Score (Dimension i) = Σ (Item Responses for Dimension i) / Number of Items

or simply:

Raw Score (Dimension i) = Σ (Item Responses for Dimension i)
```

**Example Calculation**:
If the Achievement dimension is measured by 8 items, and a respondent rates them as: 5, 5, 4, 5, 4, 5, 5, 4

- **Sum method**: Raw Score = 37
- **Average method**: Raw Score = 37/8 = 4.625

Both approaches yield dimension-level scores indicating the strength of motivation on that dimension.

**Step 3: Repeat for All 18 Dimensions**
This process is repeated for each of the 18 dimensions, producing a raw score profile with 18 values representing the individual's self-reported motivation across all measured factors.

### Why CTT for the MQ?

The decision to use CTT rather than IRT for the MQ reflects several strategic considerations:

**1. Measurement Purpose**
- The MQ emphasizes personalized insight and motivational profiling for coaching
- High-stakes selection cutoffs requiring maximal precision are not the primary application
- CTT's straightforward scoring is sufficient for the developmental context

**2. Nature of the Construct**
- Motivation is a self-reported preference rather than a maximal performance construct
- There is no "right answer" or objectively correct response
- Adaptive testing (which requires IRT) offers little benefit when measuring subjective preferences

**3. Interpretability and Transparency**
- CTT scoring is transparent and easily explained to test-takers and coaches
- The direct sum of item responses has intuitive meaning
- Developmental conversations benefit from straightforward score interpretation

**4. Comparative Simplicity**
- CTT requires less complex psychometric infrastructure than IRT
- Norm development and score conversion are more straightforward
- Updates and revisions are simpler to implement

**5. Historical Precedent**
- Motivation and values inventories traditionally use CTT
- The MQ's methodology aligns with established practices in the field (e.g., Hogan MVPI, OPQ32n normative version)

---

## Reliability Assessment via Cronbach's Alpha

### What is Cronbach's Alpha?

Cronbach's alpha (α) is the standard CTT metric for assessing internal consistency reliability—the extent to which items intended to measure the same construct actually correlate with one another. It represents the proportion of scale variance attributable to the true score (rather than error).

**The Cronbach's Alpha Formula**:

$$
\alpha = \frac{k}{k-1} \left(1 - \frac{\sum_{i=1}^{k} \sigma_{y_i}^2}{\sigma_x^2}\right)
$$

Where:
- k = number of items in the scale
- σ²(yi) = variance of item i
- σ²(x) = variance of the total scale score

**Interpretation**:
- α ranges from 0 to 1
- Higher values indicate greater internal consistency
- α = 0.70 is often considered the minimum acceptable threshold for research applications
- α = 0.80+ is considered good
- α = 0.90+ is considered excellent (though extremely high values may indicate redundancy)

### Cronbach's Alpha for MQ Scales

SHL's technical manuals report strong internal consistency for the MQ, with Cronbach's Alpha coefficients generally ranging between **0.75 and 0.85** for the 18 dimension scales. This range exceeds the standard psychometric threshold of α > 0.70 and indicates that the items within each dimension coherently measure the intended motivational construct.

**Example Reliability Values (Illustrative)**:

| Dimension | Cronbach's Alpha |
|---|---|
| Achievement | 0.82 |
| Competition | 0.79 |
| Power | 0.81 |
| Autonomy | 0.83 |
| Affiliation | 0.78 |
| Material Reward | 0.80 |
| Personal Growth | 0.84 |
| Interest | 0.81 |

These values confirm that:
1. Items are internally consistent within each dimension
2. Minimal cross-loading exists between dimensions
3. Each scale reliably measures its intended construct
4. The 18-factor structure is empirically sound

### How Cronbach's Alpha is Used in MQ Development

During the MQ's construction and validation, Cronbach's alpha played a critical quality control role:

**1. Item Selection and Refinement**
- Items with low item-total correlations (correlating weakly with the dimension total) were identified and revised or removed
- "Alpha if item deleted" analysis showed whether removing specific items would improve scale reliability
- Only items contributing positively to internal consistency were retained

**2. Factor Verification**
- Factor analysis confirmed that items clustered into the intended 18 dimensions
- Cronbach's alpha verified that items within each cluster cohered as a reliable scale
- Cross-loading items (loading on multiple factors) were eliminated or reassigned

**3. Minimizing Measurement Error**
- High alpha values indicate low measurement error (high reliability)
- This ensures that observed score differences between individuals reflect true motivational differences rather than random error
- Stable scores enable confident interpretation in coaching contexts

**4. Scale Length Optimization**
- Alpha increases with scale length (more items generally = higher reliability)
- The MQ balances reliability with efficiency by using 6-10 items per dimension
- This length achieves α > 0.75 without excessive test length

### Why Cronbach's Alpha Rather Than IRT Reliability?

For IRT-based assessments like the OPQ32r and Verify, reliability is not constant but varies as a function of ability level (calculated via the Test Information Function). However, CTT and Cronbach's alpha remain appropriate for the MQ because:

1. **CTT Scoring Framework**: The MQ uses simple summation rather than IRT theta estimation
2. **Development Context**: The MQ is primarily used for coaching, where constant SEM across the scale is acceptable
3. **Normative Self-Report**: Unlike ability tests where precision matters most at decision cutoffs, motivation profiles are interpreted holistically
4. **Simplicity**: Alpha provides a single, interpretable reliability coefficient for each scale

---

## Sten Score Conversion and Standardization

### The Need for Standardization

Raw scores on the MQ dimensions have little inherent meaning. A raw score of "37" on Achievement is uninterpretable without context: Is this high, low, or average? How does it compare to others in similar roles?

Standardization solves this problem by converting raw scores into norm-referenced standard scores that indicate relative standing compared to a defined comparison group.

### The Sten Scale

SHL uses the **sten scale** (Standard Ten) for reporting MQ scores. The sten scale is a 10-point standard score scale with specific properties:

**Sten Scale Properties**:
- **Range**: 1 to 10 (10 discrete bins)
- **Mean**: 5.5
- **Standard Deviation**: 2.0
- **Distribution**: Approximates a normal distribution when the underlying raw scores are normally distributed

**Sten Score Distribution** (approximate percentages for a normal distribution):

| Sten Score | Percentage of Population | Interpretation |
|---|---|---|
| 1 | 2.3% | Very Low |
| 2 | 4.4% | Low |
| 3 | 9.2% | Below Average |
| 4 | 15.0% | Slightly Below Average |
| 5 | 19.1% | Average |
| 6 | 19.1% | Average |
| 7 | 15.0% | Slightly Above Average |
| 8 | 9.2% | Above Average |
| 9 | 4.4% | High |
| 10 | 2.3% | Very High |

### The Standardization Process

**Step 1: Select Appropriate Norm Group**
Raw scores are standardized against a relevant comparison group (norm group). SHL maintains multiple norm groups segmented by:
- Geographic region (country/region-specific norms)
- Industry sector (e.g., finance, healthcare, technology)
- Job level (e.g., entry-level, professional, managerial, executive)
- Job family (e.g., sales, operations, technical)

**Step 2: Calculate Raw Score Statistics from Norm Group**
For each of the 18 dimensions, calculate the norm group's:
- Mean raw score (M)
- Standard deviation of raw scores (SD)

**Step 3: Convert Individual Raw Score to Z-Score**

$$
z = \frac{X - M}{SD}
$$

Where:
- X = individual's raw score
- M = norm group mean
- SD = norm group standard deviation

**Step 4: Convert Z-Score to Sten Score**

$$
\text{Sten} = (z \times 2) + 5.5
$$

Then round to the nearest integer (1-10).

**Step 5: Apply Bounds**
Cap the sten score at 1 (minimum) and 10 (maximum) to maintain the 10-point scale.

### Example Conversion

**Scenario**: A candidate scores 42 (raw score) on Achievement. The norm group (Professional-level, General Population) has:
- Mean (M) = 35
- Standard Deviation (SD) = 5

**Calculation**:
1. Z-score = (42 - 35) / 5 = 1.4
2. Sten = (1.4 × 2) + 5.5 = 2.8 + 5.5 = 8.3
3. Rounded Sten = **8**

**Interpretation**: This individual's Achievement motivation is **high** (sten 8), placing them in approximately the 80th-85th percentile of the comparison group.

### Interpretation Thresholds

SHL typically uses three broad interpretation bands:

- **Sten 1-3**: **Low** - Weak motivator or potential demotivator
- **Sten 4-7**: **Moderate** - Average motivational impact
- **Sten 8-10**: **High** - Strong motivator

These thresholds guide narrative interpretation in reports and structure coaching conversations around top motivators (high stens) and bottom motivators (low stens).

---

## Test Format and Administration

### Typical MQ Structure

The MQ (current version often labeled MQM5) has the following characteristics:

**Item Count**: Approximately **150 items**
- Each of the 18 dimensions is measured by 6-10 items
- Items are distributed across dimensions to balance reliability with test length

**Administration Time**: Approximately **25 minutes**
- The test is untimed, but most test-takers complete it within 20-30 minutes
- Faster completion than ability tests (no complex problem-solving required)
- Slower than forced-choice personality tests (rating all items on a scale takes more time than comparative choices)

**Format**: Online, self-administered questionnaire
- Presented via SHL's assessment platform
- Items typically presented one at a time or in blocks
- Progress indicators help test-takers track completion

**Instructions**: Test-takers are instructed to:
- Rate each statement based on how motivating or demotivating that factor would be for them at work
- Respond honestly rather than providing "ideal" answers
- Consider their genuine preferences rather than what they think employers want to hear

### Item Development and Content

The 150 items were developed through a rigorous process:

**1. Theoretical Framework**
- Items were written to reflect the 18 defined motivational dimensions
- Content aligned with established motivation theories (McClelland, Herzberg, Self-Determination Theory)
- Workplace relevance ensured through occupational psychology research

**2. Item Writing**
- Subject matter experts and psychometricians authored initial item pools
- Items written as short statements describing workplace scenarios or conditions
- Language kept clear, concrete, and accessible (avoiding jargon)
- Items balanced between positively and negatively worded statements

**3. Item Tryouts**
- Large pilot samples tested initial item pools
- Item statistics (means, standard deviations, item-total correlations) calculated
- Factor analysis confirmed items clustered into intended dimensions
- Poor-performing items (low discrimination, cross-loading) removed or revised

**4. Reliability and Validity Testing**
- Cronbach's alpha calculated for each dimension scale
- Test-retest reliability assessed to ensure score stability over time
- Convergent and divergent validity studies confirmed relationships with related constructs
- Criterion validity studies linked motivational profiles to engagement and performance outcomes

---

## MQ Reliability Standards

### Internal Consistency (Cronbach's Alpha)

As discussed previously, the MQ consistently achieves Cronbach's alpha values between **0.75 and 0.85** for its 18 dimension scales. This exceeds the standard psychometric threshold (α > 0.70) and indicates robust internal consistency.

**What This Means**:
- Items within each dimension measure a coherent construct
- Measurement error is minimized
- Scores are sufficiently reliable for coaching and development applications
- Between-person score differences reflect true motivational differences rather than measurement error

### Test-Retest Reliability

Test-retest reliability assesses score stability over time by administering the MQ to the same individuals on two occasions separated by a time interval (e.g., 2-4 weeks).

**Expected Values**: While specific published values vary, motivation assessments typically achieve test-retest correlations of **r = 0.75 - 0.85**, indicating that:
- Motivational profiles are relatively stable over short time periods
- The MQ measures enduring preferences rather than transient mood states
- Scores are consistent enough for longitudinal development tracking

**Important Consideration**: Some fluctuation in motivational scores over longer periods is expected and meaningful. Life circumstances, career stages, and changing priorities can legitimately alter motivational drivers. A perfect test-retest correlation would suggest the measure is insensitive to genuine change.

### Standard Error of Measurement (SEM)

Under CTT, the SEM represents the average amount of measurement error in scores:

$$
SEM = SD \times \sqrt{1 - \alpha}
$$

Where:
- SD = standard deviation of scores in the norm group
- α = Cronbach's alpha (reliability coefficient)

**Example Calculation**:
If a dimension has SD = 5 and α = 0.80:

SEM = 5 × √(1 - 0.80) = 5 × √0.20 = 5 × 0.447 = 2.24

**Interpretation**: An individual's observed sten score likely falls within ±1 sten of their true score approximately 68% of the time (assuming SEM ≈ 0.5 sten units when SD of stens = 2).

This level of precision is sufficient for coaching conversations, where the focus is on broad motivational patterns rather than precise cutoff scores.

---

## Why CTT Instead of IRT for the MQ?

### Understanding the Methodological Context

Within SHL's assessment ecosystem, the MQ is unique in retaining Classical Test Theory scoring while the OPQ32r and Verify have transitioned to Item Response Theory methodologies. This divergence is deliberate and reflects the different measurement goals of each assessment type.

### Comparison: MQ (CTT) vs. OPQ32r (Thurstonian IRT) vs. Verify (IRT/CAT)

| Assessment | Scoring Method | Key Reason for Methodology Choice |
|---|---|---|
| **MQ** | **Classical Test Theory (CTT)**, Likert summation | Measures self-reported preferences for development; simplicity and transparency are advantageous; IRT offers minimal benefit for subjective preference measurement |
| **OPQ32r** | **Thurstonian IRT** (MUPP model) | Solves ipsative scoring problems in forced-choice format; enables normative scale scores while retaining faking resistance; required for high-stakes personality selection |
| **Verify** | **Item Response Theory (IRT)** + **Computer Adaptive Testing (CAT)** | Maximizes precision and efficiency in measuring maximal cognitive performance; adaptive testing reduces items and enhances security; critical for high-stakes ability selection |

### Specific Reasons MQ Uses CTT

**1. Development vs. Selection Focus**
- **Primary Use**: The MQ is primarily used for coaching, development, and person-job matching rather than high-stakes selection cutoffs
- **Precision Requirements**: Development applications require understanding broad motivational patterns, not precise cutoff discrimination
- **CTT Advantage**: Straightforward summation provides adequate precision for developmental interpretation

**2. Self-Report Preferences vs. Maximal Performance**
- **Construct Type**: Motivation is a self-reported subjective preference, not a maximal performance construct with objective correct answers
- **No "Difficulty"**: IRT's concept of item difficulty doesn't apply meaningfully to preference statements
- **CTT Advantage**: Simple rating scales are the natural format for preference measurement

**3. Minimal Benefit from Adaptive Testing**
- **Fixed Item Set**: All 18 dimensions must be measured for a complete motivational profile
- **No Branching Logic**: Unlike ability tests where easier/harder items are selected based on performance, motivation items have no inherent difficulty ordering
- **CTT Advantage**: Fixed-form administration is simpler and equally effective

**4. Transparency and Interpretability**
- **Face Validity**: Development contexts benefit from transparent measurement; test-takers understand what is being assessed
- **Score Meaning**: Raw score sums have intuitive meaning (sum of ratings = overall motivation strength)
- **CTT Advantage**: Straightforward scoring facilitates coaching conversations and self-reflection

**5. Faking is Less Problematic**
- **Context**: The MQ is used for development rather than gatekeeping selection decisions
- **Motivation**: Test-takers have less incentive to fake when results inform their own development
- **Forced-Choice Unnecessary**: No need for the ipsative formats that necessitated Thurstonian IRT for OPQ32r
- **CTT Advantage**: Normative Likert scaling is appropriate when faking resistance is not paramount

**6. Psychometric Efficiency**
- **Infrastructure**: IRT requires extensive calibration samples, complex algorithms, and ongoing item parameter maintenance
- **Updates**: CTT-based tests are simpler to update and revise
- **Cost-Benefit**: The incremental benefit of IRT for motivation measurement does not justify the increased complexity
- **CTT Advantage**: Simpler methodology with adequate psychometric properties

### When Might IRT Be Considered for Motivation Assessment?

IRT could offer benefits for motivation assessment in specific scenarios:

- **Computerized Adaptive Administration**: If shortening test length were critical (though 25 minutes is already brief)
- **High-Stakes Selection**: If motivation scores were used for gatekeeping decisions requiring maximal precision
- **Item Banking**: If large, continuously refreshed item pools were needed for security
- **Differential Item Functioning (DIF) Analysis**: For sophisticated cross-cultural fairness analyses

However, none of these scenarios currently apply to the MQ's primary use case, making CTT the appropriate methodological choice.

---

## Norm Groups and Score Interpretation

### The Role of Norm Groups

Norm groups provide the essential context for interpreting MQ scores. A raw score gains meaning only when compared to a relevant reference population. The selection of an appropriate norm group is critical for fair and accurate interpretation.

### Available MQ Norm Groups

SHL maintains multiple norm groups for the MQ, segmented across several dimensions:

**1. Geographic Norms**
- Country or region-specific norms account for cultural differences in motivational patterns
- Examples: UK Professional, US General Population, European Managerial, Asia-Pacific Graduate

**2. Industry Sector Norms**
- Sector-specific norms recognize that different industries attract individuals with different motivational profiles
- Examples: Financial Services, Healthcare, Technology, Retail, Manufacturing

**3. Job Level Norms**
- Level-specific norms acknowledge that motivational drivers may vary by seniority
- Examples: Graduate/Entry-Level, Professional/Mid-Career, Managerial, Executive/Senior Leadership

**4. Job Family Norms**
- Function-specific norms recognize that different roles attract different motivational profiles
- Examples: Sales, Operations, Technical/IT, HR, Finance

**5. General Population Norms**
- Broad, representative samples provide baseline comparisons
- Useful when specific norms are unavailable or inappropriate

### Selecting the Appropriate Norm Group

**Best Practice Principles**:

1. **Relevance**: Choose the norm group most similar to the test-taker's situation or the intended role
2. **Representativeness**: Ensure the norm group is sufficiently large and representative
3. **Recency**: Prefer recently updated norms to reflect current motivational patterns
4. **Specificity**: More specific norms (e.g., "UK Financial Services Managers") are generally preferable to broader norms (e.g., "General Population")

**Example Scenario**:
A candidate applying for a mid-level technology project manager role in the US should ideally be compared against:
- **Primary Norm**: US Technology Professional or US Managerial norms
- **Secondary Reference**: General US Professional norms for broader context
- **Avoid**: Entry-level, sales-specific, or non-US norms

### Interpreting Norm-Referenced Sten Scores

Once standardized against an appropriate norm group, sten scores enable interpretation:

**Sten 8-10 (High Motivators)**:
- Factors scoring in this range are **strong motivators**
- These are the individual's primary drivers; their presence predicts engagement
- Absence of these factors in a role signals **disengagement risk**
- Coaching: Emphasize roles and assignments that satisfy these needs

**Sten 4-7 (Moderate Motivators)**:
- Factors scoring in this range have **average motivational impact**
- Neither strong drivers nor demotivators
- Presence or absence has modest effect on engagement
- Coaching: Secondary considerations in role fit and job design

**Sten 1-3 (Low Motivators/Demotivators)**:
- Factors scoring in this range are **weak motivators or potential demotivators**
- These factors do not energize the individual
- May be neutral (unimportant) or actively demotivating if required
- Coaching: Avoid roles where these factors are core requirements

### The Top 3 / Bottom 3 Interpretive Framework

Beyond normative comparisons, the MQ utilizes an **ipsative** (within-person) interpretive approach by identifying each individual's:

**Top 3 Motivators** (three highest sten scores):
- The individual's strongest drivers
- Critical for job fit and engagement prediction
- Should be actively present in roles and assignments
- Guide reward and recognition strategies

**Bottom 3 Motivators** (three lowest sten scores):
- The individual's weakest drivers or demotivators
- Important for identifying poor job fits
- Roles requiring these factors are at-risk placements
- Signal where flexibility or adaptation may be needed

This within-person framework complements normative interpretation by highlighting the relative importance of different motivators for each individual.

---

## Psychometric Quality and Validation

### Construct Validity

The MQ's construct validity—the extent to which it accurately measures the 18 intended motivational constructs—has been established through multiple lines of evidence:

**1. Factor Analytic Support**
- Exploratory Factor Analysis (EFA) confirmed that items cluster into 18 distinct factors
- Confirmatory Factor Analysis (CFA) verified that the 18-factor model fits the data better than alternative structures
- Minimal cross-loading indicates clean separation between dimensions

**2. Convergent Validity**
- MQ dimensions correlate appropriately with related constructs from other motivation/values inventories
- Example: MQ Achievement correlates with measures of achievement orientation; MQ Autonomy correlates with Self-Determination Theory autonomy measures

**3. Divergent Validity**
- MQ dimensions show weaker correlations with unrelated constructs
- Example: MQ Material Reward shows weaker correlation with cognitive ability than with other extrinsic motivators

**4. Theoretical Alignment**
- The 18 dimensions align with established motivation theories (McClelland, Herzberg, Self-Determination Theory)
- Factor structure reflects the theoretical organization into Energy & Dynamism, Synergy, Intrinsic, and Extrinsic domains

### Criterion Validity

Criterion validity evidence demonstrates that MQ scores predict relevant workplace outcomes:

**1. Job Satisfaction and Engagement**
- High scores on motivators present in the role predict higher job satisfaction
- Misalignment between motivational profile and job characteristics predicts disengagement

**2. Retention and Turnover**
- Motivational fit (match between profile and role) predicts retention
- The "Stay" vector in HiPo models uses MQ data to predict engagement and retention likelihood

**3. Performance Outcomes**
- When combined with ability and personality data, motivation adds incremental validity in predicting performance
- Motivation acts as a contextual modifier: ability and personality predict *what* one can do; motivation predicts *will* one do it

**4. Training and Development Outcomes**
- High Personal Growth motivation predicts training engagement and skill acquisition
- Motivational profiles predict career path preferences and developmental needs

### Fairness and Bias Analysis

SHL conducts ongoing fairness analyses to ensure the MQ does not exhibit systematic bias:

**1. Differential Item Functioning (DIF)**
- Statistical analyses test whether items function differently for different demographic groups
- Items showing substantial DIF (e.g., different meaning for different cultures) are flagged for revision

**2. Subgroup Differences**
- Mean score differences across gender, ethnicity, age, and cultural groups are monitored
- Differences in motivation (unlike ability or personality) may reflect genuine group differences in values and preferences
- Interpretation: Cultural or generational differences in motivational patterns are often meaningful rather than measurement bias

**3. Predictive Fairness**
- The MQ's predictive validity is examined across subgroups to ensure equal prediction accuracy
- Slope and intercept bias analyses ensure the MQ does not over- or under-predict outcomes for specific groups

---

## Evolution and Modernization: MQM5

### The Current Version

The current version of the MQ is often labeled **MQM5**, representing the fifth major iteration of the assessment. This version incorporates refinements based on decades of research and changing workplace contexts.

### Key Updates in MQM5

**1. Modernized Item Content**
- Statements updated to reflect contemporary work contexts
- Language modernized for clarity and relevance
- Scenarios revised to include digital/remote work considerations

**2. Work-Life Balance Emphasis**
- Motivational factors around work-life balance have become more salient in recent years
- Items explicitly assess preferences for boundary management and flexibility
- The Immersion dimension captures willingness to blur work-life boundaries

**3. Enhanced Norm Groups**
- Norm groups continuously updated to reflect current workforce demographics
- Generational shifts (e.g., Millennials and Gen Z entering workforce) necessitate norm updates
- Cultural and regional norms expanded for global use

**4. Refined Factor Structure**
- Ongoing factor analyses ensure the 18-dimension structure remains robust
- Item refinements maintain clean factor separation and high reliability
- Theoretical alignment with current motivation research maintained

**5. Digital Delivery Optimization**
- Platform enhancements improve user experience
- Mobile compatibility ensures accessibility
- Progress tracking and adaptive instructions enhance completion rates

### Future Directions

While the MQ retains its CTT foundation, potential future enhancements might include:

- **Machine Learning Integration**: Analyzing massive datasets to refine interpretation rules and identify complex motivational patterns
- **Dynamic Norms**: Real-time norm updates as data accumulates
- **Contextualized Items**: Tailoring item content to specific industries or roles
- **Longitudinal Tracking**: Enhanced platforms for tracking motivational profile changes over career stages

However, the core methodology—Likert-type items, CTT scoring, Cronbach's alpha reliability, and sten standardization—is likely to remain stable given its appropriateness for motivation measurement.

---

## Integration with OPQ and Verify

### The "Style, Power, Will" Framework

Within SHL's assessment ecosystem, the MQ complements the OPQ32 (personality) and Verify (ability) to provide a comprehensive talent assessment:

- **OPQ32 (Style)**: Measures *how* one behaves—behavioral preferences and tendencies
- **Verify (Power)**: Measures *what one can do*—cognitive capability and problem-solving ability
- **MQ (Will)**: Measures *what energizes*—motivational drivers and preferences

This three-part framework recognizes that predicting job performance and career success requires understanding not just capability (ability) and behavioral style (personality), but also motivational drivers (motivation).

### Integrated Reporting

SHL's Universal Competency Reports (UCR) integrate data from all three assessments:

**1. Competency Prediction**
- OPQ traits and Verify ability scores predict competency potential
- MQ scores act as a **contextual modifier**, flagging engagement risks

**2. The "Does Not Verify" (DNV) Logic**
- When personality suggests interest but ability is lacking (or vice versa), competency scores are penalized
- Similarly, when competency potential is high but motivation is misaligned, engagement risk is flagged

**3. High Potential (HiPo) Identification**
The three-vector HiPo model integrates all three assessments:
- **Ability** ("Can" vector): Derived from Verify G+ scores
- **Aspiration** ("Rise" vector): Derived from MQ (Progression, Power, Competition) and OPQ traits
- **Engagement** ("Stay" vector): Derived from MQ motivational fit with organizational rewards

**Example Integration**:
A candidate with:
- High Verify scores (strong cognitive ability)
- High OPQ scores on Leadership traits (behavioral style suited for leadership)
- Low MQ scores on Power and Progression (low leadership aspiration)

Might be flagged as: *High capability, but low leadership motivation—better suited for senior individual contributor roles than management.*

---

## Practical Implications for Test Users

### For HR Professionals and Recruiters

**1. Focus on Development**
- The MQ is best used for coaching, onboarding, and development rather than screening
- If used in selection, combine with ability and personality for holistic assessment

**2. Emphasize Job Fit**
- Use MQ profiles to match candidates to roles where their motivators are satisfied
- Identify "at risk" placements where motivators are misaligned with role characteristics

**3. Manage Expectations**
- The MQ provides self-reported preferences, not objective measures
- Faking is possible, so use in developmental rather than high-stakes contexts

### For Coaches and Development Professionals

**1. Structure Feedback Conversations**
- Use the Top 3 / Bottom 3 framework to guide discussions
- Explore how motivational profiles align with career goals and current roles

**2. Leverage for Career Planning**
- Help individuals understand which roles and environments will energize them
- Identify potential sources of disengagement proactively

**3. Monitor for Change**
- Motivational profiles can shift with life stages, career transitions, and changing priorities
- Re-administer periodically to track evolution

### For Test-Takers

**1. Respond Honestly**
- The MQ is most useful when responses reflect genuine preferences
- Development benefits depend on accurate self-reporting

**2. Interpret in Context**
- Scores are relative to a comparison group; a "low" score means low relative to the norm, not an absolute deficit
- All motivational profiles are valid; there are no "bad" profiles

**3. Use for Self-Awareness**
- Understanding your motivators helps you make informed career choices
- Seek roles and organizations that align with your top motivators

---

## Key Takeaways

1. **The MQ uses a Likert-type format** with a 5-point scale (Very Demotivating to Very Motivating) to measure self-reported motivational preferences

2. **Classical Test Theory (CTT) scoring** calculates raw scores by summing or averaging item responses for each of the 18 dimensions

3. **Cronbach's alpha** assesses internal consistency reliability, with MQ scales achieving values between **0.75 and 0.85**, exceeding the 0.70 threshold

4. **Sten score conversion** standardizes raw scores (mean 5.5, SD 2.0) against norm groups to enable interpretable comparisons

5. **The typical MQ format** includes approximately 150 items and takes about 25 minutes to complete

6. **CTT is appropriate for the MQ** because it measures self-reported preferences for development contexts, where simplicity and transparency are advantageous

7. **IRT methodologies (used by OPQ32r and Verify)** offer minimal benefit for motivation measurement, making CTT the efficient choice

8. **Norm group selection** is critical for accurate interpretation; more specific norms (job level, industry, region) are preferable

9. **Reliability and validity evidence** supports the MQ's psychometric quality across internal consistency, test-retest stability, construct validity, and criterion validity

10. **The MQ integrates with OPQ and Verify** in the "Style, Power, Will" framework, acting as a contextual modifier in competency prediction and HiPo identification

---

## Chapter Navigation

[← Previous: Chapter 16 - The 18 Motivation Dimensions](/psychometric-guide/chapters/16-18-dimensions/)

[Next: Chapter 18 - MQ in Practice →](/psychometric-guide/chapters/18-mq-applications/)

[↑ Back to Home](/psychometric-guide/)
