---
title: Create Security Operations email properties
description: You can specify email addresses for reports and control automatic email behaviors using email Properties.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations email properties, Security Operations email processing, Security Operations common functionality, Security Operations]
---

# Create Security Operations email properties

You can specify email addresses for reports and control automatic email behaviors using email Properties.

## Before you begin

Role required: sn\_sec\_cmn.admin

Set up external detection tools to send emails to your email parsing inbox.

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Email Processing** &gt; **Properties**.

2.  Enter your recipient mailboxes as appropriate:

    These are inbound email addresses to be processed by **Email Parsing**, rather than **Inbound Actions**.

    |Field|Description|
    |-----|-----------|
    |Inbox for Security Operations tools|Full email address for Security Operations. For example, secops\_support@yourcompany.com.|
    |Inbox for Security Incident tools|Full email address for Security Incident Response. For example, sir\_support@your.company.com.|
    |Inbox for Vulnerability Response tools|Full email address for Vulnerability Response. For example, vuln\_resp@yourcompany.com.|
    |Inbox for Threat Intelligence tools|Full email address for Threat Intelligence. For example, threat\_intel@yourcompany.com.|

3.  Click **Save**.


**Parent Topic:**[Security Operations email properties](../concept/email-properties.md)

