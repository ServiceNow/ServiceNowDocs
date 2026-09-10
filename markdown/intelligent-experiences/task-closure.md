---
title: Platform Task closure agentic workflow
description: The Task closure agentic workflow reviews open tickets against priority, sentiment, age, and status to identify which are ready to close, then guides a human agent through reviewing and closing each eligible ticket with resolution-note support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/task-closure.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 5
breadcrumb: [Platform agentic workflows, Agentic workflows, AI assets, Enable AI experiences]
---

# Platform Task closure agentic workflow

The Task closure agentic workflow reviews open tickets against priority, sentiment, age, and status to identify which are ready to close, then guides a human agent through reviewing and closing each eligible ticket with resolution-note support.

## Task closure overview

The Task closure agentic workflow screens open tickets by priority, sentiment, age, and status to flag which are eligible for closure, then walks a human agent through each eligible ticket while showing its key details and offering to close or skip. If a ticket lacks resolution notes, the workflow can draft them automatically before a final closure confirmation, and it wraps up with a summary of every ticket's outcome. This keeps agents in control while cutting the manual work of reviewing and documenting ticket closures.

The agents, tools, and triggers that are associated with the Task closure agentic workflow are provided by AI applications. You can [activate the agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-aia-use-case.md) by making triggers active and setting the display settings to include the ServiceNow Otto panel.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Prerequisites and setup

To access this workflow, you must have ServiceNow Otto for Platform installed on your instance, which you can get if you install any other AI application.

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_classify\_tasks

Agentic workflows and their AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to close. For example, you can add the itil role to the agentic workflow's list of approved roles so that it can access incident records.

## Additional configuration

You can change different settings related to the agentic workflow by changing values for the Now Assist Skill Config Var Set. To access the variable set and make changes, do the following while in the Platform AI Agents and Skills scope:

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Task Closure Skill Config**.
-   In the Now Assist Skill Config Var Set related list, select **Task Closure Eligibility Agent**.
-   Edit the variable values.
-   Save or update the record.

<table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Closure state

</td><td>

Value of the state that the task should be set to after confirmation and approval of task closure.

 Consult your table's **State** field entry on the Dictionary \[sys\_dictionary\] table for the value.

 Default:

 -   task: 3
-   incident: 7
-   problem: 7
-   change\_request: 3

</td></tr><tr><td>

Eligibility state

</td><td>

Value of the state of tasks eligible for closure.

 Default:

 -   task: 2,6
-   incident: 2,3,6
-   problem: 2,3,4,6
-   change\_request: -4,-2,-1,0

</td></tr><tr><td>

Activity Journal Fields

</td><td>

Fields that count as valid activity for the agentic workflow to consult when determining eligibility.

 Activity notices for field changes \(such as when a task changes from **Ready** to **Work in progress**\) are filtered out of consideration.

 Default: work\_notes,comments

</td></tr><tr><td>

Activity Limit

</td><td>

Number of activities consulted for eligibility consideration.

 If the total number of activities on a task exceeds the activity limit, the most recent activities are used.

 Default: 10

</td></tr><tr><td>

Eligibility Limit

</td><td>

Number of tickets to consider for closure.

 If the total number of tickets assigned to an agent exceeds the elgibility limit, the most recent tickets are evaluated.

 Default: 10

</td></tr></tbody>
</table>## Accessing the Task closure agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Home** and then the **Agentic solutions** tab.
2.  Select **Task closure**.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## Testing the Task closure agentic workflow

You can manually test an agentic workflow execution or access on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md). Start a manual test, select a test type and the name of the workflow, and use utterances in the Task field like the following samples. See [Test an agentic workflow execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

If you want to evaluate the agentic workflow over many different execution logs, run an [automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/execute-aia-eval.md).

## Sample utterance

After the workflow has been activated in AI Agent Studio, enter these or similar phrases in the ServiceNow Otto panel to trigger the workflow. You must have the sn.now\_assist\_panel\_user role to run the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

-   Close my tasks
-   Close all tickets
-   Set my tickeets to close

## AI agents used in the Task closure agentic workflow

The following table lists the agents that are used in the Task closure agentic workflow.

**Important:** In the Define availability step of each AI agent's guided setup, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|AI agent| | |

## Other Platform agentic workflows

For more information on other agentic workflows that are associated with the Platform workflow, see [Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-use-cases.md).

