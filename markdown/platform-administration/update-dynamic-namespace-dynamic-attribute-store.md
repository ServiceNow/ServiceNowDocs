---
title: Associate a dynamic attribute store with a different namespace
description: Use a different set of dynamic attributes in a dynamic attribute store field by changing its associated namespace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Associate a dynamic attribute store with a different namespace

Use a different set of dynamic attributes in a dynamic attribute store field by changing its associated namespace.

## Before you begin

Role required: dynamic\_schema\_writer

## About this task

You can reuse the dynamic attributes and dynamic categories that you define in a dynamic namespace across multiple store fields by updating the namespace specified in the store field's dictionary record.

Changing the namespace associated with a store field can modify the type of an attribute that's captured in the store field. Modifying the type of an attribute doesn't affect any data stored for it, but can change how the system interacts with that data.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the table that contains your dynamic attribute store field.

3.  In the Columns related list, select the dynamic attribute store column that you want to update.

4.  In the Attributes field, enter the name of the dynamic namespace that you want to use after the equals sign.

    For example, change:

    `dynamic_namespace=u_products/u_attributes`

    To:

    `dynamic_namespace=departments`

5.  Select **Update**.


## Result

All the dynamic attributes and dynamic categories that belong to the dynamic namespace that you entered are available to the dynamic attribute store field.

## What to do next

Associate the dynamic namespace with other dynamic attribute store fields by updating the Attributes field in the dictionary entry in each store field.

After each update, delete the dynamic namespace record that was automatically created for the dynamic attribute store field.

