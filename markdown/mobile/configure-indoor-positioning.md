---
title: Configure indoor positioning
description: Indoor positioning enables end users to see their live location on an Indoor Wayfinding map and get guided navigation to their desired destination.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Indoor Wayfinding configuration, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure indoor positioning

Indoor positioning enables end users to see their live location on an Indoor Wayfinding map and get guided navigation to their desired destination.

## Before you begin

Before you can configure indoor positioning, you must have completed the following configurations:

-   Configure Indoor Wayfinding. For more information, see [Indoor Wayfinding configuration](../concept/indoor-wayfinding-config.md).
-   Set up at least one custom map provider in the Custom Map Provider \[sys\_sg\_custom\_map\_provider\] table. For more information, see [Configure a custom map provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-service-delivery-for-mobile/configure-custom-map-provider.md)

Role required: admin

## About this task

Consider the following requirements that are related to this task.

-   If all buildings use the same location provider, only one custom map provider record is needed.
-   If different location providers are needed for each building, create a custom map provider record for each building and select the building as the key. Then assign location providers to your mobile devices.

For information about the features this configuration enables for end users, see [Indoor positioning](../concept/indoor-positioning-end-user.md).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you’re working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** in the menu.

4.  Select **Record type** and enter `sys_sg_custom_map_provider` in the search well.

5.  Select the custom map provider record you configured for indoor positioning.

6.  Depending on whether you’re configuring indoor positioning for iOS devices or Android devices, select one of the following:

    -   Under **iOS location provider**, select either **Atlas** or **Apple**.
    -   Under **Android location provider**, you can only select **Atlas**.
7.  If you select **Atlas** as your location provider, you must add the following information:

    -   Location provider app id
    -   Location provider app secret
8.  Select **Save**.


**Parent Topic:**[Indoor Wayfinding configuration](../concept/indoor-wayfinding-config.md)

