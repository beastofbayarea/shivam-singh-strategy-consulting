# Making vendor data fit Amazon’s regional fulfillment network

Amazon had already designed and activated eight US fulfillment regions in 2022–2023; public reporting showed in-region fulfillment rising from 62% to 76%. My AWS role began in July 2024, so I do not claim that network design or result.

My later program addressed a dependency inside it: vendor catalog/inventory updates took up to 38 hours and 8% contained errors. Nearby inventory is useless if the network cannot trust where it exists.

I ran the recovery with Operations, Sales, Product, Data, regional teams, Engineering, Support, and the technical organization of a seller contributing >$50 million in GMV.

## One update made the architecture undeniable

A vendor changed inventory, price, or imagery. The record moved through FTP, Oracle, manual validation, and batch transforms before listing/placement could act.

I traced timestamps, mutations, rejects, and owners through the full route. The replacement used:

- Kafka on Amazon MSK for replayable ordered events;
- Airflow for visible dependencies/recovery;
- Spark for surge transformation;
- versioned schemas and compatibility;
- real-time quality gates before availability decisions.

Kafka’s distributed log mattered because a defect or changed rule could replay known events from a controlled point rather than reconstruct a missing batch.

## A roadmap conflict became a defect-concentration decision

Product had a broad data-quality roadmap. Sales needed custom integration for the >$50M-GMV seller. Splitting the team would endanger both.

Incident analysis showed image suppression and duplicate product IDs caused ~80% of pain. I cut immediate DQA scope 60% around those two classes and assigned a tiger team to the seller.

The seller firewall blocked image retrieval. The team replaced the route with token-based authentication and a compatible flow. Integration launched two days early.

“Protected >$50M GMV” means existing seller contribution remained active, not incremental sales created.

## Custom edge, common core

Product owned the event/quality contract. Seller teams owned source correction. Data Engineering owned schema, processing, replay, and alerting. Operations decided whether degraded fields could continue. Support categorized incidents so recurrence changed source/rule rather than only response.

The seller-specific edge translated into the common contract; it did not become a second pipeline.

## Result attributable to this program

| Outcome | Baseline → target → recorded result | Measurement |
|---|---|---|
| Vendor signal | up to 38 h → <5 min → <5 min | Source event to accepted downstream signal |
| Error rate | 8% → ≤0.5% → 0.5% | Rejected/corrected records / processed |
| DQA scope | full → retain highest-value defects → 60% smaller immediate scope covering classes behind ~80% incidents | Incident distribution/backlog |
| Seller delivery | at-risk plan → on time → 2 days early | Approved milestone vs release |
| Support | index 100 → reduce recurrence → 75 | Comparable tickets; -25% |
| Annual value | no run rate → >$1M → >$1M | Annualized support/processing savings |
| New commercial value | no contract → paid proof → $200K contract | Executed agreement |
| Existing seller GMV | >$50M at risk → continuity → protected | Contribution remained active; no incrementality |

Public [Amazon Science context](https://www.amazon.science/news-and-features/how-amazon-reworked-its-fulfillment-network-to-meet-customer-demand) explains why timely local availability matters. The [Kafka distributed-log paper](https://cwiki.apache.org/confluence/download/attachments/27822226/Kafka-netdb-06-2011.pdf) and [AWS Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html) ground replay and recovery.

Path diagnosis, architecture choice, defect concentration, roadmap reallocation, the strategic-seller trade-off, common-contract governance, and economics were my decision domain. Engineering implemented; Product controlled the platform; sellers corrected sources; Operations governed degraded use; Sales managed the relationship.

The strategy-consulting contribution was not borrowed credit for regionalization. It was an operating model that made vendor truth timely, accurate, replayable, and governable enough for the regional network to act on it.
