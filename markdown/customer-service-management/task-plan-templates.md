---
title: Task Plan Templates
description: Use a task plan template to define the repeatable tasks and records that must be created for a business process. When the template is applied, these tasks and records are automatically created.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Task Plan Templates

Use a task plan template to define the repeatable tasks and records that must be created for a business process. When the template is applied, these tasks and records are automatically created.

![The template items list includes a hierarchical list of the tasks, child, cases, records, and other items that are part of the template.](../image/task-plan-template-items-list.png "Template items list for a task plan template")

A [task plan template](../task/create-task-plan-template.md) is a group of tasks and records, called template items, that are automatically created when the template is applied. A task plan template also includes conditions that determine when the template is applicable.

A [template item](../task/create-task-plan-template-item.md) can be a task, a record, or a child task. When you create a template item, you identify the type of item to be created by selecting the table where that item is to be created. For example, to create a case task, select the Task \[sn\_customerservice\_task\] table. For each template item, you can create [conditions](../task/create-task-plan-template-item-condition.md) that determine when the template item is created.

A [task plan template configuration](../task/task_plan_template_configurations.md) defines pre-set fields to streamline the process of creating task plan templates.

You can also create a hierarchy of the tasks and records to be created when the task plan template is applied by creating [child template items](../task/create-task-plan-template-child-item.md) for a template item. For example, you can create a template item that is a case record and then create child template items that are case tasks for that case record.

## Defining a process with a task plan template

Business users can define how a business process should be handled by using a task plan template. When creating a task plan template, the business owner can create the following:

-   The task plan template and the conditions for when the template applies.
-   The template items to be generated. This can include tasks, child cases, child case tasks, and other records such as work order tasks. Template items can also include attachments. These attachments are available on the tasks created from the template items.
-   The task order.
-   Conditions that specify when tasks must be created.

## Benefits of task plan templates

Task plan templates enable you to define the repeatable tasks that are routinely performed for specific business processes. When you apply the template, either to an existing case or to a new case, the system automatically creates the tasks defined in the template.

For example, a bank can use a task plan template to onboard new customers. An onboarding task plan template can include tasks similar to the following:

-   Gather customer information
-   Scan customer documents
-   Check customer credit score
-   Send welcome packet

## Task Plan Templates plugin

Users with the system administrator role can activate the Task Plan Templates \(com.sn\_task\_plan\_templates\) plugin. The Task Plan Templates application is available from the ServiceNow Store.

The Task Plan Templates application adds the Task Plan Templates module to the application navigator and includes tables and roles. For more information, see the following topics:

-   [Task Plan Templates tables](task-plan-templates-tables.md)
-   [Task Plan Templates roles](task-plan-templates-roles.md)

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Creating task plan templates

A business process owner can create a task plan template by following these steps.

<table id="table_p2k_vsl_rfc"><thead><tr><th>

Step

</th><th>

Explanation

</th></tr></thead><tbody><tr><td>

[Create a task plan template](../task/create-task-plan-template.md).

</td><td>

Create the template and set the conditions as to when the template applies.-   The template functions as a container or group of template items.
-   The template identifies a plan to apply the associated template items.

</td></tr><tr><td>

[Create one or more template items](../task/create-task-plan-template-item.md).

</td><td>

Create the template items to include in the task plan template. These items can be tasks, child cases, or child case tasks.-   Template items are the tasks or records that are to be created when the template is applied.
-   Template items can be used to define a hierarchy of parent and child entities of any task type.

</td></tr><tr><td>

[Create conditions for template items](../task/create-task-plan-template-item-condition.md).

</td><td>

Set conditions as needed for each of the template items that identifies when a template item should be created.

</td></tr><tr><td>

Publish the task plan template.

</td><td>

While in the Draft state, you can make changes to the template, template items, and template item conditions.Publish the task plan template to apply it to cases and case types.

To publish a task plan template, select **Publish** on the Task Plan Template form.

</td></tr></tbody>
</table>## Editing task plan templates

Once you create a task plan template, you can edit the template, the template items, and the template item conditions.

<table id="table_l2c_zzp_sfc"><thead><tr><th>

Step

</th><th>

Explanation

</th></tr></thead><tbody><tr><td>

[Clone a task plan template](../task/clone-task-plan-template.md).

</td><td>

Clone a task plan template that is in either the Draft or Published state.Select the task plan template number from a task plan template list. Then select **Clone**.

The system clones the task plan template, gives it a unique record number, and opens the cloned template in a new tab. The cloned template is also added to the task plan template list.

</td></tr><tr><td>

[Clone a template item](../task/clone-task-plan-template-item.md).

</td><td>

Clone a template item for a task plan template that is in the Draft state.Select a task plan template, select a template item in the Template Items tab, and then select **Clone** on the Template Item form.

The system creates a copy of the selected template item, gives it a unique record number, and displays the Template Item form.

</td></tr><tr><td>

Edit a task plan template.

</td><td>

Edit a task plan template that is in the Draft state.-   Select the task plan template number from a task plan template list to open the record in a tab.
-   Select the pencil icon next to the task plan template number to edit the form in a panel.

Make the necessary changes and then select **Save** or **Update**.

</td></tr><tr><td>

Edit a template item.

</td><td>

Edit a template item for a task plan template that is in the Draft state.-   Select the template item number from the Template Items list to open the record in a tab.
-   Select the pencil icon next to the template item number and edit the form in a panel.

Make the necessary changes and then select **Save** or **Update**.

</td></tr></tbody>
</table>## Applying task plan templates

You can apply task plan templates to existing cases or to new cases. When a case is created based on a task plan template, the template items are automatically created as defined in the template.

Task plan templates can be applied manually or automatically to an existing entity.

## Get Started tab in the contextual side panel

The Get Started tab in the contextual side panel in CSM Configurable Workspace displays information about task plan templates, template items, and template item conditions.

This tab is available for the following tables:

-   [Task Plan Template](../reference/task-plan-template-form.md) \[sn\_task\_plan\_template\]
-   [Template Item](../reference/task-plan-template-item-form.md) \[sn\_task\_plan\_template\_item\]
-   [Template Item Condition](../reference/task-plan-template-item-condition-form.md) \[sn\_task\_plan\_template\_item\_condition\]

<table id="table_dly_ysr_qfc"><thead><tr><th>

Content

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Task plan template

</td><td>

A reusable framework that you can use to define and generate a sequence of tasks.Use a task plan template to define tasks and the conditions under which those tasks must be created.

</td><td>

A bank that is onboarding a new client can use a task plan template to define tasks such as identity verification, AML checks, document collection, and account setup. Those tasks can then be automatically created for onboarding cases.

</td></tr><tr><td>

Template item

</td><td>

A task or a record, such as a case or child case, that is created for a task plan template.Each template item represents a specific task that needs to created when a task plan template is applied.

A template item can include conditions and predefined data that is used during task creation.

</td><td>

An onboarding task plan template can include template items such as the following:-   Perform anti-money laundering \(AML\) task
-   Send welcome packet

</td></tr><tr><td>

Template item conditions

</td><td>

Conditions that determine if a task should be created when the task plan template is executed.The conditions run against the template item's table. If all conditions return as true, then the task gets created.

</td><td>

A template item to "Send welcome packet" can include a condition such as "If applicant address is not empty."Based on this condition, if the applicant has provided an address, a 'Send welcome packet" task would be created.

</td></tr></tbody>
</table>