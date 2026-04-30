---
title: IBM Cloud Discovery
description: If your cloud resources are in an IBM cloud, create credentials that can access your IBM account.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# IBM Cloud Discovery

If your cloud resources are in an IBM cloud, create credentials that can access your IBM account.

<table id="table_m3q_bqm_wcb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the IBM credentials to register with the instance.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr><tr><td>

Softlayer API User

</td><td>

Softlayer cloud user name.

</td></tr><tr><td>

Softlayer API Key

</td><td>

Softlayer API key.

</td></tr><tr><td>

Bluemix API Key

</td><td>

Bluemix API key.

</td></tr></tbody>
</table>## Data collected by Service Mapping during top-down discovery

To include discovered components into application services, enable CI relationships used in tag-based discovery by Service Mapping. These CI relationships are available from the 1.0.68 release on the ServiceNow Store. For operational steps, see [Tag-based discovery configuration](../../service-mapping/concept/tag_discovery_configuration.md).

Service Mapping uses tag-based discovery to create service instance maps including the Cloud components. The Service Mapping application comes with the following preconfigured CI relationships used for tag-based discovery. These CI relationships are available from the 1.0.68 release on the ServiceNow Store.

|CI|Relationship|CI|
|---|------------|---|
|Configuration Item \[cmdb\_ci\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## IBM Cloud Discovery API list

<table id="table_mmm_csm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

IBM Constraints

</td></tr><tr><td>

object\_id

</td><td>

name

</td></tr><tr><td>

dns\_domain

</td><td>

domain

</td></tr><tr><td>

name

</td><td>

alias

</td></tr><tr><td>

short\_description

</td><td>

display\_name

</td></tr><tr><td>

region

</td><td>

name

</td></tr></tbody>
</table>|CI Attributes|IBM Constraints|
|-------------|---------------|
|object\_id|id|
|short\_description|longName|
|name|name|
|install\_status|statusId|

<table id="table_odn_dsm_qmb"><tbody><tr><td>

CI Attributes

</td><td>

IBM Constraints

</td></tr><tr><td>

object\_id

</td><td>

id

</td></tr><tr><td>

short\_description

</td><td>

description

</td></tr><tr><td>

location\_group\_type\_id

</td><td>

locationGroupTypeId

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

location\_group\_type

</td><td>

locationGroupType.name

</td></tr></tbody>
</table>|CI Attributes|IBM Constraints|
|-------------|---------------|
|object\_id|id|
|cpus|maxCpu/startCpus|
|memory|maxMemory|
|disks|&lt;not mapped&gt;|
|disks\_size|&lt;not mapped&gt;|
|nics|&lt;not mapped&gt;|
|terminated\_on|&lt;not mapped&gt;|
|state|statusId|
|termination\_protection|&lt;not mapped&gt;|
|short\_description|notes|
|name|hostname|
|dns\_domain|domain|
|fqdn|fullyQualifiedDomainName|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|cmdb\_ci\_os\_template| |
|image\_type| |
|guest\_os| |
|version| |
|offer| |
|OS Status| |
|root\_device\_type| |
|image\_source| |
|credentials| |
|infuse\_key| |
|update\_host\_name| |
|name|name|
|object\_id|id|
|short\_description|description|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|object\_id|id|
|finger\_print|fingerprint|
|created\_date|createDate|
|key|key|
|name|label|
|modify\_date|modifyDate|
|short\_description|notes|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|volume\_id|id|
|size|capacityGb|
|size\_bytes|capacityGb|
|free\_space|&lt;not mapped&gt;|
|free\_space\_bytes|&lt;not mapped&gt;|
|media\_type|&lt;not mapped&gt;|
|file\_system|&lt;not mapped&gt;|
|label|serviceResourceName|
|lun \( Logical Unit Number \)|&lt;not mapped&gt;|
|volume\_container|&lt;not mapped&gt;|
|state|?|
|storage\_type|storageTypeId|
|protected\_by|&lt;not mapped&gt;|
|share\_count|&lt;not mapped&gt;|
|sharable|FALSE|
|device|guestId|
|delete\_on\_termination|&lt;not mapped&gt;|
|mapping\_type|&lt;not mapped&gt;|
|object\_id|id|
|vdisk\_id|&lt;not mapped&gt;|
|storage\_type|nasType|
|name|serviceResourceName|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|object\_id|id|
|capacity|capacityGb|
|is\_encrypted| |
|volume\_name|serviceResourceName|
|storage\_server| |
|start\_time| |
|state| |
|snapshotSizeBytes|snapshotSizeBytes|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|state| |
|cidr|&lt;not\_mapped&gt;|
|is\_external|true/false|
|netmask|&lt;not\_mapped&gt;|
|broadcast\_address|&lt;not\_mapped&gt;|
|default\_gateway|&lt;not\_mapped&gt;|
|is\_shared|&lt;not\_mapped&gt;|
|is\_dhcp\_enabled|&lt;not\_mapped&gt;|
|scope|&lt;not\_mapped&gt;|
|max\_ports|&lt;not\_mapped&gt;|
|terminated\_on|&lt;not\_mapped&gt;|
|provided\_contracts|&lt;not\_mapped&gt;|
|object\_id|id|
|access\_port\_vlan|vlanNumber|
|&lt;not\_mapped&gt;|primarySubnetId|
|name|vlanNumber|
|&lt;not\_mapped&gt;|accountId|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|subnet\_mask|netmask|
|cidr|networkIdentifier +'/' + cidr|
|available\_ip\_count|usableIpAddressCount|
|broadcast\_address|broadcastAddress|
|primary\_dns|&lt;not mapped&gt;|
|secondary\_dns|&lt;not mapped&gt;|
|tertiary\_dns|&lt;not mapped&gt;|
|is\_dhcp\_enabled|&lt;not mapped&gt;|
|ipam\_provider|&lt;not mapped&gt;|
|domain\_name|&lt;not mapped&gt;|
|parent\_domain\_name|&lt;not mapped&gt;|
|gateway|gateway|
|route\_table\_association\_id|&lt;not mapped&gt;|
|state|&lt;not mapped&gt;|
|&lt;not mapped&gt;|modifyDate|
|&lt;not mapped&gt;|version|
|&lt;not mapped&gt;|networkVlanId|
|&lt;not mapped&gt;|isCustomerRoutable|
|object\_id|id|
|&lt;not mapped&gt;|broadcastAddress|
|&lt;not mapped&gt;|isCustomerOwned|
|&lt;not mapped&gt;|sortOrder|
|&lt;not mapped&gt;|networkIdentifier|
|&lt;not mapped&gt;|totalIpAddresses|
|&lt;not mapped&gt;|addressSpace|
|category|subnetType|
|name|networkIdentifier +'/' + cidr|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|region|&lt;not\_mapped&gt;|
|object\_id|id|
|intld|&lt;not\_mapped&gt;|
|tenant\_name|&lt;not\_mapped&gt;|
|state|&lt;not\_mapped&gt;|
|&lt;not\_mapped&gt;|port|
|&lt;not\_mapped&gt;|description|
|&lt;not\_mapped&gt;|createDate|
|&lt;not\_mapped&gt;|modifyDate|
|name|name|
|short\_description|description|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|created|createDate|
|direction|direction|
|ethertype|ethertype|
|object\_id|id|
|updated|modifyDate|
|portRangeMax|portRangeMax|
|portRangeMin|portRangeMin|
|protocol|protocol|
|remoteGroupId|remoteGroupId|
|securityGroupId|securityGroupId|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|state|"operatingStatus"|
|canonical\_hosted\_zone\_id| |
|canonical\_hosted\_zone\_name| |
|dns\_name|address|
|snat\_ip\_address| |
|vlan| |
|app\_code| |
|component\_code| |
|env\_code| |
|ip\_address\_pool| |
| |"accountId"|
| |"address"|
| |"createDate"|
| |"description"|
|object\_id|"id"|
| |isPublic|
| |"locationId"|
| |"modifyDate"|
|name|"name"|
| |"provisioningStatus"|
| |"useSystemPublicIpPool"|
| |"uuid"|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|cmdb\_ci\_lb\_service| |
|pool| |
|port|protocolPort|
|last\_port| |
|input\_url| |
|host\_name| |
|back\_end\_port| |
|front\_end\_port|protocolPort|
|listener\_protocol|protocol|
|server\_port| |
|server\_protocol| |
|traffic\_domain| |
|ssl\_certificate\_id| |
|object\_id|id|
|hit\_count| |

|CI Attributes|IBM Constraints|
|-------------|---------------|
|check\_interval\_sec|interval|
|max\_retries|maxRetries|
|monitor\_type|monitorType|
|provisioning\_status|provisioningStatus|
|timeout\_sec|timeout|
|object\_id|id|

|CI Attributes|IBM Constraints|
|-------------|---------------|
| |createDate|
|load\_balancing\_method|loadBalancingAlgorithm|
| |modifyDate|
| |protocol|
| |protocolPort|
|pool\_status|provisioningStatus|
|object\_id|uuid|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|server\_id|address|
|object\_id|id|
| |createDate|
| |modifyDate|
| |provisioningStatus|
| |uuid|
| |weight|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|name|name|
|need to see what is this?|quota\_id|
| |tags|
|object\_id|id|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|name|name|
|url|url|
|billing\_enabled|billing\_enabled|
|quota\_definition\_url|quota\_definition\_url|
|spaces\_url|spaces\_url|
|guid|guid|
|status|status|
|object\_id|metadata.guid|

|CI Attributes|IBM Constraints|
|-------------|---------------|
|name|name|
|url|url|
|object\_id|metadata.guid|
|allow\_ssh|allow\_ssh|
|guid|metadata.guid|

