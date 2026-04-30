---
title: Configure a scripted REST API to require an ACL
description: Requests to scripted REST APIs respect platform ACLs, and the requesting user must meet any table ACL requirements to access instance data. Additionally, you can configure the scripted REST API to require a specific ACL.
locale: en-US
release: xanadu
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Configure a scripted REST API to require an ACL

Requests to scripted REST APIs respect platform ACLs, and the requesting user must meet any table ACL requirements to access instance data. Additionally, you can configure the scripted REST API to require a specific ACL.

## Before you begin

Role required: web\_service\_admin

## About this task

The ACLs selected in this task apply to all API endpoints.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.

2.  Select a scripted REST API.

3.  In the **Default ACLs** field, select one or more ACLs that meet the security needs for the API. Select only those ACLs that have a **Type** of **REST\_Endpoint**.

    A requesting user must satisfy at least one of the selected ACLs. It is not necessary to satisfy all selected ACLs.

4.  Click **Update**.


## What to do next

You can override the API security settings for each individual API resource/endpoint. For details, see [Configure a scripted REST API resource to require an ACL](t_WbSvcOpRqACL.md).

-   **[Configure a scripted REST API resource to require an ACL](t_WbSvcOpRqACL.md)**  
By default, API resources/endpoints inherit security settings from the parent API. Define custom ACLs for a specific resource/endpoint to override the inherited settings.

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

