---
title: Summarize a case by using Now Assist for Customer Service Management \(CSM\)
description: Generate a summary from the fields that you selected on the case record and quickly understand the case context by using the case summarization skill in the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Summarize a case by using Now Assist for Customer Service Management \(CSM\)

Generate a summary from the fields that you selected on the case record and quickly understand the case context by using the case summarization skill in the Now Assist for Customer Service Management \(CSM\) application.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

The case summarization skill provides you with a concise summary of a customer service case, including the issue, actions taken, and resolution details. With this skill, you can do the following tasks:

-   Generate an initial summary of a case so that you can understand the case context.
-   Summarize all the work that has been done on a case.

The case summarization skill is available in CSM Configurable Workspace and in Core UI.

-   In CSM Configurable Workspace, you use the Case summary by Now Assist component to generate a summary. This component appears above the activity stream.

    **Note:** You can also generate a case summary on demand from the Now Assist panel. For more information, see .

-   In Core UI, you select the **Summarize** button on the case record to generate a summary.

The case summarization skill checks the case record to determine if there is enough information available to create a summary:

-   When an agent opens the case record.
-   When an agent refreshes the case record page

If there is enough data, the Case summary component displays the **Summarize** button. If there is not enough data, the component displays a message in place of the button.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM Configurable Workspace** and open a customer service case.

2.  In the Case summary by Now Assist component, select **Summarize**.

    The Case summary by Now Assist component appears above the activity stream. The component is collapsed by default and expands to display the summary. For longer summaries that don't fit in the window, select **View more** and use the scroll bar to view the rest of the content.

    **Note:** Generating and displaying the summary may take several seconds.

    ![AI-generated case summary for a case record.](../image/now-assist-csm-case-summary.png "Case record with case summary")

3.  When you're finished summarizing a case, you can add it to the case work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d133597e185">

Option

</th><th align="left" id="d133597e188">

Procedure

</th></tr></thead><tbody><tr><td id="d133597e194">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share Case summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d133597e221">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![Expand card icon.](../image/icon-expand.png)\) or the collapse card icon \(![Collapse card icon.](../image/icon-collapse.png)\) to see more details or fewer summary details.

</td></tr><tr><td id="d133597e242">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d133597e265">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d133597e281">

**View the information about the case summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](../concept/now-assist-csm-using.md)

