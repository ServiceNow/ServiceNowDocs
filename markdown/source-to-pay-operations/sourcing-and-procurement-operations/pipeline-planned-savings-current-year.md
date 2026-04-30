---
title: Planned Savings \(Current Year\) metric calculation
description: Planned Savings \(Current Year\) shows the projected savings from pipeline projects in Planned state—projects approved and scheduled but not yet started. This metric uses the Targeted savings field to represent future savings goals.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-03-31"
reading_time_minutes: 3
keywords: [planned savings, targeted savings, pipeline projects, analytics dashboard, savings by type, proration]
breadcrumb: [Pipeline management tab, Sourcing Pipeline Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Planned Savings \(Current Year\) metric calculation

**Planned Savings \(Current Year\)** shows the projected savings from pipeline projects in **Planned** state—projects approved and scheduled but not yet started. This metric uses the **Targeted savings** field to represent future savings goals.

**Planned Savings \(Current Year\)** tracks savings expected from pipeline projects that have been approved but where work has not begun. The metric reads from the **Targeted savings** field, which holds the savings goal set during project creation.

**Note:** Both Active Savings and Planned Savings read from the **Targeted savings** field. This is intentional — both represent projected or goal savings. The distinction is whether work on the project has started.

## Metric definition

The following attributes define the Planned Savings \(Current Year\) metric:

|**Attribute**|**Detail**|
|-------------|----------|
|Metric name|Planned Savings \(Current Year\)|
|Pipeline state|Planned|
|Savings field|Targeted savings|
|Date range|User-specified \(typically the current calendar year\)|
|Proration|Yes — overlap-based proration|
|Used in|Savings by Type chart on the analytics dashboard|

## How planned savings differs from hard savings and cost avoidance

|**Aspect**|**Hard Savings / Cost Avoidance YTD**|**Planned Savings**|
|----------|-------------------------------------|-------------------|
|Pipeline state|Closed Complete|Planned|
|Savings field|Annual hard savings / Annual cost avoidance|Targeted savings|
|What it represents|Actual achieved savings|Future projected savings|

**Note:** Planned projects have not yet completed, so only the savings target is available. This is why the **Targeted savings** field is used instead of the **Annual hard savings** or **Annual cost avoidance** fields.

## How Planned Savings Are Calculated

The Planned Savings metric is calculated month by month across the selected date range and then aggregated for the Savings by Type chart on the analytics dashboard.

-   **Receive the date range**: The dashboard passes a date range—typically the current calendar year—along with any active filters \(such as department or category\).
-   **Break the range into monthly intervals**: The system splits the full date range into individual month windows \(for example, January 1–31, February 1–28, and so on through December\).
-   **For each month, identify qualifying projects**: The system queries the pipeline project table for projects in **Planned** state where the project has a savings start date and a savings end date, the savings period overlaps with the month window, and the project has a non-zero **Targeted savings** value.
-   **Prorate each project's savings against the month window**: For each qualifying project, the system calculates the overlap between the project's savings period and the month window, then applies the proration formula. Per-day rate equals **Targeted savings** divided by project duration \(capped at 365 days\). Prorated savings equals per-day rate multiplied by overlap days.
-   **Sum the monthly totals**: The prorated savings for all qualifying projects in each month are added together to produce a monthly planned savings figure.
-   **Aggregate across months**: The monthly totals are combined into a time-series dataset used to render the Savings by Type chart on the analytics dashboard.

## Proration formula

Prorated Savings = \(Targeted Savings ÷ min\(Project Days, 365\)\) × Overlap Days.

Applied per month window across the selected date range.

## Example calculation

The following scenario demonstrates how Planned Savings is calculated for two planned pipeline projects during the date range of January 1 to December 31, 2024:

|**Pipeline**|**State**|**Targeted Savings**|**Savings Start**|**Savings End**|
|------------|---------|--------------------|-----------------|---------------|
|PIPE-201 \(Q3 Vendor Review\)|Planned|$180,000|Jul 1, 2024|Dec 31, 2024|
|PIPE-202 \(Cloud Migration Savings\)|Planned|$500,000|Jan 1, 2024|Dec 31, 2025|

-   **PIPE-201: Fully within the year \(H2 project\)**
    -   Project duration = 184 days
    -   Overlap with range = 184 days \(project falls entirely within the year\)
    -   Per-day rate = $180,000 ÷ 184 = $978.26/day
    -   Prorated savings = $978.26 × 184 = $180,000.00
-   **PIPE-202: Multi-year project \(365-day cap applies\)**
    -   Project duration = 730 days — exceeds 385 days
    -   Overlap with range = 365 days \(full year 2024\)
    -   Per-day rate = $500,000 ÷ **365 \(capped\)** = $1,369.86/day
    -   **Prorated savings = $1,369.86 × 365 = $500,000.00**

## Final aggregation

The final aggregation sums the prorated values:

|**Pipeline**|**Prorated Planned Savings**|
|------------|----------------------------|
|PIPE-201|$180,000.00|
|PIPE-202|$500,000.00|
|**Total Planned Savings \(Current Year\)**|**$680,000.00**|

**Parent Topic:**[Pipeline management tab](pipeline-mgmt-tab.md)

