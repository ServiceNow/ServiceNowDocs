---
title: Create a scripted extension point
description: Create a scripted extension point that can be placed in a script include in the base application code. By placing the scripted extension point, you designate the specific location in the application code where data or objects can be sent to a customization and where data is returned.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating and adding a scripted extension point, Using scripted extension points in server-side scripts, Using extension points to extend application functionality, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Create a scripted extension point

Create a scripted extension point that can be placed in a script include in the base application code. By placing the scripted extension point, you designate the specific location in the application code where data or objects can be sent to a customization and where data is returned.

## Before you begin

Role required: You must have the specific role for the developer or administrator of the application, or you must have the admin role.

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](https://www.servicenow.com/docs/access?context=ACL-access-checks&version=australia&pubname=australia-application-development&ft:locale=en-US) and [Delegated development and deployment](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=australia&pubname=australia-application-development&ft:locale=en-US).

## About this task

Define the content and structure for an extension point. This definition should describe how a customization should be structured, how it interacts with the application code, and how the data that is returned by a customization at the extension point is processed.

By creating a good definition, you provide a structure for the extensions.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the extension point. The name can be up to 100 alphanumeric characters, including special characters.|
    |API Name|Name of the extension point API that is pre-pended with the application scope to which it applies. This is a system-assigned name and cannot be changed.|
    |Application|Application scope against which the extension point is assigned. This is system-assigned and cannot be changed. For more information about the protections that are offered by the use of scoping, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US).|
    |Restrict to this scope|Option for restricting the extension point to the application scope only.|
    |Description|Requirements for the custom script include, such as how the UI script should be structured and how it should operate with the application code.|
    |Example|Example of how a custom script include that interacts with this extension point should be structured so it operates with the application code.|

4.  Click **Submit**.


**Parent Topic:**[Creating and adding a scripted extension point](../concept/impl-scripted-ext-pts-base-code.md)

