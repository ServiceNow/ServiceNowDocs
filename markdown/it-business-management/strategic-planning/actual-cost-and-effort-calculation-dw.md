---
title: Actual cost and effort calculation for a demand and demand task
description: Actual cost and effort represent the realized cost and time spent working on demands and demand tasks during a specific time period. These values are calculated based on approved time cards and hourly rates for resources.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Actual cost and effort calculation for a demand and demand task

Actual cost and effort represent the realized cost and time spent working on demands and demand tasks during a specific time period. These values are calculated based on approved time cards and hourly rates for resources.

## Overview of calculation

Working on demands and demand tasks involves cost and time that add to the overall expenditure of converting a demand to a product, feature, or enhancement. Demand managers must track the actual cost and effort incurred in assessment and planning activities.

-   The actual cost is calculated by multiplying the hours reported in the time card by the hourly rate of the resource.
-   The actual effort for a demand task is calculated based on the hours reported in the time card.
-   The actual effort and cost for demand tasks roll up to calculate the actual effort and cost for the demand.

## Hourly rate calculation

The hourly rate for calculating actual cost is derived in the following order:

1.  If a rate model is associated with the demand, the actual cost is calculated based on the hourly rate defined in the rate model.
2.  If a rate model is absent or if an hourly rate isn’t found in the rate model, the hourly rate is derived from the default labor rate.
3.  If an hourly rate isn’t found in the default labor rate, the hourly rate is derived from the default system property.

## Resource assignments and Time cards

Don’t create resource assignments for allocating resources or groups to a demand task. Resource assignments created in the demand are used for resource estimation of the work entity created from the demand. These resource assignments automatically move to the resulting work entity when a demand is qualified and converted.

When you submit a time card for a demand, the actual effort and cost aren’t reflected in the resource assignment. Resource assignments aren't associated with the demand by default. The actual cost and actual effort remain with the demand and aren't transferred to the created projects, even if you manually associate a resource assignment.

If a resource spends extra hours working on a demand that aren’t associated with demand tasks, this time must also be recorded. The resource submits the time card for recording extra hours using the Time Sheet Portal. This extra cost and effort is added to the demand but isn’t reflected in the actual cost and effort for the demand tasks.

## Demand-level calculations

The actual cost and actual effort for the demand are calculated as follows:

-   Demand Actual Cost = actual cost of all demand tasks + actual cost of extra activities
-   Demand Actual Effort = actual effort of all demand tasks + actual effort of extra activities

If a demand has no task or assigned resource, you can capture the actual cost by submitting a time card against the demand. Once the time card is approved, an expense line is created on the demand. The expense line is processed and the actual cost of work for that time card rolls up to the demand in the Demand Actual Cost column.

This example demonstrates actual cost and effort calculation for demand tasks and rollup to the demand.

Scenario setup - For demand D1, the demand manager creates three demand tasks \(DT1, DT2, and DT3\) and assigns resources R1, R2, and R3 to each task respectively.

|Resource|Hourly rate in the rate model|Hourly rate in the default labor rate|Hourly rate in the system property|
|--------|-----------------------------|-------------------------------------|----------------------------------|
|R1|$200|$150|$50|
|R2|$250|$200|$50|
|R3|$150|$100|$50|

Each resource spends eight hours on the assigned demand task and submits a time card.

|Actuals|Demand task DT1|Demand task DT2|Demand task DT3|
|-------|---------------|---------------|---------------|
|Actual effort|8 hours|8 hours|8 hours|
|Actual cost|200 \* 8 = $1600|250 \* 8 = $2000|150 \* 8 = $1200|

Demand rollup:

-   Demand Actual Cost = $4,800
-   Demand Actual Effort = 24 hours

|Actuals|Demand task DT1|Demand task DT2|Demand task DT3|
|-------|---------------|---------------|---------------|
|Actual effort|8 hours|8 hours|8 hours|
|Actual cost|150 \* 8 = $1200|200 \* 8 = $1600|100 \* 8 = $800|

Demand rollup:

-   Demand Actual Cost = $3,600
-   Demand Actual Effort = 24 hours

|Actuals|Demand task DT1|Demand task DT2|Demand task DT3|
|-------|---------------|---------------|---------------|
|Actual effort|8 hours|8 hours|8 hours|
|Actual cost|50 \* 8 = $400|50 \* 8 = $400|50 \* 8 = $400|

Demand rollup:

-   Demand Actual Cost = $1,200
-   Demand Actual Effort = 24 hours

