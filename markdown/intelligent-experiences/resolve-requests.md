---
title: Platform Generate resolution plan agentic workflow
description: Use the Platform Generate resolution plan AI agents agentic workflow to fetch task record details, generate resolution summary steps, and update comments or work notes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 8
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Generate resolution plan agentic workflow

Use the Platform Generate resolution plan AI agents agentic workflow to fetch task record details, generate resolution summary steps, and update comments or work notes.

## Generate resolution plan overview

The Generate resolution plan agentic workflow can help resolve tasks by collecting record details and generating resolution summaries that can be added to comments or work notes. Due to the dynamic nature of AI agents, this agentic workflow can be used for tasks that require complex logic even when provided with minimal details.

The agents, tools, and triggers that are associated with the Generate resolution plan agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](../../ai-implementation/concept/ai-native-sku-overview.md).

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

For this agentic workflow to behave as expected, you must also configure Group Action Framework \(GAF\). See [Set up AI Search for Group Action Framework](../task/setup-ai-search-gaf.md) and [Configure Group Action Framework](../task/configure-gaf.md) for more information on getting started with GAF.

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_grp\_workflow.

Agentic workflows and their AI agents use [role masking](aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](../task/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to access for potential resolution plans. For example, you can add the itil role to the agentic workflow's list of approved roles so that it can access Incident records.

## Additional configuration

You can change different settings related to the agentic workflow by changing values for the Now Assist Skill Config Var Set. To access the variable set and make changes, do the following while in the Platform AI Agents and Skills scope:

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Generate Resolution Plans Skill Config**.
-   In the Now Assist Skill Config Var Set related list, select the configuration variable set you want to edit.
-   Set the variables for the configuration type.
-   Save the Var Set.

The Generate resolution plan configuration variable set includes the following variables. You can configure either the AIS fields or the GAF field for determining how the agentic workflow gathers what work the user has. If you configure both, GAF takes priority when running the agentic workflow. For more information about GAF, see [Group Action Framework](group-action-framework.md).

<table><thead><tr><th>

Config field

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Show button

</td><td>

Display a UI action for reviewing a generated resolution plan

</td><td>

Enabled

</td></tr><tr><td>

Button label

</td><td>

Label for the UI action button to review a generated resolution plan

</td><td>

Review

</td></tr></tbody>
</table><table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search Mode

</td><td>

Options include Keyword, Semantic, or Hybrid. Keyword-based searches look at individual phrases, while semantic-based searches rely on the phrasing of utterances as well. Hybrid utilizes both strategies.

 Default: Keyword

</td></tr><tr><td>

Include Decomposition Agent in the workflow

</td><td>

Determines whether the Decomposition Agent, one of the agents in the workflow, is used. If this is unselected, the Next best action recommendation AI agent still runs.

</td></tr><tr><td>

use\_websearch

</td><td>

Enables the agentic workflow to use web searches to help collect relevant information for generating the resolution plan

</td></tr><tr><td>

AIS Semantic Indexed Names

</td><td>

???A

</td></tr><tr><td>

script\_to\_run

</td><td>

Optional script to run when the Next best action recommendation AI agent executes

</td></tr><tr><td>

save\_activity

</td><td>

Determines whether a tool creates an activity record on the sys\_aia\_agent\_execution\_activity table when saving resolution notes

</td></tr><tr><td>

AIS Search Profile

</td><td>

Profile for AI search, such as Now Assist in Virtual Agent.

</td></tr><tr><td>

Return Fields

</td><td>

Field values returned from identified relevant records

</td></tr><tr><td>

GAF Config

</td><td>

Group Action Framework grouping configuration record, which is a collection of groups of records to make searching easier

</td></tr><tr><td>

AIS Search Fields

</td><td>

Fields used by AI Search to determine what work a user has

</td></tr><tr><td>

AI Search Matching Threshold

</td><td>

Threshold value for whether AI Search considers a record to be related and relevant

</td></tr><tr><td>

Table

</td><td>

Table which has the records you want to generate resolution plans for

</td></tr><tr><td>

Related List Tables

</td><td>

Tables which contain related records that you want the AI agent to explore before generating resolution plans

</td></tr></tbody>
</table><table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agent

</td><td>

Name of the AI agent to use for generating resolution actions

</td></tr><tr><td>

tablesinfo

</td><td>

Table information for providing context for generated action steps

</td></tr></tbody>
</table>## Accessing the Generate resolution plan agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Generate Resolution Plan**.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## In-product agentic AI and UI actions

Agentic workflows can be accessed in the Core UI and in workspaces in the AI Activity panel. From there, you can track their progress, provide or review input, and see the results of the work performed. For more information, see [In-product agentic AI](in-product-agentic-ai.md) for more details about the AI Activity panel.

To enable users to access agentic workflows with UI actions, you can open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow

If you don't see your UI actions after configuring it in AI Agent Studio, ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`. See [Enable the in-product experience for agentic workflows](../task/enable-inproduct-aia.md).

## Testing the Generate Resolution Plan agentic workflow

You can manually test an agentic workflow execution or access on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](../task/define-sec-controls-aw.md). Start a manual test, select a test type and the name of the workflow, and use utterances in the Task field like the following samples. See [Test an agentic workflow execution](../task/test-aia-use-case.md).

If you want to evaluate the agentic workflow over many different execution logs, run an [automated evaluation](../task/execute-aia-eval.md).

## Sample utterance

After the workflow has been activated in AI Agent Studio, enter these or similar phrases in the Now Assist panel to trigger the workflow. You must have the sn.now\_assist\_panel\_user role to run the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

-   Generate resolution plan for INC0001
-   Create detailed resolution steps for INC0001
-   Resolve INC0001

## AI agents used in the Generate resolution plan agentic workflow

The following table lists the agents that are used in the Generate resolution plan agentic workflow.

**Important:** In the Select channels and status step of each AI agent's guided setup, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|Next best action recommendation AI agent|Identifies the steps for resolving tasks by referencing the similar task details and reviewing knowledge articles.|sn\_uxc\_gen\_ai.platform\_ai\_next\_best\_action|
|Decomposition Agent|Analyzes and breaks down each previous resolution step into smaller, actionable substeps, then creates records|sn\_uxc\_gen\_ai.platform\_ai\_resolution\_action\_ai\_agent|

## Other Platform agentic workflows

For more information on other agentic workflows associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).

