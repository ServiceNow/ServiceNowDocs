---
title: CMDB Data Ingestion API
description: The CMDB Data Ingestion API provides endpoints that enable the batch ingestion of an array of objects into an Import Set table.Inserts records into the Import Set table associated with the data source record identified by the passed-in sys\_id.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CMDB Data Ingestion API

The CMDB Data Ingestion API provides endpoints that enable the batch ingestion of an array of objects into an Import Set table.

**Warning:** This API is no longer recommended. For the same functionality with improved scalability and stability, use the [Import Set - POST /now/import/\{stagingTableName\}/insertMultiple](c_ImportSetAPI.md#) endpoint. From the Quebec release onward, any usage of the CMDB Data Ingestion API should be migrated to use the Import Set – insertMultiple endpoint instead.

In addition, this API will not work by default for zbooted instances.

This API is activated through the Configuration Management Database \(CMDB\) \(com.snc.cmdb\) plugin and requires the cmdb\_import\_api\_admin role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CMDB Data Ingestion - POST /cmdb/ingest/\{data\_source\_sys\_id\}

Inserts records into the Import Set table associated with the data source record identified by the passed-in sys\_id.

**Warning:** This API is no longer recommended. For the same functionality with improved scalability and stability, use the [Import Set - POST /now/import/\{stagingTableName\}/insertMultiple](c_ImportSetAPI.md#) endpoint. From the Quebec release onward, any usage of the CMDB Data Ingestion API should be migrated to use the Import Set – insertMultiple endpoint instead.

In addition, this API will not work by default for zbooted instances.

The request body must contain the JSON array of objects \(payload\) to insert in the Import Set table. Each object equates to a row in the table, each name-value pair equates to a column. The JSON payload must leverage the field names from the import set without the "u\_" prefix. For example, the field name "u\_matching\_record" should be "matching\_record" in the request body payload. If the Import Set table exists, the endpoint appends the rows \(objects\) to the existing Import Set table. No checking for duplicates or updating of existing records is performed.

If you are initially building an application, you must first create the associated data source record in your instance before calling this endpoint. If you are just using this endpoint to add records to an existing Import Set table, you do not need to create the data source record, but you must know its sys\_id. The data source record describes the Import Set table in which to insert the specified payload. This table must extend the Import Set Rows \[sys\_import\_set\_row\] table. Also, the data source must be set to `Attachment` and the format set to `JSON`. For more information on data sources, see [Data sources](https://www.servicenow.com/docs/access?context=c_DataSources&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

If the Import Set table defined in the data source record does not exist, the endpoint attaches the passed-in payload to the data source record. To create the initial Import Set table, you must manually import the data into the Import Set table. To import the data, on the associated Data Source form, click the **Test Load 20 Records** or **Load All Records** link in the Related Links section. Once the Import Set table is created, you cannot add columns to the table using this endpoint. If name-value pairs are later passed in that do not exist in the Import Set table, they are ignored without warning. If you need to modify the columns within the Import Set table, you can manually add them to the table. You can also delete or rename the Import Set table, and call the endpoint again using the new payload.

You must have the cmdb\_import\_api\_admin role to access this endpoint.

### URL format

Versioned URL: `/api/now/{api_version}/cmdb/ingest/{data_source_sys_id}`

Default URL: `/api/now/cmdb/ingest/{data_source_sys_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

data\_source\_sys\_id

</td><td>

Sys\_id of the data source record.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

Free-form array of objects that describe the data to append to the associated Import Set table. Each object in the array defines a row in the Import Sets table; each name-value pair a column. **Note:** This array must be named, such as `"{\"records\":[{\"hostname\": \"Hostname1\", \"serialnumber\": \"2acd3873-7fc5-454c-8844-e7769e4d6cfc\", \"model\": \"Model Id"},{\"vendor\": \"ABC Co\"}]}"`.

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
|201|Created. An attachment was added to the data source.|
|202|Accepted. Rows were added to the Import Set table.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|
|409|Conflict. Attachment already exists on the data source.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|
|501|Not Implemented. Request format is not supported.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Describes an encountered error.Data type: Object

 ```
"error": {
  "details": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.details

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message describing the error.Data type: String

</td></tr><tr><td>

import\_set

</td><td>

Name of the Import Set table to which the payload was appended.Data type: String

</td></tr><tr><td>

staged\_row\_count

</td><td>

Number of rows appended to the Import Set table.Data type: Number

</td></tr><tr><td>

staging\_table

</td><td>

Name of the data source record used to stage the payload.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "instance.service-now.com/api/now/cmdb/ingest/4dd9686d1b9800103d374087bc4bcb3d" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type:application/json" \
--data "{\"records\":[{\"hostname\": \"Hostname1\", \"serialnumber\": \"2acd3873-7fc5-454c-8844-e7769e4d6cfc\", \"model\": \"Model 5100"},{\"vendor\": \"ABC Co\"},
{\"hostname\": \"Hostname2\", \"serialnumber\": \"3adb3873-7fc5-564d-8844-e7769e4d6ded\", \"model\": \"Model 5200"},{\"vendor\": \"ACME Co\"}]}"
--user "username":"password"
```

Successful response:

```
{
  "result": {
    "staged_row_count": 2,
    "import_set": "ISET0010010",
    "staging_table": "sn_my_demo_integra_demo_data_source_01"
  }
}
```

