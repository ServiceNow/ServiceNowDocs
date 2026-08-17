---
title: ServiceNow Otto for Sales Automation release notes
description: The ServiceNow ServiceNow Otto for Sales Automation application brings platform AI capabilities to Sales Customer Relationship Management. ServiceNow Otto for Sales Automation is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-02"
reading_time_minutes: 3
---

# ServiceNow Otto for Sales Automation release notes

The ServiceNow® ServiceNow Otto for Sales Automation application brings platform AI capabilities to Sales Customer Relationship Management. ServiceNow Otto for Sales Automation is a new application in the Yokohama release.

## ServiceNow Otto for Sales Automation highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   ServiceNow Otto for Sales Automation application packages ServiceNow® platform AI capabilities to deliver AI-powered insights and automation to drive faster, smarter sales and order processes.

See [ServiceNow Otto for Sales Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/now-assist-for-sales-and-order-management-som.md) for more information.

## ServiceNow Otto for Sales Automation features

-   **[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)[Use agentic workflows in ServiceNow Otto for Sales Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/using-agentic-worklflows-in-lead-management.md)**

    The Help nurture new leads agentic workflow works with a team of AI agents to assist the sales agents to manage the life cycle of leads, either independently or under supervision.

<table id="table_tbs_1xz_v2c"><thead><tr><th>

Workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Help nurture new leads

</td><td>

-   Outlines the steps required to engage the lead with the sales agent.
-   Sends initial outreach and follow-up emails.
-   Retrieves emails, classifies the intent, and routes it to the right sales agent to take action.
-   Schedules, reschedules, or deletes the appointments based on sales agent availability.
-   Manages the leads who want to opt out or uninterested.


</td><td>

-   Lead outreach AI agent
-   Inbound email AI agent
-   Appointment management AI agent
-   Lead disinterest AI agent


</td></tr></tbody>
</table>
## Changed in this release

-   **Changes to Now Assist usage measurement**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **Some Now Assist skills are turned on by default**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **Configure ACLs for AI agents and agentic workflows**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Now Assist features are available with activation of com.sn.now.platform plugin. For more information, see .

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   ****

    Use the AI Admin Hub console to provide you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   ****

    Use this conversational interface in the CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   ****

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/sales-order-management-rn-landing.md)

