# Spotify Predictive Analytics / Classification Modeling (R)

## Overview
This project analyzes a Spotify songs dataset (~32K tracks) and builds interpretable models to understand what drives **track popularity** and to classify whether a song is a **“Hit”** (defined as the **top 25% by popularity**) versus a “Flop”. The goal is to turn audio-feature data into a practical, data-driven way to **prioritize tracks** and **guide promotion decisions**. :contentReference[oaicite:1]{index=1}

## What I Built
- **R tidyverse pipeline** to import, clean, and analyze a Spotify track dataset (audio features + popularity). :contentReference[oaicite:2]{index=2}  
- **Three modeling approaches**:
  1. **Linear regression** to model popularity as a continuous score. :contentReference[oaicite:3]{index=3}  
  2. **Logistic regression** to predict the probability a track is a **Hit** (top 25% popularity). :contentReference[oaicite:4]{index=4}  
  3. **Decision tree** to generate simple “if/then” rules that are easy for stakeholders to interpret. :contentReference[oaicite:5]{index=5}  

## Dataset & Features
The dataset contains track-level attributes including:
- Audio features (e.g., **danceability, energy, valence, acousticness, tempo, duration**)  
- Playlist genre (e.g., `playlist_genre`)  
- Popularity score (`track_popularity`, 0–100) :contentReference[oaicite:6]{index=6}  

## Business Value
This work is framed like a “record label” decision problem: instead of relying on gut feel, the analysis supports a **data-driven checklist** for selecting and promoting tracks—helping reduce wasted marketing spend and focus attention on songs whose features historically align with hits. :contentReference[oaicite:7]{index=7}  

## Key Outputs
### Hit vs. Flop Classification (Logistic Regression)
A simple classifier was created by labeling tracks as **Hit** when predicted probability ≥ 0.5 and evaluating results with a confusion matrix. :contentReference[oaicite:8]{index=8}

### Interpretable “Hit Rules” (Decision Tree)
The decision tree produces easy-to-communicate rules. Example insights from the tree:
- Highly danceable songs in certain genres are more likely to be hits.
- Some low-energy songs in specific genres are rarely hits. :contentReference[oaicite:9]{index=9}  

## Tools & Libraries
- `tidyverse`, `lubridate` for data cleaning and exploration  
- `broom` for model output tables  
- `rpart`, `rpart.plot` for decision trees  
- `knitr`, `kableExtra` for reporting :contentReference[oaicite:10]{index=10}  

## Repository Contents
- **Final report (HTML):** `Spotify-Predictive-Analytics-Classification-Modeling-Project.html` (full write-up with EDA + modeling + insights) :contentReference[oaicite:11]{index=11}  
- (Optional/Recommended) **Analysis code:** If you include the R/Rmd source used to generate the report, place it in a `/src` or `/analysis` folder for easy review.

## How to Run (If You Add the R Script / Rmd)
1. Open RStudio
2. Install packages (once):
   ```r
   install.packages(c("tidyverse","lubridate","broom","rpart","rpart.plot","knitr","kableExtra"))

