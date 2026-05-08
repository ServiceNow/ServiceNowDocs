---
title: Add dynamic attributes to a record
description: Store dynamic attributes and their values on a record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with Dynamic Schema, Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Add dynamic attributes to a record

Store dynamic attributes and their values on a record.

## Before you begin

Role required: none

To add attributes to a dynamic attribute store field, you must have write access to the table where the store field is located.

## About this task

Once you create a dynamic attribute store field and set up the dynamic categories and dynamic attributes for its namespace, you can use one or more of the dynamic attributes to describe your records.

## Procedure

1.  Navigate to the table that holds your dynamic attribute store field.

2.  Create a record by selecting **New**.

3.  In the category reference field, select the dynamic category that contains the dynamic attributes that you want to use.

4.  Capture one or more dynamic attributes in the dynamic attribute store field by entering JSON or using the API.

<table id="choicetable_vrc_vx4_zfc"><thead><tr><th align="left" id="d116086e84">

Option

</th><th align="left" id="d116086e87">

Description

</th></tr></thead><tbody><tr><td id="d116086e93">

**Enter JSON**

</td><td>

Enter one or more attributes and values in the dynamic store field. For example:```
{ "watts: 50" , "screen_size": "75", "screen_type" : "OLED" }
```

</td></tr><tr><td id="d116086e104">

**Use the API**

</td><td>

Call setValue\(\) in the GlideRecord API and send data to the dynamic attribute store field. For example:```javascript
var gr = new GlideRecord(‘products’);
gr.setValue(‘televisions->watts’, '50');
gr.setValue(‘televisions->screen_size’, '75');
gr.setValue(‘televisions->screen_type, 'OLED');
gr.insert();
```

</td></tr></tbody>
</table>
## Result

One or more dynamic attributes and their values are stored in the record. Users can query for records that have some value for an attribute. For example:

```javascript
var gr = new GlideRecord(‘products’);
gr.addQuery(‘televisions->screen_type', ‘OLED’);
gr.query();
```

