---
title: Now Assist AI agents release notes
description: The ServiceNow Now Assist AI Agents application provides solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. Now Assist AI Agents was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 16
---

# Now Assist AI agents release notes

The ServiceNow® Now Assist AI Agents application provides solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. Now Assist AI Agents was enhanced and updated in the Zurich release.

## Now Assist AI Agents highlights for the Zurich release

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Test an agentic solution in the playground in AI-native mode.
-   Add widgets for tool outputs to provide an improved experience in AI-native mode.
-   Review issues and apply suggested recommendations to agentic AI assets after automated evaluations.
-   Run improved Platform agentic workflows, including Analyze task trends, Generate my work plan, and Identify ways to improve services.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Get more insights into agentic AI asset performance with issue tracing and suggested optimizations from results pages.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Show Agent card URL when using secondary agents.
-   Review changes to Now Assist usage measurement.
-   Japanese language support for voice assistants enables Japanese-speaking users to experience natural, culturally appropriate interactions with AI voice agents.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Execute agentic workflows, AI agents, and tools in AI Agent Studio with role masking.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Run and review agentic workflow executions on forms in the Core UI and workspaces.
-   Framework extensibility with a new condition builder.
-   Support multilingual conversations.

[Zurich Patch 3](../quality/zurich-patch-3.md)

-   Consume Global Graph as a Knowledge Graph resource.
-   Check for offensive content with MCP guardian.
-   Support the latest MCP version from [Zurich Patch 3](../quality/zurich-patch-3.md).

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Authenticate users with the MCP Server to add a Model Context Protocol tool to AI agents using the Model Context Protocol Client.
-   Create ACLs for AI agents and agentic workflows to customize who can discover and trigger AI agents and agentic workflows.

Zurich EA

-   Create and maintain versions of LLM instructions for AI agents and agentic workflows to help organize and iterate on prompts and test their effectiveness.
-   Duplicate existing script, record operations, and search retrieval tools to reduce the work needed to create unique AI agents.
-   Monitor new analytics in the AI Agents Analytics dashboard to track valuable insights in customer satisfaction with AI interactions.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   View the agentic workflow and AI agent activity on your AI Agent Studio.

See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

For the Platform Now Assist release notes, see [Now Assist release notes](../analytics-intelligence-reporting/now-assist-rn.md).

**Important:** Now Assist AI agents are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The AI-native experience for an AI agent is available exclusively with the installation of the Off Glide Conversation Server plugin \(com.glide.cs.offglide\).

    **Note:** To use the AI agent in AI-native mode, make sure to test it so it works as expected.

-   **[Test an agentic solution in AI Native mode](https://www.servicenow.com/docs/access?context=test-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the AI Native playground experience to test your agentic solutions.

    **Note:** The AI-native playground experience is exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard testing playground.

-   **[Add tools and information to an AI agent](https://www.servicenow.com/docs/access?context=add-tool-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Add widgets for tool outputs to provide an improved experience in AI-native mode.

    **Note:** The display output widget options are exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard add tool form.


-   **[Evaluate voice AI agents for overall task completion and tool choice accuracy](https://www.servicenow.com/docs/access?context=execute-aia-eval&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Automated evaluations support voice AI agents. Get a better picture of overall performance by evaluating previous executions against standardized metrics.


-   **[ServiceNow AI agents as secondary agents](https://www.servicenow.com/docs/access?context=secondary-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enhance user experience for Secondary Agents by displaying the Agent card URL to admins for easy access and management so the admin can view, copy, and consume the URL easily.

    Additionally, when adding an MCP tool, the name and description of the tool are populated automatically as per the details fetched from the server and the user can update the details.


-   **[Configure role masking for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Role masking restricts access to specific roles based on configuration to verify that agentic workflows, AI agents, and tools run within the boundaries of the roles configured to meet their business needs while reducing the risk of unauthorized access to the agents and the agentic data.

-   **[Add AI agent learning](https://www.servicenow.com/docs/access?context=agent-learning&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enhance AI agent learning through episodic memory, enabling AI agents to improve by learning from past successful interactions.

-   **[Select channels and access for an agentic workflow](https://www.servicenow.com/docs/access?context=channels-access-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Create and update UI actions for workflow executions and display handling. You can specify conditions for the display of the UI actions.

-   **[Add a defined desktop action tool to an AI agent for desktop and web-based task](https://www.servicenow.com/docs/access?context=add-desktop-action-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Add Desktop action as a tool to an AI agent to perform desktop automation for repetitive tasks.

-   **[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Support multilingual conversations for AI agents across languages.

-   **[Manually test the execution of an AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The testing page on AI Agent Studio has two testing options:

    -   Manual test
    -   Automated evaluation
    Observe the different versions of an AI agent behavior in manual tests and in automated evaluations using the **Manual tests** and **Automated tests** tabs.

-   **[Test user access to an AI agent](https://www.servicenow.com/docs/access?context=test-aia-access&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Test user access to an agentic workflow](https://www.servicenow.com/docs/access?context=test-aw-access&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Test how an AI agent or agentic workflow completes a task and if it enables users permission to access it.

-   **[Model Context Protocol Client](https://www.servicenow.com/docs/access?context=mcp-client&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Authorization upgrades to support segregation of Resource Server and Authentication Server through Protected Resource Metadata \(PRM\).
    -   Use the **mcp\_guardian\_check** property to enable guardian checks for MCP Client when there’s an MCP tool call.
    -   Supervise the pagination with mouse device support to show large number of services from an MCP server through the **sn\_mcp\_client.cursor.max\_iterations** system property.
    -   Add a title field for human-friendly display names that can be used as a programmatic identifier.
-   **[Use in-product experiences for agentic workflows on forms](https://www.servicenow.com/docs/access?context=in-product-agentic-ai&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    In the Core UI and workspaces, you can use UI and declarative actions to run agentic workflows. You can also see the presence, progress, and output of agentic workflows performed on a record. The execution details for each agentic workflow include who is supervising the workflow, estimated and total time taken, processing messages, and step history.

-   **[Review and approve requests and tickets with the Approval Assistance AI agent](https://www.servicenow.com/docs/access?context=platform-approval-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    You can use the new approval assistance AI agent to view all pending approval requests and access detailed information about them. You can then approve requests and tickets and make updates to them from Now Assist in Virtual Agent.

-   **[View the Approval Info Record widget](https://www.servicenow.com/docs/access?context=approval-info-record-widget&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    The Service Portal Approval Info Record widget shows details about the approval request and a full record for an approval including the activity stream.

-   **[Configure email notification alerts for AI agent and agentic workflow executions](https://www.servicenow.com/docs/access?context=config-aia-notifications&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Configure alert email notifications for unexpected or undesired behavior from AI agents and agentic workflows. You can configure the thresholds for triggering the alerts on the Agent Properties table, and you can add or update the recipients of the email notifications from the Notifications table.

-   **[Create an external AI agent](https://www.servicenow.com/docs/access?context=create-external-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Create new external AI agents that connect to third-party agentic AI systems. Use Agent2Agent protocol or integrate agents manually to configure them in AI Agent Studio to use in the ServiceNow agentic AI system.

-   **[Add a Knowledge Graph to an AI agent](https://www.servicenow.com/docs/access?context=add-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use Enterprise Graph \(Small\) as a resource to create a Knowledge Graph tool for an AI agent in the AI Agent Studio.


-   **[Add an MCP server tool to an AI agent](https://www.servicenow.com/docs/access?context=add-mcp-server-tool&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The Model Context Protocol Client enables guardian checks for offensive content when Notion is selected as the MCP server.

-   **[Configure Model Context Protocol Client](https://www.servicenow.com/docs/access?context=configuring-mcp-client&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The Model Context Protocol Client application supports the latest MCP version.

-   **[Add a Knowledge Graph to an AI agent](https://www.servicenow.com/docs/access?context=add-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use Global Graph as a Knowledge Graph resource when creating a Knowledge Graph tool for an AI agent in the AI Agent Studio.


-   **[Model Context Protocol Client](https://www.servicenow.com/docs/access?context=mcp-client&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enable users of the ServiceNow® AI Agent Studio to access tools that are hosted externally and published using an MCP server via the Model Context Protocol Client application.

    Authenticate users with the MCP server to add the MCP tool to an AI agent.

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Review agentic activity in AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    View and troubleshoot the agentic workflow and AI agent executions on AI Agent Studio via the **Activity** page.

-   **[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) - Dynamic Orchestrator**

    Maps the appropriate agents for an agentic workflow with Dynamic Orchestrator for better performance and accuracy of the agentic workflow execution.

-   **[View analytics for customer satisfaction with AI interactions](https://www.servicenow.com/docs/access?context=ai-agent-dashboard&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Multiple new metrics have been added to the AI Agent Analytics dashboard, accessible from the AI Agent Studio to provide insight into average customer satisfaction and customer satisfaction with the best and worst performing agentic workflows and agents.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Add tools and information to an AI agent](https://www.servicenow.com/docs/access?context=add-tool-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The output transformation strategy for an AI agent output contains a new option called **Custom**. Using the custom output transformation strategy, the tool output gets transformed according to the LLM instructions.

-   **[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) - AI Agent Background Channel**

    Invoke the agentic conversations from Workspace or Core UI via the AI Agent Background channel that is associated with the AI Agent Background Provider to execute the AI agents and agentic workflows.

-   **[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) - Interactive and non interactive AI agents**

    Run AI agents and agentic workflows execution in one of the following ways:

    -   **Interactive Mode**: AI agents reach out to the user for information during fallback.
    -   **Non interactive Mode**: AI agents don’t reach out to the user during fallback but send the execution output to the user.

## UI changes

-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The guided setups for creating an AI agent and agentic workflow have been updated.

-   **[Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    New security configuration UI pages have been added in the AI Agent Studio application to configure security controls for agentic workflows and AI agents for role masking.


-   **[Follow new guided setups for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The new steps for the guided setups for AI voice agents and agentic workflows include additional help text and guidance for writing LLM instructions to help improve outcome and task completion.

-   **[Manually test the execution of an AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The tab names on the AI Agent Studio testing page have been renamed. The **Test scenario** tab is renamed to **Test AI reasoning** and the **Output** tab is renamed to **Chat responses**.


## Changed in this release

-   **[Create an external AI agent with the Agent2Agent protocol](https://www.servicenow.com/docs/access?context=create-a2a-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the A2A Protocol integration for creating external agents in the AI Agent Studio to connect with the ServiceNow AI Platform.

-   **[Updates to platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Analyze task trends](https://www.servicenow.com/docs/access?context=incident-trends&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Identify ways to improve service](https://www.servicenow.com/docs/access?context=service-improvement&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) now have post-analysis actions, including the option to download analysis and ask additional information. [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) can run as a scheduled job.

-   **[Agentic evaluation offer issue tracing and suggested optimizations](https://www.servicenow.com/docs/access?context=agentic-evals&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    After an automated evaluation of an agentic AI asset, you can receive a list of issues and suggested optimizations to address those issues. Issues come with individual record node-by-node traces to pinpoint the exact source of problems. Optimizations are suggested, and you can apply them and run a reevaluation from a single guided flow.


-   **[Updates to platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Generate resolution plans](https://www.servicenow.com/docs/access?context=resolve-requests&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) now takes related records into account when planning next steps. [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) shows suggested next steps and reruns after work is done. [Process images for new tasks](https://www.servicenow.com/docs/access?context=images-tasks&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) now links to the created task record upon creation and includes certain metadata from the image.


-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Platform Request status AI agent](https://www.servicenow.com/docs/access?context=ticket-status-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The request status AI agent provides an AI-generated summary of the most recent comments from the AI agent or other people working on a ticket. You can add attachments to an open ticket or incident to support a request action. To find more information about an open ticket, you can ask the request status AI agent follow-up questions based on previous answers from the agent.

-   **[Understand the Now Assist AI agents](https://www.servicenow.com/docs/access?context=understand-na-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The base reflection prompt has been replaced with the ReAct Orchestrator prompt, introducing a Route scheduling mode when an agent needs assistance from another agent during execution.

-   **[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Run AI agents and agentic workflows concurrently in AI Agent Background Channel and in Non-interactive mode.

-   **[Add a Knowledge Graph to an AI agent](https://www.servicenow.com/docs/access?context=add-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The Global Graph resource for creating a Knowledge Graph tool has been renamed to Enterprise Graph.


-   **[Review and complete actions on requests using the Request Status AI agent](https://www.servicenow.com/docs/access?context=ticket-status-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The ticket status AI agent has been renamed to the request status AI agent. Request details include an AI-generated summary of the most recent comments on a request. Performance has been improved.

-   **[Confirm your web search tool provider data policies](https://www.servicenow.com/docs/access?context=add-web-search-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    If you select Google as your web search provider for web search AI agent tools, Google uses [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment, and data may be routed to places outside of regions specified on your ServiceNow AI Platform instance as a result. Consult your organization's data policies before enabling AI agents with web search tools that use Google as the provider.


-   **[Add version control to instructions sent to the LLM](https://www.servicenow.com/docs/access?context=version-control&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    You can review multiple versions of instructions sent to the LLM when designing your AI agents or agentic workflows. You can choose which version is active to help with testing or evaluating the success of an AI agent or agentic workflow to compare against other versions. Versions are named and ordered by time created for organizational purposes.

-   **[Duplicate and edit existing tools when creating new AI agents](https://www.servicenow.com/docs/access?context=add-tool-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    When adding a tool to an AI agent, you can select an existing tool instead of creating a new tool. After an existing tool is added, you can change it to suit the specific needs of an AI agent.

-   **[Now Assist AI agents reference](https://www.servicenow.com/docs/access?context=na-aia-reference&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The **sn\_aia.enable\_agent\_tool\_input\_value\_overrides** system property is migrated to the Agent properties \[sn\_aia\_property\] table.


## Deprecated features

-   The support for manually integrating external agents has been deprecated from [Zurich Patch 8](../quality/zurich-patch-8.md) release.

## Activation information

Now Assist AI agents are available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using Now Assist AI agents, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Additional requirements

You must first install the supported Now Assist version of the ServiceNow AI Platform to be able to use Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Next Experience UI Framework must be enabled before you can use the Now Assist panel.

## Browser requirements

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.

## Accessibility information

-   **[Voice Input for Now Assist AI agents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see [Enable voice input for Now Assist panel](https://www.servicenow.com/docs/access?context=enable-voice-input-for-now-assist-panel&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

    After enabled, the Enable voice input for the Now Assist panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

    Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


## Localization information

The Now Assist AI agents application is built on the GPT-4o-based framework and supports localization according to the GPT-4o model.

## Related ServiceNow applications and features

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    With the ServiceNow®Now Assist panel, you can get assistance from generative AI experiences to solve customer issues faster. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information more quickly.

-   **[Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow® Generative AI Controller lets you integrate third-party LLM \(large language models\) with your workflows.

-   **[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers you need.

-   **[Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the ServiceNow® Now Assist Skill Kit to create and publish custom prompts and skills for Now Assist. Creating custom skills and prompts enables you to have greater flexibility with Now Assist generative AI capabilities.


**Parent Topic:**[AI Experiences release notes](../analytics-intelligence-reporting/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

