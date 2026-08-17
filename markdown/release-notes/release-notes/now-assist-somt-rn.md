---
title: ServiceNow Otto for Sales Customer Relationship Management for Telecommunications release notes
description: The ServiceNow Now Assist for Sales CRM for Telecommunications application enriches purpose-built industry workflows with generative AI to supercharge insights, actions, and self-service experiences. ServiceNow Otto for Sales Customer Relationship Management for Telecommunications is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-24"
reading_time_minutes: 5
---

# ServiceNow Otto for Sales Customer Relationship Management for Telecommunications release notes

The ServiceNow® Now Assist for Sales CRM for Telecommunications application enriches purpose-built industry workflows with generative AI to supercharge insights, actions, and self-service experiences. ServiceNow Otto for Sales Customer Relationship Management for Telecommunications is a new application in the Zurich release.

## ServiceNow Otto for Sales Customer Relationship Management for Telecommunications highlights for the Zurich release

-   Use the task template generation agent to create a task plan template for the given specification based on the uploaded image file.

-   Now Assist for Sales and Order Management for Telecommunications is now known as ServiceNow Otto for Sales Customer Relationship Management for Telecommunications to align with the updated product taxonomy. There is no change to functionality or existing customer configurations.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Sales and Order Management for Telecommunications \(SOMT\) is now known as Sales Customer Relationship Management for Telecommunication \(Sales CRM for Telecommunications\) to align with the updated product taxonomy. There is no change to functionality or existing customer configurations.
-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Collects the customer order information, identifies if the order needs enrichment, and creates the enrichment tasks. On closure of the enrichment task, it invokes the order fulfillment agent.
-   Uses the historic order tasks to create the order tasks. If the historic data doesn't return any results, the large language model \(LLM\) is used to get the response.
-   Checks the automation flow and fulfill order tasks.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.

-   Automatically create the fallout records based on reported issues in the order task work notes.
-   Provide customers with the option to configure product workflows using the data-driven catalog subflow as an alternative to Flow Designer, giving more options for implementing product configurations.
-   Automate the customer move order capture journey to reduce the manual effort.

See [ServiceNow Otto for Sales Customer Relationship Management for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/somt-now-assist.md) for more information.

**Important:** ServiceNow Otto for Sales CRM for Telecommunications is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## ServiceNow Otto for Sales Customer Relationship Management for Telecommunications features

-   **[Image to task plan template AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-task-template-generation-somt.md)**

    Use this agent to process an uploaded image file, extract task dependencies and store them as a task plan template for the given specification.

-   **[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)[Order enrichment agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/order-enrichment-agent-somt.md)**

    Use the order enrichment AI agent to collect the customer order information, identify if the order needs enrichment, and create the enrichment tasks. The AI agent creates a task and triggers the order fulfillment AI agent on its completion.

-   **[Order fulfillment agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/order-fulfillment-agent-somt.md)**

    Use the order fulfillment agent to identify the tasks for domain orders using historical data from similar orders. After decomposition, the fulfillment AI agent creates and fulfills order tasks by checking the historical and applicable tasks.

-   **[Task plan templates driven order fulfillment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/somt-flow-action-catalog-task.md)**

    Define tasks and their dependencies using the task plan template to orchestrate the fulfillment journey for a product to standardize fulfillment processes across products.

-   **[Move order voice AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-move-order-somt.md)**

    Use this agent to help you create a move order capture journey by collecting details such as the customer’s name, current service location, product offering, and new service address.

-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Now Assist features are available with activation of the ServiceNow Otto for TMT plugin. For more information, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

## Plugin information

The ServiceNow Otto for Sales Customer Relationship Management for Telecommunications application requires the ServiceNow Otto for TMT plugin. For more information about plugin activation, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

## Related ServiceNow applications and features

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    The AI Admin Hub console provides you with quick and effortless access to the important information that you must set up, configure, and monitor Now Assist applications and features.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use this conversational interface in the CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/technology-industry-rn-landing.md)

