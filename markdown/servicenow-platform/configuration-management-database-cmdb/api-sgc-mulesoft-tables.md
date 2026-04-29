---
title: Target tables for storing API Service Graph Connector for MuleSoft data
description: When you complete setting up the connection, you can configure the integration to periodically pull data from a MuleSoft Anypoint Platform application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MuleSoft, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Target tables for storing API Service Graph Connector for MuleSoft data

When you complete setting up the connection, you can configure the integration to periodically pull data from a MuleSoft Anypoint Platform application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.

## Anypoint API Gateway \[cmdb\_ci\_anypoint\_api\_gateway\]

The following attributes in the Anypoint API Gateway \[cmdb\_ci\_anypoint\_api\_gateway\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Anypoint API Gateway \[cmdb\_ci\_anypoint\_api\_gateway\]|Provides::Provided by|Managed API \[cmdb\_ci\_managed\_api\]|

## Managed API \[cmdb\_ci\_managed\_api\]

The following attributes in the Managed API \[cmdb\_ci\_managed\_api\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Version|version|
|Base URL|base\_url|
|Correlation ID|correlation\_id|
|Environment|environment|
|Type|type|
|Life Cycle Stage|life\_cycle\_stage|
|Description|short\_description|
|Model ID|model\_id|
|Operational status|operational\_status|
|Life Cycle Stage Status|life\_cycle\_stage\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|API Backend \[cmdb\_ci\_api\_backend\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|API Frontend \[cmdb\_ci\_api\_frontend\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Reference|API Deployment \[api\_deployment\]|

## API Frontend \[cmdb\_ci\_api\_frontend\]

The following attributes in the API Frontend \[cmdb\_ci\_api\_frontend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|API Minor Version|api\_minor\_version|
|API Version|api\_version|
|Host|host|
|ID|id|
|Method|method|
|Path|path|
|URL|url|
|Description|short\_description|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Frontend \[cmdb\_ci\_api\_frontend\]|Use End Point To::Use End Point From|API Backend \[cmdb\_ci\_api\_backend\]|

## API Backend \[cmdb\_ci\_api\_backend\]

The following attributes in the API Backend \[cmdb\_ci\_api\_backend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Host|host|
|Method|method|
|Path|path|
|URL|url|
|Name|name|
|Operational status|operational\_status|
|Type|type|

## API Deployment \[cmdb\_ci\_api\_deployment\]

The following attributes in the API Deployment \[cmdb\_ci\_api\_deployment\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|API|api|
|Name|name|

## Data Service Instance \[cmdb\_ci\_data\_service\_instance\]

The following attributes in the Data Service Instance \[cmdb\_ci\_data\_service\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Correlation ID|correlation\_id|
|Environment|environment|
|Operational status|operational\_status|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Configuration item|configuration\_item|
|Key|key|
|Value|value|
|Tag|tag|

