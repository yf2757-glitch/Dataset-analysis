#  👩‍💻Explore Lexical Decision Data - relation between reaction time and word features
_HUDK 4054 Individual Assignment 2_
## Project Information
**Creator:** Yuhan Fu  
**Principal Investigator:** Yuhan Fu  
**Data Manager:** Yuhan Fu  
**ORCID iD:** 0009-0004-8907-3114  
**Affiliation:** Teachers College, Columbia University  
**Research Date:** 2025-10-02  

## Project Description
This project explores lexical decision data to investigate how word-level features influence reaction time during word recognition. The dataset (*Haro et al., 2024*) includes average reaction times, error rates, and a rich set of psycholinguistic variables (e.g., frequency, word length, age of acquisition, familiarity, concreteness). By analyzing these variables, we aim to replicate well-established findings in psycholinguistics and highlight how word characteristics shape lexical access.

## Research Aim
The primary goal is to examine the relationship between reaction time and word features, specifically focusing on:
1. Word length (orthographic complexity)  
2. Familiarity (subjective frequency of exposure)  
3. Frequency and age of acquisition (classic predictors of lexical decision performance)

## Hypothesis
- **H1 (Word Length Effect):** Longer words will elicit slower reaction times in the lexical decision task.  
- **H2 (Familiarity Effect):** More familiar words will elicit faster reaction times.  
- **H3 (Frequency Effect):** Higher frequency words will be recognized more quickly than lower frequency words.  
- **H4 (Age of Acquisition Effect):** Words acquired earlier in life will show faster reaction times compared to later-acquired words.

## How to Reproduce

The analyses can be reproduced using **Excel** with the Data Analysis Toolpak enabled.

### 1. Descriptive Statistics
- Go to **Data → Data Analysis → Descriptive Statistics**.  
- Select variables such as `mean_rt`, `length`, `fam`, `log_frq`, and `aoa`.  
- Output mean, SD, min, max for each variable.  

### 2. Correlation Analysis
- Method A (formula):  
  - In an empty cell, type:  
    `=CORREL(B2:B1000, C2:C1000)`  
    (replace with the actual column ranges for `mean_rt` and another variable).  
- Method B (tool):  
  - Go to **Data → Data Analysis → Correlation**.  
  - Select the range covering `mean_rt`, `length`, `fam`, `log_frq`, `aoa`.  
  - Output the correlation matrix to view r values.  

### 3. Scatter Plots with Trendlines
- Select two columns (e.g., `length` and `mean_rt`).  
- Go to **Insert → Chart → Scatter Plot**.  
- Right-click data points → **Add Trendline → Linear**.  
- Check options: **Display Equation** and **Display R² on chart**.  
- Repeat for:  
  - `fam` vs. `mean_rt` (H2)  
  - `log_frq` vs. `mean_rt` (H3)  
  - `aoa` vs. `mean_rt` (H4)  

### 4. Regression (Optional)
- Go to **Data → Data Analysis → Regression**.  
- Dependent variable (Y): `mean_rt`.  
- Independent variables (X): `length`, `fam`, `log_frq`, `aoa`.  
- Output regression summary (coefficients, p-values, R²).  

### 5. Interpret Results
- **H1:** RT × Length → Positive correlation (longer words = slower RT).  
- **H2:** RT × Familiarity → Negative correlation (familiar words = faster RT).  
- **H3:** RT × Frequency → Negative correlation (higher frequency = faster RT).  
- **H4:** RT × AoA → Positive correlation (later-acquired words = slower RT).  

## Results (Preliminary Findings)

### Correlation Analyses
- **Reaction Time × Word Length (H1):**  
  r = 0.27 → Positive correlation. Longer words are associated with slower reaction times, supporting the Word Length Effect.  

- **Reaction Time × Familiarity (H2):**  
  r = -0.55 → Negative correlation. More familiar words are recognized faster, supporting the Familiarity Effect.  

- **Reaction Time × Frequency (H3):**  
  Expected: Negative correlation (higher frequency → faster RT).  
  Analysis: In this dataset, words with higher log frequency show faster reaction times, consistent with the Frequency Effect.  

- **Reaction Time × Age of Acquisition (H4):**  
  Expected: Positive correlation (later-acquired words → slower RT).  
  Analysis: Words acquired earlier in life tend to be recognized faster, supporting the Age of Acquisition Effect.  

### Summary
- **Word length** increases processing demands → slower recognition.  
- **Familiarity** improves lexical accessibility → faster recognition.  
- **Frequency** facilitates lexical access, confirming a robust frequency effect.  
- **Age of Acquisition** strongly predicts RT: earlier-acquired words are processed faster.  

These results replicate classic psycholinguistic effects observed in lexical decision tasks.


## Data Source
- Dataset: *Lexical Decision Data.xlsx*
- Task: Lexical decision (word vs. nonword judgment)
- Each row = one word, with average reaction time (RT), error rate, and psycholinguistic variables.
