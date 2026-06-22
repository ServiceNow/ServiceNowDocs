---
title: Configure offline mode properties for function instances
description: Determine if the function instance available to users in online mode is also available in offline mode. This option gives you more control over how users manage their offline tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/config-offline-property-function-instance.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Supported functions, Align apps, screens, and functions, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure offline mode properties for function instances

Determine if the function instance available to users in online mode is also available in offline mode. This option gives you more control over how users manage their offline tasks.

## Before you begin

Role required: mobile-admin, admin

## About this task

Function instances define the location of the function within the screen. For example: the footer area, top menu, or on a specific field. Define whether a function instance is available in offline mode. By default, all button instances are available offline, but you can disable specific ones if needed.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select one of the following methods to access a function instance.

<table><thead><tr><th align="left" id="d28802e98">

Method

</th><th align="left" id="d28802e101">

Procedure

</th></tr></thead><tbody><tr><td id="d28802e107">

**From an existing screen**

</td><td>

1.  Select the **Screens** category and select the screen that contains your function instances.
2.  In the configuration tree, navigate to an existing function instance.
3.  In the Settings area, select the Disable Offline field if you do not want this function instance to display in offline mode.

**Note:** The default value of the **Disable Offline** field is turned off.

</td></tr><tr><td id="d28802e136">

**From the function instance table**

</td><td>

1.  Select **All mobile records** from the menu.
2.  From the **Record type** field, select Function instance \[sys\_sg\_button\_instance\] and then either select **New** or an existing record.
3.  In the Settings area, select the Disable Offline field if you do not want this function instance to display in offline mode.

**Note:** The default value of the **Disable Offline** field is turned off.

</td></tr></tbody>
</table>4.  Select **Save**.


**Parent Topic:**[Supported functions for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/functions-offline.md)

