---
title: Configure a scripted REST API resource to require an ACL
description: By default, API resources/endpoints inherit security settings from the parent API. Define custom ACLs for a specific resource/endpoint to override the inherited settings.
locale: en-US
release: yokohama
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure a scripted REST API to require an ACL, Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Configure a scripted REST API resource to require an ACL

By default, API resources/endpoints inherit security settings from the parent API. Define custom ACLs for a specific resource/endpoint to override the inherited settings.

## Before you begin

Role required: web\_service\_admin or admin

## About this task

ACLs are checked for an authenticated user only.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.

2.  Select a scripted REST API.

3.  In the **Resources** related list, select a resource.

4.  In the **Security** tab, select the **Requires authentication** check box.

    You must select this check box to require an ACL for the resource. If you clear this check box, the resource becomes public and requires no credentials. Clear this check box only if you want to allow unauthenticated requests to access the resource, even if the parent REST service requires an ACL.

5.  Select the **Requires ACL authorization** check box.

6.  In the **ACL** field, select one or more ACLs that meet the security needs for the endpoint.

    Select only those ACLs that have a **Type** of **REST\_Endpoint**. Only users who have roles defined in the selected REST\_Endpoint type ACL are granted access to this resource.

    Selecting an ACL for a resource overrides any ACLs selected for the parent web service. Leave this field blank to use the ACLs selected for the parent web service.


**Parent Topic:**[Configure a scripted REST API to require an ACL](t_WbSvcRqACL.md)

**Related topics**  


[Configure a scripted REST API to require an ACL](t_WbSvcRqACL.md)

