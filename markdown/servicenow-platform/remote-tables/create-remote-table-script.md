---
title: Create script definitions for a remote table
description: Define scripts for a remote table to retrieve data from an external data source or edit data in the external source.
locale: en-US
release: australia
product: Remote Tables
classification: remote-tables
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create script definitions for a remote table

Define scripts for a remote table to retrieve data from an external data source or edit data in the external source.

## Before you begin

Role required: delegated\_developer with Allow scripting permissions or admin

## About this task

The ServiceNow AI Platform retrieves and caches the data for the remote table by running the query script against an external data source so you can view or modify it. You can also designate how this external data is cached and how long the data is cached in memory until the script must run again.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Remote Tables** &gt; **Definition**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_yxx_ndv_tr"><thead><tr><th>

Control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the script that you’re creating to associate with the selected remote table.

</td></tr><tr><td>

Table

</td><td>

Name of the remote table that you want to associate the script that you’re creating.

-   For a remote table in a scoped application, the name is prefixed with a namespace identifier and the string st\_ to indicate that it’s remote and part of an application.
-   For a remote table in the global application, the name is prefixed with the string u\_st\_.


</td></tr><tr><td>

Application

</td><td>

Application that is associated with this remote table. If you’re working on an application or are creating a remote table from an application record, the field defaults to that application. Otherwise, the field defaults to **Global**. Any records that are created from the table record, such as modules and security rules, are assigned to this application by default.

</td></tr><tr><td>

Active

</td><td>

Option for activating the script that you’re associating with the remote table. You can have multiple inactive script definitions for a remote table, but can only have one active script definition. When you activate a script definition, you associate it with the remote table so that you can retrieve and cache the external data.

</td></tr><tr><td>

Advanced

</td><td>

Option to access advanced caching and editing settings. Caching settings designate how the memory caching should operate in the ServiceNow AI Platform for this remote table.

**Note:** Only advanced users should set caching parameters for a remote table.

</td></tr></tbody>
</table>4.  If you selected the **Advanced** option, from the Advanced section, fill in the fields.

    **Note:** By default, the external data is cached in the memory by the user.

<table id="table_uv3_gvz_mhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cache TTL

</td><td>

Cache time to live, expressed in seconds, that external data is cached in memory for this remote table script definition. For example, enter `300` to cache the data in the memory for 5 minutes.The default value is 0, meaning data isn't cached and is retrieved every time. The maximum value is 60 minutes \(3600 seconds\).

</td></tr><tr><td>

Cache Isolation Level

</td><td>

Cache query results for each user or across all users.-   Cache per user: The cached query results should be specific to the logged-in user. This is the default value.
-   System Shared Cache: The cached query results should be the same for all users.


</td></tr><tr><td>

Enhanced Capacity

</td><td>

Option to select the enhanced capacity to support more than 1000 rows in a remote table.**Note:** If the data size that is retrieved from the external source is small, use the 1000 rows default limit in a remote table to minimize query times. You can select the **Enhanced Capacity** field if the retrieved data size is large and can be less performative.

This field isn’t supported if **Editable** is selected.

</td></tr><tr><td>

Editable

</td><td>

Option to support editing the remote table and its external data source from the instance. Use the v\_record API to customize script definitions for inserting, updating, and deleting data in the table.

</td></tr></tbody>
</table>5.  Customize the following script definitions using the v\_table, v\_query, and v\_record APIs.

    For more information about these APIs, see [v\_table – Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/v_tableAPI.md), [v\_query – Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/v_queryAPI.md), and [v\_record - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/v_recordAPI.md).

<table id="table_cqs_4gj_jdc"><thead><tr><th>

Script definition

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Query

</td><td>

The query script definition retrieves data from the external source to include in the remote table. From the Query section, customize the script using the v\_table and v\_query APIs.

 Every time a list that contains external data from a remote table is refreshed, the associated query scripts runs.

 ```javascript
(function executeQuery(v_table, v_query) {
     // Parameters:
     //      v_table - object to record response:
     //          v_table.addRow({ ... })                - adds a row to the result set.
     //              keys are the column names of the table definition.
     //              sys_id must be non-empty and uniquely identify each row.
     //                  the above rule will be strictly enforced for editable tables, and generate warnings for read-only tables.
     //                  sys_id will be supplied to the Update, and Delete scripts to specify the row's identity.
 
     //      v_query - the query definition:
     //          v_query.getEncodedQuery()              - encoded querystring
     //          v_query.getCondition(field)            - encoded querystring for the given field (includes field name, operator, and value)
     //          v_query.getParameter(field)            - parameter for the given field (only includes value for equality conditions)
     //          v_query.isGet()                        - whether the query is a single get by sys_id
     //          v_query.getSysId()                     - parameter for sys_id field
     //          v_query.isTextSearch()                 - whether the query contains a text query parameter
     //          v_query.getTextSearch()                - text search query parameter (internal field name 123TEXTQUERY321)
     //          v_query.getFirstRowWanted()            - the first row to include, don't use with caching
     //          v_query.getLastRowWanted()             - the last row to include, don't use with caching
     //          v_query.setLastErrorMessage(message)   - the message is visible from GlideRecord.getLastErrorMessage()
 
     // Sample code:
     //  try {
     //      retrieve-rows-from-external-system;     //      if (there-was-an-error) {
     //          var message = ...;     //          v_query.setLastErrorMessage(message);
     //          return;
     //      }
     //
     //      for (var row in rows) {
     //          v_table.addRow(row);
     //      }
     //  } catch (ex) {
     //      var message = ex.getMessage();
     //      v_query.setLastErrorMessage(message);
     //  }
 
  })(v_table, v_query);
```

</td></tr><tr><td>

Insert

</td><td>

The insert script definition adds a record to the external source. This script definition is available only if you selected the advanced **Editable** option. From the Insert section, customize the script using the v\_record API.

 Every time a record is added to a remote table, the associated insert scripts runs.

 ```javascript
function executeInsert(v_record) {
     // Parameters:
     //      v_record is a map of field names and values containing the sys_id of the
     //              record and the fields that need to be inserted in the record on the
     //              remote system (source of data)
     
     //          v_record.<field_name>                   - fields in the remote table GlideRecord
     //          v_record.setLastErrorMessage(message)   - signal an error
 
     // Sample code:
     //  try {
     //      update-external-system;
     //      if (there-was-an-error) {
     //          var message = ...;
     //          v_record.setLastErrorMessage(message);
     //      }
     //  } catch (ex) {
     //      var message = ex.getMessage();
     //      v_record.setLastErrorMessage(message);
     //  }
  })(v_record);
```

</td></tr><tr><td>

Update

</td><td>

The update script definition modifies a record in the external source. This script definition is available only if you selected the advanced **Editable** option. From the Update section, customize the script using the v\_record API.

 Every time a record is updated in a remote table, the associated update scripts runs.

 **Note:** If multiple users update the same record at the same time, the value on the remote system is from the last update call executed.

 ```javascript
(function executeUpdate(v_record, v_changed_fields) {
     // Parameters:
     //    v_record - a map of field names and values containing the sys_id of the record
     //          v_record.<field_name>                   - fields in the remote table GlideRecord
     //          v_record.setLastErrorMessage(message)   - signal an error
     //    v_changed_fields - a map of field names and values containing the sys_id of the record
     //          v_changed_fields.<field_name>           - changed fields in the remote table GlideRecord
 
     // Sample code:
     //  try {
     //      update-external-system;
     //      if (there-was-an-error) {
     //          var message = ...;
     //          v_record.setLastErrorMessage(message);
     //      }
     //  } catch (ex) {
     //      var message = ex.getMessage();
     //      v_record.setLastErrorMessage(message);
     //  }
  })(v_record, v_changed_fields);
```

</td></tr><tr><td>

Delete

</td><td>

The delete script definition removes a record from the external source. This script definition is available only if you selected the advanced **Editable** option. From the Delete section, customize the script using the v\_record API.

 Every time a record is deleted from a remote table, the associated delete scripts runs.

 ```javascript
(function executeDelete(v_record) {
     // Parameters:
     //      v_record - a map of field names and values containing (among others) the
     //              sys_id of the record that needs to be deleted on the remote system
     //          v_record.<field_name>                  - fields in the remote table GlideRecord
     //          v_record.setLastErrorMessage(message)   - signal an error
 
     // Sample code:
     //  try {
     //      update-external-system;
     //      if (there-was-an-error) {
     //          var message = ...;
     //          v_record.setLastErrorMessage(message);
     //      }
     //  } catch (ex) {
     //      var message = ex.getMessage();
     //      v_record.setLastErrorMessage(message);
     //  }
  })(v_record);
```

</td></tr></tbody>
</table>6.  Select **Submit**.


-   **[Example 1: Retrieving all incident records from an external source](../reference/remote-table-script-def-example1.md)**  
These are examples of script definitions you might create for retrieval and caching of data from sources external to your current instance. In this first example, we create a script to load all incident records from an external source.
-   **[Example 2: Retrieving specific records from a third-party source](../reference/remote-table-script-def-example2.md)**  
In this example, we create a script to retrieve specific types of incident records from a third-party source.
-   **[Example 3: Insert a record in an external source](../reference/remote-table-script-def-example3.md)**  
In this example, we create a script to insert an incident record into the external source.
-   **[Example 4: Update a record in an external source](../reference/remote-table-script-def-example4.md)**  
In this example, we create a script to update an incident record in the external source.
-   **[Example 5: Delete a record in an external source](../reference/remote-table-script-def-example5.md)**  
In this example, we create a script to delete an incident record from the external source.

**Parent Topic:**[Remote tables](../concept/remote-tables.md)

