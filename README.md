# LLM Humor Analysis Project

## Overview

This research project compares two approaches for generating humorous headlines using large language models (LLMs): 
1. Direct LLM generation 
2. Chain-of-Thought (CoT) conceptual blending 

The study evaluates 100 generated headlines across four metrics (humor, relevance, creativity, clarity) using LLM-as-a-Judge methodology to determine whether the more complex CoT approach provides measurable improvements over basic LLM generation.

## Key Research Questions
- **Primary Question**: Does Conceptual Blending (CoT) produce better humorous headlines than direct LLM generation?
- **Secondary Questions**:
  - Are there differences in specific quality dimensions (humor, relevance, creativity, clarity)?
  - What is the magnitude of any observed differences?

## Hypotheses
- **H0**: Conceptual Blending (CoT) does not produce better results than direct LLM generation
- **H1**: Conceptual Blending (CoT) produces better results than direct LLM generation

## Methodology
### Data Collection
- Dataset contains human evaluations of 100 headline pairs (LLM vs CoT) generated from the same seed concepts
- Each headline evaluated across four metrics:
  - Humor
  - Relevance
  - Creativity
  - Clarity

### Analysis Approach
1. Descriptive statistics and visualizations
2. Normality checks
3. Paired t-tests for overall and metric-specific comparisons
4. Effect size calculations
5. Multiple comparison adjustment
6. Non-parametric robustness checks
7. Bayesian analysis
8. Regression modeling

## Key Findings
1. **Primary Hypothesis**: No significant difference found between CoT and direct LLM generation (p = 0.769, d = 0.07)
2. **Metric-Specific Results**:
   - Clarity: Basic LLM produces significantly clearer headlines (p < 0.05)
   - Creativity: Non-significant trend favoring CoT
   - Humor and Relevance: No significant differences
3. **Bayesian Analysis**: Strong evidence in favor of null hypothesis (BF10 = 0.144)
4. **Regression Analysis**: No main effect of method, but significant metric differences

## Theoretical Implications
- Additional cognitive steps in CoT may not benefit humor generation
- Direct generation may preserve clarity better
- Creative potential of CoT requires further investigation

## Limitations
- Sample size of 100 headline pairs
- Potential rater bias in evaluations
- Limited to English language generation

## Future Research Directions
- Investigate different CoT prompting strategies
- Examine interaction effects between metrics
- Expand to other languages and text genres

## Conclusion
This study found no significant overall advantage of CoT conceptual blending over direct LLM generation for humorous headlines, with a small but significant clarity advantage for direct generation.

## Repository Structure
- `eval_dataset_transformed.csv`: Evaluation dataset
- `stats.Rmd`: R script containing all statistical analyses

## Dependencies
The analysis requires the following R packages:
- tidyverse
- ggpubr
- rstatix
- effectsize
- caret
- BayesFactor
- lme4
- ggcorrplot
