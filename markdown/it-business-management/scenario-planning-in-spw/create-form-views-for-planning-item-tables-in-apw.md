---
title: Create form views for new planning item tables in Strategic Planning
description: For every new planning item table that you create, you must create the necessary form views. You can also customize the views for existing planning items.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Define a new planning item type in Strategic Planning, Planning item configuration for lenses and portfolio plans, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create form views for new planning item tables in Strategic Planning

For every new planning item table that you create, you must create the necessary form views. You can also customize the views for existing planning items.

## Before you begin

-   [Define a new planning item type in Strategic Planning](create-planning-organization-and-planning-item-type.md).
-   Ensure that the application scope in your instance is set to Portfolio Planning.

Role required: admin

## About this task

The following are the necessary form views:

-   APW Preview: Supports the view that is used to display the planning item details on the roadmap side panel.
-   APW Default: Supports the default view of the planning item form in Strategic Planning.
-   APW New: Supports the form view that is used while creating a planning item of this type from the roadmap.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Filter the list of tables by using **Planning Item** in the Extends table column.

3.  Select a planning item type that you created.

4.  Select the **Layout Form** related link.

5.  From the **View name** field, select **New**.

6.  In the **Create New View** window, enter one of the following names in the **View name** field:

    -   To create the APW Preview view, enter **Workspace APW Preview**
    -   To create the APW Default view, enter **Workspace APW Default**
    -   To create the APW New view, enter **Workspace APW New**
    If you're creating a view other than these, ensure that your view name does not contain any special characters. For example, if you want to create a view with the name SAFe-Portfolio, replace the hyphen \(-\) with a space and enter the name as SAFe Portfolio.

7.  Select **OK**

8.  Using the Available and Selected lists of fields, select the fields to be visible on the form.

    You can also rearrange them in the order of your choice. To keep the form views of new tables consistent with that of the default settings, ensure you do the following changes:

    -   For Preview and APW Default views, select the **Strategic priority** and the **Primary goal** fields to be visible on the form.
    -   For all three views, select the field for the bottom entity of your lens to be visible on the form.
    -   For all three views, add the Milestones related list. See [Add a related list to a form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
9.  Select **Save**.

    A new form view is created for this planning item type.

10. Repeat the steps 4 through 8 to complete creating the other two form views.


## What to do next

[Create list views for new planning item tables in Strategic Planning](create-list-views-for-new-planning-item-tables-in-strategic-planning.md).

