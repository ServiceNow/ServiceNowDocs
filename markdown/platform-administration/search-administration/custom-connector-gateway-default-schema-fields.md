---
title: Custom Connector Gateway default schema fields
description: The default schema for Custom Connector Gateway external content connectors includes predefined fields to store content item metadata. Use these fields in requests your custom connector sends to the Custom Connector Gateway API endpoint.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/custom-connector-gateway-default-schema-fields.html
release: australia
product: Search Administration
classification: search-administration
topic_type: reference
last_updated: "2026-10-20"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Custom Connector Gateway external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Custom Connector Gateway default schema fields

The default schema for Custom Connector Gateway external content connectors includes predefined fields to store content item metadata. Use these fields in requests your custom connector sends to the Custom Connector Gateway API endpoint.

|Field name|Type|
|----------|----|
|author\_id|string|
|author\_name|string|
|breadcrumb\_names|string|
|breadcrumb\_urls|string|
|contributor\_ids|string|
|contributor\_names|string|
|created\_on|glide\_date\_time|
|file\_extension|string|
|file\_type|string|
|item\_type|string|
|keywords|string|
|languages|string|
|mime\_type|string|
|modified\_on|glide\_date\_time|
|preview\_url|url|
|source\_name|string|
|source\_type|string|
|source\_url|url|

All fields in the Custom Connector Gateway schema are optional and can be fed selectively. Your custom connector doesn't have to populate every field when submitting ADDDOCUMENT or TOUCHDOCUMENT requests to the API endpoint on the ingest gateway host. The only fields required in the request payload are the **title** and **url** fields from the parent schema. Include only the Custom Connector Gateway schema fields you actually need to add or update.

**Note:** All Custom Connector Gateway external content connectors on your instance share a single schema. When making changes to the Custom Connector Gateway schema for a new connector, check that those changes don't affect the behavior of your existing Custom Connector Gateway connectors.

**Parent Topic:**[Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/custom-connector-gateway-external-content-connector.md)

