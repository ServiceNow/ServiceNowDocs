---
title: View an alert analysis by Now Assist in Express List
description: View an alert analysis created by ServiceNow Now Assist using generative AI. Alert analyses include a human-readable brief of the alert and technical information to help you investigate the alert more effectively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-operations-management/service-operations-workspace-for-itom-apps/alert-simplification-el.html
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# View an alert analysis by Now Assist in Express List

View an alert analysis created by ServiceNow® Now Assist using generative AI. Alert analyses include a human-readable brief of the alert and technical information to help you investigate the alert more effectively.

## Before you begin

-   Install the ITOM plugin in the Now Assist feature. For more information, see [Install the Now Assist for IT Operations Management \(ITOM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/now-assist-for-it-operations-management/install-now-assist-itom.md).
-   View important information about the ServiceNow® Now Assist for IT Operations Management \(ITOM\) application in [Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md).

**Note:** Currently, Now Assist for ITOM only analyzes tag-based, rule-based, and Log Analytics alert groups. For all other alert group types, it only analyzes the parent alert.

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express List icon \(\[Omitted image "express-list1.png"\] Alt text: Express List icon\).

3.  In the Active alerts list, select the information icon \(\[Omitted image "info.png"\] Alt text: Information icon.\) for an alert.

4.  On the preview panel Info tab, select **Analyze** in Alert analysis by Now Assist.

5.  View the information provided in the Alert analysis.

    **Note:** Alert analyses are provided in English, irrespective of the language used in the alert description.

6.  Use the Alert analysis icons to perform related tasks.

<table id="table_om4_wwz_n1c"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Omitted image "icon-copy-to-clipboard.png"\] Alt text: Copy to clipboard icon.

</td><td>

Copy the content of the alert analysis to the clipboard.

</td></tr><tr><td>

\[Omitted image "icon-refresh-alert-summary.png"\] Alt text: Refresh icon.

</td><td>

Refresh the alert analysis.**Note:** Refreshing regenerates the results. Past results are deleted.

</td></tr></tbody>
</table>
