---
title: View data on impacted services on the preview panel in Express List
description: View extra information on the preview panel about impacted services that are bound to alerts.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [Express List, alert, preview panel, impacted services]
breadcrumb: [Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# View data on impacted services on the preview panel in Express List

View extra information on the preview panel about impacted services that are bound to alerts.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express List icon \(![Express List icon](../../event-management/image/express-list1.png)\).

3.  In the Active alerts list, select an alert check-box.

4.  On the preview panel, open the Info tab.

5.  Hover over the Impacted services section to display information icons.

    ![Impacted services on the preview panel Info tab.](../image/el-impacted-services-info.png)

6.  Select the relevant icon to display extra information on an impacted service.

<table id="table_d2k_t4f_xbc"><thead><tr><th>

Icon

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Info icon.](../image/el-info-icon.png)

</td><td>

Info

</td><td>

Displays the severity, the business criticality, and a short description of the impacted service. From this pop-up, you can open the service map in Service Operations Workspace by selecting **View service map**.

![View service map link on the Impacted Services pop-up.](../image/el-impacted-services-popup.png)

The service map shows the impacted path of alerts, enabling you to quickly assess their effect on the service. For more information, see [View unified service map and the impact paths in Service Operations Workspace](view-impact-tree.md).

If metrics data exists for this service, you can open the Metric Explorer from the pop-up by selecting **View related metrics**.

</td></tr><tr><td>

![Contact person/group icon.](../image/el-contact-person-icon.png)

</td><td>

Contact person/group

</td><td>

Displays the name of the owner of the impacted service and the support group assigned to it.

</td></tr></tbody>
</table>
