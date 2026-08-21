# Removing Fear Stock from a Growing D2C Portfolio

I led a demand-planning transformation for a portfolio of direct-to-consumer brands. I had identified that customers needed the best products to stay available while the company needed to stop tying cash up in stock that arrived after demand had moved on. I worked with brand leaders, Marketing, Sales, demand planners, Supply Chain, Finance, warehouse teams, and the ERP vendor.

The portfolio trade-off between customer availability and cash sat within my mandate, down to the SKU and purchase-order decision. The transformation spanned demand sensing, campaign planning, supplier lead times, warehouse capacity, planner authority, ERP integration, and Finance's working-capital commitments; improving one function while pushing inventory or stockouts into another did not count as success.

This was a McKinsey project from my July 2014 to June 2016 tenure. Revenue was growing about 30%, but marketing signals reached Operations two weeks late and planners added 15%–20% to orders because their incentives punished stockouts more than excess inventory. The business was not short of forecasts; it was short of a trusted decision shared by cash, service, and growth owners.

## The problem was an information and incentive bullwhip

A campaign plan stayed in Marketing. Sales history reflected demand only after it happened. A planner saw the delayed rise, added a buffer, and placed a larger order through a long supplier lead time. Inventory then arrived after the peak. Each team had acted rationally against its own measure while the portfolio produced an irrational cash result.

I traced one purchase order from campaign plan through demand signal, forecast, safety stock, supplier lead time, warehouse receipt, sale, markdown, and return. That made three causes visible:

- a 14-day delay between leading demand signals and the order decision;
- service incentives that made a 15%–20% manual “fear buffer” locally safe; and
- an ERP without an API, which allowed spreadsheets and definitions to diverge.

## I made working capital a product decision by SKU

I built an Inventory Efficiency Index combining campaign spend, search interest, sales velocity, promotions, on-hand stock, supplier lead time, and forecast uncertainty at SKU level. It produced a recommended order and safety-stock range rather than an unexplained point answer.

Inventory then received an economic job:

- **A products:** high contribution, high demand, or high customer-switching risk; protected service target and daily attention.
- **B products:** predictable core demand; tighter reorder rule and moderate buffer.
- **C products:** slow, uncertain, or aging stock; smaller buys, lower depth, or exit.

Research on supply-process forecasting supports the paired design: forecast error, on-hand inventory, order amplification, and service level need to be evaluated together. A model that lowers stock by creating lost sales is not an inventory improvement.

## The override was designed, not tolerated

Planners could accept the recommendation or override it with a reason: unmodeled promotion, supplier disruption, local trend, missing data, or judgment. A material override required approval and was later compared with actual demand.

This did three jobs. It preserved human responsibility, prevented quiet spreadsheet buffers, and created training data about what the planning feed had missed. Sales received temporary veto protection for A products, while Finance could see the cash cost of each exception.

I launched first in a lower-volatility Home Goods brand. Inventory fell 15% without lost sales in the pilot, which gave the Fashion teams operating evidence rather than a central mandate. A 90-day human-in-the-loop period preceded wider policy automation.

## Four weeks to the holiday buy; six months to an API

The ERP vendor's connector estimate would have missed the buying decision. I built a controlled interim bridge: scheduled Python extraction from validated CSV exports at 5:00 a.m., named analyst ownership, control totals and error handling, then a dashboard refresh before the 9:00 a.m. planning meeting.

I documented the bridge's owner, reconciliation checks, failure response, and retirement condition. It was technical debt with an expiry, used to protect a time-sensitive decision while the durable integration case was proved.

## Scorecard and claim boundaries

| Measure | Baseline | Objective | Result | Measurement |
|---|---:|---:|---:|---|
| Demand-signal latency | 14 days | Daily decision feed | Daily | Timestamp from source availability to planner-ready data |
| Home Goods pilot inventory | Pilot opening level indexed to 100 | Reduce without lost sales | Index 85 | Average inventory before/after, paired with sales and A-item availability |
| Portfolio inventory days | 90 | Release cash while protecting service | 70 | Average inventory divided by the portfolio's stated daily cost basis |
| Working capital | Cash tied in inventory | Release liquidity | $2.5M | Inventory balance reduction attributable to the program scope |
| A-product stockouts | Pre-program rate indexed to 100 | Reduce, not merely preserve | Index 60 | Stockout events for protected A SKUs |
| Inventory turns | 2.5× reported | Improve | 4.0× reported | Separate management-report measure; its scope is not retained and should not be algebraically combined with portfolio inventory days |
| Incremental EBITDA | No accepted program estimate | Quantify operating value | Estimated $1.2M | Modeled contribution from lower stockouts, markdown, and carrying cost; not booked profit claimed as solely mine |

I report the 90-to-70 result as inventory days, not the full cash-conversion cycle, which would also require receivables and payables. I also keep the separately reported turn measure scoped as a management metric because the surviving record does not reconcile its denominator with portfolio inventory days.

## What changed in the operating model

The transformation made one person accountable for the purchase decision while giving every function the evidence relevant to its risk. Marketing supplied leading demand, planners owned the order, Finance saw liquidity, Sales saw protected availability, and overrides improved the next cycle. That is what removed fear stock without making customer service collateral damage.

### Research used

- [Reiner and Fichtinger, demand forecasting with price and market information (2009)](https://doi.org/10.1016/j.ijpe.2008.08.009) — paired evaluation of forecast, service level, inventory, and bullwhip behavior.
- [Tashman, out-of-sample forecast evaluation (2000)](https://doi.org/10.1016/S0169-2070(00)00065-0) — rolling historical validation rather than in-sample fit.
- [Disney and Towill, customer service and bullwhip control (2006)](https://doi.org/10.1016/j.ejor.2005.01.026) — service, stock variance, and order variance as a joint replenishment problem.
- [Role chronology](https://github.com/beastofbayarea/shivam-singh-strategy-consulting/blob/main/shivam-singh-strategy-consulting.pdf) — establishes my McKinsey work period.
