---
title: Review source record changes in a DRIR case
description: When the linked incident changes, review the modifications in your DRIR case or in the email notification to stay current with incident updates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/review-source-record-changes.html
release: australia
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 2
keywords: [review changes, source record, DRIR case, incident changes, field changes]
breadcrumb: [Source record change notifications, Reporting incidents from SOW and SIR Workspace in DRIR, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Review source record changes in a DRIR case

When the linked incident changes, review the modifications in your DRIR case or in the email notification to stay current with incident updates.

## Before you begin

Role required: sn\_dri\_inc\_rptg.digital\_resilience\_incident\_manager

Before you begin:

-   You must have access to the DRIR case record.
-   The case must have a linked source incident record.
-   The source incident must have been modified since the case was created.

## About this task

Use this procedure when you receive a notification that a source record has changed. Reviewing the changes helps you stay current with the incident and maintain accurate reporting data for regulatory timelines.

## Procedure

1.  Open the DRIR case record.

    If the linked source incident has been modified, a blue banner appears at the top of the case.

2.  Review the notification banner.

    The banner displays: `"The linked source record has been updated. Review the latest changes."`

    **Note:** The banner prompts you to review changes before continuing your work on the case.

3.  Navigate to the Activity section of the DRIR case and select the **Activity** tab.

    The Activity section displays a log of changes to the case and linked records. You can review the entries that show **Field changes** with a timestamp matching when the source incident was modified.

4.  Review the field change details.

    The Activity log shows the following details for each changed field:

    -   Name of the field that changed \(for example, state, impact, urgency\)
    -   Old value
    -   New value
    -   Who made the change
    -   When the change occurred \(date and time\)
    **Note:**

    The Activity section reflects the actual changes made to the source record, keeping your case record synchronized with the current incident state.

5.  Review the email notification \(if received\).

    If you are on the case watch list or assigned as the analyst, you receive an email when the source record changes. The email subject line reads: `"DRIR Case [case number]: Source Record Updated"`

    The email body contains the details:

    -   A statement: "The source record linked to your DRIR case has been updated."
    -   DRIR case number
    -   Source record number \(for example, incident number\)
    -   Timestamp and user who made the changes
    -   A list of all changed fields with old and new values
    -   A direct link labeled **View Case** to open the DRIR case
    **Note:**

    The email also includes links to unsubscribe from notifications and to manage your notification preferences.

6.  Update your case data as needed.

    After reviewing the source record changes, update your DRIR case record to reflect the new incident data. This helps maintain alignment with the incident and supports meeting your regulatory reporting timelines.

    **Note:**

    Confirm with your administrator which case fields require updating based on source incident changes.

7.  Return to the source record if necessary.

    To investigate the changes in detail, select the source record link in the Activity section or in the email notification to open the source incident directly.


## Result

You have reviewed the source record changes and understood what was modified in the linked incident. By keeping your case current with these changes, you maintain accurate data for regulatory reporting and stay aligned with incident updates.

