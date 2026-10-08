---
title: Use touchpoint meeting skills in ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)
description: Use ServiceNow Otto for TMT skills to generate a meeting preparation guide and AI-generated participant insights for touchpoint meetings in the CRM Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/now-assist-tmt-meeting-skills.html
release: brazil
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 2
breadcrumb: [Meeting page, Touchpoints, Customer success, Use, Customer Success Management]
---

# Use touchpoint meeting skills in ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)

Use ServiceNow Otto for TMT skills to generate a meeting preparation guide and AI-generated participant insights for touchpoint meetings in the CRM Workspace.

## Before you begin

Role required: `sn_acct_lc.customer_success_agent`

## About this task

-   **Prep Brief Data Generator**

    Generates the meeting preparation guide displayed on the **Meeting insights** tab in the **Meeting preparation brief** section on the meeting page. The guide summarizes recent account interactions and key discussion topics. It's generated automatically before a scheduled meeting and can also be generated on demand from the meeting page.

-   **Transcript Analysis**

    Processes meeting transcript chunks from completed meetings to generate participant insights, displayed on the **Participant AI insights** tab for subsequent meetings. Insights include each participant's main focus areas, communication style, and attendance history. The **Process transcript** field on the meeting record controls whether transcript processing runs for a given meeting.

-   **Next Step Task Description**

    Generates the description and short description for success tasks recommended after a meeting, displayed in the **Success tasks** list on the meeting page. Use the **Show AI draft tasks** toggle to view drafted tasks, then select **Add AI drafts** to add them.


## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace** &gt; **Lists** &gt; **All Touchpoints**.

2.  Open a touchpoint and select the meeting you want to prepare for from the **Meetings** tab.

3.  On the meeting page, select the **Meeting prep guide** tab in the **Pre meeting artifacts** section.

4.  If the prep guide hasn't been generated yet, select **Create** to generate it on demand.

    A loading indicator appears while the guide is being generated. If generation fails, select **Retry**.

5.  Select **View** to open the full preparation guide.

    If the content is long, select **Show more** to expand it inline.

6.  To modify the guide, select **Refine** and choose an option \(tone, length, or audience\) from the dropdown.

7.  To share the guide by email, select **Draft Email**.

    An email composer opens with the guide content, a subject line, and opening and closing lines. The email is addressed to the first meeting participant, other than you, who is an internal user. If no other participant qualifies, the email is addressed to you, and you add the recipients. Edit the email as required before sending it.

8.  To view participant insights, select the **Participant AI insights** tab.

    Each participant is displayed as a card showing their main focus areas, communication style, and attendance history. Select **Show more** on a card to expand additional detail.

9.  After the meeting is completed, view AI-drafted success tasks by enabling the **Show AI draft tasks** toggle in the **Success tasks** list.

    Select **Add AI drafts** to add all drafted tasks at once, or select **New** to create a task manually.


**Parent Topic:**[Meeting page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-page.md)

