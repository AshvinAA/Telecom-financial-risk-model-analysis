# Telecommunication Customer Churn : A Financial Risk Model

## Summary 
Where traditional machine learning project's success are evaluated with their accuracy or F1-scores . In corporate environments however, all the predictive errors do not cost the same.

This project reframes a customer churn prediction as a Financial Risk Management problem. By developing a custom Expected Value loss function, this system shifts the focus from purely classifying customers to actively calculating and minimizing revenue drain.

## Objectives fulfilled 
- Identified $1.9 Million in lifetime revenue loss from month-to-month contracts.

- Mathematically proved that prioritizing a high-recall algorithm over a high-accuracy algorithm saves the firm massive amounts of revenue by aggressively catching high-value flight risks.

- Translated model probabilities into an actionable, tiered targeting dashboard for marketing and retention teams.

## The Business Problem 


In the telecommunications sector, customer acquisition costs are high, making retention a critical driver of profitability. When machine learning models are deployed to predict which customers will leave (churn), data scientists typically optimize for overall accuracy.

When we treat all metrics the same , we ignore the importance of one over all the others 

Here: 

- A False Positive (predicting a loyal customer will churn) results in a wasted promotional discount.

- A False Negative (failing to predict a churner) results in the loss of that customer's entire lifetime revenue.

Because the financial penalty of losing a customer is drastically higher than the cost of a promotional discount, optimizing for accuracy actually loses the business money.

## The Financial Methodology 

To align the machine learning model with the company's Profit & Loss (P&L) statement, models were evaluated strictly on their financial impact using an Expected Value (EV) Matrix.

Business Cost Assumptions:

- Cost of Retention Promo (False Positive Penalty): $50

- Average Customer Lifetime Value (False Negative Penalty): $1,531

Findings: 
While a standard Logistic Regression model achieved high statistical accuracy, it missed too many actual churners, resulting in severe financial penalties. 

The Naive Bayes and Random Forest (Balanced) algorithms acted as wider nets. They generated more False Positives (wasted promos) but successfully caught almost every churner.

This resulted in a significantly lower Total Business Loss and generated massive Net Savings compared to a "do-nothing" baseline.


## Key Business Insights

Survival analysis indicates that the highest probability of churn occurs strictly within the first 12 months. Retention budgets should be heavily front-loaded onto new customer onboarding.

Top Churn Drivers

- Month-to-Month Contracts: The lack of a contractual anchor is the primary driver of flight risk.

- Fiber Optic Service: Customers on Fiber Optic are churning at unusually high rates, suggesting a potential structural issue regarding network reliability or competitor pricing.

Top Retention Drivers:

- Long-Term Commitments: Two-year contracts drastically reduce churn probability.
- Customers enrolled in ancillary technical support are significantly less likely to leave.


## The Deliverable 

A Marketing Risk Dashboard

Risk Tier,Probability,Recommended Business Action
- Tier 1: CRITICAL,> 75%,Trigger immediate $50 retention intervention (Discount/Credit).

- Tier 2: MONITOR,40% - 75%,Enroll in automated engagement email sequences; upsell Tech Support.

- Tier 3: SAFE,< 40%,Exclude from promotional discounts to preserve marketing budget.
