---
title: Automation Center Overview dashboard
description: The Automation Center Workspace landing page is the Overview dashboard, which contains basic score cards, lists, and reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/automation-center/overview-dash.html
release: australia
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workspace, Explore, Automation Center, Workflow Data Fabric]
---

# Automation Center Overview dashboard

The Automation Center Workspace landing page is the Overview dashboard, which contains basic score cards, lists, and reports.

You can access the Overview dashboard in either of two ways:

-   By navigating to **All** &gt; **Automation Center** &gt; **Automation Center Home** &gt; **Overview**.
-   By navigating to **Workspaces** &gt; **Automation Center Workspace** &gt; **Overview**.

## Active automations

Active automations provides details of all the active automations from different sources and their business criticality. You can filter the data to view information within a specific date range, for a specific automation, or for a specific department. After you set the filter, the results will be displayed only for the specified filter. If you don’t set any filter, then data for all active automations is displayed.

The Active automations section provides reports with the following details in the form of chart.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deployed automations by business criticality

</td><td>

This chart displays data about all active automations. It also provides details about the business criticality of each of the automation. This helps you in understanding how many automations are highly critical and how many aren’t.\[Omitted image "overview-deploy-auto.png"\] Alt text: Deployed automations by business criticality

</td></tr><tr><td>

Executions summaries by source

</td><td>

Automation Center supports data from several sources, such as ServiceNow Flow, ServiceNow RPA, and other third-party sources. This chart provides execution summary details of all active automations along with their sources. This information helps you in evaluating from which sources you’re getting data and how many automations from each of the sources are active.\[Omitted image "overview-exe-source.png"\] Alt text: Executions summaries by source

</td></tr><tr><td>

Robotic Process Automation \(RPA\) by source

</td><td>

This chart displays the automations for all RPAs grouped by sources. The graph gives details of the time lines when the RPA data was sent to Automation Center.\[Omitted image "overview-rpa-source.png"\] Alt text: Robotic Process Automation RPA by source

</td></tr><tr><td>

Automations by ServiceNow Flow

</td><td>

This chart provides details of the ServiceNow flow automations with the time lines.\[Omitted image "overview-flow.png"\] Alt text: Automations by ServiceNow Flow

</td></tr><tr><td>

Document Intelligence \(DocIntel\)

</td><td>

This chart provides details of the Document Intelligence automations with the time lines.\[Omitted image "overview-docintel.png"\] Alt text: Document Intelligence DocIntel

</td></tr><tr><td>

Top 10 applications used

</td><td>

This graph provides a vertical bar report of the top 10 business applications used. For more information on associating business applications to your automations, see .\[Omitted image "overview-top10.png"\] Alt text: Top 10 applications used

</td></tr></tbody>
</table>## Spokes &amp; Transactions

Spokes &amp; Transactions section provides details about the spokes and the transactions that are available on your instance.

**Note:** To view the data in the Spokes &amp; Transactions section, you need to have the sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin role.

<table id="id_ojr_yyl_c2c"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total entitled spokes

</td><td>

Displays the number of spokes that you are entitled and installed in your instance.\[Omitted image "overview-spoke1.png"\] Alt text: Total entitled spokes

</td></tr><tr><td>

Installed spokes

</td><td>

Displays the number of spokes that are installed in your instance.\[Omitted image "overview-spoke2.png"\] Alt text: Installed spokes

</td></tr><tr><td>

Configured spokes

</td><td>

Displays the number of spokes for which connections are configured in your instance.\[Omitted image "overview-spoke3.png"\] Alt text: Configured spokes

</td></tr><tr><td>

Total entitled transactions

</td><td>

Displays the number of transactions that are available for use.\[Omitted image "overview-spoke-4.png"\] Alt text: Total entitled transactions

</td></tr><tr><td>

Consumed transactions

</td><td>

Displays the number of transactions that you have used.\[Omitted image "overview-spoke-5.png"\] Alt text: Consumed transactions

</td></tr><tr><td>

Applications with most transactions

</td><td>

Displays the applications \(scope applications\) with most transactions.You can filter the results for specific time period. By default, the last one month's data is displayed.

\[Omitted image "overview-spoke6.png"\] Alt text: Applications with most transactions

</td></tr><tr><td>

Spokes with most transactions

</td><td>

Displays the spokes with most transactions.You can filter the results for specific time period. By default, the last one month's data is displayed.

\[Omitted image "overview-spoke7.png"\] Alt text: Spokes with most transactions

</td></tr></tbody>
</table>## Future automations

The Future automations section provides details about all active automations that are planned for the future.

You can filter the data by department. If no department is selected, the data is displayed for all departments.

|Section|Description|
|-------|-----------|
|New requests|Displays all automation requests that are in the New state.\[Omitted image "overview-future-1.png"\] Alt text: New requests|
|Requests by intake source|Displays all automation requests grouped by intake source, such as Web, Process Mining, or Service Request.\[Omitted image "overview-future-2.png"\] Alt text: Requests by intake source|
|Requests to be deployed|Displays the automation requests ready to be deployed.\[Omitted image "overview-future-3.png"\] Alt text: Requests to be deployed|
|Most recent requests|Lists the automation requests sorted from most recent to oldest.\[Omitted image "overview-future-4.png"\] Alt text: Most recent requests|

**Parent Topic:**[Automation Center Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/automation-center-workspace-ui.md)

