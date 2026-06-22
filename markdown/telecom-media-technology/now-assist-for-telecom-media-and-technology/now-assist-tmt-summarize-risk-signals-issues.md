---
title: Summarize a risk signal and issues using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Generates a summary from a risk signal and issues summarization record and all associated tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-summarize-risk-signals-issues.html
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Summarize a risk signal and issues using Now Assist for Telecommunications, Media and Technology \(TMT\)

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

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d23698e147">

Option

</th><th align="left" id="d23698e150">

Procedure

</th></tr></thead><tbody><tr><td id="d23698e156">

**View more or less summary details**

</td><td>

-   To see more details summary details, select the View more icon \(\[Omitted image "icon-expand.png"\] Alt text: Expand card icon.\).
-   To see fewer summary details, select the View less icon \(\[Omitted image "icon-collapse.png"\] Alt text: Collapse card icon.\).


</td></tr><tr><td id="d23698e186">

**Provide feedback for the summary**

</td><td>

-   If you think that the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\).
-   If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d23698e219">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\) to use the summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d23698e234">

**View the information about the summary**

</td><td>

To check some details about the summary, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text: More info icon.\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spm-using.md)

