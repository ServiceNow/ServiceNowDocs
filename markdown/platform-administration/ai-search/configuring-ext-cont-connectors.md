---
title: Configuring External Content Connectors
description: Plan and configure your External Content Connectors implementation.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-08-01"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring External Content Connectors

Plan and configure your External Content Connectors implementation.

## External Content Connectors configuration overview

Configuring retrieval and indexing of content from your external content source systems requires the following steps:

<table id="table_xbh_4z2_tdc"><thead><tr><th>

Configuration step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source system administrator configures access settings for your external content source system

</td><td>

-   [Configure Atlassian Confluence Cloud for external content indexing](../task/cfg-conf-cc-ext-cont-connector.md)
-   [Configure Atlassian Jira Cloud for external content indexing](../task/cfg-src-sys-settings-jira-ext-cont-connector.md)
-   [Configure Google Drive for external content indexing](../task/cfg-gcloud-settings-gdrive-ext-cont-connector.md)
-   [Configure Microsoft SharePoint Online for external content indexing](../task/cfg-azure-spo-ext-cont-connector.md)
-   [Configure Microsoft Teams for external content indexing](../task/cfg-src-sys-settings-msteams-ext-cont-connector.md)
-   [Configure Slack for external content indexing](../task/cfg-src-sys-settings-slack-ext-cont-connector.md)

</td></tr><tr><td>

AI Search administrator creates and configures external content connectors

</td><td>

-   [Creating external content connectors](../task/creating-ext-cont-connectors.md)
    -   [Create an Atlassian Confluence Cloud external content connector](../task/create-ext-cont-connector-acc.md)
    -   [Create an Atlassian Jira Cloud external content connector](../task/create-ext-cont-connector-jira.md)
    -   [Create a Google Drive external content connector](../task/create-ext-cont-connector-gdrive.md)
    -   [Create a Microsoft SharePoint Online external content connector](../task/create-ext-cont-connector-mspo.md)
    -   [Create a Microsoft Teams external content connector](../task/create-ext-cont-connector-msteams.md)
    -   [Create a predefined web sources external content connector](../task/create-ext-cont-connector-websources.md)
    -   [Create a ServiceNow product documentation external content connector](../task/create-ext-cont-connector-snowdoc.md)
    -   [Create a Slack external content connector](../task/create-ext-cont-connector-slack.md)
-   [Configuring crawl settings for external content connectors](cfg-crawl-settings-ext-cont-connector.md) \(optional\)
    -   [Configure crawl settings for the Atlassian Confluence Cloud external content connector](../task/configure-crawl-settings-cc-ext-cont-connector.md)
    -   [Configure crawl settings for the Atlassian Jira Cloud external content connector](../task/configure-crawl-settings-jira-ext-cont-connector.md)
    -   [Configure crawl settings for the Google Drive external content connector](../task/configure-crawl-settings-gdrive-ext-cont-connector.md)
    -   [Configure crawl settings for the Microsoft SharePoint Online external content connector](../task/configure-crawl-settings-spo-ext-cont-connector.md)
    -   [Configure crawl settings for the Microsoft Teams external content connector](../task/configure-crawl-settings-msteams-ext-cont-connector.md)
    -   [Configure crawl settings for the predefined web sources external content connector](../task/configure-crawl-settings-websources-ext-cont-connector.md)
    -   [Configure crawl settings for the Slack external content connector](../task/configure-crawl-settings-slack-ext-cont-connector.md)
    -   [Configure crawl settings for the ServiceNow product documentation external content connector](../task/configure-crawl-settings-snowdoc-ext-cont-connector.md)
-   [Define a crawl schedule for an external content connector](../task/define-schedule-ext-cont-connector.md)

</td></tr></tbody>
</table>-   **[Estimating document volume for source systems](estimating-doc-volume-src-sys.md)**  
Source system tools allow you to estimate the number of documents available for retrieval by external content connectors. By estimating the available document count for a source system, you can determine whether you need to apply crawl scope restrictions when configuring an external content connector for that source system.
-   **[Configuring source systems for external content indexing](cfg-src-sys-ext-content-indexing.md)**  
Source system administrators configure settings to allow external content connectors to index your documents and security settings for search. These settings must be configured for a source system before you create an external content connector to crawl that source system.
-   **[Configure the Microsoft cloud service endpoint URL](../task/configure-ms-cloud-service-endpoint-url.md)**  
Specify the proper cloud service endpoint URL to use for external content connectors that crawl your Microsoft cloud application tenants.
-   **[Creating external content connectors](../task/creating-ext-cont-connectors.md)**  
Search administrators create external content connectors to retrieve searchable content and security principals from supported source systems.
-   **[Configuring crawl settings for external content connectors](cfg-crawl-settings-ext-cont-connector.md)**  
Search administrators can configure crawl settings for each external content connector, such as which source system locations it crawls and which types of files it sends to AI Search for indexing.
-   **[Add an external content search source to Now Assist in Virtual Agent](../task/add-ext-cont-srch-src-na-va.md)**  
Include searchable content retrieved by an external content connector in your Now Assist in Virtual Agent conversations.

**Parent Topic:**[External Content Connectors](../reference/ext-cont-connectors-landing-page.md)

