---
title: Oracle HCM \(Discovery\)
description: The Oracle HCM \(Discovery\) connector enables access to human capital management data from your Oracle HCM account without moving or copying data. Available tables and columns are discovered at runtime.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/oracle-hcm-discovery-zcc.html
release: australia
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [Oracle HCM Discovery connector, REST connector, zero-copy connector, human capital management, runtime discovery, data fabric]
breadcrumb: [Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Oracle HCM \(Discovery\)

The Oracle HCM \(Discovery\) connector enables access to human capital management data from your Oracle HCM account without moving or copying data. Available tables and columns are discovered at runtime.

Connection admins set up connections to Oracle HCM \(Discovery\) in the Zero Copy Connector Hub and grant data stewards access. Data stewards use the connection to create data fabric tables and map data from Oracle HCM. Users can then access Oracle HCM data through the table list view or GlideRecord scripts. For details, see [Managing data fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/managing-data-fabric-tables-zcc.md).

**Note:**

Oracle HCM \(Discovery\) is a **REST** connector. Before you set up this connection, review [REST connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rest-connectors.md) for prerequisites, authentication requirements, and API consumption considerations.

## Supported data types

|Oracle HCM \(Discovery\)|Data fabric table|
|------------------------|-----------------|
|varchar|String|
|bigint|Long|
|boolean|True/False|
|double|Floating Point Number|
|date|Date|
|timestamp \(3\)|Basic Date/Time|

## How Oracle HCM \(Discovery\) differs from Oracle HCM

Because Oracle HCM instances can have custom tables and column definitions, this connector does not rely solely on a fixed, built-in set of tables. Instead, it queries your Oracle HCM instance at runtime to discover which tables and columns are available. This is similar to how a JDBC-based connector discovers schema information from a database. Discovered metadata is cached to avoid repeating this discovery process for every query.

**Note:**

Oracle HCM \(Discovery\) is a separate connector from Oracle HCM. Choose Oracle HCM \(Discovery\) if you want the connector to detect available tables and columns directly from your Oracle HCM instance. This approach does not rely on a fixed, built-in set of tables.

**Related topics**  


[oracle-hcm-zcc]

[Create an Oracle HCM \(Discovery\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-oracle-hcm-discovery-connection-zcc.md)

