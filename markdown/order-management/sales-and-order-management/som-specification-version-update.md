---
title: Updating specification versions
description: Enterprises frequently create and update new versions of product and service specifications. When these changes occur, it's important to update the existing product specification in ServiceNow. Failure to update the product specifications can lead to difficulties with MACD \(Move, Add, Change, Delete\) operation when orders enter fulfillment.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create an order in Order Management, Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Updating specification versions

Enterprises frequently create and update new versions of product and service specifications. When these changes occur, it's important to update the existing product specification in ServiceNow®. Failure to update the product specifications can lead to difficulties with MACD \(Move, Add, Change, Delete\) operation when orders enter fulfillment.

Updating specification versions helps with:

-   Introducing new characteristics along with their options.
-   Adding new options to existing characteristics and removing existing characteristics or their options.
-   Renaming existing characteristics and options.
-   Incorporating new relationships and updating or removing existing relationships.
-   Adding compatibility rules.

## Specification version updates

The following list shows the types of specification version updates that can occur:

-   Characteristics
    -   New
    -   Changed - enumerations
    -   Removed
-   Child Relationships \(bundled/composed\)
    -   New
    -   Removed
    -   Change cardinality
-   Horizontal Relationships/Compatibility Rules
-   Attribute Mapping Rules

## Batch specification version update

A set of specification versions can be updated using the batch specification utility in Sales Customer Relationship Management. The specification can also be scheduled.

**What to do next**

[Configure update specification versions](../task/som-configure-specification-version-update.md)

-   **[Configure update specification versions](../task/som-configure-specification-version-update.md)**  
Configure specification version updates so that product specification versions can be updated to reflect changes and updates.
-   **[Batch update for product specification versions](../task/som-configure-specification-version-update-silent-batch-utility.md)**  
Use the inventory batch update job to update product specifications when changes occur from one version to another.
-   **[View upgrade inventory job status](../task/som-view-upgrade-inventory-job-status.md)**  
View the status of a specification upgrade job using the upgrade inventory Job status list form.

**Parent Topic:**[Create an order in Order Management](../task/som-create-product-order.md)

