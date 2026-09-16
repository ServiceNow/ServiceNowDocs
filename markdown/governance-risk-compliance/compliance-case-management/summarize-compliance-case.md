---
title: Summarize a compliance case using GRC case summarization skill
description: Use the GRC case summarization skill to generate an AI summary of a compliance case. The summary provides a consolidated view of a compliance case record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/compliance-case-management/summarize-compliance-case.html
release: zurich
product: Compliance Case Management
classification: compliance-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Case summarization for compliance cases, AI in Compliance Case Management, Compliance Case Management, Governance, Risk, and Compliance]
---

# Summarize a compliance case using GRC case summarization skill

Use the GRC case summarization skill to generate an AI summary of a compliance case. The summary provides a consolidated view of a compliance case record.

## Before you begin

**Important:** This skill is turned on by default if you have ServiceNow Otto for IRM installed. The skill is automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required:

-   sn\_comp\_case.compliance\_case\_analyst: Grants access to compliance case records.
-   sn\_grc\_sharegenai.grc\_case\_ai\_user: Grants users access to use the GRC case summarization skill.

## About this task

Compliance cases can span multiple action tasks, stakeholders, and regulatory requirements. The GRC case summarization skill generates a concise AI summary of key case details, so case analysts and managers can quickly understand the context and take informed action.

The skill collects data from predefined fields across the compliance case record. This data is assembled into a prompt and sent to the configured large language model \(LLM\) service provider, which then returns a structured summary.

**Important:** Be sure to check AI-generated summaries for accuracy.

If the **Summarize** option isn’t visible, the skill has to be activated by an admin. For instructions, refer to [Activate the GRC case summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/activate-grc-case-summarization-skill.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Compliance Workspace**.

2.  Select the List icon.

3.  Select **All cases**.

4.  Open the compliance case record that you want to summarize.

5.  Navigate to the **Overview** tab.

6.  Select **Summarize**.

    The summary is displayed. For a description of each section included in the summary, see [Components of a compliance case summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/compliance-case-management/compliance-case-summarization-skill.md).

7.  Review the summary and complete any of the following options.

<table id="choicetable_szp_rjg_d2c"><thead><tr><th align="left" id="d269236e192">

Option

</th><th align="left" id="d269236e195">

Description

</th></tr></thead><tbody><tr><td id="d269236e201">

**Edit or save the summary**

</td><td>

1.  Select **Share to case summary**.
2.  Verify the AI-generated content in the modal for accuracy and make any edits.
3.  Select **Save to case summary**.

Once saved to the case record, the summary appears in the **Overview** tab and in the **Activity** stream of the **Details** tab.

</td></tr><tr><td id="d269236e239">

**View information about the summary**

</td><td>

Select the information icon \(\[Omitted image "icon-more-info.png"\] Alt text: Info icon\) to view the disclaimer about AI-generated content:

 **"AI summarized this using the record details. Check it for accuracy."**

</td></tr><tr><td id="d269236e261">

**Expand or collapse the summary card**

</td><td>

Select **View less** to collapse the summary partially, or **View more** to expand it.

 Alternatively, select the **Expand card** icon \(\[Omitted image "3514ebeb5281c378a441ab739e20167a2630a16b.png"\] Alt text: Expand icon.\) or **Collapse card** icon \(\[Omitted image "2ed2a915ca439e54301b2d87d922206f542ed51e.png"\] Alt text: Collapse icon.\) next to **Share to case summary** to fully expand or collapse the summary.

</td></tr><tr><td id="d269236e303">

**Provide feedback**

</td><td>

Select the helpful icon \(\[Omitted image "6703440d198d8d4e598de0ee6ca6e4bb6e927811.png"\] Alt text: Helpful icon.\) for positive feedback. Select the not helpful icon \(\[Omitted image "a6fd159de17dc274016e8b4e51533176a8a3cb3c.png"\] Alt text: Not helpful icon.\) if the summary wasn't helpful.

**Note:** User feedback doesn't affect future LLM outputs. It’s collected by ServiceNow® for internal quality monitoring only.

</td></tr><tr><td id="d269236e334">

**Copy the summary**

</td><td>

Select the copy icon \(\[Omitted image "b80284abf38e005516cfbb6a89e209fea7668e29.png"\] Alt text: Copy icon.\) to copy the summary to the clipboard.

</td></tr><tr><td id="d269236e352">

**Regenerate the summary**

</td><td>

If you think that data might have changed after you viewed the summary, select the refresh icon \[Omitted image "refresh-icon.jpg"\] Alt text: to regenerate the summary information.

</td></tr></tbody>
</table>
## What to do next

The summary reflects case data at the time of generation. As the case progresses, regenerate the summary to capture the latest information, and save it to the record.

