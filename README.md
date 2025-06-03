# EPL Sentiment Analysis and Standings Prediction

This project analyzes fan sentiment on Twitter and uses it to predict English Premier League (EPL) team standings. By gathering public emotions and reactions during games, we uncover how digital fan engagement correlates with on-field performance, using NLP and data analytics.

## Overview

Fans are highly vocal online—especially on Twitter—during EPL matches. Our goal was to see whether social sentiment could be a predictive tool for league outcomes. Using the VADER sentiment model, custom football-related term lists, and SAS Viya NLP, we created team-specific metrics and attempted to predict standings both mid-season and at the season's end.

## Data Source

We used the publicly available [EPL Teams - Twitter Sentiment Dataset](https://www.kaggle.com/datasets/wjia26/epl-teams-twitter-sentiment-dataset) from Kaggle. It contains tweets from:
- July 2020 – October 2020
- Team hashtags (e.g., #Chelsea, #Arsenal)
- Tweet text and timestamps
- Pre-computed sentiment polarities

## Methods

- Custom Sentiment Lexicons: Football-specific positive/negative and win/lose keyword lists.
- Negation Handling: Terms were excluded when negated (e.g., “not brilliant” ≠ positive).
- SAS Viya NLP Concepts: Used for text parsing and tagging.
- Team Objects (Python): Encoded data as Python classes for ranking comparisons.
- Ranking Models:
  - Engagement-based (e.g., total tweets, normalized sentiment)
  - Ratio-based (e.g., Pos/Neg tweet ratio, Win/Lose tweet ratio)

## Results

### Mid-Season (Matchday 4)

The most accurate predictor was:

**(Positive + Win) / (Negative + Lose) Tweet Ratio**

This metric reflected short-term form and real-time fan optimism/pessimism well.

### End-of-Season

**Fan engagement** (total tweet volume) aligned best with final league standings.

This suggests traditional popularity and brand loyalty remain predictive of long-term team success.

## Team Spotlights

- Liverpool: Highest positive sentiment; huge global engagement.
- Everton: Perfect start and high sentiment ratio, though mid-level engagement.
- Manchester United: High tweet volume, mostly negative early on, but rebounded strongly.
- Bournemouth: Not in the EPL that season but had the lowest sentiment, reflecting post-relegation discontent.

## Limitations

- Limited to Twitter — excludes Reddit, Instagram, etc.
- Sarcasm and irony challenge sentiment analysis accuracy.
- Focused only on short timeframes (snapshot-based analysis).

## Future Work

- Incorporate additional platforms and real-time data.
- Improve sentiment analysis with transformer-based models.
- Integrate multilingual support for broader fanbases.
- Correlate with match stats, ticket sales, and financial indicators.

## Team

- Najib A.
- Yi-Chyun W.
- Akram A.
- Hayden B.
- Bashir A.


## Citation

Kaggle, EPL Teams - Twitter Sentiment Dataset  
[https://www.kaggle.com/datasets/wjia26/epl-teams-twitter-sentiment-dataset](https://www.kaggle.com/datasets/wjia26/epl-teams-twitter-sentiment-dataset)
