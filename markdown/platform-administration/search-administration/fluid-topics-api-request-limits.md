---
title: Request limits in Fluid Topics Knowledge Hub web services
description: By default, the Fluid Topics API limits the number of maps, topics, and unstructured documents retrieved by requests to Knowledge Hub web services. These default limits may prevent the Fluid Topics external content connector from indexing all of your source system content. To request increases to these limits, open a ticket in the Fluid Topics Help Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/fluid-topics-api-request-limits.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Fluid Topics external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Request limits in Fluid Topics Knowledge Hub web services

By default, the Fluid Topics API limits the number of maps, topics, and unstructured documents retrieved by requests to Knowledge Hub web services. These default limits may prevent the Fluid Topics external content connector from indexing all of your source system content. To request increases to these limits, open a ticket in the Fluid Topics Help Center.

## Default retrieval limits in the Fluid Topics API

The Fluid Topics external content connector retrieves content from your source system using requests submitted to Knowledge Hub web services provided by the Fluid Topics API. In particular, it retrieves your maps, topics, and unstructured documents via these web services.

By default, the Fluid Topics API imposes limits on how many items can be retrieved per web service request, as follows:

<table><thead><tr><th>

Item type

</th><th>

Default limit

</th></tr></thead><tbody><tr><td>

Maps

</td><td>

Limit of 1,000 maps per request to the API's List maps Knowledge Hub web service.For details on this web service, including the limit, see the [List maps](https://docs.fluidtopics.com/r/Fluid-Topics-API-Reference-Guide/Knowledge-Hub-web-services-for-everyone/Maps/List-maps) topic in the Fluid Topics API Reference Guide.

</td></tr><tr><td>

Topics

</td><td>

Limit of 1,000 topics per request to the API's Search topics Knowledge Hub web service.For details on this web service, including the limit, see the [Search topics](https://docs.fluidtopics.com/r/Fluid-Topics-API-Reference-Guide/Knowledge-Hub-web-services-for-everyone/Topics/Search-topics) topic in the Fluid Topics API Reference Guide.

</td></tr><tr><td>

Unstructured documents

</td><td>

Limit of 1,000 documents per request to the API's List unstructured documents Knowledge Hub web service.For details on this web service, including the limit, see the [List unstructured documents](https://docs.fluidtopics.com/r/Fluid-Topics-API-Reference-Guide/Knowledge-Hub-web-services-for-everyone/Unstructured-documents/List-unstructured-documents) topic in the Fluid Topics API Reference Guide.

</td></tr></tbody>
</table>If your source system contains more than 1,000 maps, topics, or unstructured documents, these default limits prevent the Fluid Topics external content connector from indexing all of your source system content. The connector needs to retrieve all of your maps, topics, or unstructured documents in a single request.

## Increasing retrieval limits in the Fluid Topics API

To request increases to these Knowledge Hub web service retrieval limits, you can open a ticket in the Fluid Topics Help Center at [https://helpcenter.fluidtopics.com/](https://helpcenter.fluidtopics.com/). Be sure to request increases to all of the retrieval relevant limits so that the Fluid Topics external content connector can retrieve all of your source system content.

As an example, if your source system includes 544 maps, 1,817 topics, and 1,193 unstructured documents, you must request increases to the default retrieval limits for both the Search topics and List unstructured documents Knowledge Hub web services.

**Parent Topic:**[Fluid Topics external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/fluid-topics-external-content-connector.md)

