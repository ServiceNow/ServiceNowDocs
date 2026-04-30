---
title: Turn on ECMAScript 2021 \(ES12\) mode for a script
description: Use the latest JavaScript features supported with ECMAScript 2021 \(ES12\) mode in server-side scripts in applications that use ES5 Standards mode or Compatibility mode.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [JavaScript modes, JavaScript engine on the platform, Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Turn on ECMAScript 2021 \(ES12\) mode for a script

Use the latest JavaScript features supported with ECMAScript 2021 \(ES12\) mode in server-side scripts in applications that use ES5 Standards mode or Compatibility mode.

## Before you begin

Role required: delegated developer role or admin

## About this task

Turning on ECMAScript 2021 \(ES12\) mode for individual scripts is an option for scripts in global or scoped applications configured to use ES5 Standards mode or Compatibility mode. All scripts in applications with the JavaScript mode set to ECMAScript 2021 \(ES12\) use ECMAScript 2021 \(ES12\). Switching the JavaScript mode to ECMAScript 2021 \(ES12\) for an existing script might change the behavior of the script. For more information, see [Considerations for switching JavaScript modes](https://www.servicenow.com/docs/access?context=considerations-switching-javascript-mode&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

**Note:** Global applications can use ECMAScript 2021 \(ES12\) mode for individual scripts but not across the application.

## Procedure

1.  Navigate to a form with a script field.

    For example, to open a script include form, navigate to **All** &gt; **System Definition** &gt; **Script Includes** or enter `sys_script_include.list` in the navigation filter.

2.  Select an existing script or **New**.

3.  Select **Turn on ECMAScript 2021 \(ES12\) mode**.

    ![Option to turn on ECMAScript 2021 ES12 mode for a script.](../image/script-js-mode.png)

    **Note:** This option is read only for scripts in applications with the JavaScript mode set to ECMAScript 2021 \(ES12\), which automatically use ECMAScript 2021 \(ES12\).

4.  Select **Submit** or **Update** to save your changes.


**Parent Topic:**[JavaScript modes](c_JS_modes.md)

