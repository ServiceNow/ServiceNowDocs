---
title: Revert normalization
description: You can revert the normalization of enterprise models in the Enterprise Asset Workspace.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Enterprise Asset Management by enterprise administrators, Configuring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Revert normalization

You can revert the normalization of enterprise models in the Enterprise Asset Workspace.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

Enterprise models with a status of **Fully Normalized**, **Partially Normalized**, **Manufacturer Normalized**, or **Manually Normalized** can be reverted. All the normalized fields present in the model are reverted and the normalization status changes to **Match not Found**.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Enterprise model management**.

2.  Open a enterprise model record that is already normalized.

3.  Select **Revert Normalization**.

4.  Select **OK** on the confirmation message box.

    Once the revert normalization process is complete, the following changes take place:

    -   fields are reset to their original values and any rule associated with the enterprise model is deactivated.
    -   After deactivation of the rule, revert normalization is run on all models that were normalized using that rule before.
    -   The deactivated rule can no longer normalize any more models. The deactivated rule can't be reactivated. It is a one time procedure.
    -   The **Revert Normalization** option on the model record is replaced with the **Normalize** option.

**Parent Topic:**[Configuring Enterprise Asset Management by enterprise administrators](../concept/config-eam-enterrpriseadmins.md)

