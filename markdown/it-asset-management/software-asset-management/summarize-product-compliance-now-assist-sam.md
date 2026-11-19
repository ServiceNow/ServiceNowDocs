---
title: Generate product compliance summaries by using ServiceNow Otto for Software Asset Management \(SAM\)
description: Generate a comprehensive summary for a product that covers software deployment, license compliance, optimization, and issues. The detailed product compliance summary helps in gaining insights into your software assets and makes it easier to manage licenses.Triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a product compliance summary. A trigger initiates an action, such as when the system generates a product compliance summary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/summarize-product-compliance-now-assist-sam.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Use generative AI skills, Using AI in Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Generate product compliance summaries by using ServiceNow Otto for Software Asset Management \(SAM\)

Generate a comprehensive summary for a product that covers software deployment, license compliance, optimization, and issues. The detailed product compliance summary helps in gaining insights into your software assets and makes it easier to manage licenses.

## Before you begin

To display the product compliance summary, select the **Display** toggle button on the **Choose where to display** page while you configure ServiceNow Otto for SAM. For details on the **Display** toggle button, see [Configuring ServiceNow Otto for Software Asset Management \(SAM\) skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-now-assist-sam.md).

Before you use the Product compliance summarization skill, install the following plugin and the store apps that match your platform release version.

<table id="table_prod_comp_plugins"><thead><tr><th>

Platform release

</th><th>

Plugin

</th><th>

Store apps

</th></tr></thead><tbody><tr><td>

Zurich or later releases

</td><td>

Software Asset Management Professional \[com.snc.samp\]

</td><td>

-   ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 3.3.0 or later
-   Software Asset Workspace \[sn\_sam\_workspace\] - 9.0.4 or later

</td></tr></tbody>
</table>Role required: sam\_user

## About this task

**Note:** The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

Starting with the Australia Patch 4 release, AWS Claude is the default model provider for the Product compliance summarization generative AI skill.

ServiceNow Otto for SAM generates the product summaries by using reconciliation results, product life-cycle reports, and dashboards such as Discovered inventory, Normalization and content, and Health check.

**Note:** Health check details are shown only for Windows Server, SQL Server, and Oracle Database.

Use a product summary and its recommended actions to decide which follow-up steps a product needs.

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

<table id="choicetable_swv_41f_f2c"><thead><tr><th align="left" id="d276760e271">

Action

</th><th align="left" id="d276760e274">

Description

</th></tr></thead><tbody><tr><td id="d276760e280">

**Copy to clipboard icon**

</td><td>

Copies the summary to a clipboard.

</td></tr><tr><td id="d276760e289">

**Refresh icon**

</td><td>

Regenerates the product summary and recommended actions.

</td></tr><tr><td id="d276760e298">

**Feedback**

</td><td>

If you found that the summary was helpful, select the helpful icon. If you found that the summary wasn't helpful, select the not helpful icon.This feedback improves the generative AI model and can help to improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/using-now-assist-sam.md)

## Product compliance summarization skill - Triggers and Inputs

Triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a product compliance summary. A trigger initiates an action, such as when the system generates a product compliance summary.

### Triggers for product compliance summarization skill

The following table lists the triggers that determine when a product compliance summary is generated and how a product compliance summary is displayed.

|Trigger|Description|
|-------|-----------|
|User-triggered|Product compliance summary is generated when the agent manually triggers the skill by selecting **Summarize** in the Publisher details page.|

### Inputs for the product compliance summarization skill

The following table lists the inputs for the product compliance summarization skill.

<table id="table_inputs_pcs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reconciliation results

</td><td>

Compliance status of the software products with regards to the discovery and entitlements.

</td></tr><tr><td>

Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]

</td><td>

Contains product life-cycle details for all the software products that are installed in your environment.

</td></tr><tr><td>

Dashboards

</td><td>

Dashboards include Discovered inventory, Normalization and content, Health check, and Optimization and Savings dashboard.

</td></tr><tr><td>

SAP related tables

</td><td>

The SAP related tables include:-   SAP Document Type \[samp\_sap\_document\_type\]
-   SAP Digital Access Usage \[samp\_sap\_digital\_access\_usage\]
-   SAP Engine Usage \[samp\_sap\_sw\_client\_access\]
-   SAP System User \[samp\_sap\_system\_user\]

</td></tr><tr><td>

Software Subscription \[samp\_sw\_subscription\] table

</td><td>

Contains information pertaining to user software subscriptions.

</td></tr><tr><td>

Purchased Subscription Details \[samp\_purchased\_subscription\_details\]

</td><td>

Contains the information pulled from the Microsoft Azure portal related to subscriptions purchased and assigned for Microsoft 365.

</td></tr><tr><td>

Software Installation table \[cmdb\_sam\_sw\_install\]

</td><td>

Contains information on all software installed in your environment.

</td></tr></tbody>
</table>