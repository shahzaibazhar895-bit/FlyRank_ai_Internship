# CTR / Engagement Opportunity Scoring Using Search Visibility Signals

## Abstract

This project investigates whether search visibility and engagement metrics can identify content pages that may benefit from CTR optimization or content review.

Using the FlyRank Internship Warehouse dataset, content-level features were aggregated from March 2026 observations.

A rule-based baseline and a Random Forest model were used to identify low-engagement content opportunities.

Results were evaluated using the same train-test split and compared using standard classification metrics.

The final output is a ranked recommendation list intended for decision-support rather than causal conclusions.

## Introduction

This project supports content review decisions by ranking pages that show strong visibility but weak click or engagement performance.

## Data

Dataset: FlyRank Internship Warehouse Dataset

Table:
fact_content_daily_performance

Time Window:
March 2026

Features:
- gsc_impressions
- gsc_clicks
- gsc_avg_position
- ga4_sessions
- ga4_engaged_sessions

Excluded:
- content_hash_id
- client_hash_id

## Methodology

Baseline:
Rule-based scoring system from ML-07.

Model:
Random Forest Classifier.

Validation:
80/20 train-test split.

Leakage Checks:
- No future windows
- No label-derived features
- Only historical observed metrics

## Results

The Random Forest model was compared against a rule-based baseline using the same train-test split.

Results were evaluated using:
- Accuracy
- Precision
- Recall
- F1 Score

## Limitations

This project identifies observed relationships between search visibility and engagement metrics.

The results should be interpreted as directional and decision-support signals.

The model does not prove causation.

## Ranked Recommendations

Pages predicted as low-engagement opportunities are ranked for review.

Possible actions:

- Improve titles
- Improve meta descriptions
- Improve content quality
- Monitor rankings

## Reproducibility

Repository:

https://github.com/YOUR_USERNAME/Flyrank-Internship

Notebook:

work/notebooks/capstone.ipynb

## Acknowledgments & Data Credit

Built on the FlyRank ML Internship Dataset.

https://flyrank.ai
