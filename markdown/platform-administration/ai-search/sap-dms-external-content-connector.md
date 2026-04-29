---
title: SAP DMS external content connector
description: The SAP DMS external content connector retrieves documents from repositories in your SAP Document Management System instance and makes their content and metadata searchable in AI Search applications.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# SAP DMS external content connector

The SAP DMS external content connector retrieves documents from repositories in your SAP Document Management System instance and makes their content and metadata searchable in AI Search applications.

Connector administrators can run or schedule content crawls to retrieve updated content and access permissions from your source system, or user permission crawls to retrieve updated security principals from your source system. Both types of crawl feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Create a subaccount in the SAP Business Technology Platform \(BTP\)](../task/create-subaccount-sap-btp.md)**  
Create a subaccount with required entitlements in your SAP global account using the SAP BT cockpit. You need this subaccount in order to configure SAP access for the SAP DMS external content connector.
-   **[Create a SAP user and role collection](../task/create-sap-user-role-collection.md)**  
Create a user and a role collection in the SAP Business Technology Platform \(BTP\) cockpit. The SAP DMS external content connector needs this user account to access your SAP DMS content.
-   **[Configure SAP DMS for external content indexing](../task/configure-sap-dms-external-content-indexing.md)**  
Create service instances and service keys in your SAP Business Technology Platform \(BTP\) global account to allow the SAP DMS external content connector to access your SAP DMS documents and repositories.
-   **[Create a SAP DMS external content connector](../task/create-ext-cont-connector-sap-dms.md)**  
Create an external content connector to retrieve searchable content and security principals from your SAP DMS source system.
-   **[Configure crawl settings for a SAP DMS external content connector](../task/configure-crawl-settings-sap-dms-external-content-connector.md)**  
Specify the folders you want your SAP DMS external content connector to crawl. Define inclusion or exclusion filters to specify which content the crawl retrieves and feeds to AI Search for indexing.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

