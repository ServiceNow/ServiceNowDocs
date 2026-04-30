---
title: Configure a mobile web screen
description: Use a mobile web screen to open a URL from within a ServiceNow mobile application. You can configure relative URLs to open pages within the ServiceNow platform.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Mobile web screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a mobile web screen

Use a mobile web screen to open a URL from within a ServiceNow mobile application. You can configure relative URLs to open pages within the ServiceNow platform.

## Before you begin

Role required: admin

## About this task

Starting with the Zurich release, end-users whose mobile web screen session expires due to session timeouts, device locking, or app backgrounding are automatically logged back into their session when they return to the web screen in their mobile app.

This feature works by default for all service portal pages but requires configuration for UXF pages. To enable this feature on UXF pages, admins must add the mobile app bridge as a data source to the page in UI Builder. For more information on how to do this, please refer to Steps 1-4 in [Add a button to your mobile web screen that launches Virtual Agent](mobwebscreen-add-button-virtagent.md).

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

Fetch type settings determine when data is loaded in screens. Change your fetch type to optimize load time performance for your screens.Select either `Prefetch`, `On-demand`, `Background`, or `Dynamic prefetch` as required according to your setup. For more information about these options, see [Mobile fetch types](../reference/applet-fetch-types.md).

</td></tr><tr><td>

URL

</td><td>

The URL you want to send the user to.

 **Note:** To add the URL for a Now Experience Framework page, which leverages the Mobile App Bridge for playbooks, see [Configure mobile web screens with Mobile App Bridge](configure-mobile-playbooks.md).

</td></tr><tr><td>

Hide screen name

</td><td>

Determines if the screen name isn’t shown as the screen header. This configuration is useful if, for example, the text already appears in the header name or if it doesn’t provide any value to the user.

</td></tr><tr><td>

Check Access Control List \(ACL\)

</td><td>

Enable this toggle to check available ACLs for access to the **URL**.

</td></tr><tr><td>

Role access

</td><td>

Determine which user roles can access this screen. If you have selected no roles, users with any role can access the screen.

</td></tr></tbody>
</table>    **Important:** The field **Open in external browser** doesn't operate as expected. Links to web content that are associated with the instance that the user is currently logged into on the mobile app open as hybrid web pages within the app. All other web content opens in the end-user's default mobile browser outside the app.

6.  If you want to turn off the native header of the mobile screen so that it doesn't interfere with the mobile web screen header, do the following configuration:

    1.  In Mobile App Builder, select **Save** to save the mobile web screen.
    2.  At the top of the Mobile Web Screen form, select the more options menu \(![More options menu](../image/button-more-ios.png)\), and then select **Open in platform**.

        The Mobile web screen configuration page opens in the web UI of your instance.

    3.  In the Mobile web screen configuration page, select the **Hide native header** check box.
    4.  Select **Update**.

        ![Hide native header results on device](../image/mobwebscrn-hide-screen-nam.png)


## What to do next

If you want to further customize your mobile web screen, see [Add a button to your mobile web screen that launches Virtual Agent](mobwebscreen-add-button-virtagent.md).

**Parent Topic:**[Mobile web screen](../concept/url-screen.md)

