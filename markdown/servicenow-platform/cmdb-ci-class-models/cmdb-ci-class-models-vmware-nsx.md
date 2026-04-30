---
title: VMware NSX load balancer extension classes
description: The CMDB CI Class Models store app adds or updates classes for VMware NSX load balancers.
locale: en-US
release: yokohama
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# VMware NSX load balancer extension classes

The CMDB CI Class Models store app adds or updates classes for VMware NSX load balancers.

The CMDB CI Class Models app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## VMware NSX load balancer

NSX is a network virtualization solution offered by VMware. Among the virtual resources included in the NSX solution are virtual LANs \(VLANs\), virtual load balancers, virtual routers, switches, and firewalls.

ServiceNow Discovery uses the [VMware NSX Advanced load balancer discovery](https://www.servicenow.com/docs/access?context=vmware-nsx-lb-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) pattern to find VMware NSX load balancers and their components: Listeners, pools, pool members, and health services.

![VMware NSX load balancer classes integrated with the CMDB class hierarchy.](../image/cmdb_ci_class_model_vmware_nsx.png "VMware NSX load balancer classes integrated with the CMDB class hierarchy")

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates. See the class columns table for further details about the columns added for each class.

CMDB CI Class Models: Release 1.10.0 adds the following classes for the VMware NSX load balancer. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

|Class|Extends|Description|
|-----|-------|-----------|
|NSX Load Balancer \[cmdb\_ci\_nsx\_lb\]|Load Balancer \[cmdb\_ci\_lb\]|The table containing the NSX Load Balancer resources.|

## Class columns

The [VMware NSX Advanced load balancer discovery](https://www.servicenow.com/docs/access?context=vmware-nsx-lb-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) pattern introduces one new table with one identification rule and entry. The table uses only the columns inherited from its parent.

**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

