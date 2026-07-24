---
title: VMware NSX load balancer extension classes
description: The CMDB CI Class Models app adds or updates classes for VMware NSX load balancers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-vmware-nsx.html
release: australia
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB CI class models, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# VMware NSX load balancer extension classes

The CMDB CI Class Models app adds or updates classes for VMware NSX load balancers.

CMDB CI Class Models is a ServiceNow Store app that adds class models that extend the CMDB class hierarchy. The new or updated classes include class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the release notes for all CMDB CI class models.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## VMware NSX load balancer

NSX is a network virtualization solution offered by VMware. Among the virtual resources included in the NSX solution are virtual LANs \(VLANs\), virtual load balancers, virtual routers, switches, and firewalls.

Discovery uses the [VMware NSX Advanced load balancer discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/vmware-nsx-lb-discovery.md) pattern to find VMware NSX load balancers and their components: Listeners, pools, pool members, and health services.

\[Omitted image "cmdb\_ci\_class\_model\_vmware\_nsx.png"\] Alt text: VMware NSX load balancer classes integrated with the CMDB class hierarchy.

## Classes

This section lists the classes that the CMDB CI Class Models app adds or updates. See the class columns table for further details about the columns added for each class.

CMDB CI Class Models: Release 1.10.0 adds the following classes for the VMware NSX load balancer. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-tables-details.md).

|Class|Extends|Description|
|-----|-------|-----------|
|NSX Load Balancer \[cmdb\_ci\_nsx\_lb\]|Load Balancer \[cmdb\_ci\_lb\]|The table containing the NSX Load Balancer resources.|

## Class columns

The [VMware NSX Advanced load balancer discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/vmware-nsx-lb-discovery.md) pattern introduces one new table with one identification rule and entry. The table uses only the columns inherited from its parent.

**Related topics**  


[CMDB schema model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_ConfigurationManagementDatabase.md)

