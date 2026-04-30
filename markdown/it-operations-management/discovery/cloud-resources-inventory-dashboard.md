---
title: Cloud Resources Explorer
description: Use the ServiceNow Cloud Resources Explorer to filter and visualize the distribution of resources across your multi cloud estate. Gain insight into operational information such as stale resources and cloud event inflow rates.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Cloud discovery reporting, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Cloud Resources Explorer

Use the ServiceNow® Cloud Resources Explorer to filter and visualize the distribution of resources across your multi cloud estate. Gain insight into operational information such as stale resources and cloud event inflow rates.

![Cloud Resources Explorer.](../image/cloud-resources-explorer.png "Cloud Resources Explorer")

The Cloud Resources Explorer supports the following cloud providers:

-   Amazon Web Services.
-   Microsoft Azure public clouds.
-   VMware vCenter.
-   Google Cloud Platform \(GCP\) \(Supported with Performance Analytics Content Pack for Cloud Resources version 1.2.1 and higher\).

## Required ServiceNow AI Platform roles

The sn\_cloud\_ops\_ws.cloud\_ops\_admin role is required to view the Cloud Resources Explorer.

## Access the Cloud Resources Explorer

To open the Cloud Resources Explorer, navigate to **All** &gt; **Cloud Discovery Workspace** &gt; **Cloud Resources Explorer**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_svb_q4d_htb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

sn\_cloud\_ops\_ws.cloud\_ops\_admin

</td><td>

-   Gain insight into the cloud resources inventory count and the current size of the Configuration Management Database \(CMDB\), and how many objects are under the purview.
-   Gain insight into fault-related information such as Cloud Discovery errors.
-   Gain insight into operational information such as the inflow and processing rate of the event.
-   Gain insight into the health of your CMDB.
-   Gain insight into the distribution of resources across the on-prem cloud and the public clouds.

</td></tr></tbody>
</table>## Indicators

-   **Cloud Discovery errors**

    Total Cloud Discovery errors encountered over time.

-   **Stale CIs &gt; 30 days**

    If a CI isn't updated in the last 30 days, it's considered as a stale CI.

    A stale CI indicates that the CI exists in the Configuration Management Database \(CMDB\), but it may or may not exist in the datacenter. Identifying the stale CIs is important for maintaining a healthy CMDB.

    Here are some of the scenarios that leads to the creation of stale CIs:

    -   The cloud resource doesn't exist, but its deletion isn't updated in the CMDB.
    -   The device may still be on the network, but the automated discovery process can't connect to the device to rediscover it.
    -   The device exists on the network and it's accessible, but the identification process isn't recognizing it uniquely. Therefore, Cloud Discovery has created a duplicate CI in the CMDB.

## Data visualizations

<table id="id_wgr_q1f_htb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration item classes

</td><td>

Horizontal bar report![Horizontal bar report.](../../reporting/image/icon-horizontal-bar-report-p.png)

</td><td>

Cloud Analytics \[sn\_disco\_cd\_analytics\]

</td><td id="cloud-resources-inventory-dashboard-ci-class-report">

This report displays the count of the top 10 CI classes discovered over time.You can select a report entry from the Configuration item classes report to view the analytics table on which the report entry is based. If you've selected a specific cloud provider, then the analytics table of that specific CI appears. Otherwise, the parent analytics table for that CI type appears.

 For example, if you select Google from the Cloud resources filter and select the Storage Volume bar from the report, the dedicated analytics table of the Google Storage Volume CI appears. If you select All Platforms from the Cloud resources filter and select the Storage Volume bar from the report, the parent analytics table of the storage volume CI appears.

</td></tr><tr><td>

Configuration items by regions

</td><td>

Horizontal bar report![Horizontal bar report.](../../reporting/image/icon-horizontal-bar-report-p.png)

</td><td>

Cloud Analytics \[sn\_disco\_cd\_analytics\]

</td><td id="cloud-resources-inventory-dashboard-ci-by-region-report">

This report displays the distribution of CIs per region \(datacenter\).

</td></tr><tr><td>

Configuration items by cloud service accounts

</td><td>

Horizontal bar report![Horizontal bar report.](../../reporting/image/icon-horizontal-bar-report-p.png)

</td><td>

Cloud Analytics \[sn\_disco\_cd\_analytics\]

</td><td id="cloud-resources-inventory-dashboard-ci-by-serv-acc-report">

This report displays the top 10-service accounts with the maximum number of discovered CIs.

</td></tr><tr><td>

Incoming events

</td><td>

Bar report![Bar report.](../../reporting/image/icon-bar-report-p.png)

</td><td>

Cloud Event \[sn\_cmp\_cloud\_event\]

</td><td id="cloud-resources-inventory-dashboard-incoming-events-report">

This report displays the trend of cloud resource events received over time.

 To view the list of all the cloud events received over a given day, select the corresponding report entry.

</td></tr><tr><td>

Total cloud resources in on-prem vs public clouds

</td><td>

Stacked bar report![Stacked bar report.](../../reporting/image/icon-bar-report-p.png)

</td><td>

Daily resource count by providers \[sn\_disco\_cd\_daily\_resource\_cnt\_by\_provider\]

</td><td id="cloud-resources-explorer-on-prem-vs-cloud">

This report displays the daily count of the resources of your organization that are spread across the on-prem cloud and the public clouds. Use this report to understand the public cloud adoption and Virtual Machine \(VM\) count over time.

 In this report, the VMware Cloud is considered on-prem.

</td></tr></tbody>
</table>To populate the Cloud Analytics \[sn\_disco\_cd\_analytics\] table, the Cloud Resources Explorer uses the same set of scheduled jobs as the Performance Analytics Content Pack for Cloud Resources. For more information on the scheduled jobs, see [Cloud Resources dashboard](cloud-resources-dashboard.md).

To view the details of the OS images discovered in the AWS, Microsoft Azure, and GCP clouds, Discovery and Service Mapping Patterns store app version 1.0.87 or later must be installed in the instance. Also, the **sn\_cmdb\_ci\_class.use\_single\_cloud\_os\_image** property must be set to `true`.

## Filters

<table id="id_ppj_q2f_htb"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud resources filter

</td><td>

Choice-based filter

</td><td>

Use the cloud resources filter to select and visualize the cloud resources data of interest.

 By default, the Cloud Resources Explorer displays data for all the cloud resources across the cloud providers of your organization. Only the cloud providers that you've selected in the Cloud provider selection page of the Cloud Discovery Workspace app appear in the cloud resources filter.

 You have the choice of the following cascading filters:

-   Platform: Select the cloud provider with the resources data that you want to visualize.
-   Region: Select the region or datacenter with the resources data that you want to visualize.
-   Service account: Select the service account with the resources data that you want to visualize.
-   CI class: Select the CI class with the resources data that you want to visualize.
-   Resource group: Select the resource group with the resources data that you want to visualize.

This field is available only when `Azure` is selected from the Platform drop-down list.


 You can filter the Incoming events report based on the Platform filter only. The data displayed in the Cloud Discovery errors indicator isn't affected by the criteria selected in the Cloud resources filter.

</td></tr><tr><td>

Day navigator

</td><td>

Choice-based filter

</td><td>

Use the Day navigator to slice the Total cloud resources in on-prem vs public clouds report across the following dimensions:

-   None: The report displays the data collected over the last one year if available.
-   First day of the month: The report displays the historical data collected for the first day of the month over the last one year if available.
-   Mid of the month: The report displays the historical data collected for the mid day of the month over the last one year if available.
-   Last day of the month: The report displays the historical data collected for the last day of the month over the last one year if available.
-   Pick a date of the month: The report displays the historical data collected for the selected day of the month over the last one year if available.

</td></tr></tbody>
</table>