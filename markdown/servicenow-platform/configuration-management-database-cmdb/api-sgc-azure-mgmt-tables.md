---
title: Target tables for storing API Service Graph Connector for Azure API Management data
description: When you complete setting up the connection, you can configure the integration to periodically pull data from an Azure API Management application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB classes.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-05-01"
reading_time_minutes: 3
breadcrumb: [Azure API Management, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Target tables for storing API Service Graph Connector for Azure API Management data

When you complete setting up the connection, you can configure the integration to periodically pull data from an Azure API Management application. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB classes.

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Account Id|account\_id|
|Name|name|
|Object ID|object\_id|
|Datacenter Type|datacenter\_type|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Contains::Contained by|Resource Group \[cmdb\_ci\_resource\_group\]|

## Azure Subscription \[cmdb\_ci\_azure\_subscription\]

The following attributes in the Azure Subscription \[cmdb\_ci\_azure\_subscription\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|

## Azure API Management \[cmdb\_ci\_azure\_api\_mgmt\]

The following attributes in the Azure API Management \[cmdb\_ci\_azure\_api\_mgmt\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Fully qualified domain name|fqdn|
|Gateway URL|gateway\_url|
|Operational status|operational\_status|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Azure API Management \[cmdb\_ci\_azure\_api\_mgmt\]|Provides::Provided by|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|
|Azure API Management \[cmdb\_ci\_azure\_api\_mgmt\]|Provides::Provided by|API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]|
|Azure API Management \[cmdb\_ci\_azure\_api\_mgmt\]|Uses::Used by|DNS Alias \[cmdb\_ci\_dns\_alias\]|
|Azure API Management \[cmdb\_ci\_azure\_api\_mgmt\]|Provides::Provided by|Managed API \[cmdb\_ci\_managed\_api\]|
|Azure API Management \[cmdb\_ci\_azure\_api\_mgmt\]|Reference|API Consumer \[api\_consumer\]|

## Resource Group \[cmdb\_ci\_resource\_group\]

The following attributes in the Resource Group \[cmdb\_ci\_resource\_group\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Operational status|operational\_status|

## DNS Alias \[cmdb\_ci\_dns\_alias\]

The following attributes in the DNS Alias \[cmdb\_ci\_dns\_alias\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|

## Managed API \[cmdb\_ci\_managed\_api\]

The following attributes in the Managed API \[cmdb\_ci\_managed\_api\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Minor Version|minor\_version|
|Name|name|
|Version|version|
|Base URL|base\_url|
|Correlation ID|correlation\_id|
|Description|short\_description|
|Fully qualified domain name|fqdn|
|Operational status|operational\_status|
|Type|type|
|Life Cycle Stage Status|life\_cycle\_stage\_status|
|Life Cycle Stage|life\_cycle\_stage|
|Model ID|model\_id|

<table id="table_epm_2fg_4bc"><thead><tr><th>

Parent class

</th><th>

Relationship type

</th><th>

Child class

</th></tr></thead><tbody><tr><td>

Managed API \[cmdb\_ci\_managed\_api\]

</td><td>

Uses::Used by

</td><td>

API Frontend \[cmdb\_ci\_api\_frontend\]

</td></tr><tr><td>

Managed API \[cmdb\_ci\_managed\_api\]

</td><td>

Uses::Used by

</td><td>

API Backend \[cmdb\_ci\_api\_backend\]

</td></tr><tr><td>

Managed API \[cmdb\_ci\_managed\_api\]

</td><td>

Uses::Used by

</td><td>

API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]**Note:** Applies only when the Discovered Scope \[discovered\_scope\] attribute value is set to `api`.

</td></tr></tbody>
</table>## API Frontend \[cmdb\_ci\_api\_frontend\]

The following attributes in the API Frontend \[cmdb\_ci\_api\_frontend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|API Minor Version|api\_minor\_version|
|API Version|api\_version|
|Host|host|
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

<table id="table_cgq_3jj_dxb"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th></tr></thead><tbody><tr><td>

Host

</td><td>

host

</td></tr><tr><td>

ID

</td><td>

id**Note:** Applicable to GraphQL APIs only.

</td></tr><tr><td>

Method

</td><td>

method**Note:** Applicable to GraphQL APIs only.

</td></tr><tr><td>

Path

</td><td>

path

</td></tr><tr><td>

URL

</td><td>

url

</td></tr><tr><td>

Name

</td><td>

name

</td></tr><tr><td>

Operational status

</td><td>

operational\_status

</td></tr></tbody>
</table>## API Consumer \[api\_consumer\]

The following attributes in the API Consumer \[api\_consumer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Discovered State|discovered\_state|
|Email|email|
|Provider|provider|
|Registration Date|registration\_date|
|Username|username|

## API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]

The following attributes in the API Product Bundle \[cmdb\_ci\_api\_product\_bundle\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Discovered Access Type|discovered\_access\_type|
|Discovered Approval Type|discovered\_approval\_type|
|Discovered State|discovered\_state|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|Contains::Contained by|Managed API \[cmdb\_ci\_managed\_api\]|
|API Product Bundle \[cmdb\_ci\_api\_product\_bundle\]|Used by::Uses|API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]|

## API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]

The following attributes in the API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Creation Date|creation\_date|
|Discovered Scope|discovered\_scope|
|Name|name|
|Sys ID|sys\_id|
|API Consumer|api\_consumer|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|API Consumer Subscription \[cmdb\_ci\_api\_consumer\_subscription\]|Reference|API Consumer Access \[api\_consumer\_access\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|

## API Consumer Access \[api\_consumer\_access\]

The following attributes in the API Consumer Access \[api\_consumer\_access\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|API Consumer|api\_consumer|
|Access type|access\_type|
|API Product Bundle|api\_product\_bundle|
|State|state|
|API Consumer Subscription|api\_consumer\_subscription|
|API|api|
|Valid to|valid\_to|

