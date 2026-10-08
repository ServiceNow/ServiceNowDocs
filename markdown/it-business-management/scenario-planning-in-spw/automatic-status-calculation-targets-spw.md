---
title: Automatic status calculation for targets
description: Target status is calculated automatically from achievement percentages when you enter actual values, and it rolls up to goals using Green, Yellow, and Red thresholds.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/automatic-status-calculation-targets-spw.html
release: brazil
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 7
breadcrumb: [Goals in Strategic Planning, Explore, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Automatic status calculation for targets

Target status is calculated automatically from achievement percentages when you enter actual values, and it rolls up to goals using Green, Yellow, and Red thresholds.

## Status calculation basics

When you enter actual values for a target period or a target breakdown, the system compares actual achievement against planned targets. The comparison uses predefined thresholds to automatically assign a status \(Green, Yellow, or Red\).

Key benefits:

-   Eliminates manual status selection for every target entry
-   Applies status consistently across the goal hierarchy
-   Reduces subjective judgment and data entry mistakes
-   Provides real-time status updates as actual values are entered
-   Supports better portfolio visibility and decision-making

\[Omitted image "automatic-status-calculation-spw.gif"\] Alt text: Automatic status calculation in Strategic Planning.

## Status calculation formulas

The system calculates target achievement percentage using a standardized formula that accounts for the start value \(baseline\) and planned target. The formula application depends on whether the target type is Maximize, Minimize, or one of the Maintain types:

-   **Maximize targets \(revenue, growth, performance\)**

    For targets where higher values are better, the standard achievement formula applies:

    ```
    Achievement % = ((Actual to date − Start Value) ÷ (Final target value − Start Value)) × 100
    ```

    **Example:** Revenue target from $1M \(start\) to $1.5M \(final target\), actuals achieved $1.35M = 70% achievement

-   **Minimize targets \(costs, defects, risk\)**

    For targets where lower values are better, the formula inverts to measure reduction:

    ```
    Achievement % = ((Start Value − Actuals to date) ÷ (Start Value − Final target value)) × 100
    ```

    **Example:** Cost reduction from $500K \(start\) to $400K \(final target\), actuals achieved $420K = 80% achievement

-   **Maintain targets \(Maintain above, Maintain below, Maintain constant\)**

    For targets where a metric must be maintained at a specific level or within a range, progress is calculated differently. Achievement is based on how many breakdown periods meet their planned target. A period is met based on the target type: at or above the planned target \(Maintain above\), at or below the planned target \(Maintain below\), or within the tolerance band of the planned target \(Maintain constant\). Periods after the latest period with an actual value aren't counted; earlier periods without an actual value count as not met:

    ```
    Progress % = (Number of periods met ÷ Number of periods up to the latest period with an actual value) × 100
    ```

    **Maintain above example:** Service uptime target to maintain above 98% over 12 months. Actuals are entered for all 12 months, and uptime was at or above 98% in 10 of them = \(10 ÷ 12\) × 100 = 83% progress

    **Maintain below example:** Operating cost target to maintain below $5M over 4 quarters. Actuals are entered for all 4 quarters, and costs stayed at or below $5M in 3 of them = \(3 ÷ 4\) × 100 = 75% progress

    **Maintain constant example:** Employee headcount target to maintain at 250 staff \(default ±5% tolerance = 237.5–262.5\) over 12 months. Actuals are entered for all 12 months, and headcount was within range for 11 of them = \(11 ÷ 12\) × 100 = 92% progress


The resulting achievement percentage is compared against configured thresholds to assign the status.

For Maintain targets, each breakdown period is Green when it meets its planned target and Red when it doesn't. The target status is based on the progress percentage, which is compared against the same thresholds, so the target status can be Green, Yellow, or Red. For Maintain constant targets, the tolerance band is ±5% by default and is set by the **sn\_gf.maintain\_constant\_tolerance\_percent** system property.

|Status|Default threshold|Meaning|
|------|-----------------|-------|
|Green|90% or higher|Target is on track or exceeded|
|Yellow|75–89%|Target is at risk; achievement below expectations|
|Red|Less than 75%|Target is significantly behind; immediate action needed|

Administrators can customize threshold percentages to align with organizational governance policies and risk tolerance. Use the system property **sn\_gfa.target.auto\_status.thresholds** to adjust values.

**System property configuration:**

```
{"enabled": true, "thresholds": {"green": 90, "yellow": 75}}
```

For instructions on system property configuration, see [Configure automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/configure-automatic-status-calculation-spw.md).

## Status calculation scenarios

Status calculation applies to the following target configurations:

-   **Targets without breakdowns:** Status is calculated once based on overall actual performance against the final target value. For Maintain-type targets, the status is Green when the actual value meets the final target value \(at or above for Maintain above, at or below for Maintain below, or within the tolerance band for Maintain constant\) and Red when it doesn't.
-   **Targets with breakdowns \(check-ins\):** Status is calculated for each check-in period \(such as weekly, monthly, or quarterly\) based on that period's achievement. For Maintain-type targets, each period is marked Green or Red depending on whether it meets its planned target. The target status is based on progress, which is the percentage of periods met, compared against the same thresholds.
-   **Targets without check-in frequency:** Status is calculated from the actual values directly, without period-based accumulation.

For Maximize and Minimize targets, the same achievement formula and thresholds apply in all scenarios. The difference is in how actual values are entered and aggregated across time periods. For more details on how the status is calculated for different scenarios, see [Status calculation specifications and examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-status-calculation-examples-spw.md).

## Milestone targets

Milestone targets track qualitative progress with a Yes or No value instead of a numeric formula. You determine whether the milestone has been achieved:

-   **Green:** If the target is achieved, the value is set to **Yes**.
-   **Red:** If the target isn't achieved, the value is set to **No**.

Yellow status is not available for milestone targets. Examples include project readiness gates, regulatory approvals, or capability certifications where achievement is binary \(complete or not complete\). Though not automatically calculated, milestone targets roll up from the target to its goal, and from the goal to parent goals if any, using worst-wins logic.

## Manual override

Target owners can override the automatically calculated status values for a target breakdown, target, or goal when business circumstances require a different assessment. When you manually override a status:

-   The manually selected status displays in place of the calculated status
-   If you update the actual value after a manual override, the system recalculates the status automatically based on the new achievement percentage
-   The recalculated status may differ from your previous manual selection

Manual override provides flexibility while maintaining the ability to recalculate based on new data.

## Automatic status rollup

Status automatically rolls up through three hierarchical layers:

1.  **Breakdown → Target:** Status rolls up from individual check-ins to the target level. When a target has period-based breakdowns \(such as quarterly check-ins\), each breakdown period receives its own status calculation. The target's overall status is then determined by aggregating these individual breakdown statuses. How the statuses are aggregated depends on whether the target's breakdowns are cumulative or non-cumulative:
    -   **Cumulative breakdowns:** Status uses *latest-wins* logic. The most recent period's status determines the target status.
    -   **Non-cumulative breakdowns:** The target's overall status is based on the combined performance across all reported breakdown periods.
2.  **Target → Goal:** Status rolls up from targets to goals using a *worst-wins* logic. The lowest-performing target status determines the goal status.
3.  **Goal → Parent goal:** Status rolls up from goals through parent goals using *worst-wins* logic.

Because of this three-layer rollup, a Red target status appears at the parent goal level, which helps portfolio leaders focus on at-risk goals.

## Custom status values

In addition to automatic Green/Yellow/Red status, target owners can apply custom status values to reflect business context that the achievement formula may not capture. Custom statuses are retained even when automatic calculation is re-enabled, allowing manual judgment to coexist with system-driven calculations.

**Parent Topic:**[Goals in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/goal-management-in-alignment-planner-workspace.md)

**Related topics**  


[Status calculation specifications and examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-status-calculation-examples-spw.md)

[Configure automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/configure-automatic-status-calculation-spw.md)

