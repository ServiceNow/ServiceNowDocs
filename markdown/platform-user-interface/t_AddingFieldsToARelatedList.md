---
title: Add fields to selections in a related list
description: When you click Edit in a related list and select an item, information about the item appears below the list. You can expand the fields that appear for the item to provide more information.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Related lists, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Add fields to selections in a related list

When you click **Edit** in a related list and select an item, information about the item appears below the list. You can expand the fields that appear for the item to provide more information.

## Before you begin

Role required: admin

## About this task

![Fields that display when a value is selected in the slushbucket.](../image/EditMemberDescAddFields.png "Fields listed for selected record")

To add fields to selections in a related list, record the exact field name, or element, not the label name. This example demonstrates adding fields to the **Groups** related list \[sys\_user\_group\].

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Views**.

2.  Select **sys\_ref\_list**.

3.  To add fields from the Group table, in the **Lists** related list, select **sys\_user\_group**.

4.  In the **List Elements** related list, click **New**.

5.  Enter the field name and its relative position when it appears in the description.

    Fields appear from top to bottom, lowest to highest number.

6.  Click **Submit**.


**Parent Topic:**[Related lists](../../../use/using-forms/concept/c_RelatedLists.md)

**Related topics**  


[Select or create records in a related list](../../../use/using-forms/task/t_SelectRelatedRecords.md)

[Configure when a related list loads](../../../use/using-forms/task/t_ConfigureWhenARelatedListLoads.md)

[Create a default filter for a related list](../../../use/using-forms/task/t_CreateADefaultFilter.md)

[Configure the edit option](../../../use/using-forms/task/t_ConfigureTheEditOption.md)

[Create defined related lists](t_CreateDefinedRelatedLists.md)

[Create a default filter for list selector records](t_CreateDefaultRelatedRecSecFilter.md)

