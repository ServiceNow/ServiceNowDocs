---
title: Revert normalization of hardware and consumable models
description: Revert the normalization of hardware and consumable models in the Hardware Asset Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/revert-norm-ham.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure Hardware Model Normalization, Integrations and advanced configuration, Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Revert normalization of hardware and consumable models

Revert the normalization of hardware and consumable models in the Hardware Asset Workspace.

## Before you begin

Role required: Users with assetor model\_admin role \(without Domain separation\), assetor model\_admin plus domain\_admin \(with Domain separation\).

**Note:** The model\_admin role is available only if the OT Asset Management application is activated on your ServiceNow instance. This role lets you revert the normalization status of OT hardware models. The model\_admin role includes the mode\_manager sub-role. For more details on OT assets, see [OT Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/ot-asset-ws-otam.md).

## About this task

You can revert normalization of hardware and consumable models with the status **Normalized**, **Partially Normalized**, or **Manufacturer Normalized**. You can't revert a Manually Normalized model.

## Procedure

1.  Navigate to a normalized hardware or consumable record.

<table id="choicetable_dsq_fhg_ywb"><thead><tr><th align="left" id="d304402e122">

Interface

</th><th align="left" id="d304402e125">

Action

</th></tr></thead><tbody><tr><td id="d304402e133">

**Hardware Asset Workspace**

</td><td>

-   For hardware models, navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Model management** &gt; **Hardware models**.
-   For consumable models, navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Model management** &gt; **Consumable models**.


</td></tr><tr><td id="d304402e188">

**Core UI**

</td><td>

-   For hardware models, navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Hardware models**.
-   For consumable models, navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Consumable models**.


</td></tr></tbody>
</table>2.  Select a hardware or consumable model record that is already normalized.

3.  Select **Revert Normalization** and select one of these options in the confirmation message:

    Revert deactivates the content rule and removes the normalization of the model. The system can’t use a deactivated content rule for normalization again.

4.  Select **Proceed** to revert the normalization, or select **Cancel** to dismiss it.


## Result

-   The system clears the normalized fields \(manufacturer, product, device type, and model\) and changes the normalization status to Match Not Found.
-   If the model was Normalized, the system recalculates its display name and deactivates its lifecycle records from the Content Service.
-   If the model was Normalized or Partially Normalized, the system deactivates the content rule that normalized it. The system also reverts all other models that the rule normalized to Match Not Found, except Manually Normalized models.
-   The system doesn’t use a deactivated rule to normalize any model, and you can’t reactivate the rule from the UI.
-   If the model is eligible for normalization, the system replaces the **Revert Normalization** option with the **Normalize** option.
-   The system doesn’t normalize the model again immediately. The next run of the HAM - Hardware Normalization job processes it. You can select **Normalize** if the option is available. A different active rule can normalize the model.

**Parent Topic:**[Configure Hardware Model Normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/Work-with-hardware-normalization.md)

