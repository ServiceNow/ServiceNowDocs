---
title: Create an external AI agent with the Agent2Agent protocol
description: Create external AI agents in AI Agent Studio to connect the ServiceNow AI Platform with third-party agentic AI providers.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 6
breadcrumb: [Create an external agent, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Create an external AI agent with the Agent2Agent protocol

Create external AI agents in AI Agent Studio to connect the ServiceNow AI Platform with third-party agentic AI providers.

## Before you begin

If you don’t see the option to create an external agent, confirm that your administrator has selected **Allow ServiceNow to access External AI Agents**. This option is available on the **Settings** page in AI Agent Studio, under **External AI Agents** &gt; **Discoverability**.

Your instance must be at least on Zurich patch 4.

Role required: sn\_aia.admin

## About this task

You can integrate third-party AI providers into the ServiceNow AI Platform by creating an external AI agent in AI Agent Studio.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**.

2.  Select **New** &gt; **External**.

3.  In the **Discover and activate** step, select the AI agent provider for your external agent and discover your agent.

    Select **Save and continue** to navigate to the next step.

    1.  Select an existing provider or add a new provider.

        If you select **Add new provider**, you must fill out the fields and then select **Save**.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the agentic AI provider.

</td></tr><tr><td>

Agent card URL

</td><td>

The URL that points to the external AI agent's Agent Card. The URL should include `well_known/agent_json`.

</td></tr><tr><td>

Under **Advanced settings**, Connection &amp; Credential alias

</td><td>

Credentials to access your external AI agent's Agent Card. You can select an existing alias or create one.

</td></tr><tr><td>

Under **Advanced settings**, Select subflow

</td><td>

Subflow that establishes Agent2Agent protocol. The default subflow should handle the majority of cases, but you can also create your own.

</td></tr></tbody>
</table>    2.  Select **Discover external AI agent** to validate the connection to your external agent.

        If discovery is successful, the name of your agent and the version number are added to the page below the Discover external AI agent button.

        ![Discover external AI agent showing a discovered AI agent](../image/external-aia-a2a-discovery.png)

    3.  Select the name of the agent to verify that the **Name**, **Version**, **Description**, and **Skills** fields are populated correctly, then select **Activate**.

        The **Agent card** tab shows the entire JSON for the agent.

        ![Summary of AI agent details and activate button](../image/external-aia-a2a-activate.png)

4.  In the **Review skills and capabilities** step, verify that the skill names are correct.

5.  In the **Define the specialty** step, add details for how the external agent fits in the ServiceNow agentic system.

    1.  Review your AI agent description.

        You can leave your AI agent description as it is, or you can add a longer description to help differentiate the agent from other AI agents. This helps enable the AI Agent Orchestrator to use your external AI agent more effectively. For suggestions for writing AI agent descriptions, see [General guidelines for creating AI agents and agentic workflows](../concept/gg-creating-aia.md).

    2.  Set your communication mode to either **Synchronous** or **Asynchronous**.

        Some agents don’t support asynchronous communication.

        Under **Advanced settings**, you can use the default subflow, an existing subflow, or create a subflow. The default subflow should work for the majority of cases.

    3.  Select your AI agent's execution Connection &amp; Credential alias for authentication.

        Choose which credentials access your external AI agent's execution endpoint. You can select an existing alias or create one. If you create one, a modal displays with options for configuring an OAuth or API Key authentication.

        ![Summary of AI agent details and activate button](../image/external-aia-a2a-define.png)

    4.  Configure access control lists \(ACLs\) for the AI agent.

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
-   **Users with specific roles**: Users that have at least one of the roles assigned to them can access the AI agent. This option is the default.

**Note:** If a user doesn't have access to an AI agent or if the user doesn't have access to at least one of the AI agents in the respective agentic workflow execution, then the whole execution aborts before the first AI agent is initiated.

-   **Public**: Any user can access the AI agent even without logging in. Use this option only when you want guests to be able to access the AI agent.


</td></tr><tr><td>

Role

</td><td>

Assign one or more specific roles from the drop-down menu.**Note:** Selecting the role is possible only when you chose the **Users with specific roles** user access.

</td></tr></tbody>
</table>6.  In the **Select a display** step, choose where you want the AI agent to appear and what message users see when the AI agent is running.

    1.  Select your AI agent's availability.

        Set the **Status** to active if you want the AI agent to be available to users with the correct role.

    2.  Select a display channel.

        You can choose to use a Virtual Agent and specify which assistant you want to access the AI agent. If you want to test the AI agent first, you don’t need to select a display channel yet.

    3.  Choose processing messages to display to the user when the AI agent is executing.

        For example, **Initiating AI agent** or **Processing record details**, or **An AI agent is looking into the request**.

    4.  Activate the AI agent.

        Select the toggle to activate the AI agent if you want the AI agent to be discoverable. If you want to test your AI agent first, wait until after you have tested it before activating it.

        If you don't see this option, you may need to scroll.

    ![Select a display step](../image/external-aia-a2a-display.png)

7.  Select **Save and test** to save the AI agent details and go to the Testing page of AI Agent Studio.


## Result

Your external AI agent is connected to ServiceNow.

## What to do next

You can [test an execution of your AI agent](test-ai-agent.md) or [its data access](test-aia-access.md). You can also add it to a new or existing agentic workflow. See [Create an agentic workflow](configure-use-case-ai-agents.md) for the steps to create or configure an agentic workflow.

**Parent Topic:**[Create an external AI agent](../concept/create-external-aia.md)

