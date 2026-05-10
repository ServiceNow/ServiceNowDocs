---
title: Create a client extension point
description: Create a client extension point that you can place in the UI scripts in the application code. By placing the client extension point, you designate the specific location in the application code where data or objects can be sent to a customization, and where data is returned.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating and adding a client extension point, Using client extension points in client-side UI scripting, Using extension points to extend application functionality, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Create a client extension point

Create a client extension point that you can place in the UI scripts in the application code. By placing the client extension point, you designate the specific location in the application code where data or objects can be sent to a customization, and where data is returned.

## Before you begin

Role required: admin or the specific role for the developer or administrator of the application

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ACL-access-checks.md) and [Delegated development and deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/delegated-development-and-deployment/c_DelegatedDevelopment.md).

## About this task

Define the content and structure for an extension point. This definition should describe how a customization should be structured, how it interacts with the application code, and how the data that is returned by a customization at the extension point is processed.

By creating a good definition, you provide a structure for your extension points.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Client Extension Points**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_tqn_cfv_s1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the extension point. The name can be up to 100 alphanumeric characters, including special characters.

</td></tr><tr><td>

API Name

</td><td>

Name of the extension point API that is pre-pended with the application scope to which it applies. This is a system-assigned name and cannot be changed.

</td></tr><tr><td>

Application

</td><td>

Application scope against which the extension point is assigned. This is system-assigned and cannot be changed. For more information about the protections that are offered by the use of scoping, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationScope.md).

</td></tr><tr><td>

Restrict to this scope

</td><td>

Option for restricting the extension point to the application scope only.

</td></tr><tr><td>

Allow access over AJAX/REST

</td><td>

Option for enabling access to the client extension point over AJAX or REST. To learn more about these development architectures and techniques, see [AJAX](../../../script/ajax/topic/p_AJAX.md#) and [REST APIs](../../../integrate/inbound-rest/concept/c_RESTAPI.md).

</td></tr><tr><td>

Description

</td><td>

Requirements for the custom UI script, such as how the UI script should be structured and how it should operate with the application code.

</td></tr><tr><td>

Example

</td><td>

Example of how a custom UI script that interacts with this extension point should be structured so it operates with the application code.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Creating and adding a client extension point](../concept/impl-client-ext-pts-base-code.md)

