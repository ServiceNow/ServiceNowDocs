---
title: Create related list views for new planning item types in Strategic Planning
description: For every new planning item table that you create, you must create the necessary related list views. You can also customize the related list views for existing planning items.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Define a new planning item type in Strategic Planning, Planning item configuration for lenses and portfolio plans, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create related list views for new planning item types in Strategic Planning

For every new planning item table that you create, you must create the necessary related list views. You can also customize the related list views for existing planning items.

## Before you begin

-   [Define a new planning item type in Strategic Planning](create-planning-organization-and-planning-item-type.md).
-   Ensure that the application scope in your instance is set to Portfolio Planning.

Role required: admin

## About this task

Every Related list that you add to your planning item tables must be in the APW Default view.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Filter the list of tables by using **Planning Item** in the Extends table column.

3.  Select a planning item type that you created.

4.  Select the **Show Form** related link.

5.  From the form header, select the Additional actions menu \(![Additional actions icon.](../images/additional-actions-icon.png)\) and select **Configure** &gt; **Related Lists**.

6.  From the **View name** field in the List view section, select **New**.

7.  In the **View name** field, enter **APW Default**.

8.  Select **OK**

9.  Using the Available and Selected lists of related lists, select the ones that you want on your planning item form.

    You can also rearrange them in the order of your choice.

10. Select **Save**.


## What to do next

[Create workspace view rules for new planning item forms in Strategic Planning](create-workspace-view-rules-for-planning-item-tables.md).

