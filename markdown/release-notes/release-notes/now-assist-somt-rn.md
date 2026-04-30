---
title: Now Assist for Sales CRM for Telecommunications release notes
description: The ServiceNow Now Assist for Sales and Order Management for Telecommunications application enriches purpose-built industry workflows with generative AI to supercharge insights, actions, and self-service experiences. Now Assist for SOMT is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-24"
reading_time_minutes: 4
---

# Now Assist for Sales CRM for Telecommunications release notes

The ServiceNow® Now Assist for Sales and Order Management for Telecommunications application enriches purpose-built industry workflows with generative AI to supercharge insights, actions, and self-service experiences. Now Assist for SOMT is a new application in the Zurich release.

## Now Assist for SOMT highlights for the Zurich release

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Collects the customer order information, identifies if the order needs enrichment, and creates the enrichment tasks. On closure of the enrichment task, it invokes the order fulfillment agent.
-   Uses the historic order tasks to create the order tasks. If the historic data doesn't return any results, the large language model \(LLM\) is used to get the response.
-   Checks the automation flow and fulfill order tasks.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

See [Now Assist for Sales CRM for Telecommunications](https://www.servicenow.com/docs/access?context=somt-now-assist&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US) for more information.

**Important:** Now Assist for SOMT is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Now Assist for SOMT features

-   **[Order enrichment agent](https://www.servicenow.com/docs/access?context=order-enrichment-agent-somt&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

    Use the order enrichment AI agent to collect the customer order information, identify if the order needs enrichment, and create the enrichment tasks. The AI agent creates a task and triggers the order fulfillment AI agent on its completion.

-   **[Order fulfillment agent](https://www.servicenow.com/docs/access?context=order-fulfillment-agent-somt&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

    Use the order fulfillment agent to identify the tasks for domain orders using historical data from similar orders. After decomposition, the fulfillment AI agent creates and fulfills order tasks by checking the historical and applicable tasks.

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Now Assist features are available with activation of the Now Assist for TMT plugin. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The Now Assist Admin console provides you with quick and effortless access to the important information that you must set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in the CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)

