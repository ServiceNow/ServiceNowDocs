---
title: Delete the incident
description: Delete the incident using a DELETE request.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the REST API Explorer, REST APIs, Web services, API implementation, API implementation and reference]
---

# Delete the incident

Delete the incident using a DELETE request.

## Before you begin

Role required: admin, web\_service\_admin, or rest\_api\_explorer

## About this task

Use the REST API Explorer to send the following request:

`DELETE https://instance.service-now.com/api/now/v1/table/incident/{sys_id}`

## Procedure

1.  In the top-left of the REST API Explorer, click **Delete a record \(DELETE\)**.

2.  In the Path Parameters section, select the **Incident \(incident\)** table.

3.  In the **sys\_id** field, enter the sys\_id of the record you created.

4.  Click **Send**.

    The response indicates the **Status code** and **Execution time** \(in milliseconds\) of the request.

    ![REST API Explorer DELETE response](../image/rest-api-exp-delete-response.png)

5.  Verify that the response **Status code** is `204`.


**Parent Topic:**[Use the REST API Explorer](../concept/use-REST-API-Explorer.md)

