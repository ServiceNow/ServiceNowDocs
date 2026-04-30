---
title: Data collected for GCP Cloud Discovery
description: Discovery collects information about cloud resources in Google Cloud Platform \(GCP\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [Patterns]
breadcrumb: [Cloud resource discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Data collected for GCP Cloud Discovery

Discovery collects information about cloud resources in Google Cloud Platform \(GCP\). Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date.**
    -   Discovery and Service Mapping Patterns.
    -   CMDB CI Class Model.
    -   Visibility Content.
-   **Configure a discovery schedule**

    [Create a discovery schedule in Cloud Discovery Workspace](../task/cloud-operations-disco-create-schedule.md)


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## GCP data collected

<table id="table_vtb_gxn_dhb"><thead><tr><th>

Table

</th><th>

ServiceNow Field

</th><th>

GCP Field

</th></tr></thead><tbody><tr><td rowspan="5">

Region \[cmdb\_ci\_google\_datacenter\]

</td><td>

object\_id

</td><td>

items.id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

short\_description

</td><td>

description

</td></tr><tr><td>

status

</td><td>

status

</td></tr><tr><td>

region

</td><td>

items.name

</td></tr><tr><td rowspan="12">

Virtual Server \[cmdb\_ci\_vm\_instance\]

</td><td>

object\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

state

</td><td>

status

</td></tr><tr><td>

cpus

</td><td>

Not mapped

</td></tr><tr><td>

memory

</td><td>

Not mapped

</td></tr><tr><td>

disks

</td><td>

disks \(array size\)

</td></tr><tr><td>

disks\_size

</td><td>

Not mapped

</td></tr><tr><td>

nics

</td><td>

networkInterfaces \(array size\)

</td></tr><tr><td>

termination\_protection

</td><td>

deletionProtection

</td></tr><tr><td>

Not mapped

</td><td>

canIpForward

</td></tr><tr><td>

Not mapped

</td><td>

selfLink

</td></tr><tr><td>

sys\_created\_on

</td><td>

creationTimestamp

</td></tr><tr><td rowspan="7">

Storage Volume \(cmdb\_ci\_storage\_volume\)

</td><td>

object\_id

</td><td>

items.id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

short\_description

</td><td>

description

</td></tr><tr><td>

state

</td><td>

status

</td></tr><tr><td>

status

</td><td>

status

</td></tr><tr><td>

size

</td><td>

sizeGb

</td></tr><tr><td>

storage\_type

</td><td>

storage\_type

</td></tr><tr><td rowspan="4">

Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]

</td><td>

object\_id

</td><td>

items.id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

public\_ip\_address

</td><td>

address

</td></tr><tr><td>

state

</td><td>

status

</td></tr><tr><td rowspan="5">

Availablility Zone \[cmdb\_ci\_availability\_zone\]

</td><td>

object\_id

</td><td>

items.id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

short\_description

</td><td>

description

</td></tr><tr><td>

state

</td><td>

status

</td></tr><tr><td>

status

</td><td>

status

</td></tr><tr><td rowspan="6">

Hardware Template \[cmdb\_ci\_compute\_template\]

</td><td>

object\_id

</td><td>

items.id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

short\_description

</td><td>

description

</td></tr><tr><td>

vcpus

</td><td>

guestCpus

</td></tr><tr><td>

memory\_mb

</td><td>

memoryMb

</td></tr><tr><td>

local\_storage\_gb

</td><td>

imageSpaceGb

</td></tr><tr><td rowspan="3">

Instance Template \[cmdb\_ci\_instance\_template\]

</td><td>

object\_id

</td><td>

items.id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

short\_description

</td><td>

description

</td></tr><tr><td rowspan="9">

Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]

</td><td>

object\_id

</td><td>

items.id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

state

</td><td>

status

</td></tr><tr><td>

volume\_name

</td><td>

sourceDisk

</td></tr><tr><td>

capacity

</td><td>

storageBytes

</td></tr><tr><td>

No mapping

</td><td>

storageBytesStatus

</td></tr><tr><td>

No mapping

</td><td>

selfLink

</td></tr><tr><td>

No mapping

</td><td>

labelFingerprint

</td></tr><tr><td>

No mapping

</td><td>

diskSizeGb

</td></tr><tr><td rowspan="5">

Disk Type \[cmdb\_ci\_disk\_type\]

</td><td>

object\_id

</td><td>

zone:name

</td></tr><tr><td>

name

</td><td>

name@zone

</td></tr><tr><td>

short\_description

</td><td>

description

</td></tr><tr><td>

valid\_disk\_size

</td><td>

validDiskSize

</td></tr><tr><td>

default\_disk\_size\_gb

</td><td>

defaultDiskSizeGb

</td></tr><tr><td rowspan="4">

Subnet \[cmdb\_ci\_cloud\_subnet\]

</td><td>

object\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

cidr

</td><td>

ipCidrRange

</td></tr><tr><td>

gateway

</td><td>

gatewayAddress

</td></tr><tr><td rowspan="7">

Image \[cmdb\_ci\_os\_template\]

</td><td>

object\_id

</td><td>

items.id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

image\_type

</td><td>

sourceType

</td></tr><tr><td>

No mapping

</td><td>

status

</td></tr><tr><td>

No mapping

</td><td>

archiveSizeBytes

</td></tr><tr><td>

No mapping

</td><td>

diskSizeGb

</td></tr><tr><td>

image\_source

</td><td>

-   sourceDisk
-   sourceDiskId

</td></tr><tr><td rowspan="3">

Load Balancer \(cmdb\_ci\_cloud\_load\_balancer\)

</td><td>

object\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

No mapping

</td><td>

defaultService

</td></tr><tr><td rowspan="10">

Load Balancer Service \(cmdb\_ci\_lb\_service\)

</td><td>

object\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

pool

</td><td>

backends

</td></tr><tr><td>

port

</td><td>

port

</td></tr><tr><td>

listener\_protocol

</td><td>

protocol

</td></tr><tr><td>

No mapping

</td><td>

portName

</td></tr><tr><td>

No mapping

</td><td>

loadBalancingScheme

</td></tr><tr><td>

No mapping

</td><td>

sessionAffinity

</td></tr><tr><td>

No mapping

</td><td>

enableCDN

</td></tr><tr><td>

service\_type

</td><td>

Backend/Frontend

</td></tr><tr><td rowspan="9">

Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]

</td><td>

object\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

monitor\_type

</td><td>

type \(tcp/http/https\)

</td></tr><tr><td>

request\_path

</td><td>

requestPath

</td></tr><tr><td>

port

</td><td>

port

</td></tr><tr><td>

unhealthy\_threshold

</td><td>

unhealthyThreshold

</td></tr><tr><td>

healthy\_threshold

</td><td>

healthyThreshold

</td></tr><tr><td>

timeout\_sec

</td><td>

timeoutSec

</td></tr><tr><td>

check\_interval\_sec

</td><td>

checkIntervalSec

</td></tr><tr><td rowspan="3">

Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]

</td><td>

object\_id

</td><td>

Instance ID from GCP

</td></tr><tr><td>

name

</td><td>

instance.substring after the last'/'

</td></tr><tr><td>

Operational status

</td><td>

status

</td></tr><tr><td rowspan="2">

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td><td>

object\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td rowspan="6">

Network \[cmdb\_ci\_network\]

</td><td>

state

</td><td>

No mapping

</td></tr><tr><td>

cidr

</td><td>

IPv4Range

</td></tr><tr><td>

is\_external

</td><td>

No mapping

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

object\_id

</td><td>

items\_id

</td></tr><tr><td>

description

</td><td>

description

</td></tr><tr><td rowspan="3">

Network ACL \[cmdb\_ci\_network\_acl\]

</td><td>

object\_id

</td><td>

id

</td></tr><tr><td>

name

</td><td>

name

</td></tr><tr><td>

short\_description

</td><td>

description

</td></tr><tr><td rowspan="9">

Network ACL Rule \[cmdb\_ci\_network\_acl\_rule\]

</td><td>

is\_outbound \(True/False\)

</td><td>

ac

</td></tr><tr><td>

dest\_from\_port

</td><td>

No mapping

</td></tr><tr><td>

dest\_to\_port

</td><td>

No mapping

</td></tr><tr><td>

src\_from\_port

</td><td>

No mapping

</td></tr><tr><td>

src\_to\_port

</td><td>

No mapping

</td></tr><tr><td>

source\_ranges

</td><td>

sourceRanges

</td></tr><tr><td>

destination\_ranges

</td><td>

destinationRanges

</td></tr><tr><td>

target\_tags

</td><td>

targetTags

</td></tr><tr><td>

allowed\_traffic

</td><td>

allowed

</td></tr><tr><td rowspan="5">

Kubernetes Clusters \[cmdb\_ci\_kubernetes\_cluster\]

</td><td>

IP address

</td><td>

ip\_address

</td></tr><tr><td>

Name

</td><td>

name

</td></tr><tr><td>

Port

</td><td>

port

</td></tr><tr><td>

Kubernetes UID

</td><td>

k8s\_uid

</td></tr><tr><td>

Vendor

</td><td>

vendor

</td></tr></tbody>
</table>**Parent Topic:**[Cloud resource discovery](cloud-discovery-collected-data.md)

**Related topics**  


[Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](../../service-mapping/reference/gcp-cloud-discovery-patterns.md)

[Service Graph Connector for GCP](https://www.servicenow.com/docs/access?context=sgc-cmdb-integration-gcp&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

[Agent Client Collector for Visibility](../../agent-client-collector/concept/acc-visibility-landing-page.md)

