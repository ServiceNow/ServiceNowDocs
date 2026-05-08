---
title: Request an analytics service
description: Request services associated with dashboards, such as to request a new dashboard or access to an existing dashboard.Analytics service requests are assigned to the Analytics group who can review and fulfill the requests.You can activate the Self-Service Portal for Analytics plugin \(com.snc.pa.bi\_service\) if you have the admin role.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Request an analytics service

Request services associated with dashboards, such as to request a new dashboard or access to an existing dashboard.

## Before you begin

Role required: none

## Procedure

1.  Navigate to either **All** &gt; **Self-Service** &gt; **Service Catalog** or **Service Portal** &gt; **Service Portal Home**.

2.  If you navigated to the Service Portal, select **Order Something**.

3.  Select the **Can We Help You?** category.

4.  Select **Analytics Request**.

5.  Select the **Request type**, such as **Request dashboard access**, **Edit a dashboard**, or **Report an issue**.

6.  If you are submitting the request for another user, select the **Request on behalf of another user** check box and select the user you are making the request for.

7.  Provide additional details about your request, such as the name of the dashboard and a description of the changes you want made.

    Available fields depend on the request type.

    A notification is automatically sent to the requesting user.


## What to do next

After you submit the request, the Analytics team is responsible for reviewing and implementing your requested changes.

**Parent Topic:**[Create and use dashboards](../concept/create-and-edit-dashboards.md)

## Fulfill an analytics request

Analytics service requests are assigned to the Analytics group who can review and fulfill the requests.

### Before you begin

At least one user must be a member of the Analytics group.

Role required:

-   Fulfiller — itil and pa\_admin. The fulfilling user must be a member of the Analytics group which automatically grants these roles.
-   Approver — itil and approver\_user

### Procedure

1.  Navigate to **All** &gt; **Service Desk** &gt; **My Groups Work**.

2.  Select a request.

3.  If the request is to grant access to a dashboard, select the **Dashboard** that this request applies to.

4.  Select one or more users as the **Request Approver**.

    This approver should not be a member of the Analytics group.

    **Note:** No approval is required when the request type is **Report an issue**.

5.  The approver can then approve the request.

    1.  Navigate to **Self-Service** &gt; **My Approvals**.

    2.  Select the request approval.

    3.  Click **Approve**.

    If the approver rejects the approval, the request is closed automatically. If the approver selects an option other than approved or rejected, the fulfiller user can close the request by setting the **State** to **Closed Skipped** or **Closed Incomplete**.

    After the request is approved, or if no approval was required, a task is created for the Analytics team. Navigate to the **Tasks** related list on the request record to view the task. An email notification is sent to the Analytics team.

6.  After the approver approves the request, perform the requested changes to fulfill the request.

    Refer to the dashboards documentation for instructions on how to modify dashboards and dashboard permissions.

7.  Update the task **State** to **Closed Complete**.

    The request **State** is updated automatically when the task is closed. An email notification is sent to the requesting user to inform the user that the requested changes are complete.


**Related topics**  


[Create and use dashboards](../concept/create-and-edit-dashboards.md)

[Share a responsive dashboard](t_ControlAccessToADashboard.md)

## Activate the Self-Service Portal for Analytics plugin

You can activate the Self-Service Portal for Analytics plugin \(com.snc.pa.bi\_service\) if you have the admin role.

### Before you begin

Role required: admin

### About this task

Self-Service Portal for Analytics activates these related plugins if they are not already active.

<table id="table_esc_ssd_3z"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Performance Analytics\[com.snc.pa\]

</td><td>

Core Performance Analytics functionality

</td></tr></tbody>
</table>### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[bundle-platadm.list-of-plugins]

