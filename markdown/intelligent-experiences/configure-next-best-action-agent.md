---
title: Create an AI agent
description: Create an AI agent in AI Agent Studio to solve problems for your users and coordinate with other AI agents while executing the agentic workflows.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-09-17"
reading_time_minutes: 19
keywords: [Agentic AI, ACLs in AI agents]
breadcrumb: [Now Assist AI agents, Enable AI experiences]
---

# Create an AI agent

Create an AI agent in AI Agent Studio to solve problems for your users and coordinate with other AI agents while executing the agentic workflows.

## Before you begin

Role required: sn\_aia.admin

## About this task

In the ServiceNow agentic ecosystem, an AI agent is a set of large language model \(LLM\) instructions and tools that can perform specific tasks.

An AI agent can collaborate with other agents to achieve better results by using fewer large language model \(LLM\) calls. AI agents can also reach out to the user if they need any help or information.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  From the **Add** drop-down, select one of the following agent creation options:**Chat** or **External**.

    1.  **Chat**: Select the Chat option to create AI agents in the AI Agent Studio to connect with internal AI agents within the ServiceNow AI Platform to execute agentic workflows.

    2.  **External**: Select the External option to create external AI agents in the AI Agent Studio to connect the ServiceNow AI Platform with the third-party agentic AI providers.

        For more information about creating external AI agents in the AI Agent Studio, see .

3.  On the New AI Agent page, in the Define the specialty step, define your AI agent and provide the specialties that this agent contains so that the LLM can analyze the wording you use to understand the purpose of the AI agent.

    ![AI Agent Guided Setup showcasing the different stages of configuring an AI agent.](../image/create-ai-agent-latest.png)

    **Note:** The more details that you provide, the more accurately your AI agent can perform.

    Select **Generate description, role, and steps** to generate a description and instructions with Now Assist in the Generate a description, role, and list of steps with Now Assist pop-up window. If you provide the description of what you want the agent to do, you can select **Generate** to write the name, description, AI agent role, and instructions fields for you. You can change those fields after the text has been generated or try again with new instructions.

    1.  Describe your AI Agent by giving it a unique name and description.

<table id="table_mp3_4nj_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent name

</td><td>

Name for the AI agent.Provide a name according to the outcome that you want your AI agent to achieve. For example: Next Best Action.

</td></tr><tr><td>

AI agent Description

</td><td>

Brief summary of what your AI agent can do autonomously. Outline all the activities that you want your AI agent to perform while solving your agentic workflow.

 Example for the Next Best Action: The Next Best Action agent identifies the optimal steps for resolving tasks by gathering details, referencing similar cases, and reviewing knowledge articles. It collaborates with the user to create a step-by-step resolution plan, revising it based on feedback, and only proceeds when the plan is approved.

**Note:** The character limit for the description is 2000.

</td></tr></tbody>
</table>    2.  Define the role and necessary steps so that the AI agent can carry out its tasks.

        **Note:** The AI agent uses this information as guidance to tailor its responses and actions.

<table id="table_uj3_msj_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent role

</td><td>

Capabilities and responsibilities for your AI agent. Roles enable your AI agent to perform its required actions.

 Example for the Next Best Action: AI agents are experts at resolving issues. Task resolution objectives, such as incident, case, or problem, can be handled, regardless of the actual problem described in the task.

**Note:** The character limit for defining the AI agent role is 2000.

</td></tr><tr><td>

List of steps

</td><td>

Necessary steps to be followed by the AI agent while carrying out its role.

**Note:** The instructions are sent to the large language model \(LLM\).

 Example for the Next Best Action: Tasks are records for tracking issues and their resolution updates through a set of journal entries. Your objective is to understand the issue with the incoming task, search for potential solutions, and provide a resolution plan for solving the issue presented in the task.

 To resolve a task, always follow this progression of steps:

1.  Get the details of the task.
2.  Fetch a list of similar tasks to understand the general procedure followed for a reference.
3.  Fetch a list of relevant knowledge articles, based on the short description of the task. If similar knowledge articles are present, understand the general procedure followed for a reference.
 After gathering the preceding details, verify that you have enough information to create a plan and perform the following actions:

1.  Generate a plan for resolving the task in a numbered list format.

**Important:** You must create the task actions in a numbered list format.

2.  Inform the user of the plan and seek feedback or approval.

**Note:** Explicitly mention that you must reach out to the user. Always treat a user's response to the plan as a critique to the current plan and not as permission or direction to proceed.

3.  Revise the plan based on the user feedback and generate a new one in a numbered list.
4.  Inform the user of the revised plan and seek feedback or approval.
5.  Repeat steps 3 and 4 until the user approves the plan.

**Note:** Don't proceed with the plan until the user confirms.

6.  After the user has approved the plan, proceed with the plan.
7.  Use the check\_with\_other\_agents tool to check if the current AI agent is unable or able to solve the given task, and to check with the other AI agents.
 If similar tasks or knowledge articles aren't present, do the following actions:

-   Inform the user that you couldn't come up with a plan because you didn't have the required resources and seek instructions.
-   If a user says they can take over the resolution process, finish the execution with the `Thank you for using NowAssist message`.
 **Note:**

-   After the tools are executed and the task is resolved, don't show or update the plan anymore.
-   If the plan is approved or revised by the user, never end the execution before the resolution is applied.
 Additional instructions:

-   Continue with normal reasoning after the preceding steps, to solve the problem.
-   Don't start a resolution until the user explicitly confirms that the plan is good to go. Always ask the user if they're satisfied with the plan.
-   Don't end the execution without applying the determined solution.
-   Don't expect the user to perform the required fix.
-   You're an AI agent and you always communicate with "assigned to" user, not the caller. Never assume any other role.
-   Never format your messages as an email. Always send them as an informal text message.


</td></tr></tbody>
</table>        Follow these guidelines for writing effective Instructions:

        -   Define the AI agent's role:

            -   Clearly state the primary function of the AI agent in one or two sentences.
            -   Example: The AI agent acts as a customer service assistant.
        -   Outline specialties:

            -   Specify the key areas or tasks that the AI agent handles.
            -   Example: Specializes in handling inquiries and resolving customer issues.
        -   Identify the business problem:

            -   Articulate the specific business challenge for the AI agent to address.
            -   Example: Reducing customer wait times by 50%.
        -   Describe the AI agent:

            -   Provide a brief scenario of how the AI agent is to be used.
            -   Example: Automating responses to common queries and escalating complex issues to human agents.
        -   Be concise and clear:

            -   Use simple and direct language.
            -   Avoid jargon and technical terms.
            -   Example: The AI agent helps customers find answers quickly.
        -   Provide actionable steps:

            -   Include specific instructions on how to set up and use the AI agent.
            -   Example: Step 1: Define the types of inquiries the AI agent handles. Step 2: Integrate the AI agent with the customer service platform.
        -   Include examples:

            -   Provide real-world examples to illustrate how the AI agent should function.
            -   Example: For example, the AI agent can automatically respond to questions about the order status.
        -   Focus on outcomes:

            -   Emphasize the benefits and outcomes of using the AI agent.
            -   Example: Using the AI agent leads to faster resolution times and higher customer satisfaction scores.
        By following these general guidelines, you can create clear and effective prompt instructions that enable you to use AI agents to their fullest potential. For more information and examples, see [General guidelines for creating AI agents and agentic workflows](../concept/gg-creating-aia.md).

    3.  Configure Access Control Lists \(ACLs\) for the AI agent.

        **Note:** The ACLs determine who has access to discover and execute the AI agent. To learn more about the ACLs you can create in AI Agent Studio and how to add more advanced security configurations, see [Implement access control in Now Assist AI agents](../concept/aia-security-implementation.md).

        This is a required step. If you have previously configured an AI agent without creating an ACL, you must generate an ACL before you can make other modifications.

        If you have already created an ACL for the AI agent, then it will appear in a list in this section. You can double-click the role pills to edit the roles.

<table id="table_rlv_bgr_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User access

</td><td>

The type of users whose access for the AI agent is defined by the following options:-   **Any authenticated user**: Any user who is logged in can access the AI agent.
-   **Users with specific roles**: Users that have at least one of the listed roles assigned to them can access the AI agent. This is the default option.

**Note:** If a user doesn't have access to an AI agent or if the user doesn't have access to at least one of the AI agents in the respective agentic workflow execution, then the whole execution aborts before the first AI agent is initiated.

-   **Public**: Any user can access the AI agent even without logging in. Use this option only when you want guests to be able to access the AI agent.


</td></tr><tr><td>

Role

</td><td>

Assign one or more specific roles from the drop-down.**Note:** Selecting the role is possible only when you chose the **Users with specific roles** user access.

</td></tr></tbody>
</table>    4.  Define the type of sys\_user the AI agent will run as.

        -   For more information about understanding the user identities that will execute the AI agent, see [User identity](../concept/aia-security-implementation.md#section_rch_xgg_hgc).
        -   For more information about understanding the rules for Access Control Lists \(ACLs\) in ServiceNow AI Platform®, see [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).
<table id="table_vjm_kpr_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run as

</td><td>

The user identity with which the AI agent runs.Select one of the following entity types that your AI agent should run as:

1.  **Dynamic user**: The logged in user \(sys\_user\) who invokes the execution of an AI agent.

The dynamic user can be the sys\_user of a trigger, agentic workflow, or human user that passes its roles to this agent \(the upstream component/entity that invoked the AI agent\).

Any execution run by a dynamic user is recorded in the name of the logged in user. For example, if an incident is created by a Dynamic user, then the incident created is recorded in the name of the currently logged in user.

**Note:** The Dynamic user is the default setting for all AI agents unless there is a specific need that justifies an AI user. Generally, most AI agents can run as dynamic users.

2.  **AI user**: The AI agent runs and executes as a preconfigured, static user identity with assigned roles that will not change regardless of who or how the execution is invoked.

The AI user is a type of sys\_user record of type AI agents. Any actions performed by an AI agent running as an AI user are recorded in the name of the AI user for that action or execution. For example, if an incident is created by an AI user, then the caller for that execution is recorded as the assigned AI user.

The AI user is a sys\_user with predefined roles.

**Warning:** Allowing public users to invoke AI users will give them elevated permissions to what data is accessible to them.

 If you do not have an AI user but want to use the **AI user** identity, you need to create a new record on the User table. See [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). Select **AI user** as the identity type.

</td></tr><tr><td>

AI user

</td><td>

Select a specific AI user from the drop-down menu.

</td></tr></tbody>
</table>        **Note:** When determining these security settings, be sure to consider the security settings for all aspects of the agentic flow, from agentic workflow, AI agents, and tools.

    5.  Specify which AI providers this AI agent does not support.

        Some AI models may perform your specific AI agent tasks better than others. You can choose an unsupported LLM from the **Select unsupported LLMs** drop-down if you do not want an AI agent to be available if a certain default AI model provider is active.

    6.  Specify categories for long-term memory.

        The choice to let an AI agent store memories about users is a general setting for long-term memory.

        -   Select **Identify Categories**.

            You see the Categories specified by the Now Assist pop-up window.

            ![The pop up window contains the list of Now Assist suggested categories based on your description and instructions for the AI agent.](../image/aia-categories.png)

        -   Add or replace the categories and select **Save**.
        For more information about setting up categories for AI agent memories, see [Set up long-term memory](long-term-memory-aia.md).

    7.  Select **Save and continue**.

        You must select **Save and continue** to create the ACL for the AI agent on the ACL table. If you want to create additional or **Deny-Unless** ACLs or add Security Attributes for the AI agent, a user with the correct elevated privileges can create them on the ACL table directly. Additional ACLs cannot be configured in AI Agent Studio.

        If you selected **Users with specific roles** for your ACL, after you've selected Save and continue, you can still edit the roles of the ACL. Return to the first page of the guided setup and double-click the role pills in the ACL section to make changes.

        You’re directed to the Add tools and information page.

4.  Select **Add tool** to equip your AI agent with various tools to accomplish its role.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add tool

</td><td>

Additional tools and data sources that you can provide your AI agent to accomplish its role. The available tools are:-   [Catalog item](add-catalog-ai-agent.md): Conversational catalog items that you can add to your AI agent.
-   [Conversational topic](add-va-topic-ai-agent.md): Use conversations to get additional information from users by adding a Virtual Agent topic to an AI agent.
-   [File upload](add-file-retrieval.md): Upload files to let AI agents analyze specialized knowledge.
-   [Flow action](add-flow-action-ai-agent.md):

Custom automated processes in your system that you can add to your AI agent.

-   [Knowledge graph](add-knowledge-graph.md): Add a knowledge graph to an AI agent in AI Agent Studio to enhance the performance of AI agents.
-   : Add a model context protocol client
-   [Now Assist Skill](add-skill-ai-agent.md): Generative AI skills in your system that you can add to your AI agent.

Example for Next Best Action AI agent: Incident summarization.

-   [Record operation](add-database-op-ai-agent.md): To create, update, look up, or delete records from an AI agent, add a record operation.
-   [Script](add-script-ai-agent.md): Editable scripts and APIs that you can add to your AI agent.

Example for the Next Best Action AI agent: Get similar incident.

-   [Search retrieval](add-retriever-ai-agent.md): Information retrieval processes in your system that you can add to your AI agent.

Example for the Next Best Action AI agent: Get relevant knowledge articles.

-   [Sub flow](add-sub-flow-ai-agent.md): Automated flows in your system that you can add to your AI agent.
-   [Add a web search to an AI agent](add-web-search-ai-agent.md): Add a web search tool to an AI agent using third-party search API such as Microsoft Bing or Google.
**Note:** You must add at least one tool to continue setting up your AI agent, but you can also add more tools to your AI agent at any point.

</td></tr></tbody>
</table>5.  Select **Save and continue**.

    You’re directed to the Define trigger page.

6.  Define a trigger and conditions for activating your AI agent.

    **Note:** Triggers are optional. If you only want your AI agent to be discoverable in chats in Now Assist in Virtual Agent, you don't need to set a trigger.

    1.  Select **Add Trigger**.

    2.  On the form, fill in the fields.

<table id="table_dw3_czl_zcc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select trigger

</td><td>

List of triggers that are available in the instance.

</td></tr><tr><td>

Name

</td><td>

Name of the trigger.

</td></tr><tr><td>

Active

</td><td>

Option to keep your trigger conditions active.

</td></tr><tr><td>

Table

</td><td>

Name of the applicable table for your agentic workflow.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that you can add to control the trigger configuration.Select **+ Add condition set** to add conditions to your agentic workflow trigger.

</td></tr><tr><td>

Method of defining sys\_user

</td><td>

-   Use an existing table
-   Use a new custom script


</td></tr><tr><td>

Sys\_user

</td><td>

The user that the AI agent runs as.

 If you select a table, then the choices could include the Caller, Resolved by, Closed by, or another user field. You can also create a custom script to generate and return the sys\_id of the user.

</td></tr><tr><td>

Objective template

</td><td>

Template instruction for an AI agent to follow during its execution.

 For some trigger types, you can also select additional fields in your template instructions.

</td></tr><tr><td>

Channel

</td><td>

Medium for the AI agent output: Now Assist panel or Virtual Agent.

**Note:**

-   If you select Virtual Agent, then you must select the assistant and portal where the AI agent is available.
-   To view the output from a triggered AI agent in the Now Assist panel, you need the now\_assist\_panel\_user role.


</td></tr><tr><td>

Show notification

</td><td>

Select the **Show Notification** option to enable notifications for your triggers.

 If there are multiple triggers with notifications enabled for the same table, only one notification will show.

</td></tr></tbody>
</table>        If you choose a scheduled trigger, additional options are available, such as the day of the week and time when you want the trigger to run.

        **Note:** When running a scheduled trigger, not every record is included in the execution. By default, the value is 10. If you want to change this number, you must set the **sn\_aia.max\_scheduled\_trigger\_query** system property to a different value.

        If you choose an email trigger, the target emails must exist on the Reply \[sys\_reply\] table. New emails aren’t available as triggers.

    3.  Select **Add**.

        You’re directed to the Define trigger page.

    4.  Select **Save and continue**.

        You’re directed to the AI agent availability page.

7.  Define AI agent availability.

    1.  Turn on the AI agent by toggling the **Status**, then select if the AI agent should be displayed in the Now Assist panel or Virtual Agent.

        **Note:** You must toggle the **Status** to activate your AI agent, but selecting either Now Assist panel or Virtual Agent is optional. Only enable them if you want your AI agent to be available in those channels. If you only plan to trigger your AI agent by other means, you don't need to enable either.

        You can select the chevron icon \(![Chevron icon.](../../../reuse/icons/product-icons/chevron-right-fill-24.svg)\) to choose which roles are required to access the AI agent.

        ![Toggle display in the AI agent guided setup with options for turning on the AI agent and selecting either Now Assist panel or Virtual Agent](../image/aia-select-display-new.png)

        **Note:** If the Now Assist panel display option isn’t available, you must enable the panel first. For more information, see [Turn on the Now Assist panel](../../now-assist-admin/task/activate-now-assist-panel.md).

    2.  Provide a processing message in the **Processing message** field of the Create a processing message section, to be displayed in the selected channel when the AI agent starts working.

        For example, **Initiating AI agent** or **Processing record details**, or **An AI agent is looking into the request**.

8.  Select **Save and test** to complete the configuration steps or review a previous step by selecting **Back**.

    Selecting Save and test leads you to the AI agent testing page, where you can test the AI agent that you created. For more information, see [Test an AI agent](test-ai-agent.md).

    To test the agentic workflow, you must have the sn\_aia.admin role and any roles the ACL configured for the AI agent requires, if applicable.


## Result

You can see the AI agent that you created in the **Manage agentic workflows and AI agents** page.

If you selected **Users with specific roles** for your ACL, you can change roles at any point. Return to the guided setup and double-click the pills to make changes. All other security changes must be done on the ACL \[sys\_security\_acl\] table by a user with elevated permissions.

