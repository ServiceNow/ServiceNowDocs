---
title: Update the incident
description: Update the incident record using either a PUT or PATCH function.
locale: en-US
release: yokohama
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use the REST API Explorer, REST APIs, Web services, API implementation, API implementation and reference]
---

# Update the incident

Update the incident record using either a PUT or PATCH function.

## Before you begin

Role required: admin, web\_service\_admin, or rest\_api\_explorer

## About this task

Use the REST API Explorer to send the following request:

`PUT https://instance.service-now.com/api/now/v1/table/incident/{sys_id}?sysparm_exclude_ref_link=true`

## Procedure

1.  In the top-left of the REST API Explorer, click **Modify a record \(PUT\)** or **Update a record \(PATCH\)**.

2.  In the Path Parameters section, select the **Incident \(incident\)** table.

3.  In the **sys\_id** field, enter the sys\_id of the record you created.

4.  In the Request Body section, click **Add a field**.

5.  Select the **Short description** field and specify a new value.

6.  Click **Send**.

    The response indicates the **Status code** and **Execution time** \(in milliseconds\) of the request.

    ![REST API Explorer PUT response](../image/rest-api-exp-put-response.png)

7.  Verify that the Response Body contains the updated **short\_description** value.


**Parent Topic:**[Use the REST API Explorer](../concept/use-REST-API-Explorer.md)

