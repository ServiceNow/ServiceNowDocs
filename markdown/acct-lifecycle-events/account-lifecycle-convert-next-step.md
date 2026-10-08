---
title: Convert a next step to an associated record
description: Convert a next step by linking it to the record that addresses the follow-up, so the record appears as an action item of the meeting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-convert-next-step.html
release: brazil
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [convert next step, meeting next step, action item, meeting applicable records]
breadcrumb: [Meeting agenda items and next steps, Touchpoints, Customer success, Use, Customer Success Management]
---

# Convert a next step to an associated record

Convert a next step by linking it to the record that addresses the follow-up, so the record appears as an action item of the meeting.

## Before you begin

-   The record that addresses the follow-up, such as a success task or an internal play, must already exist.
-   Role required: sn\_sch\_plus.next\_step\_write

## About this task

Convert a next step when a record already exists that addresses the follow-up. For background, see [Meeting agenda items and next steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-scheduler-plus.md).

## Procedure

1.  Open the next step.

    Navigate to **All** &gt; **Touchpoint Meeting** &gt; **Meeting Next Steps** and select the next step, or open it from the **Meeting Next Steps** related list in the **Related Items** panel on the meeting page.

2.  Select **Convert**.

    The **Convert** button isn't available if the next step is already converted.

3.  In the **Associated table** field, select the table that contains the record.

4.  In the **Associated record** field, select the record.

    The dialog fills in the next step and the meeting. The association type is always **Action Item**.

5.  Select **Submit**.

    The state of the next step changes to **Converted**. The record you selected appears in the **Meeting Applicable Records** for the meeting with the association type **Action Item**.

    The record also appears in the **Meeting Applicable Records** related list on the meeting record, in the classic UI and in the CRM Workspace.


## What to do next

You can convert a dropped next step. The state changes from **Dropped** to **Converted**.

**Parent Topic:**[Meeting agenda items and next steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-scheduler-plus.md)

**Related topics**  


[Meeting agenda items and next steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-scheduler-plus.md)

[Drop a next step](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-drop-next-step.md)

[Meeting recap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-post.md)

