---
title: MobileGlideRecord - Scoped
description: The MobileGlideRecord API provides the subset of GlideRecord available to mobile scripts, for querying and updating records through the mobile scripting environment.Creates an instance of the MobileGlideRecord class for the specified table. Use the new instance to query, read, insert, update, or delete records in that table.Adds an encoded query to filter the records that the query returns. Only the operators listed in the following table are supported. Field-level access controls apply to the fields used in the query conditions.Deletes the current record, which is the record loaded by get\(\) or advanced to by next\(\).Loads a single record by its sys\_id. If the record is found, the MobileGlideRecord points to it and a script can read its fields.Gets the MobileGlideElement for a field, so a script can call element methods such as getDisplayValue\(\). Reading a field with the dot operator, such as gr.priority, does the same thing.Gets the internal value of a field on the current record, as a string.Inserts the new record into the table and returns its sys\_id. Call initialize\(\) and setValue\(\) first to define the record.Creates a new, empty record with the table's default values, ready for a script to set field values and insert.Moves to the next record in the result set so a script can read its fields. Returns false when no records remain.Runs the query, including any conditions added with addEncodedQuery\(\), and loads the matching records into the result set. Call next\(\) to read each record.Sets the value of a field on the current record. The change is not saved until the script calls update\(\) or insert\(\).Saves the changes made to the current record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/MobileGlideRecordScopedAPI.html
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 16
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideRecord - Scoped

The MobileGlideRecord API provides the subset of GlideRecord available to mobile scripts, for querying and updating records through the mobile scripting environment.

Unlike a server-side GlideRecord, which doesn't enforce access controls, this class enforces read, write, and execute access checks on every field access. A field that the current user doesn't have permission to read returns an empty value. This behavior matches the data synced to the device, which is filtered by access controls before it reaches the user, so a script returns the same result wherever it's evaluated. Records can be filtered with an encoded query, which supports a subset of the available operators. For the supported operators, see documentation for the addEncodedQuery\(\) method.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

This API contains the following capabilities:

-   Creating a MobileGlideRecord object: [MobileGlideRecord - MobileGlideRecord\(String tableName\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md)
-   Querying records: [MobileGlideRecord - addEncodedQuery\(String query\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md), [MobileGlideRecord - query\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md), [MobileGlideRecord - next\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md), [MobileGlideRecord - get\(String sysId\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md)
-   Reading field values: [MobileGlideRecord - getValue\(String field\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md), [MobileGlideRecord - getElement\(String field\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md)
-   Creating and updating records: [MobileGlideRecord - initialize\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md), [MobileGlideRecord - setValue\(String field, String value\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md), [MobileGlideRecord - insert\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md), [MobileGlideRecord - update\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md)
-   Deleting records: [MobileGlideRecord - deleteRecord\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md)

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has a public constructor, [MobileGlideRecord - MobileGlideRecord\(String tableName\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md).

## MobileGlideRecord - MobileGlideRecord\(String tableName\)

Creates an instance of the MobileGlideRecord class for the specified table. Use the new instance to query, read, insert, update, or delete records in that table.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table to query or update, such as `wm_task`.|

This example creates a MobileGlideRecord for the wm\_task table.

```
var gr = new MobileGlideRecord('wm_task');
```

This example defines a helper function that counts the active records in any table, using a table name that the caller passes in.

```
function countActive(tableName) {
        var gr = new MobileGlideRecord(tableName);
        gr.addEncodedQuery('active=true');
        gr.query();
        var count = 0;
        while (gr.next()) {
        count++;
        }
        return count;
        }
        
        mgs.info('Active tasks: ' + countActive('wm_task'));
```

Output:

```
Active tasks: 2
```

## MobileGlideRecord - addEncodedQuery\(String query\)

Adds an encoded query to filter the records that the query returns. Only the operators listed in the following table are supported. Field-level access controls apply to the fields used in the query conditions.

|Operator|Description|Incident encoded query example|
|--------|-----------|------------------------------|
|`^`|\(AND\) Combines multiple conditions so that all conditions must be true for an incident to be returned. This is the default logical operator between conditions in an encoded query. Conditions are evaluated together as a logical AND.|`state=1^priority=2`|
|`^OR`|\(OR\) Combines conditions so that at least one of the conditions must be true. Useful when matching alternative states or fields. OR conditions are evaluated at the same query level unless they're grouped explicitly.|`state=1^ORstate=2`|
|`!=`|Returns incidents where the field value is different from the provided value. Records with empty values are also returned unless they're explicitly filtered.|`state!=7`|
|`<`|Returns incidents where the numeric or date field value is less than the specified value.|`priority<3`|
|`<=`|Returns incidents where the numeric or date field value is less than or equal to the specified value.|`priority<=2`|
|`>`|Returns incidents where the numeric or date field value is greater than the specified value.|`priority>2`|
|`>=`|Returns incidents where the numeric or date field value is greater than or equal to the specified value.|`priority>=4`|
|`LT_FIELD`|Compares two fields on the same incident record and returns records where the first field is earlier or smaller than the second field.|`resolved_atLT_FIELDopened_at`|
|`LT_OR_EQUALS_FIELD`|Same as `LT_FIELD`, but also includes records where both field values are equal.|`closed_atLT_OR_EQUALS_FIELDresolved_at`|
|`GT_FIELD`|Returns incidents where the first field value is greater or later than the second field value.|`resolved_atGT_FIELDopened_at`|
|`GT_OR_EQUALS_FIELD`|Returns incidents where the first field value is greater than or equal to the second field value.|`sys_updated_onGT_OR_EQUALS_FIELDsys_created_on`|
|`BETWEEN`|Returns incidents where the field value falls within the specified inclusive range. Commonly used for numeric priority ranges or date ranges.|`priorityBETWEEN2@4`|
|`ISEMPTY`|Returns incidents where the field has no value at all, including null references.|`assigned_toISEMPTY`|
|`ISNOTEMPTY`|Returns incidents where the field contains any value.|`assigned_toISNOTEMPTY`|
|`ISEMPTYSTRING`|Returns incidents where the field value is an empty string rather than null. Applies mainly to string fields.|`short_descriptionISEMPTYSTRING`|
|`LIKE`|Performs a case-insensitive partial match using wildcard logic. Returns incidents where the field contains the specified pattern.|`short_descriptionLIKEemail`|
|`NOT LIKE`|Excludes incidents where the field matches the provided pattern.|`short_descriptionNOT LIKEtest`|
|`CONTAINS`|Similar to `LIKE`, but explicitly expresses substring containment for readability.|`descriptionCONTAINSnetwork`|
|`DOES NOT CONTAIN`|Returns incidents where the field doesn't include the specified substring.|`descriptionDOES NOT CONTAINwifi`|
|`STARTSWITH`|Returns incidents where the field value begins with the specified string. Often used with incident numbers.|`numberSTARTSWITHINC`|
|`ENDSWITH`|Returns incidents where the field value ends with the specified string.|`caller_id.emailENDSWITH@company.com`|
|`IN_FIELD`|Compares two fields and returns incidents where the value of the first field exists within the value set of the second field.|`assigned_toIN_FIELDwatch_list`|
|`IN`|Returns incidents where the field value matches one of the provided values in a comma-separated list.|`stateIN1,2,3`|
|`NOT IN`|Returns incidents where the field value doesn't match any value in the provided list.|`priorityNOT IN1,5`|
|`ON`|Returns incidents where a date or date-time field falls on a specific calendar day.|`sys_created_onON2025-01-10`|
|`NOTON`|Excludes incidents created or updated on a specific calendar day.|`sys_created_onNOTON2025-01-10`|
|`SAMEAS`|Returns incidents where the values of two fields are identical. Often used for reference comparisons.|`assigned_toSAMEASopened_by`|
|`NSAMEAS`|Returns incidents where the values of two fields are different.|`assigned_toNSAMEASopened_by`|
|`MORETHAN`|Compares duration or numeric fields and returns incidents where the first field is greater than the second field.|`calendar_durationMORETHANbusiness_duration`|
|`LESSTHAN`|Compares duration or numeric fields and returns incidents where the first field is less than the second field.|`calendar_durationLESSTHANbusiness_duration`|
|`RELATIVEGT`|Returns incidents where the date field is later than a relative time expression, such as greater than one day ago.|`sys_created_onRELATIVEGT@day@ago@1`|
|`RELATIVEGE`|Same as `RELATIVEGT`, but also includes values equal to the relative time threshold.|`sys_updated_onRELATIVEGE@hour@ago@24`|
|`RELATIVELT`|Returns incidents where the date field is earlier than a relative time expression.|`sys_created_onRELATIVELT@day@ago@7`|
|`RELATIVELE`|Returns incidents where the date field is earlier than or equal to the relative time expression.|`sys_updated_onRELATIVELE@minute@ago@30`|
|`RELATIVEEE`|Returns incidents where the date field exactly matches the relative time expression.|`sys_created_onRELATIVEEE@day@ago@0`|
|`MATCH_RGX_FIELD`|Matches the target field against a regular expression stored in another field.|`short_descriptionMATCH_RGX_FIELDu_regex_pattern`|
|`MATCH_RGX`|Applies a regular expression directly to the field value.|`short_descriptionMATCH_RGX^INC[0-9]+`|
|`VALCHANGES`|Returns incidents where the specified field has changed at any point in its update history.|`stateVALCHANGES`|
|`DYNAMIC`|Uses a ServiceNow dynamic filter that resolves at run time, such as the current user.|`assigned_toDYNAMICme`|

<table id="table_MGR-addEncodedQuery_S_p" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

query

</td><td>

String

</td><td>

Encoded [query string](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_EncodedQueryStrings.md). For example, `"active=true^priority<=2"`.See the previous table for supported encoded query operators for MobileGlideRecord.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example filters work order tasks to those that are active and have a priority of 1 or 2, and then runs the query.

```
var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('active=true^priority<=2');
        gr.query();
```

This example filters work order tasks to the active, high-priority tasks that are assigned to the current user, and logs how many it found. A button condition can use this count to show a My urgent tasks button only when there are tasks to work on.

```
var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('assigned_toDYNAMICme^active=true^priority<=2');
        gr.query();
        var count = 0;
        while (gr.next()) {
        count++;
        }
        mgs.info('My urgent tasks: ' + count);
```

Output:

```
My urgent tasks: 2
```

## MobileGlideRecord - deleteRecord\(\)

Deletes the current record, which is the record loaded by get\(\) or advanced to by next\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGR-deleteRecord_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the record was deleted successfully.Possible values:

-   true: The record was deleted.
-   false: The record was not deleted.

</td></tr></tbody>
</table>This example loads a work order task by its sys\_id, deletes it, and logs whether the delete succeeded.

```
var gr = new MobileGlideRecord('wm_task');
        if (gr.get(current.getValue('sys_id'))) {
        var deleted = gr.deleteRecord();
        mgs.info(deleted);
        }
```

Output:

```
true
```

This example deletes the draft child tasks of the current record and logs how many were deleted. A write-back action can use this to clean up tasks that were created in error. The script counts only the deletes that succeed.

```
var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('parent=' + current.getValue('sys_id') + '^short_descriptionSTARTSWITHDRAFT');
        gr.query();
        var removed = 0;
        while (gr.next()) {
        if (gr.deleteRecord()) {
        removed++;
        }
        }
        mgs.info('Deleted ' + removed + ' draft tasks');
```

Output:

```
Deleted 2 draft tasks
```

## MobileGlideRecord - get\(String sysId\)

Loads a single record by its sys\_id. If the record is found, the MobileGlideRecord points to it and a script can read its fields.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|Sys\_id of the record to load. Maximum length: 32.|

<table id="table_MGR-get_S_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the record was found and loaded.Possible values:

-   true: The record was found and loaded.
-   false: The record was not found.

</td></tr></tbody>
</table>This example loads a work order task by its sys\_id and logs a message if the record is found.

```
var gr = new MobileGlideRecord('wm_task');
        if (gr.get(current.getValue('sys_id'))) {
        mgs.info('loaded');
        }
```

Output:

```
loaded
```

This example loads the parent of the current task and logs its number. The script checks the result of get\(\) so it can handle a parent that isn't found.

```
var parentTask = new MobileGlideRecord('wm_task');
        if (parentTask.get(current.getValue('parent'))) {
        mgs.info('Parent task: ' + parentTask.getValue('number'));
        } else {
        mgs.info('Parent task not found.');
        }
```

Output:

```
Parent task: WM0001001
```

## MobileGlideRecord - getElement\(String field\)

Gets the MobileGlideElement for a field, so a script can call element methods such as getDisplayValue\(\). Reading a field with the dot operator, such as `gr.priority`, does the same thing.

Dot operator field access is equivalent to this method — `gr.priority` resolves to the exact same [MobileGlideElement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md) as `gr.getElement('priority')`, including chaining through reference fields \(for example, `current.caller_id.name`\). Every example in this document that writes `current.<field>` is using this mechanism rather than calling `getElement()` explicitly.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field to access.|

|Type|Description|
|----|-----------|
|[MobileGlideElement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md)|Element wrapper for the field. See [MobileGlideElement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md) for its methods.|

This example loads a work order task, gets the element for its state field, and logs the state label.

```
var gr = new MobileGlideRecord('wm_task');
        if (gr.get(current.getValue('sys_id'))) {
        var el = gr.getElement('state');
        mgs.info(el.getDisplayValue());
        }
```

Output:

```
In Progress
```

This example defines a helper function that logs the name and display value of any field. Use getElement\(\) when the field name is stored in a variable, because the dot operator needs the name to be written in the script.

```
function showField(gr, fieldName) {
        var el = gr.getElement(fieldName);
        return el.getName() + ': ' + el.getDisplayValue();
        }
        
        mgs.info(showField(current, 'state'));
```

Output:

```
state: In Progress
```

## MobileGlideRecord - getValue\(String field\)

Gets the internal value of a field on the current record, as a string.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field to read.|

|Type|Description|
|----|-----------|
|String|Internal value of the field. Returns `null` if the field does not exist on the table or the current user does not have read access to it. Returns an empty string if the field is readable and has no value.|

This example logs the short description of the current record.

```
mgs.info(current.getValue('short_description'));
```

Output:

```
Replace filter in unit 4
```

This example tells apart a field the user can't read, an empty field, and a field with a value. A script can use this check to avoid treating a field that is hidden by access controls as an empty field.

```
var assignee = current.getValue('assigned_to');
        if (assignee === null) {
        mgs.info('Assigned to is not readable.');
        } else if (assignee === '') {
        mgs.info('Unassigned');
        } else {
        mgs.info('Assigned');
        }
```

Output:

```
Assigned
```

## MobileGlideRecord - insert\(\)

Inserts the new record into the table and returns its sys\_id. Call initialize\(\) and setValue\(\) first to define the record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the new record. Returns `null` if the insert fails for any reason, such as an access control denial, a read-only table, or a table-level validation error. The method does not throw an error, and a script cannot read the reason for a failure.|

This example creates a follow-up task for the current record and logs the sys\_id of the new task.

```
var gr = new MobileGlideRecord('wm_task');
        gr.initialize();
        gr.setValue('parent', current.getValue('sys_id'));
        gr.setValue('short_description', 'Follow-up required');
        var newSysId = gr.insert();
        mgs.info(newSysId);
```

Output:

```
9c0c1f2a3b4c5d6e7f8091a2b3c4d5e6
```

This example creates a high-priority follow-up task and checks the result of insert\(\). Because the method returns `null` when the insert fails, a script should check the return value before it uses the new record.

```
var gr = new MobileGlideRecord('wm_task');
        gr.initialize();
        gr.setValue('parent', current.getValue('sys_id'));
        gr.setValue('short_description', 'Follow-up required');
        gr.setValue('priority', '2');
        var newSysId = gr.insert();
        if (newSysId) {
        mgs.info('Follow-up task created: ' + newSysId);
        } else {
        mgs.info('Follow-up task could not be created.');
        }
```

Output:

```
Follow-up task created: 9c0c1f2a3b4c5d6e7f8091a2b3c4d5e6
```

## MobileGlideRecord - initialize\(\)

Creates a new, empty record with the table's default values, ready for a script to set field values and insert.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void|None. The record is populated with the table's default values and is ready for setValue\(\) and insert\(\).|

This example creates a MobileGlideRecord for the wm\_task table and prepares a new record with default values.

```
var gr = new MobileGlideRecord('wm_task');
        gr.initialize();
```

This example creates a checklist of child tasks for the current record and logs how many were created. The script creates a new MobileGlideRecord and calls initialize\(\) for each task.

```
var steps = ['Inspect equipment', 'Replace filter', 'Test system'];
        var created = 0;
        for (var i = 0; i < steps.length; i++) {
        var gr = new MobileGlideRecord('wm_task');
        gr.initialize();
        gr.setValue('parent', current.getValue('sys_id'));
        gr.setValue('short_description', steps[i]);
        if (gr.insert()) {
        created++;
        }
        }
        mgs.info('Created ' + created + ' tasks');
```

Output:

```
Created 3 tasks
```

## MobileGlideRecord - next\(\)

Moves to the next record in the result set so a script can read its fields. Returns `false` when no records remain.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGR-next_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether another record is available and was advanced to. Possible values:

-   true: Another record was advanced to.
-   false: The result set is exhausted.

</td></tr></tbody>
</table>This example queries the active work order tasks and logs the number of each one.

```
var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('active=true');
        gr.query();
        while (gr.next()) {
        mgs.info(gr.getValue('number'));
        }
```

Output:

```
WM0001001
        WM0001002
```

This example finds the first unassigned active task and logs its number. Use `if` instead of `while` when the script needs only one record.

```
var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('active=true^assigned_toISEMPTY');
        gr.query();
        if (gr.next()) {
        mgs.info('Next unassigned task: ' + gr.getValue('number'));
        } else {
        mgs.info('No unassigned tasks.');
        }
```

Output:

```
Next unassigned task: WM0001001
```

## MobileGlideRecord - query\(\)

Runs the query, including any conditions added with addEncodedQuery\(\), and loads the matching records into the result set. Call next\(\) to read each record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example queries the active work order tasks. The script must call next\(\) to read the records.

```
var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('active=true');
        gr.query();
```

This example queries the urgent tasks that are not assigned and logs their numbers in a single message, such as for a dispatcher's summary.

```
var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('active=true^priority<=2^assigned_toISEMPTY');
        gr.query();
        var urgent = [];
        while (gr.next()) {
        urgent.push(gr.getValue('number'));
        }
        mgs.info('Urgent unassigned: ' + urgent.join(', '));
```

Output:

```
Urgent unassigned: WM0001001, WM0001002
```

## MobileGlideRecord - setValue\(String field, String value\)

Sets the value of a field on the current record. The change is not saved until the script calls update\(\) or insert\(\).

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field to set, such as `priority`.|
|value|String|New internal value for the field. For a choice field, this is the stored value, not the label shown to the user.|

|Type|Description|
|----|-----------|
|void| |

This example sets the priority field to its internal value for a critical task.

```
gr.setValue('priority', '1');
```

This example copies the priority and builds a short description from the current record, such as to prepare a follow-up task. The values are passed as strings. The new record isn't saved until the script calls insert\(\).

```
var gr = new MobileGlideRecord('wm_task');
        gr.initialize();
        gr.setValue('short_description', 'Follow-up: ' + current.getValue('short_description'));
        gr.setValue('priority', current.getValue('priority'));
        mgs.info(gr.getValue('short_description'));
```

Output:

```
Follow-up: Replace filter
```

## MobileGlideRecord - update\(\)

Saves the changes made to the current record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the updated record.|

This example sets the priority of the current record and saves the change.

```
gr.setValue('priority', '1');
        gr.update();
```

This example loads a work order task, sets its state to work in progress, saves the change, and logs the sys\_id that update\(\) returns. A write-back action can use this pattern when a technician starts a job.

```
var gr = new MobileGlideRecord('wm_task');
        if (gr.get(current.getValue('sys_id'))) {
        gr.setValue('state', '2');
        var updatedSysId = gr.update();
        mgs.info('Updated task: ' + updatedSysId);
        }
```

Output:

```
Updated task: 9c0c1f2a3b4c5d6e7f8091a2b3c4d5e6
```

