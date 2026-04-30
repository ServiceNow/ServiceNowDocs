---
title: GlideMenu \(g\_menu and g\_item\) - Client
description: The GlideMenu API provides methods that can be used in UI context menus and in onShow scripts to customize UI context menu items.Clears the image for an item.Clears any selection images from items in the menu.Returns a menu item by item ID.Disables a menu item so that it cannot be selected. The disabled menu item is displayed in a lighter color \(grayed out\) to indicate it is disabled.Enables the specified menu item.Hides the specified menu item.Sets an image for an item.Sets the display label for a menu item. The label may contain HTML.Displays the specified item.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideMenu \(g\_menu and g\_item\)- Client

The GlideMenu API provides methods that can be used in UI context menus and in `onShow` scripts to customize UI context menu items.

There is no constructor for the GlideMenu class. Access GlideMenu methods using the `g_menu` global object.

-   `g_menu` is the UI context menu that is about to be shown. The `onShow` script can make changes to the appearance of the menu before it is displayed using these methods.
-   `g_item` is the current UI context menu item that is about to be shown. It is used in several of the g\_menu methods to specify an item.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideMenu - clearImage\(GlideMenuItem item\)

Clears the image for an item.

|Name|Type|Description|
|----|----|-----------|
|item|GlideMenuItem|Specifies the item to have its image removed from display.|

|Type|Description|
|----|-----------|
|void| |

```
g_menu.clearImage(g_item);
```

## GlideMenu - clearSelected\(\)

Clears any selection images from items in the menu.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## GlideMenu - getItem\(String itemID\)

Returns a menu item by item ID.

It can be necessary to find an item in a menu so that it can be changed before being displayed. Each menu item may be assigned a unique ID when the menu item is created \(either from a UI Context Menu entry or from the addAction\(\) method in the Dynamic Script Action\).

|Name|Type|Description|
|----|----|-----------|
|itemID|String|Specifies the item to be returned.|

|Type|Description|
|----|-----------|
|GlideMenuItem|The menu item|

## GlideMenu - setDisabled\(GlideMenuItem item\)

Disables a menu item so that it cannot be selected. The disabled menu item is displayed in a lighter color \(grayed out\) to indicate it is disabled.

|Name|Type|Description|
|----|----|-----------|
|item|GlideMenuItem|The item to be disabled.|

|Type|Description|
|----|-----------|
|void| |

```
g_menu.setDisabled(g_item);
```

## GlideMenu - setEnabled\(GlideMenuItem item\)

Enables the specified menu item.

|Name|Type|Description|
|----|----|-----------|
|item|GlideMenuItem|The item to be enabled.|

|Type|Description|
|----|-----------|
|void| |

```
g_menu.setEnabled(g_item);
```

## GlideMenu - setHidden\(GlideMenuItem item\)

Hides the specified menu item.

When hiding menu items, the separator bars are not adjusted, so it is possible to end up with the menu showing two separators in a row.

|Name|Type|Description|
|----|----|-----------|
|item|GlideMenuItem|The item to be hidden.|

|Type|Description|
|----|-----------|
|void| |

```
g_menu.setHidden(g_item);
```

## GlideMenu - setImage\(GlideMenuItem item, String imgSrc\)

Sets an image for an item.

|Name|Type|Description|
|----|----|-----------|
|item|GlideMenuItem|the item to have the image displayed.|
|imgSrc|String|the image to attach to the menu item.|

|Type|Description|
|----|-----------|
|void| |

```
g_menu.setImage(g_item, 'images/checked.gifx');
```

## GlideMenu - setLabel\(GlideMenuItem item, String label\)

Sets the display label for a menu item. The label may contain HTML.

|Name|Type|Description|
|----|----|-----------|
|item|GlideMenuItem|the item to be labeled.|
|label|String|the label to be displayed. The string may contain HTML.|

|Type|Description|
|----|-----------|
|void| |

```
g_menu.setLabel(g_item, "This is a new label");
```

## GlideMenu - setVisible\(GlideMenuItem item\)

Displays the specified item.

|Name|Type|Description|
|----|----|-----------|
|item|GlideMenuItem|The item to be displayed.|

|Type|Description|
|----|-----------|
|void| |

```
g_menu.setVisible(g_item);
```

