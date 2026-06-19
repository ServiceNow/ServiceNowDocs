---
title: Approve a collaboration request
description: Admins and App Engine admin can review and approve \(or reject\) people's requests to join an app's development in Creator Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/creator-studio/approve-collaboration-request.html
release: australia
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collaboration, Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Approve a collaboration request

Admins and App Engine admin can review and approve \(or reject\) people's requests to join an app's development in Creator Studio.

## Before you begin

If you have a controller instance configured, you must approve collaboration requests on your controller instance, not the non-production instance with Creator Studio. The controller instance is typically the production instance, but it can vary depending on how your Pipelines and Deployments application is configured. For more information, see [Configure your controller instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/config-controller-instance.md).

Role required: app\_engine\_admin

## About this task

**Note:** Users with a delegated developer role are automatically approved for collaboration.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Collaboration** &gt; **Collaboration Tasks**.

2.  Select the collaboration request in the **Number** column of the collaboration table.

    You can search or filter on the **App name** or **Invitee name** columns to find the request faster.

3.  Update the approval status in the **State** field.

    -   **Closed – Approved**
    -   **Closed – Rejected**
    -   **Canceled**
    -   **Closed – Failed**
4.  Update the record to save your changes.


**Parent Topic:**[Administering collaboration in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/creator-studio-admin-collab-tasks.md)

