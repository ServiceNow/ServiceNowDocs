---
title: Generate publisher compliance summaries by using Now Assist for Software Asset Management \(SAM\)
description: Generate a comprehensive summary for a publisher that covers software deployment, license compliance, configuration health, and optimization. The detailed publisher summary helps you to gain insights into the publisher estate.
locale: en-US
release: australia
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Generate publisher compliance summaries by using Now Assist for Software Asset Management \(SAM\)

Generate a comprehensive summary for a publisher that covers software deployment, license compliance, configuration health, and optimization. The detailed publisher summary helps you to gain insights into the publisher estate.

## Before you begin

Role required: sam\_user

## About this task

Now Assist for SAM generates the publisher summaries by using reconciliation results, product lifecycle reports, and dashboards such as Discovered inventory, Normalization and content, and Health check.

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  Select the License usage view.

3.  Select a publisher to view its summary.

4.  On the Publisher details page, select **Summarize**.

    **Note:** If the system property **com.snc.samp.manage.published.products** is set to true in your ServiceNow instance, reconciliation generates publisher results for published products, unpublished products, and for all products of a publisher. The **Summarize** button is unavailable for generating publisher compliance summary for published and unpublished products. Publisher compliance summary is not supported when filtering by **Published** or **Unpublished** status in the **Published status** filter.

    The Now Assist for SAM application starts generating the summary for the selected publisher. After the summary is compiled, the results of the summary appear under different sections.

    After it's generated, the publisher summary is not automatically saved. If you close the **Publisher details** tab where you generated the summary, or if you reload the page, the publisher summary is not available. To regenerate the summary, select **Summarize**.

    ![Microsoft compliance summary.](../image/now-assist-summarization.png)

5.  You can perform the following actions on the generated summary.

<table id="choicetable_swv_41f_f2c"><thead><tr><th align="left" id="d214907e157">

Action

</th><th align="left" id="d214907e160">

Description

</th></tr></thead><tbody><tr><td id="d214907e166">

**Copy to clipboard icon**

</td><td>

Copies the summary to a clipboard.

</td></tr><tr><td id="d214907e175">

**Refresh icon**

</td><td>

Regenerates the publisher summary.

</td></tr><tr><td id="d214907e184">

**Feedback**

</td><td>

If you found that the summary was helpful, select the helpful icon ![Helpful icon](../image/icon-helpful.png). If you found that the summary wasn't helpful, select the not helpful icon ![Not helpful icon](../image/icon-not-helpful.png).This feedback improves the generative AI model and can help to improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using generative AI skills in Now Assist for SAM](../concept/using-now-assist-sam.md)

