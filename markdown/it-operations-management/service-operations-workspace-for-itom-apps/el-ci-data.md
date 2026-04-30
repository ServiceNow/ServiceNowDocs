---
title: View data on configuration items on the preview panel in Express List
description: View additional details about configuration items \(CIs\) that are bound to alerts on the Express List preview panel.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dependency View maps, Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View data on configuration items on the preview panel in Express List

View additional details about configuration items \(CIs\) that are bound to alerts on the Express List preview panel.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: ![Express list icon](../../event-management/image/express-list1.png).

3.  In the **Active Alerts** list, select an alert check box.

4.  On the preview panel, select the **Info** tab to view it.

5.  Hover over the Configuration item name to display information icons.

    ![Configuration item on the preview panel Info tab.](../image/el-ci-info.png)

6.  Display additional information on a CI by selecting the relevant icon.

<table id="table_myp_qmh_vcc"><thead><tr><th>

Icon

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Additional information icon.](../image/el-info-icon.png)

</td><td>

Additional information

</td><td>

Shows the class, IP address, location, and environment of the CI.From the pop-up, you can open the CI topology map in Service Operations Workspace by selecting **View CI topology**.

If metrics data exists for this service, you can open the Metric Explorer from the pop-up by selecting **View related metrics**.

</td></tr><tr><td>

![Contact information icon.](../image/el-contact-person-icon.png)

</td><td>

Contact person/group

</td><td>

Shows the name of the owner of the CI, the support group assigned to it, and avatars of the individual team members.

</td></tr></tbody>
</table>7.  Select the Additional information icon ![Additional information icon.](../image/el-info-icon.png) and then select **View CI topology**.![Configuration information additional information options.](../image/configuration-item-information.png)

    The **Dependency View** map opens. The map visually represents the relationships between CIs, helping you understand how different components are interconnected.


**Parent Topic:**[Dependency View maps](../concept/dependency-maps.md)

