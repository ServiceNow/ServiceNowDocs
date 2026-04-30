---
title: Configuring work order templates
description: Work order templates allow you to quickly create well-defined work orders.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring work orders, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Configuring work order templates

Work order templates allow you to quickly create well-defined work orders.

These templates automatically create tasks and part requirements on work orders for common activities, such as password reset or memory upgrades. Work order templates and work order task templates are added to the product catalog when the Field Service Management plugin is activated.

You can enable the advanced configurations for work order templates by activating the Template Management for Field Service plugin \(com.snc.fsm\_template\_management\). Activation of this plugin adds the source table mapping, attribute mapping, work order task templates, and work order templates to the product catalog that helps configure the template to work dynamically. For more information, see [Configuring Template Management for Field Service](../../field-service-management/concept/enabling-advanced-configurations-for-wo-template.md).

Users with the wm\_admin or model\_manager role can create, edit, and delete work order templates and work order task templates.

When you create a template, you can use knowledge articles for a work order or work order tasks. You can then add Contextual Search to the knowledge article. Contextual Search helps you to create, or work on, a task with relevant knowledge articles based on the content of the task.

-   Define Search Fields: Specify the criteria to be used to search across your desired content sources.
-   Work Order Form: Add the contextual search results field to the Work Order form. Configure the form and add the **Contextual Search Results** field to your desired location on the form.
-   Work Order Task Form: Add the contextual search field to the Work Order Task form. Configure the form and add the **Contextual Search Results** field to your desired location on the form.
-   Article Attachment field: Set the field where the knowledge article will be attached. Configure the **glide.knowman.attach.fields** property to include **work\_notes** field.

## Configuration overview

The steps for setting up work order templates are:

1.  [Create a work order template](../task/t_CreateAWorkOrderTemplate.md)

    Use work order templates populate work orders with repeatable information. For example, templates can populate an Assignment group, during the template creation process. This ensures consistent information is included across all related records.

2.  \(Optional\) [Create a knowledge article for a work order template](../task/t_CreateAKnowledgeArticle.md)

    Help Field Service technicians stay consistent when completing the same types of work orders. For example, a knowledge article can be installation guides, maintenance procedures, or checklists.

3.  \(Optional\) [Manage a work order SLA](../../planning-and-policy/task/t_ManageAWorkOrderSLA.md)

    Use work order SLAs help ensure SLAs are met in time. Work order SLAs can be viewed or managed from the work order or work order task form so they're easy to access.


**Related topics**  


[Prepare work orders](../../field-service-management/concept/preparing-work-orders.md)

[Manage work order tasks](../../planning-and-policy/concept/c_WorkOrderTasks.md)

[Apply a work order template](../task/t_UseTheWorkOrderTemplate.md)

[Assign a knowledge article to a work order or work order task](../../field-service-management/task/add-knowledge-workorder.md)

