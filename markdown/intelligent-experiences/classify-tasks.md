---
title: Platform Classify tasks agentic workflow
description: Use the Platform Classify tasks AI agents agentic workflow to gather relevant information about tasks automatically and make decisions about priorities and assignments.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 7
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Classify tasks agentic workflow

Use the Platform Classify tasks AI agents agentic workflow to gather relevant information about tasks automatically and make decisions about priorities and assignments.

## Classify tasks overview

The Classify tasks agentic workflow can help improve efficiency and accuracy by automatically gathering information, prioritizing tasks, assigning teams, detecting sentiment, and generating task summaries.

The agents, tools, and triggers that are associated with the Classify tasks agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

For this agentic workflow to behave as expected, you must also configure Group Action Framework \(GAF\). See [Set up AI Search for Group Action Framework](../task/setup-ai-search-gaf.md) and [Configure Group Action Framework](../task/configure-gaf.md) for more information on getting started with GAF.

## Role masking

Required role:

[Role masking](aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](../task/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to classify. For example, you can add the itil role to the agentic workflow's list of approved roles so that it can access Incident records.

## Additional configuration

You can change different settings related to the agentic workflow by changing values for the Now Assist Skill Config Var Set. To access the variable set and make changes, do the following while in the Platform AI Agents and Skills scope:

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Task Classify Tasks Skill Config**.
-   In the Now Assist Skill Config Var Set related list, select **Field Predictor**.
-   Edit the variable values.
-   Save or update the record.

The Classify tasks configuration variable set includes the following variables. You can configure either the AIS fields or the GAF field for determining how the agentic workflow gathers what work the user has. If you configure both, GAF takes priority when running the agentic workflow. For more information about GAF, see [Group Action Framework](group-action-framework.md).

<table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search Mode

</td><td>

Options include Keyword, Semantic, or Hybrid. Keyword-based searches look at individual phrases, while semantic-based searches rely on the phrasing of utterances as well. Hybrid utilizes both strategies.

 Default: Keyword

</td></tr><tr><td>

AIS Search Fields

</td><td>

Fields used by AI Search operations to find similar records for improved prediction context

</td></tr><tr><td>

Capability

</td><td>

OneExtend capability for enhanced field prediction functionality. See [Generative AI Controller reference](../../generative-ai-controller/reference/reference-for-generative-ai-controller.md) for more details.

</td></tr><tr><td>

GAF Config

</td><td>

Skill configuration for [Group AI Framework \(GAF\)](group-action-framework.md).

</td></tr><tr><td>

AIS Search Fields

</td><td>

Fields used by AI Search to determine what work a user has

</td></tr><tr><td>

AIS Return Fields

</td><td>

Fields returned by AI Search to the agentic workflow to base decisions on

</td></tr><tr><td>

GAF Config

</td><td>

Group Action Framework grouping configuration record, which is a collection of groups of records to make searching easier

</td></tr><tr><td>

AIS Search Profile

</td><td>

Profile for AI search, such as Now Assist in Virtual Agent.

</td></tr><tr><td>

Capability Payload

</td><td>

Server-side script to generate custom payloads for OneExtend capability integration

</td></tr><tr><td>

AIS Fallback Table

</td><td>

Table used if GAF is not configured

</td></tr><tr><td>

Return Fields

</td><td>

Field values returned from identified relevant records

</td></tr><tr><td>

Check for Issue Readiness

</td><td>

Uses the information provided by the Issue Readiness AI agent

 **Warning:** Only enable if the Issue Readiness AI agent is active on your instance. Otherwise, the agentic workflow will not execute.

</td></tr><tr><td>

Fields

</td><td>

Field values to predict and update

</td></tr><tr><td>

Table

</td><td>

Table where you want to execute the agentic workflow on

</td></tr><tr><td>

Search Term Source

</td><td>

Options include Record-based and Utterance-based. Record-based derives search terms for generating context from the record itself. Utterance-based relies on the user-submitted utterance for search term options.

 Default: Record-based

</td></tr></tbody>
</table>## Accessing the Classify tasks agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Classify tasks**.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## In-product agentic AI and UI actions

Agentic workflows can be accessed in the Core UI and in workspaces in the AI Workflows panel. From there, you can track their progress, provide or review input, and see the results of the work performed. For more information, see [In-product agentic AI](in-product-agentic-ai.md) for more details about the AI Workflows panel.

To enable users to access agentic workflows with UI actions, you can open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow

If you don't see your UI actions after configuring it in AI Agent Studio, ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`.

## Testing the Classify tasks agentic workflow

You can manually test an agentic workflow execution or access on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](../task/define-sec-controls-aw.md). Start a manual test, select a test type and the name of the workflow, and use utterances in the Task field like the following samples. See [Test an agentic workflow execution](../task/test-aia-use-case.md).

If you want to evaluate the agentic workflow over many different execution logs, run an [automated evaluation](../task/execute-aia-eval.md).

## Sample utterance

After the workflow has been activated in AI Agent Studio, enter these or similar phrases in the Now Assist panel to trigger the workflow. You must have the sn.now\_assist\_panel\_user role to run the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

-   Populate the priority and assignment group for INC0001
-   Populate the empty fields on INC0001
-   Find the priority for INC001

## AI agents used in the Classify tasks agentic workflow

The following table lists the agents that are used in the Classify tasks agentic workflow.

**Important:** In the Define availability step of each AI agent's guided setup, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|Record field value prediction AI agent|Fetches, predicts, creates, and updates records with the provided details. Provides summary and justification for recommendations.|sn\_uxc\_gen\_ai.platform\_ai\_field\_predictor|

## Other Platform agentic workflows

For more information on other agentic workflows that are associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).

