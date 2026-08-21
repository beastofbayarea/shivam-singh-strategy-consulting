# Giving five offices one defensible financial record

Six departments and five offices were reconciling the same financial activity through different definitions, spreadsheet rules, and email queues. Baseline reconciliation error was 20%; exceptions had no common owner, age, or materiality.

During my D. E. Shaw experience, I orchestrated the enterprise control transformation across preparers, controllers, Finance/Operations, IT, Legal/Compliance, five offices, 200+ users, and SAP/Tableau partners.

This was not an SAP implementation. The deliverable was one financial definition, one exception object, one evidence trail, and a signed retirement decision for every legacy route.

## Meaning preceded mapping

Finance owners defined the economic meaning of each field. IT mapped it to the canonical model. Control owners reconciled totals and approved in parallel runs.

That sequence prevented a technically perfect integration from silently changing accounting meaning.

COSO supplied broad control/monitoring structure. [BCBS 239](https://www.bis.org/publ/bcbs239.htm), although aimed at bank risk data, reinforced accountable, accurate, complete, timely, adaptable information.

## The exception became the unit of work

**source → canonical field/rule → SAP match → ledger or exception → evidence → controller approval → Tableau control view**

High-confidence items matched automatically. Every exception carried amount, source, reason, materiality, owner, age, evidence, and resolution.

Repeated breaks were not merely closed faster; they entered the backlog for source-data, policy, or rule repair. SAP’s [intercompany matching pattern](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/651d8af3ea974ad1a4d74449122c620e/d6e1f222780744268eb4cbcb836f6b92.html) illustrates exact matching, auto-assignment, reasons, adjustment, and role authorization.

Tableau served three different decisions: preparers resolved work, reviewers inspected proof, executives saw close health and recurring causes.

## A non-critical pilot earned authority over the close

The first department ran in parallel with legacy and improved error/speed ~10% in month one. That evidence secured CFO/COO sponsorship and another $500,000.

Rollout moved through lower-risk offices before high-impact Finance. Each wave required:

1. reconciled source-to-target totals;
2. functioning exception ownership;
3. role training/live support;
4. parallel output within threshold;
5. signed legacy retirement.

Local champions surfaced regional requirements. Standards changed only through governance; no office could quietly recreate spreadsheets.

I also negotiated a 15% SAP license discount through multi-year terms and case-study participation, making vendor economics part of transformation design.

## Result

| Control outcome | Baseline → target → recorded result | Measurement |
|---|---|---|
| Error rate | 20% → ≤0.5% sustained → 5% Q1, later near zero reported | Exceptions / reconciled items; exact final rate absent |
| Program duration | 120 days → 15% faster → 102 days | Approved start to completion, not recurring close time |
| Exception resolution | baseline elapsed → faster → 25% faster | Median create-to-approved resolution |
| Adoption | departmental spreadsheets → ≥95% → 95% within 3 months / 200+ users | Required-role users completing governed SAP/Tableau work |
| Capacity | baseline effort → release → 25% | Recurring reconciliation time study |
| Annual operating value | 0 → cover economics → $1.5M | Annualized rework/capacity saving |
| License price | quote index 100 → improve → 85 | Executed contract; -15% |

A “300% first-year return” cannot be reconstructed because full cost/formula are missing, so I exclude it. Post-implementation reviews passed; that proves observed control operation, not future risk absence.

The definition-and-exception operating model, pilot, wave gates, adoption, vendor economics, measurement, and legacy-retirement governance were the parts I directed. Finance defined meaning; IT implemented; Controls approved; local teams adopted; vendors supplied platforms.

The durable asset was the authority to turn off the old process. SAP and Tableau scaled the workflow, but one definition, visible exception, accountable reviewer, and accepted evidence made the financial record defensible.
