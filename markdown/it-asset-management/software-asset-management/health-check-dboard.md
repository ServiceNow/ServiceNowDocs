---
title: Health check
description: Use the Health check dashboard to view the results of the health scan that is performed on the configurations in your Software Asset Management application.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Success portal view in Software Asset Workspace, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Health check

Use the Health check dashboard to view the results of the health scan that is performed on the configurations in your Software Asset Management application.

To access the Health check dashboard, navigate to **Software Asset Workspace** &gt; **Success portal** &gt; **Health check**.

**Important:** Ensure that you’ve activated the Software Asset Workspace \(com.sn\_sam\_workspace\) plugin and installed the ITAM Health Check application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/88804de177a94110ce3b5a11fe5a99c4/2.0.4?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DITAM%2520health%2520check&sl=sh) to view the Health check dashboard. You must have the scan\_user and sam\_admin role to access this dashboard and view the health score data.

If you are on the Rome or the San Diego releases, you must execute the full scan to view the results in the base system scan dashboard. For details on executing a full scan, see [Execute full scan](https://www.servicenow.com/docs/access?context=hs-execute-full-scan&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Select **Domain** and choose a domain to view the health check results.

You can also perform a scan for a suite by selecting **Execute Scan**. Verify the scan result to act accordingly. For more information, see [.](../task/run-healthcheck.md)

![Health check tab in the Success portal](../image/feb-health-check.png "Health check dashboard")

<table id="table_whp_cqv_1tb"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Suite checks available

</td><td>

Number of checks available for the following suites:-   SQL Server Config
-   SQL Server CMDB
-   Windows Server CMDB
-   Windows Server Config
-   Database Server - Oracle
-   Java - Oracle
-   Microsoft 365
-   General

</td></tr><tr><td>

Health check issues by priority

</td><td>

Issues based on priority. You can choose from the following:-   Low
-   Medium
-   High
-   Critical

</td></tr><tr><td>

Health check score

</td><td>

Indicates the number of successful health checks. For example, if 10 health checks were performed and only 6 health checks passed, the score would be 60%.

</td></tr><tr><td>

Open issue records per suite

</td><td>

The number of open records for each of the following suites:-   SQL Server Config
-   SQL Server CMDB
-   Windows Server CMDB
-   Windows Server Config
-   Database Server - Oracle
-   Java - Oracle
-   Microsoft 365
-   General

</td></tr><tr><td>

Tasks by status

</td><td>

The status of the tasks created in relation to the health score results.-   New
-   In Progress
-   On Hold
-   Resolved

</td></tr><tr><td>

Health check issues per category

</td><td>

Categorization of issues identified as a result of the health check scan.-   Discovery
-   Software Model
-   Entitlements
-   System Property
-   Miscellaneous

</td></tr></tbody>
</table>**Related topics**  


[Software Asset Management health check](sam-health-check.md)

[Run a health check scan for Software Asset Management](../task/run-healthcheck.md)

