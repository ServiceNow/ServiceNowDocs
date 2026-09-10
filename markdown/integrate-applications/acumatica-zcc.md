---
title: Acumatica
description: The Acumatica connector enables access to ERP data from your Acumatica account without moving or copying data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/acumatica-zcc.html
release: australia
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [Acumatica connector, REST connector, zero-copy connector, ERP data, data fabric]
breadcrumb: [Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Acumatica

The Acumatica connector enables access to ERP data from your Acumatica account without moving or copying data.

Connection admins set up connections to Acumatica in the Zero Copy Connector Hub and grant data stewards access. Data stewards use the connection to create data fabric tables and map data from Acumatica. Users can then access Acumatica data through the table list view or GlideRecord scripts. For details, see [Managing data fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/managing-data-fabric-tables-zcc.md).

**Note:**

Acumatica is a **REST** connector. Before you set up this connection, review [REST connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rest-connectors.md)for prerequisites, authentication requirements, and API consumption considerations.

The Acumatica connector currently supports one table.

## Supported data types

|Acumatica|Data fabric table|
|---------|-----------------|
|varchar|String|
|integer|Integer|
|double|Floating Point Number|

**Related topics**  


[Create an Acumatica connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-acumatica-connection-zcc.md)

