---
title: Using Sighting Search Parameters
description: You can use sighting search parameters that define more complex queries, which include logic and other operators supported by the specified log store.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Sighting Search, Sighting Search, TISC Enrichment Integrations, TISC Integrations, Integrating Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Using Sighting Search Parameters

You can use sighting search parameters that define more complex queries, which include logic and other operators supported by the specified log store.

## View Sighting Search Parameters

Role required: sn\_sec\_tisc.admin

To view the sighting search parameters, perform the following steps:

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations**.
2.  From the Integrations page, navigate to **Enrichment Integrations** &gt; **Sighting Search**.
3.  Look for the integration for which you want to view the Sighting Search Configuration, and click **Edit**.
4.  Select the **Sighting Search Configurations** tab.

    You can view the list of sighting search configurations.

5.  Click on the required Sighting Search Configuration to view the details of the configuration.

    ![Sighting Search Parameters tab](../image/enrich-sighting-parameters.png)

6.  Select the **Sighting Search Parameters** tab.

    You can view the list of sighting search parameters.

7.  Click on the required Sighting Search Parameter to view the details of the parameter.
8.  You can also perform the following actions on the Sighting Search Parameters tab:
    1.  To refresh the list of sighting search parameters, click ![Refresh option](../image/enrich-refresh-icon.png) icon.
    2.  To perform a list action on the sighting search parameters, click the ![List actions](../image/enrich-list-actions.png) icon.

        **Edit columns**: You can use this action to add or remove existing columns and modify the order according to your requirements.

    3.  To filter sighting search parameters based on conditions, click the ![Filter panel](../image/enrich-filter.png) icon.

        The value 1 indicates that one condition is used for the filtering.


## Create Sighting Search Parameter

`Example for query generation`

```
Configured Query: ${Observable}​

Observables Substitutes for Sightings search: Obs1 , Obs2​

Query: {Before each Value}Obs1{After each Value}{Between each value}{Before each Value}Obs2{After each Value}​

​

Let observables are: 172.32.31.41 & 192.168.10.12​

Query Formed with below configuration will be: “ip_address = 172.32.31.41 OR ip_address = 192.168.10.12”
```

To create a sighting search parameter, perform the following steps:

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations**.
2.  From the Integrations page, navigate to **Enrichment Integrations** &gt; **Sighting Search**.
3.  Look for the integration for which you want to view the Sighting Search Configuration, and click **Edit**.
4.  Select the **Sighting Search Configurations** tab.

    You can view the list of sighting search configurations.

5.  Click on the required Sighting Search Configuration to view the details of the configuration.
6.  Select the **Sighting Search Parameters** tab.

    You can view the list of sighting search parameters.

7.  To create a sighting search parameter, click **New**.

    ![Create a Sighting Search Parameter](../image/enrich-create-sighting-parameters.png)

8.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |After each value|The sighting search parameter after each observable when the search query is generated.|
    |Between each value|The sighting search parameter between each observable when the search query is generated. For example, OR.|
    |Before each value|The sighting search parameter before each observable when the search query is generated.|
    |Configuration|The configuration details of the search parameter.|
    |Observable type|Defines the type of observable category.|
    |Substitution variable|Specifies the name of the variable that is replaced by an observable value.|

9.  Click **Save**.

**Parent Topic:**[Configure Sighting Search](../task/configure-sighting-search.md)

