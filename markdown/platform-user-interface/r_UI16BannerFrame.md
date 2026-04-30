---
title: System settings for the Core UI
description: You can define system settings to customize the Core UI for yourself. The gear icon, located within the banner frame, displays the system settings window.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Core UI, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# System settings for the Core UI

You can define system settings to customize the Core UI for yourself. The gear icon, located within the banner frame, displays the system settings window.

The system settings are organized by tab.

**Note:** This information is applicable to the Core UI. For information about adjusting system settings with Next Experience enabled, see [Next Experience preferences](../../../get-started/servicenow-overview/concept/set-up-preferences-next-experience.md).

<table id="table_kj4_twh_fr"><thead><tr><th>

Control

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General tab

</td></tr><tr><td>

Accessibility enabled

</td><td>

More advanced accessibility features are activated when this setting is enabled. The platform is designed to be accessible by default. Enabling this feature makes more accessibility features available.

</td></tr><tr><td>

Accessible tooltips on forms

</td><td>

Displays a help icon next to each field that has a tooltip. This user preference can be enabled only if Accessibility is also enabled.

</td></tr><tr><td>

Data visualization patterns enabled

</td><td>

Adds pattern as well as colors to any color-based graphs or diagrams.

</td></tr><tr><td>

Compact the user interface

</td><td id="entry_CompactUI">

The UI is optimized to display more information in the browser window when this setting is enabled.

</td></tr><tr><td>

Compact list date/time

</td><td id="entry_DateTime">

Date and time values appear in a compact format when this setting is enabled. The year isn’t shown for date values within the current year, and seconds are not shown for time values. This setting isn’t available if the **Date/Time** selection is **Time Ago**.

</td></tr><tr><td>

Keyboard shortcuts enabled

</td><td>

Determines whether a user can access parts of the platform using keyboard shortcuts. For more information on available keyboard shortcuts, see [Core UI keyboard shortcuts](../../../use/navigation/reference/r_KeyboardShortcuts.md).

</td></tr><tr><td>

Home

</td><td>

Determines whether the Home module opens **Homepages** or **Dashboards**. **Important:**

The functionality found in homepages, arranging information from your instance to tell a story about your data, is found in dashboards on new instances. On upgraded instances with Next Experience enabled, users can view existing homepages if they have a direct URL, but they can't create or edit them. Responsive dashboards and Analytics Center dashboards take over homepage functionality.

Use the [Homepage deprecation help tool](https://www.servicenow.com/docs/access?context=homepage-deprecation-help-tool&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US) to convert the homepages on your instance to responsive dashboards.

For more information, see:

-   [Dashboards in the Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).
-   [Working with responsive dashboards](https://www.servicenow.com/docs/access?context=c_ResponsiveDashboards&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Date/Time

</td><td id="entry_DateTimeFormat">

The format in which dates and times appear depends on this setting. Select **Calendar** \(for example, 2015-11-13, 15:58:58\), **Time Ago** \(for example, 11 minutes ago\), or **Both**.

</td></tr><tr><td>

Language

</td><td>

Select a language or return to the default language \(![Return to default language](../image/IconUI16Reset.png)\). This setting is available if a language plugin has been activated. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Time zone

</td><td>

Select a time zone or return to the default time zone \(![Return to default time zone](../image/IconUI16Reset.png)\) for the current session. Upon the next login, the time zone setting reverts to the system default, or user profile setting for time zone.

</td></tr><tr><td>

Domain

</td><td>

Specifies the currently selected domain for organizations that are using domain separation. The user must have the domain\_admin or admin role to see this setting.

</td></tr><tr><td>

Show domain picker in header

</td><td>

Places a domain picker in the banner frame, next to the user menu, when this setting is enabled.

</td></tr><tr><td>

Printer friendly version \(![Printer friendly version icon](../image/IconUI15Print.png)\)

</td><td>

Opens a printer friendly version of the current content frame.

</td></tr><tr><td class="sub-head" colspan="2">

Theme tab

</td></tr><tr><td>

Theme

</td><td>

Select a theme for the user interface. Select the **System** theme to return to the default theme.

</td></tr><tr><td class="sub-head" colspan="2">

Lists tab

</td></tr><tr><td>

Wrap longer text in list columns

</td><td id="entry_WrapText">

Long strings wrap in list columns instead of appearing as one long line when this setting is enabled.

</td></tr><tr><td class="sub-head" colspan="2">

Forms tab

</td></tr><tr><td>

Tabbed forms

</td><td id="entry_TabbedForms">

Form sections and related lists appear in tabs when this setting is enabled.

</td></tr><tr><td>

Related list loading

</td><td>

Determines when related lists load on forms. For more information, see [Configure when a related list loads](../../../use/using-forms/task/t_ConfigureWhenARelatedListLoads.md).

</td></tr><tr><td class="sub-head" colspan="2">

Notifications tab

</td></tr><tr><td>

Search

</td><td>

Search bar for finding notifications.To find a notification:

-   Enter the name of the notification you are searching for. When you type the first three characters, the system automatically returns a list of notifications matching the characters entered.
-   Enter two asterisks to return a list of all notifications in alphabetic order \(the notifications are not organized by category\).

</td></tr><tr><td>

Allow notifications

</td><td>

Global switch for enabling or disabling all notifications.

</td></tr><tr><td>

Notification channels

</td><td>

List of your channels for receiving notifications. Use this section to:-   Enable or disable a channel by using its toggle switch. If you disable a channel, notifications are not delivered through that channel.
-   [Add channels](https://www.servicenow.com/docs/access?context=create-channel&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) using the **Create Channel** option.
-   [Modify channel information](https://www.servicenow.com/docs/access?context=modify-notif-channel&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). Click the channel row or the right arrow \(**&gt;**\) next to the appropriate channel to edit or delete it.

</td></tr><tr><td>

Notifications by category

</td><td>

List of notification categories that identify and group related notifications. Each category contains the notifications that you can subscribe to. To view the notifications in a given category, click the category row or the right arrow \(**&gt;**\) next to the appropriate category. You can:

 -   Edit settings for a notification:
    -   Enable or disable channels for the selected notification.
    -   [Apply notification conditions](https://www.servicenow.com/docs/access?context=apply-notification-conditions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US), such as schedules and filters, that affect the delivery of the notification.
-   [Create personal notifications](https://www.servicenow.com/docs/access?context=create-personal-notifications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US), which are subscriptions to specific notifications that matter to you.

</td></tr><tr><td class="sub-head" colspan="2">

Developer tab

</td></tr><tr><td>

Application

</td><td>

\(Administrators only\) Provides a link to the application picker, the Applications list \(![Link to the Applications list](../image/IconUI16ApplicationsList.png)\), and the currently selected application \(![Link to the currently selected application](../image/IconUI16Information.png)\).

</td></tr><tr><td>

Show application picker in header

</td><td>

Places an application picker in the banner frame, next to the user menu, when this setting is enabled.

</td></tr><tr><td>

Update Set

</td><td>

\(Administrators only\) Provides a link to the update sets list, the update set picker, and the currently selected update set.

</td></tr><tr><td>

Show update set picker in header

</td><td>

Places the update set picker in the banner frame, next to the user menu, when this setting is enabled.

</td></tr><tr><td>

JavaScript Log and Field Watcher

</td><td>

\(Administrators only\) Opens the client-side [JavaScript debug window](https://www.servicenow.com/docs/access?context=c_JavaScriptDebugWindow&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

</td></tr><tr><td>

Automated Test Framework Page Inspector

</td><td>

Places the inspect icon in the banner frame when this setting is enabled. Enables page developers and test designers to identify page components on customized user interfaces available for custom UI testing in the Automated Test Framework.

</td></tr></tbody>
</table>![System Settings window](../image/UI16SystemMenu.png "System Settings window, General tab")

**Parent Topic:**[Core UI](../concept/c_UI16.md)

