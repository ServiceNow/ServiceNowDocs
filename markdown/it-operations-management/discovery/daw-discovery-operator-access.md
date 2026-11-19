---
title: Discovery Operator role access in Discovery Admin Workspace
description: The discovery\_operator role provides read-only access to the Discovery Admin Workspace. Users with this role can monitor Discovery health, investigate failures, and validate results without changing the Discovery configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/daw-discovery-operator-access.html
release: brazil
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-10-21"
reading_time_minutes: 3
keywords: [Discovery, Admin, Workspace, discovery\_operator]
breadcrumb: [Discovery Admin Workspace reference, Discovery reference, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Operator role access in Discovery Admin Workspace

The discovery\_operator role provides read-only access to the Discovery Admin Workspace. Users with this role can monitor Discovery health, investigate failures, and validate results without changing the Discovery configuration.

**Note:** Access for the discovery\_operator role is available starting with Discovery Admin Workspace v1.23.0.

<table id="daw-discovery-operator-access-table"><thead><tr><th>

Page or tab

</th><th>

Available actions

</th><th>

Restricted actions

</th></tr></thead><tbody><tr><td>

[Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-admin-workspace-home.md)

</td><td>

View the Quick overview data counts, top Discovery errors, and installed ITOM Visibility apps.

</td><td>

Onboarding for Discovery, Discovery tuning advice, Quick Discovery, and the option to install apps.

</td></tr><tr><td>

[Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-admin-workspace-schedules.md): Overview tab

</td><td>

View schedule visualizations, Discovery status, and anomalies.

</td><td>

**Quick Discovery** and **New Discovery**.

</td></tr><tr><td>

[Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-admin-workspace-schedules.md): IP-based discovery tab

</td><td>

View IP-based Discovery schedules.

</td><td>

Items that require attention, including the **Review missing coverage** option and, depending on your IPAM configuration, the **Review in Settings** or **View and activate schedules** option.

</td></tr><tr><td>

[Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-admin-workspace-schedules.md): Cloud discovery and Certificate discovery tabs

</td><td>

View cloud and certificate Discovery schedules.

</td><td>

The **Delete** option.

</td></tr><tr><td>

[Schedule details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/c_daw-disco-schedule-details.md)

</td><td>

View schedule details and run history, and select **Discover now** to run the schedule.

</td><td>

**Save**, **Quick ranges**, **Edit**, and **Delete**.

</td></tr><tr><td>

[IP inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/daw-ip-inventory.md)

</td><td>

View IP data and select **Export**.

</td><td>

**New** and **Add to Range Set**.

</td></tr><tr><td>

[Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md): Errors tab

</td><td>

View and filter errors, open error details, and view the AI Insights panel.**Note:** The AI Insights panel displays only when ServiceNow Otto for Error Framework is enabled. If the plugin isn't enabled, the panel displays a prompt to enable it. For more information, see [Error Framework in Discovery Admin Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/error-framework-daw.md).

</td><td>

None.

</td></tr><tr><td>

[Error details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/daw-error-details.md): Errors tab

</td><td>

View, filter, sort, group, and export error instances. Change error states using the **Mark error as** drop-down menu in the Error details panel.

</td><td>

Options in the **Actions** drop-down menu. Available actions vary by error type.

</td></tr><tr><td>

[Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md): Anomaly detection tab

</td><td>

View schedules with anomalies and filter the anomaly list.

</td><td>

The **Actions** drop-down menu, including **Clear all anomalies**.

</td></tr><tr><td>

[Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-admin-workspace-insights.md)

</td><td>

View insights that are available based on installed plugins and instance configuration. Export list data from available insights.

</td><td>

Command validation task and SaCmdManager. Insights for applications that aren't installed. The **Access store app** option. Actions other than export in installed applications.

</td></tr><tr><td>

[Content 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-workspace-content-360.md), [Tuning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-admin-workspace-tuning.md), and [Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/discovery-admin-workspace-setup.md)

</td><td>

None. These pages don't appear in the workspace navigation.

</td><td>

All features on these pages.

</td></tr></tbody>
</table>**Parent Topic:**[Discovery Admin Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/r_discovery-admin-workspace-reference.md)

