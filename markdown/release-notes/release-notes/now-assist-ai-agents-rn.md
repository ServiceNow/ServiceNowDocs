---
title: Now Assist AI agents release notes
description: The ServiceNow Now Assist AI agents application provides solutions that can perceive the environment, make decisions, and proactively take actions to achieve specific goals without need for constant human oversight. Now Assist AI agents is a new application in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-02-11"
reading_time_minutes: 5
keywords: [Agentic AI, Now Assist AI Agents]
---

# Now Assist AI agents release notes

The ServiceNow® Now Assist AI agents application provides solutions that can perceive the environment, make decisions, and proactively take actions to achieve specific goals without need for constant human oversight. Now Assist AI agents is a new application in the Xanadu release.

## Now Assist AI agents highlights for the Xanadu release

[Xanadu Patch 10](../quality/xanadu-patch-10.md)

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

See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

For the Platform Now Assist release notes, see [Now Assist release notes](../analytics-intelligence-reporting/now-assist-rn.md).

**Important:** AI Agent Studio is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Now Assist AI agents features

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists \(ACLs\) for who can discover and trigger AI agents and agentic workflows in their guided setups in the AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to only authenticated users or publicly available.


-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

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
-   **[Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Create a use case with an execution plan to solve complex tasks with Now Assist. You can also do the following tasks:

    -   Clone an existing use case to avoid manual configuration.
    -   Create triggers when creating a use case that calls the AI agent when a condition or objective is observed.
    -   Test a use case before execution.
    -   Resolve record-based cases with AI agents.
-   **[Enable Now Assist Guardian in AI agents](https://www.servicenow.com/docs/access?context=enable-aia-na-guardian&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Enable Now Assist Guardian in AI agents to automatically identify and block offensive messages that are sent by human agents.

-   **[Multiple conversations in Now Assist AI agents](https://www.servicenow.com/docs/access?context=multiple-conversations-aia&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Enable live agents to interact with multiple AI agent conversations through the Now Assist panel.

-   **[AI Agent Analytics dashboard](https://www.servicenow.com/docs/access?context=ai-agent-dashboard&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Analyze the performance, efficiency gain, and usage of AI agents through preconfigured dashboards.


## UI changes

Xanadu Patch 5

-   Use cases are now called agentic workflows.

## Activation information

Now Assist in AI agents is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using Now Assist, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Additional requirements

You must first install the supported Now Assist version of ServiceNow to be able to use the Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

Enable the Next Experience UI Framework before you can use the Now Assist panel.

## Browser requirements

Now Assist AI agents supports various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents isn’t supported in Internet Explorer.

## Accessibility information

-   **[Voice Input for Now Assist AI agents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see Enable voice input for Now Assist panel.

    Once enabled, the Enable voice input for the Now Assist panel option will be available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for more information.

    Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


## Localization information

Now Assist AI agents is built on the GPT-4o-based framework and supports localization as per the GPT-4o model.

## Related ServiceNow applications and features

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    With the ServiceNow®Now Assist panel, you can get assistance from generative AI experiences to solve customer issues faster. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information more quickly.

-   **[Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow® Generative AI Controller lets you integrate third-party large language models \(LLMs\) with your workflows.

-   **[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers you need.

-   **[Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use the ServiceNow® Now Assist Skill Kit to create and publish custom prompts and skills for Now Assist. Creating custom skills and prompts enables you to have greater flexibility with Now Assist's generative AI capabilities.


**Parent Topic:**[Now Assist release notes](../now-assist/now-assist-rn-landing.md)

