---
title: ServiceNow Otto for Retail Service Management \(RSM\) release notes
description: The ServiceNow ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.The ServiceNow ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.The ServiceNow ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.The ServiceNow ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-11-10"
reading_time_minutes: 3
---

# ServiceNow Otto for Retail Service Management \(RSM\) release notes

The ServiceNow® ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.

## About ServiceNow Otto for Retail Service Management \(RSM\)

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Enable retail store support agents to use the store inquiry Al agent to:
    -   Search multiple knowledge sources to generate clear, traceable responses and flag uncertain cases for human review.
    -   Improve with every resolved query and seamlessly fit into HQ workflows with tailored suggestions.

## Activation and other requirements

**Important:** ServiceNow Otto for RSM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    The ServiceNow Otto for RSM plugin is available with activation of com.sn.now.platform plugin. For more information, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

## January 2026

The ServiceNow® ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.

### What's changed

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## December 2025

The ServiceNow® ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.

### What's new

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

|AI agent capabilities|Description|
|---------------------|-----------|
|Automated inquiry parsing|Analyzes incoming questions from stores and identifies key topics like discount policy, returns, and exceptions. It accurately categorizes and tags these inquiries, streamlining the processing and response to store queries.|
|Intelligent policy look-up|Searches across multiple sources—such as past resolved cases, Knowledge Base articles, and their attached documents—to deliver precise and contextually relevant guidance.|
|Response drafting with policy references|Automatically generates a suggested reply using clear policy language and provides the accurate source of the suggested reply for traceability by attaching or linking the reply.|
|Learning from resolved cases|Continuously improves by indexing newly resolved inquiries, which expands its ability to respond to similar future cases.|
|Update case information|Enables users to accept, edit, or reject the suggested resolution, and automatically updates the case resolution notes and status for accepted or edited responses, or adds work notes for rejected responses.|

### Plugin information

-   **New plugins**

    The following plugins are new in Zurich:

    -   ServiceNow Otto for RSM \(com.sn\_rtl\_assist\_rsm\): Generative AI - related features for Retail Service Management that are powered by Now Assist.
    -   RSM AI agent collection \(com.sn\_rtl\_rsm\_agents\): The RSM AI agent collection is a Retail Service Management tool that uses generative AI to boost agent productivity and streamline issue resolution. It provides proactive recommendations, enabling faster, smarter, and more personalized customer support.

## Zurich

The ServiceNow® ServiceNow Otto for Retail Service Management \(RSM\) application supports retail personas in efficiently managing and resolving cases. ServiceNow Otto for RSM is a new application in the Zurich release.

### What's new

-   **[Store inquiry AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/retail-industry/agentic-workflows-now-assist-retail.md)**

    The store inquiry AI agent is an intelligent assistant designed to support retail store support agents in efficiently managing and resolving cases.

    New tools or scripts have been added to support store inquiry case management, including:

    -   Updating case details: Modifying the current information about a case, such as adding resolution information or updating work notes.
    -   Fetching similar cases: Retrieving past cases that have similar descriptions to the current case.
    -   Retrieving metadata for selectable links: Gathering information about a source \(like a case or document\) to create a selectable link to it.
    -   Get case details: Retrieving the current information about a case, such as its short description.

