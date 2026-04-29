---
title: Add a client extension point in the base application code
description: Add the UI extension point into a UI script in the base application code. To add the extension point, place an API call that identifies the location at which registered custom artifacts execute.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating and adding a client extension point, Using client extension points in client-side UI scripting, Using extension points to extend application functionality, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Add a client extension point in the base application code

Add the UI extension point into a UI script in the base application code. To add the extension point, place an API call that identifies the location at which registered custom artifacts execute.

## Before you begin

You must first create a UI extension point before you can add it to a UI script in the application code.Role required: admin or the specific role for the developer or administrator of the application

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](https://www.servicenow.com/docs/access?context=ACL-access-checks&version=australia&pubname=australia-application-development&ft:locale=en-US) and [Delegated development and deployment](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Procedure

1.  In the application code, access the existing UI script that you want to add a scripted extension point to, or create a new one.

    To learn more about creating UI scripts, see [UI scripts](../../../script/client-scripts/concept/c_UIScripts.md#).

2.  In the UI script, add a line of code at the location that you expect to collect and process the custom UI script output.

    The code must contain the `getExtensions` command that identifies the client extension point against which the custom UI scripts are registered. This line of code is similar to what is in an application code script include for scripted extension points. For an example, see [Add a scripted extension point in the base application code](add-scripted-ext-pt-base-script-include.md).


**Parent Topic:**[Creating and adding a client extension point](../concept/impl-client-ext-pts-base-code.md)

