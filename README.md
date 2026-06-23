# QuantPath — Portfolio Optimization Tool

A quantitative portfolio construction tool built on Modern Portfolio Theory. 
Live demo: https://decision-path-forge.lovable.app

## What It Does

QuantPath screens the S&P 500 universe, selects securities using a 
momentum-volatility-liquidity scoring model, and constructs an 
optimal portfolio using Max Sharpe optimization. Risk is modeled 
using Monte Carlo simulation across 10,000 GBM paths.

## Methodology

**Security Selection**
- Universe: S&P 500 constituents
- Liquidity filter: minimum $5M average daily dollar volume
- Scoring: composite rank across momentum (50%), 
  volatility penalty (30%), and liquidity (20%)
- Top 30 securities advance to optimization

**Portfolio Optimization**
- Covariance estimation: Ledoit-Wolf shrinkage 
  (reduces estimation error in small samples)
- Objective: maximize Sharpe ratio subject to 
  long-only, fully-invested constraints
- Solver: SLSQP via PyPortfolioOpt

**Risk Analysis**
- Monte Carlo: 10,000-path GBM simulation
- Stress scenarios: Bull, Base, High Inflation, 
  Correlation Crisis, Volatility Spike, Rate Shock
- Benchmark comparison: S&P 500, Equal Weight, 60/40

## Stack

- Python (Google Colab)
- PyPortfolioOpt — optimization engine
- yfinance — market data
- NumPy, Pandas, Matplotlib
- React frontend deployed via Lovable

## Background

Built to explore how systematic, quantitative methods 
compare to discretionary portfolio construction. 
Separately applied a simplified version of this 
optimization framework in a statewide investing 
competition (~1,600 participants).

## College Admissions Calculator

`CollegeAdmissions.ipynb` is a standalone notebook, inspired by 
admissions-consulting products like John Morganelli's "BluePrint" 
(Ivy Tutors Network). It has two parts:

- **Chance Calculator** — estimates admission probability across a 
  list of colleges from a student's GPA, test scores, course rigor, 
  extracurricular strength, and hooks (legacy, first-gen, recruited 
  athlete), sorting schools into Reach / Target / Likely / Safety.
- **BluePrint-style Report Generator** — takes an intake questionnaire 
  (interests, background, goals, grade level) and produces a 
  personalized report: application theme, suggested majors, activities, 
  project ideas, summer programs, essay prompts, a financial-aid 
  overview, and a year-by-year timeline.

College stats are illustrative approximations of public Common Data 
Set figures, not live data — refresh `COLLEGE_DB` before relying on it 
for real decisions.
