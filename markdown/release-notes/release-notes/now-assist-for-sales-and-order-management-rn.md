---
title: Now Assist for Sales Force Automation \(SFA\) release notes
description: The ServiceNow Now Assist for Sales Force Automation \(SFA\) application brings platform AI capabilities to Sales Customer Relationship Management. Now Assist for SFA is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-02-11"
reading_time_minutes: 3
---

# Now Assist for Sales Force Automation \(SFA\) release notes

The ServiceNow® Now Assist for Sales Force Automation \(SFA\) application brings platform AI capabilities to Sales Customer Relationship Management. Now Assist for SFA is a new application in the Zurich release.

## Now Assist for SFA highlights for the Zurich release

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Now Assist for Sales and Order Management \(SOM\) is now known as Now Assist for Sales Force Automation \(SFA\) to align with our updated product taxonomy. There is no change to functionality or existing customer configurations.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 2](../quality/zurich-patch-2.md)

-   Enable sales agents to use the Help nurture new leads agentic workflow to:
    -   Proactively engage with initial leads
    -   Book an appointment/demo to qualify a lead
    -   Identify opt-outs and disinterest for lead disqualification

See [Now Assist for Sales Force Automation \(SFA\)](https://www.servicenow.com/docs/access?context=now-assist-for-sales-and-order-management-som&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

**Important:** Now Assist for SFA is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Use agentic workflows in Now Assist for Sales Force Automation \(SFA\)](https://www.servicenow.com/docs/access?context=using-agentic-worklflows-in-lead-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    The Help nurture new leads agentic workflow works with a team of AI agents to assist the sales agents to manage the life cycle of leads, either independently or under supervision.

<table id="table_s5m_lpg_jgc"><thead><tr><th>

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

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Now Assist features are available with activation of com.sn.now.platform plugin. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Plugin information

[Zurich Patch 2](../quality/zurich-patch-2.md)

-   **New plugins**

    The following plugin is new in Zurich:

    Now Assist for SFA \(sn\_som\_gen\_ai\): Packages AI capabilities for Sales Force Automation features in Sales CRM.


## Additional requirements

The Now Assist for SFA application requires the Sales Development AI agents.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in the CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

