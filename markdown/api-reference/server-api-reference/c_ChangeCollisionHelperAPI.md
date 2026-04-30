---
title: ChangeCollisionHelper - Global
description: The ChangeCollisionHelper script include provides helper methods found in the Change Management - Collision Detector \(com.snc.change.collision\) plugin.Adds the CI to the change's affected CI list.Returns the Affected CI sys\_ids for the given change.Returns any blackout that overlap the period defined by startDate and endDate.Returns changes scheduled in the timespan \(defined by startDate and endDate\) that have the given CI in their Affected CIs list.Returns the changes that are in the timespan \(startDate, endDate\) and that are linked to the given CI.Returns the Maintenance Schedule for a CI.Returns all the CIs that depend on the given CI.Returns all the CIs that the given CI depends on.Check if an CI is already in the change's affected CIs list.Checks if the time span defined by startDate and endDate falls in the CI's maintenance window.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ChangeCollisionHelper- Global

The ChangeCollisionHelper script include provides helper methods found in the Change Management - Collision Detector \(com.snc.change.collision\) plugin.

Use these methods in server side scripts, or when using Ajax calls on the client. You must have the Change Management - Collision Detector plugin installed to use these methods.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ChangeCollisionHelper - addCiToChangeAffectedCis\(String ci, String changeId\)

Adds the CI to the change's affected CI list.

|Name|Type|Description|
|----|----|-----------|
|ci|String|The sys\_id of the configuration item|
|changeId|String|The change record's sys\_id|

|Type|Description|
|----|-----------|
|void| |

## ChangeCollisionHelper - getAffectedCisByChangeId\(String changeId\)

Returns the Affected CI sys\_ids for the given change.

|Name|Type|Description|
|----|----|-----------|
|changeId|String|A change record's sys\_id|

|Type|Description|
|----|-----------|
|Array|An array of sys\_ids of affected CIs.|

## ChangeCollisionHelper - getBlackoutsByDate\(GlideDateTime startDate, GlideDateTime endDate\)

Returns any blackout that overlap the period defined by startDate and endDate.

|Name|Type|Description|
|----|----|-----------|
|startDate|GlideDateTime|The beginning date|
|endDate|GlideDateTime|The ending date|

|Type|Description|
|----|-----------|
|Array|An array of blackouts \(blackoutId:stringSpan\).|

## ChangeCollisionHelper - getChangesWithAffectedCi\(String ci, GlideDateTime startDate, GlideDateTime endDate\)

Returns changes scheduled in the timespan \(defined by startDate and endDate\) that have the given CI in their Affected CIs list.

|Name|Type|Description|
|----|----|-----------|
|ci|String|The configuration item's sys\_id|
|startDate|GlideDateTime|The beginning date|
|endDate|GlideDateTime|The ending date of the time span|

|Type|Description|
|----|-----------|
|Array|An array of change record's sys\_ids|

## ChangeCollisionHelper - getChangesWithCi\(String ci, GlideDateTime startDate, GlideDateTime endDate\)

Returns the changes that are in the timespan \(startDate, endDate\) and that are linked to the given CI.

|Name|Type|Description|
|----|----|-----------|
|ci|String|The configuration item's sys\_id|
|startDate|GlideDateTime|The beginning date|
|endDate|GlideDateTime|The ending date of the time span|

|Type|Description|
|----|-----------|
|Array|An array of sys\_ids for change records|

## ChangeCollisionHelper - getCiMaintenanceSchedule\(String ci\)

Returns the Maintenance Schedule for a CI.

|Name|Type|Description|
|----|----|-----------|
|ci|String|The configuration item's sys\_id|

|Type|Description|
|----|-----------|
|void| |

## ChangeCollisionHelper - getDependants\(String ci\)

Returns all the CIs that depend on the given CI.

|Name|Type|Description|
|----|----|-----------|
|ci|String|A configuration item's sys\_id|

|Type|Description|
|----|-----------|
|Array|An array of CIs|

## ChangeCollisionHelper - getDependencies\(String ci\)

Returns all the CIs that the given CI depends on.

|Name|Type|Description|
|----|----|-----------|
|ci|String|The configuration item's sys\_id|

|Type|Description|
|----|-----------|
|Array|An array of CIs|

## ChangeCollisionHelper - isCiInAffectedCis\(String ci, String changeId\)

Check if an CI is already in the change's affected CIs list.

|Name|Type|Description|
|----|----|-----------|
|ci|String|The sys\_id of the configuration item|
|changeId|String|The change record's sys\_id|

|Type|Description|
|----|-----------|
|Boolean|True if the CI already is in the change's affected CI list.|

## ChangeCollisionHelper - isDateInCiMaintenanceWindows\( GlideDateTime startDate, GlideDateTime endDate, String maintenanceWindow\)

Checks if the time span defined by startDate and endDate falls in the CI's maintenance window.

|Name|Type|Description|
|----|----|-----------|
|startDate|GlideDateTime|The beginning date|
|endDate|GlideDateTime|The ending date|
|maintenanceWindow|String|The configuration item's sys\_id|

|Type|Description|
|----|-----------|
|Boolean|True if the time span is in the CI's maintenance window|

