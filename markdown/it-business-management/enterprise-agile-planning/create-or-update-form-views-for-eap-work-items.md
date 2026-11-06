---
title: Create or update form views for EAP work items
description: Create or update form views for work item types so that the fields displayed in the Backlog and Planning board pages of Enterprise Agile Planning suit your team requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/enterprise-agile-planning/create-or-update-form-views-for-eap-work-items.html
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-10-16"
reading_time_minutes: 2
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create or update form views for EAP work items

Create or update form views for work item types so that the fields displayed in the Backlog and Planning board pages of Enterprise Agile Planning suit your team requirements.

## Before you begin

Set the application scope in your instance to Portfolio Planning Core.

Role required: sn\_apw\_advanced.eap\_admin, admin

## About this task

Configuration for form views of work item tables determines the fields that are displayed in the workspace. For a work item type in EAP, the following are the necessary form views:

-   Full details view: Determines the fields to be displayed in the Full details page. You choose this view in the **Work item view** field of the configuration record. Each default configuration uses its own view, such as **EAP Full Configuration**.
-   EAP Preview: Determines the fields to be displayed in the side panel of the Backlog or Planning board.
-   EAP New: Determines the fields to be displayed when creating a work item from the Backlog or Planning board.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Filter the list of tables by using **EAP planning item** in the Extends table column.

3.  Select a work item type that you created.

4.  Select the **Layout Form** related link.

5.  Create form views or update them.

<table id="choicetable_xcm_cz1_f1c"><thead><tr><th align="left" id="d103125e134">

Option

</th><th align="left" id="d103125e137">

Steps

</th></tr></thead><tbody><tr><td id="d103125e143">

**Create form views**

</td><td>

1.  From the **View name** field, select **New**.
2.  In the **Create New View** window, enter one of the following names in the **View name** field.
    -   To create the EAP Preview view, enter **Workspace EAP Preview**
    -   To create the EAP Full Details view, enter **Workspace EAP Full Details**
    -   To create the EAP New view, enter **Workspace EAP New**
3.  Select **OK**.
4.  For each section, select the fields to be displayed using the Available and Selected lists.

You can also rearrange them in the order of your choice.

5.  Repeat the steps to complete creating the other two form views.


</td></tr><tr><td id="d103125e220">

**Edit existing form views**

</td><td>

1.  From the **View name** field, select an EAP view to update.
2.  For each section of the view, select the fields to be displayed using the Available and Selected lists.

You can also rearrange them in the order of your choice.

</td></tr></tbody>
</table>6.  Select **Save**.


## What to do next

To show the Full details view that you created, set it as the default view for the configuration. In the navigation filter, enter `sn_apw_advanced_eap_configuration.list`, and then open the configuration. Select your view in the **Work item view** field and save the record.

[Create or update list view for EAP work items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/create-or-update-list-views-for-eap-work-items.md).

