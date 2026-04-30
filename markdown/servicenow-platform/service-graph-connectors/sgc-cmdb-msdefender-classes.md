---
title: CMDB classes targeted in Service Graph Connector for Microsoft Defender Endpoint
description: When you complete setting up the connection, you can configure the integration to pull data periodically from machines utilizing the Microsoft Defender for Endpoint security solution. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Microsoft Defender for Endpoint, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Microsoft Defender Endpoint

When you complete setting up the connection, you can configure the integration to pull data periodically from machines utilizing the Microsoft Defender for Endpoint security solution. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|Discovery source|discovery\_source|
|Install Status|install\_status|
|Name|name|
|Operating System|os|
|OS Version|os\_version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Computer \[cmdb\_ci\_computer\]|Reference|SG-Defender Machines Related \[sn\_defender\_integ\_sg\_defender\_machines\_related\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|IP Address|ip\_address|
|IP version|ip\_version|
|Name|name|
|Nic|nic|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## SG-Defender Machines Related \[sn\_defender\_integ\_sg\_defender\_machines\_related\]

The following attributes in the SG-Defender Machines Related \[sn\_defender\_integ\_sg\_defender\_machines\_related\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Agent Version|agent\_version|
|Device Id|device\_id|
|Exposure Level|exposure\_level|
|First Seen|first\_seen\_date|
|Health Status|health\_status|
|IsAadJoined|isaadjoined|
|Last Reported|last\_reported|
|Managed by|managed\_by|
|Onboarding Status|onboarding\_status|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Discovery source|discovery\_source|
|Install Status|install\_status|
|MAC Address|mac\_address|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Server \[cmdb\_ci\_server\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data when the Software Asset Management \(SAM\) application isn't installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Name|name|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data when the SAM application is installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Discovery source|discovery\_source|
|Display name|display\_name|
|Version|version|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data when the SAM application isn't installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Installed on|installed\_on|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Server \[cmdb\_ci\_server\]|

## Windows Server \[cmdb\_ci\_win\_server\]

The following attributes in the Windows Server \[cmdb\_ci\_win\_server\] table are populated by collected data when the SAM application isn't installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|Discovery source|discovery\_source|
|Install Status|install\_status|
|Name|name|
|Operating System|os|
|OS Version|os\_version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Windows Server \[cmdb\_ci\_win\_server\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Windows Server \[cmdb\_ci\_win\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Windows Server \[cmdb\_ci\_win\_server\]|Reference|SG-Defender Machines Related \[sn\_defender\_integ\_sg\_defender\_machines\_related\]|
|Windows Server \[cmdb\_ci\_win\_server\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|

