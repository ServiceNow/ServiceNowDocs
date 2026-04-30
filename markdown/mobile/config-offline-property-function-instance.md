---
title: Configure offline mode properties for function instances
description: Determine if the function instance available to users in online mode is also available in offline mode. This option gives you more control over how users manage their offline tasks.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Offline mode, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure offline mode properties for function instances

Determine if the function instance available to users in online mode is also available in offline mode. This option gives you more control over how users manage their offline tasks.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select one of the following methods to access a function instance.

<table><thead><tr><th align="left" id="d78784e92">

Method

</th><th align="left" id="d78784e95">

Procedure

</th></tr></thead><tbody><tr><td id="d78784e101">

**From an existing screen**

</td><td>

1.  Select the **Screens** category and select the screen that contains your function instances.
2.  In the configuration tree, navigate to an existing function instance.
3.  In the Settings area, select the Disable Offline field if you do not want this function instance to display in offline mode.

**Note:** The default value of the **Disable Offline** field is turned off.

</td></tr><tr><td id="d78784e134">

**From the function instance table**

</td><td>

1.  Select **All mobile records** from the menu.
2.  From the **Record type** field, select Function instance \[sys\_sg\_button\_instance\] and then either select **New** or an existing record.
3.  In the Settings area, select the Disable Offline field if you do not want this function instance to display in offline mode.

**Note:** The default value of the **Disable Offline** field is turned off.

</td></tr></tbody>
</table>4.  Select **Save**.


**Parent Topic:**[Offline mode](../concept/mobile-offline-mode.md)

