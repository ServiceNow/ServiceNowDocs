---
title: Add a scripted extension point in the base application code
description: Add the scripted extension point into a script include in the base application code. To add the extension point, include an API call that identifies the location at which registered custom artifacts execute.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/add-scripted-ext-pt-base-script-include.html
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Creating and adding, Using server-side scripted extension points, Using extension points, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Add a scripted extension point in the base application code

Add the scripted extension point into a script include in the base application code. To add the extension point, include an API call that identifies the location at which registered custom artifacts execute.

## Before you begin

Role required: You must have the specific role for the developer or administrator of the application, or you must have the admin role. You must first create a scripted extension point before you can add it to a script include in the application code.

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/building-applications/ACL-access-checks.md) and [Delegated development and deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md).

## Procedure

1.  In the application code, access the existing script include that you want to add a scripted extension point to, or create a new script include.

    To learn more about creating script includes, see [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/c_ScriptIncludes.md).

2.  In the script include, add a line of code at the location that you expect to collect and process the custom script output.

    The code must contain the [GlideScriptedExtensionPoint - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/server-api-reference/GlideScriptedExtPtScopedAPI.md) method that identifies the extension point against which the custom script includes are registered. For example:

    \[Omitted image "Ext\_point\_script\_include\_example\_short.png"\] Alt text: Script include with Call getExtensions command in application code

    **Note:** It is also a good practice to deliver error messages for application customizers when their custom scripts run in an extension instance. If something fails when the function returns arguments to the extension point, the error messages include information about how to troubleshoot the custom script.


**Parent Topic:**[Creating and adding a scripted extension point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/impl-scripted-ext-pts-base-code.md)

