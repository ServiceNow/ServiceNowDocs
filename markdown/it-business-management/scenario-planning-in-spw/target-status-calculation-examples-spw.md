---
title: Status calculation specifications and examples
description: Formulas and worked examples show how target status is calculated for each target type and how status rolls up from breakdowns to goals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/target-status-calculation-examples-spw.html
release: brazil
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-10-09"
reading_time_minutes: 10
breadcrumb: [Goals in Strategic Planning, Explore, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Status calculation specifications and examples

Formulas and worked examples show how target status is calculated for each target type and how status rolls up from breakdowns to goals.

## Status calculation for targets without breakdowns

For targets without period-based breakdowns, status is calculated once using the overall actual value against the final target value:

```
Achievement % = ((Actuals to date − Start value) ÷ (Final target value − Start value)) × 100
Status = Green if Achievement % ≥ 90; Yellow if 75–89; Red if < 75
```

**Example:** Achieve $1,000,000 revenue by year-end

-   Start value \(baseline\): $0
-   Final target value: $1,000,000
-   Actuals to date \(year-end\): $700,000
-   Achievement % = \(\($700,000 − $0\) ÷ \($1,000,000 − $0\)\) × 100 = 70%
-   **Status: Red** \(70% &lt; 75%\)

## Status calculation for targets with cumulative breakdowns

For cumulative targets with period-based breakdowns, each period's start value carries forward from the previous period's actual value. Status is calculated for each check-in period independently based on that period's start value and planned target. The achievement percentage is recalculated for each period as new data is reported, and the most recent period's status determines the target status.

```
Achievement % (for period) = ((Period actual value − Period start value) ÷ (Period planned target value − Period start value)) × 100
Status (for period) = Green if Achievement % ≥ 90; Yellow if 75–89; Red if < 75
```

**Example:** Annual revenue target with cumulative quarterly check-ins \(Planned target and Actual values shown are cumulative amounts\)

In this example, each quarter's achievement is measured from a start value of $0, comparing the cumulative actual revenue to the cumulative planned target. The "Start value" column shows $0 for Q1, then carries forward the previous quarter's cumulative actual for reference purposes \(Q2: $220K from Q1, Q3: $480K from Q2, Q4: $710K from Q3\), but the formula always uses cumulative amounts from the $0 baseline.

|Quarter|Start value|Planned target|Actual|Achievement %|Status|
|-------|-----------|--------------|------|-------------|------|
|Q1|$0|$250,000|$220,000|88%|Yellow|
|Q2|$220,000|$500,000|$480,000|96%|Green|
|Q3|$480,000|$750,000|$710,000|94.7%|Green|
|Q4|$710,000|$1,000,000|$968,000|96.8%|Green|

In this scenario, each quarter is evaluated cumulatively from a start value of $0. Achievement % is calculated by comparing cumulative actual revenue to cumulative planned target: Q1: $220K ÷ $250K = 88% \(Yellow\). Q2: $480K ÷ $500K = 96% \(Green\). Q3: $710K ÷ $750K = 94.7% \(Green\). Q4: $968K ÷ $1,000K = 96.8% \(Green\). The most recent period \(Q4\) determines the target status, which is Green. Overall, the target is progressing at 96.8% achievement against the $1,000,000 annual goal.

-   **How breakdown statuses roll up to the target status**

    The target's overall status is determined using latest-wins logic: the status of the most recently reported breakdown period becomes the target status.

    -   Q1 status: Yellow \(88%\)
    -   Q2 status: Green \(96%\)
    -   Q3 status: Green \(94.7%\)
    -   Q4 status: Green \(96.8%\) ← **Most recent**
    -   **Target status: Green** \(determined by Q4, the latest reported quarter\)
    The target displays Green status even though Q1 was Yellow, because Q4's Green status is the most current indicator of performance. If Q4's actual had fallen short and resulted in Yellow or Red, the target status would reflect that latest assessment.


\[Omitted image "target-status-rollup-cumulative-example.gif"\] Alt text: Status calculation for targets with cumulative breakdowns.

## Status calculation for targets with non-cumulative breakdowns

For non-cumulative targets with period-based breakdowns, each period is independent and does not carry forward the previous period's actual value. Status is calculated as a window aggregating all periods with actual values from the first period to the most recent period. The achievement percentage is recalculated each time a new period is reported.

```
Window = Sum of all Actuals (Q1 through most recent quarter) ÷ Sum of all Planned (Q1 through most recent quarter)
Achievement % = (Total actuals ÷ Total planned) × 100
Status = Green if Achievement % ≥ 90; Yellow if 75–89; Red if < 75
```

**Example:** Annual revenue target \($0 start, $1,000,000 final target\) with non-cumulative quarterly check-ins

|Quarter|Planned \(this quarter\)|Actual \(this quarter\)|Breakdown status|Total actual|Total planned|Target window %|
|-------|------------------------|-----------------------|----------------|------------|-------------|---------------|
|Q1|$250,000|$220,000|88% \(Yellow\)|$220,000|$250,000|88%|
|Q2|$250,000|$240,000|96% \(Green\)|$460,000|$500,000|92%|
|Q3|$250,000|$200,000|80% \(Yellow\)|$660,000|$750,000|88%|
|Q4|$250,000|$230,000|92% \(Green\)|$890,000|$1,000,000|89% \(Yellow\)|

Although Q4's individual breakdown shows Green \(92%\), the target displays Yellow \(89%\) because the target's status reflects the overall cumulative performance across all four quarters. Individual breakdown statuses show period-by-period progress, while the target status shows how the team is tracking toward the full-year goal.

**Key differences from cumulative:** In cumulative, each quarter's start value is the previous quarter's actual \($220K → $480K → $710K\), and each quarter's status is calculated individually. In non-cumulative, each quarter's Planned and Actual are independent \($250K planned each quarter\). Each quarter's status is also calculated independently: Q1 = 88% Yellow, Q2 = 96% Green, Q3 = 80% Yellow, Q4 = 92% Green. However, the target's overall status is determined by the cumulative window across all quarters: \($220K + $240K + $200K + $230K\) ÷ \($250K + $250K + $250K + $250K\) = 89% Yellow. The target can show Yellow status even when the latest quarter \(Q4\) shows Green—it reflects overall annual progress, not the most recent period alone.

-   **How breakdown statuses roll up to the target status**

    The target's overall status is determined by aggregating all periods into a cumulative window. The target status is not determined by the most recent breakdown; instead, it reflects the cumulative performance across all reported periods.

    -   Q1 status: Yellow \(88% independent\)
    -   Q2 status: Green \(96% independent\)
    -   Q3 status: Yellow \(80% independent\)
    -   Q4 status: Green \(92% independent\)
    -   **Target window:** \($220K + $240K + $200K + $230K\) ÷ \($250K + $250K + $250K + $250K\) = $890K ÷ $1,000K = 89%
    -   **Target status: Yellow** \(89% determined by cumulative window, not by latest breakdown\)

\[Omitted image "target-status-rollup-non-cumulative-example.gif"\] Alt text: Status calculation for targets with non-cumulative breakdowns.

## Status calculation for Maintain-type targets

The following example shows status calculation for a Maintain above target. For Maintain above targets, the planned target of every breakdown period defaults to the final target value of the target, and you can edit it for each period. Each period is evaluated on its own: it is Green when the actual value is greater than or equal to the planned target, and Red when the actual value is lower. Progress is the percentage of periods that meet the planned target, counted up to the latest period with an actual value. The target status is based on this progress, compared against the same thresholds as other target types \(90% for Green and 75% for Yellow by default\).

```
Period status = Green if Actual ≥ Planned target; Red if Actual < Planned target
Progress % = (Number of periods met ÷ Number of periods up to the latest period with an actual value) × 100
Target status = Green if Progress % ≥ 90; Yellow if 75–89; Red if Progress % < 75
```

**Example:** Keep API uptime at or above 99.5% through year-end, with quarterly check-ins

-   Type: Maintain above
-   Final target value: 99.5%
-   Planned target for each quarter: 99.5%

|Quarter|Planned target|Actual|Period status|Periods met|Progress|Target status|
|-------|--------------|------|-------------|-----------|--------|-------------|
|Q1|99.5%|99.6%|Green|1 of 1|100%|Green|
|Q2|99.5%|99.3%|Red|1 of 2|50%|Red|
|Q3|99.5%|99.7%|Green|2 of 3|66.7%|Red|
|Q4|99.5%|99.8%|Green|3 of 4|75%|Yellow|

In this scenario, the Q1 actual of 99.6% is greater than the planned target of 99.5%, so Q1 is Green. The target has met 1 of 1 reported periods, so progress is 100%. The Q2 actual of 99.3% is lower than the planned target, so Q2 is Red. The target has now met 1 of 2 reported periods, so progress is 50%. Because 50% is below the Yellow threshold of 75%, the **target status is Red**. The Q3 actual of 99.7% meets the planned target, so Q3 is Green, but the target has met only 2 of 3 reported periods. Progress is 66.7%, which is still below 75%, so the target status stays Red. The Q4 actual of 99.8% also meets the planned target, so the target has met 3 of 4 periods. Progress is 75%, which falls in the 75–89% range, so the **target status changes to Yellow**. Because the target status is based on progress rather than on the latest period alone, a Red period doesn't keep the target Red: the target status improves as more periods meet the planned target.

\[Omitted image "target-status-rollup-maintain-above-example.gif"\] Alt text: Status calculation for maintain-type target.

## Status rollup mechanics

Status automatically rolls up through three hierarchical layers:

-   **Layer 1 for cumulative targets: Breakdown → Target \(latest-wins logic\)**

    When a target has multiple check-in periods, the status of the target is determined by the most recent period's status:

    -   If the March check-in status is Red, the target status is Red.
    -   If the February check-in status is Yellow and the March status is Green, the target status is Green because the most recent period determines it.
-   **Layer 1 for non-cumulative targets: Breakdown → Target \(cumulative window aggregation\)**

    For non-cumulative targets with period-based breakdowns, the target's overall status is determined by aggregating all periods into a single cumulative window. The target status is determined by the cumulative performance across all reported breakdown periods.

    -   Q1 status: Yellow \(88% independent\) — Actual: $220K, Planned: $250K
    -   Q2 status: Green \(96% independent\) — Actual: $240K, Planned: $250K
    -   Q3 status: Yellow \(80% independent\) — Actual: $200K, Planned: $250K
    -   Q4 status: Green \(92% independent\) — Actual: $230K, Planned: $250K
    -   **Target window calculation:** Total Actuals \($220K + $240K + $200K + $230K = $890K\) ÷ Total Planned \($250K + $250K + $250K + $250K = $1,000K\) = 89%
    -   **Target status: Yellow** \(89% from cumulative window, even though Q4 is Green\)
    The key distinction: individual breakdowns may show Green \(Q4 at 92%\), but the target displays Yellow because the cumulative performance across all quarters \(89%\) determines the target status. This reflects overall annual progress, not just the most recent period.

-   **Layer 2: Target → Goal \(worst-wins logic\)**

    When a goal has multiple targets, the goal status is determined by the lowest-performing target:

    -   Target 1 status = Green \(90%\)
    -   Target 2 status = Red \(60%\)
    -   **Goal status = Red** \(worst-wins\)
-   **Layer 3: Goal → Parent goal \(worst-wins logic\)**

    Goals roll up to parent goals using worst-wins logic:

    -   Goal 1 \(Parent goal\) status = Yellow
    -   Goal 1.2 \(Child goal\) status = Red
    -   Target 1.2.1 status = Yellow
    As a result, the parent goal \(Goal 1\) status is Red because the Red status of the child goal rolls up to the parent goal.


## Status rollup example across three layers

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

    If you manually override status to Red, the override applies immediately. However, if you later update the actual value such that the achievement percentage would calculate as Green \(95%\), the system recalculates and displays Green. Manual overrides don't persist through data updates.

-   **Milestone targets \(qualitative goals\)**

    Milestone targets use a binary Yes/No status assignment instead of numeric formulas. You determine whether the milestone has been achieved: Yes = Green status, No = Red status. Yellow is not available. Examples: project readiness gates, regulatory approvals, capability certifications. Though not automatically calculated, milestone targets roll up from the target to its goal, and from the goal to parent goals if any, using worst-wins logic.


**Parent Topic:**[Goals in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/goal-management-in-alignment-planner-workspace.md)

