---
title: Business Insights view
description: The Business Insights view in the Cloud Cost Management Workspace provides a unified outlook of your cloud and non-cloud costs. This view helps finance, FinOps, and business teams understand the total cost of ownership \(TCO\) and unit economics for applications, departments, and business units.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/cloud-cost-management/business-insights-ccm-ws.html
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-07-15"
reading_time_minutes: 2
breadcrumb: [Cloud Cost Management Workspace, Explore, Cloud Cost Management, IT Asset Management]
---

# Business Insights view

The Business Insights view in the Cloud Cost Management Workspace provides a unified outlook of your cloud and non-cloud costs. This view helps finance, FinOps, and business teams understand the total cost of ownership \(TCO\) and unit economics for applications, departments, and business units.

The Business Insights view aggregates cloud costs from the Cloud Cost Management application with non-cloud costs from TCO. You must have the Enterprise Architecture plugin \(com.snc.apm\) installed on your instance for non-cloud costs to appear in the TCO dashboard.

Access the Business Insights view by navigating to **Workspaces** &gt; **Cloud Cost Management Workspace** &gt; **Business insights**.

The Business Insights view includes the following dashboards:

-   **Total cost of ownership \(TCO\)**: This dashboard displays cloud and non-cloud costs aggregated by business entity for a time range that you select.
-   **Unit economics**: This dashboard displays the cost, revenue, and margin for a business application per unit of measurement that you define, such as API calls or number of customers. Unit economics data requires you to upload business data, including revenue and unit counts. For more information, see [Upload business data for unit economics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/upload-business-data.md).

## Total cost of ownership \(TCO\) dashboard

\[Omitted image "business-insights-ccm.png"\] Alt text: Total cost of ownership \(TCO\) dashboard on the Business insights view in Cloud Cost Management Workspace

The Total cost of ownership \(TCO\) dashboard displays the following reports filtered by entity type and time range.

<table id="table_swf_n4s_fkc"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total cost

</td><td>

-   Spend Report Monthly Aggregated Costs \[sn\_cld\_spend\_core\_monthly\_aggregated\_cost\] table
-   Enterprise Architecture plugin \(com.snc.apm\)

</td><td>

The total cost of your resources, including the cloud costs and non-cloud costs.

</td></tr><tr><td>

Cloud cost

</td><td>

Spend Report Monthly Aggregated Costs \[sn\_cld\_spend\_core\_monthly\_aggregated\_cost\] table

</td><td>

The total cost of your cloud resources.

</td></tr><tr><td>

Non-cloud cost

</td><td>

Enterprise Architecture plugin \(com.snc.apm\)

</td><td>

The total cost of your non-cloud resources, such as labor and licensing costs.

</td></tr><tr><td>

Monthly cost breakdown

</td><td>

-   Spend Report Monthly Aggregated Costs \[sn\_cld\_spend\_core\_monthly\_aggregated\_cost\] table
-   Enterprise Architecture plugin \(com.snc.apm\)

</td><td>

Monthly breakdown of cloud costs and non-cloud costs.

</td></tr></tbody>
</table>## Unit economics dashboard

\[Omitted image "unit-economics-ccm.png"\] Alt text: Unit economics dashboard on the Business insights view in Cloud Cost Management Workspace

The Unit economics dashboard displays the following calculated values for each business application and time period.

|Report|Description|
|------|-----------|
|Average cost per &lt;unit type&gt;|Total cost \(cloud + non-cloud\) divided by the number of units you upload for that period.|
|Average revenue per &lt;unit type&gt;|Average revenue of a unit type.|
|Average margin per &lt;unit type&gt;|Average revenue minus average cost.|
|Average margin %|Average margin expressed in percentage.|
|Unit economics trend per &lt;unit type&gt;|A comparative chart showing cost, revenue, and margin for the unit type for a particular time period.|
|Monthly totals per &lt;unit type&gt;|A comparative chart showing monthly totals for the unit type.|

