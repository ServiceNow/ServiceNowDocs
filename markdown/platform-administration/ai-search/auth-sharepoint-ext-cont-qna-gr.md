---
title: Sign in to Microsoft SharePoint Online to authorize External Content Q&amp;A Genius Results
description: Obtain an OAuth 2.0 token from Microsoft SharePoint Online so that External Content Q&amp;A Genius Results can find documents and generate answers when you search.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Q&amp;A Genius Results, Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Sign in to Microsoft SharePoint Online to authorize External Content Q&amp;A Genius Results

Obtain an OAuth 2.0 token from Microsoft SharePoint Online so that External Content Q&amp;A Genius Results can find documents and generate answers when you search.

## Before you begin

You only need to perform this task if your search results page displays this informational message: `To view results generated from SharePoint, you need to be signed in.`

Role required: none

## About this task

External Content Q&amp;A Genius Results use an OAuth 2.0 token to access your Microsoft SharePoint Online instance and search for relevant documents. The OAuth 2.0 token is specific to your Microsoft SharePoint Online user account, so your search only returns documents that you can access.

Perform this task to generate a valid OAuth 2.0 token in Microsoft SharePoint Online and authorize External Content Q&amp;A Genius Results for your searches.

**Note:** How often you need to sign in depends on your Microsoft SharePoint Online instance's settings. For questions about the OAuth 2.0 token's lifespan, contact your Microsoft SharePoint Online administrator.

## Procedure

1.  Select the **Sign in** link in the informational message on your search results page.

2.  When prompted, enter your Microsoft SharePoint Online credentials to authenticate with Microsoft.

    **Note:** This login step submits your credentials directly to Microsoft. If you're unable to authenticate, contact your Microsoft SharePoint Online administrator.

3.  Once you're authenticated, repeat your previous search.

    **Note:** External Content Q&amp;A Genius Results respect your Microsoft SharePoint Online user profile security settings. If you're not seeing an expected Genius Result answer, it's a good idea to check with your Microsoft SharePoint Online administrator to make sure you have access to the appropriate source documents.


**Parent Topic:**[External Content Q&amp;A Genius Results](../concept/external-content-qna.md)

