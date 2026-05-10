---
title: Configure email-based intake for AI Risk and Compliance
description: Configure email-based intake so that incoming email messages create intake records in AI Risk and Compliance.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Configure, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Configure email-based intake for AI Risk and Compliance

Configure email-based intake so that incoming email messages create intake records in AI Risk and Compliance.

## Before you begin

Role required: admin and sn\_ai\_case\_mgmt.ai\_case\_admin

## About this task

You can submit AI‑related cases or inquiries by sending emails to configured addresses. When the system receives an email, the system automatically processes it by extracting key information, such as the subject, body, and sender, and creates the corresponding AI Case or Inquiry so that the system captures submissions consistently and makes them available for review and action. Email‑based intake requires inbound email processing to be enabled at the instance level and intake configuration to be defined in AI Case Management, which together determine how the system processes incoming emails and which intake types the system creates.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Email Properties**.

2.  Enable inbound email processing on the instance by selecting **Yes** for the **Email receiving enabled** \(`glide.email.smtp.active`\) and **Automatically create users for incoming emails from trusted domains** \(`glide.pop3readerjob.create_caller`\) properties.

    This enables inbound email processing so the instance can receive and evaluate incoming email messages.![Inbound email configuration settings that control email processing at the instance level.](../image/inbound-email-properties-airc.png)

3.  Navigate to **All** &gt; **AI Case Management** &gt; **Case Type**.

4.  Select the **Inbound Email Configuration** related list and enter the group email address configured for inbound email.

    Configuring the **Group email** field on the AI case intake type record sets the email address used for case intake.![AI case intake type showing the group email configuration.](../image/ai-case-group-email.png)

5.  Navigate to **All** &gt; **AI Case Management** &gt; **Inquiry Type**.

6.  Select the **Inbound Email Configuration** related list and enter the group email address configured for inbound email.

    Configuring the **Group email** field on the AI inquiry intake type record sets the email address used for inquiry intake.![AI inquiry intake type showing the group email configuration.](../image/ai-inquiry-group-email.png)


## Result

Emails sent to the configured group email address and the instance email address create corresponding intake records in AI Risk and Compliance.

For more information, see [Automatic creation of AI cases and inquiries from inbound email](../concept/automatic-creation-cases-inquiries-from-email.md).

