---
title: Add transient attributes to a record
description: Store transient attributes and their values on a record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with attributes transiently, Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Add transient attributes to a record

Store transient attributes and their values on a record.

## Before you begin

Role required: none

To add attributes to a dynamic attribute store field, you must have write access to the table where the store field is located.

## About this task

After creating a dynamic attribute store field on a table, you can immediately start adding attributes to a record without having to define a dynamic attribute record for each attribute. Attributes without a definition are considered transient and are treated as having values of type string when used in scripts and queries.

## Procedure

1.  Navigate to the table that holds your dynamic attribute store field.

2.  Create a record by selecting **New**.

3.  Add one or more attributes directly on the form using JSON or via the API.

<table id="choicetable_hbk_hpf_yfc"><thead><tr><th align="left" id="d81931e78">

Option

</th><th align="left" id="d81931e81">

Description

</th></tr></thead><tbody><tr><td id="d81931e87">

**Enter JSON on the form**

</td><td>

1.  In the category reference field, select the dynamic category that contains the dynamic attributes that you want to use.
2.  Enter one or more attributes and their values. For example:

    ```
"screen_resolution":"2160p","screen_size":"75","screen_type":"OLED"
    ```

</td></tr><tr><td id="d81931e107">

**Call setValue\(\)**

</td><td>

Call setValue\(\) in the GlideRecord API and send data to the dynamic attribute store field.For example:```javascript
var gr = new GlideRecord(‘products’);
gr.setValue(‘television_specs->screen_resolution', '2160p');
gr.setValue('television_specs->screen_size', '75');
gr.setValue('television_specs->screen_type', 'OLED');
gr.insert();
```

</td></tr></tbody>
</table>
## Result

One or more transient attributes are added to the store field, with each value stored as a string. Users can query or search for records using the values captured in the dynamic attribute store field. For example:

```javascript
var gr = new GlideRecord(‘products’);
gr.addQuery(‘television_specs->screen_type', ‘OLED’);
gr.query();
```

## What to do next

Decide whether to create formal definitions for each attribute. Providing a formal definition makes the attribute non-transient and allows you to modify its behavior. To provide this definition, navigate to the dynamic namespace record the store field is configured with and create a dynamic attribute record using the name of the attribute you wish to modify. See [Create a dynamic attribute](add-dynamic-attributes.md).

Note that modifying the definition of an attribute doesn't modify any data stored for that attribute. Rather, it simply modifies how the system interacts with that data. For example, attributes defined as strings sort differently than when defined as integers.

Sorting age values as strings:

```
11
19
2
25
3
```

Sorting age values as integers:

```
2
3
11
19
25
```

Any saved data that might be invalid for its defined type is treated as having a nil value appropriate for the type. For example, storing a value of "dog" for an attribute, and then formally defining it as an integer will effectively use 0 in all queries and calculations that attribute is used in, even though the data stored for the attribute remains as “dog".

