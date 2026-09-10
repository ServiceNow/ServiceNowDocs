---
title: AI Agent Studio release notes
description: The ServiceNow AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.The ServiceNow AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.The ServiceNow AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.The ServiceNow AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.The ServiceNow AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.The ServiceNow AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-08-31"
reading_time_minutes: 10
---

# AI Agent Studio release notes

The ServiceNow® AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.

## About AI Agent Studio

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

-   Redesigned AI Agent Studio with streamlined setup and evaluation processes for agentic AI assets.
-   Custom headers in external agents configuration.
-   AI specialist configuration and deployment to harness coordinated agentic AI that reasons and executes end-to-end work.

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   Add or remove AI agents or tools from the built-in AI agents.
-   Detect and disable runaway AI agent triggers to prevent unintended consumption.
-   Support conversation history for Knowledge Graph tool.
-   Enforce deny-by-default ACLs for new agentic ACL types.
-   Enable AI Agent Studio skill migration to Mosaic.

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

-   Enable UI validation for agentic AI processes and generative AI skills.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Test an agentic solution in the playground in AI-native mode.
-   Add widgets for tool outputs to provide an improved experience in AI-native mode.
-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Get more insights into agentic AI asset performance with issue tracing and suggested optimizations from results pages.

See [AI Agent Studio \(legacy\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-agents.md) for more information.

For the Platform AI release notes, see [AI Admin Hub release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn.md).

## Activation and other requirements

**Important:** AI agents and AI Agent Studio are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    AI agents and AI Agent Studio are available with activation of any AI plugin from the ServiceNow Store. For more information about the prerequisites for using AI agents, see [Install ServiceNow Otto AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-ai-agents-plugins.md).

-   **Browser requirements**

    AI agents and AI Agent Studio support various browsers, including Google Chrome and Microsoft Edge. AI agents and AI Agent Studio aren't supported in Internet Explorer.

-   **Additional requirements**

    You must first install the supported version of the ServiceNow AI Platform to be able to use AI agents and AI Agent Studio. For more information, see [Install ServiceNow Otto AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-ai-agents-plugins.md).

    Next Experience UI Framework must be enabled before you can use the ServiceNow Otto panel.


## Accessibility and localization

-   **Accessibility information**
    -   **[Voice Input for AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)**

        Administrators can enable an optional voice input setting for the ServiceNow Otto panel in the AI Admin Hub. This feature gives users a voice-to-text input option to access the generative AI skills in the panel in any supported language. For more information, see [Enable voice input for ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-voice-input-for-now-assist-panel.md).

        After enabled, the Enable voice input for the ServiceNow Otto panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-accessibility-preferences.md) for more information.

        Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.

-   **Localization information**

    AI agents and AI Agent Studio are built on the GPT-4o-based framework and supports localization according to the GPT-4o model.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn-landing.md)

## September 2026

The ServiceNow® AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.

### New in the Australia release

-   ****

    Define access rules and tools in the Model Context Protocol Servers for security control before adding them as tools to an AI agent.

-   ****

    Add security controls and tools to external AI agents.

-   ****

    Test access to an AI asset to verify whether a user has access to an agentic AI asset - AI agent and agentic workflow. In case of access denial, use Access Analyzer to see the access results in Access Management.


### What's changed

-   **New setup processes for agentic AI assets in redesigned AI Agent Studio**

    The redesigned AI Agent Studio reimagines the creation and deployment processes for agentic AI assets. New features include automated evaluations built in to the application and easy creation of AI agents for automation opportunities. See Configure AI Agent Studio settings for how to access the previous UI.


-   **[Platform Analyze task trends agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/incident-trends.md)**

    The Analyze task trends agentic workflow now includes citations for representative records associated with a pattern. Configure the workflow to include open tickets in its analysis by enabling the setting and running a Group Action Framework job to reindex with the new records.


## August 2026

The ServiceNow® AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.

### What's new

-   **Use the redesigned AI Agent Studio**

    The redesigned AI Agent Studio streamlines the creation, testing, and evaluation processes for agentic AI assets on your instance. Use identified automation opportunities to build AI agents quickly. Create test scenarios for evaluation to detect recurring patterns and opportunities for optimization.

-   ****

    The redesigned AI Agent Studio streamlines the creation and testing of external AI agents.

-   ****

    The Model Context Protocol Client application has been redesigned.

-   **[Integrating external AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/external-agent-protocols.md)**

    External agents now support custom HTTP headers in the External Agent Configuration \[sn\_aia\_external\_agent\_configuration\] table. Specify headers in JSON format to have them automatically included in API calls to external endpoints, regardless of the connection type. This is useful for passing metadata and authentication requirements that your external systems require.

-   **Manage your AI specialist in AI Agent Studio**

    AI specialists autonomously resolve high-volume requests through a single persona, know when to hand off work outside their scope, and improve over time from feedback and track record. Deploy the same foundation to every team, then configure each one in AI Agent Studio to fit that team's specific needs. Contact your ServiceNow account manager for more information about accessing Autonomous Workforce.


## June 2026

The ServiceNow® AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.

### What's new

-   **[Add a Knowledge Graph to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-knowledge-graph.md)**

    The Knowledge Graph tool configuration in AI Agent Studio has a **Conversation history** toggle that is enabled by default. When enabled, the last 5 conversation turns from the active session are passed to the KG tool allowing users to ask follow-up questions that reference the previous results.

-   **[Kill Switch in Now Assist AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-kill-switch.md)**

    Runaway agent detection automatically disables an AI agent when the same record repeatedly triggers the same agent objective beyond a configured threshold, preventing unintended consumption of requests.

-   **[AI Agent Studio skills migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-ai-agents.md)**

    Auto-migrate all the AI Agent Studio skills from on-glide execution path to the off-glide execution path.

-   **[Deny-by-default ACL configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-acl-configuration.md)**

    Enforce deny-by-default access control for AI agentic record types \(`gen_ai_agent`, `gen_ai_workflow`, `gen_ai_skill`, `Flow`, `flow_action`\) for newly activated ServiceNow instances. In previous releases, these types defaulted to allow access.

-   **[Execute a run for an AI voice agentic asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/execute-voice-aia-eval.md)**

    Automated agentic evaluations are now available for voice agents. You can generate conversations based on scenarios that are described or input manually to generate execution logs for voice agents for evaluation.


### What's changed

-   **[Create an external AI agent with the Agent2Agent protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a2a-agent.md)**

    The name of the button on the agent selection pop-up in the Discover and activate section of the external agents guided setup has been renamed to **Selected**.


-   **[Set up AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/set-up-na-aia.md)**

    Use GPT-5.4 as the default model for the Orchestrator when Azure OpenAI is the selected LLM.

-   **[Select the LLM for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/select-aia-llm.md)**

    The default third-party \(3P\) models have been upgraded to the latest versions - GPT 5.2 to GPT 5.4 to use AI agents and AI Agent Studio.

    The new generative AI Config property records **sys\_generative\_ai\_config** and **sys\_generative\_ai\_prompt\_config** have been introduced for the following model providers:

    -   Amazon Bedrock: claude-sonnet-4-6
    -   Azure OpenAI: gpt 5.4
-   **[Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-use-cases.md)**

    The following platform agentic workflows had updates to their admin configurations and behavior in user-generated sessions.

    -   [Analyze task trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/incident-trends.md): Admin configurations for additional filters such as category and service have been added.
    -   [Generate my work plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generate-work-plan.md): Additional reasoning information for the generated work plan is now displayed after the plan is created.
    -   [Identify ways to improve services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/service-improvement.md): Admin configurations for additional filters such as category and service have been added.

## Australia General Availability

The ServiceNow® AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.

### What's changed

-   **[Manually test the execution of an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-agent.md) and [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md)**

    The **AI Native** radio button in the Choose a testing mode section on the AI agent and agentic workflow manual testing playgrounds has been renamed to **Premium Chat**.


-   **[Enable UI validation for agentic AI processes and generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md)**

    The glide.ai\_record\_activity.validation.feature.enabled system property enables UI rule validation \(such as required fields\) for AI‑initiated record updates. You can selectively apply this validation based on execution context using additional system properties. For example, glide.ai\_record\_activity.ai\_detection.nap.enabled applies validation to record updates triggered from the ServiceNow Otto panel. Similar properties control validation for AI skills, Virtual Agent, and agent‑initiated actions, as listed in the [Reference for AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md). This feature is opt‑in and inactive by default.

-   **[Create an external AI agent with the Agent2Agent protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a2a-agent.md)**

    The agent to agent flow actions no longer inject an `Authorization: Bearer` header automatically. If your endpoint requires a Bearer token, include the prefix directly in the API Key credential value.


## April 2026

The ServiceNow® AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Australia release.

### What's new

-   **[Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md)**

    The AI-native experience for an AI agent is available exclusively with the installation of the Off Glide Conversation Server plugin \(com.glide.cs.offglide\).

    **Note:** To use the AI agent in AI-native mode, make sure to test it so it works as expected.

-   **[Test an agentic solution in AI Native mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-agent.md)**

    Use the AI Native playground experience to test your agentic solutions.

    **Note:** The AI-native playground experience is exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard testing playground.

-   **[Add tools and information to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-tool-aia.md)**

    Add widgets for tool outputs to provide an improved experience in AI-native mode.

    **Note:** The display output widget options are exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard add tool form.


### What's changed

-   **[Create an external AI agent with the Agent2Agent protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a2a-agent.md)**

    Use the A2A Protocol integration for creating external agents in the AI Agent Studio to connect with the ServiceNow AI Platform.

-   **[Updates to platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-use-cases.md)**

    Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Analyze task trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/incident-trends.md) and [Identify ways to improve service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/service-improvement.md) now have post-analysis actions, including the option to download analysis and ask additional information. [Generate my work plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generate-work-plan.md) can run as a scheduled job.

-   **[Agentic evaluation offer issue tracing and suggested optimizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-evals.md)**

    After an automated evaluation of an agentic AI asset, you can receive a list of issues and suggested optimizations to address those issues. Issues come with individual record node-by-node traces to pinpoint the exact source of problems. Optimizations are suggested, and you can apply them and run a reevaluation from a single guided flow.


### What's deprecated or removed

-   The support for manually integrating external agents has been deprecated from [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md) release.

