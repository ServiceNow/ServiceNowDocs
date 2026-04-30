---
title: Service Graph Connector for Qualys APIs
description: Data from the Qualys data source fields is imported with the Global Asset API and the Asset Management and Tagging API.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Qualys, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for Qualys APIs

Data from the Qualys data source fields is imported with the Global Asset API and the Asset Management and Tagging API.

Global Asset API

-   A Qualys Cybersecurity Asset Management \(CSAM\) license is required.
-   Asset information includes details such as Hardware Category and OS Category.

Asset Management and Tagging API

-   A CSAM license is not required
-   Asset information does not include details about Hardware Category and OS Category.

## Mapped attributes

The following table compares what data is imported by the two APIs. The sections after the table list data imported by the Global asset API that is not supported by the Asset Management and Tagging API.

<table id="table_h3z_1qx_c1c"><thead><tr><th>

Global Asset API

</th><th>

Asset Management and Tagging API

</th></tr></thead><tbody><tr><td>

Mapped attributesassetId

assetUUID

hostId

lastModifiedDate

agentId

createdDate

sensorLastUpdatedDate

assetType

address

dnsName

assetName

netbiosName

timeZone

biosDescription

lastBoot

totalMemory

cpuCount

lastLoggedOnUser

domainRole

hwUUID

biosSerialNumber

biosAssetTag

isContainerHost

</td><td>

Mapped attributescreated

name

dnsHostName

fqdn

os

manufacturer

tracking method

netbios

timezone

network guid

IsDockerHost

modified

lastVulnScan

model

cloudProvider

type

qwebHostId

criticalSocre

lastSystemBoot

domain

lastLogOnUser

lastComplianceScan

</td></tr><tr><td>

AWS Cloud detailsaccountId

availabilityZone

hasAgent

hostname

imageId

instanceId

instanceState

privateDNS

privateIpAddress

instanceType

qualysScanner

kernelId

launchdate

region.code

region.name

spotInstance

subnetId

vpcId

tags.key

tags.value

</td><td>

AWS Cloud detailsinstanceId

privateDnsName

privateIpAddress

instanceState

monitoringEnabled

region

accountId

availabilityZone

instance\_type

AWS Cloud tag details

-   key
-   value

</td></tr><tr><td>

MS Azure Cloud detailsvmId

state

name

imagePublisher

imageVersion

offer

location

platform

resourceGroupName

size

subnet

subscriptionId

virtualNetwork

</td><td>

MS Azure Cloud detailsresourceGroupName

vmId

state

subscriptionId

location

image\_id

publisher

version

offer

vm\_size

subnet\_id

vpc\_id

MS Azure Cloud tag details

-   key
-   value

</td></tr><tr><td>

Network interface detailshostname

addressIpV4

addressIpV6

macAddress

interfaceName

dnsAddress

gatewayAddress

manufacturer

macVendorIntroDate

netmask

addresses

</td><td>

Network interface detailsaddress

host\_name

interface\_name

macAddress

gatewayAddress

interface\_id

type

</td></tr><tr><td>

Software detailstoken1

token2

uniqueKey

publisher

installDate

id

installPath

lastUseDate

authorization

authorizationDetectionScore

</td><td>

Software detailsversion

name

</td></tr><tr><td>

Volume detailsname

free

size

</td><td>

Volume detailsname

free

size

</td></tr><tr><td>

Open port detailsport

description

protocol

detectedService

firstFound

lastUpdated

</td><td>

Open port detailsport

protocol

serviceName

service\_id

</td></tr><tr><td>

Processor detailsdescription

speed

numCPUs

noOfSocket

threadsPerCore

coresPerSocket

multithreadingStatus

</td><td>

Processor detailsname

speed

</td></tr><tr><td>

Tag detailstagId

tagName

foregroundColor

backgroundColor

businessImpact

criticalityScore

</td><td>

Asset tag detailsid

name

</td></tr><tr><td>

Agent detailsversion

configurationProfile

activations

connectedFrom

lastActivity

lastCheckedIn

lastInventory

udcManifestAssigned

errorStatus

</td><td>

Agent detailsagentVersion

agentLastCheckIn

status

platform

connectedFrom

agentId

AgentConfigurationName

ChirpStatus

</td></tr></tbody>
</table>## Additional Global asset API details

The following sections list data imported by the Global asset API that is not supported by the Asset Management and Tagging API.

## Global asset API OS details

-   fullName
-   version
-   publisher
-   osName
-   category
-   category1
-   category2
-   productName
-   edition
-   marketVersion
-   update
-   architecture
-   productUrl
-   productFamily
-   installDate
-   release

## Global asset API OS lifecycle

OS lifecycle details

-   gaDate
-   eolDate
-   eosDate
-   stage
-   lifeCycleConfidence
-   eolSupportStage
-   eosSupportStage

## Global asset API OS taxonomy

OS Taxonomy details

-   id
-   name
-   category1
-   category2

## Global asset API hardware

Hardware details

-   fullName
-   category
-   category1
-   category2
-   manufacturer
-   productName
-   model
-   productUrl
-   productFamily

## Global asset API hardware lifecycle

Hardware lifecycle details

-   introDate
-   gaDate
-   eosDate
-   obsoleteDate
-   stage
-   lifeCycleConfidence

## Global asset API taxonomy

Hardware taxonomy details

-   id
-   name
-   category1
-   category2

## Global asset API sensor

Sensor details

-   activatedForModules
-   pendingActivationForModules
-   lastVMScan
-   lastComplianceScan
-   lastFullScan
-   lastVmScanDateScanner
-   lastVmScanDateAgent
-   lastPcScanDateScanner
-   lastPcScanDateAgent
-   firstEasmScanDate
-   lastEasmScanDate

## Global asset API service

Service details

-   name
-   status
-   description

## Global asset API last location

Last location details

-   city
-   state
-   country
-   name
-   continent
-   postal

## Global asset API criticality

Criticality details

-   score
-   isDefault
-   lastUpdated

## Global asset API processor

Processor details

-   description
-   speed
-   numCPUs
-   noOfSocket
-   threadsPerCore
-   coresPerSocket
-   multithreadingStatus

## Global asset API business information

Business information details

-   businessAppListData
-   riskScore
-   passiveSensor
-   domain
-   subdomain
-   missingSoftware
-   whois
-   organizationName
-   isp
-   asn
-   easmTags
-   hostingCategory1
-   customAttributes

