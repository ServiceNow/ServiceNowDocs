---
title: Summarize a Sidebar discussion by using Now Assist for HRSD
description: Generate a summary of the Sidebar discussions between agents, requesters, and subject matter experts by using the chat summarization skill in the Now Assist for HR Service Delivery \(HRSD\) application.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use generative AI skills, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Summarize a Sidebar discussion by using Now Assist for HRSD

Generate a summary of the Sidebar discussions between agents, requesters, and subject matter experts by using the chat summarization skill in the Now Assist for HR Service Delivery \(HRSD\) application.

## Before you begin

Role required: sn\_hr\_core.case\_writer

## About this task

You can do these actions by using Sidebar discussion summarization:

-   Summarize the Sidebar discussion at any point during the discussion using the `/Summarize` quick action.
-   Share the Sidebar discussion to the work notes.
-   Provide feedback for the summary.

**Note:** The Sidebar discussion summarization skill can be found in the **HRSD** tab under the **Employee** group in Now Assist Admin.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

You can make a copy of this skill to configure it to meet your business needs. For more information, see [Make a copy of a Now Assist skill](https://www.servicenow.com/docs/access?context=make-a-copy-of-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **Agent Workspace for HRSD** and open an HR case that supports Sidebar discussion and summarization.

2.  Choose an existing discussion, or start a new discussion.

    Start a new discussion by doing these actions:

    1.  Select **Discuss**.

    2.  In the Start a Sidebar discussion modal, add participants.

    3.  Select **Start Discussion**.

3.  Generate a summary of the Sidebar discussion during the conversation either by using the Summarize quick action \(enter `/Summarize` in the Active sidebar discussion window\), or by selecting the quick action icon ![Quick action icon.](../image/now-assist-sidebar-lightning-bolt-icon.png).

4.  After summarizing the Sidebar discussion, you can add it to the case work notes, and provide feedback about it.

<table id="choicetable_vzl_myv_bcc"><thead><tr><th align="left" id="d562951e218">

Option

</th><th align="left" id="d562951e221">

Procedure

</th></tr></thead><tbody><tr><td id="d562951e227">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share Case summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d562951e254">

**Provide feedback for the summary**

</td><td>

If you'd like to provide feedback, select either the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\) or the not helpful icon ![Not helpful icon.](../image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Use Now Assist for HR Service Delivery \(HRSD\) in Agent Workspace](../concept/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation using Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-chat.md)

[Generate a chat reply recommendation by using Now Assist for HRSD](chat-recommendations-nahr.md)

[Generate a knowledge article from HR Agent Workspace with Now Assist for HRSD](gen-kb-now-assisthr.md)

[Generate a knowledge article from multiple cases](gen-kb-now-assisthr-multi-case.md)

[Generate an email reply recommendation using Now Assist for HRSD](email-recommendation-nahr.md)

[Summarize an HR case using Now Assist for HRSD](now-assist-hrsd-summarize-case.md)

[Generate resolution notes using Now Assist for HRSD](now-assist-hrsd-res-note.md)

[View employee summary reports](../../td-leader-hub/task/employee-summary-lh.md)

[Summarize actions while transferring an HR case](tcase-now-assist-hr.md)

[Use Knowledge Graph in Now Assist for HRSD](na-kb-graph.md)

[Use Now Assist for HR - Galileo Inside to answer HR-related questions](use-galileo-inside.md)

[Use the Now Assist panel in HR Agent Workspace](now-assist-panel-hr.md)

[Submit an HR request with Gen AI Virtual Agent](use-genai-hrsd.md)

[Now Assist for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework](../concept/integ-now-assist-hrsd.md)

[Analyze sentiments in Now Assist for HR Service Delivery \(HRSD\)](analyze-sentiments-now-assist.md)

