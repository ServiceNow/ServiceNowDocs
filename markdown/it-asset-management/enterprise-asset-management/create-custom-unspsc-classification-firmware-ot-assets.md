---
title: Create a custom United Nations Standard Products and Services Code \(UNSPSC\) classification for firmware in your operational technology \(OT\) assets
description: If the UNSPSC classification for any firmware that is embedded into your OT assets isn't already represented in the Enterprise Asset Management Content Service, create a custom UNSPSC classification.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Normalizing firmware for OT assets, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a custom United Nations Standard Products and Services Code \(UNSPSC\) classification for firmware in your operational technology \(OT\) assets

If the UNSPSC classification for any firmware that is embedded into your OT assets isn't already represented in the Enterprise Asset Management Content Service, create a custom UNSPSC classification.

## Before you begin

**Important:** You can create custom UNSPSC classifications only using the OT Asset Workspace. To use the OT Asset Workspace, install the OT Asset Management application on your ServiceNow instance. See [Install OT Asset Management](install-otam.md) for detailed instructions.

Role required: sn\_eam.enterprise\_admin

## About this task

The UNSPSC is a global multi-sector standard for classifying products and services. It encompasses a five-level hierarchical codeset that enables you to classify products and services at grouping levels relevant to your needs. You can use the UNSPSC to classify the firmware that is embedded into your industrial- and hardware-based OT assets.

## Procedure

1.  Navigate to **All** &gt; **OT Asset Workspace** &gt; **Normalization**.

2.  Select the **Custom firmware UNSPSC** tab.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |UNSPSC commodity ID|Eight-digit numeric code that identifies the firmware that is embedded into your OT assets.|
    |UNSPSC title|Title of the UNSPSC classification.|
    |UNSPSC description|Description of the UNSPSC classification.|
    |Active|Option that indicates if the UNSPSC classification is active.|
    |Exclude from content service|Option that excludes the UNSPSC classification from being shared with the Enterprise Asset Management Content Service.|

5.  Select **Save**.


