---
title: Integration with external knowledge sources
description: Use the external content integration feature to integrate content from various external sources and enable unified knowledge search results.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integration with external knowledge sources

Use the external content integration feature to integrate content from various external sources and enable unified knowledge search results.

Users store and manage knowledge using various external sources and search each source separately for relevant results. External content integration enables acquiring and searching all WebDAV-compliant source content from a single location. This provides users with a seamless search experience across multiple knowledge sources and drives more usage to the platform.

Using this feature, knowledge administrators can define the external content to be imported into a knowledge base and periodically run a job to import the content. Knowledge users have a seamless user experience searching for relevant content across multiple knowledge sources.

-   **[Activate the External Content Integration plugin](../task/act-ext-know-content.md)**  
The External Content Integration feature is activated with the Knowledge Management - External Content Integration plugin \(com.snc.knowledge.external\_integration\).
-   **[Define an external knowledge source](../task/define-an-external-knowledge-source.md)**  
Before you import content, create and configure the connection between the a Web Distributed Authoring and Versioning \(WebDAV\) - compliant external knowledge source and the ServiceNow knowledge base into which you want to import content. Define import parameters for the external knowledge source.
-   **[Import content from an external knowledge source](../task/run-import-job-external-content-integration.md)**  
Run an import job manually or set up a schedule to process the integrated external content.
-   **[Open knowledge search results in source system](../task/open-search-results-ext-content.md)**  
While search results are aggregated within your instance, your users can also utilize features available in the source system \(being able to edit in Microsoft SharePoint, for example\). To open knowledge search results in a host system, configure the URL to the external source system to open articles from search results directly in the source system.
-   **[Sample configuration for integrating external knowledge content](sample-ext-cont-integration.md#)**  
You can integrate content from multiple external sources so your users can acquire and search knowledge from a single location. Use this sample configuration to create a connection to your external account, configure external knowledge sources, and import content to enable search results for unified content.

**Parent Topic:**[Configuring Knowledge Management](configuring-knowledge-management.md)

