---
title: JavaScript engine on the platform
description: The JavaScript engine that evaluates server-side scripts supports the ECMAScript 2021 \(ES12\) standard.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# JavaScript engine on the platform

The JavaScript engine that evaluates server-side scripts supports the ECMAScript 2021 \(ES12\) standard.

No plugins or properties are required to install the new JavaScript engine.

The benefits of the new engine are:

-   Modern library code and scripting features, such as optional chaining, destructuring, const and let declarations, and arrow functions
-   Follows standard ECMAScript 2021 behavior

## What to know

The JavaScript engine provides an improved environment for developing scripts.

-   Beginning with the Xanadu release, when you create new scripts, ECMAScript 2021 \(ES12\) mode is turned on by default regardless of the JavaScript mode configured for the application.
-   Beginning with the Tokyo release, new and existing scoped applications can run in ECMAScript 2021 \(ES12\) mode.
-   Compatibility mode supports the legacy modifications to the legacy JavaScript engine.
-   Legacy code continues to work.

You configure the mode that the JavaScript engine uses in the design and runtime settings for applications. Available modes are ECMAScript 2021 \(ES12\), ES5 Standards, and Compatibility.

-   **[JavaScript modes](c_JS_modes.md)**  
JavaScript mode is a design and runtime setting for custom applications and scripts. To support existing server-side scripts and new scripts developed to the ECMAScript 2021 standard, the JavaScript engine has three modes: ECMAScript 2021 \(ES12\), ES5 Standards, and Compatibility.
-   **[JavaScript engine feature support](../reference/javascript-engine-feature-support.md)**  
Compare ECMAScript features between the ECMAScript 2021 \(ES12\) and ES5 Standards JavaScript modes in Yokohama. Both modes support a subset of ECMAScript features.

**Parent Topic:**[Server-side scripting](../../server-scripting/concept/c_ServerScripting.md)

**Related topics**  


[Update a custom application record](../../../build/applications/task/t_UpdateAnApplicationRecord.md)

