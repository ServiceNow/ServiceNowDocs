---
title: Embed an approval request within the Outlook email client
description: Embed an interactive approval request for service catalog requests in the email notification sent to a user. The user can accept or reject the approval request from the email client.
locale: en-US
release: yokohama
product: Approvals
classification: approvals
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Receive notifications, Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Embed an approval request within the Outlook email client

Embed an interactive approval request for service catalog requests in the email notification sent to a user. The user can accept or reject the approval request from the email client.

## Before you begin

Role required: admin

The Outlook Actionable Messages plugin \(com.sn\_ms\_oam\) should be activated.

**Note:**

-   The Outlook Actionable Messages \(OAM\) feature is not supported in all Microsoft mail products and versions. To verify whether your version of Outlook supports OAM, refer to the [Microsoft](https://docs.microsoft.com/en-us/outlook/actionable-messages/) documentation.
-   Actionable messages are supported only for emails sent from the @service-now.com email address. If you are sending an email from a customized email address, you should register as a new service in the [Microsoft](https://aka.ms/publishoam) website setting the scope as **Organization**. Specify the provider ID value in the **sn\_ms\_oam.outlookactionable.originator** property.
-   Actionable messages are based on the Sender Policy Framework \(SPF\)/DomainKeys Identified Mail \(DKIM\) validation for the email sender verification. If an email recipient receives email via an external provider, emails may not be rendered as adaptive cards.
-   You cannot customize the default actionable message templates.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  For the approval notification that requires user approval, in the **What it will contain** tab, add the following script in the **Message** field in addition to the existing information, or to the **Message** field in the configured email template if applicable.

    ```
    ${mail_script:include_approval_actionable}
    ```

    For example, for the Catalog Approval Request and Approval Request notifications, you can include the script in `request.itil.approve.role` and `change.itil.approve.role` email templates.

    This script includes the Outlook actionable message in the email notification sent to the user for approvals.

3.  Click **Update**.


**Parent Topic:**[Receive notifications](../concept/c_ReceiveNotifications.md)

