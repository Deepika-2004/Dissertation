# Autoregressive Models for High-Frequency Financial Data

This project looks at **how financial market activity changes over time** by modelling the time between consecutive market events, known as **financial durations**.

The main focus is on **Autoregressive Conditional Duration (ACD) models**, which are designed to capture dependence and clustering in high-frequency event times.

## What I looked at

I worked with three different financial markets:

* **GBP/USD** – foreign exchange
* **BTCUSDT** – cryptocurrency
* **NVDA** – US equity

The datasets contain millions of high-frequency events, which made data preparation an important part of the project.

The analysis covers:

* Constructing reliable event durations from high-frequency timestamps
* Handling simultaneous and near-simultaneous events
* Adjusting for intraday trading patterns
* Fitting different ACD models
* Comparing linear ACD, Weibull ACD and log-ACD models
* Examining persistence and residual dependence
* Comparing model forecasts with an out-of-sample test period

## Main finding

One of the interesting results was that some linear ACD models produced persistence estimates above 1, particularly for BTCUSDT and NVDA.

Rather than treating this immediately as a financial finding, I investigated whether it was related to the way very close events were constructed. The sensitivity analysis showed that **near-simultaneous events can have a substantial effect on estimated persistence**.

This highlighted an important point from the project:

> **In high-frequency financial modelling, how the events are constructed can be just as important as the model used to analyse them.**

## Tools

* **R**
* `ACDm`
* Statistical modelling and diagnostic analysis

## Data

The project uses high-frequency data from:

* Dukascopy — GBP/USD
* Binance — BTCUSDT
* Databento — NVDA

## Project structure

```text
├── code_D(2).Rmd       # Main analysis and modelling code
├── figures/            # Generated figures
├── results/            # Model results and diagnostics
└── README.md
```

## About the project

This project was completed as part of my **MSc Data Science & Analytics dissertation at the University of Leeds**.

**Dissertation:** *Autoregressive Models for High-Frequency Financial Data*
