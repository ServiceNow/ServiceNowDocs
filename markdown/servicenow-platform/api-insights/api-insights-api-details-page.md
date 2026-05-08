---
title: Viewing API details in API Insights
description: As an enterprise architect, gain insights into your organization's API performance, relationships, and governance from the API details page within the API Insights workspace.
locale: en-US
release: australia
product: API Insights
classification: api-insights
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Manage API data, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Viewing API details in API Insights

As an enterprise architect, gain insights into your organization's API performance, relationships, and governance from the API details page within the API Insights workspace.

The API details page in the API Insights workspace provides a detailed view of an API's operational status, usage, security, and relationships within CMDB.

![The API details page in the API Insights workspace](../image/api-insights-details-page.png "API details page")

.

## Accessing and using the API details page

To access the API details page, navigate to **Workspaces** &gt; **API Insights**, select the **APIs** tab, and then select an API from the **Name** column from the API data table.

## Viewing data

By default, the page displays the following data:

-   [Header region](api-insights-api-details-page.md#header)
-   [Metadata region](api-insights-api-details-page.md#metadata)
-   [Related lists](api-insights-api-details-page.md#access)
-   [Overview panel](api-insights-api-details-page.md#overview)
-   [Usage](api-insights-api-details-page.md#usage)
-   [Events](api-insights-api-details-page.md#events)
-   [Security](api-insights-api-details-page.md#security)
-   [Relationship map](api-insights-api-details-page.md#relationship)

-   **Header region**

    Displays the name of the API, version information, the API's current life cycle stage, such as Operational, or End of Life.

    The **View By** list enables you to toggle between different management platforms, if available, under which the API is managed.

    The version selector enables the selection of different versions of the API to view and manage. Select **Update** to update the details based on the selected version.

    **Note:** The **View By** list and the version selector appear only if applicable for an API.

-   **Metadata region**

    Displays the following fields.

    |Field|Description|
    |-----|-----------|
    |Description|Brief summary or purpose of the API.|
    |Last discovered|Last date the API was discovered or updated in the CMDB.|
    |Discovery source|Source from where the API was discovered.|
    |Type|Type of the API whether scripted REST API, HTTP API, platform REST API, and so on.|
    |Ownership group|Team or group responsible for managing the API.|
    |Digital interface|Interaction method of the API within the system.|

-   **Related Lists**

    Displays the following items as links with their counts.

    |Item|Description|
    |----|-----------|
    |Access requests received|Displays the number of access requests made for the API. Select the link displayed on the card to view access request details.|
    |Consumers|Displays the number of consumers of the API. Select the link displayed on the card to view details for each API consumer.|
    |Deployments|Indicates any active or past deployments of the API across environments. Select the link displayed on the card to view API deployment details.|
    |Products|Displays the number of products associated with the API. Select the link displayed on the card to view API product details.|
    |Tags|Displays the number of tags associated with the API. Select the link displayed on the card to view details for each tag.|

-   **Overview panel**

    Lists all available components of the API, organized into three subsections within the Overview panel:

    -   **Frontend**

        Contains client-side operations, including GraphQL mutations and queries that interact with the UI or user-facing functionality.

    -   **Backend**

        Contains server-side operations, including backend-specific GraphQL mutations and queries that process business logic and data.

    -   **Components**

        Contain various REST API endpoints or service interfaces, each providing a specific function or resource within the API.

    You can expand each subsection to view its endpoints and select any endpoint to see its details.

-   **Usage**

    Displays the following cards.

    |Card|Description|
    |----|-----------|
    |Average number of requests|Number of API component requests over time, represented as a line graph, with the x-axis showing the date range and the y-axis displaying the request count.|
    |Usage by version|API request distribution across different versions over the past 10 days.|

-   **Events**

    Displays the following cards.

<table id="table_r4y_31r_mcc"><thead><tr><th>

Card

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Critical alerts

</td><td>

Critical alerts from IT operations related to the API enabling identifying major issues that could affect the API’s performance.Select the card to display all the open alerts in the Service Operations Workspace and access more detailed information on them. For more information, see Service Operations Workspace.

</td></tr><tr><td>

Incidents

</td><td>

Recorded incidents, such as outages, change requests, or problems related to the API essential for tracking operational health and remediation efforts.Select the card to display all the open incidents in the Service Operations Workspace and access more detailed information on them. For more information, see Service Operations Workspace.

</td></tr></tbody>
</table>-   **Security**

    Displays the following cards.

<table id="table_a1z_c1r_mcc"><thead><tr><th>

Card

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active vulnerability items

</td><td>

Security vulnerabilities associated with the API enabling to track and resolve potential risks.Select the card to display all vulnerabilities in the Vulnerability Manager Workspace and access more detailed information on them. For more information, see Vulnerability Manager Workspace.

</td></tr><tr><td>

Security incidents

</td><td>

Security incidents, if enabled, providing insights into security breaches or issues that might have occurred with the API.Select the card to display all open security incidents in the Security Incident Response Workspace and access more detailed information on them. For more information, see Security Incident Response Workspace.

</td></tr></tbody>
</table>-   **Relationship map**

    Provides a hierarchical overview of the API relationships with its components, management platforms, business applications, and designs, making it easier to understand the API's role within the broader system architecture.In addition, provides the option to manage application service relationships. See [Managing application service relationships for APIs](api-insights-manage-serv-reln.md#).

    A relationship map is a partial unified map similar to the one used in the CMDB Workspace. To open the unified map for APIs, select **Open full map** in the Relationship map section of the API details page. To learn more, see [Unified Map](../../configuration-management/concept/cmdb-workspace-unified-map.md).

    ![API unified map](../image/api-insights-rel-map.png "Unified map for APIs")

    Nodes on the map represent the API and its components in the CMDB and lines represent connections and relationships between API components. The connections help you, for example, to assess the impact of a change to a selected node by showing components that are connected to it through relationships and references. Products such as Change Management, Incident Management, and Event Management benefit from such information.

    The map also shows the composition of application services useful with products such as Event Management and Incident Management. You can review historical changes.

    The following elements are available in the unified map for APIs:

    -   **1: Map**

        The map displays the specified API and its connections and relationships. In the example, the httpbin.org-v1.1 is the home node and the lines represent connections and relationships with other components. Select any node to view details like related application services, change history.

    -   **2: Content controls**
        -   Search for and select the home node, specify the number of relationship levels for application services to display, and reload the map after making changes.
        -   Use filters to limit the types and relationship types that appear on the map.
        -   Show or hide the timeline of events \(related items\) for the selected API
    -   **3: Toolbox**

        Use the toolbox to control several visual aspects of the map, such as zoom level or layout mode.

    -   **4: Contextual side panel**
        -   The **Attributes** panel \(![Attributes icon.](../../configuration-management/image/icon-um-attributes-panel.png)\) lists attributes like location and operational status for the selected API or relationship.
        -   The **Application services** panel \(![Application services icon.](../../configuration-management/image/icon-um-app-services-panel.png)\) lists details of application services associated with the selected API.
        -   The **Related items** panel \(![Related items icon.](../../configuration-management/image/icon-um-related-items-panel.png)\) shows related items such as active incidents or active problems for the selected API.
        -   The **Changes** panel \(![Changes icon.](../../configuration-management/image/icon-um-changes-panel.png)\) lists changes such as changes to operational status for the selected API.
    -   **5: Mini-map navigator**

        Set the zoom level or move the view to an area of interest. Select the icon to show or hide the navigator.

    -   **6: Timeline**

        The timeline indicates events \(related items\) like incidents, problems, and changes for the selected API over a specified period of time. You can use the timeline to visualize the history of changes to an API and how they affect the topology of the CMDB.


