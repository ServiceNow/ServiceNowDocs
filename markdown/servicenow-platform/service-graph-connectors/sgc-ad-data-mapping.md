---
title: CMDB classes targeted in Service Graph Connector for Active Directory
description: When you complete setting up the connection, you can configure the integration to periodically pull data. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Active Directory, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Active Directory

When you complete setting up the connection, you can configure the integration to periodically pull data. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Category|category|
|Object ID|object\_id|
|Fully qualified domain name|fqdn|
|Checked out|check\_out|
|Check in|check\_in|
|First discovered|first\_discovered|
|Operating System|os|
|OS Version|os\_version|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Key|key|
|Version|version|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Install On|installed\_on|
|Product Name|software|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Display Name|display\_name|
|Version|version|
|Discovery source|discovery\_source|

## SGC Active Directory Computer \[sn\_sec\_sgc\_ad\_active\_directory\_computer\]

The following attributes in the SGC Active Directory Computer \[sn\_sec\_sgc\_ad\_active\_directory\_computer\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Account expires|account\_expires|
|Bad password count|bad\_pwd\_count|
|Bad password time|bad\_password\_time|
|Code page|code\_page|
|Common name|cn|
|Country code|country\_code|
|Description|description|
|Display name|display\_name|
|Distinguished name|distinguished\_name|
|DN|dn|
|Dscorepropagation data|dscore\_propagation\_data|
|Instance type|instance\_type|
|Iscritical system object|iscritical\_system\_object|
|Keywords|keywords|
|Last logon|last\_logon|
|Local policy flags|local\_policy\_flags|
|Logon count|logon\_count|
|Member of|member\_of|
|Ms-DS-Host service account|msds\_host\_service\_account|
|Ms-DS-Supported encryption types|msds\_support\_ncryptiontypes|
|Name|name|
|Object class|object\_class|
|Object GUID|object\_guid|
|Other well known objects|other\_well\_known\_objects|
|Password last set|pwd\_last\_set|
|Primary group id|primary\_groupid|
|SamAccount name|sam\_account\_name|
|SamAccount type|sam\_account\_type|
|Service binding information|service\_binding\_information|
|Service class name|service\_class\_name|
|Service DNS name|service\_dns\_name|
|Service DNS name type|service\_dns\_name\_type|
|Service principal name|service\_principal\_name|
|Show in advanced view only|show\_in\_advanced\_view\_only|
|Source|source|
|User account control|user\_account\_control|
|USN changed|usn\_changed|
|USN created|usn\_created|
|When changed|when\_changed|

