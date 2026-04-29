---
title: hr\_Utils - Scoped
description: The hr\_Utils API provides basic functionality for the Human Resource \(HR\) application.Instantiates an instance of the hr\_Utils class.Gets the Sys ID of the active primary job for a provided user.Switches the primary job of a user.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# hr\_Utils- Scoped

The hr\_Utils API provides basic functionality for the Human Resource \(HR\) application.

This API requires the HR core plugin \(com.sn\_hr\_core\) and runs in the `sn_hr_core` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## hr\_Utils - hr\_Utils\(\)

Instantiates an instance of the hr\_Utils class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## hr\_Utils - getPrimaryJob\(String userId\)

Gets the Sys ID of the active primary job for a provided user.

|Name|Type|Description|
|----|----|-----------|
|userID|String|Sys ID of the HR user from the User \[sys\_user\] table assigned an active or future job in which Primary is true.|

|Type|Description|
|----|-----------|
|String|If present and active, Sys ID of the primary job from the Jobs \[sn\_hr\_core\_job\] table, null otherwise.|

```
var result = new sn_hr_core.hr_Utils().getPrimaryJob('5137153cc611227c000bbd1bd8cd2007');
gs.info('Result: ' + result);
```

Output:

```
Result: eb3c69463cd63740964fb8b1ce04f9ae
```

## hr\_Utils - switchPrimaryJob\(String userId String jobId\)

Switches the primary job of a user.

|Name|Type|Description|
|----|----|-----------|
|userId|String|Sys ID of HR user from the Users \[sys\_user\] table.|
|jobId|String|Job Sys ID from the Jobs \[sn\_hr\_core\_job\] table.|

|Type|Description|
|----|-----------|
|String|Encoded JSON with message and status, error otherwise.|

```
var result = new sn_hr_core.hr_Utils().switchPrimaryJob('5137153cc611227c000bbd1bd8cd2007', 'bc884e723c0ebf00964fb8b1ce04f9d7');
gs.info('Result: ' + result);
```

Output:

```
Result: {"message":"Switched primary job for the user successfully","status":"success"}
```

