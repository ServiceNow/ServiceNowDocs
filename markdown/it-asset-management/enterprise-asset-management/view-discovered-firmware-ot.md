---
title: View firmware models discovered on your Operational Technology \(OT\) assets
description: Get the details of all the firmware models that the discovery tool discovered on your Operational Technology \(OT\) assets.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Normalizing firmware for OT assets, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# View firmware models discovered on your Operational Technology \(OT\) assets

Get the details of all the firmware models that the discovery tool discovered on your Operational Technology \(OT\) assets.

## Before you begin

**Important:** The OT Asset Management application must be activated to access the OT Asset Workspace. For details, see [Install OT Asset Management](install-otam.md).

Role required: sn\_otam.ot\_asset\_manager

## About this task

The Discovered firmware model \[sn\_ent\_discov\_firmware\_model\] table stores the details of the firmware models discovered on your OT assets.

## Procedure

1.  Navigate to **Workspaces** &gt; **OT Asset Workspace** &gt; **OT model management**.

2.  Select the **Firmware discovered** tab.

    The list of all the installed firmware models that are discovered is shown with the following details:

    -   **Discovered manufacturer**: Name of the firmware manufacturer.
    -   **Discovered model**: Firmware model that's discovered on the OT asset.
    -   **Discovered model number**: Model number of the discovered firmware model.
    -   **Discovered version**: Version number of the discovered firmware model.
    -   **Normalization status**: Status of discovered firmware model normalization. This field can have one of the following values:
        -   **New**: The discovered firmware model has not yet run-through the normalization process.
        -   **Match not found**: The normalization process couldn’t match any of the fields of the discovered firmware model. This status could also occur when a normalization rule doesn’t exist for the firmware model.
        -   **Manually normalized**: Firmware model is normalized manually.
        -   **Normalized**: The discovered firmware model is normalized by the background job, and a firmware model is created in the Firmware model \[sn\_ent\_firmware\_model\] table. A firmware model is normalized only when the publisher, product, model, model number, and version are available.
        -   **Partially normalized**: The normalization process could at least match the product value.
        -   **Publisher normalized**: The normalization process could only match the publisher value.
    -   **Normalized firmware model**: Firmware model that's created after the discovered firmware model is normalized.

        **Important:** A firmware model is created only when the discovered firmware model is either normalized or manually normalized by specifying the product and version details.

    -   **Updated**: Date and time when the discovered firmware model was last updated.
3.  Select a record to view the details.

    The form displays the information related to the discovered firmware model in the Details and the Normalization sections.


