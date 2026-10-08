---
title: Configure the tolerance for Maintain constant targets
description: Change the tolerance band that determines whether a Maintain constant target is on target. The default tolerance is ±5%.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/configure-maintain-constant-tolerance-spw.html
release: brazil
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Maintain constant, tolerance band, target type, system property]
breadcrumb: [Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Configure the tolerance for Maintain constant targets

Change the tolerance band that determines whether a Maintain constant target is on target. The default tolerance is ±5%.

## Before you begin

Role required: admin

## About this task

A Maintain constant target is on target when the actual value stays within a tolerance band around the planned target. Administrators can change it with the **sn\_gf.maintain\_constant\_tolerance\_percent** system property.

The tolerance is a percentage of the planned target. For example, if the planned target is 250 and the tolerance is 10%, an actual value from 225 to 275 meets the target for that period.

For more information about how Maintain constant targets are evaluated, see [Target types and achievement strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-types-overview.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **System Properties**.

2.  Search for and open the **sn\_gf.maintain\_constant\_tolerance\_percent** system property.

3.  In the **Value** field, enter the tolerance percentage as a whole number.

    For example, enter 10 for a tolerance of ±10%. The default value is 5.

4.  Select **Update** to save the changes.


## Result

Maintain constant targets use the new tolerance when the status of a target breakdown period is calculated.

**Parent Topic:**[Configuring goals in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/configuring-goal-framework-apw.md)

**Related topics**  


[Target types and achievement strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/target-types-overview.md)

[Configure automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/configure-automatic-status-calculation-spw.md)

