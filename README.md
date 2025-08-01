# Social Media Sentiment vs. Polls: Predicting U.S. Presidential Election Outcomes

## Project Title & Overview

**Can Social Media Sentiment Beat Traditional Polls at Predicting U.S. Presidential Elections?**

This project investigates whether classic national opinion polling or YouTube sentiment analysis more accurately predicts U.S. presidential election winners.  
**Key findings:** Polling correctly predicts about 78% of elections across 1936–2024. Social media sentiment, however, captured certain “upset” years—such as 2016—where polls missed the mark.

### Motivation

Election forecasting is central to campaign strategy, media coverage, and even voter decision-making. With social media now shaping public opinion in real time, we set out to answer: **Should analysts and campaigns still trust polls, or does real-time sentiment offer a better signal?**

---

## Data Sources

**National Polling:**
- [Wikipedia: Polling for United States presidential elections](https://en.wikipedia.org/wiki/Polling_for_United_States_presidential_elections) (CSV)
- [270toWin: Historical Presidential Elections](https://www.270towin.com/historical-presidential-elections/) (CSV)

**Sentiment Analysis / YouTube Comments:**
- [YouTube - Official campaign channels and debate playlists, 2016, 2020, 2024:]
    - [2024 Presidential Debates (NBC News)](https://www.youtube.com/playlist?list=PL0b6OzIxLPbz9pqWh7fhgW01W1yYGWZxd)
    - [Joe Biden Campaign Channel](https://www.youtube.com/@JoeBiden)
    - [Donald Trump Campaign Channel](https://www.youtube.com/@realDonaldTrump)
    - [RFK Jr. Channel](https://www.youtube.com/@RobertKennedyJr)
    - [2016/2020 Debates, Fox News, C-SPAN, CNN, NBC News, etc.]  
    *(see YouTube scraping notebooks for full lists)*

**Data Dictionary:**  
See [Baseline_Model_Data.csv](Baseline_Model_Data.csv) and [YouTube dataset](youtube_scraper.ipynb) for column definitions:
- `year`: Election year
- `Poll_Leader`: Party leading in polls (Democrat/Republican)
- `Poll_Leading_Margin`: Poll lead size (percentage points)
- `EC_election_winner`: Electoral College winner (Democrat/Republican)
- `sentiment_score`: Compound VADER sentiment (YouTube data)
- (etc. — see data files for all variables)

**Data Preprocessing Steps:**
- **Polling data:** Scraped, averaged monthly polling for each party/year, engineered features for leader/margin, matched with election results.
- **YouTube sentiment:** Scraped comments for selected events, deduplicated, removed replies, and labeled by candidate/event for fairness and reproducibility.

---

## Methodology

### Approach

- **Polling:** Logistic regression (main), random forest for robustness.
- **Sentiment:** VADER and Hugging Face sentiment models on YouTube comments, compared to actual election outcomes.

### Software and Libraries

- **Python 3.8+**
- `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`
- `beautifulsoup4` (scraping), `nltk` (VADER), `transformers` (Hugging Face)
- Jupyter Notebook
- Google Colab Notebook

### Key Steps

- Data scraping and cleaning
- Exploratory data analysis (EDA)
- Feature engineering (poll leader, margin, sentiment scores)
- Model training and evaluation:
    - **Polling:** Logistic regression, accuracy, confusion matrix, LOOCV
    - **Sentiment:** VADER sentiment scoring, Hugging Face model outputs, accuracy against actual results
- Comparison of polling vs. sentiment models

---

## Results

### Key Findings

- **Polling:** Logistic regression using polling leader/margin predicts about **78%** of winners (using LOOCV), with most errors during “upset” years.
- **Sentiment:** VADER-based sentiment analysis explained certain surprising outcomes, most notably 2016, where YouTube sentiment captured a Republican surge polls missed.
- **Comparison:** In recent cycles, social sentiment sometimes matched or exceeded the predictive power of polls.

### Tables and Figures

- Accuracy by year (bar/line charts): Visual comparisons of polling model accuracy across all presidential election cycles, and bar graphs showing years when polls or sentiment accurately predicted the winner.
- Confusion matrices for model outputs: For both polling and sentiment models, confusion matrices show where each model got results right or wrong by party and year.
- Year-by-year upset visualizations: Charts highlight which cycles had “upset” outcomes, where sentiment diverged from polls and the actual result.
- **Sentiment analysis visualizations:** Figures showing the distribution of sentiment scores by candidate, cycle, and party. These visuals helped trace how online mood correlated with real election results.
- **Hugging Face model outputs:** Additional figures demonstrate how deep learning-based sentiment labels compared to VADER sentiment, offering another perspective on “positive” vs “negative” election sentiment.

### Model Performance

- Polling model accuracy: **78%** (LOOCV)
- Sentiment model accuracy: VADER sentiment analysis successfully matched the real winner in the 2016, 2020, and 2024 cycles, including correctly “calling” the 2016 Republican win that polling missed. Hugging Face-based sentiment labels tracked closely with VADER and actual election results, reinforcing the predictive value of social sentiment.
- See notebook visuals for precision, recall, and historical trend graphs
- **Key takeaways:** Sentiment models were particularly valuable in cycles with major polling upsets, capturing shifts in public mood and “hidden” support not measured by traditional surveys.

---

## Conclusion

**Summary of Findings:**  
- Polling is still a valuable tool but has clear blind spots—especially when public mood shifts fast, or hidden voters are missed.
- Sentiment analysis can capture shifts missed by polls, but is limited by data quality, comment restrictions, and retrospective analysis.

**Limitations:**  
- YouTube comments are not a representative sample of all voters.
- Some official campaign channels restrict or delete comments.
- Both polling and sentiment data are subject to bias and historical change.

**Future Work:**  
- Expand analysis to Twitter, Reddit, and other platforms.
- Experiment with real-time sentiment tracking and more advanced models.
- Analyze state-level or demographic breakdowns.

---

## Setup and Usage

**Installation Instructions:**
- Clone this repository
- Install requirements with `pip install -r requirements.txt` (if available)

**Running the Code:**
- Open and run `Baseline_Model_Data.ipynb` (polling analysis)
- Open and run `youtube_scraper.ipynb` (data collection) and `processing_modeling_visualization.ipynb` (sentiment analysis)

**Example Usage:**
- See provided notebooks for usage examples and to reproduce all results

---

## Contributors

- **Swathi** – Polling Data Collection, Baseline Modeling, Reporting  
- **August** – YouTube Data Collection and Curation  
- **Waleed** – Sentiment Analysis Modeling


---

## Additional Information

**Licensing:** MIT License (add LICENSE file if needed)

**Reproducibility:**  
- All data sources and code are included or linked.
- Notebooks are executable from top to bottom with the provided datasets.
- Results can be reproduced by running the notebooks as described above.
