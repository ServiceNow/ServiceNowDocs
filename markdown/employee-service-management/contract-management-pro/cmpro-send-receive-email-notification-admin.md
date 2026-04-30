---
title: Use default email notifications
description: Use the default email notifications to communicate the progress of the request.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up Contracts Core, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Use default email notifications

Use the default email notifications to communicate the progress of the request.

## Before you begin

Role required: Admin

## About this task

You can configure the email notifications for each of your actions to share the status of your approvals. Use the predefined email notifications when

-   Approval is initiated.
-   Approval is cancelled.
-   Approval is approved.
-   Approval is rejected.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Notifications**.

2.  In the Category field, search for the **Contracts Support** items.

3.  Navigate to the existing platform notifications.

4.  Add a condition where the Source table is not **sn\_cm\_core\_document\_revision**.

5.  You must manually activate by updating the Active field to true.

    **Note:** These email notifications are inactive by default.

6.  Ensure you specify the **getWorkspaceURL** value that's appropriate for your business unit.

    For example, the Legal Counsel Center getWorkspaceURL:

    ```
    getWorkspaceURL: function() {
            return "legal/counsel-center";
    ```

    . For more information, see [Configure extension point for notifications](cmpro-configure-action-extension-point-email-notification-admin.md)


## Result

You can now use the list of available default email notifications.

To create new email notifications, follow the instructions available at [Create an email notification](https://servicenow.com/docs/bundle/vancouver-platform-administration/page/administer/notification/task/t_CreateANotification.html).

**Parent Topic:**[Set up Contracts Core](../concept/cncore-setup-cmpro.md)

**Related topics**  


[Create a contract type](cncore-create-contract-type.md)

[Create document template categories](cncore-create-doc-tmplt-cat.md)

[Enable users to view email details in activity stream](cncore-enbl-user-email-astream.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Configure reminders for expiring contracts](cncore-config-rem-exp-cont.md)

[Configuring external applications for Contract Management Pro](../concept/cncore-set-ext-app-config.md)

[Configure extension point for notifications](cmpro-configure-action-extension-point-email-notification-admin.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

