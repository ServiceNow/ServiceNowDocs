---
title: Supported hardware service graph connectors for Security Posture Control
description: Supported Hardware service graph connectors with CI class, source \(product\), and tool categories. This list is not complete and is subject to change with the addition of more products.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Security Posture Control, Security Operations]
---

# Supported hardware service graph connectors for Security Posture Control

Supported Hardware service graph connectors with CI class, source \(product\), and tool categories. This list is not complete and is subject to change with the addition of more products.

For Discovery source for a connector listed, 'SG', 'SGO', or 'SGC' precedes the product name for third-party products, for example, SG-AWS, SGO-Datadog, or SGC-AD \(Active Directory\). For ServiceNow products, 'SN' or 'ServiceNow' precedes the product name, for example, SNAssetManagement for ServiceNow Hardware Asset Management.

After you install them, you can view the connectors and their categories on the connector table \[sn\_sec\_spc\_core\_connector\] in your instance.

You can view Asset types and how they map to CI classes and Connectors on the \[sn\_sec\_spc\_core\_asset\_type\_connector\] table.

|Asset type|CI class|Asset source|Connector category|
|----------|--------|------------|------------------|
|Hardware Asset|cmdb\_ci\_computer|Active Directory|Directory Services|
|Hardware Asset|cmdb\_ci\_server|AppDynamics|Application Performance Monitoring|
|Hardware Asset|cmdb\_ci\_server|Automox|Configuration and Patch Management|
|Hardware Asset|cmdb\_ci\_computer|Automox|Configuration and Patch Management|
|Hardware Asset|cmdb\_ci\_computer|BigFix|Configuration and Patch Management|
|Hardware Asset|cmdb\_ci\_server|BigFix|Configuration and Patch Management|
|Hardware Asset|cmdb\_ci\_printer|Cisco Meraki|Networking|
|Hardware Asset|cmdb\_ci\_server|Cisco Meraki|Networking|
|Hardware Asset|cmdb\_ci\_iot|Cisco Meraki|Networking|
|Hardware Asset|cmdb\_ci\_hc\_device|Cisco Meraki|Networking|
|Hardware Asset|cmdb\_ci\_netgear|Cisco Meraki|Networking|
|Hardware Asset|cmdb\_ci\_computer|Cisco Meraki|Networking|
|Hardware Asset|cmdb\_ci\_server|CrowdStrike|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_server|Datadog|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_server|Dynatrace|Application Performance Monitoring|
|Hardware Asset|cmdb\_ci\_computer|Dynatrace|Application Performance Monitoring|
|Hardware Asset|cmdb\_ci\_computer|ExtraHop Reveal\(x\)|Network Security|
|Hardware Asset|cmdb\_ci\_hc\_device|ExtraHop Reveal\(x\)|Network Security|
|Hardware Asset|cmdb\_ci\_server|ExtraHop Reveal\(x\)|Network Security|
|Hardware Asset|cmdb\_ci\_iot|ExtraHop Reveal\(x\)|Network Security|
|Hardware Asset|cmdb\_ci\_printer|ExtraHop Reveal\(x\)|Network Security|
|Hardware Asset|cmdb\_ci\_iot|Forescout|Network Security|
|Hardware Asset|cmdb\_ci\_hc\_device|Forescout|Network Security|
|Hardware Asset|cmdb\_ci\_computer|Forescout|Network Security|
|Hardware Asset|cmdb\_ci\_server|Forescout|Network Security|
|Hardware Asset|cmdb\_ci\_printer|Forescout|Network Security|
|Hardware Asset|cmdb\_ci\_server|Intune|Endpoint Management|
|Hardware Asset|cmdb\_ci\_computer|Intune|Endpoint Management|
|Hardware Asset|cmdb\_ci\_printer|Jamf Pro|Endpoint Management|
|Hardware Asset|cmdb\_ci\_server|Jamf Pro|Endpoint Management|
|Hardware Asset|cmdb\_ci\_computer|Jamf Pro|Endpoint Management|
|Hardware Asset|cmdb\_ci\_server|Lansweeper|IT Asset Management|
|Hardware Asset|cmdb\_ci\_computer|Lansweeper|IT Asset Management|
|Hardware Asset|cmdb\_ci\_printer|Lansweeper|IT Asset Management|
|Hardware Asset|cmdb\_ci\_hc\_device|LogicMonitor|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_printer|LogicMonitor|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_server|LogicMonitor|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_vm\_instance|LogicMonitor|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_iot|LogicMonitor|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_computer|LogicMonitor|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_netgear|LogicMonitor|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_server|Microsoft Defender|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_server|New Relic|Application Performance Monitoring|
|Hardware Asset|cmdb\_ci\_computer|Nexthink|Digital Employee Experience|
|Hardware Asset|cmdb\_ci\_computer|Netskope|Data Loss Prevention|
|Hardware Asset|cmdb\_hardware\_product\_model|Netskope|Data Loss Prevention|
|Hardware Asset|cmdb\_ci\_network\_adapter|Netskope|Data Loss Prevention|
|Hardware Asset|cmdb\_software\_instance|Netskope|Data Loss Prevention|
|Hardware Asset|cmdb\_sam\_sw\_install|Netskope|Data Loss Prevention|
|Hardware Asset|sn\_sec\_sgc\_netskop\_client\_attribute|Netskope|Data Loss Prevention|
|Hardware Asset|cmdb\_ci\_server|Open Telemetry|Application Performance Monitoring|
|Hardware Asset|cmdb\_ci\_computer|Puppet|Configuration and Patch Management|
|Hardware Asset|cmdb\_ci\_server|Puppet|Configuration and Patch Management|
|Hardware Asset|cmdb\_ci\_computer|Qualys|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_server|Qualys|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_vm\_instance|Qualys-ServiceNow|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_server|Qualys-ServiceNow|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_hardware|Rapid7|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_computer|SCCM|Configuration and Patch Management|
|Hardware Asset|cmdb\_ci\_server|SCCM|Configuration and Patch Management|
|Hardware Asset|cmdb\_ci\_printer|ScienceLogic|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_iot|ScienceLogic|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_server|ScienceLogic|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_computer|ScienceLogic|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_hc\_device|ScienceLogic|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_vm\_instance|ScienceLogic|Infrastructure Monitoring|
|Hardware Asset|cmdb\_ci\_hardware|ServiceNow HAM|Hardware Asset Management|
|Hardware Asset|cmdb\_ci\_hardware|ServiceNow ITOM Discovery|Discovery|
|Hardware Asset|cmdb\_ci\_aws\_datacenter|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_azure\_datacenter|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_availability\_zone|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_google\_datacenter|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_cloud\_service\_account|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_cloud\_subnet|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_compute\_template|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_network|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_vm\_instance|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_key\_value|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_os\_template|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_server|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_computer|SentinelOne|Endpoint Protection|
|Hardware Asset|sn\_sec\_sgc\_sntlone\_asset\_tags|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_ip\_address|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_network\_adapter|SentinelOne|Endpoint Protection|
|Hardware Asset|sn\_sec\_sgc\_sntlone\_additonal\_attributes|SentinelOne|Endpoint Protection|
|Hardware Asset|cmdb\_ci\_server|Tanium Asset|Endpoint Management|
|Hardware Asset|cmdb\_ci\_computer|Tanium Asset|Endpoint Management|
|Hardware Asset|cmdb\_ci\_ups|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_industrial\_sensor|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_cnc|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_hardware|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_netgear|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_industrial\_actuator|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ip\_switch|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_hub\_network|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_security|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_server|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_rtu|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_ews|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_plc|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_control|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_dcs|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_storage\_server|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_hmi|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_control\_module|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_industrial\_robot|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_historian|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_industrial\_drive|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_iot|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ip\_firewall|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_computer|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_unclassed\_hardware|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ids\_network|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_ot\_ied|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_printer|Tenable|Vulnerability Assessment|
|Hardware Asset|cmdb\_ci\_computer|VMWare Workspace ONE UEM|Endpoint Management|
|Hardware Asset|cmdb\_ci\_server|VMWare Workspace ONE UEM|Endpoint Management|
|Hardware Asset|cmdb\_ci\_printer|VMWare Workspace ONE UEM|Endpoint Management|
|Hardware Asset|cmdb\_ci\_vm\_instance|Wiz|Cloud Native Application Protection Platform|
|Hardware Asset|cmdb\_ci\_server|Wiz|Cloud Native Application Protection Platform|
|Hardware Asset|cmdb\_ci\_linux\_server|Wiz|Cloud Native Application Protection Platform|
|Hardware Asset|cmdb\_ci\_win\_server|Wiz|Cloud Native Application Protection Platform|

