---
title: App launcher integration with Okta
description: Using OOTB integration with Okta, you can automatically sync the registered applications from Okta and give your employees one–click access to a personalized list of assigned applications. Your employees can easily access all the active apps with valid entitlement in Okta without specifying the login credentials.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [App Launcher, Setup task management, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# App launcher integration with Okta

Using OOTB integration with Okta, you can automatically sync the registered applications from Okta and give your employees one–click access to a personalized list of assigned applications. Your employees can easily access all the active apps with valid entitlement in Okta without specifying the login credentials.

## Before you begin

-   The app launcher sync of applications from Okta is only compatible with the latest Okta Spoke version. Ensure you upgrade the existing Okta spoke to sync the apps on to your web applications.
-   Integrate Okta spoke with ServiceNow, Inc., create credential records, and create connection records as explained in [Okta spoke setup](https://www.servicenow.com/docs/access?context=okta-v2-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

Role required: sp\_admin, taxonomy admin, or taxonomy manager

## About this task

After the spoke setup, Okta applications are synced on daily basis to a web application table from the Okta account. To sync the latest applications, you can do the following:

-   As sn\_hr\_sp.esc\_admin, navigate to **All** &gt; **Employee Center** &gt; **Web Applications** &gt; **Update applications** to sync the updates instantly.

    When you update applications, you can track the flow execution status from the related link on the page.

-   As an admin, sync the updates automatically on need-basis or once everyday by running the **Fetch applications** schedule job from **System definition** &gt; **Scheduled jobs**.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Web Applications**.

2.  Fetch applications from the external integrations Okta, by clicking **Update applications**.

    All the Okta applications appear with the following information:

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

Description for the web application.

</td></tr><tr><td>

Active

</td><td>

Active indicates the status of the application. Only active applications for the user are displayed.

</td></tr><tr><td>

Categories

</td><td>

Category to which the application is assigned. You can create categories and assign the app to one or many app categories.

</td></tr><tr><td>

App source

</td><td>

Source of the application. Okta applications synced by admins using integrations.

</td></tr><tr><td>

Application URL

</td><td>

URL of the application

</td></tr><tr><td>

Application icon

</td><td>

Icon of the application

</td></tr><tr><td>

Application icon URL

</td><td>

URL of the application icon

</td></tr><tr><td>

Is record updated

</td><td>

Record update setting to indicate if the Okta app record is manually updated. The value changes to true on manual changes to **Name** and **application URL**. For custom apps, the default is false.**Note:** Applicable only for apps synced with the Okta integration.

</td></tr><tr><td>

Featured

</td><td>

Option to mark the application as featured. Use the **Featured** option to promote new or important or seasonal applications for higher visibility. **Note:** Featured applications have display preferences and appear on the top of the page despite any filters or sorting.

</td></tr></tbody>
</table>    Applications are fetched. You can proceed to associate topics suitable for the application.

3.  Assign the topics to applications by following the steps from [Assign topics to web applications](web-applications-topic-assignment.md).


## Result

When you sync applications, you can see the list of Okta apps. Track the flow execution status from the **Okta flow execution status** related link on the page.

## What to do next

For upgrades: When you have an existing Okta spoke and connection and if upgrade to the employee center pro with the App launcher feature, the apps get synced through a job automatically and are updated nightly. To disable the fetch applications job, you must mark the job to the inactive state from **System Definition** &gt; **Scheduled job**.

```
Scheduled Job: Fetch applications 
table: sysauto_script
sys_id: 48b46a8a4744c1109dcae052846d43cf
```

Based on the user permissions and the applications mapped with the Okta, the applications are displayed on the App launcher.

-   When user access permissions change on the Okta side, the updates are synced real-time on the applications widget. To see the changes, re-login to your Employee Center account.
-   Changes to the app metadata such as Deletion, status change, or selecting **Do not display application icon to users** reflect only after the next sync. After sync, the apps are marked inactive and hidden from users.

**Note:** When an application is hidden, users still have permissions to the application until the next sync.

