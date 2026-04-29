---
title: Create a dynamic attribute store field
description: Store dynamic attributes on a record using a dynamic attribute store field.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Dynamic Schema, Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a dynamic attribute store field

Store dynamic attributes on a record using a dynamic attribute store field.

## Before you begin

Role required: admin

## About this task

You can create a dynamic attribute store field to store one or more dynamic attributes that describe a record. When you create a dynamic attribute store field, the following schema changes occur automatically.

-   A dynamic namespace is automatically created and associated with the dynamic attribute store field. Dynamic attributes, dynamic categories and other items defined in the dynamic namespace become available to the store field. You may modify the namespace of a store field at any time without affecting data stored for that field. The system will begin interacting with that data using definitions provided by the new namespace.
-   A dynamic category reference field is automatically added to the same table and associated with the store field. This category reference field provides additional metadata for the store field to guide users when deciding which attributes to add.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the table that you want to use for storing dynamic attributes.

3.  In the Columns related list, select **New**.

4.  In the Type field, select **Dynamic Attribute Store**.

5.  Complete the form by providing a Column label.

6.  Select **Submit**.


## Result

-   A dynamic attribute store field is added to the table. An associated dynamic namespace is created with the following naming format:

    ```
    <table_name>/<dynamic_attribute_store_column_name>
    ```

-   A dynamic category reference field is added to the table. A dependency relationship is established between the category reference field and the dynamic attribute store field.

## New dynamic store field on the Products table

![A dynamic attribute store field is created for capturing attributes about products.](../image/dynamic-store-field-example.png)

## What to do next

Develop your dynamic schema by creating dynamic attributes and dynamic categories. You can build out the schema using either of the following methods:

-   Add dynamic attributes and dynamic categories to the dynamic namespace that's currently associated with the store field you created. Refer to the following topics:
    -   [Create a dynamic attribute](add-dynamic-attributes.md)
    -   [Create a dynamic category](create-dynamic-category.md)
-   Add dynamic attributes and dynamic categories to a new dynamic namespace and then associate that namespace with the store field that you created. Refer to the following topics:
    -   [Create a dynamic namespace](create-dynamic-namespace.md)
    -   [Associate a dynamic attribute store with a different namespace](update-dynamic-namespace-dynamic-attribute-store.md)

