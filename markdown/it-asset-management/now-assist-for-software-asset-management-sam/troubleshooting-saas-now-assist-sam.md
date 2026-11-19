---
title: Generate troubleshooting guidance for SaaS integrations by using ServiceNow Otto for Software Asset Management \(SAM\)
description: Generate error messages and detailed guidance to troubleshoot runtime job failures for SaaS integrations. These recommendations enable you to resolve common configuration issues and reduce downtime.Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate an error log summary. A trigger initiates an action, such as when the system generates an error log summary.Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate error resolution recommendations. A trigger initiates an action, such as when the system generates error resolution recommendations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/now-assist-for-software-asset-management-sam/troubleshooting-saas-now-assist-sam.html
release: zurich
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Use generative AI skills, ServiceNow Otto for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Generate troubleshooting guidance for SaaS integrations by using ServiceNow Otto for Software Asset Management \(SAM\)

Generate error messages and detailed guidance to troubleshoot runtime job failures for SaaS integrations. These recommendations enable you to resolve common configuration issues and reduce downtime.

## Before you begin

Before you use the Error log summarization and Error resolution recommendation skills, install the following plugin and the store apps that match your platform release version.

<table id="table_err_skills_plugins"><thead><tr><th>

Platform release

</th><th>

Plugin

</th><th>

Store apps

</th></tr></thead><tbody><tr><td>

Zurich Patch 8 or later patches

</td><td>

Software Asset Management Professional \[com.snc.samp\]

</td><td>

-   Software Asset Management - SaaS License Management \[sn\_sam\_saas\_int\] - 16.5.0 or later
-   ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 7.0.0 or later
-   Software Asset Workspace \[sn\_sam\_workspace\] - 10.0.8 or later

</td></tr></tbody>
</table>Role required: sam\_integrator

## About this task

**Note:** The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

Starting with the Australia Patch 4 release, AWS Claude is the default model provider for the Error resolution recommendation and Error log summarization generative AI skill.

ServiceNow Otto for SAM generates the troubleshooting guidance for all SaaS integrations by enabling dynamic debug-level logging for flow actions and validating connections. The troubleshooting guidance is available for both existing and new SaaS integrations.

The Error log summarization skill processes application logs and classifies failure types, such as API, code, infrastructure, database, and configuration errors.

The Error resolution recommendation skill uses that error summary to generate prioritized, step-by-step resolution guidance.

The skill correlates each error with knowledge base articles, historical solutions, support cases, and web search results.

## Procedure

1.  Navigate to **Workspace** &gt; **Software Asset Workspace** &gt; **License operations**.

2.  Select **User subscription** and then select **Direct integration profiles**.

3.  Generate troubleshooting guidance.

<table id="choicetable_azy_b5f_g3c"><thead><tr><th align="left" id="d342462e207">

Integration

</th><th align="left" id="d342462e210">

Action

</th></tr></thead><tbody><tr><td id="d342462e216">

**Existing**

</td><td>

1.  Select the integration profile from the Direct integration profiles list.

An error message is displayed on the Integration Profile form indicating that the scheduled job failed to complete successfully.

2.  Select **Troubleshoot** on the error message.

The ServiceNow Otto for SAM application generates the troubleshooting details that contain the error summary and suggested resolutions. Each error that's listed in the Error Summary section has a corresponding troubleshooting guidance in the Suggested Resolutions section.

</td></tr><tr><td id="d342462e244">

**New**

</td><td>

1.  Select **New**.
2.  Select an integration type from the drop-down list.
3.  Select **Continue**.
4.  On the Integration profile form, enter a unique and descriptive **Display name**.
5.  Verify the required user roles or API permissions specified under various subflows and select **Save**.
6.  Select the preview icon \[Omitted image "Form\_ReferenceLookupIcon.png"\] next to the **Connection &amp; Credential** field.
7.  Enter connection and credential details for this integration profile by selecting the **Create New Connection &amp; Credential** related link.
8.  Select **Create**.
9.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

The ServiceNow instance displays an error message stating that the connection validation isn't successful.

10. Select **Troubleshoot** on the error message.

The ServiceNow Otto for SAM application generates the troubleshooting details that contain the error summary and suggested resolutions. Each error that's listed in the Error Summary section has a corresponding troubleshooting guidance in the Suggested Resolutions section.

</td></tr></tbody>
</table>    \[Omitted image "now-assist-troubleshooting.png"\] Alt text: Error summary and troubleshooting guidance for SaaS integration

4.  Use the suggested resolutions and select **Validate Connection.**

    If the connection validation isn't successful, you can select the **Troubleshoot** button to regenerate the error summary and resolution guidance.

5.  After the connection validation is successful, publish the integration profile by selecting **Publish**.


**Parent Topic:**[Using generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/now-assist-for-software-asset-management-sam/using-now-assist-sam.md)

## Error log summarization skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate an error log summary. A trigger initiates an action, such as when the system generates an error log summary.

### Triggers for the Error log summarization skill

The following table lists the trigger for the Error log summarization skill.

|Trigger|Description|
|-------|-----------|
|User-triggered|Error log summary is generated when the user manually triggers the skill by selecting **Troubleshoot** on the SaaS integration profile page.|

### Inputs for the Error log summarization skill

The following table lists the inputs for the Error log summarization skill.

|Input|Description|
|-----|-----------|
|Outbound HTTP Logs \[sys\_outbound\_http\_log\]|4xx and 5xx outbound request and response details, scoped by hostname, job sys\_id, and time window.|
|Flow Execution Context \[sys\_flow\_context\]|Most recent errored flow or subflow execution context for the failing job or validate-connection action.|
|Action Type Definition \[sys\_hub\_action\_type\_definition\]|Resolves the internal name and scope of the action into the flow source sys\_id that is used for context lookup.|
|Integration Profile \[samp\_sw\_subscription\_profile\]|Profile metadata and custom properties such as action name, scope, validate timestamps, and troubleshooting parameters that scope the log queries.|
|Step-Level Execution Reports|Per-step inputs, outputs, and error details that are fetched through FlowExecutionSummaryUtil for the errored context.|

## Error resolution recommendation skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate error resolution recommendations. A trigger initiates an action, such as when the system generates error resolution recommendations.

### Triggers for the Error resolution recommendation skill

The following table lists the trigger for the Error resolution recommendation skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|Resolution recommendations are automatically generated after the Error log summarization skill produces an error summary.|

### Inputs for the Error resolution recommendation skill

The following table lists the inputs for the Error resolution recommendation skill.

|Input|Description|
|-----|-----------|
|Error summary|Consolidated error signature such as status codes, messages, failing action, and profile context that is produced by the Error log summarization skill.|
|Web search results|External guidance, vendor documentation, and API deprecation or known-issue references that are matched to the error signature.|

