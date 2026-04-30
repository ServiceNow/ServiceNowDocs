---
title: Change the navigation and menu settings in your portal experience
description: Change the header, footer, and menu settings for your custom portal experience in UI Builder to fit the needs of your organization.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure UI Builder portal experiences, Configure how users interact with your applications in UI Builder, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Change the navigation and menu settings in your portal experience

Change the header, footer, and menu settings for your custom portal experience in UI Builder to fit the needs of your organization.

## Before you begin

This task has the following prerequisites:

-   You have an existing portal experience on UI Builder. For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).
-   This workspace experience contains at least two pages.
-   You want users to be able to navigate from a page to other pages that you specify.

Role required: ui\_builder\_admin

## About this task

Set up the navigation and menu settings in the [app shell](../concept/ui-builder-glossary.md#) of your portal experience. The app shell is the wrapper of the portal contents. For example, the app shell can show things like the logo of your company, user preferences, the search icon, the configuration icon, and the user menu. You can configure this app shell in the ServiceNow AI Platform. For more information about app shells, see [Define UI experiences using app shells](../concept/app-shells-uibuilder.md).

You must be in the correct application scope to edit experience settings. If you are in a different scope, the experience settings are read-only. To change your application scope, in the main header, select the application picker \(![Application picker](../image/application-picker.png)\), and then select the application scope. For more information about the application scope, see [Learn about security and roles](security-roles.md).

**Note:** For advanced information about UX page properties, including JSON examples, see [https://www.servicenow.com/community/next-experience-articles/workspace-app-shell-ux-page-properties/ta-p/2331956](https://www.servicenow.com/community/next-experience-articles/workspace-app-shell-ux-page-properties/ta-p/2331956).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open a portal experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).

3.  Select **Settings** in the UI Builder header.

    ![Arrow pointing to the settings toggle on the experience view page.](../image/portal-settings-toggle.png)

4.  To change the settings for the header, footer, and navigation menu for the app shell of the portal experience you’re working in, select the advanced settings links.

    ![Portal experience settings for navigation.](../image/experience-portal-navigation.png "Portal experience settings for navigation")

<table id="table_yhn_b1f_h4b"><thead><tr><th>

Action

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Change the header

</td><td>

To go to the ServiceNow AI Platform®, click **Advanced header settings**.

 Here, you can change what information shows in the header of your portal experience. You can change things like a company logo, user preferences, the search icon, the configuration icon, and so on.

</td></tr><tr><td>

Show the menu

</td><td>

1.  To add a menu to your portal experience, select **Navigation Menu**.
2.  To remove the navigation menu, deselect **Navigation Menu**.
3.  To go to the ServiceNow AI Platform, select **Advanced navigation menu settings**. Here, you can change what menu and menu items are displayed in the navigation menu. For more information, see [Define UI experiences using app shells](../concept/app-shells-uibuilder.md).


</td></tr><tr><td>

Display a footer

</td><td>

1.  To add a primary footer to your portal experience, select **Primary footer**. The footer can show a footer logo, content, and other important links for your portal.
2.  To go to the ServiceNow AI Platform, click **Advanced navigation menu settings**.
3.  To add a second footer to your portal experience, select **Secondary footer**. A secondary footer includes additional text links, social media elements, and copyright information.


</td></tr></tbody>
</table>5.  Click **Save**.


**Parent Topic:**[Configure UI Builder portal experiences](../concept/ui-builder-portal-settings.md)

