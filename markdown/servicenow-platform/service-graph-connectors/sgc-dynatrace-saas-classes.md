---
title: CMDB classes targeted in Service Graph Connector for Observability - Dynatrace SaaS
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Dynatrace. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-06-03"
reading_time_minutes: 3
breadcrumb: [Observability - Dynatrace SaaS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Observability - Dynatrace SaaS

When you complete setting up the connection, you can configure the integration to periodically pull data from Dynatrace. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

**Important:** The Service Graph Connector for Observability - Dynatrace SaaS is designed for the Dynatrace SaaS \(3rd‑generation\) platform and leverages DQL-based APIs and the Grail architecture to import data from Dynatrace into the CMDB. If you're in a Dynatrace managed \(self‑hosted\) or legacy SaaS environment, you should use the Service Graph Connector for Observability - Dynatrace.

## Application \[cmdb\_ci\_appl\]

The following attributes in the Application \[cmdb\_ci\_appl\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|Configuration file|config\_file|
|Installation directory|install\_directory|
|Name|name|
|Operational status|operational\_status|
|Running process command|running\_process\_command|
|Running process key parameters|running\_process key parameters|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Application \[cmdb\_ci\_appl\]|Runs on::Runs|Computer \[cmdb\_ci\_computer\]|
|Application \[cmdb\_ci\_appl\]|Reference|Key value \[cmdb\_key\_value\]|

**Note:** Based on the Discovery Process Classifications list, the tables that extend the Application \[cmdb\_ci\_appl\] table are populated by the SGO-Dynatrace SaaS Processes \[sn\_dynatrace\_saas\_sgo\_dynatrace\_saas\_processes\] data source.

## Calculated Application Service \[cmdb\_ci\_service\_calculated\]

The following attributes in the Calculated Application Service \[cmdb\_ci\_service\_calculated\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Correlation ID|correlation\_id|
|Hide from dashboard|hide\_from\_dashboard|
|Metadata|metadata|
|Most recent discovery|last\_discovered|
|Name|name|
|Operational status|operational\_status|
|Service Populator|service\_populator|
|Service Populator Status|populator\_status|
|Service Type|type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Depends on::Used by|Configuration Item \[cmdb\_ci\]|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Runs on::Runs|Application \[cmdb\_ci\_appl\]|

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|CPU count|cpu\_count|
|CPU name|cpu\_name|
|DNS Domain|dns\_domain|
|Fully qualified domain name|fqdn|
|Is Virtual|virtual|
|MAC Address|mac\_address|
|Manufacturer|manufacturer|
|Model ID|model\_id|
|Most recent discovery|last\_discovered|
|Name|name|
|Operating System|os|
|OS Version|os\_version|
|RAM \(MB\)|ram|
|Serial number|serial\_number|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Key Value \[cmdb\_key\_value\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|IP version|ip\_version|
|Name|name|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|

## Serial Number \[cmdb\_serial\_number\]

The following attributes in the Serial Number \[cmdb\_serial\_number\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Serial Number|serial\_number|
|Serial Number Type|serial\_number\_type|
|Valid|valid|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Serial Number \[cmdb\_serial\_number\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data when the Software Asset Management \(SAM\) application isn't installed.

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Name|name|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data when the SAM application is installed.

|Attribute label|Attribute name|
|---------------|--------------|
|Discovery source|discovery\_source|
|Display name|display\_name|
|Installed on|installed\_on|
|Last scanned|last\_scanned|
|Publisher|publisher|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Installation \[cmdb\_sam\_sw\_install\]|Reference|Server \[cmdb\_ci\_server\]|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data when the SAM application isn't installed.

|Attribute label|Attribute name|
|---------------|--------------|
|Installed on|installed\_on|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|

