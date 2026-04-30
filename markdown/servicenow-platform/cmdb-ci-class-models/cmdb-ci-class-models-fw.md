---
title: Firewall extension classes
description: The CMDB CI Class Models store app adds or updates classes for firewall devices.
locale: en-US
release: yokohama
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Firewall extension classes

The CMDB CI Class Models store app adds or updates classes for firewall devices.

The CMDB CI Class Models app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Firewalls

A firewall is a network security system that, based on security policies, monitors and controls incoming and outgoing network traffic. Firewalls typically form a barrier between an internal network and an untrusted external network such as the internet. It usually consists of security policies that help secure an organization from external threats and cyberattacks. Firewall vendors may provide a centralized firewall manager to manage many firewall devices and the security policies residing on them. For example, Panorama™ is the centralized management system for Palo Alto Networks firewalls.

![Firewall extension classes integrated with the CMDB class hierarchy.](../image/cmdb-ci-class-model-fw-palo-alto-cisco.png "Firewall extension classes integrated with the CMDB class hierarchy (CMDB CI Class Models: Release 1.11.0)")

![Firewall extension classes integrated with the CMDB class hierarchy.](../image/cmdb_ci_class_model_fw.png "Firewall extension classes integrated with the CMDB class hierarchy (CMDB CI Class Models: Release 1.10.0)")

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates.See the class columns table for further details about the columns added for each class. CMDB CI Class Models: Release 1.10.0 adds or updates the following classes for the discovery of network firewall devices. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

<table id="table_kbv_s5d_dlb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP Firewall \[cmdb\_ci\_ip\_firewall\]

</td><td>

NETGEAR \[cmdb\_ci\_netgear\]

</td><td>

Contains all network firewalls.

</td></tr><tr><td>

Firewall Device \[cmdb\_ci\_firewall\_device\]

</td><td>

IP Firewall \[cmdb\_ci\_ip\_firewall\]

</td><td>

Network security system that monitors and controls incoming and outgoing network traffic, based on security policies.

</td></tr><tr><td>

Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]

</td><td>

Firewall Device \[cmdb\_ci\_firewall\_device\]

</td><td>

Fortinet firewall device.

</td></tr><tr><td>

Fortinet Firewall Interface \[cmdb\_ci\_fortinet\_firewall\_interface\]

</td><td>

Network Interface \[cmdb\_ci\_ni\_interface\]

</td><td>

Discovered by the Next Generation Fortinet Network Firewall - REST pattern. See [Fortinet firewall and FortiGate VDOM REST-based discovery](https://www.servicenow.com/docs/access?context=fortinet-fw-vdoms-rest-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

</td></tr><tr><td>

Fortinet Firewall Policy \[cmdb\_ci\_fortinet\_firewall\_policy\]

</td><td>

Firewall Security Policy \[cmdb\_ci\_firewall\_sec\_policy\]

</td><td>

Discovered by the Next Generation Fortinet Network Firewall - REST pattern. See [Fortinet firewall and FortiGate VDOM REST-based discovery](https://www.servicenow.com/docs/access?context=fortinet-fw-vdoms-rest-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

</td></tr><tr><td>

Fortinet Virtual Domain \[cmdb\_ci\_fortinet\_vdom\]

</td><td>

IP Firewall \[cmdb\_ci\_ip\_firewall\]

</td><td>

Discovered by the Next Generation Fortinet Network Firewall - REST pattern. See [Fortinet firewall and FortiGate VDOM REST-based discovery](https://www.servicenow.com/docs/access?context=fortinet-fw-vdoms-rest-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

</td></tr><tr><td>

Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]

</td><td>

Firewall Device \[cmdb\_ci\_firewall\_device\]

</td><td>

Juniper firewall device.

</td></tr><tr><td>

Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\]

</td><td>

CMDB CI \[cmdb\_ci\]

</td><td>

Group of firewall devices.

</td></tr><tr><td>

Panorama Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\_panorama\]

</td><td>

Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\]

</td><td>

Group of Panorama firewall devices.

</td></tr><tr><td>

Palo Alto Firewall Device \[cmdb\_ci\_firewall\_device\_palo\_alto\]

</td><td>

Firewall Device \[cmdb\_ci\_firewall\_device\]

</td><td>

Palo Alto firewall device.

</td></tr><tr><td>

Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]

</td><td>

\[cmdb\_ci\_cluster\]

</td><td>

Group of firewall nodes that work as a single logical entity.

</td></tr><tr><td>

Fortinet Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_fortinet\]

</td><td>

Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]

</td><td>

Fortinet firewall cluster.

</td></tr><tr><td>

Juniper Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_juniper\]

</td><td>

Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]

</td><td>

Juniper firewall cluster.

</td></tr><tr><td>

Firewall Manager \[cmdb\_ci\_firewall\_manager\]

</td><td>

CMDB CI \[cmdb\_ci\]

</td><td>

System that provides centralized management for many firewall devices and the security policies residing on them.

</td></tr><tr><td>

Panorama Firewall Manager \[cmdb\_ci\_firewall\_manager\_panorama\]

</td><td>

Firewall Manager \[cmdb\_ci\_firewall\_manager\]

</td><td>

The centralized network security management tool for Palo Alto Networks firewalls.

</td></tr><tr><td>

Firewall Security Policy \[cmdb\_ci\_firewall\_sec\_policy\]

</td><td>

CMDB CI \[cmdb\_ci\]

</td><td>

The security policy that the firewall device enforces.

</td></tr><tr><td>

Panorama Firewall Security Policy \[cmdb\_ci\_firewall\_sec\_policy\_panorama\]

</td><td>

Firewall Security Policy \[cmdb\_ci\_firewall\_sec\_policy\]

</td><td>

The security policy that the Panorama firewall device enforces.

</td></tr></tbody>
</table>CMDB CI Class Models: Release 1.12.0 adds the following class for the discovery of network firewall devices.

|Class|Extends|Description|
|-----|-------|-----------|
|Cisco Firewall Device \[cmdb\_ci\_firewall\_device\_cisco\]|Firewall Device \[cmdb\_ci\_firewall\_device\]|All Cisco Firewall devices.|

## Class columns

CMDB CI Class Models: Release 1.10.0 adds the following columns to the respective classes.

|Added columns|Description|
|-------------|-----------|
|Hardware Operating System|OS running on the hardware.|
|Hardware OS Version|OS version running on the hardware.|

|Added columns|Description|
|-------------|-----------|
|Hardware Operating System|OS running on the hardware.|
|Hardware OS Version|OS version running on the hardware.|

CMDB CI Class Models: Release 1.12.0 adds no columns to the existing classes.

**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

