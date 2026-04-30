---
title: Now Assist for Order Management release notes
description: The ServiceNow Now Assist for Order Management application brings platform AI capabilities to Sales Customer Relationship Management. Now Assist for Order Management is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-01-14"
reading_time_minutes: 4
---

# Now Assist for Order Management release notes

The ServiceNow® Now Assist for Order Management application brings platform AI capabilities to Sales Customer Relationship Management. Now Assist for Order Management is a new application in the Yokohama release.

## Now Assist for Order Management highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.

-   Enable business-to-business \(B2B\) customers to submit order cases autonomously from the Business Portal by simply describing their needs in natural language using the manage order operations agent.
-   Summarize complex orders across products, services, and fulfillment tasks, enabling agents to quickly understand status, take the right actions, and avoid navigating fragmented views to make next steps easier and improving productivity.

See [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

**Important:** Now Assist for Order Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Now Assist for Order Management features

-   **[Enable the manage order operations agent in the Business Portal](https://www.servicenow.com/docs/access?context=enable-manage-order-operations-ai-agent&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Activate the manage order operations agent so that you can make it available to your customers on the Business Portal.

-   **[Request order changes using Now Assist](https://www.servicenow.com/docs/access?context=request-order-changes-now-assist&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Use the manage order operations agent to provide a seamless experience to your customers on the Business Portal, enabling them to create order cases using a virtual assistant effortlessly. The AI agent can intelligently categorize requests for expedited delivery by creating order-related cases linked directly to the specific order, significantly reducing manual case creation and speeding up resolution times. Interaction channels include chat and voice options.

-   **[Summarize an order using Summarization for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-mgmt-summarize-order&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Generate a summary of a complex order for a unified view of the order's current state to:

    -   Respond confidently to customer queries with accurate, real-time order status.
    -   Track changes and validate details to maintain consistency and transparency.
    -   Minimize errors and improve communication across suppliers and partners.
    -   Monitor tasks that are at risk of missing deadlines.
    -   Assign tasks to appropriate resources based on priority and skill.
    -   Make rapid prioritization decisions to prevent delays and help ensure timely fulfilment.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Request the Now Assist for Order Management application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/b75a55a63f71b6108428dd8d001f8bca) and install it using the Application Manager. For more information, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in the CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

