---
title: Normalize hardware and consumable models
description: After you have created your hardware and consumable models, normalize the information of the model.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Work with hardware normalization, Use, Hardware Asset Management, IT Asset Management]
---

# Normalize hardware and consumable models

After you have created your hardware and consumable models, normalize the information of the model.

## Before you begin

Role required: admin, asset, or model\_manager

## About this task

**Note:**

-   If you have opted in to the Hardware Asset Management Content Service, you can override any life cycle values that were added from the schedule job, or you can manually add your own life cycles.
-   For a model to be fully normalized, you must add manufacturer details and a model number, and optionally a model name.
-   If you update the **Device Type** field, the normalization status is updated.

## Procedure

1.  Create a hardware or consumable model.

<table id="choicetable_k4b_k1j_pdc"><thead><tr><th align="left" id="d205060e74">

Interface

</th><th align="left" id="d205060e77">

Action

</th></tr></thead><tbody><tr><td id="d205060e83">

**Core UI**

</td><td>

1.  Navigate to one of the following paths.
    -   **Product Catalog** &gt; **Product Models** &gt; **Hardware Models**.
    -   **Product Catalog** &gt; **Product Models** &gt; **Consumable Models**.
2.  Select **New**.
3.  On the Hardware Model or Consumable Model form [fill in the details](create-hardware-consumable-model.md).
4.  Select **Save**.


</td></tr><tr><td id="d205060e150">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Model management**.
2.  Select the type of model that you want to create.
    -   For hardware models, select the **Hardware models** tab.
    -   For consumable models, select the **Consumable models** tab.
3.  Select **New**.
4.  On the Hardware model or Consumable model form, [fill in the details](create-hardware-consumable-model.md).
5.  Select **Save**.


</td></tr></tbody>
</table>    If the information is available, the model is compared against the data in the Hardware Normalization Content Service, and the model is normalized.

    **Note:** If the hardware or consumable model is normalized against the Hardware Asset Management Content Service, a life cycle is added if applicable life cycles exist in the content service.

2.  Normalize your model manually if the normalization status of your model is Partially Normalized or Publisher Normalized.

<table id="choicetable_yqq_h2j_pdc"><thead><tr><th align="left" id="d205060e230">

Interface

</th><th align="left" id="d205060e233">

Action

</th></tr></thead><tbody><tr><td id="d205060e239">

**Core UI**

</td><td>

Select the **Normalized** section and **Consumable Model Fields** section to normalize the model manually.

</td></tr><tr><td id="d205060e254">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Model management**.
2.  Select the type of model that you want to normalize.
    -   For hardware models, select the **Hardware models** tab.
    -   For consumable models, select the **Consumable models** tab.
3.  Select the model.
4.  Select **Normalize**.


</td></tr></tbody>
</table>3.  Select **Save**.

    The **Normalization Status** field is updated.


## Normalize a hardware model

You have created a hardware model for the Lenovo ThinkPad T43 and you want your asset information to be consistent across the organization.

Review the normalization status of the model by reviewing the **Normalization** section.

The normalization status is set to Partially Normalized because the name of the model is missing.

In the **Model** field, enter `2687DTU`.

Select **Save**.

The **Normalization Status** field displays **Manually Normalized**.

**Parent Topic:**[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

