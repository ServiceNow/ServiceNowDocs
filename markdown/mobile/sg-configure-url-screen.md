---
title: Configure a mobile web screen
description: Use a mobile web screen to open a URL from within a ServiceNow mobile application. You can configure relative URLs to open pages within the ServiceNow platform.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile web screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a mobile web screen

Use a mobile web screen to open a URL from within a ServiceNow mobile application. You can configure relative URLs to open pages within the ServiceNow platform.

## Before you begin

Role required: admin

**Note:**

There are limitations associated with the use of mobile web screens on navigation tabs. Currently, if the mobile web screen is accessed and authentication has expired because the session has timed out, the device has locked, or the app has been backgrounded, you must re-authenticate in the mobile web screen.

In addition, pulling to refresh the mobile web screen is unavailable on Android devices. Instead, to refresh the app, you must close it, re-start it, and then return to the mobile web screen to see refreshed content. This limitation related to pulling to refresh doesn't exist on iOS devices, version 18.4 and later.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category from the menu, and then select **New**.

4.  Select the **Mobile web** option in the Create a screen page and then select **Continue**.

5.  Complete the following fields as needed.

<table id="table_ix4_1fh_gfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of your screen. This name appears as a tile in the mobile application.

</td></tr><tr><td>

Description

</td><td>

Additional information about the screen.

</td></tr><tr><td>

Icon

</td><td>

Icon used to represent your mobile web screen when added to a launcher screen.

</td></tr><tr><td>

Fetch type

</td><td>

Fetch type settings determine when data is loaded in screens. Change your fetch type to optimize load time performance for your screens.Select either `Prefetch`, `On-demand`, `Background` or `Dynamic prefetch` as required according to your setup. For more information about these options, see [Mobile fetch types](../reference/applet-fetch-types.md).

</td></tr><tr><td>

URL

</td><td>

The URL you want to send the user to.

 **Note:** To add the URL for a Now Experience Framework page, which leverages the Mobile App Bridge for playbooks, see [Configure mobile web screens with Mobile App Bridge](configure-mobile-playbooks.md).

</td></tr><tr><td>

Hide screen name

</td><td>

Determines if the screen name is not shown as the screen header. This is useful if, for example, the text already appears in the header name or if it does not provide any value to the user.

</td></tr><tr><td>

Role access

</td><td>

Determine which user roles can access this screen. If you have selected no roles, users with any role will have access to the screen.

</td></tr></tbody>
</table>    **Important:** The field **Open in external browser** doesn't operate as expected. Instead, the ServiceNow mobile app automatically opens all mobile web screen links that navigate to the same domain as the currently logged-in instance in an internally embedded browser. Otherwise, mobile web screen links that point to web pages that don't reside on the currently logged-in instance automatically open in an external browser. Note that links opened in external browsers on Android apps might still have the appearance of the internally embedded browser window.

6.  Select **Save**.


