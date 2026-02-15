# Track 3 – Deployment Planning

## Do predictions need to be instant?

Overnight batch predictions are sufficient because churn risk does not change minute-by-minute. Weekly scoring is realistic and cost-effective.

## How would it run?

A scheduled Python job would extract updated customer data weekly, score customers using the trained model, and store results in a database table (e.g., churn_scores). The retention team would access results via a dashboard.

## Software Approach

- Scheduled Python script
- SQL data extraction
- Model scoring process
- Write predictions back to database

## Monitoring Plan

### Data Quality Check
Monitor missing values in key predictors weekly.

### Input Drift Check
Track distribution shifts in monthly fee and usage variables.

### Outcome Check
Compare predicted churn rate vs actual churn rate monthly.
