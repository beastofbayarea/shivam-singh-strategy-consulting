# Giving Five Offices One Defensible Financial Record

I led a global finance transformation across six departments and five offices. I had identified that leaders could not trust a shared report when each team defined, matched, and escalated the same financial activity differently. I worked with preparers, controllers, Finance and Operations leaders, IT, Legal and Compliance, local offices, more than two hundred users, and the SAP and Tableau partners.

## The first deliverable was not software

During my D. E. Shaw experience from July 2016 to December 2019, I audited historical reports, reconciliation breaks, source formats, spreadsheet rules, email queues, ownership, control evidence, and team effort. The baseline showed a 20% reconciliation-error rate and no common way to see the age, amount, or owner of an exception.

My remit was the operating-model reset across six departments, five offices, and more than 200 users: one financial definition, one exception object, one evidence trail, and one signed retirement decision for every legacy route. That made the work an enterprise control transformation with systems, process, adoption, vendor economics, and close authority in scope—not an SAP installation.

Finance owners defined the economic meaning of each legacy field. IT mapped it into a canonical model. Control owners reconciled totals and approved the mapping in parallel runs. That decision order mattered: an integration can move a field perfectly while changing its accounting meaning.

COSO supplied the broad control logic—risk, control activity, information, communication, and monitoring. BCBS 239, although written for bank risk data rather than this exact process, reinforced the need for accurate, complete, timely, adaptable data with accountable ownership.

## The operating model used exceptions as the unit of work

The target flow was:

`source entry → canonical field and rule → SAP matching → matched ledger or named exception → evidence → controller approval → Tableau control view`

High-confidence items were matched automatically. Unmatched or ambiguous items carried amount, source, reason, materiality, owner, age, evidence, and resolution. Repeated breaks were not simply closed faster; they became candidates for source-data, policy, or matching-rule correction.

SAP's current intercompany matching documentation illustrates the same control pattern: exact matching, auto-assignment, exception assignment, reason codes, manual adjustment, and role-specific authorization. I used those capabilities to keep judgment visible instead of forcing false agreement for the sake of automation.

Tableau showed close progress, exception age, error source, workload, and recurring root causes. A preparer needed to resolve work, a reviewer needed to inspect evidence, and an executive needed to see control health. Each role received a different view and training path.

## A small pilot earned the right to transform the close

A non-critical department ran in parallel with the legacy process. It improved errors and speed by about 10% in the first month, which helped secure CFO and COO sponsorship and an additional $500,000 of program funding.

I then moved through lower-risk offices before the highest-impact Finance teams. Every wave required:

1. source-to-target totals reconciled;
2. exception ownership working;
3. role training and live support complete;
4. parallel output inside the approved threshold; and
5. a signed decision to retire the legacy route.

This protected live reporting while local champions surfaced regional requirements. The standard could change only through documented governance; local teams could not quietly fork it back into spreadsheets.

I also negotiated a 15% SAP license discount through the multi-year commercial agreement and case-study participation. Vendor economics and support milestones were part of the transformation case, not procurement after the architecture was fixed.

## What the program delivered

| Outcome | Baseline | Target | Result | Measurement |
|---|---:|---:|---:|---|
| Reconciliation error rate | 20% | At or below 0.5% in sustained operation | 5% in Q1; later reported near zero | Exceptions divided by reconciled items for the defined run; exact final rate not retained |
| Implementation duration | 120-day program plan | 15% faster | 102 days | Calendar days from approved start to program completion; **not** recurring close time |
| Exception resolution | Baseline elapsed time | Improve | 25% faster | Median age from exception creation to approved resolution |
| Adoption | Department spreadsheets | At least 95% | 95% within 3 months across 200+ users | Required-role users completing governed work in SAP/Tableau |
| Team capacity | Existing reconciliation effort | Release for higher-value work | 25% released | Time study of recurring reconciliation activity |
| Annual operating savings | 0 | Cover transformation economics | $1.5M | Annualized avoided rework and capacity cost |
| SAP license price | Quoted price index 100 | Improve commercial terms | Index 85 | Executed contract versus initial quote |

The source record also labels first-year return as 300%, but it does not retain the full program cost or the calculation convention. I omit that ratio rather than mix a gross benefit multiple with standard net-return arithmetic. The $1.5 million annual savings is the claim supported by the retained operating model.

Post-implementation compliance reviews passed. I treat that as evidence that the process and controls operated, not as proof that future periods were risk-free.

## The transformation in one sentence

SAP and Tableau made the change scalable, but the durable asset was one financial definition, one visible exception queue, one accountable reviewer, and evidence strong enough to turn off the old process.

### Control and product references

1. [COSO, Internal Control—Integrated Framework](https://www.coso.org/guidance-on-ic/pages/default.aspx) — enterprise control and monitoring structure.
2. [Basel Committee, BCBS 239 (2013)](https://www.bis.org/publ/bcbs239.htm) — accuracy, completeness, timeliness, adaptability, and data governance.
3. [SAP S/4HANA Intercompany Matching and Reconciliation](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/651d8af3ea974ad1a4d74449122c620e/d6e1f222780744268eb4cbcb836f6b92.html) — matching architecture and governed reconciliation cases.
4. [SAP authorization objects for matching and reconciliation](https://help.sap.com/docs/sap_s4hana_on-premise/651d8af3ea974ad1a4d74449122c620e/288004c6aac34649bcdbc939f7578db2.html) — role separation, reason codes, assignments, and close authority.
5. [Role chronology](https://github.com/beastofbayarea/shivam-singh-strategy-consulting/blob/main/shivam-singh-strategy-consulting.pdf) — establishes my D. E. Shaw work period.
