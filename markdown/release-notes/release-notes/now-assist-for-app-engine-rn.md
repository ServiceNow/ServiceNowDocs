---
title: ServiceNow Otto for App Engine release notes
description: The ServiceNow ServiceNow Otto for App Engine application enables creators to enhance custom applications with AI agents and skills that application users can leverage at runtime. ServiceNow Otto for App Engine is a new application in the Yokohama Patch 3 release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-06-04"
reading_time_minutes: 3
---

# ServiceNow Otto for App Engine release notes

The ServiceNow® ServiceNow Otto for App Engine application enables creators to enhance custom applications with AI agents and skills that application users can leverage at runtime. ServiceNow Otto for App Engine is a new application in the Yokohama Patch 3 release.

## ServiceNow Otto for App Engine highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   Create and deploy AI agents within custom applications, helping to empower creators and accelerate time-to-value.
-   Build custom AI agents and skills for the unique workflow of an application using AI Skill Kit and AI Agent Studio.
-   Leverage AI agents and skills created with ServiceNow Otto for App Engine in custom applications at runtime, helping improve efficiency.

See  for more information.

**Important:** ServiceNow Otto for App Engine is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## ServiceNow Otto for App Engine features

-   ****

    Create a custom AI agent in AI Agent Studio to assist your application users with their tasks.

-   ****

    Create a custom skill for Now Assist, enabling you to have greater flexibility with the generative AI capabilities available on the ServiceNow AI Platform.


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

Install ServiceNow Otto for App Engine by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Additional requirements

Check your entitlements to determine whether you have access to the ServiceNow Otto for App Engine application.

## Related ServiceNow applications and features

-   ****

    With the ServiceNow®AI Agent Studio application, you can create, manage, or test AI agents and agentic workflows all in one place.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    ServiceNow® Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   ****

    The AI Admin Hub console provides you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   ****

    The ServiceNow® Now Assist AI agents are entities that mimic human-like intelligence by using large language models \(LLMs\).

-   ****

    ServiceNow® AI Skill Kit enables you to create and publish custom prompts and skills for Now Assist.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/build-automate-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

