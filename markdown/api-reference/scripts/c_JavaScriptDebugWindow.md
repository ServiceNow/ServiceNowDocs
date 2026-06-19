---
title: JavaScript debug window
description: The JavaScript debug window appears in a bottom pane of the user interface when an administrator turns on debugging.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/scripts/c\_JavaScriptDebugWindow.html
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# JavaScript debug window

The JavaScript debug window appears in a bottom pane of the user interface when an administrator turns on debugging.

**Note:** The JavaScript debug window is not supported with Next Experience. For more information about supported features in Next Experience, see Considerations for activating Next Experience.

Use the debug window to access these tools.

-   JavaScript Log: JavaScript that runs on the browser, such as client scripts, can include a call to jslog\(\) to send information to the JavaScript log.
-   Field Watcher: a tool that tracks and displays all actions that the system performs on a selected form field.

-   **[Access the JavaScript debug window](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/t_UsingTheJavaScriptDebugWindow.md)**  
The JavaScript debug window enables access to the JavaScript Log and the Field Watcher tools.
-   **[Watching fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/c_FieldWatcher.md)**  
The field watcher tool tracks and displays all actions that the system performs on a selected form field.
-   **[Writing to the debug log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/c_WritingToTheDebugLog.md)**  
To write to the debug log in your client-side JavaScript, or UI policies, make a call to the global function `jslog()`.

**Parent Topic:**[Debugging scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/scripts/script-debug-overview.md)

