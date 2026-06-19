---
title: Report a compliance case through email
description: Report a compliance issue by sending an email to your organization's compliance mailbox. This creates a compliance case automatically in Compliance Case Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/compliance-case-management/report-comp-case-email.html
release: australia
product: Compliance Case Management
classification: compliance-case-management
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Report compliance case, Use, Compliance Case Management, Governance, Risk, and Compliance]
---

# Report a compliance case through email

Report a compliance issue by sending an email to your organization's compliance mailbox. This creates a compliance case automatically in Compliance Case Management.

## Before you begin

Role required: none

You must know:

-   The email address designated for reporting a compliance incident \(for example compliance@company.com\).
-   The instance email ID for your ServiceNow environment \(for example, &lt;instancename&gt;@service-now.com\).

## Procedure

1.  Compose the email on Outlook.

    1.  In the To field, enter the designated compliance request email address and the instance email ID.

        The instance name should be in the format: &lt;instancename&gt;@service-now.com

    2.  Add recipients in CC if you want them added to the case watchlist.

2.  Use Outlook’s **Importance** setting to mark the priority \(for example, High or Low\).

    This priority will map to the Priority field in the created case.

3.  Add email content.

    1.  In the Subject, provide a clear subject line that will help classify the case easily.

    2.  In the Body, include information about the compliance incident.

4.  Add any relevant attachments.

    Attachments are stored in the case record for reference.

5.  Select **Send**.


## Result

The email triggers an inbound email action in the Compliance Case Management application and creates a compliance case.

Field mapping after email submission:

-   Subject → Title field

    The subject in the email is automatically captured in the Title field of the compliance case.

-   Body Content → Description field in the case

    The text in the email body is automatically captured in the Description field of the compliance case.

-   Importance → Priority field

    The importance level set in the email \(for example, High\) is mapped to the Priority field in the case.

-   Source → Email

    The source of the case is recorded as Email, indicating that the case was created from an inbound email.

-   CC Recipients → Watchlist

    Any recipients included in the CC field of the email are added to the case watchlist, allowing them to receive updates.


For a compliance admin, the case will be visible in **Compliance workspace** &gt; **List** &gt; **Cases** &gt; **Unassigned cases**.

Any reply sent by the admin appears in the Email related list of the compliance case.

**Parent Topic:**[Reporting a compliance case in GRC: Compliance Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/compliance-case-management/reporting-compliance-case.md)

