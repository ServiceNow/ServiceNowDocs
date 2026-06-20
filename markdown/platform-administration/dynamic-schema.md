---
title: Dynamic Schema
description: Define a hierarchy of categories, groups, and attributes and enable users to select groups of attributes on a record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/dynamic-schema.html
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Dynamic Schema

Define a hierarchy of categories, groups, and attributes and enable users to select groups of attributes on a record.

## Key benefits

-   Organize and define metadata in flexible schema instead of adding new columns to a table.
-   Define a structured framework for grouping dynamic attributes.
-   Capture data dynamically using different attributes per record.

## Dynamic schema workflow

1.  Plan your metadata strategy.
2.  Create groups of attributes.
3.  Add dynamic attributes to each group.
4.  Organize your groups into categories.
5.  Add dynamic attribute store fields to your tables.
6.  Populate dynamic attribute store fields using the GlideRecord setValue\(\) method.

## Use cases

-   Capture groups of attribute-value pairs that describe products sold in a large department store by defining a dynamic schema for your products. Store the attributes and their data in a dynamic attribute store field.

    For example, assume you have a custom Products table that stores records for different types of products like televisions, sunscreens, pillows, and shirts. You can create groups of dynamic attributes for each type of product \(like screen type, UPC, color, or size\). You can organize the groups into dynamic categories \(like electronics, health and beauty, home goods, and clothing\). Users can add records to your Products table and capture different attributes in each product record.

-   Describe a record by capturing one or more dynamic attribute-value pairs as string objects in a dynamic attribute store field. You can also capture transient attribute-value pairs on a record by adding a dynamic attribute store field to a table and populating the field with string data using the GlideRecord API.

## APIs

Dynamic schema also provides global APIs that enable you to access and manage dynamic attributes in your tables using JavaScripts. The following lists the APIs and methods that support dynamic attributes.

-   
-   

    Only the following GlideAggregate methods support the usage of dynamic attributes:

    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
-   
-   
-   

    Only the following GlideRecord methods support dynamic attributes:

    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   
    -   

-   **[Create a dynamic attribute group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/create-dynamic-attribute-group.md)**  
Organize related attributes into a dynamic attribute group.
-   **[Add dynamic attributes to a dynamic group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/add-dynamic-attributes.md)**  
Define the dynamic attributes that describe a record.
-   **[Create a dynamic choice set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/create-choice-set.md)**  
Define a fixed set of values for an attribute.
-   **[Add choices to a dynamic choice set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/add-choices-choice-set.md)**  
Build out a dynamic choice set by defining the choices that belong to it.
-   **[Create a dynamic category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/create-dynamic-category.md)**  
Create a container for organizing dynamic attribute groups.
-   **[Include dynamic attribute groups in a dynamic category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/add-dynamic-attribute-groups-dynamic-category.md)**  
Organize your dynamic attribute groups by relating a dynamic attribute group to a dynamic category.
-   **[Storing dynamic attributes on a record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/storing-dynamic-attributes.md)**  
After you define the categories, groups, and attributes in your dynamic schema, enable users to store the attributes and their values on a record.

**Parent Topic:**[Field administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/c_IntroductionToFields.md)

