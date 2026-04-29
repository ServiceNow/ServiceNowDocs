---
title: Registering custom UI macros against the UI extension points
description: Register custom UI macros against a selected UI extension point in the application code.Create a custom UI macro and code when you register it against a selected UI extension point.Review the listing of custom UI macros that are registered against a UI extension point. Extension instances indicate the application scope in which registered custom UI macros are used and provides a link to each. You can also activate or inactive an extension instance.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using UI extension points in server-side UI macros, Using extension points to extend application functionality, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Registering custom UI macros against the UI extension points

Register custom UI macros against a selected UI extension point in the application code.

By registering custom UI macros, you create an extension instance record that links the UI extension point definition to its implementation in the custom UI macro.

**Parent Topic:**[Using UI extension points in server-side UI macros](ui-extension-points.md)

## Register a custom UI macro

Create a custom UI macro and code when you register it against a selected UI extension point.

### Before you begin

Role required: application-specific developer, application-specific admin, or admin

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](https://www.servicenow.com/docs/access?context=ACL-access-checks&version=australia&pubname=australia-application-development&ft:locale=en-US) and [Delegated development and deployment](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=australia&pubname=australia-application-development&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **UI Extension Points**.

2.  In the UI Extension Point \[sys\_ui\_extension-point\] table, select the extension point that you want to register a custom UI macro against.

    **Note:** This listing includes UI extension points that you created and any pre-defined UI extension points that are embedded in ServiceNow AI Platform functions \(for example, Customer Service Management and Field Service Management\).

    To learn more about functions that contain pre-defined extension points, see the Related Topics links in [Using extension points to extend application functionality](extension-points.md).

3.  In the UI Extension Point record, click the **Create Implementation** related link to create a new custom UI macro and register it against the selected UI extension point.

4.  In the UI Macro form, create the custom code.

    To learn more about creating UI macros, see [UI macros](../../../script/server-scripting/concept/c_UIMacros.md#).

5.  Click **Update**.


### Result

The custom UI macro is created and registered against the UI extension point.

## Review UI extension instances

Review the listing of custom UI macros that are registered against a UI extension point. Extension instances indicate the application scope in which registered custom UI macros are used and provides a link to each. You can also activate or inactive an extension instance.

### Before you begin

Role required: admin or the specific role for the developer or administrator of the application

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](https://www.servicenow.com/docs/access?context=ACL-access-checks&version=australia&pubname=australia-application-development&ft:locale=en-US) and [Delegated development and deployment](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=australia&pubname=australia-application-development&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **UI Extension Points**.

2.  In the UI Extension Point \[sys\_ui\_extension\_point\] table, select the UI extension point that you want to view extensive instances for.

3.  In the Implementations related list of the UI Extension Point record, select a UI extension instance.

    The system displays the UI Extension Instance record.

    |Field|Description|
    |-----|-----------|
    |Point|Unique name for the UI extension point. The name can have up to 100 alphanumeric characters, including special characters.|
    |Class|UI macro in the application code in which the UI extension point is implemented.|
    |Application|Application scope against which the extension point is assigned. This is system-assigned and cannot be changed. For more information about the protections that are offered by the use of scoping, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US).|
    |Active|Active extension point in the current instance. To inactivate an extension point, clear the check box.|

4.  Click **Submit**.


**Related topics**  


[UI macros](../../../script/server-scripting/concept/c_UIMacros.md#)

[Using extension points to extend application functionality](extension-points.md)

