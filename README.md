# Unicorn Classifier

## Overview
Unicorn Classifier is a random forest classifier model that determines the appropriate funding status (Private Equity, Late Stage Venture, IPO, M&A, or Early Stage Venture) of a unicorn company. The data used was sourced from [The Crunchbase Unicorn Board](https://news.crunchbase.com/unicorn-company-list/).

## Identifying undervaluation
The model also allows us to determine if a unicorn company is undervalued or overvalued by comparing its last funding type (Series A-J, Grant, Non-equity Assistance, Post-IPO Secondary, Convertible Note, Undisclosed, Equity Crowdfunding, Debt Financing, Private Equity, Secondary Market, Corporate Round, Seed, Post-IPO Debt, Post-IPO Equity, and Initial Coin Offering) to its funding status model classification.

For instance, if a company's last funding type is Series A and our model classifies its funding status as a Late Stage Venture or IPO, we would conclude that the companty is undervalued.

## Data dictionary
Predictor variables

| Variable | Type | Description |
| ----------- | ----------- | ----------- |
| Total_Equity_Funding | Numerical | Total funding amount raised across all Funding Rounds excluding debt |
| Valuation | Numerical | Valuation of company |
| Last_Funding_Amount | Numerical | Amount of most recent Funding Round |
| Number_Of_Acquisitions | Numerical | Total number of Acquisitions |
| CB_Rank | Numerical | (Crunchbase rank) Algorithmic rank assigned to the top 100,000 most active Companies |

<br>

Dependent variable

| Variable | Type | Description |
| ----------- | ----------- | ----------- |
| Funding_Status | Categorical | An organization's most recent funding status (e.g. Early Stage Venture, Late Stage Venture, M&A) |

<br>

Unused variables (used to find patterns post-classification)

| Variable | Type | Description |
| ----------- | ----------- | ----------- |
| Valuation_Date | DateTime | Date the company was given the valuation |
| Industries | Multi-Categorical | Pertaining industries of the company |
| Top_5_Investors | Multi-Categorical | The top 5 investors with investments in this company, ordered by Crunchbase Rank |
| Founded_Date | DateTime | Date the organization was founded |
| Last_Funding_Date | DateTime | Date of most recent Funding Round |
| Last_Funding_Type | Categorical | Last funding round type (e.g. Seed, Series A, Private Equity) |
