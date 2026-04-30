---
title: GlideListProperties - Global
description: The GlideListProperties API provides methods to create a list and set list properties. For example, you can define whether a list has a filter, breadcrumbs, and search.Instantiates a GlideListProperties object.Returns the unique ID for a list.Returns the name of the list.Get the title of a list.Returns whether or not the Actions on select rows option is enabled for a list.Returns whether or not a list has navigation at the bottom.Returns whether or not the page navigation controls appear in the footer of a list.Returns whether or not a list has a filter.Returns whether or not a list has a header.Returns whether or not a header context menu is enabled for a list.Returns whether list personalization is enabled for a list.Returns whether or not a list can have popup windows.Returns whether or not rows in a list have a context menu.Returns whether or not the search bar is enabled for a list.Returns whether or not the list title appears in the list header.Returns whether a context menu appears in a list header.Returns whether or not the page navigation controls appear in the header of a list.Returns whether or not the omit filter option has been selected.Returns whether the Save Filter button is hidden in the condition builder.Returns whether or not a list shows links.Returns whether or not toggling the header columns is available for a list.Determine whether the user can change the view for the list.Determine whether users can group items in a list.Determine whether the sort option is available in a list.Displays or hides all of the available context menus for a list.Determine whether the Actions on select rows options display at the bottom of a list.Determine whether the navigation actions at the bottom of a list are hidden or not.Determine whether or not breadcrumbs appear at the top of a list.Determine whether the first page, last page, next page, and previous page buttons appear at the bottom of the list.Determine whether or not the filter displays as part of a list.Determine whether or not a list displays a header.Determine whether or not the context menu appears next to each column in a list.Determine whether or not a list has the option for personalization.Determine whether the list has a popup or modal window.Determines whether or not list rows have a context menu.Determine whether search appears for a list.Determine whether the list title appears in the header.Determine whether or not a list has a context menu in the header.Determine whether or not a list has the page navigation controls in the list header.Determine whether rows are visible in a list.Set the unique ID for a list.Defines a name for the list.Determine whether the Save Filter button appears in the condition builder.Whether or not a list includes links.Defines the list title.Determine whether users can show or hide column headers for a table.Determine whether the first page, last page, next page, and previous page buttons appear at the top and bottom of the list.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 13
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideListProperties- Global

The GlideListProperties API provides methods to create a list and set list properties. For example, you can define whether a list has a filter, breadcrumbs, and search.

To use this class, you must first instantiate a GlideListProperties object using the constructor.

For an example of this class in the base system, configure a list and select **All**. The tabbed list of options uses the personalize\_all UI page and personalize\_all\_list UI macro to set list properties such as title, context menu, and breadcrumbs.

This API includes methods that provide information about existing GlideList settings and provides options for setting various GlideList properties. For information on how to modify settings in the UI, see [GlideList2 \(g\_list\) - Client](../../GlideList2/concept/c_GlideList2API.md#) or [GlideList \(Next Experience\) - Client](../../GlideListClientNowEx/concept/GlideListClientAPINEx.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideListProperties - GlideListProperties\(\)

Instantiates a GlideListProperties object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var list = new GlideListProperties();

```

## GlideListProperties - getListID\(\)

Returns the unique ID for a list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Unique ID for the list|

```
var list = new GlideListProperties();
var getID = list.getListID();
gs.print(getID);
```

Output: 3519f77ad95f5700964f387107a8a394

## GlideListProperties - getListName\(\)

Returns the name of the list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the list.|

```
var list = new GlideListProperties();
var setName = list.setListName("my custom list");
var getName = list.getListName();
gs.print(getName);
```

Output: my custom list

## GlideListProperties - getTitle\(\)

Get the title of a list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The title of the list.|

Optional example explanation

```
var list = new GlideListProperties();
var title = list.setTitle("My title");
var getTitle = list.getTitle();
gs.print(getTitle);
```

Output: My title

## GlideListProperties - hasActions\(\)

Returns whether or not the **Actions on select rows** option is enabled for a list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns **true** if the actions option is enabled for a list.|

```
var list = new GlideListProperties();
var actions = list.setHasActions(true);
var hasActions = list.hasActions();
gs.print(hasActions);
```

Output: true

## GlideListProperties - hasBottomNav\(\)

Returns whether or not a list has navigation at the bottom.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If returns **true** the list has bottom navigation.|

```
var lp = new GlideListProperties();
var Nav = lp.setHasBottomNav(true);
var hasNav = lp.hasBottomNav();
gs.print(hasNav);
```

Output: true

## GlideListProperties - hasBottomVCR\(\)

Returns whether or not the page navigation controls appear in the footer of a list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** the page navigation controls appear in the footer of a list.|

```
var list = new GlideListProperties();
var vcr = list.setHasBottomVCR(true);
var hasVCR = list.hasBottomVCR();
gs.print(hasVCR);
```

Output: true

## GlideListProperties - hasFilter\(\)

Returns whether or not a list has a filter.

The filter property is a parent of the breadcrumbs property. If the filter property is listed as false and the breadcrumb is listed as true, `hasFilter()` still returns true because the child property is marked as true.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** a filter icon appears with the list, or the breadcrumb property is listed as true. If **false** both the filter property and the breadcrumb property are marked as false.|

```
var list = new GlideListProperties();
var filter = list.setHasFilter(true);
var breadcrumbs = list.setHasBreadcrumbs(true);
var hasFilter = list.hasFilter();
gs.print(hasFilter);

```

Output: true

## GlideListProperties - hasHeader\(\)

Returns whether or not a list has a header.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns **true** if a list has a header.|

```
var list = new GlideListProperties();
var header = list.setHasHeader(true);
var hasHeader = list.hasHeader();
gs.print(hasHeader);
```

Output: true

## GlideListProperties - hasHeaderContextMenu\(\)

Returns whether or not a header context menu is enabled for a list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** a context menu displays next to each column header in a list.|

```
var list = new GlideListProperties();
var header = list.setHasHeaderContextMenu(true);
var hasHeader = list.hasHeaderContextMenu();
gs.print(hasHeader);
```

Output: true

## GlideListProperties - hasListMechanic\(\)

Returns whether list personalization is enabled for a list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** the list mechanic is enabled for a list and the Personalize List icon appears on the page.|

```
var list = new GlideListProperties();
var mechanic = list.setHasListMechanic(true);
var hasMechanic = list.hasListMechanic();
gs.print(hasMechanic);
```

Output: true

## GlideListProperties - hasPopup\(\)

Returns whether or not a list can have popup windows.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns **true** if the list allows popups.|

```
var list = new GlideListProperties();
var popup = list.setHasPopup(true);
var hasPopup = list.hasPopup();
gs.print(hasPopup);
```

Output: true

## GlideListProperties - hasRowContextMenu\(\)

Returns whether or not rows in a list have a context menu.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** a list row can have a context menu.|

```
var list = new GlideListProperties();
var contextMenu = list.setHasRowContextMenu(true);
var hasContextMenu = list.hasRowContextMenu();
gs.print(hasContextMenu);
```

Output: true

## GlideListProperties - hasSearch\(\)

Returns whether or not the search bar is enabled for a list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** the search bar appears in the header of a list.|

```
var list = new GlideListProperties();
var search = list.setHasSearch(true);
var hasSearch = list.hasSearch();
gs.print(hasSearch);
```

Output: true

## GlideListProperties - hasTitle\(\)

Returns whether or not the list title appears in the list header.

The title context menu is a child property of title. If `setHasTitleContextMenu` is set to true, `hasTitle` also returns true, even if `setHasTitle` is set to false.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** the list title appears in the list header.|

```
var list = new GlideListProperties();
var title = list.setHasTitle(true);
var contextMenu = list.setHasTitleContextMenu(true);
var hasTitle = list.hasTitle();
gs.print(hasTitle);

```

Output: true

## GlideListProperties - hasTitleContextMenu\(\)

Returns whether a context menu appears in a list header.

The title context menu is a child property of title. If `setHasTitleContextMenu` is set to true, `hasTitle` also returns true, even if `setHasTitle` is set to false.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** the context menu appears in the list header next to the list title.|

Optional example explanation

```
var list = new GlideListProperties();
var contextMenu = list.setHasTitleContextMenu(true);
var hasContextMenu = list.hasTitleContextMenu();
gs.print(hasContextMenu);

```

Output: true

## GlideListProperties - hasTopVCR\(\)

Returns whether or not the page navigation controls appear in the header of a list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** the page navigation controls appear in the header of a list.|

```
var list = new GlideListProperties();
var vcr = list.setHasTopVCR(true);
var hasVCR = list.hasTopVCR();
gs.print(hasVCR);
```

Output: true

## GlideListProperties - isOmitFilter\(\)

Returns whether or not the omit filter option has been selected.

The ListControl omit flags take precedence in that if they are set, they negate the setting of their corresponding flag. For example, if the show filter flag has been set to true, but the ListControl omit filter is true, then checking hasFilter returns `false`.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true or false whether the omit filter flag has been selected.|

```
var lp = new GlideListProperties();
var omitFilter = lp.isOmitFilter();
gs.print(omitFilter);
```

Output: false

## GlideListProperties - isSaveFilterHidden\(\)

Returns whether the Save Filter button is hidden in the condition builder.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** the Save Filter button is hidden in the condition builder.|

```
var list = new GlideListProperties();
var SaveFilter = list.setSaveFilterHidden(true);
var hasSaveFilter = list.isSaveFilterHidden();
gs.print(hasSaveFilter);
```

Output: true

## GlideListProperties - isShowLinks\(\)

Returns whether or not a list shows links.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var links = list.setShowLinks(true);
var hasLinks = list.isShowLinks();
gs.print(hasLinks);
```

Output: true

## GlideListProperties - isToggleHeader\(\)

Returns whether or not toggling the header columns is available for a list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|If **true** users can show or hide the column headers for a table.|

```
var list = new GlideListProperties();
var toggle = list.setToggleHeader(true);
var hasToggle = list.isToggleHeader();
gs.print(hasToggle);
```

Output: true

## GlideListProperties - setCanChangeView\(Boolean onOff\)

Determine whether the user can change the view for the list.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **false** users cannot change the list view. By default, changing views is enabled.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var changeView = list.setCanChangeView(true);
```

## GlideListProperties - setCanGroup\(Boolean onOff\)

Determine whether users can group items in a list.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **false**, the group by option does not appear in the column context menu. By default the group by option appears in the list context menu.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var canGroup = list.setCanGroup(true);
```

## GlideListProperties - setCanSort\(Boolean onOff\)

Determine whether the sort option is available in a list.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **false**, the sort option does not appear in column list context menu, and users cannot click the column title to change the order of the list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var canSort = list.setCanSort(true);
```

## GlideListProperties - setContextMenus\(Boolean onOff\)

Displays or hides all of the available context menus for a list.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If set to **true** displays the title context menu, header context menu, and list context menu for a list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var context = list.setContextMenus(true);
```

## GlideListProperties - setHasActions\(Boolean\)

Determine whether the **Actions on select rows** options display at the bottom of a list.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** displays action options for a list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var actions = list.setHasActions(true);
```

## GlideListProperties - setHasBottomNav\(Boolean onOff\)

Determine whether the navigation actions at the bottom of a list are hidden or not.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|When **true** adds navigation to the bottom of a list.|

|Type|Description|
|----|-----------|
|void| |

```
var lp = new GlideListProperties();
var bottom = lp.setHasBottomNav(true);
```

## GlideListProperties - setHasBreadcrumbs\(Boolean onOff\)

Determine whether or not breadcrumbs appear at the top of a list.

Breadcrumbs are a child of filters. To hide breadcrumbs completely, you need to also set the filter to false.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** breadcrumbs appear at the top of a list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var breadcrumbs = list.setHasBreadcrumbs(true);
```

## GlideListProperties - setHasBottomVCR\(Boolean onOff\)

Determine whether the first page, last page, next page, and previous page buttons appear at the bottom of the list.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true**, the first page, last page, next page, and previous page buttons appear at the bottom of the list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var bottomVCR = list.setHasBottomVCR(true);
```

## GlideListProperties - setHasFilter\(Boolean onOff\)

Determine whether or not the filter displays as part of a list.

The filter is a parent of breadcrumbs. To remove the filter, you need to set both the filter and the breadcrumbs to false.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** a filter icon appears at the top of the list. Users can use the filter to narrow search results.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var filter = list.setHasFilter(true);
```

## GlideListProperties - setHasHeader\(Boolean onOff\)

Determine whether or not a list displays a header.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** the list displays a header.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var header = list.setHasHeader(true);
```

## GlideListProperties - setHasHeaderContextMenu\(Boolean onOff\)

Determine whether or not the context menu appears next to each column in a list.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** the context menu appears next to each column in a list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var actions = list.setHasHeaderContextMenu(true);
```

## GlideListProperties - setHasListMechanic\(Boolean onOff\)

Determine whether or not a list has the option for personalization.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** the list mechanic is enabled and the Personalize List icon appears on the page.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var mechanic = list.setHasListMechanic(true);
```

## GlideListProperties - setHasPopup\(Boolean onOff\)

Determine whether the list has a popup or modal window.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true**the list can have popup windows.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var popup = list.setHasPopup(true);
```

## GlideListProperties - setHasRowContextMenu\(Boolean onOff\)

Determines whether or not list rows have a context menu.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|When **true** list rows can have a context menu.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var contextMenu = list.setHasRowContextMenu(true);
```

## GlideListProperties - setHasSearch\(Boolean onOff\)

Determine whether search appears for a list.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** the search bar appears in the list header.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var search = list.setHasSearch(true);
```

## GlideListProperties - setHasTitle\(Boolean onOff\)

Determine whether the list title appears in the header.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** the title of the list appears in the list header.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var title = list.setHasTitle(true);

```

## GlideListProperties - setHasTitleContextMenu\(Boolean onOff\)

Determine whether or not a list has a context menu in the header.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** the context menu appears next to the list title in the header|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var contextMenu = list.setHasTitleContextMenu(true);
```

## GlideListProperties - setHasTopVCR\(Boolean onOff\)

Determine whether or not a list has the page navigation controls in the list header.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** the page navigation controls appear in the header of a list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var vcr = list.setHasTopVCR(true);
```

## GlideListProperties - setHideRows\(Boolean onOff\)

Determine whether rows are visible in a list.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** all of the rows are hidden for a list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var hideRows = list.setHideRows(true);
```

## GlideListProperties - setListID\(String ID\)

Set the unique ID for a list.

|Name|Type|Description|
|----|----|-----------|
|Unique ID|String|The unique ID for the list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var setID = list.setListID("a9dd1483d99f5700964f387107a8a3ec");
var getID = list.getListID();
gs.print(getID);
```

Output: a9dd1483d99f5700964f387107a8a3ec

## GlideListProperties - setListName\(String name\)

Defines a name for the list.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var name = list.setListName("my custom list");

```

## GlideListProperties - setSaveFilterHidden\(Boolean onOff\)

Determine whether the Save Filter button appears in the condition builder.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** the Save Filter button is hidden.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var saveFilter = list.setSaveFilterHidden(true);
```

## GlideListProperties - setShowLinks\(Boolean onOff\)

Whether or not a list includes links.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** list includes related links.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var links = list.setShowLinks(true);
```

## GlideListProperties - setTitle\(String title\)

Defines the list title.

|Name|Type|Description|
|----|----|-----------|
|title|String|Title for the list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var title = list.setTitle("My title");
```

## GlideListProperties - setToggleHeader\(Boolean onOff\)

Determine whether users can show or hide column headers for a table.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **true** an icon appears in the header that allows users to show or hide the column headers.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var toggle = list.setToggleHeader(true);

```

## GlideListProperties - setVCR\(Boolean onOff\)

Determine whether the first page, last page, next page, and previous page buttons appear at the top and bottom of the list.

|Name|Type|Description|
|----|----|-----------|
|onOff|Boolean|If **false**, the list does not have any of the page navigation buttons for a list.|

|Type|Description|
|----|-----------|
|void| |

```
var list = new GlideListProperties();
var VCR = list.setVCR(true);
```

