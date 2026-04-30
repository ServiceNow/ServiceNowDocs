---
title: Configure Aha! Roadmaps for external content indexing
description: Generate an API key in Aha! Roadmaps to allow the Aha! Roadmaps external content connector to access content from your workspaces.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-01-22"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Aha! Roadmaps external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Aha! Roadmaps for external content indexing

Generate an API key in Aha! Roadmaps to allow the Aha! Roadmaps external content connector to access content from your workspaces.

## Before you begin

Your organization must have already set up a custom Aha! domain.

Your Aha! Roadmaps account needs either the owner role for your organization's workspace or the account admin role. To learn about non-administrator and administrator roles in Aha! Roadmaps, see [https://support.aha.io/aha-roadmaps/account/billing-and-users/user-permissions~7444657360296913475](https://support.aha.io/aha-roadmaps/account/billing-and-users/user-permissions~7444657360296913475).

Role required: none

## About this task

The Aha! Roadmaps external content connector retrieves Features, Goals, Ideas, Notes, and Releases from workspaces in your Aha! Roadmaps source system using the Aha! REST API.

To allow the connector to access your Aha! Roadmaps content via the REST API, you must generate an API key in Aha! Roadmaps. Your connector admin can use this API key to configure the Aha! Roadmaps external connector for proper connection to your source system.

## Procedure

1.  In Aha! Roadmaps, generate a new API key for use by the Aha! Roadmaps external content connector.

    1.  Navigate to [https://secure.aha.io/settings/api\_keys](https://secure.aha.io/settings/api_keys) and log in with your administrator or workspace owner credentials when prompted.

    2.  Select **Generate API Key**.

    3.  Enter a name for your new API key, then select **Generate API Key**.

    4.  Copy your new API key and store it in a secure location.

        **Important:** Your external content connector admin needs this API key when configuring the Aha! Roadmaps external content connector.


## What to do next

Provide the following items to your connector admin:

-   The host URL for your Aha! Roadmaps instance. This is typically `https://<organization>.aha.io/`, where `<organization>` is the name of your organization.
-   The API key value that you copied in step [1.d](configure-aha-roadmaps-external-content-indexing.md#copy-api-key-step).

Your connector admin needs these items to configure a Aha! Roadmaps external content connector to retrieve Features, Goals, Ideas, Notes, and Releases and security principals from your Aha! Roadmaps source system.

For details on creating and configuring a Aha! Roadmaps external content connector, see [Create an Aha! Roadmaps external content connector](create-ext-cont-connector-aha-roadmaps.md).

**Parent Topic:**[Aha! Roadmaps external content connector](../concept/aha-roadmaps-external-content-connector.md)

