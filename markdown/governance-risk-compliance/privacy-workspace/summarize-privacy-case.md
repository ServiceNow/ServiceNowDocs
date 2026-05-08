---
title: Summarize a privacy case using the GRC case summarization skill
description: Use the GRC case summarization skill to generate an AI summary of a privacy case. The summary provides a consolidated view of the case life cycle, including breach-related assessment activity.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Case summarization for privacy cases, Now Assist for Privacy Management, Privacy Management, Governance, Risk, and Compliance]
---

# Summarize a privacy case using the GRC case summarization skill

Use the GRC case summarization skill to generate an AI summary of a privacy case. The summary provides a consolidated view of the case life cycle, including breach-related assessment activity.

## Before you begin

Install the Now Assist for Privacy Management application. For more information, see [Install Now Assist for Privacy Management](privacy-install-now-assist.md).

Role required:

-   sn\_privacy\_case.privacy\_case\_analyst: Grants access to privacy case records.
-   sn\_prm\_gen\_ai.user: Grants access to the Now Assist for Privacy Management skills.

    **Note:** Users with the sn\_prm\_gen\_ai.user role automatically have the sn\_grc\_sharegenai.grc\_case\_ai\_user role, which is the minimum role required to use the GRC case summarization skill.


## About this task

**Important:** This skill is turned on by default if you have Now Assist for Privacy Management installed. The skill is automatically available to appropriate role users for the application. For more information, see Now Assist skills, agents, and agentic workflows on by default.

Privacy cases can involve multiple coordinators, complex activity logs, and breach assessments. The GRC case summarization skill generates a concise AI summary of key case details, so assignees and approvers can quickly understand the context and support efficient decision-making.

The skill collects data from predefined fields and related lists across the privacy case record. This data is assembled into a prompt and sent to the configured large language model \(LLM\) service provider, which then returns a structured summary. You can edit and save the AI‑generated summary to the case record for future reference. All members of the **Assignment group** on a case record can view any summary that has been saved to that record.

**Important:** Be sure to check AI-generated summaries for accuracy.

If the **Summarize** option isn’t visible, an admin has to activate the skill from the Now Assist Admin console. For more information, refer to [Activate the GRC case summarization skill](../../now-assist-irm/task/activate-grc-case-summarization-skill.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace**.

2.  Select the List icon.

3.  Select **All cases**.

4.  Open the privacy record that you want to summarize.

5.  Navigate to the **Overview** tab.

6.  Select **Summarize**.

    The summary is displayed. For a description of each section included in it, see [Components of a privacy case summary](../concept/privacy-case-summarization-skill.md#section_rfw_5rz_k3c).

7.  Review the summary and complete any of the following options.

<table id="choicetable_szp_rjg_d2c"><thead><tr><th align="left" id="d100089e228">

Option

</th><th align="left" id="d100089e231">

Description

</th></tr></thead><tbody><tr><td id="d100089e237">

**Edit or save the summary**

</td><td>

1.  Select **Share to case summary**.
2.  Verify the AI-generated content in the modal for accuracy and make any edits.
3.  Select **Save to case summary**.

Once saved to the case record, the summary appears in the **Overview** tab and in the **Activity** stream of the **Details** tab.

</td></tr><tr><td id="d100089e275">

**View information about the summary**

</td><td>

Select the information icon \(![Info icon](../../grc-common/image/icon-more-info.png)\) next to **Privacy case summarized by Now Assist** to view a disclaimer about AI-generated content:

 **"AI summarized this using the record details. Check it for accuracy.**

</td></tr><tr><td id="d100089e300">

**Expand or collapse the summary card**

</td><td>

Select **View less** to partially collapse the summary, or **View more** to expand it.

 Alternatively, select the **Expand card** icon \(![Expand icon.](5e6d873f6db60bae022cf9fcb303bf89a63a7304.png)\) or **Collapse card** icon \(![Collapse icon.](80d47af69a337958ed1e05bed9e9686dc905b6cf.png)\) next to **Share to case summary** to fully expand or collapse the summary.

</td></tr><tr><td id="d100089e342">

**Provide feedback**

</td><td>

Select the helpful icon \(![Helpful icon.](328ef1e6ae5fbd285e9f69401ad973e953894858.png)\) for positive feedback. Select the not helpful icon \(![Not helpful icon.](1fd014625812cb2899d61e0565992deb5c4b1678.png)\) if the summary wasn't helpful.

 **Note:** User feedback doesn't affect future LLM outputs. It’s collected by ServiceNow® for internal quality monitoring only.

</td></tr><tr><td id="d100089e374">

**Copy the summary**

</td><td>

Select the copy icon \(![Copy icon.](d766411fa2cda51fca6d8b46dc674db6e0bfa2dc.png)\) to copy the summary to the clipboard.

</td></tr><tr><td id="d100089e392">

**Regenerate the summary**

</td><td>

If you think that data might have changed after you viewed the summary, select the refresh icon ![](../../grc-risk/image/refresh-icon.jpg) to regenerate the summary information.

</td></tr></tbody>
</table>
## What to do next

The summary reflects case data at the time of generation. As the case progresses, regenerate the summary to capture the latest information, and save it to the record.

