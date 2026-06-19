---
title: Receive certificate notifications via email
description: Configure certificate notifications to be delivered via email to relevant recipients.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/receive-email-certificate-notifications.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certificate alerts and notifications, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Receive certificate notifications via email

Configure certificate notifications to be delivered via email to relevant recipients.

## Before you begin

Role required: Certificate administrator \(glide.discovery.certs.cert\_admin\_user\_id\) or PKI Admin \(pki\_admin\).

## About this task

Certificate Inventory and Management sends email notifications for certificate life-cycle events such as certificate expiration, task creation, renewal completion, and auto-renewal failures.

## Procedure

1.  Configure the email address for users.

    1.  Navigate to **All** &gt; **Organization** &gt; **Users**.

    2.  Select a relevant user.

    3.  In the **Email** field, enter the email address.

    4.  Select **Update**.

2.  Enable email sending configuration.

    1.  Navigate to **All** &gt; **System Properties** &gt; **Email Properties**.

    2.  In the **Outbound Email Configuration** section, under **Email sending enabled**, select the **Yes/No** check box.

    3.  Select **Save**.

3.  Customize which certificate events trigger email notifications.

    1.  Navigate to **Workspaces** &gt; **Certificate Management**.

    2.  Select **Settings** in the menu bar and then select the **Notification** tab.

        The available notification types in the **Certificate notification policy** \[sn\_disco\_certmgmt\_notification\_policy\] table are:

        -   Auto-Renewal Failed notification
        -   Certificate Completed Failed notification
        -   Certificate Expired notification
        -   Certificate Expiring notification
        -   Certificate Renewal Task Created notification
        -   Certificate Task Creation notification
    3.  Select the Edit form icon \[Omitted image "edit-icon-workspace.png"\] Alt text: for the relevant notification type.

    4.  Verify the **Email enabled** check box is selected.

    5.  Select the **Email recipients** field and then select the email recipient you want to notify.

    6.  Select the **Email recipient Groups** field and then select the email recipient group you want to notify.

    7.  In **Email recipient fields**, enter comma-separated field names from the certificate task record to notify users or groups assigned to those fields.

        For example, to send notifications to the user and group assigned to the certificate record, you would enter `assigned_to,assignment_group`.

    8.  Select **Update**.


## Result

Certificate notifications are sent to relevant recipients as configured for each notification type.

**Parent Topic:**[Certificate alerts and notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/cert-inventory-mgmt-workflow.md)

