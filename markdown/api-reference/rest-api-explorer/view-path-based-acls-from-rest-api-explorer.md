---
title: View path-based ACLs from REST API Explorer
description: Path-based Access Control Levels \(ACLs\) enable you to define access control rules for scripted REST API endpoints using their resource path. This can be done independently of the ACL references on the operation record. Path-based ACLs enable more flexible security configurations, especially for read-only APIs and guest user experiences.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View path-based ACLs, Configure a scripted REST API to require an ACL, Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# View path-based ACLs from REST API Explorer

Path-based Access Control Levels \(ACLs\) enable you to define access control rules for scripted REST API endpoints using their resource path. This can be done independently of the ACL references on the operation record. Path-based ACLs enable more flexible security configurations, especially for read-only APIs and guest user experiences.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **REST API Explorer**

2.  Locate your API and expand the methods.

3.  Select the menu icon next to the method that you want to check.

4.  Select **View Resource ACLs**.

5.  Review the list of path-based ACLs protecting that endpoint.

    ACL interaction rules:

    -   **No Overriding:** Path-based ACLs do override operation-referenced ACLs or other path-based ACLs.
    -   **All Must Pass:** All applicable ACLs must evaluate to true for access to be granted.
    -   **Owner Control:** If the API owner has restrictive ACLs, your path-based ACLs can’t bypass them.

**Parent Topic:**[View path-based ACLs](view-path-based-acls.md)

**Related topics**  


[Add a path-based ACL for a scripted REST API](add-a-path-based-acl-for-a-scripted-rest-api.md)

[Configure a scripted REST API resource to require an ACL](t_WbSvcOpRqACL.md)

[View path-based ACLs](view-path-based-acls.md)

