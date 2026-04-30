---
title: Actual cost and effort calculation for a demand and demand task
description: The actual cost and effort are realized cost incurred and time spent for the work performed on a demand and demand task during a specific time period. Actual cost and effort are calculated based on the approved time cards and hourly rate for the resources and vary based on how the hourly rate for the resource is derived.
locale: en-US
release: yokohama
product: Demand Management
classification: demand-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Reference, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Actual cost and effort calculation for a demand and demand task

The actual cost and effort are realized cost incurred and time spent for the work performed on a demand and demand task during a specific time period. Actual cost and effort are calculated based on the approved time cards and hourly rate for the resources and vary based on how the hourly rate for the resource is derived.

Working on a demand task and demand involves cost and time, which add to the overall expenditure of converting a demand to a product, feature, or enhancement. Demand managers therefore need to know the actual cost and effort incurred in assessing and planning activities for a demand. The calculation for actual cost is derived by multiplying the hours reported in the time card by the hourly rate of the resource. The actual effort for a demand task is calculated based on the hours reported in the time card.

The actual effort and cost for the demand tasks are then rolled up for calculating actual effort and cost for the demand. The calculation of the actual cost and hourly rate for a resource is derived as follows:

-   If a rate model is associated with the demand, the actual cost is calculated based on the hourly rate defined in the rate model.
-   If a rate model is absent or if an hourly rate is not found in the rate model, then the hourly rate is derived from the default labor rate.
-   If an hourly rate is not found in the default labor rate, then the hourly rate is derived from the default system property.

Do not create and use resource assignments for allocating resources or groups to a demand task. The resource assignments that you create in the demand are used for the resource estimation of the work entity that would be created from the demand. These resource assignments are automatically moved to the resulting work entity when a demand is qualified and converted.

When you submit a time card for a demand the actual effort and cost are not reflected in the resource assignment, as the resource assignments are not associated with the demand by default. The actual cost and actual effort for the demand remains with the demand and are not transferred to the project created from the demand even if you manually associate a resource assignment with the demand.

If a resource spends extra hours working on a demand that are not associated with demand tasks, then this time must also be recorded. The resource submits the time card for recording the extra hours spent on the demand using the Time Sheet Portal. This extra cost and effort is added to the demand but is not reflected in the actual cost and effort for the demand tasks.

The actual cost and actual effort for the demand as derived from the time card data is added to the total actual cost and effort for the demand tasks. The values in the **Demand Actual Cost** and **Demand Actual Effort** fields are calculated as follows:

-   Demand Actual Cost: actual cost of all the demand tasks + actual cost of extra activities
-   Demand Actual Effort: actual effort of all the demand tasks + actual effort of extra activities

If a demand has no task or assigned resource, you can capture the actual cost by submitting a time card against the demand. Once the time card is approved, an expense line is created on the demand. The expense line is then processed and the actual cost of work for that time card is rolled up to the demand into the Demand Actual Cost column.

The following example demonstrates the actual cost and effort calculation for a demand task and its rollup to the demand.

## Actual cost and effort calculation based on demand tasks

For a demand \(D1\), the demand manager delegates activities such as initial assessment, cost estimate, and effort estimate. To delegate these activities, the demand manager creates three demand tasks \(DT1, DT2, and DT3\) and assigns resources R1, R2, and R3 to each demand task respectively.

The hourly rate defined for the resources in the rate model, default labor rate, and default system property are listed in the following table.

|Resource|Hourly rate in the rate model|Hourly rate in the default labor rate|Hourly rate in the system property|
|--------|-----------------------------|-------------------------------------|----------------------------------|
|R1|$200|$150|$50|
|R2|$250|$200|$50|
|R3|$150|$100|$50|

Each resource spends a total of eight hours while working on the assigned demand task and submits a time card.

Actual cost and effort calculation for demand task: The demand task actual cost and effort are calculated and displayed on the **Demand Task** form. The totals differ depending on the method used to derive them.

Scenario 1 shows how the total is calculated if the resource hourly rate is derived from the rate model.

|Actuals|Demand task DT1|Demand task DT2|Demand task DT3|
|-------|---------------|---------------|---------------|
|Actual effort|8 hours|8 hours|8 hours|
|Actual cost|200 \* 8 = $1600|250 \* 8 = $2000|150 \* 8 = $1200|

Scenario 2 shows how the total is calculated if the rate model is not associated with the demand and the resource hourly rate is derived from the default labor rate.

|Actuals|Demand task DT1|Demand task DT2|Demand task DT3|
|-------|---------------|---------------|---------------|
|Actual effort|8 hours|8 hours|8 hours|
|Actual cost|150 \* 8 = $1200|200 \* 8 = $1600|100 \* 8 = $800|

Scenario 3 shows how the total is calculated if the rate model is not associated with the demand and the resource hourly rate is derived from the default system property.

|Actuals|Demand task DT1|Demand task DT2|Demand task DT3|
|-------|---------------|---------------|---------------|
|Actual effort|8 hours|8 hours|8 hours|
|Actual cost|50 \* 8 = $400|50 \* 8 = $400|50 \* 8 = $400|

## Actual cost and effort roll up to a demand

The **Demand Actual Cost** and **Demand Actual Effort** fields on the Financials tab of the Demand form are populated with the sum of actual costs and actual effort of all the demand tasks.

1.  If the resource rate for demand task is derived from rate model \(Scenario 1\), the value in the Demand Actual Cost field is displayed as $4800. The value in the Demand Actual Effort field is displayed as 24 hours.
2.  If the resource rate for demand task is derived from the default labor rate \(Scenario 2\), the value in the Demand Actual Cost field is displayed as $3600. The value in the Demand Actual Effort field is displayed as 24 hours.
3.  If the resource rate for demand task is derived from the default system property \(Scenario 3\), the value in the Demand Actual Cost field is displayed as $1200. The value in the Demand Actual Effort field is displayed as 24 hours.

**Parent Topic:**[Demand Management reference](../../service-portfolio-management2/concept/demand-management-reference.md)

