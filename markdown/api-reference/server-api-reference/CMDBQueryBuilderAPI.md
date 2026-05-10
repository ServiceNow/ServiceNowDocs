---
title: CMDBQueryBuilderAPI - Global
description: Provides methods to execute Configuration Management Database \(CMDB\) Query Builder operations in server-side scripts.Creates a report that shows the results of a Configuration Management Database \(CMDB\) Query Builder query and returns the URL of the report.Deletes a Configuration Management Database \(CMDB\) Query Builder query.Returns the execution details for a Configuration Management Database \(CMDB\) Query Builder query.Saves a Configuration Management Database \(CMDB\) Query Builder query and returns the sys\_id of the saved query.Updates the JSON for a Configuration Management Database \(CMDB\) Query Builder query.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CMDBQueryBuilderAPI- Global

Provides methods to execute Configuration Management Database \(CMDB\) Query Builder operations in server-side scripts.

This API requires the Configuration Management Database \(CMDB\) application \(com.snc.cmdb\).

**Note:**

This API is only available in Global scope. To use these methods in a scoped application, see [CMDBQBScopedScriptableAPI - Scoped](../../CMDBQBScoped/concept/CMDBQBScopedAPI.md#).

For more information about CMDB Query Builder, see [CMDB Query Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-query-builder-landing-page.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CMDBQueryBuilderAPI - createReport\(String savedQueryId, String savedQueryName\)

Creates a report that shows the results of a Configuration Management Database \(CMDB\) Query Builder query and returns the URL of the report.

For scoped applications, use [CMDBQBScopedScriptableAPI - createReport\(String savedQueryId, String savedQueryName\)](../../CMDBQBScoped/concept/CMDBQBScopedAPI.md#).

<table id="id_dv4_sps_pbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

savedQueryId

</td><td>

String

</td><td>

Sys\_id of the query to use for the report.This parameter is not required if a query name is provided.

Table: Saved Queries \[qb\_saved\_query\]

</td></tr><tr><td>

savedQueryName

</td><td>

String

</td><td>

Name of the query to use for the report.This parameter is not required if a query sys\_id is provided.

Table: Saved in the **Name** field of the Saved Queries \[qb\_saved\_query\] table.

</td></tr></tbody>
</table><table id="id_tbd_tps_pbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Details about the created report and any errors.```
{
  "error": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.error

</td><td>

Error code. Returned when the report creation fails or invalid input parameters are provided. Possible errors:

-   `USER_NOT_AUTHORIZED_EXCEPTION`
-   `INVALID_PARAM`
-   `QUERY_SYS_ID_INVALID`
-   `REPORT_INELIGIBLE`

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message containing details about the success or failure of the report creation.Possible messages:

-   `<report-url>`
-   `User is unauthorized to create a CMDBQueryBuilder query report`
-   `Invalid Parameters. Please provide either a valid sysId or a valid name of a saved query`
-   `Invalid queryId. Please provide a valid saved query ID`
-   `Query must have a schedule with at least one run to create a report.`

See also [Schedule a CMDB query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/create-cmdb-query-schedule.md).

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status code. Returned when the update is successful.Value: `success`

Data type: String

</td></tr></tbody>
</table>This example shows how to create a report by passing a saved query name.

```
var queryReport = SNC.CMDBQueryBuilderAPI.createReport('', 'CMDBQueryTest1');

gs.info(JSON.stringify(JSON.parse(queryReport), null, 2));
```

Output:

```
{
   "message":"\/sys_report_template.do?sysparm_report_source_id=6d299cf81bbd4210bccf42a3b24bcb7a&sysparm_type=list&sysparm_title=CMDBQueryTest1&sysparm_source_type=source&sysparm_from_list=true&sysparm_chart_size=large&sysparm_manual_labor=true",
   "status":"success"
}
```

This example shows an error when the provided query name is invalid.

```
var queryReport = SNC.CMDBQueryBuilderAPI.createReport('', 'Test');

gs.info(JSON.stringify(JSON.parse(queryReport), null, 2));
```

Output:

```
{
   "error":"INVALID_PARAM",
   "message":"Invalid Parameters. Please provide either a valid sysId or a valid name of a saved query"
}
```

## CMDBQueryBuilderAPI - deleteQuery\(String savedQueryId, String savedQueryName\)

Deletes a Configuration Management Database \(CMDB\) Query Builder query.

For scoped applications, use [CMDBQBScopedScriptableAPI - deleteQuery\(String savedQueryId, String savedQueryName\)](../../CMDBQBScoped/concept/CMDBQBScopedAPI.md#).

<table id="id_smz_nqs_pbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

savedQueryId

</td><td>

String

</td><td>

Sys\_id of the query to delete.This parameter can be provided as an empty string if a query name is provided.

Table: Saved Queries \[qb\_saved\_query\]

</td></tr><tr><td>

savedQueryName

</td><td>

String

</td><td>

Name of the query to delete.This parameter is not required if a query sys\_id is provided.

Table: Saved in the *Name* field of the Saved Queries \[qb\_saved\_query\] table.

</td></tr></tbody>
</table><table id="id_ekn_4qs_pbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Details about the deleted query and any errors.```
{
  "error": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.error

</td><td>

Error code. Returned when the delete operation fails or invalid input parameters are provided. Possible errors:

-   `USER_NOT_AUTHORIZED_EXCEPTION`
-   `INVALID_PARAM`
-   `QUERY_DELETE_FAILED`

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message containing details about the success or failure of the delete operation.Possible messages:

-   `Successfully deleted the saved query`
-   `User is unauthorized to delete a CMDBQueryBuilder query`
-   `Invalid Parameters. Please provide either a valid sysId or a valid name of a saved query`
-   `Failed to delete the given saved query`

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status code. Returned when the update is successful.Value: `success`

Data type: String

</td></tr></tbody>
</table>This example shows how to delete a saved query by passing the query name.

```
var delQuery = SNC.CMDBQueryBuilderAPI.deleteQuery('', 'CMDBQueryTest1');

gs.info(JSON.stringify(JSON.parse(delQuery), null, 2));
```

Output:

```
{
   "message":"Successfully deleted the saved query",
   "status":"success"
}
```

## CMDBQueryBuilderAPI - getSavedQueryExecutionDetails\(String savedQueryName, Boolean executeQuery, Number timeout\)

Returns the execution details for a Configuration Management Database \(CMDB\) Query Builder query.

Optionally, you can execute the query in order to return current execution details.

If a timeout or memory issue occurs while executing the query, you can fine tune the query batch size to help alleviate these problems. For more information, see [Batch size for Query Builder saved queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/batch-size-query.md).

For scoped applications, use [CMDBQBScopedScriptableAPI - getSavedQueryExecutionDetails\(String savedQueryName, Boolean executeQuery, Number timeout\)](../../CMDBQBScoped/concept/CMDBQBScopedAPI.md#).

<table id="id_ezv_4vz_pbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

savedQueryName

</td><td>

String

</td><td>

Name of the query to retrieve execution details for. Table: *Name* field in the Saved Queries \[qb\_saved\_query\] table.

</td></tr><tr><td>

executeQuery

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to execute the specified query.Valid values:

-   true: Execute the specified query and return its execution details.
-   false: Don't execute the specified query. Return the most recent execution details for the query.

Default: False

</td></tr><tr><td>

timeout

</td><td>

Number

</td><td>

Optional. Integer value that overrides the default query execution timeout limit of five minutes.Unit: Seconds

Default: Five minutes

</td></tr></tbody>
</table><table id="id_wyc_pvz_pbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Details about the query execution and any errors.```
{
  "error": "String",
  "execution_batch_size": Number,
  "message": "String",
  "query_id": "String",
  "status": "String",
  "table_name": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.error

</td><td>

Error code. Returned when the query execution fails or the specified query is not found.Possible errors:

-   `QUERY_EXECUTION_NOT_FOUND`
-   `QUERY_NOT_FOUND`
-   `QUERY_EXECUTION_FAILED`
-   `USER_NOT_AUTHORIZED_EXCEPTION`

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.execution\_batch\_size

</td><td>

Batch size of 100 allocated for the query run. This value only returns if the **executeQuery** parameter is true. See also [Batch size for CMDB Query Builder queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/batch-size-query.md).Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message containing details about the error code. Returned when the query execution fails or the specified query is not found.Possible messages:

-   `Query execution details not found. Please execute the query.`
-   `Given saved query not found. Please make sure you are passing the name of a saved query.`
-   `Query execution failed. Please use a valid query.`
-   `User is unauthorized to execute a CMDBQueryBuilder query.`

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.query\_id

</td><td>

Sys\_id of the query execution.Data type: String

Table: Query Status \[qb\_query\_status\]

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the query execution.-   COMPLETE: Execution is complete.
-   FAILED: Error occurred while executing query.
-   TIME\_OUT: Query execution timed out.
-   MAX\_LIMIT: Maximum number of return results reached.

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.table\_name

</td><td>

Name of the table that contains the query execution details.Data type: String

</td></tr></tbody>
</table>This example shows how to get the execution status of a saved query.

```
var savedQuery = SNC.CMDBQueryBuilderAPI.getSavedQueryExecutionDetails('CMDBQueryTest1');

gs.info(JSON.stringify(JSON.parse(savedQuery), null, 2));
```

Output:

```
{
   "query_id":"024fd53a7773330033b5270bba106141",
   "table_name":"u_cmdb_qb_result_598918aacb4dbf3f1a8dcf03fce6a5d57151a4e2",
   "status":COMPLETE
}
```

This example shows how to execute a saved query and set the query execution timeout value to 10 minutes.

```
var savedQuery = SNC.CMDBQueryBuilderAPI.getSavedQueryExecutionDetails('CMDBQueryTest2', true, 600);

gs.info(JSON.stringify(JSON.parse(savedQuery), null, 2));
```

Output:

```
{
  "execution_batch_size": 100,
  "query_id": "e73428b4939baa50779bfdfb5cba1047",
  "table_name": "u_cmdb_qb_result_f0eed95be923bf3d439c87c028ae3c3af53aa739",
  "status": "COMPLETE"
}
```

The following example shows how to access information in the result table for the saved query CMDBQueryTest2 in the previous example. You can also use the result table name followed by `.list` in the filter for results.

```
var resultTableName = 'u_cmdb_qb_result_f7593958e298869427726be96f88155cce269806';
var queryId = '76bd283c931bee502285f4cc5cba10da'; // insert the query ID here
var gr = new GlideRecord(resultTableName);
gr.addQuery('query', queryId);
gr.query();
if (gr.next()) { 
     gs.info(gr.getDisplayValue('u_server_1')); // field name in the result table
}
```

Output:

```
PS LoadBal01
```

## CMDBQueryBuilderAPI - saveQuery\(String savedQueryName, String queryJson\)

Saves a Configuration Management Database \(CMDB\) Query Builder query and returns the sys\_id of the saved query.

For scoped applications, use [CMDBQBScopedScriptableAPI - saveQuery\(String savedQueryName, String queryJson\)](../../CMDBQBScoped/concept/CMDBQBScopedAPI.md#).

<table id="id_dzn_1v5_pbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="save-query-name"><td>

savedQueryName

</td><td>

String

</td><td>

Name to save the query under. Table: Saved in the **Name** field of the Saved Queries \[qb\_saved\_query\] table.

</td></tr><tr id="save-query-json"><td>

queryJson

</td><td>

String

</td><td>

JSON that defines the query.Table: Saved in the **Query** field of the Saved Queries \[qb\_saved\_query\] table.

</td></tr></tbody>
</table><table id="id_d3f_bv5_pbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing details about the saved query and any errors.```
{
   "error": "String",
   "message": "String",
   "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.error

</td><td>

Error code. Returned when the save operation fails or invalid input parameters are provided. Possible errors:

-   `USER_NOT_AUTHORIZED_EXCEPTION`
-   `QUERY_NAME_INVALID`
-   `QUERY_INVALID`
-   `QUERY_EXISTS_ALREADY`
-   `QUERY_SAVE_FAILED`

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message containing details about the success or failure of the save operation. Possible messages:

-   `Successfully saved the query with sysId <sy_id>`
-   `User is unauthorized to save a CMDBQueryBuilder query`
-   `Query name is empty. Please provide a name`
-   `QueryJson is invalid. Please provide a valid queryJson`
-   `Query name is already used, please use a different name`
-   `Unexpected exception while saving the query`

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status code. Returned when the save operation is successful.Value: `success`

Data type: String

</td></tr></tbody>
</table>This example shows how to add a query to the Saved Queries \[qb\_saved\_query\] table.

```
var queryJson = "{\"type\":\"cmdb\",\"nodes\":[{\"label\":\"Server\",\"unique_id\":\"d93f96981b310210bccf42a3b24bcb41\",\"nodeType\":\"class\",\"image\":\"images/app.ngbsm/server.svg\",\"properties\":\"\",\"allowed_connections\":[],\"filters\":{\"platform\":\"cmdb_ci_server\",\"custom\":\"\"},\"ci_type\":\"cmdb_ci_server\",\"ci_type_label\":\"Server\",\"sys_id\":\"d93f96981b310210bccf42a3b24bcb41\",\"x\":72,\"y\":337,\"returnValues\":[],\"filters_attrib\":\"\",\"applied_filters\":\"\",\"isStartNode\":true,\"nodeId\":\"d93f96981b310210bccf42a3b24bcb41_4_23_2024_5_50_54\",\"name\":\"Server 1\",\"type\":\"class\",\"refFilterApplied\":false,\"focused\":false,\"id\":\"d93f96981b310210bccf42a3b24bcb41_4_23_2024_5_50_54\",\"className\":\"cmdb_ci_server\"},{\"label\":\"Database\",\"unique_id\":\"b640269c1b310210bccf42a3b24bcb36\",\"nodeType\":\"class\",\"image\":\"images/app.ngbsm/database.svg\",\"properties\":\"\",\"allowed_connections\":[],\"filters\":{\"platform\":\"cmdb_ci_database\",\"custom\":\"\"},\"ci_type\":\"cmdb_ci_database\",\"ci_type_label\":\"Database\",\"sys_id\":\"b640269c1b310210bccf42a3b24bcb36\",\"x\":510,\"y\":340,\"returnValues\":[],\"filters_attrib\":\"\",\"applied_filters\":\"\",\"isStartNode\":false,\"nodeId\":\"b640269c1b310210bccf42a3b24bcb36_4_23_2024_5_50_57\",\"name\":\"Database 1\",\"type\":\"class\",\"refFilterApplied\":false,\"focused\":false,\"id\":\"b640269c1b310210bccf42a3b24bcb36_4_23_2024_5_50_57\",\"className\":\"cmdb_ci_database\"}],\"edges\":[{\"id\":\"Server 1_Database 1\",\"from\":\"d93f96981b310210bccf42a3b24bcb41_4_23_2024_5_50_54\",\"to\":\"b640269c1b310210bccf42a3b24bcb36_4_23_2024_5_50_57\",\"isDotted\":false,\"type\":\"relation\",\"isReverse\":false,\"direction\":\"outbound\",\"hiddenLevel\":0,\"relations\":[\"607ad1b2c0a8010e01941856b365af90\",\"1a9cb166f1571100a92eb60da2bce5c5\"]}],\"usedNames\":{\"cmdb_ci_server\":1,\"cmdb_ci_database\":1}}";

var newQuery = SNC.CMDBQueryBuilderAPI.saveQuery('CMDBQueryTest1', queryJson);

gs.info(JSON.stringify(JSON.parse(newQuery), null, 2));
```

Output:

```
{
   "message":"Successfully saved the query with sysId d93f96981b310210bccf42a3b24bcb41",
   "status":"success"
}
```

## CMDBQueryBuilderAPI - updateQuery\(String savedQueryId, String savedQueryName, String queryJson\)

Updates the JSON for a Configuration Management Database \(CMDB\) Query Builder query.

For scoped applications, use [CMDBQBScopedScriptableAPI - updateQuery\(String savedQueryId, String savedQueryName, String queryJson\)](../../CMDBQBScoped/concept/CMDBQBScopedAPI.md#).

<table id="id_s3p_mv5_pbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

savedQueryId

</td><td>

String

</td><td>

Sys\_id of the query to update.This parameter is not required if a query name is provided.

Table: Saved Queries \[qb\_saved\_query\]

</td></tr><tr><td>

savedQueryName

</td><td>

String

</td><td>

Name of the query to update.This parameter is not required if a query sys\_id is provided.

Table: Saved in the *Name* field in the Saved Queries \[qb\_saved\_query\] table.

</td></tr><tr><td>

queryJson

</td><td>

String

</td><td>

JSON to update the query with.Table: Saved in the *Query* field in the Saved Queries \[qb\_saved\_query\] table.

</td></tr></tbody>
</table><table id="id_opl_4v5_pbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Details about the updated query and any errors.```
{
  "error": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.error

</td><td>

Error code. Returned when the update fails or invalid input parameters are provided. Possible errors:

-   `USER_NOT_AUTHORIZED_EXCEPTION`
-   `INVALID_PARAM`
-   `QUERY_INVALID`
-   `QUERY_UPDATE_FAILED`
-   `UNAUTHORIZED_REPORT_SOURCE_USER`

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message containing details about the success or failure of the update. Possible messages:

-   `Successfully updated the saved query`
-   `User is unauthorized to update a CMDBQueryBuilder query`
-   `Invalid Parameters. Please provide either a valid sysId or a valid name of a saved query`
-   `QueryJson is invalid. Please provide a valid queryJson`
-   `Failed to update the given saved query`
-   `User is unauthorized to update report source of a saved query`

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status code. Returned when the update is successful.Value: `success`

Data type: String

</td></tr></tbody>
</table>This example shows how to update a saved query by passing the query name.

```
var queryJson = "{\"type\":\"cmdb\",\"nodes\":[{\"label\":\"Server\",\"unique_id\":\"d93f96981b310210bccf42a3b24bcb41\",\"nodeType\":\"class\",\"image\":\"images/app.ngbsm/server.svg\",\"properties\":\"\",\"allowed_connections\":[],\"filters\":{\"platform\":\"cmdb_ci_server\",\"custom\":\"\"},\"ci_type\":\"cmdb_ci_server\",\"ci_type_label\":\"Server\",\"sys_id\":\"d93f96981b310210bccf42a3b24bcb41\",\"x\":72,\"y\":336,\"returnValues\":[],\"filters_attrib\":\"\",\"applied_filters\":\"\",\"isStartNode\":true,\"nodeId\":\"d93f96981b310210bccf42a3b24bcb41_4_23_2024_5_50_54\",\"name\":\"Server 1\",\"type\":\"class\",\"refFilterApplied\":false,\"focused\":false,\"id\":\"d93f96981b310210bccf42a3b24bcb41_4_23_2024_5_50_54\",\"className\":\"cmdb_ci_server\"},{\"label\":\"Web Server\",\"unique_id\":\"984f5a981b310210bccf42a3b24bcb03\",\"nodeType\":\"class\",\"image\":\"images/app.ngbsm/web_server.svg\",\"properties\":\"\",\"allowed_connections\":[],\"filters\":{\"platform\":\"cmdb_ci_web_server\",\"custom\":\"\"},\"ci_type\":\"cmdb_ci_web_server\",\"ci_type_label\":\"Web Server\",\"sys_id\":\"984f5a981b310210bccf42a3b24bcb03\",\"x\":446,\"y\":330,\"returnValues\":[],\"filters_attrib\":\"\",\"applied_filters\":\"\",\"isStartNode\":false,\"nodeId\":\"984f5a981b310210bccf42a3b24bcb03_4_23_2024_6_32_19\",\"name\":\"Web Server 1\",\"type\":\"class\",\"refFilterApplied\":false,\"focused\":false,\"id\":\"984f5a981b310210bccf42a3b24bcb03_4_23_2024_6_32_19\",\"className\":\"cmdb_ci_web_server\"}],\"edges\":[{\"id\":\"Server 1_Web Server 1\",\"from\":\"d93f96981b310210bccf42a3b24bcb41_4_23_2024_5_50_54\",\"to\":\"984f5a981b310210bccf42a3b24bcb03_4_23_2024_6_32_19\",\"isDotted\":false,\"type\":\"relation\",\"isReverse\":false,\"direction\":\"outbound\",\"hiddenLevel\":0,\"relations\":[\"607ad1b2c0a8010e01941856b365af90\"]}],\"usedNames\":{\"cmdb_ci_server\":1,\"cmdb_ci_database\":1,\"cmdb_ci_web_server\":1}}";

var queryUpdate = SNC.CMDBQueryBuilderAPI.updateQuery('', 'CMDBQueryTest1', queryJson);

gs.info(JSON.stringify(JSON.parse(queryUpdate), null, 2));
```

Output:

```
{
   "message":"Successfully updated the saved query",
   "status":"success"
}
```

This example shows an error when the query sys\_id and name are both missing from the method call.

```
var queryJson = "{\"type\":\"cmdb\",\"nodes\":[{\"label\":\"Server\",\"unique_id\":\"d93f96981b310210bccf42a3b24bcb41\",\"nodeType\":\"class\",\"image\":\"images/app.ngbsm/server.svg\",\"properties\":\"\",\"allowed_connections\":[],\"filters\":{\"platform\":\"cmdb_ci_server\",\"custom\":\"\"},\"ci_type\":\"cmdb_ci_server\",\"ci_type_label\":\"Server\",\"sys_id\":\"d93f96981b310210bccf42a3b24bcb41\",\"x\":72,\"y\":336,\"returnValues\":[],\"filters_attrib\":\"\",\"applied_filters\":\"\",\"isStartNode\":true,\"nodeId\":\"d93f96981b310210bccf42a3b24bcb41_4_23_2024_5_50_54\",\"name\":\"Server 1\",\"type\":\"class\",\"refFilterApplied\":false,\"focused\":false,\"id\":\"d93f96981b310210bccf42a3b24bcb41_4_23_2024_5_50_54\",\"className\":\"cmdb_ci_server\"},{\"label\":\"Web Server\",\"unique_id\":\"984f5a981b310210bccf42a3b24bcb03\",\"nodeType\":\"class\",\"image\":\"images/app.ngbsm/web_server.svg\",\"properties\":\"\",\"allowed_connections\":[],\"filters\":{\"platform\":\"cmdb_ci_web_server\",\"custom\":\"\"},\"ci_type\":\"cmdb_ci_web_server\",\"ci_type_label\":\"Web Server\",\"sys_id\":\"984f5a981b310210bccf42a3b24bcb03\",\"x\":446,\"y\":330,\"returnValues\":[],\"filters_attrib\":\"\",\"applied_filters\":\"\",\"isStartNode\":false,\"nodeId\":\"984f5a981b310210bccf42a3b24bcb03_4_23_2024_6_32_19\",\"name\":\"Web Server 1\",\"type\":\"class\",\"refFilterApplied\":false,\"focused\":false,\"id\":\"984f5a981b310210bccf42a3b24bcb03_4_23_2024_6_32_19\",\"className\":\"cmdb_ci_web_server\"}],\"edges\":[{\"id\":\"Server 1_Web Server 1\",\"from\":\"d93f96981b310210bccf42a3b24bcb41_4_23_2024_5_50_54\",\"to\":\"984f5a981b310210bccf42a3b24bcb03_4_23_2024_6_32_19\",\"isDotted\":false,\"type\":\"relation\",\"isReverse\":false,\"direction\":\"outbound\",\"hiddenLevel\":0,\"relations\":[\"607ad1b2c0a8010e01941856b365af90\"]}],\"usedNames\":{\"cmdb_ci_server\":1,\"cmdb_ci_database\":1,\"cmdb_ci_web_server\":1}}";

var queryUpdate = SNC.CMDBQueryBuilderAPI.updateQuery('', '', queryJson);

gs.info(JSON.stringify(JSON.parse(queryUpdate), null, 2));
```

Output:

```
{
   "error":"INVALID_PARAM",
   "message":"Invalid Parameters. Please provide either a valid sysId or a valid name of a saved query"
}
```

