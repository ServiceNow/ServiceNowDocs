---
title: Create a flow definition for a remote table
description: Build and create a flow for a remote table so that you can retrieve data from an external source with it.
locale: en-US
release: zurich
product: Remote Tables
classification: remote-tables
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a flow definition for a remote table

Build and create a flow for a remote table so that you can retrieve data from an external source with it.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Remote Tables** &gt; **Definition**.

    A list of all remote tables definitions shows up.

2.  Click **New** to create a new flow definition.

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

-   For a remote table in a scoped application, the name is prefixed with a namespace identifier and the string st\_ to indicate that it’s remote and part of an application.
-   For a remote table in the global application, the name is prefixed with the string u\_st\_.


</td></tr><tr><td>

Flow

</td><td>

Option to build and define your own flow by leveraging the existing functions. Configure the mapping of the flow and tie it to thee required remote table. When the remote table is queried, the flow is triggered and the data is retrieved. See Defining the flow for more information.**Note:** The Script section doesn't show up when the **Flow** field has an entry.

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
</table>4.  In the Caching section, designate how this data is cached and how long the data is cached in the memory of the ServiceNow AI Platform:

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

5.  Click **Submit**.


-   **[Define a flow logic](define-flow.md)**  
Set the triggers and actions to define a remote table flow logic.

**Parent Topic:**[Remote tables](../concept/remote-tables.md)

