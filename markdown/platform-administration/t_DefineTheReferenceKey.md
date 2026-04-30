---
title: Define the reference key
description: By default, reference fields store the sys\_id of the record in the database.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Add a reference field, Reference field type, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Define the reference key

By default, reference fields store the sys\_id of the record in the database.

## Before you begin

Role required: personalize\_dictionary

## About this task

By defining a reference key, you can identify a field other than sys\_id to use as the unique identifier for the reference field. The value of the reference key field, instead of the sys\_id, is stored in the database for that reference field.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Open the field record \(for example, **resolved\_by** on the Incident table\).

3.  In the **Reference key** field, enter a field name on the referenced table \(for example, email on the sys\_user table\).

    **Note:** Always choose a field from the referenced table that is both required and unique.

4.  Select **Update**.


**Parent Topic:**[Add a reference field](t_AddAReferenceField.md)

