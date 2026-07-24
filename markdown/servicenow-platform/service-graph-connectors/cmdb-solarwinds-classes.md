---
title: CMDB classes targeted in Service Graph Connector for SolarWinds
description: When you complete setting up the connection, you can configure the integration to periodically pull data from SolarWinds. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 6
breadcrumb: [SolarWinds, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for SolarWinds

When you complete setting up the connection, you can configure the integration to periodically pull data from SolarWinds. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Netmask|netmask|
|IP version|ip\_version|
|Nic|nic|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Install date|install\_date|
|Installed on|installed\_on|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|
|Software Instance \[cmdb\_software\_instance\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Availability Zone \[cmdb\_ci\_availability\_zone\]

The following attributes in the Availability Zone \[cmdb\_ci\_availability\_zone\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Network \[cmdb\_ci\_network\]|

## Cloud Key Pair \[cmdb\_ci\_cloud\_key\_pair\]

The following attributes in the Cloud Key Pair \[cmdb\_ci\_cloud\_key\_pair\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
| |source\_recency\_timestamp|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Key Pair \[cmdb\_ci\_cloud\_key\_pair\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Account Id|account\_id|
|Datacenter Type|datacenter\_type|
|Name|name|
|Object ID|object\_id|

## Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]

The following attributes in the Cloud Subnet \[cmdb\_ci\_cloud\_subnet\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
| |source\_recency\_timestamp|

## Compute Template \[cmdb\_ci\_compute\_template\]

The following attributes in the Hardware Type \[cmdb\_ci\_compute\_template\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
| |source\_recency\_timestamp|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosed on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|CPU core count|cpu\_core\_count|
|CPU core thread|cpu\_core\_thread|
|CPU manufacturer|cpu\_manufacturer|
|CPU name|cpu\_name|
|CPU speed \(MHz\)|cpu\_speed|
| |source\_recency\_timestamp|
|Is Virtual|virtual|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Computer \[cmdb\_ci\_computer\]|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|

## DB Mssql Database \[cmdb\_ci\_db\_mssql\_database\]

The following attributes in the MS SQL DataBase \[cmdb\_ci\_db\_mssql\_database\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Data Base|database|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|MS SQL DataBase \[cmdb\_ci\_db\_mssql\_database\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|

## DB Mssql Instance \[cmdb\_ci\_db\_mssql\_instance\]

The following attributes in the MSFT SQL Instance \[cmdb\_ci\_db\_mssql\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Edition|edition|
|Install Status|install\_status|
|Instance Name|instance\_name|
|Name|name|
|Operational status|operational\_status|
|Service pack|service\_pack|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|MSFT SQL Instance \[cmdb\_ci\_db\_mssql\_instance\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|
|MSFT SQL Instance \[cmdb\_ci\_db\_mssql\_instance\]|Contains::Contained by|MS SQL DataBase \[cmdb\_ci\_db\_mssql\_database\]|

## Disk \[cmdb\_ci\_disk\]

The following attributes in the Disk \[cmdb\_ci\_disk\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Device ID|device\_id|
|Disk space \(GB\)|disk\_space|
|Free disk space \(GB\)|free\_space|
|Manufacturer|manufacturer|
|Model ID|model\_id|
|Name|name|
|Size|size|
|Size bytes|size\_bytes|
| |source\_recency\_timestamp|
|Volume serial number|volume\_serial\_number|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Disk \[cmdb\_ci\_disk\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Hardware \[cmdb\_ci\_hardware\]

The following attributes in the Hardware \[cmdb\_ci\_hardware\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
| |cpu\_count|
|Default Gateway|default\_gateway|
|DNS Domain|dns\_domain|
|Fully qualified domain name|fqdn|
|Manufacturer|manufacturer|
|Model ID|model\_id|
|Name|name|
| |os|
| |os\_service\_pack|
| |os\_version|
| |ram|
|Serial number|serial\_number|
| |source\_recency\_timestamp|
|Class|sys\_class\_name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## IIS Virtual directory \[cmdb\_ci\_iisdirectory\]

The following attributes in the IIS Virtual Directory \[cmdb\_ci\_iisdirectory\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Alias|alias|
|Installation directory|install\_directory|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IIS Virtual Directory \[cmdb\_ci\_iisdirectory\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|IP version|ip\_version|
|Netmask|netmask|
||source\_recency\_timestamp|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]

The following attributes in the Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Region|region|
| |source\_recency\_timestamp|
|Class|sys\_class\_name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Microsoft IIS Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\]

The following attributes in the Microsoft IIS Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Name|name|
|Operational status|operational\_status|
|PID|pid|
|Running process command|running\_process\_command|
|Type|type|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Microsoft iis Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\]|Contains::Contained by|IIS Virtual Directory \[cmdb\_ci\_iisdirectory\]|
|Microsoft iis Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|

## Network \[cmdb\_ci\_network\]

The following attributes in the Cloud Network \[cmdb\_ci\_network\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
| |source\_recency\_timestamp|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|DHCP Enabled|dhcp\_enabled|
|MAC Address|mac\_address|
|Mac manufacturer|mac\_manufacturer|
|Name|name|
|Netmask|netmask|
| |source\_recency\_timestamp|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## OS Template \[cmdb\_ci\_os\_template\]

The following attributes in the Image \[cmdb\_ci\_os\_template\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
| |source\_recency\_timestamp|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

## SAM SW Install \[cmdb\_sam\_sw\_install\]

The following attributes in the SAM SW Install \[cmdb\_sam\_sw\_install\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
| |discovery\_source|
| |display\_name|
| |last\_scanned|
| |publisher|
| |source\_recency\_timestamp|
| |version|

## Serial Number \[cmdb\_serial\_number\]

The following attributes in the Serial Number \[cmdb\_serial\_number\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Serial Number|serial\_number|
|Serial Number Type|serial\_number\_type|
| |source\_recency\_timestamp|
|Valid|valid|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Serial Number \[cmdb\_serial\_number\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Install date|install\_date|
|Name|name|
| |source\_recency\_timestamp|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|
|Software Instance \[cmdb\_software\_instance\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Spkg \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Manufacturer|manufacturer|
|Name|name|
| |source\_recency\_timestamp|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Storage Volume \[cmdb\_ci\_storage\_volume\]

The following attributes in the Storage Volume \[cmdb\_ci\_storage\_volume\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Size bytes|size\_bytes|
|Volume ID|volume\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

## VM Instance \[cmdb\_ci\_vm\_instance\]

The following attributes in the VM Instance \[cmdb\_ci\_vm\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Name|name|
|Object ID|object\_id|
| |source\_recency\_timestamp|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|Storage Volume \[cmdb\_ci\_storage\_volume\]|

**Related topics**  


[Service Graph Connector for SolarWinds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/cmdb-integration-solarwinds.md)

