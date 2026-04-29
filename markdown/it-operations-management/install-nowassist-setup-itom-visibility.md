---
title: Install ITOM Visibility using Now Assist for Setup
description: Install all required ITOM Visibility applications and plugins from the IT Operations Management Product Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Now Assist for Setup \(ITOM Visibility\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Install ITOM Visibility using Now Assist for Setup

Install all required ITOM Visibility applications and plugins from the IT Operations Management Product Hub.

## Before you begin

Verify that you have the following configuration:

-   Platform version Zurich patch 4
-   Now Assist For Platform. App ID: sn\_genai\_platform
-   Generative AI Controller. App ID: sn\_generative\_ai
-   Now Assist Skill Kit. App ID: sn\_skill\_builder
-   Now Assist for ITOM. For more information, see [Install the Now Assist for IT Operations Management \(ITOM\) plugin](../../now-assist-itom/task/install-now-assist-itom.md)
-   Activated Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
-   Activated assistants:

    -   Now Assist - Platform assistant
    -   Now Assist in Virtual Agent
    For more information, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)

-   Activated Now LLM Service as a provider. For more information, see [Manage AI models](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
-   Set Up AI Search. For more information, see [AI Search readiness for Now Assist on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=sn-ai-impl-ai-search&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
-   Verify that the following Implementation Agents were automatically installed upon upgrading to Zurich patch 4:
    -   IA Common
    -   IA Content
    -   Now Assist For Implementation Agent
    -   AI Engagement Experience \(AIEX\)\(v2.0.3\)

Role required: admin

## About this task

**Note:** Applications are installed only if you have the license. If you don’t have the required license for an application, it isn’t installed.

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home** on your instance.

2.  On the IT Operations Management tile, select **View product overview**.

3.  In the ITOM hub, select **Start setup**.

    ![IT Operations Management Product Hub start setup screen.](../image/nowassist-setup-start-setup.png)

4.  On the Installation progress page, select the install icon \(![Install icon.](../image/icon-now-assist-setup-download.png)\) on the ITOM Visibility card.

    ![Installation progress page to install ITOM Visibility.](../image/now-assist-setup-download.png)

    **Note:** Expand the What's included section to view the applications installed with ITOM Visibility.


