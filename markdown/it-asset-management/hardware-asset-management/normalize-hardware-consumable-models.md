---
title: Normalize hardware and consumable models
description: After you have created your hardware and consumable models, normalize the information of the model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/normalize-hardware-consumable-models.html
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

-   Normalization depends on whether the Content Service has a match for the manufacturer, model name, and model number on your model. Enter as much of this information as you have.
-   If you update the Device Type field, the normalization status is updated.
-   If you have opted in to the Hardware Asset Management Content Service, you can override lifecycle values that the scheduled job added, or add your own lifecycles.

## Procedure

1.  Create a hardware or consumable model.

<table id="choicetable_k4b_k1j_pdc"><thead><tr><th align="left" id="d130245e76">

Interface

</th><th align="left" id="d130245e79">

Action

</th></tr></thead><tbody><tr><td id="d130245e87">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Model management**.
2.  Select the type of model that you want to create.
    -   For hardware models, select the **Hardware models** tab.
    -   For consumable models, select the **Consumable models** tab.
3.  Select **New**.
4.  On the Hardware model or Consumable model form, [fill in the details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/create-hardware-consumable-model.md).
5.  Select **Save**.


</td></tr><tr><td id="d130245e160">

**Core UI**

</td><td>

1.  Navigate to one of the following paths.
    -   **Product Catalog** &gt; **Product Models** &gt; **Hardware Models**.
    -   **Product Catalog** &gt; **Product Models** &gt; **Consumable Models**.
2.  Select **New**.
3.  On the Hardware Model or Consumable Model form [fill in the details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/create-hardware-consumable-model.md).
4.  Select **Save**.


</td></tr><tr><td id="d130245e229">

****

</td><td>



</td></tr></tbody>
</table>    If the Content Service has a match, the system normalizes the model. If lifecycles exist for the matched model, the system adds them.

2.  If the status is Partially Normalized, Manufacturer Normalized, or Match Not Found, normalize your model manually.

<table id="choicetable_yqq_h2j_pdc"><thead><tr><th align="left" id="d130245e265">

Interface

</th><th align="left" id="d130245e268">

Action

</th></tr></thead><tbody><tr><td id="d130245e276">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Model management**.
2.  Select the type of model that you want to normalize.
    -   For hardware models, select the **Hardware models** tab.
    -   For consumable models, select the **Consumable models** tab.
3.  Select the model.
4.  Select **Normalize**.


</td></tr><tr><td id="d130245e336">

**Core UI**

</td><td>

Select the **Normalized** section and **Consumable Model Fields** section to normalize the model manually.

</td></tr><tr><td id="d130245e353">

****

</td><td>



</td></tr></tbody>
</table>3.  Select **Save**.

    The **Normalization Status** field is updated.

    For details on the normalization status and the results of normalization, see [Hardware Model Normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/hardware-normalization.md).

    .


**Parent Topic:**[Work with hardware normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/Work-with-hardware-normalization.md)

