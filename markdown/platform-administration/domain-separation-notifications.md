---
title: Domain separation and Notifications
description: Domain separation is supported in the Notifications application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Domain separation and Notifications

Domain separation is supported in the Notifications application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Overview

Domain separation is specifically supported in Notifications but not in email accounts. Notifications are not data-separated but they are process-separated. Notifications are also triggered by specific actions.

**Note:** Subscription-based notifications are not domain aware and cannot support domain-specific settings.

## How domain separation works in Notifications

There are two basic components of domain separation and Notifications.

-   Notifications are process-separated \(not data-separated\).
-   Notifications are triggered in two main ways:
    1.  When a record is Inserted or Updated

        Notifications with matching conditions AND in the same domain and global domain as the inserted/updated record are processed.

    2.  When an event defined in the notification is triggered
        1.  Events typically have a target record. For example, \[incident.inserted\] event references the incident record being inserted.
        2.  When an event is fired, notifications configured for that event in the same domain and global domain as the event’s target record are processed.

**Domains and email accounts**

Domain separation is not supported in email accounts for these reasons:

1.  Sending mail: There is only one SMTP sender per account. This prohibits providing domains for each account, and they are not configurable.
2.  For receiving Inbound mail: You can set up multiple email accounts but cannot meaningfully set the domain of an inbound email action. Inbound Actions are processed in the domain of the user who sent the email. For example: User\_A in Domain A sends an email to a ServiceNow email account which executes the “Create an incident” inbound email action. The resulting new incident created by the inbound action is in Domain A.

To learn more see [Inbound email actions](c_InboundEmailActions.md).

**Note:** If the number of email accounts exceeds 20, reception of email slows down.

## Use case

If an instance is using the [Domain separation plugin](https://www.servicenow.com/docs/access?context=c_DomainSeparationSetup&version=australia&pubname=australia-platform-security&ft:locale=en-US) and a new email notification is defined for a domain that has the same event as the notification on the global domain, the user receives two emails for the same event.

Solution: Set the \[sys\_overrides\] field on the notification that belongs to the domain so it overrides the setting on global. For more information, see [Delegated administration](https://www.servicenow.com/docs/access?context=c_DelegatedAdministration&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Parent Topic:**[Email and SMS notifications](c_EmailNotifications.md)

**Related topics**  


[Create notification categories](../task/create-notification-categories.md)

[Create an email notification](../task/t_CreateANotification.md)

[Email notifications dashboard](email-notifications-dashboard.md)

[Email diagnostics dashboard](email-diagnostics-dashboard.md)

[Email templates](c_EmailTemplates.md)

[Email layouts](email-layouts.md)

[Email retention](email-retention.md)

[Watermarks on notification emails](c_WorkingWithWatermarks.md)

[Parse an email thread](../task/parse-email.md)

[Email digests](email-digests.md)

[Email FAQs and troubleshooting notification emails](troubleshooting-notification-emails.md)

[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

