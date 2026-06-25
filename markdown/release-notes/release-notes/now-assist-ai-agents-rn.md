---
title: Now Assist AI Agents release notes
description: The ServiceNow Now Assist AI Agents application provides solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. Now Assist AI Agents was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-30"
reading_time_minutes: 8
---

# Now Assist AI Agents release notes

The ServiceNow® Now Assist AI Agents application provides solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. Now Assist AI Agents was enhanced and updated in the Australia release.

## Now Assist AI Agents highlights for the Australia release

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   Add or remove AI agents or tools from the built-in AI agents.
-   Detect and disable runaway AI agent triggers to prevent unintended Now Assist consumption.
-   Support conversation history for Knowledge Graph tool.
-   Enforce deny-by-default ACLs for new agentic ACL types.
-   Enable AI Agent Studio skill migration to Mosaic.

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

-   Enable UI validation for agentic AI processes and Now Assist skills.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Test an agentic solution in the playground in AI-native mode.
-   Add widgets for tool outputs to provide an improved experience in AI-native mode.
-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Get more insights into agentic AI asset performance with issue tracing and suggested optimizations from results pages.

See [Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-agents.md) for more information.

For the Platform Now Assist release notes, see [Now Assist release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn.md).

**Important:** Now Assist AI agents are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Add a Knowledge Graph to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-knowledge-graph.md)**

    The Knowledge Graph tool configuration in AI Agent Studio has a **Conversation history** toggle that is enabled by default. When enabled, the last 5 conversation turns from the active session are passed to the KG tool allowing users to ask follow-up questions that reference the previous results.

-   **[Kill Switch in Now Assist AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-kill-switch.md)**

    Runaway agent detection automatically disables an AI agent when the same record repeatedly triggers the same agent objective beyond a configured threshold, preventing unintended consumption of Now Assist requests.

-   **[AI Agent Studio skills migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-ai-agents.md)**

    Auto-migrate all the AI Agent Studio skills from on-glide execution path to the off-glide execution path.

-   **[Deny-by-default ACL configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-acl-configuration.md)**

    Enforce deny-by-default access control for AI agentic record types \(`gen_ai_agent`, `gen_ai_workflow`, `gen_ai_skill`, `Flow`, `flow_action`\) for newly activated ServiceNow instances. In previous releases, these types defaulted to allow access.

-   **[Execute a run for an AI voice agentic asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/execute-voice-aia-eval.md)**

    Automated agentic evaluations are now available for voice agents. You can generate conversations based on scenarios that are described or input manually to generate execution logs for voice agents for evaluation.


-   **[Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md)**

    The AI-native experience for an AI agent is available exclusively with the installation of the Off Glide Conversation Server plugin \(com.glide.cs.offglide\).

    **Note:** To use the AI agent in AI-native mode, make sure to test it so it works as expected.

-   **[Test an agentic solution in AI Native mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-agent.md)**

    Use the AI Native playground experience to test your agentic solutions.

    **Note:** The AI-native playground experience is exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard testing playground.

-   **[Add tools and information to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-tool-aia.md)**

    Add widgets for tool outputs to provide an improved experience in AI-native mode.

    **Note:** The display output widget options are exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard add tool form.


## UI changes

-   **[Create an external AI agent with the Agent2Agent protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a2a-agent.md)**

    The name of the button on the agent selection pop-up in the Discover and activate section of the external agents guided setup has been renamed to **Selected**.


-   **[Manually test the execution of an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-agent.md) and [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md)**

    The **AI Native** radio button in the Choose a testing mode section on the AI agent and agentic workflow manual testing playgrounds has been renamed to **Premium Chat**.


## Changed in this release

-   **[Set up Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/set-up-na-aia.md)**

    Use GPT-5.4 as the default model for the Orchestrator when Azure OpenAI is the selected LLM.

-   **[Select the LLM for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/select-aia-llm.md)**

    The default third-party \(3P\) models have been upgraded to the latest versions - GPT 5.2 to GPT 5.4 to use Now Assist AI Agents.

    The new generative AI Config property records **sys\_generative\_ai\_config** and **sys\_generative\_ai\_prompt\_config** have been introduced for the following model providers:

    -   Amazon Bedrock: claude-sonnet-4-6
    -   Azure OpenAI: gpt 5.4
-   **[Platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-use-cases.md)**

    The following platform agentic workflows had updates to their admin configurations and behavior in user-generated sessions.

    -   [Analyze task trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/incident-trends.md): Admin configurations for additional filters such as category and service have been added.
    -   [Generate my work plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generate-work-plan.md): Additional reasoning information for the generated work plan is now displayed after the plan is created.
    -   [Identify ways to improve services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/service-improvement.md): Admin configurations for additional filters such as category and service have been added.

-   **[Enable UI validation for agentic AI processes and Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md)**

    The glide.ai\_record\_activity.validation.feature.enabled system property enables UI rule validation \(such as required fields\) for AI‑initiated record updates. You can selectively apply this validation based on execution context using additional system properties. For example, glide.ai\_record\_activity.ai\_detection.nap.enabled applies validation to record updates triggered from the Now Assist panel. Similar properties control validation for AI skills, Virtual Agent, and agent‑initiated actions, as listed in the [Reference for Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md). This feature is opt‑in and inactive by default.

-   **[Create an external AI agent with the Agent2Agent protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a2a-agent.md)**

    The agent to agent flow actions no longer inject an `Authorization: Bearer` header automatically. If your endpoint requires a Bearer token, include the prefix directly in the API Key credential value.


-   **[Create an external AI agent with the Agent2Agent protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a2a-agent.md)**

    Use the A2A Protocol integration for creating external agents in the AI Agent Studio to connect with the ServiceNow AI Platform.

-   **[Updates to platform agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-use-cases.md)**

    Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Analyze task trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/incident-trends.md) and [Identify ways to improve service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/service-improvement.md) now have post-analysis actions, including the option to download analysis and ask additional information. [Generate my work plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generate-work-plan.md) can run as a scheduled job.

-   **[Agentic evaluation offer issue tracing and suggested optimizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-evals.md)**

    After an automated evaluation of an agentic AI asset, you can receive a list of issues and suggested optimizations to address those issues. Issues come with individual record node-by-node traces to pinpoint the exact source of problems. Optimizations are suggested, and you can apply them and run a reevaluation from a single guided flow.


## Deprecated features

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   The support for manually integrating external agents has been deprecated from [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md) release.

## Activation information

Now Assist AI agents are available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using Now Assist AI agents, see [Install Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-ai-agents-plugins.md).

## Additional requirements

You must first install the supported Now Assist version of the ServiceNow AI Platform to be able to use Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-ai-agents-plugins.md).

Next Experience UI Framework must be enabled before you can use the Now Assist panel.

## Browser requirements

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.

## Accessibility information

-   **[Voice Input for Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see [Enable voice input for Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-voice-input-for-now-assist-panel.md).

    After enabled, the Enable voice input for the Now Assist panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-accessibility-preferences.md) for more information.

    Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


## Localization information

The Now Assist AI agents application is built on the GPT-4o-based framework and supports localization according to the GPT-4o model.

## Related ServiceNow applications and features

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    With the ServiceNow®Now Assist panel, you can get assistance from generative AI experiences to solve customer issues faster. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information more quickly.

-   **[Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller.md)**

    The ServiceNow® Generative AI Controller lets you integrate third-party LLM \(large language models\) with your workflows.

-   **[AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/overview-ais.md)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers you need.

-   **[Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit-landing.md)**

    Use the ServiceNow® Now Assist Skill Kit to create and publish custom prompts and skills for Now Assist. Creating custom skills and prompts enables you to have greater flexibility with Now Assist generative AI capabilities.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn-landing.md)

