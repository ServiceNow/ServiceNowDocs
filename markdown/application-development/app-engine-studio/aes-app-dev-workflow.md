---
title: Delegate developers using AES
description: Delegated development enables designated users without a system admin role to develop or deploy applications on the ServiceNow AI Platform. This enables administrators and delegated developers to work together to deliver custom applications through App Engine Studio \(AES\).
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure AES, Configure, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Delegate developers using AES

Delegated development enables designated users without a system admin role to develop or deploy applications on the ServiceNow AI Platform. This enables administrators and delegated developers to work together to deliver custom applications through App Engine Studio \(AES\).

After an administrator reviews a request, they delegate the development work by providing a link to the developer that opens App Engine Studio in your organization's development environment. The administrator can:

-   Send the link directly to a developer via email
-   Post the link on a portal page
-   Create a catalog item for delegated developers to request App Engine Studio access

## Delegated developer role in AES

The delegated developer role enables an admin to elevate user permissions to a dedicated role with specific access for App Engine Studio.

A delegated developer has more permissions than a user, but less than an admin. The delegated developers each have their own permissions.

An admin may have several delegated developers, each with their own set of permissions. For example, you may want a designated developer for developing a time-off request, and another developer with separate permissions for creating support tickets.

Some AES features may be inaccessible to the delegated developer, depending on permissions. Your role enables you to access, edit, and add objects. If a feature of App Engine Studio is unavailable to you, contact your system administrator.

For more information about delegated development and permissions, see [Exploring Delegated Development](../../applications/concept/c_DelegatedDevelopment.md).

## Restricted ability to create apps

In addition to delegated development, admins can define whether AES users can create apps or only work on existing apps.

-   Grant access to build applications in AES by adding users to the App Engine Studio Users group in your organization's development instance. Each group member is automatically assigned the sn\_app\_eng\_studio.user role.
-   To restrict access so that users can work in App Engine Studio but not create apps or see templates, add users to the App Engine Studio User Limited group.

**Parent Topic:**[Configure App Engine Studio](configure-aes.md)

