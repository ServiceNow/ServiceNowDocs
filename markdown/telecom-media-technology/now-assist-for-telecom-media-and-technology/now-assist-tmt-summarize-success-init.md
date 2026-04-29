---
title: Summarize a success initiative using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Generate a summary from a success initiative record and all associated success tasks.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Summarize a success initiative using Now Assist for Telecommunications, Media and Technology \(TMT\)

Generate a summary from a success initiative record and all associated success tasks.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

## About this task

The success initiative summary skill provides you with a summary of the success initiative record and associated success initiative tasks. This skill available in CSM/FSM Configurable Workspace and in Core UI.

-   In CSM/FSM Configurable Workspace, you use the Success initiative summary by Now Assist component to generate a summary. This component appears above the Activities card.
-   In Core UI, you select the **Summarize** button on the success initiative record to generate a summary.

**Note:** The success initiative summarization skill must be active. If it isn’t active, summaries are generated using the out of the box case summarization skill.

The success initiative summarization skill checks the record to determine if there is enough information available to create a summary:

-   When an agent opens the success initiative record.
-   When an agent refreshes the success initiative record page.

**Note:** The success initiative summarization skill requires a minimum 50 words in the record to generate the summary.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **All Success initiatives**.

2.  Open a success initiative and select **Summarize**.

    The Success initiative summary by Now Assist component appears above the Activities card. The component is collapsed by default and expands to display the summary. Based on the inputs provided in the Engagement, account, and Short Description, the summary is generated with the following details:

    -   Overview: Summarizes the primary goal \(subject, description\), engagement, account, product, progress, due date, squad, and customer contact details.
    -   Progress updates: Summarizes current status \(work notes, recent emails\), total number of tasks, number of open and closed tasks, and any related tables.
    -   Next steps: Shows a summary list of all open tasks, required agent actions, and tasks that are due in the next 7 days.
    **Note:** Generating and displaying the summary may take several seconds. For longer summaries that don't fit in the window, select **View more** and use the scroll bar to view the rest of the content.

3.  After you're finished summarizing the success initiative, manage the results.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d19952e149">

Option

</th><th align="left" id="d19952e152">

Procedure

</th></tr></thead><tbody><tr><td id="d19952e158">

**View more or less summary details**

</td><td>

-   To see more details summary details, select the View more icon \(![Expand card icon.](../image/icon-expand.png)\).
-   To see fewer summary details, select the View less icon \(![Collapse card icon.](../image/icon-collapse.png)\).


</td></tr><tr><td id="d19952e188">

**Provide feedback for the summary**

</td><td>

-   If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\).
-   If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d19952e221">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d19952e236">

**View the information about the summary**

</td><td>

To check some details about the summary, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

