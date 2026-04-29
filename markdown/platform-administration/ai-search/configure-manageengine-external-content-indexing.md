---
title: Configure ManageEngine for external content indexing
description: Create a server-based OAuth 2.0 client application in the Zoho API console to allow the ManageEngine external content connector to access your ManageEngine source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [ManageEngine external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure ManageEngine for external content indexing

Create a server-based OAuth 2.0 client application in the Zoho API console to allow the ManageEngine external content connector to access your ManageEngine source system.

## Before you begin

You need the following permissions in your ManageEngine instance:

-   Administrator or privileged access
-   API access
-   Read-only access to knowledge base articles and their attachments

Role required: none

## About this task

The ManageEngine external content connector retrieves public-domain knowledge articles from knowledge bases in your ManageEngine source system using the ManageEngine REST API.

To allow the connector to access your ManageEngine content via the REST API, you must create a server-based OAuth 2.0 client application in the Zoho API console. Your connector admin can use the ID and secret from this client application to configure the ManageEngine external connector for proper connection to your source system.

## Procedure

1.  Navigate to the Zoho API console at [https://api-console.zoho.com/](https://api-console.zoho.com/) and log in with Administrator or privileged credentials when prompted.

2.  Create a new server-based OAuth 2.0 client application.

    1.  Select **Get Started** or **Add Client**.

        The **Get Started** link appears if you haven't added any client applications. If you've previously added one or more client applications, the **Add Client** link appears instead.

    2.  On the Choose a Client Type page, select **Server-based Applications**.

    3.  On the Create New Client page, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Client Name|Enter a unique name for your OAuth 2.0 client application.|
        |Homepage URL|Enter `https://<instance-name>.service-now.com/`, where `<instance-name>` is the hostname of your ServiceNow AI Platform® instance.|
        |Authorized Redirect URIs|Enter `https://<instance-name>.service-now.com/oauth_redirect.do`, where `<instance-name>` is the hostname of your ServiceNow AI Platform® instance.|

    4.  Select **Create**.

    The API console displays your new server-based OAuth 2.0 client application.

3.  Record the client ID and client secret for your new server-based OAuth 2.0 client application.

    1.  Select your new server-based OAuth 2.0 client application from the client list.

    2.  Navigate to the application's **Client Secret** page.

    3.  Copy the application's **Client ID** and store it in a secure location.

        **Important:** Your external content connector admin needs this client ID when configuring the ManageEngine external content connector.

    4.  Copy the application's **Client Secret** and store it in a secure location.

        **Important:** Your external content connector admin needs this client secret when configuring the ManageEngine external content connector.


## What to do next

Provide the following items to your connector admin:

-   The URL for your ManageEngine instance.
-   The client ID that you copied in step [3.c](configure-manageengine-external-content-indexing.md#copy-client-id-step).
-   The client secret that you copied in step [3.d](configure-manageengine-external-content-indexing.md#copy-client-secret-step).

Your connector admin needs these items to configure a ManageEngine external content connector to retrieve public-domain knowledge articles from your ManageEngine source system.

For details on creating and configuring a ManageEngine external content connector, see [Create a ManageEngine external content connector](create-ext-cont-connector-manageengine.md).

**Parent Topic:**[ManageEngine external content connector](../concept/manageengine-external-content-connector.md)

