---
title: Writing to the debug log
description: To write to the debug log in your client-side JavaScript, or UI policies, make a call to the global function jslog\(\).Enabling the glide.ui.ui\_policy\_debug property lets you monitor the processing of UI actions.JavaScript that runs on the browser, such as client scripts, can include a call to jslog\(\) to send information to the JavaScript Log. Users with the admin role can access this log.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Debugging scripts, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Writing to the debug log

To write to the debug log in your client-side JavaScript, or UI policies, make a call to the global function `jslog()`.

An example of using `jslog()` in JavaScript:

```
function logData (r ) {
    lastLogDate  = r. responseXML. documentElement. getAttribute ( "last_log_entry" ) ; var items  = r. responseXML. getElementsByTagName ( "log" ) ;
    jslog ( "response=" + r. responseText ) ; }
```

Additionally, when client scripts run, the name of the client script and timing information is displayed. This can be useful in determining which scripts are running and whether they are impacting performance.

**Parent Topic:**[Debugging scripts](script-debug-overview.md)

## Debug UI policies

Enabling the **glide.ui.ui\_policy\_debug** property lets you monitor the processing of UI actions.

Here are some sample log events from an incident policy that sets fields to read-only if the incident\_state is closed.

```
GlideFieldPolicy: Evaluating condition
GlideFieldPolicy:     incident_state (7) = 7 -> true
GlideFieldPolicy: --->>> TRUE
GlideFieldPolicy:    Setting opened_at disabled to true
GlideFieldPolicy:    Setting opened_by disabled to true
GlideFieldPolicy:    Setting closed_at disabled to true
GlideFieldPolicy:    Setting closed_by disabled to true
GlideFieldPolicy:    Setting company disabled to true

```

## Access the JavaScript log

JavaScript that runs on the browser, such as client scripts, can include a call to jslog\(\) to send information to the JavaScript Log. Users with the admin role can access this log.

### Before you begin

Role required: admin

### About this task

The steps to access the JavaScript debug window depend on which UI version you are using.

**Note:** The JavaScript debug window is not supported with Next Experience in Utah. For more information about supported features in Next Experience, see [Considerations for activating Next Experience](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

### Procedure

1.  Open the JavaScript log by navigating to the appropriate location for your version of the UI.

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
</table>    A new pane opens at the bottom of the screen. It shows the JavaScript Log tab and may also show the Field Watcher tab.

2.  If needed, select the **JavaScript Log** tab.

3.  Click the clear icon \(![The clear icon](../image/Eraser.png)\) to clear the contents of the log, as needed.


