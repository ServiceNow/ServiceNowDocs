---
title: Combined Now Assist AI agents release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Now Assist AI agents from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-nowassistaiagents-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 28
breadcrumb: [Products combined by family]
---

# Combined Now Assist AI agents release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Now Assist AI agents from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist AI agents release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist AI agents to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Now Assist AI agents.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Configure ACLs for AI agents and agentic workflows](https://servicenow-staging.fluidtopics.net/access?context=aia-security-implementation&family=xanadu&ft:locale=en-US)**

Configure the access control lists \(ACLs\) for who can discover and trigger AI agents and agentic workflows in their guided setups in the AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to only authenticated users or publicly available.


-   **[Create an AI agent](https://servicenow-staging.fluidtopics.net/access?context=configure-next-best-action-agent&family=xanadu&ft:locale=en-US)**

Create AI agents accomplish discrete tasks to use in a use case:

    -   Create AI agents to gather data, make decisions, and complete tasks that would otherwise need to be done by a human.
    -   Add one of the following tools or information sources for the AI agent to execute:
        -   Catalog item
        -   Conversational topic
        -   Flow action
        -   Now Assist skill
        -   Record operation
        -   Script
        -   Search retrieval
        -   Subflow
        -   Web search
-   **[Create an agentic workflow](https://servicenow-staging.fluidtopics.net/access?context=configure-use-case-ai-agents&family=xanadu&ft:locale=en-US)**

Create a use case with an execution plan to solve complex tasks with Now Assist. You can also do the following tasks:

    -   Clone an existing use case to avoid manual configuration.
    -   Create triggers when creating a use case that calls the AI agent when a condition or objective is observed.
    -   Test a use case before execution.
    -   Resolve record-based cases with AI agents.
-   **[Enable Now Assist Guardian in AI agents](https://servicenow-staging.fluidtopics.net/access?context=enable-aia-na-guardian&family=xanadu&ft:locale=en-US)**

Enable Now Assist Guardian in AI agents to automatically identify and block offensive messages that are sent by human agents.

-   **[Multiple conversations in Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=multiple-conversations-aia&family=xanadu&ft:locale=en-US)**

Enable live agents to interact with multiple AI agent conversations through the Now Assist panel.

-   **[AI Agent Analytics dashboard](https://servicenow-staging.fluidtopics.net/access?context=ai-agent-dashboard&family=xanadu&ft:locale=en-US)**

Analyze the performance, efficiency gain, and usage of AI agents through preconfigured dashboards.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Configure role masking for AI agents and agentic workflows](https://servicenow-staging.fluidtopics.net/access?context=aia-role-masking&family=yokohama&ft:locale=en-US)**

Role masking restricts access to specific roles based on configuration to verify that agentic workflows, AI agents, and tools run within the boundaries of the roles configured to meet their business needs while reducing the risk of unauthorized access to the agents and the agentic data.

-   **[Add AI agent learning](https://servicenow-staging.fluidtopics.net/access?context=agent-learning&family=yokohama&ft:locale=en-US)**

Enhance AI agent learning through episodic memory, enabling AI agents to improve by learning from past successful interactions.

-   **[Select channels and access](https://servicenow-staging.fluidtopics.net/access?context=channels-access-aw&family=yokohama&ft:locale=en-US)**

Create and update UI actions for workflow executions and display handling. You can specify conditions for the display of the UI actions.

-   **[Desktop action](https://servicenow-staging.fluidtopics.net/access?context=add-desktop-action-ai-agent&family=yokohama&ft:locale=en-US)**

Add Desktop action as a tool to an AI agent to perform desktop automation for repetitive tasks.

-   **[Configuring Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=configuring-ai-agents&family=yokohama&ft:locale=en-US)**

Support multilingual conversations for AI agents across languages.

-   **[Test execution manually](https://servicenow-staging.fluidtopics.net/access?context=test-ai-agent&family=yokohama&ft:locale=en-US) and [Test execution manually](https://servicenow-staging.fluidtopics.net/access?context=test-aia-use-case&family=yokohama&ft:locale=en-US)**

The testing page on AI Agent Studio has two testing options:

    -   Manual test
    -   Automated evaluation
Observe the different versions of an AI agent behavior in manual tests and in automated evaluations using the **Manual tests** and **Automated tests** tabs.

-   **[Test user access](https://servicenow-staging.fluidtopics.net/access?context=test-aia-access&family=yokohama&ft:locale=en-US) and [Test user access](https://servicenow-staging.fluidtopics.net/access?context=test-aw-access&family=yokohama&ft:locale=en-US)**

Test how an AI agent or agentic workflow completes a task and if it enables users permission to access it.

-   **[Model Context Protocol Client](https://servicenow-staging.fluidtopics.net/access?context=mcp-client&family=yokohama&ft:locale=en-US)**
    -   Authorization upgrades to support segregation of Resource Server and Authentication Server through Protected Resource Metadata \(PRM\).
    -   Use the **mcp\_guardian\_check** property to enable guardian checks for MCP Client when there’s an MCP tool call.
    -   Supervise the pagination with mouse device support to show large number of services from an MCP server through the **sn\_mcp\_client.cursor.max\_iterations** system property.
    -   Add a title field for human-friendly display names that can be used as a programmatic identifier.
-   **[Use in-product experiences for agentic workflows on forms](https://servicenow-staging.fluidtopics.net/access?context=in-product-agentic-ai&family=yokohama&ft:locale=en-US)**

In the Core UI and workspaces, you can use UI and declarative actions to run agentic workflows. You can also see the presence, progress, and output of agentic workflows performed on a record. The execution details for each agentic workflow include who is supervising the workflow, estimated and total time taken, processing messages, and step history.

-   **[Review and approve requests and tickets with the Approval Assistance AI agent](https://servicenow-staging.fluidtopics.net/access?context=platform-approval-aia&family=yokohama&ft:locale=en-US)**

You can use the new approval assistance AI agent to view all pending approval requests and access detailed information about them. You can then approve requests and tickets and make updates to them from Now Assist in Virtual Agent.

-   **[Configure email notification alerts for AI agent and agentic workflow executions](https://servicenow-staging.fluidtopics.net/access?context=config-aia-notifications&family=yokohama&ft:locale=en-US)**

Configure alert email notifications for unexpected or undesired behavior from AI agents and agentic workflows. You can configure the thresholds for triggering the alerts on the Agent Properties table, and you can add or update the recipients of the email notifications from the Notifications table.

-   **[Create an external agent](https://servicenow-staging.fluidtopics.net/access?context=create-external-aia&family=yokohama&ft:locale=en-US)**

Create new external AI agents that connect to third-party agentic AI systems. Use Agent2Agent protocol or integrate agents manually to configure them in AI Agent Studio to use in the ServiceNow agentic AI system.

-   **[Knowledge Graph](https://servicenow-staging.fluidtopics.net/access?context=add-knowledge-graph&family=yokohama&ft:locale=en-US)**

Use Enterprise Graph \(Small\) as a resource to create a Knowledge Graph tool for an AI agent in the AI Agent Studio.


-   **[AI Agent Studio](https://servicenow-staging.fluidtopics.net/access?context=ai-agent-studio&family=yokohama&ft:locale=en-US)**

View and troubleshoot the agentic workflow and AI agent executions on AI Agent Studio.

-   **[Configuring Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=configuring-ai-agents&family=yokohama&ft:locale=en-US) - Dynamic Orchestrator**

Maps the right agents for an agentic workflow with Dynamic Orchestrator for better performance and accuracy of the agentic workflow execution.

-   **[View analytics for customer satisfaction with AI interactions](https://servicenow-staging.fluidtopics.net/access?context=ai-agent-dashboard&family=yokohama&ft:locale=en-US)**

Multiple new metrics have been added to the AI Agent Analytics dashboard, accessible from the AI Agent Studio to provide insight into average customer satisfaction and customer satisfaction with the best and worst performing agentic workflows and agents.

-   **[New third-party AI model provider options available for all Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Create an AI agent](https://servicenow-staging.fluidtopics.net/access?context=configure-next-best-action-agent&family=yokohama&ft:locale=en-US)**

The **Add** button on the **AI agents** tab is added as a drop-down providing different agent types for AI agent creation:

    -   **Chat**
    -   **Voice**
    -   **External**
-   **[Add tools and information](https://servicenow-staging.fluidtopics.net/access?context=add-tool-aia&family=yokohama&ft:locale=en-US)**

The output transformation strategy for an AI agent output now contains a new option called **Custom**.

With Custom output transformation strategy, a **Transformation Instructions** field with a text area is enabled for the user to provide their specific instructions for refining the output as per the agentic workflow. The instructions will also ensure that the transformation is done as per the user's need.

-   **[Configuring Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=configuring-ai-agents&family=yokohama&ft:locale=en-US) - AI Agent Background Channel**

Invoke the agentic conversations from the Workspace or Core UI via the AI Agent Background channel, that is associated with the AI Agent Background Provider, to execute the AI agents and agentic workflows.

-   **[Configuring Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=configuring-ai-agents&family=yokohama&ft:locale=en-US) - Interactive and non interactive AI agents**

Run AI agents and agentic workflows execution in one of the following ways:

    -   **Interactive Mode**: AI agents reach out to the user for information during fallback.
    -   **Non interactive Mode**: AI agents do not reach out to the user during fallback but send the execution output to the user.

-   **[Select Virtual Agent as a display option for AI agents](https://servicenow-staging.fluidtopics.net/access?context=configure-next-best-action-agent&family=yokohama&ft:locale=en-US)**

Choose to display AI agent output in Virtual Agent. You can also discover AI agents in Virtual Agent conversations.

-   **[Hide citations for agentic workflows or AI agents](https://servicenow-staging.fluidtopics.net/access?context=aia-hide-citations&family=yokohama&ft:locale=en-US)**

Disable citations for specific agentic workflows or AI agents in AI Agent Studio where citations are not required or involve confidential information.

-   **[Create an AI agent](https://servicenow-staging.fluidtopics.net/access?context=configure-next-best-action-agent&family=yokohama&ft:locale=en-US)**
    -   **Long term memory**: Add or delete categories for AI agents to store and retrieve memories.
    -   Additional tools available while creating an AI agent.
        -   Knowledge graph
        -   File retrieval
-   **[Evaluate agentic AI](https://servicenow-staging.fluidtopics.net/access?context=execute-aia-eval&family=yokohama&ft:locale=en-US)**

In Now Assist Skill Kit, you can execute evaluation runs for your agentic workflows. You can select evaluation plans and the execution log datasets to judge whether your agentic workflows are consistently completing tasks and using the correct tools.


-   **[Create an AI agent](https://servicenow-staging.fluidtopics.net/access?context=configure-next-best-action-agent&family=yokohama&ft:locale=en-US)**

Create an AI agent to assist your live agents while resolving cases, incidents, or tasks:

    -   Create AI agents to gather data, make decisions, and complete tasks that would otherwise need to be done by a human.
    -   Add one of the following tools or information sources for the AI agent to execute:
        -   Catalog item
        -   Conversational topic
        -   Flow action
        -   Now Assist skill
        -   Record operation
        -   Script
        -   Search retrieval
        -   Subflow
        -   Web search
-   **[Create an agentic workflow](https://servicenow-staging.fluidtopics.net/access?context=configure-use-case-ai-agents&family=yokohama&ft:locale=en-US)**

Create an agentic workflow with an execution plan to solve complex tasks with Now Assist. You can also do the following tasks:

    -   Clone an existing agentic workflow to avoid manual configuration.
    -   Create triggers when creating an agentic workflow that calls the AI agent when a condition or objective is observed.
    -   Test an agentic workflow before execution.
    -   Resolve record-based cases with AI agents.
-   **[Enable Now Assist Guardian in AI agents](https://servicenow-staging.fluidtopics.net/access?context=enable-aia-na-guardian&family=yokohama&ft:locale=en-US)**

Enable Now Assist Guardian in AI agents to automatically identify and block offensive messages that are sent by human agents.

-   **[Multiple conversations in Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=multiple-conversations-aia&family=yokohama&ft:locale=en-US)**

Enable live agents to interact with multiple AI agent conversations through the Now Assist panel.

-   **[AI Agent Analytics dashboard](https://servicenow-staging.fluidtopics.net/access?context=ai-agent-dashboard&family=yokohama&ft:locale=en-US)**

Analyze the performance, efficiency gain, and usage of AI agents through preconfigured dashboards.


</td></tr><tr><td>

Zurich

</td><td>

-   **[ServiceNow AI agents as secondary agents](https://servicenow-staging.fluidtopics.net/access?context=secondary-agent&family=zurich&ft:locale=en-US)**

Enhance user experience for Secondary Agents by displaying the Agent card URL to admins for easy access and management so the admin can view, copy, and consume the URL easily.

Additionally, when adding an MCP tool, the name and description of the tool are populated automatically as per the details fetched from the server and the user can update the details.


-   **[Configure role masking for AI agents and agentic workflows](https://servicenow-staging.fluidtopics.net/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Role masking restricts access to specific roles based on configuration to verify that agentic workflows, AI agents, and tools run within the boundaries of the roles configured to meet their business needs while reducing the risk of unauthorized access to the agents and the agentic data.

-   **[Add AI agent learning](https://servicenow-staging.fluidtopics.net/access?context=agent-learning&family=zurich&ft:locale=en-US)**

Enhance AI agent learning through episodic memory, enabling AI agents to improve by learning from past successful interactions.

-   **[Select channels and access](https://servicenow-staging.fluidtopics.net/access?context=channels-access-aw&family=zurich&ft:locale=en-US)**

Create and update UI actions for workflow executions and display handling. You can specify conditions for the display of the UI actions.

-   **[Desktop action](https://servicenow-staging.fluidtopics.net/access?context=add-desktop-action-ai-agent&family=zurich&ft:locale=en-US)**

Add Desktop action as a tool to an AI agent to perform desktop automation for repetitive tasks.

-   **[Configure](https://servicenow-staging.fluidtopics.net/access?context=configuring-ai-agents&family=zurich&ft:locale=en-US)**

Support multilingual conversations for AI agents across languages.

-   **[Test execution manually](https://servicenow-staging.fluidtopics.net/access?context=test-ai-agent&family=zurich&ft:locale=en-US) and [Test execution manually](https://servicenow-staging.fluidtopics.net/access?context=test-aia-use-case&family=zurich&ft:locale=en-US)**

The testing page on AI Agent Studio has two testing options:

    -   Manual test
    -   Automated evaluation
Observe the different versions of an AI agent behavior in manual tests and in automated evaluations using the **Manual tests** and **Automated tests** tabs.

-   **[Test user access](https://servicenow-staging.fluidtopics.net/access?context=test-aia-access&family=zurich&ft:locale=en-US) and [Test user access](https://servicenow-staging.fluidtopics.net/access?context=test-aw-access&family=zurich&ft:locale=en-US)**

Test how an AI agent or agentic workflow completes a task and if it enables users permission to access it.

-   **[Model Context Protocol Client](https://servicenow-staging.fluidtopics.net/access?context=mcp-client&family=zurich&ft:locale=en-US)**
    -   Authorization upgrades to support segregation of Resource Server and Authentication Server through Protected Resource Metadata \(PRM\).
    -   Use the **mcp\_guardian\_check** property to enable guardian checks for MCP Client when there’s an MCP tool call.
    -   Supervise the pagination with mouse device support to show large number of services from an MCP server through the **sn\_mcp\_client.cursor.max\_iterations** system property.
    -   Add a title field for human-friendly display names that can be used as a programmatic identifier.
-   **[Use in-product experiences for agentic workflows on forms](https://servicenow-staging.fluidtopics.net/access?context=in-product-agentic-ai&family=zurich&ft:locale=en-US)**

In the Core UI and workspaces, you can use UI and declarative actions to run agentic workflows. You can also see the presence, progress, and output of agentic workflows performed on a record. The execution details for each agentic workflow include who is supervising the workflow, estimated and total time taken, processing messages, and step history.

-   **[Review and approve requests and tickets with the Approval Assistance AI agent](https://servicenow-staging.fluidtopics.net/access?context=platform-approval-aia&family=zurich&ft:locale=en-US)**

You can use the new approval assistance AI agent to view all pending approval requests and access detailed information about them. You can then approve requests and tickets and make updates to them from Now Assist in Virtual Agent.

-   **[View the Approval Info Record widget](https://servicenow-staging.fluidtopics.net/access?context=approval-info-record-widget&family=zurich&ft:locale=en-US)**

The Service Portal Approval Info Record widget shows details about the approval request and a full record for an approval including the activity stream.

-   **[Configure email notification alerts for AI agent and agentic workflow executions](https://servicenow-staging.fluidtopics.net/access?context=config-aia-notifications&family=zurich&ft:locale=en-US)**

Configure alert email notifications for unexpected or undesired behavior from AI agents and agentic workflows. You can configure the thresholds for triggering the alerts on the Agent Properties table, and you can add or update the recipients of the email notifications from the Notifications table.

-   **[Create an external agent](https://servicenow-staging.fluidtopics.net/access?context=create-external-aia&family=zurich&ft:locale=en-US)**

Create new external AI agents that connect to third-party agentic AI systems. Use Agent2Agent protocol or integrate agents manually to configure them in AI Agent Studio to use in the ServiceNow agentic AI system.

-   **[Knowledge Graph](https://servicenow-staging.fluidtopics.net/access?context=add-knowledge-graph&family=zurich&ft:locale=en-US)**

Use Enterprise Graph \(Small\) as a resource to create a Knowledge Graph tool for an AI agent in the AI Agent Studio.


-   **[Add MCP tool](https://servicenow-staging.fluidtopics.net/access?context=add-mcp-server-tool&family=zurich&ft:locale=en-US)**

The Model Context Protocol Client enables guardian checks for offensive content when Notion is selected as the MCP server.

-   **[Configure Model Context Protocol Client](https://servicenow-staging.fluidtopics.net/access?context=configuring-mcp-client&family=zurich&ft:locale=en-US)**

The Model Context Protocol Client application supports the latest MCP version.

-   **[Knowledge Graph](https://servicenow-staging.fluidtopics.net/access?context=add-knowledge-graph&family=zurich&ft:locale=en-US)**

Use Global Graph as a Knowledge Graph resource when creating a Knowledge Graph tool for an AI agent in the AI Agent Studio.


-   **[Model Context Protocol Client](https://servicenow-staging.fluidtopics.net/access?context=mcp-client&family=zurich&ft:locale=en-US)**

Enable users of the ServiceNow® AI Agent Studio to access tools that are hosted externally and published using an MCP server via the Model Context Protocol Client application.

Authenticate users with the MCP server to add the MCP tool to an AI agent.

-   **[ServiceNow AI agents as secondary agents](https://servicenow-staging.fluidtopics.net/access?context=secondary-agent&family=zurich&ft:locale=en-US)**

Use ServiceNow AI agents inside third-party agentic AI systems. Using Agent2Agent protocol, you can discover and invoke AI agents in other agentic AI systems to access ServiceNow AI Platform instance capabilities.

-   **[Configure ACLs for AI agents and agentic workflows](https://servicenow-staging.fluidtopics.net/access?context=aia-security-implementation&family=zurich&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Review agentic activity in AI Agent Studio](https://servicenow-staging.fluidtopics.net/access?context=ai-agent-studio&family=zurich&ft:locale=en-US)**

View and troubleshoot the agentic workflow and AI agent executions on AI Agent Studio via the **Activity** page.

-   **[Configure](https://servicenow-staging.fluidtopics.net/access?context=configuring-ai-agents&family=zurich&ft:locale=en-US) - Dynamic Orchestrator**

Maps the appropriate agents for an agentic workflow with Dynamic Orchestrator for better performance and accuracy of the agentic workflow execution.

-   **[View analytics for customer satisfaction with AI interactions](https://servicenow-staging.fluidtopics.net/access?context=ai-agent-dashboard&family=zurich&ft:locale=en-US)**

Multiple new metrics have been added to the AI Agent Analytics dashboard, accessible from the AI Agent Studio to provide insight into average customer satisfaction and customer satisfaction with the best and worst performing agentic workflows and agents.

-   **[New third-party AI model provider options available for all Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Add tools and information](https://servicenow-staging.fluidtopics.net/access?context=add-tool-aia&family=zurich&ft:locale=en-US)**

The output transformation strategy for an AI agent output contains a new option called **Custom**. Using the custom output transformation strategy, the tool output gets transformed according to the LLM instructions.

-   **[Configure](https://servicenow-staging.fluidtopics.net/access?context=configuring-ai-agents&family=zurich&ft:locale=en-US) - AI Agent Background Channel**

Invoke the agentic conversations from Workspace or Core UI via the AI Agent Background channel that is associated with the AI Agent Background Provider to execute the AI agents and agentic workflows.

-   **[Configure](https://servicenow-staging.fluidtopics.net/access?context=configuring-ai-agents&family=zurich&ft:locale=en-US) - Interactive and non interactive AI agents**

Run AI agents and agentic workflows execution in one of the following ways:

    -   **Interactive Mode**: AI agents reach out to the user for information during fallback.
    -   **Non interactive Mode**: AI agents don’t reach out to the user during fallback but send the execution output to the user.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Now Assist AI agents features.

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

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   ****
-   **[Request status AI agent](https://servicenow-staging.fluidtopics.net/access?context=ticket-status-aia&family=yokohama&ft:locale=en-US)**

The request status AI agent provides an AI-generated summary of the most recent comments from the AI agent or other people working on a ticket. You can add attachments to an open ticket or incident to support a request action. To find more information about an open ticket, you can ask the request status AI agent follow-up questions based on previous answers from the agent.

-   **[Configuring Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=configuring-ai-agents&family=yokohama&ft:locale=en-US)**

Run AI agents and agentic workflows concurrently in AI Agent Background Channel and in Non-interactive mode.

-   **[Knowledge Graph](https://servicenow-staging.fluidtopics.net/access?context=add-knowledge-graph&family=yokohama&ft:locale=en-US)**

The Global Graph resource for creating a Knowledge Graph tool has been renamed to Enterprise Graph.


[Yokohama Patch 8](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-8&family=yokohama&ft:locale=en-US)

-   **[Confirm your web search tool provider data policies](https://servicenow-staging.fluidtopics.net/access?context=add-web-search-ai-agent&family=yokohama&ft:locale=en-US)**

If you select Google as your web search provider for web search AI agent tools, Google will use [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment, and data may be routed to places outside of regions specified on your ServiceNow instance as a result. Consult your organization's data policies before enabling AI agents with web search tools that use Google as the provider.


-   **[Add version control to instructions sent to the LLM](https://servicenow-staging.fluidtopics.net/access?context=version-control&family=yokohama&ft:locale=en-US)**

You can review multiple versions of instructions sent to the LLM when designing your AI agents or agentic workflows. You can choose which version is active to help with testing or evaluating the success of an AI agent or agentic workflow to compare against other versions. Versions are named and ordered by time created for organizational purposes.

-   **[Duplicate and edit existing tools when creating new AI agents](https://servicenow-staging.fluidtopics.net/access?context=add-tool-aia&family=yokohama&ft:locale=en-US)**

When adding a tool to an AI agent, you can select an existing tool instead of creating a new tool from scratch. After an existing tool is added, you can make changes to suit the specific AI agent’s needs.

-   **[Reference](https://servicenow-staging.fluidtopics.net/access?context=na-aia-reference&family=yokohama&ft:locale=en-US)**

The **sn\_aia.enable\_agent\_tool\_input\_value\_overrides** system property is migrated to the \[sn\_aia\_property\] agent system property.


-   **[Monitor more AI agent analytics in the AI Agent Analytics dashboard](https://servicenow-staging.fluidtopics.net/access?context=ai-agent-dashboard&family=yokohama&ft:locale=en-US)**

Two new pages have been added to the AI Agent Analytics dashboard, giving administrators more indicators, visualizations, and breakdowns to track AI agent performance and usage.

-   **[Exploring Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=exploring-ai-agents&family=yokohama&ft:locale=en-US)**

Impersonation in Now Assist records transactions done by an AI agent in the name of the AI agent who executes the agentic workflow.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Request status AI agent](https://servicenow-staging.fluidtopics.net/access?context=ticket-status-aia&family=zurich&ft:locale=en-US)**

The request status AI agent provides an AI-generated summary of the most recent comments from the AI agent or other people working on a ticket. You can add attachments to an open ticket or incident to support a request action. To find more information about an open ticket, you can ask the request status AI agent follow-up questions based on previous answers from the agent.

-   **[Understand the Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=understand-na-aia&family=zurich&ft:locale=en-US)**

The base reflection prompt has been replaced with the ReAct Orchestrator prompt, introducing a Route scheduling mode when an agent needs assistance from another agent during execution.

-   **[Configure](https://servicenow-staging.fluidtopics.net/access?context=configuring-ai-agents&family=zurich&ft:locale=en-US)**

Run AI agents and agentic workflows concurrently in AI Agent Background Channel and in Non-interactive mode.

-   **[Knowledge Graph](https://servicenow-staging.fluidtopics.net/access?context=add-knowledge-graph&family=zurich&ft:locale=en-US)**

The Global Graph resource for creating a Knowledge Graph tool has been renamed to Enterprise Graph.


-   **[Review and complete actions on requests using the Request Status AI agent](https://servicenow-staging.fluidtopics.net/access?context=ticket-status-aia&family=zurich&ft:locale=en-US)**

The ticket status AI agent has been renamed to the request status AI agent. Request details include an AI-generated summary of the most recent comments on a request. Performance has been improved.

-   **[Confirm your web search tool provider data policies](https://servicenow-staging.fluidtopics.net/access?context=add-web-search-ai-agent&family=zurich&ft:locale=en-US)**

If you select Google as your web search provider for web search AI agent tools, Google uses [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment, and data may be routed to places outside of regions specified on your ServiceNow AI Platform instance as a result. Consult your organization's data policies before enabling AI agents with web search tools that use Google as the provider.


-   **[Add version control to instructions sent to the LLM](https://servicenow-staging.fluidtopics.net/access?context=version-control&family=zurich&ft:locale=en-US)**

You can review multiple versions of instructions sent to the LLM when designing your AI agents or agentic workflows. You can choose which version is active to help with testing or evaluating the success of an AI agent or agentic workflow to compare against other versions. Versions are named and ordered by time created for organizational purposes.

-   **[Duplicate and edit existing tools when creating new AI agents](https://servicenow-staging.fluidtopics.net/access?context=add-tool-aia&family=zurich&ft:locale=en-US)**

When adding a tool to an AI agent, you can select an existing tool instead of creating a new tool. After an existing tool is added, you can change it to suit the specific needs of an AI agent.

-   **[Reference](https://servicenow-staging.fluidtopics.net/access?context=na-aia-reference&family=zurich&ft:locale=en-US)**

The **sn\_aia.enable\_agent\_tool\_input\_value\_overrides** system property is migrated to the Agent properties \[sn\_aia\_property\] table.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Now Assist AI agents features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Now Assist AI agents features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Now Assist AI agents.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Now Assist in AI agents is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using Now Assist, see [Install Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=install-ai-agents-plugins&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Now Assist in AI agents is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using Now Assist, see [Install Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=install-ai-agents-plugins&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Now Assist AI agents are available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using Now Assist AI agents, see [Install Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=install-ai-agents-plugins&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist AI agents we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=install-ai-agents-plugins&family=xanadu&ft:locale=en-US).

 Enable the Next Experience UI Framework before you can use the Now Assist panel.

</td></tr><tr><td>

Yokohama

</td><td>

You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=install-ai-agents-plugins&family=yokohama&ft:locale=en-US).

 Enable the Next Experience UI Framework before you can use the Now Assist panel.

</td></tr><tr><td>

Zurich

</td><td>

You must first install the supported Now Assist version of the ServiceNow AI Platform to be able to use Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=install-ai-agents-plugins&family=zurich&ft:locale=en-US).

 Next Experience UI Framework must be enabled before you can use the Now Assist panel.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist AI agents we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Now Assist AI agents supports various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents isn’t supported in Internet Explorer.

</td></tr><tr><td>

Yokohama

</td><td>

Now Assist AI agents supports various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents isn’t supported in Internet Explorer.

</td></tr><tr><td>

Zurich

</td><td>

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Now Assist AI agents, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Voice Input for Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=xanadu&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see [Enable voice input for Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=enable-voice-input-for-now-assist-panel&family=xanadu&ft:locale=en-US).

Once enabled, the Enable voice input for the Now Assist panel option will be available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://servicenow-staging.fluidtopics.net/access?context=next-experience-accessibility-preferences&family=xanadu&ft:locale=en-US) for more information.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Voice Input for Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=yokohama&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see [Enable voice input for Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=enable-voice-input-for-now-assist-panel&family=yokohama&ft:locale=en-US).

Once enabled, the Enable voice input for the Now Assist panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://servicenow-staging.fluidtopics.net/access?context=next-experience-accessibility-preferences&family=yokohama&ft:locale=en-US) for more information.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Voice Input for Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see [Enable voice input for Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=enable-voice-input-for-now-assist-panel&family=zurich&ft:locale=en-US).

After enabled, the Enable voice input for the Now Assist panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://servicenow-staging.fluidtopics.net/access?context=next-experience-accessibility-preferences&family=zurich&ft:locale=en-US) for more information.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist AI agents we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Now Assist AI agents is built on the GPT-4o-based framework and supports localization as per the GPT-4o model.

</td></tr><tr><td>

Yokohama

</td><td>

Now Assist AI agents is built on the GPT-4o-based framework and supports localization according to the GPT-4o model.

</td></tr><tr><td>

Zurich

</td><td>

The Now Assist AI agents application is built on the GPT-4o-based framework and supports localization according to the GPT-4o model.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist AI agents we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

[Xanadu Patch 10](https://servicenow-staging.fluidtopics.net/access?context=xanadu-patch-10&family=xanadu&ft:locale=en-US)

-   Create ACLs for AI agents and agentic workflows to customize who can discover and trigger AI agents and agentic workflows.
-   Add secure methods for AI agent and agentic workflow operations and apply appropriate ACLs to ensure that they can only be accessed and run by authorized users.
-   Security implementation with access control lists \(ACLs\) for agentic workflows and AI agents is mandatory.

 Xanadu EA

-   Define agentic workflows with an execution plan to achieve various tasks.
-   Use the Now Assist panel to communicate with the agent during an issue resolution.
-   Clone existing AI agents and use cases to save time and avoid manual configuration.
-   Enable Now Assist Guardian to automatically identify and block offensive messages.
-   View the usage and performance of your AI agents with the AI agent analytics dashboard.
-   Enable multiple conversations for AI agents on the Now Assist panel.

 See [Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=na-ai-agents&family=xanadu&ft:locale=en-US) for more information.

 For the Platform Now Assist release notes, see [Now Assist release notes](https://servicenow-staging.fluidtopics.net/access?context=now-assist-rn&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Execute agentic workflows, AI agents, and tools in AI Agent Studio with role masking.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Run and review agentic workflow executions on forms in the Core UI and workspaces.
-   Framework extensibility with a new condition builder.
-   Support multilingual conversations.

 [Yokohama Patch 6](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

-   Create and maintain versions of LLM instructions for AI agents and agentic workflows to help organize and iterate on prompts and test their effectiveness.
-   Follow updated guided setup steps for agentic workflows and AI agents with additional guidance for successful instructions sent to the LLM.
-   Duplicate existing script, record operations, and search retrieval tools to reduce the work needed to create unique AI agents.
-   Monitor new analytics in the AI Agents Analytics dashboard to track valuable insights in customer satisfaction with AI interactions.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   View the agentic workflow and AI agent activity on your AI Agent Studio.
-   Map the right agents for agentic workflow execution with Dynamic orchestrator in Virtual Agent for better performance and accuracy.
-   Create different types of AI agents.
-   Custom output transformation strategies for an AI agent.
-   Execute AI agents and agentic workflows from workspace or Core UI.
-   Run AI agents and agentic workflows in a non-interactive execution mode.

 [Yokohama Patch 3](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   Use cases in Now Assist AI agents are now called agentic workflows.
-   Choose either Azure OpenAI or Now LLM Service as your preferred large language model \(LLM\) for AI agents and agentic workflows in the AI Agent Studio settings.
-   Use Virtual Agent for AI agent interactions.
-   Execute agentic evaluation runs to evaluate agentic workflows based on execution log data to compare against benchmarks and monitor performance.
-   Improve the quality of LLM responses by passing information between tools.
-   Hide citations for an agentic workflow or AI agent.
-   Transactions done by an AI agent for an agentic workflow are recorded in the name of the AI agent.
-   Enable AI agents to store and retrieve memories with categories.
-   Use Knowledge graph and File retrieval as tools in creating an AI agent.

 [Yokohama Patch 1](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-1&family=yokohama&ft:locale=en-US)

-   Define agentic workflows with an execution plan for automatically resolving the incoming cases and incidents.
-   Use the Now Assist panel to communicate with the agent during issue resolution.
-   Clone existing AI agents and agentic workflows to save time and avoid manual configuration.
-   Enable Now Assist Guardian to automatically identify and block offensive messages.
-   View the usage and performance of your AI agents with the AI agent analytics dashboard.
-   Enable multiple conversations for AI agents on the Now Assist panel.

 See [Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=na-ai-agents&family=yokohama&ft:locale=en-US) for more information.

 For the Platform Now Assist release notes, see [Now Assist release notes](https://servicenow-staging.fluidtopics.net/access?context=now-assist-rn&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

[\[Placeholder link text to key zurich-patch-7\]](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.

 [Zurich Patch 5](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Show Agent card URL when using secondary agents.
-   Review changes to Now Assist usage measurement.
-   Japanese language support for voice assistants enables Japanese-speaking users to experience natural, culturally appropriate interactions with AI voice agents.

 [Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Execute agentic workflows, AI agents, and tools in AI Agent Studio with role masking.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Run and review agentic workflow executions on forms in the Core UI and workspaces.
-   Framework extensibility with a new condition builder.
-   Support multilingual conversations.

 [Zurich Patch 3](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-3&family=zurich&ft:locale=en-US)

-   Consume Global Graph as a Knowledge Graph resource.
-   Check for offensive content with MCP guardian.
-   Support the latest MCP version from [Zurich Patch 3](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-3&family=zurich&ft:locale=en-US).

 [Zurich Patch 1](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Authenticate users with the MCP Server to add a Model Context Protocol tool to AI agents using the Model Context Protocol Client.
-   Create ACLs for AI agents and agentic workflows to customize who can discover and trigger AI agents and agentic workflows.

 Zurich EA

-   Create and maintain versions of LLM instructions for AI agents and agentic workflows to help organize and iterate on prompts and test their effectiveness.
-   Duplicate existing script, record operations, and search retrieval tools to reduce the work needed to create unique AI agents.
-   Monitor new analytics in the AI Agents Analytics dashboard to track valuable insights in customer satisfaction with AI interactions.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   View the agentic workflow and AI agent activity on your AI Agent Studio.

 See [Now Assist AI agents](https://servicenow-staging.fluidtopics.net/access?context=na-ai-agents&family=zurich&ft:locale=en-US) for more information.

 For the Platform Now Assist release notes, see [Now Assist release notes](https://servicenow-staging.fluidtopics.net/access?context=now-assist-rn&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

