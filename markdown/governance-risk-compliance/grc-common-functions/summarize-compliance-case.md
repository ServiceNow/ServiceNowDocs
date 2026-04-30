---
title: Summarize a compliance case using the GRC case summarization skill
description: Use the GRC case summarization skill to generate an AI summary of a compliance case. The summary provides a consolidated view of a compliance case record.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Summarize a compliance case using the GRC case summarization skill

Use the GRC case summarization skill to generate an AI summary of a compliance case. The summary provides a consolidated view of a compliance case record.

## Before you begin

**Important:** This skill is turned on by default if you have Now Assist for IRM installed. The skill is automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Role required:

-   sn\_comp\_case.compliance\_case\_analyst: Grants access to compliance case records.
-   sn\_grc\_sharegenai.grc\_case\_ai\_user: Grants users access to use the GRC case summarization skill.

## About this task

Compliance cases can span multiple action tasks, stakeholders, and regulatory requirements. The GRC case summarization skill generates a concise AI summary of key case details, so case analysts and managers can quickly understand the context and take informed action.

The skill collects data from predefined fields across the compliance case record. This data is assembled into a prompt and sent to the configured large language model \(LLM\) service provider, which then returns a structured summary.

**Important:** Be sure to check AI-generated summaries for accuracy.

If the **Summarize** option isn’t visible, the skill has to be activated by an admin. For instructions, refer to [Activate the GRC case summarization skill](activate-grc-case-summarization-skill.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Compliance Workspace**.

2.  Select the List icon.

3.  Select **All cases**.

4.  Open the compliance record that you want to summarize.

5.  Navigate to the **Overview** tab.

6.  Select **Summarize**.

    The summary is displayed. For a description of each section included in the summary, see [Components of a compliance case summary](../../grc-common/concept/compliance-case-summarization-skill.md#section_yyd_glz_k3c).

7.  Review the summary and complete any of the following options.

<table id="choicetable_szp_rjg_d2c"><thead><tr><th align="left" id="d252831e192">

Option

</th><th align="left" id="d252831e195">

Description

</th></tr></thead><tbody><tr><td id="d252831e201">

**Edit or save the summary**

</td><td>

1.  Select **Share to case summary**.
2.  Verify the AI-generated content in the modal for accuracy and make any edits.
3.  Select **Save to case summary**.

Once saved to the case record, the summary appears in the **Overview** tab and in the **Activity** stream of the **Details** tab.

</td></tr><tr><td id="d252831e239">

**View information about the summary**

</td><td>

Select the information icon \(![Info icon](../../grc-common/image/icon-more-info.png)\) next to **Compliance case summarized by Now Assist** to view a disclaimer about AI-generated content:

 **"AI summarized this using the record details. Check it for accuracy.**

</td></tr><tr><td id="d252831e264">

**Expand or collapse the summary card**

</td><td>

Select **View less** to collapse the summary partially, or **View more** to expand it.

 Alternatively, select the **Expand card** icon \(![Expand icon.](4c8d6af8f04ca00074f757d1124e0f66858f9bd4.png)\) or **Collapse card** icon \(![Collapse icon.](8cffa3bcc1d964159f63fea32116e02fa88b6445.png)\) next to **Share to case summary** to fully expand or collapse the summary.

</td></tr><tr><td id="d252831e306">

**Provide feedback**

</td><td>

Select the helpful icon \(![Helpful icon.](a3961a217c6c42794d87b70ca50a5c4e51637db4.png)\) for positive feedback. Select the not helpful icon \(![Not helpful icon.](a8538f6374f4f5e87b48dc63f04908d721aa1789.png)\) if the summary wasn't helpful.

**Note:** User feedback doesn't affect future LLM outputs. It’s collected by ServiceNow® for internal quality monitoring only.

</td></tr><tr><td id="d252831e337">

**Copy the summary**

</td><td>

Select the copy icon \(![Copy icon.](0e923b11ae593b3c5240d2fab57b32bca386c59d.png)\) to copy the summary to the clipboard.

</td></tr><tr><td id="d252831e355">

**Regenerate the summary**

</td><td>

If you think that data might have changed after you viewed the summary, select the refresh icon ![](../../grc-risk/image/refresh-icon.jpg) to regenerate the summary information.

</td></tr></tbody>
</table>
## What to do next

The summary reflects case data at the time of generation. As the case progresses, regenerate the summary to capture the latest information, and save it to the record.

