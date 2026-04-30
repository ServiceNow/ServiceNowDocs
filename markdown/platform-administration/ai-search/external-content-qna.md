---
title: External Content Q&amp;A Genius Results
description: External Content Q&amp;A Genius Results display concise, actionable AI-generated answers derived from documents in your Microsoft SharePoint Online instance.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# External Content Q&amp;A Genius Results

External Content Q&amp;A Genius Results display concise, actionable AI-generated answers derived from documents in your Microsoft SharePoint Online instance.

**Important:** Starting with the Now Assist in AI Search 10 release, the External Content Q&amp;A Genius Results feature is being prepared for future deprecation. This feature is no longer installed on new instances and is removed from instances where it's not in use, but will continue to be supported on instances where it's in use. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## External Content Q&amp;A Genius Results overview

The External Content Q&amp;A Genius Result configuration searches for documents relevant to your search using an Integration Hub subflow. If it finds sufficiently relevant documents, it sends them to the Now LLM Service, which generates answers from their content and metadata.

Each External Content Q&amp;A Genius Result answer card includes a generated answer. For reference, the answer card also includes a link you can select to download the source documents.

**Note:** Because the External Content Q&amp;A Genius Result answer is automatically generated, it's a good idea to review it for accuracy. You can provide feedback on the answer by selecting the thumbs-up icon ![](../image/genius-result-feedback-positive.png) if the generated answer is accurate, or the thumbs-down icon ![](../image/genius-result-feedback-negative.png) if it's not. Your feedback helps ServiceNow improve future versions of this Genius Result configuration.

When searching for relevant documents, the system uses your Microsoft SharePoint Online credentials and user profile, so your searches generate External Content Q&amp;A Genius Result answers from documents that you can access.

## Enabling External Content Q&amp;A Genius Results

To make External Content Q&amp;A Genius Results available for use in AI Search applications, administrators first need to perform the following steps:

1.  Ensure that the ServiceNow IntegrationHub Enterprise Pack Installer \[com.glide.hub.integrations.enterprise\] plugin is installed on your instance. If this plugin isn't installed, you can request it. For details on requesting IntegrationHub plugins, see [Request an Integration Hub plugin](https://www.servicenow.com/docs/access?context=request-integrationhub&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).
2.  Create and configure an OAuth application in the Microsoft Azure portal to verify and authorize connection requests from your ServiceNow AI Platform® instance. To learn about this procedure, see [Configure OAuth application in Microsoft Azure](https://www.servicenow.com/docs/access?context=configure-oauth-application-in-microsoft-azure&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).
3.  Add the AllSites.FullControl SharePoint delegated permission \(and grant admin consent\) to your new OAuth application in the Microsoft Azure portal. For details on this procedure, see [Configure SharePoint API permissions for your External Content Q&amp;A Genius Results OAuth 2.0 application](../task/grant-perms-azure-ext-cont-qna-grs.md).
4.  Define OAuth configuration settings for External Content Q&amp;A Genius Results. For full details on the required OAuth settings, see [Configure OAuth settings for External Content Q&amp;A Genius Results](../task/configure-oauth-ext-cont-qna-gr.md).

Next, search administrators need to enable External Content Q&amp;A Genius Results in one or more AI Search portals. To learn about this procedure, see [Enable Now Assist Genius Results in AI Search portals and mobile applications](../task/enable-now-assist-gr-ais-apps.md).

Once all these steps are completed, AI Search portal users can authorize External Content Q&amp;A Genius Results for their searches by authenticating with Microsoft SharePoint Online. For details on this authentication procedure, see [Sign in to Microsoft SharePoint Online to authorize External Content Q&amp;A Genius Results](../task/auth-sharepoint-ext-cont-qna-gr.md).

**Note:** When you activate External Content Q&amp;A Genius Results in a search application, they're available to all users with Microsoft SharePoint Online credentials who search using that application.

## Limitations

By default, External Content Q&amp;A Genius Results only support English-language searches. Administrators can enable support for other languages by activating Dynamic Translation. To learn more about how content and answers are translated, see [Dynamic Translation for Now Assist Q&amp;A Genius Results](dynamic-translation-na-gr.md). For more details on Dynamic Translation, see [Dynamic Translation](../../dynamic-translation/concept/dynamic-translation-overview.md).

External Content Q&amp;A Genius Results only generate answers from documents found in your Microsoft SharePoint Online instance. They don't generate answers from sites found in your instance.

## Interaction with other search features

The following table describes the interactions between External Content Q&amp;A Genius Results and other search features.

|Feature|Interaction with External Content Q&amp;A Genius Results Genius Results|
|-------|-----------------------------------------------------------------------|
|[Result improvement rules](result-improvement-rules-ais.md)|When computing External Content Q&amp;A Genius Result answers, AI Search doesn't apply your result improvement rules because they don't operate on documents from your Microsoft SharePoint Online instance.|
|[Stop words](stop-words-ais.md)|When computing External Content Q&amp;A Genius Result answers, AI Search doesn't remove stop words from your search.|
|[Synonyms](synonyms-ais.md)|When computing External Content Q&amp;A Genius Result answers, AI Search doesn't expand synonyms found in your search.|
|[Typo handling](typo-handling-ais.md)|When computing External Content Q&amp;A Genius Result answers, AI Search doesn't correct misspelled search terms.|

-   **[Configure SharePoint API permissions for your External Content Q&amp;A Genius Results OAuth 2.0 application](../task/grant-perms-azure-ext-cont-qna-grs.md)**  
Add the AllSites.FullControl SharePoint API delegated permission to your External Q&amp;A Genius Results OAuth 2.0 application in Microsoft Azure portal and grant admin consent to allow the application to access this permission. The OAuth 2.0 application for External Q&amp;A Genius Results requires the delegated permission to search your Microsoft SharePoint Online sites.
-   **[Configure OAuth settings for External Content Q&amp;A Genius Results](../task/configure-oauth-ext-cont-qna-gr.md)**  
Configure the settings that External Content Q&amp;A Genius Results need to interact with your Microsoft SharePoint Online instance.
-   **[Restrict the Microsoft SharePoint Online sites that External Content Q&amp;A Genius Results can search](../task/filter-spo-sites-ext-cont-qa-gr.md)**  
Define a Microsoft Keyword Query Language \(KQL\) query to restrict the set of Microsoft SharePoint Online sites \(paths\) that External Content Q&amp;A Genius Results can search for documents. Only documents that satisfy your query are eligible for External Content Q&amp;A Genius Result answer generation.
-   **[Sign in to Microsoft SharePoint Online to authorize External Content Q&amp;A Genius Results](../task/auth-sharepoint-ext-cont-qna-gr.md)**  
Obtain an OAuth 2.0 token from Microsoft SharePoint Online so that External Content Q&amp;A Genius Results can find documents and generate answers when you search.

**Parent Topic:**[Configuring Now Assist in AI Search](configuring-now-assist-ais.md)

