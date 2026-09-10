---
title: Source record change notifications
description: When the incident linked to your Digital resilience incident reporting \(DRIR\) case changes, you receive a notification in the case record and an email alert. You can then review the latest updates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/source-record-change-notifications.html
release: australia
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 2
keywords: [source record, notifications, DRIR case, incident changes, email notification]
breadcrumb: [Reporting incidents from SOW and SIR Workspace in DRIR, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Source record change notifications

When the incident linked to your Digital resilience incident reporting \(DRIR\) case changes, you receive a notification in the case record and an email alert. You can then review the latest updates.

## Source record changes

Starting with Digital resilience incident reporting version 23.x.x, the Digital resilience incident reporting \(DRIR\) application detects modifications to the incident linked to your DRIR case. When field-level changes occur on that source incident, you receive notifications to keep your case current with the latest incident data.

This feature tracks changes to critical fields such as state, impact, and urgency. Each time the source incident is modified, the system generates audit-trail records with complete information about the changes. These records include field names, old and new values, who made the change, and when.

## Importance of email notifications

Previously, when a source incident changed, the DRIR case did not automatically reflect the current state of that incident. It required manual updates to keep cases synchronized. These notifications introduced with version 23.x.x help you meet critical regulatory reporting timelines:

\[Omitted image "drir-case-src-record.png"\] Alt text: Source record.

-   Initial report: 24 hours from incident classification
-   Intermediate report: 72 hours from incident classification
-   Final report: 1 month from incident classification

By reviewing source record changes promptly, you can update your case data without requiring manual re-checks, which supports staying on track with these timelines.

## How notifications work

You receive notifications through two channels:

-   **Email notification**

    An email notification is sent to members of the case watch list and the assigned analyst whenever a tracked field changes on the linked source record.

    \[Omitted image "drir-src-record-updated-noti.png"\] Alt text: Email notifications.\[Omitted image "drir-email-preview-src-record.png"\] Alt text: Preview email.

-   **Contents of the email**

    -   A statement that the source record has been updated
    -   The DRIR case number
    -   The source record number \(for example, the incident number\)
    -   Who made the change and the timestamp
    -   The names of fields that changed, with old and new values for each
    -   A direct link to the DRIR case
    **Note:**

    Email delivery depends on your instance having a mail protocol configured.


## Tracked fields on the form

Different fields on the linked source incident trigger notifications when changed, for example, State, Impact, Urgency.

**Note:**

Additional fields may be tracked depending on your DRIR configuration. Confirm the complete list of tracked fields with your administrator.

## Recipients of the notifications

Notifications are sent to:

-   Members added to the case watch list
-   Assigned analyst for the case

**Note:**

Confirm with your administrator which users in your organization receive notifications based on watch-list membership and assigned roles.

**Related topics**  


[Review source record changes in a DRIR case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/review-source-record-changes.md)

