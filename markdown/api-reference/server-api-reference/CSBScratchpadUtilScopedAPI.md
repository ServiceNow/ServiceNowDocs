---
title: CSBScratchpadUtil - Scoped
description: The CSBScratchpadUtil API allows consumers to share "extra" information that is outside of any other Service Exchange service, with their providers.Returns the value of a specified scratchpad property.Returns the property names and values \(name-value pairs\) of all scratchpad properties associated with the specified task.Returns the list of names of all scratchpad properties associated with the specified task record.Places the scratchpad properties associated with the specified remote task or provider task in the client g\_scratchpad.Deletes the specified scratchpad property from the Scratchpad \[sn\_sb\_scratchpad\] table.Inserts a property or updates the value of a property in the Scratchpad \[sn\_sb\_scratchpad\] table.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CSBScratchpadUtil- Scoped

The CSBScratchpadUtil API allows consumers to share "extra" information that is outside of any other Service Exchange service, with their providers.

This information is stored as name-value pairs in the Scratchpad \[sn\_sb\_scratchpad\] table. The shared information must be associated with tasks that are of one of two types: provider tasks or remote tasks.

If the associated task is active, the updated scratchpad information syncs to the consumer instance. If a task is deactivated or deleted, the information in the scratchpad is also deleted after a specified number of days; by default three. This default is defined in the sn\_sb.scratchpad.autodelete.days property.

Both providers and consumers can add, update, and remove information to and from the Scratchpad table. Producers update this information using the [PSBScratchpadUtil - Scoped](../../PSBScratchpadUtil/concept/PSBScratchpadUtilScopedAPI.md#) API.

To access this API, the Service Exchange for Consumers application must be installed. This API runs in the `sn_sb_con` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CSBScratchpadUtil - get\(GlideRecord taskGR, String name\)

Returns the value of a specified scratchpad property.

<table id="table_sm3_fpg_czb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

taskGR

</td><td>

GlideRecord

</td><td>

GlideRecord of the active remote task or provider task associated with the specified scratchpad property. Tables: Remote task \[sn\_sb\_con\_remote\_task\] and Provider task \[sn\_sb\_con\_provider\_task\].

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Name of the scratchpad property whose value to retrieve. Table: Scratchpad \[sn\_sb\_scratchpad\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String or null|Value of the requested scratchpad property. Null if the property isn't found.|

The following code example shows how to call this method.

```
var rtGR = new GlideRecord("sn_sb_con_remote_task");
rtGR.setLimit(1); 
rtGR.query();  
rtGR.next() 
if (rtGR.isValidRecord()) { 
  var util = new sn_sb_con.CSBScratchpadUtil();
  util.update(rtGR, "name1", "value1"); 
  gs.info(util.get(rtGR, "name1"));
}
```

Output:

```
"value1"
```

## CSBScratchpadUtil - getAll\(GlideRecord taskGR\)

Returns the property names and values \(name-value pairs\) of all scratchpad properties associated with the specified task.

<table id="table_ism_vpg_czb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

taskGR

</td><td>

GlideRecord

</td><td>

GlideRecord of the active remote task or provider task whose associated scratchpad properties to return. Table: Remote task \[sn\_sb\_con\_remote\_task\] and Provider task \[sn\_sb\_con\_provider\_task\] tables.

</td></tr></tbody>
</table><table id="table_jsm_vpg_czb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

All property names and values contained in the specified task. For example:

`{ name1: value1, name2: value2, … }`

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var rtGR = new GlideRecord("sn_sb_con_remote_task");
rtGR.setLimit(1);
rtGR.query();  
rtGR.next() 
if (rtGR.isValidRecord()) {  
  var util = new sn_sb_con.CSBScratchpadUtil();
  util.update(rtGR, "name1", "value1"); 
  gs.info(JSON.stringify(util.getAll(rtGR))); 
}
```

Output:

```
{ "name1": "value1" }
```

## CSBScratchpadUtil - getNames\(GlideRecord taskGR\)

Returns the list of names of all scratchpad properties associated with the specified task record.

<table id="table_r5k_dqg_czb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

taskGR

</td><td>

GlideRecord

</td><td>

GlideRecord of the active remote task or provider task for which to return the list of names of all associated scratchpad properties. Table: Remote task \[sn\_sb\_con\_remote\_task\] and Provider task \[sn\_sb\_con\_provider\_task\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String Array|List of names of the scratchpad properties associated with the specified task record.|

The following code example shows how to call this method.

```
var rtGR = new GlideRecord("sn_sb_con_remote_task");
rtGR.setLimit(1); 
rtGR.query();  
rtGR.next() 
if (rtGR.isValidRecord()) {
  var util = new sn_sb_con.CSBScratchpadUtil();
  util.update(rtGR, "name1", "value1"); 
  gs.info(JSON.stringify(util.getNames(rtGR))); 
}
```

Output:

```
[ "name1" ]
```

## CSBScratchpadUtil - populateClientScratchpadBR\(GlideRecord taskGR\)

Places the scratchpad properties associated with the specified remote task or provider task in the client g\_scratchpad.

You can call this method from a UI display business rule.

<table id="table_ikg_qdb_fzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

taskGR

</td><td>

GlideRecord

</td><td>

GlideRecord of the active remote task or provider task whose associated scratchpad entries should be placed in the client g\_scratchpad. Tables: Remote task \[sn\_sb\_con\_remote\_task\] and Provider task \[sn\_sb\_con\_provider\_task\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
new sn_sb_con.CSBScratchpadUtil().populateClientScratchpadBR(current);
```

## CSBScratchpadUtil - remove\(GlideRecord taskGR, String name\)

Deletes the specified scratchpad property from the Scratchpad \[sn\_sb\_scratchpad\] table.

**Note:** Deletes are not synced to other ServiceNow instances. Scratchpad properties are automatically deleted in a specified number of days after the associated task record is deactivated or deleted.

<table id="table_x3b_nqg_czb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

taskGR

</td><td>

GlideRecord

</td><td>

GlideRecord of the active remote task or provider task associated with the specified scratchpad property. Tables: Remote task \[sn\_sb\_con\_remote\_task\] and Provider task \[sn\_sb\_con\_provider\_task\].

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Name of the scratchpad property to remove from the Scratchpad \[sn\_sb\_scratchpad\] table.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var rtGR = new GlideRecord("sn_sb_con_remote_task");
rtGR.setLimit(1); 
rtGR.query();  
rtGR.next() 
if (rtGR.isValidRecord()) {
  var util = new sn_sb_con.CSBScratchpadUtil();
  util.update(rtGR, "name1", "value1"); 
  util.remove(rtGR, “name1”);
  gs.info(util.get(rtGR, "name1")); 
}
```

Output:

```
undefined
```

## CSBScratchpadUtil - update\(GlideRecord taskGR, String name, String value, Boolean client\_side\_accessible\)

Inserts a property or updates the value of a property in the Scratchpad \[sn\_sb\_scratchpad\] table.

**Note:** The maximum number of properties that you can update in one call is 50.

<table id="table_z4p_4kg_czb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

taskGR

</td><td>

GlideRecord

</td><td>

GlideRecord of the active remote task or provider task associated with the specified scratchpad property. Tables: Remote task \[sn\_sb\_con\_remote\_task\] and Provider task \[sn\_sb\_con\_provider\_task\]

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Name of a new or existing scratchpad property. This name must be unique across all scratchpad properties.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Value of the scratchpad property. Maximum: 4000 characters.

</td></tr><tr><td>

client\_side\_accessible

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether this property is available to the client-side g\_scratchpad when populateClientScratchpadBR is called from a display business rule.Valid values:

-   true: Property is available.
-   false: Property isn't available.

Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var rtGR = new GlideRecord("sn_sb_con_remote_task");
rtGR.setLimit(1); 
rtGR.query();
rtGR.next()
if (rtGR.isValidRecord()) {
  var util = new sn_sb_con.CSBScratchpadUtil();
  util.update(rtGR, "name1", "value2");
  gs.info(util.get(rtGR, "name1")); 
} 
```

Output:

```
"value2"
```

