---
title: Create a dynamic attribute store field
description: Store dynamic attributes on a record using a dynamic attribute store field.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Storing dynamic attributes on a record, Dynamic Schema, Administering fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a dynamic attribute store field

Store dynamic attributes on a record using a dynamic attribute store field.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the table that you want use for storing dynamic attributes.

3.  In the Table Columns related list, select **New**.

4.  In the Type field, select **Dynamic Attribute Store**.

5.  Complete the form by providing a Column label, Column name, and optional field attributes as necessary.

6.  Select **Submit**.

    The dynamic attribute store field is added to the table.

7.  Create a relationship between the dynamic attribute store field and a dynamic schema reference field.

    1.  Select **Use dependent field**.

    2.  Select the **Dependent on field** drop-down list.

    3.  In the list of elements, select the dynamic schema reference field that you created by following the steps in [Create a dynamic schema reference](create-dynamic-schema-reference.md).

        **Note:** The reference field that the dynamic attribute store field depends on doesn’t need to exist on the same table. You can dot-walk to the dynamic schema metadata from the table that holds the dynamic attribute store field. For example, you might dot-walk from the Product field on your Sold Products table to the Products table to get its schema information.

8.  Select **Update**.


## Add a dynamic attribute store field

![Add a dynamic attribute store field to your table.](../image/dynamic-json-field-example.png)

## Set up the dependency between the dynamic attribute store field and a dynamic schema reference field

![Make the dynamic attribute store field dependent on the reference field.](../image/dynamic-json-dependent-on.png)

## What to do next

[Add dynamic attributes to a record](add-dynamic-attributes-record.md)

