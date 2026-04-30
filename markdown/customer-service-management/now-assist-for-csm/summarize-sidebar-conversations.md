---
title: Summarize a Sidebar discussion by using Now Assist for Customer Service Management \(CSM\)
description: Generate a summary of the Sidebar discussions between agents, requesters, and subject matter experts by using the chat summarization skill in the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
release: xanadu
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Now Assist for Customer Service Management \(CSM\), Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Summarize a Sidebar discussion by using Now Assist for Customer Service Management \(CSM\)

Generate a summary of the Sidebar discussions between agents, requesters, and subject matter experts by using the chat summarization skill in the Now Assist for Customer Service Management \(CSM\) application.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

You can do these actions by using Sidebar discussion summarization:

-   Summarize the Sidebar discussion at any point during the discussion using the `/Summarize` quick action.
-   Share the Sidebar discussion to the work notes.
-   Provide feedback for the summary.

**Note:** The Sidebar discussion summarization skill is on the chat skill card in the Customer group. For more information, see [Sidebar discussion summarization](https://www.servicenow.com/docs/access?context=now-assist-sidebar-discussion-summarization&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and open a customer service case that supports Sidebar discussion and summarization.

2.  Choose an existing discussion, or start a new discussion.

    Start a new discussion by doing these actions:

    1.  Select **Discuss**.

    2.  In the Start a Sidebar discussion modal, add participants.

    3.  Select **Start Discussion**.

    ![Modal to add participants for discussion.](../image/now-assist-sidebar-discussion.png "Sidebar discussion modal")

3.  Generate a summary of the Sidebar discussion during the conversation either by using the Summarize quick action \(enter `/Summarize` in the Active sidebar discussion window\), or by selecting the quick action icon ![Quick action icon.](../image/now-assist-sidebar-lightning-bolt-icon.png).

4.  After summarizing the Sidebar discussion, you can add it to the case work notes, and provide feedback about it.

<table id="choicetable_vzl_myv_bcc"><thead><tr><th align="left" id="d32475e210">

Option

</th><th align="left" id="d32475e213">

Procedure

</th></tr></thead><tbody><tr><td id="d32475e219">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share Case summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d32475e246">

**Provide feedback for the summary**

</td><td>

If you'd like to provide feedback, select either the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\) or the not helpful icon ![Not helpful icon.](../image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](../concept/now-assist-csm-using.md)

