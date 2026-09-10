---
title: Create an external AI agent
description: Create external AI agents in AI Agent Studio to connect the ServiceNow AI Platform with third-party agentic AI providers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-a2a-agent-new.html
release: australia
topic_type: task
last_updated: "2026-08-28"
reading_time_minutes: 6
breadcrumb: [Integrate external AI agents, AI Agent Studio, Enable AI experiences]
---

# Create an external AI agent

Create external AI agents in AI Agent Studio to connect the ServiceNow AI Platform with third-party agentic AI providers.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Home** &gt; **Create new agentic solution** and select **New AI agent for a task**.

2.  On the New AI Agent pop-up, select **Create an external agent instead**.

3.  Discover and select an external AI agent through a provider.

    1.  On the New external AI agent form, select an AI agent provider from the **Provider** drop-down or add a provider.

        If you select a **Add new provider**, fill in the fields and select **Add**.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the agentic AI provider.|
        |Discovery type| |
        |Agent card URL|The URL that points to the external AI agent's Agent Card. The URL should include `.well_known/agent_json`.|
        |Advanced settings|
        |Connection and credential alias|Credentials to access your external AI agent's Agent Card. You can select an existing alias or create one.|
        |Select Subflow|Subflow that establishes Agent2Agent protocol. The default subflow should handle the majority of cases, but you can also create your own.|

        **Note:** Additionally, you can view and edit the provider details by selecting **View provider details**.

    2.  Select **Discover external AI agent** to validate the connection to your external agent.

        If discovery is successful, the name of your agent and the version number are added to the page.\[Omitted image "discover-a2a.png"\] Alt text: Discover external AI agent showing a discovered AI agent

    3.  Select the name of the agent to verify that the **Basic Info** and **Agent card** details.

        \[Omitted image "a2a-summary-select.png"\] Alt text: Summary of AI agent details and activate button

        -   The **Basic info** tab contains the **Name**, **Version**, **Description**, **Skills**, and **Agent details**.
        -   The **Agent card** tab shows the entire JSON for the agent.
    4.  Select **Save and continue**.

    The guided setup for the selected external AI agent is now available.\[Omitted image "a2a-guided-setup.png"\] Alt text: The external AI agent guided setup.

4.  Describe and instruct the external AI agent by adding details for how it fits in the ServiceNow agentic system.

    Describe your external AI agent with a name and description. You must also select the communication mode for the external AI agent along with the subflow. You can leave your external AI agent description as it is, or you can add a longer description to help differentiate the agent from other external AI agents. This helps enable the external AI Agent Orchestrator to use your external AI agent more effectively.

    1.  Verify the **Name** and **Description** to summarize the main intention of the external AI agent.

        **Note:** If the name and description aren't clear or correct, the Orchestrator won't know how to wield the external AI agent in context.

    2.  Set your communication mode under **Communication mode** to one of the following:

        -   **Synchronous**: ServiceNow Exchanges data with the external AI agent in real-time and waits for an immediate response. The synchronous mode is selected by default.
        -   **Asynchronous**: ServiceNow exchanges data with the external AI agent and continues processing without waiting for an immediate response.

            **Note:** Asynchronous connection involves communication where the sender and receiver don't have to be active simultaneously unlike the synchronous communication mode.

            To establish asynchronous connection, you must obtain a callback URL for push notifications to function. Once you have obtained a callback URL, you must create a record on the External Agent Callback Registries \[sn\_aia\_external\_agent\_callback\_registry\] table. Go to the table, select **New**, and enter the callback URL. Save the record.

            After saving the record, a Connection &amp; Credential Alias \[sys\_alias\] record is created for you. To add authentication, you can open the Connection record associated with the sys\_alias record and add a credential to the **Credential** field. When the record is created, you can go back to the External Agent Callback Registry record you created and select **Verify URL** to test that the connection works as expected.

        **Note:** Some agents don’t support asynchronous communication.

    3.  Select a subflow under **Advanced settings**.

        You can use either the default subflow; which is **External AI Agent Card - A2A Protocol**, or an existing subflow from the **Select subflow** drop-down, or create a subflow. The default subflow should work for the majority of cases.

5.  Add authentication for an external AI agent using the connection and credential alias.

    Choose which credentials access your external AI agent's execution endpoint. You can select an existing alias or create one. If you create one, a modal displays with options for configuring an OAuth or API Key authentication.

    **Note:** For more information about the API Key credential, see [A2A API Key credential behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/a2a-api-key-credential-behavior.md).

6.  Configure access control lists \(ACLs\) for the external AI agent.

    **Note:** The ACLs determine who has access to discover and execute the AI agent. To learn more about the ACLs you can create in AI Agent Studio and how to add more advanced security configurations, see [Implement access control in AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/implement-aias-security-new.md).

    **Important:** This is a required step. If you have previously configured an external AI agent without creating an ACL, you must generate an ACL before you can make other modifications.

<table id="table_ykn_x4g_kkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User access

</td><td>

The type of users whose access for the AI agent is defined by the following options:-   **Any authenticated user**: Any user who is logged in can access the external AI agent.
-   **Users with specific roles**: Users that have at least one of the roles assigned to them can access the external AI agent. This option is the default.

**Note:** If a user doesn't have access to an external AI agent or if the user doesn't have access to at least one of the external AI agents in the respective agentic workflow execution, then the whole execution aborts before the first external AI agent is initiated.

-   **Public**: Any user can access the external AI agent even without logging in. Use this option only when you want guests to be able to access the external AI agent.

**Note:** Understand that this configuration should be used sparingly and only when needed.

</td></tr><tr><td>

Role

</td><td>

Assign one or more specific roles from the drop-down menu.**Note:** Selecting the role is possible only when you chose the **Users with specific roles** user access.

</td></tr></tbody>
</table>7.  Select a display channel where your external AI agent can be discovered.

    -   **ServiceNow Otto panel**: Users can discover and invoke this external AI agent from the ServiceNow Otto panel.
    -   **ServiceNow Otto chat assistants**: Users can discover and invoke this external AI agent from the chat assistant.
    **Note:** Both the display options are turned off by default. Choose one or both as the channel display for your external AI agent.

8.  Communicate the external AI agent's process to users.

    -   **Context for the messages**: Describe what you external agent is set to do.
    -   **In-progress message**: Choose processing messages to display to the user when the external AI agent is executing.

        For example, `Initiating AI agent` or `Processing record details`, or `An AI agent is looking into the request`.

    -   **Completion message**: Provide a completion message to display to the user when an external AI agent is done executing.

        For example: `Identified next steps` or `Processed the record details`.

    -   Select **Generate messages**.
9.  Select **Activate**.


## Result

Your external AI agent is configured with the context necessary for it to be used by the external AI Agent Orchestrator. It has the required information to accomplish its intended tasks.

## What to do next

You can [test your AI agent on a record manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-asset-new.md) to see an example execution. You can also [create an automated agentic evaluation to test the AI agent over repeated interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/launch-aia-eval.md). Automated evaluations can recommend specific optimizations if the LLM judges find underlying patterns for low success rates.

Activate your AI agent and make it ready for use by selecting **Activate**.

**Note:** The status of the external AI agent is shown as **Inactive** until it is activated.

