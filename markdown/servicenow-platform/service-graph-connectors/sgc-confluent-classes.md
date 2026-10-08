---
title: CMDB classes targeted in Service Graph Connector for Confluent
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Confluent. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-confluent-classes.html
release: brazil
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Confluent, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Confluent

When you complete setting up the connection, you can configure the integration to periodically pull data from Confluent. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Kafka Topic \[cmdb\_ci\_appl\_kafka\_topic\]

The following attributes in the Kafka Topic \[cmdb\_ci\_appl\_kafka\_topic\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Operational Status|operational\_status|
|Replication Factor|replication\_factor|
|Name|name|
|Life Cycle Stage|life\_cycle\_stage|
|Partition Count|partition\_count|
|Topic Id|topic\_id|
|Life Cycle Stage Status|life\_cycle\_stage\_status|

## Confluent Organization \[cmdb\_ci\_confluent\_organization\]

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|cmdb\_ci\_confluent\_organization|Contains::Contained by|cmdb\_ci\_confluent\_env|

## Confluent Environment \[cmdb\_ci\_confluent\_env\]

The following attributes in the Confluent Environment \[cmdb\_ci\_confluent\_env\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object Id|object\_id|
|Name|name|
|Env Creation Date|env\_creation\_date|
|Life Cycle Stage|life\_cycle\_stage|
|Env Last Updated Date|env\_last\_updated\_date|
|Life Cycle Stage Status|life\_cycle\_stage\_status|
|Operational Status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|cmdb\_ci\_confluent\_env|Contains::Contained by|cmdb\_ci\_kafka\_cluster|

## Kafka Cluster \[cmdb\_ci\_kafka\_cluster\]

The following attributes in the Kafka Cluster \[cmdb\_ci\_kafka\_cluster\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Life Cycle Stage Status|life\_cycle\_stage\_status|
|Http Endpoint|http\_endpoint|
|Name|name|
|Bootstrap Endpoint|bootstrap\_endpoint|
|Operational Status|operational\_status|
|Life Cycle Stage|life\_cycle\_stage|
|Environment|environment|
|Cluster Status|cluster\_status|
|Cluster Creation Date|cluster\_creation\_date|
|Cloud Region|cloud\_region|
|Cluster Id|cluster\_id|
|Cloud Provider|cloud\_provider|
|Cluster Last Update Date|cluster\_last\_update\_date|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|cmdb\_ci\_kafka\_cluster|Provides::Provided by|cmdb\_ci\_appl\_kafka\_topic|

## Confluent Organization \[cmdb\_ci\_confluent\_org\]

The following attributes in the Confluent Organization \[cmdb\_ci\_confluent\_org\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Org Creation Date|org\_creation\_date|
|Org Last Updated Date|org\_last\_updated\_date|
|Object Id|object\_id|
|Operational Status|operational\_status|
|Life Cycle Stage|life\_cycle\_stage|
|Life Cycle Stage Status|life\_cycle\_stage\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|cmdb\_ci\_confluent\_org|Contains::Contained by|cmdb\_ci\_confluent\_env|

