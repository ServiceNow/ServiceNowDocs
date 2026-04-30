---
title: HistoryWalker - Scoped, Global
description: The HistoryWalker API uses the audit/history tables to generate a historical version of an existing record. This historical version contains all updates to all fields for the specified glide record.Instantiates the HistoryWalker object and retrieves the historic data for the specified glide record.Fetches the database record based on the parameters, using the History Sets or Audit data to retrieve the historic data, depending on the third parameter.Gets the update number of the current walked glide record.Gets the record filled with the history/audit data after walking to an update number.Returns a copy of the record filled with the history/audit data after walking to an update number.Specifies if the record-level read access is applied on the record when retrieving from the database.Specifies if the record-level read access is applied on the record when retrieving from the database.Specifies if any of the methods that walk the record from one update to another, support the "changes" data for each element.Specifies if journal type fields are populated from the historical values.Specifies if values are set for variables that are recorded in the history.Sets the field-level read access on each element before setting the historical value of that element in the GlideRecord. If the field-level security is enabled, it prevents the API from populating the fields of the walked record that the user of the API doesn't have access to.Sets the record-level read access on the record when retrieving from the database. The record-level security prevents the API from retrieving the walked record if the user of the API doesn't have access to the GlideRecord.Sets the "changes" data support for each element for a method that walks the record from one update to another.Specifies if journal type fields are populated from the historical values.Specifies if variables are populated from the historical values.Applies the appropriate history/audit data to get a walked GlideRecord to the state when it was one update number backward. If the previous update count is missing from the history/audit data, it will walk to the previous available update count.Applies the appropriate history/audit data to get a walked GlideRecord to the state when it was one update number forward. If next update count is missing from the history/audit data, it will walk to the next available update count.Applies the appropriate history/audit data to get a GlideRecord to the state it was in a specific update count. Use getWalkedRecord\(\) or getWalkedRecordCopy\(\) after walking to an update number to retrieve the "walked" GlideRecord.Applies the appropriate history/audit data to get a GlideRecord to the state it was in for a specific record internal checkpoint. Use the getWalkedRecord\(\) or getWalkedRecordCopy\(\) method after walking to a record's internal checkpoint to retrieve the "walked" GlideRecord.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 18
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# HistoryWalker - Scoped, Global

The HistoryWalker API uses the audit/history tables to generate a historical version of an existing record. This historical version contains all updates to all fields for the specified glide record.

This API provides the ability to return a GlideRecord to a previous update count \(walked GlideRecord\) with the appropriate glide elements populated. After the walked GlideRecord is retrieved, the API provides the ability to move forward and backward between the update numbers, navigating through its historical updates.

This API enables you to:

-   Instruct the HistoryWalker API to use a specific history walker implementation to retrieve audit data.
-   Navigate through the historical version of a glide record.
-   Apply the appropriate history/audit data to get an existing GlideRecord to the state it was in a specific update count.
-   Turn off row-level access control.
-   Turn off field-level access control.
-   Turn off retrieval and processing of "changes" data.
-   Enable journal fields.
-   Enable variables.

The HistoryWalker API provides four ways to retrieve audit data:

1.  HISTORY - History walker

    If not available or not up to date, creates a History Set \[sys\_history\_set\] record for the glide record that you passed when instantiating the HistoryWalker API, using the data in the Sys Audit \[sys\_audit\] table. The sys\_history\_set table contains the name of the associated History \[sys\_history\_line\] table. The sys\_history\_line table contains a record for each field value that has been updated in the table being walked. Using this retrieval method, HistoryWalker methods retrieve history data from the generated sys\_history\_line table, instead of directly querying the sys\_audit table.

    The records within the sys\_history\_line table are sorted and grouped by ascending Update \[update\] field values rather than by chronological order. The update field is loosely associated with the Updates \[sys\_mod\_count\] field on the task table.

    **Note:** Updates of the sys\_mod\_count by clients is not synchronized and therefore can be overwritten, making this count unreliable.

2.  AUDIT - Audit walker

    Queries the sys\_audit table for the glide record that you passed when instantiating the HistoryWalker API. Each record in the sys\_audit table contains the changes to field values that occurred through the life of the record.

    Records are sorted ascending by the Update count \[record\_checkpoint\] field rather than by chronological order. The record\_checkpoint field is loosely associated with the Updates \[sys\_mod\_count\] field on the task table. One-to-one correlation is not guaranteed.

    Things to consider when deciding whether to use the AUDIT retrieval method:

    -   Size of the sys\_audit table. The sys\_audit table can become quite large as the changes for all fields in all records are maintained in this table.
    -   Possible lack of update zero record depending on the setting of the system property **glide.sys.audit\_inserts**. This property defines whether an audit record is created with the initial field values when a record is first inserted in a table. In a base system, this property is set to "false" causing the HistoryWalker API to do additional processing to account for this missing information.
    As such, running the HistoryWalker API with AUDIT isn't as performant as either HISTORY or CHECKPOINT.

3.  CHECKPOINT - Checkpoint walker

    Uses a hybrid approach to obtain historical data from the sys\_history\_set or sys\_audit table depending on the setting of the system property **com.glide.history\_walker.max\_history\_count**. If the record to walk has a sys\_mod\_count that exceeds the value set in this property, default value = 1,000, the checkpoint walker uses the sys\_audit table to obtain history data. Otherwise it uses the sys\_history\_set table.

    The reason for this check is that the sys\_history\_set table provides a more performant approach for walking history data, but only up to a certain point. When the total number of field updates reaches a certain level, approximately 10K, the generation of the sys\_history\_set table can exceed the user transaction timeout. If the timeout is exceeded, the overall results are worse in performance than running against the sys\_audit table that contains all table updates. The checkpoint walker uses the **com.glide.history\_walker.max\_history\_count** to determine the optimal record set to use to achieve the best performance.

    Records are grouped and sorted ascending by the Record Internal Checkpoint \[internal\_checkpoint\] field. Since the internal\_checkpoint field is a timestamp, the records are in chronological order. In addition, the internal\_checkpoint field has no association to the task.sys\_mod\_count field.

    The most important difference between the checkpoint walker and other walkers is that the other walkers are coupled to and driven by task.sys\_mod\_count entries and related to sys\_audit.record\_checkpoint and sys\_history\_line.update. The checkpoint walker uses the sys\_audit.internal\_checkpoint and sys\_history\_line.internal\_checkpoint fields respectively.

    The record internal checkpoint addresses both of these issues making the checkpoint walker the most reliable way to retrieve audit history data.

4.  OFFLINE - Offline history walker

    Provides the offline history feature used by applications such as the Field Service mobile offline app. When a task table extension has fields with the dictionary attribute offline\_timestamp\_field set, the offline history walker runs irrespective of any property or explicit instruction to use another walker. The offline history walker uses the sys\_history\_line and sys\_history\_set tables, which contain history data purposely ordered by date and time, to support offline updates. Only the offline history walker can give accurate results for such tables.

    **Note:** For offline updates, the HistoryWalker API is initiated automatically and the only two methods that you can use are: walkTo\(0\) and walkForward\(\). You can't call other HistoryWalker methods for offline updates.


The system property **com.snc.walker.default** defines the default type of record walking to perform when instantiating the HistoryWalker API. For upgrading customers, this property is set to "HISTORY". For new customers, this property is set to "CHECKPOINT".

When you instantiate the HistoryWalker API as follows, the **com.snc.walker.default** property determines which record walker implementation the API uses.

```
var hw = new sn_hw.HistoryWalker(<table name>, <sys_id>);
```

You can also pass the type of record walker to use when instantiating the API. It’s advisable to always include the desired walker implementation when instantiating this API.

```
var hw = new sn_hw.HistoryWalker(<table name>, <sys_id>, <walker>);
```

such as:

```
var hw = new sn_hw.HistoryWalker('incident', '1c741bd70b2322007518478d83673af3', 'CHECKPOINT');
```

To use this class in scoped and global applications, use the `sn_hw` namespace identifier. The History Walker plugin \(com.glide.history\_walker\) that is enabled by default is required to access the HistoryWalker API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## HistoryWalker - HistoryWalker\(String tableName, String sysId, String walker\)

Instantiates the HistoryWalker object and retrieves the historic data for the specified glide record.

<table id="table_sdw_1tl_qbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

String

</td><td>

Name of table that contains the record to retrieve.

</td></tr><tr><td>

sysId

</td><td>

String

</td><td>

Sys\_id of the record whose historic data you want to retrieve.

</td></tr><tr><td>

walker

</td><td>

String

</td><td>

Optional. Name of the history walker to use to retrieve the historic data for the specified record.Valid values:

-   AUDIT
-   CHECKPOINT
-   HISTORY
-   OFFLINE

Default: Walker specified in the system property com.snc.walker.default.

</td></tr></tbody>
</table>The following code example shows how to call this method to walk through the changes made to the GlideRecord using the checkpoint walker.

```

var gr_Hw = new GlideRecord('sc_req_item');
gr_Hw.get('b0d3335d49534210f877468e89703a7c');
 
var hw = new sn_hw.HistoryWalker(gr_Hw.getTableName(), gr_Hw.getUniqueValue(), 'CHECKPOINT');
hw.walkTo('19096afcc800000001');
printChangedFields(hw);
 
function printChangedFields(hw) {
   var walkedGr = hw.getWalkedRecord();
   var fields = GlideScriptRecordUtil.get(walkedGr).getChangedFieldNames();
   gs.info('Fields changed at update ' + hw.getUpdateNumber() + ' were:');
   for (var j = 0; j < fields.size(); j++) {
      var fieldName = fields.get(j) + '';
      if (fieldName !== 'variables')
         gs.info(walkedGr.getValue('sys_updated_on') + ' ' + fieldName + '=' + walkedGr.getValue(fieldName));
   }
 
   var variables = walkedGr.variables;
   for (var variableName in variables) {
      if (variables[variableName].changes())
         gs.info(walkedGr.getValue('sys_updated_on') + ' ' + variableName + '=' + variables[variableName].getValue());
   }
   gs.info('');
}
```

Output:

```
Fields changed at update 3 were:
2024-07-09 08:50:21 price=1499
2024-07-09 08:50:21 state=2
2024-07-09 08:50:21 priority=2
2024-07-09 08:50:21 recurring_price=100
```

## HistoryWalker - HistoryWalker\(String tableName, String sysId, Boolean useAudit\)

Fetches the database record based on the parameters, using the History Sets or Audit data to retrieve the historic data, depending on the third parameter.

<table id="table_h5d_ycn_qbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

String

</td><td>

Name of table containing the record to retrieve.

</td></tr><tr><td>

sysId

</td><td>

String

</td><td>

Sys\_id of the record to retrieve.

</td></tr><tr><td>

useAudit

</td><td>

Boolean

</td><td>

Flag that indicates whether to use audit data to retrieve historic date.Valid values:

-   true: Use audit data to retrieve historic date.
-   false: Use history set to retrieve historic date.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');

var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue(), true);
if (hw.walkTo(3)) {
    var oldPriority = hw.getWalkedRecord().priority;
    gs.info('Incident priority in update number ' + hw.getUpdateNumber() + ' was ' + oldPriority);
} else
    gs.info('Incident does not have update number 3');

```

Output:

```
Incident priority in update number 3 was 4
```

## HistoryWalker - getUpdateNumber\(\)

Gets the update number of the current walked glide record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|int|Current update number or -1 if record is not found.|

The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');

var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
for(int i = 0; i < 2; i++) {
  hw.walkForward();
}
gs.info('Update number: ' + hw.getUpdateNumber());
```

Output:

```
Update number: 3
```

## HistoryWalker - getWalkedRecord\(\)

Gets the record filled with the history/audit data after walking to an update number.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|The walked GlideRecord.|

The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');
 
var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
hw.walkForward();
var walkedRecord = hw.getWalkedRecord();
gs.info('Priority in update number 0: ' + walkedRecord.priority);
hw.walkForward();
walkedRecord = hw.getWalkedRecord();
gs.info('Short description in update number 1: ' + walkedRecord.short_description);
```

Output:

```
 Priority in update number 0: 4
Short description in update number 1: My monitor has stopped working
```

## HistoryWalker - getWalkedRecordCopy\(\)

Returns a copy of the record filled with the history/audit data after walking to an update number.

**Note:** The getWalkedRecord\(\) method might modify the obtained walkedRecord after walking to another update number. The getWalkedRecordCopy\(\) method gets a clone to the walked record to prevent that.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|Copy of the walked GlideRecord.|

The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');
 
var walkedRecord = [];
var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
hw.walkForward();
walkedRecord[0] = hw.getWalkedRecordCopy();
hw.walkForward();
walkedRecord[1] = hw.getWalkedRecordCopy();
 
gs.info('Priority in update number 0: ' + walkedRecord[0].priority);
gs.info('Short description in update number 1: ' + walkedRecord[1].short_description);
```

Output:

```
Priority in update number 0: 4
Short description in update number 1: My monitor has stopped working
```

## HistoryWalker - isFieldLevelSecurity\(\)

Specifies if the record-level read access is applied on the record when retrieving from the database.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ycy_1vs_qbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether field-level security is enabled.Valid values:

-   true: Field-level security is enabled.
-   false: Field-level security isn't enabled.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');

var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
gs.info('Field level security is active: ' + hw.isFieldLevelSecurity());
```

Output:

```
Field level security is active: true
```

## HistoryWalker - isRecordLevelSecurity\(\)

Specifies if the record-level read access is applied on the record when retrieving from the database.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_prv_jts_qbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether record-level security is enabled.Valid values:

-   true: Record-level security is enabled.
-   false: Record-level security isn't enabled.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');

var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
gs.info('Record level security is active: ' + hw.isRecordLevelSecurity());

```

Output:

```
Record level security is active: true
```

## HistoryWalker - isWithChanges\(\)

Specifies if any of the methods that walk the record from one update to another, support the "changes" data for each element.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_zs5_nrs_qbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether change support is enabled.Valid values:

-   true: Change support is enabled.
-   false: Change support isn't enabled.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');

var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
gs.info('Changes is active: ' + hw.isWithChanges());
```

Output:

```
Changes is active: true
```

## HistoryWalker - isWithJournalFields\(\)

Specifies if journal type fields are populated from the historical values.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_smd_1ws_qbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether journal fields are populated.Valid values:

-   true: Journal fields are populated.
-   false: Journal fields aren't populated.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');

var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
gs.info('Populating journal fields is active: ' + hw. isWithJournalFields());

```

Output:

```
Populating journal fields is active: false
```

## HistoryWalker - isWithVariables\(\)

Specifies if values are set for variables that are recorded in the history.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qhm_jxs_qbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether values are set for variables that are recorded in the history.Valid values:

-   true: Values are set.
-   false: Values aren't set.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');

var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
gs.info('Populating variables is active: ' + hw. isWithVariables());
```

Output:

```
Populating variables is active: false
```

## HistoryWalker - setFieldLevelSecurity\(Boolean fieldLevelSecurity\)

Sets the field-level read access on each element before setting the historical value of that element in the GlideRecord. If the field-level security is enabled, it prevents the API from populating the fields of the walked record that the user of the API doesn't have access to.

<table id="table_clj_xts_qbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldLevelSecurity

</td><td>

Boolean

</td><td>

Flag that indicates how to set the field-level read access security.Valid values:

-   true: Enable field-level security.
-   false: Disable field-level security.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');
 
var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
hw.setFieldLevelSecurity(false);
hw.walkForward();
```

## HistoryWalker - setRecordLevelSecurity\(Boolean recordLevelSecurity\)

Sets the record-level read access on the record when retrieving from the database. The record-level security prevents the API from retrieving the walked record if the user of the API doesn't have access to the GlideRecord.

<table id="table_trq_kss_qbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

recordLevelSecurity

</td><td>

Boolean

</td><td>

Flag that indicates how to set the record-level read access security.Valid values:

-   true: Enable record-level security.
-   false: Disable record-level security.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');

var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
hw.setRecordLevelSecurity(false);
hw.walkForward();
```

## HistoryWalker - setWithChanges\(Boolean withChanges\)

Sets the "changes" data support for each element for a method that walks the record from one update to another.

<table id="table_ob3_c2n_qbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

withChanges

</td><td>

Boolean

</td><td>

Flag that indicates whether the changes data is supported for each element.Valid values:

-   true: Change data is supported for each element.
-   false: Change data is not supported for each element.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This code example shows how to call this method with Changes data support. This example must be run in global scope.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');
var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
while (hw.walkForward()) {
  printChangedFields(hw);
}

function printChangedFields(hw) {
  var walkedGr = hw.getWalkedRecord();
  var fields = GlideScriptRecordUtil.get(walkedGr).getChangedFieldNames();
  gs.info("Fields changed at update " + hw.getUpdateNumber() + " were:");
  for (var j = 0; j < fields.size(); j++)
    gs.info(" " + fields.get(j));
  gs.info("");
}
```

This code example shows how to call this method without Changes data support. This example runs in both scoped and global environments.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');
var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
hw.setWithChanges(false);

while (hw.walkForward()) {
  var oldPriority = hw.getWalkedRecord().priority;
  gs.info('Incident priority in update number ' + hw.getUpdateNumber() + ' was ' + oldPriority);
}
```

## HistoryWalker - setWithJournalFields\(Boolean withJournalFields\)

Specifies if journal type fields are populated from the historical values.

<table id="table_nz1_nvs_qbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

withJournalFields

</td><td>

Boolean

</td><td>

Flag that indicates whether to include journal-type fields.Valid values:

-   true: Include journal-type fields.
-   false: Don't include journal-type fields.

Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');
var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
hw.setWithJournalFields(true);
if (hw.walkForward()) {
  var workNotes = hw.getWalkedRecord().work_notes;
  gs.info('Work Notes in update number ' + hw.getUpdateNumber() + ' was ' + workNotes);
}
```

## HistoryWalker - setWithVariables\(Boolean withVariables\)

Specifies if variables are populated from the historical values.

<table id="table_v4q_rws_qbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

withVariables

</td><td>

Boolean

</td><td>

Flag that indicates whether variables are populated from the historical values.Valid values:

-   true: Variable are populated.
-   false: Variable aren't populated.

Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');

var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
hw.setWithVariables(true);
hw.walkTo(0);
if (hw.walkTo(0)) {
    var varUrgency = hw.getWalkedRecord().variables.urgency;
    gs.info('Variable Urgency in update number ' + hw.getUpdateNumber() + ' was ' + varUrgency);
}

```

## HistoryWalker - walkBackward\(\)

Applies the appropriate history/audit data to get a walked GlideRecord to the state when it was one update number backward. If the previous update count is missing from the history/audit data, it will walk to the previous available update count.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_sc3_nzs_qbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether walking to the specified update number was possible.Valid values:

-   true: Able to walk to the specified update number.
-   false: Unable to walk to the specified update number.

Possible reasons: Already walked to the update number 0.


</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');
var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());

while (hw.walkBackward()) {
  var oldPriority = hw.getWalkedRecord().priority;
  gs.info('Incident priority in update number ' + hw.getUpdateNumber() + ' was ' + oldPriority);
}
```

Output:

```
Incident priority in update number 5 was 2
Incident priority in update number 4 was 4
Incident priority in update number 3 was 4
Incident priority in update number 2 was 4
Incident priority in update number 1 was 4
Incident priority in update number 0 was 4

```

## HistoryWalker - walkForward\(\)

Applies the appropriate history/audit data to get a walked GlideRecord to the state when it was one update number forward. If next update count is missing from the history/audit data, it will walk to the next available update count.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_tpm_bzs_qbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether walking to the specified update number was possible.Valid values:

-   true: Able to walk to the specified update number.
-   false: Unable to walk to the specified update number.

Possible reasons: Already walked to the GlideRecord update count.


</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');
var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());

while (hw.walkForward()) {
  var oldPriority = hw.getWalkedRecord().priority;
  gs.info('Incident priority in update number ' + hw.getUpdateNumber() + ' was ' + oldPriority);
}
```

Output:

```
Incident priority in update number 0 was 4
Incident priority in update number 1 was 4
Incident priority in update number 2 was 4
Incident priority in update number 3 was 4
Incident priority in update number 4 was 4
Incident priority in update number 5 was 2
 
```

## HistoryWalker - walkTo\(int updateCount\)

Applies the appropriate history/audit data to get a GlideRecord to the state it was in a specific update count. Use getWalkedRecord\(\) or getWalkedRecordCopy\(\) after walking to an update number to retrieve the "walked" GlideRecord.

**Note:** This method is not supported by the checkpoint walker implementation. Call the [HistoryWalker - walkTo\(String checkpoint\)](HistoryWalkerScopedAPI.md#) method when using the checkpoint walker.

|Name|Type|Description|
|----|----|-----------|
|updateCount|Integer|Update number to walk to.|

<table id="table_qjv_jys_qbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether walking to the specified update number was possible.Valid values:

-   true: Able to walk to the specified update number.
-   false: Unable to walk to the specified update number.

Possible reasons: The requested update is greater than the update count of the GlideRecord or there is no history/audit data for the requested update number.


</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var incGr = new GlideRecord('incident');
incGr.get('number', 'INC0000015');

var hw = new sn_hw.HistoryWalker(incGr.getTableName(), incGr.getUniqueValue());
if (hw.walkTo(3)) {
    var oldPriority = hw.getWalkedRecord().priority;
    gs.info('Incident priority in update number ' + hw.getUpdateNumber() + ' was ' + oldPriority);
} else
    gs.info('Incident does not have update number 3');
```

Output:

```
Incident priority in update number 3 was 4
```

## HistoryWalker - walkTo\(String checkpoint\)

Applies the appropriate history/audit data to get a GlideRecord to the state it was in for a specific record internal checkpoint. Use the getWalkedRecord\(\) or getWalkedRecordCopy\(\) method after walking to a record's internal checkpoint to retrieve the "walked" GlideRecord.

**Note:** This method is only supported by the checkpoint walker implementation.

|Name|Type|Description|
|----|----|-----------|
|checkpoint|String|Record's internal checkpoint to walk to. You can find this value in the internal\_checkpoint field of the Sys Audit \[sys\_audit\] or History \[sys\_history\_line\] table.|

<table id="table_qjv_jys_qbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether walking to the specified record's internal checkpoint was possible.Possible values:

-   true: Able to walk to the specified record's internal checkpoint.
-   false: Unable to walk to the specified record's internal checkpoint.

Possible reasons: The internal checkpoint doesn't exist.


</td></tr></tbody>
</table>The following code example shows how to call this method to walk through the changes made to the GlideRecord.

```

var gr_Hw = new GlideRecord('sc_req_item');
gr_Hw.get('b0d3335d49534210f877468e89703a7c');
 
var hw = new sn_hw.HistoryWalker(gr_Hw.getTableName(), gr_Hw.getUniqueValue(), 'CHECKPOINT');
hw.walkTo('19096afcc800000001');
printChangedFields(hw);
 
function printChangedFields(hw) {
   var walkedGr = hw.getWalkedRecord();
   var fields = GlideScriptRecordUtil.get(walkedGr).getChangedFieldNames();
   gs.info('Fields changed at update ' + hw.getUpdateNumber() + ' were:');
   for (var j = 0; j < fields.size(); j++) {
      var fieldName = fields.get(j) + '';
      if (fieldName !== 'variables')
         gs.info(walkedGr.getValue('sys_updated_on') + ' ' + fieldName + '=' + walkedGr.getValue(fieldName));
   }
 
   var variables = walkedGr.variables;
   for (var variableName in variables) {
      if (variables[variableName].changes())
         gs.info(walkedGr.getValue('sys_updated_on') + ' ' + variableName + '=' + variables[variableName].getValue());
   }
   gs.info('');
}
```

Output:

```
Fields changed at update 3 were:
2024-07-09 08:50:21 price=1499
2024-07-09 08:50:21 state=2
2024-07-09 08:50:21 priority=2
2024-07-09 08:50:21 recurring_price=100
```

