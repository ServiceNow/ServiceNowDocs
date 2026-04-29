---
title: Normalize the firmware embedded into your Operational Technology \(OT\) assets manually
description: Standardize the publisher, product, and version details of the firmware that is embedded into your OT assets by normalizing the discovered firmware models manually.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Normalizing firmware for OT assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Normalize the firmware embedded into your Operational Technology \(OT\) assets manually

Standardize the publisher, product, and version details of the firmware that is embedded into your OT assets by normalizing the discovered firmware models manually.

## Before you begin

**Important:** The OT Asset Management application must be activated to access the OT Asset Workspace. For details, see [Install OT Asset Management](install-otam.md).

The firmware product and the firmware version details of the discovered firmware model that you want to normalize should be available in the Enterprise Asset Management Content Service. If not, you can also create the firmware product and the firmware version for your firmware model. For more details, see [Create a custom firmware product for your operational technology \(OT\) assets](create-custom-firmware-product-ot-assets.md) and [Create a custom firmware version for your operational technology \(OT\) assets](create-custom-firmware-version-ot-assets.md).

Role required: sn\_otam.ot\_asset\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **OT Asset Workspace** &gt; **OT model management**.

2.  Select the **Firmware discovered** tab.

3.  Select the discovered firmware model that you want to normalize.

4.  On the form, fill in the details in the Normalization section.

    |Field|Description|
    |-----|-----------|
    |Normalized publisher|Name of the firmware manufacturer.|
    |Normalized product|Name of the firmware product.|
    |Normalized version|Version of the discovered firmware.|
    |Exclude from content service|Option that excludes the firmware model details from being shared with the Enterprise Asset Management Content Service.|

5.  Select **Save**.


## Result

The Normalization status changes to Manually Normalized.

