---
title: Create entitlements for Citrix
description: Software entitlements enable you to define license details that are matched to software models. You can add an entitlement individually or import a list from a spreadsheet.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Software Asset Management publisher pack for Citrix, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create entitlements for Citrix

Software entitlements enable you to define license details that are matched to software models. You can add an entitlement individually or import a list from a spreadsheet.

## Before you begin

Role required: sam\_user or sam\_admin. The sam\_admin role is required to import entitlements.

**Important:** You can create and import entitlements in both the Software Asset Management classic application and the Software Asset Workspace. The following steps provide details on how to create entitlements in the Software Asset Management classic application. For details on how to create entitlements in the Software Asset Workspace, see [Create entitlements in workspace](create-entitlements-workspace.md). For details on how to import entitlements in the Software Asset Workspace, see [Import bulk entitlements in workspace](import-entitlements-workspace.md).

Before you can create a software entitlement, [create a software model](add-software-model-sap.md).

## About this task

Manage available software and tie software installations \(software being used\) with entitlements \(software owned\) using software models. Create software models for all software to be monitored.

**Note:** Users with the model\_manager role can navigate to **Product Catalog** &gt; **Product Model** &gt; **Software Models** but can’t administer all aspects of software models.

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **Software Entitlement** and select **New**.

    For a detailed description of the fields related to all entitlements, see [Create entitlements in Software Asset Management classic](track-software-rights.md).

    |Field|Description|
    |-----|-----------|
    |License Metric|License metric for the license group that the software license is counted against when reconciliation is run. For detailed of the license metrics, see [Software license metrics](../concept/c_SAMLicenseMetrics.md).|

2.  To set upgrade or downgrade entitlements, select the new software entitlement record from the Software Entitlements list.

    For a detailed description on how to complete additional configurations for software entitlements, see [Create entitlements in Software Asset Management classic](track-software-rights.md).

3.  Select **Submit**.

    Your entitlement is added to the software entitlements list.


## What to do next

[Run software reconciliation](t_RunReconciliation.md) on your licenses.

**Parent Topic:**[Software Asset Management publisher pack for Citrix](../concept/citrix-publisher-pack.md)

