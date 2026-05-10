---
title: Administering data ingestion and model alignment with API Insights
description: The Overview tab in the API Insights workspace provides a centralized view of data ingestion activities and integration health.
locale: en-US
release: australia
product: API Insights
classification: api-insights
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer and monitor API data, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Administering data ingestion and model alignment with API Insights

The Overview tab in the API Insights workspace provides a centralized view of data ingestion activities and integration health.

![API Insights Overview tab for CMDB administrators.](../image/api-insights-overview-cmdb-admin.png)

## Access the API Insights Overview tab

To access the Overview tab, navigate to **Workspaces** &gt; **API Insights**. The Overview tab opens by default.

## Required roles

CMDB administrators can access the Overview tab within the API Insights workspace to monitor incoming API data, evaluate alignment with the data model, and take action on misaligned or incomplete data to verify consistent and accurate CMDB records. They can view and resolve errors in connections when importing API data into CMDB using Service Graph Connectors and adjust data based on clustering recommendations.

**Note:** As a user with the sn\_cmdb\_admin role, you need additional roles such as ml\_report\_user and cmdb\_inst\_admin to access some of the features and data.

## Features

Access the various cards on the Overview tab to gain insights on the API data available in your organization.

**Note:** Select a segment or count on a chart to open the KPI Details page and analyze how a specific metric trends over time. To learn more about the KPI Details feature, see [KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/kpi-details.md).

<table id="table_cnz_34b_mfc"><thead><tr><th>

Feature

</th><th>

Description

</th><th>

Required roles

</th></tr></thead><tbody><tr><td>

Search APIs

</td><td>

API search within the organization to locate specific APIs for review or management.

</td><td>

sn\_cmdb\_admin

</td></tr><tr><td>

Connection status

</td><td>

Total count of active API connections and processing errors.Provides insight into the status of API connections and highlights any processing issues to verify reliable data ingestion.

-   **Active connections**

Total number of installed connections with active import schedules. Select the count to view installed connections.

-   **Errors**

Total number of processing errors for installed connections.


</td><td>

sn\_cmdb\_admin and cmdb\_inst\_admin

</td></tr><tr><td>

API clustering recommendations

</td><td>

Number representing the current clustering recommendation, based on the data model recommendation settings.See [Configure data model recommendations for API clustering in API Insights](../task/api-insights-config-dm.md).

</td><td>

sn\_cmdb\_admin, ml\_report\_user, and platform\_ml\_read

</td></tr><tr><td>

APIs by discovery source

</td><td>

Total count of discovered APIs grouped by source.Provides insight into the discovery methods of APIs across your organization.

</td><td>

sn\_cmdb\_admin

</td></tr><tr><td>

APIs by life cycle

</td><td>

Total count of APIs grouped by life cycle stage as Operational, Deploy, or End of Life.Provides visibility into API readiness and maintenance status across your organization.

</td><td>

sn\_cmdb\_admin

</td></tr><tr><td>

APIs by type

</td><td>

Total count of APIs categorized by protocol or communication type.Includes technologies such as REST, GraphQL, and SOAP, providing insight into the integration styles and interoperability across your organization.

</td><td>

sn\_cmdb\_admin

</td></tr><tr><td>

APIs by environment

</td><td>

Count of APIs deployed in each environment.Highlights distribution across Development, Test, and Production stages, enabling monitoring of deployment progress and assessment of risk exposure.

</td><td>

sn\_cmdb\_admin

</td></tr><tr><td>

APIs by ownership group

</td><td>

Total count of APIs categorized by assigned ownership group. Groups APIs by managing team or function, as defined by an enterprise architect administrator with the sn\_api\_insights\_ws.api\_mgmt\_architect\_admin role in settings. For more information on setting an ownership group, see [Configure settings to manage APIs in API Insights](../task/api-insights-config-settings.md).

</td><td>

sn\_cmdb\_admin

</td></tr><tr><td>

APIs missing data

</td><td>

Count of APIs missing key attributes, including business context, ownership group, product model, or design. Each bar represents a key attribute and indicates the number of APIs missing the attribute.

Color coding indicates the severity of missing data:

-   **Red**

More than 50% of APIs are missing the attribute.

-   **Yellow**

Between 10% and 50% of APIs are missing the attribute.

-   **Green**

Less than 10% of APIs are missing the attribute.


Use the visual indicator to prioritize remediation efforts based on data completeness. Select a bar in the bar chart to start the remediation process. See [Identifying and remediating missing API data in API Insights](api-insights-resolve-gaps.md#).

</td><td>

sn\_cmdb\_admin

</td></tr><tr><td>

APIs by business application

</td><td>

Count of APIs linked to business applications.Enables tracking of API connections to business applications to improve integration after connections are established.

</td><td>

sn\_cmdb\_admin

</td></tr><tr><td>

Connections overview

</td><td>

Summary of the status and activity of API data connections using Service Graph Connectors, including counts of successful, failed, or unknown connection tests, recent import success rate, and the number of connections currently processing data imports.

</td><td>

sn\_cmdb\_admin and cmdb\_inst\_admin

</td></tr></tbody>
</table>