---
title: Working with attributes transiently
description: Start adding attributes and values to records without formally defining a full schema.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Working with attributes transiently

Start adding attributes and values to records without formally defining a full schema.

Implementing Dynamic Schema is a flexible process. To get started, you can simply add attributes and values to a dynamic attribute store field, which helps describe your records without the need for additional table columns. You can add more attributes as needed and start querying and working with them right away.

## Getting started

Implement attributes transiently using the following process.

1.  [Create a dynamic attribute store field](../task/create-dynamic-attribute-store-field-transient.md)

    Get started by creating a dynamic attribute store field for storing attributes on a record.

2.  [Add transient attributes to a record](../task/add-transient-attributes.md)

    After creating the dynamic attribute store field, describe your records by using transient attributes and string values.


## Additional implementation options

When you add attributes to a store field without formally defining them as dynamic attribute records, Dynamic Schema is functional, but limited.

-   Transient attribute values are saved as strings, which limits querying and sorting options.
-   Transient attributes aren't organized into logical categories.
-   Transient attributes don't support choice sets, which give you control over attribute values and where they can be used.

Instead, you can specify additional data types, organize attributes into categories, create dynamic choice sets, and reuse attributes in multiple store fields by formally defining your attributes in a dynamic namespace. When you're ready to take advantage of these capabilities, see [Working with Dynamic Schema](working-with-dynamic-schema.md).

