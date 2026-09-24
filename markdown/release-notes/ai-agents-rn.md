---
title: AI Agent Studio release notes
description: The ServiceNow AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Brazil release.The ServiceNow AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/ai-agents-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [AI Experiences release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# AI Agent Studio release notes

The ServiceNow® AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Brazil release.

## About AI Agent Studio



-   Redesigned AI Agent Studio with streamlined setup and evaluation processes for agentic AI assets.
-   Custom headers in external agents configuration.
-   AI specialist configuration and deployment to harness coordinated agentic AI that reasons and executes end-to-end work.



-   Add or remove AI agents or tools from the built-in AI agents.
-   Detect and disable runaway AI agent triggers to prevent unintended consumption.
-   Support conversation history for Knowledge Graph tool.
-   Enforce deny-by-default ACLs for new agentic ACL types.
-   Enable AI Agent Studio skill migration to Mosaic.



-   Enable UI validation for agentic AI processes and generative AI skills.



-   Test an agentic solution in the playground in AI-native mode.
-   Add widgets for tool outputs to provide an improved experience in AI-native mode.
-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Get more insights into agentic AI asset performance with issue tracing and suggested optimizations from results pages.

See [AI Agent Studio \(legacy\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-ai-agents.md) for more information.

For the Platform AI release notes, see .

## Activation and other requirements

**Important:** AI agents and AI Agent Studio are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    AI agents and AI Agent Studio are available with activation of any AI plugin from the ServiceNow Store. For more information about the prerequisites for using AI agents, see [Install ServiceNow Otto AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-ai-agents-plugins.md).

-   **Browser requirements**

    AI agents and AI Agent Studio support various browsers, including Google Chrome and Microsoft Edge. AI agents and AI Agent Studio aren't supported in Internet Explorer.

-   **Additional requirements**

    You must first install the supported version of the ServiceNow AI Platform to be able to use AI agents and AI Agent Studio. For more information, see [Install ServiceNow Otto AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-ai-agents-plugins.md).

    Next Experience UI Framework must be enabled before you can use the ServiceNow Otto panel.


## Accessibility and localization

-   **Accessibility information**
    -   **[Voice Input for AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md)**

        Administrators can enable an optional voice input setting for the ServiceNow Otto panel in the AI Admin Hub. This feature gives users a voice-to-text input option to access the generative AI skills in the panel in any supported language. For more information, see [Enable voice input for ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/enable-voice-input-for-now-assist-panel.md).

        After enabled, the Enable voice input for the ServiceNow Otto panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/next-experience-accessibility-preferences.md) for more information.

        Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.

-   **Localization information**

    AI agents and AI Agent Studio are built on the GPT-4o-based framework and supports localization according to the GPT-4o model.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/intelligent-experiences-rn-landing.md)

## September 2026

The ServiceNow® AI agents and AI Agent Studio provide solutions that can perceive the environment, decide, and proactively act to achieve specific goals without the need for constant human oversight. AI Agent Studio was enhanced and updated in the Brazil release.

### New in the Brazil release

-   **[Define security controls for MCP Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-sec-mcp.md)**

    Define access rules and tools in the Model Context Protocol Servers for security control before adding them as tools to an AI agent.

-   **[Create an external AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-a2a-agent-new.md)**

    Add security controls and tools to external AI agents.

-   **[Test access to an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/test-access-ai-asset.md)**

    Test access to an AI asset to verify whether a user has access to an agentic AI asset - AI agent and agentic workflow. In case of access denial, use Access Analyzer to see the access results in Access Management.

-   **[Create an external AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-a2a-agent-new.md)**

    The redesigned AI Agent Studio streamlines the creation and testing of external AI agents.

-   **[Model Context Protocol Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mcp-client-landing.md)**

    The Model Context Protocol Client application has been redesigned.

-   **[Implement access control in AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/implement-aias-security-new.md)**

    Enforce deny-by-default access control for agentic AI record types \(`gen_ai_agent`, `gen_ai_workflow`, `gen_ai_skill`, `Flow`, `flow_action`\) for newly activated ServiceNow instances. In previous releases, these types defaulted to allow access.


### What's changed

-   **[New setup processes for agentic AI assets in redesigned AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aias-landing.md)**

    The redesigned AI Agent Studio reimagines the creation and deployment processes for agentic AI assets. New features include automated evaluations built in to the application and easy creation of AI agents for automation opportunities. See [Configure AI Agent Studio settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/config-aias-settings-new.md) for how to access the previous UI.


-   **[Platform Analyze task trends agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/incident-trends.md)**

    The Analyze task trends agentic workflow now includes citations for representative records associated with a pattern. Configure the workflow to include open tickets in its analysis by enabling the setting and running a Group Action Framework job to reindex with the new records.


