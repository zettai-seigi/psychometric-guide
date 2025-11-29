---
layout: default
title: "Chapter 26: Normative Data Strategies"
parent: "Part VI: Scoring Methodologies"
nav_order: 3
---

# Normative Data Strategies

### Learning Objectives

By the end of this chapter, you will be able to:

1. Explain why raw scores and theta estimates require normative context for interpretation
2. Understand sten scores and their psychometric properties (mean = 5.5, SD = 2.0)
3. Describe SHL's normative database scope (countries, languages, job levels, industries)
4. Articulate the rationale for stratified norm groups (job level, industry, function)
5. Evaluate the trade-offs between general norms and specific comparison groups
6. Apply normative data strategically in selection and development contexts

### The Necessity of Normative Comparison

Psychometric scores—whether raw scores (number correct), theta estimates (IRT ability), or sten scores (standardized traits)—are inherently **relative**. A numerical reasoning score of θ = 1.2 or a sten of 7 on Persuasiveness conveys no information in isolation. These metrics gain meaning only through comparison to a reference group (norm group).

**The Fundamental Questions**:
- "1.2 compared to whom?"
- "7 out of 10—but relative to what population?"

Without normative context:
- Organizations cannot set defensible cut-scores.
- Candidates cannot understand their relative standing.
- Feedback lacks actionable guidance (e.g., "Your score is above average for peers in your role").

Normative data strategies transform abstract psychometric measurements into interpretable, actionable information.

### Sten Scores: SHL's Standardization Approach

SHL reports most scores using the **sten (Standard Ten) scale**, a normalized standard score system.

#### Sten Scale Properties

**Range**: 1 to 10 (discrete integers)

**Mean**: 5.5

**Standard Deviation**: 2.0

**Distribution**: Stens are designed to approximate a normal distribution when the underlying trait is normally distributed in the population.

**Interpretation**:
- **Sten 1**: Very Low (< 2.5th percentile)
- **Stens 2-3**: Low (2.5th to 16th percentile)
- **Stens 4-5**: Below Average (16th to 45th percentile)
- **Stens 6-7**: Above Average (55th to 84th percentile)
- **Stens 8-9**: High (84th to 97.5th percentile)
- **Sten 10**: Very High (> 97.5th percentile)

#### Why Stens Instead of Percentiles or T-Scores?

SHL deliberately chose stens over more granular metrics (percentiles, T-scores) for several reasons:

1. **Preventing Over-Interpretation**: Psychometric measurement has inherent error. The difference between the 62nd and 65th percentile is statistically trivial, well within the confidence interval. Reporting percentiles encourages users to over-interpret small, meaningless differences.

   Stens, with their broader bands, communicate appropriate precision. A candidate with sten 6 and another with sten 7 are "both above average," discouraging inappropriate fine distinctions.

2. **Ease of Communication**: A 10-point scale is intuitive for non-psychometricians. Hiring managers and candidates can quickly grasp "7 out of 10 on Leadership" without needing statistical training.

3. **Consistency Across Assessments**: All SHL instruments (OPQ32, Verify, MQ) report stens, creating a unified interpretive framework. A sten 8 on Numerical Reasoning has the same relative meaning as a sten 8 on Persuasiveness.

4. **Reducing Adverse Impact Concerns**: Fine-grained metrics (e.g., percentiles) can exacerbate concerns about small score differences driving selection decisions. Stens' broader bands make decision-making more defensible.

#### Converting Theta to Stens

The conversion from IRT theta estimates to stens is straightforward:

1. **Calculate the z-score** (standardized score relative to the norm group):
   z = (θ - μ_norm) / σ_norm

   Where μ_norm and σ_norm are the mean and SD of theta in the chosen norm group.

2. **Convert z-score to sten**:
   sten = 5.5 + (2 × z)

   (Rounded to the nearest integer, constrained to 1-10)

**Example**:
- Candidate theta = 1.2
- Norm group mean (μ) = 0.5, SD (σ) = 0.8
- z = (1.2 - 0.5) / 0.8 = 0.875
- sten = 5.5 + (2 × 0.875) = 5.5 + 1.75 = 7.25 → **Sten 7**

**Interpretation**: This candidate is above average (sten 7) relative to the chosen norm group.

### SHL's Normative Database: Scope and Scale

SHL maintains one of the largest normative databases in the assessment industry, accumulated over decades of global administration.

#### OPQ32 Norms

**Scope**:
- **92 comparison groups** (stratified by job level, industry, function, and geography)
- **37 countries**
- **24 languages**
- Millions of candidate records

**Stratification Dimensions**:

1. **Job Level**:
   - Operatives / Support Staff
   - Graduates / Entry-Level Professionals
   - Professional / Specialist
   - First-Line Managers / Supervisors
   - Middle Managers
   - Senior Managers / Directors
   - Executives / C-Suite

2. **Industry Sector**:
   - Banking / Financial Services
   - Engineering / Manufacturing
   - IT / Technology
   - Retail / Consumer Goods
   - Public Sector / Government
   - Healthcare
   - Professional Services (Consulting, Legal, Accounting)
   - Energy / Utilities

3. **Function**:
   - Sales / Business Development
   - Customer Service / Support
   - Operations / Logistics
   - Finance / Accounting
   - HR / Training
   - R&D / Engineering
   - Marketing / Communications

4. **Geography**:
   - Regional norms (e.g., North America, EMEA, Asia-Pacific)
   - Country-specific norms (e.g., UK Managers, US Executives, Singapore Graduates)

**Continuous Updating**: Norm groups are continuously updated as new data are collected, ensuring relevance and representativeness.

#### Verify Norms

**Scope**:
- **70+ comparison groups** (primarily by job level and industry)
- Global and regional stratifications
- Separate norms for supervised (VVT) and unsupervised (VAT) contexts

**Stratification Dimensions**:

1. **Job Level** (most critical for ability tests):
   - Operatives / Manual Workers
   - Clerical / Administrative
   - Graduates / Trainees
   - Professional / Technical
   - Managers
   - Senior Executives

2. **Industry Sector**:
   - Banking / Finance
   - Engineering / Science
   - IT / Technology
   - Public Sector

3. **Test Context**:
   - Unsupervised (VAT): Norms for candidates who took the test online without proctoring.
   - Supervised (VVT): Norms for candidates who took the verification test in controlled settings.

**Rationale for Job-Level Stratification**: Cognitive ability distributions vary substantially by job level due to self-selection and organizational selection over time. Executives as a group have significantly higher mean ability than operatives. Using a "general population" norm would make nearly all executives score in the 90th+ percentile (creating ceiling effects) and nearly all operatives score in the 10th- percentile (creating floor effects). Job-level norms provide meaningful differentiation within the relevant comparison group.

#### MQ Norms

**Scope**:
- Similar stratification to OPQ32 (job level, industry, function)
- Emphasis on **developmental norms** rather than selection cutoffs

**Usage**: MQ norms help candidates and coaches understand motivational drivers relative to peers, facilitating career conversations and engagement strategies.

### Choosing the Right Norm Group: Strategic Considerations

Selecting an appropriate norm group is a critical decision that influences score interpretation, cut-scores, and selection outcomes.

#### General vs. Specific Norms

**General Norms** (e.g., "All Professionals," "All Managers"):

**Advantages**:
- Larger sample sizes, providing statistical stability
- Simplicity (one norm group for all roles)
- Consistency across hiring contexts

**Disadvantages**:
- May obscure meaningful differences between roles, industries, or levels
- Ceiling/floor effects for specialized roles
- Less relevant comparisons (e.g., comparing a sales director to all managers, including operations and finance managers)

**Specific Norms** (e.g., "Senior Managers in Financial Services," "IT Graduates"):

**Advantages**:
- More relevant peer comparisons
- Better differentiation within specialized populations
- Reduced adverse impact (by comparing within homogeneous groups)

**Disadvantages**:
- Smaller sample sizes, potentially less stable
- Complexity (multiple norm tables required)
- Requires accurate job classification

#### SHL's Recommendations

**For High-Stakes Selection**:
- Use the **most specific norm group** that matches the target role in terms of level, function, and industry.
- Example: Hiring for a Managerial role in Banking? Use "Managers in Banking/Financial Services."

**For Developmental Feedback**:
- General norms or level-specific norms are often sufficient.
- Example: Providing feedback to a graduate trainee? Use "Graduate / Entry-Level Professionals."

**For Executive Assessment**:
- Always use Executive-specific norms to avoid ceiling effects and ensure differentiation among high-ability candidates.

**For Cross-Role Comparison** (e.g., succession planning, internal mobility):
- Use consistent norms (e.g., "All Managers") to enable direct comparability across functions.

#### Case Example: Numerical Reasoning for Different Roles

**Scenario**: An organization is hiring for two roles: (1) Graduate Analyst (Finance) and (2) Executive Director (Strategy).

**Candidate A** (Graduate Analyst applicant):
- Verify Numerical Reasoning θ = 0.8
- Compared to "All Graduates": Sten 8 (High, 90th percentile)
- Compared to "Graduates in Finance": Sten 7 (Above Average, 75th percentile)
- Compared to "All Professionals": Sten 6 (Above Average, 65th percentile)

**Candidate B** (Executive Director applicant):
- Verify Numerical Reasoning θ = 1.5
- Compared to "All Graduates": Sten 10 (Very High, 99th percentile)
- Compared to "All Executives": Sten 7 (Above Average, 80th percentile)
- Compared to "Executives in Strategy/Consulting": Sten 6 (Above Average, 70th percentile)

**Interpretation**:
- **For Candidate A**: Using "Graduates in Finance" norms is most appropriate, showing they are above average but not exceptional among finance peers. Using "All Graduates" inflates their standing; using "All Professionals" dilutes it.

- **For Candidate B**: Using "Executives in Strategy/Consulting" is critical. Without this specific norm, Candidate B appears extraordinary (sten 10 vs. Graduates), obscuring that they are merely above average among executive strategy peers. Executive roles demand differentiation at the top of the ability distribution.

### Normative Data and Adverse Impact

Norm group selection can significantly influence adverse impact (differential selection rates across demographic groups).

**Within-Group Norming** (comparing candidates only to their own demographic group) was **banned in the U.S. by the Civil Rights Act of 1991**. Organizations cannot legally use separate norm tables for different racial or gender groups.

However, **job-relevant norming** (comparing candidates to others in the same job level or function) is legal and often reduces adverse impact indirectly:

**Mechanism**:
- If a job level (e.g., Executives) has higher representation of certain demographic groups due to historical factors, using job-level norms ensures candidates are compared to relevant peers rather than the general population.
- This can reduce the magnitude of score differences between demographic groups at the selection stage.

**Caution**: Norm group selection must always be based on **job-relevant criteria** (level, function, industry), never on protected characteristics.

### The Evolution and Maintenance of Norm Groups

Normative data are not static. SHL continuously updates norm groups as new data are collected, ensuring relevance.

**Key Processes**:

1. **Data Collection**: Every administration of an SHL assessment contributes to the normative database (with candidate consent and data anonymization).

2. **Sample Size Monitoring**: Norm groups with small samples (n < 100) are flagged for limited interpretability. SHL aims for n > 200 for stable norm groups.

3. **Demographic Representativeness**: SHL monitors demographic composition (age, gender, ethnicity where permitted) to ensure norms reflect actual applicant populations.

4. **Recalibration**: Norms are periodically recalibrated to account for:
   - **Flynn Effect** (gradual increase in cognitive ability over generations)
   - **Cohort Shifts** (changing educational and workplace demographics)
   - **Test Security** (if item exposure compromises score validity, norms may shift)

5. **Regional and Cultural Validation**: Norms developed in one country are validated before use in another. Cultural differences in personality trait distributions (e.g., Assertiveness) require local norm development.

### Reporting and Transparency

SHL reports include explicit information about the norm group used, ensuring transparency:

**Typical Report Language**:
- "Numerical Reasoning: Sten 7 (Above Average compared to Managerial Professionals in Financial Services, n = 1,245)"
- "Persuasive: Sten 8 (High compared to UK Sales Professionals, n = 892)"

**Confidence Intervals**: Some reports include confidence intervals around sten scores, reflecting individual-level SEM:
- "Persuasive: Sten 8 (95% CI: Sten 7-9)"

This transparency allows users to evaluate the relevance and stability of the normative comparison.

### Key Takeaways

1. **Normative data are essential** for interpreting psychometric scores, transforming abstract metrics (theta, raw scores) into meaningful relative standings (stens, percentiles).

2. **Sten scores** (mean = 5.5, SD = 2.0, range 1-10) are SHL's standard metric, chosen to prevent over-interpretation of trivial differences and facilitate intuitive understanding.

3. **SHL maintains 92 OPQ norm groups and 70+ Verify norm groups**, stratified by job level, industry, function, and geography across 37 countries and 24 languages.

4. **Job-level stratification is critical** for cognitive ability tests, as ability distributions vary substantially across organizational levels due to selection and self-selection.

5. **Norm group selection is strategic**: Specific norms (e.g., "Executives in Consulting") provide relevant peer comparisons for selection; general norms (e.g., "All Managers") facilitate cross-role comparisons for development.

6. **Job-relevant norming** is legal and can reduce adverse impact by ensuring candidates are compared to appropriate peer groups, while within-group norming based on protected characteristics is prohibited.

7. **Norms are continuously updated** through data collection, sample size monitoring, recalibration, and cultural validation, ensuring ongoing relevance and representativeness.

8. **Transparency in reporting** (explicitly stating the norm group and sample size) enables users to evaluate the appropriateness and stability of normative comparisons.

---

## Chapter 26: Normative Data Strategies

### Learning Objectives

By the end of this chapter, you will be able to:

1. Explain why raw scores and theta estimates require normative context for interpretation
2. Understand sten scores and their psychometric properties (mean = 5.5, SD = 2.0)
3. Describe SHL's normative database scope (countries, languages, job levels, industries)
4. Articulate the rationale for stratified norm groups (job level, industry, function)
5. Evaluate the trade-offs between general norms and specific comparison groups
6. Apply normative data strategically in selection and development contexts

### The Necessity of Normative Comparison

Psychometric scores—whether raw scores (number correct), theta estimates (IRT ability), or sten scores (standardized traits)—are inherently **relative**. A numerical reasoning score of θ = 1.2 or a sten of 7 on Persuasiveness conveys no information in isolation. These metrics gain meaning only through comparison to a reference group (norm group).

**The Fundamental Questions**:
- "1.2 compared to whom?"
- "7 out of 10—but relative to what population?"

Without normative context:
- Organizations cannot set defensible cut-scores.
- Candidates cannot understand their relative standing.
- Feedback lacks actionable guidance (e.g., "Your score is above average for peers in your role").

Normative data strategies transform abstract psychometric measurements into interpretable, actionable information.

### Sten Scores: SHL's Standardization Approach

SHL reports most scores using the **sten (Standard Ten) scale**, a normalized standard score system.

#### Sten Scale Properties

**Range**: 1 to 10 (discrete integers)

**Mean**: 5.5

**Standard Deviation**: 2.0

**Distribution**: Stens are designed to approximate a normal distribution when the underlying trait is normally distributed in the population.

**Interpretation**:
- **Sten 1**: Very Low (< 2.5th percentile)
- **Stens 2-3**: Low (2.5th to 16th percentile)
- **Stens 4-5**: Below Average (16th to 45th percentile)
- **Stens 6-7**: Above Average (55th to 84th percentile)
- **Stens 8-9**: High (84th to 97.5th percentile)
- **Sten 10**: Very High (> 97.5th percentile)

#### Why Stens Instead of Percentiles or T-Scores?

SHL deliberately chose stens over more granular metrics (percentiles, T-scores) for several reasons:

1. **Preventing Over-Interpretation**: Psychometric measurement has inherent error. The difference between the 62nd and 65th percentile is statistically trivial, well within the confidence interval. Reporting percentiles encourages users to over-interpret small, meaningless differences.

   Stens, with their broader bands, communicate appropriate precision. A candidate with sten 6 and another with sten 7 are "both above average," discouraging inappropriate fine distinctions.

2. **Ease of Communication**: A 10-point scale is intuitive for non-psychometricians. Hiring managers and candidates can quickly grasp "7 out of 10 on Leadership" without needing statistical training.

3. **Consistency Across Assessments**: All SHL instruments (OPQ32, Verify, MQ) report stens, creating a unified interpretive framework. A sten 8 on Numerical Reasoning has the same relative meaning as a sten 8 on Persuasiveness.

4. **Reducing Adverse Impact Concerns**: Fine-grained metrics (e.g., percentiles) can exacerbate concerns about small score differences driving selection decisions. Stens' broader bands make decision-making more defensible.

#### Converting Theta to Stens

The conversion from IRT theta estimates to stens is straightforward:

1. **Calculate the z-score** (standardized score relative to the norm group):
   z = (θ - μ_norm) / σ_norm

   Where μ_norm and σ_norm are the mean and SD of theta in the chosen norm group.

2. **Convert z-score to sten**:
   sten = 5.5 + (2 × z)

   (Rounded to the nearest integer, constrained to 1-10)

**Example**:
- Candidate theta = 1.2
- Norm group mean (μ) = 0.5, SD (σ) = 0.8
- z = (1.2 - 0.5) / 0.8 = 0.875
- sten = 5.5 + (2 × 0.875) = 5.5 + 1.75 = 7.25 → **Sten 7**

**Interpretation**: This candidate is above average (sten 7) relative to the chosen norm group.

### SHL's Normative Database: Scope and Scale

SHL maintains one of the largest normative databases in the assessment industry, accumulated over decades of global administration.

#### OPQ32 Norms

**Scope**:
- **92 comparison groups** (stratified by job level, industry, function, and geography)
- **37 countries**
- **24 languages**
- Millions of candidate records

**Stratification Dimensions**:

1. **Job Level**:
   - Operatives / Support Staff
   - Graduates / Entry-Level Professionals
   - Professional / Specialist
   - First-Line Managers / Supervisors
   - Middle Managers
   - Senior Managers / Directors
   - Executives / C-Suite

2. **Industry Sector**:
   - Banking / Financial Services
   - Engineering / Manufacturing
   - IT / Technology
   - Retail / Consumer Goods
   - Public Sector / Government
   - Healthcare
   - Professional Services (Consulting, Legal, Accounting)
   - Energy / Utilities

3. **Function**:
   - Sales / Business Development
   - Customer Service / Support
   - Operations / Logistics
   - Finance / Accounting
   - HR / Training
   - R&D / Engineering
   - Marketing / Communications

4. **Geography**:
   - Regional norms (e.g., North America, EMEA, Asia-Pacific)
   - Country-specific norms (e.g., UK Managers, US Executives, Singapore Graduates)

**Continuous Updating**: Norm groups are continuously updated as new data are collected, ensuring relevance and representativeness.

#### Verify Norms

**Scope**:
- **70+ comparison groups** (primarily by job level and industry)
- Global and regional stratifications
- Separate norms for supervised (VVT) and unsupervised (VAT) contexts

**Stratification Dimensions**:

1. **Job Level** (most critical for ability tests):
   - Operatives / Manual Workers
   - Clerical / Administrative
   - Graduates / Trainees
   - Professional / Technical
   - Managers
   - Senior Executives

2. **Industry Sector**:
   - Banking / Finance
   - Engineering / Science
   - IT / Technology
   - Public Sector

3. **Test Context**:
   - Unsupervised (VAT): Norms for candidates who took the test online without proctoring.
   - Supervised (VVT): Norms for candidates who took the verification test in controlled settings.

**Rationale for Job-Level Stratification**: Cognitive ability distributions vary substantially by job level due to self-selection and organizational selection over time. Executives as a group have significantly higher mean ability than operatives. Using a "general population" norm would make nearly all executives score in the 90th+ percentile (creating ceiling effects) and nearly all operatives score in the 10th- percentile (creating floor effects). Job-level norms provide meaningful differentiation within the relevant comparison group.

#### MQ Norms

**Scope**:
- Similar stratification to OPQ32 (job level, industry, function)
- Emphasis on **developmental norms** rather than selection cutoffs

**Usage**: MQ norms help candidates and coaches understand motivational drivers relative to peers, facilitating career conversations and engagement strategies.

### Choosing the Right Norm Group: Strategic Considerations

Selecting an appropriate norm group is a critical decision that influences score interpretation, cut-scores, and selection outcomes.

#### General vs. Specific Norms

**General Norms** (e.g., "All Professionals," "All Managers"):

**Advantages**:
- Larger sample sizes, providing statistical stability
- Simplicity (one norm group for all roles)
- Consistency across hiring contexts

**Disadvantages**:
- May obscure meaningful differences between roles, industries, or levels
- Ceiling/floor effects for specialized roles
- Less relevant comparisons (e.g., comparing a sales director to all managers, including operations and finance managers)

**Specific Norms** (e.g., "Senior Managers in Financial Services," "IT Graduates"):

**Advantages**:
- More relevant peer comparisons
- Better differentiation within specialized populations
- Reduced adverse impact (by comparing within homogeneous groups)

**Disadvantages**:
- Smaller sample sizes, potentially less stable
- Complexity (multiple norm tables required)
- Requires accurate job classification

#### SHL's Recommendations

**For High-Stakes Selection**:
- Use the **most specific norm group** that matches the target role in terms of level, function, and industry.
- Example: Hiring for a Managerial role in Banking? Use "Managers in Banking/Financial Services."

**For Developmental Feedback**:
- General norms or level-specific norms are often sufficient.
- Example: Providing feedback to a graduate trainee? Use "Graduate / Entry-Level Professionals."

**For Executive Assessment**:
- Always use Executive-specific norms to avoid ceiling effects and ensure differentiation among high-ability candidates.

**For Cross-Role Comparison** (e.g., succession planning, internal mobility):
- Use consistent norms (e.g., "All Managers") to enable direct comparability across functions.

#### Case Example: Numerical Reasoning for Different Roles

**Scenario**: An organization is hiring for two roles: (1) Graduate Analyst (Finance) and (2) Executive Director (Strategy).

**Candidate A** (Graduate Analyst applicant):
- Verify Numerical Reasoning θ = 0.8
- Compared to "All Graduates": Sten 8 (High, 90th percentile)
- Compared to "Graduates in Finance": Sten 7 (Above Average, 75th percentile)
- Compared to "All Professionals": Sten 6 (Above Average, 65th percentile)

**Candidate B** (Executive Director applicant):
- Verify Numerical Reasoning θ = 1.5
- Compared to "All Graduates": Sten 10 (Very High, 99th percentile)
- Compared to "All Executives": Sten 7 (Above Average, 80th percentile)
- Compared to "Executives in Strategy/Consulting": Sten 6 (Above Average, 70th percentile)

**Interpretation**:
- **For Candidate A**: Using "Graduates in Finance" norms is most appropriate, showing they are above average but not exceptional among finance peers. Using "All Graduates" inflates their standing; using "All Professionals" dilutes it.

- **For Candidate B**: Using "Executives in Strategy/Consulting" is critical. Without this specific norm, Candidate B appears extraordinary (sten 10 vs. Graduates), obscuring that they are merely above average among executive strategy peers. Executive roles demand differentiation at the top of the ability distribution.

### Normative Data and Adverse Impact

Norm group selection can significantly influence adverse impact (differential selection rates across demographic groups).

**Within-Group Norming** (comparing candidates only to their own demographic group) was **banned in the U.S. by the Civil Rights Act of 1991**. Organizations cannot legally use separate norm tables for different racial or gender groups.

However, **job-relevant norming** (comparing candidates to others in the same job level or function) is legal and often reduces adverse impact indirectly:

**Mechanism**:
- If a job level (e.g., Executives) has higher representation of certain demographic groups due to historical factors, using job-level norms ensures candidates are compared to relevant peers rather than the general population.
- This can reduce the magnitude of score differences between demographic groups at the selection stage.

**Caution**: Norm group selection must always be based on **job-relevant criteria** (level, function, industry), never on protected characteristics.

### The Evolution and Maintenance of Norm Groups

Normative data are not static. SHL continuously updates norm groups as new data are collected, ensuring relevance.

**Key Processes**:

1. **Data Collection**: Every administration of an SHL assessment contributes to the normative database (with candidate consent and data anonymization).

2. **Sample Size Monitoring**: Norm groups with small samples (n < 100) are flagged for limited interpretability. SHL aims for n > 200 for stable norm groups.

3. **Demographic Representativeness**: SHL monitors demographic composition (age, gender, ethnicity where permitted) to ensure norms reflect actual applicant populations.

4. **Recalibration**: Norms are periodically recalibrated to account for:
   - **Flynn Effect** (gradual increase in cognitive ability over generations)
   - **Cohort Shifts** (changing educational and workplace demographics)
   - **Test Security** (if item exposure compromises score validity, norms may shift)

5. **Regional and Cultural Validation**: Norms developed in one country are validated before use in another. Cultural differences in personality trait distributions (e.g., Assertiveness) require local norm development.

### Reporting and Transparency

SHL reports include explicit information about the norm group used, ensuring transparency:

**Typical Report Language**:
- "Numerical Reasoning: Sten 7 (Above Average compared to Managerial Professionals in Financial Services, n = 1,245)"
- "Persuasive: Sten 8 (High compared to UK Sales Professionals, n = 892)"

**Confidence Intervals**: Some reports include confidence intervals around sten scores, reflecting individual-level SEM:
- "Persuasive: Sten 8 (95% CI: Sten 7-9)"

This transparency allows users to evaluate the relevance and stability of the normative comparison.

### Key Takeaways

1. **Normative data are essential** for interpreting psychometric scores, transforming abstract metrics (theta, raw scores) into meaningful relative standings (stens, percentiles).

2. **Sten scores** (mean = 5.5, SD = 2.0, range 1-10) are SHL's standard metric, chosen to prevent over-interpretation of trivial differences and facilitate intuitive understanding.

3. **SHL maintains 92 OPQ norm groups and 70+ Verify norm groups**, stratified by job level, industry, function, and geography across 37 countries and 24 languages.

4. **Job-level stratification is critical** for cognitive ability tests, as ability distributions vary substantially across organizational levels due to selection and self-selection.

5. **Norm group selection is strategic**: Specific norms (e.g., "Executives in Consulting") provide relevant peer comparisons for selection; general norms (e.g., "All Managers") facilitate cross-role comparisons for development.

6. **Job-relevant norming** is legal and can reduce adverse impact by ensuring candidates are compared to appropriate peer groups, while within-group norming based on protected characteristics is prohibited.

7. **Norms are continuously updated** through data collection, sample size monitoring, recalibration, and cultural validation, ensuring ongoing relevance and representativeness.

8. **Transparency in reporting** (explicitly stating the norm group and sample size) enables users to evaluate the appropriateness and stability of normative comparisons.

---

