---
title: CMDB classes targeted in the Service Graph Connector for Rapid7
description: When you complete the guided setup, you can configure the integration to periodically pull data. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Rapid7, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in the Service Graph Connector for Rapid7

When you complete the guided setup, you can configure the integration to periodically pull data. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Hardware \[cmdb\_ci\_hardware\]

The following attributes in the Hardware \[cmdb\_ci\_hardware\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Correlation ID|correlation\_id|
|MAC Address|mac\_address|
|Install Status|install\_status|
|Operational Status|operational\_status|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|IP Address|ip\_address|
|Owned By Configuration Item|owned\_by\_cmdb\_ci|

## SGC Rapid7 Asset \[sn\_sec\_sgc\_rapid7\_sgc\_rapid7\_asset\]

The following attributes in the SGC Rapid7 Asset \[sn\_sec\_sgc\_rapid7\_sgc\_rapid7\_asset\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Assessed for policies|assessed\_for\_policies|
|Assessed for vulnerabilities|assessed\_for\_vulnerabilities|
|Configuration item|configuration\_item|
|Credential assessments|credential\_assessments|
|Critical vulnerabilities|critical\_vulnerabilities|
|Exploits|exploits|
|Last assessed for vulnerabilities|last\_assessed\_for\_vulnerabilities|
|Last scan end|last\_scan\_end|
|Last scan start|last\_scan\_start|
|Malware kits|malware\_kits|
|Moderate vulnerabilities|moderate\_vulnerabilities|
|New|new|
|OS architecture|os\_architecture|
|OS description|os\_description|
|OS family|os\_family|
|OS name|os\_name|
|OS system name|os\_system\_name|
|OS type|os\_type|
|OS vendor|os\_vendor|
|OS version|os\_version|
|Remediated|remediated|
|Risk score|risk\_score|
|Same|same|
|Severe vulnerabilities|severe\_vulnerabilities|
|Tags|tags|
|Total vulnerabilities|total\_vulnerabilities|
|Type|type|
|Unique identifiers|unique\_identifiers|
|Configuration item|configuration\_item|

## Relationships created for Hardware

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Hardware \[cmdb\_ci\_hardware\]|Reference|SGC Rapid7 Asset \[sn\_sec\_sgc\_rapid7\_sgc\_rapid7\_asset\]|

## Relationships created for IP Address

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Relationships created by SGC Rapid7 Asset

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|SGC Rapid7 Asset \[sn\_sec\_sgc\_rapid7\_sgc\_rapid7\_asset\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

