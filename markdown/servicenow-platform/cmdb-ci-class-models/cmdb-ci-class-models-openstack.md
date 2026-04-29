---
title: OpenStack extension classes
description: The CMDB CI Class Models app adds or updates classes for OpenStack.
locale: en-US
release: australia
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB CI class models, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# OpenStack extension classes

The CMDB CI Class Models app adds or updates classes for OpenStack.

CMDB CI Class Models is a ServiceNow Store app that adds class models that extend the CMDB class hierarchy. The new or updated classes include class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## OpenStack

OpenStack is a cloud operating system that controls large pools of compute, storage, and networking resources throughout a datacenter. All of these resources are managed and provisioned through APIs with common authentication mechanisms. Other components provide services such as orchestration, fault management, and service management to promote high availability of user applications. OpenStack is broken up into services to enable you to plug and play components depending on your needs. These components are designed for horizontal scalability, so you can easily add new resources to grow your cloud over time.

![OpenStack classes integrated with the CMDB class hierarchy.](../image/CMDBCIClassModelsFeb20OpenStack.png "OpenStack classes integrated with the CMDB class hierarchy")

## Classes

This section lists the classes that the CMDB CI Class Models app adds or updates. See the class columns table for further details about the columns added for each class.

CMDB CI Class Models: Release 1.8.0 adds the following classes for OpenStack. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

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

