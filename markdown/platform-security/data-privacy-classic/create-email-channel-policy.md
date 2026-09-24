---
title: Create an inbound email channel policy
description: Create a new policy for the inbound email channel to define sensitive data patterns that should be masked in inbound emails.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/create-email-channel-policy.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Data privacy for inbound emails, Data Privacy, Platform Privacy]
---

# Create an inbound email channel policy

Create a new policy for the inbound email channel to define sensitive data patterns that should be masked in inbound emails.

## Before you begin

Role required: data\_privacy\_admin and admin

## Procedure

1.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Anonymization**.

2.  Select **Create new policy**.

3.  Select **Real time data** as the data policy type.

4.  Enter a descriptive name for the email channel policy.

    Use a clear name such as "email Credit Card Masking" or "Inbound Email PII Redaction" to indicate the policy's purpose.

5.  Choose **Inbound email** as the **Data to process**.

6.  Select **Continue**.

7.  Select **Select data patterns** to choose the sensitive data patterns to be masked in inbound emails.

    1.  From the available patterns list, select one or more patterns \(for example, Credit Card, Social Security Number, Email Address\).

    2.  Select **Save** to save the data pattern choices.

    Patterns define what constitutes sensitive data in the email content. Multiple patterns can be selected if emails may contain different sensitive data types.

8.  Select **Save** to save the policy in draft status, or **Publish** to make it active.

    Once activated, the policy begins monitoring inbound emails and masking sensitive data according to the configuration.


