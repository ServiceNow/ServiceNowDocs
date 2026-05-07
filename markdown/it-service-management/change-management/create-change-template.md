---
title: Create and propose a change template
description: Create, customize, and then propose for publication a change template aligned to a change model to make change creation faster, and promote data quality and consistency.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a Change model, Configure, Change Management, IT Service Management]
---

# Create and propose a change template

Create, customize, and then propose for publication a change template aligned to a change model to make change creation faster, and promote data quality and consistency.

## Before you begin

Role required: change\_manager

You must have a role with the following access with regard to the change model to create and propose a change template:

-   Access to read
-   Access to modify

## Procedure

1.  Access the Create a new change template form.

<table id="choicetable_vrd_rrt_tsb"><thead><tr><th align="left" id="d411024e65">

Source

</th><th align="left" id="d411024e68">

Description

</th></tr></thead><tbody><tr><td id="d411024e74">

**Change Model**

</td><td>

1.  Navigate to **All** &gt; **Change Models**
2.  Select the relevant change model.
3.  Navigate to the **Change Templates** tab, and then select **New**.

**Note:** You can propose a new template only if you have access to the change model.

</td></tr><tr><td id="d411024e111">

**Create a change request page**

</td><td>

1.  Navigate to a list of changes.

**Note:** The following lists are available:

    -   Open
    -   Closed
    -   All
2.  Select **New**.
3.  On the Create a new change request page, view available change models by selecting **Model**.
4.  Select the model for which you want to create a change template.
5.  Select the **More actions** menu.
6.  Select **Create a new template**.


</td></tr><tr><td id="d411024e168">

**Templates tab**

</td><td>

1.  Navigate to **All** &gt; **Change Templates**.
2.  Select **New**.
3.  Select the change model.


</td></tr></tbody>
</table>2.  In the change template record, provide the template name and a short description.

3.  Either retain the default setting that makes the template active or make the template unavailable for use even after being published by clearing the **Active** check box.

4.  In the record header, select **Save**.

    A new change template record is created in the **Draft** state with the template name provided.

5.  Configure preset fields for the template.

    1.  In the **Change Request Template** section select the required change request fields from the **Template** list.

    2.  Provide the field values to be populated by default when a change request record is created using the template.

6.  Configure the template field policies to set fields as mandatory, optional, or read-only.

    1.  In the **Template Field Policies** tab, select **New**.

    2.  Select the field name from the list to add the field for which you want to set field policies.

    3.  Determine the field policy by selecting one of the following options:.

        -   To make the field mandatory, select **Mandatory**.
        -   To have the field display only predetermined default information, select **Read only**.
    4.  Select **Submit**.

7.  Configure the child task templates.

    1.  Select **New** in the **Change Task Template** tab.

    2.  Select the template name and provide the short description.

    3.  Provide the required template information and then select **Submit**.

        **Note:** You can also add template ﬁelds and conﬁgure ﬁeld policies for the child task templates.

8.  Add templates to an existing category.

    1.  Navigate to the category tab and select **Edit**.

    2.  Move the desired templates from the Collection list to the Template list.

    3.  Select **Save**.

    **Note:** You can also create parent and child category hierarchies and assign templates for each category.

    For more information, see [Configure template categories](configure-template-categories.md).

9.  Propose the new template and share it for approval by selecting **Publish**.

    The state of the template changes to **Proposed**.

    **Note:** You cannot modify templates in the Proposed state.

    If no approvers have been configured for the change template, the template moves from Proposed to Published state by default. If the template is active, the published template is available for use immediately.

    For information about template approval flows, see [Change template management flows](../concept/change-template-management-flows.md).

10. Select **Save**.


## Result

A change template is created and sent for approval to the approvers configured in the associated change model. To view a list of approvers, access the **Approvers** tab on the Change Template page.

To view the review status of all the templates proposed by you, navigate to **All** &gt; **Models** &gt; **My Template Proposals**.

-   **[Configure template categories](configure-template-categories.md)**  
Create template categories and child categories to classify templates based on a change model, template usage, and organizational areas like software or security.
-   **[Modify a template](modify-or-retire-template.md)**  
Copy and modify change templates.
-   **[Review a change template](review-change-template.md)**  
Review a change template proposed for common change requests.
-   **[Retire a change template](retire-a-change-template.md)**  
Retire change templates that you no longer need.
-   **[Change template management flows](../concept/change-template-management-flows.md)**  
Change template management flows trigger and manage steps for the template proposal, modification, and retirement processes.

**Parent Topic:**[Create a Change model](create-a-change-model.md)

