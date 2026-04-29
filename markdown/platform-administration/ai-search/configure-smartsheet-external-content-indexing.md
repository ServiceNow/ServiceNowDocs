---
title: Configure Smartsheet for external content indexing
description: Generate an API key in Smartsheet to allow the Smartsheet external content connector to access your Smartsheet source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Smartsheet external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Smartsheet for external content indexing

Generate an API key in Smartsheet to allow the Smartsheet external content connector to access your Smartsheet source system.

## Before you begin

You need a Smartsheet account with administrator privileges. The external content connector will run in the context of this account.

Role required: none

## About this task

The Smartsheet external content connector retrieves sheets from workspaces in your Smartsheet source system using the Smartsheet API.

To allow the connector to access your Smartsheet source system via the Smartsheet API, you must generate an API key \(access token\) in Smartsheet. Your connector admin can use this API key to configure the Smartsheet external connector for proper connection to your source system.

## Procedure

1.  Record your Smartsheet domain URL.

    The domain URL typically has the format `https://example.smartsheet.com/`.

    **Important:** Your connector admin needs this Smartsheet domain URL when configuring the Smartsheet external content connector.

2.  In Smartsheet, generate an API key for the Smartsheet external content connector.

    1.  Navigate to [https://app.smartsheet.com/](https://app.smartsheet.com/) and log in with administrator credentials.

    2.  Select the **Account Settings** icon ![](../image/smartsheet-account-settings-icon.png), then select **Personal Settings…** in the context menu.

    3.  In the Personal Settings dialog box, select **API Access**, then select **Generate new access token**.

    4.  Enter a name for your API key, then select **OK**.

        As an example, you might enter `Smartsheet external content connector API key` as the name for the API key.

        The value of your new API key appears in the dialog box.

    5.  Copy the API key value and store it in a secure location.

        **Important:** Your connector admin needs this API key value when configuring the Smartsheet external content connector.

    6.  Close the API key dialog box by selecting **OK**, then close the Personal Settings dialog box by selecting **Close**.


## What to do next

Provide the following items to your connector admin:

-   The URL for your Smartsheet domain that you recorded in step [1](configure-smartsheet-external-content-indexing.md#record-smartsheet-domain-url-step).
-   The API key value that you copied in step [2.e](configure-smartsheet-external-content-indexing.md#copy-api-key-value-step).

Your connector admin needs these items to configure a Smartsheet external content connector to retrieve sheets and security principals from your Smartsheet source system.

For details on creating and configuring a Smartsheet external content connector, see [Create a Smartsheet external content connector](create-ext-cont-connector-smartsheet.md).

**Parent Topic:**[Smartsheet external content connector](../concept/smartsheet-external-content-connector.md)

