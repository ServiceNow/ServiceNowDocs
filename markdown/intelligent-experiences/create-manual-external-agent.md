---
title: Create an external AI agent with manual integration
description: Create an external AI agent by manually integrating a third-party agent in AI Agent Studio to use in agentic workflows.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 5
keywords: [servicenow protocol, manual integration]
breadcrumb: [Create an external agent, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Create an external AI agent with manual integration

Create an external AI agent by manually integrating a third-party agent in AI Agent Studio to use in agentic workflows.

## Before you begin

If you don’t see the option to create an external agent, confirm that your administrator has selected **Allow ServiceNow to access External AI Agents**. This option is available on the **Settings** page in AI Agent Studio, under **External AI Agents** &gt; **Discoverability**.

Your instance must be at least on Zurich patch 4.

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Select **New** &gt; **External**.

3.  Select the **Manual integration** method.

4.  In the **Connect a provider** step, complete the form fields to connect to your AI agent.

    1.  In the **Enter details about the provider section**, select the alias and subflow for your external AI agent.

        Your alias should point to the agentic AI provider and include an authentication token. You can create an alias by selecting **Create new alias**. After the record is created, you can refresh or start the guided setup again to see the new option.

        The **API type** is `Subflow`. Select a subflow that matches the provider. You can create your own by selecting **Create a new subflow**.

    2.  In the **Enter initial details about the external AI agent** section, complete the fields.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent ID

</td><td>

Unique identifier for your agent according to your agentic AI provider.

</td></tr><tr><td>

Metadata

</td><td>

Structured JSON that includes the required fields for your AI agent to function, for example, the **model** that the AI agent uses.

</td></tr><tr><td>

Communication mode

</td><td>

Either `Synchronous` \(real-time\) or `Asynchronous` \(allows for delay\).

</td></tr><tr><td>

Analyze response

</td><td>

Either `true` or `false`.

</td></tr></tbody>
</table>    Select **Save and continue** to navigate to the next step.

    ![Connect a provider guided setup step](../image/external-aia-man-connect.png)

5.  In the **Define the specialty** step, add details about the AI agent to give the AI Agent Orchestrator context for how to use the agent in agentic workflows.

    These fields provide context for the AI Agent Orchestrator to help understand the functions and steps required for the AI agent to have served its purpose within the workflow. Detailed role and instruction information create more effective AI agents. For suggestions for writing AI agent roles and instructions, see [General guidelines for creating AI agents and agentic workflows](../concept/gg-creating-aia.md).

    1.  In the Describe the AI agent section, add a name and description for your external AI Agent.

        The name and description field are used by the AI Agent Orchestrator to help determine when to use your AI agent. The more thorough your description, the more likely the AI agent is to be used correctly within the agentic workflow.

        You can select **Use Now Assist** to help generate the content for the name, description, AI agent role, and instructions fields. You can still change these fields are generated.

    2.  In the Instruct the AI agent section, add the AI agent role and instructions.

    3.  Configure access control lists \(ACLs\) for the AI agent.

        **Note:** The ACLs determine who has access to discover and execute the AI agent. To learn more about the ACLs you can create in AI Agent Studio and how to add more advanced security configurations, see [Implement access control in Now Assist AI agents](../concept/aia-security-implementation.md).

        This is a required step. If you have previously configured an AI agent without creating an ACL, you must generate an ACL before you can make other modifications.

<table id="table_rlv_bgr_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User access

</td><td>

The type of users whose access for the AI agent is defined by the following options:-   **Any authenticated user**: Any user who is logged in can access the AI agent.
-   **Users with specific roles**: Users that have at least one of the roles assigned to them can access the AI agent. This is the default option.

**Note:** If a user doesn't have access to an AI agent or if the user doesn't have access to at least one of the AI agents in the respective agentic workflow execution, then the whole execution aborts before the first AI agent is initiated.

-   **Public**: Any user can access the AI agent even without logging in. Use this option only when you want guests to be able to access the AI agent.


</td></tr><tr><td>

Role

</td><td>

Assign one or more specific roles from the drop-down menu.**Note:** Selecting the role is possible only when you chose the **Users with specific roles** user access.

</td></tr></tbody>
</table>    ![Define the specialty step](../image/external-aia-man-define.png)

6.  In the **Select a display** step, choose where you want the AI agent to appear and what message users see when the AI agent is running.

    1.  Select your AI agent's availability.

        Set the **Status** to active if you want the AI agent to be available to users with the correct role.

    2.  Select a display channel.

        You can choose to use a Virtual Agent and specify which assistant you want to access the AI agent. if you want to test the AI agent first, you don’t need to select a display channel yet.

    3.  Choose processing messages to display to the user when the AI agent is executing.

        For example, **Initiating AI agent** or **Processing record details**, or **An AI agent is looking into the request**.

    4.  Activate the AI agent.

        Select the toggle to activate the AI agent if you want the AI agent to be discoverable. If you want to test your AI agent first, wait until after you have tested it before activating it.

        If you don't see this option, you may need to scroll.

    ![Select a display step](../image/external-aia-a2a-display.png)

7.  Select **Save and test** to save the AI agent details and go to the Testing page of AI Agent Studio.


## Result

Your external AI agent is connected to the ServiceNow AI Platform.

## What to do next

You can [test an execution of your AI agent](test-ai-agent.md) or [its data access](test-aia-access.md). You can also add it to a new or existing agentic workflow. See [Create an agentic workflow](configure-use-case-ai-agents.md) for the steps to create or configure an agentic workflow.

**Parent Topic:**[Create an external AI agent](../concept/create-external-aia.md)

