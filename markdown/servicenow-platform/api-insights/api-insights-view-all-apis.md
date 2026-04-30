---
title: Viewing all APIs in API Insights
description: Manage and monitor all APIs within your organization by reviewing their life cycle stages, identifying missing critical attributes, and accessing helpful resources to ensure proper API maintenance and governance.
locale: en-US
release: zurich
product: API Insights
classification: api-insights
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage API data, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Viewing all APIs in API Insights

Manage and monitor all APIs within your organization by reviewing their life cycle stages, identifying missing critical attributes, and accessing helpful resources to ensure proper API maintenance and governance.

The All APIs page in the API Insights workspace provides a comprehensive overview of all APIs within an organization ensuring that APIs are properly maintained and aligned with the organization's standards for interfaces, ownership, and product models.

![All APIs page to view APIs within your organization.](../image/api-insights-all-apis-page.png "All APIs page")

## Accessing and using the All APIs page

To access the All APIs page, navigate to **Workspaces** &gt; **API Insights**, and then select the **API** tab.

## Viewing data

By default, the page displays the following data:

-   **All APIs list**

    Displays the total number of APIs managed by the organization and categorizes them by their life cycle stage \(All APIs, In design, Operational, End of Life\). You can select the each card to view APIs by their life cycle stage in the API data table.

-   **API data table**

    Lists all APIs with detailed columns for the API name, the number of consumers, management platform, life cycle stage, version, and the number of API requests processed per minute for each API listed in the table. This table provides an overview of the APIs and their status within the organization. You can select an API from the **Name** column to view API details and request access to the API managed by your team. See [Request access to an API in API Insights](../task/api-insights-req-access.md).

-   **Available actions and filters in the API data table**

    Provides several actions and filtering options to manage and refine the displayed data. These include exporting the list in various formats, refreshing the data, and applying filters to narrow down the results by platform type, instance, or specific column criteria.

    -   **Exporting API data**

        Export the APIs list as a PDF, CSV, JSON, or Microsoft Excel file by selecting **Export**, and then selecting the desired file format from the File Type list. You can either download the file to your local directory or email the file by selecting a value from the Delivery Type list. After making your selections, select **Export** to complete the process.

    -   **Refreshing the API data**

        Manually populate the API data table on demand by selecting the refresh icon \(![Refresh icon.](../image/refresh-list.png)\).

    -   **Filtering APIs by platform and instance**

        Narrow down the API list based on platform type and instance.

        -   Use the Management Platform Type list to filter APIs by platform category.
        -   Use the Management Platform Instance list to refine results by a specific ServiceNow instance.
        Select **Apply** to update the list based on the selected filters. If you select **ALL** in either list, APIs from all available options are included in the table.

    -   **Applying filters to API data columns**

        Refine the list of APIs by using column-specific filters or advanced condition sets.

        Each column in the All APIs list includes lightweight, inline filtering options:

        -   **Operator**

            Includes the comparison operator for the filter. The operator list includes `is`, `is not`, `starts with`, `ends with`, `contains`, `does not contain`, `is empty`, `is not empty`. In the **Value** field, you can enter the text or number you want to filter on and then press the Enter key. The list refreshes when the filter is applied.

            For example, selecting **contains** and entering a value in the **Value** field, filters the list to show only API records where the column contains that text.

        -   **Open panel**

            Opens the full filter panel for the selected column and provides a finer control over the filters to refine the data in the table according to the parameters that are most important for your analysis.

            You can define custom conditions for narrowing down data by selecting a field, choosing an operator, such as equals or contains, and entering a specific value. You can add multiple conditions to refine your search further, and once you've set the filters, selecting **Run** updates the API data table accordingly. The **Show labels** toggle switch controls whether the labels for the fields and operators are displayed. When enabled, it shows descriptive text next to each option to help you understand their purpose, while disabling it hides the labels for a more compact view.

        -   **Add Filter**

            Inline filter rule added for a column so you can immediately define conditions using the operator and value fields. For example, when filtering by **Type**, you can choose REST, SOAP, gRPC, Websocket, Scripted REST, and other predefined options.

-   **APIs missing data section**

    Highlights the APIs missing key attributes like business context, ownership groups, product models, and design helping to identify issues in API governance. You can select the numeric value displayed in each card to identify and resolve issues with API data. See [Identifying and remediating missing API data in API Insights](api-insights-resolve-gaps.md#).

-   **Helpful resources**

    Contains quick links to product documentation, knowledge base articles, and community forums, providing easy access to additional resources for API management.


