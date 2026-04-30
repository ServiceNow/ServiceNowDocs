---
title: Retrieve change request data using DevOpsChangeRelationshipHelper script
description: Retrieve data associated with a change request based on the specified relation type using the DevOpsChangeRelationshipHelper script include.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Retrieve change request data using DevOpsChangeRelationshipHelper script

Retrieve data associated with a change request based on the specified relation type using the DevOpsChangeRelationshipHelper script include.

## Before you begin

Role required: sn\_devops.viewer

## About this task

Use [Script Includes](https://servicenow.com/docs/bundle/paris-application-development/page/script/server-scripting/concept/c_ScriptIncludes.html) to store JavaScript functions and classes for use by server scripts. You can call the Script Include from a Business Rule, UI Action, workflow script, Scripted REST API, and so on.

This method retrieves data related to a change request based on the specified relation type.

The supported relation types are:

-   DevOpsCommonConstants.COMMIT\_TABLE
-   DevOpsCommonConstants.DEVOPS\_WORK\_ITEM
-   DevOpsCommonConstants.DEVOPS\_TEST\_SUMMARY\_TABLE
-   DevOpsCommonConstants.DEVOPS\_SECURITY\_SCAN\_SUMMARY\_TABLE
-   DevOpsCommonConstants.DEVOPS\_ARTIFACT\_VERSION\_TABLE
-   DevOpsCommonConstants.DEVOPS\_SOFTWARE\_QUALITY\_SUMMARY\_TABLE
-   DevOpsCommonConstants.DEVOPS\_PULL\_REQUEST\_TABLE

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Search for the DevOpsChangeRelationshipHelper script.

    You can call this Script Include from a Business Rule, UI Action, workflow script, Scripted REST API, and so on.


## Example

Assume you have an instance of the object containing the changeRelationHelperObj method.

```
var changeRelationHelperObj = new sn_devops.DevOpsChangeRelationshipHelper();
```

Assume you have a GlideRecord object representing a change request.

```
var changeRequest = new GlideRecord('change_request');
changeRequest.addQuery('number', 'CHG123456');
changeRequest.query();
changeRequest.next();
```

The retrieved data may include additional details depending on the relation type. If data is found, an array containing the related sys IDs information is returned. If data is not found, a debug message is displayed and an empty array is returned. If there is an issue during data retrieval, an error message is displayed with details.

Example 1: Retrieving commit data for a change request.

```
try {
    var commitsData = changeRelationHelperObj.getChangeRelationData(changeRequest, sn_devops.DevOpsCommonConstants.COMMIT_TABLE);
    if (commitsData && commitsData.length > 0) {
        gs.log('Commits Data:', commitsData);
    } else {
        gs.log('No commits found for Change Request:', changeRequest.getDisplayValue());
    }
} catch (error) {
    gs.error('Error fetching commits data:', error.getMessage());
}

```

Example 2: Retrieving work items for a change request.

```
try {
    var workItemsData = changeRelationHelperObj.getChangeRelationData(changeRequest, sn_devops.DevOpsCommonConstants.DEVOPS_WORK_ITEM);
    if (workItemsData && workItemsData.length > 0) {
        gs.log('Work Items Data:', workItemsData);
    } else {
        gs.log('No work items found for Change Request:', changeRequest.getDisplayValue());
    }
} catch (error) {
    gs.error('Error fetching work items data:', error.getMessage());
}

```

**Parent Topic:**[Accelerating your DevOps change process](../concept/dev-ops-change-acceleration.md)

