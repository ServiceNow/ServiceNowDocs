---
title: Normalize hardware and consumable models
description: After you've created your hardware and consumable models, normalize the information of the model.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Work with hardware normalization, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Normalize hardware and consumable models

After you've created your hardware and consumable models, normalize the information of the model.

## Before you begin

Role required: admin or asset

## About this task

**Note:**

-   If you've opted in to the Hardware Asset Management Content Service, you can override any life cycle values that were added from the schedule job, or you can manually add your own life cycles.
-   For a model to be fully normalized, you must add manufacturer details and a model number, and optionally a model name.
-   If you update the **Device Type** field, the normalization status is updated.

## Procedure

1.  Navigate to one of the following paths.

    -   **Product Catalog** &gt; **Product Models** &gt; **Hardware Models**
    -   **Product Catalog** &gt; **Product Models** &gt; **Consumable Models**
2.  To create a model, select **New**.

3.  On the Hardware Model or Consumable Model form, [fill in the details](create-hardware-consumable-model.md).

4.  Select **Save**.

    If the information is available, the model is compared against the data in the Hardware Normalization Content Service, and the model is normalized.

    **Note:** If the hardware or consumable model is normalized against the Hardware Asset Management Content Service, a life cycle is added if applicable life cycles exist in the content service.

5.  Based on the details you added, complete the following steps.

    1.  If the normalization status of your model is Partially Normalized or Publisher Normalized, select the **Normalized** section and **Consumable Model Fields** section to normalize the model manually.

    2.  If the normalization status of your model is Fully Normalized, but you don't like the information that was added, select **Revert Normalization**.

        All normalization fields are cleared and you can manually normalize your model.

        **Note:** This option is only available if the model is Fully Normalized, Partially Normalized, or Manufacturer Normalized. **Revert Normalization** is visible only to users with the ham\_admin role in a non-domain separated instance and is visible to users with the role ham\_admin + domain\_admin in a domain-separated instance. For more information, see [Revert normalization of hardware and consumable models](revert-norm-ham.md).

6.  Select **Save**.

    The **Normalization Status** field is updated.


## Normalize a hardware model

You've created a hardware model for the Lenovo ThinkPad T43 and you want your asset information to be consistent across the organization.

Review the normalization status of the model by selecting the **Normalization** section.

![Normalization related list with details added.](../image/partially-normalized-example.png "Normalization status")

The normalization status is set to Partially Normalized because the name of the model is missing.

In the **Model** field, enter `2687DTU`.

Select **Save**.

The **Normalization Status** field displays **Manually Normalized**.

![The Normalization Status field is updated to Manually Normalized.](../image/manually-normalized-example.png "Manually Normalized status")

**Parent Topic:**[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

