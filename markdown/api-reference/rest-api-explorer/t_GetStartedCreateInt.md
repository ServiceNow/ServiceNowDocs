---
title: Create an incident record
description: Use a POST request to create a new record.
locale: en-US
release: xanadu
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use the REST API Explorer, REST APIs, Web services, API implementation, API implementation and reference]
---

# Create an incident record

Use a POST request to create a new record.

## Before you begin

Role required: admin, web\_service\_admin, or rest\_api\_explorer

## About this task

Use the REST API Explorer to send the following request:

`POST https://instance.service-now.com/api/now/v1/table/incident`

For details about the Table API and examples, see [Table API](../concept/c_TableAPI.md#).

## Procedure

1.  In the top-left of the REST API Explorer, select **Table API** and version **v1**.

2.  Click **Create a record \(POST\)**.

    For more information about this API endpoint, see [Table - POST /now/table/\{tableName\}](../concept/c_TableAPI.md#).

3.  In the Path Parameters section, select the **Incident \(incident\)** table.

4.  In the Request Body section, click **Add a field**.

5.  Select a field and specify a value for that field.

6.  Click the plus sign \(**+**\) and specify any additional field to assign a value to.

    The request body updates automatically based on your entries, such as `{"short_description":"Test incident creation through REST", "comments":"These are my comments"}`

7.  After constructing the request, click **Send**.

    The response includes a Location header that specifies where the incident was created and how to retrieve the incident.

    **Tip:** Record this header to use in the next part of this guide.

    The response also indicates the **Status code** and **Execution time** \(in milliseconds\) of the request.

    ![REST API Explorer POST response](../image/rest-api-exp-post-response.png)


**Parent Topic:**[Use the REST API Explorer](../concept/use-REST-API-Explorer.md)

