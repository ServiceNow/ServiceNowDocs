---
title: Copy a hardware model from the Content lookup portal
description: Copy a hardware model record from the Content lookup portal to add a new model entry to the Product Model \[cmdb\_model\] table.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Work with hardware normalization, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Copy a hardware model from the Content lookup portal

Copy a hardware model record from the Content lookup portal to add a new model entry to the Product Model \[cmdb\_model\] table.

## Before you begin

Role required: asset and model\_manager

## About this task

You can create a product model record by duplicating an existing model from the Content lookup portal. The duplicated model is normalized and relevant fields are automatically populated from the source record. If a record with the same manufacturer, name, and model number exists in the Product Model \[cmdb\_model\] table, you can’t duplicate the model record.

## Procedure

1.  Navigate to **Hardware Asset Workspace** &gt; **Content lookup**.

2.  Search for a hardware model record.

3.  Open the Model details form by selecting the model number.

4.  Select **Copy model details**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Model type|Type of the model.|
    |Model categories|Model categories that the model can be associated with. Model categories are used to create configuration items \(CIs\) and assets.|

6.  Select **Create new model**.

    A confirmation message is displayed.


## Result

The model record is created and you’re redirected to the Model record form.

## What to do next

-   To publish the model to the Hardware Catalog, select **Publish to Hardware Catalog**. For more information about publishing the model to the hardware catalog, see [Publish an item to the hardware catalog](../../product-catalog/task/t_PublishAnItemToTheHardwareCatalog.md).
-   To revert the normalization of the hardware or consumable model, select **Revert Normalization**. For more information about reverting normalization, see [Revert normalization of hardware and consumable models](revert-norm-ham.md).
-   To save the changes made to the model record, select **Save**.

**Parent Topic:**[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

**Related topics**  


[Create a hardware or consumable model](create-hardware-consumable-model.md)

[Content lookup portal for Hardware Asset Management](../concept/content-lookup-ham.md#)

