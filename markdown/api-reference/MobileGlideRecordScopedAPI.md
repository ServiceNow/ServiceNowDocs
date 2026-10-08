---
title: MobileGlideRecord - Scoped
description: The MobileGlideRecord API provides the subset of GlideRecord available to mobile scripts, for querying and updating records through the mobile scripting environment..Adds an encoded query string to filter records.Deletes the current record.Retrieves a single record by its sys\_id.Retrieves the MobileGlideElement for a specified field, enabling dot-walk method calls.Gets the value of a field from the current record.Inserts the new record into the database.Creates an empty record suitable for population before an insert.Creates an instance of the MobileGlideRecord class for the specified table.Moves to the next record in the result set.Executes the query built with addEncodedQuery\(\) against the on-device database.Sets the value of a field on the current record.Updates the current record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/MobileGlideRecordScopedAPI.html
release: brazil
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideRecord - Scoped

The MobileGlideRecord API provides the subset of GlideRecord available to mobile scripts, for querying and updating records through the mobile scripting environment..

Unlike a server-side GlideRecord, which doesn't enforce access controls, this class enforces read, write, and execute access checks on every field access. A field that the current user doesn't have permission to read returns an empty value. This behavior matches the data synced to the device, which is filtered by access controls before it reaches the user, so a script returns the same result wherever it's evaluated.

Unlike a server-side GlideRecord, which doesn't enforce access controls, this class enforces read, write, and execute access checks on every field access. A field that the current user doesn't have permission to read returns an empty value. This behavior matches the data synced to the device, which is filtered by access controls before it reaches the user, so a script returns the same result wherever it's evaluated. Records can be filtered with an encoded query, which supports a subset of the available operators. For the supported operators, see documentation for the addEncodedQuery\(\) method.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has a public constructor. For more information, see MobileGlideRecord\(String tableName\).

## MobileGlideRecord - addEncodedQuery\(String query\)

Adds an encoded query string to filter records.

Adds an encoded query to filter the records. See the supported operators in the relevant documentation. See supported operatorshere Delegates to the underlying GlideRecordSecure's user-encoded-query method, not the unsafe encoded-query method. Field-level access controls are enforced on the query conditions themselves.

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

Encoded [query string](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/c_EncodedQueryStrings.md). For example, "active=true^priority&lt;=2". Only the listed operators are supported. See the previous table for supported encoded query operators for MobileGlideRecord.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example calls addEncodedQuery\_S.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('active=true^priority<=2');
gr.query();
```

## MobileGlideRecord - deleteRecord\(\)

Deletes the current record.

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
</table>This example calls deleteRecord.

```
var deleted = gr.deleteRecord();
mgs.info(deleted);
```

Output:

```
true
```

## MobileGlideRecord - get\(String sysId\)

Retrieves a single record by its sys\_id.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|Sys\_id of the record to load. Maximum length: 32.|

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether the record was found and loaded. Possible values: true, the record was found and loaded; false, the record was not found.|

This example calls get\_S.

```
var gr = new MobileGlideRecord('wm_task');
if (gr.get(current.getValue('sys_id'))) {
  mgs.info('loaded');
}
```

Output:

```
"loaded"
```

## MobileGlideRecord - getElement\(String field\)

Retrieves the MobileGlideElement for a specified field, enabling dot-walk method calls.

Dot operator field access is equivalent to this method — `gr.priority` resolves to the exact same [MobileGlideElement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideElementScopedAPI.md) as `gr.getElement('priority')`, including chaining through reference fields \(for example, `current.caller_id.name`\). Every example in this document that writes `current.<field>` is using this mechanism rather than calling `getElement()` explicitly.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field to access.|

|Type|Description|
|----|-----------|
|[MobileGlideElement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideElementScopedAPI.md)|Element wrapper for the field. See [MobileGlideElement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideElementScopedAPI.md) for its methods.|

This example calls getElement\_S.

```
var el = gr.getElement('state');
mgs.info(el.getDisplayValue());
```

Output:

```
"In Progress"
```

## MobileGlideRecord - getValue\(String field\)

Gets the value of a field from the current record.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field to read.|

|Type|Description|
|----|-----------|
|String|Internal value of the field. Returns null if field does not resolve to a real field on the table, or if the current user lacks read access to it. Returns an empty string if the field exists, is readable, and is simply empty.|

This example calls getValue\_S.

```
mgs.info(gr.getValue('short_description'));
```

## MobileGlideRecord - insert\(\)

Inserts the new record into the database.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the newly created record. Returns null on any insert failure — access-control denial, a read-only table, being blocked by an access handler, or a table-level validation error. Never throws. The underlying platform records a failure reason internally, but MobileGlideRecord does not expose a method to read it — a script can detect that insert\(\) failed but not why.|

This example calls insert.

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
"9c0c1f2a3b4c5d6e7f8091a2b3c4d5e6"
```

## MobileGlideRecord - initialize\(\)

Creates an empty record suitable for population before an insert.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void|Populates the record with table defaults, ready for setValue\(\)/insert\(\).|

This example calls initialize.

```
var gr = new MobileGlideRecord('wm_task');
gr.initialize();
```

## MobileGlideRecord - MobileGlideRecord\(String tableName\)

Creates an instance of the MobileGlideRecord class for the specified table.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table to query or update.|

This example creates a MobileGlideRecord for the wm\_task table.

```
var gr = new MobileGlideRecord('wm_task');
```

## MobileGlideRecord - next\(\)

Moves to the next record in the result set.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether another record is available and was advanced to. Possible values: true, another record was advanced to; false, the result set is exhausted.|

This example calls next.

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
"WM0001001"
"WM0001002"
```

## MobileGlideRecord - query\(\)

Executes the query built with addEncodedQuery\(\) against the on-device database.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example calls query.

```
var gr = new MobileGlideRecord('wm_task');
gr.addEncodedQuery('active=true');
gr.query();
```

## MobileGlideRecord - setValue\(String field, String value\)

Sets the value of a field on the current record.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field to set.|
|value|String|New internal value for the field.|

|Type|Description|
|----|-----------|
|void| |

This example calls setValue\_S\_S.

```
gr.setValue('priority', '1');
```

## MobileGlideRecord - update\(\)

Updates the current record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the updated record.|

This example calls update.

```
gr.setValue('priority', '1');
gr.update();
```

