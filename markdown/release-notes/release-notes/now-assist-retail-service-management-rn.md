---
title: ServiceNow Otto for Retail Service Management \(RSM\) release notes
description: The ServiceNow ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-10"
reading_time_minutes: 3
---

# ServiceNow Otto for Retail Service Management \(RSM\) release notes

The ServiceNow® ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.

## ServiceNow Otto for RSM highlights for the Zurich release

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Enable retail store support agents to use the store inquiry Al agent to:
    -   Search multiple knowledge sources to generate clear, traceable responses and flag uncertain cases for human review.
    -   Improve with every resolved query and seamlessly fit into HQ workflows with tailored suggestions.

**Important:** ServiceNow Otto for RSM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## ServiceNow Otto for RSM features

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

|AI agent capabilities|Description|
|---------------------|-----------|
|Automated inquiry parsing|Analyzes incoming questions from stores and identifies key topics like discount policy, returns, and exceptions. It accurately categorizes and tags these inquiries, streamlining the processing and response to store queries.|
|Intelligent policy look-up|Searches across multiple sources—such as past resolved cases, Knowledge Base articles, and their attached documents—to deliver precise and contextually relevant guidance.|
|Response drafting with policy references|Automatically generates a suggested reply using clear policy language and provides the accurate source of the suggested reply for traceability by attaching or linking the reply.|
|Learning from resolved cases|Continuously improves by indexing newly resolved inquiries, which expands its ability to respond to similar future cases.|
|Update case information|Enables users to accept, edit, or reject the suggested resolution, and automatically updates the case resolution notes and status for accepted or edited responses, or adds work notes for rejected responses.|

## New in the Zurich release

-   **[Store inquiry AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/retail-industry/agentic-workflows-now-assist-retail.md)**

    The store inquiry AI agent is an intelligent assistant designed to support retail store support agents in efficiently managing and resolving cases.

    New tools or scripts have been added to support store inquiry case management, including:

    -   Updating case details: Modifying the current information about a case, such as adding resolution information or updating work notes.
    -   Fetching similar cases: Retrieving past cases that have similar descriptions to the current case.
    -   Retrieving metadata for selectable links: Gathering information about a source \(like a case or document\) to create a selectable link to it.
    -   Get case details: Retrieving the current information about a case, such as its short description.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

The ServiceNow Otto for RSM plugin is available with activation of com.sn.now.platform plugin. For more information, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

## Plugin information

-   **New plugins**

    The following plugins are new in Zurich:

    -   ServiceNow Otto for RSM \(com.sn\_rtl\_assist\_rsm\): Generative AI - related features for Retail Service Management that are powered by Now Assist.
    -   RSM AI agent collection \(com.sn\_rtl\_rsm\_agents\): The RSM AI agent collection is a Retail Service Management tool that uses generative AI to boost agent productivity and streamline issue resolution. It provides proactive recommendations, enabling faster, smarter, and more personalized customer support.

## Related ServiceNow applications and features

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the AI Admin Hub console to provide you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use this conversational interface in the CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

**Parent Topic:**[Retail applications release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/retail-rn.md)

