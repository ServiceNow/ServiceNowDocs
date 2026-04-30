---
title: Configure Cornerstone for external content indexing
description: Create and authorize an OAuth 2.0 application in the Cornerstone to allow the Cornerstone external content connector to access your Cornerstone source system.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-12-18"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Cornerstone external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Cornerstone for external content indexing

Create and authorize an OAuth 2.0 application in the Cornerstone  to allow the Cornerstone external content connector to access your Cornerstone source system.

## Before you begin

You need administrator access privileges for Cornerstone OnDemand.

Role required: none

## About this task

The Cornerstone external content connector retrieves  from  in your Cornerstone source system using the Cornerstone REST API.

To allow the connector to access your Cornerstone source system via the REST API, you must configure and authorize an OAuth 2.0 application in Cornerstone OnDemand. Your connector admin can use settings copied from the OAuth 2.0 application and its  to configure the Cornerstone external connector for proper connection to your source system.

## Procedure

1.  In Cornerstone OnDemand, create a new OAuth 2.0 application for the Cornerstone external content connector.

    1.  Navigate to  and log in with administrator credentials.

    2.  

2.   for your new OAuth 2.0 application.

    1.  

    2.  

        **Important:** Your external content connector admin needs this  when configuring the Cornerstone external content connector.


## What to do next

Provide the following items to your connector admin:

-   
-   

Your connector admin needs these items to configure a Cornerstone external content connector to retrieve Catalogue and Learning objects from your Cornerstone source system.

For details on creating and configuring a Cornerstone external content connector, see [Create a Cornerstone external content connector](create-ext-cont-connector-cornerstone.md).

**Parent Topic:**[Cornerstone external content connector](cornerstone-external-content-connector.md)

