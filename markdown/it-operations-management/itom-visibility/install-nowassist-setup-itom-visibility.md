---
title: Install ITOM Visibility using ServiceNow Otto for Setup
description: Install all required ITOM Visibility applications and plugins from the IT Operations Management Product Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/itom-visibility/install-nowassist-setup-itom-visibility.html
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [ITOM Visibility, IT Operations Management]
---

# Install ITOM Visibility using ServiceNow Otto for Setup

Install all required ITOM Visibility applications and plugins from the IT Operations Management Product Hub.

## Before you begin

Verify the following:

-   You're using the Australia Patch 3, Zurich Patch 10, or later version of the ServiceNow AI Platform.
-   You have installed the ServiceNow Otto for Platform plugin \(sn\_genai\_platform\).
-   You have installed the Generative AI Controller plugin \(sn\_generative\_ai\).
-   You have installed the AI Skill Kit plugin \(sn\_skill\_builder\).
-   You have installed the ServiceNow Otto for IT Operations Management \(ITOM\) plugin. For more information, see [Install the ServiceNow Otto for IT Operations Management \(ITOM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/install-now-assist-itom.md).
-   You have activated the ServiceNow Otto panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).
-   You have activated the following assistants:

    -   ServiceNow Otto - Platform assistant
    -   ServiceNow Otto for Virtual Agent
    For more information, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/configure-now-assist-va.md).

-   You have activated Now LLM Service as a provider. For more information, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-large-language-models.md).
-   You have set up AI Search. For more information, see [AI Search readiness for ServiceNow Otto on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/sn-ai-impl-ai-search.md).
-   You have installed the following ServiceNow Otto for Setup applications from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home):
    -   ServiceNow Otto for Setup \(sn\_ia\)
    -   ServiceNow Otto for Setup Common \(sn\_ia\_common\)
    -   ServiceNow Otto for Setup Content \(sn\_ia\_content\)
    -   ServiceNow Otto for Setup Core \(sn\_ia\_now\_assist\)
    -   ServiceNow Otto for Setup Configuration \(sn\_ia\_config\)

Role required: admin

## About this task

**Note:** Applications are installed only if you have the license. If you don’t have the required license for an application, it isn’t installed.

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home** on your instance.

2.  Select the IT Operations Management tile.

3.  In the IT Operations Management Product Hub, select **Start setup**.

    \[Omitted image "nowassist-setup-start-setup.png"\] Alt text: IT Operations Management Product Hub start setup screen

4.  Select the install icon \(\[Omitted image "icon-now-assist-setup-download.png"\] Alt text: Install icon\) on the ITOM Visibility card.

    \[Omitted image "now-assist-setup-download.png"\] Alt text: Installation progress page to install ITOM Visibility

    **Note:** Expand the What's included section to view the applications installed with ITOM Visibility.


