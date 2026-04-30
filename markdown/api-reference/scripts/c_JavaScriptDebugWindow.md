---
title: JavaScript debug window
description: The JavaScript debug window appears in a bottom pane of the user interface when an administrator turns on debugging.The JavaScript debug window enables access to the JavaScript Log and the Field Watcher tools.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# JavaScript debug window

The JavaScript debug window appears in a bottom pane of the user interface when an administrator turns on debugging.

**Note:** The JavaScript debug window is not supported with Next Experience in Utah. For more information about supported features in Next Experience, see [Considerations for activating Next Experience](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

Use the debug window to access these tools.

-   JavaScript Log: JavaScript that runs on the browser, such as client scripts, can include a call to jslog\(\) to send information to the JavaScript log.
-   Field Watcher: a tool that tracks and displays all actions that the system performs on a selected form field.

![JavaScript debug window](../image/JavaScriptLog.png "JavaScript debug window")

**Parent Topic:**[Debugging scripts](script-debug-overview.md)

## Using the JavaScript debug window

The JavaScript debug window enables access to the JavaScript Log and the Field Watcher tools.

### Before you begin

Role required: admin

### About this task

The steps to access the JavaScript debug window depend on which UI version you are using.

**Note:** The JavaScript debug window is not supported with Next Experience in Utah. For more information about supported features in Next Experience, see [Considerations for activating Next Experience](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

### Procedure

1.  Open the JavaScript debug window by navigating to the appropriate location for your version of the UI.

<table id="simpletable_HowToOpenJavaScriptLogAndFieldWatcherInDifferentUIs"><tbody><tr><td>

Core UI

</td><td>

1.  Click the gear icon in the banner frame.
2.  Click the **Developer** section.
3.  Toggle the **JavaScript Log and Field Watcher** switch.


</td></tr><tr><td>

UI15

</td><td>

1.  Click the gear icon in the banner frame.
2.  Click **JavaScript Log and Field Watcher**.


</td></tr><tr><td>

UI11

</td><td>

Click the debug icon \(![The debug icon](../image/Debug.png)\) in the banner frame.

</td></tr></tbody>
</table>    The JavaScript debug window re-opens at the bottom of the screen. The tab that is currently active in the window is the last tab that was active when the window was closed.

2.  Click a tab to use one of the debug window features.

    -   JavaScript Log
    -   Field Watcher

**Related topics**  


[Writing to the debug log](c_WritingToTheDebugLog.md#)

[Field watcher](c_FieldWatcher.md#)

