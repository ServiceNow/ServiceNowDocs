---
title: AssessmentCreation - Global
description: The AssessmentCreation API provides methods that administrators can use to generate assessments and surveys.Creates one or more assessments or surveys for the specified metric type or survey definition.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# AssessmentCreation- Global

The AssessmentCreation API provides methods that administrators can use to generate assessments and surveys.

There are multiple ways to call the createAssessments\(\) method. You must set the **typeID** parameter in all cases to identify a metric type or survey definition.

Some of the factors that influence how the method behaves include:

-   Whether the target is an assessment or survey
-   Whether the assessment schedule type is on-demand or scheduled
-   Survey schedule periods
-   Parameters provided

For example, when the method is called with only the **typeID** parameter set, the method searches for stakeholders or survey users to send invitations to. In contrast, when the method is called with the **typeID** and **userID** parameters set, it attempts to send invitations to the specified users.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## AssessmentCreation - createAssessments \(String typeID, String sourceRecordID, String userID\)

Creates one or more assessments or surveys for the specified metric type or survey definition.

|Name|Type|Description|
|----|----|-----------|
|typeID|String|The sys\_id of the metric type or survey definition for which to generate assessments or surveys.|
|sourceRecordID|String|One or more comma-separated survey definition sys\_ids to include in the assessments generated. There must be an assessable record associated with the specified metric type for each source record. If this parameter is left blank, the assessments generated includes all assessable records for the specified type. This parameter is for use with assessments only.|
|userID|String|One or more comma-separated sys\_ids of users to which to send assessment or survey instances. If this parameter is left blank, the assessment stakeholders or survey users receive instances. This parameter is required for on-demand assessments.|

<table id="table_s4v_xjy_mx" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

If the method is successful, it returns a comma-separated string such as 7a2ad2253784200044e0bfc8bcbe5de1, 10, b7e8b5d4c0a80169008b49e468920048 \(Instance ID, number of instances, Group ID\) with the following values:-   instanceID: Sys\_id of the assessment or survey instance created, if there is only one. Sys\_id of one of the instances, if there are multiple. If there are multiple instances, use the group ID to retrieve data.
-   \#instances: Number of assessment or survey instances created.
-   groupID: Sys\_id of the assessment group that contains the assessment or survey instances created.

 If the method is unable to generate assessments or surveys, it returns one of the error codes.

 Error Codes

-   isscheduled - Indicates that the **userID** or **sourceRecordID** parameter should not have been used. When the **typeID** value represents a metric type with the Schedule type field set to Scheduled, the **typeID** parameter is the only parameter that may be used.
-   draft\_state - Indicates that the **typeID** value is a metric type or survey definition that is not published. Publish the metric type or survey definition.
-   invalidtype - Indicates that there is no existing metric type that matches the **typeID** value.
-   inactive - Indicates that the **typeID** value is a metric type or survey definition that is not active. Navigate to the metric type or survey definition and select the **Active** check box.
-   not\_available - Indicates that the **typeID** value is a metric type or survey definition that has no metrics or survey questions. Add at least one metric or survey question.
-   notyet - Indicates that at least one of the users in the **userID** value is assigned a survey instance for the specified survey definition, that has yet to expire. The error code returns the expiration date.
-   wip - Indicates that at least one of the users in the **userID** value is already assigned a survey instance for the survey.
-   not\_authorized - Indicates that at least one of the users in the **userID** value is not authorized to take the survey. Verify that one of the following is true:
    -   There are no survey users for the specified survey definition.
    -   All the users in the userID value are saved as survey users for the specified survey definition.
-   completed - Indicates that the **typeID** value is a survey definition with the Schedule period field set to Only Once and that at least one of the users in the **userID** value has already completed a survey instance for that survey definition.
-   nousers - Indicates that the **userID** parameter was not used and that one of the following is true:
    -   There are no stakeholders associated with the specified metric type. Set the **userID** parameter or create at least one stakeholder.
    -   There are no survey users associated with the specified survey definition. Set the **userID** parameter or create at least one survey user.
-   nosources - Indicates that the **typeID** value is a metric type with the Schedule type field set to On demand and that neither the **userID** nor **sourceRecordID** parameter was used. Set at least one of these parameters.

</td></tr></tbody>
</table>This code example shows how to generate an assessment instance in a service portal widget. This example will not work if Schedule Type is set to On Demand.

```
(function() {
  var gdtSurvey = new GlideDateTime();
  if (gdtSurvey.getDayOfMonthUTC() == 23) {
    (new SNC.AssessmentCreation()).createAssessments('d902e09a075730101263f19d7c1ed03a', // Assessment metric type sys_id
      '4baec2fe07d3f0101263f19d7c1ed0a6', // Assessable record which is the source of the assessment
      gs.getUserID()); // Users ID to send the assessment instances to
  }
})();
```

Return results:

```
bbf0b9b8072330101263f19d7c1ed00b,1,33f0f978072330101263f19d7c1ed05f
```

