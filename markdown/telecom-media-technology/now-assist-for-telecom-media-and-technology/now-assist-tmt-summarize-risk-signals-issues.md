---
title: Summarize a risk signal using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Generates a summary from a risk signal and issues summarization record and all associated tasks.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Summarize a risk signal using Now Assist for Telecommunications, Media and Technology \(TMT\)

Generates a summary from a risk signal and issues summarization record and all associated tasks.

## Before you begin

Role required: sn\_acct\_lc.agent

## About this task

The risk signal and issues summary skill provides you with a summary of the risk signal and issues record and associated risk occurrences and solutions. This skill available in CSM/FSM Configurable Workspace and in Core UI.

-   In CSM/FSM Configurable Workspace, you use the Risk signal and issues summary by Now Assist component to generate a summary. This component appears above the Activities card.
-   In Core UI, you select the **Summarize** button on the risk signal and issues record to generate a summary.

The risk signal and issues summarization skill checks the record to determine if there’s enough information available to create a summary:

-   When an agent opens the risk signal and issues record
-   When an agent refreshes the risk signal and issues record page

**Note:** The risk signal and issues summarization skill requires a minimum 50 words in the record to generate the summary.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **All Risk Signal and Issues**.

2.  Open a risk and select **Summarize**.

    The Risk signal and issues summary by Now Assist component appears above the Activities card. The component is collapsed by default and expands to display the summary. Based on the inputs provided in the Engagement, account, and Short Description, the summary is generated with the following details:

    -   Overview: Summarizes the primary goal \(subject, description\), engagement, account, product, progress, and customer contact details.
    -   Progress updates: Summarizes status of work notes, activities, and recent emails.
    -   Next steps: Provides recommendations and next steps according to the open Risk Solution records.. If no records are open, the agent generates a summary based on the Risk Category.
    **Note:** Generating and displaying the summary may take several seconds. For longer summaries that don't fit in the window, select **View more** and use the scroll bar to view the rest of the content.

3.  After you're finished summarizing the risk signal and issues, manage the results.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d29721e147">

Option

</th><th align="left" id="d29721e150">

Procedure

</th></tr></thead><tbody><tr><td id="d29721e156">

**View more or less summary details**

</td><td>

-   To see more details summary details, select the View more icon \(![Expand card icon.](../image/icon-expand.png)\).
-   To see fewer summary details, select the View less icon \(![Collapse card icon.](../image/icon-collapse.png)\).


</td></tr><tr><td id="d29721e186">

**Provide feedback for the summary**

</td><td>

-   If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\).
-   If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d29721e219">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d29721e234">

**View the information about the summary**

</td><td>

To check some details about the summary, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

