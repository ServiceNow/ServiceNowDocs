---
title: Meeting recap
description: When a meeting is completed, the meeting page displays a recap of the meeting, including an AI-generated summary, success tasks, and records associated with the meeting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-meeting-post.html
release: brazil
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 3
breadcrumb: [Meeting page, Touchpoints, Customer success, Use, Customer Success Management]
---

# Meeting recap

When a meeting is completed, the meeting page displays a recap of the meeting, including an AI-generated summary, success tasks, and records associated with the meeting.

When a meeting transitions to **Completed** state, the meeting page displays the **Meeting Recap** section. A banner indicates when post-meeting materials are ready for review.

## Meeting Recap tabs

The Meeting Recap section contains three tabs.

-   **Meeting Summary**

    Displays the AI-generated summary of the completed meeting. It includes an overview of the meeting, a brief summary, risks, issues, and next steps. It provides a summary of recent account interactions and key discussion topics to help you prepare for the conversation. The guide content is stored in the **Post meeting review** field in the **Meeting** table.You can do the following:

    -   If the summary is long, select **Show more** to expand it. Select **View** to open the full guide.
    -   To edit the guide, select **Refine** to modify tone, length, and audience.
    -   To share the guide by email, select **Draft email**. An email composer opens with the summary content, a subject line, and opening and closing lines. The email is addressed to the first meeting participant other than you. If there are no other participants, the email is addressed to you, and you add the recipients.
-   **Agenda**

    Displays the meeting agenda as it was set before the meeting. The agenda content is read from the Agenda field on the meeting record.

-   **Prep Brief**

    Displays the meeting preparation guide that was generated before the meeting. The brief includes the meeting objective, a recap of the last meeting, and the timestamp when it was generated. This is the same guide that was available on the **Meeting prep guide** tab in the [Meeting preparation brief](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-pre.md) page.


## Success Tasks

The Success tasks list displays tasks associated with the meeting.You can generate draft task descriptions automatically using the next step task description skill. Use the **Show AI draft tasks** toggle to view AI-drafted tasks that have not yet been added. Select one or more draft tasks and **Add AI drafts** to add all drafted tasks at once, or select **New** to create a task manually. You can **Edit** or **Delete** a task and select the \[Omitted image "open-link-right-outline-24.svg"\] Alt text: to navigate to the Meeting details page.

After you delete a task, a banner with **Undo** appears at the top of the page. Select **Undo** to restore the task. If the task can't be deleted, an error banner appears.

## Related Record

The Related Record section lists records associated with the meeting. Records are stored in the Meeting Applicable Records table. Use the filter tabs to view records by association type.

-   **Trigger**

    Records that triggered the creation of the meeting.

-   **Reference**

    Records referenced during the meeting, such as risk signals or incidents.

-   **Action Item**

    Records created as action items from the meeting, such as success plays.

    Records that you link when you convert a meeting next step also appear here. See [Convert a next step to an associated record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-convert-next-step.md).


Select **Add record** to associate an additional record with the meeting. Select **View record** to open a listed record.

After you remove a record from the meeting, a banner with **Undo** appears. Select **Undo** to restore the record. If you dismiss a recommended record, a banner with **Undo** also appears. If the removed record has no association type, the banner has no **Undo** option.

**Parent Topic:**[Meeting page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-page.md)

**Related topics**  


[Meeting page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-page.md)

[Meeting preparation brief](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-pre.md)

[Use touchpoint meeting skills in ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/now-assist-tmt-meeting-skills.md)

[Meeting agenda items and next steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-scheduler-plus.md)

