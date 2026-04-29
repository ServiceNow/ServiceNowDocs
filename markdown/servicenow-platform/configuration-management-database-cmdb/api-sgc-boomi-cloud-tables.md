---
title: Target tables for storing API Service Graph Connector for Boomi Cloud API Management data
description: When you complete setting up the connection, you can configure the integration to periodically pull data from a Boomi Cloud API Management application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Boomi Cloud API Management, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Target tables for storing API Service Graph Connector for Boomi Cloud API Management data

When you complete setting up the connection, you can configure the integration to periodically pull data from a Boomi Cloud API Management application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.

## Boomi API Gateway \[cmdb\_ci\_boomi\_api\_gateway\]

The following attributes in the Boomi API Gateway \[cmdb\_ci\_boomi\_api\_gateway\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Boomi API Gateway \[cmdb\_ci\_boomi\_api\_gateway\]|Provides::Provided by|Managed API \[cmdb\_ci\_managed\_api\]|
|Boomi API Gateway \[cmdb\_ci\_boomi\_api\_gateway\]|Reference|API Consumer \[api\_consumer\]|

## Managed API \[cmdb\_ci\_managed\_api\]

The following attributes in the Managed API \[cmdb\_ci\_managed\_api\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Life Cycle Stage|life\_cycle\_stage|
|Name|name|
|Life Cycle Stage Status|life\_cycle\_stage\_status|
|ID|id|
|Version|version|
|Base URL|base\_url|
|Description|short\_description|
|Operational status|operational\_status|
|Model ID|model\_id|
|Type|type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|API Backend \[cmdb\_ci\_api\_backend\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|API Frontend \[cmdb\_ci\_api\_frontend\]|

## API Frontend \[cmdb\_ci\_api\_frontend\]

The following attributes in the API Frontend \[cmdb\_ci\_api\_frontend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Method|method|
|Host|host|
|Path|path|
|URL|url|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Frontend \[cmdb\_ci\_api\_frontend\]|Use End Point To::Use End Point From|API Backend \[cmdb\_ci\_api\_backend\]|

## API Backend \[cmdb\_ci\_api\_backend\]

The following attribute in the API Backend \[cmdb\_ci\_api\_backend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|URL|url|
|Path|path|
|Host|host|
|Type|type|
|Operational status|operational\_status|

## API Consumer \[api\_consumer\]

The following attributes in the API Consumer \[api\_consumer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|API Consumer Type|api\_consumer\_type|
|Email|email|
|API Gateway|api\_gateway|
|Registration Date|registration\_date|
|Username|username|

