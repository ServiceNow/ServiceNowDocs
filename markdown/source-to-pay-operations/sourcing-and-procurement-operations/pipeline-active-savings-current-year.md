---
title: Active Savings \(Current Year\) metric calculation
description: Active Savings \(Current Year\) shows the targeted savings from pipeline projects that are currently in progress. This metric represents in-flight work where final realized savings are not yet known.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-03-31"
reading_time_minutes: 3
keywords: [active savings, targeted savings, pipeline projects, work in progress, proration, savings metrics, analytics dashboard]
breadcrumb: [Pipeline management tab, Sourcing Pipeline Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Active Savings \(Current Year\) metric calculation

**Active Savings \(Current Year\)** shows the targeted savings from pipeline projects that are currently in progress. This metric represents in-flight work where final realized savings are not yet known.

**Active Savings \(Current Year\)** reads from the **Targeted savings** field because work is still underway and the final realized savings are not yet known. The difference from Planned Savings is the pipeline state; Active Savings \(Current Year\) includes projects only in Work in Progress state.

**Note:** Both Active Savings and Planned Savings read from the **Targeted savings** field. This is intentional — both represent projected or goal savings. The distinction is whether work on the project has started.

## Metric definition

The following attributes define the Active Savings \(Current Year\) metric:

|**Attribute**|**Detail**|
|-------------|----------|
|Metric name|Active Savings \(Current Year\)|
|Pipeline state|Work in Progress|
|Savings field|Targeted savings|
|Date range|User-specified \(typically the current calendar year\)|
|Proration|Yes — overlap-based proration|
|Used in|Savings by Type chart on the analytics dashboard|

## How Active Savings are calculated

The calculation follows the same steps as Planned Savings, with the state filter set to **Work in Progress** instead of Planned.

-   **Receive the date range.** The dashboard passes a date range — typically the current calendar year — along with any active filters.
-   **Break the range into monthly intervals.** The system splits the full date range into individual month windows.
-   **For each month, identify qualifying projects.** The system queries the pipeline project table for projects in **Work in Progress** state where:
    -   The project has a savings start date and a savings end date.
    -   The savings period overlaps with the month window.
    -   The project has a non-zero Targeted savings value.
-   **Prorate each project's savings against the month window.** The system applies the same proration formula used across all four metrics:
    -   Per-day rate = Targeted savings ÷ project duration \(capped at 365 days\)
    -   Prorated savings = per-day rate × overlap days
-   **Sum the monthly totals.** The prorated savings for all qualifying projects in each month are added together.
-   **Aggregate across months.** The monthly totals are combined into a time-series dataset for the Savings by Type chart on the analytics dashboard.

## Proration formula

Prorated Savings = \(Targeted Savings ÷ min\(Project Days, 365\)\) × Overlap Days.

Applied per month window, for Work in Progress projects only.

## Example calculation

The following scenario demonstrates how Active Savings is calculated for three active pipeline projects during the date range of January 1 to December 31, 2024:

|**Pipeline**|**State**|**Targeted Savings**|**Savings Start**|**Savings End**|**Project Days**|
|------------|---------|--------------------|-----------------|---------------|----------------|
|PIPE-301 \(Ongoing Vendor Negotiation\)|Work in Progress|$240,000|Mar 1, 2024|Aug 31, 2024|184|
|PIPE-302 \(Fleet Cost Reduction\)|Work in Progress|$365,000|Jan 1, 2024|Dec 31, 2024|365|
|PIPE-303 \(Strategic Sourcing\)|Work in Progress|$1,000,000|Jun 1, 2023|May 31, 2025|730|

-   **PIPE-301: Mid-year short project**
    -   Project duration = 184 days
    -   Overlap with range = 184 days \(project falls entirely within the year\)
    -   Per-day rate = $240,000 ÷ 184 = $1,304.35/day
    -   **Prorated savings = $1,304.35 × 184 = $240,000.00**
-   **PIPE-302: Full year alignment**
    -   Project duration = 365 days
    -   Overlap with range = 365 days \(perfect alignment\)
    -   Per-day rate = $365,000 ÷ 365 = $1,000.00/day
    -   **Prorated savings = $1,000.00 × 365 = $365,000.00**
-   **PIPE-303: Multi-year project \(365-day cap applies\)**
    -   Project duration = 730 days \(Jun 2023 – May 2025\) — **exceeds 365 days**
    -   Overlap with range = 365 days \(full year 2024\)
    -   Per-day rate = $1,000,000 ÷ **365 \(capped\)** = $2,739.73/day
    -   **Prorated savings = $2,739.73 × 365 = $1,000,000.00**

## Final aggregation

The final aggregation sums the prorated values:

|**Pipeline**|**Prorated Active Savings**|
|------------|---------------------------|
|PIPE-301|$240,000.00|
|PIPE-302|$365,000.00|
|PIPE-303|$1,000,000.00|
|**Total Active Savings \(Current Year\)**|**$1,605,000.00**|

**Parent Topic:**[Pipeline management tab](pipeline-mgmt-tab.md)

