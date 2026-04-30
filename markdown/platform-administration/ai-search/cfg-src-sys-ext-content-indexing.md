---
title: Configuring source systems for external content indexing
description: Source system administrators configure settings to allow external content connectors to index your documents and security settings for search. These settings must be configured for a source system before you create an external content connector to crawl that source system.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring source systems for external content indexing

Source system administrators configure settings to allow external content connectors to index your documents and security settings for search. These settings must be configured for a source system before you create an external content connector to crawl that source system.

Each external content connector has its own source system configuration requirements, as shown in the following topics.

**Note:** The following external content connectors do not require any source system configuration.

-   Predefined web sources external content connector
-   ServiceNow® documentation external content connector

-   **[Configure Atlassian Confluence Cloud for external content indexing](../task/cfg-conf-cc-ext-cont-connector.md)**  
Register an OAuth 2.0 integration in the Atlassian Developer console and create an API key in Atlassian Administration to allow the Atlassian Confluence Cloud external content connector to crawl spaces and security principals in your Atlassian Confluence Cloud source system.
-   **[Configure Atlassian Jira Cloud for external content indexing](../task/cfg-src-sys-settings-jira-ext-cont-connector.md)**  
Register an OAuth 2.0 integration in the Atlassian Developer console and create an API key in Atlassian Administration to allow the Atlassian Jira Cloud external content connector to crawl projects and security principals in your Atlassian Jira Cloud source system.
-   **[Configure Google Drive for external content indexing](../task/cfg-gcloud-settings-gdrive-ext-cont-connector.md)**  
Enable the Google Drive and Admin SDK APIs and create a Google Cloud service account to allow the Google Drive external content connector to crawl shared drives and security principals in your Google Drive source system.
-   **[Configure Microsoft SharePoint Online for external content indexing](../task/cfg-azure-spo-ext-cont-connector.md)**  
Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft SharePoint Online external content connector to access your Microsoft SharePoint Online source system.
-   **[Configure Microsoft Teams for external content indexing](../task/cfg-src-sys-settings-msteams-ext-cont-connector.md)**  
Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft Teams external content connector to access your Microsoft Teams source system.
-   **[Configure Slack for external content indexing](../task/cfg-src-sys-settings-slack-ext-cont-connector.md)**  
Create a Slack API application to allow the Slack external content connector to crawl public channels in your Slack source system.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

