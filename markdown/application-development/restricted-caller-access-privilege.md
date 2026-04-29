---
title: Restricted caller access privilege settings
description: Define cross-scope access to an application, application resource \(such as an access control role, a business rule, a UI action, or a script include\), or event. You can even use these settings to allow or deny requests for access.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Restricted caller access privilege settings

Define cross-scope access to an application, application resource \(such as an access control role, a business rule, a UI action, or a script include\), or event. You can even use these settings to allow or deny requests for access.

## Restricted caller access privilege settings overview

Restricted caller access \[sys\_restricted\_caller\_access\] records track cross-scope applications or scripts that request access to an application, application resource, or event in the ServiceNow AI Platform. The ServiceNow AI Platform creates sys\_restricted\_caller\_access records when one of these actions occurs:

-   Caller access is set to **Caller Restriction** or **Caller Tracking**.
-   A cross-scope script attempts to access an application resource or event.

    **Note:** A system scope to target scope is an example of a cross-scope.


You can use these records to do these tasks:

-   Track cross-scope requests for access to an application resource. You can use access requests to determine which applications need access to resources and data from other application scopes.
-   Approve or deny any cross-scope requests for access to application resources or events. For example, you can create a Restricted Caller Access record to allow access for all scope-to-scope requests.

For more information, see [Requested restricted caller access \(RCA\)](requested-rca.md).

## Restricted caller access privilege setting combinations

As a target application owner, you can define various combinations of privilege settings for restricted caller access and specify whether access is allowed or denied for each relationship. RCA records must be created in the target application scope to control access to your application's resources. You can define various combinations of privilege settings for restricted caller access and specify whether access is allowed or restricted for each relationship.

You can define various combinations of the following settings:

-   **Scope**

    All application resources in a selected source or target scope. To learn more about application scopes, see [Application scope](c_ApplicationScope.md).

-   **Source**

    A specific application resource \(such as a business rule, script include, or table\) in a selected source scope.

-   **Target**

    A specific application resource in a selected target scope.


These restricted caller access privilege settings combinations include, but are not limited to, the following combinations:

-   Scope-to-scope: Control access from all resources in a source application to all resources in your target application
-   Scope-to-target: Control access from all resources in a source application to a specific resource in your target application
-   Source-to-scope: Control access from a specific source application resource to all resources in your target application
-   Source-to-target: Control access from a specific source application resource to a specific resource in your target application

For more information about these access setting combinations and to learn how to create each combination, see [Set the application scope, application resource, and event access](../task/scope-resource-access.md).

**Note:**

Source application developers who need to request access to resources in another application should coordinate with the target application owner. You can package Requested RCA records in your application, which will then be reviewed and approved or denied by the target application administrator upon installation.

## Activating application restricted caller access

You can activate application restricted caller access through one of the following methods:

-   Activate the Scoped Application Restricted Caller Access plugin \(com.glide.scope.access.restricted\_caller\).
-   Request the HR Service Delivery or Security Incident Response applications. By default, restricted caller access is active in these applications.
-   Enable the Restricted Caller Access system property for Workflow Studio.

For more information, see: [Activate application restricted caller access](../task/activate-RCA.md).

-   **[Activate application restricted caller access](../task/activate-RCA.md)**  
You can activate the Scoped Application Restricted Caller Access plugin \(com.glide.scope.access.restricted\_caller\) if you have the admin role.
-   **[Define cross-scope access to an application resource](../task/set-RCA-level.md)**  
Track cross-scope requests for access to an application resource and approve or deny requests.
-   **[Set the application scope, application resource, and event access](../task/scope-resource-access.md)**  
Create a record in the Restricted Caller Access Privileges \[sys\_restricted\_caller\_access\] table to set cross-scope resource access requests. Approve or deny requests from a source scope or source scope application resources to a target scope or to target scope application resources.

**Parent Topic:**[Application access settings](c_ApplicationAccessSettings.md)

