---
title: Writing client-side scripts
description: Write scripts that run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/client-side-scripting-overview.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Scripting, API implementation, API implementation and reference]
---

# Writing client-side scripts

Write scripts that run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.

## Client-side API reference

When writing client-side scripts, you use client-side JavaScript APIs to control aspects of how ServiceNow AI Platform is displayed and functions within the web browser. For information about available client-side APIs, see the [Client API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/api-client.md).

-   **[Client scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/client-scripts.md)**  
Client scripts allow the system to run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.
-   **[UI scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_UIScripts.md)**  
UI scripts provide a way to package client-side JavaScript into a reusable form, similar to how script includes store server-side JavaScript. Administrators can create UI scripts and run them from client scripts and other client-side script objects and from HTML code.
-   **[UI pages and macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/create-custom-ui-pages.md)**  
Use UI pages to create custom pages for an application and UI macros for custom controls or interfaces.
-   **[AJAX scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/p_AJAX.md)**  
AJAX \(asynchronous JavaScript and XML\) is a group of interrelated, client-side development techniques used to create asynchronous Web applications.
-   **[Display field messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_DisplayFieldMessages.md)**  
Rather than use JavaScript alert\(\), for a cleaner look, you can display an error on the form itself. The methods showFieldMsg\(\) and hideFieldMsg\(\) can be used to display a message just below the field itself.
-   **[General guidelines for client script design and processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/client-script-best-practices.md)**  
Well-designed client scripts can reduce the amount of time it takes users to complete a form.
-   **[Client-side scripting for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_MobilePlatformMigrationImpacts.md)**  
Client scripting for mobile is identical to scripting for the web, with some exceptions. All new scripts must conform to certain guidelines. The following items are affected on the mobile platform: client scripts, UI policies, navigator modules, and UI actions.

**Parent Topic:**[Scripting on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/scripting-landing.md)

**Related topics**  


[Client API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/api-client.md)

