---
title: Configure a default width for service catalog variables
description: Configure the default width for variables on a catalog item page to specify what percentage of the screen size that it can span.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a default width for service catalog variables

Configure the default width for variables on a catalog item page to specify what percentage of the screen size that it can span.

## Before you begin

Role required: admin

## About this task

The following figure shows how the variables for the different Apple iPhone 5 options are set to different widths.

![screenshot for page for iPhone 5 catalog item with variables of varying widths](../image/VariableDefaultWidth.png "Page for iPhone 5 catalog item with variables of varying widths")

A default width size cannot be set or does not apply to the following variables:

-   The break, container end, container split, container start, and label variables.
-   Any variable placed in a container with two-column layout.
-   A variable set with a two-column layout.
-   Any variable that is created with a custom width set in the **Variable width** field on the Variable form. For details, see [Create a service catalog variable](t_CreateAVariableForACatalogItem.md). The custom width for the variable overrides the default width set for the variable type.

**Note:** Custom variable widths are not supported in either Mobile or Service Portal.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Variables** &gt; **Variable Default Size**.

2.  For each variable type, select a default width.

<table><tbody><tr><td id="d488816e136">

**25%**

</td><td>

Configures the variable to span 25% of the available screen size.

</td></tr><tr><td id="d488816e145">

**50%**

</td><td>

Configures the variable to span 50% of the available screen size. By default, some variables require a minimum of 50% width.

</td></tr><tr><td id="d488816e154">

**75%**

</td><td>

Configures the variable to span 75% of the available screen size.

</td></tr><tr><td id="d488816e163">

**100%**

</td><td>

Configures the variable to span 100% of the available screen size.

</td></tr></tbody>
</table>3.  Click **Save**.


**Parent Topic:**[Types of catalog items](../reference/r_ExtendedCatalogItemFunctions.md)

