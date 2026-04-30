---
title: OpenStack extension classes
description: The CMDB CI Class Models store app adds or updates classes for OpenStack.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# OpenStack extension classes

The CMDB CI Class Models store app adds or updates classes for OpenStack.

The app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. You can use the added classes as any other CMDB class. Applications such as Discovery and Service Mapping patterns can use these class extensions to populate CIs and discover various technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## OpenStack

OpenStack is a cloud operating system that controls large pools of compute, storage, and networking resources throughout a datacenter. All of these resources are managed and provisioned through APIs with common authentication mechanisms. Other components provide services such as orchestration, fault management, and service management to ensure high availability of user applications. OpenStack is broken up into services to enable you to plug and play components depending on your needs. These components are designed for horizontal scalability, so you can easily add new resources to grow your cloud over time.

![OpenStack classes integrated with the CMDB class hierarchy.](../image/CMDBCIClassModelsFeb20OpenStack.png "OpenStack classes integrated with the CMDB class hierarchy")

## Classes

This section lists the relevant classes that the CMDB CI Class Models store app adds or updates. See the class columns table for further details about the columns added for each class.

CMDB CI Class Models: Release 1.8.0 adds the following classes for OpenStack. For the list of CMDB classes in a base system, including ones that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

|Class|Extends|Description|
|-----|-------|-----------|
|OpenStack Services \[cmdb\_ci\_cloud\_openstack\_service\]|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|An OpenStack web service that can be accessed via a URL.|
|OpenStack Endpoint \[cmdb\_ci\_cloud\_openstack\_endpoint\]|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|The access point of a Service.|
|OpenStack Domain \[cmdb\_ci\_cloud\_openstack\_domain\]|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|A collection of users, groups, and projects.|

## Class columns

CMDB CI Class Models: Release 1.8.0 adds the following columns to the respective classes.

|Added columns|Description|
|-------------|-----------|
|type|The Service type, which describes the API implemented by the Service. Possible values: Compute, ec2, identity, image, network, or volume.|
|enabled|Defines if the service and its endpoints appear in the Service catalog \(true/false\).|

<table id="table_ob4_kyf_pkb"><thead><tr><th>

Added columns

</th><th>

Description

</th></tr></thead><tbody><tr><td>

interface

</td><td>

The interface type, which describes the visibility of the endpoint. Possible values: -   public - Visible by end users on a publicly available network interface.
-   internal - Visible by end users on an unmetered internal network interface.
-   admin - Visible by administrative users on a secure network interface.

</td></tr><tr><td>

enabled

</td><td>

Defines if the Service and its endpoints appear in the Service catalog \(true/false\).

</td></tr></tbody>
</table>|Added columns|Description|
|-------------|-----------|
|enabled|Defines if the domain is enabled \(true/false\).|

**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

