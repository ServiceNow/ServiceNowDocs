---
title: Configure Cornerstone for external content indexing
description: Create and authorize an OAuth 2.0 application in the Cornerstone to allow the Cornerstone external content connector to access your Cornerstone source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/configure-cornerstone-external-content-indexing.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-01-13"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Cornerstone external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Cornerstone for external content indexing

Create and authorize an OAuth 2.0 application in the Cornerstone  to allow the Cornerstone external content connector to access your Cornerstone source system.

## Before you begin

You need a Cornerstone OnDemand account with the Edge APIs - Manage security permission.

Role required: none

## About this task

The Cornerstone external content connector retrieves Catalogue and Learning objects from organization units in your Cornerstone source system using the Cornerstone API.

To allow the connector to access your Cornerstone source system via the API, you must register an OAuth 2.0 application in Cornerstone OnDemand. Your connector administrator can use settings copied from the OAuth 2.0 application to configure the Cornerstone external connector for proper connection to your source system.

## Procedure

1.  In Cornerstone OnDemand, register a new OAuth 2.0 application for use by the Cornerstone external content connector.

    1.  Log in to your Cornerstone OnDemand with administrator credentials.

    2.  Select **Settings** &gt; **Admin** &gt; **Tools**, then select **Edge**.

    3.  On the Edge page, in the Develop section, select **API Management**.

    4.  On the API Management page, select **Manage OAuth 2.0 Applications**, then select **Register New Application**.

    5.  On the new application form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Application Name|Name for your new OAuth 2.0 application. As an example, you might enter `Cornerstone-XCC`.|
        |User ID|Identifier for the user account that runs the OAuth 2.0 application. Enter the ID for the administrator account you used to log in to Cornerstone OnDemand.|
        |Access Token Validity Period|Validity period in seconds for access tokens for the OAuth 2.0 application. Enter `86400` \(equivalent to 24 hours\).|

    6.  In the drop-down list for the new application form, select **Cornerstone API**, then select the options for these API scopes.

        -   training:read
        -   employee:read
        -   group:read
        -   ou:read
        -   outype:read
        -   learning:read
        -   catalog:read
        -   transcript:read
        -   task:read
        -   group:read
        -   certification:read
    7.  Select **Register Application**.

    The new application appears, with its Client ID and Client Secret fields populated.

2.  Copy the Client ID value for your new OAuth 2.0 application and store it in a secure location.

    **Important:** Your external content connector administrator needs this Client ID when configuring the Cornerstone external content connector.

3.  Copy the Client Secret value for your new OAuth 2.0 application and store it in a secure location.

    **Important:** Your external content connector administrator needs this Client Secret when configuring the Cornerstone external content connector.


## What to do next

Provide the following items to your connector administrator:

-   The Client ID value for your new OAuth 2.0 application that you copied in step [2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configure-cornerstone-external-content-indexing.md).
-   The Client Secret value for your new OAuth 2.0 application that you copied in step [3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configure-cornerstone-external-content-indexing.md).

Your connector administrator needs these items to configure a Cornerstone external content connector to retrieve Catalogue and Learning objects from your Cornerstone source system.

For details on creating and configuring a Cornerstone external content connector, see [Create a Cornerstone external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-ext-cont-connector-cornerstone.md).

**Parent Topic:**[Cornerstone external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/cornerstone-external-content-connector.md)

