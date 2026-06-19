---
title: Skill inputs and triggers for Now Assist for Software Asset Management \(SAM\)
description: Get a quick overview of the skill inputs and triggers for Now Assist for Software Asset Management \(SAM\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/now-assist-for-software-asset-management-sam/now-assist-sam-skills-inputs.html
release: australia
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Configure, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Skill inputs and triggers for Now Assist for Software Asset Management \(SAM\)

Get a quick overview of the skill inputs and triggers for Now Assist for Software Asset Management \(SAM\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.

Depending on the selected skill, you can configure the inputs or triggers. These settings determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a publisher summary. A trigger initiates an action, such as when the system generates a publisher summary.

## Publisher compliance summarization skill

For the publisher compliance summarization skill, select the triggers that determine when a publisher compliance summary is generated. You can also select the properties that control how a publisher compliance summary is displayed. To display the publisher compliance summary, you need to select the **Display** toggle button on the Choose where to display page while configuring Now Assist for SAM. For details on the **Display** toggle button, see [Configuring Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/configure-now-assist-sam.md).

The following table lists the triggers that determine when a publisher compliance summary is generated and how a publisher compliance summary is displayed.

|Trigger|Description|
|-------|-----------|
|User triggered|Publisher compliance summary that is generated when the agent manually triggers the skill by selecting **Summarize** in the Publisher details page.|

The following table lists the inputs for the publisher compliance summarization skill.

|Input|Description|
|-----|-----------|
|Reconciliation results|Compliance status of the software products with regards to the discovery and entitlements.|
|Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]|Product life-cycle details for all the software products that are installed in your environment.|
|Dashboards|Dashboards include Discovered inventory, Normalization and content, and Health check.|

## Product compliance summarization skill

For the product compliance summarization skill, select the triggers that determine when a product compliance summary is generated. You can also select the properties that control how a product compliance summary is displayed. To display the product compliance summary, you need to select the **Display** toggle button on the Choose where to display page while configuring Now Assist for SAM. For details on the **Display** toggle button, see [Configuring Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/configure-now-assist-sam.md).

The following table lists the triggers that determine when a product compliance summary is generated and how a product compliance summary is displayed.

|Trigger|Description|
|-------|-----------|
|User triggered|Product compliance summary is generated when the agent manually triggers the skill by selecting **Summarize** in the Publisher details page.|

The following table lists the inputs for the product compliance summarization skill.

<table id="table_dg5_c5k_y2c"><thead><tr><th>

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
</table>## Recommended actions skill

For the recommended actions skill, select the triggers that determine when a list of recommended actions is generated. You can also select the properties that control how recommended actions is displayed. To display recommended actions, you need to select the **Display** toggle button on the Choose where to display page while configuring Now Assist for SAM. For details on the **Display** toggle button, see [Configuring Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/configure-now-assist-sam.md).

The following table lists the triggers that determine when recommended actions are generated and how the list of recommended actions is displayed.

<table id="table_pfz_rtm_y2c"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User triggered

</td><td>

Recommended actions is generated when the user manually triggers the skill by selecting either of the two options in the Publisher details page:

-   Get recommendations icon on Recommended actions sidebar and then select **Get recommendations**.
-   **Summarize** button for a product. When you select **Summarize**, both the product summary along recommended actions gets generated.

</td></tr></tbody>
</table>The following table lists the inputs for the recommended actions skill.

<table id="table_wzh_45m_y2c"><thead><tr><th>

Inputs

</th><th>

Source

</th></tr></thead><tbody><tr><td colspan="2">

**Configuration inputs**

</td></tr><tr><td>

Health check issues

</td><td>

Scan Findings \[Scan\_finding\]

</td></tr><tr><td>

Installs requiring actions

</td><td>

Installs Unlicensed Reasons \[samp\_install\_unlicensed\_reason\]

</td></tr><tr><td>

Normalization Rate

</td><td>

Software Discovery Models \[cmdb\_sam\_sw\_discovery\_model\]

</td></tr><tr><td>

Normalization suggestions

</td><td>

Normalization Suggestions \[samp\_normalization\_suggestion\]

</td></tr><tr><td colspan="2">

**Maintenance inputs**

</td></tr><tr><td>

Remediation options

</td><td>

Remediation Options \[samp\_remediation\_option\]

</td></tr><tr><td>

End of Life

</td><td>

Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]

</td></tr><tr><td>

Missing end of life dates

</td><td>

Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]

</td></tr><tr><td>

Expiring entitlements

</td><td>

Software Entitlements \[alm\_license\]

</td></tr><tr><td colspan="2">

**Optimization inputs**

</td></tr><tr><td>

Removal candidates

</td><td>

Removal Candidates \[samp\_sw\_reclamation\_candidate\]

</td></tr><tr><td>

Optimization \(Microsoft\):

-   Inactive subscriptions
-   Unassigned subscriptions
-   Licensing optimizations

</td><td>

Software Subscriptions \[samp\_sw\_subscription\]

 Purchased Subscription Details \[samp\_purchased\_subscription\_details\]

 Microsoft Core License Optimization Reports \[samp\_ms\_optimization\_report\]

</td></tr><tr><td>

Optimization \(Adobe\):

-   Inactive users
-   Unresolved subscriptions

</td><td>

Software Subscriptions \[samp\_sw\_subscription\]

</td></tr><tr><td>

Optimization \(Red Hat\): Licensing optimizations

</td><td>

Potential savings by optimizing licenses \[samp\_license\_optimization\_summary\]

</td></tr><tr><td>

Optimization \(SAP\):

-   Inactive users
-   Named user assignment
-   Locked out user
-   Licensed non-dialog users
-   Role based license optimization
-   Transaction based license optimization
-   Unused engines

</td><td>

SAP System Users \[samp\_sap\_system\_user\]

 License Metric Results \[samp\_license\_metric\_result\]

 Removal Candidates \[samp\_sw\_reclamation\_candidate\]

</td></tr></tbody>
</table>## SaaS user resolution skill

The following table lists the trigger for the SaaS user resolution skill.

<table id="table_vjv_3gn_dhc"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Auto triggered

</td><td>

User resolution rules are automatically generated upon the activation of the SaaS user resolution skill.

</td></tr></tbody>
</table>The following table lists the inputs for the SaaS user resolution skill.

|Input|Description|
|-----|-----------|
|List of fields with the **String** and **Email** type.|User \[sys\_user\]|

## Contract entitlement data extraction skill

<table id="table_r52_v2r_2hc"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User triggered

</td><td>

An entitlement is automatically generated from a contract when the user manually triggers the skill by selecting **Import contract document** in the software contract page.

</td></tr></tbody>
</table>The following table lists the inputs for the Contract entitlement data extraction skill.

|Input|Description|
|-----|-----------|
|The contract document|The contract document that the user uploads that is used for extracting the entitlement information.|

## Error log summarization skill

The Error log summarization skill transforms raw and cluttered application logs into clean, structured error summaries through systematic analysis. The skill identifies error patterns, classifies failure types such as API, code, infrastructure, database, and configuration, traces root causes through stack traces, and extracts key technical details while filtering out irrelevant log information. This skill also processes complex log traces that contain multiple errors, timeouts, exceptions, and system failures to provide concise, actionable error summaries that enable faster debugging and issue resolution. It handles various log formats and error patterns across different technology stacks, making it essential while dealing with production incidents.

The following table lists the trigger for the Error log summarization skill.

<table id="table_err_log_sum_trig"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User triggered

</td><td>

Error log summary is generated when the user manually triggers the skill by selecting **Troubleshoot** on the SaaS integration profile page.

</td></tr></tbody>
</table>The following table lists the inputs for the Error log summarization skill.

|Input|Description|
|-----|-----------|
|Outbound HTTP Logs \[sys\_outbound\_http\_log\]|4xx and 5xx outbound request and response details, scoped by hostname, job sys\_id, and time window.|
|Flow Execution Context \[sys\_flow\_context\]|Most recent errored flow or subflow execution context for the failing job or validate-connection action.|
|Action Type Definition \[sys\_hub\_action\_type\_definition\]|Resolves the internal name and scope of the action into the flow source sys\_id that is used for context lookup.|
|Integration Profile \[samp\_sw\_subscription\_profile\]|Profile metadata and custom properties such as action name, scope, validate timestamps, and troubleshooting parameters that scope the log queries.|
|Step-Level Execution Reports|Per-step inputs, outputs, and error details that are fetched through FlowExecutionSummaryUtil for the errored context.|

## Error resolution recommendation skill

The Error resolution recommendation skill synthesizes the error summary that is produced by the Error log summarization skill with available knowledge resources to generate prioritized, step-by-step resolution guidance. The skill correlates identified errors with knowledge base articles, historical solutions, support cases, and web search results to recommend the most effective troubleshooting approach. The skill consolidates information from multiple sources, removes redundant steps, and sequences actions from quick fixes to comprehensive solutions based on failure type, system impact, and resolution probability.

The following table lists the trigger for the Error resolution recommendation skill.

<table id="table_err_res_rec_trig"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Auto triggered

</td><td>

Resolution recommendations are automatically generated after the Error log summarization skill produces an error summary.

</td></tr></tbody>
</table>The following table lists the inputs for the Error resolution recommendation skill.

|Input|Description|
|-----|-----------|
|Error summary|Consolidated error signature such as status codes, messages, failing action, and profile context that is produced by the Error log summarization skill.|
|Web search results|External guidance, vendor documentation, and API deprecation or known-issue references that are matched to the error signature.|

## Software normalization skill

The Software normalization skill helps you identify standardized publisher and product value from your discovered software data. This skill uses large language model \(LLM\)-driven knowledge to standardize raw, incomplete, or unrecognized publisher and product values submitted during entitlement import.

The following table lists the trigger for the Software normalization skill.

<table id="table_bs5_xgm_njc"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Standard Excel import**Note:** Triggers only when the source entitlement import Excel file contains an unresolved error for a Publisher or Product value and the standard content match process has failed to resolve it.

</td><td>

The Product and Publisher data in the source Excel file don't match the Content Library data.

</td></tr></tbody>
</table>The following table lists the inputs for the Software normalization skill.

|Input|Description|
|-----|-----------|
|Raw Publisher and Product value from source Excel file|Publisher and Product value given in standard Excel that are unresolved through standard Content Library match.|

## Product match reviewer skill

The Product match reviewer skill is triggered after the Software normalization skill only when the Software normalization skill can’t find the correct product match. The Product match reviewer skill helps you confirm the correct product by analyzing search results and matching them to a predicted product name.

The following table lists the trigger for the Product match reviewer skill.

|Trigger|Description|
|-------|-----------|
|When normalization skill doesn't have right content match|The Product match reviewer skill performs an AI-powered search and selects the correct product match. If no reliable match is found, the skill returns an empty result.|

The following table lists the inputs for the Product match reviewer skill.

|Input|Description|
|-----|-----------|
|Multiple products predicted from AI-powered search|Confirmed product match from the AI-based content search result.|

**Parent Topic:**[Configuring Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-for-software-asset-management-sam/configure-now-assist-sam.md)

