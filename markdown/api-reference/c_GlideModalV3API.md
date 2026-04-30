---
title: GlideModal - Client
description: The GlideModal API provides methods for displaying a content overlay.Creates an instance of the GlideModalV3 class.Get a GlideModal object by ID.Returns the value of the specified preference \(property\).Renders the UI page in the modal.Display a modal with the specified HTML content.Sets the specified field on the current form to the specified value.Set the properties and reload the modal.Sets the title of the modal.Sets the width of the modal in pixels.Change the view and reload the modal.
locale: en-US
release: xanadu
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideModal- Client

The GlideModal API provides methods for displaying a content overlay.

Use these methods in scripts anywhere that you can use client-side JavaScript. These methods are most often called from a UI action with the **Client** check box selected.

This is a fully-featured replacement for the GlideWindow and GlideDialogWindow APIs.

![Example overlay](../../Images/GlideModalV3-Client-example-overlay-dialog.png "Example overlay")

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideModal - GlideModal\(String id, Boolean readOnly, Number width\)

Creates an instance of the GlideModalV3 class.

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

UI page to load into the modal.

</td></tr><tr><td>

readOnly

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide the close button in the modal.Valid values:

-   true: Don't display the close button in the modal.
-   false: Display the close button in the modal.

Default: false

</td></tr><tr><td>

width

</td><td>

Number

</td><td>

Width of modal in pixels. Default:

Maximum width: 900 pixels

**Note:** You can also set the modal width using the [GlideModal - setWidth\(Number width\)](c_GlideModalV3API.md#) method.

</td></tr></tbody>
</table>## GlideModal - get\(String id\)

Get a GlideModal object by ID.

|Name|Type|Description|
|----|----|-----------|
|id|String|The element id of the GlideModal object.|

|Type|Description|
|----|-----------|
|GlideModal|The object.|

## GlideModal - getPreference\(String name\)

Returns the value of the specified preference \(property\).

Invoking actions that create the modal typically also create the necessary preferences for the modal using the [GlideModal - setPreference\(String name, String value\)](c_GlideModalV3API.md#) method. The UI page client script then consumes these preferences using this method.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the preference value to retrieve. This value must have previously been set on the modal using the [GlideModal - setPreference\(String name, String value\)](c_GlideModalV3API.md#) method.|

|Type|Description|
|----|-----------|
|String|Specified preference's value.|

This example shows a simple case of setting a preference and then retrieving that preference from a specified modal.

```
var gm = new GlideModal('UI_dialog_name');
//Sets the dialog title
gm.setTitle('Show title');

//sets the value of the preference table
gm.setPreference('table', 'incident');

//gets the value of the preference table
var title = gm.getPreference('table');
```

## GlideModal - render\(\)

Renders the UI page in the modal.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var gm = new GlideModal("UI_dialog_name");

//Sets the dialog title
gm.setTitle('Show title');		      	
gm.setWidth(550);

//Opens the dialog
gm.render();
```

## GlideModal - renderWithContent\(String html\)

Display a modal with the specified HTML content.

The renderWithContent\(\) method replaces the render\(\) method, and does not request a UI page to render.

|Name|Type|Description|
|----|----|-----------|
|html|String|The HTML content to be shown in the modal.|

|Type|Description|
|----|-----------|
|void| |

## GlideModal - setPreference\(String name, String value\)

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

</td><td>

Name of the form field to update. If this field does not exist on the current form, the request is ignored.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Value to store in the specified form field.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var gm = new GlideModal('UI_dialog_name');
//Sets the dialog title
gm.setTitle('Show title'); 
gm.setPreference('table', 'task'); 			
gm.setPreference('name', 'value');        	

//Opens the dialog
gm.render();
```

## GlideModal - setPreferenceAndReload\(Array properties\)

Set the properties and reload the modal.

|Name|Type|Description|
|----|----|-----------|
|properties|Array|An array of name-value pairs to be set.|

|Type|Description|
|----|-----------|
|void| |

## GlideModal - setTitle\(String title\)

Sets the title of the modal.

|Name|Type|Description|
|----|----|-----------|
|title|String|Title to be displayed|

|Type|Description|
|----|-----------|
|void| |

```
var dialog = new GlideModal('UI_dialog_name');

//Sets the dialog title
dialog.setTitle('Show title');
dialog.setPreference('name', 'value');
 			      	        
//Opens the dialogdialog.render(); 

```

## GlideModal - setWidth\(Number width\)

Sets the width of the modal in pixels.

You can also set the width of a modal when you first instantiate it using the [GlideModal - GlideModal\(String id, Boolean readOnly, Number width\)](c_GlideModalV3API.md#) method.

<table id="table_msx_wts_3v" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

width

</td><td>

Number

</td><td>

Number of pixels to set as the width of the modal.Maximum: 900 pixels

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

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
|newView|String|The view to use.|

|Type|Description|
|----|-----------|
|void| |

