---
title: Target tables for storing API Service Graph Connector for Kong Konnect data
description: When you complete setting up the connection, you can configure the integration to periodically pull data from a Kong Konnect application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Kong Konnect, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Target tables for storing API Service Graph Connector for Kong Konnect data

When you complete setting up the connection, you can configure the integration to periodically pull data from a Kong Konnect application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB tables.

## Kong Gateway \[cmdb\_ci\_kong\_gateway\]

The following attributes in the Kong Gateway \[cmdb\_ci\_kong\_gateway\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Asset tag|asset\_tag|
|Correlation ID|correlation\_id|
|Description|short\_description|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Provides::Provided by|Kong Load Balancer \[cmdb\_ci\_kong\_lb\]|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Provides::Provided by|Managed API \[cmdb\_ci\_managed\_api\]|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Uses::Used by|DNS Alias \[cmdb\_ci\_dns\_alias\]|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Reference|Key Value \[cmdb\_key\_value\]|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Reference|API Consumer \[api\_consumer\]|

## Kong Data Plane Node \[sn\_kong\_konnect\_kong\_data\_plane\_node\]

The following attributes in the Kong Data Plane Node \[sn\_kong\_konnect\_kong\_data\_plane\_node\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Hostname|hostname|
|Version|version|
|id|ID|
|Connection Alias SysId|connectionaliassysid|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kong Data Plane Node \[sn\_kong\_konnect\_kong\_data\_plane\_node\]|Reference|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|

**Note:** This table is available within the API Service Graph Connector for Kong Konnect application \(sn\_kong\_konnect\) scope.

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Account Id|account\_id|
|Name|name|
|Datacenter Type|datacenter\_type|
|Operational status|operational\_status|

## Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]

The following attributes in the Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Region|region|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## DNS Alias \[cmdb\_ci\_dns\_alias\]

The following attributes in the DNS Alias \[cmdb\_ci\_dns\_alias\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Operational status|operational\_status|

## Kong Load Balancer \[cmdb\_ci\_kong\_lb\]

The following attributes in the Kong Load Balancer \[cmdb\_ci\_kong\_lb\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Algorithm|algorithm|
|Description|short\_description|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Kong Load Balancer \[cmdb\_ci\_kong\_lb\]|Contains::Contained by|Kong Target \[cmdb\_ci\_kong\_target\]|

## Kong Target \[cmdb\_ci\_kong\_target\]

The following attributes in the Kong Target \[cmdb\_ci\_kong\_target\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Description|short\_description|
|Name|name|
|Operational status|operational\_status|
|Target|target|

## Managed API \[cmdb\_ci\_managed\_api\]

The following attributes in the Managed API \[cmdb\_ci\_managed\_api\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Base URL|base\_url|
|Description|short\_description|
|Operational status|operational\_status|
|Life Cycle Stage Status|life\_cycle\_stage\_status|
|Life Cycle Stage|life\_cycle\_stage|
|Type|type|

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
|Description|short\_description|
|Name|name|
|Operational status|operational\_status|
|Protocol|protocol|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Frontend \[cmdb\_ci\_api\_frontend\]|Use End Point To::Use End Point From|API Backend \[cmdb\_ci\_api\_backend\]|

## API Consumer \[api\_consumer\]

The following attributes in the API Consumer \[api\_consumer\] table are populated by collected data:

<table id="table_iyx_ddb_vgc"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th></tr></thead><tbody><tr><td>

ID

</td><td>

id

</td></tr><tr><td>

Custom ID

</td><td>

custom\_id

</td></tr><tr><td>

Email**Note:** Fetched using the Developers data source only.

</td><td>

email

</td></tr><tr><td>

Username

</td><td>

username

</td></tr><tr><td>

API Gateway

</td><td>

api\_gateway

</td></tr></tbody>
</table>|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Consumer \[api\_consumer\]|Reference|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|

## API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]

The following attributes in the API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Operational status|operational\_status|
|API Consumer|api\_consumer|
|ID|id|
|Creation Date|creation\_date|
|Description|short\_description|
|Last Modified Date|last\_modified\_date|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Gateway \[cmdb\_ci\_api\_gateway\]|Provides::Provided by|API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]|

## API Consumer Access \[api\_consumer\_access\]

The following attributes in the API Consumer Access \[api\_consumer\_access\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|API|api|
|API Consumer|api\_consumer|
|State|state|
|API Consumer Subscription|api\_consumer\_subscription|

## API Policy \[api\_policy\]

The following attributes in the API Policy \[api\_policy\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Managed API|managed\_api|
|ID|id|
|Protocols|protocols|
|Frontend|frontend|
|Active|active|
|Consumer|consumer|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Policy \[api\_policy\]|Reference|Managed API \[cmdb\_ci\_managed\_api\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Tag|tag|
|Configuration item|configuration\_item|
|Key|key|
|Value|value|

