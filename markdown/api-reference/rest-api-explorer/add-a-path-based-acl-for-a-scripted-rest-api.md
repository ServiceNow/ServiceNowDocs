---
title: Add a path-based ACL for a scripted REST API
description: Path-based Access Control Levels \(ACLs\) enable you to define access control rules for scripted REST API endpoints using their resource path. This can be done independently of the ACL references on the operation record. Path-based ACLs enable more flexible security configurations, especially for read-only APIs and guest user experiences.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure a scripted REST API to require an ACL, Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Add a path-based ACL for a scripted REST API

Path-based Access Control Levels \(ACLs\) enable you to define access control rules for scripted REST API endpoints using their resource path. This can be done independently of the ACL references on the operation record. Path-based ACLs enable more flexible security configurations, especially for read-only APIs and guest user experiences.

## Before you begin

Role required: security\_admin or admin

Additional requirement: the full resource path from the API's SysWS operation record \(found in the "Resource path" field\)

## About this task

Path-based ACLs are defined in the sys\_security\_acl table with the type "REST Endpoint" and apply to specific REST API resource paths. Unlike operation-referenced ACLs \(which only apply when "Requires authentication" is checked\), path-based ACLs are evaluated for every request to matching resource paths.

**When to use Path-Based ACLs:**

-   You must add security to a read-only API that you can’t modify
-   You want to enable guest access to public APIs with controlled authorization
-   You must grant access based on custom roles not defined in the original API
-   You want to add security layers without modifying the original API record

**Important:** Path-based ACLs work alongside operation-referenced ACLs, not in place of them. All applicable ACLs must pass for access to be granted.

## Procedure

1.  Navigate to **All** &gt; **sys\_security\_acl.list**.

2.  Select **New**.

3.  Select **REST Endpoint** in the **Type** field.

4.  Select the necessary HTTP method for the ACL in the **Operation** field.

    -   GET
    -   POST
    -   PUT
    -   DELETE
    -   PATCH
    -   Or other HTTP methods as needed.
5.  Enter the fill API resource oath in the **Resource Path** field.

    **Example:** /api/sn\_pa\_designer/usage\_monitoring/resource

    **Tip:** Copy this value from the "Resource path" field on the SysWS operation record to help ensure accuracy.

6.  Configure the ACL script or condition to define your access rules.

7.  Select **submit**.


## Result

The path-based ACL is active and will be evaluated for any requests to this resource path.

**Parent Topic:**[Configure a scripted REST API to require an ACL](t_WbSvcRqACL.md)

**Related topics**  


[Configure a scripted REST API resource to require an ACL](t_WbSvcOpRqACL.md)

[View path-based ACLs](view-path-based-acls.md)

[View path-based ACLs from REST API Explorer](view-path-based-acls-from-rest-api-explorer.md)

