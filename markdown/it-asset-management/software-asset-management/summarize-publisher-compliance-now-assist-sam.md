---
title: Generate publisher compliance summaries by using ServiceNow Otto for Software Asset Management \(SAM\)
description: Generate a comprehensive summary for a publisher that covers software deployment, license compliance, configuration health, and optimization. The detailed publisher summary helps you to gain insights into the publisher estate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/summarize-publisher-compliance-now-assist-sam.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Using AI in Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Generate publisher compliance summaries by using ServiceNow Otto for Software Asset Management \(SAM\)

Generate a comprehensive summary for a publisher that covers software deployment, license compliance, configuration health, and optimization. The detailed publisher summary helps you to gain insights into the publisher estate.

## Before you begin

Role required: sam\_user

## About this task

**Note:** The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

Starting with the Australia Patch 4 release, Google Gemini is the default model provider for the Publisher compliance summarization generative AI skill.

ServiceNow Otto for SAM generates the publisher summaries by using reconciliation results, product lifecycle reports, and dashboards such as Discovered inventory, Normalization and content, and Health check.

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  Select the License usage view.

3.  Select a publisher to view its summary.

4.  On the Publisher details page, select **Summarize**.

    **Note:** If the system property **com.snc.samp.manage.published.products** is set to true in your ServiceNow instance, reconciliation generates publisher results for published products, unpublished products, and for all products of a publisher. The **Summarize** button is unavailable for generating publisher compliance summary for published and unpublished products. Publisher compliance summary is not supported when filtering by **Published** or **Unpublished** status in the **Published status** filter.

    The ServiceNow Otto for SAM application starts generating the summary for the selected publisher. After the summary is compiled, the results of the summary appear under different sections.

    After it's generated, the publisher summary is not automatically saved. If you close the **Publisher details** tab where you generated the summary, or if you reload the page, the publisher summary is not available. To regenerate the summary, select **Summarize**.

    \[Omitted image "now-assist-summarization.png"\] Alt text: Microsoft compliance summary.

5.  You can perform the following actions on the generated summary.

<table id="choicetable_swv_41f_f2c"><thead><tr><th align="left" id="d290314e185">

Action

</th><th align="left" id="d290314e188">

Description

</th></tr></thead><tbody><tr><td id="d290314e194">

**Copy to clipboard icon**

</td><td>

Copies the summary to a clipboard.

</td></tr><tr><td id="d290314e203">

**Refresh icon**

</td><td>

Regenerates the publisher summary.

</td></tr><tr><td id="d290314e212">

**Feedback**

</td><td>

If you found that the summary was helpful, select the helpful icon \[Omitted image "icon-helpful.png"\] Alt text: Helpful icon. If you found that the summary wasn't helpful, select the not helpful icon \[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.This feedback improves the generative AI model and can help to improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/using-now-assist-sam.md)

