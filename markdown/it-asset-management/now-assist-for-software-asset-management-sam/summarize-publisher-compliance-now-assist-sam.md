---
title: Generate publisher compliance summaries by using Now Assist for SAM
description: Generate a comprehensive summary for a publisher that covers software deployment, license compliance, configuration health, and optimization. The detailed publisher summary helps you to gain insights into the publisher estate.
locale: en-US
release: yokohama
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Now Assist for Software Asset Management \(SAM\), Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Generate publisher compliance summaries by using Now Assist for SAM

Generate a comprehensive summary for a publisher that covers software deployment, license compliance, configuration health, and optimization. The detailed publisher summary helps you to gain insights into the publisher estate.

## Before you begin

Role required: sam\_user

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Now Assist for SAM generates the publisher summaries by using reconciliation results, product lifecycle reports, and dashboards such as Discovered inventory, Normalization and content, and Health check.

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  Select the License usage view.

3.  Select a publisher to view its summary.

4.  On the Publisher details page, select **Summarize**.

    **Note:** If the property, **com.snc.samp.manage.published.products** is set to true in your ServiceNow instance, to view the **Summarize** button, navigate to the License usage view, open the **Published status** filter in the Publishers tab, and select **Clear** to ensure that both **Published** and **Unpublished** options are not selected. The reconciliation results for all publishers appears on the page.

    The Now Assist for SAM application starts generating the summary for the selected publisher. After the summary is compiled, the results of the summary appear under different sections.

    After it's generated, the publisher summary is not automatically saved. If you close the **Publisher details** tab where you generated the summary, or if you reload the page, the publisher summary is not available. To regenerate the summary, select **Summarize**.

    ![Microsoft compliance summary.](../image/now-assist-summarization.png)

5.  You can perform the following actions on the generated summary.

<table id="choicetable_swv_41f_f2c"><thead><tr><th align="left" id="d204190e170">

Action

</th><th align="left" id="d204190e173">

Description

</th></tr></thead><tbody><tr><td id="d204190e179">

**Copy to clipboard icon**

</td><td>

Copies the summary to a clipboard.

</td></tr><tr><td id="d204190e188">

**Refresh icon**

</td><td>

Regenerates the publisher summary.

</td></tr><tr><td id="d204190e197">

**Feedback**

</td><td>

If you found that the summary was helpful, select the helpful icon ![Helpful icon](../image/icon-helpful.png). If you found that the summary wasn't helpful, select the not helpful icon ![Not helpful icon](../image/icon-not-helpful.png).This feedback improves the generative AI model and can help to improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Software Asset Management \(SAM\)](../concept/using-now-assist-sam.md)

