---
title: MobileGlideElement - Scoped
description: The MobileGlideElement API provides the subset of GlideElement available to mobile scripts. An instance is returned when a script dot-walks into a field on a MobileGlideRecord.Determines whether the field value has changed since the record was loaded.Gets the display value of the field.Gets the name of the field.Gets the internal string value of the field.Determines whether the field value is null or empty.Sets the display value of the field.Sets the internal value of the field.Returns the string representation of the field value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/MobileGlideElementScopedAPI.html
release: brazil
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideElement - Scoped

The MobileGlideElement API provides the subset of GlideElement available to mobile scripts. An instance is returned when a script dot-walks into a field on a MobileGlideRecord.

MobileGlideElement provides the subset of GlideElement that can be evaluated against the local database on a device. An instance is returned when a script dot-walks into a field on a [MobileGlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideRecordScopedAPI.md), or accesses `current.<field>` in a condition script. The element carries both the raw value and the display value of a single field, and can report whether the field has been changed. A script can therefore compare the stored value of a field with the value shown to the user, or detect an edit that hasn't been saved to the record yet.

MobileGlideElement also supports field access with the dot operator, which is what enables a chained dot-walk through reference fields. For example, `current.caller_id.name` first resolves `caller_id` to a MobileGlideElement, and then dot-walks `.name` from that element into the referenced record.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no public constructor. Obtain an instance from the `getElement(field)` method of [MobileGlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideRecordScopedAPI.md), or through dot-walk field access, which resolves to the same element.

## MobileGlideElement - changes\(\)

Determines whether the field value has changed since the record was loaded.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether the value has changed since load. Possible values: true, the value changed; false, the value did not change.|

This example calls changes.

```
if (current.priority.changes()) {
  mgs.info('Priority was changed');
}
```

Output:

```
"Priority was changed"
```

## MobileGlideElement - getDisplayValue\(\)

Gets the display value of the field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display value of the field.|

This example calls getDisplayValue.

```
mgs.info(current.state.getDisplayValue());
```

Output:

```
"In Progress"
```

## MobileGlideElement - getName\(\)

Gets the name of the field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Field name. Maximum length: 40.|

This example calls getName.

```
mgs.info(current.priority.getName());
```

Output:

```
"priority"
```

## MobileGlideElement - getValue\(\)

Gets the internal string value of the field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Internal value of the field.|

This example calls getValue.

```
mgs.info(current.state.getValue());
```

Output:

```
"2"
```

## MobileGlideElement - nil\(\)

Determines whether the field value is null or empty.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether the field is null or empty. Possible values: true, the field is null or empty; false, the field has a value.|

This example calls nil.

```
if (current.assigned_to.nil()) {
  mgs.info('Unassigned');
}
```

Output:

```
"Unassigned"
```

## MobileGlideElement - setDisplayValue\(String value\)

Sets the display value of the field.

|Name|Type|Description|
|----|----|-----------|
|value|String|New display value for the field.|

|Type|Description|
|----|-----------|
|void| |

This example calls setDisplayValue\_S.

```
current.state.setDisplayValue('In Progress');
```

## MobileGlideElement - setValue\(Object value\)

Sets the internal value of the field.

|Name|Type|Description|
|----|----|-----------|
|value|Object|New internal value for the field.|

|Type|Description|
|----|-----------|
|void| |

This example calls setValue\_O.

```
current.priority.setValue('1');
```

## MobileGlideElement - toString\(\)

Returns the string representation of the field value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|String representation of the field value.|

This example calls toString.

```
mgs.info(String(current.priority));
```

Output:

```
"1"
```

