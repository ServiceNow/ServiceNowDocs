---
title: Generate publisher compliance summaries by using ServiceNow Otto for Software Asset Management \(SAM\)
description: Generate a summary for a publisher that covers software deployment, license compliance, configuration health, and optimization. Use the summary to gain insight into the publisher estate without reviewing each product separately.Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a publisher summary. A trigger initiates an action, such as when the system generates a publisher summary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/summarize-publisher-compliance-now-assist-sam.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Using AI in Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Generate publisher compliance summaries by using ServiceNow Otto for Software Asset Management \(SAM\)

Generate a summary for a publisher that covers software deployment, license compliance, configuration health, and optimization. Use the summary to gain insight into the publisher estate without reviewing each product separately.

## Before you begin

To display the publisher compliance summary, select the **Display** toggle button on the **Choose where to display** page while you configure ServiceNow Otto for SAM. For details on the **Display** toggle button, see [Configuring ServiceNow Otto for Software Asset Management \(SAM\) skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/configure-now-assist-sam.md).

Before you use the Publisher compliance summarization skill, install the following plugins and the store app that match your platform release version.

<table id="table_pub_comp_plugins"><thead><tr><th>

Platform release

</th><th>

Plugins

</th><th>

Store app

</th></tr></thead><tbody><tr><td>

Zurich or later releases

</td><td>

-   Software Asset Management Professional \[com.snc.samp\]
-   Software Asset Workspace \[sn\_sam\_workspace\]

</td><td>

ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 1.0.0 or later

</td></tr></tbody>
</table>Role required: sam\_user

## About this task

**Note:** The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

Starting with the Australia Patch 4 release, Google Gemini is the default model provider for the Publisher compliance summarization generative AI skill.

ServiceNow Otto for SAM generates the publisher summaries by using reconciliation results, product lifecycle reports, and dashboards such as Discovered inventory, Normalization and content, and Health check.

Use a publisher summary to review the compliance status of all products from one publisher, instead of reviewing each product separately.

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  Select the License usage view.

3.  Select a publisher to view its summary.

4.  On the Publisher details page, select **Summarize**.

    **Note:** If the system property **com.snc.samp.manage.published.products** is set to true in your ServiceNow instance, reconciliation generates results for published products, unpublished products, and all products of a publisher. In this case, the **Summarize** button is unavailable for published and unpublished products. You cannot generate a publisher compliance summary when you filter by **Published** or **Unpublished** status.

    The ServiceNow Otto for SAM application starts generating the summary for the selected publisher. After the summary is compiled, the results of the summary appear under different sections.

    After it's generated, the publisher summary is not automatically saved. If you close the **Publisher details** tab where you generated the summary, or if you reload the page, the publisher summary is not available. To regenerate the summary, select **Summarize**.

    \[Omitted image "now-assist-summarization.png"\] Alt text: Microsoft compliance summary.

5.  You can perform the following actions on the generated summary.

<table id="choicetable_swv_41f_f2c"><thead><tr><th align="left" id="d303699e274">

Action

</th><th align="left" id="d303699e277">

Description

</th></tr></thead><tbody><tr><td id="d303699e283">

**Copy to clipboard icon**

</td><td>

Copies the summary to a clipboard.

</td></tr><tr><td id="d303699e292">

**Refresh icon**

</td><td>

Regenerates the publisher summary.

</td></tr><tr><td id="d303699e301">

**Feedback**

</td><td>

If you found that the summary was helpful, select the helpful icon \[Omitted image "icon-helpful.png"\] Alt text: Helpful icon. If you found that the summary wasn't helpful, select the not helpful icon \[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.This feedback improves the generative AI model and can help to improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/using-now-assist-sam.md)

## Publisher compliance summarization skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a publisher summary. A trigger initiates an action, such as when the system generates a publisher summary.

### Triggers for the publisher compliance summarization skill

The following table lists the triggers that determine when a publisher compliance summary is generated and how a publisher compliance summary is displayed.

|Trigger|Description|
|-------|-----------|
|User-triggered|Publisher compliance summary that is generated when the agent manually triggers the skill by selecting **Summarize** in the Publisher details page.|

### Inputs for the publisher compliance summarization skill

The following table lists the inputs for the publisher compliance summarization skill.

|Input|Description|
|-----|-----------|
|Reconciliation results|Compliance status of the software products with regards to the discovery and entitlements.|
|Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]|Product life-cycle details for all the software products that are installed in your environment.|
|Dashboards|Dashboards include Discovered inventory, Normalization and content, and Health check.|

