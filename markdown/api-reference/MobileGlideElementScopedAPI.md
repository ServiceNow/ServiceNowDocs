---
title: MobileGlideElement - Scoped
description: The MobileGlideElement API provides the subset of GlideElement available to mobile scripts. An instance is returned when a script dot-walks into a field on a MobileGlideRecord.Determines whether the value of the field has changed since the record was loaded, such as by an edit that has not been saved yet.Gets the value of the field as it is shown to the user, such as the label of a choice or the display value of a referenced record.Gets the name of the field that this element represents, such as priority.Gets the internal value of the field as a string. For a choice field, this is the stored value, not the label shown to the user.Determines whether the field has no value, meaning the value is null or empty.Sets the value of the field using its display value, such as the label of a choice.Sets the internal value of the field, such as the stored value of a choice.Returns the value of the field as a string.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/MobileGlideElementScopedAPI.html
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideElement - Scoped

The MobileGlideElement API provides the subset of GlideElement available to mobile scripts. An instance is returned when a script dot-walks into a field on a MobileGlideRecord.

MobileGlideElement provides the subset of GlideElement that can be evaluated against the local database on a device. An instance is returned when a script dot-walks into a field on a [MobileGlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md), or accesses `current.<field>` in a condition script. The element carries both the raw value and the display value of a single field, and can report whether the field has been changed. A script can therefore compare the stored value of a field with the value shown to the user, or detect an edit that hasn't been saved to the record yet.

MobileGlideElement also supports field access with the dot operator, which is what enables a chained dot-walk through reference fields. For example, `current.caller_id.name` first resolves `caller_id` to a MobileGlideElement, and then dot-walks `.name` from that element into the referenced record.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

This API contains the following capabilities:

-   Getting field values: [MobileGlideElement - getValue\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md), [MobileGlideElement - getDisplayValue\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md), [MobileGlideElement - toString\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md)
-   Setting field values: [MobileGlideElement - setValue\(Object value\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md), [MobileGlideElement - setDisplayValue\(String value\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md)
-   Getting field information: [MobileGlideElement - getName\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md)
-   Checking field state: [MobileGlideElement - nil\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md), [MobileGlideElement - changes\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideElementScopedAPI.md)

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no public constructor. Obtain an instance from the `getElement(field)` method of [MobileGlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideRecordScopedAPI.md), or through dot-walk field access, which resolves to the same element.

## MobileGlideElement - changes\(\)

Determines whether the value of the field has changed since the record was loaded, such as by an edit that has not been saved yet.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGE-changes_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the value of the field has changed since the record was loaded. Possible values: -   `true`: The value has changed.
-   `false`: The value is unchanged.

</td></tr></tbody>
</table>This example checks whether the priority field has changed and logs a message if it has.

```
if (current.priority.changes()) {
        mgs.info('Priority was changed');
        }
```

Output:

```
Priority was changed
```

This example checks whether the priority field has changed and logs the Boolean result.

```
var priorityChanged = current.priority.changes();
        mgs.info('Priority changed: ' + priorityChanged);
```

Output:

```
Priority changed: true
```

This example checks whether either the priority or the state field has changed and logs a single true or false result. A button condition can use this check to show a Notify manager button only after one of those fields is edited.

```
var needsReview = current.priority.changes() || current.state.changes();
        mgs.info('Needs review: ' + needsReview);
```

Output:

```
Needs review: true
```

## MobileGlideElement - getDisplayValue\(\)

Gets the value of the field as it is shown to the user, such as the label of a choice or the display value of a referenced record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of the field as it is shown to the user. For a choice field, this is the choice label.|

This example gets the display value of the state field, which is the label users see, and logs it.

```
mgs.info(current.state.getDisplayValue());
```

Output:

```
In Progress
```

This example builds a status message for users from the record number and the state label. Use the display value for text that users read, and use getValue\(\) for logic.

```
var message = 'Incident ' + current.number.getValue() + ' is now ' + current.state.getDisplayValue();
        mgs.info(message);
```

Output:

```
Incident INC0010025 is now In Progress
```

## MobileGlideElement - getName\(\)

Gets the name of the field that this element represents, such as `priority`.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the field.|

This example gets the name of the priority field and logs it.

```
mgs.info(current.priority.getName());
```

Output:

```
priority
```

This example defines a helper function that logs the name of any field that has no value. Use getName\(\) so the same function works for any field.

```
function logIfEmpty(element) {
        if (element.nil()) {
        mgs.info(element.getName() + ' is required');
        }
        }
        
        logIfEmpty(current.assigned_to);
```

Output:

```
assigned_to is required
```

## MobileGlideElement - getValue\(\)

Gets the internal value of the field as a string. For a choice field, this is the stored value, not the label shown to the user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Internal value of the field, as a string. For example, the stored value of a choice or the sys\_id of a referenced record.|

This example gets the internal value of the state field and logs it.

```
mgs.info(current.state.getValue());
```

Output:

```
2
```

This example checks whether an incident is in progress. A button condition can use this check to show a Resolve button only for incidents in that state. Compare against the internal value, which is always a string, because the label can differ by language.

```
var isInProgress = current.state.getValue() === '2';
        mgs.info('Show Resolve button: ' + isInProgress);
```

Output:

```
Show Resolve button: true
```

## MobileGlideElement - nil\(\)

Determines whether the field has no value, meaning the value is null or empty.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_MGE-nil_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the field has no value. Possible values: -   `true`: The field is null or empty.
-   `false`: The field has a value.

</td></tr></tbody>
</table>This example checks whether the assigned to field has a value and logs a message if it doesn't.

```
if (current.assigned_to.nil()) {
        mgs.info('Unassigned');
        }
```

Output:

```
Unassigned
```

This example checks whether an incident is unassigned. A button condition can use this check to show an Assign to me button only for incidents that no one owns.

```
var canAssign = current.assigned_to.nil();
        mgs.info('Show Assign to me button: ' + canAssign);
```

Output:

```
Show Assign to me button: true
```

## MobileGlideElement - setDisplayValue\(String value\)

Sets the value of the field using its display value, such as the label of a choice.

|Name|Type|Description|
|----|----|-----------|
|value|String|New display value for the field. For a choice field, this is the choice label shown to the user.|

|Type|Description|
|----|-----------|
|void| |

This example sets the state field using the label that users see.

```
current.state.setDisplayValue('In Progress');
```

This example sets the state of an incident to Resolved by its label and logs whether the field changed. A write-back action can use this approach when the label is easier to maintain than the stored value.

```
current.state.setDisplayValue('Resolved');
        mgs.info('State changed: ' + current.state.changes());
```

Output:

```
State changed: true
```

## MobileGlideElement - setValue\(Object value\)

Sets the internal value of the field, such as the stored value of a choice.

|Name|Type|Description|
|----|----|-----------|
|value|Object|New internal value for the field. For a choice field, this is the stored value, not the label shown to the user. For a reference field, this is the sys\_id of the referenced record. The value can be a string, number, or Boolean, depending on the field type.|

|Type|Description|
|----|-----------|
|void| |

This example sets the priority field using its internal value.

```
current.priority.setValue('1');
```

This example sets fields of different types on an incident, such as in a write-back action that resolves a record. The method accepts a value of any type, and the type to pass depends on the field. The script then logs each internal value, which is always returned as a string.

```
// String: a choice field takes its stored value
        current.priority.setValue('2');
        
        // Number: an integer field takes a number
        current.reassignment_count.setValue(3);
        
        // Boolean: a true/false field takes a boolean
        current.active.setValue(false);
        
        // String: a reference field takes the sys_id of the referenced record
        current.assigned_to.setValue('6816f79cc0a8016401c5a33be04be441');
        
        // String: a date-time field takes a value in the internal format
        current.due_date.setValue('2026-09-01 17:00:00');
        
        mgs.info('priority: ' + current.priority.getValue());
        mgs.info('reassignment_count: ' + current.reassignment_count.getValue());
        mgs.info('active: ' + current.active.getValue());
        mgs.info('assigned_to: ' + current.assigned_to.getValue());
        mgs.info('due_date: ' + current.due_date.getValue());
```

Output:

```
priority: 2
        reassignment_count: 3
        active: false
        assigned_to: 6816f79cc0a8016401c5a33be04be441
        due_date: 2026-09-01 17:00:00
```

## MobileGlideElement - toString\(\)

Returns the value of the field as a string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of the field as a string.|

This example calls toString\(\) on the priority field and logs the resulting string.

```
mgs.info(current.priority.toString());
```

Output:

```
1
```

This example converts the short description field to a string so the script can search it with a string method. A button condition can use this check to show an Escalate button only for incidents that mention an outage. A field element is an object, so convert it to a string before you call string methods on it or compare it with `===`.

```
var description = current.short_description.toString();
        var isOutage = description.toLowerCase().indexOf('outage') !== -1;
        mgs.info('Show Escalate button: ' + isOutage);
```

Output:

```
Show Escalate button: true
```

