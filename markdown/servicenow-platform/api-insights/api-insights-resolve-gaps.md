---
title: Identifying and remediating missing API data in API Insights
description: Identify and remediate missing API data in the API Insights workspace by linking missing elements and verifying complete API records.Improve the operational efficiency of the API ecosystem within your organization by creating a relationship or reference for APIs that lack key attributes such as business context, ownership groups, product models, or designs.
locale: en-US
release: australia
product: API Insights
classification: api-insights
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage API data, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Identifying and remediating missing API data in API Insights

Identify and remediate missing API data in the API Insights workspace by linking missing elements and verifying complete API records.

Missing metadata can reduce the effectiveness of API discovery, life cycle tracking, and ownership accountability. Common missing elements include:

-   Business context
-   Ownership group
-   Product model
-   Design details

Resolving missing data ensures a more complete, accurate view of dependencies and ownership, improving impact assessments and service management.

The Overview tab of the API Insights workspace enables improve the usability, governance, and integration of APIs by highlighting any incomplete or missing data within the Configuration Management Database \(CMDB\).

## Remediating missing API data by roles

The following roles can identify and resolve missing metadata in API:

-   An enterprise architect with the sn\_api\_insights\_ws.api\_mgmt\_architect role can access the Overview tab in the API Insights workspace to remediate missing API information using dedicated tiles for each type of missing data.
-   A CMDB administrator with the sn\_cmdb\_admin role can access the Overview tab in the API Insights workspace and select a bar within the APIs missing attributes bar chart to identify and update missing metadata.

## Monitoring key metrics

You can monitor the following missing data associated with APIs within your organization:

-   **Missing business context**

    APIs not associated with any business context reduce the clarity and governance over which business areas are providing them.

-   **Missing ownership groups**

    APIs without an assigned ownership group affect governance. Assigning ownership groups streamlines tracking remediations, managing access, and resolving issues quickly.

-   **Missing product models**

    APIs without an assigned product model limit the ability to provide accurate reporting and interactions with versioned APIs.

-   **Missing design**

    APIs with no design representation hinder their full integration into the system. Linking these APIs with their design-time counterparts \(such as digital interface records\) improves usability and operational efficiency.


## Resolving missing API data

You can resolve missing API data by creating relationships for business context or references for ownership groups, product models, or designs, to establish connections between the API and other CIs within the CMDB.

You can establish the following relationships or references in API Insights to resolve missing API data:

-   **API-to-business context relationship**

    Links an API to a specific business context, defining the context in which the API is used and creating a relationship record in the CMDB.

-   **API-to-ownership group reference**

    Links an API to a group responsible for its governance, access control, and maintenance, serving as a reference without creating a record in the CMDB.

-   **API-to-product model reference**

    Links an API to a product model, providing information on the API's versioning, product line, and life cycle stage, serving as a reference without creating a record in the CMDB.

-   **API-to-design reference**

    Links an API to its runtime or design-time interface, serving as a reference without creating a record in the CMDB.


## Create a relationship or reference to remediate missing API data

Improve the operational efficiency of the API ecosystem within your organization by creating a relationshipor reference for APIs that lack key attributes such as business context, ownership groups, product models, or designs.

### Before you begin

Role required: sn\_api\_insights\_ws.api\_mgmt\_architect, sn\_cmdb\_admin

### About this task

Available missing data categories include:

-   Missing business context
-   Missing ownership groups
-   Missing product models
-   Missing designs

    **Note:** Displayed only when the Digital Integration Management plugin \(sn\_apm\_di\) is activated.


**Important:** When creating relationships for a large number of APIs, you can automate creating relationships based on tags on API. For more information, see [Automating creating tag-based relationship mapping within API Insights](../../../Chunk1918641441.md#).

### Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  Select the Overview tab, if not already selected by default.

3.  Select a missing data category to open the list of APIs missing that attribute.

    -   As a user with the sn\_api\_insights\_ws.api\_mgmt\_architect role, in the APIs missing data section, select the number shown for a specific missing data category.
    -   As a user with the sn\_cmdb\_admin role, select a category bar in the APIs missing data bar chart.
4.  On the APIs missing data page, select the check boxes next to the API names.

5.  Resolve missing data.

    -   For resolving missing business context, select **Create relationships**.
    -   For resolving missing ownership groups, product model, or designs, select **Create reference**.
6.  Select the check boxes next to the **Name** column for the application services.

7.  Based on the type of connection needed, establish relationships or a reference.

    -   For business context, select **Create relationships**.
    -   For ownership groups, product model, or designs, select **Create reference**.
8.  In the dialog box that appears, select **Create**.


