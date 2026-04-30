---
title: Generate resolution notes using Now Assist for HRSD
description: Generate the resolution notes for a case using the resolution notes generation skill. You can improve the quality of the resolution notes by providing a summary of the issue and the steps that were taken to resolve the case.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use generative AI skills, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Generate resolution notes using Now Assist for HRSD

Generate the resolution notes for a case using the resolution notes generation skill. You can improve the quality of the resolution notes by providing a summary of the issue and the steps that were taken to resolve the case.

## Before you begin

[Configure resolution notes generation for Now Assist for HRSD](resolution-notes-nacm-config.md)

Role required: sn\_hr\_core.case\_writer

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

You can make a copy of this skill to configure it to meet your business needs. For more information, see [Make a copy of a Now Assist skill](https://www.servicenow.com/docs/access?context=make-a-copy-of-a-now-assist-skill&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  **All** &gt; **HR Case Management** &gt; **Agent Workspace for HR Case Management**

2.  Open an HR case that is assigned to you.

3.  After you finish working on the case, change the state of the case to **Closed Complete**.

4.  Select one of the following in the **Add resolution notes** window.

<table id="choicetable_tz3_gql_khc"><thead><tr><th align="left" id="d344733e130">

Option

</th><th align="left" id="d344733e133">

Description

</th></tr></thead><tbody><tr><td id="d344733e139">

**Save notes**

</td><td>

Add resolution notes to the **Close notes** field.**Note:** Review the generated text and make sure it's accurate. You may edit the notes or delete them to provide your own.

</td></tr><tr><td id="d344733e153">

**Skip notes**

</td><td>

Skip adding resolution notes to the case.

</td></tr></tbody>
</table>5.  Select the **Add resolution notes to work notes** check box to include the resolution notes in the **Work notes** field.

    ![AI-generated resolution notes appear.](../image/gen-resolution-note2.png)

6.  Edit the resolution notes using the Now Assist context menu.

    Resolution notes can be generated from the Now Assist context menu even when the case isn’t in **Closed Complete** state.

    1.  In the **Close notes** field, select the Now Assist icon\(![Now Assist icon](../image/now-assist-icon.png)\).

    2.  Select **Refine** to elaborate or shorten the text.

    3.  Select **Insert** to add the generated content into the **Close notes** field.


**Parent Topic:**[Using Now Assist for HR Service Delivery \(HRSD\) in Agent Workspace](../concept/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation using Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-chat.md)

[Summarize a Sidebar discussion by using Now Assist for HRSD](sidebar-discussion-nahr.md)

[Generate a chat reply recommendation by using Now Assist for HRSD](chat-recommendations-nahr.md)

[Generate a knowledge article from HR Agent Workspace with Now Assist for HRSD](gen-kb-now-assisthr.md)

[Generate a knowledge article from multiple cases](gen-kb-now-assisthr-multi-case.md)

[Generate an email reply recommendation using Now Assist for HRSD](email-recommendation-nahr.md)

[Summarize an HR case using Now Assist for HRSD](now-assist-hrsd-summarize-case.md)

[Summarize an ER case using Now Assist for HRSD](now-assist-hrsd-summarize-er-case.md)

[Summarize an ER case interview using Now Assist for HRSD](now-assist-hrsd-er-interview.md)

[View employee summary reports](../../td-leader-hub/task/employee-summary-lh.md)

[Summarize actions while transferring an HR case](tcase-now-assist-hr.md)

[Use Knowledge Graph in Now Assist for HRSD](na-kb-graph.md)

[Use Now Assist for HR - Galileo Inside to answer HR-related questions](use-galileo-inside.md)

[Use the Now Assist panel in HR Agent Workspace](now-assist-panel-hr.md)

[Submit an HR request with Gen AI Virtual Agent](use-genai-hrsd.md)

[Now Assist for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework](../concept/integ-now-assist-hrsd.md)

[Analyze sentiments in Now Assist for HR Service Delivery \(HRSD\)](analyze-sentiments-now-assist.md)

