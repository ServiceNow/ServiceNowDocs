---
title: CMDB classes targeted in Service Graph Connector for Akamai API Security
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Akamai API Security. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-10-12"
reading_time_minutes: 1
breadcrumb: [Akamai API Security, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Akamai API Security

When you complete setting up the connection, you can configure the integration to periodically pull data from Akamai API Security. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## API Component \[cmdb\_ci\_api\_component\]

The following attributes in the API Component \[cmdb\_ci\_api\_component\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Host|host|
|Method|method|
|Path|path|
|URL|url|
|Attributes|attributes|
|Authorization|authorization|
|Correlation ID|correlation\_id|
|Internet Facing|internet\_facing|
|Name|name|
|Operational status|operational\_status|
|Product instance identifier|product\_instance\_id|
|Request Data Types|request\_data\_types|
|Response Data Types|response\_data\_types|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Component \[cmdb\_ci\_api\_component\]|Reference|Key Value \[cmdb\_key\_value\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|
|Configuration item|configuration\_item|

**Related topics**  


[Service Graph Connector for Akamai API Security](../concept/sgc-integration-akamai.md)

