---
title: JavaScript engine on the platform
description: The JavaScript engine that evaluates server-side scripts supports the ECMAScript 2021 \(ES12\) standard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/c\_JS\_engine\_upgrade.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Write server-side scripts, Scripting, API implementation, API implementation and reference]
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

-   **[JavaScript modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_JS_modes.md)**  
JavaScript mode is a design and runtime setting for custom applications and scripts. To support existing server-side scripts and new scripts developed to the ECMAScript 2021 standard, the JavaScript engine has three modes: ECMAScript 2021 \(ES12\), ES5 Standards, and Compatibility.
-   **[Updates to the JavaScript engine in Brazil](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/updates-javascript-engine.md)**  
Review the updates to the JavaScript engine on the ServiceNow AI Platform in the Brazil release.

**Parent Topic:**[Writing server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/server-side-scripting-overview.md)

**Related topics**  


[Modify an app's settings in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/modify-an-apps-settings-in-servicenow-studio.md)

