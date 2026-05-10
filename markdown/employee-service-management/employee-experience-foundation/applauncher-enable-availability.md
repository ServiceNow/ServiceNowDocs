---
title: Configure application visibility and access
description: Enhance application discovery and navigation on the App launcher by configuring the access and visibility settings.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [App Launcher, Setup task management, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure application visibility and access

Enhance application discovery and navigation on the App launcher by configuring the access and visibility settings.

## Before you begin

Role required: Admin, ESC admin, and taxonomy manager.

Ensure you configure and enable AI search capabilities, see the following AI Search topics:

-   [Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-ais.md)
-   [Configuring navigation tabs in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/config-nav-tabs-ais.md) and tag **ESC Portal Default Search Application**

## About this task

Administrators can control user access by specifying who can and can’t use the application. You can specify the users for whom the application is **Available for** and **Not Available for**.

-   Improve the app discovery for employees to find relevant apps more quickly and easily.
-   Enhance the application discovery from a unified search experience with the **Applications** tab in search results.
-   Define the user access controls to ensure users see and access only the authorized applications.
-   Increase adoption and productivity for registered and custom applications:
    -   For Azure and Okta integrated apps, user access must be cached at the first load of the App launcher.
    -   For custom apps, permissions must be evaluated in real-time for each search.

**Note:** You can use this feature base system with the default ESC search profile. For existing users with custom search config, ensure you manually map the changes to the custom search profile.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Web Applications**.

2.  Click **New**.

3.  Configure the **Application** form as explained in [Register custom web applications with app launcher](web-applications-custom.md).

4.  Configure the user access control options for application visibility and access.

    -   **Available for**: Users or user group for whom the application is accessible and visible.
    -   **Not available for**: Users or user group for whom the application isn't accessible and visible.
5.  Click **Submit** or **Save**.


## Result

Based on the configuration, the applications are made visible to the employees both from the app launcher and from AI search results.

When an application is configured **Available for** a user, the search results show the application cards with name, icon, description, and link to the relevant applications that the user has access to.

**Note:** When the app doesn't have a configured brand icon, a default icon appears.



**Note:** When you mark an application as **Not Available for** a user, the application tab on the search results indicates the count. However, the user can’t see or navigate to the application due to user permissions.

For more information on Application security directive changes, see [App Launcher](../concept/web-application-employee-about.md)

**Related topics**  


[Manage favorites](web-configure-favorites-employee.md)

