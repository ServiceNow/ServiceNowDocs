---
title: Configure automatic status calculation for targets
description: Configure system-wide automatic status calculation settings to determine target and goal status automatically based on achievement percentages. Enable or disable automatic calculation and customize Green, Yellow, and Red threshold values to align with your organizational governance policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/scenario-planning-in-spw/configure-automatic-status-calculation-spw.html
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Configure automatic status calculation for targets

Configure system-wide automatic status calculation settings to determine target and goal status automatically based on achievement percentages. Enable or disable automatic calculation and customize Green, Yellow, and Red threshold values to align with your organizational governance policies.

## Before you begin

Role required: admin

## About this task

Administraotrs can enable or disable the automatic status calculation feature. They can also customize the threshold percentages to align with organizational governance policies. Use the system property **sn\_gfa.target.auto\_status.thresholds** to adjust threshold values.

**Default system property value:**

```
{"enabled": true, "thresholds": {"green": 90, "yellow": 75}}
```

-   `enabled:` Set to `true` to enable automatic status calculation. Set to `false` to disable and revert to manual status selection.
-   `green:` Threshold percentage for Green status \(default: 90\)
-   `yellow:` Threshold percentage for Yellow status \(default: 75\)

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **System Properties**.

2.  Search for and open the **sn\_gfa.target.auto\_status.thresholds** system property.

3.  In the **Value** field, input as `true` or `false` as needed.

    The default value is **true**.

    Customize the threshold percentages for Green and Yellow statuses as needed.

4.  Select **Update** to save the changes.


**Parent Topic:**[Configuring goals in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/configuring-goal-framework-apw.md)

