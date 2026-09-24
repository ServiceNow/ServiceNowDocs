---
title: Exploring ServiceNow Otto for app summary generation
description: With the ServiceNow Otto for Creator application, you can generate a summary of an app. You can then copy the summary to the description for the app, and use it to check for duplicate apps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-exploring-now-assist-app-summarize.html
release: brazil
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [App summary generation, AI tools and files, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Exploring ServiceNow Otto for app summary generation

With the ServiceNow Otto for Creator application, you can generate a summary of an app. You can then copy the summary to the description for the app, and use it to check for duplicate apps.

## ServiceNow Otto for app summary generation overview

ServiceNow Otto for app summary generation generates a summary of what the app does, which you can copy to the app's description by selecting the **Use as app description** button.

Additionally, ServiceNow Otto for app summary generation has the following features, which are accessed via their icons on the App summary modal:

-   Rate the summary with a thumbs up or thumbs down icon.
-   Copy the summarized text to your clipboard with one click.
-   Regenerate the summary if you want it worded differently.

## ServiceNow Otto for app summary generation users

**Note:** In addition to the following personas, users must have the sn\_app\_summary.app\_summary\_user role to use ServiceNow Otto for app summary generation.

|User|Description|
|----|-----------|
|Delegated developer|Person who has been delegated to work on an app.|
|Admin|Person who can review and approve tasks related to custom application development.|

## ServiceNow Otto for app summary generation moves to an agentic architecture

App summary moves to an agentic architecture App summary now uses an AI agent to generate application summaries. This change moves app summary from a skill-based architecture to the AI agent orchestration model.

Previously, app summary depended on table summary and app summary skills. Administrators enabled these skills from the AI Skills admin console before users could generate application summaries.

With this release, users who install the App Summary plugin receive the App Summary AI agent. App summary no longer depends on dedicated skills to complete summary generation.

The App Summary AI agent is turned off by default after plugin installation to help avoid unexpected charges. An administrator must enable the agent in AI Agent Studio before end users can generate application summaries. For more information, see [Enable the App Summary AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/enable-the-app-summary-ai-agent.md).

The end-user experience remains the same. The change affects only the underlying architecture, which now uses an agentic model instead of the earlier skill-based model.

## ServiceNow Otto for app summary generation benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Quickly generate a description of an app, which you can use to check for duplicate apps.|[Summarize the contents of an app in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/summarize-an-app-in-servicenow-studio.md)|Developer, admin|

**Parent Topic:**[App summary generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/sns-now-assist-app-summarize-landing.md)

