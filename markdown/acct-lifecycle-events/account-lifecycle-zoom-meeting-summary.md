---
title: Generate summary for Zoom meetings
description: Generate the meeting summary for virtual meetings conducted using Zoom.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up Zoom and touchpoint integration, Touchpoint home page, Customer success, Use, Customer Success Management]
---

# Generate summary for Zoom meetings

Generate the meeting summary for virtual meetings conducted using Zoom.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_application\_admin

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Navigate to **Customer Success** &gt; **All Touchpoints**.

3.  Open the touchpoint for which you want to create a virtual meeting.

4.  Follow the steps described in the [Meetings](../concept/account-lifecycle-touchpoint-home.md#section_u4k_m1h_rdc) section to schedule a Zoom meeting.

    The meeting summary can be generated only if the meeting State is set to **Scheduled**.

5.  When the meeting starts, select **AI Companion** to start creating the meeting summary.

    The meeting summary is captured and saved in the Virtual Meeting Details table.

    **Note:**

    -   A meeting summary is generated for each scheduled meeting.
    -   -   If a meeting occurs between the scheduled start and end date, the summary is captured separately for that meeting.
-   If a meeting occurs outside the scheduled date and time window, the meeting details are captured in the parent record.
    -   For recurring meetings, the summaries for all occurrences are grouped under the parent record.
    -   The Virtual Meeting Details record contains each child meeting summary.
6.  To view the summary, navigate to **All** &gt; **Touchpoints** &gt; **Meetings** &gt; **All**.

7.  Select the **Number** link to open the Meeting Details page and navigate to the Meeting Summary related list.

    **Note:** If you select a parent record, you see a list of meeting summaries of all the child records.

8.  Select the **Meeting actual start date** link.

    The meeting summary is displayed in the Virtual Meeting Details page. If the Now Assist for Telecommunications, Media and Technology \(TMT\) plugin has been installed, the following fields are populated in the meeting record:

    -   Sentiment
    -   Internal notes
    -   External notes

**Parent Topic:**[Configure Zoom to create a touchpoint meeting summary](account-lifecycle-config-zoom-sum.md)

