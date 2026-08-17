---
title: Target tables for storing API Service Graph Connector for Apigee Edge data
description: When you complete setting up the connection, you can configure the integration to periodically pull data from an Apigee Edge application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/api-sgc-apigee-edge-tables.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-07-20"
reading_time_minutes: 3
breadcrumb: [Apigee Edge, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Target tables for storing API Service Graph Connector for Apigee Edge data

When you complete setting up the connection, you can configure the integration to periodically pull data from an Apigee Edge application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.

## Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]

The following attributes in the Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]|Provides::Provided by|Managed API \[cmdb\_ci\_managed\_api\]|
|Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]|Reference|API Consumer \[api\_consumer\]|
|Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]|Provides::Provided by|API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]|
|Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]|Provides::Provided by|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|

## Managed API \[cmdb\_ci\_managed\_api\]

The following attributes in the Managed API \[cmdb\_ci\_managed\_api\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Description|short\_description|
|Base URL|base\_url|
|Version|version|
|Type|type|
|Environment|environment|
|Model ID|model\_id|
|Correlation ID|correlation\_id|
|Life Cycle Stage|life\_cycle\_stage|
|Life Cycle Stage Status|life\_cycle\_stage\_status|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|API Frontend \[cmdb\_ci\_api\_frontend\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|API Backend \[cmdb\_ci\_api\_backend\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Reference|API Deployment \[api\_deployment\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|DNS Alias \[cmdb\_ci\_dns\_alias\]|

## API Deployment \[api\_deployment\]

The following attributes in the API Deployment \[api\_deployment\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|API|api|
|Name|name|

## DNS Alias \[cmdb\_ci\_dns\_alias\]

The following attributes in the DNS Alias \[cmdb\_ci\_dns\_alias\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Operational status|operational\_status|

## API Backend \[cmdb\_ci\_api\_backend\]

The following attributes in the API Backend \[cmdb\_ci\_api\_backend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|URL|url|
|Type|type|
|Internet facing|internet\_facing|
|Operational status|operational\_status|

## API Frontend \[cmdb\_ci\_api\_frontend\]

The following attributes in the API Frontend \[cmdb\_ci\_api\_frontend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|API Version|api\_version|
|Host|host|
|Method|method|
|Path|path|
|URL|url|
|Protocol|protocol|
|Description|short\_description|
|Internet facing|internet\_facing|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Frontend \[cmdb\_ci\_api\_frontend\]|Use End Point To::Use End Point From|API Backend \[cmdb\_ci\_api\_backend\]|

## API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]

The following attributes in the API Product Bundle \[cmdb\_ci\_api\_product\_bundle\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Description|short\_description|
|Creation Date|creation\_date|
|Last Modified Date|last\_modified\_date|
|Discovered Access Type|discovered\_access\_type|
|Discovered Approval Type|discovered\_approval\_type|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|Contains::Contained by|Managed API \[cmdb\_ci\_managed\_api\]|
|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|Used by::Uses|API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]|
|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|Reference|Key Value \[cmdb\_key\_value\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Configuration item|configuration\_item|
|Key|key|
|Value|value|
|Tag|tag|

## API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]

The following attributes in the API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|API Consumer|api\_consumer|
|Creation Date|creation\_date|
|Last Modified Date|last\_modified\_date|
|Discovered State|discovered\_state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]|Reference|Key Value \[cmdb\_key\_value\]|

## API \[cmdb\_ci\_api\]

The following attribute in the API \[cmdb\_ci\_api\] table is populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Correlation ID|source\_native\_key|

## API Consumer Access \[api\_consumer\_access\]

The following attributes in the API Consumer Access \[api\_consumer\_access\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Auth Method|access\_type|
|State|state|
|Valid to|valid\_to|
|API|api|
|API Consumer|api\_consumer|
|API Product Bundle|api\_product\_bundle|
|API Consumer Subscription|api\_consumer\_subscription|

## API Consumer \[api\_consumer\]

The following attributes in the API Consumer \[api\_consumer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Username|username|
|Email|email|
|API Gateway|api\_gateway|
|Registration Date|registration\_date|
|Discovered State|discovered\_state|

