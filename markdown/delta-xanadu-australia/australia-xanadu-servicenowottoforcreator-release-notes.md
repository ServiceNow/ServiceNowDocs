---
title: Combined ServiceNow Otto for Creator release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for ServiceNow Otto for Creator from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-servicenowottoforcreator-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for Creator release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for ServiceNow Otto for Creator from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for Creator release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for Creator to Australia

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

-   **Upgrade information**

[Australia Early Availability](https://www.servicenow.com/docs/access?context=australia-all-other-fixes&family=australia&ft:locale=en-US)

    -   To upgrade the Build Agent application, upgrade the ServiceNow Otto for Creator application \(sn\_now\_creator\), which includes the Build Agent Pro plugin \(sn\_build\_agent\_pro\). To upgrade the Build Agent \(Trial\) app, upgrade the sn\_build\_agent plugin.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow Otto for Creator.

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

-   **[Build Agent, an autonomous AI agent for ServiceNow application development](https://www.servicenow.com/docs/access?context=build-agent&family=yokohama&ft:locale=en-US)**

Build Agent, located in a chat panel within the ServiceNow IDE, functions as an autonomous AI agent capable of independently generating a complete ServiceNow application. It can handle various code-related tasks, such as rewriting tables, explaining code, validating and improving existing applications, fixing application errors, and more.

-   **[Generate catalog items conversationally with Now Assist in Catalog Builder](https://www.servicenow.com/docs/access?context=create-catalog-item-using-now-assist&family=yokohama&ft:locale=en-US)**

Create catalog items and record producers efficiently using the conversational interface within Catalog Builder. Communicate your requirements and specifications for your desired catalog items through guided conversation. Now Assist for catalog generation helps to simplify and streamline the catalog item creation process.


</td></tr><tr><td>

Zurich

</td><td>

-   **[MCP connections and Build Agent](https://www.servicenow.com/docs/access?context=accelerate-design-to-development-with-figma-mcp-server&family=zurich&ft:locale=en-US)**

You can now connect the Build Agent to the Figma MCP server. The Figma MCP server enables the Build Agent to access the structured data within Figma files. This connection accelerates the transition from application design to development, helping to make the developer workflow more efficient.


</td></tr><tr><td>

Australia

</td><td>

-   **[Upload brand guidelines to generate theme colors](https://www.servicenow.com/docs/access?context=tb-create-a-theme-ai&family=australia&ft:locale=en-US)**

Upload brand guidelines as a PDF to the Theme Builder theme creation workflow to generate themes aligned with your brand.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Otto for Creator features.

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

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&family=yokohama&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Australia

</td><td>

-   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow Otto for Creator features or functionality were removed.

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

Between your current release family and Australia, some ServiceNow Otto for Creator features or functionality were deprecated.

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

-   Spoke generation has been removed from ServiceNow Otto for Creator. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website for additional information.

</td></tr><tr><td>

Zurich

</td><td>

-   Starting with version 28.4.3 of ServiceNow Otto for Creator, the now.assist.creator role has been removed as a required role for using most ServiceNow Otto for Creator skills and agents. Some skills and agents might have additional role requirements. See the [ServiceNow Otto for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&family=zurich&ft:locale=en-US) product documentation for more information.

</td></tr><tr><td>

Australia

</td><td>

Spoke generation has been removed from ServiceNow Otto for Creator. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website for additional information.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow Otto for Creator.

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

-   **Activation information**

Install ServiceNow Otto for Creator by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install ServiceNow Otto for Creator by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install ServiceNow Otto for Creator by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for Creator we have noted them here.

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
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Otto for Creator we have noted them here.

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
</table>## Accessibility information

Review details on accessibility information for ServiceNow Otto for Creator, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for ServiceNow Otto for Creator we have noted them here.

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
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Otto for Creator we have noted them here.

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

[Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Create, edit, and deploy fully functional ServiceNow applications using the Build Agent in the ServiceNow IDE.
-   Generate catalog items conversationally and preview them during the creation process with Now Assist in Catalog Builder.
-   Choose an AI model provider for all ServiceNow Otto for Code skills in the script editor.

 [Yokohama Patch 8](https://www.servicenow.com/docs/access?context=yokohama-patch-8&family=yokohama&ft:locale=en-US)

-   Removed the now.assist.creator role as a requirement for test generation.

 [Yokohama Patch 6](https://www.servicenow.com/docs/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

**Note:** Additional AI model providers are supported for the following ServiceNow Otto for Creator skills:

    -   App generation
    -   App summarization
    -   Catalog item generation
    -   Code generation
    -   Flow generation
    -   Flow summarization
    -   Playbook generation
    -   Process Mining
    -   RPA bot generation
    -   Spoke generation
    -   Test generation

 [Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   Summarize what a flow or subflow does by using generative AI.
-   Generate playbooks from inputs that refer to active actions, flows, subflows, content from installed spokes, or activity definitions.
-   Create automation and UI components in Now Assist for app generation.
-   Use the code explain and summarize feature of ServiceNow Otto for Code to explain and summarize the code. This feature is supported by both Now LLM Service and the Azure OpenAI model providers.
-   Use the Client Script Summarization skill to generate a high-level summary and a detailed explanation of a client script.

 [Yokohama Patch 1](https://www.servicenow.com/docs/access?context=yokohama-patch-1&family=yokohama&ft:locale=en-US)

-   Enable your users to create applications by using the Now Assist for app generation skill even if they don't have the admin role.
-   Use the improved application preview before generating an application by using the Now Assist for app generation skill.
-   Enable your RPA Desktop Design Studio users to create and edit automations and activities, and extend automation logic flow with ServiceNow Otto for RPA Hub.
-   Enable your ServiceNow Studio users to generate a summary of an app.
-   Use the **Quick Actions** button in the ServiceNow Otto for Code enabled script editor to edit code and add comments.
-   Use the prompt modal in inline or floating mode with ServiceNow Otto for Code.
-   ServiceNow Otto for Code now supports both Now LLM Service and Azure OpenAI model providers. When you select the Azure OpenAI model provider, all requests for the ServiceNow Otto for Code model are redirected to Azure OpenAI for evaluation and response. Additionally, you get access to the Code Explain and Code Summarize features.
-   Use the auto-complete feature of ServiceNow Otto for Code to get contextually relevant code suggestions while typing.

 See [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 9](https://www.servicenow.com/docs/access?context=zurich-patch-9&family=zurich&ft:locale=en-US)

-   Upload brand guidelines as a PDF to the Theme Builder theme creation workflow to generate themes aligned with your brand.
-   Leverage the new widget generation and widget updation skills to create widgets and modify existing widgets within the Next Experience UI Framework using natural language prompts.
-   Troubleshoot Automated Test Framework \(ATF\) tests using the Test Agent available in the Build Agent chat panel.
-   Use the Build Agent semantic search tool to find files, applications, and knowledge on your instance.
-   Validate your UI output in real-time using the Build Agent UI validation tool.
-   Use Build Agent to create agentic workflows, agents, and skills.

 [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US)

-   Build Agent is now available in ServiceNow Studio.
-   Leverage improved large language model \(LLM\) support with Build Agent.
-   With Build Agent, you can edit entire instances, not just individual apps.
-   Build Agent features extended metadata support, such as flows, Service Catalog workspaces, UI components, list controls, UI policies, and emails.
-   A new granular admin role enables users to use the mobile card generation skill.

 [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Generate themes and color palettes from brand images using the new theme generation workflow in Theme Builder.
-   Edit published or live catalog items directly through conversations with Now Assist.
-   Configure UI policies, location, access, fulfillment, and portal settings for catalog items with the catalog item generation skill.

 [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.
-   Expedite the troubleshooting process by using the ATF troubleshooting agent store application.
-   Learn about how to use UI Builder and modify UI pages with the UI Builder agent.
-   Plan your application development with the Build Agent planning tool.
-   Generate catalog items conversationally and preview them during the creation process with Now Assist in Catalog Builder.

 [Zurich Patch 3](https://www.servicenow.com/docs/access?context=zurich-patch-3&family=zurich&ft:locale=en-US)

-   Accelerate the transition from application design to development by connecting the Build Agent to the Figma Model Context Protocol server.

 [Zurich Patch 2](https://www.servicenow.com/docs/access?context=zurich-patch-2&family=zurich&ft:locale=en-US)

-   Try the Build Agent for free with the Build Agent \(Trial\).

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Create, edit, and deploy fully functional ServiceNow applications using the Build Agent in the ServiceNow IDE.
-   Enable security implementation to execute AI agents and agentic workflows through access control lists \(ACLs\) and user identities.

 See [ServiceNow Otto for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Creator. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)

-   Prepare for Now LLM Service to be deprecated in a future release.

 [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

-   Upload brand guidelines as a PDF in the theme creation workflow to generate themes that align with your brand.
-   Prepare for the app generation and test generation plugins to be deprecated in a future release.
-   Learn about Build Agent updates in the new [Build Agent release notes](https://www.servicenow.com/docs/access?context=build-agent-rn&family=australia&ft:locale=en-US).

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Generate readable documentation throughout the app development life cycle using the new release lifecycle documentation AI agent.
-   Generate themes and color palettes from brand images using the new theme generation workflow in Theme Builder.

 [Australia Early Availability](https://www.servicenow.com/docs/access?context=australia-all-other-fixes&family=australia&ft:locale=en-US)

-   Create and update applications in ServiceNow Studio using Build Agent.
-   Generate application modules in UI Builder workspaces using natural-language prompts.
-   Learn about agentic development using an AI-first approach in the new agentic development documentation.

 See [ServiceNow Otto for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

