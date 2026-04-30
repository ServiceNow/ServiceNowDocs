---
title: GlideModal \(Next Experience\) - Client
description: The GlideModal API provides methods for displaying a content overlay, known as a modal. Modals are interactive windows that appear above a page and close when a user takes an action. You can use a modal to display information, ask questions, or perform actions.Creates an instance of the GlideModal class.Closes the current modal.Returns the GlideModal object identified by the specified UI page name.Returns the GlideModal ID.Returns the value of the specified preference \(property\).Returns all preferences and values associated with the modal.Renders the UI page specified when the API was instantiated in the modal. You must call this method after you define the modal for it to appear in the UI.Displays a modal with the specified string-based HTML content.Sets the dialog name as a table preference for the GlideModal.Sets the specified preferences and then reloads the modal.Sets the specified field on the current form to the specified value.Sets the title of the modal.Sets the width of the modal. Dora has asked a very logical question here and I'm not sure where the setHeight method is. There definitely should probably be one. Let me know if you need help.Change the view and reload the modal.Returns the type as GlideModal.Updates the title specified using GlideModal setTitle\(\) method.
locale: en-US
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Client Next Experience API reference, API reference, API implementation and reference]
---

# GlideModal \(Next Experience\)- Client

The GlideModal API provides methods for displaying a content overlay, known as a modal. Modals are interactive windows that appear above a page and close when a user takes an action. You can use a modal to display information, ask questions, or perform actions.

Use the GlideModal methods in scripts anywhere that you can use client-side JavaScript. These methods are most often called from a UI action with the **Client** check box selected.

Modals can contain different types of content such as:

-   Static text
-   Dynamic text
-   Forms
-   Images
-   Buttons

Using this API you can:

-   Get an existing modal.
-   Create modal content from a UI page or from passed HTML.
-   Set the title in the modal.
-   Set the width of the modal.
-   Get and set preferences.
-   Switch modal views.

To make a modal appear in the UI you must call one of the render methods:

-   [GlideModal \(Next Experience\) - render\(\)](GModClientAPINX.md#)
-   [GlideModal \(Next Experience\) - renderWithContent\(String html\)](GModClientAPINX.md#)

The following code example shows how to create and render a modal using the UI page "UI\_dialog\_name".

```
var dialog = new nowapi.GlideModal("UI_dialog_name");

//Set the dialog title
dialog.setTitle('Show title');

//Set the dialog width		      	
dialog.setWidth(550);

//Display the modal
dialog.render();
```

**Parent Topic:**[Client Next Experience API reference](../../../../../build/applications/concept/api-client-next.md)

## GlideModal \(Next Experience\) - GlideModal\(String id, Boolean readOnly, Number/String width\)

Creates an instance of the GlideModal class.

<table id="table_ups_b4s_3v" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

String

</td><td id="GMod-GMod-id-entry">

Name of the[UI page](../../../../../script/server-scripting/reference/r_UIPages.md#) to load into the modal.You can also specify either the `glide_modal_confirm` or `glide_modal_info` modals that are provided in the base system.

Table: UI Page \[sys\_ui\_page\]

</td></tr><tr><td>

readOnly

</td><td>

Boolean

</td><td id="GMod-GMod-readOnly-entry">

Optional. Flag that indicates whether the content in the modal is read-only.Valid values:

-   true: Content is read only.
-   false: User can modify the content.

Default: false

</td></tr><tr><td>

width

</td><td>

Number or String

</td><td id="GMod-GMod-width-entry">

Optional. Width of the modal in pixels or the modal CSS class. If a pixel width is passed, it aligns the specified width with the corresponding CSS class.Possible modal CSS classes:

-   modal-alert: \(300 px\) Assigned when the specified width is 0 to 349 pixels.
-   modal-sm: \(400 px\) Assigned when the specified width is 350 to 449 pixels.
-   modal-md: \(600 px\) Assigned when the specified width is 450 to 649 pixels.
-   modal-lg: \(900 px\) Assigned when the specified width is 650 to 900 pixels.

Default: modal-md

Maximum width: 900 pixels

**Note:** You can also set the modal width using the setWidth\(\) method.

</td></tr></tbody>
</table>The following code example shows how to create a GlideModal object using an existing UI page.

```
var dialog = new nowapi.GlideModal('UI_dialog_name');

//Set the dialog title
dialog.setTitle('Show title'); 

//Set the desired preferences
dialog.setPreference('table', 'task'); 			
dialog.setPreference('name', 'value');        	

//Opens the dialog
dialog.render();
```

The following code example shows how to create a GlideModal object using the `glide_modal_confirm` file.

```
var dialog = new nowapi.GlideModal('glide_modal_confirm', true, 300);
dialog.setTitle(new GwtMessage().getMessage('Confirmation'));
dialog.setPreference('body', new GwtMessage().format("This will complete all update sets in the batch. Continue changing state to complete?"));
dialog.setPreference('focusTrap', true);
dialog.setPreference('onPromptComplete', doComplete);
dialog.setPreference('onPromptCancel', doCancel);
dialog.render();
	
function doComplete() {
  callback(true);
}
	
function doCancel() {
  callback(false);
}
```

## GlideModal \(Next Experience\) - destroy\(\)

Closes the current modal.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to use the destroy\(\) method to close a modal.

```
function cancelDialog(){

  var dialog = new nowapi.GlideModal('cancelTask');

  // Sets the dialog title
  dialog.setTitle('Cancel Task');

  // Set up valid custom HTML to display
  dialog.renderWithContent('<div style="padding:15px">
    <p>What action do you want to take?</p>
    <p><select name="cancellation" id="taskCancellation" class="form-control">
    <option value="cancelOnly" role="option">Cancel task but keep requested item open
    </option>
    <option value="cancelAll" role="option">Cancel this and all other tasks, closing the
    requested item</option></select></p><div style="padding:5px;float:right"><button 
    style="padding:5px;margin-right:10px onclick="window.changeTaskAction(this.innerHTML,
    jQuery(\'#taskCancellation\').val())" class="btn btn-default">Abort</button>
    <button style="padding:5px" class="btn btn-primary" 
    onclick="window.changeTaskAction(this.innerHTML,jQuery(\'#taskCancellation\').val())">
    Cancel Task</button></div></div>');

  // Use the windows object to ensure the code is accessible from the modal dialog
  window.changeTaskAction = function(thisButton, thisAction){

    // Close the GlideModal dialog window
    dialog.destroy();

    // Submit to the back-end
    if(thisButton=='Cancel Task'){
      if(thisAction=="cancelAll"){
        // Closed Incomplete -- will close the Requested Item and all other open tasks
        g_form.setValue('state',4);
      }else{
        // Closed Skipped -- will only close this task
        g_form.setValue('state',7);
      }
         //Regular ServiceNow form submission
         gsftSubmit(null, g_form.getFormElement(), 'cancel_sc_task');
      }
   };

   // Prevents the form from submitting when the dialog first loads
   return false;
}
```

The following code example shows how to use GlideModal.get\(\).destroy\(\) to close a modal in a client script. The following button should be declared in the UI page HTML: `<button onclick="closeMe()">close</button>`.

```
function closeGlideModal() {
  try {
    nowapi.GlideModal.get().destroy();
  } catch (err) {
    console.warn("closeGlideModal ERROR: " + err.message);
    var x = document.getElementById('THE_NAME_OF_YOUR_UI_PAGE' + '_closemodal');
    if (x) {
      x.click();
    } else {
      console.warn("No 'X' close button found!");
    }
  }
}

function closeMe() {
  setTimeout(function() {
    closeGlideModal();
  }, 100);
}
```

## GlideModal \(Next Experience\) - get\(String id\)

Returns the GlideModal object identified by the specified UI page name.

Use this method to obtain the GlideModal object to use in other GlideModal operations such as, `GlideModal.get().destroy()`.

<table id="table_vwy_xjz_3v" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

String

</td><td id="GMod-get-id-entry">

Name of the[UI page](../../../../../script/server-scripting/reference/r_UIPages.md#) associated with the modal.You can also specify either the `glide_modal_confirm` or `glide_modal_info` modals that are provided in the base system.

Table: UI Page \[sys\_ui\_page\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideModal|Requested GlideModal object.|

This example shows how to use the get\(\) method to obtain the modal that you want to close using the destroy\(\) method.

```
// If the modal was initially created like this:

var dialog = new nowapi.GlideModal("glide_modal_confirm"); 
dialog.render();

// Code using the modal
...

// Now use the get() and destroy() methods to close the modal
var glideModal = new nowapi.GlideModal().get("glide_modal_confirm");
glideModal.destroy();

// You could also code it like this:
// GlideModal.prototype.get('glide_modal_confirm').destroy();
```

## GlideModal \(Next Experience\) - getID\(\)

Returns the GlideModal ID.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|ID of the GlideModal.|

The following example demonstrates how to get the GlideModal ID on the instance.

```
var id = modal.getID();
console.log('modal id', id);
```

## GlideModal \(Next Experience\) - getPreference\(String name, String value\)

Returns the value of the specified preference \(property\).

Invoking actions that create the modal typically also create the necessary preferences for the modal using the [GlideModal \(Next Experience\) - setPreference\(String name, String value\)](GModClientAPINX.md#) method. The UI page client script can then consume these preferences using this method.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the preference value to retrieve. This value must have previously been set on the modal using the setPreference\(\) method.|
|value|String|Value of the preference to retrieve. This value must have previously been set on the modal using the setPreference\(\) method.|

|Type|Description|
|----|-----------|
|String|Specified preference's value.|

This example shows a simple case of setting a preference and then retrieving that preference from a specified modal.

```
var dialog = new nowapi.GlideModal('UI_dialog_name');
//Sets the dialog title
dialog.setTitle('Modal title');

//Sets the value of the preference table
dialog.setPreference('table', 'incident');

//Gets the value of the preference table
var title = dialog.getPreference('table');
```

## GlideModal \(Next Experience\) - getPreferences\(\)

Returns all preferences and values associated with the modal.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Specified preference's value.|

This example shows a simple case of setting a preference and then retrieving that preference from a specified modal.

```
var dialog = new nowapi.GlideModal('UI_dialog_name');
//Sets the dialog title
dialog.setTitle('Modal title');

//Sets the value of the preference table
dialog.setPreference('table', 'incident');

//Gets the value of the preference table
var title = dialog.getPreference('table');
```

## GlideModal \(Next Experience\) - render\(\)

Renders the UI page specified when the API was instantiated in the modal. You must call this method after you define the modal for it to appear in the UI.

Call this method when you use a UI page to generate the content in your modal. If you want to display HTML within a modal, call [renderWithContent\(String html\)](GModClientAPINX.md#) to render the modal.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to instantiate a GlideModal object using the UI page "UI\_dialog\_name", set the title and width of the modal, and then display the modal in the UI \(render\).

```
var dialog = new nowapi.GlideModal("UI_dialog_name");

//Set the dialog title and width
dialog.setTitle('Show title');		      	
dialog.setWidth(550);

//Display the dialog
dialog.render();
```

## GlideModal \(Next Experience\) - renderWithContent\(String html\)

Displays a modal with the specified string-based HTML content.

Use the renderWithContent\(\) method in lieu of the render\(\) method when deriving the modal content from HTML.

|Name|Type|Description|
|----|----|-----------|
|html|String|HTML content to display in the modal.|

|Type|Description|
|----|-----------|
|None| |

This code example shows how to display a modal that is constructed using the passed HTML string which contains a list of choices that the user can select from.

```
function cancelDialog(){

  var dialog = new nowapi.GlideModal('cancelTask');

  // Sets the dialog title
  dialog.setTitle('Cancel Task');

  // Set up valid custom HTML to display
  dialog.renderWithContent('<div style="padding:15px">
    <p>What action do you want to take?</p>
    <p><select name="cancellation" id="taskCancellation" class="form-control">
    <option value="cancelOnly" role="option">Cancel task but keep requested item open
    </option>
    <option value="cancelAll" role="option">Cancel this and all other tasks, closing the
    requested item</option></select></p><div style="padding:5px;float:right"><button 
    style="padding:5px;margin-right:10px onclick="window.changeTaskAction(this.innerHTML,
    jQuery(\'#taskCancellation\').val())" class="btn btn-default">Abort</button>
    <button style="padding:5px" class="btn btn-primary" 
    onclick="window.changeTaskAction(this.innerHTML,jQuery(\'#taskCancellation\').val())">
    Cancel Task</button></div></div>');

  // Use the windows object to ensure the code is accessible from the modal dialog
  window.changeTaskAction = function(thisButton, thisAction){

    // Close the GlideModal dialog window
    dialog.destroy();

    // Submit to the back-end
    if(thisButton=='Cancel Task'){
      if(thisAction=="cancelAll"){
        // Closed Incomplete -- will close the Requested Item and all other open tasks
        g_form.setValue('state',4);
      }else{
        // Closed Skipped -- will only close this task
        g_form.setValue('state',7);
      }
         //Regular ServiceNow form submission
         gsftSubmit(null, g_form.getFormElement(), 'cancel_sc_task');
      }
   };

   // Prevents the form from submitting when the dialog first loads
   return false;
}
```

## GlideModal \(Next Experience\) - setDialog\(String dialogName\)

Sets the dialog name as a table preference for the GlideModal.

<table id="table_qqw_yr1_sfc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dialogName

</td><td>

String

</td><td>

The name of the modal dialog to be used as the dialog name and corresponding preference table.See also:

-   [setPreference\(\)](GModClientAPINX.md#)
-   [setPreferenceAndReload\(\)](GModClientAPINX.md#)

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to set a modal dialog name as a table preference.

```
var dialog = new nowapi.GlideModal('change_confirm_reason', false, 648, 250);
dialog.setTitle(new GwtMessage().getMessage('Cancel Change Request'));
dialog.setPreference('focusTrap', true);
dialog.setDialog('onPromptComplete');
dialog.setPreference('onPromptCancel', onPromptCancel);
dialog.on('closeconfirm', onPromptCancel);
dialog.setPreference('buttonLabelComplete', new GwtMessage().getMessage('OK'));
dialog.setPreference('buttonLabelCancel', new GwtMessage().getMessage('Cancel'));
dialog.render();
```

## GlideModal \(Next Experience\) - setPreferenceAndReload\(Object properties\)

Sets the specified preferences and then reloads the modal.

|Name|Type|Description|
|----|----|-----------|
|properties|Object|Name-value pairs to set as preferences in the format.|

|Type|Description|
|----|-----------|
|None| |

In this example, the setPreferenceAndReload\(\) function sets preferences and reloads the modal with updated preferences. The modal renders with the initial preferences, and after 5 seconds the setPreferenceAndReload\(\) is called and reloads the modal with the updated preferences.

```
 // UI Page to render in the GlideModal is 'glide_modal_confirm'
 var glideModal = new nowapi.GlideModal("glide_modal_confirm", false, 600);
 glideModal.setTitle(getMessage("Confirmation"));
 glideModal.setPreference("body", getMessage("Are you sure you want to reject this deal registration? This action cannot be undone."));
 glideModal.setPreference('buttonLabelComplete', getMessage("Reject"));
 glideModal.setPreference('buttonLabelCancel', getMessage("Cancel"));
 glideModal.render();

 var preferences = {
     "body": "THIS IS THE UPDATED BODY PREFERENCE",
     "buttonLabelComplete": "NEW REJECT",
     "buttonLabelCancel": "NEW CANCEL"
 };

 setTimeout(function() {
     glideModal.setPreferenceAndReload(preferences);
 }, 5000);
```

## GlideModal \(Next Experience\) - setPreference\(String name, String value\)

Sets the specified field on the current form to the specified value.

<table id="table_cvd_zqs_3v" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td id="GMod-setPreference-name-entry">

Name of the form field to update. If this field does not exist on the current form, the request is ignored.

</td></tr><tr><td>

value

</td><td>

String

</td><td id="GMod-setPreference-value-entry">

Value to store in the specified form field.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to set the **table** preference to 'task' and the **name** preference to 'value'.

```
var dialog = new nowapi.GlideModal('UI_dialog_name');

//Set the dialog title
dialog.setTitle('Show title'); 

//Set the desired preferences
dialog.setPreference('table', 'task'); 			
dialog.setPreference('name', 'value');        	

//Opens the dialog
dialog.render();
```

## GlideModal \(Next Experience\) - setTitle\(String title\)

Sets the title of the modal.

|Name|Type|Description|
|----|----|-----------|
|title|String|Text to display in the title of the modal.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to set the modal title to `Table to update`.

```
var dialog = new nowapi.GlideModal('UI_dialog_name');

//Sets the dialog title
dialog.setTitle('Table to update'); 
dialog.setPreference('table', 'task'); 			      	
dialog.setWidth(550);

//Opens the dialog
dialog.render();
```

## GlideModal \(Next Experience\) - setWidth\(Number/String width\)

Sets the width of the modal.

You can also set the width of a modal when you first instantiate the API using the [GlideModal\(\)](GModClientAPINX.md#) constructor.

<table id="table_msx_wts_3v" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

width

</td><td>

Number or String

</td><td id="GMod-setWidth-width-entry">

Width of the modal in pixels or the modal CSS class. If a pixel width is passed, it aligns the specified width with the corresponding CSS class.Possible modal CSS classes:

-   modal-alert: \(300 px\) Assigned when the specified width is 0 to 349 pixels.
-   modal-sm: \(400 px\) Assigned when the specified width is 350 to 449 pixels.
-   modal-md: \(600 px\) Assigned when the specified width is 450 to 649 pixels.
-   modal-lg: \(900 px\) Assigned when the specified width is 650 to 900 pixels.

Maximum width: 900 pixels

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to set the modal width to 550 pixels.

```
var dialog = new nowapi.GlideModal('UI_dialog_name');

//Sets the dialog title
dialog.setTitle('Show title'); 
dialog.setPreference('name', 'value'); 			      	
dialog.setWidth(550);

//Opens the dialog
dialog.render();
```

## GlideModal \(Next Experience\) - switchView\(String newView\)

Change the view and reload the modal.

|Name|Type|Description|
|----|----|-----------|
|newView|String|View to use.|

|Type|Description|
|----|-----------|
|None| |

## GlideModal \(Next Experience\) - type\(\)

Returns the type as GlideModal.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Returns a string indicating that the type is GlideModal.|

## GlideModal \(Next Experience\) - updateTitle\(\)

Updates the title specified using GlideModal setTitle\(\) method.

You must always first call [GlideModal \(Next Experience\) - setTitle\(String title\)](GModClientAPINX.md#) to specify the Modal title using updateTitle\(\) to commit the change.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example demonstrates how to use set and update a modal's title by calling setTitle\(\) and updateTitle\(\) respectively.

```
var modal = new nowapi.GlideModal();
modal.renderWithContent('TEST CONTENT');

setTimeout(function() {
    modal.setTitle("TEST setTitle() AND updateTitle() METHODS"); // will only update the `title` prop, updateTitle() must be called to see change
    modal.updateTitle();
}, 3000);
```

