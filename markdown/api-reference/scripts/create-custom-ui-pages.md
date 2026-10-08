---
title: UI pages and macros
description: Use UI pages to create custom pages for an application and UI macros for custom controls or interfaces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/create-custom-ui-pages.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Write client-side scripts, Scripting, API implementation, API implementation and reference]
---

# UI pages and macros

Use UI pages to create custom pages for an application and UI macros for custom controls or interfaces.

Every UI Page is a [Jelly](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_JellyTags.md) template. Jelly turns XML into executable code. A UI Page works similar to how an index.html file is used in an AngularJS application. Jelly tags in the HTML field of the UI Page form contain AngularJS logic.

Creating [UI macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_UIMacros.md) requires knowledge of Jelly script. Review the existing UI macros for examples and suggested approaches. Those who want to build custom interfaces with JavaScript technologies should consider Service Portal as an alternative.

-   **[UI pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_UIPages.md)**  
UI pages can be used to create and display forms, dialogs, lists, and other UI components.
-   **[UI macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_UIMacros.md)**  
UI macros are discrete scripted components administrators can add to the user interface.
-   **[Jelly tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_JellyTags.md)**  
Use Jelly to turn XML into HTML.
-   **[HTML syntax editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/html-syntax-editor.md)**  
The HTML syntax editor provides support for editing HTML and Jelly scripts and defines what's rendered when the page is displayed. The HTML syntax editor can contain either static XHTML or dynamically generated content defined as Jelly, and can call script includes and UI Macros.

**Parent Topic:**[Writing client-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/client-side-scripting-overview.md)

