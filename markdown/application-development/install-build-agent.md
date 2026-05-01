---
title: Install Build Agent
description: Install the Build Agent application from the ServiceNow Store to get the Now Assist for Build Agent.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Configure, Build Agent, AI in custom applications, Developing your application, Building applications]
---

# Install Build Agent

Install the Build Agent application from the ServiceNow Store to get the Now Assist for Build Agent.

## Before you begin

-   Review the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Build Agent supports Anthropic Claude on AWS, Azure OpenAI, and Google Gemini.

Role required: admin

## Procedure

1.  From the Now Assist for Creator application page on the ServiceNow Store, select **Buy**.

2.  After approval has been granted, on your instance, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Using the search bar, search for the Now Assist for Creator application \(sn\_now\_creator\).

4.  Select **Install**.

5.  Enable the Build Agent skill:

    1.  Navigate to **Admin** &gt; **Now Assist Admin**.

    2.  Go to the **Now Assist Skills** tab and select **Creator**.

        ![Build Agent is listed as Now Assist for Creator skills.](../image/build-agent-enable.png)

    3.  Select **Turn on** to enable the skill.

    The skill is enabled for all users.


**Parent Topic:**[Configure Build Agent](configure-build-agent.md)

**Related topics**  


[Install Now Assist for Creator](https://www.servicenow.com/docs/access?context=install-now-assist-for-creator&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

