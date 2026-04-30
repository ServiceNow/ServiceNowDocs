---
title: Remote tables
description: Connect the ServiceNow AI Platform to third-party sources, or to another instance, so that you can retrieve external data and optionally cache it in memory. You can view external data in lists or forms and process it with standard Glide scripts. You can also group, sort, aggregate, and filter the data just like you would for standard internal tables.
locale: en-US
release: xanadu
product: Remote Tables
classification: remote-tables
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Remote tables

Connect the ServiceNow AI Platform to third-party sources, or to another instance, so that you can retrieve external data and optionally cache it in memory. You can view external data in lists or forms and process it with standard Glide scripts. You can also group, sort, aggregate, and filter the data just like you would for standard internal tables.

## Remote table components

Use the following components to build an external data framework:

-   **Remote tables**

    You create remote tables to describe the schema for the data that you want to retrieve from an external source.

    The table definition is in the ServiceNow AI Platform, but its rows, or external records, live in memory. You create a remote table the same way that you would create a standard internal table. You define columns and controls and designate application access for it just like you would do for an internal table. Unlike an internal table, a remote table does not get its records from the ServiceNow AI Platform database. It gets its records from running an associated script against an external data source.

    To learn more about creating remote tables, see [Create a remote table](../task/create-remote-table.md).

-   **Script definitions**

    You create and associate a script definition with a remote table. The external data that you've retrieved using the script can be cached in memory. You can also designate how this data is cached and how long the data is cached in memory. Every time that you refresh a list that contains the external data from a remote table, the associated script runs again.

    To learn more about script definitions and how to associate them with a remote table, see [Create a script definition for a remote table](../task/create-remote-table-script.md).


## How remote tables work

By using a remote table, you can retrieve the data from external sources or from another instance with REST or SOAP services. The external data lives in memory in read-only mode, which makes the data temporary, or transient, within the ServiceNow AI Platform. You can then view and manipulate the external data without importing or storing it.

You view the external data in lists or forms in the same way that you view internally stored data. You can manipulate this data by using standard Glide records, business rules, remote APIs, scripting, table reference fields, services, and development tools in the ServiceNow AI Platform.

**Important:** If the data size that is retrieved from the external source is small, use the 1000 rows default limit in a remote table to minimize query times. If the retrieved data size is large and could be less performative, in the script definition, you can select the advanced **Enhanced Capacity** field to support a large number of rows.

## External data life cycle within the ServiceNow AI Platform

The data that you retrieve from an external source has a finite duration, or life cycle, within the ServiceNow AI Platform.

-   When you run a script that is associated with a remote table, the retrieved data lives in memory for as long as the list or form appears. After you close the list or form, that external data is purged from memory. The next time that you use or view the external data in this remote table, memory is repopulated from the external system.
-   However, if you have defined caching parameters for the script, the external data remains cached in memory for the specified caching duration.

    For example, if you designate that the external data should be cached for 300 seconds, it remains cached in memory for 5 minutes. After that time expires, the cached data is purged from memory. The next time that you use or view the external data in this remote table, the cache is refreshed from the external system.


## Practical applications for remote tables

Set up and use remote tables in your enterprise when:

-   You want to fetch external data for temporary use without storing it in the ServiceNow AI Platform. For example, you can create a remote table that fetches weather-related data that appears on a homepage when a user logs in. You would then create an associated script definition that retrieves this data from a third-party weather source that is based on the user's location.
-   You want to retrieve customer details that are stored in an external Customer Relationship Management \(CRM\) application for viewing in Customer Service Management functions such as Agent Workspace.

    **Note:** To learn more about data retrieval for Customer Service Management, see [Third-party data integration for CSM](https://www.servicenow.com/docs/access?context=csm-third-party-data-integration&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

-   You want to retrieve and view personnel data from Human Capital Management \(HCM\) applications such as Workday or SAP SuccessFactors for use in HR Service Delivery functions.

## Post-filtering and sorting

When you run a remote table script, it applies post-filtering and sorting query conditions after it adds rows to a table. These applied conditions support any other required queries that the script does not handle. When you apply post-filtering and sorting, the remote table queries work like standard internal table queries.

When you create remote table scripts, you generally handle the most frequent and expansive queries in the script. Post-filtering queries and sorting can take a long time and may adversely affect how your instance performs. Use a small data set instead so that it doesn't take much time to do post-filtering and sorting.

Based on your use cases, determine if you should try a narrower query in the external call or a more expansive query. Because the internal filtering and sorting can be expensive to run on large result sets, use a narrower query when the data doesn't require extra filtering. Use a more expansive query when a more general query would return a small result set and would require extra filtering and sorting.

## Differences between remote tables and the Integration Hub

Choose whether to use a remote table or Integration Hub to process external data.

-   When you want to temporarily cache external data, use remote tables.
-   If you want more advanced importing and transformation options, including Workflow Studio, or if you want to develop custom integrations, use the Integration Hub.

**Note:** If you create a remote table that uses the data from an external source that is outside of the ServiceNow AI Platform, you must have an Integration Hub subscription entitlement. To learn more about the Integration Hub, see [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **[Activate the remote tables plugin](../task/activate-remote-tables-plugin.md)**  
If you have the admin role, you can activate the Remote Tables plugin \(com.glide.script.vtable\). This plugin includes demo data and activates related plugins if they are not already active.
-   **[Create a remote table](../task/create-remote-table.md)**  
Create a remote table so that you can see the data that you retrieved from an external source.
-   **[Create a script definition for a remote table](../task/create-remote-table-script.md)**  
Define and associate a script with a remote table so that you can retrieve data from an external source with it. The ServiceNow AI Platform retrieves and caches the data for the remote table by running the script against an external data source so you can view or modify it. You can also designate how this external data is cached and how long the data is cached in memory until the script must run again.
-   **[Create a flow definition for a remote table](../task/create-remote-table-flow.md)**  
Build and create a flow for a remote table so that you can retrieve data from an external source with it.
-   **[Debugging remote table script definitions](../reference/debugging-remote-table-scripts.md)**  
You can enable session debugging for remote table script definitions. To enable script definition logging in a session debug log, set the **glide.script.vtable.log.debug** property to **true**.
-   **[Domain separation and remote tables](domain-separation-remote-tables.md)**  
Domain separation is unsupported in remote tables. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Manage instance data sources](../../general/concept/manage-data-sources.md)

