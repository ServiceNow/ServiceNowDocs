---
title: Script includes installed with Operational Technology Manager
description: The Operational Technology Manager plugin installs the following script includes.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Manager, Operational Technology]
---

# Script includes installed with Operational Technology Manager

The Operational Technology Manager plugin installs the following script includes.

|Name|Description|
|----|-----------|
|BaseDAO|Base DAO class that all DAO classes should extend.|
|NIDSUtils|Utilities for the cmdb\_ci\_nids devices.|
|OTDevicesMigrationUtils|Migrate records from specified classes to updated class tables. For more information, see [Operational Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).|
|OTDevice|Implementation class for performing operations on the \[cmdb\_ot\_entity\] table and related \[cmdb\_ci\] and \[cmdb\_rel\_ci\] tables.|
|OTDeviceDAO|Utilities to assist with using Discovery for Operational Technology devices.|
|OTBaseDAO|Base DAO class that all DAO classes in Operational Technology should extend.|
|OTFoundationConstants|A collection of constants used by other script includes.|
|OTUtils|A collection of Operational Technology utility methods.|
|SGOTDeviceConstants|A collection of constants used by Operational Technology service graph connectors.|
|SGOTDeviceTransformUtil|A collection of transform utility methods for Operational Technology service graph connectors.|
|SGOTDataStreamBase|Base pattern to invoke a specific data stream with given inputs.|
|SGOTTroubleShootHelper|Helper methods for validating the Service Graph Connector's configurations.|
|OTAssetFilterAjax|A utility client script to filter out application records and OT Control Modules from the All OT Devices list view in the Industrial Workspace.|
|OTBulkEditHandler|Server side script to handle the IT to OT bulk edit \(conversion\) and the OT device details bulk edit that are triggered through the Flow Actions and scheduled jobs.|
|Extension Points|
|SGOTDeviceImportExtensionPoint|SG OT Device Import Extension Point which includes two methods: 1. getDeviceCMDBClassNameWithSysId; 2. getComputerType.|

**Parent Topic:**[Configuring the Operational Technology Manager](../concept/configuring-operational-technology-manager.md)

