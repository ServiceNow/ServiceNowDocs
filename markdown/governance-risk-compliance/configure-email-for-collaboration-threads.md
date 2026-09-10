---
title: Configure email for collaboration threads
description: Configure an email account and enable the outbound and inbound email properties so that crisis managers can send and receive email from collaboration threads.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/configure-email-for-collaboration-threads.html
release: australia
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 2
keywords: [email account, email properties, collaboration, business continuity management, BCM]
breadcrumb: [Setup by system administrators, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure email for collaboration threads

Configure an email account and enable the outbound and inbound email properties so that crisis managers can send and receive email from collaboration threads.

## Before you begin

Role required: admin

## About this task

Sending and receiving email from a collaboration thread requires at least one active email account and the system properties that enable outbound and inbound email processing. Configure these before crisis managers compose or receive email from a collaboration thread.

## Procedure

1.  In the filter navigator, search for and select **Email Accounts** under **System Mailboxes** and **Administration**.

    \[Omitted image "cm-collab-email-config-email-accounts-option.png"\] Alt text: Filter navigator search for the Email Accounts module.

2.  Verify that at least one active SMTP account is available for sending email and at least one active POP3 or IMAP account is available for receiving email.

    The example shows the default **ServiceNow SMTP** and **ServiceNow POP3** accounts with the **Active** column set to true.

    \[Omitted image "cm-collab-email-config-two-email-accounts.png"\] Alt text: Email Accounts list with name, active status, type, server, and port columns.

3.  In the filter navigator, search for and select **Email Properties** under **System Properties**.

    For more information on the Email Properties configurations in the ServiceNow AI Platform, see [Email properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailProperties.md).

    \[Omitted image "cm-collab-email-config-email-properties.png"\] Alt text: Filter navigator search for the Email Properties module.

4.  In **Outbound Email Configuration**, select **Yes** for **Email sending enabled**.

    \[Omitted image "cm-collab-email-config-email-properties-config.png"\] Alt text: Email Properties page with outbound and inbound email configuration sections.

5.  In **Inbound Email Configuration**, select **Yes** for **Email receiving enabled**.

6.  Select **Save**.

    Crisis managers can now send and receive email from collaboration threads on crisis events.

7.  Verify that both email properties remain enabled.

    **Note:** By default, sending and receiving email is disabled on a new instance. If **Email sending enabled** is set to **No**, emails composed from collaboration threads stay in **Send Ready** status and never move to **Sent**. If either property is disabled, the compose and reply or forward email options are hidden from the collaboration thread UI rather than shown as unavailable.


**Parent Topic:**[Setup by system administrators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/set-up-bcm-sys-admin-tasks.md)

**Related topics**  


[Creating collaborations in exercises and crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/creating-collaboration-threads-in-crisis.md)

[Create a collaboration thread in a crisis event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/compose-email-collaboration-thread-crisis.md)

