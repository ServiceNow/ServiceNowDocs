---
title: Revert normalization of hardware and consumable models
description: Revert the normalization of hardware and consumable models in the Hardware Asset Workspace.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Work with hardware normalization, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Revert normalization of hardware and consumable models

Revert the normalization of hardware and consumable models in the Hardware Asset Workspace.

## Before you begin

Role required: ham\_admin, asset

## About this task

Hardware and consumable models with a status of **Fully Normalized**, **Partially Normalized**, or **Manufacturer Normalized** can be reverted.

## Procedure

1.  Navigate to a normalized hardware or consumable record.

<table id="choicetable_dsq_fhg_ywb"><thead><tr><th align="left" id="d184164e65">

Interface

</th><th align="left" id="d184164e68">

Action

</th></tr></thead><tbody><tr><td id="d184164e74">

**Core UI**

</td><td>

-   For hardware models, navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Hardware models**.
-   For consumable models, navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Consumable models**.


</td></tr><tr><td id="d184164e122">

**Hardware Asset Workspace**

</td><td>

-   For hardware models, navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Model management** &gt; **Hardware models**.
-   For consumable models, navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Model management** &gt; **Consumable models**.


</td></tr></tbody>
</table>2.  Open a hardware or consumable model record that is already normalized.

3.  Click **Revert Normalization**.

4.  Click **OK** on the confirmation message box.


## Result

After the revert normalization process is complete, the following changes take place:

-   All the normalized fields present in the model are reverted and the normalization status changes to **Match not Found**.
-   Fields are reset to their original values and any rule associated with the model is deactivated.
-   After deactivation of the rule, revert normalization is run on all models that were normalized using that rule before.
-   The deactivated rule can no longer normalize any more models. The deactivated rule can't be reactivated. It’s a one time procedure.
-   The **Revert Normalization** option on the model record is replaced with the **Normalize** option.

**Parent Topic:**[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

