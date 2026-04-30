---
title: GlideModal - Client
description: The GlideModal API provides methods for displaying a content overlay, known as a modal. Modals are interactive windows that appear above a page and close when a user takes an action. You can use a modal to display information, ask questions, or perform actions.Creates an instance of the GlideModal class.Closes the current modal.Returns the GlideModal object identified by the specified UI page name.Returns the value of the specified preference \(property\). Use preferences to pass data into the page being rendered.Renders the UI page specified when the API was instantiated in the modal. You must call this method after you define the modal for it to appear in the UI.Displays a modal with the specified string-based HTML content.Sets the value of the specified preference \(property\). Use preferences to pass data into the page being rendered.Sets the specified preferences and then reloads the modal.Sets the title of the modal.Sets the width of the modal.Change the view and reload the modal.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 15
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideModal- Client

The GlideModal API provides methods for displaying a content overlay, known as a modal. Modals are interactive windows that appear above a page and close when a user takes an action. You can use a modal to display information, ask questions, or perform actions.

Use the GlideModal methods in scripts anywhere that you can use client-side JavaScript. These methods are most often called from a UI action with the **Client** check box selected.

Using the GlideModal API you can create custom modals or you can leverage existing base-system modals.

**Note:** This is a fully-featured replacement for the GlideWindow and GlideDialogWindow APIs.

GlideModal doesn't work in workspace, instead use the [g\_modal](../../g_modal/concept/g_modalClientAPI.md#) API.

![Example overlay](../../Images/GlideModalV3-Client-example-overlay-dialog.png "Example modal")

Modals can contain different types of content such as:

-   Static text
-   Dynamic text
-   Forms
-   Images
-   Buttons

Using this API you can:

-   Retrieve a base-system modal such as `glide_confirm`, `glide_info`, or `glide_alert`.
-   Create modal content from a UI page or from passed HTML.
-   Set the title in the modal.
-   Set the body content of the modal.
-   Set the width of the modal.
-   Get and set preferences.
-   Switch modal views.

To make a modal appear in the UI you must call one of the render methods:

-   [GlideModal - render\(\)](c_GlideModalV3API.md#)
-   [GlideModal - renderWithContent\(String html\)](c_GlideModalV3API.md#)

The following code example shows how to create and render a modal using the UI page "my\_modal".

```
var dialog = new GlideModal("my_modal");

//Set the dialog title
dialog.setTitle('Show title');

//Set the dialog width		      	
dialog.setWidth(550);

//Display the modal
dialog.render();
```

This code example shows how to create and render a modal using the renderWithContent\(\) method and HTML to define the content of the modal.

```
function cancelDialog(){

  var dialog = new GlideModal('cancelTask');
  //Sets the dialog title
  dialog.setTitle('Cancel Task');
  //Set up valid custom HTML to display
  dialog.renderWithContent('<div style="padding:15px"><p>What action do you want to take?</p>
    <p><select name="cancellation" id="taskCancellation" class="form-control">
    <option value="cancelOnly" role="option">Cancel this task but keep the requested item open</option>
    <option value="cancelAll" role="option">Cancel this and all other tasks, closing the requested item</option>
    </select></p><div style="padding:5px;float:right"><button style="padding:5px;margin-right:10px" 
    onclick="window.changeTaskAction(this.innerHTML,jQuery(\'#taskCancellation\').val())" 
    class="btn btn-default">Abort</button><button style="padding:5px" class="btn btn-primary" 
    onclick="window.changeTaskAction(this.innerHTML,jQuery(\'#taskCancellation\').val())">Cancel Task</button></div></div>');

  //Use the windows object to ensure the code is accessible from the modal dialog
  window.changeTaskAction = function(thisButton, thisAction){

    //Close the GlideModal dialog window
    dialog.destroy();

    //Submit to the back-end
    if(thisButton=='Cancel Task'){
      if(thisAction=="cancelAll"){
        g_form.setValue('state',4); //Closed Incomplete -- will close the Requested Item and all other open tasks
      }else{
        g_form.setValue('state',7); //Closed Skipped -- will only close this task
      }
         //Regular ServiceNow form submission
         gsftSubmit(null, g_form.getFormElement(), 'cancel_sc_task');
      }
   };
   return false; //Prevents the form from submitting when the dialog first load
}
```

## Base system modals

A base ServiceNow instance provides the following modals, defined as UI pages, that you can use when displaying a modal with GlideModal:

-   `glide_alert_standard`: An alert modal with an **OK** button and an info or warning icon.

    ![glide_alert_standard modal](../image/GM-glide_modal_alert.png)

-   `glide_ask_standard`: A confirmation modal with **Yes** and **No** buttons.

    ![glide_ask_standard modal](../image/GM-glide_ask_standard.png)

-   `glide_confirm`: A confirmation modal with **Don't save**, **Cancel**, and **Save** buttons.

    ![glide_confirm modal](../image/GM-glide_modal_confirm.png)

-   `glide_confirm_basic`: A confirmation modal with an **OK** and **Cancel** button, without an icon.

    ![glide_confirm_basic modal](../image/GM-glide_modal_confirm_basic.png)

-   `glide_confirm_standard`: A confirmation modal with an **OK** and **Cancel** button, and an info or warning icon.

    ![glide_confirm_standard modal](../image/GM-glide_modal_confirm_standard.png)

-   `glide_info`: An information modal with an info icon and an **OK** button the width of the modal window.

    ![glide_info modal](../image/GM-glide_modal_info.png)

-   `glide_progress_standard`: An information modal with a **Close** button, an info or warning icon, and a scrolling progress bar. The progress bar is an animated GIF image and can't be updated as a typical progress bar.

    ![glide_progress_standard modal](../image/GM-glide_modal_progress_standard.png)

-   `glide_progress_no_button`: An information modal with an info or warning icon, and a scrolling progress bar. The progress bar is an animated GIF image and can't be updated as a typical progress bar.

    ![glide_progress_no_button modal](../image/GM-glide_modal_progress_no_button.png)

-   `glide_prompt`: A modal with a prompt text box and an **OK** and **Cancel** button.

    ![glide_prompt modal](../image/GM-glide_modal_prompt.png)

-   `glide_warn`: A simple modal with an **OK** button, but no icon.

    ![glide_warn modal](../image/GM-glide_modal_warn.png)


## Preferences

Modal preferences provides a way to pass data into the modal being rendered. You use the [setPreference\(\)](c_GlideModalV3API.md#) or [setPrefAndReload\(\)](c_GlideModalV3API.md#) methods to set a preference value. You then use the [GlideModal - getPreference\(String name\)](c_GlideModalV3API.md#) method to retrieve a set preference.

To retrieve preferences in a UI page, use the following function: RP.getWindowProperties\(\).get\('preference\_name'\).

Some of the base-system modals support the following system-based preferences:

-   autoFocus: Flag that indicates whether the modal automatically receives focus once it is rendered. Set to true when the modal is initialized.
-   body: Sets the passed content in the body of the modal.
-   buttonClass: Sets the button class.
-   buttonClassCancel: Sets the class for the cancel button on the modal.
-   buttonClassComplete: Sets the class for the OK button \(complete\) on the modal.
-   buttonLabel Sets the button label.
-   buttonLabelCancel: Sets the label for the cancel button on the modal.
-   buttonLabelComplete: Sets the label for the OK button \(complete\) on the modal.
-   callbackParam: Sets a callback parameter.
-   focusTrap: Flag that indicates whether to block all interactions outside of the modal while open. Set to false when the modal is initialized.
-   modal\_title: Sets the title of the modal. Used by the setTitle\(\) method.
-   onPromptCancel: Defines a function to call when the user selects the **Cancel** button.

    For example:

    ```
    dialog.setPreference("onPromptCancel", function() {
      return false;
    });
    ```

-   onPromptComplete: Defines a function to call when the user selects the **OK** button.

    For example:

    ```
    dialog.setPreference("onPromptComplete", function () {
      gsftSubmit(null, g_form.getFormElement(), 'check_button');
    });
    ```


**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideModal - GlideModal\(String id, Boolean readOnly, Number/String width\)

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

</td><td>

Name of the[UI page](../../../../../script/server-scripting/reference/r_UIPages.md#) to load into the modal.You can find the list of available UI pages in **System UI** &gt; **UI Pages**

</td></tr><tr><td>

readOnly

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the content in the modal is read-only.Valid values:

-   true: Content is read only.
-   false: User can modify the content.

Default: false

</td></tr><tr><td>

width

</td><td>

Number or String

</td><td>

Optional. Width of the modal in pixels or the modal CSS class. If a pixel width is passed, it aligns the specified width with the corresponding CSS class.Possible modal CSS classes:

-   modal-alert: \(300 px\) Assigned when the specified width is 0 to 349 pixels.
-   modal-sm: \(400 px\) Assigned when the specified width is 350 to 449 pixels.
-   modal-md: \(600 px\) Assigned when the specified width is 450 to 649 pixels.
-   modal-lg: \(900 px\) Assigned when the specified width is 650 to 900 pixels.

Default: modal-md

Maximum width: 900 pixels

**Note:** You can also set the modal width using the [GlideModal - setWidth\(Number/String width\)](c_GlideModalV3API.md#) method.

</td></tr></tbody>
</table>The following code example shows how to create a GlideModal object using an existing UI page.

```
var dialog = new GlideModal('UI_dialog_name');

//Set the dialog title
dialog.setTitle('Show title'); 

//Set the desired preferences
dialog.setPreference('table', 'task'); 			
dialog.setPreference('name', 'value');        	

//Opens the dialog
dialog.render();
```

The following code example shows how to create a GlideModal object using the `glide_confirm` file.

```
var dialog = new GlideModal('glide_confirm', true, 300);
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

## GlideModal - destroy\(\)

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

var gmod = new GlideModal('cancelTask');
  //Sets the dialog title
  gmod.setTitle('Cancel Task');
  //Set up valid custom HTML to be displayed
  gmod.renderWithContent('<div style="padding:15px"><p>What action do you want to take?</p>
    <p><select name="cancellation" id="taskCancellation" class="form-control">
    <option value="cancelOnly" role="option">Cancel this task but keep the requested item open</option>
    <option value="cancelAll" role="option">Cancel this and all other tasks, closing the requested item</option>
    </select></p><div style="padding:5px;float:right"><button style="padding:5px;margin-right:10px" 
    onclick="window.changeTaskAction(this.innerHTML,jQuery(\'#taskCancellation\').val())" 
    class="btn btn-default">Abort</button><button style="padding:5px" 
    class="btn btn-primary" onclick="window.changeTaskAction(this.innerHTML,jQuery(\'#taskCancellation\').val())">
    Cancel Task</button></div></div>');

  //Use the windows object to ensure our code is accessible from the modal dialog
  window.changeTaskAction = function(thisButton, thisAction){

    //Close the glide modal dialog window
    gmod.destroy();

    //Submit to the back-end
    if(thisButton=='Cancel Task'){
      if(thisAction=="cancelAll"){
        g_form.setValue('state',4); //Closed Incomplete -- closes the Requested Item and all other open tasks
      }else{
        g_form.setValue('state',7); //Closed Skipped -- only closes this task
      }
      //Regular ServiceNow form submission
      gsftSubmit(null, g_form.getFormElement(), 'cancel_sc_task');
    }
  };
  return false; //Prevents the form from submitting when the dialog first load
}
```

The following code example shows how to use GlideModal.get\(\).destroy\(\) to close a modal in a client script. The following button should be declared in the UI page HTML: `<button onclick="closeMe()">close</button>`.

```
function closeGlideModal() {
  try {
    GlideModal.get().destroy();
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

## GlideModal - get\(String id\)

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

</td><td>

Name of the[UI page](../../../../../script/server-scripting/reference/r_UIPages.md#) associated with the modal.You can also specify the [base system modals](c_GlideModalV3API.md#) that are provided in a base instance.

You can find the list of available UI pages in **System UI** &gt; **UI Pages**.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|[GlideModal](c_GlideModalV3API.md#)|Requested GlideModal object.|

This example shows how to use the get\(\) method to obtain the modal that you want to close using the destroy\(\) method.

```
// If the modal was initially created like this:

var dialog = new GlideModal("glide_confirm"); 
dialog.render();

// Some code using the modal
.
.
.

// Now use the get() and destroy() methods to close the modal
var glideModal = new GlideModal().get("glide_confirm");
glideModal.destroy();

// You could also code it like this:
GlideModal.prototype.get("glide_confirm").destroy();
```

## GlideModal - getPreference\(String name\)

Returns the value of the specified preference \(property\). Use preferences to pass data into the page being rendered.

Invoking actions that create the modal typically also create the necessary preferences for the modal using the [GlideModal - setPreference\(String name, String value\)](c_GlideModalV3API.md#) method. The UI page client script can then consume these preferences using this method and the following function: RP.getWindowProperties\(\).get\('preference\_name'\).

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the preference value to retrieve. This value must have been previously set on the modal using the [GlideModal - setPreference\(String name, String value\)](c_GlideModalV3API.md#) method.|

|Type|Description|
|----|-----------|
|String|Specified preference's value.|

This example shows a simple case of setting a preference and then retrieving that preference from a specified modal.

```
var dialog = new GlideModal('UI_dialog_name');
// Sets the dialog title
dialog.setTitle('Modal title');

// Sets the value of the preference table
dialog.setPreference('table', 'incident');

// Gets the value of the preference table
var title = dialog.getPreference('table');
```

## GlideModal - render\(\)

Renders the UI page specified when the API was instantiated in the modal. You must call this method after you define the modal for it to appear in the UI.

Call this method when you use a UI page to generate the content in your modal. If you want to display HTML within a modal, call [GlideModal - renderWithContent\(String html\)](c_GlideModalV3API.md#) to render the modal.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

The following code example shows how to instantiate a GlideModal object using the UI pages `glide_confirm` and `glide_info`, set various preferences, and then display the appropriate modal in the UI \(render\).

```
var UpdateSetClient = Class.create({

  mergeConfirm: function () {
    var filterCriteriaMsg = "Please select filter criteria matching two or more update sets to merge";
    var messageMap = new GwtMessage().getMessages([filterCriteriaMsg, "Confirmation",
      "Are you sure you want to merge these {0} update sets? You will not be able to undo this action",
      "Invalid selection", "OK", "Cancel"]);
    var list = GlideList2.get('sys_update_set');
    var dialog;
    if (list.totalRows == 0 || list.totalRows == 1) {
      dialog = new GlideModal('glide_info', true, 300);
      dialog.setPreference('focusTrap', true);
      dialog.setTitle(messageMap["Invalid selection"]);
      dialog.setPreference('body', messageMap[filterCriteriaMsg]);
      dialog.setPreference('buttonLabel', messageMap["OK"]);
      dialog.render();
      return;
    }
    dialog = new GlideModal('glide_confirm', true, 300);
    dialog.setTitle(messageMap["Confirmation"]);
    dialog.setPreference('focusTrap', true);
    dialog.setPreference('body', new GwtMessage().format(
      messageMap["Are you sure you want to merge these {0} update sets? You will not be able to undo this action"],
      list.totalRows));
    dialog.setPreference('buttonLabelComplete', messageMap["OK"]);
    dialog.setPreference('onPromptComplete', this.merge);
    dialog.setPreference('buttonLabelCancel', messageMap["Cancel"]);
    dialog.setPreference('onPromptCancel', this.mergeExit);
    dialog.render();
  },

  merge: function () {
  var list = GlideList2.get('sys_update_set');
  var query = list.getQuery();
  var name = $('update_set_name').value;
  var comments = $('update_set_comments').value;

  var gurl = new GlideAjax('AngularProcessor','angular.do');
  gurl.addParam('sysparm_type', 'hub_client');
  gurl.addParam('type', 'merge_update_sets');
  gurl.addParam('name', name);
  gurl.addParam('comments', comments);
  gurl.addParam('query', query);
  gurl.getXML(function (response) {
      var data = response.responseText.evalJSON();
      var p = data.progress;
      if (p) {
        var progressId = p.progress_id;
        var map = new GwtMessage().getMessages(["Close", "Update Set Merge"]);
        var dialogClass = window.GlideModal ? GlideModal : GlideDialogWindow;
        var dd = new dialogClass("hierarchical_progress_viewer", false, "40em", "10.5em");
        dd.setPreference('focusTrap', true);
        dd.setTitle(map["Update Set Merge"]);
        dd.setPreference('sysparm_renderer_execution_id', progressId);
        dd.setPreference('sysparm_renderer_expanded_levels', '0'); // collapsed root node by default
        dd.setPreference('sysparm_button_close', map["Close"]);
        dd.render();
        //when all trackers are completed
        dd.on("executionComplete", function(trackerObj) {
          if (trackerObj.state == "2") {
            var redirectUrl = new GlideURL('sys_update_set_list.do');
            window.location.replace(redirectUrl.getURL());
            return;
          }
          var closeBtn = $("sysparm_button_close");
          if (closeBtn) {
            closeBtn.onclick = function() {
              dd.destroy();
            };
          }
        });
      }
    });
  },

  mergeExit: function () {
    // Do nothing interesting...
  }
});
```

## GlideModal - renderWithContent\(String html\)

Displays a modal with the specified string-based HTML content.

Use the renderWithContent\(\) method in lieu of the render\(\) method when deriving the modal content from HTML.

|Name|Type|Description|
|----|----|-----------|
|html|String|HTML content to display in the modal.|

|Type|Description|
|----|-----------|
|void| |

This code example shows how to display a modal that is constructed using the passed HTML string which contains a list of choices that the user can select from.

```
function cancelDialog(){

  var dialog = new GlideModal('cancelTask');
  //Sets the dialog title
  dialog.setTitle('Cancel Task');
  //Set up valid custom HTML to display
  dialog.renderWithContent('<div style="padding:15px"><p>What action do you want to take?</p>
    <p><select name="cancellation" id="taskCancellation" class="form-control">
    <option value="cancelOnly" role="option">Cancel this task but keep the requested item open</option>
    <option value="cancelAll" role="option">Cancel this and all other tasks, closing the requested item</option>
    </select></p><div style="padding:5px;float:right"><button style="padding:5px;margin-right:10px" 
    onclick="window.changeTaskAction(this.innerHTML,jQuery(\'#taskCancellation\').val())" 
    class="btn btn-default">Abort</button><button style="padding:5px" class="btn btn-primary" 
    onclick="window.changeTaskAction(this.innerHTML,jQuery(\'#taskCancellation\').val())">Cancel Task</button></div></div>');

  //Use the windows object to ensure the code is accessible from the modal dialog
  window.changeTaskAction = function(thisButton, thisAction){

    //Close the GlideModal dialog window
    dialog.destroy();

    //Submit to the back-end
    if(thisButton=='Cancel Task'){
      if(thisAction=="cancelAll"){
        g_form.setValue('state',4);//Closed Incomplete -- will close the Requested Item and all other open tasks
      }else{
        g_form.setValue('state',7);//Closed Skipped -- will only close this task
      }
         //Regular ServiceNow form submission
         gsftSubmit(null, g_form.getFormElement(), 'cancel_sc_task');
      }
   };
   return false;//Prevents the form from submitting when the dialog first load
}
```

## GlideModal - setPreference\(String name, String value\)

Sets the value of the specified preference \(property\). Use preferences to pass data into the page being rendered.

To retrieve preferences in a UI page, use the following function: RP.getWindowProperties\(\).get\('preference\_name'\). For additional information on preferences, see [GlideModal - Client](c_GlideModalV3API.md#).

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the preference whose value to set.|
|value|String|Value to store in the specified preference.|

|Type|Description|
|----|-----------|
|void| |

The following code example shows how to set the **table** preference to 'task' and the **name** preference to 'value'.

```
var dialog = new GlideModal('UI_dialog_name');

//Set the dialog title
dialog.setTitle('Show title'); 

//Set the desired preferences
dialog.setPreference('table', 'task'); 			
dialog.setPreference('name', 'value');        	

//Opens the dialog
dialog.render();
```

The following example shows how to set base preferences in a glide\_confirm modal.

```
var dialog = new GlideModal('glide_confirm', true, 300);
  dialog.setTitle('Example Title');
  dialog.setPreference('body', 'Example Body');
  dialog.setPreference('focusTrap', true);
  dialog.setPreference('callbackParam', 'exampleParameter');
  dialog.setPreference('buttonClassComplete', 'btn-primary');
  dialog.setPreference('onPromptComplete', function(param) {
    console.log('Prompt completed with param: ' + param);
  });

  dialog.setPreference('onPromptCancel', function(param) {
    console.log('Prompt cancelled with param: ' + param);
  });

dialog.render();
```

## GlideModal - setPreferenceAndReload\(Array properties\)

Sets the specified preferences and then reloads the modal.

|Name|Type|Description|
|----|----|-----------|
|properties|Array|Name-value pairs to set as preferences.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to create and render a modal and then update the `body` preference and reloading the modal.

```
var dialog = new GlideModal('glide_confirm');
dialog.setPreference('body', 'This is a test modal body');
dialog.setTitle('This is a test modal title');
dialog.render();

...

dialog.setPreferenceAndReload({'body': 'this is another body'})
```

## GlideModal - setTitle\(String title\)

Sets the title of the modal.

|Name|Type|Description|
|----|----|-----------|
|title|String|Text to display in the title of the modal.|

|Type|Description|
|----|-----------|
|void| |

The following code example shows how to set the modal title to "Table to update".

```
var dialog = new GlideModal('UI_dialog_name');

//Sets the dialog title
dialog.setTitle('Table to update'); 
dialog.setPreference('table', 'task'); 			      	
dialog.setWidth(550);

//Opens the dialog
dialog.render();
```

## GlideModal - setWidth\(Number/String width\)

Sets the width of the modal.

You can also set the width of a modal when you first instantiate the API using the [GlideModal - GlideModal\(String id, Boolean readOnly, Number/String width\)](c_GlideModalV3API.md#) method.

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

</td><td>

Width of the modal in pixels or the modal CSS class. If a pixel width is passed, it aligns the specified width with the corresponding CSS class.Possible modal CSS classes:

-   modal-alert: \(300 px\) Assigned when the specified width is 0 to 349 pixels.
-   modal-sm: \(400 px\) Assigned when the specified width is 350 to 449 pixels.
-   modal-md: \(600 px\) Assigned when the specified width is 450 to 649 pixels.
-   modal-lg: \(900 px\) Assigned when the specified width is 650 to 900 pixels.

Maximum width: 900 pixels

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following code example shows how to set the modal width to 550 pixels.

```
var dialog = new GlideModal('UI_dialog_name');

//Sets the dialog title
dialog.setTitle('Show title'); 
dialog.setPreference('name', 'value'); 			      	
dialog.setWidth(550);

//Opens the dialog
dialog.render();
```

## GlideModal - switchView\(String newView\)

Change the view and reload the modal.

|Name|Type|Description|
|----|----|-----------|
|newView|String|View to use.|

|Type|Description|
|----|-----------|
|void| |

