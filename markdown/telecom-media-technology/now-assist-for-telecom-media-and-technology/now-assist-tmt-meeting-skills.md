---
title: Use touchpoint meeting skills
description: Use the ServiceNow Otto for TMT skills to generate a meeting preparation guide and AI-generated participant insights for touchpoint meetings in the CSM/FSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-meeting-skills.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# Use touchpoint meeting skills

Use the ServiceNow Otto for TMT skills to generate a meeting preparation guide and AI-generated participant insights for touchpoint meetings in the CSM/FSM Configurable Workspace.

## Before you begin

Role required: `sn_acct_lc.customer_success_agent`

## About this task

-   **Prep Brief Data Generator**

    Generates the meeting preparation guide displayed on the **Meeting insights** tab in the **Meeting preparation brief** section on the meeting page. The guide provides a summary of recent account interactions and key discussion topics to help customer success managers prepare for the meeting. The guide is generated automatically before a scheduled meeting and can also be generated on demand from the meeting page.

-   **Transcript Analysis**

    Processes meeting transcript chunks from completed meetings to generate participant insights. The resulting insights are displayed on the **Participant AI insights** tab in the **Meeting preparation brief** section for subsequent meetings. Insights include each participant's main focus areas, communication style, and attendance history. The **Process transcript** field \(`process_transcript`\) on the meeting record controls whether transcript processing runs for a given meeting.

-   **Next Step Task Description**

    Generates the description and short description for success tasks recommended after a meeting. The drafted tasks are displayed in the **Success tasks** list on the meeting page when the meeting is completed. Use the **Show AI draft tasks** toggle to view tasks that the skill has drafted, then select **Add AI drafts** to add them.


## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **All Touchpoints**.

2.  Open a touchpoint and select the meeting you want to prepare for from the **Meetings** tab.

3.  On the meeting page, select the **Meeting prep guide** tab in the **Pre meeting artifacts** section.

4.  If the prep guide has not been generated yet, select **Create** to generate it on demand.

    A loading indicator appears while the guide is being generated. If generation fails, select **Retry**.

5.  Select **View** to open the full preparation guide.

    If the guide content is long, select **Show more** to expand it inline.

6.  To modify the guide, select **Refine** and choose an option from the dropdown.

    Refine options include tone, length, and audience. Selecting an option regenerates the guide according to the chosen adjustment.

7.  To share the guide by email, select **Draft Email**.

    An email composer opens pre-populated with the guide content. Edit the email as required before sending it.

8.  To view participant insights, select the **Participant AI insights** tab.

    Each participant is displayed as a card showing their main focus areas, communication style, and attendance history. Select **Show more** on a card to expand additional detail.

9.  After the meeting is completed, view AI-drafted success tasks by enabling the **Show AI draft tasks** toggle in the **Success tasks** list.

    Select **Add AI drafts** to add all drafted tasks at once, or select **New** to create a task manually.


**Parent Topic:**[Using ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spm-using.md)

