---
title: Using the Next Experience Unified Navigation
description: Improved navigation to access records and data, check your notifications, and set your preferences in the Next Experience Unified Navigation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [unified navigation, navigation]
breadcrumb: [Working in Next Experience, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Using the Next Experience Unified Navigation

Improved navigation to access records and data, check your notifications, and set your preferences in the Next Experience Unified Navigation.

The Next Experience Unified Navigation runs across the top of every page and includes controls that help you in navigating your instance. Easily access your workspaces and classic environment, search your instance, and receive notifications.

Select the pin icon ![](../image/pol-nav-pin.png) to pin a menu to the page.

**Note:** The Unified Navigation items described in the following table might not be available to all users. The items that appear are determined by user access and admin customizations.

![Unified navigation header](../../../administer/navigation-and-ui/image/next-exp-unified-navigation.png "Unified Navigation")

<table id="table_fcj_p1f_jqb"><thead><tr><th>

Header items

</th><th>

UI depiction

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Logo

</td><td>

![Logo.](../image/pol-servicenow-landing-page.png)

</td><td>

Returns you to the Next Experience landing page. You can replace this logo with your company logo.

</td></tr><tr><td>

Filter

</td><td>

![Filter.](../image/polaris-filter-ui.png)

</td><td>

Filter field to quickly navigate to the module you want. The search functionality accommodates missing letters in your queries. The default accuracy score can be updated by your administrator. For more information, see [Next Experience system properties](../../../administer/navigation-and-ui/reference/pol-sys-properties.md).

 For a list view, enter the table name in the format `name.list`, for example, sys\_properties.list.

 For a form view, enter the table name in the format `name.do`, for example, sys\_user.do.

 By default, filtering in any of the menus returns results from all menus, except the History menu.

</td></tr><tr><td>

All menu

</td><td>

![All menu.](../image/pol-nav-all-p.png)

</td><td>

Lists all the menu items and modules in the instance.

 Select the refresh icon ![](../image/polaris-refresh-icon.png) to obtain the latest menu items without the need to manually clear the cache.

</td></tr><tr><td>

Favorites menu

</td><td>

![Favorites.](../image/pol-nav-p.png)

</td><td>

Items you have marked as favorites, for example, favorite workspaces, classic environment, and records.

 Select the edit icon ![](../image/polaris-edit-icon.png) to open the edit modal.

 For more information on adding and editing favorites, see [Managing your favorites in Next Experience](managing-your-favorites.md#).

</td></tr><tr><td>

History menu

</td><td>

![History.](../image/pol-nav-history-p.png)

</td><td>

History of your activities across the instance.

</td></tr><tr><td>

Workspaces menu

</td><td>

![Workspace.](../image/pol-nav-workspaces-p.png)

</td><td>

Lists the workspaces you can access. The menu appears only when workspace access is available. If you have one workspace, its name appears in the header.

</td></tr><tr><td>

Admin menu

</td><td>

![Admin menu.](../image/admin-menu.png)

</td><td>

Provides access to items specific to admin functions.

</td></tr><tr><td>

Contextual app pill

</td><td>

![Contextual app pill.](../image/pol-nav-2.png)

</td><td>

Provides the context for where you are in the instance. Select the star icon to favorite the displayed page.

</td></tr><tr><td>

Global search field

</td><td>

![Global search.](../image/pol-nav-global-search.png)

</td><td>

Search for a string across your instance.

</td></tr><tr><td>

Globe

</td><td>

![Globe](../image/globe-menu.png)

</td><td>

Select the scope of your instance and the scope of your update sets. You can also select the **Update set** option and select the Plus sign icon ![](../image/plus.png) to create an update set. Any application scope other than Global displays a red circle icon ![](../../../administer/navigation-and-ui/image/icon-scope-changed.png).

</td></tr><tr><td>

Now Assist

</td><td>

![Now Assist.](../image/icon-now-assist.png)

</td><td>

Enables you to address and resolve customer issues. The [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md) helps you generate summaries for records, chats, cases, or incidents, get help, and create resolution notes. Use the menu width button to toggle between standard and wide widths. Standard and wide widths are static values and the setting that you choose is retained.The Now Assist panel is configured using the Now Assist Admin console.

</td></tr><tr><td>

Show instance tools

</td><td>

![Show instance tools](../image/pol-show-instance-tools.png)

</td><td>

Displays the application scope and current update set in a horizontal row beneath the other tool icons. To enable this feature, you must first create a system property called **glide.ui.next\_experience.instance\_tools\_disabled** and set it to **false**. When this feature is enabled, the Globe icon is hidden.

</td></tr><tr><td>

Sidebar discussions

</td><td>

![Sidebar discussions.](../image/icon-sidebar-discussions.png)

</td><td>

Engage in real-time collaboration with others based around a Workspace task-based or interaction-based record. Sidebar discussions facilitate the exchange of information and knowledge to help resolve issues faster and with higher-quality outcomes.

</td></tr><tr><td>

Usage analytics

</td><td>

![Usage analytics.](../image/next-exp-usage-analytics.png)

</td><td>

Access usage analytic data directly from your applications and web pages.

</td></tr><tr><td>

Help

</td><td>

![Help.](../image/pol-nav-help.png)

</td><td>

The Help menu includes **Get help** and **What's new**. A blue dot indicates new updates. Use **Provide Feedback** to share feedback about the current page with ServiceNow®.

</td></tr><tr><td>

OpenFrame phone

</td><td>

![OpenFrame phone.](../image/icon-openframe-phone.png)

</td><td>

OpenFrame lets you make and receive embedded, contextual calls. When calls are active, the phone icon displays a badge. For more information, see [OpenFrame overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_OpenFrameOverview.md).

</td></tr><tr><td>

Notifications menu

</td><td>

![Notifications menu.](../image/pol-nav-notifications.png)

</td><td>

View and personalize notifications that apply to you in one place. Notifications appear across your instance, including Workspace, based on your access and admin settings.

</td></tr><tr><td>

User menu

</td><td>

![User menu.](../image/pol-user-menu.png)

</td><td>

Menu items to personalize your instance. -   **Profile**: Your instance profile, which includes your personal information displayed in the instance.
-   **Preferences**: Display, accessibility, notifications, and Workspace preferences.
-   **Keyboard shortcuts**: Display a modal with keyboard shortcuts that are specific to the screen you’re viewing. For more information on the keyboard shortcut modal, see [Next Experience keyboard shortcuts](../../../use/navigation/reference/next-experience-keyboard-shortcuts.md). The keyboard shortcuts modal can also be accessed using **Command+/** \(Mac\) or **Control+/** \(Windows\).
-   **Impersonate user**: Administrators can impersonate other authenticated users for testing purposes and view impersonation logs. For more information, see [Impersonating users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/c_ImpersonateAUser.md).
-   **Elevate role**: Designate any role as an elevated privilege role, and then assign that role to one or more users. Do this when you want to restrict users from having access to the rights that the role provides immediately after login.
-   **Printer friendly version**: A printer-friendly version of the current content frame.

**Note:** The Printer-friendly version option is available in the classic environment but not in Workspace.


</td></tr></tbody>
</table>