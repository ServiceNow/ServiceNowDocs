---
title: CMDB classes targeted in Service Graph Connector for ExtraHop
description: When you complete setting up the connection, you can configure the integration to periodically pull data from ExtraHop. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ExtraHop, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for ExtraHop

When you complete setting up the connection, you can configure the integration to periodically pull data from ExtraHop. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

**Important:** ServiceNow hosted Service Graph Connector for ExtraHop is now deprecated and no longer supported or available for new activation. ExtraHop hosted Service Graph Connector for ExtraHop provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

The following attributes in the Hardware \[cmdb\_ci\_hardware\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Manufacturer|manufacturer|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Hardware \[cmdb\_ci\_hardware\]|Receives data from::Sends data to|Hardware \[cmdb\_ci\_hardware\]|

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|IP version|ip\_version|
|Name|name|
|Nic|nic|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Configuration Item|cmdb\_ci|
|MAC Address|mac\_address|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

