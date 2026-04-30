---
title: Register custom web applications with app launcher
description: As an administrator, you can register applications manually and give one-click access to the applications. You can associate topics to the applications to discover and launch useful applications from the topic page.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [App Launcher, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Register custom web applications with app launcher

As an administrator, you can register applications manually and give one-click access to the applications. You can associate topics to the applications to discover and launch useful applications from the topic page.

## Before you begin

Role required: sp\_admin, taxonomy admin, or taxonomy manager

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Web Applications**.

2.  Click **New**.

3.  On the form, fill in the following fields.

<table id="table_lgk_4yj_crb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the web application

</td></tr><tr><td>

Description

</td><td>

Description for the web application

</td></tr><tr><td>

Active

</td><td>

Active indicates the status of the web application. Only active applications for the user are displayed.

</td></tr><tr><td>

Categories

</td><td>

Category to which the application is assigned. You can create categories and assign the app to one or many app categories.

</td></tr><tr><td>

App source

</td><td>

Source of the application:-   **Custom**: Applications registered by admins using the EC Web Application option
-   **Azure**: Applications synced by admins using external integrations such as Azure.


</td></tr><tr><td>

Application URL

</td><td>

URL of the application

</td></tr><tr><td>

Application icon

</td><td>

Icon of the applicationWhen a brand icon isn't configured, a default icon appears.

**Note:** Ensure you configure a brand icon for the application for better user experience.

</td></tr><tr><td>

Application icon URL

</td><td>

URL of the application icon

</td></tr><tr><td>

Available for

</td><td>

User group for whom the app is available. Define and select the user group based on your business needs. Applicable only for custom applications.Application visibility and access are based on your configuration of the **Available for** option.

**Note:** When you mark an application as **Available for** a user, the app is visible and accessible in the search results.

</td></tr><tr><td>

Not available for

</td><td>

User group for whom the app is unavailable. Values defined at the **Not available for** take precedence over **Available for**. Applicable only for custom applications.Application visibility and access are based on how you configure the **Not available for** option.

**Note:** When you mark an application as **Not available for** a user, the app isn’t visible and accessible in the search results.

</td></tr><tr><td>

Is record updated

</td><td>

Record update setting to indicate if the Azure app record is manually updated. Value changes to true on manual changes to the app record. For custom apps, the default is false. This flag is internally used to exclude specific modified application from the regular data sync job. **Note:** Applicable only for apps synced with the Azure integration.

</td></tr><tr><td>

Featured

</td><td>

Option to mark the application as featured. Use the **Featured** option to promote new or important or seasonal applications for higher visibility. **Note:** Featured applications have display preferences and appear on the top of the page despite any filters or sorting.

</td></tr></tbody>
</table>    For more information, see [Configure application visibility and access](applauncher-enable-availability.md).

4.  Click **Submit**.

    The application is registered. You can proceed to associate topics suitable for the application.

5.  Follow the steps from [Assign topics to web applications](web-applications-topic-assignment.md) to assign the topics to applications.

6.  Click **Update** to assign the topics to an application.

7.  Define the **Order** score to determine the display of the applications on the topic page.

    -   By default, the applications appear in alphabetical order. On use, the display order changes by **Recent use** on the home page widget.
    -   For display preferences, configure the order sequence per your organizational needs.
    You can register multiple applications based on your requirements.


## Result

When you create applications, you can see the list of custom apps.

## What to do next

Your employees can access all applications and associated topics. See [Access applications from App Launcher](../concept/web-application-employee.md).

