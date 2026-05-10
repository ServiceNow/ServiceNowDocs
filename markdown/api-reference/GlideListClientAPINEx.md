---
title: GlideList \(Next Experience\) - Client
description: The GlideList API provides methods to customize lists in the Next Experience UI Framework.Adds a single term to the list query filter.Returns a comma-separated list of the sys\_ids for the items that are checked in the associated list.Returns the fixed query.Returns the field or comma-separated list of fields that are used to group the list.Returns the name of the list, which is usually the table name.Returns the first field used to order the list.Returns the name of the parent table for a related list \(the table associated with the form\).Returns the encoded query string for the list.Returns the related list field that associates the related list to the parent form.Returns the table name for the list.Returns the list title.Returns the view used to display the list.Refreshes the list. The orderBy part of the list filter is ignored so that the list uses its natural ordering when it is refreshed.Refreshes the list. The orderBy part of the list filter is included if it is specified for the list.Sets the encoded query string for the list, ignoring the orderBy and groupBy parts of the query string.Sets the list groupBy criteria for a single field.Sets the orderBy criteria for the list.Sets the number of rows per page to display.Sorts the list in ascending order and sets the field as an orderBy column.Sorts a single field in the list in descending order and sets the field as an orderByDescField column.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Client Next Experience API reference, API reference, API implementation and reference]
---

# GlideList \(Next Experience\) - Client

The GlideList API provides methods to customize lists in the Next Experience UI Framework.

This API enables adding GlideList functionality to a button in the Workspace Experience UI. Use the `g_list` variable to call each method.

To add a button, create a list action and add GlideList method calls into the **Client Script** field `onClick{}` method. For instructions, see [Use the client GlideList API in the Workspace Experience UI](../../../../../administer/workspace/task/add-api-glide.md).

![GlideList method calls in the Client Script field.](../../../../../administer/workspace/image/add-api-glidelist-workspace.png)

**Note:** Each method must be used with the refresh\(\) method, with the exceptions of sort\(\) and sortDescending\(\) methods.

The methods in this API are based on [GlideList2](../../GlideList2/concept/c_GlideList2API.md#). The following GlideList2 methods are not supported in the Next Experience framework and cause an error in the console log:

-   isUserList\(\)
-   setFirstRow\(\)
-   showHideGroups\(\)
-   showHideList\(\)
-   toggleList\(\)
-   toggleListNoPref\(\)

**Parent Topic:**[Client Next Experience API reference](../../../../../build/applications/concept/api-client-next.md)

## GlideList \(Next Experience\) - addFilter\(String filter\)

Adds a single term to the list query filter.

See also [setFilter\(\)](GlideListClientAPINEx.md#).

|Name|Type|Description|
|----|----|-----------|
|filter|String|Encoded query string in standard Glide format. See [Encoded query strings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_EncodedQueryStrings.md).|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to retrieve a list of active records and refresh the page.

```
g_list.addFilter("active=true");
g_list.refresh();
```

## GlideList \(Next Experience\) - getChecked\(\)

Returns a comma-separated list of the sys\_ids for the items that are checked in the associated list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Comma-separated list of the sys\_ids for the items that are checked in the list. Does not check to determine that the items returned are allowed to be executed.|

The following example shows how to get the sys\_ids of each record selected in a list.

```
var myChecked = g_list.getChecked();
alert(myChecked);
g_list.refresh();
```

Output in an alert box \(empty if no records are selected\):

```
079893e6b733330059128ac7ee11a967, 4fca6d45b7131010f03e9b7ade11a9d3, 5c460fbf1bd0011079e52131604bcbd9
```

## GlideList \(Next Experience\) - getFixedQuery\(\)

Returns the fixed query.

A fixed query is the part of the query that cannot be removed from the breadcrumb \(i.e., it is fixed for the user\).

Apply this method under **Related List Actions** in the Workspace Experience UI. For instructions, see [Use the client GlideList API in the Workspace Experience UI](../../../../../administer/workspace/task/add-api-glide.md).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The fixed query string for the list.|

The following example shows how to display a fixed query with a debug message in the browser console log.

```
console.log(g_list.getFixedQuery() + " debug message");
```

The output after clicking the button on the Child Incidents tab in an Incident record.

```
parent_incident=46f1784ba9fe19810018aa27fbb23482 debug message
```

## GlideList \(Next Experience\) - getGroupBy\(\)

Returns the field or comma-separated list of fields that are used to group the list.

See also:

-   [getQuery\(\)](GlideListClientAPINEx.md#)
-   [setGroupBy\(\)](GlideListClientAPINEx.md#)

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The field or comma-separated list of fields that are used to group the list.|

The following example shows how to get field groupBy values of the current list view.

```
var grpdBy = g_list.getGroupBy();
alert("The list is grouped by " + grpdBy);
g_list.refresh();
```

Output in an alert box for a list grouped by priority:

```
The list is grouped by ^GROUPBYpriority
```

## GlideList \(Next Experience\) - getListName\(\)

Returns the name of the list, which is usually the table name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The list name \(usually the table name\).|

The following example shows how to call the method.

```
g_list.getListName();
```

## GlideList \(Next Experience\) - getOrderBy\(\)

Returns the first field used to order the list.

See also:

-   [getQuery\(\)](GlideListClientAPINEx.md#)
-   [setOrderBy\(\)](GlideListClientAPINEx.md#)

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The field by which to order the list. Empty if the list is not ordered.|

The following example shows how to get field orderBy values of the current list view.

```
var orderBy = g_list.getOrderBy();
	
alert("The list is ordered by " + orderBy);
g_list.refresh();
```

Output in an alert box for a list ordered by priority:

```
The list is ordered by ^ORDERBYDESCpriority
```

## GlideList \(Next Experience\) - getParentTable\(\)

Returns the name of the parent table for a related list \(the table associated with the form\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The parent table name.|

The following example shows how to call the method.

```
g_list.getParentTable();
g_list.refresh();
```

## GlideList \(Next Experience\) - getQuery\(Object\)

Returns the encoded query string for the list.

See also:

-   [getFixedQuery\(\)](GlideListClientAPINEx.md#)
-   [getGroupBy\(\)](GlideListClientAPINEx.md#)
-   [getOrderBy\(\)](GlideListClientAPINEx.md#)
-   [setGroupBy\(\)](GlideListClientAPINEx.md#)
-   [setOrderBy\(\)](GlideListClientAPINEx.md#)

<table id="table_us2_nww_15" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;object&gt;

</td><td>

Object

</td><td>

Optional. By default, this method includes orderBy, groupBy, and fixed query in the results. You can set object properties to restrict results to one or more of the three available options.

</td></tr><tr><td>

&lt;object&gt;.orderBy

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to include orderBy in results.Valid values:

-   true: Include orderBy in results.
-   false: Do not include orderBy in results.

 Default: false

</td></tr><tr><td>

&lt;object&gt;.groupBy

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to include groupBy in results.Valid values:

-   true: Include groupBy in results.
-   false: Do not include groupBy in results.

 Default: false

</td></tr><tr><td>

&lt;object&gt;.fixed

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to include fixed query in results.Valid values:

-   true: Include fixed query in results.
-   false: Do not include fixed query in results.

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Encoded query string for the list.|

The following example shows how to display the list encoded query with a debug message in the browser console log.

```
var myQuery = g_list.getQuery();
console.log(myQuery + " message");
```

Output:

```
active=false^EQ message
```

## GlideList \(Next Experience\) - getRelated\(\)

Returns the related list field that associates the related list to the parent form.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Field that connects the list to the parent form.|

The following example shows how to call the method.

```
g_list.getRelated();
```

## GlideList \(Next Experience\) - getTableName\(\)

Returns the table name for the list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Returns the table name for the list.|

The following example shows how to display the list name for the current view.

```
var listName = g_list.getListName();
alert("The current list name is " + listName);
g_list.refresh();
```

Output in an alert box:

```
The current list name is incident
```

## GlideList \(Next Experience\) - getTitle\(\)

Returns the list title.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The list title.|

The following example shows how to call the method.

```
g_list.getTitle();
```

## GlideList \(Next Experience\) - getView\(\)

Returns the view used to display the list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The name of the view.|

The following example shows how to call the method.

```
g_list.getView();
```

## GlideList \(Next Experience\) - refresh\(Number firstRow\)

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

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to call the method.

```
g_list.addFilter("active=true");
g_list.refresh();
```

## GlideList \(Next Experience\) - refreshWithOrderBy\(Number firstRow\)

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

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to call the method.

```
g_list.refreshWithOrderBy();
```

## GlideList \(Next Experience\) - setFilter\(String filter\)

Sets the encoded query string for the list, ignoring the **orderBy** and **groupBy** parts of the query string.

See also [addFilter\(\)](GlideListClientAPINEx.md#).

|Name|Type|Description|
|----|----|-----------|
|filter|String|Encoded query string in standard Glide format. See [Encoded query strings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_EncodedQueryStrings.md).|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to restrict list results to active records.

```
g_list.setFilter("active=true");
g_list.refresh();
```

## GlideList \(Next Experience\) - setGroupBy\(String groupBy\)

Sets the list **groupBy** criteria for a single field.

See also:

-   [getGroupBy\(\)](GlideListClientAPINEx.md#)
-   [getQuery\(\)](GlideListClientAPINEx.md#)

|Name|Type|Description|
|----|----|-----------|
|groupBy|String|The **groupBy** criteria for the list.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to group listed records by Caller ID.

```
g_list.setGroupBy("caller_id");
g_list.refresh();
```

## GlideList \(Next Experience\) - setOrderBy\(String orderBy\)

Sets the **orderBy** criteria for the list.

For a single order by field, use **orderBy** field or **orderByDesc** field. For multiple fields, use `orderByField1^orderByField2^orderByField3`. **orderBy** specifies ascending order and orderByDesc specifies descending. These prefix strings are optional. If not specified, **orderBy** is the default order.

See also:

-   [getOrderBy\(\)](GlideListClientAPINEx.md#)
-   [getQuery\(\)](GlideListClientAPINEx.md#)
-   [sort\(\)](GlideListClientAPINEx.md#)
-   [sortDescending\(\)](GlideListClientAPINEx.md#)

|Name|Type|Description|
|----|----|-----------|
|orderBy|String|Single or multiple orderBy fields.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to order the list by the value of the Priority field.

```
g_list.setOrderBy("priority");
g_list.refresh();
```

## GlideList \(Next Experience\) - setRowsPerPage\(Number rows\)

Sets the number of rows per page to display.

|Name|Type|Description|
|----|----|-----------|
|rows|Number|The number of rows to display.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to limit results to 50 rows per page.

```
g_list.setRowsPerPage(50);
refresh();
```

## GlideList \(Next Experience\) - sort\(String field\)

Sorts the list in ascending order and sets the field as an **orderBy** column.

See also:

-   [getOrderBy\(\)](GlideListClientAPINEx.md#)
-   [getQuery\(\)](GlideListClientAPINEx.md#)
-   [setOrderBy\(\)](GlideListClientAPINEx.md#)
-   [sortDescending\(\)](GlideListClientAPINEx.md#)

**Note:** This method does not require the refresh\(\) method.

|Name|Type|Description|
|----|----|-----------|
|field|String|Field to use to sort the list.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to sort results by the **Number** field.

```
g_list.sort("number");
```

## GlideList \(Next Experience\) - sortDescending\(String field, Number amount\)

Sorts a single field in the list in descending order and sets the field as an **orderByDescField** column.

See also:

-   [getOrderBy\(\)](GlideListClientAPINEx.md#)
-   [getQuery\(\)](GlideListClientAPINEx.md#)
-   [setOrderBy\(\)](GlideListClientAPINEx.md#)
-   [sortDescending\(\)](GlideListClientAPINEx.md#)

**Note:** This method does not require the refresh\(\) method.

|Name|Type|Description|
|----|----|-----------|
|field|String|Field to use to sort the list.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to sort results by the Number field in descending order.

```
g_list.sortDescending("number");
```

