---
title: AI-assisted app creation with Now Assist for Creator
description: Now Assist for Creator provides core skills for rapid conversational app development. Use the integrated tools to generate scripts, optimize code, scaffold applications, and automate testing through natural language prompts.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Develop, Vibe coding and AI-assisted development, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# AI-assisted app creation with Now Assist for Creator

Now Assist for Creator provides core skills for rapid conversational app development. Use the integrated tools to generate scripts, optimize code, scaffold applications, and automate testing through natural language prompts.

**Note:** While Now Assist for Creator is not a vibe coding product suite, you can use its AI capabilities to quickly enhance app development.

Now Assist for Creator is the ServiceNow collection of generative AI skills for building apps on the ServiceNow AI Platform. Use it to generate apps, flows, code, tests, UIs, analytics, catalog items, RPA bots, and more from natural language prompts directly in offerings like ServiceNow Studio.

Some skills in Now Assist for Creator have a conversational interface and can be used for vibe coding and AI-assisted development. For example, the catalog item generation skill in Catalog Builder. For more information, see [Now Assist in Catalog Builder](https://www.servicenow.com/docs/access?context=now-assist-for-catalog-generation&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Core capabilities

For complete information on using Now Assist for Creator, see [Now Assist for Creator](../../../administer/flow-designer/concept/now-assist-for-creator-landing.md).

The following metadata-driven tools are available for using AI to develop apps:

-   Conversational development: Use Build Agent, which is part of Now Assist for Creator, to create apps and metadata through a conversational interface.
-   Application generation and scaffolding: Create tables, experiences, roles, and initial data model from a prompt.
-   Flow generation, recommendations, and summarization: Generate multi-step flows, get next step suggestions, and auto-summarize what a flow does.
-   Code generation: Prompt-based server-side and client-side scripts with AI suggestions for script includes, business rules, and GlideRecord queries.
-   Catalog item generation: Produce Service Catalog items from text directions.
-   UI generation: Build experiences by describing the desired interface.
-   Data visualization generation \(Platform Analytics\): Conversational chart and indicator creation.
-   Playbook generation: Outline automated processes from natural language.
-   RPA bot generation: Create desktop automations from text prompts inside RPA Desktop Design Studio.
-   App, table, and flow summaries: Generate explainers and summaries to support onboarding and application understanding.

## Where to start

1.  Welcome guide and skills and prompting: See the Community Welcome Guide and Skill Prompt Guides for Creator. For more information, see the following resources:
    -   [Community Welcome Guide on Community](https://www.servicenow.com/community/app-engine-articles/now-assist-for-creator-welcome-guide/ta-p/2851287)
    -   [Skill Prompt Guides on Community](https://www.servicenow.com/community/now-assist-for-creator/ct-p/creator-now-assist)
2.  Store app and release notes: Install/upgrade Now Assist for Creator skills from the ServiceNow Store.
3.  Onboarding topic in this document: See [Onboarding for vibe coding and AI-assisted development](vibe-coding-onboarding.md).

## Now Assist for Creator and AI-assisted development on the ServiceNow AI Platform

Now Assist for Creator is the ServiceNow AI Platform toolkit for using AI to generate and refine apps. Instead of switching between generic IDEs and separate agents, Now Assist for Creator provides embedded skills aligned to platform constructs \(such as tables, ACLs, flows, and catalog items\). You can describe a solution through conversation, then inspect and test it with platform tools \(such as ATF, ACLs, and the Metadata Explorer\).

## General Now Assist for Creator workflow

1.  Enable the skills: Configure the triggers, settings, and display locations for Now Assist for Creator skills to enable generative AI capabilities across the ServiceNow AI Platform. For more information, see [Activate a Now Assist skill](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
2.  Describe the app: For example, you can request to “Create a cross-training app with instructor signup, session scheduling, approvals.” Then the application generation scaffolds tables, roles, and experiences.
3.  Add process logic: Use flow generation for approvals and escalations and Flow recommendations to suggest next steps.
4.  Add custom code logic: Prompt code generation for business rule and script include logic \(such as GlideRecord queries\), and then review and refactor as needed.
5.  Expose services: Catalog item generation creates request items for sessions/resources.
6.  Automate outside the platform: RPA bot generation to fetch instructors’ availability from a desktop calendar or copy rosters.
7.  Explain and test: Use app, flow, and table summarization to document; generate tests with the test-generation skill; run ATF.

**Parent Topic:**[Vibe coding and AI-assisted development on the ServiceNow AI Platform](vibe-coding-using.md)

