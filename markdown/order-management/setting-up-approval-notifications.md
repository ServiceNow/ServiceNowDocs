---
title: Notifications in Advanced Approval Management
description: In Advanced Approval Management, as an approval request moves through the approval process, notifications about the status of the approval request are sent automatically to approval requesters and approvers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/setting-up-approval-notifications.html
release: australia
topic_type: concept
last_updated: "2026-04-06"
reading_time_minutes: 5
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Notifications in Advanced Approval Management

In Advanced Approval Management, as an approval request moves through the approval process, notifications about the status of the approval request are sent automatically to approval requesters and approvers.

## Overview of approval notifications

The notification framework handles various approval scenarios in the approval process, including approvals for simple or consolidated approval requests, approval reminders, escalations, and approval overrides. The following system notifications are automatically activated with Advanced Approval Management:

-   Advanced Approval Request
-   Approval Reminder
-   Approval Escalation
-   Approval Request for Override
-   Notify approval req requester
-   Notify approval req approvers

-   **Advanced Approval Request notifications**

    The Advanced Approval Request notification informs approvers when an approval request has been submitted by a sales agent \(requester\). There are two types of approval request notifications: simple and consolidated.

    \[Omitted image "image.approval-notif-simple-consol"\] Alt text: Simple and consolidated email notifications sent to approvers, from which they can accept or reject approval requests.

    -   Simple approvals: A notification is sent to each approver when an approval request is submitted, as shown in the following example. The approver can approve or reject the approval request from the notification.

        **Note:** Ad-hoc approvers receive a simple approval notification and can approve or reject the request from the notification. Ad-hoc approvers can also approve or reject a request from a step in the General chain in the approval workflow interface. For more information on configuring ad-hoc approvers, see [Add approvers to an approval request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-approver.md).

    -   Consolidated approvals: When an approver receives multiple approval requests for approvals within the same set of approvals, the system can consolidate those requests into a single notification email, if your approval rules admin has turned on the email consolidation feature in your approval configuration.

        An approver can use the links in the consolidated notification to accept or reject requests individually or approve all or reject all requests. Approvers can also reply to the consolidation email and use reply-based commands to approve or reject individual requests or all requests. When approvers approve or reject a request, the body of the reply notification is prefilled, indicating approval or the reason for rejection.

    Both simple and consolidated approval emails are handled through a single notification definition, with different rendering logic used to generate the appropriate message format. These approval request emails can be delivered as mobile push notifications, if approvers are using the ServiceNow Mobile app, and Advanced Approval push notifications is set as a push notification channel in their notification preferences.

    **Note:** Ad-hoc approvers receive a simple approval notification. Or they can approve or reject a request from a step in the General chain in the approval workflow interface. For more information on ad-hoc approvers, see [Add approvers to an approval request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-approver.md).

-   **Approval Reminder**

    Approval Reminder notifications are sent to approvers automatically when the **Send auto reminders** and **Reminder schedule** features are set in the approval configuration by your approval rule admin. Each reminder is a separate email and is sent at the time specified in the reminder schedule, which is triggered by a scheduled job.

    The system generates the first reminder, subsequent reminders, and a final reminder that could lead to escalation, if the escalation feature is set for the approval configuration. For details on setting approval reminders, see [Create an approval configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-approval-configuration.md).

-   **Approval Escalation**

    If the escalation feature is enabled in your approval configuration, an Approval Escalation notification is sent to an approver when they do not act on an approval request within the scheduled timeframe. The notification indicates that the approver no longer needs to approve the final request. Escalation assignees also receive an escalation notification from which they can accept or reject the request.

-   **Approval Request for Overrides**

    With overrides, an approval admin for the ServiceNowAI platform who also has the requester role can approve or reject an approval request on behalf of other approvers. For example, the approval admin might need to unblock an approval step when the step is no longer needed. The approval admin uses the **Override** option in the step card in the approval workflow interface.

    When an override occurs, original approvers receive a notification stating that their action is no longer required because the approval was overridden. For more information on overrides, see [Override an approver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/override-approval-step.md).

-   **Notify approval request approvers**

    When a requester recalls an approval request, the Notify approval request notification informs approvers that the approval request has been recalled.

-   **Notify approval request requester**

    When changes in the state of an approval request occur, the Notify approval request notification informs requesters when the state changes to approved, rejected, or recalled.


## Notification prerequisites

For successful delivery of advanced approval notifications to approvers and requesters, verify that certain notification properties and notification preferences are set.

-   As an admin, do the following:
    -   Enable the email sending \(Outbound Email Configuration\) and email receiving \(Inbound Email Configuration\) properties. For information on setting these properties, see [Email properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailProperties.md).
    -   Consider reviewing the default notifications for Advanced Approval Management by navigating to **All** &gt; **Notifications** &gt; **System Notifications** and filter the list by Advanced Approval Management.

        For example, if you want to control conditions for sending a notification, review the conditions in the **When to send** related list for a notification. If you want to change content in a notification, review the associated email template for the notification. To learn more, see [Email and SMS notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailNotifications.md).

-   As approvers and requesters, verify that you’re receiving the default system notifications in the Advanced Approvals notification category and that the notifications are being delivered using your preferred channels.

    For example, if you're an approver and you want Advanced Approval Request notifications to be delivered as push notifications on the Now® Mobile application, verify that push notifications are set up as a channel preference for the Advanced Approval Request notification.

    To learn more about managing notification categories and setting notification preferences and channels, see [Exploring preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/exploring-preferences.md).


