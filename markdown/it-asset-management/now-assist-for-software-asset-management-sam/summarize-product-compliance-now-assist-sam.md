---
title: Generate product compliance summaries by using ServiceNow Otto for Software Asset Management \(SAM\)
description: Generate a comprehensive summary for a product that covers software deployment, license compliance, optimization, and issues. The detailed product compliance summary helps in gaining insights into your software assets and makes it easier to manage licenses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/now-assist-for-software-asset-management-sam/summarize-product-compliance-now-assist-sam.html
release: zurich
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, ServiceNow Otto for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Generate product compliance summaries by using ServiceNow Otto for Software Asset Management \(SAM\)

Generate a comprehensive summary for a product that covers software deployment, license compliance, optimization, and issues. The detailed product compliance summary helps in gaining insights into your software assets and makes it easier to manage licenses.

## Before you begin

Role required: sam\_user

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

**Note:** The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

Starting with the Australia Patch 4 release, AWS Claude is the default model provider for the Product compliance summarization generative AI skill.

ServiceNow Otto for SAM generates the product summaries by using reconciliation results, product life-cycle reports, and dashboards such as Discovered inventory, Normalization and content, and Health check.

**Note:** Health check details are shown only for Windows Server, SQL Server, and Oracle Database.

When you run reconciliation with grouping, product summarization and recommended actions are available only for the parent product results, not for the individual child product results.

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  Select the License usage view.

3.  Select a publisher.

4.  On the Publisher details page, select a product.

5.  Select **Summarize**.

    The ServiceNow Otto for SAM application starts generating the summary for the selected product. After the summary is compiled, the results of the summary appear under different sections. Additionally, recommended actions are also automatically generated when you select **Summarize**.

    \[Omitted image "now-assist-sam-product-summary.png"\] Alt text: SQL Server product summarization

    After it's generated, the product summary isn’t automatically saved. If you close the Publisher details page where you generated the summary, or if you reload the page, the product summary isn’t available. To regenerate the summary, select **Summarize**.

6.  You can perform the following actions on the generated summary.

<table id="choicetable_swv_41f_f2c"><thead><tr><th align="left" id="d171095e176">

Action

</th><th align="left" id="d171095e179">

Description

</th></tr></thead><tbody><tr><td id="d171095e185">

**Copy to clipboard icon**

</td><td>

Copies the summary to a clipboard.

</td></tr><tr><td id="d171095e194">

**Refresh icon**

</td><td>

Regenerates the product summary and recommended actions.

</td></tr><tr><td id="d171095e203">

**Feedback**

</td><td>

If you found that the summary was helpful, select the helpful icon. If you found that the summary wasn't helpful, select the not helpful icon.This feedback improves the generative AI model and can help to improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/now-assist-for-software-asset-management-sam/using-now-assist-sam.md)

