---
title: Creating and adding a UI extension point
description: When developing an application, create UI extension points and add them to the server-side UI macros, such as HTML extensions, or the UI pages in the base application code.Create a UI extension point that you can place in the UI macros, such as HTML extensions, in the application code. By placing the UI extension point, you designate the specific location in the application code where data or objects can be sent to a customization and where data is returned.Add the UI extension point into a UI macro or HTML extension in the base application code. To add the extension point, place an API call that identifies the location at which registered custom artifacts execute.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Using server-side UI extension points, Using extension points, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Creating and adding a UI extension point

When developing an application, create UI extension points and add them to the server-side UI macros, such as HTML extensions, or the UI pages in the base application code.

Use a UI extension point to designate the specific location where data or objects can be sent to a registered custom UI macro and where returned results are processed.

**Parent Topic:**[Using UI extension points in server-side UI macros](ui-extension-points.md)

## Create a UI extension point

Create a UI extension point that you can place in the UI macros, such as HTML extensions, in the application code. By placing the UI extension point, you designate the specific location in the application code where data or objects can be sent to a customization and where data is returned.

### Before you begin

Role required: admin or the specific role for the developer or administrator of the application

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](https://www.servicenow.com/docs/access?context=ACL-access-checks&version=zurich&pubname=zurich-application-development&ft:locale=en-US) and [Delegated development and deployment](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

### About this task

Define the content and structure for an extension point. This definition should describe how a customization should be structured, how it interacts with the application code, and how the data that is returned by a customization at the extension point is processed.

By creating a good definition, you provide a structure for the functionality of the extensions.

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **UI Extension Points**.

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

Application scope against which the extension point is assigned. This is system-assigned and cannot be changed. For more information about the protections that are offered by the use of scoping, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

Restrict to this scope

</td><td>

Option for restricting the extension point to the application scope only.

</td></tr><tr><td>

Allow access over AJAX/REST

</td><td>

Option for enabling or disabling access to the UI extension point over AJAX or REST. To learn more about these development architectures and techniques, see [AJAX](../../../script/ajax/topic/p_AJAX.md#) and [REST APIs](../../../integrate/inbound-rest/concept/c_RESTAPI.md).

</td></tr><tr><td>

Description

</td><td>

Requirements for the custom UI macro, such as how the UI script should be structured and how it should operate with the application code.

</td></tr><tr><td>

Example

</td><td>

Example of how a custom UI macro that interacts with this extension point should be structured so it operates with the application code.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Add a UI extension point in the base application code

Add the UI extension point into a UI macro or HTML extension in the base application code. To add the extension point, place an API call that identifies the location at which registered custom artifacts execute.

### Before you begin

Role required: admin or the specific role for the developer or administrator of the application

You must first create a UI extension point before you can add it to a UI macro or UI page in the application code.

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](https://www.servicenow.com/docs/access?context=ACL-access-checks&version=zurich&pubname=zurich-application-development&ft:locale=en-US) and [Delegated development and deployment](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

### Procedure

1.  In the application code, access the existing UI macro that you want to add a scripted extension point to or create a new one.

    To learn more about creating UI macros with jelly tags, see [UI macros](../../../script/server-scripting/concept/c_UIMacros.md#) and [Jelly tags](../../../script/general-scripting/reference/r_JellyTags.md).

2.  In the UI macro, add a jelly tag with a line of code at the location that you expect to collect and process custom UI macro output.

    Typically, this line of code contains:

    -   A `call_extension` command that identifies the name of the UI extension point \(for example, `extension="global.KMArticle.ViewHeader"`\) against which the custom UI macros are registered.
    -   Arguments that are passed into the UI macro when it is rendered. For example, for a Knowledge Base article, `knowledgerecord="${knowledgeRecord}"` passes in the current knowledge record.
    -   \(Optional\) If there are multiple implementations of this extension point, using a `limit` command specifies that x number of implementations should be returned \(for example, `limit="1"`\). This figure shows a UI macro that contains these commands.
    ![UI extension point with a call_extension command in application code](../image/ui-extension-base-code-example.png)


