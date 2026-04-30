---
title: Client-side scripting
description: Run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Client-side scripting

Run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.

The client-side [Glide](https://www.servicenow.com/docs/access?context=r_GlideClassOverview&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) API provides classes and methods that you can use in client scripts.

## Before you begin

Understand the limitations of your scripting environment. For example, client scripts run on forms in the Service Portal or Mobile environments can only include certain APIs. For more information, see [Mobile client GlideForm \(g form\) scripting and migration](https://www.servicenow.com/docs/access?context=r_MobilePlatformMigrationImpacts&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

-   **[Client-side scripting design and processing](client-script-best-practices.md#)**  
Well-designed client scripts can reduce the amount of time it takes users to complete a form.
-   **[Client scripts](client-scripts.md)**  
Client scripts allow the system to run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.
-   **[UI scripts](c_UIScripts.md#)**  
UI scripts provide a way to package client-side JavaScript into a reusable form, similar to how script includes store server-side JavaScript. Administrators can create UI scripts and run them from client scripts and other client-side script objects and from HTML code.
-   **[Catalog client scripts](c_CatalogClientScriptCreation.md#)**  
Client-side scripts can add dynamic effects and validation to forms. Scripts can apply to service catalog items or variable sets, allowing administrators to use the same functionality that is available on other forms.
-   **[Mobile client GlideForm \(g form\) scripting and migration](../reference/r_MobilePlatformMigrationImpacts.md)**  
Client scripting for mobile is identical to scripting for the web, with some exceptions. All new scripts must conform to certain guidelines. The following items are affected on the mobile platform: client scripts, UI policies, navigator modules, and UI actions.
-   **[AJAX](../../ajax/topic/p_AJAX.md#)**  
AJAX \(asynchronous JavaScript and XML\) is a group of interrelated, client-side development techniques used to create asynchronous Web applications.

**Parent Topic:**[Scripting](../../topic/c_Script.md)

