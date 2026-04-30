---
title: Define queries for Sighting Search
description: You can use sighting search configurations for defining the queries used to find the prevalence of observables in your environment as part of observable investigation.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Sighting Search, Sighting Search, TISC Enrichment Integrations, TISC Integrations, Integrating Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Define queries for Sighting Search

You can use sighting search configurations for defining the queries used to find the prevalence of observables in your environment as part of observable investigation.

## View queries for Sighting Search

Role required: sn\_sec\_tisc.admin

To view the sighting search configurations, perform the following steps:

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations**.
2.  From the Integrations page, navigate to **Enrichment Integrations** &gt; **Sighting Search**.
3.  Look for the integration for which you want to view the Sighting Search Configuration, and click **Edit**.
4.  Select the **Sighting Search Configurations** tab.

    You can view the list of sighting search configurations.

    ![Sighting Search Configurations tab](../image/enrich-view-sighting-search-config.png)

5.  Click on the required Sighting Search Configuration to view the details of the configuration.
6.  To generate a test sighting search query, click the **Generate Test Sighting Search Query** action.

    **Note:** The **Generate Test Sighting Search Query** action would only work if you had configured sighting search query parameters. For more information, see [Using Sighting Search Parameters](manage-sighting-search-parameters.md).

7.  In the Generate Test Sighting Search Query pop-up, enter or paste multiple observables using comma, new line, tab, or pipe separators to generate a test query.
8.  Click **Generate** to generate the test sighting search query.
9.  You can also perform the following actions on the Sighting Search Configurations tab:
    1.  To refresh the list of sighting search configurations, click the ![Refresh option](../image/enrich-refresh-icon.png) icon.
    2.  To perform a list action on the sighting search configurations, click the ![List actions](../image/enrich-list-actions.png) icon.

        You can perform the following two list actions:

        -   **Edit columns**: You can use this action to add or remove existing columns and modify the order according to your requirements.
        -   **Reset widths**: You can use this action to reset the widths of the columns.
    3.  To filter sighting search configurations based on conditions, click the ![Filter panel](../image/enrich-filter.png) icon.

        The value 1 indicates that one condition is used for the filtering.


## Create Sighing Search Configurations

Role required: sn\_sec\_tisc.admin

```
Maximum observables per search = "maximum number of observables that can be substituted in a single search query"

Search = "Search query that should be executed in sighting search source. 
Search query can contain substitution variables that would be substituted with observables of specific type as configured in sighting search parameters when sighting search query is formed"
```

To create a sighting search configuration, perform the following steps:

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations**.
2.  From the Integrations page, navigate to **Enrichment Integrations** &gt; **Sighting Search**.
3.  Look for the integration for which you want to view the Sighting Search Configuration, and click **Edit**.
4.  Select the **Sighting Search Configurations** tab.

    You can view the list of sighting search configurations.

5.  To create a sighting search configuration, click **New**.

    ![Create a Sighting Search Configuration](../image/enrich-create-sighting-search-config.png)

6.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the sighting search configuration.|
    |Observable type|Defines the type of observable category.|
    |Sightings search source|Defines the source configured for the integration.|
    |Maximum observables per search|The number of observables before the search query is split into multiple queries. Set this value to `500` for this integration.|
    |Search|Add a native search string to form a query. For example, `${observable}`.|
    |Is saved search|Runs a saved search, that is, the Name field should match the name of the saved search.|
    |Active|Query runs only if it active option is selected.|

7.  Click **Save**.

**Parent Topic:**[Configure Sighting Search](../task/configure-sighting-search.md)

