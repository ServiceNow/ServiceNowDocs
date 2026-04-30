---
title: v\_record - Scoped, Global
description: The v\_record API enables you to sets an exception or error message on a remote table record. Remote tables allow you to retrieve data from external sources or from another instance with REST or SOAP services.Sets an exception or error message to display during editable operations on a remote table record in the form or list view, and in system logs.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# v\_record - Scoped, Global

The v\_record API enables you to sets an exception or error message on a remote table record. Remote tables allow you to retrieve data from external sources or from another instance with REST or SOAP services.

This API executes wherever GlideRecord create, update, and delete methods are used in a script with no changes to workspaces or lists and forms.

This API requires the Remote Tables plugin \(com.glide.script.vtable\) to be activated. For more information, see [Create script definitions for a remote table](https://www.servicenow.com/docs/access?context=create-remote-table-script&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Use v\_record with the [v\_query – Scoped, Global](../../v_query/concept/v_queryAPI.md#) scriptable object to query remote tables, and the [v\_table – Scoped, Global](../../v_table/concept/v_tableAPI.md#) API to create remote tables.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## v\_record - setLastErrorMessage\(String lastErrorMessage\)

Sets an exception or error message to display during editable operations on a remote table record in the form or list view, and in system logs.

**Note:** v\_record represents the remote record on which the insert, update, or delete operation is executed, therefore no tables are updated as a result of using this method.

|Name|Type|Description|
|----|----|-----------|
|lastErrorMessage|String|Exception or error message to display as the last error or exception in the remote table record. Displays on the form or list view, and is written to the system log.|

|Type|Description|
|----|-----------|
|None| |

The following example sets the exception message "Exception encountered executing the insert" to display during editable operations on a remote table record:

```
(function executeInsert(v_record) { 
   try{ 
//add logic to insert the record in the remote table 
   } catch(ex) { 
      v_record.setLastErrorMessage("Exception encountered executing the insert");
   } 
})(v_record); 
(function executeUpdate(v_record, v_changed_fields) { 
   try{
//add logic to update the record in the remote table from the changed fields in 	
// v_changed_fields 
   }catch(ex) { 
      v_record.setLastErrorMessage("Exception encountered executing the update"); 
   } 
})
(v_record, v_changed_fields); 
(function executeDelete(v_record) { 
   try{ 
//add logic to delete the record in the remote table 
   }catch(ex) { 
      v_record.setLastErrorMessage("Exception encountered executing the delete"); 
   } 
})(v_record);
```

Output:

```
"Exception encountered executing the insert"
```

The output is the exception message that was set using setLastErrorMessage\(\) when there is an exception in the operation performed on the remote system \(such as insert, update, delete\). If there is no exception returned, the operation is considered a success.

