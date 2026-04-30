---
title: Firewall extension classes
description: The CMDB CI Class Models store app adds or updates classes for firewall devices.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Firewall extension classes

The CMDB CI Class Models store app adds or updates classes for firewall devices.

The app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships \(if applicable\). You can use the added classes as any other CMDB class. Applications such as Discovery and Service Mapping patterns can use these class extensions to populate CIs and discover various technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Firewalls

A firewall is a network security system that monitors and controls incoming and outgoing network traffic, based on security policies. Firewalls typically form a barrier between an internal network and an untrusted external network, such as the internet. It usually consists of security policies that help secure an organization from external threats and cyber attacks. Firewall vendors may provide a centralized firewall manager to manage many firewall devices and the security policies residing on them. For example, Panorama™ is the centralized management system for Palo Alto Networks firewalls.

![Firewall extension classes integrated with the CMDB class hierarchy.](../image/cmdb-ci-class-model-fw-palo-alto-cisco.png "Firewall extension classes integrated with the CMDB class hierarchy (CMDB CI Class Models: Release 1.11.0)")

![Firewall extension classes integrated with the CMDB class hierarchy.](../image/cmdb_ci_class_model_fw.png "Firewall extension classes integrated with the CMDB class hierarchy (CMDB CI Class Models: Release 1.10.0)")

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates.

CMDB CI Class Models: Release 1.10.0 adds or updates the following classes for the discovery of network firewall devices. For the list of CMDB classes in a base system, including ones that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

|Class|Extends|Description|
|-----|-------|-----------|
|IP Firewall \[cmdb\_ci\_ip\_firewall\]|NETGEAR \[cmdb\_ci\_netgear\]|Contains all network firewalls.|
|Firewall Device \[cmdb\_ci\_firewall\_device\]|IP Firewall \[cmdb\_ci\_ip\_firewall\]|Network security system that monitors and controls incoming and outgoing network traffic, based on security policies.|
|Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]|Firewall Device \[cmdb\_ci\_firewall\_device\]|Fortinet firewall device.|
|Juniper Firewall Device \[cmdb\_ci\_firewall\_device\_juniper\]|Firewall Device \[cmdb\_ci\_firewall\_device\]|Juniper firewall device.|
|Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\]|CMDB CI \[cmdb\_ci\]|Group of firewall devices.|
|Panorama Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\_panorama\]|Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\]|Group of Panorama firewall devices.|
|Palo Alto Firewall Device \[cmdb\_ci\_firewall\_device\_palo\_alto\]|Firewall Device \[cmdb\_ci\_firewall\_device\]|Palo Alto firewall device.|
|Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]|\[cmdb\_ci\_cluster\]|Group of firewall nodes that work as a single logical entity.|
|Fortinet Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_fortinet\]|Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]|Fortinet firewall cluster.|
|Juniper Firewall Cluster \[cmdb\_ci\_firewall\_cluster\_juniper\]|Firewall Cluster \[cmdb\_ci\_firewall\_cluster\]|Juniper firewall cluster.|
|Firewall Manager \[cmdb\_ci\_firewall\_manager\]|CMDB CI \[cmdb\_ci\]|System that provides centralized management for many firewall devices and the security policies residing on them.|
|Panorama Firewall Manager \[cmdb\_ci\_firewall\_manager\_panorama\]|Firewall Manager \[cmdb\_ci\_firewall\_manager\]|The centralized network security management tool for Palo Alto Networks firewalls.|
|Firewall Security Policy \[cmdb\_ci\_firewall\_sec\_policy\]|CMDB CI \[cmdb\_ci\]|The security policy that the firewall device enforces.|
|Panorama Firewall Security Policy \[cmdb\_ci\_firewall\_sec\_policy\_panorama\]|Firewall Security Policy \[cmdb\_ci\_firewall\_sec\_policy\]|The security policy that the Panorama firewall device enforces.|

CMDB CI Class Models: Release 1.12.0 adds the following class for the discovery of network firewall devices.

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

