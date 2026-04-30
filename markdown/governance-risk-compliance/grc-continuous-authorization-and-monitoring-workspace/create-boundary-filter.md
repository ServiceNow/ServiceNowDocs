---
title: Create a boundary filter
description: Create boundary filters to define system elements within an authorization boundary based on specific table conditions.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [View authorization boundary details, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Create a boundary filter

Create boundary filters to define system elements within an authorization boundary based on specific table conditions.

## Before you begin

Role required: sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.information\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.sec\_control\_assessor, sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.scheduler, sn\_irm\_cont\_auth.system\_user, sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.executive\_read

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** and then select the lists icon \(![Lists icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\).

2.  From the Authorization boundaries in the Risk Management Framework \(RMF\) list, select an authorization boundary record.

3.  In the **Boundary Filters** related list, select **New**.

    ![New boundary filter.](../image/auth-bound-filter1.png)

4.  In the **Create New Boundary Filter** form, fill in the fields.

    |Fields|Descriptions|
    |------|------------|
    |Filter name|The name of the boundary filter.|
    |Authorization boundary|The authorization boundary to which this filter belongs. This field is automatically populated based on the parent record.|
    |Dynamic Filter|Select the **Dynamic Filter** option to create a filter that automatically updates based on the conditions you define. When selected, the filter operates dynamically and updates system elements daily. When **Dynamic Filter** option is cleared, the filter creates system elements that meet the conditions at the time you select **Save**. The system element doesn’t update automatically update the system elements.|
    |Table|The table you select determines which fields are available when defining filter conditions and which records the filter can evaluate. You must select a table before you can define filter conditions. For dynamic filters, the selected table is evaluated daily to update system elements based on changes that might affect which records meet the filter conditions.|

    ![Entering filter details.](../image/auth-bound-filter2.png)

    **Filter condition**: Select **Set conditions** define your conditions using field values, operators, and AND/OR logic. For dynamic filters, these conditions are evaluated daily, and system elements are automatically added or removed. For static filters, the conditions are evaluated only once at the time of boundary filter creation.

    You can select **View matching results** to preview the system elements that match your conditions before saving.

    ![Adding filter conditions.](../image/auth-bound-filter3.png)

5.  Select **Save**.

    The boundary filter is created and, if configured as a dynamic filter, begins automatically including assets that meet the specified conditions.


## Result

Assets matching the filter conditions are automatically listed in the **System Elements** related list.

**Parent Topic:**[View authorization boundary details](auth-bound-overview-ws.md)

