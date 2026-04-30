---
title: Configure inbound email to enable privacy case creation
description: This configuration allows administrators to set up a designated email address that employees can use to report privacy cases through email.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 1
breadcrumb: [Configure, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Configure inbound email to enable privacy case creation

This configuration allows administrators to set up a designated email address that employees can use to report privacy cases through email.

## Before you begin

Role required: Privacy admin

## Procedure

1.  Configure inbound email configuration:

    1.  Navigate to **All** &gt; **System Properties** &gt; **Email Properties**.

    2.  In Inbound Email Configuration section, do the following:

    -   Set **Email receiving enabled** to **Yes**.

        This enables the instance to process incoming emails.

    -   Set **Automatically create users for incoming emails** from trusted domains to **Yes**.

        This enables the application to create user records for senders from trusted domains.

2.  Add the group email address for privacy case creation:

    1.  Navigate to **All** &gt; **Privacy Case Management** &gt; **Case Configuration** &gt; **Case Type**.

    2.  Select the Inbound Email Configuration tab.

    3.  Add the group email address \(for example, create-&lt;case/inquiry&gt;@emaildomain.com\).

        This email address is used by requesters to send privacy requests that automatically generate as cases.


**Parent Topic:**[Configuring Privacy Case Management](../concept/configuring-privacy-case-management.md)

