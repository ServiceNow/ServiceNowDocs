---
title: Now Assist for Hardware Asset Management \(HAM\) release notes
description: The ServiceNow Now Assist for Hardware Asset Management \(HAM\) application brings agentic AI to Hardware Asset Management. Now Assist for Hardware Asset Management \(HAM\) is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-04"
reading_time_minutes: 4
---

# Now Assist for Hardware Asset Management \(HAM\) release notes

The ServiceNow® Now Assist for Hardware Asset Management \(HAM\) application brings agentic AI to Hardware Asset Management. Now Assist for Hardware Asset Management \(HAM\) is a new application in the Yokohama release.

## Now Assist for Hardware Asset Management \(HAM\) highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6 - Automate the hardware asset repair process by using an agentic workflow and configure Access Control Lists \(ACLs\) for both AI agents and agentic workflows.

Yokohama Patch 4 - Automate and streamline your hardware asset request process by using an agentic workflow.

See [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) for more information.

**Important:** Now Assist for Hardware Asset Management \(HAM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist for Hardware Asset Management \(HAM\) to Yokohama

Only users with the procurement\_user role can access the Help manage hardware asset requests agentic workflow including the following AI agents:

-   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent

## Now Assist for Hardware Asset Management \(HAM\) features

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   **[Optimize hardware asset repair process with the suite of AI agents](https://www.servicenow.com/docs/access?context=now-assist-ham-repair-agent-workflow&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Automate the repair of defective and out-of-warranty hardware assets by using AI agents in the Help repair hardware assets agentic workflow. These AI agents validate the repair tasks, provide detailed troubleshooting and repair instructions, and complete the tasks on receiving user confirmation.


-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the Access Control Lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


[Yokohama Patch 4](../quality/yokohama-patch-4.md)

-   **[Optimize hardware asset sourcing with the suite of AI agents](https://www.servicenow.com/docs/access?context=now-assist-ham-agentic-workflow&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Automate your hardware asset sourcing by using AI agents in the Help manage hardware asset requests agentic workflow. These AI agents can efficiently handle tasks such as automatically consuming assets from local stock, creating transfer orders, and generating purchase orders. By automating complex and repetitive tasks in the hardware asset request process, AI agents help to reduce manual intervention significantly, speed up request resolution, enhance the productivity of asset managers, and improve operational efficiency.


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

Install Now Assist for Hardware Asset Management \(HAM\) by requesting it from the ServiceNow Store.

**Note:**  To take full advantage of the Now Assist for HAM features, you should upgrade to Yokohama Patch 6 and install the Now Assist for Hardware Asset Management \(HAM\) store application.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

The Now Assist for Hardware Asset Management \(HAM\) application requires the Hardware Asset Management Pro plus license.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console for quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in ServiceNow® Service Operations Workspace to summarize a chat, an incident, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

