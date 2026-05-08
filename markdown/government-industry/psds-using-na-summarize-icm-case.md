---
title: Summarize an investigative case using the Now Assist for PSDS Investigative case summarization skill
description: Generate a summary directly from the investigative case workspace to help you understand the case context using the investigative case summarization skill in the Now Assist for Public Sector Digital Services \(PSDS\) application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Summarize an investigative case using the Now Assist for PSDS Investigative case summarization skill

Generate a summary directly from the investigative case workspace to help you understand the case context using the investigative case summarization skill in the Now Assist for Public Sector Digital Services \(PSDS\) application.

## About this task

Investigators can utilize investigative case summarization, powered by Now LLM, to gain contextual understanding of the investigation throughout its lifecycle. The investigative case summarization skill auto-generates summaries that distill key details from work notes, comments, and other case data, which can help agents resolve cases faster.

The Investigative Case Management case summarization component appears on the case record page, and is collapsed by default. When an agent generates a case summary by selecting **Summarize**, the component expands to display the summary information, including a description of the issue, the actions taken, and the next steps. For longer summaries, select **View more** and use the scroll bar to view the content.

The case summarization skill enables you to do the following actions:

-   Select Summarize to create a summary of the case details.
-   Select Share to work notes to copy the summary text to the activity stream.
    -   Review the summary text in the Share to work notes pop-up dialogue and modify the text as needed.
    -   Select Save to work notes on the pop-up dialogue to add the text to the activity stream.
-   Select the refresh icon in the component footer to refresh the text and get the latest summary.

After generating a summary, you can:

-   Review the summary information and edit as needed.
-   Provide feedback on the generated summary.
-   Add the summary information to the case work notes.
-   Copy the summary information to the clipboard.

**Note:** You can also generate a case summary on demand from the Now Assist panel. .

## Before you begin

Role required: admin

## Procedure

1.  Open an investigative case by navigating to Lists in the CSM Configurable Workspace.

2.  In the Case summary by Now Assist component, select **Summarize**.

    ![AI-generated case summary for a case record.](../image/now_assist_psds_case_summary.png "Case record with case summary")

3.  When you're finished summarizing a case, you can add it to the case work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d49570e167">

Option

</th><th align="left" id="d49570e170">

Procedure

</th></tr></thead><tbody><tr><td id="d49570e176">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share to Work notes**.
2.  In the Share Case summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d49570e203">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![Expand card icon.](../image/icon-expand.png)\) or the collapse card icon \(![Collapse card icon.](../image/icon-collapse.png)\) to see more details or fewer summary details.

</td></tr><tr><td id="d49570e224">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d49570e247">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d49570e263">

**View the information about the case summary**

</td><td>

If you want to view more details about the summary, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr></tbody>
</table>
