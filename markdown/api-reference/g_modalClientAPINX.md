---
title: g\_modal \(Next Experience\) - Client
description: The g\_modal API enables you to display a modal window to enhance application functionality.Displays an alert message relating to a UI action.Displays a confirm message relating to a UI action.Displays a confirm message related to a UI action, with the confirm button displaying a destructive style.Displays a modal that uses passed HTML to generate the content within the modal.Displays a modal window that contains the specified fields and an OK and Cancel buttons by default.Displays a modal that uses a link to an external URL or UI page for its content.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 18
breadcrumb: [Client Next Experience API reference, API reference, API implementation and reference]
---

# g\_modal \(Next Experience\)- Client

The g\_modal API enables you to display a modal window to enhance application functionality.

Use this API to display modals in workspaces.

Using this API you can:

-   Display input type fields in a modal window.
-   Show something in a frame such as a UI page or external link.
-   Perform an action on user confirmation.
-   Load a component.
-   Use HTML to populate the contents of a modal.

**Parent Topic:**[Client Next Experience API reference](../../../../../build/applications/concept/api-client-next.md)

## g\_modal \(Next Experience\) - alert\(String title, String message, Function callback, style Object\)

Displays an alert message relating to a UI action.

<table id="table_ed2_wwj_xnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

title

</td><td>

String

</td><td id="g_modal-alert-title-entry">

Optional. Title to display in the header of the modal.Default: Alert

</td></tr><tr><td>

message

</td><td>

String

</td><td id="g_modal-message-entry">

Message to display in the modal body. **Note:** If you only pass one parameter, the method treats it as the **message** parameter.

</td></tr><tr><td>

callback

</td><td>

Function

</td><td id="g_modal-callback-entry">

Optional. Function to call after the form has been submitted and processed on the server. The callback function has the form `callbackFunction(String action_verb, String sys_id, String table, String displayValue)` where:

-   **action\_verb**: Name of the UI action executed. Examples:
    -   sysverb\_cancel \(Cancel button\)
    -   sysverb\_insert \(Submit button\)
    -   sysverb\_save \(Save button\)
-   **sys\_id**: Sys\_id of the affected record.
-   **table**: Name of the table containing the record.
-   **displayValue**: Value that appears on the form.

Default: No additional processing

</td></tr><tr><td>

style

</td><td>

Object

</td><td id="g_modal-alert-style-entry">

Optional. Style of the confirmation button to display in the modal.```
"style": {
  "buttonTitle": "String",
  "buttonType": "String"
}
```

</td></tr><tr><td>

style.buttonTitle

</td><td>

String

</td><td id="g_modal-alert-style_buttonTitle-entry">

Optional. Text to display on the confirmation button.Default: OK

</td></tr><tr><td>

style.buttonType

</td><td>

String

</td><td id="g_modal-alert-style_buttonType-entry">

Optional. Type of confirmation button to display.Default: default

</td></tr></tbody>
</table><table id="table_fd2_wwj_xnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Promise

</td><td id="g_modal-promise-entry">

If a **callback** parameter is passed, returns promise if successful, error otherwise.If a **callback** parameter isn't passed, the method always returns success.

</td></tr></tbody>
</table>The following code example shows how to call this method to display an alert message 'Only the assigned to can end this action.'.

```
function onClick(g_form) {

  if (g_user.userID != g_form.getValue('assigned_to')) {
    g_modal.alert('Only the assigned to can end this action.');
    return;
  }

  var msg = getMessage("Are you sure you want to take this action?");
  g_modal.confirm(getMessage("Confirmation"), msg, function (confirmed) {
    if (confirmed) {
      g_form.setValue('state', 'closed_complete');
      g_form.save();
    }
  });

  return false;
}
```

## g\_modal \(Next Experience\) - confirm\(String title, String message, Function callback, style Object\)

Displays a confirm message relating to a UI action.

<table id="table_ed2_wwj_xnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

title

</td><td>

String

</td><td>

Optional. Title to display in the header of the modal.Default: Confirm

</td></tr><tr><td>

message

</td><td>

String

</td><td id="g_modal-message-entry">

Message to display in the modal body. **Note:** If you only pass one parameter, the method treats it as the **message** parameter.

</td></tr><tr><td>

callback

</td><td>

Function

</td><td id="g_modal-callback-entry">

Optional. Function to call after the form has been submitted and processed on the server. The callback function has the form `callbackFunction(String action_verb, String sys_id, String table, String displayValue)` where:

-   **action\_verb**: Name of the UI action executed. Examples:
    -   sysverb\_cancel \(Cancel button\)
    -   sysverb\_insert \(Submit button\)
    -   sysverb\_save \(Save button\)
-   **sys\_id**: Sys\_id of the affected record.
-   **table**: Name of the table containing the record.
-   **displayValue**: Value that appears on the form.

Default: No additional processing

</td></tr><tr><td>

style

</td><td>

Object

</td><td id="g_modal-style-entry">

Optional. Style of the confirm and cancel buttons to display in the modal.```
"style": {
  "cancelTitle": "String",
  "cancelType": "String",
  "confirmTitle": "String",
  "confirmType": "String"
}
```

</td></tr><tr><td>

style.cancelTitle

</td><td>

String

</td><td id="g_modal-style_cancelTitle-entry">

Optional. Text to display on the cancel button.Default: Cancel

</td></tr><tr><td>

style.cancelType

</td><td>

String

</td><td id="g_modal-style_cancelType-entry">

Optional. Type of cancel button to display.Valid values:

-   confirm \(blue background\)
-   default \(white background\)
-   destructive \(red background\)

Default: confirm

</td></tr><tr><td>

style.confirmTitle

</td><td>

String

</td><td id="g_modal-style_confirmTitle-entry">

Optional. Text to display on the confirm button.Default: OK

</td></tr><tr><td>

style.confirmType

</td><td>

String

</td><td id="g_modal-style_confirmType-entry">

Optional. Type of confirm button to display.Valid values:

-   confirm \(blue background\)
-   default \(white background\)
-   destructive \(red background\)

Default: default

</td></tr></tbody>
</table><table id="table_fd2_wwj_xnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Promise

</td><td id="g_modal-promise-entry">

If a **callback** parameter is passed, returns promise if successful, error otherwise.If a **callback** parameter isn't passed, the method always returns success.

</td></tr></tbody>
</table>The following code example shows how to call this method to display the confirmation message "Are you sure you want to take this action?"

```
function onClick(g_form) {

  if (g_user.userID != g_form.getValue('assigned_to')) {
    g_modal.alert('Only the assigned to can end this action.');
    return;
  }

  var msg = getMessage("Are you sure you want to take this action?");
  g_modal.confirm(getMessage("Confirmation"), msg, function (confirmed) {
    if (confirmed) {
      g_form.setValue('state', 'closed_complete');
      g_form.save();
    }
  });

  return false;
}
```

Output:

![Screen shot that shows the confirm modal generated by the code](../../g_modal/image/g_modal_confirm-modal_shot.png)

## g\_modal \(Next Experience\) - confirmDestroy\(String title, String message, Function callback, style Object\)

Displays a confirm message related to a UI action, with the confirm button displaying a destructive style.

<table id="table_ed2_wwj_xnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

title

</td><td>

String

</td><td id="g_modal-confirmDestroy-title-entry">

Optional. Title to display in the header of the modal.Default: Confirm

</td></tr><tr><td>

message

</td><td>

String

</td><td id="g_modal-message-entry">

Message to display in the modal body. **Note:** If you only pass one parameter, the method treats it as the **message** parameter.

</td></tr><tr><td>

callback

</td><td>

Function

</td><td id="g_modal-callback-entry">

Optional. Function to call after the form has been submitted and processed on the server. The callback function has the form `callbackFunction(String action_verb, String sys_id, String table, String displayValue)` where:

-   **action\_verb**: Name of the UI action executed. Examples:
    -   sysverb\_cancel \(Cancel button\)
    -   sysverb\_insert \(Submit button\)
    -   sysverb\_save \(Save button\)
-   **sys\_id**: Sys\_id of the affected record.
-   **table**: Name of the table containing the record.
-   **displayValue**: Value that appears on the form.

Default: No additional processing

</td></tr><tr><td>

style

</td><td>

Object

</td><td id="g_modal-style-entry">

Optional. Style of the confirm and cancel buttons to display in the modal.```
"style": {
  "cancelTitle": "String",
  "cancelType": "String",
  "confirmTitle": "String",
  "confirmType": "String"
}
```

</td></tr><tr><td>

style.cancelTitle

</td><td>

String

</td><td id="g_modal-style_cancelTitle-entry">

Optional. Text to display on the cancel button.Default: Cancel

</td></tr><tr><td>

style.cancelType

</td><td>

String

</td><td id="g_modal-style_cancelType-entry">

Optional. Type of cancel button to display.Valid values:

-   confirm \(blue background\)
-   default \(white background\)
-   destructive \(red background\)

Default: confirm

</td></tr><tr><td>

style.confirmTitle

</td><td>

String

</td><td id="g_modal-style_confirmTitle-entry">

Optional. Text to display on the confirm button.Default: OK

</td></tr><tr><td>

style.confirmType

</td><td>

String

</td><td id="g_modal-confirmDestroy-style_confirmType-entry">

Optional. Type of confirm button to display.Default: destructive

</td></tr></tbody>
</table><table id="table_fd2_wwj_xnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Promise

</td><td id="g_modal-promise-entry">

If a **callback** parameter is passed, returns promise if successful, error otherwise.If a **callback** parameter isn't passed, the method always returns success.

</td></tr></tbody>
</table>This example displays a confirmation modal with a red **Cancel** button and a blue **Confirm** button.

```
function callback(value){ 
  value ? console.log("confirm destroy callback") : console.log('cancel callback'); 
}

function onClick(g_form) {
  g_modal.confirmDestroy("Confirm Destroy Title", "Confirm Destroy Message", callback, {
    cancelTitle: "Cancel",
    cancelType: "destructive",
    confirmTitle: "Confirm",
    confirmType: "confirm"
  })

  .then( 

    function test() {
      g_form.setValue("state', '7");
    }, 

    function fail() {
      g_form.setValue("state", 2)
    } 
  )
}
```

## g\_modal \(Next Experience\) - richText\(String title, String richText, Function callback, String size, String cancelTitle, String confirmTitle, String cancelType, String confirmType, Object resizableConfig\)

Displays a modal that uses passed HTML to generate the content within the modal.

<table id="table_nnj_pgb_h2c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

title

</td><td>

String

</td><td id="g_modal-title-entry">

Optional. Title to display in the header of the modal.Default: blank

</td></tr><tr><td>

richText

</td><td>

String

</td><td id="g_modal-richText-richText-entry">

HTML content to display in the modal.**Note:** This method removes `<script>` tags, inline JavaScript, and other elements that might pose security exploits.

</td></tr><tr><td>

callback

</td><td>

Function

</td><td id="g_modal-callback-entry">

Optional. Function to call after the form has been submitted and processed on the server. The callback function has the form `callbackFunction(String action_verb, String sys_id, String table, String displayValue)` where:

-   **action\_verb**: Name of the UI action executed. Examples:
    -   sysverb\_cancel \(Cancel button\)
    -   sysverb\_insert \(Submit button\)
    -   sysverb\_save \(Save button\)
-   **sys\_id**: Sys\_id of the affected record.
-   **table**: Name of the table containing the record.
-   **displayValue**: Value that appears on the form.

Default: No additional processing

</td></tr><tr><td>

cancelTitle

</td><td>

String

</td><td id="g_modal-richText-cancelTitle-entry">

Optional. Text to display on the cancel button.Default: Cancel

</td></tr><tr><td>

confirmTitle

</td><td>

String

</td><td id="g_modal-richText-confirmTitle-entry">

Optional. Text to display on the confirm button.Default: OK

</td></tr><tr><td>

cancelType

</td><td>

String

</td><td id="g_modal-richText-cancelType-entry">

Optional. Type of cancel button to display.Valid values:

-   confirm \(blue background\)
-   default \(white background\)
-   destructive \(red background\)

Default: confirm

</td></tr><tr><td>

confirmType

</td><td>

String

</td><td id="g_modal-richText-confirmType-entry">

Optional. Type of confirm button to display.Valid values:

-   confirm \(blue background\)
-   default \(white background\)
-   destructive \(red background\)

Default: default

</td></tr><tr><td>

resizableConfig

</td><td>

Object

</td><td id="g_modal-resizableConfig-entry">

Optional. Configuration parameters for resizing the associated modal. If you don't want users to be able to resize the modal, don't pass this parameter.```
resizableConfig:
  {
    enableResizable: Boolean,
    resizableMaxHeight: Number,
    resizableMaxWidth: Number,
    resizableMinHeight: Number,
    resizableMinWidth: Number 
  }
```

Default: Modal is not resizable.

</td></tr><tr><td>

resizableConfig.​enableResizable

</td><td>

Boolean

</td><td id="g_modal-resizableConfig_enableResizable-entry">

Flag that indicates whether users can resize the associated modal.Valid values:

-   true: Modal is resizable. Resize handles appear on the borders of the modal.
-   false: Modal isn't resizable.

Default: false

</td></tr><tr><td>

resizableConfig.​resizableMaxHeight

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMaxHeight-entry">

Maximum resizable height of the modal.Data type: Number

Unit: Pixels

Default: Window's height.

</td></tr><tr><td>

resizableConfig.​resizableMinHeight

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMinHeight-entry">

Minimum resizable height of the modal.Data type: Number

Unit: Pixels

Default: 600px

</td></tr><tr><td>

resizableConfig.​resizableMaxWidth

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMaxWidth-entry">

Maximum resizable width of the modal.Data type: Number

Unit: Pixels

Default: Window's width

</td></tr><tr><td>

resizableConfig.​resizableMinWidth

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMinWidth-entry">

Minimum resizable width of the modal.Data type: Number

Unit: Pixels

Default: 380px

</td></tr></tbody>
</table><table id="table_onj_pgb_h2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Promise

</td><td id="g_modal-promise-entry">

If a **callback** parameter is passed, returns promise if successful, error otherwise.If a **callback** parameter isn't passed, the method always returns success.

</td></tr></tbody>
</table>The following code example shows how to display the text "This is rich text" in bold in the associated modal.

```
function callback(value){
  value ? console.log("confirm richtext callback") : console.log('cancel rich text callback'); 
} 

function onClick(g_form) {
  g_modal.richText("RichTextTitle", "<b>This is rich text</b>", callback, {
    cancelTitle: "Rich Cancel",
    confirmTitle: "Rich Confirm"
  }) 

  .then(
    function test() {
      g_form.setValue("state', '7"); 
    }, 

    function fail() {
      g_form.setValue("state", 2) 
    }
  )
}
```

Output:

![Rich text modal](../../g_modal/image/g_modal_richText-modal_shot.png)

## g\_modal \(Next Experience\) - showFields\(String title, Array fields, Function callback, String size, String cancelTitle, String confirmTitle, String cancelType, String confirmType, Object resizableConfig, String instruction\)

Displays a modal window that contains the specified fields and an **OK** and **Cancel** buttons by default.

<table id="table_ed2_wwj_xnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

title

</td><td>

String

</td><td id="g_modal-showfields-title-entry">

Optional. Title to display in the header of the modal.Default: " "

</td></tr><tr><td>

fields

</td><td>

Array of Objects

</td><td id="g_modal-showfields-fields-entry">

List of fields to display in the modal. Each field is defined in a separate object. The **fields** parameters that you pass are dependent on the type of field \(**fields.type**\) specified.The fields display in the modal in the same order as they appear in the array.

```
fields: [
  {
    autoFocus: Boolean,
    choices: "Array",
    display_value_list: "String",
    enableMentions: Boolean,
    label: "String",
    mandatory: Boolean,
    name: "String",
    referringTable: "String",
    referringRecordId: "String",
    type: "String",
    value: "String"
  }
]
```

</td></tr><tr><td>

fields.​autoFocus

</td><td>

Boolean

</td><td id="g_modal-showfields-fields_autoFocus-entry">

Optional. Flag that indicates whether the field should default to auto focus when the modal loads. Only one field should have this value set to true.Valid values:

-   true: Auto focus.
-   false: Don't auto focus.

Default: false

</td></tr><tr><td>

fields.​choices

</td><td>

Array of Objects

</td><td id="g_modal-showfields-fields_choices-entry">

Required if the **fields.type** parameter is set to `choice`. List of options to display in the associated list field. Each entry in the choice list must be specified as a separate object in the `choices` array.For example:

```
choices: [
  {
    displayValue: "String",
    value: "String
  }
]
```

</td></tr><tr><td>

fields.​choices.​displayValue

</td><td>

String

</td><td id="g_modal-showfields-fields_choices_displayValue-entry">

Optional. Value to display in the list field.Default: Blank

</td></tr><tr><td>

fields.choices.value

</td><td>

String

</td><td id="g_modal-showfields-fields_choices_value-entry">

Optional. Internal value of the value displayed in the list field.Default: Null

</td></tr><tr><td>

fields.​display\_value\_list

</td><td>

Array of Strings

</td><td id="g_modal-showfields-fields_display_value_list-entry">

Optional. List of strings to display. For example, `['item1', 'item2', 'item3']`.

</td></tr><tr><td>

fields.​enableMentions

</td><td>

Boolean

</td><td id="g_modal-showfields-fields_enableMentions-entry">

Required if **fields.type** is `html`. Flag that indicates whether you can mention a user in the modal.Valid values:

-   true: Users can be mentioned in the modal.
-   false: Users can't be mentioned in the modal.

Default: false

</td></tr><tr><td>

fields.label

</td><td>

String

</td><td id="g_modal-showfields-fields_label-entry">

Optional. Text to display as the label for this field in the modal.Default: Blank

</td></tr><tr><td>

fields.​mandatory

</td><td>

Boolean

</td><td id="g_modal-showfields-fields_mandatory-entry">

Optional. Flag that indicates whether the field is mandatory.Valid values:

-   true: Field is mandatory.
-   false: Field is optional.

Default: false

</td></tr><tr><td>

fields.​name

</td><td>

String

</td><td id="g_modal-showfields-fields_name-entry">

Internal name of the field. If the **fields.type** parameter is set to `reference` or `glide_list`, it is the reference field on the current record being used to search.

</td></tr><tr><td>

fields​.referringTable

</td><td>

String

</td><td id="g_modal-showfields-fields_referringTable-entry">

Required if the **fields.type** parameter is set to `reference` or `glide_list`. Name of the table that you are referencing from.For example: `incident`

</td></tr><tr><td>

fields.​referringRecordId

</td><td>

String

</td><td id="g_modal-showfields-fields_referringRecordId-entry">

Required if the **fields.type** parameter is set to `reference`. Sys\_id of the record that you're calling in the UI action form.

</td></tr><tr><td>

fields.type

</td><td>

String

</td><td id="g_modal-showfields-fields_type-entry">

Type of field to display in the modal. Each field type has a set of **fields.&lt;&gt;** elements that can be passed. The values in brackets \[ \] below are the **fields** elements supported by the associated **fields** type.

Valid values:

-   boolean \[autofocus, label, mandatory, name, value\]
-   choice \[autofocus, choices, label, mandatory, name, value\]
-   domain\_id \[label, referringRecordId, referringTable, value\]
-   [glide\_list](https://www.servicenow.com/community/in-other-news/managing-glide-lists/ba-p/2279191) \[autofocus, display\_value\_list, label, name, mandatory, referringRecordId, referringTable, value\]
-   html \[autofocus, enableMentions, label, mandatory, name, referringRecordId, referringTable, value\]
-   reference \[autofocus, label, mandatory, name, reference, referringRecordId, referringTable, value\]
-   string \[autofocus, label, mandatory, name, value\]
-   textarea \[autofocus, label, mandatory, name, value\]

</td></tr><tr><td>

fields.value

</td><td>

String

</td><td id="g_modal-showfields-fields_value-entry">

Optional. Value to display in the field.For example, for a choice field you might display a user prompt:

`value: getMessage(' -- Select -- ')`

Or for a reference field you might display the value of a field on the associated form:

`g_form.getValue('caller_id')`

Default: Blank

</td></tr><tr><td>

callback

</td><td>

Function

</td><td id="g_modal-callback-entry">

Optional. Function to call after the form has been submitted and processed on the server. The callback function has the form `callbackFunction(String action_verb, String sys_id, String table, String displayValue)` where:

-   **action\_verb**: Name of the UI action executed. Examples:
    -   sysverb\_cancel \(Cancel button\)
    -   sysverb\_insert \(Submit button\)
    -   sysverb\_save \(Save button\)
-   **sys\_id**: Sys\_id of the affected record.
-   **table**: Name of the table containing the record.
-   **displayValue**: Value that appears on the form.

Default: No additional processing

</td></tr><tr><td>

size

</td><td>

String

</td><td id="g_modal-size-entry">

Optional. Size of the modal.

Valid values:

-   fw: Full-width
-   sm: 420px by 315px
-   md: 600px by 450px
-   lg: 800px by 600px

**Note:** If a pixel value is specified, the modal takes up the whole browser. For example, passing "1px" makes the modal full-width.

Default: sm

</td></tr><tr><td>

cancelTitle

</td><td>

String

</td><td id="g_modal-showfields-cancelTitle-entry">

Optional. Text to display on the cancel button.Default: Cancel

</td></tr><tr><td>

confirmTitle

</td><td>

String

</td><td id="g_modal-showfields-confirmTitle-entry">

Optional. Text to display on the confirm button.Default: OK

</td></tr><tr><td>

cancelType

</td><td>

String

</td><td id="g_modal-showfields-cancelType-entry">

Optional. Type of cancel button to display.Valid values:

-   confirm \(blue background\)
-   default \(white background\)
-   destructive \(red background\)

Default: confirm

</td></tr><tr><td>

confirmType

</td><td>

String

</td><td id="g_modal-showfields-confirmType-type">

Optional. Type of confirm button to display.Valid values:

-   confirm \(blue background\)
-   default \(white background\)
-   destructive \(red background\)

Default: default

</td></tr><tr><td>

resizableConfig

</td><td>

Object

</td><td id="g_modal-resizableConfig-entry">

Optional. Configuration parameters for resizing the associated modal. If you don't want users to be able to resize the modal, don't pass this parameter.```
resizableConfig:
  {
    enableResizable: Boolean,
    resizableMaxHeight: Number,
    resizableMaxWidth: Number,
    resizableMinHeight: Number,
    resizableMinWidth: Number 
  }
```

Default: Modal is not resizable.

</td></tr><tr><td>

resizableConfig.​enableResizable

</td><td>

Boolean

</td><td id="g_modal-resizableConfig_enableResizable-entry">

Flag that indicates whether users can resize the associated modal.Valid values:

-   true: Modal is resizable. Resize handles appear on the borders of the modal.
-   false: Modal isn't resizable.

Default: false

</td></tr><tr><td>

resizableConfig.​resizableMaxHeight

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMaxHeight-entry">

Maximum resizable height of the modal.Data type: Number

Unit: Pixels

Default: Window's height.

</td></tr><tr><td>

resizableConfig.​resizableMinHeight

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMinHeight-entry">

Minimum resizable height of the modal.Data type: Number

Unit: Pixels

Default: 600px

</td></tr><tr><td>

resizableConfig.​resizableMaxWidth

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMaxWidth-entry">

Maximum resizable width of the modal.Data type: Number

Unit: Pixels

Default: Window's width

</td></tr><tr><td>

resizableConfig.​resizableMinWidth

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMinWidth-entry">

Minimum resizable width of the modal.Data type: Number

Unit: Pixels

Default: 380px

</td></tr><tr><td>

instruction

</td><td>

String

</td><td id="g_modal-showfields-instruction-entry">

Optional. Instructions to display in the modal. This content appears below the modal title and above the first field in the modal.Default: No instructions displayed

</td></tr></tbody>
</table><table id="table_fd2_wwj_xnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Promise

</td><td id="g_modal-promise-entry">

If a **callback** parameter is passed, returns promise if successful, error otherwise.If a **callback** parameter isn't passed, the method always returns success.

</td></tr></tbody>
</table>The following example shows prompting a user for a reason using a modal window, and then passing it back to the work notes field on the record. The then\(\) method returns a promise, which returns what the modal returns; *fieldValues* in this case. The work notes field on the client-side, with the field value, are in the *updatedFields* array. Since only one field is returned, the example assumes an index position of *0*.

```
function onClick(g_form) {
    g_modal.showFields({
        title: "Enter your reason",
        fields: [{
            type: 'textarea',
            name: 'work_notes',
            label: getMessage('Reason'),
            mandatory: true
        }],
        size: 'lg'
    }).then(function(fieldValues) {
        g_form.setValue('work_notes', fieldValues.updatedFields[0].value);
        g_form.save();
    });
}
```

Output:

![Screen shot of modal produced by associated code.](../../g_modal/image/g_modal_showFields-modal_shot2.png)

The following example expands on the example above, adding choice and a reference fields.

```
function onClick(g_form) {

    var fields = [{
        type: 'textarea',
        name: 'work_notes',
        label: getMessage('Reason'),
        mandatory: true
    },
    {
        type: 'choice',
        name: 'reason_code',
        label: getMessage('Reason code'),
        value: getMessage(' -- Select -- '),
        choices: [
          {
            displayValue: 'Duplicate',
            value: 'duplicate'
          },
          {
            displayValue: 'Canceled',
            value: 'canceled'
          }
        ],
        mandatory: true
    },
    {
        type: 'reference',
        name: 'caller_id',
        label: getMessage('What is your name?'),
        mandatory: true,
        reference: 'sys_user',
        referringTable: 'incident',
        referringRecordId: g_form.getUniqueValue(),
	 value: g_form.getValue('caller_id'),
	 displayValue: g_form.getDisplayValue('caller_id')
    }
  ];

  g_modal.showFields({
    title: "Enter your reason",
    fields: fields,
    size: 'lg'
  }).then(function(fieldValues) {
        g_form.setValue('work_notes', fieldValues.updatedFields[0].value);
        g_form.setValue('caller_id', fieldValues.updatedFields[2].value);
        g_form.save();
  });
}
```

Output:

![Screen shot of modal produced by associated code.](../../g_modal/image/g_modal_showFields-modal_shot1.png)

The following example shows how to use this method to display a modal that contains textarea, choices, reference, glide\_list, and domain\_id field types.

```
function onClick(g_form) {
  var fields = [
    {
      type: 'textarea',
      name: 'work_notes',
      label: getMessage('Reason'),
      mandatory: true
    },
    {
      type: 'choice',
      name: 'reason_code',
      label: getMessage('Reason code'),
      value: getMessage(' -- Select -- '),
      choices: [
        {
          displayValue: 'Duplicate',
          value: 'duplicate'
        },
        {
          displayValue: 'Canceled',
          value: 'canceled'
        }
      ],
      mandatory: true
    },
    {
      type: 'reference',
      name: 'caller_id',
      label: getMessage('What is your name?'),
      mandatory: true,
      referringTable: 'incident',
      referringRecordId: g_form.getUniqueValue(),
      value: g_form.getValue('caller_id')
    },
    {
      type: 'glide_list',
      name: 'watch_list',
      label: 'A list', 
      mandatory: false,
      referringTable: 'incident',
      referringRecordId: g_form.getUniqueValue(),
      value: '628,9ee1,f298d',
      display_value_list: ['item1', 'item2', 'item3']
    },
    {
      label: 'Domain ID',
      type: 'domain_id',
      value: 'c90d4b084a362312013398f051272c0d',
      displayValue: 'TOP/ACME',
      referringRecordId: '552c48888c033300964f4932b03eb092',
      referringTable: 'incident'
    }
  ];

  g_modal.showFields({
    title: "Enter your reason",
    fields: fields,
    size: 'lg'
  }).then(function(fieldValues) {

  });
}
```

## g\_modal \(Next Experience\) - showFrame\(String title, String url, Function callback, String size, String height, String modalHeight, String modalWidth, Boolean showClose, String autoCloseOn, Boolean hasLoadingMessage, Boolean closeOnEscape, Boolean hideOverlay, Object resizableConfig\)

Displays a modal that uses a link to an external URL or UI page for its content.

<table id="table_ed2_wwj_xnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

title

</td><td>

String

</td><td id="g_modal-title-entry">

Optional. Title to display in the header of the modal.Default: blank

</td></tr><tr><td>

url

</td><td>

String

</td><td id="g_modal-showFrame-url-entry">

URL of the information to load in the IFrame.**Note:** If only one argument is passed, it is treated as the **url** parameter.

</td></tr><tr><td>

callback

</td><td>

Function

</td><td id="g_modal-callback-entry">

Optional. Function to call after the form has been submitted and processed on the server. The callback function has the form `callbackFunction(String action_verb, String sys_id, String table, String displayValue)` where:

-   **action\_verb**: Name of the UI action executed. Examples:
    -   sysverb\_cancel \(Cancel button\)
    -   sysverb\_insert \(Submit button\)
    -   sysverb\_save \(Save button\)
-   **sys\_id**: Sys\_id of the affected record.
-   **table**: Name of the table containing the record.
-   **displayValue**: Value that appears on the form.

Default: No additional processing

</td></tr><tr><td>

size

</td><td>

String

</td><td id="g_modal-showFrame-size-entry">

Optional. Size of the modal.Valid values:

-   fw: Full-width
-   sm: 420px by 253.25px
-   md: 600px by 253.25px
-   lg: 800px x 254px

Default: lg

</td></tr><tr><td>

height

</td><td>

String

</td><td id="g_modal-showFrame-height-entry">

Optional. Height of the content section in the modal. This value is in the format of "&lt;number&gt;&lt;unit&gt;", such as "80%" or "300px". If you only pass a number, the method assumes the unit of measure is pixels.Valid units of measure:

-   %
-   em
-   px
-   vh

Default: 100% or 153.75px

</td></tr><tr><td>

modalHeight

</td><td>

String

</td><td id="g_modal-showFrame-modalHeight-entry">

Optional. Height of the modal. This value is in the format of "&lt;number&gt;&lt;unit&gt;", such as "80%" or "300px". If you only pass a number, the method assumes the unit of measure is pixels.Valid units of measure:

-   %
-   em
-   px
-   vh

Default: 254px

</td></tr><tr><td>

modalWidth

</td><td>

String

</td><td id="g_modal-showFrame-modalWidth-entry">

Optional. Width of the modal. This value is in the format of "&lt;number&gt;&lt;unit&gt;", such as "80%" or "300px". If you only pass a number, the method assumes the unit of measure is pixels.Valid units of measure:

-   %
-   em
-   px
-   vh

Default: 800px

</td></tr><tr><td>

showClose

</td><td>

Boolean

</td><td id="g_modal-showFrame-showClose-entry">

Optional. Flag that indicates whether the close icon \(X\) appears in the upper-right corner of the modal.Valid values:

-   true: Display the close icon.
-   false: Don't display the close icon.

Default: true

</td></tr><tr><td>

autoCloseOn

</td><td>

String

</td><td id="g_modal-showFrame-autoCloseOn-entry">

Optional. Condition on which to automatically close the modal.Valid values:

-   EMPTY\_BODY
-   URL\_CHANGED

Default: Don't automatically close modal.

</td></tr><tr><td>

hasLoadingMessage

</td><td>

Boolean

</td><td id="g_modal-showFrame-hasLoadingMessage-entry">

Optional. Flag that indicates whether to display the **Loading...** message in the content slot of the modal before loading the modal content. Valid values:

-   true: Display loading message.
-   false: Don't display the loading message. The content slot of the modal is empty before content is loaded.

**Note:** You can't customize the “Loading...” message; only configure whether it displays or not.

Default: false

</td></tr><tr><td>

closeOnEscape

</td><td>

Boolean

</td><td id="g_modal-showFrame-closeOnEscape-entry">

Optional. Flag that indicates whether the user can close the modal by pressing the escape key.Valid values:

-   true: Modal closes when the user presses the escape key.
-   false: Modal doesn't close when the user presses the escape key.

Default: false

</td></tr><tr><td>

hideOverlay

</td><td>

Boolean

</td><td id="g_modal-showFrame-hideOverlay-entry">

Optional. Flag that indicates whether to display the transparent gray overlay over the record page.Valid values:

-   true: Hide the transparent gray overlay over the record page.
-   false: Display the transparent gray overlay over the record page.

Default: false

</td></tr><tr><td>

resizableConfig

</td><td>

Object

</td><td id="g_modal-resizableConfig-entry">

Optional. Configuration parameters for resizing the associated modal. If you don't want users to be able to resize the modal, don't pass this parameter.```
resizableConfig:
  {
    enableResizable: Boolean,
    resizableMaxHeight: Number,
    resizableMaxWidth: Number,
    resizableMinHeight: Number,
    resizableMinWidth: Number 
  }
```

Default: Modal is not resizable.

</td></tr><tr><td>

resizableConfig.​enableResizable

</td><td>

Boolean

</td><td id="g_modal-resizableConfig_enableResizable-entry">

Flag that indicates whether users can resize the associated modal.Valid values:

-   true: Modal is resizable. Resize handles appear on the borders of the modal.
-   false: Modal isn't resizable.

Default: false

</td></tr><tr><td>

resizableConfig.​resizableMaxHeight

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMaxHeight-entry">

Maximum resizable height of the modal.Data type: Number

Unit: Pixels

Default: Window's height.

</td></tr><tr><td>

resizableConfig.​resizableMinHeight

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMinHeight-entry">

Minimum resizable height of the modal.Data type: Number

Unit: Pixels

Default: 600px

</td></tr><tr><td>

resizableConfig.​resizableMaxWidth

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMaxWidth-entry">

Maximum resizable width of the modal.Data type: Number

Unit: Pixels

Default: Window's width

</td></tr><tr><td>

resizableConfig.​resizableMinWidth

</td><td>

Number

</td><td id="g_modal-resizableConfig_resizableMinWidth-entry">

Minimum resizable width of the modal.Data type: Number

Unit: Pixels

Default: 380px

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Promise|Returns promise if successful, error otherwise. This promise is resolved when the IFrame modal is closed.|

The following example shows how to display a KB article in a model using the sys\_id of the KB article record and a base URL.

```
function onClick(g_form) {
  var kbId = '24d9243187032100deddb882a2e3ec33'; //sysId of KB article
  g_modal.showFrame({
    url: '/kb_view.do?sys_kb_id=' + kbId,
    title: 'Test Knowledge Article',
    size: 'lg',
    height: 500px
  });
}
```

Output:

![Screen shot of the modal generated by the code](../../g_modal/image/g_modal_showFrame-modal_shot.png)

This example shows how to use an embedded UI page when creating a modal. It uses window.parent.postMessage\(\) in the UI page to pass data from the iFrame back to the workspace since the g\_form API is not accessible in a UI page when it is in the iFrame.

```
function onClick(g_form) {
  function proposeMIC(data) {
    var workNotes = data.msg + "\n" + data.workNotes;
    var notes = g_form.getValue('work_notes') + ' ' + workNotes;
    var bi = g_form.getValue('business_impact') + ' ' + data.businessImpact;
    g_form.setValue('work_notes', notes.trim());
    g_form.setValue('business_impact', bi.trim());
    g_form.submit('sysverb_mim_propose');
  }
	
  function openPopup() {
    if(!g_form.getControl('work_notes')) {
      getMessage('Cannot propose major incident as "Worknotes" is not visible', function(msg) {
	 g_form.addErrorMessage(msg);
      });
      return false;
    }

    var url = "/sn_major_inc_mgmt_mim_propose.do?sysparm_stack=no&sysparm_workspace=" + true;
    g_modal.showFrame({
      title: getMessage("Propose Major Incident"),
      url: url,
      size: 'lg',
      autoCloseOn: 'URL_CHANGED',
      callback: function (ret, data) {
        if (ret)
          proposeMIC(data);
      }
    });
  }
	
  openPopup();
}
```

Output:

![Screen shot of the modal generated by the code](../../g_modal/image/g_modal_showFrame-modal_shot2.png)

