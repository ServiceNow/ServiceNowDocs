---
title: Summarize a compliance case using the GRC case summarization skill
description: Use the GRC case summarization skill to generate an AI summary of a compliance case. The summary provides a consolidated view of a compliance case record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/summarize-compliance-case.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Summarize a compliance case using the GRC case summarization skill

Use the GRC case summarization skill to generate an AI summary of a compliance case. The summary provides a consolidated view of a compliance case record.

## Before you begin

**Important:** This skill is turned on by default if you have Now Assist for IRM installed. The skill is automatically available to appropriate role users for the application. For more information, see .

Role required:

-   sn\_comp\_case.compliance\_case\_analyst: Grants access to compliance case records.
-   sn\_grc\_sharegenai.grc\_case\_ai\_user: Grants users access to use the GRC case summarization skill.

## About this task

Compliance cases can span multiple action tasks, stakeholders, and regulatory requirements. The GRC case summarization skill generates a concise AI summary of key case details, so case analysts and managers can quickly understand the context and take informed action.

The skill collects data from predefined fields across the compliance case record. This data is assembled into a prompt and sent to the configured large language model \(LLM\) service provider, which then returns a structured summary.

**Important:** Be sure to check AI-generated summaries for accuracy.

If the **Summarize** option isn’t visible, the skill has to be activated by an admin. For instructions, refer to [Activate the GRC case summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/activate-grc-case-summarization-skill.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Compliance Workspace**.

2.  Select the List icon.

3.  Select **All cases**.

4.  Open the compliance case record that you want to summarize.

5.  Navigate to the **Overview** tab.

6.  Select **Summarize**.

    The summary is displayed. For a description of each section included in the summary, see [Components of a compliance case summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/compliance-case-summarization-skill.md).

7.  Review the summary and complete any of the following options.

<table id="choicetable_szp_rjg_d2c"><thead><tr><th align="left" id="d268841e191">

Option

</th><th align="left" id="d268841e194">

Description

</th></tr></thead><tbody><tr><td id="d268841e200">

**Edit or save the summary**

</td><td>

1.  Select **Share to case summary**.
2.  Verify the AI-generated content in the modal for accuracy and make any edits.
3.  Select **Save to case summary**.

Once saved to the case record, the summary appears in the **Overview** tab and in the **Activity** stream of the **Details** tab.

</td></tr><tr><td id="d268841e238">

**View information about the summary**

</td><td>

Select the information icon \(\[Omitted image "icon-more-info.png"\] Alt text: Info icon\) next to **Compliance case summarized by Now Assist** to view a disclaimer about AI-generated content:

 **"AI summarized this using the record details. Check it for accuracy."**

</td></tr><tr><td id="d268841e263">

**Expand or collapse the summary card**

</td><td>

Select **View less** to collapse the summary partially, or **View more** to expand it.

 Alternatively, select the **Expand card** icon \(\[Omitted image "164fe1c5eda92aad2befbb60e8509a01e885bcfc.png"\] Alt text: Expand icon.\) or **Collapse card** icon \(\[Omitted image "6a261d6b6d99f1a5f95b7b28731bb51ed5601259.png"\] Alt text: Collapse icon.\) next to **Share to case summary** to fully expand or collapse the summary.

</td></tr><tr><td id="d268841e305">

**Provide feedback**

</td><td>

Select the helpful icon \(\[Omitted image "7460640cd7ecb24dc0c83ec9493197f65fc93719.png"\] Alt text: Helpful icon.\) for positive feedback. Select the not helpful icon \(\[Omitted image "632478fc6dbb398af6773211af54c1d606b6607f.png"\] Alt text: Not helpful icon.\) if the summary wasn't helpful.

**Note:** User feedback doesn't affect future LLM outputs. It’s collected by ServiceNow® for internal quality monitoring only.

</td></tr><tr><td id="d268841e336">

**Copy the summary**

</td><td>

Select the copy icon \(\[Omitted image "b39b43a47f9751945329be2990af4b95d5e09f7b.png"\] Alt text: Copy icon.\) to copy the summary to the clipboard.

</td></tr><tr><td id="d268841e354">

**Regenerate the summary**

</td><td>

If you think that data might have changed after you viewed the summary, select the refresh icon \[Omitted image "refresh-icon.jpg"\] Alt text: to regenerate the summary information.

</td></tr></tbody>
</table>
## What to do next

The summary reflects case data at the time of generation. As the case progresses, regenerate the summary to capture the latest information, and save it to the record.

