---
title: Read the inserted incident
description: Use the Location header from the POST response to run a GET request.
locale: en-US
release: yokohama
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use the REST API Explorer, REST APIs, Web services, API implementation, API implementation and reference]
---

# Read the inserted incident

Use the Location header from the POST response to run a GET request.

## Before you begin

Role required: admin, web\_service\_admin, or rest\_api\_explorer

## About this task

Use the REST API Explorer to send the following request:

`GET https://instance.service-now.com/api/now/v1/table/incident/{sys_id}`

## Procedure

1.  In the top-left of the REST API Explorer, click **Retrieve a record \(GET\)**.

2.  In the Path Parameters section, select the incident table.

3.  In the **sys\_id** field, enter the sys\_id of the record you created.

    The record sys\_id appears as a 32-character string at the end of the POST response Location header.

4.  Click **Send**.

    The response body contains a text representation of the record. You can control the format of the response, such as JSON or XML, using the **Response Format** field.

    The response also indicates the **Status code** and **Execution time** \(in milliseconds\) of the request.

    ![REST API Explorer GET response](../image/rest-api-exp-get-response-2.png)


**Parent Topic:**[Use the REST API Explorer](../concept/use-REST-API-Explorer.md)

