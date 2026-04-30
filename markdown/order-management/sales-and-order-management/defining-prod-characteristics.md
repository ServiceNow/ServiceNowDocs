---
title: Defining product characteristics and characteristic options
description: As a product catalog admin, you create the characteristics and characteristic options for product offerings and specifications. Product characteristics are attributes that define and describe a product.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create product offerings, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Defining product characteristics and characteristic options

As a product catalog admin, you create the characteristics and characteristic options for product offerings and specifications. Product characteristics are attributes that define and describe a product.

For example, if a product offering is a bike, the characteristics might include bike size and color. The characteristic options are the choices, such as the various bike sizes and colors available. Characteristics and characteristic options for products are displayed in the product configurator when agents configure products for opportunities, quotes, and orders and when customers order products using the Business Portal.

## Characteristic data input types

When you define product characteristics and characteristic options, you provide basic attribute information, including the characteristic name and the data input type for the characteristic options. The data input type indicates how the characteristic options are entered in the product configurator, such as single line text or choice selection.

The following data input types are available for characteristic options:

-   Address - Mail address
-   Attachment - External document to be attached
-   CheckBox - Select or clear an option
-   Choice - Options that can be chosen, presented as radio buttons or available from a drop-down list
-   Decimal - Numbers that require a decimal point to indicate fractional amounts
-   Dates - Date picker for selecting day, month, and year
-   Date/time - Date picker for selecting day, month, year and time of day
-   Duration - Period of time
-   Email - Email address
-   Single Line Text - Free-form text
-   Integers - Whole numbers
-   Yes/No - Yes/no response
-   Object - Structure that represents a hierarchy of attributes, also called complex characteristics. An object has parent attribute with one or more child attributes.
-   Arrays - Multiple instances of the same attribute type, such as arrays of Date, DateTime, Integer, Single Line Text, Object, and Decimal

You can use the Object type to build a hierarchy of complex characteristics, which has a top-level parent attribute with one or more child attributes. The child characteristics can be any of the data input types, including objects with data arrays.

The following example shows a characteristic hierarchy for Routing Addresses, which is a parent-level attribute with an object data type. This attribute has the following child attributes: Procurement Date, Route, Additional Address Required, BGP, Routing Type, and Address Supplier. Notice that the BGP child characteristic is an array of objects with a minimum size of 2 and maximum size of 4.

![Order for configurable product offering that has complex characteristics for the Routing Addresses of the SD WAN Controllerv2 . Shows the input prompts for the BGP characteristic options.](../image/complex-char-nodes-array.png "Example of complex characteristics in product configurator")

## Setting up complex characteristics

Defining a hierarchical attribute structure involves setting up the parent attribute, for example routing addresses, as an object type. You then define the characteristic relationships between the parent attribute and child attributes to establish the hierarchical structure and the order in which the child characteristics display in the product configurator.

For details on defining characteristics, see [Create product characteristics and characteristic options](../task/som-product-config-add-characteristics.md)

.

