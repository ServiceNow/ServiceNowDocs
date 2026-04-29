---
title: Configuring work orders
description: Field Service Management uses a task-driven process, wherein each work order encapsulates a list of essential tasks. Upon the creation of a work order, a corresponding task record is instantly generated. Task-driven processing can provide structure and clarity for intricate projects.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up work orders and tasks, Configure, Field Service Management]
---

# Configuring work orders

Field Service Management uses a task-driven process, wherein each work order encapsulates a list of essential tasks. Upon the creation of a work order, a corresponding task record is instantly generated. Task-driven processing can provide structure and clarity for intricate projects.

Work orders are the driving force behind Field Service Management. They define what Field Service agents must do to complete their jobs.

Work orders follow a specific life cycle and move through a series of states. The states can vary based on your configuration. For example, if you want to qualify work orders before they're assigned, then you can enable qualification. Qualification adds the Awaiting Qualification and Qualified work order states. For more information, see [Work order states](work-order-states.md).

Each work order requires at least one task, with the option to add more to cover all facets of the request. While tasks can be assigned to different groups and operate autonomously from the main work order request, the progression and completion of these tasks influence the overall state of the parent work order.

Preconfigured example work orders are included with the Field Service Management Demo Data plugin \(com.sng work management.demo\).

## Configuration overview

Optionally, set up one or more work order configurations.

-   [Configuring work order templates](../../it-services/concept/c_WorkOrderTemplates.md)

    Use templates to populate fields on a work order. For example, if you regularly add certain skills or parts to work orders, you can use templates to add those fields faster.

-   [Configure the qualification state for work orders](../task/configure-qualify-fsm.md)

    Allow for a quality check to make sure that the work order meets a certain standard before it moves to the next step.

-   [Customizing state flows](work-order-state-custom.md)

    Customize state flows to replace the standard process that controls how requests and their associated tasks move between states. This can be helpful if you need to add, remove, or change the states that work orders follow.

-   [Configuring Template Management for Field Service](enabling-advanced-configurations-for-wo-template.md)

    Provide advanced configurations for work order templates that enable the templates to work dynamically while creating a work order.

-   [Signed PDF summaries for closed work orders](work-order-sign-and-confirm-pdf.md#)

    Allow customers to digitally sign a PDF, and confirm that work orders are closed. A summary of the work order is created that includes the completed tasks, parts used and returned, incidental expenses, and the time required to complete the work.


