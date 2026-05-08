---
title: Dynamic Schema
description: Define a hierarchy of categories and enable users to describe a record using one or more attributes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Dynamic Schema

Define a hierarchy of categories and enable users to describe a record using one or more attributes.

## Key benefits

-   Organize and define metadata in a flexible schema instead of adding new columns to a table.
-   Capture data dynamically using different attributes per record.
-   Define a structured framework of dynamic categories and dynamic attributes.
-   Define dynamic categories and dynamic attributes once and reuse them across multiple tables using dynamic namespaces.

## Dynamic Schema elements

Dynamic Schema is composed of the following elements.

-   **Dynamic attributes**

    Name-value pairs that describe a record. You can either formally define dynamic attributes or create them on the fly as transient attributes in a dynamic attribute store field.

-   **Dynamic categories**

    Containers for organizing dynamic attributes. A dynamic category can inherit dynamic attributes from its parent category.

-   **Dynamic attribute store**

    A field type for storing one or more dynamic attributes and their values. When you create a dynamic store field, a dynamic namespace is automatically created and associated with that store field.

    After creating a store field, you can start storing values for attributes without defining them, or you can specify attribute definitions in the dynamic namespace to take advantage of additional functionality.

-   **Dynamic namespace**

    A scoped collection of dynamic attributes and dynamic categories. Each dynamic attribute store field automatically receives its own dynamic namespace or you can configure multiple dynamic attribute store fields that share a dynamic namespace.


## Implementation options

You have flexibility when deciding how to implement Dynamic Schema.

-   You can add attributes directly to a dynamic attribute store field without creating formal definitions first. These attributes are considered transient and are treated as having string values in scripts and queries. You can provide a definition for the attribute and modify its type at any time. Modifying the type of an attribute doesn't affect the stored data but changes how the system interacts with that data. See [Working with attributes transiently](transient-attributes.md).
-   You can take advantage of additional platform support and reuse for attributes by defining them in a dynamic namespace. Defining a dynamic attribute record enables you to specify its type, set choice options, organize it into dynamic categories and more. See [Working with Dynamic Schema](working-with-dynamic-schema.md).
-   You can create a dynamic namespace independently. You can add dynamic attributes and dynamic categories to that namespace, and then associate that namespace with one or more dynamic attribute store fields. This enables you to reuse attributes across multiple store fields. See [Create a dynamic namespace](../task/create-dynamic-namespace.md).

## Use cases

-   Capture attribute-value pairs that describe products sold in a large department store by defining a dynamic schema for your products. Store the attributes and their data in a dynamic attribute store field.

    For example, assume you have a custom Products table that stores records for different types of products like televisions, sunscreens, pillows, and shirts. You can create dynamic attributes for each type of product \(like screen type, UPC, color, or size\). You can organize the dynamic attributes into dynamic categories \(like Electronics, Health and Beauty, Home Goods, and Clothing\). Users can add records to your Products table and capture different attributes in each product record.

-   Describe a record by capturing one or more transient attributes, with values stored as string objects in a dynamic attribute store field. You can also capture transient attributes on a record by adding a dynamic attribute store field to a table and populating the field with string data using the GlideRecord API.
-   Filter Workspace lists using dynamic schema elements in the condition builder. For example, you can define dynamic categories and attributes for product offerings and use them to search for transactions using the condition builder in the Sales Order Management Workspace.

## APIs

Dynamic Schema also provides global APIs that enable you to access and manage dynamic attributes in your tables using JavaScripts. The following lists the APIs and methods that support dynamic attributes.

-   GlideAggregate - Global

    The following GlideAggregate methods support the usage of dynamic attributes:

    -   addAggregate\(\)
    -   addHaving\(\)
    -   getDynamicAttributeValue\(\)
    -   getDynamicAttributeDisplayValue\(\)
    -   getValue\(\)
    -   groupBy\(\)
    -   orderBy\(\)
    -   orderByAggregate\(\)
-   GlideDynamicAttributeStore - Global
-   GlideElementDynamicAttributeStore - Global
-   GlideDynamicNamespace - Global
-   GlideRecord - Global

    The following GlideRecord methods support dynamic attributes:

    -   addQuery\(\)
    -   getDisplayValue\(\)
    -   getDynamicAttribute\(\)
    -   getDynamicAttributeDisplayValue\(\)
    -   getDynamicAttributeValue\(\)
    -   getValue\(\)
    -   orderBy\(\)
    -   orderByDesc\(\)
    -   setDisplayValue\(\)
    -   setDynamicAttributeDisplayValue\(\)
    -   setDynamicAttributeValue\(\)
    -   setDynamicAttributeValues\(\)
    -   setValue\(\)

