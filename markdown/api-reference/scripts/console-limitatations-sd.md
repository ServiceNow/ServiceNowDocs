---
title: Limitations with using Console
description: You need to be aware of a few limitations when you use Console to evaluate expressions while debugging a script in runtime.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Evaluate expressions in runtime using Console, Script Debugger and Session Log, Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Limitations with using Console

You need to be aware of a few limitations when you use Console to evaluate expressions while debugging a script in runtime.

-   The properties and values of an object don't display in Console. When you try to display an object to Console, only the string value of the object appears.
-   Console doesn't support GlideSystem printing methods, such as info\(\) and print\(\).
-   You can't use the this keyword in Console.
-   A script debugger timeout occurs when you evaluate expressions in Console.
-   While executing long scripts, if you see the response `Awaiting response from server`, you can't resume debugging or stop debugging using the resume or stop controls.

**Parent Topic:**[Evaluate expressions in runtime using Console](../task/evaluate-expressions.md)

