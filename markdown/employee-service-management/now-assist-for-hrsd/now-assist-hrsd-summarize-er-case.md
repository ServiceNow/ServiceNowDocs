---
title: Summarize an ER case using Now Assist for HRSD
description: Use the ER case summarization skill to obtain a comprehensive overview of the ER case, which includes key details such as allegations, evidences, and interviews.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 6
breadcrumb: [Use generative AI skills, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Summarize an ER case using Now Assist for HRSD

Use the ER case summarization skill to obtain a comprehensive overview of the ER case, which includes key details such as allegations, evidences, and interviews.

## Before you begin

Role required: sn\_hr\_er.case\_writer

## About this task

You can use the ER case summarization skill in either Core UI or Agent Workspace for HR Case Management.

-   In Core UI, the summary appears in a banner in the case record.
-   In Agent Workspace for HR Case Management, the summary is generated in the **Details** tab.

**Note:** For information on how to configure the case summarization skill, see [Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md).

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **HR Agent Workspace**.

2.  In Workspace, open an ER case that is assigned to you.

    Alternatively, you can navigate to **All** &gt; **HR Cases** and select an ER case.

3.  Select **Summarize**.

4.  **Note:** Generating and displaying the summary may take several seconds.

5.  Review the summary details.

    A summary of a case is displayed. The summary varies based on the state of the case:

    -   In **Ready** state: Case Information, Case Overview, Involved Parties, Allegations, and Key Dates are displayed.
    -   In **Work in progress** or **Closed complete** state: Case Information, Case Overview, Involved Parties, Allegations, Interviews Summary, Evidence Summary, Allegation Outcomes, Corrective Actions, and Key Dates are displayed.

        **Note:** Attachment related details are added to the summary only when an attachment is present on ER case irrespective of case state.

    ![ER case summary on Agent Workspace for HR Case Management](../image/er-summarize-aws.png "ER case summary in HR Agent Workspace") ![ER case summary on Agent Workspace for HR Case Management](../image/er-summarize-aws1.png "ER case summary in HR Agent Workspace")

    ![ER case summary on Core UI](../image/er-summarize-core.png "ER case summary in Core UI") ![ER case summary on Core UI](../image/er-summarize-core1.png "ER case summary in Core UI")

6.  When you finish summarizing a case, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d355942e244">

Option

</th><th align="left" id="d355942e247">

Procedure

</th></tr></thead><tbody><tr><td id="d355942e253">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share**.
2.  In the Share Case summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d355942e280">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![Expand card icon.](../image/icon-expand.png)\) or the collapse card icon \(![Collapse card icon.](../image/icon-collapse.png)\) to see more details or fewer summary details.

</td></tr><tr><td id="d355942e301">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill.

</td></tr><tr><td id="d355942e324">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d355942e340">

**View the information about the case summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr><tr><td id="d355942e355">

**Refine list**

</td><td>

Elaborate or shorten the summary.

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for HR Service Delivery \(HRSD\) in Agent Workspace](../concept/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation using Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-chat.md)

[Summarize a Sidebar discussion by using Now Assist for HRSD](sidebar-discussion-nahr.md)

[Generate a chat reply recommendation by using Now Assist for HRSD](chat-recommendations-nahr.md)

[Generate a knowledge article from HR Agent Workspace with Now Assist for HRSD](gen-kb-now-assisthr.md)

[Generate a knowledge article from multiple cases](gen-kb-now-assisthr-multi-case.md)

[Generate an email reply recommendation using Now Assist for HRSD](email-recommendation-nahr.md)

[Summarize an HR case using Now Assist for HRSD](now-assist-hrsd-summarize-case.md)

[Summarize an ER case interview using Now Assist for HRSD](now-assist-hrsd-er-interview.md)

[Generate resolution notes using Now Assist for HRSD](now-assist-hrsd-res-note.md)

[View employee summary reports](../../td-leader-hub/task/employee-summary-lh.md)

[Summarize actions while transferring an HR case](tcase-now-assist-hr.md)

[Use Knowledge Graph in Now Assist for HRSD](na-kb-graph.md)

[Use Now Assist for HR - Galileo Inside to answer HR-related questions](use-galileo-inside.md)

[Use the Now Assist panel in HR Agent Workspace](now-assist-panel-hr.md)

[Submit an HR request with Gen AI Virtual Agent](use-genai-hrsd.md)

[Now Assist for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework](../concept/integ-now-assist-hrsd.md)

[Analyze sentiments in Now Assist for HR Service Delivery \(HRSD\)](analyze-sentiments-now-assist.md)

