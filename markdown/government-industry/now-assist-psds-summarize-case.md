---
title: Summarize a government case using ServiceNow Otto for Public Sector Digital Services \(PSDS\)
description: Use the case summarization skill in ServiceNow Otto for Public Sector Digital Services \(PSDS\) to generate a summary from selected case record fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/now-assist-psds-summarize-case.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, ServiceNow Otto for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Summarize a government case using ServiceNow Otto for Public Sector Digital Services \(PSDS\)

Use the case summarization skill in ServiceNow Otto for Public Sector Digital Services \(PSDS\) to generate a summary from selected case record fields.

## About this task

Government service agents can use case summarization, powered by Now LLM, to gain contextual understanding of constituent issues throughout the case's lifecycle. The case summarization skill auto-generates informative summaries that distill key details from work notes, comments, and other case data, which can help agents resolve cases faster.

The case summarization component appears below the activity picker component on the playbook page templates, and is collapsed by default. When an agent generates a case summary by selecting **Summarize**, the component expands to display the summary information. The summary includes a description of the issue, the actions taken, and the next steps. For longer summaries, select **View more** and use the scroll bar to view the content.

The case summarization skill enables you to do the following actions:

-   Select Summarize to create a summary of the case details.
-   Select Share to work notes to copy the summary text to the activity stream.
    -   Review the summary text in the Share to work notes pop-up dialog and modify the text as needed.
    -   Select Save to work notes on the pop-up dialog to add the text to the activity stream.
-   Select the refresh icon in the component footer to refresh the text and get the latest summary.

After generating a summary, you can:

-   Review the summary information and edit as needed.
-   Provide feedback on the generated summary.
-   Add the summary information to the case work notes.
-   Copy the summary information to the clipboard.

**Note:** You can also generate a case summary on demand from the ServiceNow Otto panel. .

## Before you begin

Role required: admin

## Procedure

1.  Open a government service case by navigating to Lists in the CSM Configurable Workspace.

2.  In the Case summary by ServiceNow Otto component, select **Summarize**.

    **Note:** The Case summary by ServiceNow Otto component appears above the constituent card. Generating and displaying the summary may take several seconds. The component is collapsed by default and expands to display the summary. For longer summaries that don't fit in the window, select **View more** and use the scroll bar to view the rest of the content.

    \[Omitted image "image.psds-otto-case-summary"\] Alt text: AI-generated case summary for a case record.

3.  When you're finished summarizing a case, you can add it to the case work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d54135e175">

Option

</th><th align="left" id="d54135e178">

Procedure

</th></tr></thead><tbody><tr><td id="d54135e184">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share to Work notes**.
2.  In the Share Case summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d54135e211">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(\[Omitted image "icon-expand.png"\] Alt text: Expand card icon.\) or the collapse card icon \(\[Omitted image "icon-collapse.png"\] Alt text: Collapse card icon.\) to see more details or fewer summary details.

</td></tr><tr><td id="d54135e232">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\). If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d54135e255">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d54135e271">

**View the information about the case summary**

</td><td>

If you want to view more details about the summary, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text: More info icon.\).

</td></tr></tbody>
</table>
