---
title: GlideDialogWindow - Client \(deprecated\)
description: The GlideDialogWindow API provides methods for displaying a dialog in the current window and frame.Provides methods for displaying a dialog in the current window and frame.Adjusts the body height of a dialog window to be the window height minus the header height.Closes the dialog window.Renders the dialog window.Sets a given window property to a specified value.Sets the size of the dialog window.Sets the title of the dialog window.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideDialogWindow- Client \(deprecated\)

The GlideDialogWindow API provides methods for displaying a dialog in the current window and frame.

Use these methods in scripts anywhere that you can use a client-side JavaScript. These methods are most often called from a UI action with the **Client** check box selected.

**Note:** This API has been deprecated, use the [GlideModal](../../GlideModalClientSideV3/concept/c_GlideModalV3API.md#) API instead.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideDialogWindow - GlideDialogWindow\(String id, Boolean readOnly, Number width, Number height\)

Provides methods for displaying a dialog in the current window and frame.

Use these methods in scripts anywhere that you can use a client-side JavaScript. These methods are most often called from a UI Action with the **Client** check box selected.

|Name|Type|Description|
|----|----|-----------|
|id|String|Name of the UI page to load into the dialog window.|
|readOnly|Boolean|Optional. Flag that indicates whether the dialog window is read only \(true\) or read/write \(false\). Default: false|
|width|Number|Optional. Size \(in pixels\) to set the width of the dialog window.|
|height|Number|Optional. Size \(in pixels\) to set the height of the dialog window.|

|Type|Description|
|----|-----------|
|void| |

```
// Creates a dialog window
var gdw = new GlideDialogWindow('show_list');

// Creates a read-only dialog window
var gdw = new GlideDialogWindow('show_list', true);

// Creates a dialog window that is 400 pixels wide
var gdw = new GlideDialogWindow('show_list', false, 400); 

// Creates a dialog window that is 400 pixels wide and 200 pixels tall
var gdw = new GlideDialogWindow('show_list', false, 400, 200); 
```

## GlideDialogWindow - adjustBodySize\(\)

Adjusts the body height of a dialog window to be the window height minus the header height.

You typically call this method after calling GlideDialogWindow - setSize\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var gdw = new GlideDialogWindow('show_list');
      gdw.setTitle('Test');
      gdw.setSize(750,300);
      gdw.adjustBodySize();
      gdw.render();
```

## GlideDialogWindow - destroy\(\)

Closes the dialog window.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
//Destroy the current dialog window.
      GlideDialogWindow.get().destroy();
```

## GlideDialogWindow - render\(\)

Renders the dialog window.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var gdw = new GlideDialogWindow('show_list');
      gdw.setTitle('Test');
      gdw.setSize(750,300);
      gdw.setPreference('table', 'u_test_list');
      gdw.setPreference('title', 'A New Title');
      gdw.render();
```

## GlideDialogWindow - setPreference\(String name, String value\)

Sets a given window property to a specified value.

Any window property can be set using this method.

|Name|Type|Description|
|----|----|-----------|
|name|String|The window property to set.|
|value|String|The value for the window property.|

|Type|Description|
|----|-----------|
|void| |

```
var gdw = new GlideDialogWindow('show_list');
      gdw.setTitle('Test');
      gdw.setSize(750,300);
      gdw.setPreference('table', 'u_test_list');
      gdw.setPreference('title', 'A New Title');
```

## GlideDialogWindow - setSize\(Number width, Number height\)

Sets the size of the dialog window.

If you do not pass width and height parameters, a default size is used.

|Name|Type|Description|
|----|----|-----------|
|width|Number|The width of the dialog window.|
|height|Number|The height of the dialog window.|

|Type|Description|
|----|-----------|
|void| |

```
var gdw = new GlideDialogWindow('show_list');
      gdw.setSize(750,300);
```

## GlideDialogWindow - setTitle\(String title\)

Sets the title of the dialog window.

|Name|Type|Description|
|----|----|-----------|
|title|String|The title for the current window.|

|Type|Description|
|----|-----------|
|void| |

```
//var gdw = new GlideDialogWindow('show_list');
      gdw.setTitle('test');
```

