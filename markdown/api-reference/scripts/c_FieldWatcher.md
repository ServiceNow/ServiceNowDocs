---
title: Watching fields
description: The field watcher tool tracks and displays all actions that the system performs on a selected form field.Access field-level debugging information using the field watcher.The field watcher displays field information and configuration options.Administrators may need to watch a hidden field.When information for a watched field is changed and the record is updated, the field watcher tab displays relevant information at the bottom.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [JavaScript debug window, Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Watching fields

The field watcher tool tracks and displays all actions that the system performs on a selected form field.

**Note:** Field watcher is not supported with Next Experience. For more information about supported features in Next Experience, see [Considerations for activating Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-adoption-paths.md).

Administrators can use the field watcher to figure out what happens to the field and how the value of the field changes when an event such as the firing of a business rule or enforcement of a data policy, takes place. Administrators can also impersonate non-admin users to debug what happens when those users make changes on an instance. Only one field can be watched at a time. Non-admin users with the impersonator role have access to the field watcher feature.

## How the field watcher works

The Field Watcher tool logs activity when any of the following events occur on a field:

-   The default value is set on the field.
-   User access rights for the field change due to an ACL or dictionary setting.
-   A data policy prevents the value from being set.
-   A reference qualifier query of the field value executes.
-   A UI policy changes a field to or from read-only, visible, mandatory, or editable.
-   A dependent value in another field restricts field choices.
-   The value of the field is set or changed based on:
    -   Assignment rules
    -   Actions from an engine, such as the workflow engine
    -   Business rules
    -   User entries
    -   Client scripts
    -   UI actions

**Note:** The field watcher works only on form fields. It cannot be used on list fields. Also, field watcher is not available on password-protected fields or encrypted fields. Field watcher is only available within the UI frame. The option to watch a field does not appear in the context menu if you open a record outside of the UI frame, for example, in a new tab.

**Parent Topic:**[JavaScript debug window](c_JavaScriptDebugWindow.md)

## Use field watcher

Access field-level debugging information using the field watcher.

### Before you begin

Role required: none

### Procedure

1.  Navigate to the form for which you want to view field-level debugging information.

2.  Activate field watcher by right-clicking any field label on a form and select **Watch - '&lt;field name&gt;'**.

    The debug icon appears next to the field label. From this point on, the field watcher records every action taken on the selected field. For example, if you are watching a Priority field, if the priority is changed from Moderate to Low and the record is updated, the field watcher will display information about that change.

3.  View the field watcher log by clicking the debug icon.

    A new pane opens at the bottom of the screen, showing a field watcher tab. It may also show tabs for [JavaScript Logging](c_WritingToTheDebugLog.md#) and JavaScript Debugger.

4.  Click the **Field Watcher** tab, if needed.

5.  Stop watching a field by right-clicking the field and selecting **Unwatch - &lt;field name&gt;**.

    To watch another field, right-click that field and select **Watch - &lt;field name&gt;**.

6.  Clear the field watcher log by clicking the clear log icon.

7.  Resize the field watcher pane by dragging the splitter bar up or down.

    Dragging the splitter bar to the bottom of the screen closes the field watcher pane. Reopen the pane by clicking the debug icon again.


### Field watcher tab details

The field watcher displays field information and configuration options.

The left-side of the Field Watcher tab shows the following information for the watched field.

-   **Table**: table to which the field belongs.
-   **Element**: field label.
-   **Type**: type of data stored in the field.
-   **Dependent**: field on which the current field depends.
-   **Reference**: table from which the field's value originates, if applicable.
-   **Reference Qual**: reference qualifiers that may be restricting data on the field.
-   **Attributes**: attributes on the field as specified in the dictionary entry for that field.

On the right-side of the Field Watcher tab, select the types of activity information you want to see for the selected field. Clear the check box for any type of information that is not needed.

### Watching a hidden field

Administrators may need to watch a hidden field.

#### Procedure

1.  Use the dictionary to determine the column name of the field.

2.  Elevate privileges to the security\_admin role.

3.  Navigate to **System Definition** &gt; **Scripts Background**.

4.  In Run script \(JavaScript executed on server\), enter the following command:

    ```javascript
    gs.getSession ( ). setWatchField ( "hidden_field" ) ;
    ```

    Replace hidden\_field with the column name of the hidden field.

5.  Navigate to the form containing the missing field.

    The Field Watcher tab output contains information about the hidden field.


## Viewing information for the watched field

When information for a watched field is changed and the record is updated, the field watcher tab displays relevant information at the bottom.

Field watcher information includes:

-   **Timestamp**: time the field was changed using the HH:MM:SS \(ms\) format.
    -   **Orange text**: server-side changes, such as ACLs.
    -   **Blue text**: client-side changes, such as client scripts.
-   **Type of object that changed the field and its associated name**: The type of item that changed on the field; for example, **CLIENT SCRIPT**, **BUSINESS RULE**, or **ACL**. In the case of scripts, business rules, or other configuration-type fields, field watcher displays the name of the script or business rule that changed the field, if any. Click the name to go directly to the record for that item.
-   **Old and new values**: The old and new values for the field, if the value changed0. Field watcher does not record the value if it was inserted in the form by default at the time the record was created.
-   **Additional information**: Call tracing information, such as the name of the script engine or workflow that changed the field. Click the plus icon to expand the selection.
    -   **Orange text**: Indicates server-side activity.
    -   **Blue text**: Indicates client-side activity.

