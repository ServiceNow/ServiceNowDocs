---
title: Platform Identify escalation signals agentic workflow
description: Use the Platform Identify escalation signals agentic workflow to identify tickets that require attention before they are escalated, such as tickets near the end of their SLA or ones without recent updates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/identify-escalation.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2026-05-29"
reading_time_minutes: 6
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Identify escalation signals agentic workflow

Use the Platform Identify escalation signals agentic workflow to identify tickets that require attention before they are escalated, such as tickets near the end of their SLA or ones without recent updates.

## Identify escalation signals overview

The Identify escalation signals agentic workflow identifies high-risk tasks that could damage customer sentiment or have breached their SLA or are close to breaching. Rather than waiting for human triage, the workflow evaluates active tickets using a composite scoring model based on the following variables.

-   Priority
-   Urgency
-   Impact
-   Age of ticket
-   Reassignment count
-   Sentiment trend
-   SLA proximity
-   Similar record history

The agents, tools, and triggers for the Identify escalation signals agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. To change this agentic workflow's instructions, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/clone-aia-usecase.md), adjust the settings, and activate the duplicated version.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/ai-native-sku-overview.md).

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance. You can get this by installing any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

For this agentic workflow to behave as expected, configure Group Action Framework \(GAF\). See [Set up AI Search for Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/setup-ai-search-gaf.md) and [Configure Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configure-gaf.md) for more information on getting started with GAF.

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_proactive\_escalation.

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).

In the data access settings, add the necessary roles to enable reading of the tables for the records you want to access for identification. For example, add the itil role to the agentic workflow's list of approved roles so it can access Incident records.

## Additional configuration

Change different settings related to the agentic workflow by changing values for the Now Assist Skill Config Var Set. To access the variable set and make changes, do the following while in the Platform AI Agents and Skills scope:

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Proactive Escalation Skill Config Skill Config**.
-   In the Now Assist Skill Config Var Set related list, select the configuration variable set you want to edit or create a Var Set with the Proactive Escalation Config Type for a new table.
-   Set the variables for the configuration type.
-   Save the Var Set.

The Identify escalation signals configuration variable set includes the following variables. Configure either the AIS fields or the GAF field to determine how the agentic workflow gathers the user's work. If you configure both, GAF takes priority when running the agentic workflow. For more information about GAF, see [Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/group-action-framework.md).

<table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skill input field mapper

</td><td>

Multiple field names used by the agentic workflow mapped onto the table value for the field. These are the fields used to gauge whether a ticket is at risk for escalation.

 **Note:** Changing the field name can cause the agentic workflow to not work as intended. You can change the field value without changing the field name.

 For example, the **SLA\_due** field name could be mapped to the **sla\_due** field value for the Incident table. For the Change Request table configuration, **SLA\_due** could be mapped to the **end\_date** field.

</td></tr><tr><td>

AIS Search Fields

</td><td>

Fields used by AI Search operations to find similar records for improved prediction context

</td></tr><tr><td>

AIS Search Profile

</td><td>

Profile for AI search, such as Now Assist in Virtual Agent.

</td></tr><tr><td>

GAF Config

</td><td>

Group Action Framework grouping configuration record, which is a collection of groups of records to make searching easier

</td></tr><tr><td>

AIS Return Fields

</td><td>

Fields returned by AI Search to the agentic workflow to base decisions on

</td></tr><tr><td>

Table name

</td><td>

Table that the configuration is applicable to. You must create a new Var Set for each table.

</td></tr></tbody>
</table>## Accessing the Identify escalation signals agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Identify escalation signals**.

The first step of the guided setup includes a complete list of included AI agents. Selecting an AI agent name opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## Testing the Identify escalation signals agentic workflow

You can manually test an agentic workflow execution on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md). Start a manual test, select a test type and the name of the workflow, and use utterances in the Task field like the following samples. See [Test an agentic workflow execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/test-aia-use-case.md).

If you want to evaluate the agentic workflow over many different execution logs, run an [automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/execute-aia-eval.md).

## Sample utterance

After activating the workflow in AI Agent Studio, enter "Identify my tickets that might escalate" or similar phrases in the Now Assist panel to trigger the workflow. You must have the sn.now\_assist\_panel\_user role to run the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

## AI agents used in the Identify escalation signals agentic workflow

The following table lists the agents that are used in the Identify escalation signals agentic workflow.

**Important:** In the Select channels and status step of each AI agent's guided setup, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|Proactive Escalation AI agent|Assesses open task records to determine if they require escalation. The agent will fetch open tasks, process the escalation reasoning, and display the results to the user.|sn\_uxc\_gen\_ai.platform\_ai\_proactive\_escalation|

## Other Platform agentic workflows

For more information on other agentic workflows associated with the Platform workflow, see [Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/platform-use-cases.md).

