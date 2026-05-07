---
title: Create a data product
description: Create a data product to group one or more data interfaces into a governed, publishable collection that consumers can discover and access through the Data Catalog.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-31"
reading_time_minutes: 1
breadcrumb: [Managing data products, Data Products, Workflow Data Fabric]
---

# Create a data product

Create a data product to group one or more data interfaces into a governed, publishable collection that consumers can discover and access through the Data Catalog.

## Before you begin

Role required: data\_product\_admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Data Workbench**.

2.  Select **Create** &gt; **Create data product**.

    The data product wizard opens to the **Basic details** step.

3.  Complete the basic details for the data product, then select **Continue**.

    -   **Data product name**: Enter a name for the data product.
    -   **Description**: Describe the data product and its intended use.
    -   **Tags**: Optionally add tags separated by commas to make the data product easier to find in the Data Catalog.
    -   **Application scope**: Auto-populated from your current application scope.
4.  Select **Add assets**, select the data interfaces to include, and select **Continue**.

    The data product inherits access permissions from each data interface you add. There is no separate permissions configuration at the data product level.

5.  Review the inherited permissions and select **Continue**.

    The Set permissions step lists each data interface with its role and configuration status. Permissions are read-only at this level. To change access, update the roles on the individual data interfaces.

6.  Review the data product configuration and select **Done**.

    The data product details page opens. The data product is in draft state and is not yet available to consumers.


## Result

The data product is created in draft state and visible in Data Workbench. Publish it to make it available to consumers in the Data Catalog.

## What to do next

To make the data product available to consumers, see [Publish a data product](publish-data-product-wdf.md)

**Parent Topic:**[Managing data products](../concept/manage-data-products-wdf.md)

