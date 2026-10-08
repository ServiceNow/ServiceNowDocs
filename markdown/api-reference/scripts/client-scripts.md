---
title: Client scripts
description: Client scripts allow the system to run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.Create a client script to control form behavior, respond to field changes, validate submissions, or update cell values in a list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/client-scripts.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [client script, create client script]
breadcrumb: [Write client-side scripts, Scripting, API implementation, API implementation and reference]
---

# Client scripts

Client scripts allow the system to run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.

\[Omitted video\] Description: Introduction to client scripts, script types, APIs, and good practices

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

For more information, see [Access Control Lists \(ACLs\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/access-control-rules.md) or [Data policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_DataPolicy.md).

## Where client scripts run

With the exception of onCellEdit\(\) client scripts, client scripts only apply to forms and search pages. If you create a client script to control field values on a form, you must use one of these other methods to control field values when on a list.

-   Create an access control to restrict who can edit field values.
-   Create a business rule to validate content.
-   Create a data policy to validate content.
-   Create an onCellEdit\(\) client script to validate content.
-   Disable list editing for the table.

**Note:** Client scripts are not supported on ServiceNow mobile applications.

**Parent Topic:**[Writing client-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/client-side-scripting-overview.md)

**Related topics**  


[Client API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/api-client.md)

## Create a client script

Create a client script to control form behavior, respond to field changes, validate submissions, or update cell values in a list.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **System Definition** &gt; **Client Scripts**.

2.  Select **New**.

3.  Complete the form.

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

Target user interface to which the client script applies. -   Desktop: The script runs only in the desktop Core UI.
-   Mobile / Service Portal: The script runs only in mobile, portal, or configurable workspace UIs.
-   All: The script runs across all available UIs.
**Note:** Client scripts that run on forms in the Service Portal or mobile environments can only include certain APIs. For more information, see [Client-side scripting for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/r_MobilePlatformMigrationImpacts.md).

</td></tr><tr><td>

Type

</td><td>

onLoad\(\) — runs when the system first renders the form and before users can enter data. Typically, onLoad\(\) client scripts perform client-side manipulation of the current form or set default record values.

 onSubmit\(\) — runs when a form is submitted. Typically, onSubmit\(\) scripts validate form content and confirm that the submission makes sense. An onSubmit\(\) client script can cancel form submission by returning a value of false.

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
-   **callback**: a callback that continues the execution of any other related cell edit scripts. If true is passed as a parameter, the other scripts run or the change is committed if there are no more scripts. If false is passed as a parameter, further scripts are not run and the change is not committed.


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

Enables the client script when selected. Clear this field to disable the client script.

</td></tr><tr><td>

Inherited

</td><td>

Indicates whether the client script applies to extended tables.

</td></tr><tr><td>

Global

</td><td>

When selected, the client script runs on all views of the table.

</td></tr><tr><td>

View

</td><td>

Available only when **Global** is cleared. Views on which the client script runs.

</td></tr><tr><td>

Description

</td><td>

Description of the functionality and purpose of the client script.

</td></tr><tr><td>

Messages

</td><td>

Text string \(one per line\) available to the client script as localized messages using getmessage\('\[message\]'\). For more information, see [Translate a client script message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_TranslateAClientScriptMessage.md).

</td></tr><tr><td>

Script

</td><td>

Contains the client script.

</td></tr><tr><td>

Isolate script

</td><td>

New client scripts run in strict mode, in which direct DOM access is turned off. Access to jQuery, prototype, and the window object are also turned off by default. To enable DOM access on a per-script basis, clear the **Isolate script** check box. To turn off strict mode for all new globally scoped client scripts, set the **glide.script.block.client.globals** system property to false.

</td></tr></tbody>
</table>4.  Select **Submit**.


### Get the value of a variable

Use the following syntax to obtain the value of a catalog variable. Note that the variable must have a name. Replace `variable_name` with the name of the variable.

```javascript
g_form.getValue('variable_name');
```

### Restrict the number of characters a user can type in a variable

This is an example of a script that runs when the variable is displayed, rather than when the item is ordered.

```javascript
function onLoad(){
  var sd = g_form.getControl('short_description');
  sd.maxLength=80;
}
```

