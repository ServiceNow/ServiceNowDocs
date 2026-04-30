---
title: Create or update form views for EAP work items
description: Create or update form views for work item types so that the fields displayed in the Backlog and Planning board pages of Enterprise Agile Planning suit your team requirements.
locale: en-US
release: yokohama
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create or update form views for EAP work items

Create or update form views for work item types so that the fields displayed in the Backlog and Planning board pages of Enterprise Agile Planning suit your team requirements.

## Before you begin

Set the application scope in your instance to Portfolio Planning Core.

Role required: sn\_apw\_advanced.eap\_admin

## About this task

Configuration for form views of work item tables determines the fields that are displayed in the workspace. For a work item type in EAP, the following are the necessary form views:

-   EAP Default: Determines the fields to be displayed in the Full details page.
-   EAP Preview: Determines the fields to be displayed in the side panel of the Backlog or Planning board.
-   EAP New: Determines the fields to be displayed when creating a work item from the Backlog or Planning board.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Filter the list of tables by using **EAP planning item** in the Extends table column.

3.  Select a work item type that you created.

4.  Select the **Layout Form** related link.

5.  Create form views or update them.

<table id="choicetable_xcm_cz1_f1c"><thead><tr><th align="left" id="d88770e129">

Option

</th><th align="left" id="d88770e132">

Steps

</th></tr></thead><tbody><tr><td id="d88770e138">

**Create form views**

</td><td>

1.  From the **View name** field, select **New**.
2.  In the **Create New View** window, enter one of the following names in the **View name** field:
    -   To create the EAP Preview view, enter **Workspace EAP Preview**
    -   To create the EAP Default view, enter **Workspace EAP Default**
    -   To create the EAP New view, enter **Workspace EAP New**
3.  Select **OK**.
4.  For each section, select the fields to be displayed using the Available and Selected lists.

You can also rearrange them in the order of your choice.

5.  Repeat the steps to complete creating the other two form views.


</td></tr><tr><td id="d88770e209">

**Edit existing form views**

</td><td>

1.  From the **View name** field, select an EAP view to update.
2.  For each section of the view, select the fields to be displayed using the Available and Selected lists.

You can also rearrange them in the order of your choice.

</td></tr></tbody>
</table>6.  Select **Save**.


## What to do next

[Create or update list view for EAP work items](create-or-update-list-views-for-eap-work-items.md).

