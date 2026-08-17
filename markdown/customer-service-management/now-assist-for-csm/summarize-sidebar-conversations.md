---
title: Summarize a Sidebar discussion by using ServiceNow Otto for Customer Service Management \(CSM\)
description: Generate a summary of the Sidebar discussions between agents, requesters, and subject matter experts by using the chat summarization skill in the ServiceNow Otto for Customer Service Management \(CSM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/summarize-sidebar-conversations.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI skills, ServiceNow Otto for CSM, Customer Service Management]
---

# Summarize a Sidebar discussion by using ServiceNow Otto for Customer Service Management \(CSM\)

Generate a summary of the Sidebar discussions between agents, requesters, and subject matter experts by using the chat summarization skill in the ServiceNow Otto for Customer Service Management \(CSM\) application.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

You can do these actions by using Sidebar discussion summarization:

-   Summarize the Sidebar discussion at any point during the discussion using the `/Summarize` quick action.
-   Share the Sidebar discussion to the work notes.
-   Provide feedback for the summary.

**Note:** The Sidebar discussion summarization skill is on the chat skill card in the Customer group.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and open a customer service case that supports Sidebar discussion and summarization.

2.  Choose an existing discussion, or start a new discussion.

    Start a new discussion by doing these actions:

    1.  Select **Discuss**.

    2.  In the Start a Sidebar discussion modal, add participants.

    3.  Select **Start Discussion**.

3.  Generate a summary of the Sidebar discussion.

    -   Enter `/Summarize` in the Active sidebar discussion window.
    -   Select the quick action icon \[Omitted image "now-assist-sidebar-lightning-bolt-icon.png"\] Alt text: Quick action icon..
4.  After summarizing the Sidebar discussion, you can add it to the case work notes, and provide feedback about it.

<table id="choicetable_vzl_myv_bcc"><thead><tr><th align="left" id="d38596e207">

Option

</th><th align="left" id="d38596e210">

Procedure

</th></tr></thead><tbody><tr><td id="d38596e216">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share Case summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d38596e243">

**Provide feedback for the summary**

</td><td>

If you'd like to provide feedback, select either the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\) or the not helpful icon \[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

