---
title: Automation Center Overview dashboard
description: The Automation Center Workspace landing page is the Overview dashboard, which contains basic score cards, lists, and reports.
locale: en-US
release: yokohama
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Automation Center Workspace, Exploring Automation Center, Automation Center, Data and Automation]
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

This chart displays data about all active automations. It also provides details about the business criticality of each of the automation. This helps you in understanding how many automations are highly critical and how many aren’t.![Deployed automations by business criticality](../images/overview-deploy-auto.png)

</td></tr><tr><td>

Executions summaries by source

</td><td>

Automation Center supports data from several sources, such as ServiceNow Flow, ServiceNow RPA, and other third-party sources. This chart provides execution summary details of all active automations along with their sources. This information helps you in evaluating from which sources you’re getting data and how many automations from each of the sources are active.![Executions summaries by source](../images/overview-exe-source.png)

</td></tr><tr><td>

Robotic Process Automation \(RPA\) by source

</td><td>

This chart displays the automations for all RPAs grouped by sources. The graph gives details of the time lines when the RPA data was sent to Automation Center.![Robotic Process Automation RPA by source](../images/overview-rpa-source.png)

</td></tr><tr><td>

Automations by ServiceNow Flow

</td><td>

This chart provides details of the ServiceNow flow automations with the time lines.![Automations by ServiceNow Flow](../images/overview-flow.png)

</td></tr><tr><td>

Document Intelligence \(DocIntel\)

</td><td>

This chart provides details of the Document Intelligence automations with the time lines.![Document Intelligence DocIntel](../images/overview-docintel.png)

</td></tr><tr><td>

Top 10 applications used

</td><td>

This graph provides a vertical bar report of the top 10 business applications used. For more information on associating business applications to your automations, see [Business application relationship with CIs for application information](https://www.servicenow.com/docs/access?context=application-relations&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US).![Top 10 applications used](../images/overview-top10.png)

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

Displays the number of spokes that you are entitled and installed in your instance.![Total entitled spokes](../images/overview-spoke1.png)

</td></tr><tr><td>

Installed spokes

</td><td>

Displays the number of spokes that are installed in your instance.![Installed spokes](../images/overview-spoke2.png)

</td></tr><tr><td>

Configured spokes

</td><td>

Displays the number of spokes for which connections are configured in your instance.![Configured spokes](../images/overview-spoke3.png)

</td></tr><tr><td>

Total entitled transactions

</td><td>

Displays the number of transactions that are available for use.![Total entitled transactions](../images/overview-spoke-4.png)

</td></tr><tr><td>

Consumed transactions

</td><td>

Displays the number of transactions that you have used.![Consumed transactions](../images/overview-spoke-5.png)

</td></tr><tr><td>

Applications with most transactions

</td><td>

Displays the applications \(scope applications\) with most transactions.You can filter the results for specific time period. By default, the last one month's data is displayed.

![Applications with most transactions](../images/overview-spoke6.png)

</td></tr><tr><td>

Spokes with most transactions

</td><td>

Displays the spokes with most transactions.You can filter the results for specific time period. By default, the last one month's data is displayed.

![Spokes with most transactions](../images/overview-spoke7.png)

</td></tr></tbody>
</table>## Future automations

The Future automations section provides details about all active automations that are planned for the future.

You can filter the data by department. If no department is selected, the data is displayed for all departments.

|Section|Description|
|-------|-----------|
|New requests|Displays all automation requests that are in the New state.![New requests](../images/overview-future-1.png)|
|Requests by intake source|Displays all automation requests grouped by intake source, such as Web, Process Mining, or Service Request.![Requests by intake source](../images/overview-future-2.png)|
|Requests to be deployed|Displays the automation requests ready to be deployed.![Requests to be deployed](../images/overview-future-3.png)|
|Most recent requests|Lists the automation requests sorted from most recent to oldest.![Most recent requests](../images/overview-future-4.png)|

**Parent Topic:**[Automation Center Workspace](automation-center-workspace-ui.md)

