---
title: Platform Analyze task trends agentic workflow
description: Use the Platform Analyze task trends agentic workflow to detect recurring task patterns of closed tickets so that you can understand the root cause and get recommendations to prevent them from happening in future.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/incident-trends.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 10
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Analyze task trends agentic workflow

Use the Platform Analyze task trends agentic workflow to detect recurring task patterns of closed tickets so that you can understand the root cause and get recommendations to prevent them from happening in future.

## Analyze task trends overview

The Analyze task trends agentic workflow enhances task management by detecting recurring patterns, predicting disruptions, and suggesting proactive resolution to reduce downtime and improve reliability. Tasks are grouped and analyzed by AI to analyze common recurring issues and root causes. The LLM then generates resolution recommendations based on the analysis and displays it to you. After the analysis is generated, you can continue the conversation to do the following:

-   Get a summary of each group analysis. You have to specify which group you would like to get a summary of.
-   Download the analysis as a PDF or Word document.
-   Get more information by asking follow-up questions. For example, you can ask why certain suggestions were generated.
-   Analyze the next ten groups. Each analysis is done for ten groups at a time. You can continue analyzing more groups with the same filters within the same conversation, but the other actions for the previous group are no longer available.

The exact options for follow-up actions available can be configured.

The default input fields considered for analysis are the following:

-   Short Description
-   Description
-   Resolution Notes
-   Resolution Code
-   Subcategory
-   Category

You can con figure additional input fields using a Now Assist Skill Config Var Set \[sn\_nowassist\_skill\_config\_var\_set\]. See the Additional configuration section for more information.

The agents, tools, and triggers associated with the Analyze task trends agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version instead.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/ai-native-sku-overview.md).

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance. You can get this by installing any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

For this agentic workflow to behave as expected, you should have at least 500 records on your task table.

You must also configure Group Action Framework \(GAF\). See [Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/group-action-framework.md) for more information on what GAF is and how to set it up. The Incident, Case and HR Case tables use the default GAF records, but you can configure GAF for other task tables.

GAF is set up for certain Now Assist applications for you. If you want the agentic workflow to have its own system of categorization different from the main application, you can clone an existing action strategy skill and use the clone in the var set described below. This enables you to train the groupings differently for different agentic resources.

**Note:** If you create a clone of an action strategy skill, ensure that **Optimized prediction** is enabled to use AI Search as your fallback. You can leave it unchecked if you do not use AI Search on your instance.

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_analyze\_trnds.

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to access for trend analysis. For example, you can add the itil role to the agentic workflow's list of approved roles so that it can access Incident records.

## Additional configuration

You can change different settings related to the agentic workflow by changing values for the Now Assist Skill Config Var Set. To access the variable set and make changes, do the following while in the Platform AI Agents and Skills scope:

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Analyze Task Trends**.
-   In the Now Assist Skill Config Var Set related list, select **Task Trends Input Config**.
-   Edit the variable values.
-   Save or update the record.

Time is a required filter specification in the user utterance. If you want users to be able to filter tasks by fields other than time, you can configure a **Task Table Config** var set. One for the Task table is provided as part of the application. If you want to create one for a specific table, you can create a Now Assist Skill Config Var Set \[sn\_nowassist\_skill\_config\_var\_set\]. The **Skill Config** is `Analyze Task Trends`, and the **Config Type** is `Prompt Parameter Configuration`.

<table><thead><tr><th>

Config field

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Post Analysis Actions

</td><td>

List of possible follow-up actions a user can take before the agentic workflow completes.

</td><td>

-   Get a summary
-   Get more info
-   Analyze next 10 groups
-   Download analysis

</td></tr><tr><td>

Analysis Time Frame

</td><td>

Range of time, in months, for the trends analyzer to look at records to identify trends. You can specify smaller ranges when running the agentic workflow, but this value defines the maximum limit.

</td><td>

3

</td></tr><tr><td>

GAF Record Limit

</td><td>

Number of records analyzed per GAF record grouping. See the previous **Prerequisites and setup** section.

</td><td>

8

</td></tr></tbody>
</table><table><thead><tr><th>

Config field

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Input Table

</td><td>

Table that these potential filter conditions belong to

</td><td>

Task

</td></tr><tr><td>

Input Fields

</td><td>

Additional fields that the agentic workflow can consider as context for its analysis

</td><td>

None

</td></tr><tr><td>

Filter Fields

</td><td>

Fields that users can include when invoking the agentic workflow

 If you want to add new fields, use the dot-walked display-label format like the default values.

</td><td>

-   Assignment group.Name
-   Service.Name
-   Configuration item.Name

</td></tr><tr><td>

Group Skill ID

</td><td>

The Group Action Framework grouping skill dedicated to arranging records into categories

</td><td>

No default

</td></tr><tr><td>

Action Skill ID

</td><td>

The Group Action Framework action skill dedicated to selecting and mapping representative records for each group and summarizing them

 See [Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/group-action-framework.md) for information about setting up GAF.

</td><td>

No default

</td></tr><tr><td>

Auto Classify Frequency

</td><td>

When the grouping and action skills run again to incorporate new records for analysis

</td><td>

No default

 **Note:** If you provide a Group Skill ID and an Action Skill ID but leave the Auto Classify Frequency empty, it will default to 24 hours.

</td></tr></tbody>
</table>## Accessing the Analyze task trends agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Analyze task trends**.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## In-product agentic AI and UI actions

Agentic workflows can be accessed in the Core UI and in workspaces in the AI Activity panel. From there, you can track their progress, provide or review input, and see the results of the work performed. For more information, see [In-product agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/in-product-agentic-ai.md) for more details about the AI Activity panel.

To enable users to access agentic workflows with UI actions, you can open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow

If you don't see your UI actions after configuring it in AI Agent Studio, ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`. See [Enable the in-product experience for agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/enable-inproduct-aia.md).

## Testing the Analyze task trends agentic workflow

You can manually test an agentic workflow execution or access on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md). Start a manual test, select a test type and the name of the workflow, and use utterances in the Task field like the following samples. See [Test an agentic workflow execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/test-aia-use-case.md).

If you want to evaluate the agentic workflow over many different execution logs, run an [automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/execute-aia-eval.md).

## Sample utterance

After the workflow has been activated in AI Agent Studio, use similar queries to the following to run the agentic workflow in the Now Assist panel. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

Each utterance must include the name of the table and the time frame to analyze. If the utterance doesn't include these things, the agentic workflow prompts you for more information.

The time frame specified by the user can't exceed the maximum value set by the Analysis time frame configuration.

When invoking the agentic workflow, if you want to use additional filters, such as assignment group, use the name of the field in the utterance. For example, "Analyze incident trends assigned to the Hardware group" is more likely to analyze the correct records than "Analyze Hardware incident trends."

-   Analyze incident trends related to payment issues within the last two months
-   Analyze case trends within the last month
-   Analyze HR case trends with High Priority within the last two years
-   Analyze incident and problem trends within the last two weeks

## Troubleshooting

When running this agentic workflow, it's possible to see an error that states "I couldn't analyze as I didn't have the required resources." This error occurs when GAF isn't configured for the table you want to analyze. See [Configure Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configure-gaf.md) for steps to configure GAF for the table. If you're still having issues after GAF is configured, reach out to Now Support.

## AI agents used in the Analyze task trends agentic workflow

The following table lists the agents that are used in the Analyze task trends agentic workflow.

**Important:** In the Select channels and status step of each AI agent's guided setup, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|Issue trend analysis AI agent|Analyzes grouped task data to identify recurring issues and root causes. Provides detailed, actionable recommendations using structured analysis.|sn\_uxc\_gen\_ai.platform\_ai\_analyze\_trnds|

## Other Platform agentic workflows

For more information on other agentic workflows that are associated with the Platform workflow, see [Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/platform-use-cases.md).

