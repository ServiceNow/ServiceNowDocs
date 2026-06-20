---
title: Summarize a Sidebar discussion by using Now Assist for IT Service Management \(ITSM\)
description: Generate a summary of Sidebar discussions between agents, requesters, and subject matter experts by using the Sidebar discussion summarization skill in the Now Assist for IT Service Management \(ITSM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-sidebar-discussion.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Summarize a Sidebar discussion by using Now Assist for IT Service Management \(ITSM\)

Generate a summary of Sidebar discussions between agents, requesters, and subject matter experts by using the Sidebar discussion summarization skill in the Now Assist for IT Service Management \(ITSM\) application.

## Before you begin

-   Next Experience must be enabled to summarize Sidebar discussions in Core UI. For more information, see .
-   The Sidebar Chat Summarization skill must be enabled. For more information, see .

Role required: itil

## About this task

You can do these actions by using the Sidebar discussion summarization skill:

-   Summarize the Sidebar discussion at any point during the discussion.
-   Share the Sidebar discussion to the work notes.
-   Provide feedback for the summary.

**Note:** The Sidebar discussion summarization skill is on the Chat skill card in the Technology group.

You can use Sidebar discussion summarization for any task table that you have enabled Sidebar on.

Summarizing Sidebar chats integrated with Microsoft Teams is supported. For more information, see .

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** and open an incident that supports Sidebar discussion and summarization.

2.  Choose an existing discussion, or start a new discussion.

3.  Generate a summary of the Sidebar discussion during the conversation either by either entering `/Summarize` in the Active Sidebar discussion window, or by selecting the quick action icon \[Omitted image "now-assist-sidebar-lightning-bolt-icon.png"\] Alt text: Quick action icon. and selecting **Summarize**.

    \[Omitted image "now-assist-itsm-sidebar-discuss.png"\] Alt text: Sidebar discussion summarization.

    The Sidebar discussion summary appears in the Discussion that is summarized by the Now Assist modal.

4.  Add the summary to the incident work notes, and provide feedback about it.

<table id="choicetable_oz1_rtx_1cc"><thead><tr><th align="left" id="d420945e250">

Option

</th><th align="left" id="d420945e253">

Procedure

</th></tr></thead><tbody><tr><td id="d420945e259">

**Save the summary information by adding it to the incident work notes**

</td><td>

1.  Select **Share to Work notes**.
2.  In the Share Incident summary as Work notes dialog box, edit the summary, if needed.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d420945e286">

**Provide feedback for the summary**

</td><td>

If you'd like to provide feedback, select either the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\), or the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\)

 This feedback improves the generative AI model and can help to improve future versions of this skill.

 The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
