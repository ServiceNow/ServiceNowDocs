---
title: CMDB classes targeted in Service Graph Connector for SolarWinds
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Solarwinds. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [SolarWinds, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for SolarWinds

When you complete setting up the connection, you can configure the integration to periodically pull data from Solarwinds. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

The following attributes in the Availability Zone \[cmdb\_ci\_availability\_zone\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Network \[cmdb\_ci\_network\]|

The following attributes in the Cloud Key Pair \[cmdb\_ci\_cloud\_key\_pair\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Key Pair \[cmdb\_ci\_cloud\_key\_pair\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

The following attributes in the Cloud Network \[cmdb\_ci\_network\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Account Id|account\_id|
|Name|name|
|Object ID|object\_id|
|Datacenter Type|datacenter\_type|

The following attributes in the Cloud Subnet \[cmdb\_ci\_cloud\_subnet\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|CPU core count|cpu\_core\_count|
|CPU core thread|cpu\_core\_thread|
|CPU name|cpu\_name|
|CPU speed \(MHz\)|cpu\_speed|
|CPU manufacturer|cpu\_manufacturer|
|Is Virtual|virtual|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Computer \[cmdb\_ci\_computer\]|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|

The following attributes in the Disk \[cmdb\_ci\_disk\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Model ID|model\_id|
|Device ID|device\_id|
|Name|name|
|Disk space \(GB\)|disk\_space|
|Free disk space \(GB\)|free\_space|
|Size|size|
|Size bytes|size\_bytes|
|Computer|computer|
|Manufacturer|manufacturer|
|Volume serial number|volume\_serial\_number|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Disk \[cmdb\_ci\_disk\]|Reference|Computer \[cmdb\_ci\_computer\]|

The following attributes in the Hardware \[cmdb\_ci\_hardware\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Model ID|model\_id|
|Name|name|
|DNS Domain|dns\_domain|
|Manufacturer|manufacturer|
|Serial number|serial\_number|
|Class|sys\_class\_name|
|Default Gateway|default\_gateway|
|Fully qualified domain name|fqdn|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|

The following attributes in the Hardware Type \[cmdb\_ci\_compute\_template\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosed on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

The following attributes in the IIS Virtual Directory \[cmdb\_ci\_iisdirectory\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Alias|alias|
|Installation directory|install\_directory|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IIS Virtual Directory \[cmdb\_ci\_iisdirectory\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|

The following attributes in the Image \[cmdb\_ci\_os\_template\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

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

The following attributes in the Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Region|region|
|Class|sys\_class\_name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

The following attributes in the Microsoft iis Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Running process command|running\_process\_command|
|Version|version|
|Operational status|operational\_status|
|PID|pid|
|Install Status|install\_status|
|Type|type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Microsoft iis Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\]|Contains::Contained by|IIS Virtual Directory \[cmdb\_ci\_iisdirectory\]|
|Microsoft iis Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|

The following attributes in the MS SQL DataBase \[cmdb\_ci\_db\_mssql\_database\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Data Base|database|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|MS SQL DataBase \[cmdb\_ci\_db\_mssql\_database\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|

The following attributes in the MSFT SQL Instance \[cmdb\_ci\_db\_mssql\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Edition|edition|
|Instance Name|instance\_name|
|Name|name|
|Operational status|operational\_status|
|Service pack|service\_pack|
|Install Status|install\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|MSFT SQL Instance \[cmdb\_ci\_db\_mssql\_instance\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|
|MSFT SQL Instance \[cmdb\_ci\_db\_mssql\_instance\]|Contains::Contained by|MS SQL DataBase \[cmdb\_ci\_db\_mssql\_database\]|

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|DHCP Enabled|dhcp\_enabled|
|Netmask|netmask|
|Configuration Item|cmdb\_ci|
|Mac manufacturer|mac\_manufacturer|
|MAC Address|mac\_address|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

The following attributes in the Serial Number \[cmdb\_serial\_number\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Serial Number|serial\_number|
|Serial Number Type|serial\_number\_type|
|Valid|valid|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Serial Number \[cmdb\_serial\_number\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Name|name|
|Version|version|
|Manufacturer|manufacturer|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

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

The following attributes in the Storage Volume \[cmdb\_ci\_storage\_volume\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|
|Volume ID|volume\_id|
|Name|name|
|Size bytes|size\_bytes|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

The following attributes in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|IP Address|ip\_address|
|State|state|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|Storage Volume \[cmdb\_ci\_storage\_volume\]|

**Related topics**  


[Service Graph Connector for SolarWinds](../concept/cmdb-integration-solarwinds.md)

