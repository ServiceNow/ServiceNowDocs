---
title: Modify email notifications to use notification redirection
description: Update email notifications to use the notification redirection framework so users are automatically directed to the appropriate view based on their workspace access.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [GRC notification redirection, Common GRC features, Governance, Risk, and Compliance]
---

# Modify email notifications to use notification redirection

Update email notifications to use the notification redirection framework so users are automatically directed to the appropriate view based on their workspace access.

## Before you begin

You must have notification routing rules configured before modifying notifications. For more information, see [Configure GRC notification redirection](configure-email-notification-redirection.md).

Role required: admin

## About this task

To enable redirection for a notification, replace the standard URL variables with mail script references that call the redirection framework. The system uses these mail scripts to generate URLs that route users to the appropriate view based on their workspace access.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Open the notification that you want to modify.

3.  Select the **What it will contain** tab.

4.  In the **Message HTML** field, replace the URL variable values.

    -   To display a link as the link text, replace `${URI}`, with `${mail_script:RecordNotificationRedirectionScript}`.
    -   To display the record name as the link text, replace `${URI_REF}` with `${mail_script:RecordREFNotificationRedirectionScript}`.
    -   For list view links, create a custom mail script that uses the `GRCNotificationRedirectionUtils` script include to generate the redirection URL.
5.  Select **Update**.


## Result

When users select links in the modified notification, the system automatically directs them based on their workspace access. If they have workspace access, they're directed to workspace view. If they don't have workspace access, they're directed to classic view.

**Parent Topic:**[GRC notification redirection](../concept/email-notification-redirection.md)

**Related topics**  


[Modify email notifications to use notification redirection](modify-email-notifications-to-use-notification-redirection.md)

