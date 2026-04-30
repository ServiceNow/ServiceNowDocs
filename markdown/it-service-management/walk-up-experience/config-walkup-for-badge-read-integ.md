---
title: Configure Walk-up Experience for Badge Reader Integration
description: Associate badge reader devices with an on-site Walk-up Experience queue. While you can associate more than one badge reader device to a walk-up location, individual badge reader devices are mapped to only one walk-up location.
locale: en-US
release: xanadu
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Walk-up Experience Badge Reader Integration setup and configuration, Badge Reader Integration for Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Configure Walk-up Experience for Badge Reader Integration

Associate badge reader devices with an on-site Walk-up Experience queue. While you can associate more than one badge reader device to a walk-up location, individual badge reader devices are mapped to only one walk-up location.

## Before you begin

Role required: sn\_walkup.walkup\_manager

## About this task

-   The Walk-up Experience application requires that a badge reader device is mapped to a walk-up location for feature integration.
-   Walk-up Experience managers can configure badge reader integration to a walk-up location using the Location Queues Badge Readers related list on the Walk-up Location Queue \(wu\_location\_queue\) table.
-   At least one badge reader must be activated and available to integrate with the walk-up location. Refer to [Request activation approval for a badge reader device](request-badge-reader-device-approval.md) if no badge readers are activated for use.
-   You can define a check-in reason for each badge reader. When the requester checks in a location using that badge reader, the associated check-in reason is auto populated for the check-in. If no check-in reason is associated with the badge reader, then the location reason is considered for the check-in.

## Procedure

1.  Navigate to **All** &gt; **Walk-up Experience** &gt; **Administration** &gt; **Walk-up Locations**.

2.  Click the name of the walk-up location queue that you want to associate with a badge reader device.

3.  Click the **Location Queues Badge Readers** related link.

4.  Click **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Badge Reader|Badge reader that you want to associate with the location.|
    |Location Queue|Location to which the badge reader is associated.|
    |Check-in reason|Check-in reason that you want to link with the badge reader.|
    |Check-in reason description|Description of the check-in reason that you want to link with the badge reader.|

6.  Select **Submit**.


## Result

You can integrate multiple badge readers with walk-up location.

**Parent Topic:**[Walk-up Experience Badge Reader Integration setup and configuration](../concept/walkup-badge-read-integ-config.md)

