---
title: Fortinet FortiManager discovery requirements
description: Technical requirements and configuration details for discovering Fortinet FortiManager firewalls using the Firewall Audits and Reporting application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/fortinet-fortimanager-discovery-requirements.html
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-08-24"
reading_time_minutes: 8
keywords: [FortiManager, discovery, MID server, firewall]
breadcrumb: [Reference, Firewall Audits and Reporting, ITOM Visibility, IT Operations Management]
---

# Fortinet FortiManager discovery requirements

Technical requirements and configuration details for discovering Fortinet FortiManager firewalls using the Firewall Audits and Reporting application.

## Prerequisites

Before discovering Fortinet FortiManager firewalls, verify that the Firewall Audits and Reporting application is downloaded from ServiceNow Store and installed.

## Credentials and permissions

Discovery authenticates to FortiManager using an API key. Create a dedicated read-only user account on the FortiManager appliance and generate an API key for that user.

The read-only user account requires the following minimum permissions:

|Permission area|Required access|
|---------------|---------------|
|System status|Read|
|ADOM management|Read|
|Device manager|Read|
|Policy &amp; Objects|Read|
|Policy Package|Read|
|Global objects|Read|

Configure the FortiManager API key in ServiceNow as follows:

1.  Navigate to **Discovery** &gt; **Credentials** and create a new API Key credential record with the FortiManager API key value.
2.  Create a Credential Alias and associate it with the credential record.
3.  In the FortiManager serverless discovery schedule configuration, input the credential alias.

## MID Server configuration

The MID Server must have HTTPS \(TCP 443\) network access to the FortiManager management IP address. No agent is installed on FortiManager. All discovery is API-driven from the MID Server over HTTPS using the FortiManager JSON-RPC API.

## MID Server sizing

FortiManager environments can be large, with thousands of firewall objects and policies. The following sizing is recommended:

-   **JVM heap size:** Minimum 4 GB RAM per MID Server. Set **wrapper.java.maxmemory** to `4096` in the MID Server configuration.
-   **MID Server cluster:** Deploy a cluster of 3–4 MID Servers each configured with 4 GB JVM heap to distribute the discovery load across concurrent pattern executions. You can increase this allocation if you encounter memory issues even after following the above sizing recommendations.

**Warning:** Running FortiManager discovery on an undersized MID Server \(less than 4 GB JVM heap\) may result in out-of-memory errors or incomplete discovery, particularly for large deployments with many ADOMs and policy packages.

## API endpoints

All requests use POST to `https://<fortimanager-host>/jsonrpc` with a JSON body. Authentication uses the API key credential alias configured in ServiceNow Discovery.

Key API endpoints used during discovery:

|Resource|API URL \(in params.url\)|
|--------|-------------------------|
|FortiManager system status|/sys/status|
|Firewall policies|/pm/config/adom/\{\{adom\}\}/pkg/\{\{policy-package\}\}/firewall/policy|
|Global address objects|/pm/config/global/obj/firewall/address|
|Global address groups|/pm/config/global/obj/firewall/addrgrp|
|Global service objects|/pm/config/global/obj/firewall/service/custom|
|Global service groups|/pm/config/global/obj/firewall/service/group|
|Global VIP objects|/pm/config/global/obj/firewall/vip|
|Global VIP groups|/pm/config/global/obj/firewall/vipgrp|
|Global curated ISDB objects|/pm/config/global/obj/\_fdsdb/internet-service|
|Global custom ISDB objects|/pm/config/global/obj/firewall/internet-service-custom|
|ADOM list|/dvmdb/adom|
|Devices in ADOM|/dvmdb/adom/\{\{adom\}\}/device|
|Policy packages in ADOM|/pm/pkg/adom/\{\{adom\}\}|
|ADOM address objects|/pm/config/adom/\{\{adom\}\}/obj/firewall/address|
|ADOM address groups|/pm/config/adom/\{\{adom\}\}/obj/firewall/addrgrp|
|ADOM service objects|/pm/config/adom/\{\{adom\}\}/obj/firewall/service/custom|
|ADOM service groups|/pm/config/adom/\{\{adom\}\}/obj/firewall/service/group|
|ADOM VIP objects|/pm/config/adom/\{\{adom\}\}/obj/firewall/vip|
|ADOM VIP groups|/pm/config/adom/\{\{adom\}\}/obj/firewall/vipgrp|
|ADOM custom ISDB objects|/pm/config/adom/\{\{adom\}\}/obj/firewall/internet-service-custom|

## CMDB CI attributes populated

The FortiManager discovery pattern populates comprehensive attributes for all discovered CMDB Configuration Items. The following tables detail all attributes populated for each CI type.

|Attribute|Description|
|---------|-----------|
|Name|Display name of the FortiManager appliance|
|Serial Number|Hardware serial number used as the primary identifier|
|IP Address|Management IP address|
|Is Virtual|Whether the appliance is a virtual deployment|
|Platform Type|Hardware platform model type|
|Time Zone|Configured time zone of the appliance|
|High Availability Mode|HA mode: standalone, active-passive, or active-active|
|Hostname|Configured system hostname|
|ADOM Count|Number of Administrative Domains managed|
|Managed Device Count|Total number of managed FortiGate devices|
|ADOM Enabled|Whether the ADOM feature is enabled on this appliance|
|BIOS Version|BIOS firmware version|
|Build Number|Firmware build number|
|FIPS Mode Enabled|Whether FIPS compliance mode is active|
|Max ADOM|Maximum number of ADOMs supported by the license|
|Offline Mode Enabled|Whether the appliance is operating in offline mode|
|System Part Number|Hardware part number|

**Note:** Discovery populates firmware version information in the Firmware Installation \[cmdb\_firmware\_install\_list\] table instead of directly on the FortiManager CI.

|Attribute|Description|
|---------|-----------|
|Name|Display name of the Administrative Domain|
|UUID|Globally unique identifier|
|Device Count|Number of managed devices in this ADOM|
|Object ID|Unique path to this resource: /dvmdb/adom/\{name\}|
|ADOM Type|Product type restriction \(for example, fos for FortiOS/FortiGate\)|
|Target OS Version|FortiOS version that devices in this ADOM are expected to run|
|Policy Package Count|Number of policy packages within this ADOM|
|FortiManager|Reference to the parent FortiManager CI|
|Description|Administrator-assigned description|

|Attribute|Description|
|---------|-----------|
|Name|Device display name in FortiManager|
|Serial Number|Hardware serial number used as primary identifier|
|IP Address|Device management IP address|
|Manufacturer|Device manufacturer|
|Model ID|Reference to hardware model record \[cmdb\_model\]|
|Platform Family|Operating system type \(for example, fos\)|
|High Availability Role|HA cluster role: standalone, primary, or secondary|
|FortiManager|Reference to the managing FortiManager CI|
|VDOM Enabled|Whether virtual domains are enabled \(derived from maxvdom &gt; 1\)|
|Operational Status|Device operational state integer|

**Note:** Discovery populates firmware version information in the Firmware Installation \[cmdb\_firmware\_install\_list\] table instead of directly on the device CI.

|Attribute|Description|
|---------|-----------|
|Name|Policy package name|
|Object ID|Unique path: /pm/pkg/adom/\{adom\}/\{name\}|
|Policy Count|Number of policies in this package|
|Parent ADOM|Reference to the owning ADOM CI|
|FortiManager|Reference to the root FortiManager CI|
|Package Type|pkg \(active package\) or folder \(organizational container\)|

|Attribute|Description|
|---------|-----------|
|Name|Policy display name. Fallback: "Policy \{policyid\}" when name is empty|
|UUID|Primary identifier auto-generated by FortiOS|
|Policy ID|Integer policy ID within the package|
|Policy Enabled|Whether the policy is active|
|Last Hit|Timestamp of last traffic match|
|Object ID|Unique path: /pm/config/adom/\{adom\}/pkg/\{pkg\}/firewall/policy/\{policyid\}|
|Sequence Number|Rule evaluation order within the package|
|Policy Package|Reference to the parent Policy Package CI|
|Parent ADOM|Reference to the ADOM CI this policy belongs to|
|FortiManager|Reference to the root FortiManager CI|
|Action|Policy action: accept, deny, or ipsec|
|Source Interface|Ingress interface name\(s\), comma-joined|
|Destination Interface|Egress interface name\(s\), comma-joined|
|Source Address|Source address/group object names, comma-joined|
|Destination Address|Destination address/group/VIP object names, comma-joined|
|Source Services|Service/service-group object names, comma-joined|
|Policy Schedule|Schedule object name \(for example, always\)|
|ISDB Src Enabled|Whether Internet Service is used at the source|
|ISDB Dest Enabled|Whether Internet Service is used at the destination|
|NAT Enabled|Whether source NAT is applied|
|NAT IP|NAT IP pool name when ippool is enabled|
|Traffic Logging Mode|Log level: disable, utm, or all|
|Traffic Session Logging Enabled|Whether session start events are logged|
|UTM/Security Profile Enabled|True when any UTM profile \(AV, IPS, SSL\) is applied|
|AV Profile|Antivirus profile name applied to this rule|
|IPS Sensor|IPS sensor profile name applied to this rule|
|SSL/SSH Profile|Deep inspection profile name|
|Description|Free-text description and change audit trail|

## Non-CMDB firewall object attributes populated

The following tables detail attributes populated for non-CMDB firewall object tables. All tables inherit common base attributes: Object ID, UUID, Name, Description, Discovery Source, Parent ADOM, and FortiManager reference.

|Attribute|Description|
|---------|-----------|
|Address Type|Type of address: ipmask, iprange, fqdn, wildcard, geography, or dynamic|
|Subnet|IP address and mask \(present when type = ipmask\)|
|Start IP|Start of IP range \(present when type = iprange\)|
|End IP|End of IP range \(present when type = iprange\)|
|Fully Qualified Domain Name|FQDN string \(present when type = fqdn\)|
|Geography|ISO country code\(s\) \(present when type = geography\)|
|Associated Interface|Interface this address is bound to. "any" indicates all interfaces|

|Attribute|Description|
|---------|-----------|
|Member Names|Comma-joined list of member address/group names|
|Member Count|Number of members in the group|
|Exclude Members|Comma-joined exclude-member list when exclusion mode is active|

|Attribute|Description|
|---------|-----------|
|Protocol|Layer-4 protocol type: ICMP, IP, TCP/UDP/SCTP, or ICMP6|
|TCP Port Range|Space-separated TCP ports/ranges \(present when protocol includes TCP\)|
|UDP Port Range|Space-separated UDP ports/ranges|
|SCTP Port Range|Space-separated SCTP ports/ranges|
|ICMP Type|ICMP type number \(present when protocol = ICMP\)|
|Service Category|Comma-separated category names this service belongs to|

|Attribute|Description|
|---------|-----------|
|Member Names|Comma-joined list of service member names|
|Member Count|Number of service members in the group|
|Proxy Enabled|Whether this is a proxy-mode service group|

|Attribute|Description|
|---------|-----------|
|VIP Type|Type of VIP: static-nat, server-load-balance, fqdn, or dns-translation|
|External IP|Public-facing IP that clients connect to \(before NAT\)|
|External Interface|Interface where inbound traffic arrives \(for example, wan1, any\)|
|Mapped Address|Internal real server IP or FQDN that traffic is forwarded to after DNAT|
|Port Forward Enabled|Whether port translation is applied in addition to IP translation|
|Active|Whether this VIP is active and processing traffic|
|NAT44 Enabled|Whether IPv4-to-IPv4 NAT is enabled|

|Attribute|Description|
|---------|-----------|
|External Interface|External interface all member VIPs are associated with|
|Member Names|Comma-joined list of member VIP object names|
|Member Count|Number of VIP members in the group|

|Attribute|Description|
|---------|-----------|
|Reputation Score|Threat reputation score for this internet service entry|

|Attribute|Description|
|---------|-----------|
|Firewall Policy|Reference to the Firewall Policy CI \[cmdb\_ci\_firewall\_sec\_policy\]. Cascade delete enabled.|
|Firewall Object|Reference to the base firewall object record \[sn\_disco\_firewall\_object\]. Cascade delete enabled.|
|Reference Type|Which policy field referenced this object: srcaddr, dstaddr, or service|
|Discovery Source|Source system that populated this record|

## Relationships created

Discovery establishes the following CMDB relationships between discovered Configuration Items:

|Parent CI|Relationship Type|Child CI|
|---------|-----------------|--------|
|FortiManager Network Manager|Manages::Managed By|Fortinet Firewall ADOM|
|Fortinet Firewall ADOM|Members::Member Of|Fortinet Firewall Device|
|Fortinet Firewall ADOM|Contains::Contained By|Fortinet Firewall Policy Package|
|Fortinet Firewall Policy Package|Used By::Uses|Fortinet Firewall Device|
|Fortinet Firewall Policy Package|Contains::Contained By|Fortinet Firewall Policy|

## Discovery pattern

The FortiManager discovery uses a serverless Large Payload Pattern \(LP\). The pattern name is **Fortinet FortiManager \(LP\)**.

Discovery consists of one serverless root pattern that triggers multiple independent Large Payload Patterns for global objects, ADOMs, devices, policy packages, and firewall policies.

**Parent Topic:**[Firewall Audits and Reporting reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/firewall-audit-report-reference.md)

