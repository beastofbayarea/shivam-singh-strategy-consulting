# Releasing Working Capital Without Creating D2C Stockouts

I led this demand-planning transformation during my [McKinsey experience from July 2014 to June 2016](https://github.com/beastofbayarea/shivam-singh-strategy-consulting/blob/main/shivam-singh-strategy-consulting.pdf).

The brands were growing, but cash was accumulating in inventory. Marketing signals reached Operations as much as two weeks late, planners added 15%–20% buffers because they did not trust the forecast, and Finance, Sales, and Supply Chain optimized different measures. The ERP also had no API before a critical holiday purchase decision.

My assignment was to release working capital while protecting the products and service levels that created the revenue.

## I mapped the decision, not only the stock

I followed the purchase-order value stream from campaign plan and demand signal through forecast, planner decision, supplier lead time, warehouse receipt, and customer sale. That exposed where information aged, where a buffer entered, and which team absorbed the consequence.

I then joined advertising, search, sales, stock, lead-time, and promotion signals in a daily SKU-level planning feed. The goal was not a more impressive forecast; it was a better purchase decision with enough evidence for a planner to understand and challenge it.

Tashman's work on out-of-sample forecast evaluation influenced the validation design. I tested performance over rolling historical windows rather than judge the model on the same periods used to tune it.

## Inventory had different economic jobs

A blanket 22% reduction would have released cash quickly and damaged availability. I classified inventory by economic role and protected service targets for high-value A-class items. Slow, uncertain, seasonal, and strategic products received different policies.

The scorecard paired inventory days and working capital with stockouts, availability, turns, and contribution. No function could claim success by improving its own measure while transferring the cost elsewhere.

## I kept human judgment observable

Planners could override the recommendation, but they selected a reason. Those reason codes made judgment part of the learning loop: a promotion not represented in the feed, a supplier issue, a local demand change, or simple disagreement could be evaluated later.

I piloted the process in a lower-volatility brand before expanding. World Bank impact-evaluation guidance influenced the comparison design so observed inventory and service changes could be evaluated against a credible baseline rather than attributed automatically to the new process.

## The ERP constraint did not stop the decision

Waiting for a full integration would have missed the holiday buy. I built a deliberate CSV bridge with validation, ownership, and a documented replacement path. It was a temporary operating control, not an accidental permanent architecture.

The bridge delivered the daily decision feed in time and created evidence for the durable integration investment.

## What changed

- Inventory days fell from 90 to 70.
- The program released $2.5 million in working capital.
- Inventory turns improved from 2.5 to 4.0 times.
- A-class stockouts declined 40%.
- Incremental EBITDA reached an estimated $1.2 million.

I report the 90-to-70 movement specifically as inventory days, not as the broader cash-conversion cycle.

## The transformation lesson

Working capital improves sustainably when the organization trusts the demand decision. I combine current signals, economic segmentation, visible overrides, and paired liquidity-and-service measures. That allows the business to remove fear inventory without treating availability as collateral damage.

## External foundations

These sources supplied the primary forecast-validation and causal-measurement methodology. My resume establishes employment chronology only.

| Source | How I applied it |
|---|---|
| [Tashman — Out-of-sample tests of forecasting accuracy (2000)](https://www.sciencedirect.com/science/article/pii/S0169207000000650) | I used its rolling out-of-sample principles to validate demand performance beyond the model-fitting period. |
| [World Bank — Impact Evaluation in Practice](https://www.worldbank.org/en/programs/sief-trust-fund/publication/impact-evaluation-in-practice) | I used its counterfactual principles to evaluate inventory and service changes against a credible baseline. |
