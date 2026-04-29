---
title: Sync your applications from Microsoft Entra ID
description: As an administrator, you can sync your single-sign-on applications and give one-click access to the applications. You can associate topics to the applications to launch useful applications right from the portal.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [App Launcher, Setup task management, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Sync your applications from Microsoft Entra ID

As an administrator, you can sync your single-sign-on applications and give one-click access to the applications. You can associate topics to the applications to launch useful applications right from the portal.

## Before you begin

Role required: sp\_admin and admin

-   The App Launcher synchronization of applications from Azure is compatible only with the latest Microsoft Entra ID spoke version. Ensure that you upgrade the existing Azure AD spoke to sync the apps with your web applications.
-   Azure AD integration enables your employees to access and manage pre-integrated apps.
-   Integrate Azure AD spoke with ServiceNow, create credential records, and create connection records as explained in [Azure AD spoke setup](https://www.servicenow.com/docs/access?context=set-up-azure&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   Understand the basics of [Azure](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/) spoke and service principals.
-   Enable easier access to all active apps with valid entitlement in SSO without asking for login credentials.

## About this task

By using the App Launcher with Employee Center Pro, you can do the following actions:

-   Sync the registered applications from the connected Azure AD account to your applications widget.
-   Enable access to the applications based on user permissions for Azure identity management.
-   Manage all active applications of Azure AD in your instance.
-   Configure the application integration such as add, create, and assign applications to users or groups.
-   Change the app icon, label, and link or mark the app as inactive.

Azure AD integration enables your employees to access and manage pre-integrated apps.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Web Applications**.

2.  To fetch applications from the Azure account, click **Update applications**.

    All the Azure applications appear. See the following information:

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

Description for the web application. **Note:** For Azure apps, the description is empty due to an Azure API limitation. However, you can manually add the description.

</td></tr><tr><td>

Active

</td><td>

Status of the web application. Only active applications for the user are displayed.

</td></tr><tr><td>

Categories

</td><td>

Category to which the application is assigned. You can create categories and assign the app to one or many app categories.

</td></tr><tr><td>

App source

</td><td>

Source of the application:Azure: Applications that are synchronized by administrators who use external integrations such as Azure.

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

User group for whom the app is available. Define and select the user group based on your business needs. This field is applicable only for custom applications.Application visibility and access are based on your configuration of the **Available for** option.

**Note:** When you mark an application as **Available for** a user, the app is visible and accessible in the search results.

</td></tr><tr><td>

Not available for

</td><td>

User group for whom the app is unavailable. Values that are defined at the **Not available for** take precedence over **Available for**. This field is applicable only for custom applications.Application visibility and access are based on your configuration the **Not available for** option.

**Note:** When you mark an application as **Not available for** a user, the app is not visible and accessible in the search results.

</td></tr><tr><td>

Is record updated

</td><td>

Record update setting to indicate if the Azure app record is manually updated. The value changes to true on manual changes. For custom apps, the default is false.**Note:** This field is applicable only for apps that are synchronized with the Azure integration.

</td></tr><tr><td>

Featured

</td><td>

Option to mark the application as featured. Use the **Featured** option to promote new or important or seasonal applications for higher visibility. **Note:** Featured applications have display preferences and appear on the top of the page despite any filters or sorting.

</td></tr></tbody>
</table>    **Note:** API [throttling](https://docs.microsoft.com/en-us/graph/throttling) limits vary based on multi-tenant or single-tenant configuration.

3.  Click **Save**.

    Applications are fetched. You can proceed to associate topics that are suitable for the application.

4.  To assign the topics to the applications, see [Assign topics to web applications](web-applications-topic-assignment.md).


## Result

When you sync applications, you can see the list of Azure apps and track the flow execution status from the related link on the page.

## What to do next

To sync the latest apps, you can do the following actions:

-   Click **Update applications** from **All** &gt; **Employee Center** &gt; **Web Applications** to sync the updates instantly with the sn\_hr\_sp.esc\_admin role. When you update apps, you can track the flow execution status from the related link on the page.
-   Run the **Fetch applications** schedule job from **System definition** &gt; **Scheduled jobs** to sync the updates automatically on an as needed-basis or once a day.

**For upgrades:** When you have an existing Azure AD spoke and connection and upgrade to the employee center pro with the App Launcher, the apps get synced through a job automatically and are updated nightly. To disable the fetch applications job, you must mark the job as inactive from **System Definition** &gt; **Scheduled job**.

```
Scheduled Job: Fetch applications 
table: sysauto_script
sys_id: 48b46a8a4744c1109dcae052846d43cf
```

Based on the user permissions, service principals, and the applications that are mapped with the Azure service principals, the applications are displayed on the App Launcher. Verify the service principals from the Azure app service principals.

-   When user access permissions change at the Azure side, the updates are synced real-time on the applications widget. To see the changes, re-login to your Azure account.
-   Changes to the app metadata reflect only after the next sync.

**Note:** When an application is hidden, users still have permissions to the application until the next synchronization.

