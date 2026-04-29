---
title: Revert normalization of firmware models
description: Revert the normalization of firmware models in the OT Asset Workspace.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Normalizing firmware for OT assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Revert normalization of firmware models

Revert the normalization of firmware models in the OT Asset Workspace.

## Before you begin

**Important:** The OT Asset Management application must be activated to access the OT Asset Workspace. For details, see [Install OT Asset Management](install-otam.md).

Role required: sn\_otam.ot\_asset\_manager

## About this task

Normalization of firmware models with a Normalization status of **Normalized**, **Partially normalized**, **Publisher normalized**, or **Manually normalized** can be reverted.

## Procedure

1.  Navigate to **Workspaces** &gt; **OT Asset Workspace** &gt; **OT model management**.

2.  Select the **Firmware discovered** tab.

3.  Select the normalized discovered firmware model for which you want to revert normalization.

4.  Select **Revert Normalization**.


## Result

After the revert normalization process is complete, the following changes take place:

-   All the normalized fields present in the firmware model are reverted and the normalization status changes to **Match not found**.
-   The normalization rule associated with the firmware model gets deactivated. The deactivated rule can no longer normalize any more firmware models. The deactivated rule can't be reactivated. It’s a one-time procedure.
-   After deactivation of the normalization rule, revert normalization is run on all models that were normalized using that rule earlier.
-   The **Revert Normalization** option on the model record is replaced with the **Normalize** option.

