---
title: Now Assist for Workplace Service Delivery \(WSD\) release notes
description: The ServiceNow Now Assist for Workplace Service Delivery \(WSD\) application enables agents to summarize case information, generate resolution notes, and summarize the chat information for an interaction. Your agents can understand the chat and case context and propose quicker resolutions to your customers. Now Assist for WSD was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-16"
reading_time_minutes: 4
---

# Now Assist for Workplace Service Delivery \(WSD\) release notes

The ServiceNow® Now Assist for Workplace Service Delivery \(WSD\) application enables agents to summarize case information, generate resolution notes, and summarize the chat information for an interaction. Your agents can understand the chat and case context and propose quicker resolutions to your customers. Now Assist for WSD was enhanced and updated in the Yokohama release.

## Now Assist for Workplace Service Delivery \(WSD\) highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Help map admins configure the map during bulk updates to Indoor Mapping using the Automate map updates AI agentic workflow.
-   Optimize a maintenance case based on the space utilization rate of the location where a maintenance case is created using the Optimize cleaning activities AI agentic workflow.

Yokohama Patch 3

-   Manage temporary space closures AI agentic workflow for emergency meeting room maintenance. This team of AI agents block a space for maintenance and move any existing reservations from the blocked room to a new location.
-   Help manage workplace reservations for updating existing event planning reservations. This team of AI agents retrieve the reservation from workplace case details, analyze the reservation, and update the workplace case notes.

See [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist for WSD is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Optimize cleaning activities agentic workflow](https://www.servicenow.com/docs/access?context=optimize-cleaning-activities-agent&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use the Optimize cleaning activities agentic workflow to manage cleaning and maintenance schedules of a maintenance case based on the space utilization rate of the location where a maintenance case is created.

-   **[Automate map updates agentic workflow](https://www.servicenow.com/docs/access?context=automate-map-updates-agent-ai&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use the Automate map updates AI agentic workflow to configure the map during bulk updates to Indoor Mapping.

    The Map Admin Agent autonomously retrieves the sources for the CAD file and resumes the import task. If the correct source isn't found, the agent moves the task to the Waiting user input state.


-   **[Manage temporary space closures agentic workflow](https://www.servicenow.com/docs/access?context=manage-temp-space-closure-agent-ai&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use the Manage temporary space closures agentic workflow when an emergency maintenance request is created.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Manage temporary space closures|AI agentic workflow blocks a room for emergency maintenance and moves any existing reservation from the blocked location to another.|

-   **[Help manage workplace reservations agentic workflow](https://www.servicenow.com/docs/access?context=manage-workplace-reservations-agent-ai&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use the Help manage workplace reservations agentic workflow for updating a planned event reservation's time, date, or duration.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Help manage workplace reservations|AI agentic workflow autonomously reschedules events happening in the workplace and update an existing reservations date, time, or duration.|


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

Install Now Assist for Workplace Service Delivery \(WSD\) by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.


**Parent Topic:**[Now Assist for Workplace Service Delivery \(WSD\) Release Notes](wsd-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

