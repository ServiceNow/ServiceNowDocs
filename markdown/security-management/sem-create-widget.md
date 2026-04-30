---
title: Create a custom widget
description: Create a custom widget in the Security exposure management \(SEM\) workspace to visualize findings data that meets your organization’s reporting needs. This feature enables administrators to extend the default widgets in the visualization library by adding new widgets that reflect organization-specific risk and exposure metrics.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 1
breadcrumb: [Configure Visualization library, Implement, Unified Security Exposure Management, Security Operations]
---

# Create a custom widget

Create a custom widget in the Security exposure management \(SEM\) workspace to visualize findings data that meets your organization’s reporting needs. This feature enables administrators to extend the default widgets in the visualization library by adding new widgets that reflect organization-specific risk and exposure metrics.

## Before you begin

-   Check that the visualization group limit set by the system property **sn\_sec\_sem.vizGroupLimit** \(default = 10 widgets in a group\) isn’t exceeded before adding a new widget.
-   Verify that the **Group by** value you plan to use doesn’t exist in another widget. The **Group by** field must be unique.

Role required: admin

## Procedure

1.  Navigate to **Security Exposure Management** &gt; **Administration** &gt; **Visualization library**.

2.  Select **New**.

3.  On the new Visualization widget form, enter the required details.

    For a full description of each field, see [Visualization widget fields](../../security-exposure-management-administration/reference/sem-vis-widget-fields.md).

4.  Select **Save**.


## Result

The widget is now saved to the Visualization Library and can be used when creating or editing dashboards.

**Note:**

-   You can create or update widgets in the Findings view, but not in the Remediation overview page. Widgets in the Remediation overview are predefined and cannot be created or edited. You can only change their display order or activate or deactivate them.
-   Only the widgets marked as **Active** appear in the dashboard creation view.

