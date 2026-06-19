---
title: Retrieve existing incidents
description: Use a GET request to view existing incident records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-api-explorer/t\_GetStartedRetrieveExisting.html
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the REST API Explorer, REST APIs, Web services, API implementation, API implementation and reference]
---

# Retrieve existing incidents

Use a GET request to view existing incident records.

## Before you begin

Role required: admin, web\_service\_admin, or rest\_api\_explorer

## About this task

Use the REST API Explorer to send the following request:

`GET https://instance.service-now.com/api/now/v1/table/incident`

## Procedure

1.  In the top-left of the REST API Explorer, select **Table API** and version **v1**.

2.  Click **Retrieve records from a table \(GET\)**.

    For more information about this API endpoint, see [Table - GET /now/table/\{tableName\}](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/c_TableAPI.md).

3.  In the Path Parameters section, select the **Incident \(incident\)** table.

4.  Scroll to the bottom of the page and click **Send**.

    The response includes incident records from the instance. The REST API Explorer limits queries to 10 records at a time. Only the first 10 incident records appear. The response also includes a Link header that provides the URL to query the next 10 incident records.

    The response also indicates the **Status code** and **Execution time** \(in milliseconds\) of the request.

    \[Omitted image "rest-api-exp-get-response.png"\] Alt text: REST API Explorer GET response


**Parent Topic:**[Use the REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/use-REST-API-Explorer.md)

