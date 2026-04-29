---
title: Import Set API
description: The Import Set API provides endpoints that allow you to interact with import set tables.Retrieves the specified import staging record and resulting transformation result.Inserts incoming data into a specified staging table and triggers transformation based on predefined transform maps in the import set table.Inserts multiple records into a specified staging table and triggers transformation based on predefined transform maps or Robust Transform Engine \(RTE\) configurations in a single request.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Import Set API

The Import Set API provides endpoints that allow you to interact with import set tables.

This API transforms incoming data based on associated transform maps. The import set API supports synchronous transforms. The Import Set API mirrors the existing SOAP interface.

## Security

Access to tables via the REST API is restricted by BasicAuth. To allow access to tables without any authentication or authorization, add the table name to sys\_public.list. ACLs defined on tables are still enforced, and it is the administrator's responsibility to deactivate ACLs.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Import Set - GET /now/import/\{stagingTableName\}/\{sys\_id\}

Retrieves the specified import staging record and resulting transformation result.

### URL format

Versioned URL: `/api/now/{api_version}/import/{stagingTableName}/{sys_id}`

Default URL: `/api/now/import/{stagingTableName}/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

stagingTableName

</td><td>

Name of the table from which to obtain the import data.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the record that contains the data.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Indicates the specified resource was not available. As import set tables are deleted frequently based on a schedule, GET requests may return 404 Not Found responses if the transformation result no longer exists.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_edp_5dz_cmb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

import\_set

</td><td>

Name of the import set.Data type: String

</td></tr><tr><td>

result

</td><td>

List of objects that contain information on the data sets that were imported.Data type: Array

```
"result": [
  {
    "display_name": "String",
    "display_value": "String",
    "record_link": "String",
    "status": "String",
    "sys_id": "String",
    "table": "String",
    "transform_map": "String"
  }
]
```

</td></tr><tr><td>

result.display\_name

</td><td>

Display name of the specific column in the table for which the display value is true. For example, `number`.Data type: String

</td></tr><tr><td>

result.display\_value

</td><td>

Display value of the **display\_name** column. For example, `CHG0000123`.Data type: String

</td></tr><tr><td>

result.record\_link

</td><td>

Table API GET request for the imported record.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the import.Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the import record.Data type: String

</td></tr><tr><td>

result.table

</td><td>

Name of the table in which the data was imported.Data type: String

</td></tr><tr><td>

result.transform\_map

</td><td>

Name of the transform map.Data type: String

</td></tr><tr><td>

staging\_table

</td><td>

Name of the import staging table.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/import/imp_user/e2928be64f411200adf9f8e18110c777" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "import_set": "ISET0010001",
  "staging_table": "imp_user",
  "result": [
    {
      "transform_map": "User",
      "table": "sys_user",
      "display_name": "name",
      "display_value": "John Public",
      "record_link": "https://instance.service-now.com/api/now/table/sys_user/ea928be64f411200adf9f8e18110c777",
      "status": "inserted",
      "sys_id": "ea928be64f411200adf9f8e18110c777"
    }
  ]
}
```

## Import Set - POST /now/import/\{stagingTableName\}

Inserts incoming data into a specified staging table and triggers transformation based on predefined transform maps in the import set table.

Transformation occurs synchronously. For each transform map that you define, the responses include transformation results such as information on the target records.

**Note:** The status\_message and error\_message fields on transformation scripts are processed and returned in response, along with any custom response fields.

### URL format

Versioned URL: `/api/now/{api_version}/import/{stagingTableName}`

Default URL: `/api/now/import/{stagingTableName}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

**Note:** The Import Set POST method accepts only name-value pairs of String data types in request body parameters. If any other data type is provided, the resulting value stored in the import set table might not conform to the intended format. For example, the ":" notion of the nested JSON object is changed to "=".

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

stagingTableName

</td><td>

Name of the table from which to import the data.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Call specific

</td><td>

Name-value pairs to insert in the import fields.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|201|Successful. The request was successfully created.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_xth_xdz_cmb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

import\_set

</td><td>

Name of the import set.Data type: String

</td></tr><tr><td>

result

</td><td>

List of objects that contain information on the data sets that were imported.Data type: Array

```
"result": [
  {
    "display_name": "String",
    "display_value": "String",
    "record_link": "String",
    "status": "String",
    "sys_id": "String",
    "table": "String",
    "transform_map": "String"
  }
]
```

</td></tr><tr><td>

result.display\_name

</td><td>

Display name of the specific column in the table for which the display value is true. For example, `number`.Data type: String

</td></tr><tr><td>

result.display\_value

</td><td>

Display value of the **display\_name** column. For example, `CHG0000123`.Data type: String

</td></tr><tr><td>

result.record\_link

</td><td>

Table API GET request for the imported record.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the import.Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the import record.Data type: String

</td></tr><tr><td>

result.table

</td><td>

Name of the table in which the data was imported.Data type: String

</td></tr><tr><td>

result.transform\_map

</td><td>

Name of the transform map.Data type: String

</td></tr><tr><td>

staging\_table

</td><td>

Name of the import staging table.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/import/imp_user" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{'first_name':'John','last_name':'Public','user_id':'john.public','email':'john.public@company.com'}" \
--user "username":"password"
```

```
{
  "import_set": "ISET0010001",
  "staging_table": "imp_user",
  "result": [
    {
      "transform_map": "User",
      "table": "sys_user",
      "display_name": "name",
      "display_value": "John Public",
      "record_link": "https://instance.servicenow.com/api/now/table/sys_user/ea928be64f411200adf9f8e18110c777",
      "status": "inserted",
      "sys_id": "ea928be64f411200adf9f8e18110c777"
    }
  ]
}
```

## Import Set - POST /now/import/\{stagingTableName\}/insertMultiple

Inserts multiple records into a specified staging table and triggers transformation based on predefined transform maps or Robust Transform Engine \(RTE\) configurations in a single request.

Transformation is asynchronous by default. To set synchronous transformation, create a new record in the Rest Insert Multiples \[sys\_rest\_insert\_multiple\] table, select the source table, and set the transformation to synchronous.

This endpoint can send a request body in two possible formats.

-   **Data source file format**

    If you generate a staging table from a JSON data source, match the JSON format of the source file.

-   **Staging table column format**

    Default. Matches the staging table column request body format in key value pairs.


### URL format

Versioned URL: `/api/now/{api_version}/import/{stagingTableName}/insertMultiple`

Default URL: `/api/now/import/{stagingTableName}/insertMultiple`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

**Note:** The Import Set POST method accepts only name-value pairs of String data types in request body parameters. If any other data type is provided, the resulting value stored in the import set table might not conform to the intended format. For example, the ":" notion of the nested JSON object is changed to "=".

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

stagingTableName

</td><td>

Name of the import set table from which to import the data. Refer to [Import sets key concepts](https://www.servicenow.com/docs/access?context=c_ImportSetsKeyConcepts&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

multi\_import\_set\_id

</td><td>

Sys\_id of an entry in the Multi Import Sets \[sys\_multi\_import\_set\] table. If specified, adds the current import to this multiple import set instead of adding to a new multiple import set.Data type: String

Table:

</td></tr><tr><td>

run\_after

</td><td>

Sys\_id of the entry to run. Enables running the current import set after the specified import set is complete. You can use this parameter to enforce the sequential order of imports.This parameter is only valid in asynchronous transformations.

Data type: String

Table: Import Sets \[sys\_import\_set\]

</td></tr></tbody>
</table><table id="table_uc3_ztw_rnb" class="rest_api_request_body"><thead><tr><th>

Format

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source file

</td><td>

This request body format matches the JSON file format used to create the data source. Provide the request body in the same format as the JSON in the data source. JSON input varies depending on the properties in your data source. Refer to JSON information in [File type data source](https://www.servicenow.com/docs/access?context=r_FileTypeDataSource&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).-   This option is only available if the staging table was created using a JSON data source. Refer to [Create a File type data source](https://www.servicenow.com/docs/access?context=create-file-type-data-source&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
-   You must define the path of the data source in the Data Source \[sys\_data\_source\] table in the **Path for each row** field.
-   To change the default behavior for the REST Insert Multiple user, create an entry in the REST Insert Multiples \[sys\_rest\_insert\_multiple\] table.
-   Enable the **Use data source format** in the REST insert multiple entry.

Data type: Object

</td></tr><tr><td>

Staging table column \(default\)

</td><td>

This request body format matches staging table columns. Use the **records** array of key-value pairs matching the staging table column to insert in the import fields. Each JSON key is maps the table column to a JSON value representing the value to be inserted. JSON input varies depending on what fields are in your staging table.The column mapping default key value is to the column table.

```
{
   "records":[
      {
         "<ColumnLabel1>":"<value>",
         "<ColumnLabel2>":"<value>"
      },
      {
         "<ColumnLabel1>":"<value>",
         "<ColumnLabel2>":"<value>"
      }
   ]
}
```

You can modify mapping settings by adding an entry in the Rest Insert Multiples \[sys\_rest\_insert\_multiple\] table and changing the **Column mapping** from **Label** to **Column name**.

```
{
   "records":[
      {
         "<column_name1>":"<value>",
         "<column_name2>":"<value>"
      },
      {
         "<column_name1>":"<value>",
         "<column_name2>":"<value>"
      }
   ]
}
```

The [Data dictionary tables](https://www.servicenow.com/docs/access?context=c_DataDictionaryTables&version=australia&pubname=australia-platform-administration&ft:locale=en-US) provides details on table fields in the system.

Data type: Array

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|201|Successful. The request was successfully created.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body \(JSON\)

<table id="table_smw_4xr_lnb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

import\_set\_id

</td><td>

Sys\_id of the added record. For asynchronous requests, you can use this value to run another import set after this import set process is complete.Data type: String

Table: Import Sets \[sys\_import\_set\]

</td></tr><tr><td>

multi\_import\_set\_id

</td><td>

Sys\_id of the added record. Use this value to group multiple import sets into one set.Data type: String

Table: Multi Import Sets \[sys\_multi\_import\_set\]

</td></tr></tbody>
</table>### Sample cURL request

The following example shows how to run a transform on an import table called u\_employee\_import\_set\_table using the staging table column format.

```
curl "https://instance.servicenow.com/api/now/import/u_employee_import_set_table/insertMultiple" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"records\": [
  {
   \"Address\": \"Hollywood\",
   \"Name\": \"Tom\",
   \"ID\": \"123\"
  },
  {
   \"Address\": \"Vine\",
   \"Name\": \"Irene\",
   \"ID\": \"456\"
  }
  ]
}" \
--user 'username':'password'
```

Results include sys\_ids for new records in the Import Sets \[sys\_import\_set\] and Multi Import Sets \[sys\_multi\_import\_set\] tables.

```
{
  "import_set_id": "<import_set_sys_id>",
  "multi_import_set_id": "<multi_import_set_sys_id>"
}
```

