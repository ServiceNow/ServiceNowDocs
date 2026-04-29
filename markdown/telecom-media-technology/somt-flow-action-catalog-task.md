---
title: Task plan templates driven order fulfillment
description: Use the task plan template to define tasks and their dependencies that are needed to orchestrate the fulfillment journey for a product to standardize fulfillment processes across products.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Sales and Order Management for Telecommunications \(SOMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# Task plan templates driven order fulfillment

Use the task plan template to define tasks and their dependencies that are needed to orchestrate the fulfillment journey for a product to standardize fulfillment processes across products.

A no-code approach in ServiceNow® that allows you to create task orchestration workflows using task plan templates. It as an alternative to flow designer, giving more options for implementing product configurations.

For more information about Flow actions for fulfillment subflow definition, see [Flow actions for fulfillment subflow definition](https://www.servicenow.com/docs/access?context=order-mgt-flow-actions-fulfillment-subflows&version=australia&pubname=australia-order-management&ft:locale=en-US).

When the template is configured for a specification, the out of box logic, on domain order creation automatically searches for a matching template, based on the task's specification and action of domain order. When a template match is found, the template is applied to generate the order tasks under the domain order. To learn more about task plan template, see [Task plan templates](https://www.servicenow.com/docs/access?context=task-plan-templates&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

## Benefits of task plan template

It enables non-technical users to do the following:

-   Define fulfillment journeys.
-   Manage task dependencies for simple task creation without developer involvement.
-   Reduce IT dependency.
-   Accelerate deployment of new offerings.

## Create a task plan template

You can create a task plan template by following these steps.

<table id="table_xq4_wp2_k3c"><thead><tr><th>

Step

</th><th>

Explanation

</th></tr></thead><tbody><tr><td>

[Create a task plan template](https://www.servicenow.com/docs/access?context=create-task-plan-template&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

</td><td>

Create the template and set the conditions as to when the template applies.-   The template functions as a container or group of template items.
-   The template identifies a plan to apply the associated template items.

</td></tr><tr><td>

[Configure task plan template](../task/configure-task-plan-template.md)

</td><td>

To add conditions to a template item that determines when a template item is applicable.

</td></tr><tr><td>

[Create one or more template items](https://www.servicenow.com/docs/access?context=create-task-plan-template-item&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

</td><td>

Create the template items to include in the task plan template. These items can be tasks, child cases, or child case tasks.-   Template items are the tasks or records that are to be created when the template is applied.
-   Template items can be used to define a hierarchy of parent and child entities of any task type.

</td></tr><tr><td>

[Create conditions for template items](https://www.servicenow.com/docs/access?context=create-task-plan-template-item-condition&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

</td><td>

Set conditions as needed for each of the template items that identifies when a template item should be created.

</td></tr><tr><td>

[Task dependencies for task plan templates](https://www.servicenow.com/docs/access?context=task-dependencies-for-task-plan-templates&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

</td><td>

It provides controlled sequencing within the generated records from the template items in the Task Plan Template Dependency table. By defining predecessor and successor relationships, the tasks can start at correct time reducing ambiguity for agents.

</td></tr><tr><td>

Publish the task plan template.

</td><td>

While in the Draft state, you can make changes to the template, template items, and template item conditions.

 It allows to publish if the same condition template is not available.

 Publish the task plan template to apply it to cases and case types.

 To publish a task plan template, select **Publish** on the Task Plan Template form.

</td></tr></tbody>
</table>