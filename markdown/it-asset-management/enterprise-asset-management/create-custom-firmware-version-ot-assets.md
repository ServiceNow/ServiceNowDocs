---
title: Create a custom firmware version for your operational technology \(OT\) assets
description: If the version of the firmware that is embedded into your OT assets isn't already represented in the Enterprise Asset Management Content Service, create a custom firmware version.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Normalizing firmware for your operational technology \(OT\) assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a custom firmware version for your operational technology \(OT\) assets

If the version of the firmware that is embedded into your OT assets isn't already represented in the Enterprise Asset Management Content Service, create a custom firmware version.

## Before you begin

**Important:** You can create custom firmware versions only using the OT Asset Workspace. To use the OT Asset Workspace, install the OT Asset Management application on your ServiceNow instance. See [Install OT Asset Management](install-otam.md) for detailed instructions.

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **All** &gt; **OT Asset Workspace** &gt; **Normalization**.

2.  Select the **Custom firmware versions** tab.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Version|Firmware version.|
    |Product|Firmware product that the firmware version applies to.|
    |Next version available|Option that indicates if the next firmware version is currently available.|
    |Active|Option that indicates if the firmware version is active.|
    |Exclude from content service|Option that excludes the firmware version from being shared with the Enterprise Asset Management Content Service.|

5.  Select **Save**.


