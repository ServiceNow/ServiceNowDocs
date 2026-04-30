---
title: ServiceNow instance external content connector
description: The ServiceNow instance external content connector retrieves KB article records \(and their attachments\) from your ServiceNow AI Platform source instance and makes their content and metadata searchable in AI Search applications in your ServiceNow AI Platform destination instance.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-04"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# ServiceNow instance external content connector

The ServiceNow instance external content connector retrieves KB article records \(and their attachments\) from your ServiceNow AI Platform source instance and makes their content and metadata searchable in AI Search applications in your ServiceNow AI Platform destination instance.

The ServiceNow AI Platform instance that you want the external content connector to retrieve searchable content and metadata from is your source instance. The instance where the connector runs and populates search applications with the retrieved data is your destination instance.

Search administrators can run or schedule content crawls to retrieve updated content from your source instance, or user permission crawls to retrieve updated security principals from your source instance. Both types of crawl feed their data to AI Search for indexing on your destination instance.

In your destination instance, the indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

**Important:** Your source and destination instances must be distinct from one another. The ServiceNow® instance external content connector is not designed to feed an instance's content back into itself.

You can only create one ServiceNow® instance external content connector on a given destination instance.

## User permissions

To view search results from the source instance, a user on the destination instance must satisfy the following conditions:

-   There must be a matching user account defined for them on the source instance, with the same email address.
-   Their user account on the source instance must have access to the content represented by the search results.

If these conditions are not satisfied, the destination instance user won't be able to see search results crawled from the source instance.

-   **[Configure your ServiceNow AI Platform instance for external content indexing](../task/configure-sn-aip-instance-external-content-indexing.md)**  
Create and configure a non-interactive service user account on your ServiceNow AI Platform® source instance to allow access by the ServiceNow instance external content connector.
-   **[Create a ServiceNow instance external content connector](../task/create-ext-cont-connector-snow-instance.md)**  
Create an external content connector to retrieve searchable content and security principals from a ServiceNow AI Platform instance.
-   **[Configure crawl settings for a ServiceNow instance external content connector](../task/configure-crawl-settings-snow-instance-external-content-connector.md)**  
Specify the content types that you want your ServiceNow instance external content connector to retrieve when running content crawls.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](../task/create-user-mapping-crawl-external-content-connector.md)

