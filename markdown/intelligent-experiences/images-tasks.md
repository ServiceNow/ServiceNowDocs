---
title: Platform Process images for new tasks agentic workflow
description: Use the Platform Process images for new tasks agentic workflow to convert images to actionable tasks.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 6
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Process images for new tasks agentic workflow

Use the Platform Process images for new tasks agentic workflow to convert images to actionable tasks.

## Process images for new tasks overview

The process images for new tasks agentic workflow can help decrease manual data entry and improve task organization by automatically converting images into task records. First, the agentic workflow extracts information from the image, such as error messages, and presents the analysis to the user. Then, the user is presented with the details of the task, such as short description, category, and priority, before it is submitted so that they can make any changes. Once the information is confirmed, the agentic workflow creates an incident record and attaches the image.

The agents, tools, and triggers that are associated with the process images for new tasks agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) and set the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it to create a custom agentic workflow](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](../../ai-implementation/concept/ai-native-sku-overview.md).

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

Users must have the **sn\_uxc\_gen\_ai.platform\_ai\_image\_processor** role to invoke the agentic workflow.

If you want the ability for users to create tasks from images using Now Assist for Virtual Agent, you must activate the Image Processor Agent, Record management AI agent, and Document and visual insights AI agent and set the display to include Virtual Agent. This agentic workflow cannot be discovered in Virtual Agent, so you must enable the individual AI agents that comprise it.

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_image\_processor.

Agentic workflows and their AI agents use [role masking](aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](../task/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to be able to make tasks on. For example, you can add the itil role to the agentic workflow's list of approved roles so that it can access Incident records.

## Additional configuration

You can change different settings related to the agentic workflow by changing values for the Now Assist Skill Config Var Set. To access the variable set and make changes, do the following while in the Platform AI Agents and Skills scope:

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Image to task config**.
-   In the Now Assist Skill Config Var Set related list, select the **Tables Mapping** configuration variable set.
-   Set the variables for the configuration type.
-   Save the Var Set.

<table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

role\_and\_table\_map

</td><td>

When a user triggers this agentic workflow, it checks the role of the invoking user and uses the map to determine what tables a user can make a record on. For example, if you map itil to Incident table, then users with the itil role can make Incident records with images.

</td></tr><tr><td>

get\_location\_details

</td><td>

Determines whether information about the image's location is included in metadata extraction.

</td></tr><tr><td>

tableslist

</td><td>

List of tables where you can make tasks from images

</td></tr></tbody>
</table>## Accessing the Process images for new tasks agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Process images for new tasks**.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## In-product agentic AI and UI actions

Agentic workflows can be accessed in the Core UI and in workspaces in the AI Activity panel. From there, you can track their progress, provide or review input, and see the results of the work performed. For more information, see [In-product agentic AI](in-product-agentic-ai.md) for more details about the AI Activity panel.

To enable users to access agentic workflows with UI actions, you can open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow

If you don't see your UI actions after configuring it in AI Agent Studio, ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`. See [Enable the in-product experience for agentic workflows](../task/enable-inproduct-aia.md).

## Sample utterance

After the workflow has been activated in AI Agent Studio, enter `Convert image to new task` or similar phrases in the Now Assist panel to trigger the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin and sn\_uxc\_gen\_ai.platform\_ai\_image\_processor roles.

## AI agents used in the Process images for new tasks agentic workflow

The following table lists the agents that are used in the Process images for new tasks agentic workflow.

**Important:** In the Define availability step of each AI agent's guided setup, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|Document and visual insights AI agent|Extracts information from images.|platform\_ml\_di.creation\_agent|

## Other Platform agentic workflows

For more information on other agentic workflows associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).

