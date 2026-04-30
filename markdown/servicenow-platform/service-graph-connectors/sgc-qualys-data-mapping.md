---
title: CMDB classes targeted in the Service Graph Connector for Qualys
description: When you complete setting up the connection, you can configure the integration to periodically pull data. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table. The Service Graph Connector for Qualys identifies and classifies information about various configuration Items \(CIs\).
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Qualys, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in the Service Graph Connector for Qualys

When you complete setting up the connection, you can configure the integration to periodically pull data. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table. The Service Graph Connector for Qualys identifies and classifies information about various configuration Items \(CIs\).

## SGC Qualys Asset Cloud Tag

The following attributes in the SGC Qualys Asset Cloud Tag \[sn\_sec\_sgc\_qualys\_asset\_cloud\_tag\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Qualys Asset|qualys\_asset|
|Value|value|
|Configuration item|configuration\_item|

## SGC Qualys Asset Software Details \[sn\_sec\_sgc\_qualys\_asset\_software\_details\]

The following attributes in the SGC Qualys Asset Software Details \[sn\_sec\_sgc\_qualys\_asset\_software\_details\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|token1|
|Qualys Asset|qualys\_asset|
|Configuration item|configuration\_item|
|Unique key|unique\_key|
|Id|id|
|Install Path|install\_path|
|Last Use Date|last\_use\_date|
|Version|token2|

## Hardware Type \[cmdb\_ci\_compute\_template\]

The following attributes in the Hardware Type \[cmdb\_ci\_compute\_template\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|

## Image \[cmdb\_ci\_os\_template\]

The following attributes in the Image \[cmdb\_ci\_os\_template\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Offer|offer|
|Version|version|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Discovery source|discovery\_source|
|Name|name|
|Version|version|
|Manufacturer|manufacturer|

## SGC Qualys Asset Network Interface Details \[sn\_sec\_sgc\_qualys\_asset\_nic\_details\]

The following attributes in the SGC Qualys Asset Network Interface Details \[sn\_sec\_sgc\_qualys\_asset\_nic\_details\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Configuration item|configuration\_item|
|IPv4|ip\_v4|
|Addresses|addresses|
|Interface Id|interface\_id|
|IPv6|ip\_v6|
|MAC Vendor Intro Date|mac\_vendor\_intro\_date|
|Qualys Asset|qualys\_asset|
|Type|type|

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Manufacturer|manufacturer|
|Name|name|
|Asset tag|asset\_tag|
|Class|sys\_class\_name|
|CPU count|cpu\_count|
|DNS Domain|dns\_domain|
|First discovered|first\_discovered|
|Fully qualified domain name|fqdn|
|Install Status|install\_status|
|Operating System|os|
|Operational status|operational\_status|
|OS Address Width \(bits\)|os\_address\_width|
|OS Service Pack|os\_service\_pack|
|OS Version|os\_version|
|RAM \(MB\)|ram|

## SGC Qualys Asset Open Port Details \[sn\_sec\_sgc\_qualys\_asset\_open\_port\_details\]

The following attributes in the SGC Qualys Asset Open Port Details \[sn\_sec\_sgc\_qualys\_asset\_open\_port\_details\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Port|port|
|Protocol|protocol|
|Description|description|
|Detected Service|detected\_service|
|First Found|first\_found|
|Last Updated|last\_updated|
|Qualys Asset|qualys\_asset|
|Service Id|service\_id|

## SGC Qualys Asset Details \[sn\_sec\_sgc\_qualys\_asset\_details\]

The following attributes in the SGC Qualys Asset Details \[sn\_sec\_sgc\_qualys\_asset\_details\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Asset Name|asset\_name|
|Activated Modules|activated\_modules|
|Address|address|
|Agent Configuration Profile|agent\_configuration\_profile|
|Agent Connected From|agent\_connected\_from|
|Agent Eror Status|agent\_error\_status|
|Agent ID|agent\_id|
|Agent Last Activity|agent\_last\_activity|
|Agent Last Checked In|agent\_last\_checked\_in|
|Agent Last Inventory|agent\_last\_inventory|
|Agent Platform|platform|
|Agent Status|status|
|Agent UDC Manifest Assigned|agent\_udc\_manifest\_assigned|
|Agent Version|agent\_version|
|ASN|asn|
|Asset ID|asset\_id|
|Asset Type|asset\_type|
|Asset UUID|asset\_uuid|
|Assigned Location|assigned\_location|
|AWS Host Name|aws\_host\_name|
|AWS Kernel ID|aws\_kernel\_id|
|AWS Launch Date|aws\_launch\_date|
|AWS Region Name|aws\_region\_name|
|Azure Image Publisher|azure\_image\_publisher|
|Azure Platform|azure\_platform|
|Azure Subnet|azure\_subnet|
|Azure Virtual Network|azure\_virtual\_network|
|Bios Description|bios\_description|
|Bios Serial Number|bios\_serial\_number|
|Business AppListData|business\_applist\_data|
|Business Information|business\_information|
|Chirp Status|chirp\_status|
|City|lastlocation\_city|
|Continent|lastlocation\_continent|
|Country|lastlocation\_country|
|Custom Attribrutes|custom\_attributes|
|Domain|domain|
|Domain Role|domain\_role|
|ESAM Tags|easm\_tags|
|First EASM Scan Date|first\_easm\_scan\_date|
|Hardware Category|hardware\_category|
|Hardware Category1|hardware\_category1|
|Hardware Category2|hardware\_category2|
|Hardware FullName|hardware\_fullname|
|Hardware Lifecycle Confidence|hardware\_lifecycle\_lifecycleconfidence|
|Hardware Lifecycle EOSDate|hardware\_lifecycle\_eosdate|
|Hardware Lifecycle GaDate|hardware\_lifecycle\_gadate|
|Hardware Lifecycle IntroDate|hardware\_lifecycle\_introdate|
|Hardware Lifecycle ObsoleteDate|hardware\_lifecycle\_obsoletedate|
|Hardware Lifecycle Stage|hardware\_lifecycle\_stage|
|Hardware Model|hardware\_model|
|Hardware Product Family|hardware\_product\_family|
|Hardware Product Name|hardware\_product\_name|
|Hardware Product URL|hardware\_product\_url|
|Hardware Texonomy Category1|hardware\_taxonomy\_category1|
|Hardware Texonomy Category2|hardware\_taxonomy\_category2|
|Hardware Texonomy ID|hardware\_taxonomy\_id|
|Hardware Texonomy Name|hardware\_taxonomy\_name|
|Has Agent|aws\_has\_agent|
|Host ID|host\_id|
|Hosting Category1|hosting\_category1|
|Hw UUID|hw\_uuid|
|Is Container Host|is\_container\_host|
|IsDefault|criticality\_isdefault|
|ISP|isp|
|Last Boot|last\_boot|
|Last Compliance Scan|last\_compliance\_scan|
|Last EASM Scan Date|last\_easm\_scan\_date|
|Last Full Scan|last\_full\_scan|
|Last Location Name|lastlocation\_name|
|Last Logged On User|last\_logged\_on\_user|
|Last Modified Date|last\_modified\_date|
|Last PC Scan Date Agent|last\_pc\_scan\_date\_agent|
|Last PC Scan Date Scanner|last\_pc\_scan\_date\_scanner|
|Last Updated|criticality\_lastupdated|
|Last VM Scan|last\_vm\_scan|
|Last VM Scan Date Agent|last\_vm\_scan\_date\_agent|
|Last VM Scan Date Scanner|last\_vm\_scan\_date\_scanner|
|Missing Software|missing\_software|
|NetBios Name|netbios\_name|
|Network Guid|network\_guid|
|Organization Name|organization\_name|
|OS Category|os\_category|
|OS Category1|os\_category1|
|OS Category2|os\_category2|
|OS Edition|os\_edition|
|OS Lifecycle Confidence|os\_lifecycle\_confidence|
|OS Lifecycle EOL Date|os\_lifecycle\_eol\_date|
|OS Lifecycle EOLSupport Stage|os\_lifecycle\_eol\_supportstage|
|OS Lifecycle EOS Date|os\_lifecycle\_eos\_date|
|OS Lifecycle EOSSupport Stage|os\_lifecycle\_eos\_supportstage|
|OS Lifecycle Ga Date|os\_lifecycle\_ga\_date|
|OS Lifecycle Stage|os\_lifecycle\_stage|
|OS Market Version|os\_market\_version|
|OS Name|os\_name|
|OS Product Family|os\_product\_family|
|OS Product Name|os\_product\_name|
|OS Product URL|os\_product\_url|
|OS Release|os\_release|
|OS Taxonomy Category1|os\_taxonomy\_category1|
|OS Taxonomy Category2|os\_taxonomy\_category2|
|OS Taxonomy ID|os\_taxonomy\_id|
|OS Taxonomy Name|os\_taxonomy\_name|
|Passive Sensor|passive\_sensor|
|Postal|lastlocation\_postal|
|Provider|provider|
|Qualys Scanner|qualys\_scanner|
|Risk Score|risk\_score|
|Score|criticality\_score|
|Sensor Last Updated Date|sensor\_last\_updated\_date|
|Spot Instance|spot\_instance|
|State|lastlocation\_state|
|SubDomain|subdomain|
|Time Zone|time\_zone|
|Tracking Method|tracking\_method|
|WhoIs|whois|

## Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

The following attributes in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|IP Address|ip\_address|
|Monitor|monitor|
|State|state|
|VM Instance ID|vm\_inst\_id|

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Account Id|account\_id|
|Name|name|
|Object ID|object\_id|
|Datacenter Type|datacenter\_type|

## Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

The following attributes in the Cloud Mgmt Network Interface \[cmdb\_ci\_nic\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|MAC Address|mac\_address|
|Name|name|
|Object ID|object\_id|
|Public IP|public\_ip|
|DNS Domain|dns\_domain|
|Host Name|host\_name|
|IP default gateway|ip\_default\_gateway|
|Netmask|netmask|
|Manufacturer|manufacturer|

## Availability Zone \[cmdb\_ci\_availability\_zone\]

The following attributes in the Availability Zone \[cmdb\_ci\_availability\_zone\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|

## SGC Qualys Asset Tag \[sn\_sec\_sgc\_qualys\_asset\_tag\]

The following attributes in the SGC Qualys Asset Tag \[sn\_sec\_sgc\_qualys\_asset\_tag\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Tag Id|tag\_id|
|Tag Name|tag\_name|
|Background Color|background\_color|
|Business Impact|business\_impact|
|Criticality Score|criticality\_score|
|Foreground Color|foreground\_color|
|Qualys Asset|qualys\_asset|

## SGC Qualys Asset Processor Details \[sn\_sec\_sgc\_qualys\_asset\_processor\_details\]

The following attributes in the SGC Qualys Asset Processor Details \[sn\_sec\_sgc\_qualys\_asset\_processor\_details\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Description|processor\_description|
|Cores Per Socket|processor\_corespersocket|
|Multi Threading Status|processor\_multithreadingstatus|
|No Of Socket|processor\_noofsocket|
|Number of CPUs|processor\_numcpus|
|Qualys Asset|qualys\_asset|
|Speed|processor\_speed|

## File System \[cmdb\_ci\_file\_system\]

The following attributes in the File System \[cmdb\_ci\_file\_system\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Free space bytes|free\_space\_bytes|
|Size bytes|size\_bytes|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the File System \[cmdb\_ci\_file\_system\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Installed on|installed\_on|
|Name|name|
|Install date|install\_date|

## Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]

The following attributes in the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Region|region|

## AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]

The following attributes in the AWS Datacenter \[cmdb\_ci\_aws\_datacenter\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object ID|object\_id|
|Region|region|

## Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]

The following attributes in the Cloud Subnet \[cmdb\_ci\_cloud\_subnet\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Display name|display\_name|
|Publisher|publisher|
|Version|version|
|Discovery source|discovery\_source|
|Install date|install\_date|

## Cloud Network \[cmdb\_ci\_network\]

The following attributes in the Cloud Network \[cmdb\_ci\_network\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Object ID|object\_id|

## SGC Qualys Asset Service Details \[sn\_sec\_sgc\_qualys\_asset\_service\_details\]

SGC Qualys Asset Service Details \[sn\_sec\_sgc\_qualys\_asset\_service\_details\].

| | |
|---|---|
|Name|name|
|Description|description|
|Qualys Asset|qualys\_asset|
|Status|status|

## Relationships created by Cloud Network \[cmdb\_ci\_network\]

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|

## Relationships created by Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Image \[cmdb\_ci\_os\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Virtualized by::Virtualizes|Server \[cmdb\_ci\_server\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Hardware Type \[cmdb\_ci\_compute\_template\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

## Relationships created by Server \[cmdb\_ci\_server\]

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Reference|SGC Qualys Asset Network Interface Details \[sn\_sec\_sgc\_qualys\_asset\_nic\_details\]|
|Server \[cmdb\_ci\_server\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|
|Server \[cmdb\_ci\_server\]|Reference|SGC Qualys Asset Service Details \[sn\_sec\_sgc\_qualys\_asset\_service\_details\]|
|Server \[cmdb\_ci\_server\]|Reference|SGC Qualys Asset Software Details \[sn\_sec\_sgc\_qualys\_asset\_software\_details\]|
|Server \[cmdb\_ci\_server\]|Reference|SGC Qualys Asset Open Port Details \[sn\_sec\_sgc\_qualys\_asset\_open\_port\_details\]|
|Server \[cmdb\_ci\_server\]|Reference|SGC Qualys Asset Processor Details \[sn\_sec\_sgc\_qualys\_asset\_processor\_details\]|
|Server \[cmdb\_ci\_server\]|Reference|SGC Qualys Asset Tag \[sn\_sec\_sgc\_qualys\_asset\_tag\]|
|Server \[cmdb\_ci\_server\]|Reference|SGC Qualys Asset Cloud Tag \[sn\_sec\_sgc\_qualys\_asset\_cloud\_tag\]|
|Server \[cmdb\_ci\_server\]|Reference|SGC Qualys Asset Details \[sn\_sec\_sgc\_qualys\_asset\_details\]|
|Server \[cmdb\_ci\_server\]|Contains::Contained by|File System \[cmdb\_ci\_file\_system\]|

## Relationships created by Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Relationships created by Hardware Type \[cmdb\_ci\_compute\_template\]

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Hardware Type \[cmdb\_ci\_compute\_template\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

## Relationships created by Image \[cmdb\_ci\_os\_template\]

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

## Relationships created by Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|

## Reference-type relationships

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|SGC Qualys Asset Software Details \[sn\_sec\_sgc\_qualys\_asset\_software\_details\]|Reference|Server \[cmdb\_ci\_server\]|
|SGC Qualys Asset Network Interface Details \[sn\_sec\_sgc\_qualys\_asset\_nic\_details\]|Reference|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|SGC Qualys Asset Cloud Tag \[sn\_sec\_sgc\_qualys\_asset\_cloud\_tag\]|Reference|Server \[cmdb\_ci\_server\]|
|Software Instance \[cmdb\_software\_instance\]|Reference|Server \[cmdb\_ci\_server\]|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

