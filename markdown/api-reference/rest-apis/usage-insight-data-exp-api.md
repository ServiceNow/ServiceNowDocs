---
title: UXA Data Export Service API
description: The UXA Data Export Service API provides an endpoint to asynchronously export user experience analytics \(UXA\) data. The data export result is delivered in batches to a dedicated Hermes topic for your ServiceNow instance.Submits an asynchronous request to export user experience analytics \(UXA\) data. The data export result is delivered in batches to a dedicated Hermes topic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/rest-apis/usage-insight-data-exp-api.html
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 8
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# UXA Data Export Service API

The UXA Data Export Service API provides an endpoint to asynchronously export user experience analytics \(UXA\) data. The data export result is delivered in batches to a dedicated Hermes topic for your ServiceNow instance.

For more information about UXA, see [Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/user-exp-analytics-landing.md).

Use cases:

-   Bring usage data from your ServiceNow instance into an external enterprise analytics or business intelligence tool so it can be reported alongside data from other sources.
-   Build end-to-end views of a user journey that spans the ServiceNow AI Platform and other systems.
-   Move large volumes of usage data on a recurring schedule, beyond what is supported by manual export.

This API requires the Usage Insight Data Export application \(sn\_uxa\_data\_export\), which is available on the ServiceNow Store. The calling user must have the sn\_uxa\_data\_export.user role. For automated exports, create a dedicated user for the export service rather than assigning the role to a personal user.

No manual [Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/hermes-messaging-service.md) topic setup is required. A dedicated topic \(uxa.sn\_uxa\_data\_export.data\_export\_results\) is automatically created on the first export request.

After the first call to this API, set up your Kafka client to consume the data from the Hermes topic:

-   [Set up a secure connection to the Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/set-up-secure-connection-to-hermes.md) with a defined topic ACL for the uxa.sn\_uxa\_data\_export.data\_export\_results topic set to Read Only.
-   [Configure two Kafka consumer processes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/producing-consuming-hermes.md) with bootstrap addresses, the uxa.sn\_uxa\_data\_export.data\_export\_results topic, and your keystore and truststore. Use the same Consumer Group ID for both processes. The consumer port ranges \(typically 4100–4103 and 4200–4203\) must be open to consume messages from a Hermes topic. Verify the consumer ports by navigating to **Hermes Messaging Service** &gt; **Diagnostics**.
-   [Configure the SSL connection to Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/consume-messages-hermes.md) in the consumer properties files using the truststore and keystore that you generated.
-   Consume messages from the Hermes topic using a Python consumer or Kafka CLI. For more information, see [Usage Insights Data Export — How to consume the results from Hermes? \[KB3135555\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3135555). Messages must be consumed within the 36 hour retention window, after which they expire from the Hermes topic.

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/rest-apis/api-rest.md)

## UXA Data Export Service - POST /sn\_uxa\_data\_export/data\_export

Submits an asynchronous request to export user experience analytics \(UXA\) data. The data export result is delivered in batches to a dedicated Hermes topic.

**Important:** Batch messages must be consumed by your Kafka client within the 36 hour retention window, after which they expire from the Hermes topic.

### URL format

Versioned URL: `/api/sn_uxa_data_export/{api_version}/data_export`

### Supported request parameters

|Name|Description|
|----|-----------|
|api\_version|Required. Version of the endpoint to access. The current version is `v1`.|

|Name|Description|
|----|-----------|
|None| |

<table id="table_request_body_uxa" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

app\_sys\_id

</td><td>

Sys\_id of the UXA application to export data for. To retrieve this value, open the Network tab in your browser's developer tools and filter by `metric`.**AppSysId** is located in the request payload.

Table: Usage Insights App \[sys\_analytics\_app\]

Default: Data is exported for all UXA applications.

Data type: String

</td></tr><tr><td>

channel

</td><td>

Name of the channel to export data for.Valid values:

-   AINativeExperience
-   Chat
-   CoreUI
-   Mobile
-   NowExperience
-   Web

Default: Data is exported for all channels.

Data type: String

</td></tr><tr><td>

columns

</td><td>

Required. List of columns to include in the export.Supported columns:

-   `Name`: Name of the event.
-   `Timestamp`: Date and time the event occurred.
-   `InstanceUserIdHashed`: A hashed, privacy-preserving identifier for the user associated with the event. For more information, see [User privacy, tracking, and user consent management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/user-exp-analytics-track-options.md).
-   `AppSysId`: Sys\_id of the UXA application the data is for.
-   `SessionId`: A unique identifier assigned to a continuous period of user activity, grouping together all the events that happen during that visit. It resets after a period of inactivity of 30 minutes or continuous activity for 4 hours, starting a new session.
-   `Properties`: Additional metadata attached to an event that captures details such as what the user interacted with, the type of interacting, or the language.

Data type: Array

</td></tr><tr><td>

data\_source

</td><td>

Required. The data to export. The only currently supported value is `events`. Events include user activity such as page views, clicks, and navigation.**Note:** Use the Usage Insights dashboard to view your event data.

Data type: String

</td></tr><tr><td>

from\_date

</td><td>

Required. Inclusive start of the export date range in ISO 8601 format, rounded to the nearest hour.The maximum supported date range, from start to end date, is 90 days.

Data type: String

</td></tr><tr><td>

name\_filter

</td><td>

Name of the event to export data for.Default: Data is exported for all events.

Data type: String

</td></tr><tr><td>

to\_date

</td><td>

Required. Exclusive end of the export date range in ISO 8601 format, rounded to the nearest hour.The maximum supported date range, from start to end date, is 90 days.

Data type: String

</td></tr></tbody>
</table>### Headers

<table id="table_fvk_ddp_rjc" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

HTTP basic authentication or OAuth bearer token.Basic authentication format:

```
Authorization: Basic <base64-encoded-username:password>
```

OAuth format:

```
Authorization: Bearer <access-token>
```

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

<table id="table_status_codes_uxa"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

202

</td><td>

Accepted. The export job was queued for processing.

</td></tr><tr><td>

400

</td><td>

Bad Request. The request failed validation.Common reasons:

-   Request body is missing or malformed.
-   Invalid data source. The only supported source is `events`.
-   Unrecognized column. Valid columns are: Name, Timestamp, InstanceUserIdHashed, AppSysId, SessionId, Properties.
-   Duplicate column.
-   `columns` must be a non-empty array.
-   `from_date` is required and must be in ISO 8601 format, rounded to the nearest hour.
-   `to_date` is required and must be in ISO 8601 format, rounded to the nearest hour.
-   `to_date` must be after `from_date`.
-   Date range exceeds the maximum \(90 days\).
-   Hermes endpoints are not yet available. This can happen shortly after plugin activation.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

402

</td><td>

Quota exceeded. The monthly data export cap has been exceeded.

</td></tr><tr><td>

403

</td><td>

Forbidden. The calling user does not have a required role. The `sn_uxa_data_export.user` role is required to call this API.

</td></tr><tr><td>

429

</td><td>

Too Many Requests. The rate limit of 60 requests per hour has been exceeded. Retry after the rate-limit window resets.

</td></tr><tr><td>

500

</td><td>

Internal server error. Data export is not configured on this instance. Contact your administrator to set the Valk Query Service URL.

</td></tr><tr><td>

503

</td><td>

Service Unavailable. Retry with exponential backoff.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_response_body_uxa"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing information about the data export job.Success structure:

```
"result": {
   "hermes_topic_endpoint": "String",
   "job_id": "String",
   "status": "String" 
}
```

Error structure:

```
"result": {
   "error": "String", 
   "message": "String"
}
```

Data type: Object

</td></tr><tr><td>

result.error

</td><td>

Error code.Data type: String

</td></tr><tr><td>

result.hermes\_topic\_endpoint

</td><td>

The Hermes topic where the data export result is delivered in batches.Data type: String

</td></tr><tr><td>

result.job\_id

</td><td>

Unique identifier for the export job. Each batch of data delivered to the Hermes topic contains the **job\_id** for the job it belongs to.

Data type: String

</td></tr><tr><td>

result.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

result.status

</td><td>

The status of the export request. A value of `accepted` means the export is queued for processing.Data type: String

</td></tr></tbody>
</table>### Data export batch message format

The data export result is delivered asynchronously to the Hermes topic in batches. Each batch message contains the data in JSON format and carries enrichment headers.

|Header|Description|
|------|-----------|
|SNaction|This value is always `INITIAL`, which indicates this is a bulk historical export rather than a live data feed.|
|SNdata\_seeding\_time\_UTC|Date and time the data was queried in ISO 8601 format \(UTC\).|
|SNinstance|Name of the ServiceNow instance that initiated the export.|
|SNorigin|Origin of the message, which is `sn_uxa_data_export`.|
|SNtableName|The data source table, such as `events`.|

<table id="table_yth_cdv_rjc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

columns

</td><td>

List of columns included in the export.Data type: Array

</td></tr><tr><td>

creation\_date

</td><td>

Date and time the export job was created in ISO 8601 format \(UTC\). Data type: String

</td></tr><tr><td>

from\_date

</td><td>

Inclusive start of the export date range contained in this batch in ISO 8601 format.Data type: String

</td></tr><tr><td>

instance\_id

</td><td>

Unique identifier of the ServiceNow instance that initiated the export.

</td></tr><tr><td>

job\_id

</td><td>

Unique identifier for the export job. Each batch of data delivered to the Hermes topic contains the **job\_id** for the job it belongs to.

Data type: String

</td></tr><tr><td>

rows

</td><td>

The exported data rows, LZ4-compressed and base64-encoded. Each data row is an array of values matching the column order defined in **columns**.To decode:

1.  Base64-decode the string.
2.  LZ4-decompress the result.
3.  JSON-parse to get an array of row arrays.

Example of decoded, decompressed, and parsed **rows** when **columns** are `["Name", "Timestamp", "InstanceUserIdHashed"]`:

```
"rows": [
    ["click", "2025-01-15T10:00:00", "0762d92db72412103a248bdc4e24a527"],
    ["click", "2025-01-15T10:05:00", "5862c90db32522103a858cbb4e11a928"]
]
```

Data type: String

</td></tr><tr><td>

rows\_encoding

</td><td>

Encoding applied to the **rows** field. This value is always `lz4+base64` \(LZ4-compressed and base64-encoded\).Data type: String

</td></tr><tr><td>

subtask\_num

</td><td>

The sequence number of this batch \(1-based indexing\). When **subtask\_num** equals **total\_subtasks**, all batches have been delivered.Data type: Number

</td></tr><tr><td>

to\_date

</td><td>

Exclusive end of the export date range contained in this batch in ISO 8601 format.Data type: String

</td></tr><tr><td>

total\_subtasks

</td><td>

Total number of batches included in the export job.Data type: Number

</td></tr><tr><td>

version

</td><td>

Message format version. This value is always `1.0`.

</td></tr></tbody>
</table>For testing and troubleshooting, you can view batch messages in the [Hermes Topic Inspector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/view-messages-hermes-topic.md).

### cURL request

This example exports click events recorded through the NowExperience channel for a single application during January 2025.

```
curl "https://instance.service-now.com/api/sn_uxa_data_export/v1/data_export" \
--request POST \
--header 'Accept:application/json' \
--header 'Content-Type:application/json' \
--header 'Authorization: Bearer <access_token>' \
--data '{
  "data_source": "events",
  "columns": ["Name", "Timestamp", "InstanceUserIdHashed"],
  "from_date": "2025-01-01T00:00:00",
  "to_date": "2025-02-01T00:00:00",
  "name_filter": "click",
  "channel": "NowExperience",
  "app_sys_id": "6735143c87c07610f13ebbf7ccbb35e1"
}' \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "job_id": "abc-123-def-456",
    "status": "accepted",
    "hermes_topic_endpoint": "snc.<instance>.uxa.sn_uxa_data_export.data_export_results"
  }
}
```

### Result batch message

Result batch message 1 out of 10 for the export delivered asynchronously to the Hermes topic.

```
{
   "version": "1.0",
   "job_id": "abc-123-def-456",
   "instance_id": "instance-id",
   "creation_date": "2025-06-01T12:00:00+00:00",
   "from_date": "2025-01-01T00:00:00",
   "to_date": "2025-02-01T00:00:00",
   "subtask_num": 1,
   "total_subtasks": 10,
   "columns": ["Name", "Timestamp", "InstanceUserIdHashed"],
   "rows_encoding": "lz4+base64",
   "rows": "<base64-encoded LZ4-compressed JSON array>"
}
```

Decoded, decompressed, and parsed **rows**:

```
"rows": [
   ["click", "2025-01-15T10:00:00", "0762d92db72412103a248bdc4e24a527"],
   ["click", "2025-01-15T10:05:00", "5862c90db32522103a858cbb4e11a928"]
]
```

