---
title: Combined AI Agent Studio release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for AI Agent Studio from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-aiagentstudio-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined AI Agent Studio release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for AI Agent Studio from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Agent Studio release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Agent Studio to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

-   **[Evaluate voice AI agents for overall task completion and tool choice accuracy](https://www.servicenow.com/docs/access?context=execute-aia-eval&family=zurich&ft:locale=en-US)**

Automated evaluations support voice AI agents. Get a better picture of overall performance by evaluating previous executions against standardized metrics.


</td></tr><tr><td>

Australia

</td><td>

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


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing AI Agent Studio features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Updates to platform agentic workflows](https://www.servicenow.com/docs/access?context=platform-use-cases&family=zurich&ft:locale=en-US)**

Several platform agentic workflows have seen updates to how they work and what configurations are available for AI admins. [Generate resolution plans](https://www.servicenow.com/docs/access?context=resolve-requests&family=zurich&ft:locale=en-US) now takes related records into account when planning next steps. [Generate my work plan](https://www.servicenow.com/docs/access?context=generate-work-plan&family=zurich&ft:locale=en-US) shows suggested next steps and reruns after work is done. [Process images for new tasks](https://www.servicenow.com/docs/access?context=images-tasks&family=zurich&ft:locale=en-US) now links to the created task record upon creation and includes certain metadata from the image.


</td></tr><tr><td>

Australia

</td><td>

-   **[External agents with Agent2Agent](https://www.servicenow.com/docs/access?context=create-a2a-agent&family=australia&ft:locale=en-US)**

The name of the button on the agent selection pop-up in the Discover and activate section of the external agents guided setup has been renamed to **Selected**.


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

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some AI Agent Studio features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

-   The support for manually integrating external agents has been deprecated from [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US) release.

</td></tr><tr><td>

Australia

</td><td>

-   The support for manually integrating external agents has been deprecated from [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US) release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate AI Agent Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Activation information**

AI agents are available with activation of AI plugins from the ServiceNow Store. For more information about the prerequisites for using AI agents and AI Agent Studio, see [Install ServiceNow Otto AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

AI agents and AI Agent Studio are available with activation of any AI plugin from the ServiceNow Store. For more information about the prerequisites for using AI agents, see [Install ServiceNow Otto AI Agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Agent Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Additional requirements**

You must first install the supported application version of the ServiceNow AI Platform to be able to use AI agents and AI Agent Studio. For more information, see [Install ServiceNow Otto AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&family=zurich&ft:locale=en-US).

Next Experience UI Framework must be enabled before you can use the ServiceNow Otto panel.


</td></tr><tr><td>

Australia

</td><td>

-   **Additional requirements**

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

Zurich

</td><td>

-   **Browser requirements**

AI agents and AI Agent Studio support various browsers, including Google Chrome and Microsoft Edge. AI agents and AI Agent Studio aren't supported in Internet Explorer.


</td></tr><tr><td>

Australia

</td><td>

-   **Browser requirements**

AI agents and AI Agent Studio support various browsers, including Google Chrome and Microsoft Edge. AI agents and AI Agent Studio aren't supported in Internet Explorer.


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Agent Studio, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **[Voice Input for AI agents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the ServiceNow Otto panel in the . This feature gives users a voice-to-text input option to access the generative AI skills in the panel in any supported language. For more information, see [Enable voice input for ServiceNow Otto panel](https://www.servicenow.com/docs/access?context=enable-voice-input-for-now-assist-panel&family=zurich&ft:locale=en-US).

After enabled, the Enable voice input for the ServiceNow Otto panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&family=zurich&ft:locale=en-US) for more information.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


</td></tr><tr><td>

Australia

</td><td>

-   **Accessibility information**
    -   **[Voice Input for AI agents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=australia&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the ServiceNow Otto panel in the AI Admin Hub. This feature gives users a voice-to-text input option to access the generative AI skills in the panel in any supported language. For more information, see [Enable voice input for ServiceNow Otto panel](https://www.servicenow.com/docs/access?context=enable-voice-input-for-now-assist-panel&family=australia&ft:locale=en-US).

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

Zurich

</td><td>

-   **Localization information**

AI agents and AI Agent Studio are built on the GPT-4o-based framework and supports localization according to the GPT-4o model.


</td></tr><tr><td>

Australia

</td><td>

-   **Localization information**

AI agents and AI Agent Studio are built on the GPT-4o-based framework and supports localization according to the GPT-4o model.


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for AI Agent Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

[Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US)

-   Redesigned AI Agent Studio with streamlined setup and evaluation processes for agentic AI assets.
-   Custom headers in external agents configuration.
-   AI specialist configuration and deployment to harness coordinated agentic AI that reasons and executes end-to-end work.

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

-   Redesigned AI Agent Studio with streamlined setup and evaluation processes for agentic AI assets.
-   Custom headers in external agents configuration.
-   AI specialist configuration and deployment to harness coordinated agentic AI that reasons and executes end-to-end work.

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

 See [AI Agent Studio \(legacy\)](https://www.servicenow.com/docs/access?context=na-ai-agents&family=australia&ft:locale=en-US) for more information.

 For the Platform AI release notes, see [AI Admin Hub release notes](https://www.servicenow.com/docs/access?context=now-assist-rn&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

