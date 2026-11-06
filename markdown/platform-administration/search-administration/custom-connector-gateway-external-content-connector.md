---
title: Custom Connector Gateway external content connector
description: The Custom Connector Gateway external content connector makes a source system's content and metadata searchable in AI Search applications. Retrieve content, metadata, and users with your own custom connector and push that data to the gateway connector using the Custom Connector Gateway API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/custom-connector-gateway-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-10-21"
reading_time_minutes: 3
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Custom Connector Gateway external content connector

The Custom Connector Gateway external content connector makes a source system's content and metadata searchable in AI Search applications. Retrieve content, metadata, and users with your own custom connector and push that data to the gateway connector using the Custom Connector Gateway API.

Unlike other external content connectors, the Custom Connector Gateway connector doesn't run content or user permission crawls to retrieve content and security principals from the source system. Instead, it serves as a way for your custom connector to submit retrieved content and security principals for indexing via the Custom Connector Gateway API.

The process of indexing searchable content from your source system with a custom connector looks like this:

1.  Your custom connector executes periodic crawls to retrieve document content and metadata and security principal details from your source system.
2.  During each crawl, your custom connector submits add and delete requests for documents and security principals to the `xcc-ingest` Custom Connector Gateway API endpoint on your ingest gateway host.
3.  The ingest gateway host transmits document and security principal add and delete requests submitted via the Custom Connector Gateway API to the Custom Connector Gateway connector running on your ServiceNow AI Platform instance.
4.  On your ServiceNow AI Platform® instance, the Custom Connector Gateway connector feeds the retrieved data to AI Search for indexing, making it searchable in your AI Search applications.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

To learn more about developing a custom connector, see [Implementing a custom connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/implementing-custom-connector.md). For details on the endpoint and operations available in the Custom Connector Gateway API, see [Custom Connector Gateway API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/custom-connector-gateway-api.md).

## Custom Connector Gateway prerequisites

Before you can use the Custom Connector Gateway connector, you must configure your ServiceNow AI Platform instance to satisfy the connector's prerequisites. For details on this procedure, see [Configure your ServiceNow AI Platform instance to support the Custom Connector Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-instance-custom-connector-gateway.md).

## The ingest gateway host

The ingest gateway host is a server provided by ServiceNow to facilitate Custom Connector Gateway API operations. It's distinct from both your ServiceNow AI Platform instance and your AI Search node.

**Note:** Architectural components for ingest gateway hosts are deployed in ServiceNow regional datacenters. If your ServiceNow AI Platform instance is hosted in an in-country datacenter, check with your ServiceNow contact to confirm whether ingest gateway hosts are supported in your in-country datacenter before beginning implementation.

-   **[Implementing a custom connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/implementing-custom-connector.md)**  
Your custom connector retrieves content, metadata, and security principals from a system of your choice. It runs on your local or cloud server and uses the Custom Connector Gateway API to send its retrieved data to a Custom Connector Gateway external content connector defined on your ServiceNow AI Platform® instance. The Custom Connector Gateway connector feeds the retrieved data to AI Search for indexing.
-   **[Find the hostname for your ingest gateway host](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/find-hostname-ingest-gateway-host.md)**  
Look up the hostname for the ingest gateway host associated with your ServiceNow AI Platform® instance. Your custom connector needs this hostname to send its Custom Connector Gateway API requests to the proper host.
-   **[Get the sys\_id for a Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/get-sys-id-custom-connector-gateway-external-content-connector.md)**  
Retrieve the sys\_id for a Custom Connector Gateway external content connector. This sys\_id value is required when creating or retrieving a Java Web Token \(JWT\) using the Custom Connector Gateway API.
-   **[Configure your ServiceNow AI Platform instance to support the Custom Connector Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-instance-custom-connector-gateway.md)**  
Configure settings in your ServiceNow AI Platform instance to satisfy the prerequisites for the Custom Connector Gateway.
-   **[Create a Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-ext-cont-connector-custom-connector-gateway.md)**  
Create a Custom Connector Gateway external content connector to index searchable content and security principals retrieved by your custom connector implementation.
-   **[Custom Connector Gateway default schema fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/custom-connector-gateway-default-schema-fields.md)**  
The default schema for Custom Connector Gateway external content connectors includes predefined fields to store content item metadata. Use these fields in requests your custom connector sends to the Custom Connector Gateway API endpoint.

**Parent Topic:**[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configuring-ext-cont-connectors.md)

