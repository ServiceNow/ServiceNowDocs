---
title: Summarize a Sidebar discussion
description: Generate a summary of the Sidebar discussions between agents, dispatchers, and subject matter experts by using the Sidebar summarization skill in the Now Assist for Field Service Management \(FSM\) application.On the ServiceNow Agent application, generate a summary of the Sidebar discussions between agents, dispatchers, and subject matter experts by using the Sidebar summarization skill in the Now Assist for Field Service Management \(FSM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/now-assist-for-field-service-management-fsm/na-fsm-summarize-sidebar-platform.html
release: zurich
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Now Assist for FSM]
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

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

2.  Expand the **Customer** panel and select **FSM**.

3.  Select **Activate skill** on the **Sidebar summarization** skill card.

    The **Work Order Task** table displayed in the **Choose tables** page is selected by default, and cannot be changed.

4.  Select **Select display** in the **Sidebar summarization** page.

5.  Turn on the **In-product desktop** display option.

6.  Select **Save and continue**.

7.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and open a work order task that supports Sidebar discussion and summarization.

8.  Choose an existing discussion, or start a new discussion.

    To start a new discussion, follow these steps.

    1.  Select **Discuss**.

    2.  Add participants in the **Start a Sidebar discussion** modal.

    3.  Select **Start Discussion**.

    \[Omitted image "now-assist-sidebar-discussion.png"\] Alt text: Modal to add participants for discussion

9.  Generate a summary of the Sidebar discussion during the conversation either by using the Summarize quick action \(enter `/Summarize` in the Active sidebar discussion window\), or by selecting the quick action icon \(\[Omitted image "now-assist-sidebar-lightning-bolt-icon.png"\] Alt text: icon image\).

10. After summarizing the Sidebar discussion, you can add it to the work notes, and provide feedback about it.

<table id="choicetable_vzl_myv_bcc"><thead><tr><th align="left" id="d81045e284">

Option

</th><th align="left" id="d81045e287">

Procedure

</th></tr></thead><tbody><tr><td id="d81045e293">

**Save the summary information by adding it to the work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d81045e320">

**Provide feedback for the summary**

</td><td>

If you'd like to provide feedback, select either the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\) or the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/now-assist-for-field-service-management-fsm/using-now-assist-fsm.md)

## Summarize a Sidebar discussion on the ServiceNow Agent application

On the ServiceNow Agent application, generate a summary of the Sidebar discussions between agents, dispatchers, and subject matter experts by using the Sidebar summarization skill in the Now Assist for Field Service Management \(FSM\) application.

### Before you begin

Role required: wm\_agent

Ensure the Sidebar for Field Service Management plugin \(com.sn\_fsm\_sidebar\) is activated. For more information, see [Activate Sidebar for the Field Service Mobile Agent application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/mobile-experience-for-field-service-management-glide-family/activate-sidebar-mobile.md).

### About this task

Summarize the Sidebar discussion at any point during the discussion using the /Summarize quick action.

### Procedure

1.  Navigate to a Sidebar discussion.

    -   To view discussions for a specific work order task, navigate to the work order task and select the **Record Sidebar** \(\[Omitted image "icon-sidebar-record-mobile.png"\] Alt text: Record Sidebar icon.\) icon.
    -   To view all discussions, select the **Global Sidebar** \(\[Omitted image "icon-sidebar-global-mobile.png"\] Alt text: Global Sidebar\) icon.
2.  Tap a discussion.

3.  Generate a summary of the Sidebar discussion during the conversation either by using the Summarize quick action \(enter `/Summarize` in the Active sidebar discussion window\), or by selecting the quick action icon \(\[Omitted image "now-assist-sidebar-lightning-bolt-icon.png"\] Alt text: quick action\).


