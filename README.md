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

## Dataset Information
- **Source:** Open Science Framework (OSF)  
- **Project Link:** [https://osf.io/rvyxt](https://osf.io/rvyxt)  
- **How to Find:**  
  - On OSF, search with keyword: *lexical task*.  
  - Locate the dataset titled: *AI-generated estimates of word familiarity, valence, arousal and concreteness in Spanish*.  
  - Inside the project page, you can download the file: **Haro et al (2024) Lexical decision data.xlsx**.  
- **File Name Adjustment:**  
  - On my local computer, I renamed the file to **Lexical decision data.xlsx** for simplicity.  
  - (This step is optional; you can keep the original filename if preferred.)  
## Data Dictionary

| Variable name | Readable name       | Units         | Allowed values | Definition | Synonyms | Description |
|---------------|---------------------|---------------|----------------|------------|----------|-------------|
| word          | Word                | Text (string) | Any Spanish word | The lexical item presented in the task | stimulus | The target word shown to participants in the lexical decision task. |
| mean_rt       | Mean reaction time  | Milliseconds  | Positive values | Average reaction time for the word in the lexical decision task | RT | Higher values indicate slower recognition. |
| mean_error    | Mean error rate     | Percentage (%)| 0–100           | Average error rate (%) across participants | error rate | Proportion of incorrect responses for the word. |
| valence       | Valence rating      | 1–9 scale     | 1 = negative, 9 = positive | Emotional valence rating | affect | Perceived pleasantness/unpleasantness of the word. |
| arousal       | Arousal rating      | 1–9 scale     | 1 = calm, 9 = highly arousing | Emotional arousal rating | activation | Degree of excitement or activation evoked by the word. |
| conc          | Concreteness        | 1–9 scale     | Higher = more concrete | Concreteness rating | imageability | Extent to which the word refers to a tangible, perceptible entity. |
| fam           | Familiarity         | 1–9 scale     | Higher = more familiar | Familiarity rating | subjective frequency | Degree to which the word is perceived as commonly known/used. |
| aoa           | Age of acquisition  | Years         | Positive values | Average age at which the word is typically acquired | AoA | Lower = earlier acquired, easier/faster recognition. |
| log_frq       | Log frequency       | Log-transformed frequency | Any real number | Word frequency (log transformed) | frequency | Higher frequency words are recognized faster. |
| log_ctx_div   | Log context diversity | Log-transformed | Any real number | Contextual diversity of word occurrences | context diversity | Higher = word appears across more varied contexts. |
| length        | Word length         | Letters       | Positive integers | Number of letters in the word | characters | Orthographic length of the stimulus. |
| n             | Orthographic neighbors | Count | Positive integers | Number of words differing by one letter | neighbors | Words orthographically similar to the target. |
| nhf           | Higher-frequency neighbors | Count | Positive integers | Number of orthographic neighbors with higher frequency | HF neighbors | Indicator of lexical competition. |
| freq_hf       | Frequency of higher-frequency neighbors | Frequency count | Positive values | Frequency of the most frequent orthographic neighbor | — | Reflects the dominance of neighboring words. |
| old20         | Orthographic Levenshtein Distance 20 | Distance metric | Positive values | Mean distance to the 20 closest orthographic neighbors | OLD20 | Lower = more similar to other words. |
| bg_freq       | Background frequency | Frequency count | Positive values | Frequency in the background corpus | corpus freq | Global frequency across a reference corpus. |
| tg_freq       | Target frequency     | Frequency count | Positive values | Frequency in the target corpus | — | Frequency within the experimental corpus. |
| num_phon      | Number of phonemes   | Count | Positive integers | Number of phonemes in the word | phon count | Size of the phonological representation. |
| num_syll      | Number of syllables  | Count | Positive integers | Number of syllables in the word | syllables | Basic phonological segmentation. |
| n_phon        | Phonological neighbors | Count | Positive integers | Number of words differing by one phoneme | phon neighbors | Phonologically similar words. |
| nhf_phon      | Higher-frequency phonological neighbors | Count | Positive integers | Number of phonological neighbors with higher frequency | HF phon neighbors | Reflects competition in spoken word recognition. |
## Standards Compliance

The chosen metadata standard for this project is the **DDI Codebook (DDI-C) standard**.

### Why DDI-C?
- The dataset is a **single experimental dataset** (lexical decision task results) rather than a large-scale longitudinal survey.  
- DDI-C is designed for **study-level documentation** and **variable-level metadata**, which is sufficient for this type of dataset.  
- Unlike DDI-Lifecycle, which covers the entire research process (design, collection, versioning, reuse), DDI-C focuses on **describing the dataset and its variables**, making it appropriate here.

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
