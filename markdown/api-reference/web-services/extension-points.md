---
title: Using extension points to extend application functionality
description: Use extension points to extend the functionality of an application without altering the original application code. You can use pre-existing extension points available in selected ServiceNow AI Platform applications, or you can add extension points when you develop custom applications in your own instance.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Using extension points to extend application functionality

Use extension points to extend the functionality of an application without altering the original application code. You can use pre-existing extension points available in selected ServiceNow AI Platform applications, or you can add extension points when you develop custom applications in your own instance.

## Using extension points

By using extension points, you can integrate customizations without actually altering the core components in the application code. Extension points can prevent your custom code interactions from breaking, which often occurs after an upgrade if you directly embed the custom code into the application code.

Extension points that are embedded in the application code act as out-points, where data passes to the custom code, and as in-points that handle the returned results. When creating an application, the returned data or objects must conform to the requirements that you define for the extension point.

**Note:** Some out-of-box configured CSM Query Rules cannot be changed or disabled because they are also used in constants within a business rule.

## Types of extension points

You can create extension points to process the custom code that uses the following types of artifacts:

-   **Scripted extension points**

    Extension points in server-side script includes that store JavaScript functions and object classes. To learn about scripts includes and how to implement scripted extension points in the application and custom code, see:

    -   [Script includes](../../../script/server-scripting/concept/c_ScriptIncludes.md#)
    -   [Creating and adding a scripted extension point](impl-scripted-ext-pts-base-code.md)
    -   [Using extension points to extend application functionality](extension-points.md)
-   **UI extension points**

    Extension points that are used in server-side UI macros such as HTML extensions.

    UI macros are discrete scripted components that you can add to the user interface. You use them to add custom content to a UI page, without having to directly modify the page. For example, you can use UI macros to add headers and footers to the standard Knowledge Base View \(kb\_view\) UI page in which KB articles appear.

    To learn about UI macros and how to implement UI extension points in the application and custom code, see:

    -   [UI macros](../../../script/server-scripting/concept/c_UIMacros.md#)
    -   [Creating and adding a UI extension point](impl-ui-ext-pts-base-code.md#)
    -   [Using extension points to extend application functionality](extension-points.md)
-   **Client extension points**

    Extension points that are used in client-side UI scripting, typically for modifying forms.

    UI scripts enable you to package client-side JavaScript into a reusable form, which is similar to how script includes store server-side JavaScript. You can create UI scripts and run them from client scripts, from other client-side script objects, and from HTML code.

    To learn about UI scripts and how to implement client extension points in application and custom code, see:

    -   [UI scripts](../../../script/client-scripts/concept/c_UIScripts.md#)
    -   [Creating and adding a client extension point](impl-client-ext-pts-base-code.md)
    -   [Using extension points to extend application functionality](extension-points.md)

When you use extension points to process customizations, you create a defined structure for integrating custom data or functionality into an application. Custom server-side script includes, UI macros such as HTML extensions, and client-side UI scripts are all external to the application code and only interact with it at specified extension points.

## Application code

The term application code refers to:

-   **Standard application code**

    Standard, or base, application code that comprises the ServiceNow AI Platform.

    Pre-defined extension points are already embedded in certain applications, such as Customer Service Management and Field Service Management. To learn more about the ServiceNow AI Platform applications that contain pre-defined extension points, see the following:

    |Application|Extension point topic|
    |-----------|---------------------|
    |Coaching|[Coaching troubleshooting](https://www.servicenow.com/docs/access?context=coaching-troubleshooting&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)|
    |Continual Improvement Management|[Improvement with other applications](https://www.servicenow.com/docs/access?context=cim-integration&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)|
    |Customer Service Management|[Extension points in Customer Service Management](https://www.servicenow.com/docs/access?context=extension-points-customer-service&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)|
    |[Creating custom user roles](https://www.servicenow.com/docs/access?context=creating-custom-csm-user-roles&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)|
    |[CSM integration with Change Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-change&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)|
    |[CSM integration with Incident Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-incident&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)|
    |[CSM integration with Problem Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-problem&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)|
    |[CSM integration with Request Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-request&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)|
    |Field Service Management|[Extension points in Field Service Management](https://www.servicenow.com/docs/access?context=extension-points-field-service&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)|
    |Knowledge Management|[Use extension points for Knowledge Management](https://www.servicenow.com/docs/access?context=extension-points-km-plugins&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)|
    |Orchestration|[Client software distribution extension network](https://www.servicenow.com/docs/access?context=c_CSDExtensionFramework&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) [Installed with client software distribution](https://www.servicenow.com/docs/access?context=r_IWClientSWDist&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)|
    |Password Reset|[Password Reset script includes](https://www.servicenow.com/docs/access?context=c_InstalledPasswordResetScripts&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)|

-   **Internally developed custom applications for your enterprise**

    You can add extension points to handle the registration of custom artifacts that are used to modify or extend the functionality of an application. When developers create custom code, they register, or pair, specific custom artifacts with specific extension points. Adding extension points enables integration of future customizations without having to change your base code.


## Creating an extension point in the application code

You want to ensure that the internally developed applications that you create for your enterprise can be properly customized, combined, and upgraded as needed. Extension points enable you to modify the functionality and user interface for an application without editing its core components. Use of extension points also creates a highly defined structure for functionality extensions.

When you create an extension point, you can restrict its use to the application scope in which it is defined or specify that the extension point can run in all scopes globally. If the application scope is restricted, customizations that are registered against the extension point can only run in the designated application scope. Before designing and building an application that includes extension points, you should:

-   Identify where to place extension points in the application code to accommodate custom script includes, UI macros, or UI scripts.
-   Determine the content and structure for an extension point. This definition should describe how a customization should be structured, how it interacts with the application code, and how the data that is returned by a customization at the extension point is processed.

To create extension points and embed them in the application code, perform the following tasks:

1.  Create an extension point and define its custom interface. This is an example of a scripted extension point.

    ![Scripted extension point example](../image/Extension_point_example.png)

2.  Designate specific places in the application code where data or objects can be sent to a customization, and where data is returned.
3.  Create an artifact, such as a script include, UI macro, or UI script, that calls the [GlideScriptedExtensionPoint - Scoped](../../../app-store/dev_portal/API_reference/GlideScriptedExtensionPointAPI/concept/GlideScriptedExtPtScopedAPI.md#) method. This method identifies the extension point at which registered custom artifacts execute in the application code.

    ![Base application code script include with getExtensions command.](../image/Extension_point_script_include_example.png)


## Enabling debugging and logging

When you create a extension point, you should also enable debugging and logging. Debugging and logging help you to identify and fix issues that are related to the use of custom artifacts with an extension point. When you enable the debugger, you can set break points in script includes, UI macros, or UI scripts. You can check the logs to see the following details:

-   When an extension point finds active extension instances, including the total number of extension instances found and the time each extension instance was found.
-   When an extension point executes extension instances, including the total number of custom artifacts executed and the time of each executed. It also includes the total number that failed to execute and the time at which each extension instance failed.

**Note:** To learn more about how to enable debugging and how it works, see:

-   [Script Debugger and Session Log](../../../script/debugging/concept/script-debugger.md)
-   [Debugging applications](../../../script/debugging/concept/c_DebuggingApplications.md#)
-   [Writing to the debug log](../../../script/debugging/concept/c_WritingToTheDebugLog.md#)

## Registering a custom artifact against an extension point

When you are customizing an application, you extend the base functionality by using custom artifacts, such as server-side script includes, UI macros, or client-side UI scripts. To design and build custom artifacts, perform the following tasks:

1.  Review the listing of available extension points that are appropriate to the specific type of custom artifact that you are creating.
    -   These listings include extension points that you created and any pre-defined extension points that are embedded in the ServiceNow AI Platform functions.
    -   Each listing includes information about an extension point in the application code that calls a custom artifact and what data or objects should be returned to it.
2.  Select an extension point.
3.  Determine how to structure the custom artifact. The structure should be based on the extension point descriptions. The descriptions include the requirements for using the artifact with the custom code and where the artifact will located in the base application code.
4.  Create the custom artifact and code when you register it against the selected extension point. Through registration, you create an extension instance record that links the extension point definition to its implementation in the custom artifact.

## How registered custom artifacts are processed

When the application code executes and finds an embedded API call containing an extension point, it:

1.  Uses the extension point in the API call to determine which custom artifacts are registered against it.
2.  Sends the appropriate data or objects to the registered custom artifacts.
3.  Collects the returned output from each custom artifact.
4.  Processes and incorporates the returned results into the base application.

-   **[Using scripted extension points in server-side scripts](scripted-extension-points.md)**  
Use the scripted extension points in the server-side script includes that store JavaScript functions and object classes. By using extension points, you can integrate customizations without actually altering the core components in the application code.
-   **[Using UI extension points in server-side UI macros](ui-extension-points.md)**  
Use UI extension points in the server-side UI macros, such as HTML extensions, to add custom content to a UI page without having to directly modify the page. By using UI extension points, you can integrate customizations without actually altering the core components in the application code.
-   **[Using client extension points in client-side UI scripting](client-extension-points.md)**  
Use client extension points in client-side UI scripting to modify forms, so that you do not have to directly modify the form. By using client extension points, you can integrate customizations without actually altering the core components in the application code.

**Parent Topic:**[Additional integration resources](../../../integrate/outbound-web-services/concept/additional-integration-resources.md)

