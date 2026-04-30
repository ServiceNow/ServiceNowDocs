---
title: Hard Savings YTD metric calculation
description: Hard Savings YTD \(Year-to-Date\) shows the total realized savings from pipeline projects that were closed and completed within the current calendar year. These are confirmed, negotiated savings — not estimates or projections.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-03-31"
reading_time_minutes: 4
keywords: [hard savings, year-to-date, pipeline projects, procurement, savings proration, closed complete, annual savings]
breadcrumb: [Pipeline management tab, Sourcing Pipeline Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Hard Savings YTD metric calculation

**Hard Savings YTD** \(Year-to-Date\) shows the total realized savings from pipeline projects that were closed and completed within the current calendar year. These are confirmed, negotiated savings — not estimates or projections.

## Metric definition

The following attributes define the Hard Savings YTD metric:

|**Attribute**|**Detail**|
|-------------|----------|
|Metric name|Hard Savings Year-to-Date|
|Pipeline state|Closed Complete|
|Savings field|Annual hard savings|
|Date range|January 1 to December 31 of the current year|
|Proration|Yes — based on the overlap between the project's savings period and the current year|
|Year-over-year comparison|Yes — the metric automatically compares the current year total against the same date range in the previous year|

## Key concepts

-   **Annual hard savings** is the field on a pipeline project record that holds the actual negotiated savings value, entered when the project is closed and completed.
-   Only projects in Closed Complete state contribute to this metric.
-   Savings are prorated based on how many days of the project's savings period fall within the current calendar year.
-   For projects that span more than one year, the per-day savings rate is calculated using a 365-day cap. This prevents multi-year project totals from being diluted across the full project duration and ensures the metric always reflects an annual savings rate.

## How Hard Savings YTD Is Calculated

The following steps describe how the system arrives at the Hard Savings YTD figure displayed on the dashboard widget.

1.  **Establish the date range.** The system sets the calculation range to January 1 through December 31 of the current calendar year. This same process also runs against the previous calendar year to enable year-over-year comparison.
2.  **Identify qualifying projects.** The system queries the pipeline project table for all projects assigned to the current user that meet the following criteria:
    -   The project is in **Closed Complete** state.
    -   The project has a savings start date and a savings end date.
    -   The savings period overlaps with the target year — the savings start date falls on or before December 31, and the savings end date falls on or after January 1.
    -   The project has a non-zero value in the Annual hard savings field.
3.  **Calculate overlap days for each project.** For each qualifying project, the system determines how many days the project's savings period fall within the target year. This is the number of days between the later of \(the savings start date or January 1\) and the earlier of \(the savings end date or December 31\).
4.  **Calculate the per-day savings rate.** The system divides the project's total hard savings value by the project's duration in days. If the project spans more than 365 days, the duration is capped at 365 to normalize the rate to an annual basis.
5.  **Prorate the savings.** The prorated savings for each project equals the per-day rate multiplied by the number of overlap days. Projects where the savings period falls entirely within the current year receive their full hard savings value.
6.  **Aggregate and round.** The prorated savings values for all qualifying projects are added together. The result is rounded to two decimal places.
7.  **Compute the year-over-year comparison.** Steps 2–6 run a second time against the previous calendar year. The system calculates the difference and percentage change between the two year totals.
8.  **Return the result.** The current year total is displayed as the Hard Savings YTD value on the dashboard widget, together with the year-over-year change indicator.

## Proration formula

Prorated Savings = \(Hard Savings ÷ min\(Project Days, 365\)\) × Overlap Days.

Overlap Days = the number of days the project's savings period intersects with the target year's date range.

**The 365-day cap explained:** For a project that spans 1,095 days \(3 years\), using the actual project duration as the divisor would spread the savings across 1,095 days and significantly understate the annual figure. Capping the divisor at 365 ensures the per-day rate reflects the project's intended annual savings value, not a fraction of it.

## Example calculation

The following scenario demonstrates how Hard Savings YTD is calculated for three pipeline projects during the year-to-date range of January 1 to December 31, 2024:

|**Pipeline**|**State**|**Hard Savings**|**Savings Start**|**Savings End**|**Project Days**|
|------------|---------|----------------|-----------------|---------------|----------------|
|PIPE-001 \(Supplier Renegotiation\)|Closed Complete|$120,000|Jan 1, 2024|Dec 31, 2024|365|
|PIPE-002 \(Contract Consolidation\)|Closed Complete|$365,000|Jul 1, 2024|Jun 30, 2025|365|
|PIPE-003 \(Multi-Year Agreement\)|Closed Complete|$730,000|Jan 1, 2023|Dec 31, 2025|1,095|

-   **PIPE-001: Full overlap**
    -   Project duration = 365 days
    -   Overlap with YTD range = 365 days \(project falls entirely within the year\)
    -   Per-day rate = $120,000 ÷ 365 = $328.77/day
    -   Prorated savings = $328.77 × 365 = $120,000.00
-   **PIPE-002: Partial overlap \(starts mid-year\)**
    -   Project duration = 365 days \(Jul 1, 2024 – Jun 30, 2025\)
    -   Overlap with YTD range = 184 days \(Jul 1 – Dec 31, 2024\)
    -   Per-day rate = $365,000 ÷ 365 = $1,000.00/day
    -   Prorated savings = $1,000.00 × 184 = $184,000.00
-   **PIPE-003: Multi-year project \(365-day cap applies\)**
    -   Project duration = 1,095 days \(Jan 1, 2023 – Dec 31, 2025\) — **exceeds 365 days**
    -   Overlap with YTD range = 365 days \(full year 2024\)
    -   Per-day rate = $730,000 ÷ **365 \(capped\)** = $2,000.00/day
    -   Prorated savings = $2,000.00 × 365 = $730,000.00

**Why the cap matters here:** PIPE-003 spans 1,095 days across three years. Without the 365-day cap, the per-day rate would be $730,000 ÷ 1,095 = $667/day — and only $243,333 would be attributed to 2024. The cap corrects for this by treating the savings as an annual figure, which returns the full $730,000 to the 2024 total.

## Final aggregation

The final aggregation sums the prorated values:

|**Pipeline**|**Prorated Hard Savings**|
|------------|-------------------------|
|PIPE-001|$120,000.00|
|PIPE-002|$184,000.00|
|PIPE-003|$730,000.00|
|**Total Hard Savings YTD**|**$1,034,000.00**|

**Parent Topic:**[Pipeline management tab](pipeline-mgmt-tab.md)

