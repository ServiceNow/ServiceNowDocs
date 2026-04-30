---
title: Summarize a Sidebar discussion
description: Generate a summary of the Sidebar discussions between agents, dispatchers, and subject matter experts by using the Sidebar summarization skill in the Now Assist for Field Service Management \(FSM\) application.On the Mobile Agent application, generate a summary of the Sidebar discussions between agents, dispatchers, and subject matter experts by using the Sidebar summarization skill in the Now Assist for Field Service Management \(FSM\) application.
locale: en-US
release: yokohama
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for Field Service Management \(FSM\), Now Assist for Field Service Management \(FSM\)]
---

# Summarize a Sidebar discussion

Generate a summary of the Sidebar discussions between agents, dispatchers, and subject matter experts by using the Sidebar summarization skill in the Now Assist for Field Service Management \(FSM\) application.

## Before you begin

Role required: wm\_dispatcher, wm\_manager

## About this task

You can do these actions using Sidebar summarization:

-   Summarize the Sidebar discussion at any point during the discussion using the /Summarize quick action.
-   Share the Sidebar discussion to the work notes.
-   Provide feedback for the summary.

**Note:** The Sidebar discussion summarization skill is on the chat skill card in the Customer group.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and open a work order task that supports Sidebar discussion and summarization.

2.  Choose an existing discussion, or start a new discussion.

    To start a new discussion, follow these steps.

    1.  Select **Discuss**.

    2.  Add participants in the **Start a Sidebar discussion** modal.

    3.  Select **Start Discussion**.

    ![Modal to add participants for discussion](../../customer-service-management/image/now-assist-sidebar-discussion.png "Sidebar discussion modal")

3.  Generate a summary of the Sidebar discussion during the conversation either by using the Summarize quick action \(enter `/Summarize` in the Active sidebar discussion window\), or by selecting the quick action icon \(![icon image](../../customer-service-management/image/now-assist-sidebar-lightning-bolt-icon.png)\).

4.  After summarizing the Sidebar discussion, you can add it to the work notes, and provide feedback about it.

<table id="choicetable_vzl_myv_bcc"><thead><tr><th align="left" id="d84190e202">

Option

</th><th align="left" id="d84190e205">

Procedure

</th></tr></thead><tbody><tr><td id="d84190e211">

**Save the summary information by adding it to the work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d84190e238">

**Provide feedback for the summary**

</td><td>

If you'd like to provide feedback, select either the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\) or the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Field Service Management \(FSM\)](../concept/using-now-assist-fsm.md)

## Summarize a Sidebar discussion on the Now Mobile Agent application

On the Mobile Agent application, generate a summary of the Sidebar discussions between agents, dispatchers, and subject matter experts by using the Sidebar summarization skill in the Now Assist for Field Service Management \(FSM\) application.

### Before you begin

Role required: wm\_agent

Ensure the Sidebar for Field Service Management plugin \(com.sn\_fsm\_sidebar\) is activated. For more information, see [Activate Sidebar for the Field Service Mobile Agent application](activate-sidebar-mobile.md).

### About this task

Summarize the Sidebar discussion at any point during the discussion using the /Summarize quick action.

### Procedure

1.  Navigate to a Sidebar discussion.

    -   To view discussions for a specific work order task, navigate to the work order task and select the **Record Sidebar** \(![Record Sidebar icon.](../image/icon-sidebar-record-mobile.png)\) icon.
    -   To view all discussions, select the **Global Sidebar** \(![Global Sidebar](../image/icon-sidebar-global-mobile.png)\) icon.
2.  Tap a discussion.

3.  Generate a summary of the Sidebar discussion during the conversation either by using the Summarize quick action \(enter `/Summarize` in the Active sidebar discussion window\), or by selecting the quick action icon \(![quick action](../../customer-service-management/image/now-assist-sidebar-lightning-bolt-icon.png)\).


