---
title: Push Metrics API
description: The Push Metrics API provides endpoints that enable you to push raw Metric Intelligence data from an external source to the MID Server.Pushes raw Operational Intelligence data from an external source to the MID Server.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-10-17"
reading_time_minutes: 2
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Push Metrics API

The Push Metrics API provides endpoints that enable you to push raw Metric Intelligence data from an external source to the MID Server.

This API is based on client-side tools that push the raw data from the external source to the MID Server. The Metric Intelligence extension is required to be configured with the **Enable REST Listener** option enabled. For more information on setting up the MID Server, see [Get started with Metric Intelligence](https://www.servicenow.com/docs/access?context=get-started-metrics&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

For information on authentication requirements, see [Configure the MID Web Server extension](https://www.servicenow.com/docs/access?context=configure-mid-web-server-extension&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Push Metrics - POST /mid/sa/metrics

Pushes raw Operational Intelligence data from an external source to the MID Server.

### URL format

Default URL: `/api/mid/sa/metrics`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ci2metric\_id

</td><td>

List of key-value pairs to use to identify the configuration item \(CI\). It is formerly known as **ci\_identifier**. The script continues to accept **ci\_identifier**.Data type: Object

</td></tr><tr><td>

metric\_type

</td><td>

Name of the metric.Data type: String

</td></tr><tr><td>

node

</td><td>

IP address, FQDN, name of the CI, or host. In the example below, the name of the Linux server where the disks are installed.Data type: String

</td></tr><tr><td>

resource\_path

</td><td>

The path of the resource for which metric data is being collected. In the example below, `C:\` is the resource for which metric data is collected.Data type: String

</td></tr><tr><td>

source

</td><td>

Data source monitoring the metric type.Data type: String

</td></tr><tr><td>

timestamp

</td><td>

Epoch time stamp of the metric. Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

unit

</td><td>

Unit type that is associated with the source metric type.Table: Monitoring System Metric Types \[sa\_source\_metric\_type\]

Data type: String

</td></tr><tr><td>

value

</td><td>

Value of the metric.Data type: Number

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

The request body must be surrounded by square brackets, as shown in this example.

```
curl -X POST "https://<mid-server-host>/api/mid/sa/metrics"
-H "Content-Type: application/json"
-U "username":"password"
-d "[{
    "metric_type": "Disk C: % Free Space",
    "resource_path": "C:\\",
    "node": "lnux100",
    "value": 50,
    "timestamp": 1473183012000,
    "ci2metric_id": {
        "node": "lnux100"
    },
    "source": "Splunk"
}]"
```

