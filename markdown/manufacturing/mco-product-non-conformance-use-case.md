---
title: Product non-conformance use case
description: Use case scenarios demonstrate when and how to use the Product non-conformance application to create and resolve the product non-conformance issue. It provides practical examples of common product non-conformance situations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-product-non-conformance-use-case.html
release: australia
topic_type: concept
last_updated: "2026-03-18"
reading_time_minutes: 2
breadcrumb: [Quality issue management, Explore, Manufacturing Commercial Operations]
---

# Product non-conformance use case

Use case scenarios demonstrate when and how to use the Product non-conformance application to create and resolve the product non-conformance issue. It provides practical examples of common product non-conformance situations.

## Use Case 1: Airbag Sensor Defect Non-Conformance Management

Scenario

Alectri receives multiple dealer reports of airbag warning lights activating unexpectedly in 2024 Voltar VS vehicles. The non-conformance case requires immediate triage, containment of affected vehicles, and potential escalation to a quality investigation.

The quality team encounter some challenges:

-   No clear ownership for triaging and assigning the case
-   Difficulty identifying all impacted vehicles across the dealer network
-   Missing visibility into containment costs and actions according to vehicle
-   No structured process for linking containment actions to specific assets
-   Unclear escalation path to broader quality investigations
-   Limited traceability of resolution activities

Solution

Triage and Assignment: James, the quality triager, receives the non-conformance case.

1.  Reviews the initial dealer report describing unexpected airbag warning lights in 2024 Voltar VS vehicles
2.  Sets assignment group to Quality Non-Conformance Resolvers and assigns to Sophie \(PNCC Resolver\)
3.  Creates tasks for field engineers to inspect affected vehicles, collect diagnostic data, and validate airbag sensor readings

The case moves from Reported to Owned status with clear accountability.

Non-Conformance Resolution: Sophie investigates and resolves the issue:

1.  Opens the case and reviews product details \(2024 Voltar VS, VIN ranges, production dates\), dealer reports, and diagnostic attachments
2.  Marks the initial review step complete after confirming the issue pattern
3.  Identifies 47 impacted vehicles across 12 dealerships and creates a containment action: "Disable airbag system and provide loaner vehicles until repair"
4.  Links the containment action to each of the 47 vehicles through impacted asset actions, tracking which vehicle received containment and when
5.  Adds additional impacted assets as field reports come in
6.  Creates containment expense lines for loaner vehicles and diagnostic work
7.  Adds resolution code "Sensor calibration failure requires investigation"
8.  Creates expense lines to capture costs associated with containment activities, including vehicle quarantine logistics and diagnostic inspections
9.  Adds corrective actions:
    -   Replaces the faulty airbag sensor on all 47 confirmed vehicles with a validated replacement part
    -   Updates sensor firmware on all replaced units to the latest calibration version
10. Adds resolution code "Sensor calibration failure — corrective action applied"
11. Closes containment activities
12. Reviews closure readiness

Recognizing a pattern affecting multiple vehicles and potential safety implications, Sophie escalates by creating a Quality Investigation for deeper cross-functional analysis.

The [Product non-conformance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-product-non-conformances.md) workspace provides guided setup to resolve the issue.

Benefits

-   Clear accountability: Structured ownership from triage through resolution
-   Targeted containment: Affected inventory quarantined before customer delivery, minimizing risk
-   Corrective action tracking: Sensor replacement and firmware updates recorded against each impacted vehicle
-   Asset-level traceability: Links between containment actions and specific vehicles
-   Cost visibility: Expense tracking for containment activities
-   Structured escalation: Direct path from non-conformance to quality investigation
-   Complete documentation: Resolution codes and closure readiness verify thoroughness

Outcome

James triages and assigns the non-conformance case with clear ownership. Sophie resolves the issue with complete traceability across 47 impacted vehicles — documenting containment actions, corrective repairs, firmware updates, and associated costs. The structured workflow enables rapid response while maintaining accountability at every step. Recognizing broader impact patterns, Sophie escalates the issue to a quality investigation, enabling deeper cross-functional analysis to help prevent recurrence.

**Related topics**  


[Report an issue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-report-an-issue.md)

[Product non-conformance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-product-non-conformances.md)

