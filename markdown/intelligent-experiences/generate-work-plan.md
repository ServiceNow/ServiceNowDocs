---
title: Platform Generate my work plan agentic workflow
description: Use the Platform Generate my work plan agentic workflow to create personalized work plans for currently assigned work.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 8
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Generate my work plan agentic workflow

Use the Platform Generate my work plan agentic workflow to create personalized work plans for currently assigned work.

## Generate my work plan overview

The Generate my work plan agentic workflow creates personalized work plans based on current assigned work. This reduces manual effort and guesswork in work planning. The AI agents identify and retrieve all work assigned to the user, predict effort required to complete work, and generate an actionable work plan. Effort is estimated based on historical records related to the open work items. Generated work plans emphasize the highest priority work by examining the following information and can result in faster resolution and fewer missed SLAs.

-   User sentiment
-   Short description
-   Priority
-   Description
-   Due date
-   Escalation
-   State
-   Updated
-   Number
-   Impact
-   SLA

The agents, tools, and triggers associated with the Generate my work plan agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by adding triggers and setting the display settings to include the Now Assist panel. To change this agentic workflow's instructions, [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version instead.

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance. You can get this by installing any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

Now LLM is not a supported LLM provider for the Generate my work plan agentic workflow.

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_work\_planner.

Agentic workflows and their AI agents use [role masking](aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](../task/define-sec-controls-aw.md).

In the data access settings, add the necessary roles to enable reading of the tables for the records you want to access for potential work plans. For example, add the itil role to the agentic workflow's list of approved roles so that it can access Incident records.

## Additional configuration

Change different settings related to the agentic workflow by changing values for the Now Assist Skill Config Var Set. To access the variable set and make changes, do the following while in the Platform AI Agents and Skills scope:

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Generate my work plan config**.
-   In the Now Assist Skill Config Var Set related list, select **New**.
-   Enter a name for your Config Var Set.
-   Set Config Type to be either `User schedule` or `Generate my work plan`.
-   Save the Var Set record.
-   Set the variables for the config type.
-   Save the Var Set.

The work plan config var set includes general variables for running the agentic workflow.

<table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schedule job

</td><td>

Creates a scheduled job that automatically runs, allowing users to see updated prioritization suggestions after making progress in their work.

</td></tr><tr><td>

Schedule job frequency

</td><td>

How long after a record in the original work plan is updated for the agentic workflow to run again. Default: 30 minutes

</td></tr><tr><td>

Predict estimates

</td><td>

Predict estimated time to complete work per record.

</td></tr><tr><td>

Exclude task table

</td><td>

By default, certain fields are used for prioritizing work on the Task table. You can configure what fields to use on individual tables, such as the Incident table. Enable this to only plan for tables configured and not other records which are task or extension of task tables.

</td></tr><tr><td>

Max tasks

</td><td>

The maximum number of tasks that can be recommended to a user for their work plan.

</td></tr></tbody>
</table>The Incident config var set includes the following variables. Configure either the AIS fields or the GAF field for determining how the agentic workflow gathers what work the user has. If you configure GAF, it takes priority when running the agentic workflow. For more information about GAF, see [Group Action Framework](group-action-framework.md).

Use this config var set as a template to change any values for other tables, such as the Case or HR Case tables.

**Note:** If you select **Exclude task table** in the work plan config var set, only the tables that have these var sets configured are included for work in the suggested work plan.

<table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table for record types that someone can work on

</td></tr><tr><td>

Conditions

</td><td>

Filter criteria for determining eligible tasks

</td></tr><tr><td>

Record fields

</td><td>

Fields passed to the workflow for analysis

</td></tr><tr><td>

Time worked

</td><td>

Custom or edited field for specifying time worked. By default, the agentic workflow uses the **Time worked** field.

</td></tr><tr><td>

AIS Search Profile

</td><td>

Specific AI Search profile

</td></tr><tr><td>

AIS Search Fields

</td><td>

Fields AI Search looks at for determining similarity

</td></tr><tr><td>

AIS Return Fields

</td><td>

Fields returned by AI Search to the agentic workflow to base decisions on

</td></tr><tr><td>

GAF Config

</td><td>

Group Action Framework grouping configuration record, which is a collection of groups of records to make searching easier.

</td></tr><tr><td>

Assigned to field

</td><td>

The field for the user who works on the record. By default, the agentic workflow uses the **assigned\_to** field.

</td></tr><tr><td>

Order by

</td><td>

JSON object containing the ordering information for how work records are prioritized.

</td></tr></tbody>
</table>By default, the Generate my work plan agentic workflow relies on the User \[sys\_user\] record's Schedule field. If there is no schedule defined on the User record, the workflow consults the Schedule \[chm\_schedule\] table for the user. If neither are present, the assumed schedule is a weekday schedule from 8:00 a.m. to 5:00 p.m.

Change what tables and fields to look for schedule information with the **User schedule** config type.

<table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table where user schedule information is stored

</td></tr><tr><td>

Conditions

</td><td>

\(Optional\) Conditions to determine what user schedule to associate with the user.

</td></tr><tr><td>

Schedule column

</td><td>

Field where specific schedule information is stored

</td></tr></tbody>
</table>## Accessing the Generate my work plan agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Generate my work plan**.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in AI Agent Studio, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## In-product agentic AI and UI actions

Access agentic workflows in the Core UI and in workspaces in the AI Activity panel. From there, track their progress, provide or review input, and see the results of the work performed. For more information, see [In-product agentic AI](in-product-agentic-ai.md) for more details about the AI Activity panel.

To enable users to access agentic workflows with UI actions, open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. Select a UI action as a possible way to access the workflow.

If you don't see your UI actions after configuring it in AI Agent Studio, verify that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`. See [Enable the in-product experience for agentic workflows](../task/enable-inproduct-aia.md).

## Testing the Generate my work plan agentic workflow

Manually test an agentic workflow execution or access on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](../task/define-sec-controls-aw.md). Start a manual test, select a test type and the name of the workflow, and use utterances in the Task field like the following samples. See [Test an agentic workflow execution](../task/test-aia-use-case.md).

To evaluate the agentic workflow over many different execution logs, run an [automated evaluation](../task/execute-aia-eval.md).

## Sample utterance

After the workflow is activated in AI Agent Studio, enter `What should I work on today?` or similar phrases in the Now Assist panel to trigger the workflow. You must have the sn.now\_assist\_panel\_user role to run the workflow. Also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

Users must have the sn\_uxc\_gen\_ai.platform\_ai\_work\_planner role to execute the agentic workflow.

## AI agents used in the Generate my work plan agentic workflow

The following table lists the agents used in the Generate my work plan agentic workflow.

**Important:** In the Select channels and status step of each AI agent's guided setup, verify that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|Prioritize work AI Agent​|Dynamically orders tasks based on parameters like urgency, priority, SLAs, sentiment, and impact.|sn\_uxc\_gen\_ai.platform\_ai\_work\_planner|

## Other Platform agentic workflows

For more information on other agentic workflows associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).

