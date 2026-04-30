---
title: Set up the deflection configuration for Self-Service Analytics
description: Associate a period of time with an activity context that defines how long a system will wait for a case to be created to match a deflection pattern.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Self-Service Analytics, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up the deflection configuration for Self-Service Analytics

Associate a period of time with an activity context that defines how long a system will wait for a case to be created to match a deflection pattern.

## Before you begin

[Configure activity patterns for Self-Service Analytics](configure-activity-pattern.md).

Role required: sn\_ssa\_core.self\_service\_manager

## Procedure

1.  Navigate to **All** &gt; **Self-Service Analytics** &gt; **Configuration** &gt; **Deflection Configuration**.

2.  In the Deflection Configurations list, search for and select the deflection configuration for your activity context.

    -   For customer contacts, select **Contact Case Deflection Configuration**.
    -   For consumers, select **Consumer Case Deflection Configuration**.
    -   For user entities other than consumers and customer contacts, click **New** to create another deflection configuration or modify an existing configuration.
3.  On the Deflection Configuration form, verify the default field values for an existing configuration or fill in the values for a custom configuration.

<table id="table_trj_yvb_4lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for your deflection configuration.

</td></tr><tr><td>

Activity Context

</td><td>

Type of activities for which you want to collect data. For more information, see [Configure activity contexts for Self-Service Analytics](configure-activity-context.md).

</td></tr><tr><td>

Description

</td><td>

Summary of the configuration.

</td></tr><tr><td>

Application

</td><td>

Scope of the application that contains the user entity. This field is automatically set based on the application scope selected in the application picker.

</td></tr><tr><td>

Window

</td><td>

Activity context window \(duration\) for tracking activities that match a deflection pattern.Example: To track the create case activity for a consumer within a day, set the window as 1 day.

 -   If the consumer created a case within that window, the deflection pattern matched is not a deflection.
-   If the consumer did not create a case within that window, the deflection pattern matched is a potential deflection.
-   If the consumer did not create a case and the last activity is submitted positive feedback for any self-service channel content within that window, the deflection pattern matched is a confirmed deflection.


</td></tr></tbody>
</table>4.  In the Deflection Patterns related list, add or modify existing deflection patterns to associate them with the deflection configuration or add a new pattern.

    This related list appears only if a deflection configuration exists.

5.  In the Deflection Metrics related list, add or modify an existing deflection metric table that stores the deflection data for an activity pattern associated with a deflection type.

    This related list appears only if a deflection configuration exists. Alternatively, you can also configure a deflection metric table by navigating to **Self-Service Analytics** &gt; **Deflection Metric**.

6.  On the Deflection Configuration form, click **Update**.


## What to do next

[Configure scheduled jobs for Self-Service Analytics](configure-scheduled-job-ssa.md).

**Parent Topic:**[Configure Self-Service Analytics](config-ssa.md)

