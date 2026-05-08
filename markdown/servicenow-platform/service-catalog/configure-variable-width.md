---
title: Configure a default width for Service Catalog variables
description: Configure the default width for variables on a catalog item page to specify what percentage of the screen size that it can span.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a default width for Service Catalog variables

Configure the default width for variables on a catalog item page to specify what percentage of the screen size that it can span.

## Before you begin

Role required: admin

## About this task

A default width size cannot be set or does not apply to the following variables:

-   The break, container end, container split, container start, and label variables.
-   Any variable placed in a container with two-column layout.
-   A variable set with a two-column layout.
-   Any variable that is created with a custom width set in the **Variable width** field on the Variable form. For details, see [Create a service catalog variable](t_CreateAVariableForACatalogItem.md). The custom width for the variable overrides the default width set for the variable type.

**Note:** Custom variable widths are not supported in either Now® Mobile or Service Portal.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Variables** &gt; **Variable Default Size**.

2.  For each variable type, select a default width.

<table><tbody><tr><td id="d554342e142">

**25%**

</td><td>

Configures the variable to span 25% of the available screen size.

</td></tr><tr><td id="d554342e151">

**50%**

</td><td>

Configures the variable to span 50% of the available screen size. By default, some variables require a minimum of 50% width.

</td></tr><tr><td id="d554342e160">

**75%**

</td><td>

Configures the variable to span 75% of the available screen size.

</td></tr><tr><td id="d554342e169">

**100%**

</td><td>

Configures the variable to span 100% of the available screen size.

</td></tr></tbody>
</table>3.  Select **Save**.


**Parent Topic:**[Types of catalog items](../reference/r_ExtendedCatalogItemFunctions.md)

