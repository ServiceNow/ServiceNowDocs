---
title: Deprecated Continual Improvements dashboard
description: The Continual Improvements dashboard enables an Improvement Process Coordinator or Manager to determine which process to start next, how many initiatives they have underway at a given time, and what the employee participation is.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/continual-improvement-management/continual-improvements-dashboard.html
release: yokohama
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Continual Improvement Management, IT Service Management]
---

# Deprecated Continual Improvements dashboard

The Continual Improvements dashboard enables an Improvement Process Coordinator or Manager to determine which process to start next, how many initiatives they have underway at a given time, and what the employee participation is.

This dashboard is included in the Continual Improvements Management plugin.

\[Omitted image "cimdash.png"\] Alt text: The Overview tab of the Continual Improvements dahsboard, showing employee engagement, total initiatives, the open backlog, and a prioritized list of CIM record according to Spotlight

\[Omitted image "cmdash-outcome-analysis.png"\] Alt text: The Outcome Analysis tab shows how many outcomes were achieved and KPIs completed in the preceding 6 months

## End users and roles

|End user|Required role|
|--------|-------------|
|Improvement Process Coordinator: Needs to verify the status of their initiatives.|sn\_cim.improvement\_coordinator|
|Improvement Process Manager: Must be able to see the state of all improvement processes and assign employees where they are needed.|sn\_cim.improvement\_manager|

## Data visualizations

The Continual Improvements dashboard includes the following visualizations:

|Report Title|Type|Description|
|------------|----|-----------|
|Employee Engagement|Column\[Omitted image "column-icon.png"\] Alt text: Single-score icon|State is not Closed or Cancelled Trended by Created|
|Total Initiatives|Horizontal Bar\[Omitted image "horizontal-bar.png"\] Alt text: Horizontal bar icon|State is not Closed or Cancelled Grouped by State|
|Open Backlog|Single Score\[Omitted image "single-score.png"\] Alt text: Single-score icon|State is not Closed or Cancelled|
|Unassigned|Single Score\[Omitted image "single-score.png"\] Alt text: SIngle-score icon|CIM Coordinator is empty and State is n ot Closed or Cancelled|
|Prioritized List Using Spotlight|List \[Omitted image "scorecard-icon.png"\] Alt text: List icon|Name: Benefit High Query: benefit=high Weight: 50|
|Name: Benefit Low Query: benefit=low Weight: 30|
|Name: Benefit Medium Query: benefit=medium Weight: 40|
|Name: Effort Estimate Extra Large Query: cim\_estimate=4 Weight: 50|
|Name: Effort Estimate Large Query: cim\_estimate=3 Weight: 40|
|Name: Effort Estimate Medium Query: cim\_estimate=2 Weight: 30|
|Name: Effort Estimate Small Query: cim\_estimate=1 Weight: 20|
|Name: Priority 1 Query: priority=1 Weight: 50|
|Name: Priority 2 Query: priority=2 Weight: 40|
|Name: Priority 3 Query: priority=3 Weight: 30|
|Name: Priority 4 Query: priority=4 Weight: 20|
|Name: Priority 5 Query: priority=5 Weight: 10|

