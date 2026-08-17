---
title: View an alert analysis by ServiceNow Otto in Express List
description: View an alert analysis created using generative AI. Alert analyses include a human-readable brief of the alert and technical information to help you investigate the alert more effectively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/alert-summary-now-assist-express-list.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [generative AI for IT Operations Management, generative AI for ITOM, alert analysis, Express List]
breadcrumb: [Respond to alerts, Express List in SOW for ITOM, Event Management, ITOM AIOps, IT Operations Management]
---

# View an alert analysis by ServiceNow Otto in Express List

View an alert analysis created using generative AI. Alert analyses include a human-readable brief of the alert and technical information to help you investigate the alert more effectively.

## Before you begin

Install the ServiceNow Otto for ITOM plugin. For more information, see [Install the ServiceNow Otto for IT Operations Management \(ITOM\) application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/install-now-assist-itom.md).

**Note:** Currently, ServiceNow Otto for ITOM only supports tag-based, CMDB, Log Analytics, Mixed, Automated, and Network Traffic-based alert groups. For all other alert group types, it only analyzes the parent alert.

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the navigation bar, select the Express List icon \(\[Omitted image "express-list1.png"\] Alt text: Express List icon.\).

3.  In the Active alerts list, select the information icon \(\[Omitted image "info.png"\] Alt text: Information icon.\) next to the alert.

4.  On the preview panel **Info** tab, select **Analyze** in Alert analysis by ServiceNow Otto.

5.  View the information provided in the Alert analysis.

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
