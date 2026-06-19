---
title: Install Build Agent
description: For the Paid version of Build Agent, install the Now Assist for Creator application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/building-applications/install-build-agent.html
release: zurich
product: Building Applications
classification: building-applications
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Install Build Agent

For the Paid version of Build Agent, install the Now Assist for Creator application from the ServiceNow Store.

## Before you begin

The Paid version of Build Agent is part of Now Assist for Creator, and is a ServiceNow AI Platform® feature that's activated by default when Now Assist for Creator is installed. You don't need an entitlement to start exploring Build Agent.

-   Review the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   You can use Build Agent on a Personal Development Instance \(PDI\). For more information, see [Accessing Build Agent in ServiceNow Studio and the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/access-build-agent.md).
-   Build Agent supports the following models:
    -   Gemini 2.5 Pro
    -   Azure OpenAI 5.4
    -   Opus 4.6

Role required: admin

## About this task

Build Agent is enabled by default to create apps with AI, for example in ServiceNow Studio. To use other Now Assist products, such as the app generation skill, disable Build Agent. For example, using the setting in your ServiceNow Studio preferences.

**Note:** The trial app was formerly called "Build Agent" and has been renamed to "Build Agent \(Trial\)."

## Procedure

1.  From the Now Assist for Creator application page on the ServiceNow Store, select **Buy**.

2.  After approval has been granted, on your instance, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Using the search bar, search for the Now Assist for Creator application \(sn\_now\_creator\).

4.  Select **Install**.

5.  Enable the Build Agent skill:

    1.  Navigate to **Admin** &gt; **Now Assist Admin**.

    2.  Go to the **Now Assist Skills** tab and select **Creator**.

        \[Omitted image "build-agent-enable.png"\] Alt text: Build Agent is listed as Now Assist for Creator skills.

    3.  Select **Turn on** to enable the skill.

    The skill is enabled for all users.


**Parent Topic:**[Configure Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/configure-build-agent.md)

