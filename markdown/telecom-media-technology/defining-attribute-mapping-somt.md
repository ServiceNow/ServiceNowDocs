---
title: Defining mappings for attribute value propagation to domain orders
description: By defining attribute-mapping rules between two specifications in the product catalog, your fulfillment agents can access all relevant characteristic values in your product, service, and resource orders.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-06"
reading_time_minutes: 2
breadcrumb: [Configuring product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Defining mappings for attribute value propagation to domain orders

By defining attribute-mapping rules between two specifications in the product catalog, your fulfillment agents can access all relevant characteristic values in your product, service, and resource orders.

## Attribute mapping overview

Orders, for example telecommunications orders, contain many characteristics and characteristic values that are populated at different stages of the order life cycle. Order Management automatically propagates and transforms the characteristics and characteristic values throughout the order fulfillment process. This automatic propagation of attributes across the product, service, or resource orders help to improve your operational efficiency and eliminate errors in the fulfillment process.

**Note:** Attribute values are another name for order characteristic values.

## When value attribute values are assigned and how they're used

Orders contain many characteristics and characteristic values that are populated at different stages of the order life cycle. Multi-site enterprise orders contain various attributes that are related to customer, product, service, and resource information. The ServiceNow AI Platform populates these attributes with the corresponding values at the different stages of the order life cycle.

The ServiceNow AI Platform decomposes orders and order line items into various suborders \(product, service, and resource orders\) and assigns them to different user groups and users. Different user groups then work with the various suborders to complete the required fulfillment tasks for a given order.

## Catalog-driven attribute mapping and value propagation

The order fulfillment flow needs prior information on how specification characteristics are mapped and associated so that the characteristics are propagated from one domain order to another domain order. If you're a product catalog manager, you can define rules-driven attribute mappings between and among selected product, service, and resource specifications. When you define attribute mappings, validations run to verify that they're unique, don't conflict with each other, or conflict with defined specification relationships and decomposition rules.

To learn more about specification relationships, see [Create specification relationships, quantity mapping, and decomposition rules for Sales CRM for Telecommunications](../task/create-specification-relationships-somt.md).

The Order Management application executes attribute mappings during the order fulfillment process and sets and propagates order characteristic values across the various suborders.

The order fulfillment process evaluates the attribute-mapping rules that you define. The attribute values are propagated from the domain orders that are associated with the source specification to the domain orders that are associated with the target specification.

With catalog driven rule-based attribute propagation, your fulfillment agents have all the relevant and correct information that they require to work effectively on order tasks. The attribute-mapping functionality reduces errors and improves efficiency in the order fulfillment process as follows:

-   Without rules-driven attribute mapping, your users have to assign the attribute values manually, which can be error-prone and time-consuming.
-   These values propagate to lower domain orders and are used for inventory creation, service activation, and account and billing updates. Fixing an error takes a significant amount of effort and time for your users when these values are manually assigned.
-   Attribute mappings promote the proper flow of crucial data through the associated domain orders. This mapping makes consistent data available to users with different roles when they're processing an order.

