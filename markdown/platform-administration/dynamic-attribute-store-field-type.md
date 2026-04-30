---
title: Dynamic attribute store field type
description: The dynamic attribute store field type stores one or more dynamic attributes and their values.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Dynamic attribute store field type

The dynamic attribute store field type stores one or more dynamic attributes and their values.

You can describe a record by capturing one or more dynamic attribute-value pairs as string objects in a dynamic attribute store field. For details on defining a flexible schema and creating a dynamic attribute store field to capture attributes and their values, see [Dynamic Schema](dynamic-schema.md).

You can also simply capture attribute-value pairs on a record by adding a dynamic attribute store field to a table and populating the field with string data using the Glide API. After populating the field with string data, you can query the field just like any string field.

When configuring a dynamic schema, you can create a relationship between a dynamic attribute store field and a dynamic schema reference field. You can make the dynamic attribute store field dependent on the dynamic schema reference field.

