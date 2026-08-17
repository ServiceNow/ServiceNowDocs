---
title: Combined AI Agent Studio release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for AI Agent Studio from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-aiagentstudio-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 23
breadcrumb: [Products combined by family]
---

# Combined AI Agent Studio release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for AI Agent Studio from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Agent Studio release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Agent Studio to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for AI Agent Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&family=zurich&ft:locale=en-US)**

The AI-native experience for an AI agent is available exclusively with the installation of the Off Glide Conversation Server plugin \(com.glide.cs.offglide\).

**Note:** To use the AI agent in AI-native mode, make sure to test it so it works as expected.

-   **[Test an agentic solution in Premium Chat mode](https://www.servicenow.com/docs/access?context=test-ai-agent&family=zurich&ft:locale=en-US)**

Use the Premium Chat playground experience to test your agentic solutions.

**Note:** The AI-native playground experience is exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard testing playground.

-   **[Add tools and information](https://www.servicenow.com/docs/access?context=add-tool-aia&family=zurich&ft:locale=en-US)**

Add widgets for tool outputs to provide an improved experience in AI-native mode.

**Note:** The display output widget options are exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard add tool form.


-   **[Evaluate voice AI agents for overall task completion and tool choice accuracy](https://www.servicenow.com/docs/access?context=execute-aia-eval&family=zurich&ft:locale=en-US)**

Automated evaluations support voice AI agents. Get a better picture of overall performance by evaluating previous executions against standardized metrics.


-   **[ServiceNow AI agents as secondary agents](https://www.servicenow.com/docs/access?context=secondary-agent&family=zurich&ft:locale=en-US)**

Enhance user experience for Secondary Agents by displaying the Agent card URL to admins for easy access and management so the admin can view, copy, and consume the URL easily.

Additionally, when adding an MCP tool, the name and description of the tool are populated automatically as per the details fetched from the server and the user can update the details.


-   **[Configure role masking for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Role masking restricts access to specific roles based on configuration to verify that agentic workflows, AI agents, and tools run within the boundaries of the roles configured to meet their business needs while reducing the risk of unauthorized access to the agents and the agentic data.

-   **[Add AI agent learning](https://www.servicenow.com/docs/access?context=agent-learning&family=zurich&ft:locale=en-US)**

Enhance AI agent learning through episodic memory, enabling AI agents to improve by learning from past successful interactions.

-   **[Select channels and access](https://www.servicenow.com/docs/access?context=channels-access-aw&family=zurich&ft:locale=en-US)**

Create and update UI actions for workflow executions and display handling. You can specify conditions for the display of the UI actions.

-   **[Defined desktop action for desktop and web-based tasks](https://www.servicenow.com/docs/access?context=add-desktop-action-ai-agent&family=zurich&ft:locale=en-US)**

Add Desktop action as a tool to an AI agent to perform desktop automation for repetitive tasks.

-   **[Configure](https://www.servicenow.com/docs/access?context=configuring-ai-agents&family=zurich&ft:locale=en-US)**

Support multilingual conversations for AI agents across languages.

-   **[Test execution manually](https://www.servicenow.com/docs/access?context=test-ai-agent&family=zurich&ft:locale=en-US) and [Test execution manually](https://www.servicenow.com/docs/access?context=test-aia-use-case&family=zurich&ft:locale=en-US)**

The testing page on AI Agent Studio has two testing options:

    -   Manual test
    -   Automated evaluation
Observe the different versions of an AI agent behavior in manual tests and in automated evaluations using the **Manual tests** and **Automated tests** tabs.

-   **[Test user access](https://www.servicenow.com/docs/access?context=test-aia-access&family=zurich&ft:locale=en-US) and [Test user access](https://www.servicenow.com/docs/access?context=test-aw-access&family=zurich&ft:locale=en-US)**

Test how an AI agent or agentic workflow completes a task and if it enables users permission to access it.

-   **[Model Context Protocol Client](https://www.servicenow.com/docs/access?context=mcp-client&family=zurich&ft:locale=en-US)**
    -   Authorization upgrades to support segregation of Resource Server and Authentication Server through Protected Resource Metadata \(PRM\).
    -   Use the **mcp\_guardian\_check** property to enable guardian checks for MCP Client when there’s an MCP tool call.
    -   Supervise the pagination with mouse device support to show large number of services from an MCP server through the **sn\_mcp\_client.cursor.max\_iterations** system property.
    -   Add a title field for human-friendly display names that can be used as a programmatic identifier.
-   **[Use in-product experiences for agentic workflows on forms](https://www.servicenow.com/docs/access?context=in-product-agentic-ai&family=zurich&ft:locale=en-US)**

In the Core UI and workspaces, you can use UI and declarative actions to run agentic workflows. You can also see the presence, progress, and output of agentic workflows performed on a record. The execution details for each agentic workflow include who is supervising the workflow, estimated and total time taken, processing messages, and step history.

-   **[Review and approve requests and tickets with the Approval Assistance AI agent](https://www.servicenow.com/docs/access?context=platform-approval-aia&family=zurich&ft:locale=en-US)**

You can use the new approval assistance AI agent to view all pending approval requests and access detailed information about them. You can then approve requests and tickets and make updates to them from ServiceNow Otto in Virtual Agent.

-   **[View the Approval Info Record widget](https://www.servicenow.com/docs/access?context=approval-info-record-widget&family=zurich&ft:locale=en-US)**

The Service Portal Approval Info Record widget shows details about the approval request and a full record for an approval including the activity stream.

-   **[Configure email notification alerts for AI agent and agentic workflow executions](https://www.servicenow.com/docs/access?context=config-aia-notifications&family=zurich&ft:locale=en-US)**

Configure alert email notifications for unexpected or undesired behavior from AI agents and agentic workflows. You can configure the thresholds for triggering the alerts on the Agent Properties table, and you can add or update the recipients of the email notifications from the Notifications table.

-   **[Create an external agent](https://www.servicenow.com/docs/access?context=create-external-aia&family=zurich&ft:locale=en-US)**

Create new external AI agents that connect to third-party agentic AI systems. Use Agent2Agent protocol or integrate agents manually to configure them in AI Agent Studio to use in the ServiceNow agentic AI system.

-   **[Knowledge Graph](https://www.servicenow.com/docs/access?context=add-knowledge-graph&family=zurich&ft:locale=en-US)**

Use Enterprise Graph \(Small\) as a resource to create a Knowledge Graph tool for an AI agent in the AI Agent Studio.


-   **[Add MCP tool](https://www.servicenow.com/docs/access?context=add-mcp-server-tool&family=zurich&ft:locale=en-US)**

The Model Context Protocol Client enables guardian checks for offensive content when Notion is selected as the MCP server.

-   **[Configure Model Context Protocol Client](https://www.servicenow.com/docs/access?context=configuring-mcp-client&family=zurich&ft:locale=en-US)**

The Model Context Protocol Client application supports the latest MCP version.

-   **[Knowledge Graph](https://www.servicenow.com/docs/access?context=add-knowledge-graph&family=zurich&ft:locale=en-US)**

Use Global Graph as a Knowledge Graph resource when creating a Knowledge Graph tool for an AI agent in the AI Agent Studio.


-   **[Model Context Protocol Client](https://www.servicenow.com/docs/access?context=mcp-client&family=zurich&ft:locale=en-US)**

Enable users of the ServiceNow® AI Agent Studio to access tools that are hosted externally and published using an MCP server via the Model Context Protocol Client application.

Authenticate users with the MCP server to add the MCP tool to an AI agent.

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&family=zurich&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Review agentic activity in AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&family=zurich&ft:locale=en-US)**

View and troubleshoot the agentic workflow and AI agent executions on AI Agent Studio via the **Activity** page.

-   **[Configure](https://www.servicenow.com/docs/access?context=configuring-ai-agents&family=zurich&ft:locale=en-US) - Dynamic Orchestrator**

Maps the appropriate agents for an agentic workflow with Dynamic Orchestrator for better performance and accuracy of the agentic workflow execution.

-   **[View analytics for customer satisfaction with AI interactions](https://www.servicenow.com/docs/access?context=ai-agent-dashboard&family=zurich&ft:locale=en-US)**

Multiple new metrics have been added to the AI Agent Analytics dashboard, accessible from the AI Agent Studio to provide insight into average customer satisfaction and customer satisfaction with the best and worst performing agentic workflows and agents.

-   **[New third-party AI model provider options available for all AI applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

-   **[Add tools and information](https://www.servicenow.com/docs/access?context=add-tool-aia&family=zurich&ft:locale=en-US)**

The output transformation strategy for an AI agent output contains a new option called **Custom**. Using the custom output transformation strategy, the tool output gets transformed according to the LLM instructions.

-   **[Configure](https://www.servicenow.com/docs/access?context=configuring-ai-agents&family=zurich&ft:locale=en-US) - AI Agent Background Channel**

Invoke the agentic conversations from Workspace or Core UI via the AI Agent Background channel that is associated with the AI Agent Background Provider to execute the AI agents and agentic workflows.

-   **[Configure](https://www.servicenow.com/docs/access?context=configuring-ai-agents&family=zurich&ft:locale=en-US) - Interactive and non interactive AI agents**

Run AI agents and agentic workflows execution in one of the following ways:

    -   **Interactive Mode**: AI agents reach out to the user for information during fallback.
    -   **Non interactive Mode**: AI agents don’t reach out to the user during fallback but send the execution output to the user.

</td></tr><tr><td>

Australia

</td><td>

-   **[Integrating external AI agents](https://www.servicenow.com/docs/access?context=external-agent-protocols&family=australia&ft:locale=en-US)**

External agents now support custom HTTP headers in the External Agent Configuration \[sn\_aia\_external\_agent\_configuration\] table. Specify headers in JSON format to have them automatically included in API calls to external endpoints, regardless of the connection type. This is useful for passing metadata and authentication requirements that your external systems require.


-   **[Knowledge Graph](https://www.servicenow.com/docs/access?context=add-knowledge-graph&family=australia&ft:locale=en-US)**

The Knowledge Graph tool configuration in AI Agent Studio has a **Conversation history** toggle that is enabled by default. When enabled, the last 5 conversation turns from the active session are passed to the KG tool allowing users to ask follow-up questions that reference the previous results.

-   **[Kill Switch](https://www.servicenow.com/docs/access?context=aia-kill-switch&family=australia&ft:locale=en-US)**

Runaway agent detection automatically disables an AI agent when the same record repeatedly triggers the same agent objective beyond a configured threshold, preventing unintended consumption of requests.

-   **[AI Agent Studio skills migration](https://www.servicenow.com/docs/access?context=configuring-ai-agents&family=australia&ft:locale=en-US)**

Auto-migrate all the AI Agent Studio skills from on-glide execution path to the off-glide execution path.

-   **[Deny-by-default ACL configuration](https://www.servicenow.com/docs/access?context=aia-acl-configuration&family=australia&ft:locale=en-US)**

Enforce deny-by-default access control for AI agentic record types \(`gen_ai_agent`, `gen_ai_workflow`, `gen_ai_skill`, `Flow`, `flow_action`\) for newly activated ServiceNow instances. In previous releases, these types defaulted to allow access.

-   **[Execute a run for an AI voice agentic asset](https://www.servicenow.com/docs/access?context=execute-voice-aia-eval&family=australia&ft:locale=en-US)**

Automated agentic evaluations are now available for voice agents. You can generate conversations based on scenarios that are described or input manually to generate execution logs for voice agents for evaluation.


-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&family=australia&ft:locale=en-US)**

The AI-native experience for an AI agent is available exclusively with the installation of the Off Glide Conversation Server plugin \(com.glide.cs.offglide\).

**Note:** To use the AI agent in AI-native mode, make sure to test it so it works as expected.

-   **[Test an agentic solution in AI Native mode](https://www.servicenow.com/docs/access?context=test-ai-agent&family=australia&ft:locale=en-US)**

Use the AI Native playground experience to test your agentic solutions.

**Note:** The AI-native playground experience is exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard testing playground.

-   **[Add tools and information](https://www.servicenow.com/docs/access?context=add-tool-aia&family=australia&ft:locale=en-US)**

Add widgets for tool outputs to provide an improved experience in AI-native mode.

**Note:** The display output widget options are exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard add tool form.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing AI Agent Studio features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Set up AI agents](https://www.servicenow.com/docs/access?context=set-up-na-aia&family=zurich&ft:locale=en-US)**

Use GPT-5.4 as the default model for the Orchestrator when Azure OpenAI is the selected LLM.

-   **[Select the model provider](https://www.servicenow.com/docs/access?context=select-aia-llm&family=zurich&ft:locale=en-US)**

The default third-party \(3P\) models have been upgraded to the latest versions - GPT 5.2 to GPT 5.4 to use AI Agents.

The new generative AI Config property records **sys\_generative\_ai\_config** and **sys\_generative\_ai\_prompt\_config** have been introduced for the following model providers:

    -   Amazon Bedrock: claude-sonnet-4-6
    -   Azure OpenAI: gpt 5.4
-   **[Platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&family=zurich&ft:locale=en-US)**

The following platform agentic workflows had updates to their admin configurations and behavior in user-generated sessions.

    -   [Analyze task trends](https://www.servicenow.com/docs/access?context=incident-trends&family=zurich&ft:locale=en-US): Admin configurations for additional filters such as category and service have been added.
    -   [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&family=zurich&ft:locale=en-US): Additional reasoning information for the generated work plan is now displayed after the plan is created.
    -   [Identify ways to improve services](https://www.servicenow.com/docs/access?context=service-improvement&family=zurich&ft:locale=en-US): Admin configurations for additional filters such as category and service have been added.

-   **[Enable UI validation for agentic AI processes and generative AI skills](https://www.servicenow.com/docs/access?context=na-aia-reference&family=zurich&ft:locale=en-US)**

The glide.ai\_record\_activity.validation.feature.enabled system property enables UI rule validation \(such as required fields\) for AI‑initiated record updates. You can selectively apply this validation based on execution context using additional system properties. For example, glide.ai\_record\_activity.ai\_detection.nap.enabled applies validation to record updates triggered from the ServiceNow Otto panel. Similar properties control validation for AI skills, Virtual Agent, and agent‑initiated actions, as listed in the [Reference for Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-aia-reference&family=zurich&ft:locale=en-US). This feature is opt‑in and disabled by default.

-   **[External agents with Agent2Agent](https://www.servicenow.com/docs/access?context=create-a2a-agent&family=zurich&ft:locale=en-US)**

The agent to agent flow actions no longer inject an `Authorization: Bearer` header automatically. If your endpoint requires a Bearer token, include the prefix directly in the API Key credential value.


-   **[External agents with Agent2Agent](https://www.servicenow.com/docs/access?context=create-a2a-agent&family=zurich&ft:locale=en-US)**

Use the A2A Protocol integration for creating external agents in the AI Agent Studio to connect with the ServiceNow AI Platform.

-   **[Updates to platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&family=zurich&ft:locale=en-US)**

Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Analyze task trends](https://www.servicenow.com/docs/access?context=incident-trends&family=zurich&ft:locale=en-US) and [Identify ways to improve service](https://www.servicenow.com/docs/access?context=service-improvement&family=zurich&ft:locale=en-US) now have post-analysis actions, including the option to download analysis and ask additional information. [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&family=zurich&ft:locale=en-US) can run as a scheduled job.

-   **[Agentic evaluation offer issue tracing and suggested optimizations](https://www.servicenow.com/docs/access?context=agentic-evals&family=zurich&ft:locale=en-US)**

After an automated evaluation of an agentic AI asset, you can receive a list of issues and suggested optimizations to address those issues. Issues come with individual record node-by-node traces to pinpoint the exact source of problems. Optimizations are suggested, and you can apply them and run a reevaluation from a single guided flow.


-   **[Updates to platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&family=zurich&ft:locale=en-US)**

Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Generate resolution plans](https://www.servicenow.com/docs/access?context=resolve-requests&family=zurich&ft:locale=en-US) now takes related records into account when planning next steps. [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&family=zurich&ft:locale=en-US) shows suggested next steps and reruns after work is done. [Process images for new tasks](https://www.servicenow.com/docs/access?context=images-tasks&family=zurich&ft:locale=en-US) now links to the created task record upon creation and includes certain metadata from the image.


-   **[Changes to AI usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Request status AI agent](https://www.servicenow.com/docs/access?context=ticket-status-aia&family=zurich&ft:locale=en-US)**

The request status AI agent provides an AI-generated summary of the most recent comments from the AI agent or other people working on a ticket. You can add attachments to an open ticket or incident to support a request action. To find more information about an open ticket, you can ask the request status AI agent follow-up questions based on previous answers from the agent.

-   **[Understand AI agents](https://www.servicenow.com/docs/access?context=understand-na-aia&family=zurich&ft:locale=en-US)**

The base reflection prompt has been replaced with the ReAct Orchestrator prompt, introducing a Route scheduling mode when an agent needs assistance from another agent during execution.

-   **[Configure](https://www.servicenow.com/docs/access?context=configuring-ai-agents&family=zurich&ft:locale=en-US)**

Run AI agents and agentic workflows concurrently in AI Agent Background Channel and in Non-interactive mode.

-   **[Knowledge Graph](https://www.servicenow.com/docs/access?context=add-knowledge-graph&family=zurich&ft:locale=en-US)**

The Global Graph resource for creating a Knowledge Graph tool has been renamed to Enterprise Graph.


-   **[Review and complete actions on requests using the Request Status AI agent](https://www.servicenow.com/docs/access?context=ticket-status-aia&family=zurich&ft:locale=en-US)**

The ticket status AI agent has been renamed to the request status AI agent. Request details include an AI-generated summary of the most recent comments on a request. Performance has been improved.

-   **[Confirm your web search tool provider data policies](https://www.servicenow.com/docs/access?context=add-web-search-ai-agent&family=zurich&ft:locale=en-US)**

If you select Google as your web search provider for web search AI agent tools, Google uses [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment, and data may be routed to places outside of regions specified on your ServiceNow AI Platform instance as a result. Consult your organization's data policies before enabling AI agents with web search tools that use Google as the provider.


-   **[Add version control to instructions sent to the LLM](https://www.servicenow.com/docs/access?context=version-control&family=zurich&ft:locale=en-US)**

You can review multiple versions of instructions sent to the LLM when designing your AI agents or agentic workflows. You can choose which version is active to help with testing or evaluating the success of an AI agent or agentic workflow to compare against other versions. Versions are named and ordered by time created for organizational purposes.

-   **[Duplicate and edit existing tools when creating new AI agents](https://www.servicenow.com/docs/access?context=add-tool-aia&family=zurich&ft:locale=en-US)**

When adding a tool to an AI agent, you can select an existing tool instead of creating a new tool. After an existing tool is added, you can change it to suit the specific needs of an AI agent.

-   **[Reference](https://www.servicenow.com/docs/access?context=na-aia-reference&family=zurich&ft:locale=en-US)**

The **sn\_aia.enable\_agent\_tool\_input\_value\_overrides** system property is migrated to the Agent properties \[sn\_aia\_property\] table.


</td></tr><tr><td>

Australia

</td><td>

-   **[Set up AI agents](https://www.servicenow.com/docs/access?context=set-up-na-aia&family=australia&ft:locale=en-US)**

Use GPT-5.4 as the default model for the Orchestrator when Azure OpenAI is the selected LLM.

-   **[Select the model provider](https://www.servicenow.com/docs/access?context=select-aia-llm&family=australia&ft:locale=en-US)**

The default third-party \(3P\) models have been upgraded to the latest versions - GPT 5.2 to GPT 5.4 to use AI agents and AI Agent Studio.

The new generative AI Config property records **sys\_generative\_ai\_config** and **sys\_generative\_ai\_prompt\_config** have been introduced for the following model providers:

    -   Amazon Bedrock: claude-sonnet-4-6
    -   Azure OpenAI: gpt 5.4
-   **[Platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&family=australia&ft:locale=en-US)**

The following platform agentic workflows had updates to their admin configurations and behavior in user-generated sessions.

    -   [Analyze task trends](https://www.servicenow.com/docs/access?context=incident-trends&family=australia&ft:locale=en-US): Admin configurations for additional filters such as category and service have been added.
    -   [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&family=australia&ft:locale=en-US): Additional reasoning information for the generated work plan is now displayed after the plan is created.
    -   [Identify ways to improve services](https://www.servicenow.com/docs/access?context=service-improvement&family=australia&ft:locale=en-US): Admin configurations for additional filters such as category and service have been added.

-   **[Enable UI validation for agentic AI processes and generative AI skills](https://www.servicenow.com/docs/access?context=na-aia-reference&family=australia&ft:locale=en-US)**

The glide.ai\_record\_activity.validation.feature.enabled system property enables UI rule validation \(such as required fields\) for AI‑initiated record updates. You can selectively apply this validation based on execution context using additional system properties. For example, glide.ai\_record\_activity.ai\_detection.nap.enabled applies validation to record updates triggered from the ServiceNow Otto panel. Similar properties control validation for AI skills, Virtual Agent, and agent‑initiated actions, as listed in the [Reference for AI agents](https://www.servicenow.com/docs/access?context=na-aia-reference&family=australia&ft:locale=en-US). This feature is opt‑in and inactive by default.

-   **[External agents with Agent2Agent](https://www.servicenow.com/docs/access?context=create-a2a-agent&family=australia&ft:locale=en-US)**

The agent to agent flow actions no longer inject an `Authorization: Bearer` header automatically. If your endpoint requires a Bearer token, include the prefix directly in the API Key credential value.


-   **[External agents with Agent2Agent](https://www.servicenow.com/docs/access?context=create-a2a-agent&family=australia&ft:locale=en-US)**

Use the A2A Protocol integration for creating external agents in the AI Agent Studio to connect with the ServiceNow AI Platform.

-   **[Updates to platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&family=australia&ft:locale=en-US)**

Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Analyze task trends](https://www.servicenow.com/docs/access?context=incident-trends&family=australia&ft:locale=en-US) and [Identify ways to improve service](https://www.servicenow.com/docs/access?context=service-improvement&family=australia&ft:locale=en-US) now have post-analysis actions, including the option to download analysis and ask additional information. [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&family=australia&ft:locale=en-US) can run as a scheduled job.

-   **[Agentic evaluation offer issue tracing and suggested optimizations](https://www.servicenow.com/docs/access?context=agentic-evals&family=australia&ft:locale=en-US)**

After an automated evaluation of an agentic AI asset, you can receive a list of issues and suggested optimizations to address those issues. Issues come with individual record node-by-node traces to pinpoint the exact source of problems. Optimizations are suggested, and you can apply them and run a reevaluation from a single guided flow.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some AI Agent Studio features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some AI Agent Studio features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate AI Agent Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

AI agents are available with activation of AI plugins from the ServiceNow Store. For more information about the prerequisites for using AI agents and AI Agent Studio, see [Install ServiceNow Otto AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

AI agents and AI Agent Studio are available with activation of any AI plugin from the ServiceNow Store. For more information about the prerequisites for using AI agents, see [Install ServiceNow Otto AI Agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Agent Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

You must first install the supported application version of the ServiceNow AI Platform to be able to use AI agents and AI Agent Studio. For more information, see [Install ServiceNow Otto AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=zurich&ft:locale=en-US).

 Next Experience UI Framework must be enabled before you can use the ServiceNow Otto panel.

</td></tr><tr><td>

Australia

</td><td>

You must first install the supported version of the ServiceNow AI Platform to be able to use AI agents and AI Agent Studio. For more information, see [Install ServiceNow Otto AI Agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=australia&ft:locale=en-US).

 Next Experience UI Framework must be enabled before you can use the ServiceNow Otto panel.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for AI Agent Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

AI agents and AI Agent Studio support various browsers, including Google Chrome and Microsoft Edge. AI agents and AI Agent Studio aren't supported in Internet Explorer.

</td></tr><tr><td>

Australia

</td><td>

AI agents and AI Agent Studio support various browsers, including Google Chrome and Microsoft Edge. AI agents and AI Agent Studio aren't supported in Internet Explorer.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Agent Studio, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Voice Input for AI agents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the ServiceNow Otto panel in the . This feature gives users a voice-to-text input option to access the generative AI skills in the panel in any supported language. For more information, see [Enable voice input for ServiceNow Otto panel](https://www.servicenow.com/docs/access?context=enable-voice-input-for-now-assist-panel&family=zurich&ft:locale=en-US).

After enabled, the Enable voice input for the ServiceNow Otto panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&family=zurich&ft:locale=en-US) for more information.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


</td></tr><tr><td>

Australia

</td><td>

-   **[Voice Input for AI agents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=australia&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the ServiceNow Otto panel in the . This feature gives users a voice-to-text input option to access the generative AI skills in the panel in any supported language. For more information, see [Enable voice input for ServiceNow Otto panel](https://www.servicenow.com/docs/access?context=enable-voice-input-for-now-assist-panel&family=australia&ft:locale=en-US).

After enabled, the Enable voice input for the ServiceNow Otto panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&family=australia&ft:locale=en-US) for more information.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for AI Agent Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

AI agents and AI Agent Studio are built on the GPT-4o-based framework and supports localization according to the GPT-4o model.

</td></tr><tr><td>

Australia

</td><td>

AI agents and AI Agent Studio are built on the GPT-4o-based framework and supports localization according to the GPT-4o model.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for AI Agent Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US)

-   Custom headers in external agents configuration.

 [Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US)

-   Add or remove AI agents or tools from the built-in AI agents.
-   Detect and disable runaway AI agent triggers to prevent unintended consumption.
-   Support conversation history for Knowledge Graph tool.
-   Enforce deny-by-default ACLs for new agentic ACL types.
-   Enable AI Agent Studio skill migration to Mosaic.

 [Zurich Patch 9](https://www.servicenow.com/docs/access?context=zurich-patch-9&family=zurich&ft:locale=en-US)

-   Enable UI validation for agentic AI processes and generative AI skills.

 [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US)

-   Test an agentic solution in the playground in AI-native mode.
-   Add widgets for tool outputs to provide an improved experience in AI-native mode.
-   Review issues and apply suggested recommendations to agentic AI assets after automated evaluations.
-   Run improved Platform agentic workflows, including Analyze task trends, Generate my work plan, and Identify ways to improve services.

 [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Get more insights into agentic AI asset performance with issue tracing and suggested optimizations from results pages.

 [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Show Agent card URL when using secondary agents.
-   Review changes to usage measurement.
-   Japanese language support for voice assistants enables Japanese-speaking users to experience natural, culturally appropriate interactions with AI voice agents.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Execute agentic workflows, AI agents, and tools in AI Agent Studio with role masking.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.
-   Run and review agentic workflow executions on forms in the Core UI and workspaces.
-   Framework extensibility with a new condition builder.
-   Support multilingual conversations.

 [Zurich Patch 3](https://www.servicenow.com/docs/access?context=zurich-patch-3&family=zurich&ft:locale=en-US)

-   Consume Global Graph as a Knowledge Graph resource.
-   Check for offensive content with MCP guardian.
-   Support the latest MCP version from [Zurich Patch 3](https://www.servicenow.com/docs/access?context=zurich-patch-3&family=zurich&ft:locale=en-US).

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Authenticate users with the MCP Server to add a Model Context Protocol tool to AI agents using the Model Context Protocol Client.
-   Create ACLs for AI agents and agentic workflows to customize who can discover and trigger AI agents and agentic workflows.

 Zurich EA

-   Create and maintain versions of LLM instructions for AI agents and agentic workflows to help organize and iterate on prompts and test their effectiveness.
-   Duplicate existing script, record operations, and search retrieval tools to reduce the work needed to create unique AI agents.
-   Monitor new analytics in the AI Agents Analytics dashboard to track valuable insights in customer satisfaction with AI interactions.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.
-   View the agentic workflow and AI agent activity on your AI Agent Studio.

 See [AI Agent Studio](https://www.servicenow.com/docs/access?context=na-ai-agents&family=zurich&ft:locale=en-US) for more information.

 For the Platform AI release notes, see [ServiceNow Otto release notes](https://www.servicenow.com/docs/access?context=now-assist-rn&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   Custom headers in external agents configuration.

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Add or remove AI agents or tools from the built-in AI agents.
-   Detect and disable runaway AI agent triggers to prevent unintended consumption.
-   Support conversation history for Knowledge Graph tool.
-   Enforce deny-by-default ACLs for new agentic ACL types.
-   Enable AI Agent Studio skill migration to Mosaic.

 [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

-   Enable UI validation for agentic AI processes and generative AI skills.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Test an agentic solution in the playground in AI-native mode.
-   Add widgets for tool outputs to provide an improved experience in AI-native mode.
-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Get more insights into agentic AI asset performance with issue tracing and suggested optimizations from results pages.

 See [AI Agent Studio](https://www.servicenow.com/docs/access?context=na-ai-agents&family=australia&ft:locale=en-US) for more information.

 For the Platform AI release notes, see [ServiceNow Otto release notes](https://www.servicenow.com/docs/access?context=now-assist-rn&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

