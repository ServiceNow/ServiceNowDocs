---
title: Revert normalization of hardware and consumable models
description: Revert the normalization of hardware and consumable models in the Hardware Asset Workspace.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Work with hardware normalization, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Revert normalization of hardware and consumable models

Revert the normalization of hardware and consumable models in the Hardware Asset Workspace.

## Before you begin

Role required: Users with assetor model\_admin role \(without Domain separation\), assetor model\_admin and domain\_admin \(with Domain separation\).

**Note:** The model\_admin role is available only if the OT Asset Management application is activated on your ServiceNow instance. This role enables you to revert the normalization status of OT hardware models. For more details on OT assets, see [OT Asset Workspace](../../enterprise-asset-management/concept/ot-asset-ws-otam.md). The model\_admin role includes the mode\_manager sub-role.

## About this task

Hardware and consumable models with a status of **Fully Normalized**, **Partially Normalized**, **Manufacturer Normalized**, or **Manually Normalized** can be reverted.

## Procedure

1.  Navigate to a normalized hardware or consumable record.

<table id="choicetable_dsq_fhg_ywb"><thead><tr><th align="left" id="d204428e98">

Interface

</th><th align="left" id="d204428e101">

Action

</th></tr></thead><tbody><tr><td id="d204428e107">

**Core UI**

</td><td>

-   For hardware models, navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Hardware models**.
-   For consumable models, navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Consumable models**.


</td></tr><tr><td id="d204428e155">

**Hardware Asset Workspace**

</td><td>

-   For hardware models, navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Model management** &gt; **Hardware models**.
-   For consumable models, navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Model management** &gt; **Consumable models**.


</td></tr></tbody>
</table>2.  Select a hardware or consumable model record that is already normalized.

3.  Select **Revert Normalization** and select one of these options in the confirmation message:

    -   To mark your confirmation and proceed with reverting model normalization, select **Proceed**.
    -   To dismiss the model normalization revert, select **Cancel**.
    **Note:** The revert normalization confirmation feature is available with Hardware Asset Management version 15.0.0 onwards.


## Result

After the revert normalization process is complete, the following changes take place:

-   All the normalized fields present in the model are reverted and the normalization status changes to **Match not Found**.
-   Fields are reset to their original values and any rule associated with the model is deactivated.
-   After deactivation of the rule, revert normalization is run on all models that were normalized using that rule before.
-   The deactivated rule can no longer normalize any more models. The deactivated rule can't be reactivated. It’s a one-time procedure.
-   The **Revert Normalization** option on the model record is replaced with the **Normalize** option.

**Parent Topic:**[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

