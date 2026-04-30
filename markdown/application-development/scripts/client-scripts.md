---
title: Client scripts
description: Client scripts allow the system to run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Client-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Client scripts

Client scripts allow the system to run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.

Introduction to client scripts, script types, APIs, and good practices

Use client scripts to configure forms, form fields, and field values while the user is using the form. Client scripts can:

-   make fields hidden or visible
-   make fields read only or writable
-   make fields optional or mandatory based on the user's role
-   set the value in one field based on the value in other fields
-   modify the options in a choice list based on a user's role
-   display messages based on a value in a field

**Warning:**

Client scripts are intended to optimize the user experience on a form. Client scripts are not meant to protect unwanted access to data.

To prevent unwanted access to data, ensure that sensitive fields are hidden or read-only through ACLs or data policies.

For more information, see [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) or [Data policy](https://www.servicenow.com/docs/access?context=c_DataPolicy&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Where client scripts run

With the exception of onCellEdit\(\) client scripts, client scripts only apply to forms and search pages. If you create a client script to control field values on a form, you must use one of these other methods to control field values when on a list.

-   Create an access control to restrict who can edit field values.
-   Create a business rule to validate content.
-   Create a data policy to validate content.
-   Create an onCellEdit\(\) client script to validate content.
-   Disable list editing for the table.

**Note:** Client scripts are not supported on ServiceNow mobile applications.

## Client script form

<table id="table_trz_nvg_zz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the client script.

</td></tr><tr><td>

Table

</td><td>

Table to which the client script applies.

</td></tr><tr><td>

UI Type

</td><td>

Target user interface to which the client script applies.

</td></tr><tr><td>

Type

</td><td>

onLoad\(\) — runs when the system first renders the form and before users can enter data. Typically, onLoad\(\) client scripts perform client-side-manipulation of the current form or set default record values.

 onSubmit\(\) — runs when a form is submitted. Typically, onSubmit\(\) scripts validate things on the form and ensure that the submission makes sense. An onSubmit\(\) client script can cancel form submission by returning a value of false.

 onChange\(\) — runs when a particular field value changes on the form. The onChange\(\) client script must specify these parameters.

-   **control**: the DHTML widget whose value changed.

**Note:** **control** is not accessible in mobile and service portal.

-   **oldValue**: the value the widget had when the record was loaded.

**Note:** Old values aren't returned for the HTML field type.

-   **newValue**: the value the widget has after the change.
-   **isLoading**: identifies whether the change occurs as part of a form load.
-   **isTemplate**: identifies whether the change occurs as part of a template load.

 onCellEdit\(\) — runs when the list editor changes a cell value. The onCellEdit\(\) client script must specify these parameters.

-   **sysIDs**: an array of the sys\_ids for all items being edited.
-   **table**: the table of the items being edited.
-   **oldValues**: the old values of the cells being edited.
-   **newValue**: the new value for the cells being edited.
-   **callback**: a callback that continues the execution of any other related cell edit scripts. If true is passed as a parameter, the other scripts are executed or the change is committed if there are no more scripts. If false is passed as a parameter, any further scripts are not executed and the change is not committed.

</td></tr><tr><td>

Field Name

</td><td>

Name of the field to which the script applies. Available only if the script responds to a field value change \(onChange or onCellEdit script types\).

</td></tr><tr><td>

Application

</td><td>

Application where this client script resides.

</td></tr><tr><td>

Active

</td><td>

Enables the client script when selected. Unselect this field to disable the client script.

</td></tr><tr><td>

Inherited

</td><td>

Indicates whether the client script applies to extended tables.

</td></tr><tr><td>

Global

</td><td>

If true, the client script runs on all views of the table.

</td></tr><tr><td>

View

</td><td>

Only visible when **Global** is unselected. Views on which the client script will run.

</td></tr><tr><td>

Description

</td><td>

Content describing the functionality and purpose of the client script.

</td></tr><tr><td>

Messages

</td><td>

Text string \(one per line\) available to the client script as localized messages using getmessage\('\[message\]'\). For additional information, see [Translate a client script message](https://www.servicenow.com/docs/access?context=t_TranslateAClientScriptMessage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Script

</td><td>

Contains the client script.

</td></tr><tr><td>

Isolate script

</td><td>

New client scripts are run in strict mode, with direct DOM access disabled. Access to jQuery, prototype, and the window object are also disabled. To disable this on a per-script basis, configure this form and select the **Isolate script** check box. To disable this feature for all new globally-scoped client-side scripts set the system property glide.script.block.client.globals to false.

</td></tr></tbody>
</table>**Parent Topic:**[Client-side scripting](client-side-scripting-overview.md)

