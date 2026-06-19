---
title: View data on impacted services on the preview panel in Express List
description: View extra information on the preview panel about impacted services that are bound to alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-operations-workspace-for-itom-apps/el-impacted-services-data.html
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View data on impacted services on the preview panel in Express List

View extra information on the preview panel about impacted services that are bound to alerts.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon \[Omitted image "express-list1.png"\].

3.  In the Active alerts list, select an alert check-box.

4.  On the preview panel, open the Info tab.

5.  Hover over the Impacted services section to display information icons.

    \[Omitted image "el-impacted-services-info.png"\] Alt text: Impacted services on the preview panel Info tab.

6.  Select the relevant icon to display extra information on an impacted service.

<table id="table_d2k_t4f_xbc"><thead><tr><th>

Icon

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Omitted image "el-info-icon.png"\] Alt text: Info icon.

</td><td>

Info

</td><td>

Displays the severity, the business criticality, and a short description of the impacted service. From this pop-up, you can open the service map in Service Operations Workspace by selecting **View service map**.

\[Omitted image "el-impacted-services-popup.png"\] Alt text: View service map link on the Impacted Services pop-up.

The service map shows the impacted path of alerts, enabling you to quickly assess their effect on the service. For more information, see [View unified service map and the impact paths in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/view-impact-tree.md).

If metrics data exists for this service, you can open the Metric Explorer from the pop-up by selecting **View related metrics**.

</td></tr><tr><td>

\[Omitted image "el-contact-person-icon.png"\] Alt text: Contact person/group icon.

</td><td>

Contact person/group

</td><td>

Displays the name of the owner of the impacted service and the support group assigned to it.

</td></tr></tbody>
</table>
