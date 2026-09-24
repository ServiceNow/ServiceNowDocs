---
title: Install Autonomous Engineer
description: Install Autonomous Engineer from the ServiceNow Store to make it available on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/install-autonomous-engineer.html
release: brazil
topic_type: task
last_updated: "2026-09-14"
reading_time_minutes: 1
keywords: [Autonomous Engineer, install, setup, ServiceNow Studio, Build Agent, agent packs]
audience: programmer
breadcrumb: [Configure, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Install Autonomous Engineer

Install Autonomous Engineer from the ServiceNow Store to make it available on your instance.

## Before you begin

Autonomous Engineer is a separate application available in the ServiceNow Store. Installing Autonomous Engineer also installs Build Agent as a dependency. Installing Build Agent alone does not install Autonomous Engineer.

-   Check your entitlements to confirm your access to Autonomous Engineer before installing.
-   Review the Autonomous Engineer application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   You can use Autonomous Engineer on a Personal Development Instance \(PDI\) or in Developer Sandboxes. For more information, see [Accessing Build Agent in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/access-build-agent.md).

Role required: admin

## About this task

For instructions on installing ServiceNow products from the ServiceNow Store, see [Install an application or plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/installing-applications-in-application-manager.md).

## Procedure

1.  From the Autonomous Engineer application page on the ServiceNow Store, select **Buy**.

2.  After approval has been granted, on your instance, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Using the search bar, search for the Autonomous Engineer application.

4.  Select **Install**.

    Autonomous Engineer and Build Agent are installed on your instance.

5.  Enable the Autonomous Engineer skill:

    1.  Navigate to **All** &gt; **AI Admin Hub****Skills**.

    2.  Select the **Creator** tab.

    3.  Locate Autonomous Engineer in the skills list and select **Turn on**.

    The skill is enabled for all users.


## What to do next

After installing Autonomous Engineer, install the agent pack for the product domain you plan to implement. For more information, see [Agent packs for Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown).

**Parent Topic:**[Configure Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/configure-autonomous-engineer.md)

