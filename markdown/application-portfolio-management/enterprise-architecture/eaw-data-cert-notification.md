---
title: Data certification task notifications
description: When a data certification policy runs in the Enterprise Architecture Workspace, the system automatically sends email notifications to task assignees as due dates approach. This notification behavior is provided by the CMDB Data Manager and does not require additional configuration in the Enterprise Architecture Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/enterprise-architecture/eaw-data-cert-notification.html
release: australia
product: Enterprise Architecture
classification: enterprise-architecture
topic_type: concept
last_updated: "2026-05-15"
reading_time_minutes: 2
breadcrumb: [Working with data certification, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Data certification task notifications

When a data certification policy runs in the Enterprise Architecture Workspace, the system automatically sends email notifications to task assignees as due dates approach. This notification behavior is provided by the CMDB Data Manager and does not require additional configuration in the Enterprise Architecture Workspace.

You can control when notifications are sent by setting the **Days to complete** field when creating a certification policy and by enabling notifications in the CMDB Workspace Data Manager settings. For more information, see [Create a certification policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/enterprise-architecture/eaw-create-policy.md) and .

## Notification configuration

The due date notifications for certification tasks are controlled by the **Notifications** property \(`sn_cmdb_ws.cmdb.dm.policy_types.due_date_notification`\) in the CMDB Workspace Data Manager Settings page. The default value of this property is `attestation,certification`, which means due date notifications are active for both certification and attestation policy types.

To modify this setting, navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **Management**, select the **Data Manager** link, and then select **Settings** in the left navigation bar. The **Notifications** property requires the `data_manager_admin` role to update.

## Set the notification schedule in a certification policy

The **Days to complete** field in the **Options** form of a certification policy determines the time interval used to calculate when notifications are sent. The interval starts when a certification task is created and ends when the specified number of days elapses.

For more information, see [Options form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/enterprise-architecture/eaw-data-cert-options-form.md).

**Note:** Set a realistic number of days to allow assignees enough time to review and certify records before the due date. Notifications are sent at the 50%, 70%, and 90% milestones of this interval.

## Notification schedule

After a certification task is created and notifications are enabled, the system sends email reminders automatically based on how much of the **Days to complete** interval has elapsed. Notifications stop as soon as the task is closed.

|Notification|When sent|Recipients|
|------------|---------|----------|
|Due date is approaching|50% of the interval has elapsed|Task assignee \(`assigned_to` user\)|
|70% of the interval has elapsed|
|90% of the interval has elapsed|
|Due date breached|On the due date \(task still open\)|Task assignee \(`assigned_to` user\) and the assignee's manager \(`assigned_to.manager`\)|

## Respond to a notification

When you receive a due date notification, use the task number in the email subject to locate the certification task. For information about reviewing and completing certification tasks, see [Review and certify data certification tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/enterprise-architecture/eaw-approve-data-cert-tasks.md).

After the task is closed, no further notifications are sent for that task.

**Parent Topic:**[Working with data certification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/enterprise-architecture/eaw-work-with-data-cert.md)

