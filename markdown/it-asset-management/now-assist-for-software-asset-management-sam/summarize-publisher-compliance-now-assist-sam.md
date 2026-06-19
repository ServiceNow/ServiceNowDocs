---
title: Generate publisher compliance summaries by using Now Assist for SAM
description: Generate a comprehensive summary for a publisher that covers software deployment, license compliance, configuration health, and optimization. The detailed publisher summary helps you to gain insights into the publisher estate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/now-assist-for-software-asset-management-sam/summarize-publisher-compliance-now-assist-sam.html
release: zurich
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Generate publisher compliance summaries by using Now Assist for SAM

Generate a comprehensive summary for a publisher that covers software deployment, license compliance, configuration health, and optimization. The detailed publisher summary helps you to gain insights into the publisher estate.

## Before you begin

Role required: sam\_user

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see .

Now Assist for SAM generates the publisher summaries by using reconciliation results, product lifecycle reports, and dashboards such as Discovered inventory, Normalization and content, and Health check.

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  Select the License usage view.

3.  Select a publisher to view its summary.

4.  On the Publisher details page, select **Summarize**.

    **Note:** If the property, **com.snc.samp.manage.published.products** is set to true in your ServiceNow instance, to view the **Summarize** button, navigate to the License usage view, open the **Published status** filter in the Publishers tab, and select **Clear** to ensure that both **Published** and **Unpublished** options are not selected. The reconciliation results for all publishers appears on the page.

    The Now Assist for SAM application starts generating the summary for the selected publisher. After the summary is compiled, the results of the summary appear under different sections.

    After it's generated, the publisher summary isn’t automatically saved. If you close the **Publisher details** tab where you generated the summary, or if you reload the page, the publisher summary is not available. To regenerate the summary, select **Summarize**.

    \[Omitted image "now-assist-summarization.png"\] Alt text: Microsoft compliance summary.

5.  You can perform the following actions on the generated summary.

<table id="choicetable_swv_41f_f2c"><thead><tr><th align="left" id="d205959e169">

Action

</th><th align="left" id="d205959e172">

Description

</th></tr></thead><tbody><tr><td id="d205959e178">

**Copy to clipboard icon**

</td><td>

Copies the summary to a clipboard.

</td></tr><tr><td id="d205959e187">

**Refresh icon**

</td><td>

Regenerates the publisher summary.

</td></tr><tr><td id="d205959e196">

**Feedback**

</td><td>

If you found that the summary was helpful, select the helpful icon \[Omitted image "icon-helpful.png"\] Alt text: Helpful icon. If you found that the summary wasn't helpful, select the not helpful icon \[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.This feedback improves the generative AI model and can help to improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using generative AI skills in Now Assist for SAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/now-assist-for-software-asset-management-sam/using-now-assist-sam.md)

