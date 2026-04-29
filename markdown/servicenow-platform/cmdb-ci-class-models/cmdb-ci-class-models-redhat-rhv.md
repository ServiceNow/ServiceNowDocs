---
title: Red Hat Virtualization \(RHV\) extension classes
description: The CMDB CI Class Models app adds or updates classes for Red Hat Virtualization \(RHV\) OLVM or RHV.
locale: en-US
release: australia
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CMDB CI class models, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Red Hat Virtualization \(RHV\) extension classes

The CMDB CI Class Models app adds or updates classes for Red Hat Virtualization \(RHV\) OLVM or RHV.

CMDB CI Class Models is a ServiceNow Store app that adds class models that extend the CMDB class hierarchy. The new or updated classes include class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

Starting with version 1.28.0, Discovery and Service Mapping Patterns supports both OLVM and RHV discovery. For more information, see [Oracle Linux Virtualization Manager and Red Hat Virtualization discovery](https://www.servicenow.com/docs/access?context=red-hat-virtualization-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US). The RHV patterns, tables, and related items have been renamed to oVirt.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Red Hat Virtualization \(RHV\)

Red Hat Virtualization \(RHV\) is a virtualization product that is based on the Kernel-based Virtual Machine \(KVM\) hypervisor. RHV uses the SPICE protocol and Virtual Desktop Server Manager \(VDSM\) with an RHEL centralized management server. The RHV solution is based on two primary software components: Red Hat Virtualization Manager \(RHV-M\) and Red Hat Virtualization Hypervisors or hosts: Red Hat Enterprise Linux or RHV Host \(RHV-H\).

**Note:** The Discovery application uses patterns to find RHV components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store. For more information, see [Oracle Linux Virtualization Manager and Red Hat Virtualization discovery](https://www.servicenow.com/docs/access?context=red-hat-virtualization-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

![Red Hat Virtualization class model.](../image/CIClassModels1.5.0l.png "RHV classes integrated with the CMDB class hierarchy")

## Classes

This section lists the classes that the CMDB CI Class Models app adds or updates. See the class columns table for further details about the columns added for each class.

CMDB CI Class Models: Release 1.8.0 adds the following classes for RHV. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

<table id="table_ghd_qtj_tkb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

RHV LDC\[cmdb\_ci\_rhv\_ldc\]

</td><td>

Logical Datacenter\[cmdb\_ci\_logical\_datacenter\]

</td><td>

RHV logical datacenter.

</td></tr><tr><td>

RHV Datacenter \[cmdb\_ci\_rhv\_datacenter\]

 This class is deleted.

</td><td>

N/A

</td><td>

N/A

</td></tr></tbody>
</table>CMDB CI Class Models: Release 1.6.0 adds the following classes for RHV.

<table id="table_x53_n4v_phb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

RHV Server\[cmdb\_ci\_rhv\_server\]

</td><td>

Virtualization Server\[cmdb\_ci\_virtualization\_server\]

</td><td>

The RHV virtualization host.

</td></tr><tr><td>

RHV Object\[cmdb\_ci\_rhv\_object\]

</td><td>

Virtual Machine Object\[cmdb\_ci\_vm\_object\]

</td><td>

A base class for other classes to derive from.

</td></tr><tr><td>

RHV Manager\[cmdb\_ci\_rhv\_manager\]

</td><td>

Application\[cmdb\_ci\_appl\]

</td><td>

RHV Manager instance.

</td></tr><tr><td>

RHV Cluster\[cmdb\_ci\_rhv\_cluster\]

</td><td>

RHV Object\[cmdb\_ci\_rhv\_object\]

</td><td>

RHV cluster.

</td></tr><tr><td>

RHV Datacenter\[cmdb\_ci\_rhv\_datacenter\]

 **Note:** This class is being deleted in the CMDB CI Class Models 1.6.0 release.

</td><td>

RHV Object\[cmdb\_ci\_rhv\_object\]

</td><td>

RHV datacenter.

</td></tr><tr><td>

RHV Virtual Machine Instance\[cmdb\_ci\_rhv\_vm\_instance\]

</td><td>

Virtual Machine Instance\[cmdb\_ci\_vm\_instance\]

</td><td>

RHV virtual machine instance.

</td></tr></tbody>
</table>## Class columns

CMDB CI Class Models: Release 1.6.0 adds the following columns to the respective classes.

|Added columns|Description|
|-------------|-----------|
|url|URL used to access the object.|

|Added columns|Description|
|-------------|-----------|
|href\_id|Href ID.|
|manager\_id|Manager ID.|
|url|URL to access the object \(used in child classes\).|

|Added columns|Description|
|-------------|-----------|
|url|URL of the manager.|
|product\_name|Product name.|

|Added columns|Description|
|-------------|-----------|
|cpu\_type|CPU type.|
|cpu\_architecture|CPU architecture.|
|ksm|Enabled state of kernel same-page merging \(KSM\) memory policy.|
|fencing\_policy|Fencing policy.|
|memory\_overcommitment|Amount of over-commitment memory allowed on the cluster.|
|transparent\_huge\_pages|Transparent huge memory pages policy.|
|ballooning|Memory ballooning for guests.|
|compatibility\_version|Compatibility version.|

|Added columns|Description|
|-------------|-----------|
|mgmt\_url|Management URL.|
|cpu\_architecture|CPU architecture.|
|delete\_protected|Delete protected \(true/false\).|
|ha\_priority|HA priority.|
|high\_availability|High availability \(true/false\).|
|memory\_policy\_guaranteed|Amount of memory guaranteed \(MB\).|
|memory\_policy\_max\_mb|Maximum memory in the dynamic memory allocation policy.|
|multi\_queues|Multi queues.|
|placement\_policy|Placement policy.|
|cpu\_sockets|Number of CPU sockets.|
|stateless|Stateless \(true/false\).|
|storage\_error\_resume\_behaviour|Behavior of a virtual machine that is paused due to storage I/O error. For examples, AUTO\_RESUME, LEAVE\_PAUSED, and KILL.|
|start\_time|Start time.|
|stop\_time|Stop time.|
|threads|Number of threads.|
|time\_zone|Time zone.|
|usb|USB enabled state.|
|run\_once|Run once.|
|type|RHV type.|

The following class was deleted in the CMDB CI Class Models 1.6.0 release.

|Added columns|Description|
|-------------|-----------|
|quota\_mode|Quota mode policy.|

**Related topics**  


[Oracle Linux Virtualization Manager and Red Hat Virtualization discovery](https://www.servicenow.com/docs/access?context=red-hat-virtualization-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

[CMDB schema model](c_ConfigurationManagementDatabase.md)

