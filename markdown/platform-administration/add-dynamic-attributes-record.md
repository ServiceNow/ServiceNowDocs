---
title: Add dynamic attributes to a record
description: Store dynamic attributes and their values on a record.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Storing dynamic attributes on a record, Dynamic Schema, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Add dynamic attributes to a record

Store dynamic attributes and their values on a record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the table that holds your dynamic attribute store field.

2.  Create a new record by selecting **New**.

3.  In the dynamic schema reference field you created, select the group, groups, category, or categories that contain the attributes that you want to store on the record.

4.  Call setValue\(\) in the GlideRecord API and send data to the dynamic attribute store field.


## Setting a value in the voltage attribute in a Product table record

```javascript
var gr = new GlideRecord(‘products’);
gr.setValue(‘groups_json->global_electronics_group->voltage’, 40);
gr.insert();

```

In the example, the schema was defined a dynamic schema with a category of **groups\_json**, a group of **global\_electronics\_group** and an attribute of **voltage**. A typical example may be **category = Television**, **group = dimensions**, **attribute = screen size**.

**Parent Topic:**[Storing dynamic attributes on a record](../concept/storing-dynamic-attributes.md)

