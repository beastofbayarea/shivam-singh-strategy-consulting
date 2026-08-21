# Removing fear stock from a growing D2C portfolio

Revenue was growing ~30%, but demand signals reached Operations two weeks late. Planners added 15–20% to purchase orders because stockouts hurt their targets more than excess stock. Inventory arrived after demand moved on.

At McKinsey, I made the transformation executable across brand leaders, Marketing, Sales, Planning, Supply Chain, Finance, warehouses, and the ERP vendor. Customer availability versus cash became a SKU- and PO-level executive decision, not a contest between functions.

## One purchase order exposed the bullwhip

I traced a PO from campaign plan through signal, forecast, safety stock, lead time, receipt, sale, markdown, and return.

Three failures emerged:

- 14-day information delay;
- incentives that made a 15–20% “fear buffer” locally rational;
- no ERP API, allowing spreadsheets and definitions to diverge.

Marketing, Sales, and Planning were each acting sensibly inside their own measures. The portfolio was creating irrational working-capital outcomes.

## Working capital became a product decision

I built an Inventory Efficiency Index joining campaign spend, search interest, sales velocity, promotions, on-hand stock, supplier lead time, and forecast uncertainty. It returned an order/safety-stock range rather than an unexplained point.

SKUs received economic roles:

- **A:** high contribution, demand, or switching risk—protected service and daily attention.
- **B:** predictable core—tighter reorder, moderate buffer.
- **C:** slow, uncertain, or aging—smaller buys, lower depth, or exit.

A forecast counted as better only if inventory, order amplification, service, markdown, and lost sales improved together. Research on [demand forecasting with market information](https://doi.org/10.1016/j.ijpe.2008.08.009) and [bullwhip/service control](https://doi.org/10.1016/j.ejor.2005.01.026) supported that joint evaluation.

## Overrides became governed evidence

Planners could accept or override for unmodeled promotion, supplier disruption, local trend, missing data, or judgment. Material overrides required approval and later comparison with actual demand.

This preserved responsibility, exposed the cash cost of exceptions, stopped invisible spreadsheet padding, and created evidence about missing signals. Sales received temporary veto protection for A items; Finance could see the liquidity trade.

I piloted Home Goods because volatility was lower. Inventory fell 15% without lost sales. That operating proof earned a 90-day human-in-the-loop expansion to Fashion rather than imposing a central algorithm.

## A controlled bridge protected the holiday buy

The ERP connector estimate missed the decision window. I introduced scheduled Python extraction from validated CSV at 5:00 a.m., named analyst ownership, control totals/error handling, and dashboard refresh before the 9:00 a.m. meeting.

The bridge had a reconciliation rule, failure response, owner, and retirement date. It was explicit technical debt used to protect one buying cycle while proving the durable API case.

## Cash and service outcomes

| Outcome | Baseline → target → recorded result | Measurement |
|---|---|---|
| Signal latency | 14 days → daily → daily | Source availability to planner-ready data |
| Home Goods inventory | index 100 → reduce without lost sales → 85 | Average stock paired with sales and A-item availability |
| Portfolio inventory days | 90 → release cash/protect service → 70 | Average inventory / stated daily cost basis; -22.2% |
| Working capital | baseline tied in stock → release → $2.5M | Inventory-balance reduction within program scope |
| A-item stockouts | index 100 → reduce → 60 | Protected-SKU events; -40% |
| Inventory turns | 2.5× → improve → 4.0× | Separate management measure; denominator does not reconcile with portfolio days |
| EBITDA | no accepted estimate → quantify → ~$1.2M modeled | Lower stockout/markdown/carrying cost; not booked profit solely caused by me |

I call 90→70 inventory days, not cash-conversion cycle, which would also need receivables/payables.

Root-cause tracing, the index and SKU roles, override governance, pilot sequence, interim integration, operating decisions, and Finance bridge were my transformation responsibilities. Marketing supplied demand; planners placed orders; Sales protected service; Finance controlled liquidity; Supply Chain/Warehouses executed.

The transformation removed fear stock by changing information, incentives, authority, and technology together. Cash was released because teams shared one SKU-level decision—not because planners were told to buy less.
