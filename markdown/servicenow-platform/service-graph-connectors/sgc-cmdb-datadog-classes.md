---
title: CMDB classes targeted in Service Graph Connector for Observability - Datadog
description: When you complete setting up the connection, the data is automatically pulled from Datadog. The data is saved in target tables.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Observability-Datadog, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Observability - Datadog

When you complete setting up the connection, the data is automatically pulled from Datadog. The data is saved in target tables.

## Cloud DataBase \[cmdb\_ci\_cloud\_database\]

The following attributes in the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|
|Fully qualified domain name|fqdn|
|Name|name|
|Type|type|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

The following attributes in the Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Reference|Key Value \[cmdb\_key\_value\]|

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Account Id|account\_id|
|Name|name|
|Object ID|object\_id|
|Datacenter Type|datacenter\_type|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Nic|nic|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|

## Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]

The following attributes in the Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Region|region|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Configuration Item|cmdb\_ci|
|MAC Address|mac\_address|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Server \[cmdb\_ci\_server\]|

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|CPU core thread|cpu\_core\_thread|
|CPU count|cpu\_count|
|CPU speed \(MHz\)|cpu\_speed|
|CPU type|cpu\_type|
|Disk space \(GB\)|disk\_space|
|DNS Domain|dns\_domain|
|Fully qualified domain name|fqdn|
|Name|name|
|Operating System|os|
|RAM \(MB\)|ram|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Server \[cmdb\_ci\_server\]|Reference|Key Value \[cmdb\_key\_value\]|

**Related topics**  


[Service Graph Connector for Observability - Datadog](../concept/sgc-cmdb-integration-datadog.md)

