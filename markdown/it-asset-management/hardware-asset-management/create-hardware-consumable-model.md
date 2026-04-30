---
title: Create a hardware or consumable model
description: To begin tracking your hardware and consumable assets, create a hardware or consumable model. Then, add lifecycle information to keep track of the lifecycle phase of your model.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Work with hardware normalization, Use, Hardware Asset Management, IT Asset Management]
---

# Create a hardware or consumable model

To begin tracking your hardware and consumable assets, create a hardware or consumable model. Then, add lifecycle information to keep track of the lifecycle phase of your model.

## Before you begin

Role required: admin or asset

## Procedure

1.  Navigate to one of the following paths.

    -   **Product Catalog** &gt; **Product Models** &gt; **Hardware Models**
    -   **Product Catalog** &gt; **Product Models** &gt; **Consumable Models**
2.  Click **New**.

3.  Complete the following steps if you are adding a hardware model.

    1.  On the Hardware Model form, click the **Consumable Model Fields** section.

    2.  Click **Save**.

    3.  To add additional information on the asset, click the [Hardware model details](../reference/hardware-model-fields.md).

    4.  To add unit information, click the [Hardware model details](../reference/hardware-model-fields.md).

    5.  To link a compatible model, click the [Compatibles](../reference/hardware-model-fields.md#section_ijc_l3c_2jb) and then click **Add Compatible**.

    6.  To add a model substitution, click the [Substitutes](../reference/hardware-model-fields.md#section_ldn_k2x_dkb) and then click **Add Substitution**.

    7.  To manually normalize your hardware model, click the [Normalization section](normalize-hardware-consumable-models.md).

    8.  To add a configuration item, click the [Configuration Items](../reference/hardware-model-fields.md#section_kct_j5r_cjb).

    9.  To add your model to the Product Catalog, click the [Hardware model details](../reference/hardware-model-fields.md).

    10. To publish the model to the Hardware Catalog, click the **Publish to Hardware Catalog** related link.

    11. To add related assets, click the [Hardware model details](../reference/hardware-model-fields.md).

    12. To add a model component, click the [Model Components](../reference/hardware-model-fields.md#section_rzd_53c_2jb).

    13. To add vendor information to your model, click the [Vendor Catalog Items](../reference/hardware-model-fields.md#section_wb4_53c_2jb) and click **New**.

    14. To add lifecycle information, click the [Hardware Model Lifecycles](../reference/hardware-model-fields.md#section_n1d_v3c_2jb), click **New**.

        If a lifecycle with the same source, lifecycle type, lifecycle phase, and source exits, an error message appears.

        **Note:** While you can delete lifecycles that you've added, you can't delete lifecycles that are created from the Hardware Asset Management Content Service.

4.  Complete the following steps if you are adding a consumable model.

    1.  On the Consumable Model form, the [fill in the details](../reference/consumable-model-fields.md).

    2.  Click **Save**.

    3.  To add additional information on the consumable asset, click the [Hardware model details](../reference/hardware-model-fields.md).

    4.  To add your model to the Product Catalog, click the [Hardware model details](../reference/hardware-model-fields.md).

    5.  To add vendor information to your model, click the [Vendor Items related list](../reference/consumable-model-fields.md#section_jjq_pzx_cjb).

    6.  To add lifecycle information, click the [Consumable Model Lifecycle related list](../reference/consumable-model-fields.md#section_zvj_qzx_cjb) and click **New**.

        If a lifecycle with the same source, lifecycle type, lifecycle phase, and source exits, an error message appears.

        **Note:** While you can delete lifecycles that you've added, you can't delete lifecycles that are created from the Hardware Asset Management Content Service

5.  Click **Submit**.


## Result

The model appears in either the Hardware Model or Consumable Model list.

**Note:** If you want to exclude this model from the Hardware Asset Management Content Service, select the **Exclude from content service** option.

## Create a hardware model

You've purchased the ThinkPad T43 and you need to begin tracking the asset.

To begin tracking your asset, add the following information to the Hardware form.

|Field|Description|
|-----|-----------|
|Manufacturer|Lenovo|
|Name|ThinkPad T43|

Click **Save**.

The **Display name** field is updated with the name of the manufacturer and the name of the hardware.

![The Display name field is updated with what you entered in the Manufacturer and Name fields.](../image/hardware-model-manu-name.png "Hardware form")

Currently, the Lenovo ThinkPad T43 is generally available. Add the lifecycle status to accurately track the phase of the asset.

Click the Hardware Lifecycle Model related list and click **New**. Add the following information to the Hardware Model Lifecycle form.

|Field|Description|
|-----|-----------|
|Lifecycle type|General Availability|
|Phase start date|2019-10-08|
|Phase end date|2019-10-31|

Click **Submit**.

The lifecycle is added to the record.

![The General Availability lifecycle phase is added to the record.](../image/hardware-model-ga-lifecycle.png "Hardware Model Lifecycles")

When the general availability phase is over, the ThinkPad T43 will be discontinued. Add the end of life information to the asset to accurately track the lifecycle.

Click the Hardware Lifecycle Model related list and click **New**. Add the following information to the Hardware Model Lifecycle form.

|Field|Description|
|-----|-----------|
|Lifecycle type|End of Life|
|Phase start date|2019-11-01|
|Phase end date|2019-11-30|

Click **Submit**.

The End of Life lifecycle is added to the record and both lifecycle phases are displayed in the Hardware Model Lifecycle related list.

![The End of Life lifecycle phase is added to the record.](../image/hardware-model-end-life-lifecycle.png "Lifecycle phases in the Hardware Model Lifecycles list")

## What to do next

After you've added your hardware or consumable models, you can [normalize the data](normalize-hardware-consumable-models.md).

**Parent Topic:**[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

