---
title: Set the JavaScript mode for an application
description: Configure which ECMAScript features can be used in an application by selecting the JavaScript mode.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [JavaScript modes, JavaScript engine on the platform, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Set the JavaScript mode for an application

Configure which ECMAScript features can be used in an application by selecting the JavaScript mode.

## Before you begin

Role required: delegated developer role granting full access or admin

## About this task

The JavaScript mode is a design and runtime setting for custom applications and scripts. To support existing server-side scripts and new scripts developed to the ECMAScript 2021 standard, the JavaScript engine has three modes: ECMAScript 2021 \(ES12\), ES5 Standards, and Compatibility. For more information about each mode, see [JavaScript modes](c_JS_modes.md).

For applications that use ES5 Standards or Compatibility mode, you can also turn on ECMAScript 2021 \(ES12\) for individual scripts in the application. For more information, see [Turn on ECMAScript 2021 \(ES12\) mode for a script](set-es12-mode-scripts.md).

**Note:** Switching the JavaScript mode to ECMAScript 2021 \(ES12\) for an existing application might change the behavior of its scripts. For more information, see [Considerations for switching JavaScript modes](considerations-switching-javascript-mode.md).

## Procedure

1.  In the application navigator, enter `sys_app.list`.

2.  Select an application.

3.  In the **JavaScript Mode** field, select the mode to use.

    -   ECMAScript 2021 \(ES12\): Supports a subset of ECMAScript 2021 \(ES12\) and ECMAScript 2022 \(ES13\) syntax and features.
    -   ES5 Standards Mode: Supports ECMAScript5 syntax and features.
    -   Compatibility Mode: Used for all scripts developed prior to the addition of ES5 Standards mode.
4.  Select **Update**.


**Parent Topic:**[JavaScript modes](c_JS_modes.md)

**Related topics**  


[Legacy - Update a custom application record](https://www.servicenow.com/docs/access?context=t_UpdateAnApplicationRecord&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

