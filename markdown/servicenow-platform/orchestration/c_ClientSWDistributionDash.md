---
title: Client software distribution dashboard
description: The CSD dashboard provides a collection of visual reports for the Client Software Distribution application.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Client Software Distribution, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Client software distribution dashboard

The CSD dashboard provides a collection of visual reports for the Client Software Distribution application.

## CSD dashboard

To access the CSD dashboard, navigate to **Client Software Distribution** &gt; **Requested Software** &gt; **Dashboard**.

![Sample report from CSD dashboard](../image/CSDSampleGraph.png "Sample report from CSD dashboard")

<table id="table_sbk_x2h_ft"><thead><tr><th>

Report

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open Tasks

</td><td>

Displays all open tasks grouped by the requested item's stage value.-   Type: [Create a basic list report](https://www.servicenow.com/docs/access?context=t_CreateAListReport&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   Table: Catalog Task \[sc\_task\]

</td></tr><tr><td>

Top 10 Applications Installed

</td><td>

Displays the top 10 applications installed by request count.-   **Type**: [Create a bar report](https://www.servicenow.com/docs/access?context=c_CreateBarCharts&version=australia&pubname=australia-now-intelligence&section=t_CreateABarChartReport&ft:locale=en-US)
-   **Table**: Requested Software \[sn\_client\_sf\_dist\_req\_software\]

</td></tr><tr><td>

Total Software Request Item Over Time

</td><td>

Displays the total software items requested each month. -   **Type**: [Line reports](https://www.servicenow.com/docs/access?context=c_CreateLineCharts&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   **Table**: Requested Software \[sn\_client\_sf\_dist\_req\_software\]

</td></tr><tr><td>

Requests Completed Report

</td><td>

Displays the total of software requests completed each month.-   **Type**: [Line reports](https://www.servicenow.com/docs/access?context=c_CreateLineCharts&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   **Table**: Requested Software \[sn\_client\_sf\_dist\_req\_software\]

</td></tr><tr><td>

Installed Software Not Entitled

</td><td>

Displays installed software that users or devices are not entitled to use. This can be software deployed through CSD or by another process that does not comply with licensing. This report is on a Software Asset Management table.-   **Type**: [Create a basic list report](https://www.servicenow.com/docs/access?context=t_CreateAListReport&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   **Table**: Software Installation \[cmdb\_sam\_sw\_install\]

</td></tr><tr><td>

Software Installation Status

</td><td>

Displays the count of requested software, grouped by installation status, for each month.-   **Type**: [Line reports](https://www.servicenow.com/docs/access?context=c_CreateLineCharts&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   **Table**: Requested Software \[sn\_client\_sf\_dist\_req\_software\]

</td></tr><tr><td>

Software Requested Item Stage Report

</td><td>

Displays the sum of all requested items, grouped by the requested item’s stage, for each month.-   **Type**: [Line reports](https://www.servicenow.com/docs/access?context=c_CreateLineCharts&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   **Table**: Requested Software \[sn\_client\_sf\_dist\_req\_software\]

</td></tr><tr><td>

License Counts Available

</td><td>

Displays the license counts for all available applications.-   **Type**: [Create a basic list report](https://www.servicenow.com/docs/access?context=t_CreateAListReport&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   **Table**: SCCM Application Catalog Item \[sn\_client\_sf\_dist\_sccm\_app\_cat\_item\]

</td></tr></tbody>
</table>## Usage Overview dashboard

Navigate to **Client Software Distribution** &gt; **Usage Overview** to view the current transaction count for your instance.

**Parent Topic:**[Client Software Distribution](c_ClientSoftwareDistribution.md)

