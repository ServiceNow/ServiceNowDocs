---
title: Report a privacy case through email
description: Identify and manage issues related to the impacted areas for the reported privacy case. You can also create issues from the Privacy Case Management landing page.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Report a privacy case, Use, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Report a privacy case through email

Identify and manage issues related to the impacted areas for the reported privacy case. You can also create issues from the Privacy Case Management landing page.

## Before you begin

Role required: N/A

You must know:

-   The email address designated for reporting privacy incident \(for example privacy@company.com\).
-   The instance email ID for your ServiceNow environment \(for example, &lt;instancename&gt;@service-now.com\).

## Procedure

1.  Compose the email in Outlook.

    1.  In the To field, enter the designated privacy request email address and the instance email ID.

        The instance name should be in the format: &lt;instancename&gt;@service-now.com

    2.  Add recipients in CC if you want them added to the case watchlist.

2.  Use Outlook’s Importance setting to mark the priority \(for example, High or Low\).

    This priority will map to the Priority field in the created case.

3.  Add email Content

    1.  In the Subject, provide a clear subject line that will help classify the case easily.

    2.  In the Body, include the information about the privacy incident.

4.  Add any relevant attachments.

    Attachments are stored in the case record for reference.

5.  Select **Send**.


## Result

The email triggers an inbound email action in the Privacy Management application and creates a privacy case.

Field mapping after email submission:

-   Subject → Title field

    The subject in the email is automatically captured in the Title field of the privacy case.

-   Body Content → Description field in the case

    The text in the email body is automatically captured in the Description field of the privacy case.

-   Importance → Priority field

    The importance level set in the email \(for example, High\) is mapped to the Priority field in the case.

-   Source → Email

    The source of the case is recorded as Email, indicating that the case was created from an inbound email.

-   Sender → Requester field

    The email sender’s name is added as the Requester in the case.

-   CC Recipients → Watchlist

    Any recipients included in the CC field of the email are added to the case Watchlist, allowing them to receive updates.


For privacy admin, the case will be visible in **Workspaces** &gt; **Privacy Workspace** &gt; **List** &gt; **Cases** &gt; **Unassigned cases**.

Any reply sent by the admin appears in the Email tab of the privacy case.

**Parent Topic:**[Reporting a privacy case](../concept/reporting-a-privacy-case.md)

