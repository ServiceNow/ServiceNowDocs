---
title: Automatic status calculation for targets
description: Automatically determine status for targets consequently rolling up to goals based on achievement percentages. Status is calculated when you enter actual values and achievement of actuals compared to the planned target against predefined thresholds \(Green, Yellow, Red\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/scenario-planning-in-spw/automatic-status-calculation-targets-spw.html
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 5
breadcrumb: [Goals in Strategic Planning, Explore, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Automatic status calculation for targets

Automatically determine status for targets consequently rolling up to goals based on achievement percentages. Status is calculated when you enter actual values and achievement of actuals compared to the planned target against predefined thresholds \(Green, Yellow, Red\).

## What is automatic status calculation?

When you enter actual values for a target period or a target breakdown, the system compares actual achievement against planned targets. The comparison uses predefined thresholds to automatically assign a status \(Green, Yellow, or Red\). This eliminates manual status selection, reduces data entry errors, and improves organizational governance.

Key benefits:

-   Eliminates manual status selection for every target entry
-   Ensures consistent status assignment across the portfolio
-   Reduces subjective judgment and data entry mistakes
-   Provides real-time status updates as actual values are entered
-   Supports better portfolio visibility and decision-making

\[Omitted image "image.automatic-status-calculation-spw"\] Alt text: Automatic status calculation in Strategic Planning

## How status is calculated

The system calculates target achievement percentage using a standardized formula that accounts for the start value \(baseline\) and planned target. The formula application depends on whether your target is designed to maximize or minimize performance:

-   **Maximize targets \(Revenue, growth, performance\)**

    For targets where higher values are better, use the standard achievement formula:

    ```
    Achievement % = ((Actual to date − Start Value) ÷ (Final target value − Start Value)) × 100
    ```

    **Example:** Revenue target from $1M \(start\) to $1.5M \(Final target\), actuals achieved $1.35M = 70% achievement

-   **Minimize targets \(Costs, defects, risk\)**

    For targets where lower values are better, the formula inverts to measure reduction:

    ```
    Achievement % = ((Start Value − Actuals to date) ÷ (Start Value − Final target value)) × 100
    ```

    **Example:** Cost reduction from $500K \(start\) to $400K \(final target\), actuals achieved $420K = 80% achievement


The resulting achievement percentage is compared against configured thresholds to assign status:

|Status|Default Threshold|Meaning|
|------|-----------------|-------|
|Green|90% or higher|Target is on track or exceeded|
|Yellow|75–89%|Target is at risk; achievement below expectations|
|Red|Less than 75%|Target is significantly behind; immediate action needed|

Administrators can customize threshold percentages to align with organizational governance policies and risk tolerance. Use the system property **sn\_gfa.target.auto\_status.thresholds** to adjust values.

**System property configuration:**

```
{"enabled": true, "thresholds": {"green": 90, "yellow": 75}}
```

For instructions on system property configuration, see [Configure automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/configure-automatic-status-calculation-spw.md).

## Status calculation scenarios

Status calculation applies to three target configurations:

-   **Targets without breakdowns:** Status is calculated once based on overall actual performance against the Final target value
-   **Targets with breakdowns \(check-ins\):** Status is calculated for each check-in period \(weekly, monthly, quarterly\) based on that period's achievement
-   **Targets without check-in frequency:** Status is calculated based on direct actuals without period-based accumulation

In all scenarios, the same achievement formula and thresholds apply. The difference is in how actual values are entered and aggregated across time periods. For more details on how the status is calculated for different scenarios, see [Status calculation specifications and examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/target-status-calculation-examples-spw.md).

## Milestone targets

Milestone targets track qualitative progress against defined maturity levels \(e.g., Planning, Execution, Delivery, Launch\) instead of using numeric formulas. Status is assigned manually based on whether current progress matches the defined milestone stage. Examples: project readiness, capability maturity, process implementation.

Milestone targets support only two status values:

-   **Green:** Current progress matches or exceeds the defined milestone stage
-   **Red:** Current progress lags behind or does not match the defined milestone stage

Yellow status is not available for milestone targets. Though not automatically calculated, milestone targets still roll up through the portfolio hierarchy using worst-wins logic and contribute to overall portfolio health.

## Manual override

Target owners can override the automatically calculated status values for a target breakdown, target, or goal when business circumstances require a different assessment. When you manually override a status:

-   The manually selected status displays in place of the calculated status
-   If you update the actual value after a manual override, the system recalculates the status automatically based on the new achievement percentage
-   The recalculated status may differ from your previous manual selection

Manual override provides flexibility while maintaining the ability to recalculate based on new data.

## Automatic status rollup

Status automatically rolls up through three layers of the portfolio hierarchy:

1.  **Breakdown → Target:** Status rolls up from individual check-ins to the target level. The rollup logic depends on the breakdown type:
    -   **Cumulative breakdowns:** Status uses *latest-wins* logic. The most recent period's status determines the target status.
    -   **Non-cumulative breakdowns:** Status uses *worst-wins* logic. The lowest-performing period's status determines the target status.
2.  **Target → Goal:** Status rolls up from targets to goals using a *worst-wins* logic. The lowest-performing target status determines the goal status.
3.  **Goal → Parent goal:** Status rolls up from goals through parent goals using *worst-wins* logic.

This three-layer cascade ensures portfolio leaders see a true picture of execution health. A red target immediately propagates as a red signal at the portfolio level, prioritizing attention on at-risk initiatives.

## Custom status values

In addition to automatic Green/Yellow/Red status, target owners can apply custom status values to reflect business context that the achievement formula may not capture. Custom statuses are retained even when automatic calculation is re-enabled, allowing manual judgment to coexist with system-driven calculations.

**Parent Topic:**[Goals in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/goal-management-in-alignment-planner-workspace.md)

**Related topics**  


[Status calculation specifications and examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/target-status-calculation-examples-spw.md)

[Configure automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/configure-automatic-status-calculation-spw.md)

