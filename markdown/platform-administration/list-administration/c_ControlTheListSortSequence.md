---
title: Controlling the sort sequence used to display lists
description: All lists have a default sort sequence based on the type of fields present in the list.For any list, if the user has clicked a column header to sort by that column, then that action is remembered. The next time that list is displayed, the same field is used to order the list.
locale: en-US
release: australia
product: List Administration
classification: list-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Controlling the sort sequence used to display lists

All lists have a default sort sequence based on the type of fields present in the list.

When a user displays a list for the first time, it is sorted by one of the following items.

-   The **ORDERBY** arguments found the URL. \(See the following section on sort order control.\)
-   The **&lt;table&gt;.db.order** and **&lt;table&gt;.db.order.direction** user preferences.
-   The **isOrder** dictionary attribute.
-   The **Order** field if one is present in the table.
-   The **Number** field if one is present in the table.
-   The **Name** field if one is present in the table.
-   The field specified as the display field for the table.

**Note:** The task table is an exception to the preceding sequence. Task and tables extended from task use the **Number** field when no URL arguments or user preferences are found.

## Setting default order with user preferences

The **&lt;table&gt;.db.order** and **&lt;table&gt;.db.order.direction** user preferences determine the field and sort direction seen by the user. A default sort can be created by creating user preference records with no value in the **User** field and checking the **System** check box. This preference is applied to any users who do not have their own preference.

## Setting the default sort order in the system dictionary

An administrator can set the sort order of records displayed for a table in the system dictionary when there is no other sort specified. This is done by adding an attribute called **isOrder** with a value of **true** to the dictionary entry of the desired field. This sort is the sort order presented to all users initially. Once a user sorts a list, that user preference is saved, and the list is always sorted for that user based on the previous sorting preference.

**Note:** **isOrder** can define which field is used for list sorting, but cannot control the sort direction.

## Sorting a column in a list according to session language

By default, when sorting columns in lists, the field values are ordered according to the English alphabet. To support sorting a column according to the user's session language, you can configure the instance behavior and behavior of individual columns. See [Sorting according to the session language](../../localization/task/sorting-session-language.md#).

**Related topics**  


[System dictionary](../../data-dictionary-tables/concept/c_SystemDictionary.md)

[bundle-platux.c_UserPreferences]

[Altering tables and fields using dictionary attributes](../../reference-pages/concept/c_DictionaryAttributes.md)

## Sort order control

For any list, if the user has clicked a column header to sort by that column, then that action is remembered. The next time that list is displayed, the same field is used to order the list.

This remembered sort field can be overridden by adding a *sysparm\_order* specification to the definition of the module. For example, if each time **News** is displayed, you want the new items listed in order of importance, then the **News** module can be updated accordingly.

![Module arguments to set the sort order based on the Importance field](../image/SortSequence.png "Set module sort order to the Importance field value")

The actual order \(ascending or descending\) can be specified by adding a *sysparm\_order\_direction* specification. Here are two examples of sorting a list by the **sys\_created\_on** field, one ascending and one descending:

```
&sysparm_order=sys_created_on &sysparm_order_direction=desc
&sysparm_order=sys_created_on &sysparm_order_direction=asc
```

### Sort by multiple fields

To sort a list by multiple fields, remove everything from the filter field and place it in the arguments field. For example, if the filter specifies **\[Active\] \[is\] \[true\]** and you want to sort by category and subcategory, remove the condition and put the following in the module arguments:

```
active=true^ORDERBYcategory^ORDERBYsubcategory
```

This argument first orders by the category and then orders by the subcategory. If you want any field to be a descending sort, then change *ORDERBY* to be *ORDERBYDESC*.

