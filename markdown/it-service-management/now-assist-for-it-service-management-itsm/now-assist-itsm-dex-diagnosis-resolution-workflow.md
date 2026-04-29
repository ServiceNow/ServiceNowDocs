---
title: DEX issue diagnosis and resolution agentic workflow
description: Use the Digital End-User Experience \(DEX\) issue diagnosis and resolution agentic workflow from the Now Assist panel to diagnose and resolve common issues on DEX monitored devices.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [DEX, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# DEX issue diagnosis and resolution agentic workflow

Use the Digital End-User Experience \(DEX\) issue diagnosis and resolution agentic workflow from the Now Assist panel to diagnose and resolve common issues on DEX monitored devices.

## DEX issue diagnosis and resolution agentic workflow overview

Using the DEX issue diagnosis and resolution agentic workflow:

-   Get automated diagnoses for incidents on DEX monitored end-user devices. Root cause analysis is generated based on sources like device health check data from 24 hours before the incident to incident time and similar past incidents. With the integration of Zoom specific diagnostics, you can diagnose Zoom call quality issues by correlating device, network, and application data.
-   Get resolution plans for detected device issues based on remedial actions and self-help instructions, past incident resolutions, and Knowledge Base articles.
-   Provide approval and have the resolution summary automatically stamped to the Work notes of an incident record.

## Applications required to access the agentic workflow

To access the DEX issue diagnosis and resolution agentic workflow, make sure that you install the following applications:

-   Now Assist for IT Service Management \(ITSM\) \(sn\_itsm\_gen\_ai\) plugin.
-   Digital End-User Experience application. For more information, see [Install Digital End-User Experience](../../digital-end-user-experience/task/install-app-device-health.md) and [Configuring Digital End-User Experience](../../digital-end-user-experience/concept/config-dex-console.md).

## Roles required to access the agentic workflow

To use the DEX issue diagnosis and resolution agentic workflow, you must have one of the following role combinations:

-   sn\_dex.service\_desk\_user and ITIL
-   sn\_dex.engineer and ITIL

## Additional requirements to access the agentic workflow

The DEX issue diagnosis and resolution agentic workflow provides incident diagnosis and resolution only when the following requirements are met.

-   The agentic workflow must be activated. For more information, see [Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
-   The incident number must be valid.
-   The incident record must be associated with a single, DEX monitored physical endpoint or device. Only one device configuration item \(CI\) must be configured either as the primary CI in the **Configuration item** field or in the **Affected CIs** list.
-   The device associated with the incident must have a DEX compatible operating system. For more information, see [DEX system requirements](../../digital-end-user-experience/concept/dex-sys-requirements.md).
-   The incident must be created within the past month. Incidents older than one month cannot be diagnosed and resolved using the agentic workflow.
-   To make sure that the correct agentic workflow is initiated, include the phrase "diagnose and resolve" in your Now Assist panel prompt.

## Accessing the agentic workflow

Service desk agents can access the agentic workflow from the Service Operations Workspace by using the Now Assist panel.

Administrators can access the agentic workflow from the AI Agent Studio.

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **DEX issue diagnosis and resolution workflow**.

## AI agents used in the DEX issue diagnosis and resolution agentic workflow

In the DEX issue diagnosis and resolution agentic workflow, two AI agents are used for incident diagnosis and resolution on DEX monitored devices.

<table id="table_mby_lh2_bhc"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

DEX diagnosis AI agent

</td><td>

Performs root cause analysis of the issue by using data from sources such as device health check metrics, device or service events, and similar past incidents. It then provides the diagnosis, highlighting affected components, data sources, and patterns.If there is insufficient or inconclusive data, the agent returns a message stating no diagnosis is possible and specifies the additional information required.

</td></tr><tr><td>

DEX resolution plan AI agent

</td><td>

Collects DEX resolutions that include remedial actions and self-help instructions, past incident resolutions, and Knowledge Base articles. It then generates a resolution plan with actionable steps to resolve the incident and prompts for confirmation about updating the resolution in the Work notes field of the incident record.If no resolution is found for an incident, the agent returns a message stating so. The incident would then require manual investigation and resolution.

</td></tr></tbody>
</table>## Generating an incident diagnosis and resolution plan in the Service Operations Workspace

Service desk agents can use the agentic workflow to generate incident diagnosis and resolution plan from the Service Operations Workspace.

1.  In the Service Operations Workspace, open the incident record from the Incidents list.
2.  Select the Now Assist icon ![Now Assist icon](../image/icon-now-assist-panel.png) to open the Now Assist panel.
3.  Type your prompt that includes the phrase "diagnose and resolve". For example, Diagnose and resolve this incident.

After the resolution plan is generated, you can execute it directly from the Investigation tab of the incident record. For more information, see [Incident investigation with DEX](../../digital-end-user-experience/concept/dex-diagnostics-guided-resolutions.md).

**Example of DEX issue diagnosis and resolution agentic workflow output in Service Operations Workspace**![DEX issue diagnosis and resolution agentic workflow output in Now Assist panel within the Service Operations Workspace](../../digital-end-user-experience/image/dex-agentic-nap.png)

## Generating an incident diagnosis and resolution plan in the ServiceNow AI Agent Studio

**Note:** Make sure that you have the required privileges to test the agentic workflow and generate incident diagnosis and resolution plan from the AI Agent Studio.

In the agentic workflow record:

1.  Review the information in the Define key requirements screen, make updates if necessary, and then select **Continue**.
2.  In the Define user access screen, review or add roles that can access the use case, and then select **Continue**.
3.  In the Define data access screen, review the user identity for the AI agent, make updates if necessary, and then select **Continue**.
4.  In the Define trigger screen, make updates if necessary, and then select **Continue**. For more information about defining triggers, see [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
5.  In the Select display screen, choose where you want the agentic workflow output to be displayed, and then select **Save and test**.
6.  In the Test details screen, enter your prompt in the **Task** field, and then select **Continue to Test Chat Response**.

    Example prompt: Diagnose and resolve *incident number*.


The agent executes the request for the agentic workflow.

**Example of DEX issue diagnosis and resolution agentic workflow output in the ServiceNow AI Agent Studio**![DEX issue diagnosis and resolution agentic workflow output in AI Agent Studio](../../digital-end-user-experience/image/dex-diagnosis-resolution-workflow.png)

