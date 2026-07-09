---
title: Product non-conformance use case
description: Use case scenarios demonstrate when and how to use the Product non-conformance application to create and resolve the product non-conformance issue. It provides practical examples of common product non-conformance situations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-product-non-conformance-use-case.html
release: australia
topic_type: concept
last_updated: "2026-03-18"
reading_time_minutes: 1
breadcrumb: [Quality management, Explore, Manufacturing Commercial Operations]
---

# Product non-conformance use case

Use case scenarios demonstrate when and how to use the Product non-conformance application to create and resolve the product non-conformance issue. It provides practical examples of common product non-conformance situations.

## Scenario: Airbag Sensor Defect escalation

Alectri receives multiple dealer reports of unexpected airbag warning lights in 2024 Voltar VS vehicles. The quality team must triage, contain affected inventory, and escalate to deeper investigation — while facing these challenges:

The quality team encounter some challenges:

-   Ownership: no clear ownership for initial triage and assignment
-   Visibility across network: difficulty identifying all impacted vehicles across the dealer network
-   Cost tracking: lack of visibility into containment costs and actions per vehicle
-   Asset linkage: no structured link between containment to specific assets
-   Escalation path: unclear escalation path to broader quality investigations

## Solution

Triage and Assignment: James, the quality triager, receives the non-conformance case.

1.  Triage and Assign: Quality triager James reviews the dealer report and assigns the case to Sophie \(PNCC Resolver\) with clear accountability.
2.  Investigate and Document: Sophie reviews case details, confirms the issue pattern, and identifies 47 impacted vehicles across 12 dealerships.
3.  Contain and Track: Sophie creates a containment action \(disable system, provide loaner vehicles\) and links it to each impacted asset. She records containment costs \(quarantine, diagnostics, loaner fees\).
4.  Correct and Escalate: Sophie applies corrective actions \(sensor replacement, firmware updates\), closes the case, and escalates to Quality Investigation for cross-functional pattern analysis.

The [Product non-conformance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-product-non-conformances.md) workspace provides guided setup to resolve the issue.

## Benefits

Compare the impact of using the Product Non-Conformance application.

|Without MCO|With MCO Non-Conformance|
|-----------|------------------------|
|Unstructured triage; unclear ownership|Guided assignment and accountability from day one|
|Manual tracking of affected vehicles; high error risk|Asset-level traceability with systematic containment linking|
|Cost visibility scattered across systems|Centralized expense tracking per asset and action|
|Ad hoc escalation paths; delayed investigations|Structured escalation to quality investigations with full context|

## Outcome

James triages with clear ownership. Sophie resolves the airbag issue across 47 impacted vehicles — documenting containment, repairs, firmware updates, and costs with full audit trail. The structured workflow enables rapid response while the escalation path ensures broader quality patterns are investigated systematically.

**Related topics**  


[Report an issue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-report-an-issue.md)

[Product non-conformance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-product-non-conformances.md)

