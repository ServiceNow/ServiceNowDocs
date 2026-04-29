---
title: Lifecycle management APIs
description: CI Lifecycle Management provides a set of state management APIs for manipulating CI operational states, and applying CI actions.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB CI Lifecycle Management \(legacy\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Lifecycle management APIs

CI Lifecycle Management provides a set of state management APIs for manipulating CI operational states, and applying CI actions.

State management APIs adhere to restrictions and allowances specified by Not Allowed CI Actions, Compatible CI Actions, and Not Allowed Operational Transitions. If an API attempts to perform a restricted operation, the operation is blocked, an error is logged, and a task is automatically created if appropriate.

Lifecycle management APIs can set operational states and CI actions to CMDB groups by utilizing lifecycle management bulk APIs.

## Registration APIs

-   registerOperator\(\) - Method to register operator with state management for non-workflow user.
-   unregisterOperator\(String requestorId\) - Method to unregister operator for non-workflow users.
-   isValidRequestor\(String requestorId\) - Method to determine if the specified requestor is a valid active workflow user or a registered user.
-   isLeaseExpired\(String requestorId, String ciSysId, String ciActionName\) - Method to check if registered user lease expired.
-   extendCIActionLease\(String requestorId, String ciSysId, String ciActionName, String leaseTime\) - Method to extend CI Action Lease time, for registered users. If previous lease already expired, extend lease from now.

## Operational State APIs

-   setBulkCIOperationalState\(String requestorId, String sysIdList, String opsLabel, String opsStateListOld\) - Method to set Operational State for an array of CIs.
-   getOperationalState\(String ciSysId\) - Method to get CI Operational State.

## CI Actions APIs

-   addBulkCIAction\(String requestorId, String sysIdList, String ciActionName, String ciActionListOld, String leaseTime\) - Method to add CI Action for an array of CIs.
-   removeBulkCIAction\(String requestorId, String sysIdList, String ciActionName\) - Method to remove a CI Action for a list of CIs.
-   getCIActions\(String ciSysId\) - Method to get CI Actions.

## Not Allowed Action Based on Operational State API

isNotAllowedAction \(String ciType, String opsLabel, String actionName\) - Method to check if a specific CI action is not allowed for specific Operational State on a CI Type.

## Not Allowed Operational State Transition API

isNotAllowedOpsTransition\(String ciType, String opsLabel, String transitionOpsLabel\) - Method to check if specific operational state transition is not allowed on a CI Type.

## Compatible Action API

isCompatibleCIAction\(String actionName, String otherActionName\)- Method to check if two specific actions are compatible with each other.

## Using state management APIs

```
// 1. Register Operator with State Mgmt
var output = SNC.StateManagementScriptableApi.registerOperator();
var jsonUntil = new JSON();
var result = jsonUntil.decode(output);
var requestorId = result.requestorId;

// Get list of sys_ids to update
var sys_ids;

// 2. Set list of sys_ids's Operational State to 'Repair in Progress'
output = SNC.StateManagementScriptableApi.setBulkCIOperationalState(requestorId, sys_ids,'Repair in Progress');
gs.print(output);

// 3. Set list of sys_ids's CI Action State to 'Patching'
output = SNC.StateManagementScriptableApi.addBulkCIAction(requestorId, sys_ids, 'Patching');
gs.print(output);
```

**Parent Topic:**[CMDB CI Lifecycle Management \(legacy\)](cmdb-ci-lifecycle-mgmt.md)

