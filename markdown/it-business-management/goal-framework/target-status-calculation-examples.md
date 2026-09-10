---
title: Status calculation specifications and examples
description: Detailed specifications for status calculation across different target types, calculation formulas for targets with and without breakdowns, and worked examples demonstrating status assignment and rollup mechanics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/goal-framework/target-status-calculation-examples.html
release: australia
product: Goal Framework
classification: goal-framework
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Explore, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Status calculation specifications and examples

Detailed specifications for status calculation across different target types, calculation formulas for targets with and without breakdowns, and worked examples demonstrating status assignment and rollup mechanics.

## Status calculation for targets without breakdowns

For targets without period-based breakdowns, status is calculated once using the overall actual value against the Final target value:

```
Achievement % = ((Actuals to date − Start Value) ÷ (Final target value − Start Value)) × 100
Status = Green if Achievement % ≥ 90; Yellow if 75–89; Red if < 75
```

**Example:** Achieve $1,000,000 revenue by the year-end

-   Start value \(baseline\): $0
-   Final target value: $1,000,000
-   Actuals to date \(year-end\): $700,000
-   Achievement % = \(\($700,000 − $0\) ÷ \($1,000,000 − $0\)\) × 100 = 70%
-   **Status: Red** \(70% &lt; 75%\)

## Status calculation for targets with breakdowns \(check-ins\)

For targets with period-based breakdowns \(weekly, monthly, quarterly\), status is calculated for each check-in period independently:

```
Achievement % (for period) = ((Period Actual − Period Start) ÷ (Period Planned − Period Start)) × 100
Status (for period) = Green if Achievement % ≥ 90; Yellow if 75–89; Red if < 75
```

**Example:** Annual revenue target with quarterly check-ins

|Quarter|Start Value|Planned|Actual|Achievement %|Status|
|-------|-----------|-------|------|-------------|------|
|Q1|$0|$250,000|$220,000|88%|Yellow|
|Q2|$220,000|$500,000|$480,000|92.9%|Green|
|Q3|$480,000|$750,000|$710,000|76.7%|Yellow|
|Q4|$710,000|$1,000,000|$968,000|86%|Yellow|

In this scenario, each quarter is evaluated independently against the $1,000,000 annual target \(Final target value\). Q1 started with Yellow status \(88%\), Q2 improved to Green \(92.9%\), Q3 declined to Yellow \(76.7%\), and Q4 improved slightly but remained Yellow \(86%\). Each quarter's start value is the previous quarter's actual achievement. The most recent period \(Q4\) determines the target status, which is Yellow.

## Status rollup mechanics

Status automatically rolls up through three hierarchical layers:

-   **Layer 1: Breakdown → Target \(Latest-wins logic\)**

    When a target has multiple check-in periods, the status of the target is determined by the most recent period's status:

    -   If March check-in status is Red, target status = Red
    -   If February check-in status is Yellow and March is Green, target status = Green \(most recent wins\)
-   **Layer 2: Target → Goal \(Worst-wins logic\)**

    When a goal has multiple targets, the goal status is determined by the lowest-performing target:

    -   Target 1 status = Green \(90%\)
    -   Target 2 status = Red \(60%\)
    -   **Goal status = Red** \(worst-wins\)
-   **Layer 3: Goal → Parent goal \(Worst-wins logic\)**

    Goals roll up to parent goals using worst-wins logic:

    -   Goal 1 status = Yellow
    -   Goal 2 status = Red
    -   Initiative status = Red \(cascades up\)
    -   Portfolio status = Red \(single red initiative propagates to portfolio\)

## Status rollup example: Three-layer cascade

This example shows how status cascades through all three layers:

```
LAYER 1 — Check-ins roll up to Targets (Latest-wins):
  Q1 Revenue Target:
    Week 1: Green (92%)
    Week 2: Yellow (78%)
    Week 3: Green (91%)  ← Most recent; Target Status = Green

LAYER 2 — Targets roll up to Goals (Worst-wins):
  Annual Growth Goal:
    Q1 Revenue Target: Green (91%)
    Q1 Cost Target: Red (60%)
    ├─ Goal Status = Red (cost target drags down entire goal)

LAYER 3 — Goals roll up to Parent goals (Worst-wins):
  Strategic Goals:
    Growth Goal: Red (from Annual Growth Goal)
    Efficiency Goal: Green (80%)
    Innovation Goal: Yellow (78%)
    ├─ Parent goal Status = Red (single red target/child goal cascades to parent goal)
```

## Special status calculation cases

-   **Manual override then recalculation**

    If you manually override status to Red, then later update the actual value such that the achievement percentage would calculate as Green \(95%\), the system recalculates and displays Green. Manual overrides do not persist through data updates.

-   **Milestone targets \(qualitative goals\)**

    Milestone targets use qualitative maturity levels \(e.g., Planning, Execution, Delivery, Launch\) instead of numeric formulas. Status is assigned manually based on milestone stage progress. Examples: project readiness, capability maturity, process implementation. Though not automatically calculated, milestone targets still roll up using worst-wins logic and affect portfolio health.


