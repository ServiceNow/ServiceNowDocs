---
title: Dynamic Schema
description: Define a hierarchy of categories, groups, and attributes and enable users to select groups of attributes on a record.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Administering fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
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

-   [DynamicSchemaAPI - Global](https://www.servicenow.com/docs/access?context=DynamicSchemaAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)
-   [GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

    Only the following GlideAggregate methods support the usage of dynamic attributes:

    -   [GlideAggregate - addAggregate\(String agg, String name\)](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideAggregate-addAggregate_String_String&ft:locale=en-US)
    -   [GlideAggregate - addHaving\(String aggName, String fieldName, String operator, String value\)](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=yokohama&pubname=yokohama-api-reference&section=GlideAgg-addHaving_S_S_S_S&ft:locale=en-US)
    -   [GlideAggregate - getValue\(String name\)](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideAggregate-getValue_String&ft:locale=en-US)
    -   [GlideAggregate - groupBy\(String name\)](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideAggregate-groupBy_String&ft:locale=en-US)
    -   [GlideAggregate - orderBy\(String name\)](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideAggregate-orderBy_String&ft:locale=en-US)
    -   [GlideAggregate - orderByAggregate\(String agg, String fieldName\)](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideAggregate-orderByAggregate_String_String&ft:locale=en-US)
-   [GlideDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttStoreAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)
-   [GlideElementDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideElementDynamicAttStoreAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)
-   [GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

    Only the following GlideRecord methods support dynamic attributes:

    -   [GlideRecord - addQuery\(String name, Object operator, Object value\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideRecord-AddQuery_String_Object_Object&ft:locale=en-US)
    -   [GlideRecord - getDisplayValue\(String name\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideRecord-getDisplayValue&ft:locale=en-US)
    -   [GlideRecord - getDynamicAttribute\(String fullPath\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-getDynamicAttribute_S&ft:locale=en-US)
    -   [GlideRecord - getDynamicAttribute\(String dynamicAttributeField, String groupAttrPath\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-getDynamicAttribute_S_S&ft:locale=en-US)
    -   [GlideRecord - getDynamicAttributeDisplayValue\(String fullPath\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-getDynAttributeDisplayValue_S&ft:locale=en-US)
    -   [GlideRecord - getDynamicAttributeDisplayValue\(String dynamicAttributeField, String groupAttrPath\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-getDynAttributeDisplayValue_S_S&ft:locale=en-US)
    -   [GlideRecord - getDynamicAttributeValue\(String fullPath\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-getDynamicAttributeValue_S&ft:locale=en-US)
    -   [GlideRecord - getDynamicAttributeValue\(String dynamicAttributeField, String groupAttrPath\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-getDynamicAttributeValue_S_S&ft:locale=en-US)
    -   [GlideRecord - getValue\(String fieldName\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideRecord-getValue_String&ft:locale=en-US)
    -   [GlideRecord - orderBy\(String fieldName\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideRecord-orderBy_String&ft:locale=en-US)
    -   [GlideRecord - orderByDesc\(String fieldName\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideRecord-orderByDesc_String&ft:locale=en-US)
    -   [GlideRecord - setDisplayValue\(String name, Object value\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideRecord-setDisplayValue_String_Object&ft:locale=en-US)
    -   [GlideRecord - setDynamicAttributeDisplayValue\(String fullPath, Object value\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-setDynAttributeDisplayValue_S_O&ft:locale=en-US)
    -   [GlideRecord - setDynamicAttributeDisplayValue\(String dynamicAttributeField, String groupAttrPath, Object value\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-setDynAttributeDisplayValue_S_S_O&ft:locale=en-US)
    -   [GlideRecord - setDynamicAttributeValue\(String fullPath, Object value\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-setDynamicAttributeValue_S_O&ft:locale=en-US)
    -   [GlideRecord - setDynamicAttributeValue\(String dynamicAttributeField, String groupAttrPath, Object value\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-setDynamicAttributeValue_S_S_O&ft:locale=en-US)
    -   [GlideRecord - setDynamicAttributeValues\(String dynamicAttributeField, GlideDynamicAttributeStore values\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=GR-setDynAttributeValues_S_O&ft:locale=en-US)
    -   [GlideRecord - setValue\(String name, Object value\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&section=r_GlideRecord-setValue_String_Object&ft:locale=en-US)

