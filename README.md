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

This section documents all YouTube playlists and videos used for scraping public comments, organized by year, candidate, and debate event. Comment counts are provided for each dataset.

---

### 2016 Presidential Election

#### Campaign Speech Videos

**Hillary Clinton**
- **Playlist:** `PL3-OIwNPoC3Lj68487lgoJiwrXx5lVO8e`
- **Comments stored:** `Data/2016hillary_comments.csv`
- **Videos:**
    - [June 7, 2016, Hillary Clinton makes history (Full speech)](https://www.youtube.com/watch?v=FN6KBbug9gA)
    - [July 25, 2016, Hillary Clinton's full speech at the 2016 DNC](https://www.youtube.com/watch?=C6GnHBEBWYE)
    - [August 8, 2016, Hillary Clinton Kissimmee FULL Speech](https://www.youtube.com/watch?v=HG6MEdn1QBs)
    - [September 23, 2016, Mirrors | Hillary Clinton](https://www.youtube.com/watch?v=vHGPbl-werw)
    - [October 31, 2016, Kent, Ohio Rally](https://www.youtube.com/watch?v=_uqmcnwjHrY)
    - [November 8, 2016, Midnight rally in North Carolina](https://www.youtube.com/watch?v=n7Tamj06FQs)
- **Comment totals:**  
    - With replies: 1,669  
    - Without replies: 1,001

**Donald Trump**
- **Playlist:** `PL3-OIwNPoC3II9mG8jLIN8ODWydLnU1bB`
- **Comments stored:** `Data/2016trump_comments.csv`
- **Videos:**
    - [May 25, 2016, Anaheim, CA](https://www.youtube.com/watch?v=ltNVyvK8Paw)
    - [July 21, 2016, RNC Cleveland, OH](https://www.youtube.com/watch?v=F5XmFG3221s)
    - [August 19, 2016, First Campaign TV Ad](https://www.youtube.com/watch?v=FEgykfioeuw)
    - [September 6, 2016, Greenville, NC](https://www.youtube.com/watch?v=gXMAvppTSAY)
    - [October 30, 2016, Greeley, CO](https://www.youtube.com/watch?v=aMZsKq99hdk)
    - [November 5, 2016, Denver, CO](https://www.youtube.com/watch?v=KIKNSZ_Nf3w)
- **Comment totals:**  
    - With replies: 4,721  
    - Without replies: 2,023

---

#### Presidential Debate Videos

We sampled equally from media sources representing both political leanings. For source trustworthiness and rationale, see [Pew Research](https://www.pewresearch.org/journalism/2014/10/21/section-1-media-sources-distinct-favorites-emerge-on-the-left-and-right/).

**Democratic-Leaning & Mainstream Media**  
- **Playlist:** [Link](https://www.youtube.com/watch?v=rfq0Yw2sMq0&list=PL3-OIwNPoC3Lhs0Iob2u9_jMaBhubek3r)  
- **Comments stored:** `Data/2016Dem_debate_comments.csv`
- **Videos:**  
    - [NBC, First Debate](https://www.youtube.com/watch?v=855Am6ovK7s)
    - [NYT, Second Debate](https://www.youtube.com/watch?v=rfq0Yw2sMq0)
    - [NBC, Second Debate](https://www.youtube.com/watch?v=FRlI2SQ0Ueg)
    - [23ABC, Second Debate](https://www.youtube.com/watch?v=h-gkBUbU_F4)
    - [CBS, Final Debate](https://www.youtube.com/watch?v=FZ_G5j9yVIU)
    - [C-SPAN, Final Debate](https://www.youtube.com/watch?v=ANT_ZBhpvtw&t=173s)
    - [NYT, Final Debate](https://www.youtube.com/watch?v=Z_pEb1bDN-w)
- **Comment totals:**  
    - With replies: 94,219  
    - Without replies: 52,283

**Republican-Leaning & Alternative Media**  
- **Playlist:** [Link](https://www.youtube.com/watch?v=lTgieGfYVQs&list=PL3-OIwNPoC3JFEvZP_nSMPrib8viH2KX-)
- **Comments stored:** `Data/2016Rep_Debates_comments.csv`
- **Videos:**  
    - [First Debate Highlights](https://www.youtube.com/watch?v=lTgieGfYVQs)
    - [FOX, First Debate](https://www.youtube.com/watch?v=lIexQNGxwog)
    - [Fox News, Third Debate Pt 1](https://www.youtube.com/watch?v=cyx5e2c1SgU)
    - [Fox News, Third Debate Pt 2](https://www.youtube.com/watch?v=BgPENwntzKk)
    - [Fox News, Third Debate Pt 3](https://www.youtube.com/watch?v=Uaujjp3JKGY)
    - [CBC, Final Debate](https://www.youtube.com/watch?v=dXWdiz--X0s)
    - [NBC News-YouTube Democratic Debate (Full)](https://www.youtube.com/watch?v=ti2Nokoq1J4)
- **Comment totals:**  
    - With replies: 11,005  
    - Without replies: 5,569

---

### 2020 Presidential Election

#### Campaign Speech Videos

**Joe Biden**
- **Playlist:** `PL3-OIwNPoC3IHwPNuYmzxr6Lk7Fx_XViX`
- **Comments stored:** `Data/2020biden_comments.csv`
- **Videos:**  
    - [April 29, Bloomberg News](https://www.youtube.com/watch?v=lFISnAndKOA)
    - [April 29, CBS](https://www.youtube.com/watch?v=ApsEgQvHfIo)
    - [May 18, Biden Campaign](https://www.youtube.com/watch?v=FaN-Pf_LW1Q)
    - [June 11, Washington Post](https://www.youtube.com/watch?v=pB4BxNjMb7Q)
    - [July 6, MSNBC](https://www.youtube.com/watch?v=DvWrekxwo2o)
    - [August 7, Biden Campaign](https://www.youtube.com/watch?v=FiPVOx-cAfQ)
    - [September 2, DMRegister](https://www.youtube.com/watch?v=9GvZh9Rs7nE)
    - [October 31, NBC](https://www.youtube.com/watch?v=Tc0Gb6coKKQ)
    - [November 2, Pittsburgh Rally](https://www.youtube.com/watch?v=Fkh0DXiCvPA)
- **Comment total (without replies):** 4,357

**Donald Trump**
- **Playlist:** `PL3-OIwNPoC3LAML6nXUF4D1ynbi17-ILC`
- **Comments stored:** `Data/2020trump_comments.csv`
- **Videos:**  
    - [May 20, Fox News](https://www.youtube.com/watch?v=GgINUxecNrg)
    - [June 20, Yahoo Finance](https://www.youtube.com/watch?v=niCxnEyG0SM)
    - [July 4, USA Today](https://www.youtube.com/watch?v=mXD4zPY4Ai0&t=56s)
    - [August 15, CBS](https://www.youtube.com/watch?v=Iw_lKnYHrDc)
    - [September 12, One America News](https://www.youtube.com/watch?v=5nD2s9dWess)
    - [October 21, NBC](https://www.youtube.com/watch?v=wolUfDLP2Kw)
    - [November 1, NBC](https://www.youtube.com/watch?v=BRnyOdnDpmc)
- **Comment total (without replies):** 10,398

---

#### Presidential Debate Videos

**Democratic-Leaning & Mainstream Media**
- **Playlist:** `PL3-OIwNPoC3Lpa7NKQXfKolxzEjel7x6A`
- **Comments stored:** `Data/2020Dem_debate_comments.csv`
- **Videos:**  
    - [September 29, CNN](https://www.youtube.com/watch?v=yHFI8TsSKXY)
    - [September 29, CBS](https://www.youtube.com/watch?v=9HnKFUNlcfY)
    - [October 22, CNN](https://www.youtube.com/watch?v=rOn7uGVVf1I)
    - [October 22, NBC](https://www.youtube.com/watch?v=UCA1A5GqCdQ)
- **Comment total (without replies):** 25,944

**Republican-Leaning & Alternative Media**
- **Playlist:** `PL3-OIwNPoC3I8nu1EMXZbL9YFuqb1XAkj`
- **Comments stored:** `Data/2020Rep_Debates_comments.csv`
- **Videos:**  
    - [September 29, Sky News](https://www.youtube.com/watch?v=K8Z9Kqhrh5c&t=516s)
    - [September 29, CSPAN](https://www.youtube.com/watch?v=wW1lY5jFNcQ)
    - [October 22, WSJ](https://www.youtube.com/watch?v=RHISJrOODJ4)
    - [October 22, CSPAN](https://www.youtube.com/watch?v=bPiofmZGb8o)
- **Comment total (without replies):** 17,235

---

### 2024 Presidential Election

*Note: Kamala Harris announced her candidacy in July 2024, so comment collection began in July rather than April.*

#### Campaign Speech Videos

**Kamala Harris**
- **Playlist:** `PL3-OIwNPoC3ITusqZ8RCe9ssy0ApktiBk`
- **Comments stored:** `Data/2024kamela_comments.csv`
- **Videos:**  
    - [July 21, ABC News](http://youtube.com/watch?v=V_I7gRpwTBc)
    - [July 30, FOX 5 Atlanta](https://www.youtube.com/watch?v=_lpYc-Ww8j4)
    - [August 11, WFAA, ABC, Las Vegas](https://www.youtube.com/watch?v=3P_lKUqz9E8)
    - [August 6, Fox local, Philadelphia](https://www.youtube.com/watch?v=rONg2cCqFBk)
    - [September 25, WFAA, ABC, Pittsburgh](https://www.youtube.com/watch?v=-i64tqglpmA)
    - [October 4, Campaign, Flint, MI](https://www.youtube.com/watch?v=gVzjoxj-ZQQ)
    - [November 4, WFAA, ABC, Pennsylvania](https://www.youtube.com/watch?v=TlR70XK8LiA)
- **Comment total (without replies):** 10,200

**Donald Trump**
- **Playlist:** `PL3-OIwNPoC3LxBJ6G_jJYpX98W0AoGYoY`
- **Comments stored:** `Data/2024trump_comments.csv`
- **Videos:**  
    - [July 19, FOX RNC](https://www.youtube.com/watch?v=YEsd7esFjbw)
    - [August 21, FOX 4, NC Rally](https://www.youtube.com/watch?v=aKN7R92eoxM)
    - [September 21, FOX 4, NC Rally](https://www.youtube.com/watch?v=OZXpNddHBm8)
    - [September 21, WFAA ABC, Wilmington, NC](https://www.youtube.com/watch?v=xC9rEV0GQ2c&list=PL3-OIwNPoC3LxBJ6G_jJYpX98W0AoGYoY&index=3)
    - [October 24, WFAA ABC, Latrobe, PA](https://www.youtube.com/watch?v=bI_lAV16738)
    - [November 1, FOX Michigan Rally](https://www.youtube.com/watch?v=4v46FwsLUOc)
- **Comment total (without replies):** 7,844

---

#### Presidential Debate Videos

There was one debate on September 10, 2024, between Kamala Harris and Donald Trump.

**Democratic-Leaning & Mainstream Media**
- **Playlist:** `PL3-OIwNPoC3L405ZyoH5Yb6oR_Od49j7i`
- **Comments stored:** `Data/2024Dem_debate_comments.csv`
- **Videos:**  
    - [ABC](https://www.youtube.com/watch?v=4aw5FziSc14)
    - [MINT](https://www.youtube.com/watch?v=npgogT5ir4M)
    - [Bloomberg News](https://www.youtube.com/watch?v=WATb4fet7MA)
    - [Boston Globe](https://www.youtube.com/watch?v=OQgE0ETV81s)
    - [PBS](https://www.youtube.com/watch?v=yjPxL5w3OOU)
    - [NBC](https://www.youtube.com/watch?v=fpu1QEB03xA)
    - [ABC](https://www.youtube.com/watch?v=4dOgWZsDB6Q)
    - [CNN](https://www.youtube.com/watch?v=kADujQsWO68)
- **Comment total (without replies):** 36,480

**Republican-Leaning & Alternative Media**
- **Playlist:** `PL3-OIwNPoC3KQ4d8hMwGIQnBB4A3Dm3UO`
- **Comments stored:** `Data/2024Rep_debate_comments.csv`
- **Videos:**  
    - [WSJ](https://www.youtube.com/watch?v=VgsC_aBquUE)
    - [FOX](https://www.youtube.com/watch?v=4IGd0BrrXoI)
- **Comment total (without replies):** 51,652

---

**References:**
- [Pew Research Center Media Trust Study (2014)](https://www.pewresearch.org/journalism/2014/10/21/section-1-media-sources-distinct-favorites-emerge-on-the-left-and-right/)


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
