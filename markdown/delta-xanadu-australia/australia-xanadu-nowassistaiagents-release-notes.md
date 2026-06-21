---
title: Combined Now Assist AI Agents release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Now Assist AI Agents from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-nowassistaiagents-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Now Assist AI Agents release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Now Assist AI Agents from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist AI Agents release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist AI Agents to Australia

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

Between your current release family and Australia, new features were introduced for Now Assist AI Agents.

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

-   **[Knowledge Graph](https://www.servicenow.com/docs/access?context=add-knowledge-graph&family=australia&ft:locale=en-US)**

The Knowledge Graph tool configuration in AI Agent Studio has a **Conversation history** toggle that is enabled by default. When enabled, the last 5 conversation turns from the active session are passed to the KG tool allowing users to ask follow-up questions that reference the previous results.

-   **[Kill Switch](https://www.servicenow.com/docs/access?context=aia-kill-switch&family=australia&ft:locale=en-US)**

Runaway agent detection automatically disables an AI agent when the same record repeatedly triggers the same agent objective beyond a configured threshold, preventing unintended consumption of Now Assist requests.

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

Between your current release family and Australia, some changes were made to existing Now Assist AI Agents features.

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

-   **[Set up Now Assist AI agents](https://www.servicenow.com/docs/access?context=set-up-na-aia&family=australia&ft:locale=en-US)**

Use GPT-5.4 as the default model for the Orchestrator when Azure OpenAI is the selected LLM.

-   **[Select the model provider](https://www.servicenow.com/docs/access?context=select-aia-llm&family=australia&ft:locale=en-US)**

The default third-party \(3P\) models have been upgraded to the latest versions - GPT 5.2 to GPT 5.4 to use Now Assist AI Agents.

The new generative AI Config property records **sys\_generative\_ai\_config** and **sys\_generative\_ai\_prompt\_config** have been introduced for the following model providers:

    -   Amazon Bedrock: claude-sonnet-4-6
    -   Azure OpenAI: gpt 5.4
-   **[Platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&family=australia&ft:locale=en-US)**

The following platform agentic workflows had updates to their admin configurations and behavior in user-generated sessions.

    -   [Analyze task trends](https://www.servicenow.com/docs/access?context=incident-trends&family=australia&ft:locale=en-US): Admin configurations for additional filters such as category and service have been added.
    -   [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&family=australia&ft:locale=en-US): Additional reasoning information for the generated work plan is now displayed after the plan is created.
    -   [Identify ways to improve services](https://www.servicenow.com/docs/access?context=service-improvement&family=australia&ft:locale=en-US): Admin configurations for additional filters such as category and service have been added.

-   **[Enable UI validation for agentic AI processes and Now Assist skills](https://www.servicenow.com/docs/access?context=na-aia-reference&family=australia&ft:locale=en-US)**

The glide.ai\_record\_activity.validation.feature.enabled system property enables UI rule validation \(such as required fields\) for AI‑initiated record updates. You can selectively apply this validation based on execution context using additional system properties. For example, glide.ai\_record\_activity.ai\_detection.nap.enabled applies validation to record updates triggered from the Now Assist panel. Similar properties control validation for AI skills, Virtual Agent, and agent‑initiated actions, as listed in the [Reference for Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-aia-reference&family=australia&ft:locale=en-US). This feature is opt‑in and inactive by default.

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

Between your current release family and Australia, some Now Assist AI Agents features or functionality were removed.

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

Between your current release family and Australia, some Now Assist AI Agents features or functionality were deprecated.

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

Review information on how to activate Now Assist AI Agents.

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

Now Assist AI agents are available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using Now Assist AI agents, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist AI Agents we have noted them here.

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

You must first install the supported Now Assist version of the ServiceNow AI Platform to be able to use Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=australia&ft:locale=en-US).

 Next Experience UI Framework must be enabled before you can use the Now Assist panel.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist AI Agents we have noted them here.

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

Now Assist AI agents support various browsers, including Google Chrome and Microsoft Edge. Now Assist AI agents aren't supported in Internet Explorer.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Now Assist AI Agents, such as specific requirements or compliance levels.

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

-   **[Voice Input for Now Assist AI agents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=australia&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see [Enable voice input for Now Assist panel](https://www.servicenow.com/docs/access?context=enable-voice-input-for-now-assist-panel&family=australia&ft:locale=en-US).

After enabled, the Enable voice input for the Now Assist panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&family=australia&ft:locale=en-US) for more information.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist AI Agents we have noted them here.

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

The Now Assist AI agents application is built on the GPT-4o-based framework and supports localization according to the GPT-4o model.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist AI Agents we have noted them here.

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

[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Add or remove AI agents or tools from the built-in AI agents.
-   Detect and disable runaway AI agent triggers to prevent unintended Now Assist consumption.
-   Support conversation history for Knowledge Graph tool.
-   Enforce deny-by-default ACLs for new agentic ACL types.
-   Enable AI Agent Studio skill migration to Mosaic.

 [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

-   Enable UI validation for agentic AI processes and Now Assist skills.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Test an agentic solution in the playground in AI-native mode.
-   Add widgets for tool outputs to provide an improved experience in AI-native mode.
-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Get more insights into agentic AI asset performance with issue tracing and suggested optimizations from results pages.

 See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&family=australia&ft:locale=en-US) for more information.

 For the Platform Now Assist release notes, see [Now Assist release notes](https://www.servicenow.com/docs/access?context=now-assist-rn&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

