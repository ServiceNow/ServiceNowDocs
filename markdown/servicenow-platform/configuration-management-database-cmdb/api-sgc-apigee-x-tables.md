---
title: Target tables for storing API Service Graph Connector for Apigee X data
description: When you complete setting up the connection, you can configure the integration to periodically pull data from an Apigee X application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 4
breadcrumb: [Apigee X, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Target tables for storing API Service Graph Connector for Apigee X data

When you complete setting up the connection, you can configure the integration to periodically pull data from an Apigee X application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.

## Google Organization Project \[cmdb\_ci\_gcp\_project\]

The following attributes in the Google Organization Project \[cmdb\_ci\_gcp\_project\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Parent|parent\_ci|
|Name|name|
|Object ID|object\_id|
|Install Status|install\_status|
|Operational status|operational\_status|
|Parent Id|parent\_id|
|Parent Type|parent\_type|
|Project Id|project\_id|
|Time|time|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Google Organization Project \[cmdb\_ci\_gcp\_project\]|Reference|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|
|Google Organization Project \[cmdb\_ci\_gcp\_project\]|Reference|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|
|Google Organization Project \[cmdb\_ci\_gcp\_project\]|Contains::Contained by|Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]|

## Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]

The following attributes in the Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Install Status|install\_status|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|APIgee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]|Provides::Provided by|Managed API \[cmdb\_ci\_managed\_api\]|
|APIgee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]|Reference|API Consumer \[api\_consumer\]|
|Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]|Provides::Provided by|API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]|
|Apigee API Gateway \[cmdb\_ci\_apigee\_api\_gateway\]|Provides::Provided by|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|

## Managed API \[cmdb\_ci\_managed\_api\]

The following attributes in the Managed API \[cmdb\_ci\_managed\_api\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Description|short\_description|
|Life Cycle Stage|life\_cycle\_stage|
|ID|id|
|Name|name|
|Version|version|
|Base URL|base\_url|
|Model ID|model\_id|
|Correlation ID|correlation\_id|
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

## API Consumer \[api\_consumer\]

The following attributes in the API Consumer \[api\_consumer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|API Gateway|api\_gateway|
|Custom ID|custom\_id|
|Email|email|
|Registration Date|registration\_date|
|Username|username|

## API Frontend \[cmdb\_ci\_api\_frontend\]

The following attributes in the API Frontend \[cmdb\_ci\_api\_frontend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|API Version|api\_version|
|Host|host|
|Method|method|
|Path|path|
|URL|url|
|Description|short\_description|
|Name|name|
|Operational status|operational\_status|
|Protocol|protocol|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Frontend \[cmdb\_ci\_api\_frontend\]|Use End Point To::Use End Point From|API Backend \[cmdb\_ci\_api\_backend\]|

## API Backend \[cmdb\_ci\_api\_backend\]

The following attributes in the API Backend \[cmdb\_ci\_api\_backend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|URL|url|
|Name|name|
|Operational status|operational\_status|
|Type|type|

## API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]

The following attributes in the API Product Bundle \[cmdb\_ci\_api\_product\_bundle\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Creation Date|creation\_date|
|Description|short\_description|
|Discovered Access Type|discovered\_access\_type|
|Discovered Approval Type|discovered\_approval\_type|
|Last Modified Date|last\_modified\_date|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|Contains::Contained by|API \[cmdb\_ci\_api\]|
|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|Used by::Uses|API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]|
|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|Reference|Key Value \[cmdb\_key\_value\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Tag|tag|
|Configuration item|configuration\_item|
|Key|key|
|Value|value|

## API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]

The following attributes in the API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Creation Date|creation\_date|
|API Consumer|api\_consumer|
|Discovered State|discovered\_state|
|Last Modified Date|last\_modified\_date|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]|Reference|Key Value \[cmdb\_key\_value\]|

## API Consumer Access \[api\_consumer\_access\]

The following attributes in the API Consumer Access \[api\_consumer\_access\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Auth Method|access\_type|
|State|state|
|Valid to|valid\_to|
|API Product Bundle|api\_product\_bundle|
|API Consumer Subscription|api\_consumer\_subscription|
|API|api|
|API Consumer|api\_consumer|

## Cloud Organizations \[cmdb\_ci\_cloud\_org\]

The following attributes in the Cloud Organizations \[cmdb\_ci\_cloud\_org\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|
|Install Status|install\_status|
|Name|name|
|Operational status|operational\_status|
|Time|time|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|Contains::Contained by|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|

## Google Organization Folder \[cmdb\_ci\_gcp\_folder\]

The following attributes in the Google Organization Folder \[cmdb\_ci\_gcp\_folder\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Parent|parent\_ci|
|Object ID|object\_id|
|Install Status|install\_status|
|Name|name|
|Operational status|operational\_status|
|Parent Id|parent\_id|
|Parent Type|parent\_type|
|Time|time|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|Reference|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|
|Google Organization Folder \[cmdb\_ci\_gcp\_folder\]|Reference|Cloud Organizations \[cmdb\_ci\_cloud\_org\]|

## DNS Alias \[cmdb\_ci\_dns\_alias\]

The following attributes in the DNS Alias \[cmdb\_ci\_dns\_alias\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Operational status|operational\_status|

