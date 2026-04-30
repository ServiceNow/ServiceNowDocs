---
title: GlideListV3 \(g\_list\) - Client \(deprecated\)
description: The GlideListV3 API provides methods to manipulate lists.Adds a single term to the list query filter.Returns the GlideList object for specified list.Returns the GlideList object for the specified DOM element.Returns a comma-separated list of sys\_ids for checked items in the list. Does not return items that are not allowed to be executed.Returns the sysparm\_fixed query.Returns the form's target attribute.Returns the field or comma-separated list of fields that are used to group the list.Returns the name of the list, which is usually the table name.Returns the first field used to order the list.Returns the name of the parent table \(the table associated with the form\).Returns the encoded query string for the list.Returns the referring URL.Returns the related list field that associates the related list to the parent form.Returns the related list type.Returns the relationship record id, if this is type REL related list.Returns the number of rows returned by the query.Returns the number of rows to be displayed on a page.Returns the table name of the list.Returns the list title.Returns the view used to display the list.Returns true if the list has been personalized by the user.Refreshes the list. The orderBy part of the list filter is ignored so that the list's natural ordering is used.Refreshes the list using the orderBy fields.Sets the encoded query string for the list ignoring the orderBy and groupBy parts of the query string.Sets the encoded query string for the list, and then refreshes the list using the new filter.Sets the first row to be displayed when the list is refreshed.Specifies where to display the response from the form.Sets the groupBy criteria for the list, for a single field or multiple fields.Sets the orderBy criteria for the list.Sets the parent form referring url.Set the number of rows to display on a page.Displays or hides all of the groups within the list and saves the current collapsed/expanded state of the groups as a user preference.Displays or hides the list and saves the current collapsed/expanded state of the list as a user preference.Sort the list in ascending order.Sorts the list in descending order.Toggles the list display between collapsed and expanded, and saves the state as a user preference.Toggles the list display between collapsed and expanded, but does not save the state as a user preference.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideListV3 \(g\_list\) - Client \(deprecated\)

The GlideListV3 API provides methods to manipulate lists.

You access the GlideListV3 methods by using the `g_list` global object. These methods are used in UI context menus and UI actions. The g\_list object is not available for related lists on the form link UI action.

**Note:**

This API is no longer supported. Consider using the [GlideList2\(\)](../../GlideList2/concept/c_GlideList2API.md#) API instead.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideListV3 - addFilter\(String filter\)

Adds a single term to the list query filter.

|Name|Type|Description|
|----|----|-----------|
|filter|String|Query string condition to add.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - get\(String listId\)

Returns the GlideList object for specified list.

|Name|Type|Description|
|----|----|-----------|
|listId|String|The list name.|

|Type|Description|
|----|-----------|
|Object|The GlideList object for the specified list, or null if not found.|

## GlideListV3 - get\(Object DomElement\)

Returns the GlideList object for the specified DOM element.

|Name|Type|Description|
|----|----|-----------|
|DomElement|Object|The DOM element ID for which you want the GlideList object.|

|Type|Description|
|----|-----------|
|Object|The GlideList object for the specified DOM element. Returns null if the DOM element is not found.|

## GlideListV3 - getChecked\(\)

Returns a comma-separated list of sys\_ids for checked items in the list. Does not return items that are not allowed to be executed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Comma-separated list of the sys\_ids for checked items in the list. Does not return items that are not allowed to be executed.|

## GlideListV3 - getFixedQuery\(\)

Returns the sysparm\_fixed query.

The fixed query is the part of the query that cannot be removed from the breadcrumb \(i.e., it is fixed for the user\). It is specified by including a **sysparm\_fixed\_query** parameter for the application module.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The fixed query string for the list.|

## GlideListV3 - getFormTarget\(\)

Returns the form's target attribute.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The form's target attribute.|

## GlideListV3 - getGroupBy\(\)

Returns the field or comma-separated list of fields that are used to group the list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The field or comma-separated list of fields used to group the list.|

## GlideListV3 - getListName\(\)

Returns the name of the list, which is usually the table name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The list name.|

## GlideListV3 - getOrderBy\(\)

Returns the first field used to order the list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The field used to order the list, or an empty string if the list is not sorted.|

## GlideListV3 - getParentTable\(\)

Returns the name of the parent table \(the table associated with the form\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The parent table name.|

## GlideListV3 - getQuery\(Object options\)

Returns the encoded query string for the list.

<table id="table_mdc_nmy_pv" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

options

</td><td>

Object

</td><td>

The options can be one or more of the following.-   orderby - include ORDERBY in the query
-   groupby - include GROUPBY in the query
-   fixed - include sysparm\_fixed\_query in the query
-   all - include all the options in the query

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Encoded query string for the list.|

## GlideListV3 - getReferringUrl\(\)

Returns the referring URL.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Returns the parent form's URL, or '\*' if there is no parent form.|

## GlideListV3 - getRelated\(\)

Returns the related list field that associates the related list to the parent form.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Field that connects the list to the parent form.|

## GlideListV3 - getRelatedListType\(\)

Returns the related list type.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The relationship table type.|

## GlideListV3 - getRelationshipId\(\)

Returns the relationship record id, if this is type REL related list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The sys\_id of the relationship record.|

## GlideListV3 - getRowCount\(\)

Returns the number of rows returned by the query.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of rows returned by the query.|

## GlideListV3 - getRowsPerPage\(\)

Returns the number of rows to be displayed on a page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of rows to be displayed on a page.|

## GlideListV3 - getTableName\(\)

Returns the table name of the list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The list's table name.|

## GlideListV3 - getTitle\(\)

Returns the list title.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The list title.|

## GlideListV3 - getView\(\)

Returns the view used to display the list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The name of the view|

## GlideListV3 - isUserList\(\)

Returns true if the list has been personalized by the user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the list layout has changed.|

## GlideListV3 - refresh\(Number firstRow, Object additionalParams\)

Refreshes the list. The orderBy part of the list filter is ignored so that the list's natural ordering is used.

|Name|Type|Description|
|----|----|-----------|
|firstRow|Number|\(Optional\) The first row to display in the list. If not specified, the list's current first row is used.|
|additionalParams|Object|\(Optional\) Name- value pairs that are submitted with the list refresh request.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - refreshWithOrderBy\(Number firstRow, Object additionalParams\)

Refreshes the list using the orderBy fields.

|Name|Type|Description|
|----|----|-----------|
|firstRow|Number|\(Optional\) The first row to display in the list. If not specified, the list's current first row is used.|
|additionalParams|Object|\(Optional\) Name- value pairs that are submitted with the list refresh request.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - setFilter\(String filter, Boolean saveOrderBy, Boolean saveGroupBy\)

Sets the encoded query string for the list ignoring the orderBy and groupBy parts of the query string.

|Name|Type|Description|
|----|----|-----------|
|filter|String|An encoded query string.|
|saveOrderBy|Boolean|The default is false. When true uses the orderBy part of the query.|
|saveGroupBy|Boolean|The default is false. When true uses the groupBy part of the query.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - setFilterAndRefresh\( String filter\)

Sets the encoded query string for the list, and then refreshes the list using the new filter.

This preserves the groupby and orderby parameters.

|Name|Type|Description|
|----|----|-----------|
|filter|String|Encoded query string.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - setFirstRow\(Number firstRow\)

Sets the first row to be displayed when the list is refreshed.

|Name|Type|Description|
|----|----|-----------|
|firstRow|Number|The row number in the list.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - setFormTarget\(String target\)

Specifies where to display the response from the form.

|Name|Type|Description|
|----|----|-----------|
|target|String|The form.target attribute value to use.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - setGroupBy\(String groupBy\)

Sets the **groupBy** criteria for the list, for a single field or multiple fields.

For a single field, use field or groupByField. The groupBy prefix is optional. For multiple fields use `field1^field2^field3` or `groupByField1^groupByField2^groupByField3`.

|Name|Type|Description|
|----|----|-----------|
|String|groupBy|The group by criteria for the list.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - setOrderBy\(String orderBy\)

Sets the **orderBy** criteria for the list.

For a single order by field use **orderBy** field or **orderByDescField**. For multiple fields, use `orderByField1^orderByField2^orderByField3`. **orderBy** specifies ascending order and orderByDesc specifies descending. These prefix strings are optional. If not specified **orderBy** is assumed.

|Name|Type|Description|
|----|----|-----------|
|orderBy|String|Single or multiple order by fields.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - setReferringUrl\(String url\)

Sets the parent form referring url.

|Name|Type|Description|
|----|----|-----------|
|url|String|The parent form's URL|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - setRowsPerPage\(Number numRows\)

Set the number of rows to display on a page.

|Name|Type|Description|
|----|----|-----------|
|numRows|Number|The number of rows to display on a page.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - showHideGroups\(Boolean showFlag\)

Displays or hides all of the groups within the list and saves the current collapsed/expanded state of the groups as a user preference.

|Name|Type|Description|
|----|----|-----------|
|showFlag|Boolean|When true, displays the groups within the list.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - showHideList\(Boolean showFlag\)

Displays or hides the list and saves the current collapsed/expanded state of the list as a user preference.

|Name|Type|Description|
|----|----|-----------|
|showFlag|Boolean|When true, displays the list.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - sort\(String field\)

Sort the list in ascending order.

|Name|Type|Description|
|----|----|-----------|
|field|String|The field to be used to sort the list.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - sortDescending\(String field\)

Sorts the list in descending order.

|Name|Type|Description|
|----|----|-----------|
|field|String|The field used to sort the list.|

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - toggleList\(\)

Toggles the list display between collapsed and expanded, and saves the state as a user preference.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## GlideListV3 - toggleListNoPref\(\)

Toggles the list display between collapsed and expanded, but does not save the state as a user preference.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

