---
title: Configure assets
description: An asset is a specific product or instance that is supported for a customer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-configure-assets.html
release: australia
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 1
keywords: [asset, configure, hardware, license, inventory]
breadcrumb: [Initial setup, Configure, Manufacturing Commercial Operations]
---

# Configure assets

An asset is a specific product or instance that is supported for a customer.

## About this task

Assets in MCO represent equipment, software, facilities, and consumables deployed across dealer. Configuring individual assets allows you to maintain detailed records of ownership, location, maintenance history, and deployment status. This is foundational for warranty claims processing, recall management, and dealer operations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Products** &gt; **Assets**.

2.  Select **New**.

3.  Select the type of asset to create:

    -   Hardware
    -   Software License
    -   Consumable
    -   License
    -   Facility
4.  Complete the asset form with the following information:

    |Field|Description|
    |-----|-----------|
    |Name|A descriptive name for the asset \(for example, "Dell Laptop Model 5490" or "Windows 11 Enterprise License"\).|
    |Asset Tag|A unique identifier assigned by your organization for tracking and inventory purposes.|
    |Serial Number|The manufacturer's serial number for the asset.|
    |Location|The physical location or dealer facility where the asset is deployed.|
    |Model|The product model or version.|
    |Warranty Start|The date warranty coverage begins.|
    |Warranty End|The date warranty coverage expires.|
    |Cost|The acquisition or replacement cost of the asset.|

5.  Select **Submit**.

    For more information on importing assets, see [Import assets with guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/import-csm-assets.md).


## Result

The new asset is created and is set to be available in the MCO system. The asset can now be linked to install base items, associated with dealer, tracked through repair claims, and included in recall campaigns. You can view asset details, update maintenance records, and monitor deployment status from the assets list.

## What to do next

Consider these next steps:

-   Link the asset to an install base item to associate it with a customer or dealer.
-   For bulk asset creation, use the asset import feature instead of creating assets individually.

