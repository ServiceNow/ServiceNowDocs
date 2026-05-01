---
title: Use the Orchestration Usage dashboard
description: This dashboard shows an overview of Orchestration usage metrics to show customers how their organization uses Orchestration and to support license compliance.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use the Orchestration Usage dashboard

This dashboard shows an overview of Orchestration usage metrics to show customers how their organization uses Orchestration and to support license compliance.

## Before you begin

Role required: orchestration\_manager

## Procedure

1.  To view the dashboard, navigate to **Orchestration** &gt; **Operations &amp; Troubleshooting** &gt; **Orchestration Usage Dashboard**.

    The Orchestration Usage dashboard is displayed. The tabs on the dashboard include Licensable Usage and Orchestration Usage. Reports on these tabs include:

<table id="table_zrt_5qy_pz"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Transaction Summary Last 12 months

</td><td>

A running transaction count of all Orchestration transactions over the last 12 months. Includes: -   The count of orchestration transactions associated with the HR Application
-   The count of Orchestration transactions associated with the Security Operations Application


</td></tr><tr><td>

Transaction Summary YTD

</td><td>

Cumulative count of all transactions since the time the Orchestration plugin was activated or the customer upgraded to Geneva.

</td></tr><tr><td>

365 day Running Average of Server

</td><td>

The running average over the last 365 days for cmdb\_ci\_computer - cmdb\_ci\_server. This includes all physical and virtual client nodes and excludes server nodes from the count.

</td></tr><tr><td>

365 day Running Average of Client

</td><td>

The running average over the last 365 days for cmdb\_ci\_server. This includes all physical and virtual server nodes.

</td></tr><tr><td>

Orchestration Transactions by Month for Last 12 Months

</td><td>

 

</td></tr><tr><td>

Average Client Nodes Orchestrated Last 365 Days

</td><td>

 

</td></tr><tr><td>

Average Server Nodes Orchestrated Last 365 Days

</td><td>

 

</td></tr><tr><td>

Number of Orchestration Activities Developed Last 365 Days

</td><td>

The aggregate number of activity definitions you have developed and OOB activity definitions you have modified. This number includes activity elements \(Activities build with the Activity Designer\) you have developed and OOB activity definitions you have modified. **Note:** his number excludes activity elements that are shipped with ServiceNow Applications that use the Orchestration Runtime e.g. ServiceNow Security Operations and Human Resources Apps.

</td></tr><tr><td>

Cumulative Client Nodes Orchestrated by Month

</td><td>

 

</td></tr><tr><td>

Cumulative Server Nodes Orchestrated by Month

</td><td>

 

</td></tr><tr><td>

Usage by Provider Last 12 Months

</td><td>

Breaks down emphasis by provider, such as PowerShell, JDBC, SSH, etc.

</td></tr><tr><td>

Top 10 Orchestration Activities

</td><td>

 

</td></tr></tbody>
</table>2.  You can add more widgets to the dashboard by clicking the **Add Content** icon \(![Add Content icon](../../../use/homepages/image/AddContent.png)\) in the upper right corner of the dashboard.

    **Note:** You should not modify the first tab in this Dashboard. If you want a different dashboard experience, add a tab and customize that with your usage reports.


