---
title: Target types and achievement strategies
description: The types define how goal achievement is measured: growth, reduction, staying within limits, or a yes/no milestone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/goal-framework/target-types-gf.html
release: brazil
product: Goal Framework
classification: goal-framework
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 9
keywords: [target type, Maximize, Minimize, Maintain above, Maintain below, Maintain constant, Milestone]
breadcrumb: [Explore, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Target types and achievement strategies

The types define how goal achievement is measured: growth, reduction, staying within limits, or a yes/no milestone.

## Target types at a glance

Target types define the direction and measurement approach for your goals. Each type has a specific formula for calculating achievement and progress. When you create a target, select the type that best reflects your goal's strategic intent, as described in the following table.

|Target type|Best use case|Achievement criteria|
|-----------|-------------|--------------------|
|Maximize|Goals to grow or increase a metric: revenue, customer satisfaction, productivity, market share, employee engagement|Progress increases as the actual value moves from the start value toward the target value. Status is Green at 90% or higher.|
|Minimize|Goals to reduce or decrease a metric: costs, defects, environmental impact, customer churn, incident count|Progress increases as actual values decrease toward the target value. Status is Green at 90% or higher.|
|Maintain above|Goals where a metric must stay at or above a threshold: service uptime, compliance rating, customer retention rate, system availability|A period is met when its actual value is greater than or equal to its planned target. Progress is the percentage of periods met, up to the latest period with an actual value.|
|Maintain below|Goals where a metric must stay at or below a cap: operating costs, error rate, support ticket backlog, environmental emissions|A period is met when its actual value is less than or equal to its planned target. Progress is the percentage of periods met, up to the latest period with an actual value.|
|Maintain constant|Goals requiring stability: staffing levels, quality scores, inventory levels, process consistency|A period is met when its actual value is within the tolerance band around its planned target \(±5% by default\). Progress is the percentage of periods met, up to the latest period with an actual value.|
|Milestone|Qualitative goals with yes/no outcomes: project completion, regulatory approval, capability certification, system deployment|Binary achievement \(Yes = Green, No = Red\). No Yellow status available|

## Maximize targets

Maximize targets measure progress toward increasing a metric from a baseline to a higher target value. Use this type when success means growing or improving a value.

**How achievement is calculated:**

```
Achievement % = ((Actual to date − Start Value) ÷ (Final target value − Start Value)) × 100
```

**Example — Revenue growth:**

-   Start value: $1,000,000
-   Final target value: $1,500,000
-   Current actual: $1,350,000
-   Achievement: \(\($1,350,000 − $1,000,000\) ÷ \($1,500,000 − $1,000,000\)\) × 100 = 70%
-   Status: Red \(70% is below the Yellow threshold which is 75%\)

**When to use:** Revenue, market share, customer satisfaction, productivity metrics, employee retention rate.

## Minimize targets

Minimize targets measure progress toward decreasing a metric from a baseline to a lower goal. Use this type when success means reducing or eliminating an undesirable value.

**How achievement is calculated:**

```
Achievement % = ((Start Value − Actuals to date) ÷ (Start Value − Final target value)) × 100
```

**Example — Cost reduction:**

-   Start Value: $500,000
-   Final Target Value: $400,000
-   Current Actual: $420,000
-   Achievement: \(\($500,000 − $420,000\) ÷ \($500,000 − $400,000\)\) × 100 = 80%
-   Status: Yellow \(within 75–89% threshold\)

**When to use:** Cost reduction, defect elimination, incident reduction, environmental emissions targets, customer complaints.

## Maintain targets

Maintain targets focus on keeping a metric stable or within acceptable boundaries rather than progressing toward a new value. Use these types for governance, compliance, and operational consistency goals.

For Maintain types, the planned target of every target breakdown equals the final target value. The **Actuals to date** value of the target is the actual value entered for the latest breakdown period, not a sum of all periods. Progress stays empty until you enter an actual value for at least one period. A period without an actual value that falls before the latest period with an actual value counts as not met. The **Target value distribution** field is hidden for Maintain types.

## Maintain above targets

A Maintain above target succeeds when the actual value stays at or above a specified threshold across reporting periods.

**How achievement is calculated:**

```
Progress % = (Number of periods met ÷ Number of periods up to the latest period with an actual value) × 100
```

**Example — Service uptime:**

-   Target type: Maintain above
-   Final target value \(Threshold\): 98% uptime
-   Check-in frequency: Monthly \(12 periods\)
-   Uptime by month: Jan–Oct all ≥98%, Nov &lt;98%, Dec ≥98% \(11 of 12 months pass\)
-   Achievement: \(11 ÷ 12\) × 100 = 92%

**When to use:** Service level agreements \(SLAs\), compliance ratings, uptime targets, customer retention rates, system availability.

## Maintain below targets

A Maintain below target succeeds when the actual value stays at or below a specified threshold \(cap\) across reporting periods.

**How achievement is calculated:**

```
Progress % = (Number of periods met ÷ Number of periods up to the latest period with an actual value) × 100
```

**Example — Operating cost cap:**

-   Target type: Maintain below
-   Final target value \(Cap\): $1,500,000 per quarter
-   Check-in frequency: Quarterly \(4 periods\)
-   Quarterly costs: Q1=$1.2M, Q2=$1.1M, Q3=$1.3M, Q4=$1.5M \(all ≤ $1.5M\)
-   Achievement: \(4 ÷ 4\) × 100 = 100%

**When to use:** Cost caps, budget limits, error rate limits, support ticket backlog targets, emission caps.

## Maintain constant targets

A Maintain constant target succeeds when the actual value stays within a tolerance band around the planned target. The band is ±5% by default. Administrators can change it with the **sn\_gf.maintain\_constant\_tolerance\_percent** system property. Use this type for metrics that require stability and consistency.

**Tolerance band calculation:**

```
Success range = [Planned target − (|Planned target| × Tolerance %), Planned target + (|Planned target| × Tolerance %)]
```

**How achievement is calculated:**

```
Progress % = (Number of periods met ÷ Number of periods up to the latest period with an actual value) × 100
```

**Example — Employee headcount:**

-   Target type: Maintain constant
-   Final target value: 250 employees
-   Tolerance band: 237.5–262.5 employees \(±5% of 250\)
-   Check-in frequency: Monthly \(12 periods\)
-   Headcount by month: 11 months within 237.5–262.5 range, 1 month at 268 \(outside range\)
-   Achievement: \(11 ÷ 12\) × 100 = 92%

**When to use:** Staffing stability, quality score consistency, inventory levels, process performance, team capacity management.

## Milestone targets

Milestone targets are binary \(yes/no\) and measure qualitative achievement rather than numeric progression. A milestone is either complete \(Green\) or incomplete \(Red\).

**Achievement logic:**

-   Yes = Green \(100% achievement\)
-   No = Red \(0% achievement\)
-   Yellow status is not available for milestones

**Example — Project go-live milestone:**

-   Target: "Complete system deployment by Q4 2026"
-   Unit of Measure: Yes/No
-   Target Type: Milestone \(automatically set for Yes/No metrics\)
-   Result: Green if the deployment is complete; otherwise, Red.

**When to use:** Project milestones, regulatory approvals, capability certifications, system implementations, go-live dates, governance checkpoints.

## Progress and status calculation

For Maximize and Minimize targets, progress is calculated as a percentage and compared against the default thresholds in the following table to assign a status.

|Status|Default threshold|Meaning|
|------|-----------------|-------|
|Green|90% or higher|Target is on track or exceeded|
|Yellow|75–89%|Target is at risk; achievement below expectations|
|Red|Less than 75%|Target is significantly behind; immediate action needed|

Status is automatically calculated when you enter actual values. For Maintain targets, each breakdown period is Green when it meets its planned target and Red when it doesn't. The target status is based on the progress percentage, which is compared against the same thresholds as Maximize and Minimize targets \(90% for Green and 75% for Yellow by default\), so the target status can be Green, Yellow, or Red.

For detailed calculation examples for all target types, see [Automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/automatic-status-calculation-targets-spw.md).

## Target type selection

Ask yourself these questions when deciding on a target type:

1.  **Is your goal about growing or reducing a metric?** Choose **Maximize** \(growth\) or **Minimize** \(reduction\).
2.  **Is your goal about keeping something stable or within limits?** Choose one of the Maintain types:
    -   **Maintain above**: Must stay at or above a minimum
    -   **Maintain below**: Must stay at or below a maximum
    -   **Maintain constant**: Must stay within a range
3.  **Is your goal qualitative with a yes/no outcome?** Choose **Milestone**.
4.  **Do you need to track performance across multiple time periods?** Add a check-in frequency \(Daily, Weekly, Monthly, Quarterly, Yearly\) to any target type. Maintain targets especially benefit from check-in frequency to measure consistency across periods.

For examples of different scenarios and target type recommendations, see [Add targets for a goal in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/set-targets-for-goal-egm.md).

## Changing the type of a target

You can change the type of a target that already has actual values. A confirmation message appears before the change is applied.

-   When you change from one Maintain type to another, the actual values are kept and progress is recalculated.
-   When you change between **Maximize**, **Minimize**, and a Maintain type, the actual value and progress of the target are cleared, and any target breakdowns are regenerated without actual values.
-   When you change to **Milestone**, any target breakdowns are deleted.

For the steps, see [Change the type of a target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/change-target-type-gf.md).

## Target types and target automation

All target types support target automation, which auto-populates the **Actuals to date** field from a configured data source. Target automation is especially useful in the following scenarios:

-   Minimize targets pulling defect counts from issue tracking systems
-   Maximize targets pulling revenue figures from financial systems
-   Maintain targets pulling operational metrics from monitoring systems

For configuration guidance, see [Target actuals automation in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-actuals-automation-spw.md).

**Related topics**  


[Target form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/target-form.md)

[Create targets for a goal using Goal Framework or Goal Framework for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/set-targets-for-goal.md)

[Change the type of a target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/change-target-type-gf.md)

[Target breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/target-breakdowns-gf.md)

[Automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/automatic-status-calculation-targets.md)

[Configure the tolerance for Maintain constant targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/configure-maintain-constant-tolerance.md)

