---
title: Set up email alerts for Patient 0 events
description: Configure Zscaler Internet Access product to identify and scan for unknown, potentially malicious files, such as Patient 0 events so that you can protect your network from malicious files.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up email alerts for Patient 0 events

Configure Zscaler Internet Access product to identify and scan for unknown, potentially malicious files, such as Patient 0 events so that you can protect your network from malicious files.

## Before you begin

Role required: sn\_si.admin, Zscaler Internet Access admin

## About this task

Patient O is an alert class that includes an unknown file that has been permitted to download but is found to be malicious. The patient 0 event is classified as critical. You can set up the ServiceNow AI Platform to receive email alerts at regular intervals for Patient 0 events.

## Procedure

1.  Navigate to **All** &gt; **System Mailboxes** &gt; **Administration** &gt; **Email Properties**.

2.  In the Inbound Email Configuration section, select the **Email receiving enabled** option.

    ![Configuring inbound email.](../image/zscaler-inbound-email-config.png "Inbound email configuration")

3.  Click **Save**.

4.  Navigate to **System Mailboxes** &gt; **Administration** &gt; **Email Accounts**.

    ![ServiceNow AI Platform SMTP email account.](../image/zscaler-smtp-email-account.png)

5.  Select the **ServiceNow SMTP** email account.

    Note the user name. The user name that is identified here is the ServiceNow AI Platform email address that you use to configure in Zscaler for Patient 0 alerts.

    ![User name for the ServiceNow AI Platform SMTP account.](../image/zscaler-user-name.png "User name for the ServiceNow AI Platform SMTP account")

6.  Log in to the Zscaler Internet Access administration portal.

    **Note:** For more information on the Zscaler Internet Access administration portal, see the [Zscaler documentation](https://help.zscaler.com/zia/configuring-patient-0-alert).

7.  Navigate to **Administration** &gt; **Alerts** &gt; **Publish Alerts**.

8.  Click **Add Alert Subscription**.

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Email|ServiceNow AI Platform SMTP account email address.|
    |Description|Field for adding more details about the Patient 0 alerts.|

10. Click **Save**.


