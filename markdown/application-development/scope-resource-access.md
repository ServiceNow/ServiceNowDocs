---
title: Set the application scope, application resource, and event access
description: Create a record in the Restricted Caller Access Privileges \[sys\_restricted\_caller\_access\] table to set cross-scope resource access requests. Approve or deny requests from a source scope or source scope application resources to a target scope or to target scope application resources.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Restricted caller access privilege settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Set the application scope, application resource, and event access

Create a record in the Restricted Caller Access Privileges \[sys\_restricted\_caller\_access\] table to set cross-scope resource access requests. Approve or deny requests from a source scope or source scope application resources to a target scope or to target scope application resources.

## Before you begin

If you enable application administration for the target application, only application administrators of the target application can set access to an application. If application administration is not enabled, an admin user can set access to an application.

Role required: application admin or admin

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](../concept/ACL-access-checks.md) and [Delegated development and deployment](../concept/c_DelegatedDevelopment.md).

## About this task

You can set the following restricted caller access privilege settings combinations:

-   Scope-to-Scope
-   Scope-to-Target
-   Source-to-Scope
-   Source-to-Target

**Note:** In the Rome release, we have enforced that an RCA privilege record must be present in the target application to grant access to a resource. This means that the target scope must match the application scope.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Application Restricted Caller Access**.

2.  On the form, fill in the fields.

<table id="table_sjf_q2q_zdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operation

</td><td>

Operation performed on the target resource.-   Read
-   Write
-   Create
-   Delete
-   Execute API


</td></tr><tr><td>

Source

</td><td>

Cross-scope record that is accessing a restricted application resource.

</td></tr><tr><td>

Source Scope

</td><td>

Scope of the calling application.

</td></tr><tr><td>

Source Table

</td><td>

Table that contains the Source record.

</td></tr><tr><td>

Source Type

</td><td>

Type of record that is calling the application resource:-   ACL
-   Business Rule
-   Document Title
-   Flow
-   Flow Action
-   GlideScopedEvaluator
-   Inbound Email Script
-   Orchestration RunScript Activity
-   Record Producer Script
-   Service Portal Widget
-   Scheduled Script
-   Scope
-   Script Include
-   UI Action
-   UI Macro
-   UI Page
-   Workflow Activity
For example, to allow access from an entire application, select **Scope**.

</td></tr><tr><td>

Status

</td><td>

Status of the access request:-   Requested
-   Denied
-   Allowed
-   Invalidated
**Note:** If a calling resource changes, the restricted caller access record status changes to Invalidated. If you enable application administration, only application administrators of the target application can update the status of a request.

</td></tr><tr><td>

Target

</td><td>

Record of the requested resource.

</td></tr><tr><td>

Target Scope

</td><td>

Scope of the requested resource.

</td></tr><tr><td>

Target Table

</td><td>

Table that contains the Target record.

</td></tr><tr><td>

Target Type

</td><td>

Type of requested resource.-   Event

**Note:** An event is a special type of target for restricted caller access. By selecting an event in a target scope, you give a source application permission to queue an event that is registered as part of a target application. However, if you set the caller access on the event registry to None, it prevents cross-scope access calls to an event. This setting combination is a one-to-one relationship. To learn more about events, and their function, see [Events](https://www.servicenow.com/docs/access?context=events&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). If you set caller access to None on the event registry, the cross-scope access calls to an event are denied.

-   Scope
-   Table
-   Script Include
For example, to allow access to an entire application, select **Scope**.

</td></tr></tbody>
</table>
-   **[Scope-to-scope settings](../reference/scope-to-scope-settings.md)**  
Allow or deny access of all application resources in a source scope to all application resources in a target scope. This setting combination is a many-to-many relationship.
-   **[Scope-to-target settings](../reference/scope-to-target-settings.md)**  
Allow or deny access of all application resources in a source scope to a specific application resource \(business rule, table, script include, or event\) in a target scope.
-   **[Source-to-scope settings](../reference/source-to-scope-settings.md)**  
Allow or deny access of a specific application resource in a source scope to all application resources in a target scope.
-   **[Source-to-target settings](../reference/source-to-target-settings.md)**  
Allow or deny access of a specific application resource in a source scope to a specific application resource in a target scope.

**Parent Topic:**[Restricted caller access privilege settings](../concept/restricted-caller-access-privilege.md)

