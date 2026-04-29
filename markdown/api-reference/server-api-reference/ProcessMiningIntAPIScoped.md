---
title: ProcessMiningIntegrationAPI - Scoped
description: The ProcessMiningIntegrationAPI script include provides methods to manage process mining projects and retrieve findings and breakdowns.Creates a process mining project.Deletes a process mining project.Gets breakdown statistics for a process mining project.Gets findings for a process mining project.Gets the mining status of a process mining project.Retrieves a process mining project.Submits a process mining project for mining.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ProcessMiningIntegrationAPI- Scoped

The ProcessMiningIntegrationAPI script include provides methods to manage process mining projects and retrieve findings and breakdowns.

This script include requires the Process Mining plugin \(sn\_po\). For more information, see [Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

The calling user must have the sn\_process\_mining\_analyst or sn\_process\_mining\_power\_user role.

The following system properties can be used to manage API functionality.

-   **__promin.limit.api.project\_creation__**

    Limits the number of projects that can be created daily using APIs.

    Default: 25.

-   **__promin.limit.api.max\_daily\_minings__**

    Limits the number of minings that can be scheduled daily using APIs.

    Default: 25.

-   **__promin.limit.api.max\_daily\_minings\_per\_project__**

    Limits the number of minings that can be scheduled daily per project using APIs.

    Default: 1.

-   **__promin.api.allow\_no\_role\_mining__**

    Allows projects to be mined by users without the sn\_process\_mining\_analyst role.

    Default: False.

-   **__promin.api.auto\_share\_project\_with\_creator__**

    Automatically shares the project with the creator of the project.

    Default: False.


**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ProcessMiningIntegrationAPI - createProject\(String table, Array activities, Array breakdowns, String encodedQuery, String templateType, Object permissions, Boolean autoRetire\)

Creates a process mining project.

A project acts as a blueprint for Process Mining operations. It selects the process that the mining is done on and which attributes of the process are considered while mining.

<table id="table_xs3_lqs_kdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

table

</td><td>

String

</td><td>

Name of the table containing the data to analyze.

</td></tr><tr><td>

activities

</td><td>

Array

</td><td>

Activity definitions for the project. An activity definition is an attribute of the process to consider while mining, such as state or assignment group. It must be a column from the table specified in the **table** parameter. At least one activity definition is required to mine a project. For more information about activity definitions, see [Set activity definitions](https://www.servicenow.com/docs/access?context=set-activity-def&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

**Note:** Activity definitions are also included in the project template specified in the **templateType** parameter. Use the **activities** parameter to specify any additional activities not included in the template.

```
["<column_name>"]
```

</td></tr><tr><td>

breakdowns

</td><td>

Array

</td><td>

Breakdown definitions for the project.A breakdown definition allows you to filter records and analyze a process map by categories, such as priority or business category. It must be a column from the table specified in the **table** parameter. Breakdown definitions aren't required to mine a project. For more information about breakdown definitions, see [Set breakdown definitions](https://www.servicenow.com/docs/access?context=breakdown&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

**Note:** Breakdown definitions are also included in the project template specified in the **templateType** parameter. Use the **breakdowns** parameter to specify any additional breakdowns not included in the template.

```
["<column_name>"]
```

</td></tr><tr><td>

encodedQuery

</td><td>

String

</td><td>

Encoded query to select the data to analyze. This allows you to limit the data that is analyzed, such as by selecting data only from a specified time period.To include all data in the table, you can pass an empty string.

</td></tr><tr><td>

templateType

</td><td>

String

</td><td>

Type of template to use for the project.Valid values:

-   Default
-   Digital Portfolio Management
-   Vendor Management
-   WFO

For a project that is not part of Workforce Optimization \(WFO\), Vendor Management, or Digital Portfolio Management, choose Default. For example, to create a Performance Analytics project, select Default.

</td></tr><tr><td>

permissions

</td><td>

Object

</td><td>

Map of groups, roles, and users to share the project with, where the key is a sys\_id and the value specifies the type \(group, role, or user\).All users who the project is shared with can view the analyzed model and view project configurations. Only users with the sn\_process\_optimization\_analyst or sn\_process\_optimization\_power\_user can mine the project.

```
{
   "<user_sys_id>":"user",
   "<role_sys_id>":"role",
   "<group_sys_id>":"group"
}
```

</td></tr><tr><td>

autoRetire

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to automatically retire the project.

 Valid values:

-   true: The project is automatically retired seven days after creation.
-   false: The project isn't automatically retired.

 Default: False

</td></tr></tbody>
</table><table id="id_x1l_krq_c2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing information about the project.```
{
   "entity": {Object},
   "findingDefinitionKPIMap": {Object},
   "id": "String",
   "lastMined": String",
   "miningState": "String",
   "name": "String",
   "permissions": [Array],
   "retiredDate": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.entity

</td><td>

Object containing information about the data analyzed in the project.Data type: Object

```
{
   "activityDefinitions": [Array],
   "breakdownDefinitions": [Array],
   "condition": "String,"
   "table": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.entity.activityDefinitions

</td><td>

Activity definitions for the project.Data type: Array

```
[
   {
      "activityOfInterest":Boolean,
      "field":"String",
      "type":"String"      
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.entity.activityDefinitions.activityOfInterest

</td><td>

Flag that indicates whether field changes appear in the analyst workbench.

 Valid values:

-   true: Field changes appear in the analyst workbench.
-   false: Field changes don’t appear in the analyst workbench, but can still be used in contextual conditions in transitions or findings.

</td></tr><tr><td>

&lt;Object&gt;.entity.activityDefinitions.field

</td><td>

Field containing the data to analyze. The field must be from the table specified in the **table** parameter.

</td></tr><tr><td>

&lt;Object&gt;.entity.activityDefinitions.type

</td><td>

The type of values to mine.Valid values:

-   Field Values \(Default\): This is the default selection. This option is available whenever you create an activity definition.
-   Date Time: Uses date time value from the actual record rather than the audit history and is displayed as a grouped node on the process map.
-   Compound: One node or process graph representing change in the multiple field value from the actual record rather than the audit history.
-   Child Attached: This option is available when you have selected two tables for table configuration and have set a child-parent relationship. This option is available only for the parent table configuration. In the visualization, you will see when the child was attached in the process.
-   Parent Attached: This option creates a node on the child process representing when a parent record was attached to a child.

</td></tr><tr><td>

&lt;Object&gt;.entity.breakdownDefinitions

</td><td>

Breakdown definitions for the project.Data type: Array

```
[
 {
   "field":"String",
   "fieldLabel":"String"
 }
]
```

</td></tr><tr><td>

&lt;Object&gt;.entity.breakdownDefinitions.field

</td><td>

Name of the field used in the breakdown.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.entity.breakdownDefinitions.fieldLabel

</td><td>

Label of the field used in the breakdown.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.entity.condition

</td><td>

Encoded query to select the data to analyze.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.entity.table

</td><td>

Name of the table containing the data to analyze.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.findingDefinitionKPIMap

</td><td>

Map of improvement opportunities and key performance indicators \(KPIs\), where the map key is an improvement opportunity sys\_id and the value is an array of sys\_ids of the KPIs impacted by the improvement opportunity.Improvement opportunities are located in the Finding Definition \[promin\_finding\_def\] and Automated Finding Definition \[promin\_automated\_finding\] tables. KPIs are located in the Indicator \[pa\_indicators\] table.

For more information about improvement opportunities and KPIs, see [Setting improvement opportunities](https://www.servicenow.com/docs/access?context=working-with-imp-opp&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) and [Viewing business insights](https://www.servicenow.com/docs/access?context=view-business-findings&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

Data type: Object

```
{
   "<finding_def_sys_id":[
      "<kpi_sys_id>"
   ]
}
```

</td></tr><tr><td>

&lt;Object&gt;.id

</td><td>

Sys\_id of the project.Table: Project Definition \[promin\_project\]

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.lastMined

</td><td>

Date the project was last mined.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.miningState

</td><td>

Mining state for the project.For descriptions of mining states, see [Mining states](https://www.servicenow.com/docs/access?context=generate-process-map&version=australia&pubname=australia-now-intelligence&section=extraction-states&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.name

</td><td>

Name of the project.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.permissions

</td><td>

Group, role, and user permissions for the project.Data type: Object

```
[
   {
      "type":"String",
      "value":"String"      
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.permissions.type

</td><td>

Type of permission.Valid values:

-   group
-   role
-   user

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.permissions.value

</td><td>

Sys\_id of the group, role, or user to grant permissions.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.retiredDate

</td><td>

Date the project will be retired.Data type: String

</td></tr></tbody>
</table>This example creates a project using data from incidents created last month.

```
SNC.ProcessMiningIntegrationAPI
.createProject(
"incident", // table name
["state"], // activity definitions
["priority"], // breakdown definitions
"sys_created_onONLast month@javascript:gs.beginningOfLastMonth()@javascript:gs.endOfLastMonth()", // incident created on last month
"DEFAULT", // template type
{"02acf036b3120010ed7fc9c316a8dc0c":"user"}, // map of permissions "sys_id":"type"
true // auto retire project
);
```

Output:

```
{
   "entity":{
      "table":"incident",
      "condition":"sys_created_onONLast month@javascript:gs.beginningOfLastMonth()@javascript:gs.endOfLastMonth()",
      "activityDefinitions":[
         {
            "field":"assignment_group",
            "type":"DEFAULT",
            "activityOfInterest":false
         },
         {
            "field":"business_service",
            "type":"DEFAULT",
            "activityOfInterest":false
         },
         {
            "field":"category",
            "type":"DEFAULT",
            "activityOfInterest":false
         },
         {
            "field":"priority",
            "type":"DEFAULT",
            "activityOfInterest":false
         },
         {
            "field":"state",
            "type":"DEFAULT",
            "activityOfInterest":false
         }
      ],
      "breakdownDefinitions":[
         {
            "field":"contact_type",
            "fieldLabel":"Channel"
         },
         {
            "field":"assignment_group",
            "fieldLabel":"Assignment group"
         },
         {
            "field":"location",
            "fieldLabel":"Location"
         },
         {
            "field":"priority",
            "fieldLabel":"Priority"
         },
         {
            "field":"category",
            "fieldLabel":"Category"
         }
      ]
   },
   "name":"Incident Process",
   "permissions":[
      {
         "value":"62826bf03710200044e0bfc8bcbe5df1",
         "type":"user"
      },
      {
         "value":"02acf036b3120010ed7fc9c316a8dc0c",
         "type":"user"
      }
   ],
   "id":"a4286c4f4f831210c98b8a4a91ce0bf5",
   "miningState":"NEW",
   "findingDefinitionKPIMap":{
      "f23c20c34fc31210c98b8a4a91ce0bac":[
         "002d65c3d7131100b96d45a3ce6103e2"
      ]
   },
   "retiredDate":null,
   "lastMined":null
}
```

## ProcessMiningIntegrationAPI - deleteProject\(String projectId\)

Deletes a process mining project.

<table id="table_cfn_f5t_kdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

projectId

</td><td>

String

</td><td>

Sys\_id of the project.Table: Project Definition \[promin\_project\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example deletes a process mining project.

```
SNC.ProcessMiningIntegrationAPI.deleteProject("a4286c4f4f831210c98b8a4a91ce0bf5");
```

## ProcessMiningIntegrationAPI - getBreakDownStats\(String projectId\)

Gets breakdown statistics for a process mining project.

Breakdowns allow you to filter records and analyze a process by categories, such as priority or business category.

<table id="table_qqp_l5t_kdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

projectId

</td><td>

String

</td><td>

Sys\_id of the project.Table: Project Definition \[promin\_project\]

</td></tr></tbody>
</table><table id="table_rqp_l5t_kdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

Array of breakdown objects. Each object contains statistics for the breakdown.```
[
   {
      "caseCount": Number,
      "field": "String",
      "fieldValue": "String",
      "performanceStats": {Object},
      "tableName": "String",
      "variantCount": Number     
   }
]
```

</td></tr><tr><td>

&lt;Array&gt;.caseCount

</td><td>

Number of cases from the Case Record \[promin\_case\_record\] table that are part of this breakdown.Data type: Number

</td></tr><tr><td>

&lt;Array&gt;.field

</td><td>

Field used for the breakdown.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.fieldValue

</td><td>

Field value used for the breakdown.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.performanceStats

</td><td>

Performance statistics for the breakdown.```
{
   "max": Number,
   "mean": Number,
   "median": Number, 
   "min": Number,  
   "n": Number, 
   "q1": Number, 
   "q3": Number, 
   "q4": Number, 
   "stdDeviation": Number, 
   "sum": Number, 
   "total": Number, 
   "trimmedAverage": Number, 
   "trimmedPercentage": Number
}
```

Data type: Object

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.max

</td><td>

Longest time a record took to complete a route.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.mean

</td><td>

Average time that records took to complete a route, from the time records were opened to closed.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.median

</td><td>

Duration middle value, or average of two middle values.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.min

</td><td>

Shortest time a record took to complete a route.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.n

</td><td>

Number of records that are part of this breakdown.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.q1

</td><td>

Duration first quartile value.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.q3

</td><td>

Duration third quartile value.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.q4

</td><td>

Duration fourth quartile value \(maximum\).Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.stdDeviation

</td><td>

Variation from the route duration average value.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.sum

</td><td>

Sum total of all duration times, from the first to the last event, for all records that follow a route.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.total

</td><td>

Sum total of all duration times, from the first to the last event, for all records that follow a route.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.trimmedAverage

</td><td>

Average time that records took to complete a route, calculated after removing a percentage of smallest and largest values.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.trimmedPercentage

</td><td>

Percentage used to calculate the **trimmedAverage** value.Data type: Number

</td></tr><tr><td>

&lt;Array&gt;.tableName

</td><td>

Table used for the breakdown.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.variantCount

</td><td>

Count of variants \(a unique sequence of activities performed in a process\) corresponding to this breakdown. Data type: Number

</td></tr></tbody>
</table>This example gets breakdown statistics for a project.

```
SNC.ProcessMiningIntegrationAPI.getBreakDownStats("a4286c4f4f831210c98b8a4a91ce0bf5");
```

Output:

```
[
   {
      "fieldValue":"1",
      "field":"priority",
      "tableName":"incident",
      "variantCount":21,
      "caseCount":33,
      "performanceStats":{
         "sum":6.4945381E7,
         "min":0.0,
         "max":5.2334704E7,
         "n":33,
         "median":0.0,
         "mean":0.0,
         "total":64945381,
         "stdDeviation":9144841.0,
         "trimmedAverage":165594.0,
         "trimmedPercentage":-1.0,
         "q1":0.0,
         "q3":313333.0,
         "q4":5.2334704E7
      }
   }
]
```

## ProcessMiningIntegrationAPI - getFindings\(String projectId\)

Gets findings for a process mining project.

<table id="table_syh_k5t_kdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

projectId

</td><td>

String

</td><td>

Sys\_id of the project.Table: Project Definition \[promin\_project\]

</td></tr></tbody>
</table><table id="table_tyh_k5t_kdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

Array of findings objects.```
[
   {
      "caseIds":[Array],  
      "category": "String",
      "categoryDescription": "String",
      "categoryLabel": "String",
      "createdOn": Number, 
      "findingDefId": "String", 
      "id": "String",
      "impactedKpis": [Array],
      "matchingRecords": Number,
      "message": "String",
      "performanceStats": {Object},
      "shortMessage": "String",
      "tableName": "String",
      "totalRecords": Number,
      "type": "String",
      "typeLabel": "String",    
      "versionId": "String"  
   }
]
```

</td></tr><tr><td>

&lt;Array&gt;.caseIds

</td><td>

List of IDs of cases that match the finding pattern. Located in the Case ID column of the Case Record \[promin\_case\_record\] table.Data type: Array

</td></tr><tr><td>

&lt;Array&gt;.category

</td><td>

Category of the finding.Possible values:

-   AUTOMATION
-   COMPLIANCE
-   CONFORMANCE
-   COST
-   PERFORMANCE
-   QUALITY
-   SPEED

Data type: String

</td></tr><tr><td>

&lt;Array&gt;.categoryDescription

</td><td>

Description of the finding category.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.categoryLabel

</td><td>

Label for the finding category.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.createdOn

</td><td>

Creation date of the finding.Data type: Number

</td></tr><tr><td>

&lt;Array&gt;.findingDefId

</td><td>

Sys\_id of the improvement opportunity.Improvement opportunities are located in the Finding Definition \[promin\_finding\_def\] and Automated Finding Definition \[promin\_automated\_finding\] tables.

Data type: String

</td></tr><tr><td>

&lt;Array&gt;.id

</td><td>

Sys\_id of the finding. Located in the Finding \[promin\_finding\] table.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.impactedKpis

</td><td>

List of sys\_ids of KPIs impacted by the finding. Located in the Indicator \[pa\_indicators\] table.Data type: Array

</td></tr><tr><td>

&lt;Array&gt;.matchingRecords

</td><td>

Number of Case IDs from the Case Record \[promin\_case\_record\] table that match the finding pattern.Data type: Number

</td></tr><tr><td>

&lt;Array&gt;.message

</td><td>

Message from the improvement opportunity.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.performanceStats

</td><td>

Performance statistics for the finding.```
{
   "max": Number,
   "mean": Number,
   "median": Number, 
   "min": Number,  
   "n": Number, 
   "q1": Number, 
   "q3": Number, 
   "q4": Number, 
   "stdDeviation": Number, 
   "sum": Number, 
   "total": Number, 
   "trimmedAverage": Number, 
   "trimmedPercentage": Number
}
```

Data type: Object

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.max

</td><td>

Longest time a record took to complete a route.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.mean

</td><td>

Average time that records took to complete a route, from the time records were opened to closed.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.median

</td><td>

Duration middle value, or average of two middle values.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.min

</td><td>

Shortest time a record took to complete a route.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.n

</td><td>

Number of records that are part of this finding.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.q1

</td><td>

Duration first quartile value.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.q3

</td><td>

Duration third quartile value.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.q4

</td><td>

Duration fourth quartile value \(maximum\).Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.stdDeviation

</td><td>

Variation from the route duration average value.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.sum

</td><td>

Sum total of all duration times, from the first to the last event, for all records that follow a route.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.total

</td><td>

Sum total of all duration times, from the first to the last event, for all records that follow a route.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.trimmedAverage

</td><td>

Average time that records took to complete a route, calculated after removing a percentage of smallest and largest values.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

&lt;Array&gt;.performanceStats.trimmedPercentage

</td><td>

Percentage used to calculate the **trimmedAverage** value.Data type: Number

</td></tr><tr><td>

&lt;Array&gt;.shortMessage

</td><td>

Short message from the improvement opportunity.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.tableName

</td><td>

Name of the table used in the finding.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.totalRecords

</td><td>

Total number of records analyzed in the mining.Data type: Number

</td></tr><tr><td>

&lt;Array&gt;.type

</td><td>

Type of improvement opportunity.Possible values:

-   EXTRA\_STEP
-   EXTREME\_DURATION
-   EXTREME\_REPETITION
-   OTHER
-   PATTERN
-   PERFORMANCE\_OUTLIER
-   PINGPONG
-   REWORK

For more information, see [Setting Automated improvement opportunities](https://www.servicenow.com/docs/access?context=automated-findings&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

&lt;Array&gt;.typeLabel

</td><td>

Label for the improvement opportunity type.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.versionId

</td><td>

Sys\_id of the project version. Located in the Project Definition Version \[promin\_model\_def\_version\] table.Data type: String

</td></tr></tbody>
</table>This example gets findings for a project.

```
SNC.ProcessMiningIntegrationAPI.getFindings("a4286c4f4f831210c98b8a4a91ce0bf5");
```

Output:

```
[
   {
      "message":"Rework on Closed",
      "id":"0ef09b2e1c6cf0d98045e6ba1c3c9edb",
      "type":"REWORK",
      "createdOn":1727036052.000000000,
      "category":"AUTOMATION",
      "tableName":"incident",
      "categoryLabel":"Automation",
      "matchingRecords":111,
      "versionId":"9a2f187177b412102f7a1b56ba5a99e2",
      "totalRecords":19758,
      "findingDefId":"791f587177b412102f7a1b56ba5a99eb",
      "categoryDescription":"Category that groups all opportunities that are subject to automation.",
      "impactedKpis":[
         
      ],
      "performanceStats":{
         "sum":2.09532828E8,
         "min":1.0,
         "max":6563078.0,
         "n":111,
         "median":1036715.0,
         "mean":1.0,
         "total":209532828,
         "stdDeviation":1855944.0,
         "trimmedAverage":1716904.0,
         "trimmedPercentage":-1.0,
         "q1":776859.0,
         "q3":2246368.0,
         "q4":6563078.0
      },
      "typeLabel":"Automation",
      "shortMessage":"Closed",
      "caseIds":[
         "119e4a569397fd14849bbcd74dba1018",
         "b16b355f47197190498cc044846d43b0",
         "cf9bca7597fe7d90ef889504a253af9e",
      ]
   }
]
```

## ProcessMiningIntegrationAPI - getMiningStatus\(String projectId\)

Gets the mining status of a process mining project.

<table id="table_r12_j5t_kdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

projectId

</td><td>

String

</td><td>

Sys\_id of the project.Table: Project Definition \[promin\_project\]

</td></tr></tbody>
</table><table id="table_s12_j5t_kdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the project sys\_id and a tracker. ```
{
   "projectId":"String",
   "trackerId":"String"  
}
```

</td></tr><tr><td>

&lt;Object&gt;.projectId

</td><td>

Sys\_id of the project.Table: Project Definition \[promin\_project\]

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.trackerId

</td><td>

Sys\_id of the tracker that monitors the mining progress for the project.Table: Execution Tracker \[sys\_execution\_tracker\]

Data type: String

</td></tr></tbody>
</table>This example gets the mining status for a project.

```
SNC.ProcessMiningIntegrationAPI.getMiningStatus("c0b91f0cff01121047cae835f2cb14bc");
```

Output:

```
{
   "trackerId":"aec9530cff01121047cae835f2cb147e",
   "projectId":"c0b91f0cff01121047cae835f2cb14bc"
}
```

## ProcessMiningIntegrationAPI - getProject\(String projectId\)

Retrieves a process mining project.

<table id="table_ik3_d5t_kdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

projectId

</td><td>

String

</td><td>

Sys\_id of the project.Table: Project Definition \[promin\_project\]

</td></tr></tbody>
</table><table id="id_x1l_krq_c2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing information about the project.```
{
   "entity": {Object},
   "findingDefinitionKPIMap": {Object},
   "id": "String",
   "lastMined": String",
   "miningState": "String",
   "name": "String",
   "permissions": [Array],
   "retiredDate": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.entity

</td><td>

Object containing information about the data analyzed in the project.Data type: Object

```
{
   "activityDefinitions": [Array],
   "breakdownDefinitions": [Array],
   "condition": "String,"
   "table": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.entity.activityDefinitions

</td><td>

Activity definitions for the project.Data type: Array

```
[
   {
      "activityOfInterest":Boolean,
      "field":"String",
      "type":"String"      
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.entity.activityDefinitions.activityOfInterest

</td><td>

Flag that indicates whether field changes appear in the analyst workbench.

 Valid values:

-   true: Field changes appear in the analyst workbench.
-   false: Field changes don’t appear in the analyst workbench, but can still be used in contextual conditions in transitions or findings.

</td></tr><tr><td>

&lt;Object&gt;.entity.activityDefinitions.field

</td><td>

Field containing the data to analyze. The field must be from the table specified in the **table** parameter.

</td></tr><tr><td>

&lt;Object&gt;.entity.activityDefinitions.type

</td><td>

The type of values to mine.Valid values:

-   Field Values \(Default\): This is the default selection. This option is available whenever you create an activity definition.
-   Date Time: Uses date time value from the actual record rather than the audit history and is displayed as a grouped node on the process map.
-   Compound: One node or process graph representing change in the multiple field value from the actual record rather than the audit history.
-   Child Attached: This option is available when you have selected two tables for table configuration and have set a child-parent relationship. This option is available only for the parent table configuration. In the visualization, you will see when the child was attached in the process.
-   Parent Attached: This option creates a node on the child process representing when a parent record was attached to a child.

</td></tr><tr><td>

&lt;Object&gt;.entity.breakdownDefinitions

</td><td>

Breakdown definitions for the project.Data type: Array

```
[
 {
   "field":"String",
   "fieldLabel":"String"
 }
]
```

</td></tr><tr><td>

&lt;Object&gt;.entity.breakdownDefinitions.field

</td><td>

Name of the field used in the breakdown.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.entity.breakdownDefinitions.fieldLabel

</td><td>

Label of the field used in the breakdown.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.entity.condition

</td><td>

Encoded query to select the data to analyze.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.entity.table

</td><td>

Name of the table containing the data to analyze.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.findingDefinitionKPIMap

</td><td>

Map of improvement opportunities and key performance indicators \(KPIs\), where the map key is an improvement opportunity sys\_id and the value is an array of sys\_ids of the KPIs impacted by the improvement opportunity.Improvement opportunities are located in the Finding Definition \[promin\_finding\_def\] and Automated Finding Definition \[promin\_automated\_finding\] tables. KPIs are located in the Indicator \[pa\_indicators\] table.

For more information about improvement opportunities and KPIs, see [Setting improvement opportunities](https://www.servicenow.com/docs/access?context=working-with-imp-opp&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) and [Viewing business insights](https://www.servicenow.com/docs/access?context=view-business-findings&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

Data type: Object

```
{
   "<finding_def_sys_id":[
      "<kpi_sys_id>"
   ]
}
```

</td></tr><tr><td>

&lt;Object&gt;.id

</td><td>

Sys\_id of the project.Table: Project Definition \[promin\_project\]

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.lastMined

</td><td>

Date the project was last mined.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.miningState

</td><td>

Mining state for the project.For descriptions of mining states, see [Mining states](https://www.servicenow.com/docs/access?context=generate-process-map&version=australia&pubname=australia-now-intelligence&section=extraction-states&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.name

</td><td>

Name of the project.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.permissions

</td><td>

Group, role, and user permissions for the project.Data type: Object

```
[
   {
      "type":"String",
      "value":"String"      
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.permissions.type

</td><td>

Type of permission.Valid values:

-   group
-   role
-   user

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.permissions.value

</td><td>

Sys\_id of the group, role, or user to grant permissions.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.retiredDate

</td><td>

Date the project will be retired.Data type: String

</td></tr></tbody>
</table>This example retrieves a process mining project.

```
SNC.ProcessMiningIntegrationAPI.getProject("fa465748ff01121047cae835f2cb1473");
```

Output:

```
{
   "entity":{
      "table":"incident",
      "activityDefinitions":[
         {
            "field":"assignment_group",
            "type":"DEFAULT",
            "activityOfInterest":false
         },
         {
            "field":"business_service",
            "type":"DEFAULT",
            "activityOfInterest":false
         },
         {
            "field":"state",
            "type":"DEFAULT",
            "activityOfInterest":false
         },
         {
            "field":"category",
            "type":"DEFAULT",
            "activityOfInterest":false
         },
         {
            "field":"priority",
            "type":"DEFAULT",
            "activityOfInterest":false
         }
      ],
      "condition":"",
      "breakdownDefinitions":[
         {
            "field":"contact_type",
            "fieldLabel":"Channel"
         },
         {
            "field":"close_code",
            "fieldLabel":"Resolution code"
         },
         {
            "field":"assignment_group",
            "fieldLabel":"Assignment group"
         },
         {
            "field":"location",
            "fieldLabel":"Location"
         },
         {
            "field":"priority",
            "fieldLabel":"Priority"
         },
         {
            "field":"category",
            "fieldLabel":"Category"
         }
      ]
   },
   "name":"Incident Process",
   "permissions":[
      {
         "value":"some_group_sys_id",
         "type":"group"
      },
      {
         "value":"some_role_sys_id",
         "type":"role"
      },
      {
         "value":"some_user_sys_id",
         "type":"user"
      }
   ],
   "id":"fa465748ff01121047cae835f2cb1473",
   "miningState":"NEW",
   "findingDefinitionKPIMap":{
      
   },
   "retiredDate":1728292672.622894000,
   "lastMined":null
}
```

## ProcessMiningIntegrationAPI - scheduleMining\(String projectId\)

Submits a process mining project for mining.

<table id="table_yyx_h5t_kdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

projectId

</td><td>

String

</td><td>

Sys\_id of the project.Table: Project Definition \[promin\_project\]

</td></tr></tbody>
</table><table id="table_s12_j5t_kdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the project sys\_id and a tracker. ```
{
   "projectId":"String",
   "trackerId":"String"  
}
```

</td></tr><tr><td>

&lt;Object&gt;.projectId

</td><td>

Sys\_id of the project.Table: Project Definition \[promin\_project\]

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.trackerId

</td><td>

Sys\_id of the tracker that monitors the mining progress for the project.Table: Execution Tracker \[sys\_execution\_tracker\]

Data type: String

</td></tr></tbody>
</table>This example submits a project for mining.

```
SNC.ProcessMiningIntegrationAPI.scheduleMining("c0b91f0cff01121047cae835f2cb14bc");
```

Output:

```
{
   "trackerId":"aec9530cff01121047cae835f2cb147e",
   "projectId":"c0b91f0cff01121047cae835f2cb14bc"
}
```

