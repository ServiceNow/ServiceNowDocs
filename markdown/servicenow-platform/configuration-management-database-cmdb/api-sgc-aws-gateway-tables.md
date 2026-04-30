---
title: Target tables for storing API Service Graph Connector for AWS API Gateway data
description: When you complete setting up the connection, you can configure the integration to periodically pull data from an AWS API Gateway service. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB classes.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-01-20"
reading_time_minutes: 2
breadcrumb: [AWS API Gateway, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Target tables for storing API Service Graph Connector for AWS API Gateway data

When you complete setting up the connection, you can configure the integration to periodically pull data from an AWS API Gateway service. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] classes and other non-CMDB classes.

## AWS API Gateway \[cmdb\_ci\_aws\_api\_gateway\]

The following attributes in the AWS API Gateway \[cmdb\_ci\_aws\_api\_gateway\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|AWS API Gateway \[cmdb\_ci\_aws\_api\_gateway\]|Provides::Provided by|Managed API \[cmdb\_ci\_managed\_api\]|
|AWS API Gateway \[cmdb\_ci\_aws\_api\_gateway\]|Reference|API Policy \[api\_policy\]|
|AWS API Gateway \[cmdb\_ci\_aws\_api\_gateway\]|Reference|API Consumer \[api\_consumer\]|
|AWS API Gateway \[cmdb\_ci\_aws\_api\_gateway\]|Uses::Used by|DNS Alias \[cmdb\_ci\_dns\_alias\]|

## DNS Alias \[cmdb\_ci\_dns\_alias\]

The following attributes in the DNS Alias \[cmdb\_ci\_dns\_alias\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Operational status|operational\_status|

## Managed API \[cmdb\_ci\_managed\_api\]

The following attributes in the Managed API \[cmdb\_ci\_managed\_api\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Life Cycle Stage Status|life\_cycle\_stage\_status|
|ID|id|
|Name|name|
|Base URL|base\_url|
|Operational status|operational\_status|
|Life Cycle Stage|life\_cycle\_stage|
|Model ID|model\_id|
|Type|type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|API Frontend \[cmdb\_ci\_api\_frontend\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|API Backend \[cmdb\_ci\_api\_backend\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Reference|API Deployment \[api\_deployment\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Reference|Key Value \[cmdb\_key\_value\]|

## API Frontend \[cmdb\_ci\_api\_frontend\]

The following attributes in the API Frontend \[cmdb\_ci\_api\_frontend\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Host|host|
|Method|method|
|Path|path|
|URL|url|
|Authorization|authorization|
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
|ID|id|
|URL|url|
|Name|name|
|Operational status|operational\_status|
|Type|type|

## API Consumer \[api\_consumer\]

The following attributes in the API Consumer \[api\_consumer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ID|id|
|Username|username|
|API Gateway|api\_gateway|

## API Consumer Access \[api\_consumer\_access\]

The following attributes in the API Consumer Access \[api\_consumer\_access\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|API|api|
|API Consumer|api\_consumer|
|State|state|

## API Deployment \[api\_deployment\]

The following attributes in the API Deployment \[api\_deployment\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|API|api|

## API Policy \[api\_policy\]

The following attributes in the API Policy \[api\_policy\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Consumer|consumer|
|ID|id|
|Managed API|managed\_api|

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

