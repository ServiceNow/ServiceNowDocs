---
title: Learn about security and roles
description: Set up the security and roles for your UI Builder instance.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Learning UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Learn about security and roles

Set up the security and roles for your UI Builder instance.

Security and roles in UI Builder are controlled through your application scope, domain separation, and protection policy settings.

## Roles

Roles control access to features and capabilities in UI Builder. The admin role provides access to all features and capabilities. After access has been granted to a role, all the groups or users assigned to the role are granted the access. Roles can contain other roles, and any access granted to a role is granted to any role that contains it. For more information, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Application scope

Application scoping protects applications by identifying and restricting access to application files and data. Administrators can specify what parts of an application are accessible to other applications, which helps to protect data and application files. In UI Builder, System administrators and developers set application scope when creating a page. Note, you cannot change the application scope after creating the page, so choose your scope carefully.

Changing the scope in UI Builder also changes the scope in the ServiceNow AI Platform®, and vice versa.

When creating a page, it’s important for admins and developers to be aware of the scope they are in for the workspace or portal experience. Choose the correct application scope for your experience. The scope picker is to the right of the URL field. The scope defaults to the scope that the user is currently in within the ServiceNow AI Platform®.

![Application scope picker in UI Builder with the Global scope highlighted.](../image/application-scope-picker.png)

If you change to a different scope while in a page, you’re notified that you are in a different application scope from the one the page was created in. For more information, see [Application scope](../../../build/applications/concept/c_ApplicationScope.md).

## Delegated developers for UI Builder

If you have the application-specific admin role or the system-level admin role, you can delegate application development in ServiceNow® Studio to designated developers at the UI Builder application level.

## Protection policy

A protection policy prevents anyone from modifying and/or copying an application file or its related record. A protection policy is typically used when the author of an application is different than the company that uses the application. UI Builder notifies you if you try to modify a protected record. For more information, see [Application file protection policy](../../../build/applications/concept/c_ProtectingApplicationFiles.md).

**Parent Topic:**[Learning UI Builder](../concept/learning-uib.md)

