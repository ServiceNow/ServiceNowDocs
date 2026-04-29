---
title: Configure the expected OT devices for a site
description: Configure the number of expected OT devices for a site so that you can use the % of Expected OT Devices in CMDB indicator in the OT progress scorecard.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up the Operational Technology Progress Scorecard, Configure, Industrial Workspace, Operational Technology]
---

# Configure the expected OT devices for a site

Configure the number of expected OT devices for a site so that you can use the **% of Expected OT Devices in CMDB** indicator in the OT progress scorecard.

## Before you begin

Role required: ot\_progress\_scorecard\_editor and cmdb\_ot\_isa\_viewer with site access assigned for relevant sites through user criteria

**Note:** For more information about site access through user criteria, see [Review the homepage destination rules for the Industrial Workspace](review-iw-homepage-destination-rules.md).

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Progress Scorecard Attributes**.

2.  If you need to create a record with your site, complete these actions.

    1.  Select **New**.
    2.  In the **Site** field, add your site.
    3.  In the **Value** field, add the number of expected OT devices for that site.

        **Note:** Don't include OT control modules in this value.

    4.  Select **Save**.
3.  If a record with your site exists and you want to modify the expected devices, complete these actions.

    1.  Select the record you want to edit.
    2.  In the **Value** field, modify the number of expected OT devices for that site.

        **Note:** Don't include OT control modules in this value.

    3.  Select **Update**.

**Parent Topic:**[Setting up the Operational Technology Progress Scorecard](../concept/setting-up-the-ot-progress-scorecard.md)

