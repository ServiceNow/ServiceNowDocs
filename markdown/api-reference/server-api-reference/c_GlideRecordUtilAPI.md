---
title: GlideRecordUtil - Global
description: The GlideRecordUtil script include is a utility class for working with GlideRecords.Returns the GlideRecord object for the specified configuration item \(CI\) using just the sys\_id of the CI.Returns an array of all the fields in the specified GlideRecord.Returns a GlideRecord instance for the given table, positioned to the given sys\_id, and of the right class \(table\).Returns a Java ArrayList of the ancestors of the specified table name.Sets the fields in the specified GlideRecord with the field values contained in the specified hashmap, unless that field name is in the ignore hashmap.Populates the given hashmap from the given GlideRecord instance. Each field in the GlideRecord becomes a property in the hashmap.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideRecordUtil- Global

The GlideRecordUtil script include is a utility class for working with GlideRecords.

This script include is available in server-side scripts. For use cases, see [Using discovery script includes](../../../../../script/server-scripting/concept/c_ScriptIncludes.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideRecordUtil - getCIGR\(String sys\_id\)

Returns the GlideRecord object for the specified configuration item \(CI\) using just the sys\_id of the CI.

Use this method to quickly obtain a specific CI without knowing its associated class/table.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of the desired CI.|

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord object of the specified CI.|

The following example returns the GlideRecord object for the specified CI using just the sys\_id of the CI.

```
var now_GR = new GlideRecordUtil().getCIGR("2dfd7c8437201000deeabfc8bcbe5d56");
```

## GlideRecordUtil - getFields\(GlideRecord gr\)

Returns an array of all the fields in the specified GlideRecord.

**Note:** If there is a field name which is the same as the table name, the getFields\(\) method does not return the value of the field.

|Name|Type|Description|
|----|----|-----------|
|gr|GlideRecord|GlideRecord instance positioned to a valid record.|

|Type|Description|
|----|-----------|
|Array|Field names for the specified GlideRecord.|

```
var queryString = "priority=1^ORpriority=2";
var now_GR = new GlideRecord('incident');
now_GR.addEncodedQuery(queryString);
now_GR.query();
now_GR.next();

var gRU = new GlideRecordUtil();
var fieldList = gRU.getFields(now_GR);
gs.info(fieldList);
```

Output: Line breaks added for presentation.

```
sys_id,skills,closed_by,assigned_to,contract,category,escalation,state,reassignment_count,location,
time_worked,order,due_date,number,upon_approval,sys_tags,sla_due,follow_up,reopen_count,notify,business_stc,
caused_by,rejection_goto,assignment_group,comments_and_work_notes,incident_state,opened_at,parent_incident,
business_service,wf_activity,calendar_duration,group_list,caller_id,comments,priority,sys_updated_by,
variables,delivery_task,resolved_at,sys_updated_on,parent,active,opened_by,expected_start,watch_list,
company,upon_reject,work_notes,sys_created_by,additional_assignee_list,approval_set,cmdb_ci,user_input,
sys_created_on,close_code,contact_type,resolved_by,rfc,approval_history,activity_due,severity,child_incidents,
,subcategory,work_end,closed_at,close_notes,variables,business_duration,knowledge,approval,sys_domain_path,
sys_mod_count,problem_id,calendar_stc,work_start,sys_domain,correlation_id,sys_class_name,short_description,
impact,description,correlation_display,urgency,made_sla,delivery_plan,work_notes_list
```

## GlideRecordUtil - getGR\(String baseTable, String sys\_id\)

Returns a GlideRecord instance for the given table, positioned to the given sys\_id, and of the right class \(table\).

This method is useful when you need to load a GlideRecord from a sys\_id, but you don't know what the actual table is \(because it may be extended from the base table\). This method always returns a GlideRecord of the correct type base\_table: the name of the base table that the specified sys\_id is in.

|Name|Type|Description|
|----|----|-----------|
|baseTable|String|The name of the base table containing the sys\_id.|
|sys\_id|String|The sys\_id of the desired record.|

|Type|Description|
|----|-----------|
|GlideRecord|The GlideRecord for the specified sys\_id.|

```
var now_GR = new GlideRecordUtil().getGR("cmdb_ci_computer", "2dfd7c8437201000deeabfc8bcbe5d56");
```

## GlideRecordUtil - getTables\(String tableName\)

Returns a Java ArrayList of the ancestors of the specified table name.

For example, given cmdb\_ci\_linux\_server, this would return cmdb\_ci\_linux\_server, cmdb\_ci\_server, cmdb\_ci\_computer, cmdb\_ci\_hardware, cmdb\_ci, and cmdbr.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table.|

|Type|Description|
|----|-----------|
|ArrayList|List of ancestors of the specified table.|

The following example shows the ancestors of the cmdb\_ci\_linux\_server table.

```
var tables = new GlideRecordUtil().getTables("cmdb_ci_linux_server");
gs.info("Tables returned: " + tables);
```

Output:

```
Tables returned: [cmdb_ci_linux_server, cmdb_ci_server, cmdb_ci_computer, cmdb_ci_hardware, cmdb_ci, cmdb]

```

## GlideRecordUtil - mergeToGR\(Object hashMap, GlideRecord now\_GR, Object ignore\)

Sets the fields in the specified GlideRecord with the field values contained in the specified hashmap, unless that field name is in the ignore hashmap.

|Name|Type|Description|
|----|----|-----------|
|hashMap|Object|An Object instance \(being used as a hashmap\), with properties named for fields and containing the fields' value.|
|GlideRecord|GR|The GlideRecord instance to receive the field values.|
|ignore|Object|An optional hashmap of field names to ignore.|

|Type|Description|
|----|-----------|
|void| |

This example updates a computer record's name and os fields, but does not update the sys\_created\_by field:

```
var now_GR = new GlideRecordUtil().getGR("cmdb_ci_computer", "2dfd7c8437201000deeabfc8bcbe5d56");   
var obj = {"name": "xyz", "os": "windows 2000", "sys_created_by", "aleck.lin"};
var ignore = {"sys_created_by": true};
new GlideRecordUtil().mergeToGR(obj, now_GR, ignore);
now_GR.update();
```

## GlideRecordUtil - populateFromGR\(Object hashMap, GlideRecord now\_GR, Object ignore\)

Populates the given hashmap from the given GlideRecord instance. Each field in the GlideRecord becomes a property in the hashmap.

|Name|Type|Description|
|----|----|-----------|
|hashMap|Object|An object being used as a hashmap.|
|now\_GR|GlideRecord|A GlideRecord instance positioned to a valid record.|
|ignore|Object|An optional hashmap of file names not to populate.|

|Type|Description|
|----|-----------|
|void| |

```
var objectToPopulate = {};
var now_GR = new GlideRecordUtil().getGR("cmdb_ci_computer", "2dfd7c8437201000deeabfc8bcbe5d56");
var ignore = {"sys_created_on": true, "sys_updated_by": true};
new GlideRecordUtil().populateFromGR(objectToPopulate, now_GR, ignore);
// Now the objectToPopulate contains field/value pairs from the computer GlideRecord
```

