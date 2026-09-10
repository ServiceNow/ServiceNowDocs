---
title: Creating collaborations in exercises and crisis events
description: Starting with BCM core release 12.x.x, crisis managers can create collaboration threads on crisis events to coordinate responses with recovery teams and send email updates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/creating-collaboration-threads-in-crisis.html
release: zurich
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Structured workflows for crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Creating collaborations in exercises and crisis events

Starting with BCM core release 12.x.x, crisis managers can create collaboration threads on crisis events to coordinate responses with recovery teams and send email updates.

## Collaboration threads overview

A collaboration thread groups the recovery teams, impacted assets, and email communication for a specific coordination effort on a crisis event. Each collaboration thread belongs to exactly one crisis event and is deleted if that crisis event is deleted. A collaboration thread cannot be deleted on its own; set its **State** field to close it instead.

Collaborations details are displayed in the **Collaboration threads** related list on the crisis event record, as shown in the example.

\[Omitted image "cm-collab-tab-email.png"\] Alt text: Collaborations related list on a crisis event record with number, name, recovery teams, impacted assets, updated, and state columns.

A collaboration thread includes the following details in columns:

-   Number
-   Name
-   Recovery teams
-   Impacted assets
-   Updated
-   State with a value of Open or Closed

For descriptions of these fields, see [Create Collaboration thread form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-collaboration-thread-crisis-event-form.md).

Collaboration threads centralize crisis response coordination, replacing scattered emails and spreadsheets with a single record of decisions, actions, and communications. Automatic recovery-team notifications and activity-stream propagation keep responders informed in real time and preserve a complete audit trail for post-event analysis and compliance reporting.

## Action items, emails, attachments, and activity on a collaboration thread

A collaboration thread record groups its related information under the **Action items**, **Emails**, and **Email Attachments** tabs, as shown in the example.

\[Omitted image "cm-related-tables-for-collaborations.png"\] Alt text: Collaboration thread record with Details, Action items, Emails, and Email Attachments tabs.

Use the **Action items** tab to track follow-up tasks assigned during the coordination effort, with ownership and status for each item.

On the **Emails** tab, the emails sent from a collaboration thread are listed. Files attached to it are listed in its **Email Attachments** tab. Both tabs are read-only: an email appears in the **Emails** tab only after it is sent from the thread, and you can't add or remove entries directly in either tab.

Saving a collaboration thread sends an automatic notification email to the members of the recovery teams selected on the thread. The email notifies them that a new thread was opened and links back to it. This system-generated email is separate from any email you send afterward with **Compose email**, and it also appears in the **Emails** tab.

Field changes, emails, and attachments on a collaboration thread are added to its parent crisis event's activity feed for review, as shown in the example.

\[Omitted image "cm-event-record-activity-stream.png"\] Alt text: Crisis event Details tab with an activity feed listing field changes and updates.

## Roles associated with collaboration threads

Users with the sn\_recovery.event\_manager or sn\_recovery.event\_user role can create and update collaboration threads, including their State and work notes. Users with the sn\_recovery.event\_viewer role can read collaboration threads, including their work notes.

-   **[Create a collaboration thread in a crisis event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/compose-email-collaboration-thread-crisis.md)**  
Create a collaboration thread on a crisis event and send an email to its recovery teams to coordinate a response.

**Parent Topic:**[Structured workflows for crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/perform-tasks-to-manage-crisis-events.md)

