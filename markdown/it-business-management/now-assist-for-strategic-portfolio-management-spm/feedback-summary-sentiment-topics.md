---
title: Summarize the feedback by using Now Assist for Strategic Portfolio Management \(SPM\)
description: Generate a summary from the name and description of the feedback records so that you can analyze a large volume of feedback quickly without reading each feedback record manually. You can do this task by using the multi feedback summarization skill in the Now Assist for Strategic Portfolio Management \(SPM\) application.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Feedback summarization, Multi summarization skill, Summarize feedback]
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Summarize the feedback by using Now Assist for Strategic Portfolio Management \(SPM\)

Generate a summary from the name and description of the feedback records so that you can analyze a large volume of feedback quickly without reading each feedback record manually. You can do this task by using the multi feedback summarization skill in the Now Assist for Strategic Portfolio Management \(SPM\) application.

Multi feedback summarization video.

## Before you begin

If you have users with custom roles that need access to this skill, you must update ACLs for those roles and also add those custom roles to the In product role.

The Feedback or Multi feedback summarization skill is activated by default. For more information on how to activate the skill if it isn't automatically activated or if you want to change the skill configuration, see [Configure Now Assist Admin features](../concept/configuring-na-spm.md).

Role required: pf\_user

## About this task

With the feedback or multi feedback summarization skill, you can get enough details about the feedback that you received on your product so that you can improve the product features, usability, and performance.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** and select **Feedback**.

2.  From the Feedback page, select any feedback filter card.

3.  From the feedback list, select one or multiple feedback records.

    View a loader for the side panel while the summary content loads for a more engaging loading experience.

    If you want to generate a summary for one feedback record, you can either generate it from the list level or at the record level. At the record level, the feedback summary is displayed in the Now Assist component. The component is collapsed by default and expands to display the summary.

4.  Select **Summarize**.

    View an animation for the Now assist icon when you hover over it.

    You can generate a summary of a single feedback record by using the feedback summarization skill. This image shows the AI-generated summary for a single feedback record.

    ![AI-generated summary for a single feedback record using feedback summarization skill.](../images/single-feedback-summarization-screen.png)

    You can use the multi feedback summarization skill to generate summaries of one or multiple feedback records. For example, you can analyze the high-priority feedback, filter them, summarize the records, and gain insights into the requirements.

    ![AI-generated summary for multiple feedback records using the multi feedback summarization skill.](../images/multi-feedback-summarization-example.png)

    **Note:** Because the information in these fields is automatically generated, it's a good idea to review the text and make sure it's accurate.

    The feedback or multi feedback summarization skill uses the name and description information of the feedback record to generate a paragraph or bullet-point summary from the feedback.

    View the hover animation for the Now Assist icon on the Summarize button in the feedback list and Docs.

5.  When you're finished summarizing the feedback, you can expand or collapse the summary, provide feedback, copy it, or view information about it.

<table id="choicetable_mzf_fyg_y1c"><thead><tr><th align="left" id="d186484e174">

Option

</th><th align="left" id="d186484e177">

Procedure

</th></tr></thead><tbody><tr><td id="d186484e183">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![Expand card icon.](../images/icon-expand-spm.png)\) or the collapse card icon \(![Collapse card icon.](../images/icon-collapse-spm.png)\) to see more details or fewer summary details.

</td></tr><tr><td id="d186484e204">

**More information on summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(![More information icon.](../images/icon-more-information-spm.png)\).

</td></tr><tr><td id="d186484e219">

**View more or less summary**

</td><td>

Select **View more** or **View less** to see more or less summary information.

</td></tr><tr><td id="d186484e234">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../images/icon-helpful-feedback.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../images/icon-nt-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d186484e258">

**Copy the feedback summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../images/icon-copy-spm.png)\) to use the feedback summary information for another purpose, such as pasting it into an email.

</td></tr><tr><td id="d186484e273">

**Refresh the summary**

</td><td>

Select **Refresh** to reload the feedback summary.

</td></tr><tr><td id="d186484e285">

**Copy and create epic from summary**

</td><td>

Select **Copy and create epic** to create a planning or non-planning item by using the feedback summary.

</td></tr></tbody>
</table>    **Note:** The feedback summarization or multi summarization skill checks the feedback records to determine if enough information is available to generate a summary. If there isn't enough feedback content to summarize, you can add more content and retry.

    On the side panel, you can select the preview record icon \(![preview record icon.](../../../administer/task-table/image/preview-record-icon.png)\) to view the additional details or select preview generated summary icon \(![Preview generated summary icon.](../images/preview-generated-summary-icon.png)\) to view the summarization output.

6.  Select **Copy and create epic** to copy the generated summary and create a planning item.

    Save time and streamline your work flow by linking the feedback with planning items, which eliminates the need to copy summaries. You can quickly create work items in Feedback and view them in the roadmap.


**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

