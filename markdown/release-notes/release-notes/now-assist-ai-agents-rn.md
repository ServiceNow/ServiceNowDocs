---
title: Now Assist AI Agents release notes
description: The ServiceNow Now Assist AI Agents application provides solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. Now Assist AI Agents was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-30"
reading_time_minutes: 5
---

# Now Assist AI Agents release notes

The ServiceNow® Now Assist AI Agents application provides solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. Now Assist AI Agents was enhanced and updated in the Australia release.

## Now Assist AI Agents highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

-   Test an agentic solution in the playground in AI-native mode.
-   Add widgets for tool outputs to provide an improved experience in AI-native mode.
-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Get more insights into agentic AI asset performance with issue tracing and suggested optimizations from results pages.

See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information.

For the Platform Now Assist release notes, see [Now Assist release notes](../analytics-intelligence-reporting/now-assist-rn.md).

**Important:** Now Assist AI agents are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The AI-native experience for an AI agent is available exclusively with the installation of the Off Glide Conversation Server plugin \(com.glide.cs.offglide\).

    **Note:** To use the AI agent in AI-native mode, make sure to test it so it works as expected.

-   **[Test an agentic solution in AI Native mode](https://www.servicenow.com/docs/access?context=test-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Use the AI Native playground experience to test your agentic solutions.

    **Note:** The AI-native playground experience is exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard testing playground.

-   **[Add tools and information to an AI agent](https://www.servicenow.com/docs/access?context=add-tool-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Add widgets for tool outputs to provide an improved experience in AI-native mode.

    **Note:** The display output widget options are exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard add tool form.


## UI changes

-   **[Manually test the execution of an AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) and [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The **AI Native** radio button in the Choose a testing mode section on the AI agent and agentic workflow manual testing playgrounds has been renamed to **Premium Chat**.


## Changed in this release

-   **[Create an external AI agent with the Agent2Agent protocol](https://www.servicenow.com/docs/access?context=create-a2a-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Use the A2A Protocol integration for creating external agents in the AI Agent Studio to connect with the ServiceNow AI Platform.

-   **[Updates to platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Analyze task trends](https://www.servicenow.com/docs/access?context=incident-trends&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) and [Identify ways to improve service](https://www.servicenow.com/docs/access?context=service-improvement&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) now have post-analysis actions, including the option to download analysis and ask additional information. [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) can run as a scheduled job.

-   **[Agentic evaluation offer issue tracing and suggested optimizations](https://www.servicenow.com/docs/access?context=agentic-evals&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    After an automated evaluation of an agentic AI asset, you can receive a list of issues and suggested optimizations to address those issues. Issues come with individual record node-by-node traces to pinpoint the exact source of problems. Optimizations are suggested, and you can apply them and run a reevaluation from a single guided flow.


## Deprecated features

[Australia Patch 1](../quality/australia-patch-1.md)

-   The support for manually integrating external agents has been deprecated from [Australia Patch 1](../quality/australia-patch-1.md) release.

## Activation information

Now Assist AI agents are available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using Now Assist AI agents, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Additional requirements

You must first install the supported Now Assist version of the ServiceNow AI Platform to be able to use Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Next Experience UI Framework must be enabled before you can use the Now Assist panel.

## Browser requirements

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.

## Accessibility information

-   **[Voice Input for Now Assist AI agents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see [Enable voice input for Now Assist panel](https://www.servicenow.com/docs/access?context=enable-voice-input-for-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

    After enabled, the Enable voice input for the Now Assist panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) for more information.

    Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


## Localization information

The Now Assist AI agents application is built on the GPT-4o-based framework and supports localization according to the GPT-4o model.

## Related ServiceNow applications and features

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    With the ServiceNow®Now Assist panel, you can get assistance from generative AI experiences to solve customer issues faster. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information more quickly.

-   **[Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow® Generative AI Controller lets you integrate third-party LLM \(large language models\) with your workflows.

-   **[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers you need.

-   **[Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    Use the ServiceNow® Now Assist Skill Kit to create and publish custom prompts and skills for Now Assist. Creating custom skills and prompts enables you to have greater flexibility with Now Assist generative AI capabilities.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

