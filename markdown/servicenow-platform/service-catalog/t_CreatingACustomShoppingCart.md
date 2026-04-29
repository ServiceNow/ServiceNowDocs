---
title: Create a custom cart
description: Administrators with a knowledge of Jelly can customize the look and feel of service catalog carts, either globally or for specific catalog items, using the UI macro capability.Link the default cart or a custom cart to an item so the requester sees the pertinent information.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create scripts, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a custom cart

Administrators with a knowledge of Jelly can customize the look and feel of service catalog carts, either globally or for specific catalog items, using the UI macro capability.

## Before you begin

Role required: admin

## About this task

**Note:** You can configure cart layouts without scripting.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Macros**.

2.  Click **New** to create a new macro.

3.  Fill in the details and write the script to define your custom cart.

    **Note:** Designing a custom cart requires knowledge of the Jelly expression language. For reference purposes, the default cart script appears in the list as catalog\_cart\_default.

4.  Click **Submit**.


## What to do next

After creating a custom card, you can reuse it and link it to catalog items.

**Parent Topic:**[Create scripts](../reference/r_ServiceCatalogScriptingExtensn.md)

## Link a cart to an item

Link the default cart or a custom cart to an item so the requester sees the pertinent information.

### Before you begin

Role required: catalog\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Items**.

2.  Open an item to test the new cart.

3.  In the **Cart** field, select the cart to use.

    You can configure the form layout to add this field to the form.

4.  Save the changed form.


