---
title: Create a custom firmware product for your operational technology \(OT\) assets
description: If the firmware product that is embedded into your OT assets isn't already represented in the Enterprise Asset Management Content Service, create a custom firmware product.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Normalizing firmware for OT assets, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a custom firmware product for your operational technology \(OT\) assets

If the firmware product that is embedded into your OT assets isn't already represented in the Enterprise Asset Management Content Service, create a custom firmware product.

## Before you begin

**Important:** You can create custom firmware products only using the OT Asset Workspace. To use the OT Asset Workspace, install the OT Asset Management application on your ServiceNow instance. See [Install OT Asset Management](install-otam.md) for detailed instructions.

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **All** &gt; **OT Asset Workspace** &gt; **Normalization**.

2.  Select the **Custom firmware products** tab.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Manufacturer|Manufacturer of the firmware product.|
    |Product|Name of the firmware product.|
    |UNSPSC classification|Eight-digit numeric code that identifies the firmware product.|
    |Description|Description of the firmware product.|
    |Active|Option that indicates if the firmware product is active.|
    |Exclude from content service|Option that excludes the firmware product from being shared with the Enterprise Asset Management Content Service.|

5.  Select **Save**.


## Result

The custom firmware product is created. If any existing firmware publisher uses the same manufacturer as the custom firmware product, the Enterprise Asset Management application automatically associates that firmware publisher with the custom firmware product. Otherwise, the Enterprise Asset Management application creates a custom firmware publisher to associate with the custom firmware product.

