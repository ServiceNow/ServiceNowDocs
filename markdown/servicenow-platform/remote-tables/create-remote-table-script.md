---
title: Create a script definition for a remote table
description: Define and associate a script with a remote table so that you can retrieve data from an external source with it. The ServiceNow AI Platform retrieves and caches the data for the remote table by running the script against an external data source so you can view or modify it. You can also designate how this external data is cached and how long the data is cached in memory until the script must run again.
locale: en-US
release: xanadu
product: Remote Tables
classification: remote-tables
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a script definition for a remote table

Define and associate a script with a remote table so that you can retrieve data from an external source with it. The ServiceNow AI Platform retrieves and caches the data for the remote table by running the script against an external data source so you can view or modify it. You can also designate how this external data is cached and how long the data is cached in memory until the script must run again.

## Before you begin

Role required: admin

## About this task

You create script definitions for remote tables like you do for other scripts. To learn more about entering, modifying, and debugging scripts, see [JavaScript syntax editor](https://www.servicenow.com/docs/access?context=c_SyntaxEditor&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Remote Tables** &gt; **Definition**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_yxx_ndv_tr"><thead><tr><th>

Control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the script that you are creating to associate with the selected remote table.

</td></tr><tr><td>

Table

</td><td>

Name of the remote table that you want to associate the script that you are creating.

-   For a remote table in a scoped application, the name is prefixed with a namespace identifier and the string st\_ to indicate that it is remote and part of an application.
-   For a remote table in the global application, the name is prefixed with the string u\_st\_.


</td></tr><tr><td>

Application

</td><td>

Application that is associated with this remote table. If you are working on an application or are creating a remote table from an application record, the field defaults to that application. Otherwise, the field defaults to **Global**. Any records that are created from the table record, such as modules and security rules, are assigned to this application by default.

</td></tr><tr><td>

Active

</td><td>

Option for activating the script that you are associating with the remote table. You can have multiple inactive script definitions for a remote table, but can only have one active script definition.

</td></tr><tr><td>

Advanced

</td><td>

Option to access the Caching section to designate how the memory caching should operate in the ServiceNow AI Platform for this remote table. **Note:** Only advanced users should set caching parameters for a remote table.

</td></tr></tbody>
</table>4.  In the Script section, add your JavaScript syntax to the skeleton template:

    **Note:** The Script section shows up only when the Flow field is empty.

    ![Remote table script editor template](../images/remote_tables_script_editor.png)

    **Note:** To learn more about entering, modifying, and debugging scripts, see [JavaScript syntax editor](https://www.servicenow.com/docs/access?context=c_SyntaxEditor&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

5.  In the Caching section, designate how this data is cached and how long the data is cached in the memory of the ServiceNow AI Platform:

<table id="table_uv3_gvz_mhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cache TTL

</td><td>

Cache time to live, expressed in seconds, that external data is cached in memory for this remote table script definition. For example, enter `300` to cache the data in the memory for 5 minutes.The maximum value you can enter is 60 minutes \(3600 seconds\).

</td></tr><tr><td>

Enhanced Capacity

</td><td>

Option to select the enhanced capacity to support more than 1000 rows in a remote table.**Note:** If the data size that is retrieved from the external source is small, use the 1000 rows default limit in a remote table to minimize query times. You can select the **Enhanced Capacity** field if the retrieved data size is large and can be less performative.

</td></tr></tbody>
</table>    **Note:** By default, the external data is cached in the memory by user.

6.  Click **Submit**.


## Result

When you activate a script definition, you associate it with the remote table so that you can retrieve and cache the external data.

-   **[Example 1: Retrieving all incident records from an external source](../reference/remote-table-script-def-example1.md)**  
These are examples of script definitions you might create for retrieval and caching of data from sources external to your current instance. In this first example, we create a script to load all incident records from an external source.
-   **[Example 2: Retrieving specific records from a third-party source](../reference/remote-table-script-def-example2.md)**  
In this example, we create a script to retrieve specific types of incident records from a third-party source.

**Parent Topic:**[Remote tables](../concept/remote-tables.md)

**Related topics**  


[v\_query – Scoped, Global](https://www.servicenow.com/docs/access?context=v_queryAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[v\_table – Scoped, Global](https://www.servicenow.com/docs/access?context=v_tableAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

