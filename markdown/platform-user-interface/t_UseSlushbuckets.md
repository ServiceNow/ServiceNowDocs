---
title: Configure items on forms or in lists using a list collector
description: Use a list collector to add, remove, or move items in a form or list. List collectors allow you to select multiple items from a list of available items and to remove items from a list of selected items. Some list collectors provide filter and search controls for available items, such as adding items to related lists.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure items on forms or in lists using a list collector

Use a list collector to add, remove, or move items in a form or list. List collectors allow you to select multiple items from a list of available items and to remove items from a list of selected items. Some list collectors provide filter and search controls for available items, such as adding items to related lists.

## Before you begin

Role required: admin

## About this task

Use list collectors to personalize lists, add items to related lists, and Service Catalog list collector variables. Some list collectors allow users to customize the order of selections, such as when you are configuring a form or list.

The list collector interface has two columns: the available items on the left and the selected items on the right.

Information fields for the highlighted available item appear beneath some list collectors. The information fields are the same as the reference lookup for a reference field on a form. To modify which fields appear, configure the reference lookup list.

## Procedure

-   To add items to the selection, double-click an available item on the left or select an item and click the add icon \(**&gt;**\).

    The new item is added at the bottom of the selected items column on the right.

-   To remove items from the selection, double-click the item on the right, or select the item and click the remove icon \(**&lt;**\).

-   To select multiple consecutive items, hold the Shift key and click the first and last item.

-   To select multiple non-consecutive items, hold the Ctrl key \(Command key on Mac\) and click the desired items.

-   To accessibly select multiple items, tab to each item and press the spacebar to select each item.

    Use the arrow key or tab to the **Add** button to move items from one list to another.

-   To filter available items, create conditions using the condition builder and click **Run filter**.

-   To search available items, enter text in the **Search** field.

    The list of available items is filtered as you type.

    ![List collector with a search for "Bo" that is showing search results for items containing "bo"](../image/SlushbucketRelatedList.png "Filter Items")

-   To move items one position, select the items and click the up or down icon.

-   To move an item multiple positions, select consecutive items above or below the item then click the up or down icon. In this example, to move **Assigned to** to the top of the selections order, complete the following steps.

    1.  Hold the Shift key and click **Short description** then **Number**.

    2.  Click the down icon.

        ![Arrange items](../image/PersonalizeListLayout.png "Arrange items")


-   **[Set the number of list collector items visible in the available column](t_SetNumSlushbucketItemsVisible.md)**  
You can modify the **glide.xmlhttp.excessive** property to change the number of items that appear in the **Available** column of the list collector.

**Parent Topic:**[Common UI elements](../topic/p_CommonUIElements.md)

**Related topics**  


[Personal lists](../../using-lists/concept/c_PersonalLists.md#)

