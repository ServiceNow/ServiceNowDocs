---
title: Network Intrusion Detection System \(NIDS\) CI extension class
description: The Network Intrusion Detection System \(NIDS\) \[cmdb\_ci\_nids\] class builds the relationships between passive network monitoring appliances, and the devices on the network that it discovers.​ A NIDS Manager manages the NIDS sensors that detect the devices and builds "detects::detected by” relationships between the NIDS records \(parent\) and the CIs it discovers \(child\).​
locale: en-US
release: zurich
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [CMDB CI class models, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Network Intrusion Detection System \(NIDS\) CI extension class

The Network Intrusion Detection System \(NIDS\) \[cmdb\_ci\_nids\] class builds the relationships between passive network monitoring appliances, and the devices on the network that it discovers.​ A NIDS Manager manages the NIDS sensors that detect the devices and builds "detects::detected by” relationships between the NIDS records \(parent\) and the CIs it discovers \(child\).​

This topic lists the relevant classes that the CMDB CI Class Models store app adds or updates. See the class columns table for further details about the columns added for each class.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Network Intrusion Detection System \(NIDS\) schema structure​

![NIDS schema structure.](../image/nids-appliance-model.png)

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates.See the class columns table for further details about the columns added for each class.

CMDB CI Class Models: Release 1.30 adds the following classes for the Network Intrusion Detection System \(NIDS\). For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

|Class|Extends|Description|
|-----|-------|-----------|
|Network Intrusion Detection System \(NIDS\) \(cmdb\_ci\_nids\)|cmdb\_ci\_ids\_network|NIDS is an intrusion detection system within the network that examines the traffic from all devices on the network. NIDS scanners build relationships between the OT network scanning appliances, and the OT devices on the network.​ An NIDS Manager manages the NIDS sensors.​|

## Class columns

CMDB CI Class Models: Release 1.30 adds the following columns to the Network Intrusion Detection System \(NIDS\) \[cmdb\_ci\_nids\] class.

|Column label|Column name|Description|
|------------|-----------|-----------|
|NIDS source ID|Correlation\_id|Identifier of the NIDS device. Uses the assigned Correlation ID for the NIDS as its nids\_source\_id.|
|NIDS source name|nids\_source\_name|Name of the NIDS device.|
|Network type assignment|network\_type\_assignment|Designates if the device is on an IT or OT network.|
|NIDS assignment site|isa\_entity\_site|ISA site assigned to the NIDS. This information is available when the logged in user has an assigned ISA Admin role.|

## Roles and Access Control Logic \(ACLs\)

The NIDS Admin \(cmdb\_nids\_admin\) role is associated with the Network Intrusion Detection System \(NIDS\) \[cmdb\_ci\_nids\] class: Can create, read, update, and delete Network IDS \(NDIS\) OT records. To view the Network IDS Application selection on the application menu, you must have this role.

## Key relationship structure

For each CMDB CI record with a “Detected by” relationship with an NIDS record, a ServiceNow Operational Technology Certified Service Graph Connector does the following:

1.  Assigns the following NIDS-related metadata values to the CI:
    1.  Location
    2.  Company
    3.  Related users \(Owned by, Managed by, Supported by, Assigned to\)
    4.  Related user groups \(Approval group, Managed by Group, Support group, Change group\)
2.  If the NIDS network type is set to OT, it assigns the following NIDS-related metadata values to the CI:
    1.  Creates an OT device \(cmdb\_ot\_entity\) record for the CI, using the cmdb\_ot\_entity reference on the CI.
    2.  Assigns the NIDS assignment zone to the OT device record.
    3.  If the Industrial Process Manager is installed, assign the NIDS assignment site to the OT device record.
3.  *Life Cycle Stage* and *Life Cycle Stage Status* values for the CI are used to capture the learning mode of a sensor.
    -   If *Life Cycle Stage* is **Operational** and *Life Cycle Stage Status* is **Learning Mode**, then validation is unsuccessful.
    -   If *Life Cycle Stage Status* is **In Use**, validation is successful.

