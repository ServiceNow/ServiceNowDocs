---
title: GlideList2 \(g\_list\) - Client
description: The GlideList2 API provides methods to customize \(v2\) lists.Adds a single term to the list query filter.Returns the GlideList2 object for the list that contains the specified item.Returns the GlideList2 object for the list specified.Returns a comma-separated list of the sys\_ids for the items that are checked in the associated list.Returns the fixed query. Returns the field or comma-separated list of fields that are used to group the list.Returns the name of the list, which is usually the table name.Returns the first field used to order the list.Returns the name of the parent table for a related list \(the table associated with the form\).Returns the encoded query string for the list.Returns the related list field that associates the related list to the parent form.Returns the table name for the list.Returns the view used to display the list.Returns the list title.Returns true if the list has been personalized by the user by choosing the list mechanic and changing the list layout.Refreshes the list. The orderBy part of the list filter is ignored so that the list uses its natural ordering when it is refreshed.Refreshes the list. The orderBy part of the list filter is included if it is specified for the list.Sets the encoded query string for the list, ignoring the orderBy and groupBy parts of the query string.Sets the encoded query string for the list, including the orderBy and groupBy if specified, and then refreshes the list using the new filter.Sets the first row that appears in the list when the list is refreshed.Sets the list groupBy criteria for a single field.Sets the orderBy criteria for the list.Sets the number of rows per page to display.Shows or hides all the groups within the list and saves the current collapsed/expanded state of the groups as a user preference.Displays or hides the list and saves the current collapsed/expanded state of the list as a user preference.Sorts the list in ascending order and sets the field as an orderBy column.Sorts a single field in the list in descending order and sets the field as an orderByDescField column.Toggles the display of the list and saves the current collapsed/expanded state of the list as a user preference.Toggles the display of the list but does not save the current collapsed/expanded state of the list as a user preference.
locale: en-US
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideList2 \(g\_list\)- Client

The GlideList2 API provides methods to customize \(v2\) lists.

The variable `g_list` is used to access a specified list object. The `g_list` variable is not available to the related lists form link UI action. It is available to the lists form link UI action.

These methods are used in UI context menus and UI actions.

Several of these methods are available in Next Experience UI Framework. For details, see [GlideList \(Next Experience UI Framework\)](../../GlideListClientNowEx/concept/GlideListClientAPINEx.md#).

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideList2 - addFilter\(String filter\)

Adds a single term to the list query filter.

|Name|Type|Description|
|----|----|-----------|
|filter|String|Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).|

|Type|Description|
|----|-----------|
|void| |

```
g_list.addFilter("active=true");
```

## GlideList2 - get\(Object DOMelement\)

Returns the GlideList2 object for the list that contains the specified item.

|Name|Type|Description|
|----|----|-----------|
|DOMelement|Object|The DOM element ID for the list for which you want the GlideList2 object.|

|Type|Description|
|----|-----------|
|Object|The GlideList2 object or null if not found.|

## GlideList2 - get\(String ListID\)

Returns the GlideList2 object for the list specified.

|Name|Type|Description|
|----|----|-----------|
|ListID|String|The list ID for which you want the GlideList2 object.|

|Type|Description|
|----|-----------|
|Object|The GlideList2 object or null if not found.|

```
function assignLabelActionViaLookupModal(tableName, listId) {
	var list = GlideList2.get(listId);
	if (!list)
		return;

	assignLabelViaLookup(tableName, sysIds, list.getView());
}
```

## GlideList2 - getChecked\(\)

Returns a comma-separated list of the sys\_ids for the items that are checked in the associated list.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|Comma-separated list of the sys\_ids for the items that are checked in the list. Does not check to determine that the items returned are allowed to be executed.|

```
function removeLabelActionViaLookupModal(tableName, listId) {
  var list = GlideList2.get(listId);
  if (!list)
    return;

  var sysIds = list.getChecked();
  if (!sysIds)
    return;

  removeLabelViaLookup(tableName, sysIds);
}
```

## GlideList2 - getFixedQuery\(\)

Returns the fixed query.

A fixed query is the part of the query that cannot be removed from the breadcrumb \(i.e., it is fixed for the user\). It is specified by including a **sysparm\_fixed\_query** parameter for the application module.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The fixed query string for the list.|

```
var list = GlideList2.get(container.readAttribute('list_id'));
var filter = this._getFilter(element);
var fixedQuery = list.getFixedQuery();
if (fixedQuery)
  filter = fixedQuery + "^" + filter;
```

## GlideList2 - getGroupBy\(\)

Returns the field or comma-separated list of fields that are used to group the list.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The field or comma-separated list of fields that are used to group the list.|

```
function runFilterV2Lists(name, filter) {
  var list = GlideList2.get(name);	
    if (list) {
      var groupBy = list.getGroupBy();
      if (groupBy)  
        filter += "^" + groupBy;
		
        list.setFilterAndRefresh(filter);
    }
}
```

## GlideList2 - getListName\(\)

Returns the name of the list, which is usually the table name.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The list name \(usually the table name\).|

```
var list = GlideList2.get(name);	
var listName = list.getListName();

```

## GlideList2 - getOrderBy\(\)

Returns the first field used to order the list.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The field by which to order the list. Empty if the list is not ordered.|

```
var list = GlideList2.get(listId);
if (!list)
  return;
var orderBy = list.getOrderBy();
```

## GlideList2 - getParentTable\(\)

Returns the name of the parent table for a related list \(the table associated with the form\).

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The parent table name.|

```
for (var id in GlideLists2) {
  var list = GlideLists2[id];
  if (list.getTableName() == listTableName && list.getParentTable() == tableName)
    return list.getContainer();
}

```

## GlideList2 - getQuery\(Boolean orderBy, Boolean groupBy, Boolean fixed, Boolean all\)

Returns the encoded query string for the list.

<table id="table_us2_nww_15" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

orderBy

</td><td>

Boolean

</td><td id="gList_parmDesc_orderByB">

Optional. Flag that indicates whether to include orderBy in results.Valid values:

-   true: Include orderBy in results.
-   false: Do not include orderBy in results.

 Default: false

</td></tr><tr><td>

groupBy

</td><td>

Boolean

</td><td id="gList_parmDesc_groupByB">

Optional. Flag that indicates whether to include groupBy in results.Valid values:

-   true: Include groupBy in results.
-   false: Do not include groupBy in results.

 Default: false

</td></tr><tr><td>

fixed

</td><td>

Boolean

</td><td id="gList_parmDesc_fixed">

Optional. Flag that indicates whether to include fixed query in results.Valid values:

-   true: Include fixed query in results.
-   false: Do not include fixed query in results.

 Default: false

</td></tr><tr><td>

all

</td><td>

Boolean

</td><td id="gList_parmDesc_all">

Default. Flag that indicates whether to include orderBy, groupBy, and fixed query in results.Valid values:

-   true: Include orderBy, groupBy, and fixed query in results.
-   false: Do not include all three options in results.

 Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Encoded query string for the list.|

```
var list = GlideList2.get(this.listID);
var ajax = new GlideAjax("AJAXJellyRunner", "AJAXJellyRunner.do");
  ajax.addParam("sysparm_query_encoded", list.getQuery({groupby: true, orderby: true}));
  ajax.addParam("sysparm_table", list.getTableName());
  ajax.addParam("sysparm_view", list.getView());
```

## GlideList2 - getRelated\(\)

Returns the related list field that associates the related list to the parent form.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|Field that connects the list to the parent form.|

```
var list = GlideList2.get(name);
var related = list.getRelated();
if (related) 
  ajax.addParam("sysparm_is_related_list", "true");
```

## GlideList2 - getTableName\(\)

Returns the table name for the list.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|Returns the table name for the list.|

```
GlideList2.getListsForTable = function(table) {
    var lists = [];
    for (var id in GlideLists2) {
        var list = GlideLists2[id];
        if (list.getTableName() == table)
            lists.push(list);
    }
    return lists;
}
```

## GlideList2 - getView\(\)

Returns the view used to display the list.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The name of the view.|

```
function assignLabelActionViaLookupModal(tableName, listId) {
	var list = GlideList2.get(listId);
	if (!list)
		return;

	assignLabelViaLookup(tableName, sysIds, list.getView());
}
```

## GlideList2 - getTitle\(\)

Returns the list title.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The list title.|

```
var list = GlideList2.get(name);	
var listTitle = list.getTitle();

```

## GlideList2 - isUserList\(\)

Returns **true** if the list has been personalized by the user by choosing the list mechanic and changing the list layout.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|Boolean|True if the list layout has been changed.|

```
var list = GlideList2.get(listId);
if (!list)
  return;
if (list.isUserList())
  var tableName = list.getTableName();
```

## GlideList2 - refresh\(Number firstRow, String additionalParms\)

Refreshes the list. The **orderBy** part of the list filter is ignored so that the list uses its natural ordering when it is refreshed.

<table id="table_plc_vmx_15" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

firstRow

</td><td>

Number

</td><td id="gList_parmDesc_firstRowN">

The first row to appear in the list.Default: First row of the current view.

</td></tr><tr><td>

additionalParms

</td><td>

String

</td><td id="gList_parmDesc_addtl">

Optional name-value pairs that are submitted with the list refresh request.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
$timeout(function() {
  if (GlideList.lists) {
    var list = GlideList.get(name);
    if (list) {
       if (sortBy) {
         if (sortDirection == 'ASC')
            list.sort(sortBy);
         else
            list.sortDescending(sortBy);
         }  
       list.refresh();
     }
   }
}			
```

## GlideList2 - refreshWithOrderBy\(Number firstRow, String description\)

Refreshes the list. The **orderBy** part of the list filter is included if it is specified for the list.

<table id="table_rlc_vmx_15" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

firstRow

</td><td>

Number

</td><td id="gList_parmDesc_firstRowN">

The first row to appear in the list.Default: First row of the current view.

</td></tr><tr><td>

description

</td><td>

String

</td><td id="gList_parmDesc_description">

Optional name-value pairs that are submitted with the list refresh request.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
ga.getXML(function(serverResponse) {
  var response = serverResponse.responseXML.getElementsByTagName("response")[0];
  if (response) {
    var list = GlideList2.getByName("backlog_stories");
    list.refreshWithOrderBy();
    var status = response.getAttribute('status');
    $j('html, body').animate({scrollTop: $j("#"+data.record.sys_id).offset().top},500);
    if (status == 'failure') {
      alert('${gs.getMessage("Story cannot be created. Team is not associated with any project.")}');
    }
  }
}
```

## GlideList2 - setFilter\(String filter\)

Sets the encoded query string for the list, ignoring the **orderBy** and **groupBy** parts of the query string.

|Name|Type|Description|
|----|----|-----------|
|filter|String|Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).|

|Type|Description|
|----|-----------|
|void| |

```
list = GlideList2.get($(side+"ContentDivRelease").select(".list_div")[0].getAttribute("id"));
if (list) {
  list.setFilter("active=true");
  list.refresh(1);
 }
```

## GlideList2 - setFilterAndRefresh\(String filter\)

Sets the encoded query string for the list, including the **orderBy** and **groupBy** if specified, and then refreshes the list using the new filter.

|Name|Type|Description|
|----|----|-----------|
|filter|String|Encoded query string.|

|Type|Description|
|----|-----------|
|void| |

```
function updateListFilter(projectID) {
  var list = GlideList2.getByName("backlog_stories");
  var fixedQuery = $('hdn_additional_filters').value;
  if(!projectID) {
      list.setFilterAndRefresh(fixedQuery + "^ORDERBYteam_index");
      list.setOrderBy("team_index");
  }
}
```

## GlideList2 - setFirstRow\(Number rowNum\)

Sets the first row that appears in the list when the list is refreshed.

|Name|Type|Description|
|----|----|-----------|
|rowNum|Number|Row number of the first row to display.|

|Type|Description|
|----|-----------|
|void| |

```
var nextRow = 0;
var rowsPerPage = 20;
var list = GlideList2.get(listId);
if (!list)
  return;
list.setFirstRow(nextRow);
nextRow = nextRow + rowsPerPage;

```

## GlideList2 - setGroupBy\(String groupBy\)

Sets the list **groupBy** criteria for a single field.

|Name|Type|Description|
|----|----|-----------|
|groupBy|String|The **groupBy** criteria for the list.|

|Type|Description|
|----|-----------|
|void| |

```
function runContextAction(listId) {
  var g_list = GlideList2.get(listId);
  g_list.setGroupBy('');
  g_list.refresh(1);
}
```

## GlideList2 - setOrderBy\(String orderBy\)

Sets the **orderBy** criteria for the list.

For a single order by field, use **orderBy** field or **orderByDesc** field. For multiple fields, use `orderByField1^orderByField2^orderByField3`. **orderBy** specifies ascending order and orderByDesc specifies descending. These prefix strings are optional. If not specified, **orderBy** is the default order.

|Name|Type|Description|
|----|----|-----------|
|orderBy|String|Single or multiple orderBy fields.|

|Type|Description|
|----|-----------|
|void| |

```
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            updateOrderBy: function(orderBy){
  var list = GlideList2.get(this.listID);
  if (list)
    list.setOrderBy(orderBy);
};
```

## GlideList2 - setRowsPerPage\(Number rows\)

Sets the number of rows per page to display.

|Name|Type|Description|
|----|----|-----------|
|rows|Number|The number of rows to display.|

|Type|Description|
|----|-----------|
|void| |

```
link: function(scope) {
  var list = GlideList2.get(scope.listId);
  list.setRowsPerPage(scope.maxRows);
  list.setFilterAndRefresh(scope.tableQuery);
}
```

## GlideList2 - showHideGroups\(Boolean showFlag\)

Shows or hides all the groups within the list and saves the current collapsed/expanded state of the groups as a user preference.

|Name|Type|Description|
|----|----|-----------|
|showFlag|Boolean|If **true**, shows the groups within the list.|

|Type|Description|
|----|-----------|
|void| |

```
function showHideAllGroups(showFlag) {
  var list = GlideList2.get(listId);
  if (!list)
    return;
  list.showHideGroups(showFlag);
}
```

## GlideList2 - showHideList\(Boolean showFlag\)

Displays or hides the list and saves the current collapsed/expanded state of the list as a user preference.

|Name|Type|Description|
|----|----|-----------|
|showFlag|Boolean|If **true**, displays the list.|

|Type|Description|
|----|-----------|
|void| |

```
GlideList2.toggleAll = function(expandFlag) {
for (var id in GlideLists2) {
  var list = GlideLists2[id];
list.showHideList(expandFlag);
}
```

## GlideList2 - sort\(String field\)

Sorts the list in ascending order and sets the field as an **orderBy** column.

|Name|Type|Description|
|----|----|-----------|
|field|String|Field to use to sort the list.|

|Type|Description|
|----|-----------|
|void| |

```
$timeout(function() {
  if (GlideList.lists) {
    var list = GlideList.get(name);
    if (list) {
       if (sortBy) {
         if (sortDirection == 'ASC')
            list.sort(sortBy);
         else
            list.sortDescending(sortBy);
         }  
       list.refresh();
     }
   }
}
```

## GlideList2 - sortDescending\(String field, Number amount\)

Sorts a single field in the list in descending order and sets the field as an **orderByDescField** column.

|Name|Type|Description|
|----|----|-----------|
|field|String|Field to use to sort the list.|

|Type|Description|
|----|-----------|
|void| |

```
$timeout(function() {
  if (GlideList.lists) {
    var list = GlideList.get(name);
    if (list) {
       if (sortBy) {
         if (sortDirection == 'ASC')
            list.sort(sortBy);
         else
            list.sortDescending(sortBy);
         }  
       list.refresh();
     }
   }
}
```

## GlideList2 - toggleList\(\)

Toggles the display of the list and saves the current collapsed/expanded state of the list as a user preference.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|void| |

```
var list = GlideList2.get(listId);
if (!list)
  return;
list.toggleList();
```

## GlideList2 - toggleListNoPref\(\)

Toggles the display of the list but does not save the current collapsed/expanded state of the list as a user preference.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|void| |

```
var list = GlideList2.get(listId);
if (!list)
  return;
list.toggleListNoPref();
```

