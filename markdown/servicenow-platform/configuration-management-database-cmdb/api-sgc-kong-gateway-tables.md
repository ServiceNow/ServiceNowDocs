---
title: Target tables for storing API Service Graph Connector for Kong Gateway data
description: When you complete setting up the connection, you can configure the integration to periodically pull data from a Kong Gateway application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-10-16"
reading_time_minutes: 3
breadcrumb: [Kong Gateway, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Target tables for storing API Service Graph Connector for Kong Gateway data

When you complete setting up the connection, you can configure the integration to periodically pull data from a Kong Gateway application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.

## Kong Gateway \[cmdb\_ci\_kong\_gateway\]

The following attributes in the Kong Gateway \[cmdb\_ci\_kong\_gateway\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Admin URL|admin\_url|
|Database|database|
|Description|short\_description|
|Operational status|operational\_status|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Provides::Provided by|Kong Load Balancer \[cmdb\_ci\_kong\_lb\]|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Provides::Provided by|Managed API \[cmdb\_ci\_managed\_api\]|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Reference|Kong Workspace \[kong\_workspace\]|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Reference|API Policy \[api\_policy\]|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Reference|API Consumer \[api\_consumer\]|

## Kong Workspace \[kong\_workspace\]

The following attributes in the Kong Workspace \[kong\_workspace\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|API Gateway|api\_gateway|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kong Workspace \[kong\_workspace\]|Reference|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|

## Kong Load Balancer \[cmdb\_ci\_kong\_lb\]

The following attributes in the Kong Load Balancer \[cmdb\_ci\_kong\_lb\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Algorithm|algorithm|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kong Load Balancer \[cmdb\_ci\_kong\_lb\]|Contains::Contained by|Kong Target \[cmdb\_ci\_kong\_target\]|
|Kong Load Balancer \[cmdb\_ci\_kong\_lb\]|Reference|Key Value \[cmdb\_key\_value\]|

## Kong Target \[cmdb\_ci\_kong\_target\]

The following attributes in the Kong Target \[cmdb\_ci\_kong\_target\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Target|target|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kong Target \[cmdb\_ci\_kong\_target\]|Reference|Key Value \[cmdb\_key\_value\]|

## Managed API \[cmdb\_ci\_managed\_api\]

The following attributes in the Managed API \[cmdb\_ci\_managed\_api\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Life Cycle Stage|life\_cycle\_stage|
|Life Cycle Stage Status|life\_cycle\_stage\_status|
|ID|id|
|Name|name|
|Base URL|base\_url|
|Type|type|
|Model ID|model\_id|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|API Frontend \[cmdb\_ci\_api\_frontend\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|API Backend \[cmdb\_ci\_api\_backend\]|

## API Backend \[cmdb\_ci\_api\_backend\]

The following attributes in the API Backend \[cmdb\_ci\_api\_backend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Host|host|
|ID|id|
|Path|path|
|URL|url|
|Name|name|
|Port|port|
|Protocol|protocol|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Backend \[cmdb\_ci\_api\_backend\]|Uses::Used by|Kong Load Balancer \[cmdb\_ci\_kong\_lb\]|

## API Frontend \[cmdb\_ci\_api\_frontend\]

The following attributes in the API Frontend \[cmdb\_ci\_api\_frontend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Host|host|
|ID|id|
|Method|method|
|Path|path|
|URL|url|
|Name|name|
|Protocol|protocol|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Frontend \[cmdb\_ci\_api\_frontend\]|Use End Point To::Use End Point From|API Backend \[cmdb\_ci\_api\_backend\]|

## API Consumer \[api\_consumer\]

The following attributes in the API Consumer \[api\_consumer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|API Gateway|api\_gateway|
|Custom ID|custom\_id|
|Username|username|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Consumer \[api\_consumer\]|Reference|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|

## API Policy \[api\_policy\]

The following attributes in the API Policy \[api\_policy\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Frontend|frontend|
|ID|id|
|Active|active|
|Name|name|
|Protocols|protocols|
|Managed API|managed\_api|
|Consumer|consumer|
|API Gateway|api\_gateway|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Policy \[api\_policy\]|Reference|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Configuration item|configuration\_item|
|Key|key|
|Value|value|

