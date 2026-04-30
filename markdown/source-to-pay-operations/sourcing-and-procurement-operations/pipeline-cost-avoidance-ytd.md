---
title: Cost Avoidance YTD metric calculation
description: Cost Avoidance YTD measures the costs that were prevented through pipeline projects during the current calendar year. Unlike hard savings, which reflect a direct reduction in spend, cost avoidance captures expenditures that were not incurred.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-03-31"
reading_time_minutes: 3
keywords: [cost avoidance, pipeline projects, savings metrics, proration, year-to-date]
breadcrumb: [Pipeline management tab, Sourcing Pipeline Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Cost Avoidance YTD metric calculation

**Cost Avoidance YTD** measures the costs that were prevented through pipeline projects during the current calendar year. Unlike hard savings, which reflect a direct reduction in spend, cost avoidance captures expenditures that were not incurred.

Cost avoidance captures prevented expenditures such as avoiding a price increase, preventing an unnecessary purchase, or reducing exposure to a risk-related cost. The metric operates on the same proration engine as Hard Savings YTD but reads from a different field on the project record.

## Metric definition

The following attributes define the **Cost Avoidance YTD** metric:

|**Attribute**|**Detail**|
|-------------|----------|
|Metric name|Cost Avoidance Year-to-Date|
|Pipeline state|Closed Complete|
|Savings field|Annual cost avoidance|
|Date range|January 1 to December 31 of the current year|
|Proration|Yes — based on the overlap between the project's savings period and the current year|
|Year-over-year comparison|Yes — the metric automatically compares the current year total against the same date range in the previous year|

## Differences between cost avoidance and hard savings

Cost avoidance and hard savings represent distinct types of financial impact:

|**Aspect**|**Hard Savings**|**Cost Avoidance**|
|----------|----------------|------------------|
|Nature|Direct reduction in budget spend|Prevention of a cost that would otherwise have been incurred|
|Field on project record|Annual hard savings|Annual cost avoidance|
|Visibility on P&amp;L|Directly reflected|Counterfactual — represents what was not spent|
|Calculation logic|Identical — both use the same proration engine|Identical — both use the same proration engine|

## How Cost Avoidance YTD Is Calculated

The calculation follows the same steps as Hard Savings YTD. The only difference is that the system reads the **Annual cost avoidance** field on each project record rather than the Annual hard savings field.

-   **Establish the date range**: The system sets the calculation range to January 1 through December 31 of the current calendar year. The same process also runs against the previous year for comparison.
-   **Identify qualifying projects**: The system queries the pipeline project table for all Closed Complete projects assigned to the current user where the savings period overlaps with the target year and the project has a non-zero value in the Annual cost avoidance field.
-   **Calculate overlap days for each project**: The system identifies how many days of the project's savings period fall within the target year.
-   **Calculate the per-day savings rate**: The project's total cost avoidance value is divided by its duration in days, capped at 365 days for projects that span more than one year.
-   **Prorate the savings**: The prorated cost avoidance for each project equals the per-day rate multiplied by the overlap days.
-   **Aggregate and round**: The prorated values for all qualifying projects are summed and rounded to two decimal places.
-   **Compute the year-over-year comparison**: The same steps run against the previous year, and the system calculates the difference and percentage change.

## Proration formula

The proration formula calculates the portion of cost avoidance that falls within the target year:

**Prorated Cost Avoidance = \(Cost Avoidance ÷ min\(Project Days, 365\)\) × Overlap Days**

Overlap Days represents the number of days the project's savings period intersects with the target year's date range.

## Example calculation

The following scenario demonstrates how **Cost Avoidance YTD** is calculated for two pipeline projects during the year-to-date range of January 1 to December 31, 2024:

|**Pipeline**|**State**|**Cost Avoidance**|**Savings Start**|**Savings End**|**Project Days**|
|------------|---------|------------------|-----------------|---------------|----------------|
|PIPE-101 \(Prevented Price Increase\)|Closed Complete|$200,000|Apr 1, 2024|Mar 31, 2025|365|
|PIPE-102 \(License Optimization\)|Closed Complete|$90,000|Jan 1, 2024|Jun 30, 2024|181|

-   **PIPE-101 has a partial overlap with the year-to-date range:**
    -   Project duration = 365 days \(Apr 1, 2024 – Mar 31, 2025\)
    -   Overlap with YTD range = 275 days \(Apr 1 – Dec 31, 2024\)
    -   Per-day rate = $200,000 ÷ 365 = $547.95/day
    -   Prorated cost avoidance = $547.95 × 275 = $150,684.93
-   **PIPE-102 falls entirely within the year-to-date range:**
    -   Project duration = 181 days
    -   Overlap with YTD range = 181 days \(project falls entirely within the year\)
    -   Per-day rate = $90,000 ÷ 181 = $497.24/day
    -   Prorated cost avoidance = $497.24 × 181 = $90,000.00

## Final aggregation

The final aggregation sums the prorated values:

|**Pipeline**|**Prorated Cost Avoidance**|
|------------|---------------------------|
|PIPE-101|$150,684.93|
|PIPE-102|$90,000.00|
|**Total Cost Avoidance YTD**|**$240,684.93**|

**Parent Topic:**[Pipeline management tab](pipeline-mgmt-tab.md)

