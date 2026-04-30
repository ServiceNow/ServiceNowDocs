---
title: GlideForm \(g\_form\) - Client
description: The GlideForm API provides methods to customize forms.Adds an icon on a field's label.Adds an icon on a field's label.Displays the specified error message at the top of the form.Displays a floating form message at the top of the form detail section. The message does not cover UI actions.Adds the specified informational message to the top of the form.Adds a choice to the end of a choice list field.Adds a choice to the list field at the position specified.Removes all informational and error messages from the top of the form.Removes all form messages of any type.Removes all form messages of a given type.Removes all options from the choice list.Removes any value\(s\) from the field.Prevents file attachments from being added.Allows file attachments to be added. Shows the paper clip icon.Used to draw attention to a particular field. Flashes the specified color for a specified duration of time in the specified field.Returns the most recent action name, or, for a client script, the sys\_id of the UI action clicked.Returns a Boolean value for the specified field.Returns the HTML element for the specified field.Returns the decimal value of the specified field.Gets the display value from a form in the core UI.Gets the display value from a form in Service Portal.Returns the HTML element specified by the parameter.Returns the HTML element for the form.Returns the HTML element of the help text for the specified field.Returns the integer value of the field.Returns the plain text value of the field label.Returns the option element for a selected box named fieldName where choiceValue matches the option value.Returns the GlideRecord for a specified field.Returns an array of related list names from the current form.Returns all section names, whether visible or not.Returns an array of the form's sections.Returns the name of the table to which this record belongs.Returns the sys\_id of the record displayed in the form.Returns the value of the specified form field.Hides all field messages.Hides all field messages of the specified type.Hides the error message placed by showErrorBox\(\).Hides the first message that appears in the specified field on the current form.Hides the specified related list on the form.Hides all related lists on the form.Returns true while a live update is being done on the record the form is showing.Returns true if the field is mandatory.Returns true if the record has never been saved.Returns true if the section is visible.Determines whether the field associated with the passed-in field name is visible on the current form.Registers a custom event listener that detects when any field in the current form is modified by a user.You can update a list collector variable.Removes the icon from the specified field that matches the icon and title.Removes the icon from the specified field that matches the icon, title, and color.Removes the specified option from the choice list.Saves the record without navigating away \(update and stay\).Makes the specified field mandatory.Shows or hides a section.Sets the value of a specified form field to the value of a specified display value in a reference record.Displays an error message under the specified form field \(either a control object or the name of the field\). If the control or field is currently off the screen and the scrollForm parameter is true, the form scrolls to the control or field.Displays either an informational or error message under the specified form field \(either a control object or the name of the field\). If the control or field is off the screen, the form is scrolled to the field.Displays either an informational or error message under the specified form field \(either a control object or the name of the field\). If the control or field is currently off the screen and scrollForm is true, the form is scrolled to the field.Makes the specified field available or unavailable.Displays or hides a field.Sets the plain text value of the field label.Makes the specified field read-only or editable.Sets the value of a specified form field to the passed in value.Makes a Service Catalog variable editor read only.Displays or hides the field.Displays an error message under the specified form field \(either a control object or the name of the field\). If the control or field is currently off the screen, the form scrolls to the control or field.Displays the specified related list on the form.Displays all the form's related lists.Saves the record.Performs the UI action specified by the parameter.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 34
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideForm \(g\_form\) - Client

The GlideForm API provides methods to customize forms.

GlideForm.js is the JavaScript class containing the methods. Only use GlideForm methods on the client. You can use these methods to make custom changes to the form view of records. All validation of examples was done using client scripts.

You can also use some of these methods in other client scripts \(such as Catalog Client Scripts or Wizard Client Scripts\), but you must first test this to determine whether they will work as expected.

**Note:** The methods getControl\(\), getHelpTextControl\(\), getElement\(\), and getFormElement\(\) are deprecated for mobile devices. For information on using GlideForm for mobile, see [Mobile Client GlideForm \(g\_form\) Scripting and Migration](../../../../../script/client-scripts/reference/r_MobilePlatformMigrationImpacts.md).

There is no constructor for the GlideForm class. Access GlideForm methods using the `g_form` global object.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideForm - addDecoration\(String fieldName, String icon, String title\)

Adds an icon on a field's label.

Adding the same item twice is prevented; however, you can add the same icon with a different title.

**Note:** This method is not supported by Service Catalog.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|
|icon|String|The font icon to show next to the field. Supported icons - icon-user, icon-user-group, icon-lightbulb, icon-home, icon-mobile, icon-comment, icon-mail, icon-locked, icon-database, icon-book, icon-drawer, icon-folder, icon-catalog, icon-tab, icon-cards, icon-tree-right, icon-tree, icon-book-open, icon-paperclip, icon-edit, icon-trash, icon-image, icon-search, icon-power, icon-cog, icon-star, icon-star-empty, icon-new-ticket, icon-dashboard, icon-cart-full, icon-view, icon-label, icon-filter, icon-calendar, icon-script, icon-add, icon-delete, icon-help, icon-info, icon-check-circle, icon-alert, icon-sort-ascending, icon-console, icon-list, icon-form, and icon-livefeed.|
|title|String|The text title for the icon.|

|Type|Description|
|----|-----------|
|void| |

```
g_form.addDecoration('caller_id', 'icon-star', 'preferred member');
```

## GlideForm - addDecoration\(String fieldName, String icon, String title, String color\)

Adds an icon on a field's label.

Adding the same item twice is prevented; however, you can add the same icon with a different title.

**Note:** This method is not supported by Service Catalog.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|
|icon|String|The font icon to show next to the field. Supported icons - icon-user, icon-user-group, icon-lightbulb, icon-home, icon-mobile, icon-comment, icon-mail, icon-locked, icon-database, icon-book, icon-drawer, icon-folder, icon-catalog, icon-tab, icon-cards, icon-tree-right, icon-tree, icon-book-open, icon-paperclip, icon-edit, icon-trash, icon-image, icon-search, icon-power, icon-cog, icon-star, icon-star-empty, icon-new-ticket, icon-dashboard, icon-cart-full, icon-view, icon-label, icon-filter, icon-calendar, icon-script, icon-add, icon-delete, icon-help, icon-info, icon-check-circle, icon-alert, icon-sort-ascending, icon-console, icon-list, icon-form, and icon-livefeed.|
|title|String|The text title for the icon.|
|color|String|A CSS color.|

|Type|Description|
|----|-----------|
|void| |

```
g_form.addDecoration('caller_id', 'icon-star', 'Mark as Favorite', 'color-green');
```

## GlideForm - addErrorMessage\(String message\)

Displays the specified error message at the top of the form.

This message appears for approximately four seconds and then disappears. This timeout is not configurable at this time.

|Name|Type|Description|
|----|----|-----------|
|message|String|Message to display.|

|Type|Description|
|----|-----------|
|void| |

```
g_form.addErrorMessage('This is an error');
```

## GlideForm - addFormMessage\(String message, String type, Object options\)

Displays a floating form message at the top of the form detail section. The message does not cover UI actions.

See also:

-   [clearAllFormMessages\(\)](c_GlideFormAPI.md#)
-   [clearFormMessages\(\)](c_GlideFormAPI.md#)

<table id="table_f2v_zym_4pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

String

</td><td>

Message to display.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

The type of message.Valid values:

-   error
-   info
-   warning

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional. Object containing buttons to add to the form message and any metadata needed to handle a button click.```
{
  buttons: [Array],
  meta: {Object}
}
```

</td></tr><tr><td>

options.buttons

</td><td>

Array

</td><td>

Array of buttons to add to the form message.```
buttons: [
  {
    label: "String", 
    actionName: "String"
  }
]
```

</td></tr><tr><td>

options.buttons.label

</td><td>

String

</td><td>

Text to display on the button.

</td></tr><tr><td>

options.buttons.actionName

</td><td>

String

</td><td>

Name used by FORM\_MESSAGE\_BUTTON\_CLICKED event handlers to determine the button that was clicked.For example, if you add a button with the actionName `assign_to_me`, you must create an event handler in UIB on the FORM\_MESSAGE\_BUTTON\_CLICKED event that only executes when the actionName is `assigned_to_me`.

</td></tr><tr><td>

options.meta

</td><td>

Object

</td><td>

Map of any metadata needed to handle the button click formatted as key-value pairs. ```
meta: {
  'key': 'value'
}
```

For example, for an **Assign to me** button the event handler needs the sys\_id of the user to assign the record to.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to add form messages of each type.

```
g_form.addFormMessage('info message','info');
g_form.addFormMessage('warning message','warning');
g_form.addFormMessage('error message','error');
g_form.addFormMessage('info2 message','info');
g_form.addFormMessage('warning2 message','warning');
g_form.addFormMessage('error2 message','error');
g_form.addFormMessage('Would you like to reassign this to yourself?', 'info', {buttons: [{label: "Assign to me", actionName: "assign_to_me"}], meta: {'userId': '46d44a23a9fe19810012d100cca80666'}});
```

## GlideForm - addInfoMessage\(String message\)

Adds the specified informational message to the top of the form.

This message appears for approximately four seconds and then disappears. This timeout is not configurable at this time.

|Name|Type|Description|
|----|----|-----------|
|message|String|Message to display.|

|Type|Description|
|----|-----------|
|void| |

```
g_form.addInfoMessage('The top five fields in this form are mandatory');
```

## GlideForm - addOption\(String fieldName, String choiceValue, String choiceLabel\)

Adds a choice to the end of a choice list field.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The name of the field.|
|choiceValue|String|The value to be stored in the database.|
|choiceLabel|String|The value displayed.|

|Type|Description|
|----|-----------|
|void| |

```
g_form.addOption('priority', '6', '6 - Really Low');
```

## GlideForm - addOption\(String fieldName, String choiceValue, String choiceLabel, Number choiceIndex\)

Adds a choice to the list field at the position specified.

**Note:** Duplicate list labels are not supported in Service Portal. For example, items with label text matching another label are ignored and not added to the list.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|
|choiceValue|String|The value stored in the database.|
|choiceLabel|String|The value displayed.|
|choiceIndex|Number|Order of the choice in the list. The index is into a zero based array.|

|Type|Description|
|----|-----------|
|void| |

```
g_form.addOption('priority', '2.5', '2.5 - Moderately High', 3);
```

## GlideForm - clearMessages\(\)

Removes all informational and error messages from the top of the form.

Removes informational and error messages added with g\_form.addInfoMessage\(\) and g\_form.addErrorMessage\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
g_form.clearMessages();
```

## GlideForm - clearAllFormMessages\(\)

Removes all form messages of any type.

See also:

-   [addFormMessage\(\)](c_GlideFormAPI.md#)
-   [clearFormMessages\(\)](c_GlideFormAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to clear all messages from the form.

```
g_form.clearAllFormMessages();
```

## GlideForm - clearFormMessages\(String type\)

Removes all form messages of a given type.

See also:

-   [addFormMessage\(\)](c_GlideFormAPI.md#)
-   [clearAllFormMessages\(\)](c_GlideFormAPI.md#)

<table id="table_ilw_bzm_4pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

type

</td><td>

String

</td><td>

The type of message.Valid values:

-   error
-   info
-   warning

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to clear all error messages from the form.

```
g_form.clearFormMessages('error');
```

## GlideForm - clearOptions\(String fieldName\)

Removes all options from the choice list.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|

|Type|Description|
|----|-----------|
|void| |

## GlideForm - clearValue\(String fieldName\)

Removes any value\(s\) from the field.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|

|Type|Description|
|----|-----------|
|void| |

## GlideForm - disableAttachments\(\)

Prevents file attachments from being added.

This method is not available on the mobile platform. If this method is run on a mobile platform, no action occurs.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## GlideForm - enableAttachments\(\)

Allows file attachments to be added. Shows the paper clip icon.

This method is not available on the mobile platform. If this method is run on a mobile platform, no action occurs.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## GlideForm - flash\(String fieldName, String color, Number count\)

Used to draw attention to a particular field. Flashes the specified color for a specified duration of time in the specified field.

This method is not supported by Service Catalog.

This method is not available on the mobile platform. If this method is run on a mobile platform, no action occurs.

<table id="table_htn_w2w_ts" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldName

</td><td>

String

</td><td>

Specifies the field to highlight in the following format: `"<table-name>.<field-name>"`.

</td></tr><tr><td>

color

</td><td>

String

</td><td>

RGB color or acceptable CSS color.

</td></tr><tr><td>

count

</td><td>

Number

</td><td>

Specifies how long the label will flash. Options include:-   2: Flashes for 1 second
-   0: Flashes for 2 seconds
-   -2: Flashes for 3 seconds
-   -4: Flashes for 4 seconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
g_form.flash("incident.number", "#FFFACD", 0);
```

## GlideForm - getActionName\(\)

Returns the most recent action name, or, for a client script, the sys\_id of the UI action clicked.

**Note:** Not available in Wizard client scripts.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The current action name.|

```
function onSubmit() {
   var action = g_form.getActionName();
   alert('You pressed ' + action);
}
```

## GlideForm - getBooleanValue\(String fieldName\)

Returns a Boolean value for the specified field.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|

|Type|Description|
|----|-----------|
|Boolean|Returns false if the field value is false or undefined; otherwise returns true.|

## GlideForm - getControl\(String fieldName\)

Returns the HTML element for the specified field.

Compound fields may contain several HTML elements. This method is generally not necessary as there are built-in methods that use the fields on a form.

If the field is a reference field and the control is a choice list, getControl\(\) may not return a control as expected. In this case, use `sys_select.<table name>.<field name>`.

This method is not available in mobile scripts or Service Portal scripts.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|

|Type|Description|
|----|-----------|
|HTMLElement|The field's HTML element.|

## GlideForm - getDecimalValue\(String fieldName\)

Returns the decimal value of the specified field.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The name of the field.|

|Type|Description|
|----|-----------|
|String|The decimal value of the specified field.|

```
function onChange(control, oldValue, newValue, isLoading) {
   alert(g_form.getDecimalValue('percent_complete'));
}
```

## GlideForm - getDisplayBox\(String fieldName\)

Gets the display value from a form in the core UI.

**Note:** To get a display value from a form in Service Portal, use the [getDisplayValue\(\)](c_GlideFormAPI.md#) method.

See also:

-   [getValue\(\)](c_GlideFormAPI.md#)
-   [Get the display value of a reference variable](https://www.servicenow.com/community/developer-blog/get-display-value-of-reference-variable-service-catalog/ba-p/2287763)

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field from which you want to retrieve a value in the form.|

|Type|Description|
|----|-----------|
|None| |

```
var caller = g_form.getDisplayBox('caller_id').value;

var assignee = g_form.getDisplayBox('assigned_to').value;

if (caller == assignee)
{
   alert('in');
}
```

## GlideForm - getDisplayValue\(String fieldName\)

Gets the display value from a form in Service Portal.

**Note:** To get a display value from a form in the core UI, use the [getDisplayBox\(\)](c_GlideFormAPI.md#) method.

See also:

-   [getValue\(\)](c_GlideFormAPI.md#)
-   [Get the display value of a reference variable](https://www.servicenow.com/community/developer-blog/get-display-value-of-reference-variable-service-catalog/ba-p/2287763)

**Note:** In the core UI, calling this method as `g_form.getDisplayValue()` without an argument returns the record display value rather than the display value of an individual field.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field from which you want to retrieve a value in the form.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to get the display value of a reference variable in the core UI or Service Portal. The use case for this example is on the [community](https://www.servicenow.com/community/developer-blog/get-display-value-of-reference-variable-service-catalog/ba-p/2287763) site.

```
function onChange(control, oldValue, newValue, isLoading) {
     if (isLoading || newValue == '') {
          return;
     }
     if(window == null){
          var valuePortal = g_form.getDisplayValue('requester');
          alert('Portal->' + valuePortal);
     }
     else{
          var valueNative = g_form.getDisplayBox('requester').value;     
          alert('CoreUI->' + valueCoreUI);
     }
     //Type appropriate comment here, and begin script below
}
```

## GlideForm - getElement\(String id\)

Returns the HTML element specified by the parameter.

Compound fields may contain several HTML elements. This method is generally not necessary as there are built-in methods that use the fields on a form.

This method is not available in mobile scripts or Service Portal scripts.

|Name|Type|Description|
|----|----|-----------|
|id|String|The field id.|

|Type|Description|
|----|-----------|
|HTMLElement|The field's HTML element.|

## GlideForm - getFormElement\(\)

Returns the HTML element for the form.

This method is not available in mobile scripts or Service Portal scripts.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|HTMLFormElement|The HTML element for the form.|

## GlideForm - getHelpTextControl\(String fieldName\)

Returns the HTML element of the help text for the specified field.

This method is applicable to service catalog variables only.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|

|Type|Description|
|----|-----------|
|HTMLElement|Help text field's HTML element.|

## GlideForm - getIntValue\(String fieldName\)

Returns the integer value of the field.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|

|Type|Description|
|----|-----------|
|Number|Integer value of the field.|

## GlideForm - getLabelOf\(String fieldName\)

Returns the plain text value of the field label.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name|

|Type|Description|
|----|-----------|
|String|The label text.|

```
if (g_user.hasRole('itil')) {
    var oldLabel = g_form.getLabelOf('comments');
    g_form.setLabelOf('comments', oldLabel + ' (Customer visible)');
}
```

## GlideForm - getOption\(String fieldName, String choiceValue\)

Returns the option element for a selected box named **fieldName** where **choiceValue** matches the option value.

**Note:** This method does not work on read-only fields.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|
|choiceValue|String|Value of the option.|

|Type|Description|
|----|-----------|
|HTMLElement|The HTMLElement for the option. Returns null if the field or option is not found.|

The following example shows how to get the label for a choice list value.

```
// Get the label for a choice list value
// fieldName is 'category'
 
function onChange(control, oldValue, newValue, isLoading) {
var choiceValue = g_form.getValue('category');
var choiceLabel = g_form.getOption('category', choiceValue).text; 
}
```

## GlideForm - getReference\(String fieldName, Function callBack\)

Returns the GlideRecord for a specified field.

If a callback function is present, this routine runs asynchronously. The browser \(and script\) processing continues normally until the server returns the reference value, at which time, the callback function is invoked. If a callback function is not present, this routine runs synchronously and processing halts \(causing the browser to appear to hang\) while waiting on a server response.

**Important:** It is strongly recommended that you use a callback function.

Callback function support for ServiceCatalogForm.getReference is available.

**Note:** Using this method requires a call to the server which requires additional time and may introduce latency to your page. Use this method with caution. For additional information, see [Client script design and processing](../../../../../script/client-scripts/concept/client-script-best-practices.md#).

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|
|callBack|Function|Name of the call back function.|

<table id="table_l4c_1yb_5s" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GlideRecord

</td><td>

GlideRecord object for the specified field. If the specified reference cannot be found, it returns an initialized GlideRecord object where currentRow = -1 and rows.length = 0.

</td></tr></tbody>
</table>```
function onChange(control, oldValue, newValue, isLoading) {
    g_form.getReference('caller_id', doAlert); // doAlert is our callback function
}
 
function doAlert(caller) { // reference is passed into callback as first arguments
   if (caller.getValue('vip') == 'true') {
      alert('Caller is a VIP!');
   }
}
```

## GlideForm - getRelatedListNames\(\)

Returns an array of related list names from the current form.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|String array of related list names from the current form. The related list names are listed in the order in which they appear on the form.|

```
var listNames = g_form.getRelatedListNames();

for (var i = 0; i < listNames.length; i++) {  
  this.showRelatedList(listNames[i]);
 }
```

## GlideForm - getSectionNames\(\)

Returns all section names, whether visible or not.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array of strings|The section names.|

## GlideForm - getSections\(\)

Returns an array of the form's sections.

This method is not available on the mobile platform. If this method is run on a mobile platform, no action occurs.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array of HTML elements|The form's sections.|

```
function onChange(control, oldValue, newValue, isLoading) {
   //this example was run on a form divided into sections (Change form)
   // and hid a section when the "state" field was changed
   var sections = g_form.getSections();
   if (newValue == '2') {
      g_form.setSectionDisplay(sections[1], false);
   } else {
      g_form.setSectionDisplay(sections[1], true);
   }
}
```

## GlideForm - getTableName\(\)

Returns the name of the table to which this record belongs.

On the server side, the table for the current record can be retrieved with current.sys\_class\_name or current.getTableName\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the table.|

```
function onLoad() {
    if (g_form.isNewRecord()) {
        var tableName = g_form.getTableName(); //Get the table name
    }
}
```

## GlideForm - getUniqueValue\(\)

Returns the sys\_id of the record displayed in the form.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The record's sys\_id.|

```
function onLoad() {
   var incSysid = g_form.getUniqueValue();
   alert(incSysid);
}
```

## GlideForm - getValue\(String fieldName\)

Returns the value of the specified form field.

This method also supports getting values from a multi-row variable set \(MRVS\). To obtain data from fields within an MRVS, you must first use `JSON.parse(getValue('<mrvs_field_name>') || '[]')` to obtain the MRVS array, and then use indexing to access the fields within the row objects. For more details, see the code example below.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field whose value to return.|

|Type|Description|
|----|-----------|
|String|Value of the specified field.|

The following example shows how to get the short description from the current form.

```
function onChange(control, oldValue, newValue, isLoading) {
   alert(g_form.getValue('short_description'));
}
```

The following example shows how to get values from an MRVS. In this example, salaries are being managed through the Service Catalog. The client script searches all rows within the MRVS for the value entered in the **Job title** and then updates the matching entries within the MRVS with what is entered in the **Salary** field. The MRVS is named "variable\_set\_1" and contains the following fields within each row object: Employee name \[employee\_name\], Job title \[employee\_job\_title\], and Salary \[employee\_salary\]. In addition, the Catalog Item contains: Job title \[job\_title\] and Salary \[salary\].

```
function onChange(control, oldValue, newValue, isLoading) {
if (isLoading || newValue == '') {
return;
}
 
// Get the MRVS
var vs1 = g_form.getValue('variable_set_1') || '[]';
var multiRowVariableSet = JSON.parse(vs1);
 
for (var i = 0; i < multiRowVariableSet.length; i++) {
// Check if the entered job title matches the title in the current MRVS row
  if (multiRowVariableSet[i].employee_job_title == g_form.getValue("job_title")){
    // Update the value of a matching field with the new salary
    multiRowVariableSet[i].employee_salary = newValue;
  }
}
 
// Update the MRVS
g_form.setValue('variable_set_1', JSON.stringify(multiRowVariableSet));
}
```

## GlideForm - hideAllFieldMsgs\(\)

Hides all field messages.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## GlideForm - hideAllFieldMsgs\(String type\)

Hides all field messages of the specified type.

<table id="table_y2c_qhw_ts" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

type

</td><td>

String

</td><td>

The type of message.Valid values:

-   error
-   info

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## GlideForm - hideErrorBox\(String fieldName\)

Hides the error message placed by showErrorBox\(\).

Whenever possible, use hideFieldMsg\(\) rather than this method whenever possible.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The name of the field or control.|

|Type|Description|
|----|-----------|
|void| |

## GlideForm - hideFieldMsg\(String fieldName, Boolean clearAll\)

Hides the first message that appears in the specified field on the current form.

Use the [GlideForm - showFieldMsg\(String field, String message, String type\)](c_GlideFormAPI.md#) or [GlideForm - showFieldMsg\(String field, String message, String type, Boolean scrollForm\)](c_GlideFormAPI.md#) methods to display messages on a form.

For example, the following code snippet shows how to display two messages on the `work_notes` field of a form and then hide the first message:

```
g_form.showFieldMsg('work_notes', 'First message', "error");
g_form.showFieldMsg('work_notes', 'Second message', "error");
g_form.hideFieldMsg('work_notes', false); // This call hides the 'First message'
```

<table id="table_xnf_3pw_ts" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldName

</td><td>

String

</td><td>

Name of the field on which to hide the message.

</td></tr><tr><td>

clearAll

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to hide all messages for the specified field.Valid values:

-   true: Hide all messages.
-   false: Only hide the first message being displayed.

Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following example shows how to clear all messages for a specified form field and then display an encryption error message.

```
function submitEncryptedInputs() {
  return processEncryptedInputs(function(inputName, fieldName) {
    if (!checkEncryptedFieldValue(fieldName)) {
      g_form.hideFieldMsg(fieldName, true); // Hide all messages for the specified field
      g_form.showFieldMsg(fieldName, "Your activity requires an encrypted input.", "error");
      return false;
    }
    return true;
  });
}
```

## GlideForm - hideRelatedList\(String listTableName\)

Hides the specified related list on the form.

This method is not available on the mobile platform. If this method is run on a mobile platform, no action occurs.

|Name|Type|Description|
|----|----|-----------|
|listTableName|String|Name of the related list. Use the sys\_id to hide a list through a relationship.|

|Type|Description|
|----|-----------|
|void| |

## GlideForm - hideRelatedLists\(\)

Hides all related lists on the form.

This method is not available on the mobile platform. If this method is run on a mobile platform, no action occurs.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## GlideForm - isLiveUpdating\(\)

Returns true while a live update is being done on the record the form is showing.

This can be used in an onChange\(\) client script to determine if a change to the record is because of a live update from another session. The client script can then decide what action to take, or not to take. This applies to systems using Core UI with live forms enabled.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if a live update is happening on the record displayed by the form.|

## GlideForm - isMandatory\(String fieldName\)

Returns true if the field is mandatory.

Mandatory fields are visually distinguished by an asterisk next to the field label. The asterisk is red if the field is empty, and black if the field is not empty. The system displays a validation message if a user attempts to save or submit the form without completing those fields. For more information, see [Form fields](https://www.servicenow.com/docs/access?context=c_FormFields&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|

|Type|Description|
|----|-----------|
|Boolean|True if the field is required, false otherwise.|

## GlideForm - isNewRecord\(\)

Returns true if the record has never been saved.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if the record has not been saved; otherwise false.|

```
function onLoad() {
   if(g_form.isNewRecord()){
      alert('New Record!');
   }
}
```

## GlideForm - isSectionVisible\(String sectionName\)

Returns true if the section is visible.

**Important:** The isSectionVisible\(\) function is not supported in Workspace.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true when the section is visible; otherwise, false is returned.|

## GlideForm - isVisible\(String fieldName\)

Determines whether the field associated with the passed-in field name is visible on the current form.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field to check whether it is visible on the current form.|

<table id="table_qs3_gqy_m2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified field is visible on the current form.Valid values:

-   true: Field is visible on the form.
-   false: Field isn't visible on the form.

</td></tr></tbody>
</table>The following code example shows how to check if the `user_address` field is visible on the current form.

```
if(g_form.isVisible('user_address')) {
    alert('is visible');
}
else {
    alert('is hidden');
}
```

## GlideForm - onUserChangeValue\(Function fn\)

Registers a custom event listener that detects when any field in the current form is modified by a user.

When a form field is modified, the event listener calls the function that is passed in when the listener is initially registered. This listener is only triggered when a user makes a change to a field on the form. Changes from client scripts, UI policies, or any other non-user interactions, do not trigger the listener.

**Note:** This method does not work for journal fields or Service Catalog items in the classic environment.

<table id="table_m5y_wll_1hb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fn

</td><td>

Function

</td><td>

Function to call when a user changes the value of a field within the current form. This is actually the function code, not just the function name. This function must accept the following three arguments:

 -   field name
-   original field value
-   updated field value

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Function|Function to call to unregister the onUserChangeValue event listener.|

```
var handler = function(fieldname, originalValue, newValue) {
  console.log('The field ('+ fieldname + ') has a new value of: ' + newValue); // function code
}
 
var unregister = g_form.onUserChangeValue(handler);
 
// To unregister the event listener
unregister();
```

## GlideForm - refreshSlushbucket\(String fieldName\)

You can update a list collector variable.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the slush bucket.|

|Type|Description|
|----|-----------|
|void| |

```
g_form.refreshSlushbucket('bucket');
```

## GlideForm - removeDecoration\(String fieldname, String icon, String title\)

Removes the icon from the specified field that matches the icon and title.

**Note:** This method is not supported by Service Catalog.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Field name.|
|icon|String|Name of the icon to remove.|
|title|String|The icon's text title \(name\).|

|Type|Description|
|----|-----------|
|void| |

```
function onChange(control, oldValue, newValue, isLoading) {
	// if the caller_id field is not present, then we can't add an icon anywhere
	if (!g_form.hasField('caller_id'))
		return;
 
	if (!newValue)
		return;
 
	g_form.getReference('caller_id', function(ref) {
		g_form.removeDecoration('caller_id', 'icon-star', 'VIP');
 
		if (ref.getValue('vip') == 'true')
			g_form.addDecoration('caller_id', 'icon-star', 'VIP');			
	});
}
```

## GlideForm - removeDecoration\(String fieldname, String icon, String title, String color\)

Removes the icon from the specified field that matches the icon, title, and color.

**Note:** This method is not supported by Service Catalog.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Field name.|
|icon|String|Name of the icon to remove.|
|title|String|The icon's text title \(name\).|
|color|String|A CSS color|

|Type|Description|
|----|-----------|
|void| |

```
g_form.removeDecoration('caller_id', 'icon-star', 'VIP', 'blue');
```

## GlideForm - removeOption\(String fieldName, String choiceValue\)

Removes the specified option from the choice list.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|
|choiceValue|String|The value stored in the database. This is not the label.|

|Type|Description|
|----|-----------|
|void| |

```
g_form.removeOption('priority', '1');
```

## GlideForm - save\(\)

Saves the record without navigating away \(update and stay\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## GlideForm - setMandatory\(String fieldName, Boolean mandatory\)

Makes the specified field mandatory.

Mandatory fields are visually distinguished by an asterisk next to the field label. The asterisk is red if the field is empty, and black if the field is not empty. The system displays a validation message if a user attempts to save or submit the form without completing those fields. For more information, see [Form fields](https://www.servicenow.com/docs/access?context=c_FormFields&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

**Note:** Whenever possible, use a UI policy rather than this method.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|
|mandatory|Boolean|When true makes the field mandatory. When false makes the field optional.|

|Type|Description|
|----|-----------|
|void| |

## GlideForm - setSectionDisplay\(String sectionName, Boolean display\)

Shows or hides a section.

|Name|Type|Description|
|----|----|-----------|
|sectionName|String|The section name is lower case with an underscore replacing the first space in the name, and with the remaining spaces being removed, for example "Section Four is Here" becomes "section\_fourishere". Other non-alphanumeric characters, such as ampersand \(&amp;\), are removed. Section names can be found by using the getSectionNames\(\) method.|
|display|Boolean|When true shows the section. When false hides the section.|

|Type|Description|
|----|-----------|
|Boolean|Returns true when successful.|

## GlideForm - setValue\(String fieldName, String value, String displayValue\)

Sets the value of a specified form field to the value of a specified display value in a reference record.

To improve performance by preventing a round trip when setting the value for a reference field, use this method, not setValue\(fieldName, value\). When setting multiple reference values for a list collector field, pass arrays in the **value** and **displayValue** parameters.

**Note:** The method setValue\(\) can cause a stack overflow when used in an OnChange client script. This is because every time the value is set, it will register as a change, which may re-trigger the OnChange client script. To prevent this, perform a check that will validate that the new value will be different from the old value. For example, before performing `setValue(shortDesc, newValue.toUpperCase());`, validate that the short description is not already uppercase. This will prevent the client script from applying the toUpperCase\(\) more than once.

<table id="table_oxn_vrc_5s" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldName

</td><td>

String

</td><td>

Name of the form field to update.

</td></tr><tr><td>

value

</td><td>

String or Array

</td><td>

Sys\_id of the reference record to use to update the field.If the specified field is a GlideList, this parameter can contain an array of sys\_ids. In this case, the method performs a lookup of all records specified in the array and those values are used to update the contents of the specified field \(related list\).

**Note:** When defining a value in a choice list, be sure to use number value rather than the label.

</td></tr><tr><td>

displayValue

</td><td>

String or Array

</td><td>

Field within the specified reference record to use to update the specified field. For example, in the User \[sys\_user\] table it might be userName.If the specified field is a GlideList, this parameter can contain an array of display value names.

For additional information on display values, see [Display value](https://www.servicenow.com/docs/access?context=c_DisplayValues&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows passing the sys\_id of the reference record that contains the userName field to use to update the **assigned\_to** form field.

```
g_form.setValue('assigned_to', userSysID, userName);
```

This example shows passing an array of reference record sys\_ids and an array of corresponding display value names to use to update the form fields in the GlideList **glide-list\_field\_name**.

```
g_form.setValue('glide-list_field_name', sysIDArray, displayNameArray);
```

## GlideForm - showErrorBox\(String name, String message, Boolean scrollForm\)

Displays an error message under the specified form field \(either a control object or the name of the field\). If the control or field is currently off the screen and the scrollForm parameter is true, the form scrolls to the control or field.

A global property \(glide.ui.scroll\_to\_message\_field\) is available that controls automatic message scrolling when the form field is off screen \(scrolls the form to the control or field\). The showFieldMsg\(\) method is a similar method that requires a type parameter.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the field or control.|
|message|String|Message to display.|
|scrollForm|Boolean|When true scrolls the form to the field. When false the form does not scroll to the field.|

|Type|Description|
|----|-----------|
|void| |

## GlideForm - showFieldMsg\(String field, String message, String type\)

Displays either an informational or error message under the specified form field \(either a control object or the name of the field\). If the control or field is off the screen, the form is scrolled to the field.

A global property \(glide.ui.scroll\_to\_message\_field\) is available that controls automatic message scrolling when the form field is off screen \(scrolls the form to the control or field\).

The showErrorBox\(\) method is a shorthand method that does not require the type parameter.

**Note:** This method does not work with the **journal\_field** type field in Core UI.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field or control.|
|message|String|Message to display.|
|type|String|"error","info", or "warning".|

|Type|Description|
|----|-----------|
|void| |

```
g_form.showFieldMsg('impact','Low impact response time can be one week','info');
```

## GlideForm - showFieldMsg\(String field, String message, String type, Boolean scrollForm\)

Displays either an informational or error message under the specified form field \(either a control object or the name of the field\). If the control or field is currently off the screen and scrollForm is true, the form is scrolled to the field.

A global property \(glide.ui.scroll\_to\_message\_field\) is available that controls automatic message scrolling when the form field is off screen \(scrolls the form to the control or field\).

The showErrorBox\(\) method is a shorthand method that does not require the type parameter.

**Note:** This method does not work with the **journal\_field** type field in Core UI.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the field or control.|
|message|String|Message to display.|
|type|String|"error","info", or "warning".|
|scrollForm|Boolean|When true, the form scrolls to the field if it is off screen. When false, the form does not scroll.|

|Type|Description|
|----|-----------|
|void| |

```
g_form.showFieldMsg('impact','Low impact not allowed with High priority','error',false);
```

## GlideForm - setDisabled\(String fieldName, Boolean disable\)

Makes the specified field available or unavailable.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|
|disable|Boolean|When true disables the field. When false enables the field.|

|Type|Description|
|----|-----------|
|void| |

## GlideForm - setDisplay\(String fieldName, Boolean display\)

Displays or hides a field.

This method cannot hide a mandatory field with no value. If the field is hidden, the space is used to display other items. Whenever possible, use a UI policy instead of this method.

|Name|Type|Description|
|----|----|-----------|
|fieldname|String|Name of the field.|
|display|Boolean|When true displays the field, when false hides the field.|

|Type|Description|
|----|-----------|
|void| |

```
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
   //If the page isn't loading
   if (!isLoading) {
      //If the new value isn't blank
      if (newValue != '') {
         g_form.setDisplay('priority', false);   
      }
      else 
         g_form.setDisplay('priority', true);
      }
   }
```

## GlideForm - setLabelOf\(String fieldName, String label\)

Sets the plain text value of the field label.

**Note:** This method is not supported by Service Catalog.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|
|label|String|The field text label.|

|Type|Description|
|----|-----------|
|void| |

```
if (g_user.hasRole('itil')) {
    var oldLabel = g_form.getLabelOf('comments');
    g_form.setLabelOf('comments', oldLabel + ' (Customer visible)');
}
```

## GlideForm - setReadOnly\(String fieldName, Boolean readOnly\)

Makes the specified field read-only or editable.

Whenever possible, use a UI policy instead of this method.

To make a mandatory field read-only, you must first remove the mandatory requirement for that field by using the setMandatory\(\) method.

Once you set a field to read-only, you cannot use the [setValue\(\)](c_GlideFormAPI.md#) method to update the value of that field. If you need to set the value in this way, you must set the readOnly value to false.

<table id="table_xdf_qpc_5s" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldName

</td><td>

String

</td><td>

Name of the field.

</td></tr><tr><td>

readOnly

</td><td>

Boolean

</td><td>

Flag that determines whether the associate field is editable or read-only.Possible values:

-   true: Set field to read-only
-   false: Set field to be editable

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how set the Variable Editor to read only. To do this in Service Catalog tables, use setVariablesReadOnly\(\).

```
// Create a Client Script on a table (e.g., incident) and paste this script
// Uncheck (set to false) the "isolate script" checkbox (not available by default)
// To add the isolate script checkbox to the form, configure form layout to add the checkbox
function onLoad() { 
  $("variable_map").querySelectorAll("item").forEach(function(item){
    var variable = item.getAttribute("qname"); 
    g_form.setReadOnly("variables."+ variable, true); 
  }); 
}
```

## GlideForm - setValue\(String fieldName, String value\)

Sets the value of a specified form field to the passed in value.

This method also supports setting values in a multi-row variable set \(MRVS\). You must first use `JSON.parse(getValue('<mrvs_field_name>'))` to obtain the MRVS array and then use indexing to update the fields within the row objects. Once all values are updated in the MRVS, use the setValue\(\) method to save the updated MRVS array. For more details, see the code example below.

**Note:** The method setValue\(\) can cause a stack overflow when used in an OnChange client script. This is because every time the value is set, it will register as a change, which may re-trigger the OnChange client script. To prevent this, perform a check that will validate that the new value will be different from the old value. For example, before performing `setValue(shortDesc, newValue.toUpperCase());`, validate that the short description is not already uppercase. This will prevent the client script from applying the toUpperCase\(\) more than once.

<table id="table_bqz_pqc_5s" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldName

</td><td>

String

</td><td>

Name of the form field to update.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

String value to set in the specified field.**Note:** When defining a value in a choice list, be sure to use the number value rather than the label.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following example shows how to set the short description in the current form.

```
g_form.setValue('short_description', 'replace this with appropriate text');
```

The following example shows how to set values in an MRVS. In this example, salaries are being managed through the Service Catalog. The client script searches all rows within the MRVS for the value entered in the **Job title** and then updates the matching entries within the MRVS with what is entered in the **Salary** field. The MRVS is named "variable\_set\_1" and contains the following fields within each row object: Employee name \[employee\_name\], Job title \[employee\_job\_title\], and Salary \[employee\_salary\]. In addition, the Catalog Item contains: Job title \[job\_title\] and Salary \[salary\].

```
function onChange(control, oldValue, newValue, isLoading) {
if (isLoading || newValue == '') {
return;
}

// Get the MRVS
var multiRowVariableSet = JSON.parse(g_form.getValue('variable_set_1'));

for (var i = 0; i < multiRowVariableSet.length; i++) {
// Check if the entered job title matches the title in the current MRVS row
  if (multiRowVariableSet[i].employee_job_title == g_form.getValue("job_title")){
    // Update the value of a matching field with the new salary
    multiRowVariableSet[i].employee_salary = newValue;
  }
}

// Update the MRVS
g_form.setValue('variable_set_1', JSON.stringify(multiRowVariableSet));
}
```

## GlideForm - setVariablesReadOnly\(Boolean isReadOnly\)

Makes a Service Catalog variable editor read only.

**Note:** This method is only applicable to Service Catalog variable editors in the core UI. This method is not supported in the Service Catalog form.

The method must be placed in the client script of the table in which the variable editor is added, such as Requested Item \[sc\_req\_item\], Incident \[incident\], and so on. To set variables to read only in other tables, use the [setReadOnly\(\)](c_GlideFormAPI.md#) method.

See also: [Service Catalog variable editors](https://www.servicenow.com/docs/access?context=service-catalog-variable-editor&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

<table id="table_xdf_qpc_5s" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isReadOnly

</td><td>

Boolean

</td><td>

Flag that determines whether the variable editor is read only.Possible values:

-   true: Sets the variable editor as read-only.
-   false: Sets the variable editor as editable.

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

Adding the following line to a client script sets the variable editor to read only.

```
g_form.setVariablesReadOnly(true);
```

## GlideForm - setVisible\(String fieldName, Boolean display\)

Displays or hides the field.

On desktop UI, the space is left blank when hidden. On Mobile or Service Portal UI, the space is filled in my other fields when hidden. This method cannot hide mandatory fields with no value.

Use UI Policy rather than this method whenever possible.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The field name.|
|display|Boolean|When true displays the field. When false hides the field.|

|Type|Description|
|----|-----------|
|void| |

```
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
   //If the page isn't loading
   if (!isLoading) {
      //If the new value isn't blank
      if(newValue != '') {
         g_form.setVisible('priority', false); 
      }
      else
         g_form.setVisible('priority', true); 
      }
   }
```

## GlideForm - showErrorBox\(String name, String message\)

Displays an error message under the specified form field \(either a control object or the name of the field\). If the control or field is currently off the screen, the form scrolls to the control or field.

A global property \(glide.ui.scroll\_to\_message\_field\) is available that controls automatic message scrolling when the form field is off screen \(scrolls the form to the control or field\). The showFieldMsg\(\) method is a similar method that requires a type parameter.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the control or field.|
|message|String|The message to be displayed.|

|Type|Description|
|----|-----------|
|void| |

## GlideForm - showRelatedList\(String listTableName\)

Displays the specified related list on the form.

This method is not available on the mobile platform. If this method is run on a mobile platform, no action occurs.

|Name|Type|Description|
|----|----|-----------|
|listTableName|String|Name of the related list.|

|Type|Description|
|----|-----------|
|void| |

## GlideForm - showRelatedLists\(\)

Displays all the form's related lists.

This method is not available on the mobile platform. If this method is run on a mobile platform, no action occurs.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## GlideForm - submit\(\)

Saves the record.

The user is taken away from the form, returning them to where they were.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## GlideForm - submit\(String verb\)

Performs the UI action specified by the parameter.

|Name|Type|Description|
|----|----|-----------|
|verb|String|An action\_name from a sys\_ui\_action record. The action name must be for a visible form button.|

|Type|Description|
|----|-----------|
|void| |

