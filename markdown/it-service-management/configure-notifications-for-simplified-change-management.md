---
title: Configure notifications for Simplified Change Management
description: Add and manage notifications for Change Management to keep users informed about approvals, status updates, and task assignments at key steps in the change process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-notifications-for-simplified-change-management.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 4
breadcrumb: [Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure notifications for Simplified Change Management

Add and manage notifications for Change Management to keep users informed about approvals, status updates, and task assignments at key steps in the change process.

## Before you begin

Role required: sn\_itsm\_chg\_admin.notification\_config

## About this task

Notifications keep stakeholders informed at critical points in the change lifecycle such as when a change is submitted for approval, assigned, updated, or completed.

The following types of pre-configured notifications are available:

-   Assignment and task notifications alert users when a change request or change task is assigned directly to them or to their group, ensuring the right people are aware of new work.
-   Update notifications notify relevant parties when a change request or task receives a work note or comment, whether the record is assigned or unassigned, so no updates go unnoticed.
-   Status and lifecycle notifications cover key state transitions, including when a change request is approved, rejected, put on hold, taken off hold, or when its state changes. Emergency change created and Unauthorized change created notifications flag high-priority situations requiring immediate attention.
-   CAB notifications manage meeting logistics for CAB delegates and board members, covering meeting invitations, cancellations, and delegate additions so all participants have the information they need ahead of CAB reviews.
-   Calendar notifications handle adding and removing change events from assignees' calendars, keeping schedules aligned with change activity.
-   External and survey notifications inform stakeholders when an external change is registered in the system and prompt users to complete a survey on change completion.
-   Approval notifications \(Change approved, Change rejected\) alert the assigned user of the final approval decision, supporting timely action on the change.

## Procedure

1.  From the header of your ServiceNow instance, navigate to **All** &gt; **Admin Home**.

2.  From the **Manage your products** section, select **View product overview** for IT Service Management.

3.  On the Product Hub page for IT Service Management, from the Configure your product section, select **Configure**.

4.  On the Configuration Console, from the left navigation panel, select **ITSM fulfiller experience &gt; Change Management &gt; Notifications**. \[Omitted image "simplified-change-notifications.png"\] Alt text: Notifications configuration page

    The **Notifications** list displays the pre-configured change notifications based on change definitions, showing each notification's name, active status, category, email template, and trigger conditions.

5.  To create a new notification, select **Add a notification** on the top-right corner of the list.

6.  Fill in the following fields.

    |Field|Action|
    |-----|------|
    |**Name**|Enter a descriptive name for the notification.|
    |**Table**|Select the table that triggers this notification. This field is required.|
    |**Mandatory**|Select if users cannot opt out of this notification.|
    |**Category**|Select a category to group the notification with related items.|
    |**Allow Digest**|Select to combine multiple updates for the same record into a single notification within a set time interval.|

    **Note:** The notification is marked as active by default. To make it inactive, deselect the **Active** option.

7.  On the **When to send** tab, define the trigger conditions.

<table id="table_ibc_3pb_kr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Send when

</td><td>

Select under what condition that the notification is sent: -   When a record is inserted or updated
-   When a particular event is fired
-   When [Notification step](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/trigger-notification-action-designer.md) in Flow Designer


</td></tr><tr><td>

Weight

</td><td>

\[Required\] Set a numerical value for the notification priority relative to duplicate notifications.

</td></tr><tr><td>

Conditions

</td><td>

Use the condition builder to select the conditions under which this notification is sent.

</td></tr><tr><td>

Inserted

</td><td>

Select the check box to enable email notification when a record is inserted. This field appears when you set the **Send when** field to **Record inserted or updated**.

</td></tr><tr><td>

Updated

</td><td>

Select the check box to enable email notification when a record is updated. This field appears when you set the **Send when** field to **Record inserted or updated**.

</td></tr><tr><td>

Event name

</td><td>

Select the event that triggers this notification. This field appears when you set the **Send when** field to **Event is fired**.

</td></tr><tr id="AdvancedConditions"><td>

Advanced condition

</td><td>

Create a script to perform certain actions, like sending a notification based on the current email record, changing field values, or changing system properties.

</td></tr></tbody>
</table>8.  Select the **Who will receive** tab and configure the notification recipients, such as users, groups, or subscribers.

9.  Select the **What it will contain** tab and configure the email template and message body content.

    For more information on creating notifications, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateANotification.md).

10. Select **Submit**.

11. On the Notifications landing page, select **Mark as configured** to save your settings and mark this step as complete.

    To revert changes made in the current session before saving, select **Undo**.

    As an alternative to the form-based wizard, you can also complete this configuration through the **Configure with Now Assist** conversational flow, accessible from the banner at the top of the page.

    **Note:** To deactivate a low-value notification without deleting it, locate it in the **Notifications** list and set its **Active** field to **false**. Deactivated notifications remain in the list and can be reactivated at any time.


## Result

The notification is saved and appears in the **Notifications** list. It fires automatically whenever the defined conditions are met.

**Parent Topic:**[Configuring Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-change-management-experience-in-it-service-management.md)

