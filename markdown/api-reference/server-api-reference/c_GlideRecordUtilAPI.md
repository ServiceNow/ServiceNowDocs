---
title: GlideRecordUtil - Global
description: The GlideRecordUtil script include is a utility class for working with GlideRecords.Returns the GlideRecord object for the specified configuration item \(CI\) using just the sys\_id of the CI.Returns an array of all the fields in the specified GlideRecord.Returns a GlideRecord instance for the given table, positioned to the given sys\_id, and of the right class \(table\).Returns a list of the ancestors of a specified table.Sets the fields in the specified GlideRecord with the field values contained in the specified hashmap, unless that field name is in the ignore hashmap.Populates a given hashmap from a GlideRecord. Each field in the GlideRecord becomes a property in the hashmap.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
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
|[GlideRecord](../../GlideRecord/concept/c_GlideRecordAPI.md#)|GlideRecord object of the specified CI.|

The following example returns the GlideRecord object for the specified CI using just the sys\_id of the CI.

```
var now_GR = new GlideRecordUtil().getCIGR("2dfd7c8437201000deeabfc8bcbe5d56");
```

## GlideRecordUtil - getFields\(GlideRecord gr\)

Returns an array of all the fields in the specified GlideRecord.

**Note:** If there is a field name which is the same as the table name, the getFields\(\) method does not return the value of the field.

|Name|Type|Description|
|----|----|-----------|
|gr|[GlideRecord](../../GlideRecord/concept/c_GlideRecordAPI.md#)|GlideRecord instance positioned to a valid record.|

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
|[GlideRecord](../../GlideRecord/concept/c_GlideRecordAPI.md#)|The GlideRecord for the specified sys\_id.|

```
var now_GR = new GlideRecordUtil().getGR("cmdb_ci_computer", "2dfd7c8437201000deeabfc8bcbe5d56");
```

## GlideRecordUtil - getTables\(String tableName\)

Returns a list of the ancestors of a specified table.

**Note:** The specified table is included in the list of its ancestors.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table.|

|Type|Description|
|----|-----------|
|Array|List of ancestors of the specified table.|

The following example shows the ancestors of the Linux Server \[cmdb\_ci\_linux\_server\] table.

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
|now\_GR|[GlideRecord](../../GlideRecord/concept/c_GlideRecordAPI.md#)|The GlideRecord instance to receive the field values.|
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

Populates a given hashmap from a GlideRecord. Each field in the GlideRecord becomes a property in the hashmap.

<table id="table_czg_4lw_4t" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

hashMap

</td><td>

Object

</td><td>

The object to populate with fields and values from a GlideRecord.

</td></tr><tr><td>

now\_GR

</td><td>

[GlideRecord](../../GlideRecord/concept/c_GlideRecordAPI.md#)

</td><td>

A GlideRecord instance positioned to a valid record.

</td></tr><tr><td>

ignore

</td><td>

Object

</td><td>

Optional. A hashmap of field names to exclude when populating the object.For each key-value pair in the map, the key is the name of the field to exclude and the value is `true`.

```
{"field_name": true}
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example populates an object with fields and values from a Computer \[cmdb\_ci\_computer\] record.

```
var util = new GlideRecordUtil();
var objectToPopulate = {};
var computer = util.getCIGR("2dfd7c8437201000deeabfc8bcbe5d56"); // get CI record from cmdb_ci_computer
var ignore = {"sys_created_on": true, "sys_updated_by": true};
util.populateFromGR(objectToPopulate, computer, ignore);
// Now objectToPopulate contains field/value pairs from the computer GlideRecord
gs.info(JSON.stringify(objectToPopulate));
```

Output:

```
{
   "sys_id": "2dfd7c8437201000deeabfc8bcbe5d56",
   "operational_status": "1",
   "os_service_pack": "Service Pack 2",
   "cpu_manufacturer": "7aad6d00c611228400f00e0f80b67d2d",
   "sys_updated_on": "2024-07-27 22:28:37",
   "first_discovered": "2007-03-13 20:55:20",
   "invoice_number": "INV0166221",
   "sys_created_by": "admin",
   "warranty_expiration": "2019-10-07",
   "ram": "1534",
   "cpu_name": "Intel(R) Pentium(R) M processor 1.86GHz",
   "cpu_speed": "798",
   "sys_domain_path": "/",
   "disk_space": "51",
   "cost_center": "d9d0a971c0a80a641c20b13d99a48576",
   "assigned": "2024-03-16 07:00:00",
   "purchase_date": "2018-10-07",
   "last_discovered": "2007-04-12 23:17:45",
   "can_print": "0",
   "sys_class_name": "cmdb_ci_computer",
   "manufacturer": "aa0a6df8c611227601cd2ed45989e0ac",
   "cpu_count": "1",
   "vendor": "aa0a6df8c611227601cd2ed45989e0ac",
   "assigned_to": "47de9c73c61122930033f6521d1bb785",
   "os_version": "5.1.2600",
   "serial_number": "L3BB911",
   "cd_rom": "0",
   "unverified": "0",
   "asset": "8bc1ba8837f3100044e0bfc8bcbe5db9",
   "cpu_core_count": "1",
   "skip_sync": "0",
   "sys_domain": "global",
   "install_date": "2023-10-06 08:00:00",
   "asset_tag": "P1000227",
   "hardware_status": "installed",
   "install_status": "1",
   "name": "*ASSET-IBM",
   "virtual": "0",
   "po_number": "PO27711",
   "sys_class_path": "/!!/!2/!(",
   "company": "a66b1fb03710200044e0bfc8bcbe5d08",
   "department": "221f79b7c6112284005d646b76ab978c",
   "cost": "3665",
   "os": "Windows XP Professional",
   "sys_mod_count": "17",
   "monitor": "0",
   "model_id": "a9a2d0c3c6112276010db16c5ddd3461",
   "cost_cc": "USD",
   "location": "8225b668ac1d55eb679878e192fca315",
   "category": "Do not migrate to asset",
   "fault_count": "0"
}
```

