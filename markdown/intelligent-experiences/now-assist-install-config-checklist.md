---
title: Solving installation and configuration issues with Now Assist
description: Use this checklist to address issues or gaps in your Now Assist configuration.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
keywords: [installing Now Assist, AI features, AI products, updating Now Assist, solutions, Now Assist, GenAI, generative AI, configure Now Assist]
breadcrumb: [ServiceNow AI implementation, Enable AI experiences]
---

# Solving installation and configuration issues with Now Assist

Use this checklist to address issues or gaps in your Now Assist configuration.

<table id="table_xxd_g5n_5fc"><thead><tr><th class="filter">

Feature

</th><th>

Issue

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

AI agents

</td><td>

I can't find agent spokes

</td><td>

Install the Now Assist for Spokes application from the ServiceNow Store. For details, see [Now Assist for Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/now-assist-spokes.md).

</td></tr><tr><td>

AI Control Tower

</td><td>

No data on the Evaluations tab

</td><td>

Verify that the Conversation Evaluator \[sn\_na\_conv\_eval\] plugin is active. Also verify that the Smooth Flowing Conversation Chat Eval skill is active in the Now Assist Admin console. \(This skill may appear in the Platform workflow or in the Other workflow, depending on your instance.\)

</td></tr><tr><td>

AI Search

</td><td>

External content isn't included in search results

</td><td>

You can use External Content Connectors to include other sources in your search results. For details, see [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/ext-cont-connectors-landing-page.md).

</td></tr><tr><td>

AI Search

</td><td>

Now Assist in AI Search Genius results don't appear

</td><td>

1.  Verify that AI Search and Now Assist in AI Search are installed and configured.
2.  To use Now Assist Q&amp;A Genius Results in AI Search applications, link the Now Assist Q&amp;A Genius Result configuration to your search profiles for those applications. For details, see [Link a Genius Result configuration to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/link-gr-search-profile-ais.md).
3.  Verify that all Now Assist plugins are up to date.
4.  Try repairing the plugins.

</td></tr><tr><td>

Knowledge articles

</td><td>

I can't generate a knowledge article

</td><td>

1.  Verify that Now Assist in Knowledge Management is installed and configured.
2.  Verify that all Now Assist plugins are up to date.
3.  Verify that the knowledge generation skill is activated. For details, see [Activate a Now Assist skill](../task/configure-a-now-assist-skill.md).
4.  Try repairing the plugins.

</td></tr><tr><td>

Knowledge articles

</td><td>

The KB generation popup doesn't appear in Core UI

</td><td>

Now Assist in Knowledge Management formatters may be missing from the form layout, possibly due to form customizations. For details, see [KB1710178](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1710178).

</td></tr><tr><td>

Now Assist applications

</td><td>

I want to view my subscriptions

</td><td>

See [Product subscriptions overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/subscriptions-overview-v2.md).

</td></tr><tr><td>

Now Assist panel

</td><td>

Can't access skills in the Now Assist panel

</td><td>

-   Verify that the skill is configured to display in the Now Assist panel. For details, see [Edit a Now Assist skill](../task/edit-a-now-assist-skill.md).
-   If you are using Now Assist in Virtual Agent, verify that search sources were configured for the Now Assist panel. You can specify search sources for a Now Assist panel assistant when you set it up. Search sources are essential for the Now Assist panel and Virtual Agent. Without them, they cannot discover or rank skills and agentic workflows. For details, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md) and [Assign search sources to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/add-info-sources-assistant.md).

If Now Assist in Virtual Agent is not installed, the Now Assist panel uses default search sources.


</td></tr><tr><td>

Now Assist panel

</td><td>

Some users don't get a response to a question

</td><td>

Many Now Assist skills require specific user roles. Verify that there are active skills with the user's role. For details, see [Activate a Now Assist skill](../task/configure-a-now-assist-skill.md).

</td></tr><tr><td>

Now Assist panel

</td><td>

I don't want skills to be available in Now Assist panel

</td><td>

Disable the Now Assist panel when you configure the skill. For details, see [Edit a Now Assist skill](../task/edit-a-now-assist-skill.md).

</td></tr><tr><td>

Now Assist panel

</td><td>

Options for Now Assist panel are grayed out in the Now Assist Admin console

</td><td>

The sn\_nowassist\_admin.user role provides read-only access only. To make configuration changes, the user must have the sn\_nowassist\_admin.nsa\_admin role.

</td></tr><tr><td>

Now Assist setup

</td><td>

Errors after clone

</td><td>

Try repairing affected plugins. For details, see [Repair a ServiceNow application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/repair-app.md).

</td></tr><tr><td>

Now Assist setup

</td><td>

The Q&amp;A results skill is not in the Now Assist Admin console

</td><td>

Set up AI Search. For details, see [Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-ais.md).

</td></tr><tr><td>

Now Assist setup

</td><td>

Features/skills are missing or generally not working

</td><td>

-   Verify that all of your Now Assist plugins are up to date. For details, see [Install an update to a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_InstallUpdates.md).
-   Verify that version and dependency requirements are met. For details, see [Evaluating version requirements and dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/versions-dependencies.md).
-   For skills, verify that they are active in the Now Assist Admin console. For details, see [Activate a Now Assist skill](../task/configure-a-now-assist-skill.md).
-   Verify that the user has the correct role for the skill.
-   Try clearing the cookies and cache in the web browser.
-   Try repairing Generative AI Controller. For details, see [Repair a ServiceNow application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/repair-app.md).

</td></tr><tr><td>

Now Assist setup

</td><td>

Can't edit a skill

</td><td>

Verify that you have the Now Assist Admin role: sn\_nowassist\_admin.nsa\_admin.

 You can edit a skill or make a copy of a skill to edit. For details, see [Edit a Now Assist skill](../task/edit-a-now-assist-skill.md) and [Make a copy of a Now Assist skill](../task/make-a-copy-of-a-now-assist-skill.md).

</td></tr><tr><td>

Now Assist setup

</td><td>

Missing entries, fields, and errors

</td><td>

-   Verify that all of your Now Assist plugins are up to date. For details, see [Install an update to a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_InstallUpdates.md).
-   Try repairing the application. For details, see [Repair a ServiceNow application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/repair-app.md).
-   Try repairing Generative AI Controller. For details, see [Repair a ServiceNow application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/repair-app.md).

</td></tr><tr><td>

Now Assist setup

</td><td>

Problems upgrading Now Assist applications

</td><td>

-   Verify that you have a license for the application.
-   If the application was not previously installed, request it from the [ServiceNow Store](https://store.servicenow.com/store) \(Opt In\).
-   If the application was previously installed, you may need to procure it from the [ServiceNow Store](https://store.servicenow.com/store) again. For details, see [Updating applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/updating-apps-app-manager.md).

</td></tr><tr><td>

Now Assist setup

</td><td>

Skills not working in Legacy Agent Workspace

</td><td>

Now Assist skills are not available in Legacy Workspace. Upgrade to Service Operations Workspace to use Now Assist.

</td></tr><tr><td>

Now Assist for Code

</td><td>

Don't see code suggestions

</td><td>

-   Verify that the skill is active. For details, see [Activate a Now Assist skill](../task/configure-a-now-assist-skill.md).
-   Verify that the user has the appropriate role. Any authenticated builder can use the related active skill.
-   Verify that autocomplete is enabled. For details, see [Generate code with autocomplete](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/generate-code-with-autocomplete.md).

</td></tr><tr><td>

Now Assist for Creator

</td><td>

Skills not available or not working

</td><td>

-   Verify that the skill is active in the Now Assist Admin console.
-   Verify that the user has the appropriate role. Any authenticated builder can use the related active skill.

</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

Now Assist Skill Kit is not visible on my instance

</td><td>

-   Verify that you have at least one Now Assist product installed. For details, see [Install Now Assist plugins](../task/install-now-assist-feature-plugins.md).
-   Verify that the sn\_skill\_builder.admin role is assigned to the user.

</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

Skills are read-only

</td><td>

Verify that the sn\_skill\_builder.admin role is assigned to the user.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

Topic not returning as expected

</td><td>

-   Verify that the Virtual Agent topic is in the Active state and is published. For details, see [Publish a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/publish-virtual-agent-topic.md).
-   Verify that the topics are using LLM topic discovery. NLU/keyword topics cannot be used in a portal that is using Now Assist in Virtual Agent. You can migrate NLU/keyword topics to LLM, however. For details, see [Migrating NLU/keyword Virtual Agent topics to LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/llm-topic-migration.md).

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

Can't add topics to the portal

</td><td>

Verify that the topics are using LLM topic discovery. NLU/keyword topics cannot be added to a portal that is using Now Assist in Virtual Agent. You can migrate these topics to LLM, however. For details, see [Migrating NLU/keyword Virtual Agent topics to LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/llm-topic-migration.md).

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

Configuration issues

</td><td>

1.  Verify that the plugin is up to date. For details, see [Install an update to a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_InstallUpdates.md).
2.  Follow the guided setup to install and configure it. For details, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md).

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

Unable to choose fallback options in setup

</td><td>

If you're using a custom fallback topic, this option may be unavailable in guided setup. For details, see [KB1760362: Now Assist Chat Setup Not Allowing to Set Fallback Option](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1760362). You may need to log in to view the article.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

Chat is not showing search results

</td><td>

-   Verify that all of your Now Assist plugins are up to date. For details, see [Install an update to a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_InstallUpdates.md).
-   Verify that AI Search and Now Assist in AI Search are set up and configured. For details, see [Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-ais.md) and [Install Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/install-now-assist-ais.md).
-   Verify that search sources were configured for the Virtual Agent assistant. You can specify search sources for an assistant when you set it up. Search sources are essential for Virtual Agent and the Now Assist panel. Without them, they cannot discover or rank skills and agentic workflows. For details, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md) and [Assign search sources to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/add-info-sources-assistant.md).

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

Error when attempting to migrate Virtual Agent NLU conversations to LLM

</td><td>

Verify that you have the correct role, either virtual\_agent\_admin or sn\_vad\_genai.topic\_migration\_admin. For more information, see [Migrate NLU topics to LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/migrate-nlu-llm.md).

</td></tr></tbody>
</table>