---
title: Create a dynamic attribute store field
description: Create a dynamic attribute store field for storing transient attributes on a record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with attributes transiently, Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a dynamic attribute store field

Create a dynamic attribute store field for storing transient attributes on a record.

## Before you begin

Role required: admin

## About this task

You can create a dynamic attribute store field to store one or more transient attributes that describe a record. When you create a dynamic attribute store field, the following schema changes occur automatically.

-   A dynamic namespace is automatically created and associated with the dynamic attribute store field. The namespace associated with a store field can be modified at any time.
-   A dynamic category reference field is automatically added to the same table. You can store any dynamic attribute that you want in the store field, but the dynamic category reference field can help users determine which attributes to store.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the table that you want to use for storing attributes.

3.  In the Columns related list, select **New**.

4.  In the Type field, select **Dynamic Attribute Store**.

5.  Complete the form by entering a Column label.

6.  Select **Submit**.


## Result

-   A dynamic attribute store field is added to the table. An associated dynamic namespace is created with the following naming format:

    ```
    <table_name>/<dynamic_attribute_store_column_name>
    ```

-   A dynamic category reference field is added to the table. A dependency relationship is established between the category reference field and the dynamic attribute store field.

## A dynamic attribute store field is added to the Products table

![A dynamic attribute store field called mystore is added to the Products table.](../image/dynamic-store-field-example-transient.png)

## What to do next

Populate the dynamic attribute store field with one or more attributes. See [Add transient attributes to a record](add-transient-attributes.md).

