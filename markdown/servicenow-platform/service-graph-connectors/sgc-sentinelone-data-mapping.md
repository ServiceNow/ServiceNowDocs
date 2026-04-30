---
title: CMDB classes targeted in the Service Graph Connector for SentinelOne
description: When you complete setting up the connection, you can configure the integration to periodically pull data. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-12-04"
reading_time_minutes: 5
breadcrumb: [SentinelOne, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in the Service Graph Connector for SentinelOne

When you complete setting up the connection, you can configure the integration to periodically pull data. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]

The following attributes in the AWS Datacenter \[cmdb\_ci\_aws\_datacenter\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Object Id|object\_id|
|Region|region|
|Name|name|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Hosted On: Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]

The following attributes in the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Object Id|region|
|Name|name|
|Region|region|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Hosted On: Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Availability Zone \[cmdb\_ci\_availability\_zone\]

The following attributes in the Availability Zone \[cmdb\_ci\_availability\_zone\] table are populated by collected data.

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|Contains:Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object Id|object\_id|
|Region|region|

## GCP Datacenter \[cmdb\_ci\_google\_datacenter\]

The following attributes in the GCP Datacenter \[cmdb\_ci\_google\_datacenter\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object Id|object\_id|
|Account Id|account\_id|
|Datacenter Type|datacenter\_type|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|GCP Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted On: Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

The following attributes in the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object Id|object\_Id|
|Account Id|account\_Id|
|Datacenter Type|datacenter\_type|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|Network \[cmdb\_ci\_network\]|Hosted On: Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Cloud Subnets \[cmdb\_ci\_cloud\_subnet\]

The following attributes in the Cloud Subnets \[cmdb\_ci\_cloud\_subnet\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Object Id|object\_id|
|Name|name|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|Network \[cmdb\_ci\_network\]|Contains:Contained by|Cloud Subnets \[cmdb\_ci\_cloud\_subnet\]|

## Hardware Type \[cmdb\_ci\_compute\_template\]

The following attributes in the Hardware Type \[cmdb\_ci\_compute\_template\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Object Id|object\_id|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|Compute Template \[cmdb\_ci\_compute\_template\]|Hosted On: Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|VM Instance \[cmdb\_ci\_vm\_instance\]|Provisioned From::Provisioned|Compute Template \[cmdb\_ci\_compute\_template\]|

## Cloud Network \[cmdb\_ci\_network\]

The following attributes in the Cloud Network \[cmdb\_ci\_network\] table are populated by collected data.

|Attribute label|Atribute name|
|---------------|-------------|
|Object Id|object\_id|
|Name|name|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|Network \[cmdb\_ci\_network\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

The following attributes in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Object Id|object\_id|
|Name|name|
|VM Instance ID|vm\_inst\_id|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|VM Instance \[cmdb\_ci\_vm\_instance\]|Hosted On: Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|VM Instance \[cmdb\_ci\_vm\_instance\]|Virtualized by::Virtualizes|Server \[cmdb\_ci\_server\]|
|VM Instance \[cmdb\_ci\_vm\_instance\]|Hosted On: Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|
|Tag|tag|

## Image \[cmdb\_ci\_os\_template\]

The following attributes in the Image \[cmdb\_ci\_os\_template\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Object Id|object\_id|
|Name|name|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|Image \[cmdb\_ci\_os\_template\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Serial number|serial\_number|
|CPU speed \(MHz\)|cpu\_speed|
|CPU count|cpu\_count|
|RAM \(MB\)|ram|
|OS Address Width \(bits\)|os\_address\_width|
|Operating System|os|
|CPU core count|cpu\_core\_count|
|Fully qualified domain name|fqdn|
|CPU name|cpu\_name|
|First Discovered|first\_discovered|

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Serial number|serial\_number|
|CPU speed \(MHz\)|cpu\_speed|
|CPU count|cpu\_count|
|RAM \(MB\)|ram|
|OS Address Width \(bits\)|os\_address\_width|
|Operating System|os|
|CPU core count|cpu\_core\_count|
|Fully qualified domain name|fqdn|
|CPU name|cpu\_name|
|First Discovered|first\_discovered|

## SentinelOne Asset Tags \[sn\_sec\_sgc\_sntlone\_asset\_tags\]

The following attributes in the SentinelOne Asset Tags \[sn\_sec\_sgc\_sntlone\_asset\_tags\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|ID|tags\_id|
|Key|tags\_key|
|Value|tags\_value|
|Assigned At|tags\_assignedat|
|Assigned By|tags\_assignedby|
|Assigned By ID|assigned\_by\_id|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Name|name|
|Nic|nic|
|IP version|ip\_version|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Owns:Owned by|IP Address \[cmdb\_ci\_ip\_address\]|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Mac Address|mac\_address|
|Name|name|
|Ip Default Gateway|ip\_default\_gateway|
|Discovery Source|discovery\_source|

|Parent Class|Relationship Type|Child Class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Owns:Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## SentinelOne Additional Attributes \[sn\_sec\_sgc\_sntlone\_additonal\_attributes\]

The following attributes in the SentinelOne Additional Attributes \[sn\_sec\_sgc\_sntlone\_additonal\_attributes\] table are populated by collected data.

<table id="table_whf_nq3_ccc"><thead><tr><th>

Attribute label

</th><th>

Attribute name

</th></tr></thead><tbody><tr><td>

NetworkInterfaces Name

</td><td>

networkinterfaces\_name

</td></tr><tr><td>

NetworkInterfaces GatewayMacAddress

</td><td>

networkinterfaces\_gatewaymacaddress

</td></tr><tr><td>

UUID

</td><td>

uuid

</td></tr><tr><td>

Configuration item

</td><td>

configuration\_item

</td></tr><tr><td>

Network Quarantine Enabled

</td><td>

network\_quarantine\_enabled

</td></tr><tr><td>

Last Successful Scan Date

</td><td>

last\_successful\_scan\_date

</td></tr><tr><td>

License\_Key

</td><td>

license\_key

</td></tr><tr><td>

First Discovered

</td><td>

first\_discovered

</td></tr><tr><td>

Location Enabled

</td><td>

location\_enabled

</td></tr><tr><td>

Ad ComputerDistinguishedName

</td><td>

ad\_computerdistinguishedname

</td></tr><tr><td>

Agent Version

</td><td>

agent\_version

</td></tr><tr><td>

Scan Status

</td><td>

scan\_status

</td></tr><tr><td>

Scan Started At

</td><td>

scan\_started\_at

</td></tr><tr><td>

ID

</td><td>

id

</td></tr><tr><td>

IP Address Subnet

</td><td>

ip\_address\_subnet

</td></tr><tr><td>

Mitigation Mode Suspicious

</td><td>

mitigation\_mode\_suspicious

</td></tr><tr><td>

Last Scan Finished At

</td><td>

last\_scan\_finished\_at

</td></tr><tr><td>

Firewall Enabled

</td><td>

firewall\_enabled

</td></tr><tr><td>

Console Migration Status

</td><td>

console\_migration\_status

</td></tr><tr><td>

Group ID

</td><td>

group\_id

</td></tr><tr><td>

Operational State Expiration

</td><td>

operational\_state\_expiration

</td></tr><tr><td>

Last IP To Mgmt

</td><td>

last\_ip\_to\_mgmt

</td></tr><tr><td>

Threat Reboot Required

</td><td>

threat\_reboot\_required

</td></tr><tr><td>

Machine Type

</td><td>

machine\_type

</td></tr><tr><td>

Is Pending Uninstall

 Ranger Status

</td><td>

Is\_pending\_uninstall

 ranger\_status

</td></tr><tr><td>

Ad LastUserDistinguishedName

</td><td>

ad\_lastuserdistinguishedname

</td></tr><tr><td>

Agent Up To Date

</td><td>

agent\_up\_to\_date

</td></tr><tr><td>

Ranger Version

</td><td>

ranger\_version

</td></tr><tr><td>

Last Boot Time

</td><td>

last\_boot\_time

</td></tr><tr><td>

Disk Encryption Status

</td><td>

disk\_encryption\_status

</td></tr><tr><td>

Mitigation Mode

</td><td>

mitigation\_mode

</td></tr><tr><td>

Last Full Scan

</td><td>

last\_full\_scan

</td></tr><tr><td>

Agent Uninstalled

</td><td>

agent\_uninstalled

</td></tr><tr><td>

Extenal Id

</td><td>

extenal\_id

</td></tr><tr><td>

Updated At

</td><td>

updated\_at

</td></tr><tr><td>

Last Scan Aborted At

</td><td>

last\_scan\_aborted\_at

</td></tr><tr><td>

Network Status

</td><td>

network\_status

</td></tr><tr><td>

Show Alert Icon

</td><td>

show\_alert\_icon

</td></tr><tr><td>

Subscribed On

</td><td>

subscribed\_on

</td></tr><tr><td>

Account ID

</td><td>

account\_id

</td></tr><tr><td>

Recently Active

</td><td>

recently\_active

</td></tr><tr><td>

Active Threats

</td><td>

active\_threats

</td></tr><tr><td>

Allow Remote Shell

</td><td>

allow\_remote\_shell

</td></tr><tr><td>

Site Name

</td><td>

site\_name

</td></tr><tr><td>

First Full Mode Time

</td><td>

first\_full\_mode\_time

</td></tr><tr><td>

Infected

</td><td>

infected

</td></tr><tr><td>

App Vulnerability Status

</td><td>

app\_vulnerability\_status

</td></tr><tr><td>

Site ID

</td><td>

site\_id

</td></tr><tr><td>

Agent Installer Type

</td><td>

agent\_installer\_type

</td></tr><tr><td>

Account Name

</td><td>

acount\_name

</td></tr><tr><td>

NetworkInterfaces Name

</td><td>

networkinterfaces\_name

</td></tr><tr><td>

NetworkInterfaces GatewayMacAddress

</td><td>

networkinterfaces\_gatewaymacaddress

</td></tr><tr><td>

NetworkInterfaces ID

</td><td>

networkinterfaces\_id

</td></tr><tr><td>

user\_actions\_needed

</td><td>

user\_actions\_needed

</td></tr><tr><td>

aws\_security\_group

</td><td>

aws\_security\_group

</td></tr><tr><td>

proxyState\_console

</td><td>

proxyState\_console

</td></tr><tr><td>

proxyState\_deepVisibility

</td><td>

proxyState\_deepVisibility

</td></tr><tr><td>

Ad UserPrincipalName

</td><td>

ad\_userPrincipalName

</td></tr><tr><td>

Ad ComputerMemberOf

</td><td>

ad\_computerMemberOf

</td></tr><tr><td>

Ad ComputerDistinguishedName

</td><td>

ad\_computerDistinguishedName

</td></tr><tr><td>

Ad LastUserMemberOf

</td><td>

ad\_lastUserMemberOf

</td></tr><tr><td>

Ad LastUserDistinguishedName

</td><td>

ad\_lastUserDistinguishedName

</td></tr><tr><td>

Ad Mail

</td><td>

ad\_mail

</td></tr><tr><td>

Agent Decommissioned

</td><td>

agent\_decommissioned

</td></tr><tr><td>

Agent Operational State

</td><td>

agent\_operational\_state

</td></tr><tr><td>

Last Active Date

</td><td>

last\_active\_date

</td></tr><tr><td>

Group Updated At

</td><td>

group\_updated\_at

</td></tr><tr><td>

Missing Permissions

</td><td>

missing\_permissions

</td></tr></tbody>
</table>## Service Graph Connector for SentinelOne Properties

<table id="table_r4g_4r3_ccc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sec\_sgc\_sntlone.api\_page\_size

</td><td>

Enter the number of records per page to retrieve.-   Type: string
-   Default value: 1000
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>**Note:** To open the System Properties \[sys\_properties\] table, enter sys\_properties.LIST in the navigation filter.

