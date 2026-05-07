---
title: Map a custom context variable to a transaction entity
description: Associate a custom pricing context variable to a particular transaction entity type in Sales Customer Relationship Management.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Map a custom context variable to a transaction entity

Associate a custom pricing context variable to a particular transaction entity type in Sales Customer Relationship Management.

## Before you begin

Verify that you're in the appropriate application scope for the transaction type. For example, if you're mapping a context variable for orders, the application scope is Order Management. Use the Globe ![](../../../reuse/icons/product-icons/globe-outline-24.svg) icon in the navigation bar to change the application scope.

Role required: admin

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Context Rule Management** &gt; **Variable Mappings**.

3.  Select **New**.

4.  In the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Entity|The Sales Customer Relationship Management entity for which the variable will be used. Select the entity, for example Opportunity or Order.|
    |Table|Name of the application table for the transaction.|
    |Field|Field from the application table that is related to the custom context variable. Select the field.|
    |Key|Custom context variable. Select the variable from the list of pricing context variables.|
    |Advanced| |

5.  Select **Save**.


## Result

The custom context variable is available for use in pricing matrices.

