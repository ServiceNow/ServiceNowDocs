---
title: Create a hardware or consumable model
description: To begin tracking your hardware and consumable assets, create a hardware or consumable model. Then, add lifecycle information to keep track of the lifecycle phase of your model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/create-hardware-consumable-model.html
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

    3.  To add additional information on the asset, click the [Hardware model details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md).

    4.  To add unit information, click the [Hardware model details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md).

    5.  To link a compatible model, click the [Compatibles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md) and then click **Add Compatible**.

    6.  To add a model substitution, click the [Substitutes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md) and then click **Add Substitution**.

    7.  To manually normalize your hardware model, click the [Normalization section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/normalize-hardware-consumable-models.md).

    8.  To add a configuration item, click the [Configuration Items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md).

    9.  To add your model to the Product Catalog, click the [Hardware model details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md).

    10. To publish the model to the Hardware Catalog, click the **Publish to Hardware Catalog** related link.

    11. To add related assets, click the [Hardware model details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md).

    12. To add a model component, click the [Model Components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md).

    13. To add vendor information to your model, click the [Vendor Catalog Items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md) and click **New**.

    14. To add lifecycle information, click the [Hardware Model Lifecycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md), click **New**.

        If a lifecycle with the same source, lifecycle type, lifecycle phase, and source exits, an error message appears.

        **Note:** While you can delete lifecycles that you've added, you can't delete lifecycles that are created from the Hardware Asset Management Content Service.

4.  Complete the following steps if you are adding a consumable model.

    1.  On the Consumable Model form, the [fill in the details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/consumable-model-fields.md).

    2.  Click **Save**.

    3.  To add additional information on the consumable asset, click the [Hardware model details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md).

    4.  To add your model to the Product Catalog, click the [Hardware model details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-model-fields.md).

    5.  To add vendor information to your model, click the [Vendor Items related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/consumable-model-fields.md).

    6.  To add lifecycle information, click the [Consumable Model Lifecycle related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/consumable-model-fields.md) and click **New**.

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

\[Omitted image "hardware-model-manu-name.png"\] Alt text: The Display name field is updated with what you entered in the Manufacturer and Name fields.

Currently, the Lenovo ThinkPad T43 is generally available. Add the lifecycle status to accurately track the phase of the asset.

Click the Hardware Lifecycle Model related list and click **New**. Add the following information to the Hardware Model Lifecycle form.

|Field|Description|
|-----|-----------|
|Lifecycle type|General Availability|
|Phase start date|2019-10-08|
|Phase end date|2019-10-31|

Click **Submit**.

The lifecycle is added to the record.

\[Omitted image "hardware-model-ga-lifecycle.png"\] Alt text: The General Availability lifecycle phase is added to the record.

When the general availability phase is over, the ThinkPad T43 will be discontinued. Add the end of life information to the asset to accurately track the lifecycle.

Click the Hardware Lifecycle Model related list and click **New**. Add the following information to the Hardware Model Lifecycle form.

|Field|Description|
|-----|-----------|
|Lifecycle type|End of Life|
|Phase start date|2019-11-01|
|Phase end date|2019-11-30|

Click **Submit**.

The End of Life lifecycle is added to the record and both lifecycle phases are displayed in the Hardware Model Lifecycle related list.

\[Omitted image "hardware-model-end-life-lifecycle.png"\] Alt text: The End of Life lifecycle phase is added to the record.

## What to do next

After you've added your hardware or consumable models, you can [normalize the data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/normalize-hardware-consumable-models.md).

**Parent Topic:**[Work with hardware normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/Work-with-hardware-normalization.md)

