---
title: Configure Notion for external content indexing
description: Create and authorize an internal integration in the Notion integrations dashboard to allow the Notion external content connector to access your Notion source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Notion external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Notion for external content indexing

Create and authorize an internal integration in the Notion integrations dashboard to allow the Notion external content connector to access your Notion source system.

## Before you begin

You need a Notion account with the Workspace owner role for your organization's workspace. To learn about workspace member roles, see the [Manage members &amp; guests](https://www.notion.com/help/add-members-admins-guests-and-groups) Notion help resource.

Role required: none

## About this task

The Notion external content connector retrieves pages and files from your Notion source system using the Notion REST API.

To allow the connector to access your Notion source system via the Notion REST API, you must configure and authorize an internal integration in the Notion integrations dashboard. Your connector admin can use settings copied from the internal integration to configure the Notion external connector for proper connection to your source system.

**Important:** The Notion external content connector doesn't retrieve per-user permissions when running content crawls. All content indexed by the connector is searchable by all mapped users who have access to your configured AI Search experience.

## Procedure

1.  In the Notion integrations dashboard, create a new internal integration for the Notion external content connector.

    1.  Navigate to [https://www.notion.so/profile/integrations](https://www.notion.so/profile/integrations) and log in with your Notion credentials.

    2.  Select **New integration**.

    3.  Enter a name for your new integration.

        As an example, you might enter `Notion external content connector`.

    4.  Select your organization's workspace as the workspace to associate with your new integration.

    5.  Set your new integration's type to **Internal**.

    6.  Select **Save**.

    A message indicates that your new internal integration was successfully created and shows a **Configure integration settings** button.

2.  Get the secret for your new internal integration.

    1.  Select **Configure integration settings**.

        The Configuration page for your new internal integration appears.

    2.  Locate the internal integration secret and display its value by selecting **Show**.

    3.  Copy the internal integration secret and record it in a secure location.

        **Important:** Your external content connector admin needs this internal integration secret when configuring the Notion external content connector.

3.  Configure the capabilities for your new internal integration.

    1.  In the Capabilities section, under Content Capabilities, select the **Read content** option if it's not already selected.

    2.  In the Capabilities section, under User Capabilities, select the **Read user information including email address** option if it's not already selected.

4.  Perform the following steps to enable your new internal integration for each page in your workspace that you want the Notion external content connector to be able to retrieve searchable content and metadata from.

    **Note:** Enabling your internal integration for a page automatically enables it for all of that page's subpages.

    1.  Navigate to the selected Notion page.

    2.  In the menu at the upper right of the page, navigate to **. . .** &gt; **Connections** &gt; **Add connection**.

    3.  Select your new internal integration from the list of available connections.

    4.  Select **Confirm**.

    The selected Notion page and all of its subpages are added to your internal integration, allowing the Notion external content connector to retrieve their searchable content and metadata.


## What to do next

Provide the internal integration secret that you copied in step [2.c](configure-notion-external-content-indexing.md#copy-internal-integration-secret-step) to your connector admin.

Your connector admin needs this item to configure a Notion external content connector to retrieve pages, files, and security principals from your Notion source system.

For details on creating and configuring a Notion external content connector, see [Create a Notion external content connector](create-ext-cont-connector-notion.md).

**Parent Topic:**[Notion external content connector](../concept/notion-external-content-connector.md)

