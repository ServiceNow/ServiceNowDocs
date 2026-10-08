---
title: Create touchpoints and meeting records using ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)
description: Send an email to your instance to create touchpoint and meeting records directly from the inbound email.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/now-assist-tmt-email-template.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Touchpoints, Customer success, Use, Customer Success Management]
---

# Create touchpoints and meeting records using ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)

Send an email to your instance to create touchpoint and meeting records directly from the inbound email.

## Before you begin

Role required: Success agent

To enable email sending, see [Outbound email configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_OutboundMailConfiguration.md). To enable email receiving, see [Inbound email configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_InboundMailConfiguration.md).

## Procedure

1.  Launch the email application.

2.  Select **New Email**.

    The new email must contain the following:

    |Field|Description|
    |-----|-----------|
    |From|Email address of the sender.|
    |To|Email address of the instance \(*instancename*@service-now.com\). For example: devgen@service-now.com.|
    |Subject|Must start with the prefix "Touchpoint:". For example: "Touchpoint: Create a touchpoint for test."|
    |Email message|For touchpoints, must include: Engagement number, Due date, Subject, Description. For meetings, must include: Source, Start date and time, End date and time, Meeting subject.|

3.  Select **Send**.

    **Note:** The instance may take several seconds to receive the email.


## Result

-   The instance validates the email using Inbound Email Actions.
-   If validation fails, you receive an email with the validation error and template description.
-   If validation passes, a record is created and you receive a success email with a link to the created record.
-   Emails are prepared and pushed to the outbound queue, where they're scheduled to be sent.

**Parent Topic:**[Touchpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-use-touchpoints.md)

