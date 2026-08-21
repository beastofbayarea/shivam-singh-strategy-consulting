# Making Vendor Data Fit Amazon's Regional Fulfillment Network

I led a vendor-data and roadmap recovery inside Amazon's regional fulfillment network. I had identified that customers and sellers could not benefit from nearby inventory when vendor updates arrived late or wrong, and a major seller needed an integration the existing roadmap could not absorb. I worked with Operations, Sales, Product, Data, regional delivery teams, engineers, support, and the seller's technical team.

## Where my work begins—and where it does not

Amazon publicly designed and activated its eight U.S. fulfillment regions during 2022 and 2023. Amazon Science reports that in-region fulfillment rose from 62% to 76% during that earlier transformation. My AWS role began in July 2024, so I do not claim to have originated the eight-region strategy or produced the 62%→76% result.

My later project addressed an operating dependency inside that model: vendor catalog and inventory changes took as long as 38 hours to become usable and 8% contained errors. Regional placement depends on current local availability; stale data can block a customer promise as completely as a physical capacity failure.

## I traced one update until the architecture became undeniable

A vendor changed inventory, price, or an image. The record moved through FTP, Oracle, manual validation, and batch transformation before listing and placement systems could use it. I followed timestamps, transformations, rejects, and ownership across the path instead of accepting “slow vendor onboarding” as the diagnosis.

The replacement used:

- Kafka on Amazon MSK for a replayable vendor-event stream;
- Airflow for visible dependencies and recovery;
- Spark for distributed transformation during large surges;
- versioned schemas and compatibility rules; and
- real-time quality checks before a record could influence availability.

The Kafka distributed-log design matters here because a consumer can replay an ordered event history after a defect or rule change. That converted recovery from reconstructing a missing batch into reprocessing known events from a controlled point.

## A roadmap conflict became a defect-concentration decision

Product had committed to a broad data-quality product while Sales needed a custom integration for a seller contributing more than $50 million in GMV. Splitting the team evenly would have endangered both.

I analyzed vendor incidents and found that image suppression and duplicate product identifiers caused about 80% of the pain. I cut the immediate quality roadmap by 60% around those two failures and released a tiger team for the seller integration. The seller's firewall blocked image retrieval, so the team replaced that path with token-based authentication and a compatible retrieval flow.

The integration launched two days early. “Protected $50 million in GMV” means the existing seller contribution at risk was retained; it is not $50 million of incremental sales created by the project.

## Decision rights after launch

Product owned the common event and quality contract. Seller teams owned source corrections. Data Engineering owned processing, schema compatibility, replay, and alerting. Operations decided whether a degraded field could continue. Support categorized incidents so recurring tickets changed a rule or source, not only the next response.

This kept a one-off integration from fragmenting the platform. The custom edge translated into the common contract; it did not become a second pipeline.

## Results attributable to this project

| Measure | Baseline | Target | Result | Measurement |
|---|---:|---:|---:|---|
| Vendor-signal latency | Up to 38 hours | Under 5 minutes | Under 5 minutes | Source-event time to accepted downstream signal |
| Data error rate | 8% | At or below 0.5% | 0.5% | Rejected or corrected records divided by processed records |
| DQA launch scope | Full roadmap | Preserve highest-value defect coverage | 60% smaller immediate scope, retaining the two classes behind ~80% of incidents | Incident distribution and approved backlog |
| Seller integration | At-risk schedule | Protect seller relationship and ship on time | 2 days early | Approved milestone versus production release |
| Support demand | Ticket baseline indexed to 100 | Reduce recurring defects | Index 75 | Comparable support tickets after launch |
| Annual savings | No accepted run rate | Exceed $1M | More than $1M | Annualized support and processing savings |
| Commercial result | No new contract | Convert proof into paid value | $200K contract | Executed commercial agreement |
| Existing seller GMV at risk | More than $50M | Protect continuity | Protected | Seller contribution remained active; no incremental GMV attribution |

## Strategic importance without borrowed credit

Public Amazon evidence explains why this dependency mattered. Regionalization shortened distance and reduced network complexity; later Amazon reporting tied it to faster delivery and lower cost to serve. My project's contribution was narrower and defensible: make vendor data timely, accurate, recoverable, and supportable enough for a regional network to use.

### External context and technical grounding

- [Amazon 2022 shareholder letter](https://ir.aboutamazon.com/files/doc_downloads/AnnualMeetingMaterials/2023/2022-Shareholder-Letter.pdf) — primary description of the national-to-eight-region redesign.
- [Amazon Science, regional fulfillment at 62%→76% (2023)](https://www.amazon.science/news-and-features/how-amazon-reworked-its-fulfillment-network-to-meet-customer-demand) — public timing and result used to bound, not inflate, my role.
- [Amazon 2023 Sustainability Report](https://sustainability.aboutamazon.com/2023-sustainability-report.pdf) — external record of eight-region operations and additional in-region units.
- [Kreps, Narkhede, and Rao, Kafka distributed log (2011)](https://cwiki.apache.org/confluence/download/attachments/27822226/Kafka-netdb-06-2011.pdf) — event ordering, partitioning, consumption, and replay model.
- [AWS Well-Architected Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html) — failure isolation, observability, and recovery method.
- [Role chronology](https://github.com/beastofbayarea/shivam-singh-strategy-consulting/blob/main/shivam-singh-strategy-consulting.pdf) — establishes my AWS tenure beginning in July 2024.
