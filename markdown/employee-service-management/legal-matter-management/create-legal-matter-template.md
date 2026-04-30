---
title: Create a legal matter template
description: Create a legal matter template that you can apply to a legal matter when promoting from a legal request. The legal matter created using the template contains predefined data such as phases, tasks, ownership, and approvals.
locale: en-US
release: zurich
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Legal matter templates, Configure, Legal Matter Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create a legal matter template

Create a legal matter template that you can apply to a legal matter when promoting from a legal request. The legal matter created using the template contains predefined data such as phases, tasks, ownership, and approvals.

## Before you begin

Role required: sn\_lg\_matter.matter\_config

## About this task

You can also reuse an existing matter template to create a matter template. To do that, you can open an existing template and copy it using the **Copy Template** related link. You can then modify the newly created template as required.

## Procedure

1.  Navigate to **All** &gt; **Legal Matter** &gt; **Templates** &gt; **All**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_xfp_wby_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated template number.

</td></tr><tr><td>

Name

</td><td>

Unique name for the matter template.

</td></tr><tr><td>

Flow

</td><td>

Workflow associated with the matter.

</td></tr><tr><td>

State

</td><td>

State of the matter template. The default value when creating a matter template is Draft.

</td></tr><tr><td>

Active

</td><td>

Option for marking the matter template active.Only active matter templates are available for selection when creating a matter.

</td></tr><tr><td>

Intake form mapping

</td><td>

The intake form to which the matter is mapped. While promoting a legal request to a matter, the intake form mapping enables the associated matter template available for legal fulfillers to select and apply to the promoted matter.

</td></tr><tr><td class="sub-head" colspan="2">

Matter Defaults section

</td></tr><tr><td>

Template

</td><td>

Default values that pre-populate the fields of a legal matter form that is created using the template.Select a field from the list and enter a default value.

</td></tr></tbody>
</table>4.  Click **Submit**.

    A legal matter template is created in the Draft state. The Phases, Tasks, Approvals, and Approver Groups related lists are displayed.

5.  In the Phases related list, [create phase templates](create-phase-template-for-matter-template.md).

6.  In the Tasks related list, [create task templates](create-task-template-for-matter-phase-template.md).

    You can also create matter task templates from the Tasks related list on the Matter Phase Template form.

7.  In the Approver Groups related list, add user groups to whom the matter template is sent for approval.

    1.  In the Approver Groups related list, click **Edit**.

    2.  On the Edit Members form, select a user group from the **Collection** list and click **Add** to add it to the **Approver Groups List**.

        Only the user groups from the Legal department are listed in the **Collection** list.

    3.  Click **Save**.

        The selected approver groups are added to the Approver Groups related list. The members of these groups are listed in the Approvals related list. An email notification is sent to these members for approval of the matter template.

        **Note:** Any user who belongs to multiple groups will only receive one notification and will only appear once in the Approvals list.

8.  Click **Submit for approval**.

    -   If an approver group is selected, the template is sent to the group for approval. The state of the matter template updates to Waiting Approval. Anyone from the approver group can [review and approve the matter template](approve-reject-matter-template.md) to publish it.
    -   If an approver group is not selected, the matter is directly published and its state is Published.
    **Note:** When an existing matter template is updated and published, any associated intake forms reflect the latest version of the template.


-   **[Create a phase template for a matter template](create-phase-template-for-matter-template.md)**  
Create a phase template for a matter template for resolving the matter in an organized way. When you apply a legal matter template while creating a matter, the associated phases from the template are added by default to the matter.
-   **[Create a task template within a phase template](create-task-template-for-matter-phase-template.md)**  
Create a task template within a phase template of a legal matter template. When you apply a legal matter template while creating a matter, the associated phases and tasks from the template are added by default to the matter.

**Parent Topic:**[Legal matter templates](../concept/legal-matter-administration.md)

