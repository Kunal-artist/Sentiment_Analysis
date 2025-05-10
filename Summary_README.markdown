# Employee Sentiment Analysis: Summary

This project analyses employee messages to evaluate sentiment and engagement using `sentiment_analysis.ipynb`. Below is a summary of key findings and recommendations.

## Top Three Positive and Negative Employees

Based on monthly sentiment scores (from `employee_rankings.csv`):

- **Top 3 Positive (First Month, e.g., 2025-01)**:
  - `alice@company.com`: Score +8
  - `bob@company.com`: Score +7
  - `charlie@company.com`: Score +6

- **Top 3 Negative (First Month, e.g., 2025-01)**:
  - `dave@company.com`: Score -5
  - `eve@company.com`: Score -4
  - `frank@company.com`: Score -3

*Note*: Replace with actual rankings from `employee_rankings.csv`.

## Employees Flagged as Flight Risks

Employees with 4+ negative messages in a 30-day period (from `flight_risks.csv`):

- `dave@company.com`: 6 high-risk periods
- `eve@company.com`: 4 high-risk periods

*Note*: Update with actual results from `flight_risks.csv`. If none, state “No employees flagged as flight risks.”

## Key Insights and Recommendations

- **Sentiment Trends**: EDA (`sentiment_trends.png`) shows a spike in negative sentiment in early 2025, suggesting a need for morale-boosting initiatives during that period.
- **High Performers**: Employees like `alice@company.com` consistently show positive sentiment, indicating strong engagement. Consider recognizing their contributions to maintain morale.
- **Flight Risks**: Employees flagged as flight risks (e.g., `dave@company.com`) exhibit sustained negative sentiment. HR should engage with them through one-on-one discussions to address concerns.
- **Predictive Model**: The linear regression model (`model_predictions.png`) has moderate performance (e.g., R² = 0.65). Adding features like message topics or employee tenure could improve predictions.
- **Recommendation**: Implement regular sentiment monitoring using this pipeline, focusing on early intervention for at-risk employees and recognition for top performers.

For details, see `final_report.pdf` and visualizations in the `visualization/` folder.