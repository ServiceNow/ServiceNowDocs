---
title: Using the Next Experience Unified Navigation
description: Improved navigation to access records and data, check your notifications, and set your preferences in the Next Experience Unified Navigation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/using-the-next-experience-global-header.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [unified navigation, navigation]
breadcrumb: [Explore, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Using the Next Experience Unified Navigation

Improved navigation to access records and data, check your notifications, and set your preferences in the Next Experience Unified Navigation.

The Next Experience Unified Navigation runs across the top of every page and includes controls that help you in navigating your instance. Easily access your workspaces and classic environment, search your instance, and receive notifications.

Select the pin icon \[Omitted image "pol-nav-pin.png"\] Alt text: to pin a menu to the page.

**Note:** The Unified Navigation items described in the following table might not be available to all users. The items that appear are determined by user access and admin customizations.

\[Omitted image "next-exp-unified-navigation.png"\] Alt text: Unified navigation header

<table id="table_fcj_p1f_jqb"><thead><tr><th>

Header items

</th><th>

UI depiction

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Logo

</td><td>

\[Omitted image "pol-servicenow-landing-page.png"\] Alt text: Logo.

</td><td>

Returns you to the Next Experience landing page. You can replace this logo with your company logo.

</td></tr><tr><td>

Filter

</td><td>

\[Omitted image "polaris-filter-ui.png"\] Alt text: Filter.

</td><td>

Filter field to quickly navigate to the module you want. The search functionality accommodates missing letters in your queries. The default accuracy score can be updated by your administrator. For more information, see [Next Experience system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/pol-sys-properties.md).

 For a list view, enter the table name in the format `name.list`, for example, sys\_properties.list.

 For a form view, enter the table name in the format `name.do`, for example, sys\_user.do.

 By default, filtering in any of the menus returns results from all menus, except the History menu.

</td></tr><tr><td>

All menu

</td><td>

\[Omitted image "pol-nav-all-p.png"\] Alt text: All menu.

</td><td>

Lists all the menu items and modules in the instance.

 Select the refresh icon \[Omitted image "polaris-refresh-icon.png"\] Alt text: to obtain the latest menu items without the need to manually clear the cache.

</td></tr><tr><td>

Favorites menu

</td><td>

\[Omitted image "pol-nav-p.png"\] Alt text: Favorites.

</td><td>

Items you have marked as favorites, for example, favorite workspaces, classic environment, and records.

 Select the edit icon \[Omitted image "polaris-edit-icon.png"\] Alt text: to open the edit modal.

 For more information on adding and editing favorites, see [Managing your favorites in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/managing-your-favorites.md).

</td></tr><tr><td>

History menu

</td><td>

\[Omitted image "pol-nav-history-p.png"\] Alt text: History.

</td><td>

History of your activities across the instance.

</td></tr><tr><td>

Workspaces menu

</td><td>

\[Omitted image "pol-nav-workspaces-p.png"\] Alt text: Workspace.

</td><td>

Lists the workspaces you can access. The menu appears only when workspace access is available. If you have one workspace, its name appears in the header.

</td></tr><tr><td>

Admin menu

</td><td>

\[Omitted image "admin-menu.png"\] Alt text: Admin menu.

</td><td>

Provides access to items specific to admin functions.

</td></tr><tr><td>

Contextual app pill

</td><td>

\[Omitted image "pol-nav-2.png"\] Alt text: Contextual app pill.

</td><td>

Provides the context for where you are in the instance. Select the star icon to favorite the displayed page.

</td></tr><tr><td>

Global search field

</td><td>

\[Omitted image "pol-nav-global-search.png"\] Alt text: Global search.

</td><td>

Search for a string across your instance.

</td></tr><tr><td>

Globe

</td><td>

\[Omitted image "globe-menu.png"\] Alt text: Globe

</td><td>

Select the scope of your instance and the scope of your update sets. You can also select the **Update set** option and select the Plus sign icon \[Omitted image "plus.png"\] Alt text: to create an update set. Any application scope other than Global displays a red circle icon \[Omitted image "icon-scope-changed.png"\] Alt text:.

</td></tr><tr><td>

Now Assist

</td><td>

\[Omitted image "icon-now-assist.png"\] Alt text: Now Assist.

</td><td>

Enables you to address and resolve customer issues. The [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/now-assist-panel-overview.md) helps you generate summaries for records, chats, cases, or incidents, get help, and create resolution notes. Use the menu width button to toggle between standard and wide widths. Standard and wide widths are static values and the setting that you choose is retained.The Now Assist panel is configured using the Now Assist Admin console.

</td></tr><tr><td>

Show instance tools

</td><td>

\[Omitted image "pol-show-instance-tools.png"\] Alt text: Show instance tools

</td><td>

Displays the application scope and current update set in a horizontal row beneath the other tool icons. To enable this feature, you must first create a system property called **glide.ui.next\_experience.instance\_tools\_disabled** and set it to **false**. When this feature is enabled, the Globe icon is hidden.

</td></tr><tr><td>

Sidebar discussions

</td><td>

\[Omitted image "icon-sidebar-discussions.png"\] Alt text: Sidebar discussions.

</td><td>

Engage in real-time collaboration with others based around a Workspace task-based or interaction-based record. Sidebar discussions facilitate the exchange of information and knowledge to help resolve issues faster and with higher-quality outcomes.

</td></tr><tr><td>

Usage analytics

</td><td>

\[Omitted image "next-exp-usage-analytics.png"\] Alt text: Usage analytics.

</td><td>

Access usage analytic data directly from your applications and web pages.

</td></tr><tr><td>

Help

</td><td>

\[Omitted image "pol-nav-help.png"\] Alt text: Help.

</td><td>

The Help menu includes **Get help** and **What's new**. A blue dot indicates new updates. Use **Provide Feedback** to share feedback about the current page with ServiceNow®.

</td></tr><tr><td>

OpenFrame phone

</td><td>

\[Omitted image "icon-openframe-phone.png"\] Alt text: OpenFrame phone.

</td><td>

OpenFrame lets you make and receive embedded, contextual calls. When calls are active, the phone icon displays a badge. For more information, see [OpenFrame overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_OpenFrameOverview.md).

</td></tr><tr><td>

Notifications menu

</td><td>

\[Omitted image "pol-nav-notifications.png"\] Alt text: Notifications menu.

</td><td>

View and personalize notifications that apply to you in one place. Notifications appear across your instance, including Workspace, based on your access and admin settings.

</td></tr><tr><td>

User menu

</td><td>

\[Omitted image "pol-user-menu.png"\] Alt text: User menu.

</td><td>

Menu items to personalize your instance. -   **Profile**: Your instance profile, which includes your personal information displayed in the instance.
-   **Preferences**: Display, accessibility, notifications, and Workspace preferences.
-   **Keyboard shortcuts**: Display a modal with keyboard shortcuts that are specific to the screen you’re viewing. For more information on the keyboard shortcut modal, see [Next Experience keyboard shortcuts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/next-experience-keyboard-shortcuts.md). The keyboard shortcuts modal can also be accessed using **Command+/** \(Mac\) or **Control+/** \(Windows\).
-   **Impersonate user**: Administrators can impersonate other authenticated users for testing purposes and view impersonation logs. For more information, see [Impersonating users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/c_ImpersonateAUser.md).
-   **Elevate role**: Designate any role as an elevated privilege role, and then assign that role to one or more users. Do this when you want to restrict users from having access to the rights that the role provides immediately after login.
-   **Printer friendly version**: A printer-friendly version of the current content frame.

**Note:** The Printer-friendly version option is available in the classic environment but not in Workspace.


</td></tr></tbody>
</table>